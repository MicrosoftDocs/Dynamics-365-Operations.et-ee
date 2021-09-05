---
title: Power Appsi halduskeskuses ei saa keskkonda luua
description: Selles teemas selgitatakse, mida teha, kui administraator ei saa Microsoft Power Appsi halduskeskuses keskkonda luua.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 50a5aac71ec8ed850cfad32bdb1b8d589eb2885a
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413557"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Power Appsi halduskeskuses ei saa keskkonda luua

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Väljastamine**

- Rentniku/keskkonna administraator ei saa Microsoft Power Appsi halduskeskuses keskkonda luua.
- Kasutajal pole litsentsi, mis annab õiguse keskkondi luua.

**Lahendus**

Veenduge, et rentniku administraator on keskkonda loovale kasutajale määranud kehtiva Power Apps P2 litsentsi. Keskkondade loomiseks pakuvad õigusi järgmised Microsoft Dynamicsi teenuseplaanid.

| Üldine toote varude arvestusühik (SKU)       | Power Apps P2 teenusepakett  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | Power Apps for Dynamics 365 |
| Microsoft Dynamics 365 plaan, Enterprise Edition | Power Apps for Dynamics 365 |

Pange tähele, et erinevad Microsoft Office’i SKU-d annavad samuti selle õiguse lisaks eraldiseisvatele Power Appsi plaani 2 SKU-dele. Oluline on, et üks nendest SKU-dest oleks olemas.

1. Avage [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Looge keskkondi, järgides juhiseid teemas [Rakenduse Human Resources ettevalmistamine](/dynamics365/unified-operations/talent/provisioning-talent).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
