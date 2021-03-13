---
title: Kulumuudatuste simuleerimine planeeritud kulude kuluversiooni kasutades
description: Selles artiklis selgitatakse, kuidas saab kulumuudatuste mõjusid toodetud kauba arvutatud kuludele simuleerida eraldi kuluversiooniga planeeritud kuludele.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 78183
ms.assetid: 1e41953f-cdb9-4598-b776-46e49383a773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 053709cb7a4ffb30e1e4968096ea4df5e67242e5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011818"
---
# <a name="simulate-cost-changes-by-using-a-costing-version-for-planned-costs"></a>Kulumuudatuste simuleerimine planeeritud kulude kuluversiooni kasutades

[!include [banner](../includes/banner.md)]

Selles artiklis selgitatakse, kuidas saab kulumuudatuste mõjusid toodetud kauba arvutatud kuludele simuleerida eraldi kuluversiooniga planeeritud kuludele.

Kulumuudatuste mõjusid toodetud kauba arvutatud kuludele saab simuleerida eraldi kuluversiooniga planeeritud kuludele. Kasutage eraldi kuluversiooni astmelisi kulumuudatusi kajastavate ootel kulukirjete sisestamiseks ja kulu mõju arvutamiseks toodetavatele kaupadele. Kuna koosluse arvutustes kasutatakse aktiivsete kulude taande põhimõtet, tuleb sisestada ainult astmelised kulumuudatused.

## <a name="guidelines-for-defining-the-simulation-costing-version"></a>Juhised simuleeriva kuluversiooni määratlemiseks
Kasutage simulatsioonideks kuluversiooni määratlemisel järgmisi juhiseid.

-   Määrake suvandi **Planeeritud kulud** kulu tüüp.
-   Määrake kuluversioonile selgitav identifikaator, nt **Simulatsioon**.
-   Veenduge, et sisu sisaldab kulukirjeid.
-   Lubage kulukirjete sisestus. Ärge blokeerige ootel kulude sisestust.
-   Lubage kõigile saitidele kulukirjete sisestust. Saidi määramisel piirate kulukirjete sisestamist sellele saidile.
-   Takistage ootel kulude aktiveerimist. Kuluversiooni simulatsioonis tuleb kulukirjete jaoks sisestada ainult ootel kulud.
-   Ärge sisestage alguskuupäeva. Arvutamiskuupäev sisestatakse iga koosluse kalkulatsiooni jaoks, mis kasutab kuluversiooni simulatsiooni.
-   Määrake suvandi **Praegu aktiivne** taande põhimõte. Taande põhimõte võimaldab sisestada astmelise kulumuudatuse simulatsiooni eesmärgil, kuid kasutab praegu aktiivseid kulusid kõigi muude kulukirjete allikana. Eeldame, et kõik praegu aktiivsed kulud on olemas kõigi muude kulukirjete jaoks.
-   Määrake **versiooni omahinna** omahinna mudel, kuid ärge piirake kalkulatsioone. Näiteks võivad simulatsioonid kasutada **koosluse kalkulatsioonigrupi** omahinna mudelit, et näidata püsikulu andmete allikat ostetud kaupade puhul.
-   Määrake **mitme taseme** koosnevusrežiim, kuid ärge piirake kalkulatsioone. Simulatsioonid saavad kasutada teisi koosnevusrežiime.

## <a name="costing-versions"></a>Kuluversioonid
Järgmised stsenaariumid illustreerivad kuluversiooni simulatsiooni kasutamist, et simuleerida kulumuudatuste mõju. Enne kulumuudatuse simulatsiooni sisestamist kustutage kuluversiooni simulatsioonis olevad ootel kulukirjed, et alustaksite n-ö puhtalt lehelt. Kasutage lehte **Kauba hind**, et vaadata ja kustutada ootel kulukirjeid, mis on seotud kauba hindade ja kulukategooria hindadega.

-   Simuleerige ostetud kauba kulu muutmist. Näiteks kulumuudatus võib kajastada oluliste ostetud materjalide kulude eeldatavat kasvu või kahanemist. Ostetud kauba erineva kulu määramiseks kasutage lehte **Kauba hind**, et sisestada kuluversiooni simulatsiooni ootel kulukirje.
-   Simuleerige kulukategooria kulu muutmist. Näiteks kulumuudatus võib kajastada operatsiooniressursside töö- või tunnimäärade eeldatavat kasvu või kahanemist. Kulukategooria erineva kulu määramiseks kasutage lehte **Kulukategooria hind**, et sisestada kuluversiooni simulatsiooni ootel kulukirje.
-   Simuleerige kulu muutumist kaudse kulu kalkulatsiooni valemis. Näiteks võib kulumuudatus kajastada tootmise üldkulude eeldatavat kasvu või kahanemist. Muutuse määramiseks kaudse kulu kalkulatsiooni valemis kasutage lehte **Kuluarvestuse lehe seadistus**, et sisestada kuluversiooni simulatsioonis olev ootel kulukirje ning kontrollida ja salvestada muudatus.

Pärast kulumuudatuste simulatsiooni sisestamist arvutage toodetavate kaupade kulud, mida kulumuudatused mõjutavad. Kasutage kuluversiooni simulatsiooni jaoks lehte **Kalkulatsioon** ja määrake valitud toodetud kaubad, mida kulumuudatused mõjutavad. Koosluse arvutusi rakendatakse kõigi toodetavate kaupade puhul, v.a juhul, kuivalite kindlad kaubad. Teise võimalusena saate koosluse kalkulatsiooni valikut kasutada kasutuskoha värskenduste jaoks. Vaadake kuluversiooni simulatsioonis olevaid kauba kulukirjeid, et analüüsida, kuidas simuleeritud kulumuudatused valitud toodetavate kaupade kulusid mõjutasid. Kasutage kulude vaatamiseks ja analüüsimiseks lehte **Kauba hind** ja lehte **Kauba kulu arvutamine**.



