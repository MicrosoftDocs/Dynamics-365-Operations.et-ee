---
title: Asukohapõhise poetuvastuse lubamine
description: Selles teemas kirjeldatakse, kuidas lülitada rakenduse Dynamics 365 Commerce saidil sisse asukohapõhine poetuvastus.
author: brianshook
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 304d8d2f05916295b9c6320561d6a25ff40df955
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003092"
---
# <a name="enable-location-based-store-detection"></a>Asukohapõhise poetuvastuse lubamine


[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas lülitada rakenduse Dynamics 365 Commerce saidil sisse asukohapõhine poetuvastus.

## <a name="overview"></a>Ülevaade

Commerce’i asukohapõhine poetuvastus võimaldab pakkuda klientidele asjakohast saidi sisu vastavalt nende asukohale. Kui asukohapõhine poetuvastus on sisse lülitatud, kasutab Commerce’i renderdusteenus kliendi veebibrauseri IP-aadressi riigi/piirkonna teavet, et suunata klient parima saadaoleva geograafilise saidi konfiguratsiooni juurde.

## <a name="privacy-notice"></a>Privaatsusavaldus

Kui lülitate asukohapõhise poetuvastuse funktsiooni sisse, saadetakse kliendi brauseri teave Microsofti asukoha teenusele. Seda teavet kasutatakse siis, et pakkuda kliendile sisu, mis on tema asukohaga seotud. Nii kliendi brauserist saadetud teabele kui ka kliendilt saadud asukohapõhisele teabele kehtivad privaatsuse ja küpsiste vastavuse poliitikad.

## <a name="turn-on-location-based-store-detection"></a>Asukohapõhise poetuvastuse sisselülitamine

Asukohapõhise poetuvastuse sisselülitamiseks Commerce’is toimige järgmiselt.

1. Avage autorluse tööriistas oma sait.
1. Valige navigeerimispaanilt vasakult suvand **Saidi haldus**.
1. Valige **Saidi sätted**.
1. Seadke suvand **Luba asukohapõhine poetuvastus** olekusse **Sees**.

## <a name="additional-resources"></a>Lisaressursid

[Domeeninime konfigureerimine](configure-your-domain-name.md)

[Uue e-kaubanduse saidi juurutamine](deploy-ecommerce-site.md)

[E-kaubanduse saidi loomine](create-ecommerce-site.md)

[Veebisaidi seostamine kanaliga](associate-site-online-store.md)

[Robots.txt-failide haldamine](manage-robots-txt-files.md)

[Kasutaja sisselogimiseks kohandatud lehtede seadistamine](custom-pages-user-logins.md)

[Sisuedastusvõrgu (CDN) toe lisamine](add-cdn-support.md)
