---
title: Kassajääk
description: Selles teemas kirjeldatakse, kuidas rahavoo prognoosimise funktsioon prognoosib organisatsiooni sularahajäägi konkreetsetel aegadel. Lisaks kirjeldab see valikuid, mis on saadaval erinevatel ajavahemikel prognooside kuvamiseks.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: bf99ce5c9de00061cba2f49d00cc9dbc728753a8
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752876"
---
# <a name="cash-position"></a>Kassajääk

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Sularahajääk on lühiajalise prognoosi rahavoo projektsioon. See põhineb laekumata arvete ja tellimuste eest tasuvate kliendilt sularaha sissetulekute projektsioonil ning sularaha väljamaksete projektsioonil, mis makstakse hankijatele arvete ja tellimuste ostude eest.

Kui süsteem prognoosib kliendimakseid, kasutab see makse prognoosimiseks kliendi makseprognooside funktsiooni. Ilma makseprognoosideta kasutatakse maksekuupäeva arvutamiseks iga kliendi puhul kliendiarve makseks teisendamisele nõutavat keskmist aega. Avatud klienditellimuste puhul arvutab süsteem arve kuupäeva kasutades arveldatavate klientide tellimuse rea keskmist päevade arvu. Seejärel kasutab see arve kuupäeva makse prognoosimise funktsiooni sisendina. Kliendimakse prognoosimise funktsioon arvutab iga tellimuserea maksekuupäeva. 

Tasumata arvete maksekuupäev hinnatakse ligikaudselt makseprognoosi algusest, valides kuupäeva, mis vastab kumulatiivse jaotuse funktsiooni viiekümnendikule.

Hankijatele maksmise prognoosimiseks kasutatakse sarnast lähenemist. Iga hankija puhul arvutab süsteem keskmise aja, mis on vajalik hankija arve makseks teisendamiseks. Seda päevade arvu kasutatakse seejärel maksekuupäeva arvutamiseks. Avatud hankija tellimuste puhul arvutab süsteem arve kuupäeva, võttes arvesse keskmise päevade arvu, mis on nõutav iga hankija puhul tellimuse ridade arveks teisendamiseks. Süsteem arvutab seejärel maksekuupäeva, kasutades keskmist aega, et teisendada hankija arve iga hankija puhul makseks.

Vahekaardi **sularahajääk** ülemine jaotis sisaldab sularahajäägi diagrammi. Sellel diagrammil kuvatakse sularaha sissetulekud ja väljaminekud ning nende mõju likviidsuse lõppsaldole. Sularahajäägi graafiku üksikasju saab vaadata iga päev, kord nädalas, kord kuus või kord kvartalis. Kui valite suvandi **Iga päev**, saate vaadata järgmise 21 päeva prognoose. Kui valite suvandi **Iga nädal**, saate vaadata järgmise 20 nädala prognoose. Kui valite suvandi **Iga kuu**, saate vaadata järgmise 12 kuu prognoose. Kui valite suvandi **Iga kvartal**, saate vaadata järgmise 12 kvartali prognoose. Kui vajate vahekaardi **Sularahajääk** sisu vaatamiseks ekraanil rohkem ruumi, saate graafiku peita.

Vahekaardi **Sularahajääk** alumine osa kuvav ametikoha, rahavoo, projitseeritud maksete ja pangakonto üksikasjad.

- Teave ruudustikud **Ametikoha üksikasjad** on esitatud kolmes jaotises: likviidsuskontode loend, raha sissetuleku moodustavate dokumentide loend ja sularaha väljaminekute loendi moodustavate dokumentide loend. Ruudustikus kuvatakse ka sularahajäägi saldod. Esimese vaadeldava perioodi likviidsete kontode saldo on algsaldo. Järgnevate perioodide jooksul arvutatakse likviidsuse kontode saldod sularaha sissetulekute lisandumise ja sularaha väljaminekute vähenemise põhjal võrreldes eelmiste perioodidega. Saldo moodustavate kannete üksikasjade vaatamiseks valige link **Saldo**.
- Ruudustik **Rahavoogude ruudustik** näitab sularaha sissevoolu ja sularaha väljavoolu perioodi kohta ning nende mõju likviidsuse konto saldodele. Esimese perioodi likviidsete kontode saldo on algsaldo. Järgnevate perioodide jooksul arvutatakse likviidsuse kontode saldod sularaha sissetulekute lisandumise ja sularaha väljaminekute vähenemise põhjal võrreldes eelmiste perioodidega.
- Ruudustik **Prognoositud panga saldo** ruudustik näitab eeldatavaid sularaha väljaminekuid ja nende mõju likviidsuse kontodele.
- Ruudustik **Pangakonto** kuvab eeldatava sularaha sissetulekute ja väljaminekute mõju pangasaldole.

Sularahajäägi salvestamiseks ja redigeerimiseks looge hetktõmmis. Lisateavet selle kohta, kuidas hetktõmmistega töötada, vt teemast [Hetktõmmiste ülevaade](payment-snapshots.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
