---
title: Ärikataloogide laiendatav mõju B2B-kohandustele
description: Selles teemas kirjeldatakse ärikataloogide laiendatavuse mõju B2B-funktsioonile moodulis Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 04/28/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: aff333bfe8003233dd5d8181aa8c5dd7eaeffcd0
ms.sourcegitcommit: 0abc777986112ea2332f5bf0e815b303b952356c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/29/2022
ms.locfileid: "8657187"
---
# <a name="extensibility-impact-of-commerce-catalogs-for-b2b-customizations"></a>Ärikataloogide laiendatav mõju B2B-kohandustele

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Selles teemas kirjeldatakse ärikataloogide **laiendatavuse mõju B2B-funktsioonile** moodulis Microsoft Dynamics 365 Commerce.

Kui soovite kataloogi konteksti kohandatud stsenaariumitele laiendada, võib teie kohandusi vajada uuendada. See värskendus järgib standardset protsessi, mida kliendid peavad järgima, kuna nende kohandused ei pruugi pärast täienduste viimast funktsioone automaatselt toetada. Kui teie kohandused sisaldavad oma kogemuses mis tahes uut funktsiooni või viga parandusi, soovitame kohandamiskoodi vastavalt värskendada. See värskendus sarnaneb muudatustega, mida Microsoft võib teha tuumkoodi kohta.

Vaadake üle kohandusjuhtumid, mis järgnevad määramaks, kas teie kohandusi tuleb uuendada.

> [!NOTE]
> - Kõik toote rakenduse programmeerimisliidesed (API-d) peavad olema kataloogiga kursis. Seepärast on kriitiline, et te läbite **CatalogID parameetri**.
> - Vaikekataloog (**CatalogID0**=**·**) ei ole kehtiv kataloog sisselogitud ettevõtete vahel (B2B) kasutajatele. Seetõttu nurjuvad kõik API kutsed, mis läbivad "0" või kasutavad vaikeväärtust, sest saidi kasutajatel pole juurdepääsu kataloogile 0. Õige kogemuse saamiseks tuleb kliendi API kutsed uuendada nii, et nad läbivad kataloogi valijas valitud kataloogi ID. Kui kasutate vaikeväärtust ja kasutaja vahetab katalooge, peaks veebisait esitama andmed valitud kataloogi kohta. Seetõttu peaksid kohandatud API-d valitud kataloogi läbima, et sobida API-d, mis käitatakse rakenduse põhikoodist.

Järgmised kohandamisjuhtumid nõuavad arenduse uuendusi:

- **1. juhtum:** klient tutvustab enda andmetegevusi [,](e-commerce-extensibility/data-actions.md) mis kutsub tootega seotud API-d või andmetegevusi. Vajalikud on järgmised värskendus etapid:

    1. Kui andmetegevus kasutab otse API kutset, uuendage andmetegevus nii, et see läbiks kataloogi ID, nagu näha järgmises näite näites.

        ![Uuendatud andmetegevus, mis läbib kataloogi ID.](./media/customization1_a.png)

    1. Kui andmetegevus kutsub kohandamise sees muud tootega seotud andmetegevust, tuleb koodi uuendada nii, et see läbiks mõned uued parameetrid, nt **requestContext**. Parameetrit **requestContext** kasutatakse praeguse kataloogi ID toomiseks, nagu näidatud järgmises näite näites.

        ![Uuendatud andmetegevus, mis läbib uue parameetri.](./media/customization1_b.png)

- **2. juhtum** : kliendil [on alistatud andmetegevus](e-commerce-extensibility/data-action-overrides.md). Nõutav on järgmine uuendussamm:

    - Värskendage andmetegevus nii nagu 1. juhtumi puhul.

- **Juhtum 3:** kliendil on vaate laiend, skripti moodul või moodul, [mis sisaldab kutseid](e-commerce-extensibility/modules-overview.md#clone-a-module-library-module) API-le või andmetegevusse. Nõutav on järgmine uuendussamm:

    - Uuendage koodi nii, nagu see on 1. juhtumi puhul, nagu näha järgmises näite näites.

       ![Uuendatud kood, mis edastab uue parameetri.](./media/customization3.png)

- **4. juhtum:** klient kasutab getById **API** kutset. Nõutav on järgmine uuendussamm:

    - Minge selle asemel **getByIds** API kutsele, **sest getById** URL-kutsel on mõned piirangud ja see ei toeta kataloogiteadmist.

- **5. juhtum:** kliendil on andmetegevus, mis toob teavet mitme toote kohta, mis võivad olla erinevatest kataloogidest. Nõutav on järgmine uuendussamm:

    - Tükelda API kõned kataloogi ID järgi. Näiteks ostukorvi API-de puhul võib ostukorv sisaldada tooteid erinevatest kataloogidest. Tooteread tuleb grupeerida kataloogi ID järgi ja need peavad kutsuma API-d iga kataloogi puhul eraldi, nagu näha järgmises näite näites.

        ![Uuendatud andmetegevus, mis rühmitab tooteread kataloogi ID järgi.](./media/customization5.png)

## <a name="additional-resources"></a>Lisaressursid

[Looge B2B-saitide jaoks ärikataloogid](catalogs-b2b-sites.md)

[B2B KKK ärikataloogid](catalogs-b2b-sites-FAQ.md)
