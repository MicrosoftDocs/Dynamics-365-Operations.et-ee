---
title: Põhivarakande valikud
description: Selles teemas kirjeldatakse põhivara kannete loomiseks saadaolevaid erinevaid viise.
author: moaamer
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: kfend
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 507e263e7267fe96cdf9ed78a84924839c2de982
ms.sourcegitcommit: e09f5c6d78d7942af950ae3f6407df2fedceeba4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/06/2022
ms.locfileid: "8719744"
---
# <a name="fixed-asset-transaction-options"></a>Põhivarakande valikud

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

### <a name="options-for-entering-fixed-asset-transaction-types"></a>Põhivara kandetüüpide sisestamise suvandid


| Kande tüüp                    | Moodul                   | Suvandid                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| Soetamine, Soetamise korrigeerimine | Põhivarad             | Põhivara, Põhivara varud   |
|                                     | Pearaamat           | Päevaraamat                           |
|                                     | Ostureskontro         | Arve tööleht, Arve kinnitamise tööleht |
|                                     | Hanked | Ostutellimus                            |
| Kulum                        | Põhivarad             | Põhivarad                              |
|                                     | Pearaamat           | Päevaraamat                           |
| Likvideerimine                            | Põhivarad             | Põhivarad                              |
|                                     | Pearaamat           | Päevaraamat                           |
|                                     | Müügireskontro      | Vabas vormis arve                         |

Kulumiperioodide põhivara järelejäänud väärtust ei värskendata kulumikande tüüpi tööleherea käsitsi loomisel või importimisel andmeüksuse kaudu. Seda väärtust värskendatakse, kui töölehe rea loomiseks kasutatakse kulumisoovituste protsessi.

Lisateavet leiate jaotisest [Põhivarade integreerimine](fixed-asset-integration.md).

Süsteem väldib kulumi sisestamist samasse perioodi kaks korda. Näiteks kui kaks kasutajat loovad kulumisoovitusi jaanuariks eraldi, sisestatakse esimese kasutaja kulum esimesele töölehele. Kui teine kasutaja sisestab kulumi teisele töölehele, kontrollib süsteem viimast kulumiarvestust ega sisesta sama perioodi kulumit teist korda.

### <a name="transactions-that-require-a-different-voucher-number"></a>Kanded, mille vautšeri numbrid on erinevad

Järgmistes põhivarakannetes kasutatakse erinevaid kandenumbreid:

- Varale tehakse täiendav soetamine ja arvutatakse järelkulum.
- Vara tükeldatakse.
- Likvideerimise kulumi arvutamiseks kasutatav parameeter on sisse lülitatud ja vara likvideeritakse.
- Vara teenuse kuupäev on enne soetamiskuupäeva. Seega sisestatakse kulumi korrigeerimine.

> [!NOTE]
> Kannete sisestamisel veenduge, et kõik kanded oleksid seotud sama põhivaraga. Kannet ei sisestata, kui see hõlmab rohkem kui ühte põhivara, isegi kui väli **Uus kanne** on määratud pearaamatu lehel **Töölehe nimed** valikule **Ainult üks kande number**. Kui kaasate kandesse rohkem kui ühe põhivara, kuvatakse teade "Kandel võib olla ainult üks põhivarakanne" ja te ei saa kannet sisestada.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
