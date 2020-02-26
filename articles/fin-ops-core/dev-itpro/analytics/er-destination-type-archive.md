---
title: ER-i sihtkoha tüübi arhiveerimine
description: Sellest teemast leiate teatevt, kuidas konfigureerida arhiivi sihtkoha iga väljamineva dokumendi loomiseks konfigureeritud elektroonilise aruandluse (ER) vormingu iga kausta või faili komponendi jaoks.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 15611a4f0000ca5ccb0ac3f4012251d5bf5689ec
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019728"
---
# <a name="ArchiveDestinationType">Arhiivi sihtkoht</a>

[!include [banner](../includes/banner.md)]

Saate konfigureerida arhiivi sihtkoha iga väljamineva dokumendi loomiseks konfigureeritud elektroonilise aruandluse (ER) vormingu iga kausta või faili komponendi jaoks. Sihtkoha sätte põhjal talletatakse loodud dokument ER tööde loendi kirje manusena.

Selle valiku abil saab saata loodud dokumendi Microsoft SharePointi kausta või Microsoft Azure’i salvestusruumi. Määrake valiku **Lubatud** väärtuseks **Jah** väljundi saatmiseks valitud dokumenditüübiga määratletud sihtkohta. Valida saab ainult neid dokumenditüüpe, millel grupiks on määratud **Fail**. Dokumendi [tüübid](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) saate määratleda jaotistes **Organisatsiooni haldus**\>  **Dokumendihaldus**\> **Dokumenditüübid**. ER-i sihtkohtade konfiguratsioon on sama, mis dokumendihaldussüsteemi konfiguratsioon.

[![Leht Dokumenditüübid](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)

Asukoht määrab, kuhu fail salvestatakse. Kui sihtkoht **Arhiiv** on lubatud, saab konfiguratsiooni käivitamise tulemused salvestada tööarhiivi. Tulemusi saate vaadata jaotises **Organisatsiooni haldus** \> **Elektrooniline aruandlus** \> **Elektroonilise aruandluse arhiivitud tööd**.

> [!NOTE]
> Tööarhiivi jaoks saate dokumenditüübi valida, liikudes jaotisesse **Organisatsiooni haldus** \> **Tööruumid** \> **Elektrooniline aruandlus** \> **Elektroonilise aruandluse parameetrid**. Lisateabe saamiseks vt teemat [Elektroonilise aruandluse (ER) raamistiku konfigureerimine](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).

## <a name="sharepoint"></a>SharePoint

Faili saab salvestada selleks mõeldud SharePointi kausta. SharePointi vaikeserveri määratlemiseks avage **Organisatsiooni haldus**\> **Dokumendihaldus**\> **Dokumendihalduse parameetrid**. Vahekaardil **SharePoint** konfigureerige SharePointi kaust. Seejärel saate valida selle kausta, kuhu ER väljund salvestatakse. Selle dokumenditüübi **SharePoint**i asukoht peab olema valitud.

[![SharePointi kausta valimine](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)

## <a name="azure-storage"></a>Azure’i salvestusruum

Kui dokumenditüübi asukohaks on määratud **Azure'i salvestusruum**, saate faili salvestada Azure’i salvestusruumi.

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)
- [Elektroonilise aruandluse (ER) sihtkohad](electronic-reporting-destinations.md)
- [Dokumendihalduse konfigureerimine](../../fin-ops/organization-administration/configure-document-management.md)
