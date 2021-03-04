---
title: Broneeringute tõrkeotsing laohalduses
description: Selles teemas kirjeldatakse, kuidas lahendada lao broneerimistega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6151797001b1ccdb7e371c70b90c304a5ab422d8
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645115"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a>Broneeringute tõrkeotsing laohalduses

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas lahendada lao broneerimistega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a>Kuvatakse järgnev tõrge „Broneeringuid ei saa eemaldada, kuna loodud on töö, mis sõltub nendest broneeringutest”.

### <a name="issue-description"></a>Probleemi kirjeldus

Te ei saa varude broneerimist müügirealt maha võtta, kuna rea suhtes on avatud töö.

### <a name="issue-resolution"></a>Probleemi lahendamine

Uurige, kas avatud pakkimisgrupi töö on olemas, et tuua kaup pakkimisühiku teise asukohta (nt *Uks*). Vaadake üle kirjed **Töö loomise ajaloo logi** ja **Töö üksikasjade** lehtedel, et teha kindlaks, mis kaupa füüsiliselt broneerib, ja seejärel lõpetage või kustutage töö, et broneeringut vabastada.

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a>Kuvatakse järgmine tõrketeade: "Varude kogust -%1 ei saanud uuendada kauba %2 ebapiisavate kaubavaru kannete tõttu."

### <a name="issue-description"></a>Probleemi kirjeldus

See probleem võib ilmneda juhul, kui süsteem ei saa varude kogust värskendada, kuna pole piisavalt laokandeid, millel on määratud dimensioone. Siin on täieliku tõrketeate täistekst:

> Varude kogust -%1 ei saanud värskendada, kuna pole piisavalt laokandeid kaubaga %2, mille dimensioonid on suurus =%3, värvus =%4, täiendused =%5, sait =%6, ladu =%7, asukoht =%8, varude olek = saadaval, identifitseerimisnumber =%9, partii number =%10 ID-kood %11 saatepartii ID %12.

### <a name="issue-resolution"></a>Probleemi lahendamine

Veenduge, et varude kanded ei broneeriks kauba kogust füüsiliselt. Näiteks võivad need kanded avada kvaliteetseid tellimusi, lao blokeerimise kirjeid või väljaminekuordereid.

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a>Kuvatakse järgmine tõrketeade: "Füüsilist laoseisu... ei saa broneerida, kuna laos on saadaval ainult 0,00."

### <a name="issue-description"></a>Probleemi kirjeldus

See probleem võib ilmneda juhul, kui süsteem ei saa varude kogust värskendada, kuna pole piisavalt laokandeid, millel on määratud dimensioone. Siin on täieliku tõrketeate täistekst:

> Füüsiline vaba kaubavaru sait=%1, ladu=%2, varude olek=saadaval, partii number=%3, omanik=%4: %5 ei saa broneerida, kuna laos on saadaval ainult 0,00.

### <a name="issue-resolution"></a>Probleemi lahendamine

See probleem on tõenäoliselt põhjustatud avatud tööst. Lõpetage töö või võtke vastu ilma töö loomiseta. Veenduge, et varude kanded ei broneeriks kauba kogust füüsiliselt. Näiteks võivad need kanded olla avatud kvaliteetsed tellimused, lao blokeerimise kirjed või väljamineku tellimused.

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a>Kuvatakse järgmine tõrketeade: "Kui soovite määrata voo, peavad koorma read määrama dimensioonid asukoha kohal. Nende dimensioonide määramiseks broneerige ja looge uuesti koorma rida."

### <a name="issue-description"></a>Probleemi kirjeldus

Kui kasutate kaupa, millel on "partii eespool" broneerimise hierarhia (mille **partiinumbri** dimensioon on paigutatud *enne* **Asukoha** dimensiooni), ei tööta osalise koguse jaoks **Väljasta lattu** käsklus **Koorma plaanimise töölaua** lehel. Te saate selle tõrketeate ja ükski töö ei ole loodud osalise koguse jaoks.

Kui aga kasutate kaupa, millel on "partii allpool" broneerimise hierarhia (mille **partiinumbri** dimensioon on paigutatud *allapoole* **Asukoha** dimensiooni), saate väljastada osalise koguse **Koorma plaanimise töölaua** lehel.

### <a name="issue-resolution"></a>Probleemi lahendamine

Selline käitumine on nii kavandatud. Kui asetate broneerimise hierarhias dimensiooni **Asukoha** dimensioonist ettepoole, peab see olema määratud enne lattu väljastamist. Microsoft on seda probleemi hinnanud ja on määranud, et see on funktsiooni piirang koorma planeerimise töölaualt lattu väljastamise ajal. Osalisi koguseid ei saa väljastada, kui ühe või mitme dimensiooni **Asukoht** on määramata.

Lisateavet vt [Paindlik dimensiooni broneerimise poliitika laotasemel](flexible-warehouse-level-dimension-reservation.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]