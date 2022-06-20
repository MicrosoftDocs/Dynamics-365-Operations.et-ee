---
title: Jalusemoodul
description: See artikkel hõlmab jaluse mooduleid ja nende autorit Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4e7796d9700eabc923f2bb45187832d5993ae56e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876608"
---
# <a name="footer-module"></a>Jalusemoodul  

[!include [banner](includes/banner.md)]

See artikkel katab jaluse mooduleid ja kirjeldab, kuidas neid luua Microsoft Dynamics 365 Commerce.

Jaluse moodul on erikonteiner, mida kasutatakse lehe jaluses kuvatavate moodulite majutamiseks. Näiteks võib see sisaldada linke saidi erinevatele lehtedele, nagu lehed **Võtke meiega ühendust** ja **Poe eeskirjad**.

Järgmisel pildil on näide jaluse moodulist saidi lehel.

![Jaluse mooduli näide.](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a>Jaluse mooduli atribuudid 

Nagu enamik konteinereid, toetab jaluse moodul pealkirja ja laiuse atribuute. Samuti toetab mitme jaluse kategooria moodulite lisamist. Iga lisatud jaluse kategooria moodul renderdatakse jaluse mooduli veeruna.

## <a name="modules-available-in-a-footer-module"></a>Jaluse moodulis saadaolevad moodulid

**Jaluse** üksus – jaluse kaubamoodul võib sisaldada pealkirja või linki. Päist kasutatakse tavaliselt jaluse sektsiooni pealkirjana.  Iga jaluse linki saab konfigureerida nii, et sellel on ainult tekst (nt lingid „Võtke meiega ühendust” „Privaatsus”), või nii, et sellel on nii tekst kui ka pilt (nt sotsiaalmeedia lingid). Kui on esitatud nii pealkiri kui ka link, on seosest eelistuseks pealkirja atribuut. 

**Tagasi üles** – moodul tagasi üles pakub linki kiiresti tagasi lehe ülaossa navigeerimiseks. Nõutav on sihtkoht. Sihtkoha vaikeväärtus on \#, mis viib kasutaja lehekülje ülaossa.

## <a name="create-a-footer-module"></a>Jalusemooduli loomine

1. Avage **Fragmendid** ja valige uue fragmendi loomiseks **Uus**.
1. Dialoogiaknas **Vali** tükk valige **konteinerimoodul**, sisestage killu nimi ja seejärel valige **OK**.
1. **Valige konteineri vaikepesas** kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.
1. Dialoogiaknas **Vali** moodulid valige jaluse **kategooria** moodul ja seejärel valige **OK**.
1. Jaluse **kategooria pesas** valige kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.
1. Dialoogiaknas **Vali** moodulid valige jaluse **kauba** moodul ja seejärel valige **OK**.
1. Valige pesa **Jaluse üksus** ja seejärel konfigureerige parempoolsel atribuutide paanil vajaduse pealkiri, link ja lingi tekst ning vajadusel pilt.
1. Rohkemate jaluse üksuste lisamiseks korrake iga kord samme 5 kuni 7.
1. Oma jalusesse "tagasi ülemisele" lingi lisamiseks valige jaluse kategooria pesast ellips (**...**) **ja** seejärel valige **lisamoodul**.
1. Dialoogiaknas **Vali** moodulid valige moodul **Tagasi ülemisele** ja seejärel valige **OK**.
1. Valige pesa **Tagasi üles** ja seejärel konfigureerige parempoolsel atribuutide paanil vajaduse järgi tekst ja muud mooduli atribuudid.
1. Valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

Päise igal lehel kuvamise tagamiseks järgige neid samme iga malli jaoks, mis on saidi jaoks loodud.

1. Lisage mooduli **Vaikeleht** pesas **Jalus** loodud jaluse fragment.
1. Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

Lisades lehe mallidele fragmendi, aitate tagada, et jalus renderdatakse igal lehel.

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Konteinermoodul](add-container-module.md)

[Ostukastimoodul](add-buy-box.md)

[Ostukorvimoodul](add-cart-module.md)

[Maksmismoodul](add-checkout-module.md)

[Tellimuse kinnituse moodul](order-confirmation-module.md)

[Päise moodul](author-header-module.md)

[Jaluse moodul](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
