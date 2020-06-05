---
title: Konteinerisse määramise seadistamine
description: Selles teemas kirjeldatakse koormuste konteineriseerimise automeerimist laohalduses.
author: ShylaThompson
manager: tfehr
ms.date: 07/22/19
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0f042e6ffe5ecf01b9e5044fc83d081528fbc56
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383293"
---
# <a name="set-up-containerization"></a>Konteinerisse määramise seadistamine

[!include [banner](../../includes/banner.md)]

Selles teemas kirjeldatakse koormuste konteineriseerimise automeerimist laohalduses. Automaatne konteinerite koostamine loob saadetiste jaoks konteinerid ja komplekteerimistööd pärast voo töötlemist ja töö read saab jagada kogustesse, mis vastavad konteineritele. See aitab laotöötajatel komplekteerida kaupu otse valitud konteinerisse. Võrreldes käsitsi pakkimise protsessiga, on sellised toimingud nagu konteinerite loomine, kaupade määramine ja konteinerite sulgemine süsteemi automatiseeritud. See protseduur kasutab demoettevõtet USMF ja selle viib läbi lao juhataja.


## <a name="set-up-a-wave-template"></a>Voomalli seadistamine
1. Avage navigeerimispaanil **Moodulid > Laohaldus > Häälestus > Vood > Voomallid**.
2. Valige suvand **Uus**.
3. Sisestage väärtus väljale **Voomalli nimi**.
4. Sisestage väärtus väljale **Voomalli kirjeldus**.
5. Sisestage või valige väärtus väljale **Sait**.
6. Sisestage või valige väärtus väljale **Ladu**.
7. Laiendage jaotist **Meetodid**. Paan **Valitud meetodid** loetleb meetodeid valitud voomalli tüübi jaoks. Voomall peab sisaldama konteineri koostamise meetodit.  
8. Sisestage väärtus väljale **Voo etapi kood**. Sisestage lisatud meetodile vooetapi kood, mis võib olla mis tahes kood. On võimalik lisada meetodit mitu korda ja määrata erinevad vooetapi koodid. Selleks valige **Selle meetodi jaoks korratav** lehel **Voo töötlemise meetodid**.  
9. Valige käsk **Salvesta**.
10. Sulgege leht.

## <a name="set-up-a-container-type"></a>Konteineri tüübi häälestamine
1. Avage navigeerimispaanil **Moodulid > Laohaldus > Häälestus > Konteinerid > Konteineri tüübid**. Võite määratleda oma konteinerid lehel **Konteineri tüübid**. Saate konfigureerida konteinerite füüsilised mõõdud, sh taara kaalu ja maksimaalse kaalu, maksimaalse mahu, pikkuse, laiuse ning kõrguse. Selles näites on meil kolmes erinevas suuruses karpe.  
2. Valige suvand **Uus**.
3. Sisestage väärtus väljale **Konteineri tüübi kood**.
4. Sisestage arv väljale **Taara kaal**.
5. Sisestage arv väljale **Maksimaalne kaal**.
6. Sisestage arv väljale **Maht**.
7. Sisestage arv väljale **Pikkus**.
8. Sisestage arv väljale **Laius**.
9. Sisestage arv väljale **Kõrgus**.
10. Sisestage väärtus väljale **Kirjeldus**.
11. Valige käsk **Salvesta**.
13. Korrake etappe 2-11 kaks korda veel, et teha kokku kolm konteineri tüüpi.
14. Sulgege leht.

## <a name="set-up-a-container-group"></a>Konteinerigrupi häälestamine
1. Avage navigeerimispaanil **Moodulid > Laohaldus > Häälestus > Konteinerid > Konteineri rühmad**.
2. Valige toimingupaanil nupp **Uus**. Saate häälestada konteineritüüpide loogilised grupid. Saate iga grupi jaoks määrata järjestuse, mille alusel konteinereid koostada, ja konteinerite täitmisprotsendi. Kauba mõõtude alusel määratakse, kas see mahub konteinerisse. Kasutatakse konteinerit, mille mõõdud on kaubaga kõige sarnasemad. Kui grupis on mitu konteineritüüpi, soovitame korraldada järjestuse suuruse alusel, nii et suurim konteiner on esimene, järjekorras nr 1, ja väikseim konteiner viimane.    
3. Sisestage **Konteineri rühma ID** väljale enne loodud väärtus.
4. Sisestage väärtus väljale **Kirjeldus**.
5. Korrake etappe 2-4 kõige kolme varem loodud konteineri tüübi jaoks.
6. Valige käsk **Salvesta**.
7. Sulgege leht.

## <a name="set-up-a-container-build-template"></a>Konteineri koostemalli häälestamine
1. Avage navigeerimispaanil **Moodulid > Laohaldus > Häälestus > Konteinerid > Konteineri ehituse mallid**.
2. Valige suvand **Uus**. Konteineri koostamise mall põhineb sellel, milliseid konteinerite protsesse tehakse. Iga konteineri koostemall määratleb ühe konteineri loomise protsessi, mida kasutab voo mall. Suvand **Päringu redigeerimine** võimaldab teil määratleda tingimusi, mille juures valitud malli töödelakse. Näiteks võite soovida käitada konteinerite loomist ainult teatud klientide, toodete või ladude puhul, või saate lisada vastavad päringuvahemikud malli. Väli **Voo etapi kood** näitab kuidas on konteineri ehitus seotud voo malli etappidega. Kui voog on käivitatud, määrab see kindlaks, milliseid konteineri koostemalle kasutatakse konteineri koostamise alustamiseks. Väli Aluspäringu tüübid määrab, mida pakkida ja millel põhineb filtripäring. 
3. Sisestage väärtus väljale **Konteineri malli ID**.
4. Sisestage või valige väärtus väljale **Konteineri rühma ID**.
5. Sisestage väärtus väljale **Voo etapi kood**.
6. Valige märkeruut **Luba tükeldatud valikud**.
7. Valige käsk **Salvesta**.
8. Valige **Konteinerite segamise piirangud**. Koostamisloogika pausid võimaldavad seadistada reeglid eraldusridade konteinerisse pakkimise kohta. Näiteks, kui lisate **Üksuse numbri välja**, kui üksused on konteineritesse määratud, luuakse uue üksuse numbri korral uus konteiner. See takistab töötajaid pakkimast kahe erineva kliendi eraldusridu samasse konteinerisse.  
9. Valige suvand **Uus**.
10. Valige suvand väljal **Tabel**.
11. Sisestage või valige väärtus väljale **Välja valik**.
12. Valige nupp **OK**.

