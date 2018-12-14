---
title: PowerAppsi halduskeskuses ei saa keskkonda luua
description: See teema selgitab, mida teha, kui administraator ei saa Microsoft PowerAppsi halduskeskuses keskkonda luua.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 6f9b7ceef6895b295e6ae5a50d8ac7970497efe5
ms.contentlocale: et-ee
ms.lasthandoff: 12/04/2018

---

# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a>PowerAppsi halduskeskuses ei saa keskkonda luua

[!include [banner](includes/banner.md)]

**Probleem**

- Rentniku/keskkonna administraator ei saa Microsoft PowerAppsi halduskeskuses keskkonda luua.
- Litsents, mis annab kasutajatele õiguse teostada keskkonna loomise etappi, ei ole määratud otse seda etappi teostavale kasutajale.

**Lahendus**

Veenduge, et rentniku administraator oleks määranud kehtiva PowerApps P2 litsentsi otse kasutajale, kes teostab keskkonna loomise etappi. Siit leiate Microsoft Dynamicsi teenuseplaanid, mis annavad selle õiguse.

| Üldine toote varude arvestusühik (SKU)       | PowerApps P2 teenuseplaan  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | PowerApps for Dynamics 365 |
| Microsoft Dynamics 365 plaan, Enterprise Edition | PowerApps for Dynamics 365 |

Pange tähele, et erinevad Microsoft Office’i SKU-d annavad samuti selle õiguse, lisaks eraldiseisvatele PowerAppsi plaani 2 SKU-dele. Oluline on, et üks nendest SKU-dest oleks olemas.

1. Avage [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Looge keskkondi, järgides juhiseid jaotises [Talenti ettevalmistamine](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).

