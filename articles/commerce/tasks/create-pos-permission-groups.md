---
title: Kassa loagruppide loomine
description: Selles teemas tutvustatakse, kuidas luua kassa loagruppe.
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
ms.openlocfilehash: 1d4634ec275d3d1c2a131c4c1d61cc983e485b14
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798485"
---
# <a name="create-pos-permission-groups"></a>Kassa loagruppide loomine

[!include [banner](../includes/banner.md)]

Selles teemas tutvustatakse, kuidas luua kassa loagruppe. Selle tegevuse loomisel kasutati demoettevõtte USRT-i andmeid. See ülesanne on mõeldud kaubandustoimingute halduri rolli jaoks.

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