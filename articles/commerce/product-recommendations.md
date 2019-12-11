---
title: Tootesoovituste ülevaade
description: Selles teemas antakse üldist teavet tootesoovituste kohta. Tootesoovitused võimaldavad klientidel kergesti ja kiiresti leida tooteid, mida nad soovivad ja isegi tooteid, mida nad algselt ei kavatsenud osta.
author: Moonma
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: eb369e6d1356ba13a2310d523b671ac57b9642bf
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770042"
---
# <a name="product-recommendations-overview"></a>Tootesoovituste ülevaade

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Rakendust Microsoft Dynamics 365 Commerce saab kasutada tootesoovituste kuvamiseks e-kaubanduse veebisaidil ja kassa (POS) seadmes. Tootesoovitused on kaubad, millest klient võib huvitatud olla. Soovitused põhinevad teiste klientide ostude suundumustel võrgus ja kliendiga näost-näkku suhtlevates kauplustes.

Tootesoovitused võimaldavad klientidel lihtsalt ja kiiresti leida tooteid, mida nad soovivad, kui neil on kogemus, mis neile hästi sobib. Ristmüüki ja ülesmüüki saab kasutada isegi selleks, et aidata klientidel leida täiendavaid tooteid, mida nad algselt ei kavatsenud osta. Kui soovitusi kasutatakse toote avastuse hõlbustamiseks, võivad need luua rohkem konversiooni võimalusi, aidata suurendada müügitulu ja aidata veelgi suurendada kliendi rahulolu ja hoidmist.

Kaubanduses toetavad tootesoovitused suures osas Microsofti soovituste masinõppe tehnoloogiaid.


## <a name="scenarios"></a>Stsenaariumid

Tootesoovitused on saadaval järgmiste stsenaariumide puhul.

- **E-kaubanduse lehe sirvimise või sihtlehe mis tahes kaupluse lehel:** kui kliendid või kaupluse kaastöötajad külastavad kaupluse lehte, võib soovituse mootor soovitada tooteid loendites **Uus**, **Enim müüdud** ja **Populaarsed**.
- **Lehel toote üksikasjad:** kui kliendid või kaupluse kaastöötajad külastavad lehte **Toote üksikasjad**, soovitab soovituse mootor lisakaupu, mida tõenäoliselt ka ostetakse. Need kaubad kuvatakse loendis **Inimestele meeldib ka**.
- **Kande või kassa lehel:** soovituse mootor pakub kaupu, mis põhinevad kogu ostukorvis olevate kaupade loendil. Need kaubad kuvatakse loendis **Sageli koos ostetud**.

## <a name="recommendation-service"></a>Soovitamise teenus

Tootesoovitused kasutavad soovituste masinõppe tehnoloogiaid järgmisel viisil.

- Andmed vormingus, mida soovitusteenus nõuab, ekstraheeritakse kaubanduse operatiivandmebaasist ja saadetakse olemi kauplusesse.
- Soovitusteenus kasutab andmeid soovitusmudelite koolitamiseks järgmiste loendite jaoks: **Inimestele meeldib ka**, **Sageli koos ostetud**, **Uus**, **Enim müüdud** ja **Populaarsed**.

## <a name="additional-resources"></a>Lisaressursid

[Tootesoovituste lubamine](enable-product-recommendations.md)

[Kureeritud tootesoovituste loendite loomine](create-editorial-recommendation-lists.md)

[AI-ML-põhiste tootesoovituse tulemuste haldamine](modify-product-recommendation-results.md)

[Tootesoovituste loendite lisamine lehtedele](add-reco-list-to-page.md)
