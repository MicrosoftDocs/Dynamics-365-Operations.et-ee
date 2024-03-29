---
title: Kaardimoodul
description: See artikkel käsitleb kaardimoodulite kaardistamist ja kirjeldab nende konfigureerimist moodulis Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: d72091baf2f216bfbe33950950f8917c3ba1ba5c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283342"
---
# <a name="map-module"></a>Kaardimoodul

[!include [banner](includes/banner.md)]


See artikkel käsitleb kaardimoodulite kaardistamist ja kirjeldab nende konfigureerimist moodulis Microsoft Dynamics 365 Commerce.

Kaardimoodul kuvab kaupluste asukohad interaktiivsel kaardil, mis renderdatakse [Bing Maps V8 Web Controli](/bingmaps/v8-web-control/) abil. Vajalik on Bing Maps kaartide API võti ja see tuleb lisada jagatud parameetrite lehele rakenduses Commerce peakontorid. Kaardimoodulid pakuvad erinevaid vaateid, nagu tee-, ülalt- ja tänavavaade, mida kasutajad saavad valida, et vaadata kaardil asukohti. Need võimaldavad ka toiminguid, nagu suumimine ja kasutaja asukoha kasutamine.

Kaardimoodul töötab koos kaupluse valija mooduliga, et määrata kaupluste geograafilised asukohad, mis tuleb kaardil renderdada. Kaupluse valija ja kaardimoodul teevad koostööd, kui kasutaja valib saidilehel kaupluse ühes nendest moodulitest. Kaardimooduleid saab kasutada ka teiste stsenaariumide puhul, mis ei ole seotud kaupluse valija moodulitega koos töötamisega. Kuid selleks tuleb moodulit kohandada.

> [!NOTE]
> Kaardimoodul on saadaval rakenduse Dynamics 365 Commerce väljalaskes 10.0.13.

Järgmisel pildil on näide kaardimoodulist, mida kasutatakse kaupluste asukohtade lehel.

![Kaupluse valija mooduli näide.](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a>Mooduli atribuudid

| Atribuudi nimi             | Väärtus                 | Kirjeldus |
|---------------------------|-----------------------|-------------|
| Päis | Tekst | Mooduli pealkiri. |
| Rõhknaela suvandid: vaikeikoon | Pilt | Rõhknaelasümboli pilt, mida kasutatakse kaardil kuvatud kaupluste puhul. |
| Rõhknaela suvandid: aktiivse üksuse ikoon | Pilt | Rõhknaelasümboli pilt, mida kasutatakse kaardil valitud kaupluse puhul. |
| Rõhknaela suvandid: ikooni vaikevärv | Tähemärkide string | Kaardil olevate rõhknaelasümbolite värvi tekstiline või kuueteistkümnendsüsteemis väärtus. |
| Rõhknaela suvandid: aktiivse üksuse ikooni värv | Tähemärkide string | Kaardil valitud rõhknaelasümbolite värvi tekstiline või kuueteistkümnendsüsteemis väärtus. |
| Näita indeksit | **Tõene** või **Väär** | Kui selle atribuudi väärtuseks on seatud **Tõene**, näitavad kõik kauplust tähistavad rõhknaelasümbolid indeksit. See indeks ühtib indeksiga loendivaates, mida kaupluse valija moodul näitab. |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a>Lubatud vastendamis-URL-ide lisamine saidi sisu turbepoliitika direktiividele

Et kaardimoodul saaks suhelda Bingi kaartidega, peate tagama, et teie saidi sisu turbepoliitikas (CSP) oleksid lubatud järgmised vastendamise URL-id. Seadistus toimub Commerce'i saidiehitajas, lisades lubatud URL-id erinevatele saidi CSP-direktiividele (nt **img-src**). Lisateavet leiate teemast [Sisu turbepoliitika](manage-csp.md). 

- Lisage direktiivile **connect-src** väärtus **&#42;.bing.com**.
- Lisage direktiivile **img-src** väärtus **&#42;.virtualearth.net**.
- Lisage direktiivile **script-src** väärtus **&#42;.bing.com, &#42;.virtualearth.net**.
- Lisage direktiivile **script style-src** väärtus **&#42;.bing.com**.

## <a name="add-a-map-module-to-a-page"></a>Lehele kaardimooduli lisamine

Üksikasjalikku teavet kaardimooduli lehel konfigureerimise kohta leiate teemast [Kaupluse valija moodul](store-selector.md). 
 
## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Ostukastimoodul](add-buy-box.md)

[Ostukorvimoodul](add-cart-module.md)

[Kaupluse valimise moodul](store-selector.md)

[Organisatsiooni Bingi kaartide haldamine](./dev-itpro/manage-bing-maps.md)

[Bing Maps V8 Web Control](/bingmaps/v8-web-control/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
