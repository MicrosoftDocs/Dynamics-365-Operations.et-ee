---
title: Hankija arve automatiseerimine
description: "Selles teemas selgitatakse funktsioone, mis on saadaval hankija arvete täielikuks automatiseerimiseks, isegi manuseid sisaldavate arvete puhul."
author: twheeloc
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 5bfde00f88a12711c2519aaea19dd7a48196a828
ms.contentlocale: et-ee
ms.lasthandoff: 06/20/2017

---
# <a name="vendor-invoice-automation"></a>Hankija arve automatiseerimine

Selles teemas selgitatakse funktsioone, mis on saadaval hankija arvete täielikuks automatiseerimiseks, isegi manuseid sisaldavate arvete puhul.

Organisatsioonid, kus soovitakse ostureskontro protsesse sujuvamaks muuta, käsitlevad arvete töötlemist sageli ühe peamise protsessivaldkonnana, mis peaks olema tõhusam. Paljudel juhtudel annavad need organisatsioonid paberarvete töötlemise üle optilise märgituvastusega (OCR) tegelevatele teenusepakkujatele. Siis saavad nad masinloetavad arve metaandmed koos iga arve skannitud kujutisega. Automatiseerimisel abistamiseks koostatakse siis viimase etapi jaoks lahendus, mis võimaldab neid üksusi siis arveldussüsteemis kasutada. Microsoft Dynamics 365 for Finance and Operations, Enterprise edition võimaldab nüüd selle viimase etapi automatiseerimist valmislahenduse abil, kasutades arve automatiseerimislahendust.

## <a name="solution-context"></a>Lahenduse kontekst

Arve automatiseerimislahendus võimaldab kasutada standardliidest, mis suudab võtta arve päisest ja arve ridadelt ning ka arvega seotud manustest vastu arve metaandmeid. Väline süsteem, mis suudab genereerida selle liidesega ühilduvaid üksusi, suudab saata voo Finance and Operationsisse arvete ja manuste automaatseks töötlemiseks.

Järgmisel illustratsioonil on integratsiooni näidisstsenaarium, kus Contoso on sõlminud hankija arvete töötlemiseks partnerluse OCR-teenuse pakkujaga. Contoso hankijad saadavad teenusepakkujale meili teel arveid. OCR-i töötluse kaudu genereerib teenusepakkuja arve metaandmed (päise ja/või read) ja arve skannitud kujutise. Seejärel teisendab integratsioonikiht need üksused, et Finance and Operations saaks neid tarbida.

![Integreerimise näidisstsenaarium](media/vendor_invoice_automation_01.png)

Kui on vajalik arve integreerimine, on võimalikus mitu eelmise stsenaariumi variatsiooni. Andmete migreerimine on teine kasutusviis, kus seda liidest saab kasutada Finance and Operationsis arvete ja manuste loomiseks.

### <a name="solution-components"></a>Lahenduse komponendid

Lahenduse jalajälg sisaldab järgmisi komponente.

+ Arve päise, arve ridade ja arve manuste andmeüksused
+ Erandite töötlemine arvete puhul
+ Kõrvuti manusevaatur arvetel

Ülejäänud teema kirjeldab üksikasjalikult neid lahenduse komponente.

## <a name="data-entities"></a>Andmeüksused

Andmepakett on tööühik, mis tuleb saata Finance and Operationsisse arvete päiste, ridade ja manuste loomiseks. Andmepaketi koosteüksuste jaoks kasutatakse järgmisi andmeüksusi.

+ Hankija arve päis
+ Hankija arve rida
+ Hankijaarve dokumendimanus

Hankija arve dokumendi manus on uus andmeüksus, mis selle funktsiooni osana kasutusele võetakse. Hankija arve päiseüksust on muudetud nii, et see toetab manuseid. Selle funktsiooni jaoks pole hankija arve reaüksust muudetud.

See teema ei anna andmepaketi üksikasjalikku definitsiooni. Samuti ei selgita see, kuidas andmepakette luua. Selle teabe leiate jaotisest [Andmeüksuste ja pakettide raamistik](/dynamics365/en-us/unified-operations/dev-itpro/data-entities/data-entities-data-packages).

Arveid ja manuseid sisaldavate testandmete kiireks genereerimiseks tehke järgmist.

