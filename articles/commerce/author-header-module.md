---
title: Päise moodul
description: See teema hõlmab päise mooduleid ja kirjeldab, kuidas lehe päiseid rakenduses Microsoft Dynamics 365 Commerce luua.
author: anupamar
manager: annbe
ms.date: 05/28/2020
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
ms.dyn365.ops.version: ''
ms.openlocfilehash: e7dde3ba1ad375b309ae66cc6d31ccad85615e45
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686618"
---
# <a name="header-module"></a>Päise moodul

[!include [banner](includes/banner.md)]

See teema hõlmab päise mooduleid ja kirjeldab, kuidas lehe päiseid rakenduses Microsoft Dynamics 365 Commerce luua.

## <a name="overview"></a>Ülevaade

Dynamics 365 Commerce'i lehe päis koosneb mitmest moodulist, nagu päis, navigeerimismenüü, otsing, reklaambänner ja küpsistega nõustumise moodulid. 

Päise moodul sisaldab saidi logo, linke navigeerimise hierarhiale, linke teistele saidi lehekülgedele, ostukorvi sümbolit, soovinimekirja sümbolit, sisselogimise suvandeid ja otsinguriba. Päise moodul optimeeritakse automaatselt seadmele, millega saiti vaadatakse (teisisõnu töölauga seade või mobiilne seade). Näiteks mobiilses seadmes on navigeerimisriba ahendatud nupule **Menüü** (mida nimetatakse mõnikord ka *hamburgerimenüüks*).

Järgmisel pildil on näide päise moodulist avalehel.

![Päise mooduli näide](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a>Päise mooduli atribuudid

Päise moodul toetab atribuute **Logo pilt**, **Logo link** ja **Minu konto lingid**. 

Lehel logo määratlemiseks kasutatakse atribuute **Logo pilt** ja **Logo link**. Lisateavet vt jaotisest [Logo lisamine](add-logo.md). 

Atribuuti **Minu konto lingid** saab kasutada konto lehtede määratlemiseks, millele saidi omanik soovib päises kiirlinke kuvada.

## <a name="modules-that-are-available-in-a-header-module"></a>Päise moodulis saadaolevad moodulid

Päise moodulis saab kasutada järgmisi mooduleid.

- **Navigeerimismenüü** – navigeerimismenüü tähistab kanali navigeerimishierarhiat ja teisi staatilisi navigeerimislinke. Kanali navigeerimishierarhiat saab konfigureerida rakenduses Dynamics 365 Commerce. Navigeerimise menüül on atribuut **Navigeerimise allikas**, mida kasutatakse jaemüügi serveri navigatsiooni menüü elementide ja staatilise menüü elementide määramiseks allikana. Kui allikana on määratud staatilised menüü-elemendid, saab esitada seotud linke teistele saidi lehekülgedele. Konfigureeritud üksused ilmuvad seejärel päise navigeerimises. 

- **Otsing** – otsingu moodul võimaldab kasutajatel sisestada otsinguterminid toodete otsimiseks. Vaikimisi otsingulehe URL ja otsingupäringu parameetrid peavad olema antud jaotises **Saidi sätted \> Laiendused**. Otsingu moodulil on atribuudid, mis võimaldavad teil vajadusel otsingunupu peita või soovikohaselt sildistada. Otsingumoodul toetab ka automaatse soovitamise valikuid, näiteks nagu toote, võtmesõna ja kategooria otsitulemused.

- **Ostukorvi ikoon** – ostukorvi ikooni moodul tähistab ostukorvi ikooni, mis näitab ostukorvis olevate kaupade arvu igal ajahetkel. Lisateavet vt teemast [Ostukorvi ikooni moodul](cart-icon-module.md).

## <a name="create-a-header-module-for-a-page"></a>Lehele päise mooduli loomine

Päise mooduli loomiseks tehke järgmist.

1. Avage **Fragmendid** ja valige uue fragmendi loomiseks **Uus**.
1. Valige dialoogiboksis **Uus lehe fragment** moodul **Konteiner**, sisestage lehe fragmendi nimi ja valige seejärel **OK**.
1. Valige pesa **Vaikekonteiner** ja seejärel määrake parempoolsel atribuutide paanil atribuudi **Laius** väärtuseks **Täida konteiner**.
1. Valige pesas **Vaikekonteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodulid **Reklaambänner** ja **Küpsistega nõustumine** ning seejärel **OK**.
1. Valige pesas **Vaikekonteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Konteiner** ja klõpsake seejärel **OK**.
1. Valige pesa **Konteiner** ja seejärel määrake parempoolsel atribuutide paanil atribuudi **Laius** väärtuseks **Täida konteiner**.
1. Valige pesas **Konteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Päis** ja klõpsake seejärel **OK**.
1. Valige päise mooduli pesas **Navigeerimismenüü** kolmikpunkt (**...**) ja seejärel **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Navigeerimismenüü** ja klõpsake seejärel **OK**.
1. Konfigureerige navigeerimismenüü atribuutide paanil vajaduse järgi atribuudid.
1. Valige päise mooduli pesas **Otsing** kolmikpunkt (**...**) ja seejärel **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Otsing** ja klõpsake seejärel **OK**.
1. Konfigureerige otsingumooduli atribuutide paanil vajaduse järgi atribuudid.
1. Valige päise mooduli pesas **Ostukorvi ikoon** kolmikpunkt (**...**) ja seejärel **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Ostukorvi ikoon** ja klõpsake seejärel **OK**.
1. Konfigureerige ostukorvi ikooni mooduli atribuutide paanil vajaduse järgi atribuudid. Kui soovite, et ostukorvi ikoon kuvaks ostukorvi kokkuvõtet (tuntud ka kui miniostukorv), kui kasutaja hiirt selle kohal hoiab, siis valige **Kuva miniostukorv**.
1. Valige **Salvesta**, valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

Päise igal lehel kuvamise tagamiseks järgige neid samme iga malli jaoks, mis on saidi jaoks loodud.

1. Lisage mooduli **Vaikeleht** pesas **Päis** loodud jaluse fragment.
1. Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Konteineri moodul](add-container-module.md)

[Ostukasti moodul](add-buy-box.md)

[Ostukorvimoodul](add-cart-module.md)

[Ostukorvi ikooni moodul](cart-icon-module.md)

[Väljaregistreerimismoodul](add-checkout-module.md)

[Tellimuse kinnituse moodul](order-confirmation-module.md)

[Päise moodul](author-header-module.md)

[Jaluse moodul](author-footer-module.md)
