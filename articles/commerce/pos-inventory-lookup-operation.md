---
title: Varude otsimine POS-is
description: See artikkel kirjeldab Dynamics 365 Commerce, kuidas kasutada müügikohas varude otsingutoimingut, et vaadata toodete vaba kaubavaru saadavust kaupluste ja ladude lõikes.
author: boycezhu
ms.date: 08/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: fc8c7dad0a7cb66ba7d6c6f527be84cfe74dee52
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288321"
---
# <a name="inventory-lookup-operation-in-pos"></a>Varude otsimine POS-is

[!include [banner](includes/banner.md)]

See artikkel kirjeldab Dynamics 365 Commerce, kuidas kasutada müügikohas varude otsingutoimingut, et vaadata toodete vaba kaubavaru saadavust kaupluste ja ladude lõikes.

Täpne reaalajas ülevaade varudest kogu organisatsioonis aitab kaupluste töötajatel pakkuda kiiret ja tõhusat klienditeenindust. Kõige olulisem hetk on see, mil klient on valmis tegema ostuotsust. On oluline, et jaekaupluse kassapidajatel oleks reaalajas või peaaegu reaalajas varude teave käeulatuses, et nad saaksid pakkuda täpseid toote tarne ja komplekteerimise aegu.

Varude otsingutoiming rakenduses Commerce POS aitab jaemüüjatel saavutada tegevusülevaateid ja saada vihjeid, ühendades kauplused Commerce headquartersiga. See funktsioon tagab kaupluste ja ladude toodete varude saadavaloleku vaate. Samuti aitab see jaemüüjatel suurendada tõhusust ja säästlikkust, tõhustades varude planeerimist reaalajas.

Kui varude otsingutoiming on käivitatud kassa rakendusest, kasutab kassapidaja numbriklaviatuuri tootenumbri sisestamiseks, et teha päringuid oma laoteabe kohta. Kui sisestatud tootel on variante, saab kassapidaja valikuliselt valida dimensioone või muid väärtusi, et kontrollida konkreetse tootevariandi laoteavet.

## <a name="inventory-lookup-list-view-for-individual-products"></a>Üksikute toodete varude otsinguloendi vaade

Üksiku toote puhul annab varude otsingutoiming varude otsinguloendi vaate, mis näitab järgmiste toodete teavet asukohtade loendi kohta:

- **Varud** – viitab toote saadaolevale füüsilisele kogusele.
- **Reserveeritud** – viitab peakontorist toodud füüsiliselt reserveeritud kogusele.
- **Tellitud** – viitab peakontorist toodud „tellitud kokku” kogusele.
- **Ühik** – viitab peakontoris konfigureeritud varude mõõtühikule.

Asukohtade loendi vaade hõlmab kõiki kauplusi ja ladusid, mis on konfigureeritud täitmisgruppides, mille juurde praegune kauplus on lingitud, nagu näha järgmises näitepildis.

![Varude otsingu toimingute loendi vaade.](media/inventory-lookup-list-view.png)

> [!NOTE]
> Veenduge, et teie praegune kauplus on kaasatud seotud täitmisgruppidesse.

POS-i rakenduse ribal on saadaval järgmised toimingud:

- **Sordi** – tegevus võimaldab kassa kasutajal sortida loendivaate andmeid mitmesuguste kriteeriumide alusel. Asukohapõhine sortimine on vaikesortimisvalik.

    - **Geograafiline asukoht** (kõige lähemast asukohast kõige kaugemasse asukohta, aluseks on kaugus praeguse kauplusega)
    - **Nimi** (kasvavas või kahanevas järjestuses)
    - **Kaupluse nimi** (kasvavas või kahanevas järjestuses)
    - **Varud** (kahanevas järjestuses)
    - **Reserveeritud** (kahanevas järjestuses)
    - **Tellitud** (kahanevas järjestuses)

