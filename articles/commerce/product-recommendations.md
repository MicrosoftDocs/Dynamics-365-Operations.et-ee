---
title: Tootesoovituste ülevaade
description: Selles teemas antakse üldist teavet tootesoovituste kohta. Tootesoovitused võimaldavad klientidel kergesti ja kiiresti leida tooteid, mida nad soovivad ja isegi tooteid, mida nad algselt ei kavatsenud osta.
author: Moonma
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 044a5c21e4ebf1bf83edc74335e655b9388bc1d4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795593"
---
# <a name="product-recommendations-overview"></a>Tootesoovituste ülevaade

[!include [banner](includes/banner.md)]

Rakendust Microsoft Dynamics 365 Commerce saab kasutada tootesoovituste kuvamiseks e-kaubanduse veebisaidil ja kassa (POS) seadmes. Tootesoovitused on kaubad, millest klient võib huvitatud olla. Soovitused põhinevad teiste klientide ostude suundumustel võrgus ja kliendiga näost-näkku suhtlevates kauplustes.

Tootesoovitused võimaldavad klientidel lihtsalt ja kiiresti leida tooteid, mida nad soovivad, kui neil on kogemus, mis neile hästi sobib. Ristmüüki ja ülesmüüki saab kasutada isegi selleks, et suunata kliente leidma täiendavaid tooteid, mida nad algselt ei kavatsenud osta. Kui soovitusi kasutatakse toote avastuse täiustamiseks, võivad need luua rohkem konversiooni võimalusi, aidata suurendada müügitulu ja aidata veelgi suurendada kliendi rahulolu ja hoidmist.

E-kaubanduses toetavad tootesoovitused suures osas Microsofti soovituste masinõppe tehnoloogiaid.

## <a name="recommendation-service"></a>Soovitamise teenus

Tootesoovituste teenus kasutab tehisintellekti ja masinõppe (AI-ML) tehnoloogiaid järgmisel viisil.

- Andmed vormingus, mida soovitusteenus nõuab, ekstraheeritakse kaubanduse operatiivandmebaasist ja saadetakse Azure Data Lake Storage'isse või olemi kauplusesse.
- Soovitusteenus kasutab talletatud andmeid soovitusmudelite koolitamiseks järgmiste loendite jaoks: **Inimestele meeldib ka**, **Sageli koos ostetud**, **Uus**, **Enim müüdud** ja **Populaarsed**.

## <a name="scenarios"></a>Stsenaariumid

Tootesoovitused on saadaval järgmiste stsenaariumide puhul.

- **E-kaubanduse lehe sirvimise või sihtlehe mis tahes kaupluse lehel:** kui kliendid või kaupluse kaastöötajad külastavad kaupluse lehte, võib soovituse mootor soovitada tooteid loendites **Uus**, **Enim müüdud** ja **Populaarsed**.
- **Lehel toote üksikasjad:** kui kliendid või kaupluse kaastöötajad külastavad lehte **Toote üksikasjad**, soovitab soovituse mootor lisakaupu, mida tõenäoliselt ka ostetakse. Need kaubad kuvatakse loendis **Inimestele meeldib ka**.
- **Kande või kassa lehel:** soovituse mootor pakub kaupu, mis põhinevad kogu ostukorvis olevate kaupade loendil. Need kaubad kuvatakse loendis **Sageli koos ostetud**.
- **Isikupärastatud soovitused** : turustajad võivad pakkuda sisselogitud klientidele isikupärastatud loendeid **Teile valitud** koos uue funktsiooniga, mis võimaldab olemasolevaid loendi stsenaariumeid vastavalt sellele kliendile isikupärastada. Lisateabe saamiseks vt [Isikupärastatud soovituste lubamine.](personalized-recommendations.md).

### <a name="types-of-product-recommendations"></a>Tootesoovituste tüübid

Järgmine tabel kirjeldab erinevaid automatiseeritud tootesoovituste tüüpe, mis on saadaval jaemüüjatele lahenduses Dynamics 365 Commerce rakendamiseks [tootekogumi mooduli kaudu](product-collection-module-overview.md). Jaemüüjad saavad kuvada ka sisselogitud kasutajale isikupärastatud tulemusi, kui saidi autor valib selle suvandi.

| Tootekogumi moodul  | Tüüp | Kirjeldus |
|----------------------------|------|-------------|
| New                        | Algoritmiline | See moodul kuvab uusimate toodete loendi, mis on kanalitele ja kataloogidele hiljuti valitud. |
| Enim müüdud               | Algoritmiline | See moodul kuvab toodete loendi, mis on järjestatud kõige suurema müügi arvu alusel. |
| Populaarsed                   | Algoritmiline | See moodul näitab kõige kõrgema jõudlusega toodete loendit valitud perioodil, mis on järjestatud suurima müüginumbri järgi.  |
| Kliendid ostavad sageli koos | AI-ML | See moodul soovitab toodete loendit, mida tavaliselt ostetakse koos tarbija praeguse ostukorvi sisuga. |
| Inimestele meeldib ka           | AI-ML | See moodul soovitab tooteid lähteväärtuse toote põhjal, tuginedes tarbija ostuharjumustele. |
| Valib teile              | AI-ML | See moodul soovitab isikupärastatud toodete loendit sisselogitud kasutaja ostuharjumuste põhjal. Külalisekasutaja jaoks on see loend ahendatud. |

## <a name="additional-resources"></a>Lisaressursid

[ Azure Data Lake Storage'i lubamine Dynamics 365 Commerce'i keskkonnas](enable-adls-environment.md)

[Luba tootesoovitused](enable-product-recommendations.md)

[Isikupärastatud soovituste lubamine](personalized-recommendations.md)

[Isikupärastatud tootesoovitustest loobumine](personalization-gdpr.md)

[„Sarnaste toodete vaatamise” soovituste lubamine](shop-similar-looks.md)

[Tootesoovituste lisamine kassas](product.md)

[Soovituste lisamine kandeekraanile](add-recommendations-control-pos-screen.md)

[AI-ML-i soovituste tulemuste kohandamine](modify-product-recommendation-results.md)

[Loo kuraatorite soovitused käsitsi](create-editorial-recommendation-lists.md)

[Soovituste loomine demoandmetega](product-recommendations-demo-data.md)

[Tootesoovituste KKK](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]