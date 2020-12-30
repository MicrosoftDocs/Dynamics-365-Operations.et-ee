---
title: Laotöö tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada laotööga tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.
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
ms.openlocfilehash: a00ae517ff583e4231099d8e9f5d5b5a696cf7f7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645789"
---
# <a name="troubleshoot-warehouse-work"></a>Laotöö tõrkeotsing

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas lahendada laotööga tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a>Ma ei saa liigutada identifitseerimisnumbrid seerianumbriga kaupadega, kui jälgimise dimensiooni grupis on tühi väljaminek ja tühi sissetulek lubatud.

### <a name="issue-description"></a>Probleemi kirjeldus

Te ei saa teisaldada identifitseerimisnumbrit kasutades **Teisaldamine** menüükäsku, kui seerianumbril on jälgimise dimensiooni grupis *Tühjad väljaminekud lubatud* ja *Tühjad vastuvõtmised lubatud* ning kui mitu identifitseerimisnumbrit on samas asukohas, millest mõnel on seerianumbrid ja mõnel neist ei ole.

### <a name="issue-resolution"></a>Probleemi lahendamine

See probleem parandatakse muudatustega, mida kasutatakse [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687). Need muudatused muudavad **Seerianumbri** välja valikuliseks, kui tühi sissetulek ja tühi väljaminek on lubatud.

## <a name="i-receive-the-following-error-message-in-the-warehouse-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a>Kui teisaldamise töötlemisel kuvatakse lao rakenduses järgmine tõrketeade: "Lao omanik %1 pole selles protsessis lubatud."

### <a name="issue-description"></a>Probleemi kirjeldus

**Omaniku** jälgimise dimensioon puudub, kui liikumiste tegemiseks kasutatakse lao rakendust. Regulaarne lao ülekandmise tööleht Supply Chain Management rakendusest näib töötavad plaanipäraselt ja seda saab sisestada ainult siis, kui **Omaniku** dimensioon on täidetud.

### <a name="issue-resolution"></a>Probleemi lahendamine

Microsoft on seda probleemi hinnanud ja on määranud, et see on funktsiooni piirang. Praegu toetavad laohalduse protsessid ainult selle juriidilise isiku omanduses olevat laovaru.
