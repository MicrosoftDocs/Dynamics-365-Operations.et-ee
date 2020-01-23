---
title: Commerce'i eelvaatekeskkonna ülevaade
description: See teema annab ülevaate rakenduse Microsoft Dynamics 365 Commerce eelvaatekeskkonnast.
author: v-chgri
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 901583afde4739be5313fa129ff0e52f11326881
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906066"
---
# <a name="commerce-preview-environment-overview"></a>Commerce'i eelvaatekeskkonna ülevaade

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

See teema annab ülevaate rakenduse Microsoft Dynamics 365 Commerce eelvaatekeskkonnast.

## <a name="overview"></a>Ülevaade

Commerce'i eelvaatekeskkond on valikuline lõpust lõppu Dynamics 365 Commerce'i eelvaatekeskkond, mis laseb potentsiaalsetel klientidel proovida Commerce toodet enne selle üldist vabastamist üldsusele.

Jättes kõrvale mõned väikesed piirangud, mis ei mõjuta funktsioone või praktilisust, pakub Commerce eelvaatekeskkond täielikku kauplemise kogemust ja seda saavad kasutada kliendid ja rakenduspartnerid, et hinnata toodet, anda tagasisidet ja teha sobivuse/vahe analüüs.

## <a name="limitations-of-the-commerce-preview-environment"></a>Commerce eelvaatekeskkonna piirangud

Kuigi Commerce eelvaatekeskkond pakub kõiki Commerce'i funktsioonide ja praktilisuste kogumit, on mõned väikesed piirangud:

- Kuigi Commerce eelvaatekeskkonnas ei ole geograafilisi piiranguid, saab keskkonda komponente, nagu Retail Cloud Scale Unit (RCSU) ja e-kaubanduse rakendusi, ette valmistada ainult Ameerika Ühendriikides.
- Commerce Preview keskkonnal on 30-päevase ajalimiit alates e-kaubanduse ettevalmistamise kuupäevast.
- Commerce Preview keskkonda saab edukalt rakendada ja lähtestada ainult keskkonnas, mis kasutab demo topoloogiat, kus kõik keskkonna komponendid on kasutusele võetud ühe virtuaalarvuti (VM) abil. Selle OneBox VM topoloogia peamine piirang on samaaegsete kasutajate arv, mida eelvaate keskkond saab toetada.
- Commerce eelvaatekeskkonda saab hinnata ainult seni, kuni on olemas Commerce'i toote üldine kättesaadavus (GA). Uued demo keskkonnad on saadaval pärast GA-d.

## <a name="get-started"></a>Alusta

Commerce eelvaatekeskkonna ettevalmistamiseks vaadake teemat [Commerce eelvaatekeskkonna ettevalmistamiseks](provisioning-guide.md).

## <a name="additional-resources"></a>Lisaressursid

[Commerce'i eelvaatekeskkonna ettevalmistamine](provisioning-guide.md)

[Commerce'i eelvaatekeskkonna konfigureerimine](cpe-post-provisioning.md)

[Commerce'i eelvaatekeskkonna valikuliste funktsioonide konfigureerimine](cpe-optional-features.md)

[Commerce'i eelvaatekeskkonna KKK](cpe-faq.md)
