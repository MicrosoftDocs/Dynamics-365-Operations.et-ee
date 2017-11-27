---
title: Krediitkaardikannete importimine ja haldamine
description: "Selles teemas kirjeldatakse kuludega seotud krediitkaardikannete importimist ja haldamist. Neid kandeid saab seadistada nii, et need imporditakse automaatselt korduva graafiku alusel või neid saab vajaduse järgi käsitsi importida."
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e640c9e44add5599be4a2e381b4ffd81f212889c
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="import-and-maintain-credit-card-transactions"></a>Krediitkaardikannete importimine ja haldamine

[!include[banner](../includes/banner.md)]

Kuludega seotud krediitkaardikandeid saab seadistada nii, et neid imporditakse automaatselt korduva graafiku alusel. Teise võimalusena saab kandeid vajaduse järgi käsitsi importida. Krediitkaardikanded imporditakse krediitkaardikannete andmeüksuse kaudu.

Andmeüksuste kohta leiate lisateavet jaotisest [Andmeüksused](../../dev-itpro/data-entities/data-entities.md).

## <a name="import-credit-card-transactions"></a>Saate importida krediitkaardikanded.

1. Tehke lehel **Krediitkaardikanded** valik **Kannete importimine**. Kui avate andmehalduse esimest korda, peab süsteem andmeüksuste loendi värskendama, enne kui jätkata saate.
2. Sisestage väljale **Nimi** imporditöö kordumatu kirjeldus.
3. Valige väljalt **Lähteandmete vorming** imporditavaid krediitkaardikandeid sisaldava faili vorming.
4. Valige **Laadi üles** ja otsige siis üles ja valige imporditav fail.
5. Kui fail on üles laaditud, siis valideerige krediitkaardikande faili vastendus ja krediitkaardi kannete andmeüksuse veerud, valides paanilt lingi **Kuva kaart**. Kui ilmneb vastendamistõrkeid või kui vastendust on vaja muuta, siis tehke vastendamise muudatused vahekaardilt **Vastendamise visualiseering** või vahekaardilt **Vastendamise üksikasjad**.
6. Krediitkaardikannete automatiseerimiseks valige **Korduva andmetöö loomine**. Siis saate määrata kordumise, mis määratleb, kui sageli krediitkaardikandeid tuleks importida. Kui olete lõpetanud, valige **OK**.
7. Valitud faili kohe importimiseks valige **Impordi**.
8. Kui importimise ajal tekib tõrge, saate vaadata käivituslogi või koondatud andmeid, et näha, milliseid vigu on vaja eduka importimise tagamiseks parandada.

> [!NOTE]
> Kui importida on vaja mitut failivormingut, tuleb luua igale vormingu tüübile eraldi imporditööd.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Lõpetatud töötajate krediitkaardikannete ümbermääramine

Pärast töötaja kirje lõpetamist keelatakse töötaja Active Directory domeeniteenuste (ADDS) konto. Kuid võib olla aktiivseid krediitkaardikandeid, mis tuleb siiski kuludesse kanda ja korvata. Lehelt **Krediitkaardikanded** saate määrata töötaja ümber mis tahes krediitkaardikandele, kus seostatud töötaja on lõpetatud.

Valige vähemalt üks krediitkaardikanne ja seejärel **Kannete ümbermääramine**. Seejärel saate valida teise töötaja, kellele krediitkaardikanded määrata. Pärast nende krediitkaardikannete ümbermääramist saab need kuluaruande jaoks valida ja tasuda tavalise kuluaruande korvamise protsessi kaudu.

