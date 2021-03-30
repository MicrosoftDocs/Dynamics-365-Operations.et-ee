---
title: Toote üksikasjade lehe ülevaade
description: See teema annab ülevaate toote üksikasjade lehtedest (PDP-dest) rakenduses Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 020c2a72515eb112adb33c6b58e3a5084339d040
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243825"
---
# <a name="product-details-pages-overview"></a>Toote üksikasjade lehe ülevaade

[!include [banner](includes/banner.md)]

See teema annab ülevaate toote üksikasjade lehtedest (PDP-dest) rakenduses Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Ülevaade

PDP annab toote kohta üksikasjalikku teavet ja laseb klientidel valida toote suvandid, nagu suurus, stiil ja värv. PDP peaks esitlema kogu toote teavet, mis on kliendile vajalik ostuotsuse tegemiseks.

Järgmisel joonisel on toodud PDP näide.

![Toote üksikasjade lehe näide](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a>Päise ja jaluse moodulid

PDP ülaosas on päis, mis näitab kõiki tootekategooriaid ja teisi lehekülgi, mida jaemüüja soovib klientidele sirvimiseks pakkuda. Lehe allosas on jalus, mis sisaldab kiireid linke erinevatele teemadele, mis võivad klientidele huvi pakkuda.

## <a name="buy-box-module"></a>Ostukasti moodul

PDP kõige olulisem moodul on ostukasti moodul, mis kuvatakse lehe põhijaotises esimese üksusena. Ostukasti moodul kuvab olulise tooteteabe, nagu tootenimetus, toote kirjeldus, toote hind, toote pildid ja toote hinnangud.

Ostukasti moodul võimaldab kliendil valida toote suvandid (nt suurus, stiil ja värv) ja lisada toote ostukorvi. Samuti võimaldab see kliendil toote veebis osta ja sellele kauplusesse järele minna. Veebis ostes ja kauplusesse järele minemise moodul kasutab integratsiooni Bing Mapsi rakenduse programmeerimise liidestega (API-dega), et leida lähedalasuvaid kauplusi või kauplusi teises kliendi määratud asukohas.

Ostukasti moodul nõuab toote ID-d. See ID tuletatakse lehekülje kontekstist. Kui ostukasti moodul lisatakse lehele, kus lehekülje kontekst ei sisalda toote ID-d, ei renderda see teavet õigesti.

## <a name="product-specifications-module"></a>Toote spetsifikatsioonide moodul

Toote spetsifikatsioonide moodulit saab kasutada toote kohta lisateabe esitamiseks. Need üksikasjad võetakse toote atribuutidest rakenduses Commerce. Toote spetsifikatsioonide moodul näitab iga atribuuti, mille **nähtavuse** väärtuseks on seatud **tõene**. See nõuab toote ID-d toote atribuutide toomiseks.

## <a name="recommendations-module"></a>Soovituste moodul

Soovituste moodul on oluline moodul PDP-s. Kui kliendid sirvivad tooteid, tuleb neile esitada rohkem toote võimalusi, et nad saaksid leida õige toote ja teha ostu. Soovitused aitavad klientidel lihtsalt avastada seotud sisu ja jätkata ostlemist.

Saadaval on eri tüüpi soovituste loendid.

- Loend **Inimestele meeldib ka** põhineb masina õppimisel. See kasutab soovituste esitamiseks teiste klientide kannete ajalugu. Selle loendi loob soovituste teenus ja see meenutab loendeid "kliendid, kes ostsid selle, ostsid ka...". Selle loendi loomiseks on vaja toote ID-d.
- Loendit **Seotud** saab konfigureerida toote jaoks rakenduses Commerce. Näiteks pruuni nahast reisikoti puhul saab seotud loendi jaoks konfigureerida rohkem käekotte, mis on nahast või mõeldud reisimiseks. Muud tüüpi seostuvaid loendeid, nagu **Aksessuaarid** ja **Rohkem selliseid**, saab konfigureerida samuti rakenduses Commerce. Selle loendi loomiseks on vaja toote ID-d. Seega, kui see on lisatud avalehele, kus lehekülje kontekst ei sisalda toote ID-d, on loend tühi.
- Algoritmiliselt loodud soovituste loendeid, nagu **Populaarsed**, **Enim müüdud** ja **Uus**, saab kasutada PDP-s. Kuigi need loendid ei pruugi olla otse seotud tootega PDP-s, on teisi viise, kuidas aidata klientidel leida tooteid, mis võivad neid huvitada. Seda tüüpi loendid ei nõua toote ID-d. Need on üldised loendid, mis luuakse saidil olevate ostude põhjal.
- Redaktori loendid on käsitsi kureeritud loendid. Näiteks võib jaemüüja otsustada käsitsi kureerida loendi toodetest, mida ta soovib näidata.

## <a name="ratings-and-reviews-modules"></a>Hinnangute ja arvustuste moodulid

Arvustuste kuvamiseks ja lisamiseks saab kasutada kolme moodulit.

- **Arvustused** – see moodul loetleb teiste klientide esitatud hinnangud ja arvustused. Kliendid saavad arvustusi sortida ja filtreerida. See moodul võimaldab klientidel lisaks näidata, kas arvustus meeldib neile või ei meeldi, ja teavitada probleemidest.
- **Arvustuse kirjutamine** – see moodul võimaldab kliendil kirjutada oma tootearvustusi.
- **Hinnangute histogramm** – see moodul sisaldab histogrammi, mis näitab toote hinnangute suundumust.

Lisateavet leiate jaotisest [Hinnangute ja arvustuste ülevaade](ratings-reviews-overview.md).

## <a name="marketing-modules"></a>Turundusmoodulid

Kui turunduse sisu on konkreetse toote puhul unikaalne, saab mis tahes turunduse moodulit lisada PDP-sse. Saate lisada turunduse moodulid PDP-sse lehekülge "rikastades". Lisateavet vt teemast [Tootelehe rikastamine](enrich-product-page.md).

## <a name="additional-resources"></a>Lisaressursid

[Avalehe ülevaade](quick-tour-home-page.md)

[Ostukorvi ja väljaregistreerimise ülevaade](quick-tour-cart-checkout.md)

[Kontohalduse lehtede ülevaade](quick-tour-account-management.md)

[Toote üksikasjade lehe rikastamine](enrich-product-page.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]