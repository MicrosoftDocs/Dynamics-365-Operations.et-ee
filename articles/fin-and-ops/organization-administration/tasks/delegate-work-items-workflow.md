---
title: Töövoos olevate tööüksuste delegeerimine
description: Kui plaanite olla kontorist väljas või muul viisil tööüksustega tegelemiseks kättesaamatu, saate tööüksused teistele kasutajatele delegeerida või ümber määrata.
author: jasongre
manager: AnnBe
ms.date: 04/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: feace647d7acef6abf86b13fcb8019c622c55ff6
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509448"
---
# <a name="delegate-work-items-in-a-workflow"></a>Tööüksuste delegeerimine töövoos

[!include [task guide banner](../../includes/task-guide-banner.md)]

## <a name="manually-delegate-a-work-item"></a>Tööüksuse käsitsi delegeerimine

Üksiku tööüksuse delegeerimiseks valige menüüst **Töövoog** suvand **Delegeeri** ja seejärel sisestage delegeeritav kasutaja ning kommentaar. See määrab tööüksuse ümber nimetatud kasutajale, nii et ta saaks selle lõpule viia.

## <a name="automatically-delegate-work-items"></a>Tööüksuste automaatne delegeerimine

Kui plaanite minna kontorist välja või olla muul moel kättesaamatu teatud ajaperioodil tööüksustega töötamiseks, saate uued tööüksused automaatselt teistele kasutajatele delegeerida, kasutades lehte **Kasutaja suvandid**.

### <a name="set-up-automatic-delegation"></a>Automaatse delegeerimise seadistamine
1. Avage Üldine > Häälestamine > Kasutaja suvandid.
2. Klõpsake vahekaarti Töövoog.
    * Veenduge, et jaotis Delegatsioon on laiendatud.    Konfigureerimaks süsteemi automaatselt tööüksuseid teistele kasutajatele delegeerima, peate looma delegeerimisreeglid, mis määravad, millal teatud tüüpi tööüksuseid delegeeritakse. Järgige delegeerimisreegli loomiseks neid juhiseid.  
3. Klõpsake vahekaarti Lisa.
4. Väljal Ulatus valige suvand.
    * Kõik – saate delegeerida kõik teile määratud tööüksused.    Moodul – saate delegeerida ainult tööüksused, mis on seotud konkreetse töövoo tüübiga. Kui valite selle suvandi, peate valima väljal Nimi töövoo tüübi.    Töövoo – saate delegeerida ainult konkreetse töövooga seotud tööüksused. Kui valite selle suvandi, peate valima töövoo väljal Nimi.  
5. Väljal Delegeeri valige kasutaja, kellele tööüksuseid delegeerida.
    * Kasutage välju Alguskuupäev ja -kellaaeg ja Lõppkuupäev ja -kellaaeg, et määrata, millal soovite tööüksuste automaatselt delegeerimist.  
6. Väljale Alguskuupäev ja -kellaaeg sisestage kuupäev ja kellaaeg.
7. Väljale Lõppkuupäev ja -kellaaeg sisestage kuupäev ja kellaaeg.
8. Märkige delegeerimisreegli aktiveerimiseks ruut Lubatud.
    * Kui valisite suvandi Ulatus sätteks Moodul, siis peate väljal Nimi valima mooduli.    Kui valisite suvandi Ulatus sätteks Töövoog, siis peate väljal Nimi valima konkreetse delegeeritava töövoo.  
9. Väljale Kommentaar sisestage kommentaar, mis selgitab tööüksuste delegeerimise põhjust.

