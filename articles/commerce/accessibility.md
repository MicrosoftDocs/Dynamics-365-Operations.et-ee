---
title: Hõlbustusfunktsioonid ja -võimalused
description: See artikkel annab teavet juurdepääsufunktsioonide ja võimaluste kohta Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: a797b94d8101100574169cdcecfe8df2b5954c15
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278147"
---
# <a name="accessibility-features-and-capabilities"></a>Hõlbustusfunktsioonid ja -võimalused

[!include [banner](includes/banner.md)]

See artikkel annab teavet juurdepääsufunktsioonide ja võimaluste kohta Microsoft Dynamics 365 Commerce.

Hõlbustusfunktsioonid ja -võimalused annavad kõigile kasutajatele funktsionaalsed vahendid juurdepääsuks ja toimingute tegemiseks, et nad saaksid täita oma eesmärke. See lai kasutajate hulk võib nõuda abistavaid tööriistu kuulmiseks, nägemiseks, liikuvuseks või neurodiversiteediks.

Erinevad funktsioonid Dynamics 365 Commerce võimaldavad teil oma saiti ehitada nii, et see hõlmaks abistavat funktsiooni. Saidi kujundamisel peaksite arvestama hõlbustusfunktsioonide funktsionaalsuse aladega, mis on nimetatud [Microsoft Accessibility Centeris ](https://www.microsoft.com/accessibility). 

See artikkel kirjeldab mõningaid juurdepääsufunktsioonide lisaalasid, mida peaksite arvestama, kui kasutate Dynamics 365 Commerce.

## <a name="image-alt-text"></a>Pildi alt tekst

Dynamics 365 Commerceon sisseehitatud digitaalse varahalduse süsteem, et jälgida teie saidil kasutatavaid pildi ja video varasid. Pildi pealdisi, kirjeldusi ja ALT-teksti saab lisada kujutisele atribuutide paanile, kui see on valitud või üles laaditud.

## <a name="video-accessibility"></a>Video juurdepääs

Dynamics 365 Commerce digitaalse varahalduse süsteem toetab paljusid video sisu hõlbustusfunktsioone. Järgmises tabelis on loetletud mõned näited.

| Video funktsioon               | Kirjeldus |
|-----------------------------|-------------|
| Suletud pealdis (CC)      | Tekst, mida saab kuvada video heli- ja audiot kirjeldavate elementide jaoks, et aidata kasutajaid, kes on kurdid või vaegkuuljad |
| Subtiitrid                   | Pealdise failid, mis näitavad konteksti vihjete või dialoogi kuvamise teksti |
| Audio ärakirjad           | Video-vara helist loodud räägitud sõnade tekstiline koopia |
| Kirjeldav heli           | Mitte esmane heli kanal, mis kirjeldab ekraanil kuvatavat sisu või konteksti |
| Minimaalne vanus            | Atribuut, mis võib talletada vanuse alampiiri, mis peab vaatajal video vaatamiseks olema (ainult metaandmed) |

### <a name="configure-video-accessibility-elements"></a>Video hõlbustusfunktsioonide elementide konfigureerimine

Oma saidi jaoks saate Commerce'i jaotises **meediumiteek** üles laadida video varad, millel on suletud pealdiste, korrapärase heli ja kirjeldava heli jaoks eraldi failid. Suletud pealdisi saab ka automaatselt luua, kui video vara üles laaditakse.

#### <a name="generate-or-upload-closed-caption-files-during-video-asset-upload"></a>Suletud pealdise failide loomine või üleslaadimine video vara üleslaadimise ajal

Kui soovite video üleslaadimisel automaatselt luua suletud pealdise faili, järgige seda sammu.

- Dialoogiaknas **vara üleslaadimine** märkige **Loo suletud pealdised automaatselt**. Kui loote suletud pealdise faili, ei ole suletud pealdise failide jaoks saadaval faili valija dialoogiaknas saadaval.

Kui soovite video üleslaadimisel suletud pealdise faili käsitsi üles laadida, järgige seda sammu.

- Dialoogiaknas **vara üleslaadimine** eemaldage **Loo suletud pealdised automaatselt**.

Video tavaliste heli-või kirjeldavate helifailide üleslaadimiseks kasutage dialoogiaknas **vara üleslaadimine** faili valijat.

> [!NOTE]
> Pärast video vara üleslaadimist saab lisada ka suletud pealdise, korrapärase heli ja kirjeldava heli vara. Liikuge **meediumiteeki**, valige video vara ja siis **Redigeeri**, et seda vaadata. Seejärel laadige lisavarad üles video vara atribuutide paanil.

#### <a name="edit-cc-and-audio-transcript-files"></a>CC ja audio-kirjutuse failide redigeerimine

CC ja audio-kirjutuse faile saab redigeerida otse autorluse tööriistas. Video taasesitus on saadaval redigeerimise ajal.

CC ja audio-kirjutuse failide redigeerimiseks toimige järgmiselt.

1. Avage **meediumiteek** ja valige video vara failinimi. Kuvatakse suletud pealdise ja ärakirja sisu redaktor.
1. Valige suvand **Redigeeri**.
1. Saate redigeerida suletud pealdise või ärakirja teksti.
1. Kui olete lõpetanud, valige **Salvesta** ja seejärel **Lõpeta redigeerimine**.
1. Kui olete avaldamiseks valmis, valige **avalda**.

#### <a name="set-the-minimum-age-attribute"></a>Vanuse alampiiri atribuudi määramine

**Minimaalse vanuse** metaandmete atribuuti saab seostada video varadega.

Video vara **vanuse alampiiri** atribuudi määramiseks järgige neid samme.

1. Avage **meediumiteek** ja valige video vara.
1. Valige suvand **Redigeeri**.
1. Määrake video vara paanil atribuudid **vanuse alampiiri** atribuut.

> [!NOTE]
> Atribuutide paani kasutatakse ainult metaandmete atribuudi väärtuse seadistamiseks ja talletamiseks. Selle atribuudi kasutamiseks taasesituse väravamutatsiooniga tuleb luua kohandatud moodulid.

## <a name="additional-resources"></a>Lisaressursid

[Vormide, toodete ja juhtelementide hõlbustatus](/dynamics365/unified-operations/dev-itpro/user-interface/enable-accessibility)

[Microsoft juurdepääsukeskus](https://www.microsoft.com/accessibility)

[Dynamics 365 hõlbustusfunktsioonide keskus](/dynamics365/get-started/accessibility/index)

[Vastavuse ülevaade](compliance-overview.md)

[Küpsise vastavus](cookie-compliance.md)

[Privaatsuspoliitika lehe lisamine](add-privacy-page.md)

[Jälgitud sisumuudatustega seostatud kasutaja ID-de asendamine](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
