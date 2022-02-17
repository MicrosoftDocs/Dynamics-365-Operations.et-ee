---
title: Laohalduse mobiilirakenduse konfigureerimine pilve- ja servaskaala ühikute jaoks
description: Selles teemas selgitatakse, kuidas seadistada laohalduse mobiilirakendusi ladudele, mida teenindab pilve- või servaskaala üksus.
author: perlynne
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 1fa00b40db2f6246029876964dca9d3229567848
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071772"
---
# <a name="configure-the-warehouse-management-mobile-app-for-cloud-and-edge-scale-units"></a>Laohalduse mobiilirakenduse konfigureerimine pilve- ja servaskaala ühikute jaoks

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas seadistada laohalduse mobiilirakendusi nii, et neid saaks kasutada ladudes, mida teenindab pilve- või servaskaala üksus.

## <a name="prerequisites"></a>Eeltingimused

Enne kui hakkate häälestama mobiilsideseadmeid pilve- või servaskaala üksusega ühenduse loomiseks, kinnitage, et need saavad ettevõtte jaoturiga ühenduse luua. Juhised leiate teemast [Laohalduse mobiilirakenduse installimine ja ühendamine](../warehousing/install-configure-warehouse-management-app.md).

## <a name="additional-setup-when-you-run-the-warehouse-management-mobile-app-against-a-scale-unit"></a>Täiendav häälestus, kui käivitate laohalduse mobiilirakenduse skaalaühiku vastu

Laoskaala ühiku töökoormuse [juurutamisprotsessi osana](cloud-edge-landing-page.md#scale-unit-manager-portal) sünkroonitakse enamik andmeid, mis on vajalikud laohalduse mobiilirakenduste seadmete ühendamiseks, automaatselt ettevõtte jaoturist skaalaüksusega. Siiski peate sisestama andmed **Azure Active Directory rakenduste lehele (** süsteemihalduse **häälestusrakendused \>\>Azure Active Directory) skaalaüksuse** juurutusse. Lisaks peate võib-olla värskendama kasutaja ID ettevõtte **vaikeväärtust** või looma uue kasutaja. Kasutajad, kes on seotud ettevõttega, mida pole skaalaüksuse juurutuses olemas, ei saa sisse logida, kui laohalduse mobiilirakendus on selle skaalaüksusega ühendatud.

> [!NOTE]
> Kuna rakenduste **Azure Active Directory lehel** olevad andmed ei ole sünkroonitud, peate need andmed käsitsi säilitama, kui soovite lao töökoormuse teisaldada mõnda muusse skaalaühikusse.

Pidage meeles, et iga laohalduse mobiilirakenduse ühenduse häälestuse osana peab määratud Azure Active Directory ressursi URL olema ettevõtte jaoturi asemel skaalaühiku jaoks.
