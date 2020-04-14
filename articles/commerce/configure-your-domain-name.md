---
title: Domeeninime konfigureerimine
description: Selles teemas selgitatakse, kuidas konfigureerida rakenduse Microsoft Dynamics 365 e-kaubanduse saidi domeeni nime.
author: psimolin
manager: AnnBe
ms.date: 03/02/2020
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
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2ad9ca3aee21301ef6d830d7b29982a45cd53f60
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096816"
---
# <a name="configure-your-domain-name"></a>Domeeninime konfigureerimine


[!include [banner](includes/banner.md)]

Selles teemas selgitatakse, kuidas konfigureerida rakenduse Microsoft Dynamics 365 e-kaubanduse saidi domeeni nime. 

## <a name="add-domains-during-e-commerce-initialization"></a>Domeenide lisamine e-kaubanduse lähtestamise ajal

Domeenide seostamiseks e-kaubanduse keskkonnaga, lähtestage e-kaubandus, nagu on kirjeldatud teemas [Uue e-kaubanduse saidi juurutamine](deploy-ecommerce-site.md). Lähtestamise ajal palutakse teil anda teavet, mida kasutatakse teie e-kaubanduse keskkonna ettevalmistamiseks. Lisage väljale **Toetatud hostinimed** kõik domeenid, mida kavatsete selle keskkonnaga kasutada. Mitu domeeni tuleb eraldada semikooloniga. Sel viisil on domeenid konfigureeritud kõikides vajalikes e-kaubanduse komponentides ja need on kasutusvalmis, kui vahetate liikluse sisuedastusvõrgust (CDN) või veebiserverist ja suunate selle e-kaubanduse eesserveritesse.

## <a name="add-domains-after-e-commerce-initialization"></a>Domeenide lisamine pärast e-kaubanduse lähtestamist

E-kaubanduse keskkonnaga uute domeenide seostamiseks pärast e-kaubanduse lähtestamist, peate esitama teenusetaotluse.

## <a name="additional-resources"></a>Lisaressursid

[Uue e-kaubanduse saidi juurutamine](deploy-ecommerce-site.md)

[Võrgupoe kanali häälestamine](online-stores.md)

[e-Commerce saidi loomine](create-ecommerce-site.md)

[Veebisaidi seostamine kanaliga](associate-site-online-store.md)

[robots.txt-failide haldamine](manage-robots-txt-files.md)

[URL-i hulgiümbersuunamiste üleslaadimine](upload-bulk-redirects.md)

[B2C rentniku seadistus Kaubanduses](set-up-B2C-tenant.md)

[Kasutaja sisselogimiseks kohandatud lehtede seadistamine](custom-pages-user-logins.md)

[Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas](configure-multi-B2C-tenants.md)

[Sisuedastusvõrgu (CDN) toe lisamine](add-cdn-support.md)

[Asukohapõhise poetuvastuse lubamine](enable-store-detection.md)
