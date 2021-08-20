---
title: Rakenduse Asset Management parameetrid
description: Rakenduses Asset Management tuleb seadistada varade, töökäskude ja töökäsu planeerimisega seotud parameetrid.
author: johanhoffmann
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4e1deef00f01d83bc809a004265c386ba9d300df5fa4a1be245812ed5632059f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751957"
---
# <a name="asset-management-parameters"></a>Rakenduse Asset Management parameetrid

[!include [banner](../../includes/banner.md)]

Rakenduses Asset Management tuleb seadistada varade, töökäskude ja töökäsu planeerimisega seotud parameetrid. Selles teemas kirjeldatakse nende seadistamist. Lehe avamiseks valige **Varahaldus** > **Seadistus** > **Varahalduse parameetrid**.

> [!NOTE]
> Kui soovite häälestada süsteemi, mis sisaldab varahalduse funktsioonide katsetamiseks demoandmeid, vt juhiseid teemast [Demokeskkonna juurutamine](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).

## <a name="the-assets-tab"></a>Vahekaart Varad

Vahekaart **Varad** sisaldab järgmisi sätteid.

- **Töö vaikeasukoht** on standardne töö asukoht, mis uute varade loomisel valitakse varades automaatselt.  
- Valige väljal **Standardne kalender** kalender, mida kasutatakse varade KPI-de arvutamiseks, kui varas pole ressurssi valitud.  
- Valige väljal **Vaade** standardne vaade, mis kuvatakse, kui avate suvandi **Varade vaade** (**Varahaldus** > **Ühine** > **Varad** > **Varade vaade**).
- **Taotluse vaiketüüp** on standardne hooldusnõude tüüp, mis valitakse automaatselt uue taotluse loomisel.  
- Töötüüpide eelarved talletatakse väljal **Eelarveprojekt** valitud projektis. Iga töötüübi puhul luuakse eelarveprojektis automaatselt uus tegevus. Töötüübi eelarved salvestatakse seejärel eelarveprojektis.  
- Valige väljal **Mudel** töötüübi ja töökäsu eelarvetes kasutatav eelarvemudel.

## <a name="the-work-orders-tab"></a>Vahekaart Töökäsud

Vahekaart **Töökäsud** sisaldab järgmisi sätteid.

- **Töökäsu vaiketüüp** määratleb standardsätted töökäsu loomisel.  
- **Ennetava töökäsu tüüp** määratleb töökäsu tüübi, mida kasutatakse töökäskude loomisel hoolduskavadest. Kui see väli jäetakse tühjaks, kasutatakse välja **Töökäsu vaiketüüp** töökäsu tüüpi.  
- Väljal **Seotud töökäsu mask** saate määratleda töökäskude maksimumarvu, mida saa töökäsuga siduda. Näiteks ## võimaldab teil siduda kuni 99 töökäsku. Kui määratlete siin kirjeldatud maski, nummerdatakse seotud töökäsud [töökäsuga seotud töökäsu töökäsu ID]-01,-02,-03 jne. Kui te sellel väljal maski ei määratle, saab seostuv töökäsk järgmise järjestikuste töökäsu ID.  
- Valige **Jah** suvandis **Kopeeri vead**, kui soovite automaatselt kopeerida töökäskudes registreeritud vead seotud hooldusnõuetesse. 
- Väljal **Tase** saate määratleda töö asukoha taseme, mis sisestatakse automaatselt töökäsku, kui kõik seotud töökäsu tööd viitavad samale töö asukohale. Kui kõik töökäsu tööd pole määratletud tasemel seotud sama töö asukohaga, jäetakse väli **Töö asukoht** töökäsul tühjaks. Näiteks kui sisestate sellele väljale numbri „1”, on see töö asukoha struktuuris ülemine tase. Kui sisestate sellele väljale numbri „0”, ei ole te määratlenud kindlat töö asukoha taset, vaid töökäsu kõik töökäsu tööd peavad olema seotud töökäsule lisatava töö asukoha sama töö asukoht.  
- Töökäsule tarbimise sisestamisel kasutatavaid töölehti saab valida kiirkaardi **Üldine** väljadel **Tund**, **Üksus** ja **Kulu**.  
- Väljal **Tootekeele allikas** valige, millist keelt kasutada varahalduse aruannetes olevate toodete nimede puhul. Saate valida ettevõtte kontol seadistatud keele, või praegu rakendusse sisse logitud kasutaja jaoks seadistatud keele.  
- Valige **Jah** suvandi **Reaalajas uuendus** jaoks, kui soovite automaatselt värskendada töö tüübi vaikeväärtuste, hoolduskavade ja hoolduskordade muudatusi.
  - Kui valite väärtuse **Ei**, ei uuendata töötüüpide vaikeväärtusi, hoolduskavasid ega hoolduskordi varahalduses automaatselt.
  - Kui teil on sünkroonitud suur hulk andmeid, nt mitu vara või töö asukohta, mis on seadistatud hoolduskavades või hoolduskordades või suur hulk hoolduskavasid või -kordi, valige väärtus **Ei**.  
  - Kui teete muudatusi töötüübi vaikeväärtustes või hoolduskavades või hoolduskordades ja olete reaalajas uuendamise jaoks valinud **Ei**, ei pruugita hoiatust kuvada, kui muudatused mõjutavad järgmist.
    - Hoolduskavades või -kordades seadistatud töö asukohad  
    - Hoolduskavades või -kordades seadistatud objektid  
    - Hoolduskavade seadistus  
    - Hoolduskordade seadistus  
