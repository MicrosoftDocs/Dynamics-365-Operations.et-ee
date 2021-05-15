---
title: Tööaja mallide loomine
description: Tööajamallid määratlevad kogu nädala tööaja ja neid kasutatakse ajavahemiku tööaegade loomiseks.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed1981b7c1427c902f237f0aa95f63e89bc345ab
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920924"
---
# <a name="create-working-time-templates"></a>Tööaja mallide loomine

[!include [banner](../../includes/banner.md)]

Tööajamallid määratlevad kogu nädala tööaja ja neid kasutatakse ajavahemiku tööaegade loomiseks. See protseduur näitab, kuidas tööajamalli määratleda, kasutades tööaja plaanimise atribuute tööajaintervallide kategooriatesse jaotamiseks. Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.

1. Valige **Tööruumid > Ressursi elutsükli haldus**.
1. Valige **Tööaja mallide loomine**.

## <a name="create-working-time-template"></a>Tööajamalli loomine

1. Valige suvand **Uus**.
1. Tippige väärtus väljale **Tööaja mall**.
1. Sisestage väärtus väljale **Nimi**.
1. Laiendage jaotist **Esmaspäev**.
1. Valige **Lisa**.
1. Sisestage kellaaeg väljale **Alates**.
    * Määrake kellaaeg, millal töö hommikul algab.  
1. Sisestage kellaaeg väljale **Kuni**.
    * Määrake töötajate lõunavaheaja alguskellaaeg.  
1. Valige **Lisa**.
1. Sisestage kellaaeg väljale **Alates**.
    * Määrake töö jätkamise kellaaeg pärast lõunat.  
1. Sisestage kellaaeg väljale **Kuni**.
    * Määrake tööpäeva lõpp.  

## <a name="replicate-working-times-to-all-week-days"></a>Tööaegade kopeerimine kõigile nädalapäevadele

1. Valige suvand **Kopeeri päev**.
    * Kopeerige tööajamääratlused esmaspäevalt teisipäevale.  
1. Valige nupp **OK**.
1. Valige suvand **Kopeeri päev**.
    * Kopeerige tööajamääratlused esmaspäevalt kolmapäevale.  
1. Tehke valik väljal **Kuni nädalapäevani**.
1. Valige nupp **OK**.
1. Valige suvand **Kopeeri päev**.
    * Kopeerige tööajamääratlused esmaspäevalt neljapäevale.  
1. Tehke valik väljal **Kuni nädalapäevani**.
1. Valige nupp **OK**.
1. Valige suvand **Kopeeri päev**.
    * Kopeerige tööajamääratlused esmaspäevalt reedele.  
1. Tehke valik väljal **Kuni nädalapäevani**.
1. Valige nupp **OK**.

## <a name="define-time-slots-for-special-operations"></a>Eritoimingute ajavahemike määratlemine

1. Laiendage jaotist **Reede**.
1. Otsige loendist ja valige soovitud kirje.
1. Valige või sisestage väärtus väljal **Atribuut**.
1. Otsige loendist ja valige soovitud kirje.
1. Valige või sisestage väärtus väljal **Atribuut**.

## <a name="mark-weekend-days-as-closed-for-pickup"></a>Puhkepäevade märkimine komplekteerimiseks suletuks

1. Laiendage jaotist **Laupäev**.
1. Valige väljal *Komplekteerimiseks suletud* suvand **Jah**.
1. Laiendage jaotist **Pühapäev**.
1. Valige väljal *Komplekteerimiseks suletud* suvand **Jah**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]