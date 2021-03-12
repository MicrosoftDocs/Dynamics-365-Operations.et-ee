---
title: Rendikohustise lühiajalise osa ümberklassifitseerimine
description: Selles teemas selgitatakse, kuidas luua igakuise töölehe kirjet, rendikohustise osa lühiajaliseks ümberklassifitseerimiseks.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 46bcd396c93bc1d2944241165d438f8ccc013e20
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442559"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a>Rendikohustise lühiajalise osa ümberklassifitseerimine

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas luua igakuise töölehe kirjet, rendikohustise osa lühiajaliseks ümberklassifitseerimiseks. Kui pakktöötluses valitud graafik on **Lühiajalise rendikohustise ümberklassifitseerimine**, luuakse töölehe kanne. Seda kirjet kasutatakse rendikohustise praeguse osa sisestamiseks kuu viimasel päeval. Samal ajal sisestatakse tühistamise kirje järgmise kuu esimesel päeval.

Rendikohustise lühiajaline osa kuvatakse kohustuse amortisatsioonigraafikus. Kui töölehe kanne on sisestatud, siis on veerg **Kohustuse ümberklassifitseerimise tööleht loodud** saadaval ja töölehe ID on sisestatud ka graafikusse.

Lühiajalise kohustise ümberklassifitseerimise töölehe kirje loomiseks ja sisestamiseks toimige järgmiselt.

1. Avage **Vara rentimine \> Perioodiline \> Töölehe partiina loomine**.
2. Valige dialoogikasti **Töölehe partiina loomine** väljal **Vali graafik** suvand **Lühiajalise rendikohustise ümberklassifitseerimine**.
3. Valige rendigrupp väljal **Rendigrupp**. Teise võimalusena valige raamatu ID väljal **Raamatu ID**.
4. Lülitage sisse parameeter **Sisestamine**. Teise võimalusena, kui kanne tuleb luua, kuid mitte sisestada, jätke see parameeter välja.
5. Enne kirje sisestamist selle vaatamiseks lülitage sisse parameeter **Eelvaatle enne sisestamist**.
6. Valige nupp **OK**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]