- **Filtreeri** – tegevus võimaldab kassa kasutajal vaadata konkreetse asukoha filtreeritud andmeid.
- **Kuva kaupluse saadavus** – tegevus võimaldab kassa kasutajal vaadata lubamiseks saadaval (ATP) koguseid valitud kaupluses olevale tootele.
- **Kuva kaupluse asukohta** – tegevus avab eraldi lehe, et kuvada valitud kaupluse kaardivaade, aadress ja kauplusetunnid.
- **Kättesaamine poest** – tegevus loob klienditellimuse tootevariandi jaoks, millele tullakse valitud asukohta järele, ja suunab kasutaja kandekuvale.
- **Saada toode** – tegevus loob klienditellimuse tootevariandi jaoks, mis saadetakse valitud poest, ja suunab kasutaja kandekuvale.
- **Kõigi variantide kuvamine** – variantidega toote puhul aktiveerib see tegevus loendivaate asemel maatriksivaate, kus kuvatakse kõigi tootevariantide laoteave.
- **Lisa kandele** – tegevus lisab toote ostukorvi ja suunab kasutaja kandekuvale.

> [!NOTE]
> Asukohapõhine sortimine, mida tutvustati rakenduse Commerce versiooni 10.0.17 väljalaskes, kuvab praeguse kaupluse ülaosas. Teiste asukohtade jaoks määratakse asukoha ja praeguse kaupluse vaheline kaugus Commerce Headquarter’is määratletud koordinaatidega (laius- ja pikkuskraad). Kaupluse asukohateave määratletakse kauplusega seotud tootmisüksuse esmasel aadressil. Mittelao puhul määratletakse asukoha teave lao aadressis. Enne versiooni 10.0.17 kuvab loendivaade alati praeguse kaupluse ülaosas ja sordib teised asukohad tähestikulises järjekorras.
>
> **Kuva kaupluse saadavus**, **Kuva kaupluse asukohta**, **Kauplusesse järeleminemine**, ja **Toote saatmise** toimingud pole kauplusevälistes asukohtades saadaval.

## <a name="inventory-lookup-matrix-view-for-variants"></a>Varude otsingumaatriksi vaade variantide puhul

Variantide abil põhitoote puhul pakub varude otsingutoiming ka dimensioonipõhist maatriksivaadet, mis kuvab varude saadavuse teabe kõigi põhitoote variantide kohta valitud asukohas. Vaikimisi näitab maatriksivaade praeguse poe andmeid. Saate **Kaupluse** toimingu abil otsida varude teavet teistest kauplustest, mis on konfigureeritud täitmisrühmades, millega praegune pood on lingitud.

Järgmine kuva näitab kassas varude otsingumaatriksi vaadet.

![Varude otsingu toimingute maatriksvaade.](media/inventory-lookup-matrix-view.png)

Maatriksivaates esindab iga lahter üksikut varianti ja kuvab vaba kaubavaru (vaba füüsilise) väärtuse parempoolses allnurgas kui **reserveeritud** (füüsiliselt reserveeritud) ja **tellitud** (kogu tellitud) väärtused ülemises vasakus nurgas. Järgmises tabelis selgitatakse erinevate laoseisu väärtusi.

| Laoseisu väärtus                            | Kirjeldus |
|------------------------------------------|-------------|
| Numbriline väärtus, mis on suurem kui 0 (null) | Variant on väljastatud valitud asukoha jaoks ja te saate lahtris teha täiendavaid toiminguid. |
| **0** (null)                             | Variant on väljastatud valitud asukoha jaoks, kuid kaup pole valitud asukohas saadaval. Saate siiski teha lahtris täiendavaid toiminguid. |
| **p/s**, või passiivne lahter              | Varianti pole valitud asukoha jaoks väljastatud ja te ei saa lahtris täiendavaid toiminguid teha. |

Dimensiooniväärtuste kuvamisjärjestus maatriksi vaates põhineb Commerce Headquarters dimensiooni kuvamistellimuse konfiguratsioonil. Saate muuta dimensioonikuva tellimuse konfiguratsiooni, valides kasutamiseks uue dimensiooni. 

