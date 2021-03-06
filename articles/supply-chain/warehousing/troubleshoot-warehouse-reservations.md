---
title: Broneeringute tõrkeotsing laohalduses
description: Selles teemas kirjeldatakse, kuidas lahendada lao broneerimistega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d0d73396772ed9e8397797d6685fb550d911303b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828102"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a>Broneeringute tõrkeotsing laohalduses

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas lahendada lao broneerimistega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.

Teemade kohta, mis on seotud partii- ja seerianumbri registreerimistega, vt [Lao partii ja seeria reserveerimise hierarhiate tõrkeotsing](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
