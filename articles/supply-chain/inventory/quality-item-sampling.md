---
title: Kvaliteedijuhtimise kauba valim
description: Selles teemas kirjeldatakse, kuidas seadistada kauba valimeid.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ea749c470ab1d80f1f3974596a2cd4a1f5b7b32d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578484"
---
# <a name="quality-management-item-sampling"></a>Kvaliteedijuhtimise kauba valim

[!include [banner](../includes/banner.md)]

Kauba valimit kasutatakse kvaliteediseose osana. See määratleb praeguse füüsilise laovaru summa, mida tuleb kontrollida. Valimi aluseks võib olla fikseeritud kogus, protsent või terve litsentsiplaat.

## <a name="set-up-item-sampling"></a>Kauba valimi seadistamine

Kauba valimi seadistamiseks järgige neid samme.

1. Avage **Varude haldus \> Seadistus \> Kvaliteedijuhtimine \> Kauba valim**.
1. Valige suvand **Uus**.
1. Sisestage väärtus väljale **Kauba valim**.
1. Sisestage väärtus väljal **Kirjeldus**.
1. Sisestage arv väljale **Väärtus**. See väärtus on seotud külgneval väljal valitud koguse spetsifikatsiooni väärtusega.
1. Jaotises **Protsess** valige märkeruut **Täielik blokeerimine**, kui testi ebaõnnestumisel tuleks kogu partii või tellimisrea kogus blokeerida. Kui see ruut tühjendatakse, blokeeritakse testi ebaõnnestumisel ainult kvaliteeditellimuses olevad kaubad.
1. Valige käsk **Salvesta**.
1. Sulgege leht.

> [!NOTE]
> Funktsioon *Kvaliteedijuhtimine laoprotsesside jaoks* pakub täiendavaid kauba valimi määramise võimalusi. See lisab *Kauba valimi ulatus* kontseptsiooni ja võimaldab määratleda koguse spetsifikatsioonina täieliku litsentsi plaadi. Kui olete selle funktsiooni lubanud, vaadake jaotist [Kvaliteedijuhtimine laoprotsesside jaoks](quality-management-for-warehouses-processes.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
