---
title: Ostureskontro arvete võrdlemise ülevaade
description: Ostureskontro arvete võrdlemine on hankija arve, ostutellimuse ja toote sissetuleku teabe vastavusse viimise protsess.
author: sunfzam
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendInvoicePostingHistory
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "27361"
- intro-internal
ms.assetid: 9f3dace7-05d8-4974-8f85-aca2e224876c
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: befc9b9ef3dcd5545ff3f252a706cab546165cb0
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/02/2021
ms.locfileid: "7595061"
---
# <a name="accounts-payable-invoice-matching-overview"></a>Ostureskontro arvete võrdlemise ülevaade

[!include [banner](../includes/banner.md)]

Ostureskontro arvete võrdlemine on hankija arve, ostutellimuse ja toote sissetuleku teabe vastavusse viimise protsess.

Dokumentide vastavusseviimisel nimetatakse nende dokumentide erinevusi vastavusseviimise lahknevusteks. Vastavusseviimise lahknevusi võrreldakse määratud hälvetega. Kui vastavusseviimise lahknevus ületab lubatud kõikumisprotsendi või summa, kuvatakse vastavusseviimise hälbe ikoonid lehel Hankija arve ja lehel Arve ajalugu ja vastavusseviimise üksikasjad. 

Näiteks sisestate ostutellimuse ühe rea kaubaga 1000 patareid hinnaga 1,00 tk. Hankija kinnitab ja edastab ostutellimuse. Hankija lähetab 1000 patareid ja te sisestate toote sissetuleku 1000 patarei kohta hinnaga 1,00 tk. Patareide laokulu värskendatakse koos selle hinnaga. 

Arve saabub 1000-le patareile hinnaga 1,10 tk. Teie juriidilise isiku poliitika lubab selle kategooria kaubale 5-protsendilist netoühiku hinnakõikumist. Hind 1,05 oleks vastuvõetav, aga 1,10 juba mitte. Kui sisestate arve teavet, tuvastatakse hinna vastavusseviimise lahknevus ja saate arve salvestada, kuni lahknevus lahendatakse.

Saate kasutada järgmist tüüpi ostureskontro arvete vastavusseviimist.

-   Arve koondsummade vastavusseviimine – arve koondsummade vastavusseviimine ostutellimuse koondsummadega. Seda tüüpi arvete vastavusseviimine sisaldab kõige vähem üksikasju, seega saab selle suvandi abil määrata juhtelemendid, mis minimeerivad töötajate arvete vastavusseviimise teabe ülevaatamisele kuluvat aega.
-   Kahesuunaline vastavusseviimine – arve hinnateave viiakse vastavusse ostutellimuse hinnateabega.
-   Kolmesuunaline vastavusseviimine – arve hinnateave viiakse vastavusse ostutellimuse hinnateabega. Arvel olevat koguse teavet saab samuti viia vastavusse arve puhul valitud toote sissetulekute koguseteabega.
-   Tasude vastavusseviimine – arvel olevate tasude andmed (summad) viiakse vastavusse ostutellimusel olevate tasude andmetega (summadega).

> [!NOTE]
> Arve kinnitamise muid vorme saab kasutada hankija arve poliitikate abil. 

Kahesuunaline ja kolmesuunaline vastavusseviimine viivad hinnateabe alati vastavusse ühiku hinna alusel. Saate konfigureerida neid vastavusse viimise poliitikaid ka nii, et hinnateave viiakse vastavusse koondhinna alusel.
-   Ühiku netohinna vastavusseviimine – kahesuunalise või kolmesuunalise vastavusseviimise puhul viiakse iga arverea ühiku netohind vastavusse ostutellimuse ühiku netohinnaga. Ühiku netohind määratakse järgmise valemiga: rea netosumma / rea kogus
-   Koondhindade vastavusseviimine – kahesuunalise või kolmesuunalise vastavusseviimise puhul viiakse iga arverea netosumma (koondhinda) vastavusse ostutellimuse netosummaga. Netosumma määratakse järgmise valemiga: *(ühiku hind \* rea kogus) + rea tasud – rea allahindlused*. Koguhindasid protsendi järgi vastavusse viies võrdleb süsteem väärtusi kandevaluutat kasutades. Koguhindasid summa järgi vastavusse viies võrdleb süsteem väärtusi arvestusvaluutat kasutades. Kui arveldate ostutellimuse rea osaliselt, toimub koguhinna vastendamise kinnitamine viimasel arvel selle rea puhul. 

