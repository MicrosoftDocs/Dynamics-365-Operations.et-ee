---
title: Tagastatavad tasud arvutatakse tagastatud koguse alusel valesti
description: See teema annab tõrkeotsingu juhised, mis aitavad kassapidajatel tagastatavate kaupade koguse kohta kassas (POS) valesid tagastatavaid tasusid vaadata.
author: gvrmohanreddy
ms.date: 03/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c8ecaa0cb73d06ac66b57cce815264e841a2259b
ms.sourcegitcommit: 94ebdaae6dc996b205ac78ed546e38f91f4f46ed
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/28/2022
ms.locfileid: "8489724"
---
# <a name="refundable-charges-are-miscalculated-based-on-the-quantity-returned"></a>Tagastatavad tasud arvutatakse tagastatud koguse alusel valesti

[!include [banner](../../includes/banner.md)]

See teema annab tõrkeotsingu juhised, mis aitavad kassapidajatel tagastatavate kaupade koguse kohta kassas (POS) valesid tagastatavaid tasusid vaadata.

## <a name="description"></a>Kirjeldus

Klient tagastab nende kaupade osalise koguse, mis osteti müügitellimuse jaoks, mille reatasemel on tagastatavad tasud. Kuid osalise tagasimakse kuvamise asemel näitab kassa kõiki tasusid tagasisaadav summana.

Näiteks ostab klient kauba kohta kokku viis $5 kauba kohta, kauba $25. Klient tagastab siis kolme kauba viiest. Kassapidajale kuvatakse kassas $25 tagastatav tasu eeldatava $15 kolme tagastatud kauba eest.

## <a name="resolution"></a>Lahendus

### <a name="turn-on-the-enable-refunding-charges-based-on-the-refunded-quantity-feature"></a>Lülitage tagasimakstavate koguste funktsiooni põhjal sisse funktsioon Luba kulude tagastamine.

Microsoft Dynamics 365 Commerce Versiooni 10.0.26 **kohaselt** võimaldab tagastatud koguse funktsioonil põhinevate kulude tagastamise lubamine rea tasandil tagastatavate kulude arvutamist tagastatavate kaupade koguse alusel.

Commerce Headquartersi **tagastatud koguse funktsioonil põhinevate tagasimaksete** lubamise lubamiseks järgige neid samme.

1. Avage funktsioonihalduse **tööruum** (Süsteemiadministraatori **tööruumide \> funktsioonihaldus \>**).
1. Saadaolevaid funktsioone loendis otsige ja valige **funktsiooni Luba tagasimaksete tasud tagastatud koguse põhjal**.
1. Valige parempoolsel paanil suvand **Luba kohe**.
