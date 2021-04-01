---
title: SEO metaandmete haldamine
description: See teema kirjeldab, kuidas hallata rakenduses Microsoft Dynamics 365 Commerce otsingumootori optimeerimise (SEO) metaandmeid.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 00942befef9f9b6a878766bbbb5341426e31db2c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252602"
---
# <a name="manage-seo-metadata"></a>SEO metaandmete haldamine


[!include [banner](includes/banner.md)]

See teema kirjeldab, kuidas hallata rakenduses Microsoft Dynamics 365 Commerce otsingumootori optimeerimise (SEO) metaandmeid.

## <a name="overview"></a>Ülevaade

Saidi SEO metaandmeid saab hallata saidikaarte ja lehe metaandmeid kasutades.
    
## <a name="site-maps"></a>Saidikaardid

Saidikaart vastendus on teie veebisaidi lehtede (XML-vormingus) masinloetav loend. See on mõeldud otsingumootorite poolt kasutamiseks, et need saaksid teie saidilt paremaid otsingutulemusi pakkuda. Saidikaarte saab otsingumootoritesse käsitsi sisse tuua või avaldada robotite TXT-failis.

Dynamics 365 Commerce toetab saidikaartide automaatset loomist. Saidikaarte uuendatakse lehtede avaldamisel ja avaldamise tühistamisel automaatselt.

### <a name="turn-on-site-map-generation"></a>Saidikaardi loomise sisselülitamine

1. Logige autorluse tööriista sisse.
1. Jaotises **Saidid** valige suvand **Fabrikam** (või oma saidi nimi).
1. Valige navigeerimispaanilt vasakult suvand **Saidi haldus**.
1. Veenduge, et suvand **Saidikaardid lubatud** on sisse lülitatud.

## <a name="page-metadata"></a>Lehe metaandmed

Dynamics 365 Commerce võimaldab teil hallata individuaalsete lehtede SEO metaandmeid. Saate seda teavet vaadata ja muuta lehe konteineri jaotises **SEO atribuudid**. Praegu toetatakse järgmisi SEO metaandmete atribuute.

- Tiitel
- Kirjeldus
- SEO märksõnad
- ARIA-sildid
- noindex
- nofollow
- noarchive
- nocache
- noOpenDirectoryProject
- nosnippet
- noImageIndex
- unavailableAfter

### <a name="modify-page-metadata"></a>Lehe metaandmete muutmine

Lehe metaandmete muutmiseks toimige järgmiselt.

1. Jaotises **Saidid** valige suvand **Fabrikam** (või oma saidi nimi).
1. Valige navigeerimispaanilt vasakult suvand **Lehed**.
1. Valige avaleht, et avada see lehe redaktoris.
1. Klõpsake käsuribal käsku **Redigeeri**.
1. Parempoolsel atribuutide paanil laiendage suvandit **Vaikimisi metasildid**.
1. Uue metasildi lisamiseks valige suvand **Lisa** ja sisestage seejärel silt väljale. Olemasoleva metasildi eemaldamiseks valige selle kõrval paremal prügikasti sümbol.
1. Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.
1. Sisestage väljale **Kommentaarid** suvand **Uuendatud metasildid** ja valige seejärel **OK**.
1. Lehe eelvaate kuvamiseks valige suvand **Eelvaade**. Kui olete lõpetanud, sulgege eelvaate vahekaart, et naasta autorluse tööriista.
1. Valige **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Olemasoleva saidilehe muutmine](modify-existing-page.md)

[Uue saidilehe lisamine](add-new-page.md)

[Lehepaigutuste valimine](select-page-layouts.md)

[Lehe salvestamine, eelvaade ja avaldamine](save-preview-publish-page.md)

[Tootelehe rikastamine](enrich-product-page.md)

[Kategooria sihtlehe rikastamine](enrich-category-page.md)

[Lehe sisu hõlbustusfunktsioonide kinnitamine](verify-accessibility.md)

[Dünaamiliste e-kaubanduse lehtede loomine URL-parameetrite põhjal](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]