1. Logige oma Finance and Operationsi eksemplari sisse.
1. Avage **Ostureskontro** > **Arved** > **Ootel hankija arved**.
1. Looge arved, millel on read ja manused.

    > [!NOTE]
    > Manused peavad olema päise manused. Praegu ei toeta hankija arvedokumendi manuse üksus reamanuseid.

1. Avage tööruum **Andmehaldus**.
1. Looge eksporditöö, mis sisaldab hankija arve päist, hankija arve rida ja hankija arvedokumendi manuse üksusi.
1. Eksportige andmed.
1. Laadige eksporditud andmed paketina alla. Nüüd saate kasutada paketti andmete importimiseks sihteksemplaridesse testimise eesmärgil.

### <a name="determining-the-legal-entity-for-an-invoice"></a>Arve juriidilise isiku määramine

Andmepakettide kaudu imporditud arved saab seostada juriidilise isikuga, mille juurde need kuuluvad, kahel viisil.

+ Arvet töötlev imporditöö impordib selle samasse ettevõttesse, milles töö tööruumis **Andmehaldus** plaaniti. Teisisõnu: töö ettevõte määrab ettevõtte, millele arve kuulub.
+ Kui arveid sisaldav andmepakett saadetakse Finance and Operationsisse, saab kutsuja (st integreerimislahendus, mis töötab väljaspool Finance and Operationsit) nimetada selgelt HTTP taotluses ettevõtte ID. Sel juhul alistatakse ettevõtte kontekst, milles töötlemistöö Finance and Operationsis töötab, ja arved imporditakse HTTP taotluse kaudu edastatud ettevõttesse.

> [!NOTE]
> See käitumine on standardne andmehalduse käitumine. Seda on selgitatud siin, arvete kontekstis, üksnes terviklikkuse huvides.

## <a name="exception-processing"></a>Erandi töötlemine

Stsenaariumide korral, kus hankija arved tulevad Finance and Operationsisse integreerimise kaudu, peab olema Ostureskontro töörühma liikmel lihtne võimalus erandite või nurjunud arvete töötlemiseks ja ootel arvete loomiseks nurjunud arvetest. See hankija arvete erandite töötlemine on nüüd Finance and Operationsi osa.

### <a name="exceptions-list-page"></a>Erandite loendileht

Uus arve erandite loendileht on saadaval jaotises **Ostureskontro** > **Arved** > **Impordi nurjumised** > **Hankija arved, mille importimine nurjus**. Sellel lehel kuvatakse kõik hankija arve päisekirjed hankija arve päise andmeüksuse vahetabelist. Pange tähele, et saate vaadata samu kirjeid tööruumis **Andmehaldus**, kus saate teha ka samad toimingud, mis on antud erandi käsitlemise funktsioonis. Kuid kasutajaliides, mida erandi käsitlemise funktsioon pakub, on optimeeritud funktsionaalse kasutaja jaoks.

![Erandite loendileht](media/vendor_invoice_automation_02.png)

See loendileht sisaldab järgmisi välju, mis tulevad sisse voo kaudu.

+ **Ettevõte** – ettevõte, millele arve kuulub
+ **Tõrketeade** – haldusraamistiku väljastatav tõrketeade, mis selgitab, miks arvet ei saanud luua
+ **Number** – arve number
+ **Arve konto**
+ **Nimi** – hankija nimi
+ **Hankija konto**
+ **Ostutellimus** – arve ostutellimuse number
+ **Sisestuskuupäev**
+ **Arve kuupäev**
+ **Arve kirjeldus**
+ **Valuuta**
+ **Logi**
+ **Rea viide** – välisest süsteemist pärinev identifikaator

    > [!NOTE]
    > Rea viide ei ole arve ID.

Loendilehel on ka eelvaatepaan, mida saab kasutada järgmiselt.

+ Kogu tõrketeate kuvamiseks, et tabelis poleks vaja veergu **Tõrketeade** laiendada.
+ Kogu arve manuste loendi kuvamiseks, kui arvega tuli kaasa manuseid.

Loendileht toetab järgmisi tegevusi.

+ **Redigeerimine** – avage erandi kirje redigeerimisrežiimis, et saaksite probleemid kõrvaldada.
+ **Valikud** – juurdepääs loendilehtedel olevatele standardvalikutele. Saate kasutada valikut **Lisa tööruumi** erandite loendilehe kinnitamiseks tööruumi loendi või paanina.

