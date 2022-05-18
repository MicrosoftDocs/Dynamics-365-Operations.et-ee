---
title: Finantsdimensioonikomplektid
description: See teema kirjeldab finantsdimensioonide komplekte ja annab näpunäiteid nende kasutamise optimeerimiseks.
author: yukonpeegs
ms.date: 03/07/2022
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: c583a2a89b45b59ea76ffd8e38b6206c9ca9ed41
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722572"
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

## <a name="delete-a-dimension-set"></a>Dimensioonikogumi kustutamine

Ärge kustutage **ega looge uuesti dimensioonikomplekte** mis tahes lahenduse vormina, et lahendada konkreetse dimensioonikogumi potentsiaalseid probleeme bilansiandmetega. Dimensioonikogumi taasloomine on kulukas. Lisateabe saamiseks probleemide korral võtke ühendust klienditoega. 


Lisateavet leiate jaotisest [Finantsdimensioonid](financial-dimensions.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
