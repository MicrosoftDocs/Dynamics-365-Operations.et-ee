---
title: Ostulepingud
description: Selles artiklis antakse teavet ostulepingute kohta. Ostuleping on leping, mis kohustab organisatsiooni ostma konkreetset kogust või kindlat summat, kasutades aja jooksul mitut ostutellimust. Selle kohustuse täitmise eest saab ostja erihindu ja allahindlusi.
author: kamaybac
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AgreementClassification, AgreementLine, AgreementLinePrompt, PurchAgreement, PurchAgreementCreate, PurchAgreementGenerateReleaseOrder, PurchAgreementHistory, PurchAgreementInvoiceJournal, PurchLine, AgreementLines
audience: Application User
ms.reviewer: kamaybac
ms.custom: 11634
ms.assetid: 8ac20adf-7412-4929-be8c-aaedf23a76ad
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: affbbf0666704b435c31cccdf8ed8205917e56bb64378aa856ad34134685f7f5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780170"
---
# <a name="purchase-agreements"></a>Ostulepingud

[!include [banner](../includes/banner.md)]

Selles artiklis antakse teavet ostulepingute kohta. Ostuleping on leping, mis kohustab organisatsiooni ostma konkreetset kogust või kindlat summat, kasutades aja jooksul mitut ostutellimust. Selle kohustuse täitmise eest saab ostja erihindu ja allahindlusi. 

Ostutellimused võivad kehtida konkreetsele tootekogusele, konkreetsele toote valuutasummale või konkreetsele toodete valuutasummale hankekategoorias. Ostulepingu hinnad ja allahindlused tühistavad mis tahes olemasolevates kaubanduslepetes määratud hinnad ja allahindlused.  

Lehel **Ostulepingud** saate luua, rakendada ja jälgida ostulepinguid, mis on sõlmitud teie organisatsiooni ja hankijate vahel. Näiteks pärast ostulepingu loomist saate otse sellest tellida. Igal ostulepingul on kehtivusperiood, mille on määranud ostulepingu loonud isik. Ostu tarnekuupäev peab jääma selle kehtivusperioodi jõustumiskuupäevade vahemikku.  

Pärast ostulepingu koostamist tuleb see aktiveerida, enne kui see jõustub. Ostulepingu aktiveerimiseks määrake valiku **Märgi lepe kehtivaks** olekuks **Jah**. 

Ostulepingu kasutamise ja kinnitamise vältimiseks märkige lepingu olekuks **Suletud**. Saate alati uuendada olekule **Kehtiv** mis tahes ajal pärast selle muudatuse tegemist.

## <a name="responsible-workers-on-purchase-agreements"></a>Vastutavad töötajad ostulepingutel

Saate tuvastada ostulepingu klassifikatsioonis peamise vastutava töötaja ja teisese vastutava töötaja. Need väärtused rakendatakse tulemiks saadud ostulepingus. Te ei pea vastutavaid töötajaid ostulepingusse lisama ja neid on võimalik ostulepingus endas juhtumipõhiselt muuta. Te ei saa määrata teisest vastutavat töötajat ilma esmase vastutava töötaja määramiseta, ehkki teil ei pea olema teisest vastutavat töötajat. Te ei saa määrata sama töötajat nii esmaseks kui ka teiseseks vastutavaks töötajaks.

> [!IMPORTANT]
> Enne vastutava isiku funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.
> 
> - **Moodul:** *hanked*
> - **Funktsiooni nimi:** *ostulepingu vastutav isik*

## <a name="commitment-types"></a>Kohustuse tüübid
Iga ostulepingu rida on kohustus midagi osta. Kohustuse täitmiseks saate kasutada mitme ostutellimuse (PO) ridu. On nelja tüüpi kohustusi.

-   **Toote koguse kohustus** – ostate konkreetse koguse tooteid.
-   **Toote väärtuse kohustus** – ostate konkreetse valuutasumma eest tooteid.
-   **Tootekategooria väärtuse kohustus** – ostate konkreetse valuutasumma eest hankekategoorias. Summa võib olla kataloogikauba või mittekataloogikauba kohta.
-   **Väärtuse kohustus** – ostate konkreetse valuutasumma eest mis tahes toote või tooteid mis tahes hankekategoorias.

## <a name="pricing-terms-for-purchase-agreements"></a>Ostulepingute hinnakujunduse tingimused
Hinnakujunduse tingimused võivad erineda olenevalt kohustuse tüübist. Ostulepingute hinnakujunduse tingimused tühistavad mis tahes muud hinnakujunduse tingimused, mis on kaubanduslepetes seadistatud. Järgmises tabelis kirjeldatakse hinnaga seotud välju, mida iga kohustuse tüüp mõjutab. Välju, mis sisaldavad valikut **Jah**, saab värskendada tellimuse real.

| Kohustuse tüüp                   | Ühiku hind | Hinnaühik | Allahindluse protsent | Skonto summa |
|-----------------------------------|------------|------------|------------------|----------------------|
| Toote koguse kohustus       | Jah        | Jah        | Jah              | Jah                  |
| Toote väärtuse kohustus          |            |            | Jah              |                      |
| Tootekategooria väärtuse kohustus |            |            | Jah              |                      |
| Väärtuse kohustus                  |            |            | Jah              |                      |

## <a name="policies-for-purchase-agreements"></a>Ostulepingute poliitikad
Järgmised poliitikad mõjutavad seda, kuidas ostulepingu kohustuse ja vastava ostutellimuse ridade vaheline seos toimib.

