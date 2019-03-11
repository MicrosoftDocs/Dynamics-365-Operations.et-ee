---
title: Põhivara ülekandmine
description: See tegevuse juhis kannab põhivara raamatu finantsteabe ühest finantsdimensioonist kogumist uude finantsdimensiooni kogumisse.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb8a5b94d9a0bb510daa2a698524e0c380597991
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "357193"
---
# <a name="transfer-a-fixed-asset"></a>Põhivara ülekandmine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See tegevuse juhis kannab põhivara raamatu finantsteabe ühest finantsdimensioonist kogumist uude finantsdimensiooni kogumisse.  See kasutab USMF-i juriidilise isiku puhul raamatupidaja rolli ja demoandmeid.

1. Minge jaotisse Põhivarad > Põhivarad > Põhivarad.
2. Leidke ja valige loendist vara, mida soovite soetada.
3. Klõpsake toimingupaanil suvandit Põhivara.
4. Klõpsake suvandit Põhivara ülekandmine.
5. Sisestage kuupäev väljale Ülekandmise kuupäev.
6. Sisestage ülekandmise kirjeldamiseks kommentaarid.
    * Selles loendis kuvatakse kõik põhivara raamatud.  
7. Märkige raamatud, mille soovite uude finantsdimensiooni kogumisse üle kanda.
    * Loend kuvab valitud raamatu puhul olemasolevad finantsdimensiooni väärtused.  
    * Valige finantsdimensioon, mida soovite valitud põhivara raamatu puhul värskendada.  
8. Klõpsake väljal Finantsdimensioon otsingu avamiseks ripploendi nuppu.
    * Vajaduse korral määrake muid finantsdimensiooni väärtusi.  
    * Kõik finantsdimensiooni väärtused muutuvad ülekande ilmnemisel, olenemata sellest, kas väärtus on sisestatud või tühjaks jäetud. Näiteks kui sisestasite väärtuse suvandi BusinessUnit puhul ja jätsite suvandite CostCenter ja Osakond finantsdimensioonid tühjaks. Kui teie konto struktuur lubab jätta parameetrite CostCenter ja Osakond väärtused tühjaks, on ülekandmise tulemusena igas väärtusmudelis parameetril BusinessUnit uus väärtus ja parameetrite CostCenter ja Osakond väärtus tühi.  
9. Klõpsake käsku Uuenda.
    * Teil on võimalus muudatusi enne ülekande lõpetamist vaadata.  
    * Enne põhivara raamatu ülekandmist vaadake tulemusi.  
10. Klõpsake käsku Ülekanne.

