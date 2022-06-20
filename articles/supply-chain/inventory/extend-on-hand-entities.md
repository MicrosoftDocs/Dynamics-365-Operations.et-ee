---
title: Vaba kaubavaru andmeüksuste laiendamine
description: See artikkel annab näite, mis näitab, kuidas lisada laiendatud välju vaadetele INVENTORSITEONHANDENTITY ja INVENTWAREWAREONHANDENTITY, et vaba kaubavaru andmeüksuste võimalused saaksid laienditega töötada.
author: yufeihuang
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 352b466a185bcd0778ea17e598129864c1547987
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906033"
---
# <a name="extend-inventory-on-hand-data-entities"></a>Vaba kaubavaru andmeüksuste laiendamine

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management pakub [laiendatavuse](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) funktsioone, mis võimaldavad teil [lisada tabelile välju laienduse kaudu](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md). See artikkel annab näite, mis `INVENTORSITEONHANDENTITY``INVENTWAREHOUSEONHANDENTITY` näitab, kuidas lisada laiendatud välju vaatele ja vaatele, nii et vaba kaubavaru andmeüksuste võimalused saavad laienditega töötada. Lisateavet andmeüksuste kohta leiate teemast [Andmehalduse ülevaade](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

> [!NOTE]
> Siin on loend mõnest vaba kaubavaru üksusest.
>
> - Vaba kaubavaru laoala järgi
> - Vaba kaubavaru laoala järgi V2
> - Vaba kaubavaru lao järgi
> - Vaba kaubavaru lao järgi V2

Pärast väljade lisamist tabelitele, mida kasutab vaade `inventSiteOnHandView`, peate mootori sünkroonima, et laiendusi tuvastataks õigesti.

1. Laiendage laiendusvälja lisamise kaudu vaadet `InventSiteOnHandView`.
1. Laiendage laiendusväljade abil vaadet `InventSiteOnHandAggregatedView`.
1. Laiendage `InventSiteOnHandAggregatedViewBuilder`i klassi viewBuilder, muutes meetodit `getExtensionFields()`. Sel viisil vastendate üksuse viewBuilder sünkroomise käitamisel vana vaate väljad uue vaate väljadega.

Näiteks olete laienduse kaudu lisanud tabelisse `InventTable` järgmised neli välja.

- Kohandatud väli 1
- Kohandatud väli 2
- Kohandatud väli 3
- Kohandatud väli 4

Sel juhul peate muutma meetodit `getExtensionFields()` järgmisel viisil.

```xpp
[ExtensionOf(classStr(InventSiteOnHandAggregatedViewBuilder))]
public final class InventOnHandAggregatedViewBuilder\_Extension
{
    protected Map getExtensionFields()
    {
        next getExtensionFields();
        Map extensionFields = new Map(Types::Int64, Types::Int64);
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 1), fieldNum(InventSiteOnHandAggregatedView, Custom field 1));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 2), fieldNum(InventSiteOnHandAggregatedView, Custom field 2));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 3), fieldNum(InventSiteOnHandAggregatedView, Custom field 3));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 4), fieldNum(InventSiteOnHandAggregatedView, Custom field 4));
        return extensionFields;
    }
}
```

Pärast nende juhiste järgimist saate uute väljade lisamise teel laiendada andmeüksusi „vaba kaubavaru laoala järgi” ja „vaba kaubavaru lao järgi”. Sel viisil tagate, et laiendatud väljad tuvastatakse ja kaasatakse neid andmeüksusi kasutavate andmete migreerimisel.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]