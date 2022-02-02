---
title: Pilvepõhise otsingu ülevaade
description: See teema annab rakenduse Microsoft Dynamics 365 Commerce pilvepõhise otsingu ülevaate.
author: ashishmsft
ms.date: 06/29/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: eb34780d5bdd41a128fff543fe0f1ef73cfead8b
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2022
ms.locfileid: "7983665"
---
# <a name="cloud-powered-search-overview"></a>Pilvepõhise otsingu ülevaade

[!include [banner](includes/banner.md)]

See teema annab rakenduse Microsoft Dynamics 365 Commerce pilvepõhise otsingu ülevaate.

Toote tuvastatavus aitab tagada, et kliendid saavad kategooriaid sirvides, otsides ja filtreerides tooteid kiiresti ja hõlpsalt leida. Jaemüüjad peavad toodete avastamist esmaseks vahendiks klientidega suhtlemisel kõigis kanalites.

Kliendid on harjunud veebiotsingu mootorite peaaegu hetkelise reaktsiooniajaga, keeruliste e-kaubanduse veebisaitidega, sotsiaalsete rakendustega, otsingusõna tippimisel automaatselt ilmuvate soovitustega, mitmetahulise navigeerimisega ja esiletõstmisega. Kui kliendid ei leia ühest e-kaubanduse poest otsitavat toodet piisavalt kiiresti, siis nad ei kõhkle, et minna erinevasse e-kaupluse poodi.

Rakenduse Dynamics 365 Commerce pilvepõhine toote tuvastamine aitab jaemüüjatel jätkuvalt suurendada kliendi kinnipidamise ja teisendamise määrasid kõikide kanalite üleselt, nii e-kaubanduse kanalites kui ka kassa kanalites.

Rakenduse Dynamics 365 Commerce otsingul on parandatud võimalused, et aidata jaemüüjatel saavutada parem toodete tuvastatavus. Samal ajal pakuvad need võimalused e-kaubanduse liikluse jaoks vajalikku skaleeritavust ja jõudlust.

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

Praegused automaatse soovituse funktsioonid näitavad ainult märksõnu, mis käivitavad vastava märksõna otsingu. Rakenduse Dynamics 365 Commerce uute täiustuste abil saavad kliendid sageli tuvastada lingid toodetele enne, kui nad on tippimise lõpetanud.

Dynamics 365 Commerce toetab ka erinevate kategooriate märksõnade vasteid. See funktsioon võimaldab klientidel näha kattuvate märksõnade arvu kategooriate lõikes ja käivitada märksõnade otsimise teistes kategooriates.

Järgmisel joonisel on kujutatud näide, kus kasutatakse kõikehõlmavaid automaatseid soovitusi.

![kõikehõlmavad automaatsed soovitused.](./media/ImmersiveAutoSuggestUX.png)

## <a name="sort"></a>Tüüp

Rakenduse Dynamics 365 Commerce täiustatud sortimine võimaldab klientidel sortida, otsida ja sirvida otsingutulemusi ning täpsustada neid kriteeriumite põhjal, nagu hind, toote nimi ja tootenumber. Kliendid saavad lisaks sorteerida tulemusi selle põhjal, kas toode on uus, suurima läbimüügiga või hiljuti lisatud.

>[!NOTE]
>Need pilvepõhised otsinguvõimalused on saadaval alates versioonist 10.0.8. Veenduge, et jaotises **Kaubanduse parameetrid > konfiguratsiooniparameetrid** on kirje ProductSearch.UseAzureSearch väärtuseks määratud „tõene”. 
![Pilvepõhise otsingu konfiguratsiooniparameetrid.](./media/CloudPoweredSearchConfigurationParameters.png)

## <a name="additional-resources"></a>Lisaressursid

[Kategooria vaikesihtlehe ja otsingutulemuste lehe ülevaade](category-search-page-overview.md)

[SEO metaandmete haldamine](manage-seo-metadata.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
