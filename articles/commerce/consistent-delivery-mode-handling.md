---
title: Luba tarnerežiimi järjepidev käsitlemine e-äri kanalites
description: See teema kirjeldab, kuidas lubada järjepidevat tarneviisi käsitlemist Microsoft Dynamics 365 Commerce, et käsitleda võimalikke e-äri kanalite tasude voogudega seotud probleeme.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 4cecd70dacd72572afc8e6cb65530bf2be4cc93d
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349922"
---
# <a name="enable-consistent-delivery-mode-handling-in-e-commerce-channels"></a>Luba tarnerežiimi järjepidev käsitlemine e-äri kanalites 

[!include [banner](includes/banner.md)]

See teema kirjeldab, kuidas lubada järjepidevat tarneviisi käsitlemist Microsoft Dynamics 365 Commerce, et käsitleda võimalikke e-äri kanalite tasude voogudega seotud probleeme.

Salvestamata Dynamics 365 Commerce päisetaseme tasusid ei rakendata e-äri kanalites vaikimisi. Selline käitumine võib põhjustada e-äri kanalites ühe või mõlemad järgmised probleemid:

- Proeerimata päisetaseme tasusid ei kuvata.
- Tarneviiside tasud pole tarneviisi ja väljaregistreerimistellimuse kokkuvõtte vahel järjepidevad.

Nende probleemide lahendamiseks peate lülitama sisse funktsiooni Luba tarnerežiimi **järjepidev käsitlemine kanalis**. See funktsioon tagab, et päringuteta päisetasandi tasud ilmuvad e-äri kanalites ja et müügitellimuse tarneteavet käsitseb järjepidev sama taotluse töövoog.

## <a name="turn-on-the-enable-consistent-delivery-mode-handling-in-channel-feature"></a>Lülita kanali funktsioonis sisse järjepideva tarneviisi käsitlemine

Commerce headquartersi **kanali funktsioonis ühtse tarnerežiimi** käsitlemise lubamiseks järgige neid samme.

1. Avage funktsioonihalduse tööruum **(** Süsteemihalduse tööruumide **funktsioonihaldus \>\>).**
1. Saadaolevaid funktsioone loendis otsige ja valige kanalis **luba kooskõlas tarnerežiimi käsitsemine**.
1. Valige parempoolsel paanil suvand **Luba kohe**.
