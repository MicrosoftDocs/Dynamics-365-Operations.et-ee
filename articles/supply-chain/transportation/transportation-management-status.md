---
title: Transpordihalduse olekud
description: See teema selgitab, kuidas luua transpordi olekut ja vastendada seda olekut vedaja olekuga.
author: Weijiesa
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3e528c13b1df68dde5a73a7d7cae3973b99b6f5e
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671614"
---
# <a name="transportation-management-statuses"></a>Transpordihalduse olekud

[!include [banner](../includes/banner.md)]

Seadistage transpordi olekute põhikoodid, et tõlgendada kättetoimetajate poolt tarnitud koode. See võimaldab teil oleku pakkumiseks ühendada saadetise vedajatega. Transpordi oleku põhikoodi jaoks esitatud transpordi olek võib aidata jälgida koorma, saadetise või konteineri olekut. Koorma, saadetise või konteineri kindlat transpordi olekut saab uuendada ainult läbi andmevahetuse ja mitte käsitsi kasutajaliidese kaudu.

## <a name="create-a-transportation-status"></a>Transpordi oleku loomine

Uue transpordi oleku loomiseks toimige järgmiselt:

1. Avage **Transpordihaldus \> Seadistus \> Transpordioleku koondüksused**.
1. Transpordi oleku koondüksuse loomiseks valige **Uus**.
1. Väljal **Transpordi oleku koondüksus** sisestage transpordi oleku kordumatu kood.
1. Väljal **Transpordi tüüp** valige transpordi tüübiks *Saadetise vedaja* või *Keksus*.
1. Sisestage nimi ja transpordi olek.
1. Sulgege leht.

## <a name="map-a-transportation-status-to-a-carrier-status"></a>Transpordi oleku vastendamine vedaja olekuga

Transpordi oleku vastendamiseks vedaja olekuga järgige järgmisi samme:

1. Avage **Transpordihaldus \> Seadistus \> Vedajad \> Vedaja transpordi olek**.
1. Kättetoimetaja koodi vastendamiseks transpordi oleku põhikoodiga valige **Uus**.
1. Valige vedaja ja veoteenuse kordumatu ID.
1. Valige transpordi oleku kood, mida soovite vastendada valitud vedaja koodiga.
1. Sisestage kättetoimetaja kasutatav väliskood.
1. Sulgege leht.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]