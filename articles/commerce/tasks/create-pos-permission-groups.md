---
title: " Kassa loagruppide loomine"
description: See artikkel selgitab, kuidas kassa loagruppi luua.
author: scott-tucker
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 009f311dd00f48edb8c0f6622f0a5107881ab2ca
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905420"
---
# <a name="create-pos-permission-groups"></a> Kassa loagruppide loomine

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas kassa loagruppi luua. Selle tegevuse loomisel kasutati demoettevõtte USRT-i andmeid. See ülesanne on mõeldud kaubandustoimingute halduri rolli jaoks.

1. Avage navigeerimispaanil **Moodulid > Jaemüük ja kaubandus > Töötajad > Loagrupid**.
2. Valige suvand **Uus**.
3. Väljale **Kassa loagrupi ID** sisestage väärtus.
4. Sisestage väärtus väljale **Kirjeldus**.
5. Valige väärtus **Jah** väljal **Kellaaja kirjete kuvamine**. Saate nüüd oma kassalubade grupile erinevaid lube anda või neid eemaldada. Mõne loa jaoks saate määrata väärtuse, mida kasutatakse hindamiseks, kas kassa kasutaja saab seda toimingut teha. See tegevusjuhend annab mõned load, mida kassapidajale võidakse määrata.  
6. Valige väärtus **Jah** väljal **Luba tellimuse loomine**.
7. Valige väärtus **Jah** väljal **Luba tellimuse redigeerimine**.
8. Valige väärtus **Jah** väljal **Luba tellimuse toomine**.
9. Valige väärtus **Jah** väljal **Luba parooli muutmine**.
10. Valige väärtus **Jah** väljal **Luba pimedalt sulgemine**.
11. Valige käsk **Salvesta**. Pärast muudatuste salvestamist peate käivitama personali jaotusgraafiku, et muutused ärikanalitesse edastada. 
12. Navigeerimispaanil avage **Moodulid > Personaliosakond > Tööd > Tööd**.
13. Järgmisena määrame kassalubade grupi töö järgi. Otsige loendist ja valige soovitud kirje.
14. Valige suvand **Redigeeri**.
15. Laiendage jaotist **Töö klassifikatsioon**.
16. Sisestage või valige väärtus väljal POS permission group (Kassalubade grupp). Kõik töötajad, kelle ametikohad sellele tööle vastavad, kasutavad selle kassalubade grupi sätteid, kui töötajate kassalube ei ole nende ametikoha tasemel tühistatud.  
17. Valige käsk **Salvesta**. Pärast muudatuste salvestamist peate käivitama personali jaotusgraafiku, et muutused kanalitesse edastada.  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]