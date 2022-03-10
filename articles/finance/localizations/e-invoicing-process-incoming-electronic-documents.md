---
title: Sissetulevate elektrooniliste dokumentide töötlemine
description: See teema annab ülevaate sissetulevate elektrooniliste dokumentide töötlemisest.
author: dkalyuzh
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9701367e1ba1f9dbd1e53deb863c10af4213a359
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371863"
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
