---
title: Väljuvate kaupade laotoimingute tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada väljuvate kaupade laotoimingutega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.
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
ms.openlocfilehash: 491803c5f9394f47a996c4e4c7fb8925e9464e644c99e5c1ab434706af6ad74e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756651"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a>Väljuvate kaupade laotoimingute tõrkeotsing

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas lahendada väljuvate kaupade laotoimingutega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a>Kuvatakse järgmine tõrketeade: "Müügitellimust ei saanud väljastada."

### <a name="issue-description"></a>Probleemi kirjeldus

See probleem võib ilmneda mitmel põhjusel. Näiteks on tellimus krediidihalduses ja ühtegi saadetist ei saa luua enne, kui kõigi müügitellimusega seotud müügiridade jaoks on sisestatud kehtiv postiaadress. Teise võimalusena võib olla ootel tellimus, millega tuleb tegeleda enne, kui tellimuse saab lattu väljastada. See ootele panemine võib olla seotud tellimusega või see võib olla tingitud kliendi kontost.

### <a name="issue-resolution"></a>Probleemi lahendamine

Lisage või värskendage aadressi müügitellimuse ja tellimuse ridadel ning seejärel väljastage tellimus lattu. Tellimusi saab lattu väljastada ainult siis, kui neil on kehtiv tarneaadress (iga **Organisatsiooni halduse** moodulis oleva aadressi vormingu seadistuse kohta).

Uurige tellimuse ootel olekut ja lahendage probleemid. Seejärel eemaldage ootele panemine tellimuselt või kliendilt ja väljastage tellimus lattu.

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a>Kuvatakse järgmine teade: "Saadetis koormale 1% on kinnitatud." Kuid ridu ei sisestata.

### <a name="issue-description"></a>Probleemi kirjeldus

Koorma saadetis on kinnitatud, kuid ei ole edasist sisestamist.

### <a name="issue-resolution"></a>Probleemi lahendamine

Saatmise kinnitus ei mõjuta sisestamist. See lihtsalt uuendab saadetise ja koorma olekut. Sisestamine peab toimuma eraldi protsessis.

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a>Kuvatakse järgmine tõrketeade: "Otsetarne ei ole võimeline töötlema ladu 1%, kuna see on lubatud laohalduseks. Määrake mõni muu ladu, mis pole laohalduse jaoks lubatud."

### <a name="issue-description"></a>Probleemi kirjeldus

Kaup lisatakse müügireal otsetarneks laost, mis on lubatud laohalduse jaoks (WMS). See tõrketeade kuvatakse müügirea uuendamisel. 

### <a name="issue-resolution"></a>Probleemi lahendamine

Microsoft on seda probleemi hinnanud ja on määranud, et see on funktsiooni piirang. Praegu ei toeta WMS otsetarnet. Seetõttu peate otsetarne kasutamiseks valima mitte-WMS kauba ja lao.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]