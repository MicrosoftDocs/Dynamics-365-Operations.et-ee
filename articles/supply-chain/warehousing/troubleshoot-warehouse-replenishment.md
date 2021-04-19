---
title: Lao täiendamise tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada lao täiendamisega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 8940f729e1115405e8d6e50eccc92d9fffe37f3e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828078"
---
# <a name="troubleshoot-warehouse-replenishment"></a>Lao täiendamise tõrkeotsing

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas lahendada lao täiendamisega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a>Saan järgneva tõrketeate: "Töö %1 blokeeringut ei saa tühistada, kuna see on lõpule viimata täiendamistöö."

### <a name="issue-description"></a>Probleemi kirjeldus

Komplekteerimise töö on blokeeritud sõltuva täiendamistöö tõttu.

### <a name="issue-resolution"></a>Probleemi lahendamine

Kui kasutate voo nõudluse täiendamist, kui komplekteerimise asukoht tuleb komplekteerida, et täita allika tellimuse nõudlust, loob süsteem nii täiendamise töö kui ka komplekteerimise töö. Kuid see blokeerib komplekteerimise töö seni, kuni täiendamise töö on lõpetatud. Selline käitumine on tahtlik, sest komplekteerimise asukohas ei ole piisavalt varusid, kui täiendamise töö on lõpule viidud. Täitke täiendamise töö ja seejärel töödelge komplekteerimise töö.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]