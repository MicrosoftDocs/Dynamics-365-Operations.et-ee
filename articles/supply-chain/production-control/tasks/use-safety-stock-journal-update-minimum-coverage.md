---
title: Puhvervaru abil minimaalse laovaru uuendamine
description: See protseduur näitab, kuidas arvutada varasemate kannete põhjal minimaalse laovaru soovitusi ja uuendada siis soovituste abil kauba laovaru.
author: ChristianRytt
manager: tfehr
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 95dec1dba97923e58cfb603434a01cab6f66a3de
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252794"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a>Puhvervaru abil minimaalse laovaru uuendamine

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas arvutada varasemate kannete põhjal minimaalse laovaru soovitusi ja uuendada siis soovituste abil kauba laovaru. Seda tehakse puhvervaru töölehe abil. Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid. See ülesanne on mõeldud tootmise plaanijale minimaalsete laovarude säilitamiseks.


## <a name="create-a-new-safety-stock-journal-name"></a>Uue puhvervaru töölehe nime loomine
1. Avage **Navigeerimispaneelil** **Koondplaneerimine > Seadistus > Puhvervaru töölehe nimed**.
2. Klõpsake valikut **Uus**.
3. Tippige väljale **Nimi** väärtus Materjal.
4. Tippige väljale **Kirjeldus** väärtus Materjal.
5. Sulgege leht.

## <a name="create-a-safety-stock-journal"></a>Puhvervaru töölehe loomine
1. Avage **Navigeerimispaneelil** **Koondplaneerimine > Koondplaneerimine > Käivita > Puhvervaru arvutus**.
2. Klõpsake valikut **Uus**.
3. Sisestage või valige väärtus väljal **Nimi**. Valige puhvervaru töölehe nimi, mille lõite, nt Materjal.  
4. Klõpsake suvandit **Loo read**.
5. Sisestage kuupäev väljale **Alates kuupäevast**.  
6. Sisestage kuupäev väljale **Lõppkuupäev**.
7. Klõpsake valikut **OK**. See loob read dimensioonidele, millel on laokanded.  

## <a name="calculate-proposal"></a>Arvuta soovitus
1. Klõpsake valikut **Arvuta soovitus**.
2. Tehke valik **Kasuta täitmisaja jooksul keskmist väljaminekut**.
3. Määrake valiku **Korrutustegur** väärtuseks 10. Tegurit Korruta kasutatakse soovituse korrigeerimiseks. Kuna demoandmetel on vaid mõned kanded, tuleb realistliku soovituse saamiseks tegur määrata.  
4. Klõpsake valikut **OK**. Kerige alla M0002 ja M0003 leidmiseks. Vaadake veergu **Arvutatud miinimumkogus**.   

## <a name="update-minimum-quantity"></a>Miinimumkoguse uuendamine
1. Sisestage number väljale **Uus miinimumkogus**. Uuendage väärtust Uus miinimumkogus nii, et see vastaks väärtusele jaotises Arvutatud miinimumkogus. Kui Arvutatud miinimum on null, võite sisestada soovitud tulevase väärtuse. Näiteks võite sisestada sellele väljale väärtuse Arvutatud miinimumkogus M0002 kohta, millel on ladu 12.  
2. Otsige loendist ja valige soovitud kirje. Näiteks võite valida M0002, millel on ladu 12.  
3. Sisestage number väljale **Uus miinimumkogus**. Uuendage väärtust Uus miinimumkogus nii, et see vastaks väärtusele jaotises Arvutatud miinimumkogus. Kui Arvutatud miinimum on null, võite sisestada soovitud tulevase väärtuse.  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>Uue miinimumkoguse sisestamine ja tulemuse kinnitamine
1. Klõpsake käsku **Sisesta**.
2. Klõpsake valikut **OK**.
3. Klõpsake, et järgida linki väljal **Kaubakood**.
4. Klõpsake, et järgida linki väljal **Kaubakood**.
5. Klõpsake **Toimingupaanil** valikut Plaan.
6. Klõpsake valikut **Kauba laovarud**. Pange tähele, et väärtuseks **Miinimumkogus** on määratud uus miinimumkogus puhvervaru töölehelt.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]