---
title: Väheneva jääkväärtuse kuluarvestusmeetod pärast tükeldamist
description: Selles teemas kirjeldatakse meetodit, mida kasutatakse põhivarades kulumi arvutamiseks pärast seda, kui vara tükeldatakse väheneva jääkväärtuse meetodil.
author: moaamer
manager: Ann Beebe
ms.date: 11/17/2020
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
ms.search.validFrom: 2020-11-17
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 615d17c71b904d426081d4c57492ba7e95c2c749
ms.sourcegitcommit: 65f9e2584c0530b1a71655aae09101691726b47f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/01/2020
ms.locfileid: "4650657"
---
# <a name="reduce-balance-depreciation-after-a-split"></a>Väheneva jääkväärtuse kuluarvestusmeetod pärast tükeldamist

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse meetodit, mida kasutatakse põhivarades kulumi arvutamiseks pärast seda, kui vara tükeldatakse teiseks varaks väheneva jääkväärtuse meetodil. Vararaamatus konfigureeritud kulumiaastaks on finantsaasta. Lisateavet vt teemast [Saldo kulumi vähendamine](reduce-balance-depreciation.md) ja [Põhivara tükeldamine](tasks/split-fixed-asset.md).

Kui tükeldate põhivara eelarveperioodi jooksul, mis on vara soetamise perioodist hilisem kui periood, arvestatakse vähendatud saldoga kulumit eelmise aasta vara raamatupidamisliku jääkväärtuse (NBV) alusel. See arvestab ka soetamise ja kulumi korrigeerimise kandeid, mis loodi vara tükeldamise kandest. Selline käitumine eeldab, et vara soetati ühel finantsaastal ja tükeldatakse hilisemal finantsaastal. Summa, mis tuleb amortiseerida algse vara puhul pärast tükeldamist peegeldab vara raamatupidamislikku jääkväärtust enne vara tükeldamist ja tükeldamiseks sisestatud soetamise ja kulumi korrigeerimise kannet.

Näiteks kehtivad järgmised tingimused.

- Finantsperiood on 30. juuni kuni 1. juuli.
- Väheneva saldo protsent on 18 protsenti ja vara soetatakse 2019. aasta juunis soetamismaksumusega 10 000 USD.
- Esimese finantsaasta kulum võrdub 18 000 USD-ga, igakuine kulum võrdub 150 USD-ga ja vara amortiseeritakse seejärel summas 738.75 USD kuni novembrini 2019.
- Novembris 2019 tükeldatakse 80 protsenti varast teiseks põhivaraks.

[![Väheneva jääkväärtuse kuluarvestusmeetod pärast tükeldamist](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)

Algse vara kulumi summa on $1822.25. See summa võrdub raamatupidamisliku jääkväärtusega enne tükeldatud kande sisestamist (9111.25 USD), pluss soetuse korrigeerimine, mis luuakse tükeldatud kande (8000 USD) sisestamisel, pluss kulumi korrigeerimine, mis luuakse tükeldatud kande (711 USD) jooksul. Seetõttu on teise aasta kulum (1822.25 × 18 protsenti) ÷ 12 = 27.33 USD.

Uue põhivara kulumiarvestuse summa esimesel aastal on (8000 × 18 protsenti) ÷ 12 = 120 USD.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]