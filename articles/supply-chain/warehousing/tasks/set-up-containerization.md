--- 
title: "Konteinerisse määramise seadistamine"
description: Protseduur kirjeldab koormakonteinerite koostamise automatiseerimist laohalduses.
author: YuyuScheller
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 76334f7ee4efe33df4a86aaa11a59748387cec89
ms.openlocfilehash: c5faf926071dec5d2ddc1c9e921a98ecd0754917
ms.contentlocale: et-ee
ms.lasthandoff: 11/02/2017

---
# <a name="set-up-containerization"></a>Konteinerisse määramise seadistamine

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Protseduur kirjeldab koormakonteinerite koostamise automatiseerimist laohalduses. Automaatne konteinerite koostamine loob saadetiste jaoks konteinerid ja komplekteerimistööd pärast voo töötlemist ja töö read saab jagada kogustesse, mis vastavad konteineritele. See aitab laotöötajatel komplekteerida kaupu otse valitud konteinerisse. Võrreldes käsitsi pakkimise protsessiga, on sellised toimingud nagu konteinerite loomine, kaupade määramine ja konteinerite sulgemine süsteemi automatiseeritud. See protseduur kasutab demoettevõtet USMF ja selle viib läbi lao juhataja.


## <a name="set-up-a-wave-template"></a>Voomalli seadistamine
1. Avage Laohaldus > Seadistus > Vood > Voomallid.
2. Klõpsake valikut Uus.
3. Tippige väärtus väljale Voomalli nimi.
4. Tippige väärtus väljale Voomalli kirjeldus.
5. Sisestage või valige väärtus väljal Koht.
6. Sisestage või valige väärtus väljal Ladu.
7. Laiendage jaotist Meetodid.
    * Paan Valitud meetodid loetleb valitud voomalli tüübi meetodid. Voomall peab sisaldama konteineri koostamise meetodit.  
8. Otsige loendist ja valige soovitud kirje.
9. Tippige väärtus väljale Voo etapi kood.
    * Sisestage lisatud meetodile vooetapi kood, mis võib olla mis tahes kood. On võimalik lisada meetodit mitu korda ja määrata erinevad vooetapi koodid. Selleks tehke lehel Vooprotsessi meetodid valik Selles voo mallis korratav.  
10. Klõpsake nuppu Salvesta.
11. Sulgege leht.

## <a name="set-up-a-container-type"></a>Konteineri tüübi häälestamine
1. Avage Laohaldus > Seadistus > Konteinerid > Konteinerite tüübid.
    * Saate määratleda oma konteinerid lehel Konteineri tüübid. Saate konfigureerida konteinerite füüsilised mõõdud, sh taara kaalu ja maksimaalse kaalu, maksimaalse mahu, pikkuse, laiuse ning kõrguse. Selles näites on meil kolmes erinevas suuruses karpe.  
2. Klõpsake valikut Uus.
3. Tippige väärtus väljale Konteineri tüübi kood.
4. Sisestage number väljale Taarakaal.
5. Sisestage number väljale Maksimaalne kaal.
6. Sisestage number väljale Maht.
7. Sisestage number väljale Pikkus.
8. Sisestage number väljale Laius.
9. Sisestage number väljale Kõrgus.
10. Sisestage väljale Kirjeldus soovitud väärtus.
11. Klõpsake nuppu Salvesta.
12. Klõpsake valikut Uus.
13. Tippige väärtus väljale Konteineri tüübi kood.
14. Sisestage väljale Kirjeldus soovitud väärtus.
15. Sisestage number väljale Taarakaal.
16. Sisestage number väljale Maksimaalne kaal.
17. Sisestage number väljale Maht.
18. Sisestage number väljale Pikkus.
19. Sisestage number väljale Laius.
20. Sisestage number väljale Kõrgus.
21. Klõpsake nuppu Salvesta.
22. Klõpsake valikut Uus.
23. Tippige väärtus väljale Konteineri tüübi kood.
24. Sisestage väljale Kirjeldus soovitud väärtus.
25. Sisestage number väljale Taarakaal.
26. Sisestage number väljale Maksimaalne kaal.
27. Sisestage number väljale Maht.
28. Sisestage number väljale Pikkus.
29. Sisestage number väljale Laius.
30. Sisestage number väljale Kõrgus.
31. Klõpsake nuppu Salvesta.
32. Sulgege leht.

