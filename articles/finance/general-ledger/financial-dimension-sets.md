---
title: Finantsdimensioonikomplektid
description: See teema kirjeldab finantsdimensioonide komplekte ja annab näpunäiteid nende kasutamise optimeerimiseks.
author: yukonpeegs
ms.date: 03/23/2021
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 415a41100cc5be740f064d52598cd256c0aa2ae1d45473c8039bdc6e22381b3c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739974"
---
# <a name="financial-dimension-sets"></a>Finantsdimensioonikomplektid

[!include [banner](../includes/banner.md)]

See teema kirjeldab finantsdimensioonide komplekte ja annab näpunäiteid nende kasutamise optimeerimiseks.

Dimensioonikomplekt on finantsdimensioonide järjestatud loend, mida saab kasutada pearaamatu andmete summeerimiseks kasutaja määratletud viisil. Dimensioonikogumite esmane kasutamine on proovibilansi määratlemine.

Ainus standardne dimensioonikogum on dimensioonikogum, mis sisaldab ainult põhikontot.

Finantsdimensioonikogumite loomiseks ja haldamiseks kasutage lehte **Finantsdimensioonikogumid**.

## <a name="dimension-set-balances"></a>Dimensiooni määratud saldod

Dimensioonikogumil võivad olla finantsdimensioonidel põhinevad saldod. Saldod on pearaamatus olemas ja põhinevad dimensioonikogumi määratlusel. Saldod summeeritakse pearaamatu andmetest, et aidata parandada jõudlust nende toomisel (nt proovibilansi loomisel).

## <a name="create-balances"></a>Saldode loomine

Kasutage nuppu **Loo saldod**, et lähtestada saldod dimensioonikogumi jaoks, millel pole praegu saldosid.

> [!NOTE]
> Soovitame piirata saldodega dimensioonikogumite arvu, kuna saldouuendused mõjutavad kõiki pearaamatu konteerimistegevusi.

## <a name="update-balances"></a>Värskenda saldosid

Viimase pearaamatu konteerimistegevuse kaasamiseks saldodesse kasutage nuppu **Uuenda saldosid**. Saldouuendused on kerge koormusega toimingud. Nad peavad töötlema ainult pearaamatu konteerimistegevust, mis on toimunud pärast viimast uuendamist.

> [!NOTE]
> Proovibilansi kuvamine nõuab värskendust veendumaks, et kuvatavad saldod on ajakohased. Kaaluge korduva pakett-töö kasutamist, et teie kõige sagedamini kasutatavate dimensioonikogumite uuendused oleks kiired. Sel viisil aitate minimeerida aega, mida proovibilansi kasutajad peavad ootama.

## <a name="rebuild-balances"></a>Taasta saldod

Saldode nullist uuesti loomiseks kasutage nuppu **Loo saldod uuesti**. Sel viisil aitate tagate, et need vastaksid pearaamatu andmetele. Saldode taastamine nõuab palju töötlemist ja seda ei tohiks tavaliselt nõuda.

> [!NOTE]
> Kui teil on stsenaarium, mis nõuab regulaarselt saldode taastamist, soovitame teil pöörduda klienditoe poole. Klienditugi aitab teil määratleda, miks saldod pearaamatu andmetega ei ühti.

## <a name="clear-balances"></a>Saldode tasaarvestus

Saldode eemaldamiseks ja edasiste värskenduste peatamiseks kasutage nuppu **Tühjenda saldod**. Dimensioonikomplekt ei mõjuta enam pearaamatu konteerimistegevusi.

Lisateavet leiate jaotisest [Finantsdimensioonid](financial-dimensions.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
