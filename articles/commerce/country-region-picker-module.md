---
title: Riigi/regiooni valija moodul
description: See teema hõlmab tarneaadressi moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce konfigureerida.
author: stuharg
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2021-08-12
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 3134e10c096525ec2d82365a25eff16a3c5d5e11
ms.sourcegitcommit: d420b96d37093c26f0e99c548f036eb49a15ec30
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/03/2021
ms.locfileid: "7472597"
---
# <a name="countryregion-picker-module"></a>Riigi/regiooni valija moodul

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

See teema hõlmab tarneaadressi moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce konfigureerida.

Riigi/regiooni valijamoodul kasutab [geotuvastuse ja ümbersuunamise](geo-detection-redirection.md) funktsiooni rakenduses Dynamics 365 Commerce soovitatud URL-ide näitamiseks klientidele, kes taotlevad e-ärisaidi URL-i, mis ei ole seotud nende riigi või regiooniga.

Näiteks klient Kanadas taotleb saidi URL-i, mis ei ole Kanadaga seostatud. Sel juhul näitab riigi/regiooni valija dialoogiboks, mis soovitab Kanadaga seotud saidi URL-e. Järgmisel joonisel on näide valija riigi/piirkonna dialoogiboksist.

![Riigi/regiooni valija dialoogiboksi näide avalehel.](./media/Geo_country-region-module-insitu.png)

## <a name="countryregion-picker-module-properties&quot;></a>Riigi/regiooni valija mooduli atribuudid

| Atribuudi nimi              | Väärtus       | Kirjeldus |
| -------------------------- | ----------- | ----------- |
| Päis                    | Tekst        | Dialoogiakna ülaosas kuvatav pealkiri. |
| Alapealkiri                 | Tekst        | Pealkirja all kuvatav alapealkiri. |
| Riik: kuva string    | Tekst        | URL-i suvandi kuvatav nimi (nt &quot;Kanada"). |
| Riik: kuva alamstring | Tekst        | URL-i suvandi valikuline kuvamise alamstring (nt "inglise" või "prantsuse"). |
| Riik: riigi pilt     | Meedia vara | URL-i suvandiga seostatud valikuline pilt (nt Kanada lipu pilt). |
| Riik: riigi URL       | Tekst        | URL, mis vastab kanalile ja lokaadile, mis on konfigureeritud riigi või regiooni jaoks Commerce'i saidikonstruktori **kanalite** lehel (**Saidisätete \> Kanalid**). See URL peab täpselt vastama URL-ile, mis on **kanalite** lehel konfigureeritud. |
| Tegevuslink                | Tegevuslink | Valikuline link, mis kuvatakse dialoogiboksi allosas. Näiteks võib see link osutada siselehele, kus on loend kõigi nende riikide ja piirkondade kohta, mida sait toetab. |

## <a name="add-a-countryregion-picker-module-to-a-page"></a>Riigi/regiooni valijamooduli lisamine lehele

Riigi/regiooni valijamoodulit saab päisemoodulisse lisada kas otse või ühiskasutuses killu abil. Lisateavet päise moodulite kohta vt teemast [Päisemoodul](author-header-module.md).

## <a name="configure-the-countryregion-picker-module-in-commerce-site-builder"></a>Riigi/regiooni valijamooduli konfigureerimine Commerce'i saidi koostajas

> [!NOTE]
> Riigi/regiooni valijamoodulis peavad klientide jaoks soovitavad URL-id olema konfigureeritud riigiobjektideks.

Iga URL-i puhul, mida soovite klientidele kuvada ja soovitada, järgige Neid samme Commerce'i saidi koostajas.

1. Valige riigi/piirkonna valijamooduli pesa.
1. Valige atribuutide paani jaotises **Riigi loend** suvand **Lisa riik**.
1. Valige uus **Riigi** ruut.
1. Sisestage **kuvatav string** väljale kuvatav nimi (nt **Kanada**).
1. Valikuline: **Kuva alamstring** väljale sisestage kuvatav alamstring (nt **prantsuse** või **fr-ca**).
1. Valikuline: valige meediateegist pilt.
1. Sisestage **Riigi URL** väljale URL. See URL peab täpselt vastama **Kanalid** lehel kuvatavale URL-ile ja olema kanaliga vastendatud, k.a riigi või regiooniga seostatud lokaadiga.
1. Valige nupp **OK**.
1. Korrake neid samme teiste riigi URL-ide puhul, mida soovite riigi/piirkonna valijamoodulis kuvada.

## <a name="additional-resources"></a>Lisaressursid

[Saate häälestada geotuvastust ja ümbersuunamist](geo-detection-redirection.md)

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Päisemoodul](author-header-module.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]