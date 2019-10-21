---
title: Põhivara ülekandmine
description: See tegevuse juhis kannab põhivara raamatu finantsteabe ühest finantsdimensioonist kogumist uude finantsdimensiooni kogumisse.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 167591cf160916f256e2d10f122eca312ba07639
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186827"
---
# <a name="transfer-a-fixed-asset"></a>Põhivara ülekandmine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See tegevuse juhis kannab põhivara raamatu finantsteabe ühest finantsdimensioonist kogumist uude finantsdimensiooni kogumisse.  See kasutab USMF-i juriidilise isiku puhul raamatupidaja rolli ja demoandmeid.

1. Avage navigeerimispaanil **Moodulid > Põhivara > Põhivara > Põhivara**.
2. Leidke ja valige loendist vara, mida soovite soetada.
3. Klõpsake toimingupaanil **Põhivara**.
4. Klõpsake **Põhivara edastamine**.
5. Sisestage kuupäev väljale **Edastuse kuupäev**.
6. Sisestage ülekandmise kirjeldamiseks kommentaarid.
    
    Selles loendis kuvatakse kõik põhivara raamatud.  
7. Märkige raamatud, mille soovite uude finantsdimensiooni kogumisse üle kanda.
    * Loend kuvab valitud raamatu puhul olemasolevad finantsdimensiooni väärtused.  
    * Valige finantsdimensioon, mida soovite valitud põhivara raamatu puhul värskendada.  
8. Klõpsake väljal **Finantsdimensioon** ripplonedi nuppu otsingu avamiseks.
    * Vajaduse korral määrake muid finantsdimensiooni väärtusi.  
    * Kõik finantsdimensiooni väärtused muutuvad ülekande ilmnemisel, olenemata sellest, kas väärtus on sisestatud või tühjaks jäetud. Näiteks kui sisestasite väärtuse suvandi BusinessUnit puhul ja jätsite suvandite CostCenter ja Osakond finantsdimensioonid tühjaks. Kui teie konto struktuur lubab jätta parameetrite CostCenter ja Osakond väärtused tühjaks, on ülekandmise tulemusena igas väärtusmudelis parameetril BusinessUnit uus väärtus ja parameetrite CostCenter ja Osakond väärtus tühi.  
9. Klõpsake **Värskenda**.
    * Teil on võimalus muudatusi enne ülekande lõpetamist vaadata.  
    * Enne põhivara raamatu ülekandmist vaadake tulemusi.  
10. Klõpsake **Edasta**.

