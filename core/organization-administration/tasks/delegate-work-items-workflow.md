--- 
title: "Töövoos olevate tööüksuste delegeerimine"
description: "Kui plaanite olla kontorist väljas või muul viisil tööüksustega tegelemiseks kättesaamatu, saate tööüksused teistele kasutajatele delegeerida või ümber määrata."
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 30415b28166d5551f43da04a28b0a5194323f2ab
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="delegate-work-items-in-a-workflow"></a>Töövoos olevate tööüksuste delegeerimine

[!include[task guide banner](../../includes/task-guide-banner.md)]

Kui plaanite olla kontorist väljas või muul viisil tööüksustega tegelemiseks kättesaamatu, saate tööüksused teistele kasutajatele delegeerida või ümber määrata. See protseduur aitab teil konfigureerida süsteemi automaatselt delegeerima teie tööüksused teisele kasutajale.



Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="set-up-automatic-delegation"></a>Automaatse delegeerimise seadistamine
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

