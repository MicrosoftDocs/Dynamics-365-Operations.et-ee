---
title: Kaupluse varude haldamine
description: "See artikkel kirjeldab dokumendi tüüpe, mida saate kasutada varude haldamiseks."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5e5043d5951015fc14d29989ef4cab20a8b24f3b
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="manage-store-inventory"></a>Kaupluse varude haldamine

[!include[banner](includes/banner.md)]


See artikkel kirjeldab dokumendi tüüpe, mida saate kasutada varude haldamiseks.

Organisatsiooni varude haldamiseks saab kasutada järgmist tüüpi dokumente.

## <a name="purchase-orders"></a>Ostutellimused
Ostutellimused koostatakse peakontoris. Kui ostutellimuse päisesse on kaasatud jaemüügiladu, saab tellimust vastu võtta kaupluses, kasutades rakenduses Microsoft Dynamics 365 for Operations – jaemüük kaasaegset kassat (MPOS) või pilve POS-i. Pärast kaupluses vastuvõetud koguste sisestamist saab need kohalikult täiendavaks modifitseerimiseks salvestada. Teise võimalusena saab kogused kooskõlastada ja saata peakontorisse. Peakontoris kuvatakse kaupluses vastu võetud kogused rakenduses Dynamics 365 for Operations ostutellimuse real **Kohe tarnitav**.

## <a name="transfer-orders"></a>Üleviimistellimused
Üleviimistellimuses saab määrata, et konkreetne kauplus on koht, kust kaupu saab teele panna. Sellisel juhul kuvatakse üleviimistellimus kaupluses MPOS-is või pilve POS-is komplekteerimistaotlusena. Pärast taotletud koguste komplekteerimist need kooskõlastatakse ja saadetakse peakontorisse. Peakontoris kuvatakse kaupluses komplekteeritud kogused rakenduses Dynamics 365 for Operations üleviimistellimuse väljal **Läheta kohe**. Üleviimistellimuses saab määrata, et konkreetne kauplus on koht, kuhu kaupu saab saata. Sellisel juhul kuvatakse üleviimistellimus kaupluses MPOS-is või pilve POS-is vastuvõtmistaotlusena. Pärast kaupluses vastuvõetud koguste sisestamist saab need kohalikult täiendavaks modifitseerimiseks salvestada. Teise võimalusena saab kogused kooskõlastada ja saata peakontorisse. Peakontoris kuvatakse kaupluses vastu võetud kogused rakenduses Dynamics 365 for Operations üleviimistellimuse real **Kohe tarnitav**.

## <a name="stock-counts"></a>Laoinventuurid
Laoinventuurid võivad olla plaanipärased või plaanivälised. Plaanitud laoinventuurid algatab peakontor, mis määrab ka loendatavad kaubad. Peakontor loob inventuuridokumendi, mida saab vastu võtta kaupluses, kus vaba laovaru kogused sisestatakse MPOS-is või pilve POS-is. Plaanimata laoinventuurid käivitatakse kaupluses ja vaba laoseisu koguseid värskendatakse MPOS-is või pilve POS-is. Erinevalt ajastatud laoinventuuridest puudub plaanimata laovarudel eelmääratletud kaupade loend. Mõlemat tüüpi laoinventuuri lõpetamisel see kooskõlastatakse ja saadetakse peakontorisse. Peakontoris inventuur kinnitatakse ja sisestatakse.






