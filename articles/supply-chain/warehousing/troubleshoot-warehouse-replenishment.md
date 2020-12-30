---
title: Lao täiendamise tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada lao täiendamisega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e4d87e85520c2b6f2346fddf3b985d4e17fe35cb
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644869"
---
# <a name="troubleshoot-warehouse-replenishment"></a>Lao täiendamise tõrkeotsing

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas lahendada lao täiendamisega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a>Saan järgneva tõrketeate: "Töö %1 blokeeringut ei saa tühistada, kuna see on lõpule viimata täiendamistöö."

### <a name="issue-description"></a>Probleemi kirjeldus

Komplekteerimise töö on blokeeritud sõltuva täiendamistöö tõttu.

### <a name="issue-resolution"></a>Probleemi lahendamine

Kui kasutate voo nõudluse täiendamist, kui komplekteerimise asukoht tuleb komplekteerida, et täita allika tellimuse nõudlust, loob süsteem nii täiendamise töö kui ka komplekteerimise töö. Kuid see blokeerib komplekteerimise töö seni, kuni täiendamise töö on lõpetatud. Selline käitumine on tahtlik, sest komplekteerimise asukohas ei ole piisavalt varusid, kui täiendamise töö on lõpule viidud. Täitke täiendamise töö ja seejärel töödelge komplekteerimise töö.
