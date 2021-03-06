---
title: Hübriid-klienditellimused
description: Hübriid-klienditellimus on üksik tellimus, mis sisaldab tooteid, mille klient saab kauplusest kaasa võtta, ja tooteid, mis hiljem peale võetakse või välja saadetakse.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6357c034059523f83ba05a1da53cae691ef74758
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798933"
---
# <a name="hybrid-customer-orders"></a>Hübriid-klienditellimused

[!include [banner](includes/banner.md)]

Hübriid-klienditellimus on üksik tellimus, mis sisaldab tooteid, mille klient saab kauplusest kaasa võtta, ja tooteid, mis hiljem peale võetakse või välja saadetakse.

Commerce'is saate valida kas klienditellimuse kõigi toodete tarnimise või kliendi tellimuse valitud toodete tarnimise. Tarnimiseks märgitud tooteridade eest esitatakse arve pärast tellimuse loomist automaatselt, sama toimub ka tellimuse puhul, mis võetakse peale pärast tellimuse loomist. Hübriidtellimuste eest tasumisele kuuluv summa määratakse, lisades deposiidiprotsendi komplekteeritavate ja lähetatavate toodete ridadele koos tarneridade täieliku summaga. Hübriid-tellimuste puhul vahetab süsteem kliendi tellimuse režiimi ja sularaharežiimi järgmiselt.

- Kui kõigi ostukorvis olevate toodete puhul on tarneviisiks määratud **Sularahatarne**, siis käsitletakse kannet sularahakandena.
- Kui mõnele ostukorvi reale on määratud **Komplekteeri** või **läheta tarne**, siis käsitletakse tellimust kliendi tellimuse kandena.

Kui on valitud ostukorvi rida ja **Komplekteeri valitud**, **Saada valitud** või **Tarni valitud**, siis määratakse selle tarneviisiga ainult konkreetne ostukorvi rida. Sellisel juhul jätkub toimingu allavoolu voog tavalisel viisil. Kuid kui on valitud **Komplekteeri valitud**, **Saada valitud** või **Tarni valitud** ja ostukorvi rida ei valita, siis avaneb uus leht, millel on loetletud kõik ostukorvi read. Sellel ekraanil saate valida korraga mitu rida tarneviisi määramiseks. Kui kasutate ridade valimiseks seda meetodit, siis tühistatakse mis tahes reale eelnevalt määratud tarneviis.

## <a name="additional-resources"></a>Lisaressursid

[Kliendi tellimused Modern POS-is (MPOS-is)](customer-orders-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]