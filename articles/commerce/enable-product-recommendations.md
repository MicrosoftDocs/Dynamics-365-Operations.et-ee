---
title: Tootesoovituste lubamine
description: Selles teemas selgitatakse, kuidas teha tehisintellekti masinõppel (AI-ML) põhinevad tootesoovitused rakenduses Microsoft Dynamics 365 Commerce klientidele kättesaadavaks.
author: bebeale
manager: AnnBe
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 59c83409ede5e006ddf030d396934eeb6cd8df76
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010120"
---
# <a name="enable-product-recommendations"></a>Tootesoovituste lubamine

[!include [banner](includes/banner.md)]

Selles teemas selgitatakse, kuidas teha tehisintellekti masinõppel (AI-ML) põhinevad tootesoovitused rakenduses Microsoft Dynamics 365 Commerce klientidele kättesaadavaks. Lisateavet tootesoovituste funktsioonide kohta leiate jaotisest [Ülevaade tootesoovitustest](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Tootesoovituste eelkontroll

Enne lubamist võtke arvesse, et tootesoovitusi toetatakse ainult Commerce'i klientide jaoks, kes on migreerinud salvestusruumi kasutama rakenduses Azure Data Lake Storage. 

Enne soovituste lubamist tuleb kontoris lubada järgmised konfiguratsioonid:

1. Veenduge, et Azure Data Lake Storage oleks ostetud ja keskkonnas edukalt kontrollitud. Lisateabe saamiseks vt [Veenduge, et Azure Data Lake Storage oleks ostetud ja keskkonnas edukalt kontrollitud](enable-ADLS-environment.md).
2. Veenduge, et üksuse kaupluse värskendamine oleks automatiseeritud. Lisateabe saamiseks vt [Veenduge, et üksuse kaupluse värskendamine oleks automatiseeritud](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).
3. Kinnitage, et Azure AD identiteedi konfiguratsioon sisaldab kirjet üksuse Soovitused jaoks. Lisateavet selle tegevuse kohta leiate altpoolt.

Lisaks veenduge, et RetailSale’i mõõtmised oleksid lubatud. Selle seadistamisprotsessi kohta lisateabe saamiseks vt [Mõõtudega töötamine](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).

## <a name="azure-ad-identity-configuration"></a>Azure AD identiteedi konfiguratsioon

See etapp on nõutav kõigil klientidel, kes kasutavad konfiguratsiooni infrastruktuur teenusena (IaaS). Klientide, kes kasutavad service fabricut (SF), peaks see etapp olema automaatne ja soovitame kinnitada, et see säte konfigureeritakse ootuspäraselt.

### <a name="setup"></a>Häälestus

1. Otsige kontorist lehte **Azure Active Directory rakendused**.
2. Kontrollige, kas üksusel „RecommendationSystemApplication-1” on olemas kanne.

Kui kannet pole olemas, lisage uus kanne järgmise teabega.

- **Kliendi ID** – d37b07e8-dd1c-4514-835d-8b918e6f9727
- **Nimi** – RecommendationSystemApplication-1
- **Kasutaja ID** – RetailServiceAccount

Salvestage ja sulgege leht. 

## <a name="turn-on-recommendations"></a>Soovituste sisselülitamine

Tootesoovituste sisselülitamiseks tehke järgmist.

1. Commerce'i peakontorist otsige valikut **Funktsioonihaldus**.
1. Saadaolevate funktsioonide vaatamiseks valige **Kõik**. 
1. Sisestage otsinguväljale **Soovitused**.
1. Valige funktsioon **Tootesoovitused**.
1. Tehke atribuutide paanil **Tootesoovitused** valik **Luba kohe**.

![Soovituste sisselülitamine](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> See protseduur käivitab tootesoovituste loendite loomise protsessi. Enne loenditele juurdepääsu ja nende kuvamist kassas või rakenduses Dynamics 365 Commerce, võib kuluda mitu tundi.

## <a name="configure-recommendation-list-parameters"></a>Soovituste loendi parameetrite konfigureerimine

Vaikimisi pakub AI-ML-i põhine tootesoovituste loend soovitatavaid väärtusi. Saate vaikimisi soovitatud väärtusi muuta, et need vastaksid teie ettevõtte vooga. Lisateavet vaikimisi parameetrite muutmise kohta leiate teemast [AI-ML-põhiste tootesoovituse tulemuste haldamine](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>Kassaseadmetes soovituste kuvamine

Pärast soovituste lubamist kaubanduse kontoris, tuleb soovituste paneel lisada paigutuse tööriista kaudu juhtelemendi kassaekraanile. Selle protsessi kohta lisateabe saamiseks vt taamat [Soovituste juhtelemendi lisamine kassaseadmete kandeekraanile](add-recommendations-control-pos-screen.md). 

## <a name="enable-personalized-recommendations"></a>Isikupärastatud soovituste lubamine

Rakenduses Dynamics 365 Commerce saavad jaemüüjad teha kättesaadavaks isikupärastatud tootesoovitused (tuntud ka kui isikupärastamine). Sel viisil saab isikupärastatud soovitusi lisada kliendi kasutuskogemusele veebis ja kassas. Kui isikupärastamise funktsioon on sisse lülitatud, saab süsteem seostada kasutaja ostu- ja tooteteabe individualiseeritud tootesoovituste loomiseks.

Lisateavet isikupärastatud soovituste kohta vaadake jaotisest [Isikupärastatud soovituste lubamine](personalized-recommendations.md).

## <a name="additional-resources"></a>Lisaressursid

[Tootesoovituste ülevaade](product-recommendations.md)

[ Azure Data Lake Storage'i lubamine Dynamics 365 Commerce'i keskkonnas](enable-adls-environment.md)

[Isikupärastatud soovituste lubamine](personalized-recommendations.md)

[„Sarnaste toodete vaatamise” soovituste lubamine](shop-similar-looks.md)

[Isikupärastatud tootesoovitustest loobumine](personalization-gdpr.md)

[Tootesoovituste lisamine kassas](product.md)

[Soovituste lisamine kandeekraanile](add-recommendations-control-pos-screen.md)

[AI-ML-i soovituste tulemuste kohandamine](modify-product-recommendation-results.md)

[Loo kuraatorite soovitused käsitsi](create-editorial-recommendation-lists.md)

[Soovituste loomine demoandmetega](product-recommendations-demo-data.md)

[Tootesoovituste KKK](faq-recommendations.md)