### <a name="exception-details-page"></a>Erandi üksikasjade leht

Kui käivitate redigeerimisrežiimi, kuvatakse probleemidega arve erandi üksikasjade leht. Kui on manuseid, kuvatakse arve ja vaikemanus erandi üksikasjade lehel kõrvuti.

![Erandi üksikasjade leht](media/vendor_invoice_automation_03.png)

Eelneval illustratsioonil ei olnud sisse tulnud hankija arve päises ridu. Seetõttu on ridade osa tühi.

Erandi üksikasjade leht toetab järgmist toimingut.

+ **Ootel arve loomine** – kui olete erandi töötlemise käigus arvel olevad probleemid kõrvaldanud, võite klõpsata seda nuppu ootel arve loomiseks. Ootel arvete loomine toimub taustal (asünkroonse toiminguna).

### <a name="shared-service-vs-organization-based-exception-processing"></a>Jagatud teenus võrreldes organisatsioonipõhise erandi töötlemisega

Erandite loendileht toetab standardseid turbekonstruktsioone, mida **andmehalduse** tööruum vahetabeli kirjete töötlemiseks toetab. Arve imporditööd saab kaitsta järgmiselt.

+ Kasutaja rolliga
+ Kasutaja järgi
+ Juriidilise isiku järgi

![Imporditöö, mida kaitstakse kasutaja rolli ja juriidilise isiku järgi](media/vendor_invoice_automation_04.png)

Kui arve imporditöö jaoks on konfigureeritud turvalisus, arvestab erandite loendileht neid sätteid. Kasutajad näevad ainult neid arve erandi kirjeid, mida see seadistus neil näha lubab.

Näiteks Contoso on otsustanud töödelda arve erandeid juriidilise isiku järgi. Seetõttu konfigureeritakse turvalisus arve imporditöö puhul sellisel viisil, et kasutaja juriidilises isikus A näeb ainult arve erandeid juriidilises isikus A, samas kui kasutaja juriidilises isikus B näeb ainult arve erandeid juriidilises isikus B. Selline seadistus võimaldab arve erandite haldamise kohustusi jagada.

Contoso võib otsustada ka turvalisust mitte kehtestada, et samad kasutajad saaksid töödelda arve erandeid kõigi juriidiliste isikute puhul. See seadistus lubab jagatud teenuste stsenaariumi arve erandite haldamiseks.

## <a name="side-by-side-attachment-viewer"></a>Kõrvuti manusevaatur

Hankija arvete manuste hõlpsaks kuvamiseks on järgmistel arveldusprotsessis kasutatavatel lehtedel nüüd manusevaatur.

+ **Erandite käsitlemine**
+ Leht **Ootel hankija arved** (saadaval ka arve ülevaatusprotsessis)
+ Päringuleht **Arve tööleht** (sisestatud arvete jaoks)

Siin on põhifunktsioonid, mida manusevaatur pakub.

+ Kõigi dokumendihalduri toetatavate manusetüüpide kuvamine (failid, kujutised, URL-id ja märkused).
+ Mitmeleheliste TIFF-failide kuvamine.
+ Järgmiste toimingute tegemine pildifailidega.
  + Pildi osade esiletõstmine.
  + Pildi osade blokeerimine.
  + Märkuste lisamine pildile.
  + Pildi suurendamine ja vähendamine.
  + Pildi panoraamimine.
  + Tegevuste tagasivõtmine ja uuesti tegemine.
  + Pildi sobitamine suurusega.

> [!NOTE]
> Need tegevused on saadaval ainult pildifailide puhul (JPEG, TIFF, PNG jne). Kõik muudatused, mida nende tegevustega pildil teete, salvestatakse pildifaili. Praegu ei sisalda manusevaatur versioonide kasutamist ega auditeerimisvõimalusi.

### <a name="default-attachment"></a>Vaikemanus

Kui hankija arvel on mitu manust, saate määrata ühe dokumendi lehel **Manused** vaikemanuseks. Valik **On vaikemanus** on uus valik, mis lisati selle funktsiooni osana. See valik on näha ka hankija arvedokumendi manuse andmeüksuses. Seetõttu saab vaikemanuse määrata integreerimiste kaudu.

