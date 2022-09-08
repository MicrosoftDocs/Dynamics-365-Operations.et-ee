---
title: Otsingutulemuste moodul
description: See artikkel katab otsingutulemuste moodulid ja kirjeldab, kuidas lisada neid saidi lehtedele moodulis Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 08/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: eeb7cd0769fcb866a3d7dcc03e8e87daf24b2c5d
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405289"
---
# <a name="search-results-module"></a>Otsingutulemuste moodul

[!include [banner](includes/banner.md)]

See artikkel katab otsingutulemuste moodulid ja kirjeldab, kuidas lisada neid saidi lehtedele moodulis Microsoft Dynamics 365 Commerce.

Otsingutulemuste moodul annab tulemuseks tooteotsingu ja loendi tootele kohaldatavatest filtritest. Dynamics 365 Commerce'i saitide otsingumooduleid saab kasutada järgmiste stsenaariumidega saitide renderdamiseks.

- Kasutajaotsingu käivitatud otsingutulemused
- Otsingutulemused, mis näitavad kindlat tootekomplekti, nt "Osta sarnaseid tooteid"
- Kindlasse kategooriasse kuuluvate toodete loendid

Lisateavet kategooria ja otsingutulemuste lehtede kohta vt jaotisest [Vaikekategooria sihtleht ja otsingutulemuste lehe ülevaade](category-search-page-overview.md).

Järgmisel joonisel on kujutatud Fabrikami saidi kategooria otsingutulemuste leht.

