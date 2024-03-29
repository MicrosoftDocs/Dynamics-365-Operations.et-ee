---
title: Luba tootesoovitused
description: See artikkel selgitab, kuidas teha klientidele kättesaadavaks microsofti teabel põhinevad tootesoovitused (AI-ARVUTI Microsoft Dynamics 365 Commerce).
author: bebeale
ms.date: 09/08/2022
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: fc1b43fa70e6652d38b1141e2d93cf323f70a756
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460017"
---
# <a name="enable-product-recommendations"></a>Luba tootesoovitused

[!include [banner](includes/banner.md)]

See artikkel selgitab, kuidas teha klientidele kättesaadavaks microsofti teabel põhinevad tootesoovitused (AI-ARVUTI Microsoft Dynamics 365 Commerce). Lisateavet tootesoovituste funktsioonide kohta leiate jaotisest [Ülevaade tootesoovitustest](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Tootesoovituste eelkontroll

1. Veenduge, et teil on kehtiv Dynamics 365 Commerce soovituste litsents.
1. Veenduge, et üksuse kauplus on ühendatud kliendi-omase Azure Data Lake Storage Gen2 kontoga. Lisateabe saamiseks vt [Veenduge, et Azure Data Lake Storage oleks ostetud ja keskkonnas edukalt kontrollitud](enable-ADLS-environment.md).
1. Kinnitage, et Azure AD identiteedi konfiguratsioon sisaldab kirjet üksuse Soovitused jaoks. Lisateavet selle tegevuse kohta leiate altpoolt.
1. Veenduge, et üksuse kaupluse päevane värskendus Azure Data Lake Storage Gen2-sse on plaanitud. Lisateabe saamiseks vt [Veenduge, et üksuse kaupluse värskendamine oleks automatiseeritud](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).
1. Luba üksuselao RetailSale'i mõõtmised. Selle seadistamisprotsessi kohta lisateabe saamiseks vt [Mõõtudega töötamine](/dynamics365/ai/customer-insights/pm-measures).
1. Veenduge, et teie keskkond on konfigureerinud kättesaavad ja toetatud regioonid praegu toetatud regioonides järgmiselt:

    - **Toetatud regioonid:** EL/US/CA/AU.
    - **Toetatud regioonid:** US/CA/AU. Kui teenimispiirkond ei vasta ühele olemasolevatest toetatud regioonidest, valib soovituste teenus kõige lähema toetatud teeninduspiirkonna.

Pärast ülaltoodud sammude täitmist olete soovituste lubamiseks valmis.

> [!NOTE]
> On teada probleem, mille puhul soovitused ei ilmu pärast järgmiste sammude lõpuleviimist. Selle probleemi põhjuseks on andmevoo probleemid keskkonnas. Kui teie keskkonnas ei näidata soovitamise tulemusi, [konfigureerige soovituste teenuse alternatiivsed andmed, järgides soovituste jaoks alternatiivse andmevoo häälestamise samme](set-up-alternate-data-flow.md). Teil peavad nende sammude lõpuleviimiseks olema Azure’i administraatori õigused. Kui vajate abi, võtke ühendust oma FastTracki esindajaga.

## <a name="azure-ad-identity-configuration"></a>Azure AD identiteedi konfiguratsioon

See samm on vajalik ainult klientidele, kes käitavad infrastruktuuri teenusena (IaaS) konfiguratsioonina. Azure AD Identiteedi konfiguratsioon on automaatne klientide puhul, kes töös Azure Service Fabric jooksevad, kuid soovitame kontrollida, et säte on konfigureeritud nii, nagu oodatud.

### <a name="setup"></a>Häälestus

1. Otsige rakendusest Commerce headquarters **Azure Active Directory rakenduste** lehte.
1. Kontrollige, kas üksusel **SoovitusSüsteemRakendus-1** on olemas kanne. Kui kirjet pole olemas, looge see, kasutades järgmist teavet:

    - **Kliendi ID**: d37b07e8-dd1c-4514-835d-8b918e6f9727
    - **Nimi**: RecommendationSystemApplication-1
    - **Kasutaja ID**: RetailServiceAccount

1. Salvestage ja sulgege leht. 

## <a name="turn-on-recommendations"></a>Soovituste sisselülitamine

Tootesoovituste sisselülitamiseks tehke järgmist.

1. Commerce'i peakontorist otsige valikut **Funktsioonihaldus**.
1. Saadaolevate funktsioonide vaatamiseks valige **Kõik**. 
1. Sisestage otsinguväljale **Soovitused**.
1. Valige funktsioon **Tootesoovitused**.
1. Tehke atribuutide paanil **Tootesoovitused** valik **Luba kohe**.

![Soovituste sisselülitamine.](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> - Ülaltoodud protseduur käivitab tootesoovituste loendite loomise protsessi. Enne loenditele juurdepääsu ja nende kuvamist kassas või rakenduses Dynamics 365 Commerce, võib kuluda mitu tundi.
> - See konfiguratsioon ei luba kõiki soovituste funktsioone. Täpsemaid funktsioone, nagu isikupärastatud soovitused, "kaupluste sarnane välja näeb" ja "ostu sarnane kirjeldus" juhitakse sihtotstarbelise funktsioonihalduse kirjetega. Lisateavet nende funktsioonide lubamise kohta Commerce headquartersis vt [Luba isikupärastatud soovitused](personalized-recommendations.md), [Luba soovitused "kaupluste sarnane"](shop-similar-looks.md) ja [luba "shop similar description" soovitused](shop-similar-description.md).

## <a name="configure-recommendation-list-parameters"></a>Soovituste loendi parameetrite konfigureerimine

Vaikimisi pakub AI-ML-i põhine tootesoovituste loend soovitatavaid väärtusi. Saate vaikimisi soovitatud väärtusi muuta, et need vastaksid teie ettevõtte vooga. Lisateavet vaikimisi parameetrite muutmise kohta leiate teemast [AI-ML-põhiste tootesoovituse tulemuste haldamine](modify-product-recommendation-results.md).

## <a name="include-recommendations-in-e-commerce-experiences"></a>Soovituste kaasamine e-ärikogemustest

Pärast soovituste lubamist Commerce Headquartersis on Commerce moodulite kuvamiseks kasutatavad ärimoodulid konfigureerimiseks valmis. Lisateavet vt teemast [Toote kogumismoodulid](product-collection-module-overview.md).

## <a name="show-recommendations-on-pos-devices"></a>Kassaseadmetes soovituste kuvamine

Pärast soovituste lubamist Commerce peakorteris, tuleb soovituste paneel lisada paigutuse tööriista kaudu juhtelemendi kassaekraanile. Selle protsessi kohta lisateabe saamiseks vt taamat [Soovituste juhtelemendi lisamine kassaseadmete kandeekraanile](add-recommendations-control-pos-screen.md). 

## <a name="enable-personalized-recommendations"></a>Isikupärastatud soovituste lubamine

Rakenduses Dynamics 365 Commerce saavad jaemüüjad teha kättesaadavaks isikupärastatud tootesoovitused (tuntud ka kui isikupärastamine). Sel viisil saab isikupärastatud soovitusi lisada kliendi kasutuskogemusele veebis ja kassas. Kui isikupärastamise funktsioon on sisse lülitatud, saab süsteem seostada kasutaja ostu- ja tooteteabe individualiseeritud tootesoovituste loomiseks.

Lisateavet isikupärastatud soovituste kohta vaadake jaotisest [Isikupärastatud soovituste lubamine](personalized-recommendations.md).

## <a name="additional-resources"></a>Lisaressursid

[Tootesoovituste ülevaade](product-recommendations.md)

[Azure Data Lake Storage'i lubamine Dynamics 365 Commerce'i keskkonnas](enable-adls-environment.md)

[Soovituste alternatiivse andmevoo häälestamine](set-up-alternate-data-flow.md)

[Luba isikupärastatud soovitused](personalized-recommendations.md)

[Luba "osta sarnaseid" soovitused](shop-similar-looks.md)

[Isikupärastatud tootesoovitustest loobumine](personalization-gdpr.md)

[Tootesoovituste lisamine kassas](product.md)

[Soovituste lisamine kandeekraanile](add-recommendations-control-pos-screen.md)

[AI-ML-i soovituste tulemuste kohandamine](modify-product-recommendation-results.md)

[Loo kuraatorite soovitused käsitsi](create-editorial-recommendation-lists.md)

[Soovituste loomine demoandmetega](product-recommendations-demo-data.md)

[Tootesoovituste KKK](faq-recommendations.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
