---
title: Üks kanne
description: Ühe kandega finantstöölehtede jaoks (üldine tööleht, põhivara tööleht, hankija maksete tööleht jne) saate sisestada mitu alampearaamatu kannet ühes kandes.
author: kweekley
manager: AnnBe
ms.date: 11/05/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerParameters, AssetProposalDepreciation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 8.0.2
ms.openlocfilehash: 68ec3cb028462865e914cbcb25ff28dbaf9a4f01
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442421"
---
# <a name="one-voucher"></a>Üks kanne

[!include [banner](../includes/banner.md)]


## <a name="what-is-one-voucher"></a>Mis on funktsioon Üks kanne?

Olemasoleva funktsiooniga finantstöölehtede jaoks (üldine tööleht, põhivara tööleht, hankija maksete tööleht jne) saate sisestada mitu alampearaamatu kannet (klient, hankija, põhivara, projekt ja pank) ühes kandes. Microsoft nimetab seda funktsiooni *Üheks kandeks*. Saate ühe kande loomisel kasutada üht järgmistest viisidest.

- Seadistage töölehe nimi (**Pearaamat** \> **Töölehe seadistus** \> **Töölehe nimed**), nii et välja **Uus kanne** väärtus oleks **Ainult üks kande number**. Iga töölehele lisatud rida lisatakse nüüd samale kandele. Seetõttu saab kande sisestada mitmerealise kandena, konto/vastaskonto samal real või kombinatsioonina.

    [![Üks rida](./media/same-line.png)](./media/same-line.png)

    > [!IMPORTANT]
    > Sätte Üks kanne definitsioon **ei** kata juhtumeid, kus töölehe nimed seadistatakse valikule **Üks kande number**, kuid kasutaja sisestab seejärel kande, mis sisaldab ainult pearaamatukonto tüüpe. Selles teemas tähendab Üks kanne, et olemas on üks kanne, mis sisaldab rohkem kui üht hankijat, klienti, panka, põhivara või projekti.

- Sisestage mitmerealine kanne, kus vastaskonto puudub.

    [![Mitmerealine kanne](./media/Multi-line.png)](./media/Multi-line.png)

- Sisestage kanne, kus nii konto kui ka vastaskonto sisaldavad alampearaamatu konto tüüpi, näiteks **Hankija**/**Hankija**, **Klient**/**Klient**, **Hankija**/**Klient**, või **Pank**/**Pank**.

    [![Alampearaamatu kanne](./media/subledger.png)](./media/subledger.png)

## <a name="issues-with-one-voucher"></a>Ühe kande probleemid

