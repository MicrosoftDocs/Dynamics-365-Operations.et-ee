---
title: Saabuvate kaupade laotoimingute tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada saabuvate kaupade laotoimingutega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.
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
ms.openlocfilehash: 60b6e37ec9d716f635c2d25374ac25a82286660e
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645968"
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

Uus sissetuleva koorma käitlemise funktsioon *Koorma koguste ülelaekumine* lahendab selle probleemi. Lülitage see funktsioon sisse, minge [Funktsioonihaldusesse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja lülitage sisse järgmised funktsioonid (samas järjekorras nagu need on loetletud):

1. Ostutellimuse varude kannete seostamine koormusega
1. Koorma koguste liigne vastuvõtt

Lisateavet vt teemast [Registreeritud toodete koguste sisestamine ostutellimuste eest](inbound-load-handling.md#post-registered-quantities).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]