- Kiirkaardil **Kategooria** saab määratleda töökäskude kasutamisega seotud vaikekategooriaid.  

## <a name="the-work-order-scheduling-tab"></a>Vahekaart Töökäsu plaanimine

Vahekaart **Töökäsu plaanimine** sisaldab kiirkaardi **Üldine** järgmisi sätteid.

- **Graafiku ajapiir** määratleb perioodi päevades, mis arvutatakse töökäsu eeldatavast alguskuupäevast, mille jooksul töökäsu töid planeeritakse.  
- **Koondplaan** on seotud mooduli **Organisatsiooni haldus** ressurssidega. Kui valite sellel väljal koondplaani, saate vaadata töökäskudega seotud võimsuse reserveerimisi valikus **Võimsuse reserveerimised** (**Organisatsiooni haldus** > **Ressursid** > **Ressursid** > valige ressurss vahekaardil > **Ressurss** nupp > **Võimsuse reserveerimised**). Kui jätate selle välja tühjaks, saate vaadata töökäskude täiskoormusi valikus **Täiskoormus** (**Organisatsiooni haldus** \> **Ressursid** \> **Ressursid** \> valige ressursi vahekaart \> **Ressurss** \> **Täiskoormus** nupp).  

>[!NOTE]
>Valik, mis puudutab koondplaani kasutamist moodulis **Varade haldus** ja seotud vorm, mida kasutatakse võimsuse reserveerimiste või täiskoormuse ülevaate saamiseks, on standardseadistus. Olenevalt seadistusest väljal **Koondplaan**, on teil võimalik pääseda võimsuse teabele juurde nii valikus **Võimsuse reserveerimine** kui ka **Täiskoormus** moodulis **Organisatsiooni haldus**. Seadistust ei saa luua, kui mõlemas vaates kuvatakse võimsuse reserveerimised.  

Järgmises loendis kirjeldatud väljad on seotud arvutatud hinnanguskooridega, mida kasutatakse töökäsu prioriteedi arvutamiseks töökäsu planeerimisel.