Ühe kande funktsioon tekitab probleeme tasakaalustamise, maksuarvestuse, kande tühistamise, alampearaamatu ja pearaamatu vastavusseviimise, finantsaruandluse ja muu ajal. (Lisateavet probleemide kohta, mis tekivad tasakaalustamise ajal, vt näiteks jaotisest [Üksik mitme kliendi- või hankijakirjega kanne](https://docs.microsoft.com/dynamics365/finance/accounts-payable/single-voucher-multiple-customer-vendor-records).) Õigeks toimimiseks ja aruandluseks on nende protsesside ja aruannete jaoks vaja kande üksikasju. Kuigi mõni stsenaarium võib olenevalt organisatsiooni seadistusest siiski õigesti toimida, esineb sageli probleeme, kui ühte kandesse sisestatakse mitu kannet.

Näiteks sisestate järgmise kande.

[![Näide](./media/example.png)](./media/example.png)

Seejärel loote aruande **Kulud hankija järgi** tööruumi **Finantsülevaated**. Selles aruandes grupeeritakse kulukonto saldo hankijagrupi ja seejärel hankija järgi. Kui aruanne on loodud, ei suuda süsteem määrata, millised hankijagrupid/hankijad sisestasid kulu 250.00. Kuna kande üksikasjad on puudu, eeldab süsteem, et kogu 250.00 kulu on sisestanud esimene kandes leiduv hankija. Seega kuvatakse see 250.00 kulu, mis sisaldub põhikonto 600120 saldol, selle hankijagrupi/hankija all. Kuid on väga tõenäoline, et kande esimene hankija ei ole õige hankija. Seetõttu on aruanne ilmselt vale.

[![Kulud](./media/expenses.png)](./media/expenses.png)

## <a name="the-future-of-one-voucher"></a>Ühe kande tulevik

Ülaltoodud probleemide tõttu aegub ühe kande funktsioon. Kuid kuna on olemas sellest funktsioonist olenevad funktsionaalsed vahemikud, ei aegu funktsioon ühekorraga. Selle asemel kasutatakse järgmist graafikut.

- **Kevad 2018 väljaanne** – funktsioon lülitatakse vaikimisi välja parameetri **Luba ühe kande raames mitu kannet** kaudu **Üldisel** vahekaardil **Pearaamatu parameetrite** lehel. Saate funktsiooni siiski sisse lülitada, kui teie organisatsioonil on stsenaarium, mis langeb selles teemas allpool loetletud funktsionaalsuse vahemikku.

    - Kui klienntidel on ettevõttestsenaarium, milleks pole üht kannet vaja, ei ole vaja funktsionaalsust sisse lülitada. Microsoft ei paranda vigu aladel, millest räägitakse selles teemas allpool, kui seda funktsiooni kasutatakse, kuigi olemas on muu lahendus.
    - Lõpetage ühe kande kasutamine integratsioonidele, v.a juhul, kui vajate seda funktsiooni mõne funktsionaalse vahemiku jaoks.

- **Hilisemad väljaanded** – täidetakse kõik funktsionaalsed vahemikud. **Pärast funktsionaalsete vahemike täitmist ja uute funktsioonide tarnimist kulub Ühe kande funktsionaalsuse jäädava väljalülitamiseni vähemalt üks aasta**, sest klientidele ja sõltumatutele tarkvaratarnijatele (ISV) peab jääma piisavalt aega uutele funktsionaalsustele reageerimiseks. Näiteks võib neil olla vaja värskendada oma äriprotsesse, üksuseid ja integratsioone.

> [!IMPORTANT]
> Suvandit **Ainult üks kande number** **ei ole** töölehe nime seadistustest eemaldatud. Seda suvandit toetatakse endiselt, kui kanne sisaldab ainult pearaamatukonto tüüpe. Kliendid peavad selle sätte kasutamisel olema ettevaatlikud, sest kannet ei sisestata, kui nad kasutavad suvandit **Ainult üks kande number**, kuid sisestavad rohkem kui ühe kliendi, hankija, panga, põhivara või kliendi. Lisaks saavad kliendid endiselt sisestada erinevate alampearaamatu tüüpide kombinatsiooni, nagu makse ühes kandes, mis sisaldab **Hankija**/**Pank** kontotüüpe.

## <a name="why-use-one-voucher"></a>Miks kasutada üht kannet?

Klientidega peetud vestluste põhjal on Microsoft koostanud järgmise loendi stsenaariumidest, kus kliendid kasutavad ühe kande funktsioonid, ja põhjustest, miks nad neid kasutavad. Mõnda neist ärivajadustest on võimalik täita vaid ühe kande funktsiooni kasutades. Kui paljude stsenaariumide korral võivad alternatiivsed lahendused vastata samadele ärivajadustele.

### <a name="scenarios-that-require-one-voucher"></a>Stsenaariumid, mille jaoks on vaja ühe kande funktsiooni

Järgmiseid stsenaariume on võimalik täita ainult ühe kande funktsiooni kasutades. Kui teie organisatsioonil on mõni neist stsenaariumitest, peate lubama mitme kande sisestamist ühte kandesse, muutes parameetrit **Luba ühe kande raames mitu kannet** lehel **Pearaamatu parameetrid**. Need funktsionaalsed vahemikud täidetakse teiste funktsioonidega hilisemates väljaannetes.

> [!Note]
> [Iga järgneva stsenaariumi jaoks peab väli **Luba ühe kande raames mitu kannet** olema määratud väärtusele „Jah” kiirkaardil **Üldine** lehel **Üldised pearaamatu parameetrid**.]

### <a name="post-vendor-or-customer-payments-in-summary-form-to-a-bank-account"></a>Hankija või kliendi maksete sisestamine pangakonto kokkuvõttevormi

**Stsenaarium** Organisatsioon edastab loendi hankijate ja summadega pangale ning pank kasutab seda loendit hankijatele organisatsiooni nimel maksmiseks. Pank sisestab maksete summa pangakontole üksiku tagastusena.

Hankija maksete summeerimist toetatakse vaid ühe kande funktsiooni kaudu. Iga hankija sisestatakse eraldi reana, et säilitada ostureskontro alammooduli üksikasjad. Kuid kõikide maksete koondsumma tasaarvestatakse pangakonto ühe reaga. Seetõttu on tagastus panga alampearaamatus näidatud ühe koondsummana.

**Stsenaarium** Organisatsioon hoiustab kliendimakseid või pank hoiustab kliendimakseid organisatsiooni nimel ja deposiit kuvatakse pangakontol tervikväljamaksena.

Kliendimaksete summeerimist toetab tavaliselt hoiustamise funktsioon. Kuid kui kasutate makseviisil vahekontot, toetatakse seda stsenaariumi vaid ühe kande funktsiooni kaudu. Kliendimaksed sisestatakse sama moodi, nagu on kirjeldatud hankija maksete summeerimise kohta.

### <a name="mechanism-to-group-transactions-from-a-business-event"></a>Ärisündmuse kannete grupeerimise mehhanism

**Stsenaarium** Organisatsioonil on üks ärisündmus, mis käivitab mitu kannet. Kuid raamatupidamisosakond soovib paremaks auditeerimiseks vaadata raamatupidamiskirjeid koos.

Kui organisatsioon peab vaatama ärisündmuse raamatupidamiskirjeid koos, tuleb kasutada ühe kande funktsiooni. 

### <a name="country-specific-features"></a>Riigikohased funktsioonid

**Stsenaarium** Ühtse haldusdokumendi (SAD) funktsioon Poola jaoks nõuab praegu üksiku kande kasutamist. Kui selle funktsiooni jaoks on saadaval rühmitamisvalik, peate edasi kasutama ühe kande funktsiooni. Võib olla vee riigikohaseid funktsioone, mis nõuavad ühe kande funktsiooni.

### <a name="customer-prepayment-payment-journal-that-has-taxes-on-multiple-lines"></a>Kliendi ettemakse tööleht, millel on maksud mitmel real

Selles stsenaariumis on ühe kande kliendid üks ja sama klient, sest kanne simuleerib kliendi tellimuse ridu. Ettemakse tuleb sisestada ühte kandesse, kuna maksuarvestus tuleb teha kliendi tehtud üksiku makse ridades.

### <a name="customer-reimbursement"></a>Kliendi tagasimakse

**Stsenaarium** Klient teeb tellimusele ettemakse ja tellimuse ridades on eri maksud, mis tuleb ettemakse jaoks salvestada. Ettemakse kliendi makse on üks kanne, mis simuleerib tellimuse ridu, nii et iga rea summale saab salvestada sobiva maksu.

Kui korvamise perioodiline ülesanne käivitatakse Müügireskontro mooduli, loob see kande, et viia saldo kliendilt hankijale. Selles stsenaariumis tuleb kliendile tagasi maksmiseks kasutada Ühe kande funktsiooni.

### <a name="fixed-asset-maintenance-catch-up-depreciation-split-asset-calculate-depreciation-on-disposal"></a>Põhivara hooldus: järelkulum, vara tükeldamine, likvideerimise kulumi arvutamine
Järgmised põhivara kanded loovad samuti ühes kandes mitu kannet.

- Varale tehakse täiendav soetamine ja arvutatakse järelkulum.
- Vara tükeldatakse.
- Likvideerimise kulumi arvutamiseks kasutatav parameeter on sisse lülitatud ja vara likvideeritakse.
- Vara teenuse kuupäev on enne soetamiskuupäeva. Seega sisestatakse kulumi korrigeerimine.

> [!Note]
> Kannete sisestamisel veenduge, et kõik kanded oleksid seotud sama põhivaraga. Kannet ei sisestata, kui see hõlmab rohkem kui ühte põhivara, isegi kui väli **Uus kanne** on määratud pearaamatu lehel **Töölehe nimed** valikule Ainult üks kande number. Kui kaasate kandesse rohkem kui ühe põhivara, kuvatakse teade **Kandel võib olla ainult üks põhivarakanne** ja te ei saa kannet sisestada.  

### <a name="bills-of-exchange-and-promissory-notes"></a> Käskveksel ja võlatähed
Käskvekslid ja võlatähed nõuavad Ühe kande kasutamist, sest kanded viivad kliendi või hankija saldo ühelt Müügireskontro/ostureskontro pearaamatukontolt teisele, olenevalt makse olekust.

## <a name="scenarios-that-dont-require-one-voucher"></a>Stsenaariumid, mille jaoks ei ole vaja ühe kande funktsiooni

Järgmisi stsenaariume on võimalik teha muude vahenditega ja nende jaoks ei pea kasutama Ühe kande funktsiooni.

### <a name="post-customer-payments-in-summary-form-to-the-bank-account"></a>Kliendimaksete sisestamine pangakonto kokkuvõttevormi

Organisatsioon hoiustab kliendimakseid või pank hoiustab kliendimakseid organisatsiooni nimel ja deposiit kuvatakse pangakontol tervikväljamaksena.

Kliendimaksete summeerimist toetatakse hoiustamise funktsiooni kaudu, kui makseviisis ei kasutata "vahekontot".

### <a name="netting"></a>Tasaarveldus

Tasaarvelduses tasaarveldatakse hankija ja kliendi saldod üksteisega, kuna hankija ja klient on üks ja sama osapool. See lähenemine vähendab rahavahetust organisatsiooni ja kliendi/hankija osapoole vahel.

Tasaarveldust saab teha, sisestades suurenemise ja vähenemise eraldi kannetesse ning sisestades seejärel tasaarvelduse pearaamatukontole tasakaalustuse.

### <a name="post-in-summary-to-the-general-ledger"></a>Koondsisestamine pearaamatusse

Organisatsioonid soovivad sageli pearaamatusse sisestada koondvormis, et vähendada andmete hulka. Kuid tavaliselt on nendel organisatsioonidel siiski vaja, et kande üksikasjad jääks alles. Kui koondvormis sisestamine läbi ühe kande on tehtud, ei ole kande üksikasjad teada ja neid ei saa säilitada.

- Kuna kande üksikasju ei saa praegu säilitada, soovitame organisatsioonidel Ühe kande funktsiooni koondvormis sisestamiseks **mitte** kasutada.
- Kui Ühe kande tugi eemaldatakse, saab töölehtedele juurutada lähtedokumendi ja raamatupidamise raamistikud. Need raamistikud säilitavad siis kande üksikasjad ja toetavad summeerimist pearaamatusse.


### <a name="settle-multiple-unposted-payments-to-the-same-invoice"></a>Mitme sisestamata makse tasakaalustamine samale arvele

See stsenaarium esineb enamasti organisatsioonides, kus kliendid saavad ostude eest maksmiseks kasutada mitut makseviisi. Selles stsenaariumis peab organisatsioon suutma salvestada mitut sisestamata makset ja tasakaalustama neid kliendiarve suhtes.

Uue funktsiooniga, mis lisati rakenduse Microsoft Dynamics 365 for Operations versioonile 1611 (november 2016), saab mitut sisestamata makset tasakaalustada ühe arve suhtes. Mitut kliendimakset pole enam vaja sisestada ühte kandesse.

### <a name="import-bank-statement-transactions"></a>Pangaväljavõtte kannete importimine

Pangad teevad sageli makseid ja võtavad makseid vastu organisatsiooni nimel ning need kanded salvestatakse rakendusse Finance pangalt saadud faili kaudu. Organisatsioonid soovivad sageli neid kandeid kokku rühmitada, kasutades pangaväljavõtte numbrit failis. Kuna iga kanne on pangaväljavõttel üksikasjalikult esitatud, ei ole summeerimine panga alampearaamatus vajalik.

Kandeid saab rühmitada, kasutades töölehe muid välju, näiteks töölehe partiinumbrit või dokumendinumbrit.


### <a name="transfer-balances"></a>Kanna saldod üle

Organisatsioonil võib olla vaja üle kanda saldo ühelt hankijalt teisele hankijale kas vea tõttu või kuna teine hankija on kohustuse üle võtnud. Seda tüüpi ülekanded esinevad ka selliste kontotüüpide nagu **Klient** ja **Pank** kohta.

Saldo ülekandeid ühelt kontolt (hankija, klient, pank jne) teisele kontole saab teha eraldi kannete kaudu ning tasaarvelduse pearaamatukontole saab sisestada tasakaalustuse.

### <a name="enter-beginning-balances"></a>Algsaldode sisestamine

Organisatsioonid sisestavad sageli alampearaamatu kontodele (hankija, kliendi-, põhivarakontodele jne) algsaldosid ühe kandena. Iga alampearaamatu konto algsaldosid saab sisestada eraldi kannetena ja tasaarvelduse pearaamatukontole saab sisestada tasakaalustuse.

### <a name="correct-the-accounting-entry-of-a-posted-customer-or-vendor-document"></a>Sisestatud kliendi- või hankija dokumentide raamatupidamiskirje parandamine

Organisatsioonil võib olla vaja parandada sisestatud arve raamatupidamiskirje müügireskontro või ostureskontro pearaamatukontot, aga seda arvet ei saa tühistada või parandada teise mehhanismi kaudu.

Kui parandus on vaja teha Müügireskontro või Ostureskontro pearaamatukontole, tuleb korrigeerida otse pearaamatukontot. Korrigeerida ei saa, sisestades hankija või kliendi kaudu. See lähenemine nõuab, et korrigeerimine tehakse seisakuajal, kui pearaamatukonto lubab ajutiselt käsitsi sisestamist.

### <a name="the-system-allows-it"></a>„Süsteem lubab seda”

Organisatsioonid kasutavad sageli ühe kande funktsiooni lihtsalt seetõttu, et süsteem lubab neil seda kasutada, mõistmata selle mõju.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]