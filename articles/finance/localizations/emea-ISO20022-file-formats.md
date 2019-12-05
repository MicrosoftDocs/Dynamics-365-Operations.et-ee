---
title: ISO20022-failide importimine
description: Selles teemas selgitatakse ISO 20022 camt.054- ja pain.002-vormingus maksefailide importimist rakendusse Microsoft Dynamics 365 Finance.
author: neserovleo
manager: AnnBe
ms.date: 07/27/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, CustBankAccounts, VendPaymMode, VendBankAccounts
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Italy, Latvia, Lithuania, Norway, Poland, Spain, Sweden, Switzerland, United Kingdom
ms.author: v-lenest
ms.search.validFrom: 2017-06-01
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: b809ba8d92772d8f3f416d4854d4af322e6f954a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773427"
---
# <a name="import-iso20022-files"></a>ISO20022-failide importimine

[!include [banner](../includes/banner.md)]

Saate importida järgmistes vormingutes maksefaile.

 - **ISO20022 camt.054 kreeditaviis** – selles vormingus sissetulevate maksete importimine kliendi maksetöölehele.
 - **ISO20022 pain.002 oleku tagastus** ja **ISO20022 camt.054 deebetaviis** – neis vormingutes tagastusfailid saate importida AP maksekande töölehele.

## <a name="prerequisites-for-importing-the-camt054-credit-advice-file"></a>Eeltingimused camt.054-vormingus kreeditaviisi faili importimiseks
Pangateatiste importimiseks vormingus camt.054.001.002 kliendi maksetöölehele peate täitma järgmised eeltingimused.

1. Importige **ISO20022 camt.054** elektroonilise aruandluse konfiguratsioon teenusest Microsoft Dynamics Lifecycle Services (LCS). Seejärel valige see konfiguratsioon lehe **Kliendi makseviis** väljal **Impordivormingu konfiguratsioon**. Lisateavet vaadake jaotisest [Makseviiside failivormingud](emea-select-file-formats-for-the-method-of-payments.md).
2. Sisestage lehel **Kõik kliendi** iga kliendi nimi ja organisatsiooni number.
3. Seadistage lehel **Kliendi pangakonto** kliendi pangakonto kirje, sisestades järgmise teabe: IBAN või pangakonto number ja SWIFT-kood või protsessikood.
4. Seadistage lehel **Pangakontod** juriidilise isiku pangakontod, sisestades järgmise teabe: IBAN või pangakonto number, SWIFT-kood või protsessikood, valuuta ja aadress.

   > [!NOTE]
   > Kui kavatsete kasutada pangakonto täpsemat vastavusseviimist, valige kiirkaardil **Vastavusseviimine** suvandi **Pangakonto täpsem vastavusseviimine** sätteks **Jah**. Kui kavatsete vastavusse viia sisestamata imporditud maksed, valige suvandi **Kasuta elektrooniliste maksete kinnituseks pangaväljavõtteid** sätteks **Jah**.

5. Valikuline: saate seadistada lehel **Kandekoodide vastendamine** vastenduse failis olevate panga kandekoodide ja panga kandetüüpide vahel.
6. Kui fail sisaldab kandetasusid, mille soovite sisestada koos sissetuleva maksega, looge maksetasu lehel **Kliendi maksetasu**. Seejärel seostage maksetasu lehel **Makseviisid** maksetasu seadistuses määratud pangakontoga.
7. Kui imporditakse ESR-maksed ja need sisaldavad ISR-i viiteid (kohaldub Šveitsi juriidilistele isikutele), tehke järgmine seadistus.

    - Sisestage väljal **Kliendi maksed, konto pikkus** ISR-i viidetes või kliendi automaatseks tuvastamiseks kasutatava kliendikoodi pikkus.
    - Veenduge, et kliendi number ja arve number (numbrijadad) koosneksid ainult numbritest. Need ei tohi sisaldada muid märke. Arve number ei tohi alata nulliga.
    - Sisestage juriidilise isiku pangakonto ESR, BESR ja protsessikood. Lisateavet vt teemast [ESR-i kliendimaksete importimine](emea-che-esr-customer-payments-import.md), kuna nõutavad on sarnased sätted.
    
