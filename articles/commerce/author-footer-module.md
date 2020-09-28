---
title: Jaluse moodul
description: See teema hõlmab jaluse mooduleid ja kuidas neid rakenduses Dynamics 365 Commerce koostada.
author: anupamar
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: 6dd9f214fbeeeaabadac4853916363c20a3288ca
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761197"
---
# <a name="footer-module"></a>Jaluse moodul  

[!include [banner](includes/banner.md)]

See teema hõlmab jaluse mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce luua.

## <a name="overview"></a>Ülevaade

Jaluse moodul on erikonteiner, mida kasutatakse lehe jaluses kuvatavate moodulite majutamiseks. Näiteks võib see sisaldada linke saidi erinevatele lehtedele, nagu lehed **Võtke meiega ühendust** ja **Poe eeskirjad**.

Järgmisel pildil on näide jaluse moodulist saidi lehel.

![Jaluse mooduli näide](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a>Jaluse mooduli atribuudid 

Nagu enamik konteinereid, toetab jaluse moodul pealkirja ja laiuse atribuute. Samuti toetab mitme jaluse kategooria moodulite lisamist. Iga lisatud jaluse kategooria moodul renderdatakse jaluse mooduli veeruna.

## <a name="modules-available-in-a-footer-module"></a>Jaluse moodulis saadaolevad moodulid

**Jaluse üksused** – jaluse üksuste moodul võib sisaldada pealkirja, pilti ja linki. Pealkirja saab kasutada kas eraldi või koos pildi ja lingiga. Iga jaluse linki saab konfigureerida nii, et sellel on ainult tekst (nt lingid „Võtke meiega ühendust” „Privaatsus”), või nii, et sellel on nii tekst kui ka pilt (nt sotsiaalmeedia lingid).

**Tagasi üles** – moodul tagasi üles pakub linki kiiresti tagasi lehe ülaossa navigeerimiseks. Nõutav on sihtkoht. Sihtkoha vaikeväärtus on \#, mis viib kasutaja lehekülje ülaossa.

## <a name="create-a-footer-module"></a>Jalusemooduli loomine

1. Avage **Fragmendid** ja valige uue fragmendi loomiseks **Uus**.
1. Valige dialoogiboksis **Uus fragment** moodul **Konteiner**, sisestage fragmendi nimi ja valige seejärel **OK**.
1. Valige pesas **Vaikekonteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Jaluse kategooria** ja klõpsake seejärel **OK**.
1. Valige pesas **Jaluse kategooria** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Jaluse üksus** ja klõpsake seejärel **OK**.
1. Valige pesa **Jaluse üksus** ja seejärel konfigureerige parempoolsel atribuutide paanil vajaduse pealkiri, link ja lingi tekst ning vajadusel pilt.
1. Rohkemate jaluse üksuste lisamiseks korrake iga kord samme 5 kuni 7.
1. Jalusele lingi „Tagasi üles“ lisamiseks valige pesas **Jaluse kategooria** kolmikpunkt (**...**) ja seejärel **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Tagasi üles** ja klõpsake seejärel **OK**.
1. Valige pesa **Tagasi üles** ja seejärel konfigureerige parempoolsel atribuutide paanil vajaduse järgi tekst ja muud mooduli atribuudid.
1. Valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

Päise igal lehel kuvamise tagamiseks järgige neid samme iga malli jaoks, mis on saidi jaoks loodud.

1. Lisage mooduli **Vaikeleht** pesas **Jalus** loodud jaluse fragment.
1. Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

Lisades lehe mallidele fragmendi, aitate tagada, et jalus renderdatakse igal lehel.

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Konteinermoodul](add-container-module.md)

[Ostukasti moodul](add-buy-box.md)

[Ostukorvi moodul](add-cart-module.md)

[Maksmise moodul](add-checkout-module.md)

[Tellimuse kinnituse moodul](order-confirmation-module.md)

[Päise moodul](author-header-module.md)

[Jaluse moodul](author-footer-module.md)
