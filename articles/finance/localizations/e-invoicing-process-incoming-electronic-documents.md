---
title: Sissetulevate elektrooniliste dokumentide töötlemine
description: See artikkel annab ülevaate sissetulevate elektrooniliste dokumentide töötlemisest.
author: gionoder
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 554bc8fde3b2135eb878d885541c76ecd6d66493
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277297"
---
# <a name="processing-of-incoming-electronic-documents"></a>Sissetulevate elektrooniliste dokumentide töötlemine

[!include [banner](../includes/banner.md)]

Sissetulevaid elektroonilisi dokumente, nt hankija elektroonilisi arveid, saab importida ja töödelda kahel viisil:

- Failid tuuakse väliskanalitest ja edastatakse otse ühendatud rakendusele. Seal läbitakse täiendav teisendamine ja seejärel imporditakse nad andmebaasi.
- Failid on läbitud eeltöötlusesse elektroonilise arveldamise teenuses ja seejärel edastatakse teie ühendatud rakendusele.

Elektrooniline arveldamine toetab kahte kanalit sissetulevatele dokumentidele: e-post ja Microsofti kaustad SharePoint.

On olemas TWP seadistustüüpe, mis määratlevad, kas dokumendid on eeltöötluses või edastatakse otse teie ühendatud rakendusele:

- **Andmekanal** – süsteem pääsub dokumendi otse seotud rakendusele.
- **Andmekanal koos müügivõimaluste** töötlemisega – saate seadistada lisategevused, mis käivitatakse enne dokumendi saatmist ühendatud rakendusse.

Teavet selle kohta, kuidas seadistada stsenaariume erinevate kanalite sissetulevate elektrooniliste dokumentide töötlemiseks, [vaadake konfigureerige meilikanalit](e-invoicing-configure-email.md) ja [konfigureerige SharePoint kanal](e-invoicing-configure-sharepoint-channel.md).
