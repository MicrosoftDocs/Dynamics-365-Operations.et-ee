---
title: Power Appsi halduskeskuses ei saa keskkonda luua
description: Selles artiklis selgitatakse, mida teha, kui administraator ei saa Microsoft Power Appsi halduskeskuses keskkonda luua.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 73c8910900ba6486a8e60a547b07ea0c82a6cb10
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053343"
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