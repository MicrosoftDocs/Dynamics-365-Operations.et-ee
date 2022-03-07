---
title: Hilinemised
description: Selles teemas antakse teavet hilinenud kuupäevade kohta koondplaneerimises. Hilinenud kuupäev on realistlik kande vastuvõtmise tähtaeg, kui varaseim koondplaneerimise arvutatud täitmise kuupäev on nõutavast kuupäevast hilisem.
author: ChristianRytt
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e89830feea12b4f5703e0eda622729887dd9bf46
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573749"
---
# <a name="delays"></a>Hilinemised

[!include [banner](../includes/banner.md)]

Selles teemas antakse teavet hilinenud kuupäevade kohta koondplaneerimises. Hilinenud kuupäev on realistlik kande vastuvõtmise tähtaeg, kui varaseim koondplaneerimise arvutatud täitmise kuupäev on nõutavast kuupäevast hilisem.

Koondplaneerimine saab arvutada varaseima kande täitmise kuupäeva täitmisaegade, materjali saadavuse, võimsuse saadavuse ja erinevate plaanimisparameetrite põhjal. 

Kui koondplaneerimine arvutab praegusest kuupäevast varasema tellimuse kuupäeva, ei saa tellimust täita õigel ajal. Seetõttu lükatakse tellimus edasi. Sellisel juhul plaanib koondplaneerimine tellimust praegusest kuupäevast edasi ja hõlmab täitmisaegu. Need täitmisajad algavad mis tahes madalama taseme kaubakomponentidega. Tellimus saab seejärel edasilükatud kuupäeva. Edasilükatud kuupäev on praegustel andmetel põhinev realistlik tähtaeg. Koondplaneerimine arvutab ka hilinemispäevade arvu. 

Mõningatel juhtudel võite hilinemisi mitte arvutada, näiteks kui kasutajad teavad, et saavad täitmisaegu kiirendada, valides alternatiivsed tarneviisid. 

Saate konfigureerida laovarude grupi viivituste arvutamise viisi. Seejärel saate laovarude grupi hiljem kaubale lisada. 

Lehel **Koondplaneerimise parameetrid** saate seadistada viivituste arvutamise algusaja. Kui tellimus täidetakse pärast seda aega, lisatakse tellimuse viivituskuupäevale ühepäevane viivitus. 

> [!NOTE]
> Varasemates versioonides nimetati arvutatud viivitusi *tähtajateadeteks*, hilinenud kuupäeva *tähtajakuupäevaks* ja hilinenud kannet *tulevaseks kandeks*.

## <a name="limited-delays-in-production-setup-with-multiple-bom-levels"></a>Piiratud viivitused tootmise seadistamisel mitme kooslusetasemega
Kui töötate mitme kooslusetasemega tootmise seadistuse viivitustega, on oluline meeles pidada, et koondplaneerimise käitamise osana värskendatakse viivitusega ainult viivitust põhjustava üksuse kohal (koosluse struktuuris) olevad üksused. Muudele koosluse struktuuri üksustele ei saa viivitust rakendada enne esimese koondplaneerimise käitamist, kui ülataseme plaanitud tellimus on kinnitatud. 

Selle teadaoleva piirangu lahendamiseks saab koosluse struktuuri ülaosa viivitustega tootmistellimused kinnitada enne järgmise koondplaneerimise käitamist. Nii säilitatakse viivitusega kinnitatud plaanitud tootmistellimuse viivitus ja kõik selle aluseks olevad komponendid ajakohastatakse vastavalt.
Tegevusteateid saab kasutada ka plaanitud tellimuste tuvastamiseks, mida saab koosluse struktuuri muude viivituste tõttu hilisemale kuupäevale teisaldada.

## <a name="desired-date"></a>Soovitud kuupäev

Lehe **Plaanitud tellimus** vahekaardil **Viivitused** on planeeritud kuupäeva parameeter **Soovitud kuupäev**. Plaanitud tellimuse soovitud kuupäev on viivituste aluskuupäev, mis on arvutatud kuupäev, mis võrdub parameetrist **Netonõue** arvutatud parameetriga **Nõutav kuupäev**. Kui plaanitud tellimus on koosluse rida, tootmisrida või kanban-rida, on soovitud kuupäeva aluseks **Vajaduse kuupäev** ja soovitud kuupäeva ei kuvata lehel **Plaanitud tellimus**.

## <a name="additional-resources"></a>Lisaressursid

[Laovarude sätted](coverage-settings.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]