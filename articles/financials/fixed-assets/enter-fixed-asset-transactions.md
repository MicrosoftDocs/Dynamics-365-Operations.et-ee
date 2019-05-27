---
title: Põhivara kande valikud
description: Selles teemas kirjeldatakse põhivara kannete loomiseks saadaolevaid erinevaid viise.
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6362a63bca43b5ac8da14becf6b966e459365ce1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552737"
---
# <a name="fixed-asset-transaction-options"></a>Põhivara kande valikud

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse põhivara kannete loomiseks saadaolevaid erinevaid viise.

Põhivarad on võimalik integreerida ostureskontroga, müügireskontroga, hanke ja pearaamatuga. Samuti saate kaupu laohalduses põhivaradesse üle viia, kui soovite neid kaupu ettevõttesiseselt kasutada.

## <a name="accounts-payable"></a>Ostureskontro
Saate sisestada põhivarakanded lehele Töölehe kanne. Selle lehe saab avada lehelt Arve tööleht. Saate avada lehe Töölehe kanne ka lehelt Arve kinnitamise tööleht. Tehke väljal Vastaskonto tüüp valik Põhivara. Seejärel valige väljalt Vastaskonto põhivara number. Sisestage vahekaardil Põhivarad väärtused väljadele Kande tüüp ja Raamat.

## <a name="accounts-receivable"></a>Müügireskontro
Saate sisestada põhivarakanded lehele Vabas vormis arve.  Valige vabas vormis arve lehe ruudustikus Arve read reaüksus. Klõpsake kiirkaarti Rea üksikasjad. Sisestage likvideerimiskandele põhivara number ja raamat. Vabas vormis arvete puhul on põhivarakande tüübiks alati Likvideerimine – müük.

## <a name="procurement-and-sourcing"></a>Hanked
Saate sisestada põhivarakanded lehele Ostutellimus. Sisestage ostutellimuse loomiseks vajalik teave ja klõpsake seejärel nuppu OK. Klõpsake lehel Ostutellimus kiirkaarti Rea üksikasjad. Seejärel sisestage vahekaardile Põhivara teave põhivara kohta. 

Olemasolevale põhivarale soetuskande sisestamiseks määrake põhivara number, raamat ja kande tüüp. Põhivara ei saa sisestada, kui osa sellest teabest on puudu. Uuele põhivarale soetuskande sisestamiseks tehke valik Uus põhivara? ja valige siis põhivaragrupp uuele põhivarale määramiseks. Ükski põhivara väli ei ole rea jaoks saadaval, kui kaup on laomudeligrupis, mis kasutab standardkulu laomudelit. Suvandid, mis on määratud lehel Põhivara parameetrid, määravad selle, kas saate ostumoodulitest soetuskandeid sisestada. 

Kui põhivara soetamiseks kasutatakse ostutellimust või töölehte Põhivara varud, mõjutab see laoväärtust.

## <a name="general-ledger"></a>Pearaamat
Kõiki põhivara kandetüüpe saab sisestada lehele Päevaraamat. Samuti saate põhivarade puhul töölehti kasutada põhivarakannete sisestamiseks.

## <a name="options-for-entering-fixed-asset-transaction-types"></a>Põhivara kandetüüpide sisestamise suvandid


| Kande tüüp                    | Moodul                   | Suvandid                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| Soetamine, Soetamise korrigeerimine | Põhivarad             | Põhivara, Põhivara varud   |
|                                     | Pearaamat           | Päevaraamat                           |
|                                     | Ostureskontro         | Arve tööleht, Arve kinnitamise tööleht |
|                                     | Hanked | Ostutellimus                            |
| Kulum                        | Põhivarad             | Põhivarad                              |
|                                     | Pearaamat           | Päevaraamat                           |
| Likvideerimine                            | Põhivarad             | Põhivarad                              |
| ** **                               | Pearaamat           | Päevaraamat                           |
| ** **                               | Müügireskontro      | Vabas vormis arve                         |


Kulumiperioodide põhivara järelejäänud väärtust ei värskendata kulumikande tüüpi tööleherea käsitsi loomisel või importimisel andmeüksuse kaudu. Seda väärtust värskendatakse, kui töölehe rea loomiseks kasutatakse kulumisoovituste protsessi.

Lisateavet leiate jaotisest [Põhivarade integreerimine](fixed-asset-integration.md).
