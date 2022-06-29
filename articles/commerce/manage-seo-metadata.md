---
title: SEO metaandmete haldamine
description: See artikkel kirjeldab, kuidas hallata otsingumootori optimeerimise (SEO) metaandmeid moodulis Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 99c28c2bff7b683f3e92dea4ba24d8bead556443
ms.sourcegitcommit: 6616b969afd6beb11a79d8e740560bf00016ea7f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/17/2022
ms.locfileid: "9027305"
---
# <a name="manage-seo-metadata"></a>SEO metaandmete haldamine

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas hallata otsingumootori optimeerimise (SEO) metaandmeid moodulis Microsoft Dynamics 365 Commerce.

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
1. Leheredaktoris lehe ülaosas kuvatakse liigenduskontroll vasakul, **valige** suvand Liigendusrežiim (käigu sümbol) ja seejärel valige liigendusvaade **Täpsem**.
1. Laiendage liigendusvaates puu juhtelemente HTML-peapesa **sisu kuvamiseks**.
1. **Valige HTML-peapesast** soovitud SEO-moodul (**nt Lehe** kokkuvõte, **Tootelehe kokkuvõte**, **Kategoorialehe kokkuvõte** või **Metatagid**).
1. Redigeerige atribuutide paanil paremal soovitud SEO-andmeid valitud SEO-mooduli jaoks (nt Pealkiri **, Kirjeldus** **või Ühiskasutuse pilt** **).**
1. Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.
1. Sisestage **väljale** Kommentaarid uuendatud **SEO-andmed** ja seejärel valige **OK**.
1. Lehe eelvaate kuvamiseks valige suvand **Eelvaade**. Kui olete lõpetanud, sulgege eelvaate vahekaart, et naasta autorluse tööriista.
1. Valige **Avalda**.

> [!TIP]
> Autorid saavad leheredaktoris **kasutada** vasaku liigendusredaktori ülaosas liigendusrežiimi suvandit (käigusümbolit), **et lülitada üldise liigendusvaate ja täpsema** **liigendusvaate vahel.** **Üldine liigendusvaade** on vaikesäte ja filtreerib **liigenduse nii, et see näitab lehekülje keha** HTML-pesas ainult mooduleid. **Täpsem liigendusvaade** näitab tervet lehemoodulit, sh **HTML-i pea**, **kehaosa algus** ja keha **lõpupesad**. See vaade on kasulik, kui autorid peavad redigeerima konkreetsed SEO või skripti mooduli sätted lehekülje jaoks.

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
