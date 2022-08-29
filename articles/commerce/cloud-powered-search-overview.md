---
title: Pilvepõhise otsingu ülevaade
description: See artikkel annab ülevaate pilvepõhisest otsingust Microsoft Dynamics 365 Commerce
author: ashishmsft
ms.date: 02/28/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.assetid: ''
ms.openlocfilehash: ed80ff42ea5c6e6a904ea2855953d006f66aad37
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273662"
---
# <a name="cloud-powered-search-overview"></a>Pilvepõhise otsingu ülevaade

[!include [banner](includes/banner.md)]

See artikkel annab ülevaate pilvepõhisest otsingust Microsoft Dynamics 365 Commerce

Toote tuvastatavus aitab tagada, et kliendid saavad kategooriaid sirvides, otsides ja filtreerides tooteid kiiresti ja hõlpsalt leida. Jaemüüjad kaaluvad toote tuvastamist peamiseks tööriistaks kliendiga suhtlemiseks läbi pilveskaala üksuse (CSU) toestatud kanalite, nagu e-äri ja müügikoha (POS).

Kliendid on harjunud veebiotsingu mootorite peaaegu hetkelise reaktsiooniajaga, keeruliste e-kaubanduse veebisaitidega, sotsiaalsete rakendustega, otsingusõna tippimisel automaatselt ilmuvate soovitustega, mitmetahulise navigeerimisega ja esiletõstmisega. Kui kliendid ei leia kiiresti toodet, mida nad ühe e-kaubanduskaupluse seast otsib, ei soovi nad minna teise e-äri kauplusesse.

Pilve toega toote leidmine äris aitab jaemüüjatel jätkata tarbijalojaalsuse ja teisendusmäärade suurendamiseks kõigis CSU kanalites.

Commerce’i otsingukogemus on täiustatud võimalusi, et aidata jaemüüjatel paremini tooteavastada. Samal ajal tarnivad need võimalused skaleeritavust ja jõudlust, mis on vajalik e-kaubanduse liikluseks.

## <a name="browse-and-search"></a>Sirvimine ja otsing

Otsingu asjakohasus ja jõudlus on omnikanali kogemuse põhitegurid, kuna toote tuvastamine sõltub peamiselt teabe toomise ja sisu navigeerimise otsingu funktsioonidest. Efektiivne ja tõhus sirvimis- ja otsingukogemus aitavad teisendamist suurendada.

Järgmisel illustratsioonil on toodud tüüpiline sirvimis- ja otsingufunktsiooni näide.

![Sihtlehe otsing.](./media/SearchLanding.png)

## <a name="faceted-navigation-and-choice-summary"></a>Mitmetahuline navigeerimine ja valiku kokkuvõte 

Mitmetahuline navigeerimine aitab klientidel hõlpsamini sisu sirvida, võimaldades neil filtreerida piiritlusatribuutidega, mis on lingitud terminikomplekti mõistetega. Kui klient on valinud ja rakendanud piiritlusatribuudid, kuvatakse valikute kokkuvõte. 

Mitmetahulist navigeerimist kasutades saate konfigureerida erinevad piiritlusatribuudid erinevatele terminikomplekti mõistetele, ilma et peaksite täiendavaid lehti looma. 

Järgmisel joonisel on kujutatud näide, kus otsingus kasutatakse mitmetahulist navigeerimist.

![Valikute kokkuvõte.](./media/ChoiceSummary.png)

## <a name="immersive-autosuggest"></a>Kõikehõlmavad automaatsed soovitused

Praeguse automaatuuendusfunktsiooniga kuvatakse märksõna, mis käivitab vastava märksõna otsingu. Äris tehtud uute täiustuste tõttu saavad kliendid sageli avastada linke toodetele, enne kui nad on tippimise lõpetanud.

Commerce toetab ka märksõna sobivusfunktsioone mitmetes kategooriates. See funktsioon võimaldab klientidel näha kattuvate märksõnade arvu kategooriate lõikes ja käivitada märksõnade otsimise teistes kategooriates.

Järgmisel joonisel on kujutatud näide, kus kasutatakse kõikehõlmavaid automaatseid soovitusi.

![kõikehõlmavad automaatsed soovitused.](./media/ImmersiveAutoSuggestUX.png)

## <a name="sort"></a>Sordi

Sortimisfunktsioon võimaldab klientidel sortida, otsida ja sirvida kategooria tulemusi ning piiritleda need kriteeriumidega nagu hind, toote nimi ja tootenumber. Kui lubate [tootesoovitused](product-recommendations.md) oma keskkonnas, saavad kliendid sortida tulemusi ka täiustatud sortimiskriteeriumide (nt uue, parimate müügi ja trendide) alusel.


> [!NOTE]
> Need pilvepõhised otsinguvõimalused on saadaval alates versioonist 10.0.8. Veenduge, et commerce Parameters oleks jaotises ProductSearch.UseAzureSearch **kirje seatud konfiguratsiooniparameetrites väärtusele > "tõene"**. 
![Pilvepõhise otsingu konfiguratsiooniparameetrid.](./media/CloudPoweredSearchConfigurationParameters.png)
>Täpsemad sortimisvalikud nagu uus, best-müük ja trending on saadaval Commerce SSK versiooniga 9.35+ Dynamics 365 Commerce ja 10.0.20 väljalaskega.  


## <a name="additional-resources"></a>Lisaressursid

[Kategooria vaikesihtlehe ja otsingutulemuste lehe ülevaade](category-search-page-overview.md)

[SEO metaandmete haldamine](manage-seo-metadata.md)


[!INCLUDE [footer-include](../includes/footer-banner.md)]