Tavaliselt toimuvad arvete vastavusseviimise arvutused automaatselt, kui redigeerite hankija arveid lehel Hankija arve. Teise võimalusena saab arveid võrrelda vajaduse korral. Arvete vastavusseviimist vajaduse korral juhitakse juriidilise isiku puhul vahekaardi Arve kinnitamine lehel Ostureskontro parameetrid jaotises Arve päise oleku automaatne värskendamine. Arveid saab viia vastavusse ka arve ülevaatamise protsessi käigus. Arvete vastavusseviimise tulemusi saab vaadata ka lehel Hankija arve ja seotud arve vastavusseviimise lehtedel.

## <a name="invoice-totals-matching"></a> Arvesummade vastavusseviimine
Arve koondsummade vastavusseviimist saab kasutada tagamiseks, et arve koondsummad ei erineks eeldatavatest summadest rohkem kui lubatud hälbe võrra. Arve koondsummade vastavusseviimise üksikasjade lehel võrreldakse kuut koondsummat, nagu on näidatud järgmises tabelis. Kui arve koondsummade vastavusseviimise lubatud hälve on 20%, käsitletakse vastavusseviimise lahknevusena kogu allahindluse summa hälbeprotsenti 100%.

| Koondsumma väli    | Arve tegelik koondsumma | Arve eeldatav koondsumma | Erinevuse protsent | Vastendamise olek |
|----------------|----------------------|------------------------|---------------------|--------------|
| Saldo        | 495,00               | 495,00                 | 0%                  | Arvestatud       |
| Lõppallahindlus | 0,00                 | 9,90                   | 1                | Nurjunud       |
| Tasud        | 64,90                | 64,90                  | 0%                  | Arvestatud       |
| Käibemaks      | 139,98               | 137,50                 | 2%                  | Arvestatud       |
| Ümardus      | 0,00                 | 0,00                   | 0%                  | Arvestatud       |
| Arve summa | 699,88               | 687,50                 | 2%                  | Arvestatud       |

Arve koondsummade vastavusseviimist juhitakse juriidilise isiku puhul nupuga Arvesummade vastavusseviimine lehel Ostureskontro parameetrid. Võrreldakse eeldatavat arve koondsummat ja tegelikku arve koondsummat. Eeldatav arvesumma arvutatakse ostutellimuse hindade, tasude ja käibemaksu teabe ning arve koguste alusel.

## <a name="two-way-price-totals-matching"></a> Kahesuunaline koondhindade vastavusseviimine
Kasutage kahesuunalist vastavusseviimist, veendumaks, et ostutellimuse ja arve hinnaandmete hälve on lubatud piirides. Saate võrrelda iga arve rea ja kõikide ootel ja varem sisestatud arve ridade netosumma hinnateavet vastava ostutellimuse rea netosummaga. Seda nimetatakse koondhindade vastavusseviimiseks. 

Koondhindade vastavusseviimine võib põhineda protsendil, summal või protsendil ja summal. 

Kui ostuhinna koondsumma hälbeprotsent on määratud, võrreldakse viit välja, nagu järgmises tabelis näidatud. Kuna ostutellimuse koondsumma kõikumisprotsent on 10%, näitab koondhinna hälbeprotsent 50% vastavusseviimise lahknevust.

| Vastendamise olek | Arve netosumma | Eeldatav netosumma | Erineva ostuhinna koondsumma (hälbe summa) | Erineva ostuhinna protsent kokku (hälbe protsent) | Ostuhinna kogusumma hälbe protsent |
|--------------|--------------------|---------------------|--------------------------------------------------|-----------------------------------------------------------------|----------------------------------------|
| Arvestatud       | 105,00             | 100,00              | 5,00                                             | 5%                                                              | 10%                                    |
| Nurjunud       | 150,00             | 100,00              | 50,00                                            | 0,5                                                             | 10%                                    |

Kui ostuhinna koondsumma hälbe summa on määratud, võrreldakse viit välja, nagu järgmises tabelis näidatud. Kuna ostutellimuse koondsumma kõikumisprotsent on 100,00, näitab koondhinna hälbe summa 105,00 vastavusseviimise lahknevust.

