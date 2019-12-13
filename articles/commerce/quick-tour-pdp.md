---
title: Toote üksikasjade lehtede ülevaade
description: See teema annab ülevaate toote üksikasjade lehtedest (PDP-dest) rakenduses Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3b02d50adbfcda27d590bcb87fd9669d67d4a01c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697861"
---
# <a name="overview-of-product-details-pages"></a>Toote üksikasjade lehtede ülevaade

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

See teema annab ülevaate toote üksikasjade lehtedest (PDP-dest) rakenduses Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Ülevaade

PDP annab toote kohta üksikasjalikku teavet ja laseb klientidel valida toote suvandid, nagu suurus, stiil ja värv. PDP peaks esitlema kogu toote teavet, mis on kliendile vajalik ostuotsuse tegemiseks.

Järgmisel joonisel on toodud PDP näide.

![Toote üksikasjade lehe näide](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a>Päise ja jaluse moodulid

PDP ülaosas on päis, mis näitab kõiki tootekategooriaid ja teisi lehekülgi, mida jaemüüja soovib klientidele sirvimiseks pakkuda. Lehe allosas on jalus, mis sisaldab kiireid linke erinevatele teemadele, mis võivad klientidele huvi pakkuda.

## <a name="buy-box-module"></a>Ostukasti moodul

Kõige olulisem moodul PDP-s on ostukasti moodul. Seetõttu on see esimene üksus lehe põhijaotises. Ostukasti moodul on konteineri moodul ja see majutab mitu moodulit, mis sisaldavad kõige olulisemat teavet toote kohta. See teave sisaldab toote nime, toote pilte, kirjeldust, hinda ja toote hinnanguid.

Ostukasti moodul võimaldab kliendil valida toote suvandid (nt suurus, stiil ja värv) ja lisada toote ostukorvi. Samuti võimaldab see kliendil toote veebis osta ja sellele kauplusesse järele minna. Veebis ostes ja kauplusesse järele minemise moodul kasutab integratsiooni Bing Mapsi rakenduse programmeerimise liidestega (API-dega), et leida lähedalasuvaid kauplusi või kauplusi teises kliendi määratud asukohas.

Ostukasti moodul nõuab toote ID-d. See ID tuletatakse lehekülje kontekstist. Kui ostukasti moodul lisatakse lehele, kus lehekülje kontekst ei sisalda toote ID-d, ei renderda see teavet õigesti.

## <a name="product-specifications-module"></a>Toote spetsifikatsioonide moodul

Toote spetsifikatsioonide moodulit saab kasutada toote kohta lisateabe esitamiseks. Need üksikasjad võetakse toote atribuutidest rakenduses Dynamics 365 Retail. Toote spetsifikatsioonide moodul näitab iga atribuuti, mille **nähtavuse** väärtuseks on seatud **tõene**. See nõuab toote ID-d toote atribuutide toomiseks.

## <a name="recommendations-module"></a>Soovituste moodul

Soovituste moodul on oluline moodul PDP-s. Kui kliendid sirvivad tooteid, tuleb neile esitada rohkem toote võimalusi, et nad saaksid leida õige toote ja teha ostu. Soovitused aitavad klientidel lihtsalt avastada seotud sisu ja jätkata ostlemist.

Saadaval on eri tüüpi soovituste loendid.

- Loend **Inimestele meeldib ka** põhineb masina õppimisel. See kasutab soovituste esitamiseks teiste klientide kannete ajalugu. Selle loendi loob soovituste teenus ja see meenutab loendeid "kliendid, kes ostsid selle, ostsid ka...". Selle loendi loomiseks on vaja toote ID-d.
- Loendit **Seotud** saab konfigureerida toote jaoks jaemüügis. Näiteks pruuni nahast reisikoti puhul saab seotud loendi jaoks konfigureerida rohkem käekotte, mis on nahast või mõeldud reisimiseks. Muud tüüpi seostuvaid loendeid, nagu **Aksessuaarid** ja **Rohkem selliseid** saab konfigureerida ka jaemüügis. Selle loendi loomiseks on vaja toote ID-d. Seega, kui see on lisatud avalehele, kus lehekülje kontekst ei sisalda toote ID-d, on loend tühi.
- Algoritmiliselt loodud soovituste loendeid, nagu **Populaarsed**, **Enim müüdud** ja **Uus**, saab kasutada PDP-s. Kuigi need loendid ei pruugi olla otse seotud tootega PDP-s, on teisi viise, kuidas aidata klientidel leida tooteid, mis võivad neid huvitada. Seda tüüpi loendid ei nõua toote ID-d. Need on üldised loendid, mis luuakse saidil olevate ostude põhjal.
- Redaktori loendid on käsitsi kureeritud loendid. Näiteks võib jaemüüja otsustada käsitsi kureerida loendi toodetest, mida ta soovib näidata.

## <a name="ratings-and-reviews-module"></a>Hinnangute ja arvustuste moodul

Hinnangute ja arvustuste moodulis kuvatakse teiste klientide esitatud hinnangud ja arvustused. Samuti võimaldab see kliendil kirjutada toote kohta oma arvustuse. Lisaks sisaldab see histogrammi, mis näitab toote hinnangute trendi. Lisateavet leiate jaotisest [Hinnangute ja arvustuste ülevaade](ratings-reviews-overview.md).

## <a name="marketing-modules"></a>Turundusmoodulid

Kui turunduse sisu on konkreetse toote puhul unikaalne, saab mis tahes turunduse moodulit lisada PDP-sse. Saate lisada turunduse moodulid PDP-sse lehekülge "rikastades". 

## <a name="additional-resources"></a>Lisaressursid

[Avalehe ülevaade](quick-tour-home-page.md)

[Kategooria vaikesihtlehe ja otsingutulemuste lehe ülevaade](category-search-page-overview.md)

[Ostukorvi ja maksmise lehtede ülevaade](quick-tour-cart-checkout.md)

[Kontohalduse lehtede ülevaade](quick-tour-account-management.md)
