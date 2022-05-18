---
title: Finantsdimensioonid ja põhikontod paremalt vasakule loetavates keeltes
description: See teema kirjeldab otsuseid, mida tuleb teha, kui kasutate paremalt vasakule keelt ja peate seadistama finantsdimensioonid ning põhikontod.
author: RyanCCarlson2
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: rcarlson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5de2e0e6e56651487ebd36e3594eb378ce6154ea
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734949"
---
# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a>Finantsdimensioonid ja põhikontod paremalt vasakule loetavates keeltes

[!include [banner](../includes/banner.md)]

See teema kirjeldab mõningaid juurutamisotsuseid, mida tuleb arvestada, kui kasutate paremalt vasakule keelt, ja peate seadistama finantsdimensioonid ja põhikontod.

Finantsdimensioonid ja põhikontod on juurutamise plaanimisfaasi põhikomponendid. Pärast finantsdimensioonide ja põhikontode loomist süsteemis kasutatakse neid lehtedel **Konto struktuuride konfigureerimine**, **Täpsemad konto struktuurid** ja **Finantsdimensiooni konfiguratsioon rakenduste integreerimiseks**. Nendel lehtedel määratletud tellimust kasutatakse andmete sisestamise ja tarbimise süsteemis. Mõnes süsteemis kohas ilmuvad finantsdimensioonid ja põhikontod eraldi väljadel. Teistes kohtades, nagu töölehed, finantsdimensioonid ja põhikontod, ilmuvad need ühe stringina.

## <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a>Parimad tavad finantsdimensioonide ja põhikontode seadistamiseks paremalt vasakul süsteemis

- Kui valite kontoplaanide jaoks eraldaja, valige üks eraldaja suvanditest: kaks sidekriipsu (`--`), kaks pulka (`||`), kaks punkti (`..`) või kaks allkriipsu (`\\`).
- Finantsdimensiooni ja põhikonto väärtuste loomisel kasutage ainult numbreid ja paremalt vasakule keele märke.
- Vältige valitud kontoplaani eraldaja kasutamist finantsdimensiooni ja põhikonto väärtustes.

Neid parimaid tavasid järgides saate tagada kasutaja määratletud tellimuse pideva tähistamise kogu süsteemis.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
