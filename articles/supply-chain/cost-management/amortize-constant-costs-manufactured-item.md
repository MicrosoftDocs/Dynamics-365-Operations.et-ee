---
title: Toodetud kauba püsikulude amortiseerimine
description: Toodetud kauba püsikulud peegeldavad operatsiooni seadistusaegu ja konstantse koguse või konstantse praagi summaga komponente.
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 7ccd5ce3e2ed58db8f13eebbcfa6fe5fb544d6c7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "329455"
---
# <a name="amortize-constant-costs-for-a-manufactured-item"></a>Toodetud kauba püsikulude amortiseerimine

[!include [banner](../includes/banner.md)]

Toodetud kauba püsikulud peegeldavad operatsiooni seadistusaegu ja konstantse koguse või konstantse praagi summaga komponente. 

Saatepartii suuruse kuluarvestuse kontseptsiooni kasutatakse nende konstantsete kulude amortiseerimiseks toodetud kauba kalkuleeritud kulus. Sellel kontseptsioonil on mitmeid sünonüüme, üks neist on saatepartii suuruse raamatupidamine. Püsikulude amortiseerimise kontseptsioonil on samuti mitmeid sünonüüme, üks neist on proportsionaalsed püsikulud.

Toodetud kauba saatepartii suuruse kuluarvestuse kogust kasutatakse koosluse kalkulatsioonis. Kogus sõltub sellest, kuidas käivitate ja teostate koosluse kalkulatsiooni, vastavalt alltoodud illustratsioonile:

-   Vaikekalkulatsiooni kogus kauba koosluse kalkulatsioonis \– kauba standardse tellimuse kogus laovarude jaoks toimib vaikimisi selle saatepartii suuruse kuluarvestuse puhul, kuid vaikeväärtus võib olla suurem kogus, et peegeldada kauba tellimuskoguse kordühikut. Kauba standardset tellimuse kogust ja kordühikut saab määrata selle vaiketellimuse sätete või saidikohaste tellimuse sätete piires.
-   Määratletud arvutuskogus kauba koosluse kalkulatsioonis ? määratletud arvutuskogus toimib kauba saatepartii suuruse kuluarvestusena. Algselt kasutab kalkulatsiooni kogus määratud kauba standardse tellimuse kogust, kuid vaikeväärtust saab käsitsi alistada. Määratletud arvutuskogus tähistab määratletud kauba ja tootmise koosluse rea tüübiga toodetud komponentide puhul saatepartii suuruse kuluarvestust. See põhineb eeldusel, et komponenti toodetakse täpne kogus. Teiste toodetud komponentide, millel on koosluse rea tüüpi kaup, saatepartii suuruse kuluarvestus peegeldab nende standardset tellimuse kogust.
-   Määratletud vastavalt tellimusele tehtud arvutuse kogus toote koosluse kalkulatsioonis ? määratletud arvutuskogus toimib kauba ja selle toodetud komponentide saatepartii suuruse kuluarvestusena, kui koosluse kalkulatsioonid kasutavad vastavalt tellimusele tehtud koosnevusarvutuse režiimi. Eeldatakse, et toodetud komponente toodetakse täpne kogus, just nagu toodetud komponendi puhul, mille koosluse rea tüüp on tootmine.
-   Määratletud arvutuskogus tellimusekohases koosluse kalkulatsioonis ? tellimusekohast koosluse kalkulatsiooni saab teha rea üksuse puhul müügitellimusel, müügipakkumisel või teenusetellimusel. Määratletud arvutuskogus kasutab algse rea kauba kogust, kuid vaikekogust saab alistada. Saate valida, kas tellimuse kohane koosluse kalkulatsioon kasutab vastavalt tellimusele tehtud või mitmetasandilist koosnevusarvutuse režiimi.

Toodetud kauba amortiseeritud püsikulude arvutatud kogust nimetatakse terminiga tasud.





