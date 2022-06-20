---
title: Adventure Works teema ülevaade
description: See artikkel annab ülevaate Adventure Worksi kujundusest ja kirjeldab selle rakendumist saidi lehtedele teemas Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 12/03/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4f13d6c1c4b0e2764c22dc3d7311c726fac7989d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874983"
---
# <a name="adventure-works-theme-overview"></a>Adventure Works teema ülevaade

[!include [banner](includes/banner.md)]

See artikkel annab ülevaate Adventure Worksi kujundusest ja kirjeldab selle rakendumist saidi lehtedele teemas Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce e-kaubanduse teema nimega Adventure Works. Adventure Worksi teemas kuvatakse spordi- ja matitooted ning optimeeritakse rikaste ja täiustatud täiustatud teletellingikogemuse jaoks. See pakub tänapäevast ilmet, uusi kavandeid ja meelelahutusefektisid, et luua e-äri klientidele elev e-kaubanduse kogemus.

## <a name="trial-environments-in-commerce"></a>Proovikeskkonnad Commerce'is

Kui soovite näha, kuidas Adventure Works'i teema välja näeb, kui see on paigutatud ettevõtetelt tarbijatele (B2C) ja ettevõtetevahelisele (B2B) saitidele, külastage järgmisi proovisaite.

- [Adventure Worksi B2C sait](https://www.adventure-works.com/)
- [Adventure Worksi B2B sait](https://www.adventure-works.com/business)

## <a name="theme-capabilities"></a>Teema võimalused

Adventure Worksi teema annab järgmised uued võimalused:

- Videomängija moodul toetab nüüd pealkirja, lõigu ja lingi funktsiooni täiendavate ülekannete jaoks.
- Animatsiooni kaudu on sisu paremad üleminekud.
- "Ostukorvi lisamise" toiming käivitab minikorvi teatise esitamise asemel.
- Kiirvaatemoodul on paan, mis saitidelt asub nii töölaual kui ka mobiilsetes vaateportides.
- Saidilehtedel on uued kavandid. 
- Turundussisu saab konfigureerida ostukorvi ja minikorvi jaoks (kui need on tühjad).
- Minikorv võib kuvada kampaaniateateid, nt "Tasuta saatmine üle $50 tellimuste korral."
- Kirjelduskaarte renderdatakse otsingu- ja kategoorialehtedel.

Adventure Worksi teema sisaldab nüüd Commerce'i mooduliteegis järgmisi ihaldusmooduleid:

- [Paaniloendi moodul](tile-list-module.md)
- [Interaktiivse funktsiooni moodul](interactive-feature-module.md)
- [Aktiivse pildi moodul](active-image-module.md)
- [Tellimismoodul](subscribe-module.md)
- [Pildiloendi moodul](image-list-module.md)

Adventure Worksi teema on täielikult vaatega ja pakub töölaua, mobiili ja tahvelarvuti vaateportide optimeeritud kogemust.

> [!IMPORTANT]
> Adventure Works teema ja uued moodulid on saadaval alates Dynamics 365 Commerce väljalaske versioonist 10.0.20.

Järgmine näide näitab näidet avalehe kohta, mis kasutab Adventure Worksi kujundust.

![Näide kodulehe kohta, mis kasutab Adventure Worksi kujundust](./media/aw_b2c.PNG)

Järgmine näide näitab näidet loendi lehe kohta, mis kasutab Adventure Worksi kujundust.

![Näide loendilehe kohta, mis kasutab Adventure Worksi kujundust](./media/Aw_list.PNG)

Järgmine pilt näitab näidet toote üksikasjade lehe (PDP) kohta, mis kasutab Adventure Worksi kujundust.

![Näide toote üksikasjade lehe (PDP) kohta, mis kasutab Adventure Worksi kujundust](./media/aw_pdp.PNG)

## <a name="use-the-adventure-works-theme-for-b2b-sites"></a>Kasutage Adventure Worksi kujundust B2B-saitide puhul

Adventure Worksi teema on ka viitekujundus ettevõtetele (B2B) saitidele. Adventure Worksi teemas kuvatakse kõik B2B moodulid ja töövood. Lisateavet B2B saidi häälestamise kohta vt teemast [B2B saidi häälestus](./b2b/set-up-b2b-site.md).

Järgmine pilt näitab näidet B2B avalehe kohta, mis kasutab Adventure Worksi kujundust.

![Näide B2B kodulehe kohta, mis kasutab Adventure Worksi kujundust](./media/aw_b2b.PNG)

## <a name="theme-extensions"></a>Kujunduse laiendid

Adventure Worksi teema sisaldab mitut teemalaiendit, nt **Vaate laiendeid** ja **Mooduli määratluse** laiendeid. Adventure Worksi kujundust saab kasutada sarnaste laienduste järgus viitekujunduseks. Näiteks loendileht Adventure Worksi kujunduses rakendatakse horisontaalse täpsustajaga vaate laiendina. (Vastandina kasutatakse Fabrikami kujunduses vasakpaani täpsustajat.)

Sarnaselt hõlmavad muud moodulid mooduli definitsiooni laiendeid. Näiteks hõlmab [ostukorvi ikoonimoodul](cart-icon-module.md) kaht täiendavat **tühja ostukorvi** ja **kampaaniasisu** pesasid, mis on rakendatud mooduli definitsioon laiendite abil. Lisaks on päisemoodulisse lisatud uus **mobiilse logo** atribuut, et toetada mobiilsete vaateportide logo. See atribuut on rakendatud päisemooduli definitsiooni laiendina.

Lisateavet kujunduse laiendite kohta vt teemast [Kujunduse laiendid](e-commerce-extensibility/theme-module-extensions.md).

## <a name="install-the-adventure-works-theme"></a>Adventure Worksi kujunduse installimine

Lugege, kuidas installida Adventure Worksi kujundus, jaotisest [Installi Adventure Worksi kujundus](install-adventure-works.md).

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Paaniloendi moodul](tile-list-module.md)

[Interaktiivne funktsioonimoodul](interactive-feature-module.md)

[Aktiivne pildimoodul](active-image-module.md)

[Telli moodul](subscribe-module.md)

[Pildi loendi moodul](image-list-module.md)

[Kujunduse laiendid](e-commerce-extensibility/theme-module-extensions.md)

[Ostukorvi ikooni moodul](cart-icon-module.md)

[B2B e-kaubandussaidi häälestamine](./b2b/set-up-b2b-site.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
