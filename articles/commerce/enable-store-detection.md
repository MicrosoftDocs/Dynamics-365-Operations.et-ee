---
title: Asukohapõhise poetuvastuse lubamine
description: See artikkel kirjeldab, kuidas lülitada sisse asukohapõhine kaupluse tuvastamine oma saidi Dynamics 365 Commerce puhul.
author: brianshook
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 38c93e30a606d818d909a4ec014009c18c25e8c5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274336"
---
# <a name="enable-location-based-store-detection"></a>Asukohapõhise poetuvastuse lubamine

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas lülitada sisse asukohapõhine kaupluse tuvastamine oma saidi Dynamics 365 Commerce puhul.

Commerce’i asukohapõhine poetuvastus võimaldab pakkuda klientidele asjakohast saidi sisu vastavalt nende asukohale. Kui asukohapõhine poetuvastus on sisse lülitatud, kasutab Commerce’i renderdusteenus kliendi veebibrauseri IP-aadressi riigi/piirkonna teavet, et suunata klient parima saadaoleva geograafilise saidi konfiguratsiooni juurde.

## <a name="privacy-notice"></a>Privaatsusavaldus

Kui lülitate asukohapõhise poetuvastuse funktsiooni sisse, saadetakse kliendi brauseri teave Microsofti asukoha teenusele. Seda teavet kasutatakse siis, et pakkuda kliendile sisu, mis on tema asukohaga seotud. Nii kliendi brauserist saadetud teabele kui ka kliendilt saadud asukohapõhisele teabele kehtivad privaatsuse ja küpsiste vastavuse poliitikad.

## <a name="turn-on-location-based-store-detection"></a>Asukohapõhise poetuvastuse sisselülitamine

Asukohapõhise poetuvastuse sisselülitamiseks Commerce’is toimige järgmiselt.

1. Avage autorluse tööriistas oma sait.
1. Valige navigeerimispaanilt vasakult suvand **Saidi haldus**.
1. Valige **Saidi sätted**.
1. Seadke suvand **Luba asukohapõhine poetuvastus** olekusse **Sees**.

## <a name="additional-resources"></a>Lisaressursid

[Domeeninime konfigureerimine](configure-your-domain-name.md)

[Uue e-kaubanduse rentniku juurutamine](deploy-ecommerce-site.md)

[E-kaubanduse saidi loomine](create-ecommerce-site.md)

[Dynamics 365 Commerce'i saidi seostamine võrgukanaliga](associate-site-online-store.md)

[Robots.txt-failide haldamine](manage-robots-txt-files.md)

[Üleslaadimise URL suunab ümber hulgi](upload-bulk-redirects.md)

[B2C rentniku seadistus Kaubanduses](set-up-B2C-tenant.md)

[Kasutaja sisselogimiseks kohandatud lehtede seadistamine](custom-pages-user-logins.md)

[Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas](configure-multi-B2C-tenants.md)

[Sisuedastusvõrgu (CDN) toe lisamine](add-cdn-support.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
