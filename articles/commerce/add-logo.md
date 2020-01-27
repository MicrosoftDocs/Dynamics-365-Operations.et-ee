---
title: Logo lisamine
description: Selles teemas kirjeldatakse, kuidas lisada logo rakenduses Microsoft Dynamics 365 Commerce oma saidile.
author: bicyclingfool
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23bac9aae6beb59912bbc9e1f2c6958c007550b0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914614"
---
# <a name="add-a-logo"></a>Logo lisamine

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas lisada logo rakenduses Microsoft Dynamics 365 Commerce oma saidile.

## <a name="overview"></a>Ülevaade

Kui te loote oma saiti, on üks esimesi asju, mida te tõenäoliselt teete, lisada oma ettevõtte või kaubamärgi logo saidi päisesse. Dynamics 365 Commerce Online Starter Kit pakub moodulit, mis muudab selle ülesande lihtsaks.

Logo saate lisada otse mallile, paigutusele või lehele. Sel viisil saate hõlpsasti muuta logo, mis kuvatakse kindlatel lehekülgedel või lehekülgede gruppides. See teema katab siiski kõige sagedasema stsenaariumi, kuhu lisate oma logo päise fragmenti, mida saab taaskasutada teie saidi kõigi lehtede puhul.

## <a name="prerequisites"></a>Eeltingimused

Enne kui saate lisada logo kõigile oma saidi lehtedele, peate need ülesanded lõpetama.

1. Laadige oma logo üles digitaalsete varade haldurile, millele pääsete juurde lehelt **varad**.
1. Loo päise fragment Lisateavet fragmentide loomise ja kasutamise kohta leiate teemast [töö fragmentidega](work-with-fragments.md)
1. Kaasake päise fragment malli, mida teie saidi leheküljed kasutavad paigutuse ja mooduli suvandite jaoks. Vaadake lisateavet mallidega töötamise kohta jaotisest [Töö mallidega](work-with-templates.md).

## <a name="add-a-logo-to-a-header-fragment"></a>Logo lisamine päise fragmenti

Oma saidi päise fragmenti logo lisamiseks toimige järgmiselt.

1. Vasakpoolses navigeerimispaanil valige **fragmendid**ja seejärel valige loodud päise fragment.
2. Valige suvand **Registreeri välja**.
3. Laiendage **päise** pesa ja **logo** pesa.
4. Valige **logo** pesa jaoks kolmikpunkti nupp (**…**) ja seejärel valige käsk **Lisa moodul**.
5. Valige logo moodul.
6. Konfigureerige paremal atribuutide paanil logo moodulit nii, et teie logo oleks näha.
7. Salvestage pease fragment, kontrollige seda ja avaldage see.

Pärast värskendatud päise fragmenti avaldamist kuvatakse kõik saidi lehed, mis kasutavad päise fragmenti sisaldavat malli, mis näitavad teie logo.

## <a name="additional-resources"></a>Lisaressursid

[Saidi kujunduse valimine](select-site-theme.md)

[CSS-i alistusfailidega töötamine](css-override-files.md)

[Leheikooni lisamine](add-favicon.md)

[Tervitussõnumi lisamine](add-welcome-message.md)

[Autoriõiguste teatise lisamine](add-copyright-notice.md)

[Saidile keelte lisamine](add-languages-to-site.md)

[Telemeetria toetamiseks saidile skriptikoodi lisamine](add-telemetry.md)

