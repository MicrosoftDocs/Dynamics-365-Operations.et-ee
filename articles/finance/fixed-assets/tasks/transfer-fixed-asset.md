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
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0770011a76b1e4cc8b4d13e54fab2d0fba43f8a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975912"
---
# <a name="transfer-a-fixed-asset"></a>Põhivara ülekandmine

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]