---
title: Domeeninime konfigureerimine
description: See artikkel selgitab, kuidas konfigureerida domeeni nime Microsoft Dynamics 365 e-kaubanduse saidi jaoks.
author: josaw1
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.search.form: ''
ms.openlocfilehash: 298ce84008e60cc82a494320b6a41f35338508c3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278620"
---
# <a name="configure-your-domain-name"></a>Domeeninime konfigureerimine


[!include [banner](includes/banner.md)]

See artikkel selgitab, kuidas konfigureerida domeeni nime Microsoft Dynamics 365 e-kaubanduse saidi jaoks. 

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
