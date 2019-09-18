---
title: PowerAppsi halduskeskuses ei saa keskkonda luua
description: Selles teemas selgitatakse, mida teha, kui administraator ei saa Microsoft PowerAppsi halduskeskuses keskkonda luua.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 96119ca869cbbb15ed8d8d5d0fe3b0f94b5f36cc
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742838"
---
# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a>Ei saa luua keskkonda PowerAppsi halduskeskuses

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

Pange tähele, et erinevad Microsoft Office’i SKU-d annavad samuti selle õiguse lisaks eraldiseisvatele PowerAppsi plaani 2 SKU-dele. Oluline on, et üks nendest SKU-dest oleks olemas.

1. Avage [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Looge keskkondi, järgides juhiseid jaotises [Talenti ettevalmistamine](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).
