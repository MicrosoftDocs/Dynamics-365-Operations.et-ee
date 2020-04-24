---
title: Hooldusintervallid
description: Hooldusintervall näitab sagedust, millega hooldustellimuse ridu hooldusleppe ridade jaoks hooldustellimuste automaatsel loomisel luuakse.
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5766d8ce1fa382f3f014e160d311b2dfab2bf774
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216271"
---
# <a name="service-intervals"></a>Hooldusintervallid

[!include [banner](../includes/banner.md)]

Hooldusleppe intervall näitab sagedust, millega hooldustellimuse ridu hooldusleppe ridade jaoks hooldustellimuste automaatsel loomisel luuakse.

Kui te loote hooldustellimusi automaatselt, luuakse hooldustellimuse read vastavalt intervallile, mis te olete hooldusleppe rea jaoks määranud leppe rea alguskuupäevast alates.

Kui hooldusleppe rea väli **Intervall** on lehel **Hoolduslepped** tühi, on rida ühekordne sündmus ja seda ei kasutata korduvalt hooldustellimuste loomiseks.

## <a name="example"></a>Näide

See näide illustreerib, kuidas hooldusintervall hooldusleppe ja hooldustellimuse ridasid hooldustellimuses mõjutab.

### <a name="create-a-service-agreement"></a>Hooldusleppe loomine.

Esmalt looge hoolduslepe ja seadke suvand **Hooldustellimuste ühendamine** väärtusele **Hooldusleppega**.

1. Klõpsake valikut **Hoolduslepped**
2. Uue hooldusleppe loomiseks klõpsake **toimingupaani** vahekaardi **Hoolduslepe** grupis **Uus** valikut **Hoolduslepe**.
3. Sisestage kirjeldus, valige väljal **Projekti ID** projekt ja sisestage kuupäev väljale **Alguskuupäev**.
4. Väljal **Hooldustellimuste ühendamine** valige **Hooldusleppega**.

Olete loonud järgmise hooldusleppe.

| Project      | Alguskuupäev                                                                         |
|--------------|------------------------------------------------------------------------------------|
| Teie projekt | Projektile määratud kuupäev. Selles näites on kasutatud tänast kuupäeva. |

### <a name="create-a-service-agreement-line"></a>Hooldusleppe rea loomine

Järgmiseks loote hooldusleppe rea kande tüübiga **Tund**.

Selle näite osa lõpetamiseks peate lehel **Hooldusintervallid** looma 10-päevase hooldusintervalli. 

1. Valige äsja loodud hoolduslepe. 
2. Kiirkaardil **Read** klõpsake nuppu **Lisamine** lehe **Hoolduslepped** alumisel paanil uue rea loomiseks.
3. Väljal **Kande tüüp** valige **Tund**.
4. Väljal **Töötaja** valige töötaja, kes hooldust teostab.
5. Väljal **Hooldusintervall** valige 10-päevane intervall.

Olete loonud järgmise teabega hooldusleppe rea.

| Kande tüüp | Alguskuupäev                               | Teenuse intervall |
|------------------|------------------------------------------|------------------|
| Tund             | Tänane kuupäev.                        | Iga 10 päeva järel    |
| Töötaja           | Hooldust teostav töötaja. |                  |

Rea jaoks ei ole määratud kellaaja akent. 

### <a name="create-planned-service-orders"></a>Planeeritud hooldustellimuste loomine

Nüüd saate luua tuleval kuul planeeritud hooldustellimusi ja hooldustellimuste ridasid.

1. Lehe **Hoolduslepped** **toimingupaanil**, vahekaardil **Tarnimine** klõpsake valikut **Planeeritud hooldustellimused**.
2. Lehel **Hooldustellimuste loomine** sisestage väljale **Alguskuupäev** tänane kuupäev ning väljale **Lõppkuupäev** tänasest kuupäevast üks kuu hilisem kuupäev.
3. Seadke liugur **Tund** asendisse **Jah**. 
4. Klõpsake nupul **OK**.

Kuna hooldustellimusel ei toimu grupeerimist (määratud suvandiga **Hooldusleppega** moodulis **Hooldustellimuste ühendamine**), luuakse iga hooldustellimuse kohta üks hooldustellimuse rida.

### <a name="service-orders-created"></a>Loodud hooldustellimused

Dialoogiaknas **Hooldustellimuste loomine** määratud ajavahemikus on loodud kolm hooldustellimuse rida. Hooldustellimuse ridasid saate vaadata lehel **Hoolduslepped** (**Toimingupaan** \> vahekaart **Tarnimine** \> nupp **Kuvamine**).

## <a name="related-topics"></a>Seotud teemad

[Hooldusintervallide seadistamine](set-up-service-intervals.md)  

