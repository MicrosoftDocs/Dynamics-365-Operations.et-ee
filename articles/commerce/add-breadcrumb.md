---
title: Lingirea moodul
description: See teema hõlmab lingirea mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 38efc3a60ae0ba49db2036dc84c49e4896727d94
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621056"
---
# <a name="breadcrumb-module"></a>Lingirea moodul

[!include [banner](includes/banner.md)]

See teema hõlmab lingirea mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

## <a name="overview"></a>Ülevaade

Lingirea mooduleid kasutatakse saidi lehtede teisese navigeerimise võimaldamiseks. Tavaliselt kuvatakse need lehe ülaosas päise all. Kuigi lingirea mooduleid saab lisada igale lehele, kasutatakse neid kõige sagedamini toote üksikasjade lehtedel, et kuvada toote kategooriahierarhiat ja pakkuda kiiret võimalust saidil navigeerimiseks. Lingirea moodulit saab kasutada ka lingi „Tagasi tulemuste juurde“ kuvamiseks, kui kasutajad avavad otsingus või loendilehel toote üksikasjade lehe. Nii saavad kasutajad kiiresti filtreeritud loendilehele tagasi pöörduda ning jätkata ostlemist.

Tootekategooria kontekstiga lehtedel, nagu näiteks toote üksikasjade lehed ja kategooria lehed, kuvavad lingirea moodulid kategooriahierarhiat. Kategooria kontekstita lehtedel kuvavad lingirea moodulid vaikimisi **&lt;Saidi juur&gt; / &lt;Praegune leht&gt;**. Lisaks saab lingirea mooduleid teist tüüpi saidilehtedel käsitsi konfigureerida, et kuvada saidil konkreetsete lehtede linke.

Järgmisel pildil on näidatud lingirea mooduli näide, kus on toodud toote üksikasjade lehe kategooriahierarhia.

![Lingirea mooduli näide](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a>Lingirea mooduli sätted

Lingirea moodul tugineb sättele **Lingirea kuvamistüüp toote üksikasjade lehel**, mis on määratletud saidiehitaja jaotises **Saidi sätted \> Laiendused**. Sellel sättel on kolm võimalikku väärtust.

- **Kuva kategooriahierarhia** – kui see väärtus on valitud, kuvatakse lingirea moodulis toote üksikasjade lehel vaadatava toote terviklik kategooriahierarhia.
- **Kuva tagasi tulemuste juurde** – kui see väärtus on valitud, kuvab lingirea moodul toote üksikasjade lehel linki „Tagasi tulemuste juurde“, juhul kui kasutaja on avanud toote üksikasjade lingi moodulist, mis võimaldab lingi „Tagasi tulemuste juurde“ kuvamist. See funktsioon on saadaval juhul, kui kasutajad navigeerivad kategooria, otsingu, loendi ja soovituste loendi lehtedelt. Selle funktsionaalsuse toetamiseks on tootekogumi ja otsingutulemuste moodulitel atribuut nimega **Luba toote üksikasjade lehel tagasi tulemuste juurde**. See atribuut annab teile paindlikkuse määratleda, millised moodulid peaks toetama toote üksikasjade lehel lingi „Tagasi tulemuste juurde“ funktsiooni. Näiteks kui lingirea mooduli sätte **Lingirea kuvamistüüp toote üksikasjade lehel** jaoks on valitud suvand **Kuva tagasi tulemuste juurde** ja otsingulehe otsingutulemuste mooduli jaoks on valitud suvand **Luba toote üksikasjade lehel tagasi tulemuste juurde**, siis kuvatakse link „Tagasi tulemuste juurde“, kui kasutaja navigeerib otsingulehelt toote üksikasjade lehele.
- **Kuva kategooriahierarhia ja tagasi tulemuste juurde** – see väärtus on eelmise kahe kombinatsioon. Kui see väärtus on valitud, siis kuvab lingirea moodul toote üksikasjade lehel nii terviklikku kategooriahierarhiat kui ka linki „Tagasi tulemuste juurde“ (kui see on konfigureeritud).

## <a name="breadcrumb-module-properties"></a>Lingirea mooduli atribuudid

| Atribuudi nimi | Väärtused | Kirjeldus |
|---------------|--------|-------------|
| Juur | Tekst või link| See valikuline atribuut määratleb lingirea saidijuure jaoks lingi teksti ja lingi sihtkoha. Kui atribuut ei ole konfigureeritud, siis juurt ei määratleta. |
| Lingirea link | Seos | See valikuline atribuut määratleb käsitsi konfigureeritud lingirea lingid, kui need lingid on nõutud. Lingid kuvatakse selles järjekorras, nagu need on loetletud. |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a>Lingirea mooduli lisamine uuele lehele

Toote üksikasjade lehele lingirea mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Avage **Saidi sätted /> Laiendused** ja seejärel valige sättes **Lingirea kuvamistüüp toote üksikasjade lehel** suvand **Kuva kategooriahierarhia**.
1. Avage **Mallid** ja seejärel valige toote üksikasjade lehe mall.
1. Valige ostukasti moodulit sisaldavas pesas **Konteiner** kolmikpunkt (**...**) ja seejärel **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Lingirida** ja klõpsake seejärel **OK**.
1. Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Avage **Lehed** ning avage toote üksikasjade lehe malli kasutav toote üksikasjade leht. Kui toote üksikasjade lehte ei ole veel olemas, siis looge see.
1. Valige ostukasti moodulit sisaldavas pesas **Konteiner** kolmikpunkt (**...**) ja seejärel **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Lingirida** ja klõpsake seejärel **OK**.
1. Valige pesas **Lingirida** toodud atribuutide paanilt **Juur**, valige **Lingi tekst**.
1. Valige dialoogiboksis **Lingi tekst** suvand **Avaleht** ja seejärel valige jaotises **Lingi sihtkoht** suvand **Lisa link**.
1. Valige lingirea juure jaoks link dialoogiboksis **Lisa link** ning valige seejärel **OK**.
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.
1. Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Kategooria vaikesihtlehe ja otsingutulemuste lehe ülevaade](category-search-page-overview.md)

[Tootekogumi moodulid](product-collection-module-overview.md)

[Ostukasti moodul](add-buy-box.md)