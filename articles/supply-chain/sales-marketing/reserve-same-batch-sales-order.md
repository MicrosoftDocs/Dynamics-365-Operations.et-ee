---
title: Sama partii reserveerimine müügitellimuse jaoks
description: Selles artiklis selgitatakse, kuidas seadistada toodet lubama varude reserveerimist üksiku varude partii suhtes.
author: omulvad
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e0937be76aa687ed986ff83e67f2db3e2dadd0f0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807652"
---
# <a name="reserve-the-same-batch-for-a-sales-order"></a>Sama partii reserveerimine müügitellimuse jaoks

[!include [banner](../includes/banner.md)]

Selles artiklis selgitatakse, kuidas seadistada toodet lubama varude reserveerimist üksiku varude partii suhtes.

Sama partii reserveerimisel saate reserveerida müügitellimuse rea varusid ühe varupartii suhtes. Näiteks võib tapeeti telliv klient soovida, et kogu tellimus täidetaks samast partiist, et vältida rullidevahelist erinevust. Toote seadistamiseks nii, et kasutataks sama partii reserveerimist, peavad järgmised sätted olema tootele määratavas kauba mudeligrupis, jälgimisdimensioonide grupis ja laoala dimensioonigrupis aktiivsed.

- **Kauba mudeligrupid** – kauba mudeligrupil peavad olema varude poliitikate väljagrupis **Reserveerimine** valitud väljad **Sama partii valimine** ja **Konsolideeri vajadus**.
- **Jälgimisdimensioonide grupid** – jälgimisdimensiooni grupil peab olema partiinumbri puhul valitud väli **Laovarude planeerimine dimensioonide kaupa**.
- **Laodimensioonide grupid** – laodimensiooni grupil peab olema väljadele **Laoala** ja **Ladu** valitud väli **Laovarude planeerimine dimensioonide kaupa**.

Kui reserveerite sama partii valikuga müügitellimuse real olevale tootele varusid, püüab süsteem reserveerida tellitud koguse ühest varude partiist. Arvestatakse ka konkreetse partii atribuudi nõudeid. Kui kogust ei saa ühest partiist täita, kuvatakse leht **Sama partii reserveerimise konflikt**. See leht kirjeldab probleeme ja ka tegevusi, mida saate reserveerimise jätkamiseks teha. Järgmised tingimused võivad partii reserveerimist takistada.

- Partii likvideerimiskoodil on müügi väljal **Blokeeri reserveering** lipp **Blokeeritud**.
- Partii on aegumiskuupäeva ja kehtivate kliendi müümispäevade alusel aegunud. Kaupa saab siiski reserveerimisel arvestada, kui kauba mudeligrupp on selle kauba puhul arvestatakse „esimesena aegunud esimesena välja” (FEFO) kuupäeva ja kui komplekteerimise kriteeriumina on valitud parim-enne kuupäev.
- Partiil pole jäänud järele piisavalt kõlblikkusaja päevi, tuginedes aegumiskuupäevale ja parim-enne kuupäevale, millele on liidetud kliendi müümispäevad.

Laoala dimensiooni grupiga seostatud kaupade puhul, millel on lubatud suvand **Kasuta laohaldusprotsesse**, saate reserveerida kindlaid partiinumbreid, kasutades reserveerimishierarhiat, kus partiinumbri varude dimensioon on määratletud asukohadimensiooni kohal. Seda tüüpi reserveerimishierarhiat nimetatakse ka *Partiiüle\[asukoht\]* reserveerimishierarhiaks. Müügi ja ülekandetellimuse ridade lehel **Partii reserveerimine** saate ka valida ja reserveerida mitu rida saadaolevate partiinumbrite põhjal. Lisateabe saamiseks selle kohta, mida teha, kui kasutate reserveerimishierarhiat, kus partiinumbri dimensioon on asukoha (*Partiiüle\[asukoht\]*) all, vaadake teemat [Paindlik dimensiooni reserveerimise poliitika laotaseme](../warehousing/flexible-warehouse-level-dimension-reservation.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
