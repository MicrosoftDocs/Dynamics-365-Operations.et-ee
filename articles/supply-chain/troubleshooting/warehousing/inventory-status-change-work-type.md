---
title: Varude oleku muudatust ei saa töö tüübina valida
description: Töömalli rida ei saa varude oleku muudatuse jaoks luua, kuna töö tüüpi kasutatakse ainult süsteemiprotsessides. Valige mõni muu töö tüüp.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ad7f26f3235d15779583f9cdadeb4e6dca16242a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476154"
---
# <a name="cant-select-inventory-status-change-in-the-work-type-column"></a>Varude oleku muutmist ei saa veerus Töö tüüp valida

## <a name="symptoms"></a>Sümptomid

Microsoft Dynamics 365 Supply Chain Management konfigureerimisel võidakse kuvada järgmine tõrketeade:

> Varude oleku muutmiseks ei saa töömalli rida luua, kuna töö tüüp ei sobi. Valige mõni muu töö tüüp.

## <a name="resolution"></a>Lahendus

Selline käitumine on nii kavandatud. *Varude oleku muutmise* töö tüüpi kasutatakse ainult süsteemi protsessidega. Seda ei saa konfigureerida. Kuna töö tüüpide loend on fikseeritud kui loendamine, ei saa lisakirjeid **Töö tüübi** rippmenüüst välja filtreerida.
