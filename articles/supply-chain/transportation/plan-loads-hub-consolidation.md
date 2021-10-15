---
title: Koormuste planeerimine kasutades keskuse konsolideerimise ülevaadet
description: See artikkel kirjeldab saadetiste keskusse konsolideerimise funktsiooni, kui tarnite kaupu erinevatest ladudest samale kliendile või võtate kaupu vastu mitmelt hankijalt samasse lattu.
author: Henrikan
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, TMSParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "92273"
- intro-internal
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 248bc0cc4d00dfc5ccff7edfb555af31645649d7
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574925"
---
# <a name="plan-loads-using-hub-consolidation-overview"></a>Koormuste planeerimine kasutades keskuse konsolideerimise ülevaadet

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab saadetiste keskusse konsolideerimise funktsiooni, kui tarnite kaupu erinevatest ladudest samale kliendile või võtate kaupu vastu mitmelt hankijalt samasse lattu.

Saadetisi võib olla mõistlik keskusse konsolideerida, kui tarnite kaupu erinevatest ladudest samale kliendile või kui kaupu tarnitakse mitmelt hankijalt samasse lattu.

## <a name="building-loads"></a>Koormate koostamine
Enne keskusse konsolideerimise kasutamist peate lubama valiku **Transiidi plaanimine** lehel **Transpordihalduse parameetrid**. Peate looma ka keskused, kus konsolideerimine toimub. Järgmisel diagrammil on keskusse konsolideerimise näide. Praegusel juhul lähevad erinevatest ladudest pärinevad müügitellimused samale kliendile. Peamised koormad koostatakse müügitellimuste põhjal tavalisel viisil, kasutades lehte **Koorma planeerimise töölaud**. Kahe koorma konsolideerimiseks keskusse enne nende kliendile tarnimist tehke lehe **Koorma planeerimise töölaud** väljal **Transport** valik **Keskusse konsolideerimine**. Kui valite igale koormale õige keskuse, on koormate kohaleviimise sihtkohaks keskus. Samuti on jaotises **Pakkumine ja nõudlus** lehel **Koorma planeerimise töölaud** kaks transporditaotluse rida. Seejärel saate lisada need kaks rida uuele koormale. Sellel uuel koormal on mõlemad müügitellimuse read ja pealevõtmise aadressiks keskus ning kohaleviimise aadressiks klient A. Seejärel on kolm koormat teiste koormate sarnaselt hindamiseks ja suunamiseks valmis. Saate valida igale koormale sobiva süsteemi soovitatud vedaja. [![Hub`i konsolideerimine.](./media/hubconsol.jpg)](./media/hubconsol.jpg) Sama meetodit saab kasutada ka mitme üleviimistellimuse koormate konsolideerimiseks. Sellisel juhul on eelmise diagrammi klient A ladu. Teine võimalus on konsolideerida mitme ostutellimuse koormad, kui koormad tarnitakse erinevatelt hankijatelt samasse lattu. Teil võib olla rohkem kui üks konsolideerimiskeskus ja suurema arvu koormate puhul erinevatest ladudest saate konsolideerida mitmesse keskusse. Pärast põhikoormate koostamist ja keskuse konsolideerimise valiku kasutamist koostatakse uued koormad, kasutades konsolideeritud transporditaotluse ridu. Seejärel saab koormaid hinnata ja suunata.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]