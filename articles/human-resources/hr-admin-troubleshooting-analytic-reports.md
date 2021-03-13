---
title: Analüütiliste aruannete tõrkeotsing
description: See artikkel selgitab, mida teha, kui kliendiandmete muudatusi ei kuvata kliendi tööruumides.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c5e1a1d7044567a07acedf71e65ed244275acfd9
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112228"
---
# <a name="troubleshoot-analytic-reports"></a>Analüütiliste aruannete tõrkeotsing

**Väljastamine**

Kliendiandmete muudatusi ei kuvata kliendi tööruumide vahekaartidel **Analüütika**.

**Põhjus**

Vaikimisi värskendatakse Microsoft Power BI aruandeid iga nelja tunni järel mõõtmete juurutamise pakett-töö graafiku kohaselt.

**Eraldusvõime**

Probleem võib olla ainult ajastuse küsimus. Järgige neid samme, et alustada pakett-tööd ja värskendada analüütika tööruume.

1. Avage leht **Pakett-tööd** valikus **Süsteemihaldus \> Lingid \> Pakett-töö \> Pakett-tööd**. Teise võimalusena kasutage otsingut ja sisestage **Pakett-töö**.
1. Leidke loendist töö **Mõõtme juurutamine**.
1. Valige lehe ülaosas **Redigeeri** ja määrake planeeritud alguskuupäevaks/-kellaajaks väärtus, mis värskendab analüütika praegusele ajale lähemal.

![Pakett-tööd](media/batch-jobs.png)