- **Prioriteet** – hinnanguskoor, mis arvutatakse koos hinnanguuskooriga väljadel **Kriitilisus** ja **Alguskuupäev**. Number sellel väljal on jagatud numbriga töökäsu väljal **Prioriteet**. Näiteks kui sellele väljale on sisestatud väärtus „5,00” ja töökäsul on prioriteet „20”, siis on prioriteedi hinnanguskoor 0,25.  
- **Kriitilisus** – hinnanguskoor, mis arvutatakse koos hinnanguuskooriga väljadel **Prioriteet** ja **Alguskuupäev**. Number sellel väljal on korrutatud numbriga töökäsu väljal **Kriitilisus**. Näiteks kui sellele väljale on sisestatud väärtus „10,00” ja töökäsul on kriitilisus „5”, siis on kriitilisuse hinnanguskoor 50.  
- **Alguskuupäev** – hinnanguskoor, mis arvutatakse koos hinnanguskoorigas väljadel **Prioriteet** ja **Kriitilisus**. See väli näitab päeva skoori negatiivse väärtusena ja seda võrreldakse töökäsu väljaga **Eeldatav algus**. Näiteks kui sellele väljale sisestatakse väärtus „10,00” ja töökäsu eeldatav alguskuupäev on kolme päeva pärast, on skoori tulemus miinus 30,00. Tulemuste 0,25 ja 50 lisamine eespool kirjeldatud väljade **Prioriteet** ja **Kriitilisus** näidetest annab kokku pluss 20,25. Seda numbrit võrreldakse töökäsu planeerimisel kõigi teiste töökäskude reitinguskooridega ja seejärel planeeritakse suurimad reitinguskoorid esimesena.  
- **Vastutav töötaja** – hinnanguskoor, mis on arvutatud koos valikute **Vastutavate töötajate grupp**, **Eelistatud töötaja**, **Eelistatud töötajate grupp**, **Varade asukoht** ja **Alguskuupäev** hinnanguskoori väärtustega. Kui sellele väljale on sisestatud väärtus "50,00" ja töökäsul on valitud vastutav töötaja, saab töötaja töökäsu planeerimisel töötaja koguarvutuses 50 punkti.  
- **Vastutavate töötajate grupp** – hinnanguskoor, mis on arvutatud koos valikute **Vastutava töötaja**, **Eelistatud töötaja**, **Eelistatud töötajate grupp**, **Varade asukoht** ja **Alguskuupäev** hinnanguskoori väärtustega. Kui sellele väljale on sisestatud väärtus "50,00" ja töökäsul on valitud vastutav töötaja, saab töötaja töökäsu planeerimisel töötaja koguarvutuses 50 punkti.  
- **Piira vastutava töötajaga** – see piirab töökäsu ajastamiseks töötajate arvu. Valige väärtus **Ei**, kui soovite arvutada kõigi töötajate skoori, olenemata sellest, kas need on seadistatud vastutavate töötajatena või vastutavate töötajate grupi osana. Valige väärtus **Jah**, kui soovite arvutada töökäsul vastutava töötajana seadistatud töötajate skoori ja/või kes on kaasatud töökäsul valitud vastutavate töötajate gruppi.  
- **Eelistatud töötaja** – hinnanguskoor, mis on arvutatud koos valikute **Vastutav töötaja**, **Eelistatud töötaja**, **Eelistatud töötajate grupp**, **Varade asukoht** ja **Alguskuupäev** hinnanguskoori väärtustega. Neli reitinguskoori arvutatakse ja liidetakse, et anda skoor, mille alusel valitakse, milline töötaja tuleks töökäsu planeerimisel valida millise töökäsu jaoks. Kui sellele väljale on sisestatud väärtus „10,00” ja töökäsul on töötaja valitud eelistatud töötajaks, saab see töötaja töökäsu planeerimisel töötaja koguarvutuses 10 punkti.  
- **Eelistatud töötajate grupp** – hinnanguskoor, mis on arvutatud koos valikute **Vastutav töötaja**, **Eelistatud töötaja**, **Eelistatud töötajate grupp**, **Varade asukoht** ja **Alguskuupäev** hinnanguskoori väärtustega. Kui sellele väljale on sisestatud väärtus „10,00” ja töökäsul on töötaja määratud eelistatud töötajate gruppi, saab see töötaja töökäsu planeerimisel töötaja koguarvutuses 10 punkti.  
- **Piira eelistaud töötajaga** – see piirab töökäsu ajastamiseks töötajate arvu. Valige väärtus **Ei**, kui soovite arvutada kõigi töötajate skoori, olenemata sellest, kas need on seadistatud eelistatud töötajatena või eelistatud töötajate grupi osana. Valige väärtus **Jah**, kui soovite arvutada ainult nende töötajate skoori, kes on seadistatud eelistatud töötajatena ja/või on kaasatud eelistatud töötajate gruppi.  
- **Asukoht** – hinnanguskoor, mis on arvutatud koos valikute **Vastutav töötaja**, **Eelistatud töötaja**, **Eelistatud töötajate grupp**, **Varade asukoht** ja **Alguskuupäev** hinnanguskoori väärtustega. Kui sellele väljale sisestatakse väärtus "3000,00", saab töötaja arvutuse punktid 3000, kui töötaja asub samas tehases või rajatises kui vara, millel tööd planeeritakse.  
  - Kui teie ettevõte kasutab töö asukohti, saavad töötajad täispunktid, kui need asuvad varaga seotud töö asukohas. Kui vara töö asukoht on emaettevõtte vara, saavad töötajad selles töö asukohas 1/2 skoori. Kui sellel asukohal on ka emaettevõte, saavad töötajad selles asukohas 1/3 skoori. Kui sellel asukohal on ka emaettevõte, saavad töötajad selles asukohas 1/4 skoori jne.  
  - Kui teie ettevõte kasutab vara asukohta, mida me ei soovita, kasutatakse asukoha skoori arvutamiseks asukohta, ala ja tsooni. Töötajad saavad täiskoori, kui nad asuvad varaga seotud asukohas, alal ja tsoonis. Kui töötaja asukoht vastab ainult asukohale ja alale, on töötaja reitinguskoor 2/3 täisskoorist. Kui töötaja asukoht vastab ainult asukohale, on töötaja reitinguskoor 1/3 täisskoorist.  
