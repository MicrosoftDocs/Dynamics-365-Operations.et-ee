---
title: Arve automatiseerimine skannitud dokumentide korral
description: See artikkel selgitab funktsioone, mis on saadaval hankijaarvete, isegi nende arvete, mis sisaldavad manuseid, lõpetamise lõpetamise automatiseerimiseks.
author: abruer
ms.date: 03/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendEditInvoiceHeaderStagingListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0449a13989bad45cf0456a2678e5724036d2af3d
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070690"
---
# <a name="invoice-automation-for-scanned-documents"></a>Arve automatiseerimine skannitud dokumentide korral

[!include [banner](../includes/banner.md)]

See artikkel selgitab andmeüksuseid, mis on saadaval hankija arvete ja manustega arvete lõpetamise automatiseerimiseks.

Organisatsioonid, kus soovitakse ostureskontro protsesse sujuvamaks muuta, käsitlevad arvete töötlemist sageli ühe peamise protsessivaldkonnana, mis peaks olema tõhusam. Paljudel juhtudel annavad need organisatsioonid paberarvete töötlemise üle optilise märgituvastusega (OCR) tegelevatele teenusepakkujatele. Siis saavad nad masinloetavad arve metaandmed koos iga arve skannitud kujutisega. Automatiseerimisel abistamiseks koostatakse siis viimase etapi jaoks lahendus, mis võimaldab neid üksusi siis arveldussüsteemis kasutada. Selle viimase etapi automatiseerimine on nüüd valmislahenduses lubatud, kasutades arve automatiseerimislahendust.

## <a name="solution-context"></a>Lahenduse kontekst

Arve automatiseerimislahendus võimaldab kasutada standardliidest, mis suudab võtta arve päisest ja arve ridadelt ning ka arvega seotud manustest vastu arve metaandmeid. Väline süsteem, mis suudab genereerida selle liidesega ühilduvaid üksusi, suudab saata voo arvete ja manuste automaatseks töötlemiseks.

Järgmisel illustratsioonil on integratsiooni näidisstsenaarium, kus Contoso on sõlminud hankija arvete töötlemiseks partnerluse OCR-teenuse pakkujaga. Contoso hankijad saadavad teenusepakkujale meili teel arveid. OCR-i töötluse kaudu genereerib teenusepakkuja arve metaandmed (päise ja/või read) ja arve skannitud kujutise. Seejärel teisendab integratsioonikiht need üksused, et neid saaks tarbida.

![Integreerimise näidisstsenaarium.](media/vendor_invoice_automation_01.png)

Kui on vajalik arve integreerimine, on võimalikus mitu eelmise stsenaariumi variatsiooni. Andmete migreerimine on teine kasutusviis, kus seda liidest saab kasutada arvete ja manuste loomiseks.

### <a name="solution-components"></a>Lahenduse komponendid

Lahenduse jalajälg sisaldab järgmisi komponente.

+ Arve päise, arve ridade ja arve manuste andmeüksused
+ Erandite töötlemine arvete puhul
+ Kõrvuti manusevaatur arvetel

Ülejäänud artikkel annab lahenduse komponentide üksikasjalikud kirjeldused.

## <a name="data-entities"></a>Andmeüksused

Andmepakett on tööühik, mis tuleb saata arvete päiste, ridade ja manuste loomiseks. Andmepaketi koosteüksuste jaoks kasutatakse järgmisi andmeüksusi.

+ Hankija arve päis
+ Hankija arve rida
+ Hankijaarve dokumendimanus

Hankija arve dokumendi manus on uus andmeüksus, mis selle funktsiooni osana kasutusele võetakse. Hankija arve päiseüksust on muudetud nii, et see toetab manuseid. Selle funktsiooni jaoks pole hankija arve reaüksust muudetud.

Üksikasjalikku teavet andmepakettide kohta vaadake teemast [Andmehalduse ülevaade](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md). Lisateavet andmepakettide loomise kohta andmehalduse tööruumi kasutades vaadake jaotisest Andmepakettide [töötlemine ja kasutamine Dynamics 365 finantside ja toimingute rakenduste lahenduses](../../fin-ops-core/dev-itpro/lcs-solutions/process-data-packages-lcs-solutions.md).

