---
title: "Tootmistellimuste lõpetatuks kinnitamine"
description: "Lõpetatuks kinnitamine on tootmisetapp. Selles etapid kinnitatakse valmistoode ja see teisaldatakse tootmistellimusest varudesse."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 80a882e51332d87835bdfb41a1bb1fcda2471f02
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="report-production-orders-as-finished"></a>Tootmistellimuste lõpetatuks kinnitamine

[!INCLUDE [banner](../includes/banner.md)]

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




