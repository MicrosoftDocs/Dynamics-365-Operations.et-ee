---
title: Kaardimoodul
description: See teema hõlmab kaardimooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce konfigureerida.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: a0f5d902289c5867095e34a135c50d342f3c4f13
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/31/2020
ms.locfileid: "3646910"
---
# <a name="map-module"></a>Kaardimoodul

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

See teema hõlmab kaardimooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce konfigureerida.

## <a name="overview"></a>Ülevaade

Kaardimoodul kuvab kaupluste asukohad interaktiivsel kaardil, mis renderdatakse [Bing Maps V8 Web Controli](https://docs.microsoft.com/bingmaps/v8-web-control/) abil. Vajalik on Bing Maps kaartide API võti ja see tuleb lisada jagatud parameetrite lehele rakenduses Commerce peakontorid. Kaardimoodulid pakuvad erinevaid vaateid, nagu tee-, ülalt- ja tänavavaade, mida kasutajad saavad valida, et vaadata kaardil asukohti. Need võimaldavad ka toiminguid, nagu suumimine ja kasutaja asukoha kasutamine.

Kaardimoodul töötab koos kaupluse valija mooduliga, et määrata kaupluste geograafilised asukohad, mis tuleb kaardil renderdada. Kaupluse valija ja kaardimoodul teevad koostööd, kui kasutaja valib saidilehel kaupluse ühes nendest moodulitest. Kaardimooduleid saab kasutada ka teiste stsenaariumide puhul, mis ei ole seotud kaupluse valija moodulitega koos töötamisega. Kuid selleks tuleb moodulit kohandada.

Kaardimoodul võeti kasutusele Commerce'i versioonis 10.0.13.

Järgmisel pildil on näide kaardimoodulist, mida kasutatakse kaupluste asukohtade lehel.

![Kaupluse valija mooduli näide](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a>Mooduli atribuudid

| Atribuudi nimi             | Väärtus                 | Kirjeldus |
|---------------------------|-----------------------|-------------|
| Pealkiri | Tekst | Mooduli pealkiri. |
| Rõhknaela suvandid: vaikeikoon | Pilt | Rõhknaelasümboli pilt, mida kasutatakse kaardil kuvatud kaupluste puhul. |
| Rõhknaela suvandid: aktiivse üksuse ikoon | Pilt | Rõhknaelasümboli pilt, mida kasutatakse kaardil valitud kaupluse puhul. |
| Rõhknaela suvandid: ikooni vaikevärv | Tähemärkide string | Kaardil olevate rõhknaelasümbolite värvi tekstiline või kuueteistkümnendsüsteemis väärtus. |
| Rõhknaela suvandid: aktiivse üksuse ikooni värv | Tähemärkide string | Kaardil valitud rõhknaelasümbolite värvi tekstiline või kuueteistkümnendsüsteemis väärtus. |
| Näita indeksit | **Tõene** või **Väär** | Kui selle atribuudi väärtuseks on seatud **Tõene**, näitavad kõik kauplust tähistavad rõhknaelasümbolid indeksit. See indeks ühtib indeksiga loendivaates, mida kaupluse valija moodul näitab. |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a>Lubatud vastendamis-URL-ide lisamine saidi sisu turbepoliitika direktiividele

Et kaardimoodul saaks suhelda Bingi kaartidega, peate tagama, et teie saidi sisu turbepoliitikas (CSP) oleksid lubatud järgmised vastendamise URL-id (tuntud ka kui valgesse nimekirja lisamine). Seadistus toimub Commerce'i saidiehitajas, lisades lubatud URL-id erinevatele saidi CSP-direktiividele (nt **img-src**). Lisateavet leiate teemast [Sisu turbepoliitika](manage-csp.md). 

- Lisage direktiivile **connect-src** väärtus **&#42;.bing.com**.
- Lisage direktiivile **img-src** väärtus **&#42;.virtualearth.net**.
- Lisage direktiivile **script-src** väärtus **&#42;.bing.com, &#42;.virtualearth.net**.
- Lisage direktiivile **script style-src** väärtus **&#42;.bing.com**.

## <a name="add-a-map-module-to-a-page"></a>Lehele kaardimooduli lisamine

Üksikasjalikku teavet kaardimooduli lehel konfigureerimise kohta leiate teemast [Kaupluse valija moodul](store-selector.md). 
 
## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Ostukasti moodul](add-buy-box.md)

[Ostukorvimoodul](add-cart-module.md)

[Kaupluse valimise moodul](store-selector.md)

[Organisatsiooni Bingi kaartide haldamine](./dev-itpro/manage-bing-maps.md)

[Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/)