| Vastendamise olek | Arve netosumma | Eeldatav netosumma | Erineva ostuhinna koondsumma (hälbe summa) | Erineva ostuhinna koondsumma arvestusvaluutas (hälbe summa) | Ostuhinna kogusumma hälve |
|--------------|--------------------|---------------------|--------------------------------------------------|-------------------------------------------------------------------------|--------------------------------|
| Arvestatud       | 150,00             | 100,00              | 50,00                                            | 50,00                                                                   | 100,00                         |
| Nurjunud       | 205,00             | 100,00              | 105,00                                           | 105,00                                                                  | 100,00                         |

Kui koondhindade vastavusseviimine on seadistatud hälbeprotsendiga ja hälbe summaga, mida mõnikord nimetatakse summaks, mida ei tohi ületada, arvestatakse hindamisel, kas real on vastavusseviimise lahknevus, mõlemat hälvet. Kui protsent või summa ületab hälbe, nagu on näha järgmises tabelis väärtustel 150,00 ja 205,00, on real vastavusseviimise lahknevus.

| Vastendamise olek | Arve netosumma | Eeldatav netosumma | Erineva ostuhinna protsent kokku (hälbe protsent) | Ostuhinna kogusumma hälbe protsent | Erineva ostuhinna koondsumma arvestusvaluutas (hälbe summa) | Ostuhinna kogusumma hälve |
|--------------|--------------------|---------------------|-----------------------------------------------------------------|----------------------------------------|-------------------------------------------------------------------------|--------------------------------|
| Arvestatud       | 105,00             | 100,00              | 5%                                                              | 10%                                    | 5,00                                                                    | 100,00                         |
| Nurjunud       | 150,00             | 100,00              | 0,5                                                             | 10%                                    | 50,00                                                                   | 100,00                         |
| Nurjunud       | 205,00             | 100,00              | 105%                                                            | 10%                                    | 105,00                                                                  | 100,00                         |

Kahesuunalist vastavusseviimist juhitakse juriidilise isiku puhul väljaga Rea vastavusseviimise poliitika lehel Ostureskontro parameetrid. Olenevalt valikust väljal Luba vastavusseviimise poliitika alistamine saate valida kahesuunalise vastavusseviimise konkreetse hankija, kauba või kauba ja hankija kombinatsiooni puhul lehel Vastavusse viimise poliitika ja konkreetsel ostutellimusel lehel Ostutellimus.

Hinna koondsummade vastavusseviimist juhitakse juriidilise isiku puhul nupuga Koondhindade vastavusseviimine lehel Ostureskontro parameetrid. Ostuhinna koondsumma hälbeprotsent ja hälbe summa (summa, mida ei tohi ületada) on samuti sellel lehel määratletud.

## <a name="two-way-net-unit-price-matching"></a> Kahesuunaline ühiku netohinna vastavusseviimine
Kasutage kahesuunalist vastavusseviimist, veendumaks, et ostutellimuse ja arve hinnaandmete hälve on lubatud piirides. Saate võrrelda arvel iga kauba ühiku netohinna hinnateavet. Seda nimetatakse ühiku netohinna vastavusseviimiseks. 

Arve koondsummade vastavusseviimise üksikasjade lehel võrreldakse üheksat rea summat, nagu on näidatud järgmises tabelis. Kui ühiku netohinna lubatud hinnahälve on 10%, käsitletakse vastavusseviimise lahknevusena ühiku netohinna hälbeprotsenti 22,61%.

| Rea väli                    | Arve väärtus | Ostutellimuse väärtus | Erinevuse protsent | Vastendamise olek |
|-------------------------------|---------------|----------------------|---------------------|--------------|
| Ühiku hind                    | 55,40         | 55,38                | 0%                  | Arvestatud       |
| Hinnaühik                    | 1,00          | 1,00                 | 0%                  | Arvestatud       |
| Ostukulud          | 50,00         | 0,00                 | 1                | Nurjunud       |
| Allahindlus                      | 0,00          | 0,00                 | 0%                  | Arvestatud       |
| Allahindluse protsent              | 0,00          | 0,00                 | 0%                  | Arvestatud       |
| Multiallahindlus            | 0,00          | 0,00                 | 0%                  | Arvestatud       |
| Multiallahindluse protsent | 0,00          | 0,00                 | 0%                  | Arvestatud       |
| Netosumma                    | 271,60        | 221,52               | 22,61%              | Nurjunud       |
| Ühiku netohind                | 67,9000       | 55,3800              | 22,61%              | Nurjunud       |

