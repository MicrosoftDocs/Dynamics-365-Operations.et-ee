---
title: Töövoo KKK
description: Teemas on toodud vastused korduma kippuvatele küsimustele rakenduse Microsoft Dynamics 365 for Finance and Operations töövoo süsteemi kohta.
author: ChrisGarty
manager: AnnBe
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6240b1b5136937aa47f455547fed6f0c7c08e2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509287"
---
# <a name="workflow-system"></a>Töövoo süsteem

[!include [banner](../includes/banner.md)]

Teemas on toodud vastused korduma kippuvatele küsimustele rakenduse Microsoft Dynamics 365 for Finance and Operations töövoo süsteemi kohta.

## <a name="notifications"></a>Teatised

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Miks võetakse tööüksuse tagasilükkamisel vastu mitu teatist?
Tööüksuse tagasilükkamisel viiakse see tööüksus tagasilükatuna lõpuni. Algatajale luuakse ja määratakse teine tööüksus. See tähendab, et algataja saab teatise tagasilükatud tööüksuse kohta ja kasutaja, kellele määrati uus „taotletakse muudatust” tööüksus, saab eraldi teatise. 

Iga teatis on erineva tööüksuse jaoks, kuid nende sarnasus võib põhjustada segadust. Otsime võimalusi selle tulevases väljaandes parandamiseks.

### <a name="why-are-my-workflow-exports-failing"></a>Miks minu töövoo eksport nurjub?
Praegu on töövoo ekspordi funktsioonil piirang, milles töövoo nimede pikkus ei tohi ületada 48 märki. Kasutades nime, mis on pikem kui 48 märki võib põhjustada tõrke "Server ei saanud taotlust autentida" ja/või takistada faili eksportimist failitüübita. Järgmine ajaveebipostitus sisaldab üksikasju [Töövoo ekspordi tõrkeotsingu](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting) kohta.
