---
title: „Sarnaste toodete vaatamise” soovituste lubamine
description: Selles teemas kirjeldatakse, kuidas lubada „sarnaste toodete vaatamise” tootesoovitused rakenduses Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 2e57965a1073982a7b6c34b79dbf6e5b90d7ee30
ms.sourcegitcommit: 15c68822f4d412bfc609be31b3702f18c81ea0bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2020
ms.locfileid: "3666304"
---
# <a name="enable-shop-similar-looks-recommendations"></a>„Sarnaste toodete vaatamise” soovituste lubamine

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Selles teemas kirjeldatakse, kuidas lubada „sarnaste toodete vaatamise” tootesoovitused rakenduses Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Ülevaade

Rakenduse Dynamics 365 Commerce soovituste funktsioon „sarnaste toodete vaatamine” kasutab tehisintellekti ja masinõpet (AI-ML), et pakkuda klientidele visuaalselt sarnaste toodete soovitusi. Tehes „sarnaste toodete vaatamise” soovitused kõigis Commerce'i jaemüügikanalites kättesaadavaks, saavad jaemüüjad klientide rahulolu suurendada, aidates klientidel leida lihtsamini, mida nad tahavad.

„Sarnaste toodete vaatamise” soovituste funktsioon kasutab alustootevariante, et leida ja soovitada jaemüüja tootekataloogis visuaalselt sarnaseid tooteid. 

„Sarnaste toodete vaatamise” soovitused on saadaval nii kassas (POS) kui ka e-kaubanduses.

### <a name="example-scenarios"></a>Näidisstsenaariumid

- Klient vaatab musta triibulist kampsunit ja talle soovitatakse sarnast punast kampsunit. Klient valib algselt vaadatud toote asemel soovitatud toote ja seejärel soovitatakse talle sarnaseid punast värvi tooteid. 
- Klient kasutab „sarnaste toodete vaatamise” soovitusi, et avastada kõrvarõngad, mis sobivad sõrmusega, mille ostmisest on klient huvitatud.

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a>„Sarnaste toodete vaatamise” soovituste lubamine Commerce'i peakontoris

Tootesoovitusi toetatakse ainult Commerce'i klientide puhul, kes on hakanud kasutama Azure Data Lake Gen2 salvestusruumi.

### <a name="prerequisites"></a>Eeltingimused

Enne kui jaemüüjad saavad hakata näitama klientidele „sarnaste toodete vaatamise” soovitusi, tuleb täita kaks eeltingimust.

- [Tootesoovituste lubamine](enable-product-recommendations.md) Commerce'i peakontoris.
- Veenduge, et meediaserver toetaks HTTPS-i kutseid.

Et soovitusmootor pääseks juurde tootepiltidele, peavad jaemüüjad looma toote URL-id. Commerce'i peakontoris toote URL-ide loomiseks toimige järgmiselt.

1. Avage **Tootepildid**.
1. Valige toimingupaanil **Meediumimalli määratlemine**.
1. Valige atribuutide paanil**Meediumimalli määratlemine** jaotisest **Meediumide URL-id** suvand **Loo URL-id**.

> [!NOTE]
> Kui lubate „sarnaste toodete vaatamise” soovituste funktsiooni, algab tootesoovituste loendite loomise protsess. Kuluda võib kuni üks päev enne, kui need loendid on saadaval ja nähtavad veebis ning kassaterminalides.

„Sarnaste toodete vaatamise” soovituste funktsiooni lubamiseks Commerce'i peakontoris toimige järgmiselt.

1. Avage **Funktsioonihaldus**.
1. Leidke üles ja valige saadaolevate funktsioonide loendist suvand **Sarnaste toodete vaatamine**.
1. Valige parempoolsel paanil **Luba**, et teenus sisse lülitada.

Järgmisel illustratsioonil on näha funktsioon **Sarnaste toodete vaatamine** Commerce'i peakontori lehel **Funktsioonihaldus**.

![Sarnaste toodete vaatamise funktsioon Commerce'i peakontori funktsioonihalduse lehel](./media/enableshopsimilarlooks.png)

Kui eelmised ülesanded on lõpule viidud, täiendatakse kassaterminale automaatselt kontekstilise paneeliga **Sarnaste toodete ostmine**. Valides suvandi **Vaata lisa**, saavad kassaterminali kasutajaid avada spetsiaalse „sarnaste toodete vaatamise” lehe, mida saab veelgi filtreerida.

> [!NOTE]
> Kui lülitate „sarnaste toodete vaatamise” soovituste funktsiooni välja, ei mõjutata muid tootesoovituste tüüpe. Lisateavet tootesoovituste kohta leiate teemast [Tootesoovituste ülevaade](product-recommendations.md).

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a>Sarnaste toodete vaatamise nupu lisamine toote üksikasjade lehele Commerce'i saidiehitaja abil

Pärast „sarnaste toodete vaatamise” soovituste funktsiooni lubamist Commerce'i peakontoris saavad jaemüüjad lisada Commerce'i saidiehitaja suvandi abil nupu **Vaata sarnaseid tooteid** mis tahes toote üksikasjade lehel (PDP) olevasse ostkasti. Klient, kes valib selle nupu, viiakse spetsiaalsele „sarnaste toodete vaatamise” lehele, millel näidatakse visuaalselt sarnaseid tooteid. Seal saab klient toodete edasiseks filtreerimiseks kasutada suvandeid.

Et lisada nupp **Vaata sarnaseid tooteid** toote üksikasjade lehele Commerce'i saidiehitaja abil toimige järgmiselt.

1. Avage olemasolev saidiehitaja leht, mis sisaldab ostukastimoodulit.
1. Valige vasakpoolsel navigeerimispaanil ostukastimoodul.
1. Valige parempoolsel navigeerimispaanil märkeruut **Luba sarnaste toodete vaatamise link**.
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**. Pärast lehe avaldamist on PDP-l nupp **Vaata sarnaseid tooteid**.

Järgmisel illustratsioonil on näha saidiehitajas toodete üksikasjade näidislehel märkeruut **Luba sarnaste toodete vaatamise link** ja nupp **Vaata sarnaseid tooteid**.

![Saidiehitajas toote üksikasjade lehel olev märkeruut „Luba sarnaste toodete vaatamise link” ja nupp „Vaata sarnaseid tooteid”](./media/SSLecomtooling.png)

## <a name="additional-resources"></a>Lisaressursid

[Tootesoovituste ülevaade](product-recommendations.md)

[ Azure Data Lake Storage'i lubamine Dynamics 365 Commerce'i keskkonnas](enable-adls-environment.md)

[Luba tootesoovitused](enable-product-recommendations.md)

[Isikupärastatud tootesoovitustest loobumine](personalization-gdpr.md)

[Tootesoovituste lisamine kassas](product.md)

[Soovituste lisamine kandeekraanile](add-recommendations-control-pos-screen.md)

[AI-ML-i soovituste tulemuste kohandamine](modify-product-recommendation-results.md)

[Loo kuraatorite soovitused käsitsi](create-editorial-recommendation-lists.md)

[Soovituste loomine demoandmetega](product-recommendations-demo-data.md)

[Tootesoovituste KKK](faq-recommendations.md)