## <a name="set-up-a-container-group"></a>Konteinerigrupi häälestamine
1. Avage Laohaldus > Seadistus > Konteinerid > Konteinerigrupid.
2. Klõpsake valikut Uus.
    * Saate häälestada konteineritüüpide loogilised grupid. Iga grupi puhul saate määrata järjekorra, milles soovite konteinereid pakkuda, ja täidetavate konteinerite protsendi. Kauba suuruse mõõtude alusel tehakse kindlaks, kas see mahub konteinerisse. Kasutatakse konteinerit, mille mõõdud on kaubaga kõige sarnasemad. Kui grupis on mitu konteineritüüpi, soovitame korraldada järjestuse suuruse alusel, nii et suurim konteiner on esimene, järjekorras nr 1, ja väikseim konteiner viimane.    
3. Tippige väärtus väljale Konteinerigrupi ID.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Klõpsake Uus.
6. Märkige loendis valitud rida.
7. Sisestage või valige väärtus väljal Konteineri tüüp.
8. Klõpsake Uus.
9. Märkige loendis valitud rida.
10. Sisestage või valige väärtus väljal Konteineri tüüp.
11. Klõpsake Uus.
12. Märkige loendis valitud rida.
13. Sisestage või valige väärtus väljal Konteineri tüüp.
14. Klõpsake nuppu Salvesta.
15. Sulgege leht.

## <a name="set-up-a-container-build-template"></a>Konteineri koostemalli häälestamine
1. Avage Laohaldus > Seadistus > Konteinerid > Konteineri koostemallid.
2. Klõpsake valikut Uus.
    * Konteineri koostamise mall põhineb sellel, milliseid konteinerite protsesse tehakse. Iga konteineri koostemall määratleb ühe konteineri loomise protsessi, mida kasutab voo mall. Suvandi Päringu redigeerimine abil saate määratleda tingimused, mille alusel valitud malli töödeldakse. Näiteks võite soovida käitada konteinerite loomist ainult teatud klientide, toodete või ladude puhul, või saate lisada vastavad päringuvahemikud malli. Väli Voo etapi kood näitab, kuidas konteineri koostemall on seotud voomalli etappidega. Kui voog on käivitatud, määrab see kindlaks, milliseid konteineri koostemalle kasutatakse konteineri koostamise alustamiseks. Väli Aluspäringu tüübid määrab, mida pakkida ja millel põhineb filtripäring.  
3. Märkige loendis valitud rida.
4. Tippige väärtus väljale Konteinerimalli ID.
5. Sisestage või valige väärtus väljal Konteinerigrupi ID.
6. Tippige väärtus väljale Voo etapi kood.
7. Märkige ruut Tükeldatud valiku lubamine.
8. Klõpsake nuppu Salvesta.
9. Klõpsake suvandit Konteineri koostamise piirangud.
    * Koostamisloogika pausid võimaldavad seadistada reeglid eraldusridade konteinerisse pakkimise kohta. Näiteks kui lisate välja Kauba kood, kui kauou konteineritesse määratakse, luuakse uus konteiner, kui on olemas uus kauba kood. See takistab töötajaid pakkimast kahe erineva kliendi eraldusridu samasse konteinerisse.  
10. Klõpsake valikut Uus.
11. Valige suvand väljal Tabel.
12. Sisestage väärtus väljale Vali väli.
13. Klõpsake nuppu OK.