## <a name="import-the-camt054-credit-advice-file-into-the-customer-payment-journal"></a>Camt.054 kreeditaviisi faili importimine kliendi maksetöölehele
1. Klõpsake lehel **Kliendi maksetöölehe read** suvandeid **Funktsioonid** > **Maksete importimine**.
2. Valige makseviis, millel on ISO20022 camt.054 vormingu jaoks vajalikud sätted.
3. Määrake nõutavad parameetrid ja faili tee, seejärel klõpsake **OK**. Fail imporditakse.

## <a name="prerequisites-for-importing-files-in-the-pain002-status-return-and-camt054-debit-advice-formats-into-the-ap-payment-transfer-journal"></a>Eeltingimused pain.002 oleku tagastuse ja camt.054 deebetaviisi vormingus failide importimiseks AP maksekande töölehele
Pangateatiste importimiseks järgmistes ISO20022 vormingutes lehele **Hankija makseülekanne** peate täitma järgmised eeltingimused: pain.002.001.003 oleku tagastuse teated ja camt.054.001.002 deebetaviis.

1. Importige **ISO20022 camt.054** ja **ISO20022 pain.002** ER-i konfiguratsioonid LCS-ist.
2. Valige lehe **Hankija makseviis** väljadel **Tagastusvormingu konfiguratsioon** ja **Tagastusvormingu teisene konfiguratsioon** imporditud ER-i konfiguratsioonid. Peate aktiveerima üldise elektroonilise tagastusvormingu valitud makseviisi jaoks.
3. Seadistage lehel **Tagastusvormingu oleku vastendamine** olekukoodide vastendus pain.002 olekute ja hankija maksetöölehe olekute vahel.

    Siin on näide oleku seadistamisest.

    Tagastuse olek | Makse olek
    --------------|---------------
    RJCT          | Tagasi lükatud
    ACCP          | Aktsepteeritud
    ACSP          | Vastu võetud

4. Seadistage lehel **Tagastusvormingu tõrkekoodid** pain.002 tõrkekoodid ja kirjeldused vastavalt välistele ISO20022 oleku põhjusekoodidele.

    Siin on näide tõrkekoodi seadistuse osast.

    Kood | Nimi
    -----|-----
    AC01 | IncorrectAccountNumber
    AC02 | InvalidDebtorAccountNumber
    AC03 | InvalidCreditorAccountNumber
    AC04 | ClosedAccountNumber
    AC05 | ClosedDebtorAccountNumber
    AC06 | BlockedAccount

5. Kui camt.054-fail sisaldab kandetasusid, mille soovite sisestada koos sissetuleva maksega, looge maksetasu lehel **Hankija maksetasu**. Seejärel seostage maksetasu lehel **Makseviisid** maksetasu seadistuses määratud pangakontoga.

## <a name="import-the-pain002-status-return-or-camt054-debit-advice-files-into-the-vendor-payment-journal"></a>Pain.002 oleku tagastuse või camt.054 deebetaviisi failide importimine hankija maksetöölehele
1. Avage menüüs Ostureskontro leht **Makseülekanded**.
2. Klõpsake lehel **Makseülekanded** suvandit **Tagastusfail – hankija**.
3. Valige makseviis, millel on ISO20022 failide jaoks vajalikud sätted, seejärel klõpsake **OK**.
4. Valige failivorming, mille plaanite importida, seejärel klõpsake **OK**.
5. Määrake nõutavad parameetrid ja faili tee, seejärel klõpsake **OK**.

Kui impordite pain.002-faili, värskendatakse hankija makseridade olekut imporditud failis oleva teabe põhjal.

Kui impordite camt.054-faili, peate määrama järgmised lisaparameetrid.

- **Tasu ID** – saate sisestada tasu ID, mis määratleb uued maksetasu read, mis luuakse hankija maksetöölehe real, kui tasu summa on camt.054-failis olemas.
- **Uue töölehe nime** ja **Uue töölehe kirjeldus** – saate sisestada töölehe nime ja kirjelduse, millele töödeldud kanded üle kantakse. Pärast ülekannet tuleb uuel töölehel määrata uued kandenumbrid.
- **Otsekorralduse kannete importimine** – seadke selle suvandi sätteks **Jah**, kui väljaminevad otsekorraldused tuleb importida hankija maksetöölehele.
- **Töölehe nimi** – saate määratleda imporditud otsekorralduse kannete jaoks uue töölehe nime.
- **Kannete tasakaalustamine** – seadke selle suvandi sätteks **Jah**, kui imporditud hankijamaksed tuleb süsteemis leitud arvetega tasakaalustada.