Kahesuunalist vastavusseviimist juhitakse juriidilise isiku puhul väljaga Rea vastavusseviimise poliitika lehel Ostureskontro parameetrid. Olenevalt valikust väljal Luba vastavusseviimise poliitika alistamine saate valida kahesuunalise vastavusseviimise konkreetse hankija, kauba või kauba ja hankija kombinatsiooni puhul lehel Vastavusse viimise poliitika ja konkreetsel ostutellimusel lehel Ostutellimus. 

Ühiku netohinna vastavusseviimist juhitakse juriidilise isiku puhul nupuga Luba arvete vastavusseviimise kontrollimine lehel Ostureskontro parameetrid. Ühiku netohinna hälbeprotsente saab konfigureerida kaupade, kaubagruppide, hankijate, hankijagruppide, kauba ja hankija kombinatsioonide või juriidilise isiku puhul lehel Hinnahälbed.

## <a name="two-way-price-totals-matching-and-net-unit-price-matching"></a> Kahesuunaline koondhindade vastavusseviimine ja ühiku netohinna vastavusseviimine
Koondhindade vastavusseviimist ja ühiku netohinna vastavusseviimist saab kasutada koos. See näide eeldab järgmist konfiguratsiooni.

-   Kauba USB-draiv ühiku netohinna hälve on 10%.
-   Juriidilise isiku koondhindade vastavusseviimise hälve on 15% või 500,00.

Ostutellimuses on järgmine rida.

| Kaubakood | Kogus | Ühiku hind | Netosumma |
|-------------|----------|------------|------------|
| USB‑draiv   | 1000    | 10,00      | 10,000.00  |

Sisestatud on kolm arvet, nagu on näidatud järgmises tabelis. Arvel 3 on arve vastavusseviimise lahknevus, kuna hälve 1880,00 ületab ostuhinna hälbesumma 500,00. Koondhindade vastavusseviimise puhul sisaldab arve netosumma kõiki eelnevalt sisestatud arveid lisaks sellele arvele, millega praegu töötate.

| Kaubakood          | Kogus | Ühiku hind | Netosumma | Hinna vastendamine | Koguhinna vastendus |
|----------------------|----------|------------|------------|-------------|-------------------|
| Arve 1: USB-draiv | 800      | 10,80      | 8640,00   | Arvestatud      | Arvestatud            |
| Arve 2: USB-draiv | 100      | 10,80      | 1080,00   | Arvestatud      | Arvestatud            |
| Arve 3: USB-draiv | 200      | 10,80      | 2160,00   | Arvestatud      | Nurjunud            |
| Kokku                |          |            | 11 880,00  |             |                   |

## <a name="three-way-matching"></a>Kolmesuunaline vastavusse viimine

Kolmesuunalist vastavusse viimist saate kasutada veendumiseks, et ostutellimuse ja arve hinnaandmete hälve on lubatud piirides, ning veendumiseks, et arve kogus ühtib vastavate toote sissetulekute kogustega.

Samu reasummasid võrreldakse vastavusseviimise üksikasjade lehel sarnaselt kahesuunalisele vastavusseviimisele. Lisaks viiakse arve kogus vastavusse vastuvõetud toote sissetuleku kogustega. Kui arve kogus erineb vastavusse viidud toote sisstuleku kogusest, on olemas koguse vastavusseviimise tõrge.

| Rea väli                    | Arve väärtus | Ostutellimuse väärtus | Erinevuse protsent | Vastendamise olek |
|-------------------------------|---------------|----------------------|---------------------|--------------|
| Ühiku hind                    | 55,40         | 55,38                | 0%                  | Arvestatud       |
| Hinnaühik                    | 1,00          | 1,00                 | 0%                  | Arvestatud       |
| Ostukulud          | 50,00         | 0,00                 | 1                | Nurjunud       |
| Allahindlus                      | 0,00          | 0,00                 | 0%                  | Arvestatud       |
| Allahindluse protsent              | 0,00          | 0,00                 | 0%                  | Arvestatud       |
| Multiallahindlus            | 0,00          | 0,00                 | 0%                  | Arvestatud       |
| Multiallahindluse protsent | 0,00          | 0,00                 | 0%                  | Arvestatud       |
| Netosumma                    | 271,60        | 221,52               | 22,61%              | Nurjunud       |
| Ühiku netohind                | 67,9000       | 55,3800              | 22,61%              | Nurjunud       |

| Rea väli                     | Arve väärtus | Vastendamise olek |
|--------------------------------|---------------|--------------|
| Arve kogus               | 4,00          |              |
| Kõik vastendatud toote sissetulekud | 0,00          | Nurjunud       |

