---
title: Jaluse moodul
description: See teema hõlmab jaluse mooduleid ja kuidas neid rakenduses Dynamics 365 Commerce koostada.
author: anupamar
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7c253cd9620180b09f2f5cae232e46d236deabdd
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697309"
---
# <a name="footer-module"></a>Jaluse moodul  

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

See teema hõlmab jaluse mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce luua.

## <a name="overview"></a>Ülevaade

Jaluse moodul on erikonteiner, mida kasutatakse lehe jaluses kuvatavate moodulite majutamiseks. Näiteks võib see sisaldada linke saidi erinevatele lehtedele, nagu lehed **Võtke meiega ühendust** ja **Poe eeskirjad**.

## <a name="footer-module-properties"></a>Jaluse mooduli atribuudid 

Nagu enamik konteinereid, toetab jaluse moodul pealkirja ja laiuse atribuute. Samuti toetab mitme jaluse kategooria moodulite lisamist. Iga lisatud jaluse kategooria moodul renderdatakse jaluse mooduli veeruna.

## <a name="modules-available-in-a-footer-module"></a>Jaluse moodulis saadaolevad moodulid

**Jaluse üksused** – jaluse üksuste moodul võib sisaldada pealkirja, pilti ja linki. Pealkirja saab kasutada kas eraldi või koos pildi ja lingiga. Iga jaluse linki saab konfigureerida nii, et sellel on ainult tekst (nt lingid „Võtke meiega ühendust” „Privaatsus”), või nii, et sellel on nii tekst kui ka pilt (nt sotsiaalmeedia lingid).

**Tagasi üles** – moodul tagasi üles pakub linki kiiresti tagasi lehe ülaossa navigeerimiseks. Nõutav on sihtkoht. Sihtkoha vaikeväärtus on #, mis viib kasutaja lehekülje ülaossa.

## <a name="author-a-footer-module"></a>Jaluse mooduli koostamine

1. Valige navigeerimispaanil suvand **Fragmendid** ja valige seejärel **Uus lehe fragment**.
1. Dialoogiaknas **Uus lehe fragment** valige jaluse moodul, sisestage lehe fragmendi nimi ja valige seejärel **OK**.
1. Valige vasakul liigendpuus jaluse mooduli kolmikpunkti nupp (**…**) ja seejärel suvand **Lisa moodul**.
1. Valige dialoogiaknas **Lisa moodul** jaluse kategooria moodul ja klõpsake seejärel nuppu **OK**.
1. Valige liigendpuus jaluse kategooria mooduli kolmikpunkti nupp ja seejärel suvand **Lisa moodul**.
1. Valige dialoogiaknas **Lisa moodul** jaluse üksuse moodul ja klõpsake seejärel nuppu **OK**.
1. Valige liigendpuus jaluse üksuse moodul. Seejärel konfigureerige parempoolsel atribuutide paanil pealkiri, link ja lingi tekst ning vastavalt vajadusele pilt.
1. Rohkemate jaluse üksuste lisamiseks korrake samme 5 kuni 7.
1. Jalusele lingi Tagasi üles lisamiseks valige jaluse kategooria mooduli kolmikpunkti nupp ja seejärel suvand **Lisa moodul**.
1. Valige dialoogiaknas **Lisa moodul** tagasi üles moodul ja klõpsake seejärel nuppu **OK**.
1. Valige liigendpuus tagasi üles moodul. Seejärel konfigureerige paremal atribuutide paanil vastavalt vajadusele tagasi üles moodul.
1. Salvestage lehe fragment, kontrollige seda ja avaldage see.

Järgige igal saidi jaoks loodud lehe mallil järgmisi etappe.

1. Lisage jaluse mooduli vaikelehe pesas **Peamine** jaluse fragment, mille lõite.
1. Salvestage mall, kontrollige seda ja avaldage see.

Lisades lehe mallidele lehe fragmendi, aitate tagada, et jalus renderdatakse igal lehel.

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Konteinermoodul](add-container-module.md)

[Ostukasti moodul](add-buy-box.md)

[Ostukorvi moodul](add-cart-module.md)

[Maksmise moodul](add-checkout-module.md)

[Tellimuse kinnituse moodul](order-confirmation-module.md)

[Päise moodul](author-header-module.md)

[Jaluse moodul](author-footer-module.md)
