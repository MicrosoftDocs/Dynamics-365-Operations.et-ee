---
title: Koosluseridade automaatse tarbimise põhimõtte sätteid ei järgita
description: Koosluseridade automaatse tarbimise põhimõtte sätteid ei järgita.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 84a84728016119a2a02f59f6903171afbceb48e7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026441"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a>Koosluseridade automaatse tarbimise põhimõtte sätteid ei järgita

KB number: 4612725

## <a name="symptoms"></a>Sümptomid

See probleem ilmneb, kui **Automaatse koosluse tarbimise** väli **Automaatse värskendamise** vahekaardil **Tootmise juhtimise parameetrite** lehel on seadistatud kui *Juhtimispõhimõte*. See säte näitab, et ostutellimuse saades tuleb automaatselt tarbida kõiki koosluseridu. Kui koosluseridade **juhtmispõhimõtte** väli on eraldi seatud väärtusele *Käsitsi*, võite eeldada, et koosluseridu ei tarbita automaatselt. Kui see probleem ilmneb, tarbitakse siiski automaatselt koosluseridu, kus **Juhtimispõhimõtte** väli väärtuseks on määratud *Käsitsi*.

## <a name="resolution"></a>Eraldusvõime

Kui teil tekib selline probleem, võivad teie tootmise juhtimise parameetrid olla seadistatud alluma **Juhtmispõhimõtte** sätetele koosluse ridadel. Kontrollige **Tootmise juhtimise parameetrid** lehel **Automaatse uuendamise** vahekaardil **Automaatne koosluse** tarbimine väärtust. Kui sätteks *Alati* ignoreerib süsteem kõigi koosluseridade **Juhtmispõhimõtte** sätet ja tühjendab alati. Süsteemi koosluseridade **Juhtmispõhimõttele** allutamiseks muutke välja **Automaatne koosluse** *Juhtmispõhimõtteks*.
