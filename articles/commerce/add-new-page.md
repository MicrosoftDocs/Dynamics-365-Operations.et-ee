---
title: Uue saidilehe lisamine
description: Selles teemas kirjeldatakse, kuidas lisada rakenduses Microsoft Microsoft Dynamics 365 Commerce uus saidi leht.
author: psimolin
ms.date: 02/03/2022
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
ms.openlocfilehash: e0c2a73ae9e85cb299e7cb6fc70562659cdfadc5
ms.sourcegitcommit: 1eef00796f7c5511f432b01800cdf8920992d7d5
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2022
ms.locfileid: "8090715"
---
# <a name="add-a-new-site-page"></a>Uue saidilehe lisamine

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas lisada rakenduses Microsoft Microsoft Dynamics 365 Commerce uus saidi leht.

Pärast saidi mallide ja fragmentide loomist on järgmine etapp lehtede loomise alustamine, mis neid kasutavad. Alustamiseks peate valima malli või paigutuse, lehe nime ja lehe URL-i.

## <a name="template-or-layout"></a>Mall või paigutus

Saate kasutada kas oma uue lehe malli või paigutust. Lisateavet vaadake teemast [Mallide ja paigutuste ülevaade](templates-layouts-overview.md).

## <a name="specify-the-page-name"></a>Lehe nime määramine

Lehe nimi peab olema teie saidile ainulaadne ja kirjeldav, et saaksite selle hõlpsalt leida ja teised inimesed teaksid, milleks leht mõeldud on. Lehe saate hiljem ümber nimetada, redigeerides seda ja valides seejärel atribuudipaanil lehe nime kõrval pliiatsi sümboli.

## <a name="specify-the-page-url"></a>Lehe URL-i määramine

Teil võib olla võimalus sisestada uue lehe URL. Lehe loomisel saate sisestada stringi, mida kasutatakse täieliku URL-i moodustamiseks. See string on tuntud kui suhteline URL või URL-i komponent. Seejärel luuakse URL-i komponendi põhjal täielik URL ja sellele määratakse uus leht. Saate URL-i komponenti hiljem muuta, enne kui avaldate lehe. Lisateavet vaadake teemast [Lehe URL-i loomine](create-page-URL.md) .

> [!NOTE]
> Dynamics 365 Commerce lahutab URL-id ja sisu. Teisisõnu saab luua lehe, mis ei ole URL-iga seotud, ja saab luua URL-i, mis ei ole seotud lehega. Seega saab URL-i sisu ära vahetada ja see ei nõua seisakuid ning ümbersuunamisi on hõlpsam hallata.

## <a name="add-a-new-page"></a>Uue lehe lisamine

Oma saidile uue saidi lehe lisamiseks toimige järgmiselt.

1. Jaotises **Saidid** valige suvand **Fabrikam** (või oma saidi nimi).
1. Valige suvand **Uus leht**.
1. Valige dialoogiaknas **Uus leht** mall ja valige seejärel nupp **OK**.
1. Väljale **Lehe nimi** sisestage lehe nimi (näiteks **Minu uus leht**).
1. Väljale **URL** sisestage string (URL-i komponent), et URL lõpetada (näiteks **minuuusleht**).
1. Valige nupp **OK**. Kuvatakse lehe redaktor. Pange tähele, et päis ja jalus lisatakse lehele automaatselt, olenevalt teie valitud mallist.
1. Lehe liigenduses valige pesa **Peamine**, valige kolmikpunkt nupp (**...**) ja seejärel valige suvand **Lisa moodul**.
1. Valige suvand **Konteiner** ja seejärel nupp **OK**
1. Valige **Sujuv konteiner**, kolmikpunkti nupp ja seejärel käsk **Lisa moodul**.
1. Valige **Sisurikas plokk** ja valige seejärel **OK**.
1. Valige **Sisurikas plokk**, kolmikpunkti nupp ja seejärel käsk **Lisa moodul**.
1. Valige **Sisurikka ploki üksus** ja valige seejärel **OK**.
1. Parempoolsel atribuutide paanil valige **Lõik** ja seejärel sisestage väljale **Minu katsetekst**.
1. Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.
1. Sisestage väljale **Kommentaarid** suvand **Lisatud uus leht** ja valige seejärel **OK**.
1. Lehe eelvaate kuvamiseks valige suvand **Eelvaade**. Kui olete lõpetanud, sulgege eelvaate vahekaart, et naasta autorluse tööriista.
1. Valige **Avalda**.
1. Navigeerimisteel (lingirida) valige **Fabrikam** (või oma saidi nimi).
1. Valige navigeerimispaanilt vasakult suvand **URL-id**.
1. Leidke loendist ja valige oma URL (**minuuusleht**).
1. Valige **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Olemasoleva saidilehe muutmine](modify-existing-page.md)

[Lehepaigutuste valimine](select-page-layouts.md)

[SEO metaandmete haldamine](manage-seo-metadata.md)

[Lehe salvestamine, eelvaade ja avaldamine](save-preview-publish-page.md)

[Tootelehe rikastamine](enrich-product-page.md)

[Kategooria sihtlehe rikastamine](enrich-category-page.md)

[Lehe sisu hõlbustusfunktsioonide kinnitamine](verify-accessibility.md)

[Dünaamiliste e-kaubanduse lehtede loomine URL-parameetrite põhjal](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