Maatriksivaate lahtris on saadaval järgmised toimingud:

- **Müü kohe** – tegevus lisab valitud toote ostukorvi ja suunab kasutaja kandekuvale.
- **Kättesaamine poest** – tegevus loob valitud variandi jaoks klienditellimuse, millele tullakse valitud kauplusesse järele, ja suunab kasutaja kandekuvale.
- **Saada toode** – tegevus loob klienditellimuse valitud tootevariandi jaoks, mis saadetakse valitud poest, ja suunab kasutaja kandekuvale.
- **Saadavus** – tegevus viib kasutaja eraldi lehele, kus kuvatakse valitud kaupluses valitud variandi ATP kogused.
- **Kuva kõik asukohad** – tegevus aktiveerib standardse varude saadavusloendi vaate, kus kuvatakse valitud variandi laoteave.
- **Kuva toote üksikasjad** – tegevus suunab kasutaja valitud variandi toote üksikasjade lehele.

## <a name="access-inventory-lookup-from-other-pages-in-pos"></a>Juurdepääs varude otsingule teistelt müügikoha lehtedelt

Müügikoha kasutajad pääsevad kassas teistelt lehtedelt juurde varude otsingutoimingule.

Järgmine näide näitab POS-i PDP-st varude otsimise tulemusi.

![Otsing varudest toote üksikasjade lehelt.](media/inventory-lookup-from-product-details-page.png)

Põhitoote PDP-s saate kasutada rakenduseribal **Kõikide variantide kuvamise** toimingut, et käivitada varude otsingumaatriksi vaade, mis kuvab toote kõigi variantide varude saadavaloleku teabe praeguses kaupluses. Üksiku toote puhul kuvab PDP selle toote vaba kaubavaru (füüsiliselt saadaoleva) väärtuse praeguses kaupluses. Lisaks saate valida lingi **Muu kaupluste laod**, et käivitada varude otsingutoiming, et kontrollida toote saadavust teistele kauplustele või ladudele.

> [!NOTE]
> Toiming **Kõigi variantide kuvamine** on saadaval ainult kauba tooteetalonide korral, millel on tootevariandid. See pole saadaval eraldiseisvate toodete või komplektide korral.

Saate konfigureerida varude otsingutoimingu nii, et see kuvatakse lingina kassakande ekraanil nupupaneelil. Pärast konfigureerimist, kui kasutaja valib ostukorvi rea ja seejärel valib nupu **Varude otsing** kuvatakse valitud toote varude otsinguloendi vaadet. Lisateavet nupupaneelide konfigureerimise kohta kassa ekraani paigutuse kujundaja tööriista abil vt [kassa kasutajaliidese visuaalsetest konfiguratsioonidest](pos-screen-layouts.md).

## <a name="inventory-lookup-with-channel-side-calculation"></a>Müügikoha varude otsing kanalipoolse arvutusega

Commerce Release 10.0.9 ja varasemas luuakse **füüsiline väärtus** laootsingu toimingus saadav väärtus rakenduses Commerce Headquarters reaalajas teenusekutse kaudu. Rakenduse Commerce release 10.0.10 ja uuemate versioonide puhul saate konfigureerida müügikoha varude otsingutoimingu kasutama äriserveri kanalipoolset arvutust, et määrata saadav füüsiline väärtus, mis võib anda usaldusväärsema ja täpsema hinnangu vaba kaubavaru kohta, andes arvesse kandeandmed, mis ei ole veel peakontoriga sünkroonitud. Lisateavet kanalipoolse varude arvutamise ja seotud kassa konfiguratsiooni kohta peakontoris vt [Varude saadavuse arvutamine jaemüügikanalitele](calculated-inventory-retail-channels.md).

## <a name="additional-resources"></a>Lisaressursid

[Kassa kasutajaliidese visuaalsed konfiguratsioonid](pos-screen-layouts.md)

[Varude saadavuse arvutamine jaemüügikanalite jaoks](calculated-inventory-retail-channels.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
