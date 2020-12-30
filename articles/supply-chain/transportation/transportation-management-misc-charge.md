---
title: Transpordi halduse lisakulud
description: See teema selgitab, kuidas transpordi loodud tasusid tuleb seostada tasu koodiga.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2b703d770c7f9ea684716368cf1e7dbe5fec8710
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/29/2020
ms.locfileid: "4426728"
---
# <a name="transportation-management-miscellaneous-charges"></a>Transpordi halduse lisakulud

[!include [banner](../includes/banner.md)]

Nii nagu kõigi teiste lisatasude puhul, tuleb transpordi loodud tasusid seostada tasu koodiga. Vastasel juhul ei lisata neid tagasi tellimusele lisakuluna. **Kulude kood** määratleb, kuidas tasu arvestatakse seoses tellimuse ja tellimuse reaga, kuhu see lisatakse.

Minge **Transpordi haldus > Seadistus > Hinnang > Lisakulud**, et määratleda kvalifitseeruvad kriteeriumid, mis määravad, millal kindlat **Tasu koodi** rakendatakse tasule.

Teil peaks olema vähemalt üks seadistus iga vastava **Tasumooduli** sätte jaoks (*Klient* ja *Hankija*), kus **Lisakulude tüüp** on seatud väärtusele *Ei ole*. Kui see puudub, siis lisakulu *ei* lisata tellimusele.