Saate vaadata imporditud teavet lehel **Makseülekanded**. 

## <a name="additional-details"></a>Täiendavad üksikasjad

LCS-ist vormingu konfiguratsiooni importimisel impordite kogu konfiguratsioonipuu, seega kaasatakse mudel ja mudeli vastendamise konfiguratsioonid. Alates 8. versioonist asuvad maksemudeli vastendamised lahenduspuu eraldiseisvates ER-konfiguratsioonides (makse mudeli vastendamine 1611, makse mudeli vastendamine sihtkohta ISO20022 jne). Ühe mudeli (maksemudeli) all on palju erinevaid maksevorminguid, mistõttu on mugava halduse huvides parim eraldi vastendamine. Näiteks saab kasutada ISO20022 makseid krediidiülekannete failide loomiseks ja seejärel pangast tagastusteadete importimiseks. Sel juhul peaks kasutama järgmiseid konfiguratsioone.

 - **Maksemudel**
 - **Makse mudeli vastendamine 1611** – vastendust kasutatakse eksportfaili loomiseks
 - **Makse mudeli vastendamine sihtkohta ISO20022** – konfiguratsioonis kasutatakse andmete importimiseks kõiki vastendusi ("sihtkohta" vastendamise suund)
 - **ISO20022 krediidiülekanne** – see konfiguratsioon sisaldab vormingu osa, mis vastutab makse mudeli vastendamise 1611 põhjal ekspordifaili loomise (pain.001)eest, ja mudeli vastendamise komponendi vormingut, mida kasutatakse koos makse mudeli vastendamisega sihtkohta ISO20022, et registreerida eksporditud maksed süsteemi edasise impordi eesmärgil (impordi CustVendProcessedPayments tehnilisse tabelisse).
 - **ISO20022 krediidiülekanne (CE)**, kus CE tähistab riigi laiend – ISO20022 krediidiülekandest tuletatud sama struktuuri ja teatud riigikohaste erinevustega vorming
 - **Pain.002** – seda vormingut kasutatakse koos makse mudeli vastendamisega sihtkohta ISO20022, et importida pain.002-fail hankija makseülekannete töölehele
 - **Camt.054** – seda vormingut kasutatakse koos makse mudeli vastendamisega sihtkohta ISO20022, et importida camt.054-fail hankija makseülekannete töölehele Sama vormingukonfiguratsiooni kasutatakse kliendimaksete impordi funktsiooni puhul, kuid konfiguratsiooni Maksemudeli vastendamine sihtkohta ISO20022 puhul kasutatakse teistsugust vastendamist.

Elektroonilise aruandluse kohta lisateabe saamiseks vaadake teemat [Elektroonilise aruandluse ülevaade](../../dev-itpro/analytics/general-electronic-reporting.md).

## <a name="additional-resources"></a>Lisaressursid
- [Hankijamaksete loomine ja eksportimine ISO20022 maksevormingu abil](./tasks/create-export-vendor-payments-iso20022-payment-format.md)
- [ISO20022 kreeditiülekande konfiguratsiooni importimine](./tasks/import-iso20022-credit-transfer-configuration.md)
- [ISO20022 otsekorralduse konfiguratsiooni importimine](./tasks/import-iso20022-direct-debit-configuration.md)
- [Ettevõtte pangakontode seadistamine ISO20022 kreeditkorralduste jaoks](./tasks/set-up-company-bank-accounts-iso20022-credit-transfers.md)
- [Ettevõtte pangakontode seadistamine ISO20022 otsekorralduste jaoks](./tasks/set-up-company-bank-accounts-iso20022-direct-debits.md)
- [Klientide ja kliendi pangakontode seadistamine ISO20022 otsekorralduste jaoks](./tasks/set-up-bank-accounts-iso20022-direct-debits.md)
- [Makseviisi seadistamine ISO20022 kreeditkorralduse jaoks](./tasks/set-up-method-payment-iso20022-credit-transfer.md)
- [Makseviisi seadistamine ISO20022 otsekorralduse puhul](./tasks/setup-method-payment-iso20022-direct-debit.md)
- [Hankijate ja hankija pangakontode seadistamine ISO20022 kreeditkorralduste jaoks](./tasks/set-up-vendor-iso20022-credit-transfers.md)
