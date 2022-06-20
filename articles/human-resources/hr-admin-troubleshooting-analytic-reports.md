---
title: Analüütiliste aruannete tõrkeotsing
description: See artikkel selgitab, kuidas tõrkeotsingut ja diagnoosimist, kui kliendi andmete muutusi ei kuvata üheski kliendi tööruumis.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1e6ae8931679feb2103172eb1a21649734acd995
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902223"
---
# <a name="troubleshoot-analytic-reports"></a>Analüütiliste aruannete tõrkeotsing


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Väljastamine**

Kliendiandmete muudatusi ei kuvata kliendi tööruumide vahekaartidel **Analüütika**.

**Põhjus**

Vaikimisi värskendatakse Microsoft Power BI aruandeid iga nelja tunni järel mõõtmete juurutamise pakett-töö graafiku kohaselt.

**Eraldusvõime**

Probleem võib olla ainult ajastuse küsimus. Järgige neid samme, et alustada pakett-tööd ja värskendada analüütika tööruume.

1. Avage leht **Pakett-tööd** valikus **Süsteemihaldus \> Lingid \> Pakett-töö \> Pakett-tööd**. Teise võimalusena kasutage otsingut ja sisestage **Pakett-töö**.
1. Leidke loendist töö **Mõõtme juurutamine**.
1. Valige lehe ülaosas **Redigeeri** ja määrake planeeritud alguskuupäevaks/-kellaajaks väärtus, mis värskendab analüütika praegusele ajale lähemal.

![Pakett-tööd.](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
