---
title: Koormate plaanimine keskuse konsolideerimisega
description: "See artikkel kirjeldab saadetiste keskusse konsolideerimise funktsiooni, kui tarnite kaupu erinevatest ladudest samale kliendile või võtate kaupu vastu mitmelt hankijalt samasse lattu."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSLoadPlanningWorkbench
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 92273
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 080d46281416835729fd1595079939cd30c9aed8
ms.lasthandoff: 03/31/2017


---

# <a name="plan-loads-using-hub-consolidation"></a>Koormate plaanimine keskuse konsolideerimisega

See artikkel kirjeldab saadetiste keskusse konsolideerimise funktsiooni, kui tarnite kaupu erinevatest ladudest samale kliendile või võtate kaupu vastu mitmelt hankijalt samasse lattu.

Saadetisi võib olla mõistlik keskusse konsolideerida, kui tarnite kaupu erinevatest ladudest samale kliendile või kui kaupu tarnitakse mitmelt hankijalt samasse lattu.

## <a name="building-loads"></a>Koormate koostamine
Enne keskusse konsolideerimise kasutamist peate lubama valiku **Transiidi plaanimine **lehel **Transpordihalduse parameetrid**. Peate looma ka keskused, kus konsolideerimine toimub. Järgmisel diagrammil on keskusse konsolideerimise näide. Praegusel juhul lähevad erinevatest ladudest pärinevad müügitellimused samale kliendile. Peamised koormad koostatakse müügitellimuste põhjal tavalisel viisil, kasutades lehte **Koorma planeerimise töölaud**. Kahe koorma konsolideerimiseks keskusse enne nende kliendile tarnimist tehke lehe **Koorma planeerimise töölaud** väljal **Transport** valik **Keskusse konsolideerimine**. Kui valite igale koormale õige keskuse, on koormate kohaleviimise sihtkohaks keskus. Samuti on jaotises **Pakkumine ja nõudlus** lehel **Koorma planeerimise töölaud** kaks transporditaotluse rida. Seejärel saate lisada need kaks rida uuele koormale. Sellel uuel koormal on mõlemad müügitellimuse read ja pealevõtmise aadressiks keskus ning kohaleviimise aadressiks klient A. Seejärel on kolm koormat teiste koormate sarnaselt hindamiseks ja suunamiseks valmis. Saate valida igale koormale sobiva süsteemi soovitatud vedaja. [![Rummu konsolideerimise](./media/hubconsol.jpg)](./media/hubconsol.jpg) konsolideerida mitu üleviimistellimuste jaoks raskuste abil saate ka sama meetodit. Sellisel juhul on eelmise diagrammi klient A ladu. Teine võimalus on konsolideerida mitme ostutellimuse koormad, kui koormad tarnitakse erinevatelt hankijatelt samasse lattu. Teil võib olla rohkem kui üks konsolideerimiskeskus ja suurema arvu koormate puhul erinevatest ladudest saate konsolideerida mitmesse keskusse. Pärast põhikoormate koostamist ja keskuse konsolideerimise valiku kasutamist koostatakse uued koormad, kasutades konsolideeritud transporditaotluse ridu. Seejärel saab koormaid hinnata ja suunata.


