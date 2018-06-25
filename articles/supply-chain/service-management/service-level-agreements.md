---
title: Teenustaseme lepped
description: "Teenindustaseme lepingus nõustub klient minimaalse reageerimisajaga, mille arvestamise aluseks on ajavahemik teenusettevõte probleemi registreerimise ja probleemi lahendamise vahel."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 63389ed348e9b1bebe00d9aaa9f78b97ac39317b
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="service-level-agreements"></a>Teenustaseme lepped        

[!include [banner](../includes/banner.md)]


Teenusetaseme lepe (SLA) on teenusettevõtte ja teenuskliendi vaheline leping. Teenusetaseme leppes nõustub klient minimaalse reageerimisajaga, mille arvestamise aluseks on ajavahemik teenusettevõte probleemi registreerimise ja probleemi lahendamise vahel.

Teenusetaseme lepe kehtestab klientidele pakutava standardse teenusetaseme, samuti muudab see teenusettevõtte jaoks selgeks, millal teenusetöö tuleb lõpetada.

Kliendile erinevate teenusetasemete pakkumiseks saab luua mis tahes arvu teenusetaseme leppeid.

## <a name="create-a-service-level-agreement"></a>Teenusetaseme leppe loomine

1.  Klõpsake valikut **Teenuste haldus** \> **Häälestamine** \> **Hoolduslepped** \> **Teenindustaseme lepingud**.

2.  Sisestage väljale **Teenindustaseme leping** teenindustaseme lepingu nimi.

3.  Sisestage aeg, millal soovite lubada teenindustaseme lepinguga seotud lõpetatud teenuse kõned. Seejärel valige kalender, kui soovite teenindustaseme lepingu aluseks võtta konkreetse kalendri.

## <a name="apply-a-service-level-agreement"></a>Teenusetaseme leppe rakendamine

Teenusetaseme lepe rakendatakse otse teenuselepingule.

Hooldustellimused, mille loote käsitsi ja seote teenusetaseme leppega teenuselepingusse antud teenusetaseme leppe alusel.

Automaatselt loodud teenusetellimusi teenusetaseme leppega ei seota.

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a>Teenusetaseme leppe rakendamine teenuseleppele

1.  Klõpsake valikut **Hooldushaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldusleppegrupid**. Valige teenuselepe, millele soovite teenusetaseme leppe rakendada, ja klõpsake **toimingupaanil** valikut **Redigeeri**.

2.  Valige väljal **Teenindustaseme leping** teenindustaseme leping, mida soovite määrata.

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a>Teenusetaseme leppe rakendamine teenuselepingu grupile

1.  Klõpsake valikut **Hooldushaldus** \> **Häälestamine** \> **Hooldustellimused** \> **Hooldusleppegrupid**.

2.  Valige väljal **Teenindustaseme leping** teenindustaseme leping, mida soovite määrata.

## <a name="track-time-on-a-service-order-against-an-sla"></a>Teenusetellimuse aja jälgimine teenusetaseme leppe alusel

Kui loote uue hooldustellimuse teenuseleppele, millele on määratud teenindustaseme leping, käivitatakse teenuse tarnimise ajaintervall ja süsteem hakkab tarneaega jälgima. Peale selle saate seada järgmised valikud.

  - Saate alustada ja lõpetada teenusetellimuse aja registreerimise, et registreerida teenusetellimustele kulutatud aja kogusumma.

  - Saate jälgida kokkulangevust teenindustaseme lepingus seatud ajaintervalliga.

  - Saate määratleda põhjuse koodid, mis tuleb seadistada, kui teenindustaseme lepingus seatud ajaintervall ületatakse.

## <a name="see-also"></a>Vt ka

[teenustaseme lepingute vastavuse vaatamine](view-compliance-with-service-level-agreements.md)

  


