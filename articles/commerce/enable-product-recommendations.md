---
title: Tootesoovituste lubamine
description: Selles teemas selgitatakse, kuidas teha tehisintellekti masinõppel (AI-ML) põhinevad tootesoovitused rakenduses Microsoft Dynamics 365 Commerce klientidele kättesaadavaks.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2d3f1bc2526eeacb4bd6338a0679eadd95a75989
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024952"
---
# <a name="enable-product-recommendations"></a>Tootesoovituste lubamine

[!include [banner](includes/banner.md)]

Selles teemas selgitatakse, kuidas teha tehisintellekti masinõppel (AI-ML) põhinevad tootesoovitused rakenduses Microsoft Dynamics 365 Commerce klientidele kättesaadavaks. Lisateavet tootesoovituste funktsioonide kohta leiate jaotisest [Ülevaade tootesoovitustest](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Tootesoovituste eelkontroll

Enne lubamist võtke arvesse, et tootesoovitusi toetatakse ainult kaubanduse klientide jaoks, kes on migreerinud salvestusruumi kasutama rakendust Azure Data Lake Storage (ADLS). 

ADLS lubamise juhiste saamiseks vaadake teemat [Kuidas lubada ADLS Dynamics 365 keskkonnas](enable-ADLS-environment.md).

Lisaks veenduge, et RetailSale’i mõõtmised oleksid lubatud. Selle seadistusprotsessi kohta lisateabe saamiseks minge [siia.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)


## <a name="turn-on-recommendations"></a>Soovituste sisselülitamine

Tootesoovituste sisselülitamiseks tehke järgmist.

1. Avage **Jaemüük ja kaubandus &gt; Tootesoovitused &gt; Soovituste parameetrid**.
1. Jagatud parameetrite loendis valige suvand **Soovituste loendid**.
1. Määrake suvand **Luba soovitused** valikule **Jah**.

![tootesoovituste lubamine](./media/enableproductrecommendations.png)

> [!NOTE]
> See protseduur käivitab tootesoovituste loendite loomise protsessi. Enne loenditele juurdepääsu ja nende nägemist kassas või rakenduses Dynamics 365 Commerce, võib kuluda mitu tundi.

## <a name="configure-recommendation-list-parameters"></a>Soovituste loendi parameetrite konfigureerimine

Vaikimisi pakub AI-ML-i põhine tootesoovituste loend soovitatavaid väärtusi. Saate vaikimisi soovitatud väärtusi muuta, et need vastaksid teie ettevõtte vooga. Lisateavet vaikimisi parameetrite muutmise kohta leiate teemast [AI-ML-põhiste tootesoovituse tulemuste haldamine](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>Kassaseadmetes soovituste kuvamine

Pärast soovituste lubamist kaubanduse kontoris, tuleb soovituste paneel lisada paigutuse tööriista kaudu juhtelemendi kassaekraanile. Selle protsessi kohta lisateabe saamiseks vt taamat [Soovituste juhtelemendi lisamine kassaseadmete kandeekraanile](add-recommendations-control-pos-screen.md). 

## <a name="enable-personalized-recommendations"></a>Luba isikupärastatud soovitused

Lisateavet isikupärastatud soovituste saamise kohta vaadake jaotisest [Isikupärastatud soovituste lubamine](personalized-recommendations.md).

## <a name="additional-resources"></a>Lisaressursid

[Tootesoovituste ülevaade](product-recommendations.md)

[Luba isikupärastatud soovitused](personalized-recommendations.md)

[Tootesoovituste loendite lisamine lehtedele](add-reco-list-to-page.md)

[Kassaseadmetele soovituste paneeli lisamine](add-recommendations-control-pos-screen.md)

[Tootekogumi mooduli ülevaade](product-collection-module-overview.md)

[ADLS lubamine Dynamics 365 keskkonnas](enable-ADLS-environment.md)

