---
title: Veose seadistamine
description: Selles teemas selgitatakse, kuidas konfigureerida sissetuleva veose laotoiminguid.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: bcc5ce7d9b9031fe8e9589798e07162106277767
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987275"
---
# <a name="set-up-consignment"></a>Veose seadistamine

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas konfigureerida sissetuleva veose laotoiminguid.

Veose varud on varud, mis kuuluvad hankijale, kuid mida hoitakse teie tegevuskohas. Kui olete valmis tarbima või kasutama varusid, võtate varude omandiõiguse üle. See teema kirjeldab veose protsesside lubamiseks vajalikku seadistust. Veoseprotsesside kohta lisateabe saamiseks vaadake teemat [Saadetise seadistamine](consignment.md).

## <a name="inventory-owners"></a>Varude omanikud
Füüsiliste sissetulevate veose varude kirjendamiseks peate määratlema hankijast omaniku. Seda tehakse lehel **Varude omanik**. Kui teete valiku **Hankija konto**, loob see väljade **Nimi** ja **Omanik** jaoks vaikeväärtused. Väärtus väljal **Omanik** on hankijale nähtav, seega võite soovi korral seda muuta, kui hankijakonto nimesid pole välistel inimestel lihtne tuvastada. On võimalik redigeerida välja **Omanik**, kuid ainult kirje **Varude omanik** salvestamiseni. Väli **Nimi** täidetakse selle osapoole nimega, millega hankija konto on seostatud ja seda ei saa muuta.

[![inventory-owners](./media/inventory-owners.png)](./media/inventory-owners.png)

## <a name="tracking-dimension-group"></a>Jälgimisdimensioonigrupp
Veose protsessides kasutatavad kaubad tuleb seostada valikuga **Jälgimisdimensioonigrupp**, kus dimensioon **Omanik** on määratud sättele **Aktiivne**. Dimensioonil Omanik on suvandid **Füüsiline ladu** ja **Finantsiline laovaru** valitud. Suvand **Laovarude planeerimine dimensioonide kaupa** pole kunagi valitud.

[![tracking-dimension-group](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)

## <a name="inventory-ownership-change-journal"></a>Varude omandiõiguse muutmise tööleht
Töölehte **Varude omandiõiguse muutmine** kasutatakse, et kirjendada veose varude omandiõiguse ülekannet hankijalt juriidilisele isikule, kes seda tarbib. Nagu iga varude töölehega, tuleb see tuvastada lao töölehe nimega. Need nimed luuakse lehel **Lao töölehe nimed** ja valik **Töölehe tüüp** tuleb määrata sättele **Omandiõiguse muutmine**.

[![inventory-ownership-change-journal](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Hankija koostöö veoseprotsessides
Kui hankijad kasutavad hankija koostööliidest, saavad nad seda kasutada varude tarbimise jälgimiseks teie tegevuskohas. Lisateavet hankijate koostööks tarnijate seadistamise kohta leiate jaotisest [Hankijaportaali kasutaja turvalisus](../procurement/configure-security-vendor-portal-users.md).
