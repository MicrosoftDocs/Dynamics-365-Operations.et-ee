---
title: Rakenduse Asset Management parameetrid
description: Rakenduses Asset Management tuleb seadistada varade, töökäskude ja töökäsu planeerimisega seotud parameetrid.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3336a3357578b25522e1ac457a48349f88b7318d
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024564"
---
# <a name="asset-management-parameters"></a>Rakenduse Asset Management parameetrid

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Rakenduses Asset Management tuleb seadistada varade, töökäskude ja töökäsu planeerimisega seotud parameetrid. Selles teemas kirjeldatakse nende seadistamist. Vormi avamiseks valige **asset management** > **Seadistus** > **Rakenduse Asset Management parameetrid**.

Nuppu **Loo andmeviisard** saab kasutada ettevõtte test- või demoandmete eesmärgil seadistusandmete automaatseks loomiseks rakenduses Dynamics 365 Supply Chain Management. Viisardi kasutamise kohta teabe saamiseks lugege tehnilist ülevaadet „Testiandmete seadistamine rakenduses Asset Management”.

Link **Varad**

- **Töö vaikeasukoht** on standardne töö asukoht, mis uute varade loomisel valitakse varades automaatselt.  
- Valige väljal **Standardne kalender** kalender, mida kasutatakse varade KPI-de arvutamiseks juhul, kui varas pole ressurssi valitud.  
- Valige väljal **Vaade** standardne vaade, mis kuvatakse, kui avate vormi **Varade vaade** (**Varahaldus** > **Ühine** > **Varad** > **Varade vaade**).
- **Taotluse vaiketüüp** on standardne hooldusnõude tüüp, mis valitakse automaatselt uue taotluse loomisel.  
- Kui soovite luua varadega seotud projekte, luuakse valikus **Rakenduse Asset Management parameetrid** valikuid **Põhiprojekt**, **Projektihierarhia** ja suvandit **Projektide automaatne loomine** puudutavad projektiseosed.  
- Väljal **Töökäsu projekti mask** saate määratleda töötellimuste ja alamvarade jaoks lubatud alamprojektide arvu. Töökäsu maski kasutatakse selleks, et määratleda, kui palju töötellimusi saab põhivarale luua ja seotud töökäskude töö projektis kasutada. Töökäsu mask seadistataks väljal **Seotud töökäsu mask** valikus **Rakenduse Asset Management parameetrid** (**Asset Management** > **Seadistus** > **Rakenduse Asset Management parameetrid** > **Töökäsud**).  
>[!NOTE]
>Seostuva töökäsu maski vorming on räsimärkide (#) arv olenevalt teie loodavate töökäskude maksimumarvust. Näide: # # võimaldab teil luua kuni 99 alamprojektid.  
- Töötüüpide eelarved talletatakse väljal **Eelarveprojekt** valitud projektis. Iga töötüübi puhul luuakse eelarveprojektis automaatselt uus tegevus. Töötüübi eelarved salvestatakse seejärel eelarveprojektis.  
- Valige väljal **Mudel** töötüübi ja töökäsu eelarvetes kasutatav eelarvemudel.  


Link **Töökäsud**

- **Töökäsu vaiketüüp** määratleb standardsätted töökäsu loomisel.  
- **Ennetava töökäsu tüüp** määratleb töökäsu tüübi, mida kasutatakse töökäskude loomisel hoolduskavadest. Kui see väli jäetakse tühjaks, kasutatakse välja **Töökäsu vaiketüüp** töökäsu tüüpi.  
- Väljal **Seotud töökäsu mask** saate määratleda töökäskude maksimumarvu, mida saa töökäsuga siduda. Näide: Näide: # # võimaldab teil kuni 99 töökäsku siduda. Kui määratlete siin kirjeldatud maski, nummerdatakse seotud töökäsud [töökäsuga seotud töökäsu töökäsu ID]-01,-02,-03 jne. Kui te sellel väljal maski ei määratle, saab seostuv töökäsk järgmise järjestikuste töökäsu ID.  
- Tehke tumblernupul **Kopeeri vead** valik „Jah”, kui soovite automaatselt kopeerida töökäskudes registreeritud vead seotud hooldusnõuetesse.  
- Väljal **Tase** saate määratleda töö asukoha taseme, mis sisestatakse automaatselt töökäsku, kui kõik seotud töökäsu tööd viitavad samale töö asukohale. Kui kõik töökäsu tööd pole määratletud tasemel seotud sama töö asukohaga, jäetakse väli **Töö asukoht** töökäsul tühjaks. Näide: kui sisestate sellele väljale numbri „1”, on see töö asukoha struktuuris ülemine tase. Kui sisestate sellele väljale numbri „0”, ei ole te määratlenud kindlat töö asukoha taset, vaid töökäsu kõik töökäsu tööd peavad olema seotud töökäsule lisatava töö asukoha sama töö asukoht.  
- Töökäsule tarbimise sisestamisel kasutatavaid töölehti saab valida kiirkaardi **Üldine** väljadel **Tund**, **Üksus** ja **Kulu**.  
- Väljal **Tootekeele allikas** valige, millist keelt kasutada varahalduse aruannetes olevate toodete nimede puhul. Saate valida ettevõtte kontol seadistatud keele, või praegu rakendusse sisse logitud kasutaja jaoks seadistatud keele.  
- Kui soovite automaatselt värskendada töö tüübi vaikeväärtuste, hoolduskavade ja hoolduskordade muudatusi, tehke tumblernupul **Reaalajas uuendus** valik „Jah”.
> - Kui valite väärtuse „Ei”, ei uuendata töötüüpide vaikeväärtusi, hoolduskavu ja hoolduskordi moodulis Asset Management automaatselt.  
> - Kui teil on sünkroonitud suur hulk andmeid, nt mitu vara või töö asukohta, mis on seadistatud hoolduskavades või hoolduskordades või suur hulk hoolduskavasid või -kordi, valige tumblernupul väärtus „Ei”.  
> - Kui teete muudatusi töötüübi vaikeväärtustes või hoolduskavades või hoolduskordades ja olete reaalajas uuendamise jaoks valinud „Ei”, ei pruugita hoiatust kuvada, kui muudatused mõjutavad järgmist:
>   - hoolduskavades või -kordades seadistatud töö asukohad;  
>   - hoolduskavades või -kordades seadistatud objektid;  
>   - hoolduskavade seadistus  
>   - hoolduskordade seadistus.  
- Kiirkaardil **Kategooria** saab määratleda töökäskude kasutamisega seotud vaikekategooriaid.  


Link **Töökäsu planeerimine**

- **Graafiku ajapiir** määratleb perioodi päevades, mis arvutatakse töökäsu eeldatavast alguskuupäevast, mille jooksul töökäsu töid planeeritakse.  
- **Koondplaan** on seotud mooduli **Organisatsiooni haldus** ressurssidega. Kui valite sellel väljal koondplaani, saate vaadata töökäskudega seotud võimsuse reserveerimisi valikus **Võimsuse reserveerimised** (**Organisatsiooni haldus** > **Ressursid** > **Ressursid** > valige ressurss vahekaardil > **Ressurss** nupp > **Võimsuse reserveerimised**). Kui jätate selle välja tühjaks, saate vaadata töökäskude täiskoormusi valikus **Täiskoormus** (**Organisatsiooni haldus** \> **Ressursid** \> **Ressursid** \> valige ressursi vahekaart  \> **Ressurss** \> **Täiskoormus** nupp).  

>[!NOTE]
>Valik, mis puudutab koondplaani kasutamist või mittekasutamist moodulis **Varade haldus** ja seotud vorm, mida kasutatakse võimsuse reserveerimiste või täiskoormuse ülevaate saamiseks, on standardseadistus. Olenevalt seadistusest väljal **Koondplaan**, on teil võimalik pääseda võimsuse teabele juurde nii valikus **Võimsuse reserveerimine** kui ka **Täiskoormus** moodulis **Organisatsiooni haldus**. Seadistust ei saa luua, kui mõlemas vaates kuvatakse võimsuse reserveerimised.  

Allpool olevas täpploendis kirjeldatud väljad on seotud arvutatud reitinguskooridega, mida kasutatakse töökäsu prioriteedi arvutamiseks töökäsu planeerimisel.

- **Prioriteet** - reitinguskoor, mis arvutatakse koos reitinguskooriga väljadel **Kriitilisus** ja **Alguskuupäev**. Number sellel väljal on jagatud numbriga töökäsu väljal **Prioriteet**. Näide: kui sellele väljale on sisestatud väärtus „5,00” ja töökäsul on prioriteet „20”, siis on prioriteedi reitinguskoor 0,25.  
- **Kriitilisus** - reitinguskoor, mis arvutatakse koos reitinguskooriga väljadel **Prioriteet** ja **Alguskuupäev**. Number sellel väljal on korrutatud numbriga töökäsu väljal **Kriitilisus**. Näide: kui sellele väljale on sisestatud väärtus „10,00” ja töökäsul on kriitilisus „5”, siis on kriitilisuse reitinguskoor 50.  
- **Alguskuupäev** - reitinguskoor, mis arvutatakse koos reitinguskooriga väljadel **Prioriteet** ja **Kriitilisus**. See väli näitab päeva skoori negatiivse väärtusena ja seda võrreldakse töökäsu väljaga **Eeldatav algus**. Näide: kui sellele väljale sisestatakse väärtus "10,00" ja töökäsu eeldatav alguskuupäev on kolme päeva pärast, on reitingu tulemus miinus 30,00. Tulemuste 0,25 ja 50 lisamine eespool kirjeldatud väljade **Prioriteet** ja **Kriitilisus** näidetest annab kokku pluss 20,25. Seda numbrit võrreldakse töökäsu planeerimisel kõigi teiste töökäskude reitinguskooridega ja seejärel planeeritakse suurimad reitinguskoorid esimesena.  
- **Vastutav töötaja** - reitinguskoor, mis on arvutatud koos valikute **Vastutavate töötajate grupp**, **Eelistatud töötaja**, **Eelistatud töötajate grupp**, **Varade asukoht** ja **Alguskuupäev** reitinguskoori väärtustega. Kui sellele väljale on sisestatud väärtus "50,00" ja töökäsul on valitud vastutav töötaja, saab töötaja töökäsu planeerimisel töötaja koguarvutuses 50 punkti.  
- **Vastutavate töötajate grupp** - reitinguskoor, mis on arvutatud koos valikute **Vastutav töötaja**, **Eelistatud töötaja**, **Eelistatud töötajate grupp**, **Varade asukoht** ja **Alguskuupäev** reitinguskoori väärtustega. Kui sellele väljale on sisestatud väärtus "50,00" ja töökäsul on valitud vastutav töötaja, saab töötaja töökäsu planeerimisel töötaja koguarvutuses 50 punkti.  
- Valiku **Piira vastutava töötajaga** tumblernupp Jah/Ei piirab töökäsu planeerimiseks saadaolevate töötajate arvu. Valige väärtus „Ei”, kui soovite arvutada kõigi töötajate skoori, olenemata sellest, et need on seadistatud vastutavate töötajatena või vastutavate töötajate grupi osana. Valige väärtus „Jah”, kui soovite arvutada töökäsul vastutava töötajana seadistatud töötajate skoori ja/või kes on kaasatud töökäsul valitud vastutavate töötajate gruppi.  
- **Eelistatud töötaja** - reitinguskoor, mis on arvutatud koos valikute **Vastutav töötaja**, **Eelistatud töötaja**, **Eelistatud töötajate grupp**, **Varade asukoht** ja **Alguskuupäev** reitinguskoori väärtustega. Neli reitinguskoori arvutatakse ja liidetakse, et anda skoor, mille alusel valitakse, milline töötaja tuleks töökäsu planeerimisel valida millise töökäsu jaoks. Kui sellele väljale on sisestatud väärtus „10,00” ja töökäsul on töötaja valitud eelistatud töötajaks, saab see töötaja töökäsu planeerimisel töötaja koguarvutuses 10 punkti.  
- **Eelistatud töötajate grupp** - reitinguskoor, mis on arvutatud koos valikute **Vastutav töötaja**, **Eelistatud töötaja**, **Eelistatud töötajate grupp**, **Varade asukoht** ja **Alguskuupäev** reitinguskoori väärtustega. Kui sellele väljale on sisestatud väärtus „10,00” ja töökäsul on töötaja määratud eelistatud töötajate gruppi, saab see töötaja töökäsu planeerimisel töötaja koguarvutuses 10 punkti.  
- Valiku **Piira eelistaud töötajaga** tumblernupp Jah/Ei piirab töökäsu planeerimiseks saadaolevate töötajate arvu. Valige väärtus „Ei”, kui soovite arvutada kõigi töötajate skoori, olenemata sellest, kas need on või ei ole seadistatud eelistatud töötajatena või eelistatud töötajate grupi osana. Valige väärtus „Jah”, kui soovite arvutada ainult nende töötajate skoori, kes on seadistatud eelistatud töötajatena ja/või on kaasatud eelistatud töötajate gruppi.  
- **Asukoht** - reitinguskoor, mis on arvutatud koos valikute **Vastutav töötaja**, **Eelistatud töötaja**, **Eelistatud töötajate grupp**, **Varade asukoht** ja **Alguskuupäev** reitinguskoori väärtustega. Kui sellele väljale sisestatakse väärtus "3000,00", saab töötaja arvutuse punktid 3000, kui töötaja asub samas tehases või rajatises kui vara, millel tööd planeeritakse.  

  - Kui teie ettevõte kasutab töö asukohti, saavad töötajad täispunktid, kui need asuvad varaga seotud töö asukohas. Kui vara töö asukoht on emaettevõtte vara, saavad töötajad selles töö asukohas 1/2 skoori. Kui sellel asukohal on ka emaettevõte, saavad töötajad selles asukohas 1/3 skoori. Kui sellel asukohal on ka emaettevõte, saavad töötajad selles asukohas 1/4 skoori jne.  
  - Kui teie ettevõte kasutab vara asukohta, mida me ei soovita, kasutatakse asukoha skoori arvutamiseks asukohta, ala ja tsooni. Töötajad saavad täiskoori, kui nad asuvad varaga seotud asukohas, alal ja tsoonis. Kui töötaja asukoht vastab ainult asukohale ja alale, on töötaja reitinguskoor 2/3 täisskoorist. Kui töötaja asukoht vastab ainult asukohale, on töötaja reitinguskoor 1/3 täisskoorist.  

- Valiku **Piira asukohaga** tumblernupp Jah/Ei piirab töökäsu planeerimiseks saadaolevate töötajate arvu. Valige „Ei”, kui soovite arvutada kõigi töötajate skoori kõigis töö asukohtades. Valige "Jah", kui soovite arvutada ainult töökäsu töö asukohaga seotud töötajate skoori.

>[!NOTE]
>Töökäskude planeerimise kiirendamiseks on kasutusele võetud kolm tumblernuppu „Piirang: ...", piirates töötajatele arvutatud skooride arvu.

**Töötaja töösuhte alguskuupäev** - reitinguskoor, mis on arvutatud koos valikute **Vastutav töötaja**, **Eelistatud töötaja**, **Eelistatud töötajate grupp**, **Varade asukoht** ja **Alguskuupäev** reitinguskoori väärtustega. See väli näitab päeva skoori negatiivse väärtusena ja seda võrreldakse töökäsu väljaga **Eeldatav algus**. Näide: kui sellele väljale sisestatakse väärtus "10,00" ja töökäsu eeldatav alguskuupäev on homme, on reitingu tulemus miinus 10,00.

  - Eeldades, et ükski vastutav töötaja ja vastutav töötajate grupp pole planeeritava töökäsu jaoks valitud, peate lisama ja lahutama reitinguskoori väärtused näidete eespool toodud väljadel **Eelistatud töötaja**, **Eelistatud töötajate grupp**, **Varade asukoht** ja **Alguskuupäev** saate koguväärtuseks 3010,00. See tähendab, et töötaja, kes on juba valitud nii eelistatud töötajaks kui ka kaasatud töökäsu eelistatud töötajate gruppi on saanud suure skoori ja töötaja asub ka samas rajatises kui vara, mille jaoks tuleb töö planeerida. Kõik see tähendab, et on hea võimalus, et kõnealune töökäsu planeerimisel töö täitmiseks.  
  - Kui eespool toodud kaheksast väljast ühele sisestatakse väärtus „0,00”, siis seda reitinguskoori ei arvestata töökäsu planeerimisel.  


Link **Dokumentide tüübid**

Saate valida dokumentide tüübid, mis peaksid olema saadaval töökäsu aruandega seotud manuste printimiseks. Selleks klõpsake jaotises **Saadaolevad** dokumendi tüüpi ja klõpsake ![edasinoolega](media/15-setup-for-objects.png) nuppu. Kui soovite valitud dokumenditüübi eemaldada, valige dokumenditüüp jaotises **Valitud** ja klõpsake  ![tagasinoolega](media/16-setup-for-objects.png) nuppu.



Link **Numbriseeriad**

Valige selles jaotises nõutavad numbriseeriad. Varade jaoks on kaks numbriseeriat: üks käsitsi loodud varadele ja üks ootel varade kaudu loodud varadele.