Kolmesuunalist vastavusseviimist juhitakse juriidilise isiku puhul väljaga Rea vastavusseviimise poliitika lehel Ostureskontro parameetrid. Olenevalt valikust väljal Luba vastavusseviimise poliitika alistamine saate valida kolmesuunalise vastavusseviimise konkreetse hankija, kauba või kauba ja hankija kombinatsiooni puhul lehel Vastavusse viimise poliitika ja konkreetsel ostutellimusel lehel Ostutellimus.

## <a name="charges-matching"></a> Tasude võrdlemine
Tasude vastavusseviimist saab kasutada tagamiseks, et tasud ei erineks eeldatavatest summadest rohkem kui lubatud hälbeprotsendi võrra. Iga arvele ja ostutellimusele rakendatava tasukoodi koondsummasid võrreldakse lehel Tasude väärtuste võrdlemine – arve:, nagu on näidatud järgmises tabelis. Kui tasukoodi lubatud hälve on 25%, käsitletakse vastavusseviimise lahknevusena litsentsitasude koodi hälbeprotsenti 99 999 999 999,99%.

> [!NOTE] 
> Hälbeprotsent 99 999 999 999,99% tähendab, et ostutellimusel põhinev eeldatav summa on null ja arve tegelik summa on positiivne väärtus. 

| Tasude vastavusseviimise olek | Arve kulude kood | Arvutatud tegelik koguväärtus | Eeldatav tegelik koguväärtus | Hälbe hulk | Erinevuse protsent | Hälbe protsent |
|----------------------|----------------------|-------------------------------|---------------------------------|-----------------|---------------------|----------------------|
| Nurjunud               | Litsents              | 25                            | 0                               | 25              | 99 999 999 999,99%  | 25%                  |
| Arvestatud               | Veos              | 200                           | 200                             | 0               | 0%                  | 25%                  |
| Nurjunud               | Kiirsaadetis             | 4                             | 2                               | 2               | 1                | 25%                  |

Tasude vastavusseviimist juhitakse juriidilise isiku puhul nupuga Tasude vastavusseviimine lehel Ostureskontro parameetrid. Tasude hälbe kõikumisprotsendid saab seadistada lehel Tasude hälbed.

> [!NOTE]
> Tasude võrdlemine toimub ainult nende tasukoodide kohta, mille puhul lehel Tasukood on valitud nupp Võrdle ostutellimuse ja arve väärtusi.

## <a name="related-functionality"></a> Seotud funktsioon
Hankijaarved põhinevad ostutellimuste asemel tihti tegelikke saadetisi kajastavatel toote sissetulekutel. Vahel ei kattu arvete summad ostutellimuste summadega, ja vahel ei kattu lähetatavad kogused arveldatud kogustega. Saate aidata hallata seda teavet järgmistel viisidel.
-   Saate koostada hankija arve toote sissetulekute põhjal. Arvete puhul soovitatakse automaatselt toote sissetulekuid ja saate valida, milliseid toote sissetulekuid kasutada. Samuti saate valida mitme ostutellimuse hulgast konkreetsed toote sissetuleku reaüksused, kui seda vaja on.
-   Vaadake ja kinnitage koguse erinevused arvel arveldatud koguse ja toote sissetulekul saadud koguse vahel. Kui seal on erinevus, saate arve salvestada ja hiljem selle teise toote sissetulekuga kohaldada või muuta arve koguse saadud kogusele vastavaks.
-   Sisestage arve summad, mida ei kaasatud algsesse ostutellimusse, nii et arve teave kattuks arvega, mille hankijalt saite. Saate võrrelda ostutellimuste tasusid arvete tasudega. Vajaduse korral saate tasud arvetele lisada ja määrata need arve ridadele.
-   Vaadake ja kinnitage hinna võrdluslahknevusi arve ühiku netohinna ja ostutellimuse ühiku netohinna vahel. Võite seadistada hinnakõikumisprotsendid juriidilistele isikutele, hankijatele ja kaupadele. Kui hankija arve rea hind pole vastuvõetava hinnakõikumise piires, võite arve salvestada, kuni see on sisestamiseks kinnitatud või kuni saate hankijalt paranduse.

Lisateabe saamiseks vaadake jaotiseid [Kolmepoolsed vastavusse viimise poliitikad](three-way-matching-policies.md) ja [Ostureskontro arve vastavuse valideerimise seadistamine](tasks/set-up-accounts-payable-invoice-matching-validation.md). 






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
