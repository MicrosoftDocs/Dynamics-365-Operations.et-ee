---
title: Töövoos olevate tööüksuste delegeerimine
description: Kui plaanite olla kontorist väljas või muul viisil tööüksustega tegelemiseks kättesaamatu, saate tööüksused teistele kasutajatele delegeerida või ümber määrata.
author: ChrisGarty
manager: AnnBe
ms.date: 06/23/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d98d84b89f1f3322a9c896b74b63a3b6425b13b
ms.sourcegitcommit: 267864eb0dccd6e26d49d280bd4ad1b770a73a77
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/26/2020
ms.locfileid: "3515760"
---
# <a name="delegate-work-items-in-a-workflow"></a>Tööüksuste delegeerimine töövoos

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a>Tööüksuse käsitsi delegeerimine

Üksiku tööüksuse delegeerimiseks valige menüüst **Töövoog** suvand **Delegeeri** ja seejärel sisestage delegeeritav kasutaja ning kommentaar. See määrab tööüksuse ümber nimetatud kasutajale, nii et ta saaks selle lõpule viia.

## <a name="manually-delegate-multiple-work-items"></a>Mitme tööüksuse käsitsi delegeerimine

Mitut tööüksust saab korraga delegeerida lehelt **Minule määratud tööüksused**. Järgmised töövoo tüübid sobivad hulgidelegeerimiseks: ostulepingu kinnitamise töövoog, ostutellimuse töövoog, ostutaotluse ülevaatus ja hankija arve töövoog. Funktsioon **Mitme tööüksuse delegeerimine** on vaikimisi keelatud ja seda saab lubada jaotises **Tööruumid > Funktsioonihaldus**. Selle funktsiooni lubamiseks abi saamiseks võtke ühendust oma süsteemiadministraatoriga.
1.  Avage jaotis **Üldine > Üldine > Tööüksused > Mulle määratud tööüksused**.
2.  Valige delegeeritavad tööüksused.
3.  Klõpsake menüül **Tööüksuste delegeerimine**.
4.  Väljal **Kasutaja** valige kasutaja, keda soovite määrata tööüksuseid delegeerima.
5.  Väljale **Kommentaar** sisestage kommentaar, mis selgitab, miks te tööüksusi delegeerite.
6.  Tööüksuse delegeerimise lõpule viimiseks klõpsake nuppu **Tööüksuste delegeerimine**.

## <a name="automatically-delegate-work-items"></a>Tööüksuste automaatne delegeerimine

Kui plaanite minna kontorist välja või olla muul moel kättesaamatu teatud ajaperioodil tööüksustega töötamiseks, saate uued tööüksused automaatselt teistele kasutajatele delegeerida, kasutades lehte **Kasutaja suvandid**.

### <a name="set-up-automatic-delegation"></a>Automaatse delegeerimise seadistamine
1. Avage **Üldine > Seadistus > Kasutaja suvandid**.
2. Klõpsake vahekaarti **Töövoog**. Veenduge, et jaotis Delegeerimine on laiendatud. Konfigureerimaks süsteemi automaatselt tööüksuseid teistele kasutajatele delegeerima, peate looma delegeerimisreeglid, mis määravad, millal teatud tüüpi tööüksuseid delegeeritakse. Järgige delegeerimisreegli loomiseks neid juhiseid.  
3. Klõpsake käsku **Lisa**.
4. Väljal **Ulatus** valige sobiv variant.
    - Kõik – saate delegeerida kõik teile määratud tööüksused.
    - Moodul – saate delegeerida ainult tööüksused, mis on seotud konkreetse töövoo tüübiga. Kui valite selle suvandi, peate valima väljal Nimi töövoo tüübi.
    - Töövoo – saate delegeerida ainult konkreetse töövooga seotud tööüksused. Kui valite selle suvandi, peate valima töövoo väljal Nimi.  
5. Väljal **Delegaat** valige kasutaja, keda soovite määrata tööüksuseid delegeerima. Kasutage välju Alguskuupäev ja -kellaaeg ja Lõppkuupäev ja -kellaaeg, et määrata, millal soovite tööüksuste automaatselt delegeerimist.  
6. Väljale **Alguskuupäev/kellaaeg** sisestage kuupäev ja kellaaeg.
7. Väljale **Lõppkuupäev/kellaaeg** sisestage kuupäev ja kellaaeg.
8. Valige märkeruut **Lubatud**, et aktiveerida delegeerimise reegel. Kui valisite ulatuseks **Moodul**, peate seejärel valima mooduli väljal Nimi. Kui valisite ulatuseks **Töövoog**, peate seejärel valima konkreetse töövoo, mida delegeerida väljal Nimi.  
9. Väljale **Kommentaar** sisestage kommentaar, mis selgitab, miks te tööüksusi delegeerite.

