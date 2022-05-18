---
title: Luba "osta sarnase kirjeldusega" soovitused
description: Selles teemas kirjeldatakse, kuidas lubada „osta sarnase kirjeldusega” tootesoovitused rakenduses Microsoft Dynamics 365 Commerce.
author: bsokolov
ms.date: 01/13/2021
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
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 733b21870f9dd7ffa42fce3bccf669a59d633b14
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690999"
---
# <a name="enable-shop-similar-description-recommendations"></a>Luba "osta sarnaseid kirjeldusi" soovitused

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas lubada „osta sarnase kirjeldusega” tootesoovitused rakenduses Microsoft Dynamics 365 Commerce.

Rakenduse Dynamics 365 Commerce soovituste funktsioon „osta sarnase kirjeldusega” kasutab tehisintellekti ja masinõpet (AI-ML), et pakkuda klientidele sarnaste kirjeldustega tooteid, nagu need, mida klient otsib. Tehes „osta sarnaste kirjeldustega” soovitused kõigis Commerce'i jaemüügikanalites kättesaadavaks, saavad jaemüüjad aidata klientidel lihtsamini leida seda, mida nad soovivad.

„Osta sarnase kirjeldusega” funktsionaalsuse soovituse kasutavad toote nime ja kirjeldust, et leida ja soovitada sarnaseid tooteid jaemüüja tootekataloogist.

„Osta sarnase kirjeldusega” soovitused on saadaval nii kassas (POS) kui ka e-kaubanduse kogemustes.

## <a name="example-scenarios"></a>Näidisstsenaariumid

Järgmine näitestsenaarium näitab soovituste tüüpe, mida funktsiooniga "osta sarnase kirjeldusega" saab pakkuda.

- Klient vaatab retrostiilis sarvraamidega prille ja saab jaemüüja tööstusharude kontekstis teiste prillide soovitusi, millel on sarnane disain.
- Klient kasutab soovitust "osta sarnase kirjeldusega", et avastada kohvimaitseid, mis on sarnased varem sellelt jaemüüjalt ostetud maitsele.

## <a name="set-up-shop-similar-description-recommendations"></a>Soovituste "osta sarnase kirjeldusega" seadistamine

Tootesoovitusi toetatakse ainult Commerce'i klientide puhul, kes on hakanud kasutama Azure Data Lake Storage Gen2 salvestusruumi.

### <a name="prerequisites"></a>Eeltingimused

Enne soovituste "osta sarnase kirjeldusega" kuvamist klientidele peate täitma järgmised eeltingimused.

- [Tootesoovituste lubamine](enable-product-recommendations.md) Commerce'i peakontoris.
- Veenduge, et meediaserver toetaks HTTPS-i kutseid.

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a>Soovituste "osta sarnase kirjeldusega" funktsiooni sisselülitamine

„Osta sarnase kirjeldusega” soovituste funktsiooni lubamiseks Commerce'i peakontoris toimige järgmiselt.

1. Otsige ja valige tööruumi **Funktsioonihaldus** saadaolevate funktsioonide loendist **Osta sarnase kirjeldusega**.
1. Valige parempoolselt paanilt **Luba**.

> [!NOTE]
> Kui lülitate funktsiooni sisse, hakkab süsteem looma tootesoovituste loendeid. Kuluda võib kuni üks päev enne, kui need loendid on saadaval ja nähtavad veebis ning kassaterminalides.
>
> Kui lülitate selle funktsiooni välja, siis teist tüüpi tootesoovitusi see ei mõjutata. Lisateavet tootesoovituste kohta leiate teemast [Tootesoovituste ülevaade](product-recommendations.md).

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a>Nupu Osta sarnase kirjeldusega lisamine toote üksikasjade lehtedele

Pärast „Osta sarnase kirjeldusega” soovituste funktsiooni lubamist Commerce'i peakontoris saate mistahes toote üksikasjade lehele (DPD) lisada nupu **Osta sarnase kirjeldusega**. Klient, kes valib selle nupu, viiakse spetsiaalsele **Osta sarnase kirjeldusega** lehele, millel näidatakse visuaalselt sarnaseid tooteid. Seal saab klient toodete edasiseks filtreerimiseks kasutada suvandeid.

Et lisada nupp **Osta sarnase kirjeldusega** toote üksikasjade lehele Commerce'i saidiehitaja abil toimige järgmiselt.

1. Avage olemasolev saidiehitaja leht, mis sisaldab ostukastimoodulit.
1. Valige vasakpoolsel navigeerimispaanil ostukastimoodul.
1. Valige parempoolsel navigeerimispaanil märkeruut **Luba link Osta sarnase kirjeldusega**.
1. Valige käsk **Salvesta**.
1. Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**. Pärast lehe avaldamist on PDP-l nupp **Osta sarnase kirjeldusega**.

Järgmisel illustratsioonil on näha saidiehitajas toodete üksikasjade näidislehel märkeruut **Luba link Osta sarnase kirjeldusega** ja nupp **Osta sarnase kirjeldusega**.

![Luba DPD saidiehitajas link Osta sarnase kirjeldusega ja nupp Osta sarnase kirjeldusega.](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a>Lisaressursid

[Tootesoovituste ülevaade](product-recommendations.md)

[ Azure Data Lake Storage'i lubamine Dynamics 365 Commerce'i keskkonnas](enable-adls-environment.md)

[Luba tootesoovitused](enable-product-recommendations.md)

[Luba "osta sarnaseid" soovitused](shop-similar-looks.md)

[AI-ML-i soovituste tulemuste kohandamine](modify-product-recommendation-results.md)

[Loo kuraatorite soovitused käsitsi](create-editorial-recommendation-lists.md)

[Tootesoovituste KKK](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]