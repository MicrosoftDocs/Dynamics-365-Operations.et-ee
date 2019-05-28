---
title: Tootmistellimuste lõpetatuks kinnitamine
description: Lõpetatuks kinnitamine on tootmisetapp. Selles etapid kinnitatakse valmistoode ja see teisaldatakse tootmistellimusest varudesse.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 61c12ee3a831abcb46af18645eba55fe100c99c9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567394"
---
# <a name="report-production-orders-as-finished"></a>Tootmistellimuste lõpetatuks kinnitamine

[!include [banner](../includes/banner.md)]

Lõpetatuks kinnitamine on tootmisetapp. Selles etapid kinnitatakse valmistoode ja see teisaldatakse tootmistellimusest varudesse.

Kui lõpetatud kaupade kogus on kinnitatud tootmistellimusel lõpetatuks, uuendatakse see varudes laoseisuna. Algselt plaanitud tellimuse koguse osalised kogused saab kinnitada lõpetatuks. Samuti on võimalik kinnitada vigased kogused koos seostatud vea põhjusega, kui koguste lõpetamist kinnitatakse. Kui tootmistellimus jõuab etappi Lõpetamine kinnitatud, näitab see, et tootmistellimuses rohkem koguseid ei kinnitata.
Järgmised omadused seostatakse ka protsessiga **Kinnita lõpetamine**.
-   On võimalik seadistada toormaterjali tarbimine ja kinnitatud kogusega proportsionaalne aeg (tagantjärele)
-   Laoprotsessideks lubatud kaupadele saab luua ladustamistöö.
-   Saab seadistada, et pearaamatukontodele teatatakse lõpetatud kaupade plaanitud või standardne kuluväärtus.
-   Kinnitatud kogusele saab luua kvaliteettellimuse kvaliteediseose seadistuse alusel.

Kogus kinnitatakse väljastuskohta. Seejärel luuakse laotöö, et teisaldada kogus väljastuskohast selle lõppsihtkohta, mille määratleb ladustamistöö asukoha korraldus.

-   Kvaliteettellimuse saab luua, kui tootmistellimuse kinnitatakse lõpetatuks, kui kvaliteediseos on seadistatud.

## <a name="set-a-production-order-to-reporting-as-finished"></a>Tootmistellimuse lõpetatuks kinnitamise määramine
Saate määrata tootmistellimuse väärtuseks **Kinnita lõpetamine** standardse tootmistellimuse värskendamisfunktsiooni kaudu või protsessikaardi ja töökaardi töölehtede kaudu või töölehe **Kinnita lõpetamine** kaudu. Saate oleku värskendada ka väärtusele **Kinnita lõpetamine** töökaardi terminali ja töökaardi seadme lehtede kaudu, kui kinnitate tootmistellimuse viimase töö. Lõpuks saate lubada suvandi **Kinnita lõpetamine** kaasaskantava laoseadme lahenduse protsessina.  



