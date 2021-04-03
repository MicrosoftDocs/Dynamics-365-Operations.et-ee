---
title: AI-ML-põhiste tootesoovituse tulemuste kohandamine
description: Selles teemas selgitatakse, kuidas kohandada tehisintellekti masinõppel (AI-ML) põhinevaid tootesoovituse tulemusi teie ettevõttele.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b9e370faed7feb0640959a9fcc4b608f18f9ffc1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263942"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a>AI-ML-põhiste tootesoovituse tulemuste kohandamine


[!include [banner](includes/banner.md)]

Selles teemas selgitatakse, kuidas kohandada tehisintellekti masinõppel (AI-ML) põhinevaid tootesoovituse tulemusi teie ettevõttele. 

Pärast tootesoovituste lubamist hakkavad kehtima vaikesätted; need parameetrid töötavad, võivad töötada paljude vajaduste jaoks. Parim on planeerida kulutada aega hindamisele, kas tulemused vastavad toodete müügiliikumisele. Soovitame hinnata tulemusi paar päeva, enne kui muudate parameetreid vastavalt vajadusele enne uuesti testimist. 

## <a name="understanding-recommendation-list-parameters"></a>Soovituste loendi parameetrite mõistmine

Enne parameetrite muutmist vaadake, kuidas need mõjutavad tulemusi allpool.

### <a name="trending-product-list"></a>Populaarne tooteloend

Populaarses tooteloendis on võimalik muuta kahte parameetrit.

![Populaarse loendi vaikeparameetrite näide](./media/exampletrendingparameters.png)

1. **Kaasa viimase X päeva uued tooted** – tooteid, mis on lisatud konkreetne arv päevi enne praegust kuupäeva, saab kasutada tootekanditaatide valimiseks. Vaikeväärtus pildil näitab, et populaarsete toodete loendis saab kasutada tooteid, mis on vähemalt 180 päeva vabad.
1. **Kaasa viimase X päeva müügid** – müügitehinguid, mis on toimunud konkreetne arv päevi enne praegust kuupäeva, saab kasutada toodete tellimiseks. Ülaltoodud vaikeväärtus näitab, et kõiki viimase 30 päeva jooksul sooritatud toote ostusid kasutatakse toote asukoha määratlemiseks populaarsete toodete loendis. 

### <a name="best-selling-product-list"></a>Enim müüdud toodete loend

Sõltuvalt teie ettevõttest, võib loend Enim müüdud anda populaarsete toodetega võrreldes erineva tulemuse, olgugi need mõlemad kasutavad toodete tellimiseks kandeandmeid. Kuna suvandil enim müüdud puudub sortimise kuupäeva põhjal tähtaeg, võib suvand enim müüdud tõsta esile endiselt väga populaarsed vanemad tooted, mis võisid populaarsete loendist välja langeda. 

Enim müüdud toodete loendis on võimalik muuta ühte parameetrit.

![Enim müüdud loendi vaikeparameetri näide](./media/examplebestsellingparameters.PNG)

1. **Kaasa viimase X päeva müügid** – müügitehinguid, mis on toimunud konkreetne arv päevi enne praegust kuupäeva, saab kasutada toodete tellimiseks. Ülaltoodud vaikeväärtus näitab, et kõiki viimase 30 päeva jooksul sooritatud toote ostusid kasutatakse toote asukoha määratlemiseks enim müüdud toodete loendis. 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a>Toodete käsitsi soovituse loenditesse lisamine või nendest eemaldamine

### <a name="for-new-trending-or-best-selling-lists"></a>Loendite Uus, Populaarne ja Enim müüdud jaoks

1.  Avage **Jaemüük ja kaubandus** > **Tootesoovitused** > **Soovituste parameetrid**.
1.  Jagatud parameetrite loendis valige suvand **Soovituste loendid**.
1.  Valige toodete loendisse lisamine või sellest eemaldamine.
1.  Toodete tabelisse lisamiseks valige suvand **Lisa rida.** 
1.  Veerus Toode otsige toodet suvandi **Nimi** või **Tootenumber** järgi.

    ![Näide toodete otsimisest uute toodete loendis](./media/examplenewlistconfiguration1.png)

1.  Valige veerus Rea tüüp üks kahest suvandist.
    -   **Kaasa** – sunnib toote loendi ette
    -   **Välista** – tühistab toote loendis ilmumise
    
    ![Näide toote kaasamisest või välistamisest uute toodete loendist](./media/examplenewlistconfiguration2.png)

1.  Suvandi **Kuvamise järjekord** muutmine muudab järjestust, kuidas suvandiga **kaasa** tähistatud tooted loendisse ilmuvad.
    - Kui kahel tootel on sama **kuvamise järjestuse** väärtus, siis võib nende kahe tulemuse lõplik tellimus kontorist erineda.
1.  Toodete tabelist eemaldamiseks: valige eemaldatav rida ja klõpsake käsku **Eemalda**.


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a>Loendite Inimestele meeldib ka ja Sageli koos ostetud jaoks

Loendite Sageli koos ostetud või Inimestele meeldib ka kontekstis kasutatakse masinõpet tarbija ostumustrite analüüsimiseks, et soovitada sageli koos ostetavaid seotud tooteid ainulaadseks lähteväärtuse tooteks. 
 
*Lähteväärtuse toode* on toode, mille jaoks soovite tulemusi luua. Soovituse loendite käsitsi reguleerimise kontekstis te lisate või eemaldate selle toote tulemusi. 

Lähteväärtus toote tulemuste käsitsi lisamiseks või eemaldamiseks tehke järgmist.
1.  Valige suvand **Lähteväärtuse toode**. 
1.  Veerus **Toode** otsige toodet suvandite **Nimi** või **Tootenumber** alusel.
![Näide toote otsimisest loendist Sageli koos ostetud](./media/exampleFBTlistconfiguration1.png)
1. Valige veerus **Rea tüüp** üks kahest suvandist.
    - **Kaasa** – sunnib toote loendi ette
    - **Välista** – tühistab toote loendis ilmumise     
![Näide toote loendisse Sageli koos ostetud kaasamisest või sellest eemaldamisest](./media/exampleFBTlistconfiguration2.png)
1.  Toodete tabelist eemaldamiseks: valige eemaldatav rida ja klõpsake käsku Eemalda.


## <a name="additional-resources"></a>Lisaressursid

[Tootesoovituste ülevaade](product-recommendations.md)

[Azure Data Lake Storage'i lubamine Dynamics 365 Commerce'i keskkonnas](enable-adls-environment.md)

[Luba tootesoovitused](enable-product-recommendations.md)

[Isikupärastatud soovituste lubamine](personalized-recommendations.md)

[Isikupärastatud tootesoovitustest loobumine](personalization-gdpr.md)

[„Sarnaste toodete vaatamise” soovituste lubamine](shop-similar-looks.md)

[Tootesoovituste lisamine kassas](product.md)

[Soovituste lisamine kandeekraanile](add-recommendations-control-pos-screen.md)

[Loo kuraatorite soovitused käsitsi](create-editorial-recommendation-lists.md)

[Soovituste loomine demoandmetega](product-recommendations-demo-data.md)

[Tootesoovituste KKK](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]