![Otsingutulemuste lehe näide Fabrikami saidil.](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a>Otsingutulemuste mooduli atribuudid

Järgmises tabelis loetletakse otsingutulemimoodulite atribuudid koos nende väärtuste ja kirjeldustega.

| Atribuut | Väärtused | Kirjeldus |
|----------|--------|-------------|
| Kaupu lehekülje kohta | Täisarv | Kaupade arv, mis tuleb igal lehel kuvada. |
| Luba PDP naasmine | **Tõene** või **Väär** | Kui see atribuut on seatud väärtusele **Tõene**, siis kui kasutaja valib otsingutulemuste lehel toote, kuvatakse avatud toote üksikasjade lehe (DPD) lingireal link "Tagasi tulemuste juurde". |
| Laienda piiritlusatribuudid | **Kõik**, **1**, **2**, **3**, or **4** | Parimate filtrite arv, mis tuleks lehe laadimisel laiendada. Näiteks kui selle atribuudi väärtuseks on seatud **3**, laiendatakse leheküljel esimesed kolm filtrit. |
| Peida kategooriahierarhia kuvamine | **Tõene** või **Väär** | Kui atribuudi väärtuseks on seatud **Tõene**, on leheküljel kategooriahierarhia kuvamine peidetud. Kui kasutate kategooria hierarhia kuvamiseks [lingirea moodulit](add-breadcrumb.md), peaks see atribuut olema seasitatud olekusse **Tõene**.|
| Tooteatribuutide kaasamine otsingutulemitesse | **Tõene** või **Väär** | Kui selle atribuudi väärtuseks on seadistatud **Tõene**, tagastatakse otsingutulemustes toodete atribuudid. Kuigi neid atribuute saab Commerce'i saidil kuvada, on vajalik laiendus.|
| Kuva sidusettevõtte hinnad | **Tõene** või **Väär** | Kui selle atribuudi väärtuseks on seatud **Tõene**, kuvatakse toote allahindluse hinnad otsingutulemustes, kui lehte sirvib sisselogitud kasutaja. |
| Värskenda piiritluspaneeli | **Tõene** või **Väär** | Kui selle atribuudi väärtuseks on seatud **Tõene**, värskendatakse piiritluspaneeli, kui valitud on piiritlejad. Selles režiimis käituvad mõned mitme valikuga rafineerimistehased piiritluspaneeli värskendamisel nagu ühe valikuga rafineerimistehased. |

> [!IMPORTANT]
> Rakenduse Commerce väljalaskes 10.0.16 ja uuemas saab konfiguratsiooni **Kuva allahindluse hinnad** kasutada allahindluse hindade lehel näitamiseks.
>
> Commerce'i versiooni 10.0.20 väljalaskes ja uuemates versioonides **Piiri värskendamise paneeli** konfiguratsiooni kasutada piiritluspaneeli värskendamiseks piiritluspaneeli valimise ajal.

## <a name="supported-modules"></a>Toetatud moodulid

Otsingutulemuse moodul toetab [kiirvaate moodulit](quick-view-module.md), mis võimaldab kasutajatel otsingutulemuste lehelt tooteteavet vaadata ja lisada asju ostukorvi.

## <a name="add-a-search-results-module-to-a-category-page"></a>Otsingutulemuste mooduli lisamine kategoorialehele

Otsingutulemuste mooduli lisamiseks saidikonstruktori kategoorialehele, järgige neid samme.

1. Avage **Mallid** ja valige uue malli loomiseks **Uus**.
1. Sisestage dialoogiboksi **Uus mall** nimi **Otsingutulemus** ja seejärel valige **OK**.
1. Kehapesas **valige** kolmikpunkt (...) ja seejärel valige **lisamoodul**.
1. Dialoogiaknas **Vali** moodulid valige vaikelehemoodul **ja** seejärel valige **OK**.
1. Vaikelehe **mooduli põhipesas** **valige kolmikpunkt (...) ja seejärel valige lisamoodul** **.**
1. Dialoogiaknas **Vali** moodulid valige konteinerimoodul **ja** seejärel valige **OK**.
1. **Valige konteineri** pesast kolmikpunkt (...) ja seejärel valige **lisamoodul**.
1. Dialoogiaknas **Vali** moodulid valige moodul **Breadcrumb** ja seejärel valige **OK**.
1. Sisestage atribuutide paanile **Lingirida** väärtus **1** üksuse **Miinimum esinemiskorrad** puhul.
1. **Valige konteineri** pesast kolmikpunkt (...) ja seejärel valige **lisamoodul**.
1. Dialoogiaknas **Vali** moodulid valige otsingutulemuste **moodul** ja seejärel valige **OK**.
1. Sisestage atribuutide paanil **Otsingutulemused** väärtus **1** üksuse **Miiniumu esinemiskorrad** puhul ja seejärel seadistage mistahes muud vajalikud otsingutulemuste mooduli atribuudid. Mallis nende atribuutide seadmisega tagate, et konkreetse kategooria lehekülje kohandused kaasavad need sätted automaatselt.
1. Valige **Lõpeta redigeerimine** ja seejärel valige malli avaldamiseks **Avalda**.
1. Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.
1. Dialoogiaknas **Uue lehe loomine** sisestage jaotises **Lehe nimi** kategooria **ja** seejärel valige väärtus **Edasi**.
1. Valige **valiku Vali mall** all **loodud otsingutulemuste** mall ja seejärel klõpsake nuppu **Edasi**.
1. Valige **valiku Vali paigutus** all lehekülje paigutus (nt Paindlik **paigutus**) ja seejärel klõpsake nuppu **Edasi**.
1. Vaadake **jaotises Ülevaade ja lõpetamine** üle lehe konfiguratsioon. Kui teil on vaja lehekülje teavet redigeerida, valige **Tagasi**. Kui lehekülje teave on õige, valige Loo **leht**.
1. Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="inventory-aware-search-results-module"></a>Laoseisule teadliku otsingutulemuste moodul

Otsingutulemuste moodulit saab konfigureerida nii, et see hõlmaks laoandmeid ja pakkuda järgmisi kogemused:

- Kuvab kaubavaru taseme sildid koos toodetega.
- Laost väljas toodete peitmine tooteloendist
- Kuvab tooteloendi lõpus laost väljas tooted.
- Toetab laopõhise toote filtreerimist.

Nende kogemuste lubamiseks peate esmalt **lubama täiustatud e-commerce’i** tootetuvastuse varude teadmise funktsioonina ja seejärel konfigureerima mõned eeltingimuste sätted Commerce Headquartersis. Lisateavet vt varudest teadmise [tooteloendist](inventory-aware-product-listing.md).

## <a name="additional-resources"></a>Lisaressursid

[Kategooria vaikesihtlehe ja otsingutulemuste lehe ülevaade](category-search-page-overview.md)

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Kiirvaatemoodul](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
