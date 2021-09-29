---
title: Mobiilseadmete globaalsed parameetrid
description: Selles teemas selgitatakse, kuidas seadistada mobiili seadmeid Laohalduse parameetrite lehel.
author: HuberIvan
ms.date: 08/13/2021
ms.topic: article
ms.search.form: WHS
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-huberivan
ms.search.validFrom: 2021-08-13
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 03c10232d55c99c73e625170797f89f6c77e812b
ms.sourcegitcommit: 99bde425ade701ef244c6bca6d411aef94a59b3c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/20/2021
ms.locfileid: "7505561"
---
# <a name="global-mobile-device-parameters"></a>Mobiilseadmete globaalsed parameetrid

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas seadistada globaalsed laohaldusparameetrid, mis mõjutavad süsteemi suhtlemist mobiilseadmetega.

Lisateavet laotööliste seadistamise kohta leiate teemast [Halda laotöötajat](manage-warehouse-workers.md). Lisateavet, mis on seotud litsentsiplaadi käsitlemisega mobiilseadmetes, leiate teemast [Litsentsiplaadi vastuvõtmine mobiilirakenduse Warehouse Management kaudu](warehousing-mobile-device-app-license-plate-receiving.md). Tsüklite loendamise kohta lisateabe saamiseks vaadake [Tsüklite loendamine](cycle-counting.md) ja [Tsükli loendamise näite stsenaariumid](cycle-counting-scenarios.md).

## <a name="open-the-warehouse-management-parameters-page"></a>Avage Laohalduse parameetrite leht

**Laohalduse parameetrite** lehe avamiseks minge lehele **Laohaldus \> Seadistamine \> Laohalduse parameetrid**. Seejärel saate määrata väljad, mis on seotud mobiilseadmete tööga, nagu on kirjeldatud selle teema järgmises osas.

## <a name="mobile-device-fasttab-on-the-general-tab"></a>Mobiilseadme kiirkaart vahekaardil Üldine

Ülemaailmsed mobiili seaded leiate **Mobiiliseade** Kiirkaardi vahekaardilt **Üldine** lehelt **Laohalduse parameetrid**. Saadaval on järgmised väljad.

| Field | Kirjeldus |
|---|---|
| Mobiilse seadme märkuse tüüp | Saate valida teabe tüübi, mis müügitellimuse komplekteerimisel töötajatele kuvatakse. |
| Skannitud koguse piirang | Sisestage maksimaalne üksuse kogus, mida töötaja saab iga seansi ajal skannida, kasutades mobiilseadme menüüelementi, millel on **Töö loomise protsess** väärtuseks *Reguleerimine*. See väli ei mõjuta skanneerimist, mida tehakse muud tüüpi menüüelemendi abil. |
| Kasuta mobiilse seadme seansi logimist | Töötaja sisselogimisajaloo pidamiseks määrake see suvand väärtusele *Jah*. Logi vaatamiseks avage **Töökasutajate seansid \> Päringud ja aruanded \> Mobiilse seadme logid \> Töökasutajate seansid**. |
| Salvestatud tõrgete arv | Sisestage maksimaalne veakirjete arv, mille süsteem peaks salvestama. Veaogi vaatamiseks avage **Töökasutajate seansid \> Päringud ja aruanded \> Mobiilse seadme logid \> Töökasutajate seansid**. |
| Vaikimisi lao üleviimise tööleht | Valige päevik, mida kasutatakse siis, kui töötajad kasutavad mobiiliseadet toodete teisaldamiseks ühest laost teise. |
| Saate lubada ostutellimuse rea registreerimis välisel ülevaatamisel | Määrake selle suvandi väärtuseks *Jah*, kui töötajad peaksid saama mobiilseadme abil registreerida ostutellimuste tellimuste read, mille **Kinnitusolek** väärtus on *Välises ülevaates*. Seadistage see suvand väärtusele *Ei*, et takistada töötajaid registreerimast ridu ostutellimustele, mis on väliselt üle vaadatud. |
| Luba RSAT-tugi | See väli lubab Warehouse Management mobiilirakenduse ülesannete valideerijat, mis logib ja kinnitab iga rakenduse toimingu. Kuna see protsess võib süsteemi jõudlust oluliselt aeglustada, peaksite valideerija lubama ainult testimise ajal. Te ei tohiks seda kunagi tootmiskeskkonnas lubada. |