- **Piira eelistaud asukohaga** – see piirab töökäsu ajastamiseks töötajate arvu. Valige **Ei**, kui soovite arvutada kõigi töötajate skoori kõigis töö asukohtades. Valige **Jah**, kui soovite arvutada ainult töökäsu töö asukohaga seotud töötajate skoori.

>[!NOTE]
>Töökäskude planeerimise kiirendamiseks on kasutusele võetud kolm välja „Piirang:", piirates töötajatele arvutatud skooride arvu.

**Töötaja töösuhte alguskuupäev** – hinnanguskoor, mis on arvutatud koos valikute **Vastutav töötaja**, **Eelistatud töötaja**, **Eelistatud töötajate grupp**, **Varade asukoht** ja **Alguskuupäev** hinnanguskoori väärtustega. See väli näitab päeva skoori negatiivse väärtusena ja seda võrreldakse töökäsu väljaga **Eeldatav algus**. Näide: kui sellele väljale sisestatakse väärtus "10,00" ja töökäsu eeldatav alguskuupäev on homme, on reitingu tulemus miinus 10,00.

  - Eeldades, et ükski vastutav töötaja ja vastutav töötajate grupp pole planeeritava töökäsu jaoks valitud, peate lisama ja lahutama reitinguskoori väärtused näidete eespool toodud väljadel **Eelistatud töötaja**, **Eelistatud töötajate grupp**, **Varade asukoht** ja **Alguskuupäev** saate koguväärtuseks 3010,00. See tähendab, et töötaja, kes on juba valitud nii eelistatud töötajaks kui ka kaasatud töökäsu eelistatud töötajate gruppi on saanud suure skoori ja töötaja asub ka samas rajatises kui vara, mille jaoks tuleb töö planeerida. See tähendab, et on hea võimalus, et kõnealune töötaja valitakse töökäsu planeerimisel töö täitmiseks.  
  - Kui eespool toodud kaheksast väljast ühele sisestatakse väärtus „0,00”, siis seda reitinguskoori ei arvestata töökäsu planeerimisel.  

## <a name="the-document-types-tab"></a>Vahekaart Dokumendi tüübid

Saate valida dokumentide tüübid, mis peaksid olema saadaval töökäsu aruandega seotud manuste printimiseks. Selleks valige jaotises **Saadaolevad** dokumendi tüüpi ja valige ![edasi nool.](media/15-setup-for-objects.png). Kui soovite valitud dokumenditüübi eemaldada, valige dokumenditüüp jaotises **Valitud** ja valige ![tagasinool](media/16-setup-for-objects.png) nuppu.

## <a name="the-number-sequences-tab"></a>Vahekaart Numbriseeriad

Valige selles jaotises nõutavad numbriseeriad. Varade jaoks on kaks numbriseeriat: üks käsitsi loodud varadele ja üks ootel varade kaudu loodud varadele.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]