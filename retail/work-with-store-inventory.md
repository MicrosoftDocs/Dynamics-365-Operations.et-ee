---
title: Kaupluse varude haldamine
description: Selles artiklis kirjeldatakse dokumendid, mille abil saate hallata varude liigid.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fbe9945799f1e65ed6ad624a3df270fa4eb72b88
ms.lasthandoff: 03/31/2017


---

# <a name="manage-store-inventory"></a>Kaupluse varude haldamine

Selles artiklis kirjeldatakse dokumendid, mille abil saate hallata varude liigid.

Organisatsiooni varude haldamiseks saab kasutada järgmist tüüpi dokumente.

## <a name="purchase-orders"></a>Ostutellimused
Ostutellimused koostatakse peakontoris. Kui jaemüügi ladu sisaldab kliendile, et saab vastu poest kaasaegne POS (MPOS) või pilve POS kasutades operatsioonide - jaemüügi Microsoft Dynamics 365. Kui kogused, poe juures on sisestanud, salvestada lokaalselt täiendavat muutmist. Teise võimalusena saab kogused kooskõlastada ja saata peakontorisse. Peakontoris, saadi poest kogused kuvatakse Dynamics 365 korral on **kohe** ostutellimuse välja.

## <a name="transfer-orders"></a>Üleviimistellimused
Üleviimistellimuses saab määrata, et konkreetne kauplus on koht, kust kaupu saab teele panna. Sel juhul kuvatakse maksekorralduse poodi komplekteerimislehe päringuga MPOS või pilve POS. Pärast seda, kui on taotletud kogused võetakse peale, nad on pühendunud ja saadetakse peakontor. Peakontoris, korjati poest kogused kuvatakse Dynamics 365 korral on **saatke kohe** üleviimiskorralduse välja. Üleviimistellimuses saab määrata, et konkreetne kauplus on koht, kuhu kaupu saab saata. Sel juhul maksekorralduse kuvatakse poes MPOS või pilve POS vastuvõtva taotluse. Kui kogused, poe juures on sisestanud, salvestada lokaalselt täiendavat muutmist. Teise võimalusena saab kogused kooskõlastada ja saata peakontorisse. Peakontoris, saadi poest kogused kuvatakse Dynamics 365 korral on **kohe** üleviimiskorralduse välja.

## <a name="stock-counts"></a>Laoinventuurid
Laoinventuurid võivad olla plaanipärased või plaanivälised. Plaanitud laoinventuurid algatab peakontor, mis määrab ka loendatavad kaubad. Peakontor loob poest, kus tegelik vaba varude on kantud MPOS või pilve POS summa inventuuri dokument. Planeerimata varude arv on algatatud kaupluse ja tegeliku vaba varude on uuendatud MPOS või pilve POS. Erinevalt ajastatud varude vähesus, planeerimata varude arv ei ole eelnevalt määratletud loetelu. Mõlemat tüüpi laoinventuuri lõpetamisel see kooskõlastatakse ja saadetakse peakontorisse. Peakontoris inventuur kinnitatakse ja sisestatakse.




