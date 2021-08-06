---
title: Eelarvesoovituste lubamine (eelversioon)
description: Selles teemas selgitatakse, kuidas lülitada finantsülevaadetes sisse eelarvesoovituste funktsioon.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: d3fac4cbb80493c7cf94e3d9f4a4f544a749fb64
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638605"
---
# <a name="enable-budget-proposals-preview"></a>Eelarvesoovituste lubamine (eelversioon)

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas lülitada finantsülevaadetes sisse eelarvesoovituste funktsioon.

1. Kasutage teavet teenuse Microsoft Dynamics Lifecycle Services (LCS) lehelt, et ühendada Azure SQL-i esmane eksemplar selle keskkonnaga. Käivitage järgmine Transact-SQL (T-SQL) käsk, et lülitada liivakasti keskkonna eelväljaanded sisse. (Enne rakendusobjekti serveriga \[AOS\] eemalt ühenduse loomist võib olla vajalik, et peate LCS-is lülitama oma IP-aadressi juurdepääsu sisse.)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > Jätke see samm vahele, kui kasutate 10.0.20 või uuemat versiooni või kui kasutate Service Fabric juurutamist. Finantsülevaadete meeskond peaks olema väljaande juba teie jaoks sisse lülitanud. Kui te funktsiooni tööruumis **Funktsioonihaldus** ei näe või kui selle sisselülitamisel esineb probleeme, võtke ühendust aadressil <fiap@microsoft.com>.

2. Avage tööruum **Funktsioonide haldus** ja järgige järgmisi etappe.

    1. Valige **Otsi värskendusi**.
    2. Otsige suvandit **Eelarve soovitus** ja lülitage see funktsioon sisse.

3. Avage suvand **Eelarvestamine \> Seadistus \> Põhiline eelarvestamine \> Eelarvesoovitus (eelversioon)** ja valige suvand **Luba funktsioon**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
