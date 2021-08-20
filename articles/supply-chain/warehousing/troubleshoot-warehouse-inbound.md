---
title: Saabuvate kaupade laotoimingute tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada saabuvate kaupade laotoimingutega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.
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
ms.openlocfilehash: 6d7fcb2ed32c57b8701bee5b90889a0a63e1f7061aa9014480ae8c543e1f229a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748663"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a>Saabuvate kaupade laotoimingute tõrkeotsing

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas lahendada saabuvate kaupade laotoimingutega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a>Kuvatakse järgmine tõrketeade: "Kvaliteetne tellimus %1 on loodud. Kogumiprofiili ei leitud, kontrollige oma konfiguratsiooni."

### <a name="issue-description"></a>Probleemi kirjeldus

See tõrketeade on seotud vastuvõtu protsessiga, kus kvaliteedijuhtimine (QMS) on sisse lülitatud. Sõltuvalt teie keskkonna konfiguratsioonist võib lisateave tõrkesõnumit tekitava tehingu kohta aidata probleemi lahendada.

### <a name="issue-resolution"></a>Probleemi lahendamine

Esmalt vaadake üle [kogumi komplekteerimise](set-up-cluster-picking.md) seadistus ja veenduge, et teie kogumiprofiilid on õigesti seadistatud. Te ei saa kasutada mobiilse seadme menüükäsku kogumi komplekteerimiseks, kui pole kogumiprofiilid ei ole seadistatud. Sõltuvalt teie keskkonnast võib olla ka võimalik üle vaadata teisi seotud konfiguratsioone.

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a>Kasutatav kombineeritud identifitseerimisnumber ei tööta ühegi likvideerimise koodi, v.a krediidi puhul.

### <a name="issue-description"></a>Probleemi kirjeldus

Kui likvideerimise koodi **Tegevuse** välja väärtuseks on seatud *Krediit* või *Praak*, saate tagastatud kaupade töötlemiseks kasutada ainult [Kombineeritud identifitseerimisnumbri vastuvõtmise](mixed-license-plate-receiving.md) menüükäsku.

### <a name="issue-resolution"></a>Probleemi lahendamine

Microsoft on seda probleemi hinnanud ja on määranud, et see on funktsiooni piirang. Hetkel toetatakse kombineeritud identifitseerimisnumbri vastuvõtmiseks ainult [likvideerimiskoode](../service-management/set-up-disposition-codes.md), mille puhul on **Tegevuse** välja väärtuseks seatud *Krediit* või *Praak*.

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a>Kui ma käitan vastuvõetud toodete perioodilise ülesande värskendamist, kinnitatakse kinnitamata ostutellimused.

### <a name="issue-description"></a>Probleemi kirjeldus

Pärast seda, kui käivitate *Toote sissetulekute uuendamise* perioodilise ülesande, kinnitab süsteem automaatselt kinnitamata ostutellimused, millel on lao kande olek *Registreeritud*.

### <a name="issue-resolution"></a>Probleemi lahendamine

Uus sissetuleva koorma käitlemise funktsioon *Koorma koguste ülelaekumine* lahendab selle probleemi. Selle funktsiooni sisselülitamiseks minge [Funktsioonihaldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruum ja lülitage sisse järgmised funktsioonid (samas järjekorras nagu need on loetletud):

1. Ostutellimuse varude kannete seostamine koormusega
1. Koorma koguste liigne vastuvõtt

Lisateavet vt teemast [Registreeritud toodete koguste sisestamine ostutellimuste eest](inbound-load-handling.md#post-registered-quantities).

## <a name="when-i-register-inbound-orders-i-receive-the-following-error-message-the-quantity-is-not-valid"></a>Sissetulevate tellimuste registreerimisel kuvatakse järgmine tõrketeade: "Kogus on kehtetu".

### <a name="issue-description"></a>Probleemi kirjeldus

Kui väli **Litsentsiplaadi grupeerimise poliitika** on seatud väärtusele *Kasutaja määratud* mobiilse seadme menüükäsule, mida kasutatakse sissetulevate tellimuste registreerimiseks, saate tõrketeate ("Kogus on kehtetu") ja registreerimist ei saa lõpule viia.

### <a name="issue-cause"></a>Väljastamise põhjus

Kui *kasutaja määratletud* on kasutatud litsentsiplaadi grupeerimispoliitikana, tükeldab süsteem sissetulevad varud eraldi litsentsiplaatideks, nagu näitab ka ühiku seeriagrupp. Kui vastuvõetava kauba jälgimiseks kasutatakse partii- või seerianumbreid, tuleb iga partii või seerianumbri kogus registreerida registreeritud numbrimärgi kohta. Kui litsentsiplaadi jaoks määratud kogus ületab koguse, mis praeguste mõõtmete jaoks tuleb veel saada, kuvatakse tõrketeade.

### <a name="issue-resolution"></a>Probleemi lahendamine

Kui registreerite kauba mobiilse seadme menüü-üksuse abil, kus väli **Litsentsiplaadi grupeerimise poliitika** väärtuseks on seatud *Kasutaja määratud*, võib süsteem nõuda litsentsiplaadi numbrite, partii- või seerianumbrite kinnitamist või sisestamist.

Litsentsiplaadi kinnituslehel näitab süsteem praeguse litsentsiplaadi jaoks eraldatud kogust. Partii- või seeriakinnituse lehtedel näitab süsteem kogust, mis praegusel litsentsiplaadile peab veel laekuma. See hõlmab ka välja, kus saate sisestada koguse, et registreerida see litsentsiplaadi ja partii- või seerianumbri kombinatsioon. Sel juhul veenduge, et litsentsiplaadile registreeritav kogus ei ületaks vastuvõetud kogust.

Kui sissetuleva tellimuse registreerimisel luuakse liiga palju litsentsiplaate, saab välja **Litsentsiplaadi grupeerimise poliitika** väärtust muuta väärtuseks *Litsentsiplaadi grupeerimine*, määrata kaubale uus ühiku seeriagrupp või üksuse seeriagrupi suvand **litsentsiplaadi grupeerimise** inaktiveerida.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
