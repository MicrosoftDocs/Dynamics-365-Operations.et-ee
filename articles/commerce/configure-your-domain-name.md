---
title: Domeeninime konfigureerimine
description: Selles teemas selgitatakse, kuidas konfigureerida rakenduse Microsoft Dynamics 365 e-kaubanduse saidi domeeni nime.
author: psimolin
manager: AnnBe
ms.date: 10/01/2019
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
ms.openlocfilehash: 4db774783dba4b1cea9552da3cff29a9528bd496
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002170"
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

[E-kaubanduse saidi loomine](create-ecommerce-site.md)

[Veebisaidi seostamine kanaliga](associate-site-online-store.md)

[Robots.txt-failide haldamine](manage-robots-txt-files.md)

[Kasutaja sisselogimiseks kohandatud lehtede seadistamine](custom-pages-user-logins.md)

[Sisuedastusvõrgu (CDN) toe lisamine](add-cdn-support.md)

[Asukohapõhise poetuvastuse lubamine](enable-store-detection.md)
