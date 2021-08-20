---
title: Domeeninime konfigureerimine
description: Selles teemas selgitatakse, kuidas konfigureerida rakenduse Microsoft Dynamics 365 e-kaubanduse saidi domeeni nime.
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9718effc776c64b2912a01972ad986eb332196a4477a952672fb147eaaf400c3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719497"
---
# <a name="configure-your-domain-name"></a>Domeeninime konfigureerimine


[!include [banner](includes/banner.md)]

Selles teemas selgitatakse, kuidas konfigureerida rakenduse Microsoft Dynamics 365 e-kaubanduse saidi domeeni nime. 

## <a name="add-domains-during-e-commerce-initialization"></a>Domeenide lisamine e-kaubanduse lähtestamise ajal

Domeenide seostamiseks enda Dynamics 365 Commerce'i e-kaubanduse keskkonnaga lähtestage e-kaubandus, nagu on kirjeldatud teemas [Uue e-kaubanduse rentniku juurutamine](deploy-ecommerce-site.md). Lähtestamise ajal palutakse teil anda teavet, mida kasutatakse teie e-kaubanduse keskkonna ettevalmistamiseks. Lisage väljale **Toetatud hostinimed** kõik domeenid, mida kavatsete selle keskkonnaga kasutada. Mitu domeeni tuleb eraldada semikooloniga. Sel viisil on domeenid konfigureeritud kõikides vajalikes kaubanduse komponentides ja need on kasutusvalmis, kui suunate liikluse sisuedastusvõrgust (CDN) või veebiserverist e-kaubanduse eesserveritesse.

## <a name="add-domains-after-e-commerce-initialization"></a>Domeenide lisamine pärast e-kaubanduse lähtestamist

Uute domeenide seostamiseks enda e-kaubanduse keskkonnaga pärast e-kaubanduse lähtestamist peate esitama teenusetaotluse.

## <a name="additional-resources"></a>Lisaressursid

[Uue e-kaubanduse rentniku juurutamine](deploy-ecommerce-site.md)

[E-kaubanduse saidi loomine](create-ecommerce-site.md)

[Dynamics 365 Commerce'i saidi seostamine võrgukanaliga](associate-site-online-store.md)

[Robots.txt-failide haldamine](manage-robots-txt-files.md)

[Üleslaadimise URL suunab ümber hulgi](upload-bulk-redirects.md)

[B2C rentniku seadistus Kaubanduses](set-up-B2C-tenant.md)

[Kasutaja sisselogimiseks kohandatud lehtede seadistamine](custom-pages-user-logins.md)

[Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas](configure-multi-B2C-tenants.md)

[Sisuedastusvõrgu (CDN) toe lisamine](add-cdn-support.md)

[Asukohapõhise poetuvastuse lubamine](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]