-   **Maksimum rakendatud** – kõikide tellimuse ridade koondkogus ega koondsumma ei või ületada seotud kohustuses määratud kogust ega summat.
-   **Hind ja allahindlus on fikseeritud** – tellimusereal olev hind ja seotud kohustuses olev hind peavad olema samad. Kui hinda tellimuse real muudetakse, on seos kohustusega katkestatud. Kui seos on katkenud, ei panusta tellimuse rida kohustuse täitmisse.
-   **Minimaalne väljastussumma ja maksimaalne väljastussumma** – kui summa on määratud, saate sõnumi, kui teete tellimusereal muudatuse, mille tagajärjel erineb tellimuserida seotud kohustusest.

## <a name="fulfillment-calculations-for-purchase-agreements"></a>Ostulepingute täitmise arvutused
Täitmise kogused ja summad on näidatud vahekaardil **Täitmine** kiirkaardil **Rea üksikasjad** lehel **Ostulepingud**.  

Alal **Täitmine** on näidatud järelejäänud summa või kogus, mida on kohustuse täitmiseks vaja.  

Alal **Leping** on näidatud koondkogus või koondsumma, mille puhul müügilepingu rida kehtib.  

Pääsete juurde ostutellimuse ridadele ja arveridadele, mis panustavad täitmise kalkulatsiooni, valides ridadel või ostulepingu päises tegevuse **Seotud teave**.

## <a name="confirmations-and-version-history-for-purchase-agreements"></a>Ostulepingute kinnitused ja versiooniajalugu
Kui kinnitate ostulepingu, salvestatakse ostulepingu praegune versioon ajalootabelisse. Kui muudate ostulepingut, saate selle uuesti kinnitada, et salvestada ajalukku ostulepingu teine versioon. Kui te ostulepingut ei kinnita, saate seda siiski ostutellimuste koostamiseks kasutada. Kuid ostulepingu ajaloo teavet ei salvestata. Saate kõiki lepingu versioone eelvaadata või printida. Seejärel saate parandusi kinnituse saamiseks oma hankijaga jagada.

## <a name="applying-purchase-agreements-in-the-ordering-process"></a>Ostulepingute kasutamine tellimisprotsessis
Ostutellimuse koostamisel saate sellele ostulepingu rakendada. Lepingu tingimustest pärinev teave (nt maksetingimused, tarnetingimused ja tarneaadress) kopeeritakse siis ostutellimuse päisesse. Kui ostutellimus sisaldab vähemalt ühte rida ostulepingus määratud toodete ja kategooriate kohta, kasutatakse nende ridade puhul ostulepingu hindu ja allahindlusi. Tellimuse real olev summa või kogus panustab ostulepingu kohustuse täitmisse. Sama ostutellimus võib sisaldada mõlemat rida, mis ei ole seotud ostulepinguga ja ridadega, millel on ostulepingu kohustus.  

Saate valida ostulepingu ainult ostutellimuse loomisel. Pärast ostutellimuse loomist ei saa ostulepingut valida.  
Mõnes olukorras, kus ostutellimused luuakse kaudselt, saate määrata, kas Supply Chain Management otsib kehtivaid ostulepinguid automaatselt. Näiteks võiksite seda teha, kui kinnitate automaatselt plaanitud ostutellimusi või loote ostutellimusi, mis põhinevad müügitellimustel.

## <a name="matching-policy-on-purchase-agreements"></a>Ostulepingute vastavusse viimise poliitika
Saate määratleda ostulepingu päises rea vastavusse viimise poliitika. See rea vastavusse viimise poliitika arvestab ostureskonto parameetrite rea vastavusse viimise poliitikaga, kui väli **Luba vastavusse viimise poliitika alistamine** lehel **Ostureskontro parameetrid** (kiirkaardil **Hinna ja koguse sobitamine**) on määratud valikule **Kõrgem kui ettevõttepoliitika**. Ostulepingule viitavad dokumendid kasutavad rea vastavusse viimise poliitikat, mis on määratletud ostulepingu päises, kui just vastava kauba, kauba ja hankija või kategooria ostupoliitika jaoks pole teisiti määratletud.

## <a name="purchase-agreements-and-intercompany-trade"></a>Ostulepingud ja kontsernisisene kaubandus
Kontsernisiseseid kaubandussuhteid saab luua erinevates juriidilistes isikutes olevate hankija kontode ja kliendi kontode vahel. Kui ühele osapoolele luuakse müügi- või ostutellimus, luuakse kontsernisisene tellimusahel. Tellimusahelas luuakse müügi- ja ostutellimus sobivates juriidilistes isikutes.  

Saate luua ostu- või müügilepingu ühele kontsernisisesele kaubandusosapoolele. Seejärel saate luua vastava müügi- või ostulepingu teisele kontsernisisesele kaubandusosapoolele muus juriidilises isikus.  

Kui loote kontsernisisese ostutellimuse, mis kasutab kontsernisisest ostulepingut ühes juriidilises isikus, kasutab vastav kontsernisisene müügitellimus vastavat kontsernisisest müügilepingut teises juriidilises isikus. Müügi- ja ostulepingute kohustuste täitmine on sünkroonitud, nagu ka kontsernisisesed müügi- ja ostutellimused.

## <a name="financial-dimensions-on-purchase-agreements"></a>Ostulepingute finantsdimensioonid
Saate kopeerida finantsdimensioonid dokumentide päistesse või ostutellimuse üksikutele ridadele. Kui muudate dimensioone lepingu päises või lepingu real, ei mõjuta muudatus ühtegi väljastatud tellimust, kuid kajastub kõigil uutel tellimustel.

## <a name="additional-resources"></a>Lisaressursid

- [Ostulepingu loomine](tasks/create-purchase-agreement.md)
- [Ostutellimuse loomisel rakendage ostulepingut](tasks/create-purchase-release-order-purchase-agreement.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]