Vaikemanuseks saab määrata ainult ühe dokumendi. Pärast dokumendi määramist vaikemanuseks kuvatakse see arve avamisel automaatselt manusevaaturis. Kui te ühtegi dokumenti vaikemanuseks ei määra, ei näita vaatur arve avamisel automaatselt ühtegi manust.

### <a name="showhide-invoice-attachments"></a>Kuva/peida arve manused

Uus nupp, mis on saadaval päringulehtedel **Erandi töötlemine**, **Ootel arve** ja **Arve tööleht**, võimaldab manusevaaturit kuvada või peita.

### <a name="security"></a>Turvalisus

Rollipõhise turvalisuse kaudu juhitakse järgmisi tegevusi manusevaaturis.

+ Esiletõstmine
+ Blokeeri
+ Kommenteerimine

### <a name="pending-vendor-invoices-page"></a>Hankija ootelolevate arvete leht

Järgmised õigused annavad manusevaaturile kirjutuskaitstud juurdepääsu või lugemise/kirjutamise juurdepääsu esiletõstmise, blokeerimise ja kommenteerimise toimingute jaoks.

+ **Hankija arve pildi haldamine** – see privileeg annab lugemis-/kirjutamisõiguse.
+ **Hankija arve pildi kuvamine** – see privileeg annab kirjutuskaitstud juurdepääsu.

Järgmised kohustused annavad manusevaaturile kirjutuskaitstud juurdepääsu või lugemise/kirjutamise juurdepääsu järgmiste tegevuste jaoks.

+ **Hankija arvete haldamine** – sellele kohustusele on määratud hankija arvete pildi haldamise privileeg.
+ **Hankija arve oleku kohta päringu esitamine** – sellele kohustusele on määratud hankija arve pildi vaatamise privileeg.

Järgmised rollid annavad manusevaaturile kirjutuskaitstud juurdepääsu või lugemise/kirjutamise juurdepääsu järgmiste tegevuste jaoks.

+ **Ostureskontro ametnik** ja **Ostureskontro juht** – nendele rollidele määratakse kohustus Hankija arvete haldamine.
+ **Ostureskontro ametnik**, **Ostureskontro juht**, **Ostureskontro tsentraliseeritud maksuametnik** ja **Ostureskontro maksuametnik** – nendele rollidele määratakse kohustus Hankija arve oleku kohta päringu esitamine.

### <a name="invoice-exception-details-page"></a>Arve erandi üksikasjade leht

Järgmised õigused annavad manusevaaturile kirjutuskaitstud juurdepääsu või lugemise/kirjutamise juurdepääsu esiletõstmise, blokeerimise ja kommenteerimise toimingute jaoks.

> [!NOTE]
> Valmis kujul annavad selles jaotises nimetatud rollid arve piltidele manusevaaturis kirjutuskaitstud juurdepääsu. Kui rollil peaks olema piltide puhul ka kirjutamisõigusega juurdepääs, saate anda sellele rollile kirjutamisõiguse, kasutades siin kirjeldatud privileegi ja kohustust.

+ **Hankija arve päiseüksuse pildi haldamine** – see privileeg annab manuses olevate arve piltide lugemise/kirjutamise õiguse.
+ **Hankija arve päiseüksuse pildi kuvamine** – see privileeg annab õiguse manuses oleva arve pildi kirjutuskaitsega avamiseks.

Järgmised kohustused annavad manusevaaturile kirjutuskaitstud juurdepääsu järgmiste tegevuste jaoks.

+ **Hankija arvete haldamine** – sellele kohustusele on määratud hankija arve päiseüksuse pildi haldamise privileeg.

Järgmised rollid annavad manusevaaturile kirjutuskaitstud juurdepääsu järgmiste tegevuste jaoks.

+ **Ostureskontro ametnik** ja **Ostureskontro juht** – nendele rollidele määratakse kohustus Hankija arvete haldamine.

Vaikimisi, kui kasutaja roll annab mõnel lehel redigeerimisõigused, on kasutajal redigeerimisõigused ka manusevaaturis esiletõstmise, blokeerimise ja kommenteerimise toiminguteks. Kuid kui on stsenaariume, mille puhul konkreetsel rollil peaksid olema redigeerimisõigused lehel, kuid mitte manusevaaturis, saab sel puhul kasutada sobivaid privileege eespool antud loendist.

