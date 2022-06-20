---
title: Optimeerimise laiendatavuse planeerimine
description: See artikkel kirjeldab laiendamisvõimalusstsenaariume, mida plaanimise optimeerimine toetab.
author: t-benebo
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-07-07
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 7d649110959e6bcfdaeb32dd53c55dbc446ed1be
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857540"
---
# <a name="planning-optimization-extensibility"></a>Optimeerimise laiendatavuse planeerimine

[!include [banner](../../includes/banner.md)]

See artikkel kirjeldab laiendamisvõimalusstsenaariume, mis on seotud koondplaneerimisega ja mida toetatakse planeerimise optimeerimises. Need võimalused on saadaval alates Microsoft Dynamics 365 Supply Chain Management versioonist 10.0.13.

## <a name="custom-processing-when-master-planning-is-completed"></a>Kohandatud töötlus, kui koondplaneerimine on lõpetatud

Plaanimise optimeerimise kõige tavalisema laiendamisvõimaluse stsenaariumi korral tehakse kohandatud töötlemine pärast plaani värskendamist. Näiteks võite lisada plaanitud tellimuste tabelisse (`ReqPO`) veeru või soovite võib-olla tuletada genereeritud plaanist mõnda statistilist teavet. Peamine laiendatavuspunkt, mis neid stsenaariume võimaldab, on `jobCompletedSuccessfully` meetod `MpsMasterPlanningEvents` klassis.

```X++
public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
```

Siin on näide laiendist, mis seadistab plaanitud tellimusele kohandatud `CstmOrderPriority` välja.

```X++
[ExtensionOf(classStr(MpsMasterPlanningEvents))]
public static final class MpsMasterPlanningEvents_Cstm_Extension
{
    public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
    {
        ttsbegin;

        var affectedPlannedOrdersQuery = _args.parmPostProcessingQueryBuilder().buildAffectedPlannedOrdersQuery();
        var affectedPlannedOrdersQueryRun = new QueryRun(affectedPlannedOrdersQuery);

        while (affectedPlannedOrdersQueryRun.next())
        {
            ReqPO reqPO = affectedPlannedOrdersQueryRun.get(tableNum(ReqPO));
            reqPO.selectForUpdate(true);
            reqPO.CstmOrderPriority = reqPO.ReqDate - systemDateGet() < 7 ? CstmPlannedOrderPriority::Urgent : CstmPlannedOrderPriority::Regular;
            reqPO.doUpdate();
        }

        ttscommit;

        next jobCompletedSuccessfully(_args);
    }

}
```

Kohandatud loogika lisamisel arvestage järgmisi piiranguid ja parimaid tavasid:

- `jobCompletedSuccessfully` meetodit nimetatakse kandeväliseks. Seetõttu on plaan kasutajale juba nähtav, kui kohandatud loogika käivitub. Kui teie kohandus määrab plaanitud tellimustele lisaväljad, on oluline teada saada, et nende väljade väärtused on lõpuks järjepidevad (teisisõnu võivad need olla kohe pärast planeerimistöö lõpetamist ajakohane).
- Teine koondplaneerimise töö võib käivituda kui `jobCompletedSuccessfully` meetodit kutsutakse. Uus töö võib mõjutada plaani või selle osa. Uus töö võib värskendada või kustutada samad plaanitud tellimused või vajadusekanded, mis loodi või uuendati osana käsitsetud `jobCompletedSuccessfully`planeerimistööst. Uuenduskonflikti erandeid tuleb käsitleda selle sündmuse laiendusena.
- Vältige seda meetodit laiendades ühe kandeulatuse kasutamist. Üks koondplaneerimise käitamine võib luua miljonites vajadusekannetes ja sadades tuhandetes plaanitud tellimustes. Kui kõiki neid kandeid ja plaanitud tellimusi töödeldakse ühe kande ulatuses, siis ilmnevad paljud SQL-lukud ja blokeeritakse teised planeerimisprotsessid. Lisaks, kui kannet hoitakse pikka aega, luuakse SQL-andmebaasis "kummitus-kirjeid". Kummitus-kirjed mõjutavad negatiivselt kõiki süsteemi protsesse.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]