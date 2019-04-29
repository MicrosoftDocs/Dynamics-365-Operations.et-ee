---
title: Analüüsiaruanded on värskendamata
description: See teema selgitab, mida teha, kui kliendiandmete muudatusi ei kuvata kliendi tööruumides.
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
ms.openlocfilehash: d6a6487b50908093f876237ffef840a3144b3fe6
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/19/2019
ms.locfileid: "857449"
---
# <a name="analytic-reports-are-not-updated"></a>Analüüsiaruanded on värskendamata

[!include [banner](includes/banner.md)]

**Probleem**

Kliendiandmete muudatusi ei kuvata kliendi tööruumide vahekaartidel **Analüütika**.

**Põhjus**

Vaikimisi värskendatakse Microsoft Power BI aruandeid iga nelja tunni järel mõõtmete juurutamise pakett-töö graafiku kohaselt.

**Eraldusvõime**

Probleem võib olla ainult ajastuse küsimus. Järgige neid samme, et alustada pakett-tööd ja värskendada analüütika tööruume.

1. Avage leht **Pakett-tööd** valikus **Süsteemihaldus \> Lingid \> Pakett-töö \> Pakett-tööd**. Teise võimalusena kasutage otsingut ja sisestage **Pakett-töö**.
1. Leidke loendist töö **Mõõtme juurutamine**.
1. Valige lehe ülaosas **Redigeeri** ja määrake planeeritud alguskuupäevaks/-kellaajaks väärtus, mis värskendab analüütika praegusele ajale lähemal.

![Pakett-tööd](media/batch-jobs.png)
