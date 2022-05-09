---
title: Otsingutulemuste moodul
description: See teema hõlmab otsingutulemuste mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
ms.date: 04/21/2022
ms.topic: article
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
ms.openlocfilehash: 15b3bb50eb0b75fa19ac8e136da83cb362b4cec6
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/27/2022
ms.locfileid: "8644922"
---
# <a name="search-results-module"></a>Otsingutulemuste moodul

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

See teema hõlmab otsingutulemuste mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

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

Otsingutulemuste mooduli lisamiseks kategoorialehele toimige järgmiselt.

1. Avage **Mallid** ja valige uue malli loomiseks **Uus**.
1. Sisestage dialoogiboksi **Uus mall** nimi **Otsingutulemus** ja seejärel valige **OK**.
1. Valige lahtris **Keha** kolmikpunkt (...) ja seejärel valige **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Vaikeleht** ja klõpsake seejärel **OK**.
1. Valige lahtris **Peamine** moodulis **Vaikeleht** kolmikpunkt (...) ja seejärel valige **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Konteiner** ja klõpsake seejärel **OK**.
1. Valige lahtris **Konteiner** kolmikpunkt (…) ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Lingirida** ja klõpsake seejärel **OK**.
1. Sisestage atribuutide paanile **Lingirida** väärtus **1** üksuse **Miinimum esinemiskorrad** puhul.
1. Valige lahtris **Konteiner** kolmikpunkt (…) ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Otsingutulemused** ja klõpsake seejärel **OK**.
1. Sisestage atribuutide paanil **Otsingutulemused** väärtus **1** üksuse **Miiniumu esinemiskorrad** puhul ja seejärel seadistage mistahes muud vajalikud otsingutulemuste mooduli atribuudid. Mallis nende atribuutide seadmisega tagate, et konkreetse kategooria lehekülje kohandused kaasavad need sätted automaatselt.
1. Valige **Lõpeta redigeerimine** ja seejärel valige malli avaldamiseks **Avalda**.
1. Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.
1. Valige dialoogiboksis **Malli valik** loodud **Otsingutulemuste** mall, sisestage **Kategooria leht** üksuse **Lehekülje nimi** jaoks ja seejärel valige **OK**. Kuna kõik väärtused on mallis seadistatud, on lehekülg avaldamiseks valmis.
1. Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="enable-inventory-awareness-for-the-search-results-module"></a>Lubage otsingutulemuste mooduli jaoks varude teadlikkus

Kliendid eeldavad üldiselt, et e-äri veebisait on laost kursis kogu sirvimise kogemuse jooksul, nii et nad saavad otsustada, mida teha, kui tootel varusid pole. Otsingutulemuste moodulit saab konfigureerida nii, et see hõlmaks laoandmeid ja pakkuda järgmisi kogemused:

- Saate kuvada varude saadavuse sildi koos tootega.
- Laost väljas toodete peitmine tooteloendist
- Näitab tooteloendi lõppu laost väljas valmistatud tooteid.
- Filtreerige tooted otsingutulemuste alusel laovarude taseme alusel.

Nende kogemuste lubamiseks peate esmalt lubama **täiustatud e-commerce'i** tootetuvastuse varudele vastavalt funktsioonihalduse **tööruumis**.

> [!NOTE]
> **Täiustatud e-commerce'i tootetuvastuse** varudest teadmise funktsioon on saadaval commerce version 10.0.20 väljaandes ja hilisemates versioonides.

Laoseisust teadmise tooteotsing kasutab tooteatribuudiid varude saadavusteabe saamiseks. Funktsiooni eeltingimusena tuleb luua sihtotstarbelised tooteatribuudid, varude andmed tuleb nende jaoks sisestada ja need tuleb lisada võrgukanalile. 

Selleks, et luua sihtotstarbelised tooteatribuudid varudele teadmise otsingutulemuste mooduli toetamiseks, järgige neid samme.

1. Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Tooted ja varud**.
1. Valige ja avage **asusta tooteatribuudid laotasemega**.
1. Sisestage dialoogiboksis järgmine teave:

    1. Määrake toote **atribuudi ja tüübi nime** väljal sihtotstarbeline tooteatribuudi nimi, mis luuakse varude andmete hõivamiseks.
    1. Väljal Varude **saadavus valige** koguse tüüp, mis peaks laovarude taseme arvutamine põhinema (nt Füüsiline **saadavus**). 

1. Saate töö taustal käivitada. Kuna toote laovaru muudatusi luhkavas keskkonnas, soovitame tungivalt selle töö pakktöötlusena planeerida.

> [!NOTE]
> Oma e-äri veebisaidi lehtede ja moodulite ühtse laotaseme arvutamiseks valige kindlasti sama kogusetüüp nii varude saadavuse puhul kui **ka** Commerce headquartersis **ja Ärisaidi koostajas sättel põhinev** varude tase. Saidiehitaja kohta lisateabe saamiseks vt teemat [Varude sätete rakendamine](inventory-settings.md).

Võrgukanali toote atribuutide konfigureerimiseks järgige neid samme. 

1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kanali kategooriad ja toote atribuudid**.
2. Valige võrgukanal, et lubada laoteadpõhise otsingu tulemuste moodul.
3. Valige ja avage seostatud atribuudigrupp ning seejärel lisage vastloodud toote atribuut.
4. Commerce'i versioonide puhul enne 10.0.27 väljalaset valige suvand Atribuudi metaandmete määramine, valige uuesti lisatud tooteatribuut ja seejärel lülitage sisse kanali atribuut Näita, **Toomine**, **·** **Saab** muuta ja neid saab **päringusse** teha.**·**
5. Minge jaemüügi **ja rakenduse Commerce \> Retail ja Commerce IT jaotusgraafikusse \>** ja käitage **1150-töö** (kataloog). Kui planeerite **tooteatribuudid** laotaseme tööga pakktöötlusena, on soovitatav planeerida 1150-töö ka pakett-tööna, mis töötab samas sageduses.

> [!NOTE]
> Toodete puhul, mida näidatakse otsingutulemuste moodulis, kuvatakse varude tase üksiku varianditaseme asemel põhitoote tasemel. Sellel on ainult kaks võimalikku väärtust: "saadaval" ja "laost otsas". Väärtuse tegelik silt tuuakse laotaseme profiili [määratlusest](inventory-buffers-levels.md). Meistritoode loetakse laost lõppenuks ainult siis, kui kõik selle variandid on otsas.

Kui kõik eelnevad konfiguratsioonietapid on lõpule viidud, kuvavad otsingutulemuste lehtede täpsustajad varudepõhist filtrit ja otsingutulemuste moodul hangib laoandmed kulisside taga. Seejärel saate Commerce saidi koostajas konfigureerida sätte **Tooteloendi lehtede laosätted**, et juhtida seda, kuidas otsingutulemuste moodul kuvab laost otsas tooteid. Lisateavet vt teemast [Varude sätete rakendamine](inventory-settings.md).

## <a name="additional-resources"></a>Lisaressursid

[Kategooria vaikesihtlehe ja otsingutulemuste lehe ülevaade](category-search-page-overview.md)

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Kiirvaatemoodul](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
