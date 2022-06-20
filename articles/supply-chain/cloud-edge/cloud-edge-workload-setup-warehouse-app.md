---
title: Warehouse Managementi pilvrakenduse ja perimeeterskaalaüksuste konfigureerimine
description: See artikkel selgitab, kuidas häälestada laohalduse mobiilirakendusi ladudele, mida pakub pilve või servaskaala üksus.
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
ms.openlocfilehash: 86edef2dfa6e9c71c04d50f185148be3a622fea1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865234"
---
# <a name="configure-the-warehouse-management-mobile-app-for-cloud-and-edge-scale-units"></a>Warehouse Managementi pilvrakenduse ja perimeeterskaalaüksuste konfigureerimine

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas seadistada laohalduse mobiilirakendusi nii, et neid saab kasutada ladudes, mida teenindab pilve või servaskaala üksus.

## <a name="prerequisites"></a>Eeltingimused

Enne kui alustate mobiilsete seadmete seadistamist ühenduma pilve või servaskaala ühikuga, veenduge, et nad saavad ettevõtte keskusega ühendust luua. Juhiseid vaadake teemast Laohalduse [mobiilirakenduse installimine ja ühendamine](../warehousing/install-configure-warehouse-management-app.md).

## <a name="additional-setup-when-you-run-the-warehouse-management-mobile-app-against-a-scale-unit"></a>Täiendav häälestus laohalduse mobiilirakenduse käivitamisel kaaluühikuga

Osana laoskaala [ühiku töökoormuste juurutusprotsessist](cloud-edge-landing-page.md#scale-unit-manager-portal) sünkroonitakse enamik andmeid, mis on vajalikud laohalduse mobiiliseadmete ühendamiseks, automaatselt ettevõtte keskusest kaaluüksusega. Peate siiski sisestama andmed rakenduste lehele (**Azure Active Directory** **\> Süsteemihalduse \>Azure Active Directory seadistuse rakendused**) kaalu ühiku juurutamisel. Lisaks võib juhtuda, et peate värskendama ettevõtte **vaikeväärtust** kasutaja ID jaoks või looma uue kasutaja. Kasutajad, kes on seotud ettevõttega, mida pole kaaluühiku juurutuses olemas, ei saa sisse logida, kui laohalduse mobiilirakendus on ühendatud selle kaaluüksusega.

> [!NOTE]
> Kuna avalduste lehel **Azure Active Directory** salvestatud andmeid ei sünkroonita, peate neid andmeid käsitsi hooldama, kui soovite teisaldada oma lao töökoormused teise kaaluühikusse.

Pidage meeles, et osana iga laohalduse Azure Active Directory mobiilirakenduse ühendusseadistusest peab määratud ressursi URL olema ettevõttekeskuse asemel kaaluühikule.
