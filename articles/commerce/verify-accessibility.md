---
title: Lehe sisu hõlbustusfunktsioonide kinnitamine
description: See artikkel kirjeldab, kuidas kontrollida lehekülje sisu hõlbustusfunktsioone Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: caccb6085947193e4a5f8a8555722dd073f0c275
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884756"
---
# <a name="verify-page-content-accessibility"></a>Lehe sisu hõlbustusfunktsioonide kinnitamine

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas kontrollida lehekülje sisu hõlbustusfunktsioone Microsoft Dynamics 365 Commerce.

Kui olete lehe muutmise lõpetanud, veenduge, et sisu oleks veebis kõigile juurdepääsetav. Commerce’i autorluse tööriistades saate hõlpsalt kontrollida lehe sisu juurdepääsetavust, kasutades sisse-ehitatud teenust [Microsoft Accessibility Insights](https://accessibilityinsights.io/). See teenus kontrollib teie lehe sisu vastavalt uusimatele [World Wide Webi konsortsiumi (W3C) juurdepääsetavuse](https://www.w3.org/standards/webdesign/accessibility) juhistele.

Enne selle kasutamist peab teenuse [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integratsioon olema rentniku või saidi tasemel sisse lülitatud.

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a>Teenuse Microsoft Accessibility Insights sisselülitamine rentniku kõikide saitide jaoks

Teenuse [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integratsiooni sisselülitamiseks kõikide rentniku Commerce’i saitide jaoks toimige järgmiselt.

> [!NOTE]
> Rentniku sätete avamiseks peate olema Commerce’i süsteemiadministraatorina sisse logitud.

1. Logige Commerce’i süsteemiadministraatorina sisse.
1. Valige vasakpoolsel navigeerimispaanil selle laiendamiseks suvand **Rentniku sätted** (hammasratta sümboli kõrval).
1. Jaotises **Rentniku sätted** valige suvand **Funktsioonid**.
1. Seadke valik **Hõlbustuskontroll** väärtusele **Sees**.

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a>Teenuse Microsoft Accessibility Insights sisselülitamine ühe saidi jaoks

Teenuse [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integratsiooni sisselülitamiseks Commerce’i ühe saidi jaoks toimige järgmiselt.

1. Jaotises **Saidid** valige suvand **Fabrikam** (või oma saidi nimi).
1. Vasakpoolsel navigeerimispaanil valige suvand **Saidi sätted** selle laiendamiseks.
1. Jaotises **Saidi sätted** valige suvand **Funktsioonid**.
1. Seadke valik **Hõlbustuskontroll** väärtusele **Sees**.

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a>Kodulehe sisu juurdepääsetavuse kontrollimine

Integreeritud teenuse [Microsoft Accessibility Insights](https://accessibilityinsights.io/) kasutamiseks Commerce’is oma kodulehe sisu skannimiseks ja kinnitamiseks toimige järgmiselt.

1. Jaotises **Saidid** valige suvand **Fabrikam** (või oma saidi nimi).
1. Valige vasakpoolsel navigeerimispaanil suvand **Lehed**.
1. Leidke ja valige avaleht, et avada see lehe redaktoris.
1. Klõpsake käsuribal käsku **Kontrolli kasutushõlpsust**. Kuvatakse leht **Kontrolli kasutushõlpsust**.
1. Vadake pärast skannimise lõpetamist aruande sisu üle.
1. Kui mõni kontroll ebaõnnestus, valige iga ebaõnnestunud kontroll, et seda laiendada, et saaksite vaadata rohkem üksikasju.
1. Pärast selle läbivaatamist aruande sulgemiseks kerige lehe **Kontrolli kasutushõlpsust** lõppu ja valige **OK**.

## <a name="additional-resources"></a>Lisaressursid

[Olemasoleva saidilehe muutmine](modify-existing-page.md)

[Uue saidilehe lisamine](add-new-page.md)

[Lehepaigutuste valimine](select-page-layouts.md)

[SEO metaandmete haldamine](manage-seo-metadata.md)

[Lehe salvestamine, eelvaade ja avaldamine](save-preview-publish-page.md)

[Tootelehe rikastamine](enrich-product-page.md)

[Kategooria sihtlehe rikastamine](enrich-category-page.md)

[Dünaamiliste e-kaubanduse lehtede loomine URL-parameetrite põhjal](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
