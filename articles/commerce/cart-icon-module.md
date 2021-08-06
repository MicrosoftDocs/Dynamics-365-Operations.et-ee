---
title: Ostukorvi ikooni moodul
description: See teema hõlmab ostukorvi ikooni moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d9e3850d98e716d1bbea2017f6e8c9d75f19adc9
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/17/2021
ms.locfileid: "6637997"
---
# <a name="cart-icon-module"></a>Ostukorvi ikooni moodul

[!include [banner](includes/banner.md)]

See teema hõlmab ostukorvi ikooni moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

Ostukorvi ikooni moodul tähistab ostukorvi lehe päisemoodulis ja kuvab ostukorvis olevate kaupade arvu. Ostukorvi ikooni moodul kuvab ka ostukorvi kokkuvõtte (tuntud ka kui väike ostukorv), kui hiirt hõljutatakse üle ostukorvi. Väike ostukorv esitab kasutajale kokkuvõtte ostukorvis olevatest kaupadest, ilma et peaksite liikuma ostukorvi lehele. Lisaks võimaldab see kasutajal ka otse kassa lehele minna, kui nad on kokkuvõttega rahul. See vähendab lehekülgede vahel liikumiste arvu ja teeb väljaregistreerimise kiiremaks. 

Järgmisel pildil on kuvatud näide ostukorvi ikooni moodulist, kus on kuvatud Fabrikami päises miniostukorv.

![Ostukorvi ikooni mooduli näide.](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a>Mooduli atribuudid

- **Kuva väike ostukorv** – kui on tõene, võimaldab see atribuut kuvada ostukorvi kokkuvõtte (väikese ostukorvi) hiire hõljutamisel ostukorvi ikooni kohal. Seda funktsiooni toetatakse ainult töölaua vaateportide korral.

## <a name="module-properties-in-the-adventure-works-theme"></a>Mooduli atribuudid Adventure Works teemas

Adventure Works teema kujunduses sisaldab ostukorvi ikoonimoodul kaht täiendavat pesa minikorvi jaoks. Need pesad lisatakse mooduli definitsiooni laiendina.

- **Tühjad ostukorvi kampaaniad** – see pesa võtab sisubloki mooduli. Kui ostukorv on tühi, kuvatakse määratud sisubloki moodul. Sisublokaadi moodulit saab kasutada kampaaniate, turunduse sisu ja kategooria lehtede linkide jaoks, et aidata klientidel ostuteed jätkata.
- **Kampaaniasisu** – seda pesa saab kasutada kampaaniate näitamiseks, nt "Tasuta saatmine suurema tellimuse puhul kui $100." Kampaaniasisu pesas saab kasutada sisublokki, tekstiblokki ja pildiloendi mooduleid.

Järgmine pilt näitab ostukorvi ikoonimooduli näidet Adventure Worksi kujunduses, mis kuvab soodussisu minikorvis.

![Ostukorvi ikoonimooduli näide Adventure Worksi kujunduses](./media/AW_minicart.PNG)

> [!IMPORTANT]
> Adventure Works teema pesad on saadaval alates Dynamics 365 Commerce väljalaske versioonist 10.0.20.

## <a name="add-a-cart-icon-module-to-a-page"></a>Lehele ostukorvi ikooni mooduli lisamine

Ostukorvi ikooni mooduli lisamiseks vaadake teemat [Päise moodul](author-header-module.md).

## <a name="additional-resources"></a>Lisaressursid

[Ostukorvimoodul](add-cart-module.md)

[Maksmismoodul](add-checkout-module.md)

[Makse moodul](payment-module.md)

[Tarneaadressi moodul](ship-address-module.md)

[Tarnevalikute moodul](delivery-options-module.md)

[Järeletulemisteabe moodul](pickup-info-module.md)

[Tellimuse üksikasjade moodul](order-confirmation-module.md)

[Kinkekaardi moodul](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
