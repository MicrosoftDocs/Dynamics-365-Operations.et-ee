---
title: Riigi/regiooni valija moodul
description: See teema hõlmab tarneaadressi moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce konfigureerida.
author: stuharg
ms.date: 04/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2021-08-12
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 9c20e614053b7a79cf962990dbd13ca0f45d5a00
ms.sourcegitcommit: 4861ec2d3ae24cc9dd4ad3ac748fd05be3d80c70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/06/2022
ms.locfileid: "8551666"
---
# <a name="countryregion-picker-module"></a>Riigi/regiooni valija moodul

[!include [banner](includes/banner.md)]

See teema hõlmab tarneaadressi moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce konfigureerida.

Riigi/regiooni valijamoodul [kasutab geotuvastuse](geo-detection-redirection.md)Dynamics 365 Commerce ja ümbersuunamise funktsiooni soovitatud saitide näitamiseks klientidele, kes taotlevad e-ärisaidi URL-i, mis ei ole seotud nende riigi või regiooniga.

Näiteks soovib klient Kanadas saidi URL-i, mis on seotud muu riigiga kui Kanada. Sel juhul näitab riigi/regiooni valija dialoogiboks, mis soovitab Kanadaga seotud saidi URL-e. 

## <a name="how-it-works"></a>Toimimisviis

Kui geotuvastus ja ümbersuunamine on saidi puhul lubatud ja klient taotleb saidi URL-i, kasutatakse kliendi kohta tuvastatud riiki ja taotletud URL-i määramaks, kas see URL on vastendatud riigile, kus klient on. URL-ide ja riikide vaheline vastendamine määratakse kanalite **lehel Commerce'i** **saidikonstruktori saidisätete** all. 

Kui taotluse URL ei vasta ühelegi kliendi riigiga vastendatud URL-le, tagastatakse vastuses selle riigiga vastendatud ühe või mitme URL-i loend. Riigi/regiooni valija võrdleb kõiki loendis sisestatud URL-e riigi/regiooni moodulis konfigureeritud URL-dega. Iga leitud täpse vaste puhul renderdab riigi/regiooni valija selle URL-i kuvamispäise, alapealkirja ja pildi ning hüperlingid need elemendid URL-i kasutades.

Kui klient valib riigi/regiooni valija suvandi, võetakse ta hüperlingiga URL-ile. See URL kirjutatakse küpsistele **\_ msdmeeter365\_\_\_\_** nii, et seda saab kasutada kliendi saidi-eelistusena. Seejärel, kui klient taotleb järgmisel korral URL-i, mis ei ole seotud nende riigi või regiooniga, suunatakse need automaatselt ümber oma eelistatud riiki. Seetõttu on soovitatav kasutada [e](site-selector.md)-kaubanduse saidil ka saidi valijamoodulit, et klientidel oleks võimalus oma saidi-eelistusi alistada või uuendada. 

Kui klient sulgeb riigi/regiooni valija dialoogiboksi, ei kirjutata küpsistet ja klient jääb praegusele saidile. 

Järgmisel joonisel on näide valija riigi/piirkonna dialoogiboksist.

![Riigi/regiooni valija dialoogiboksi näide avalehel.](./media/Geo_country-region-module-insitu.png)

## <a name="countryregion-picker-module-properties"></a>Riigi/regiooni valija mooduli atribuudid

| Atribuudi nimi              | Väärtus       | Kirjeldus                                                  |
| -------------------------- | ----------- | ------------------------------------------------------------ |
| Päis                    | Tekst        | Dialoogiakna ülaosas kuvatav pealkiri.       |
| Alapealkiri                 | Tekst        | Pealkirja all kuvatav alapealkiri.               |
| Riik: kuva string    | Tekst        | URL-i suvandi kuvatav nimi (nt "Kanada").   |
| Riik: kuva alamstring | Tekst        | URL-i suvandi valikuline kuvamise alamstring (nt "inglise" või "prantsuse"). |
| Riik: riigi pilt     | Meedia vara | URL-i suvandiga seostatud valikuline pilt (nt Kanada lipu pilt). |
| Riik: riigi URL       | Tekst        | Konfigureeritav riigi/regiooni saidi URL. See URL peab täpselt vastama URL-ile, mille määras riigi/regiooni **jaoks** **Commerce**'i saidikonstruktori saidisätete all kanalite lehel. Url-i domeen peab olema ka kohandatud domeen, mis on **määratud kanalite lehe väljal Domeeni vastendamine, mitte saidi tööaadress,** **mida Commerce pakub, kui loote oma e-ärikeskkonna (nt URL-i**).`https://<yourcompany>.commerce.dynamics.com/` |
| Tegevuslink                | Tegevuslink | Valikuline link, mis kuvatakse dialoogiboksi allosas. Näiteks võib see link osutada siselehele, kus on loend kõigi nende riikide ja piirkondade kohta, mida sait toetab. |

## <a name="add-a-countryregion-picker-module-to-a-page"></a>Riigi/regiooni valijamooduli lisamine lehele

Riigi/regiooni valijamoodulit saab päisemoodulisse lisada kas otse või ühiskasutuses killu abil. Lisateavet päise moodulite kohta vt teemast [Päisemoodul](author-header-module.md).

## <a name="configure-the-countryregion-picker-module-in-commerce-site-builder"></a>Riigi/regiooni valijamooduli konfigureerimine Commerce'i saidi koostajas

> [!NOTE]
> Riigi/regiooni valijamoodulis peavad klientide jaoks soovitavad URL-id olema konfigureeritud riigiobjektideks.

Iga saidi URL-i puhul, mida soovite klientidele kuvada ja soovitada, järgige Neid samme Commerce'i saidiloojas.

1. Valige riigi/piirkonna valijamooduli pesa.
1. Valige atribuutide paani jaotises **Riigi loend** suvand **Lisa riik**.
1. Valige uus **Riigi** ruut.
1. Sisestage **kuvatav string** väljale kuvatav nimi (nt **Kanada**).
1. Valikuline: **Kuva alamstring** väljale sisestage kuvatav alamstring (nt **prantsuse** või **fr-ca**).
1. Valikuline: valige meediateegist pilt.
1. Sisestage **Riigi URL** väljale URL. See URL peab täpselt vastama KANALI lehel kuvatavale URL-ile, mis on **vastendatud** kanaliga, k.a riigi või regiooniga seostatud lokaadiga. 
1. Valige nupp **OK**.
1. Korrake neid samme teiste riigi URL-ide puhul, mida soovite riigi/piirkonna valijamoodulis kuvada.

## <a name="additional-resources"></a>Lisaressursid

[Saate häälestada geotuvastust ja ümbersuunamist](geo-detection-redirection.md)

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Päisemoodul](author-header-module.md)

[Saidi valija moodul](site-selector.md)

[Lingireamoodul](add-breadcrumb.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
