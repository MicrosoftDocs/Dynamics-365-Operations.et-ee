---
title: Ühtse tarnerežiimi käsitlemise lubamine e-kaubanduse kanalites
description: See artikkel kirjeldab, kuidas lubada järjepidevat tarneviisi käsitlemist Microsoft Dynamics 365 Commerce, et käsitleda võimalikke e-äri kanalite tasude voogudega seotud probleeme.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: f32f1915f8f7de1d5536b69b05bc74c6149dfda6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885581"
---
# <a name="enable-consistent-delivery-mode-handling-in-e-commerce-channels"></a>Ühtse tarnerežiimi käsitlemise lubamine e-kaubanduse kanalites 

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas lubada järjepidevat tarneviisi käsitlemist Microsoft Dynamics 365 Commerce, et käsitleda võimalikke e-äri kanalite tasude voogudega seotud probleeme.

Salvestamata Dynamics 365 Commerce päisetaseme tasusid ei rakendata e-äri kanalites vaikimisi. Selline käitumine võib põhjustada e-äri kanalites ühe või mõlemad järgmised probleemid:

- Proeerimata päisetaseme tasusid ei kuvata.
- Tarneviiside tasud pole tarneviisi ja väljaregistreerimistellimuse kokkuvõtte vahel järjepidevad.

Nende probleemide lahendamiseks peate lülitama sisse funktsiooni Luba tarnerežiimi **järjepidev käsitlemine kanalis**. See funktsioon tagab, et päringuteta päisetasandi tasud ilmuvad e-äri kanalites ja et müügitellimuse tarneteavet käsitseb järjepidev sama taotluse töövoog.

## <a name="turn-on-the-enable-consistent-delivery-mode-handling-in-channel-feature"></a>Lülita kanali funktsioonis sisse järjepideva tarneviisi käsitlemine

Commerce headquartersi **kanali funktsioonis ühtse tarnerežiimi** käsitlemise lubamiseks järgige neid samme.

1. Avage funktsioonihalduse tööruum **(** Süsteemihalduse tööruumide **funktsioonihaldus \>\>).**
1. Saadaolevaid funktsioone loendis otsige ja valige kanalis **luba kooskõlas tarnerežiimi käsitsemine**.
1. Valige parempoolsel paanil suvand **Luba kohe**.