Arveid ja manuseid sisaldavate testandmete kiireks genereerimiseks tehke järgmist.

1. Logige oma eksemplari sisse.
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
+ Kui arveid sisaldav andmepakett saadetakse Finance’i, saab kutsuja (st integreerimislahendus, mis töötab väljaspool Finance’i) nimetada selgelt HTTP taotluses ettevõtte ID. Sel juhul alistatakse ettevõtte kontekst, milles töötlemistöö Finance’is töötab, ja arved imporditakse HTTP taotluse kaudu edastatud ettevõttesse.

> [!NOTE]
> See käitumine on standardne andmehalduse käitumine. Seda on selgitatud siin, arvete kontekstis, üksnes terviklikkuse huvides.

## <a name="exception-processing"></a>Erandi töötlemine

Stsenaariumides, kus hankija arved integreerituse kaudu finantsidesse ja toimingutesse tulevad, peab ostureskontro töörühma liige töötlema erandeid või nurjunud arveid ja looma ootel arveid nurjunud arvetest. See hankija arvete erandtöötlemine on nüüd finantside ja toimingute osa.

### <a name="vendor-invoices-that-failed-to-import-list-page"></a>Hankijaarved, mille loendilehele importimine ei õnnestunud

Uus arve erandite loendileht on saadaval jaotises **Ostureskontro** > **Arved** > **Impordi nurjumised** > **Hankija arved, mille importimine nurjus**. Sellel lehel kuvatakse kõik hankija arve päisekirjed hankija arve päise andmeüksuse vahetabelist. Pange tähele, et saate vaadata samu kirjeid tööruumis **Andmehaldus**. Tööruumis **Andmehaldus** saate teha ka samu toiminguid, mis on antud erandi käsitlemise funktsioonis. Erandite käsitlemise funktsioon on optimeeritud funktsiooni kasutaja jaoks, mis lihtsustab kasutamist.

![Erandite loendileht.](media/vendor_invoice_automation_02.png)

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

Loendileht toetab järgmisi tegevusi.

+ **Redigeerimine** – avage erandi kirje redigeerimisrežiimis, et saaksite probleemid kõrvaldada.
+ **Valikud** – juurdepääs loendilehtedel olevatele standardvalikutele. Saate kasutada valikut **Lisa tööruumi** erandite loendilehe kinnitamiseks tööruumi loendi või paanina.

### <a name="vendor-invoices-that-failed-to-import-details-page"></a>Hankijaarved, mille üksikasjade lehele importimine ei õnnestunud

Kui käivitate redigeerimisrežiimi, avaneb **väljaminevate arvete hankijaarvete leht, mille üksikasjade importimine ebaõnnestus**. Kui on probleeme arvega, millel on manus, siis manust ei kuvata. Manus tuleb uuesti arvele lisada.

Lehel **hankijaarvete kohta, mille üksikasjade importimine ebaõnnestus**, saate luua ootel arve. Kui olete erandi töötlemise käigus arvel olevad probleemid kõrvaldanud, valige nupp **Ootel arve loomine** ootel arve loomiseks. Ootel arve luuakse taustal. 

### <a name="shared-service-vs-organization-based-exception-processing"></a>Jagatud teenus võrreldes organisatsioonipõhise erandi töötlemisega

Erandite loendileht toetab standardseid turbekonstruktsioone, mida **andmehalduse** tööruum vahetabeli kirjete töötlemiseks toetab. Arve imporditööd saab kaitsta järgmiselt.

+ Kasutaja rolliga
+ Kasutaja järgi
+ Juriidilise isiku järgi

![Imporditöö, mida kaitstakse kasutaja rolli ja juriidilise isiku järgi.](media/vendor_invoice_automation_04.png)

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

## <a name="security"></a>Turvalisus

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

### <a name="vendor-invoice-attachment"></a>Hankija arve manused

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

