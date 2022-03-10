---
title: Otsingutulemuste moodul
description: See teema hõlmab otsingutulemuste mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
ms.date: 10/15/2021
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
ms.openlocfilehash: bae825ed7093494c48abac119c480be0dba4f951
ms.sourcegitcommit: 9c2bc045eafc05b39ed1a6b601ccef48bd62ec55
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/14/2021
ms.locfileid: "7919470"
---
# <a name="search-results-module"></a>Otsingutulemuste moodul

[!include [banner](includes/banner.md)]


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

Kliendid eeldavad üldiselt, et e-kaubanduse sait on kogu sirvimiskogemuse jooksul laoseisust teadlik, et nad saaksid otsustada, mida teha, kui toote laoseis puudub. Otsingutulemuste moodulit saab täiustada nii, et see hõlmaks laoandmeid ja pakuks järgmisi kasutuskogemusi.

- Näidake koos toodetega varude saadavuse silti.
- Peida laost otsas olevad tooted.
- Kuvage otsingutulemuste loendi lõpus laost otsas olevad tooted.
    
Nende kasutuskogemuste lubamiseks peate Commerce'i peakorteris konfigureerima järgmised eeltingimusesätted.

### <a name="enable-the-enhanced-e-commerce-product-discovery-to-be-inventory-aware-feature"></a>Lubage täiustatud e-kaubanduse tootetuvastuse funktsioon, et olla varude suhtes teadlik

> [!NOTE]
> Funktsioon **Täiustatud e-kaubanduse tootetuvastus, et olla laoseisust teadlik** on saadaval alates Commerce'i versiooni 10.0.20 väljalaskest.

Et lubada Commerce'i peakorteris **Täiustatud e-kaubanduse tootetuvastuse funktsioon laoseisust teadlikuks**, järgige neid samme.

1. Avage **Tööruumid \> Funktsioonihaldus**.
1. Otsige funktsiooni **Täiustatud e-kaubanduse tootetuvastuse** ja lubage see.

### <a name="configure-the-populate-product-attributes-with-inventory-level-job"></a>Konfigureerige toote atribuutide täitmine laotaseme tööga

Töö **Tooteatribuutide täitmine laotasemega** loob varude saadavuse jäädvustamiseks uue tooteatribuudi ja määrab seejärel selle atribuudi iga põhitoote uusimale laotaseme väärtusele. Kuna müüdava toote või sortimendi laovarude saadavus muutub pidevalt, soovitame tungivalt ajastada töö partiiprotsessina.

Töö **Tooteatribuutide täitmine laotasemega** konfigureerimiseks Commerce'i peakorteris toimige järgmiselt.

1. Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Tooted ja varud**.
1. Valige **Toote atribuutide täitmine laotaseme tööga**.
1. Dialoogiaknas **Tooteatribuutide täitmine laotasemega** toimige järgmiselt.

    1. Määrake jaotises **Parameetrid** väljal **Toote atribuut ja tüübi nimi** nimi spetsiaalsele tooteatribuudile, mis luuakse varude saadavuse jäädvustamiseks.
    1. Valige jaotises **Parameetrid** väljal **Laovarude saadavus** kogus, millel laoseisu arvutamine peaks põhinema (nt **Saadaval füüsiliselt**).
    1. Jaotises **Käita taustal** konfigureerige töö taustal töötama ja soovi korral lülitage sisse valik **Partiitöötlus**. 

> [!NOTE]
> Oma e-kaubanduse saidi PDP-de ja tooteloendi lehtede järjepidevaks varude taseme arvutamiseks valige kindlasti sama koguse valik nii Commerce'i peakorteri sätte **Varude saadavuse põhjal** kui ka **Varude taseme jaoks, mis põhineb** säte Commerce saidiehitajas. Saidiehitaja kohta lisateabe saamiseks vt teemat [Varude sätete rakendamine](inventory-settings.md).

### <a name="configure-the-new-product-attribute"></a>Seadistage uue toote atribuut

Pärast töö **Tooteatribuutide täitmine laotasemega** käivitamist peate konfigureerima äsja loodud tooteatribuudi e-kaubanduse saidil, kus soovite otsingutulemuste mooduli jaoks lubada laoseisu.

Uue tooteatribuudi konfigureerimiseks Commerce'i peakorteris toimige järgmiselt.

1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kanali kategooriad ja toote atribuudid** ja valige e-kaubanduse sait.
1. Valige ja avage seotud atribuutide rühm, lisage sellele äsja loodud tooteatribuut ja seejärel sulgege leht.
1. Valige **Määra atribuudi metaandmed**, valige äsja lisatud tooteatribuut ja seejärel lülitage sisse **Kuva atribuut kanalil**, **Laaditav**, **Saab täpsustada** ja **Saab küsida** valikud.

> [!NOTE]
> Otsingutulemuste moodulis kuvatavate toodete puhul sisestatakse varude tase põhitoote tasemel, mitte üksiku variandi tasemel. Sellel on ainult kaks võimalikku väärtust: "saadaval" ja "laost otsas". Väärtuste tegelik tekst hangitakse [laotaseme profiili](inventory-buffers-levels.md) definitsioonist. Meistritoode loetakse laost lõppenuks ainult siis, kui kõik selle variandid on otsas. Variandi varude tase määratakse toote laotaseme profiili definitsiooni alusel. 

Kui kõik eelnevad konfiguratsioonietapid on lõpule viidud, kuvavad otsingutulemuste lehtede täpsustajad varudepõhist filtrit ja otsingutulemuste moodul hangib laoandmed kulisside taga. Seejärel saate Commerce saidi koostajas konfigureerida sätte **Tooteloendi lehtede laosätted**, et juhtida seda, kuidas otsingutulemuste moodul kuvab laost otsas tooteid. Lisateavet vt teemast [Varude sätete rakendamine](inventory-settings.md).

## <a name="additional-resources"></a>Lisaressursid

[Kategooria vaikesihtlehe ja otsingutulemuste lehe ülevaade](category-search-page-overview.md)

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Kiirvaatemoodul](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
