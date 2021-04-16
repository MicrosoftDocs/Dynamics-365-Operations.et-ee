---
title: Eelarvesoovituste lubamine (eelversioon)
description: Selles teemas selgitatakse, kuidas lülitada finantsülevaadetes sisse eelarvesoovituste funktsioon.
author: ShivamPandey-msft
ms.date: 07/24/2020
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
ms.openlocfilehash: 7e90a1a2f2a8e7808f03ce9a6ee58c027bd48d8d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818700"
---
# <a name="enable-budget-proposals-preview"></a>Eelarvesoovituste lubamine (eelversioon)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Selles teemas selgitatakse, kuidas lülitada finantsülevaadetes sisse eelarvesoovituste funktsioon.

1. Kasutage teavet teenuse Microsoft Dynamics Lifecycle Services (LCS) lehelt, et ühendada Azure SQL-i esmane eksemplar selle keskkonnaga. Käivitage järgmine Transact-SQL (T-SQL) käsk, et lülitada liivakasti keskkonna eelväljaanded sisse. (Enne rakendusobjekti serveriga \[AOS\] eemalt ühenduse loomist võib olla vajalik, et peate LCS-is lülitama oma IP-aadressi juurdepääsu sisse.)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > Kui teie Microsoft Dynamics 365 Finance on Service Fabricu juurutus, saate selle sammu vahele jätta. Finantsülevaadete meeskond peaks olema väljaande juba teie jaoks sisse lülitanud. Kui te funktsiooni tööruumis **Funktsiooni haldus** ei näe või kui teil esineb selle sisselülitamisel probleeme, saatke [finantsülevaadete rakenduse eelversiooni meeskonnale](mailto:fiap@microsoft.com) meil.

2. Avage tööruum **Funktsioonide haldus** ja järgige järgmisi etappe.

    1. Valige **Otsi värskendusi**.
    2. Otsige suvandit **Eelarve soovitus** ja lülitage see funktsioon sisse.

3. Avage suvand **Eelarvestamine \> Seadistus \> Põhiline eelarvestamine \> Eelarvesoovitus (eelversioon)** ja valige suvand **Luba funktsioon**.

#### <a name="privacy-notice"></a>Privaatsusavaldus
Eelvaated 1) võivad kasutada vähem privaatsus- ja turbemeetmeid kui rakenduse Dynamics 365 Finance and Operations teenus; 2) ei ole hõlmatud selle teenuse teenusetaseme leppes; 3) ei tohi olla kasutusel isiklike andmete ega muude andmete töötlemiseks, mis on seaduste või määrustega kaitstud; 4) on piiratud toega.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]