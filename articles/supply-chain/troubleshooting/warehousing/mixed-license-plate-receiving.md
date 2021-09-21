---
title: Kasutatav kombineeritud identifitseerimisnumber ei tööta kõigi koodide puhul
description: Kui likvideerimise koodi Tegevuse välja väärtuseks on seatud Krediit või Praak, saate tagastatud kaupade töötlemiseks kasutada ainult Kombineeritud identifitseerimisnumbri vastuvõtmise menüükäsku.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b762255bc5ef6a1e15688a9c635940e92e67db3c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476145"
---
# <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-but-credit"></a>Kasutatav kombineeritud identifitseerimisnumber ei tööta ühegi likvideerimise koodi, v.a krediidi puhul

## <a name="symptoms"></a>Sümptomid

Kui likvideerimise koodi **Tegevuse** välja väärtuseks on seatud *Krediit* või *Praak*, saate tagastatud kaupade töötlemiseks kasutada ainult [Kombineeritud identifitseerimisnumbri vastuvõtmise](/dynamics365/supply-chain/warehousing/mixed-license-plate-receiving) menüükäsku.

## <a name="resolution"></a>Lahendus

Microsoft on seda probleemi hinnanud ja on määranud, et see on funktsiooni piirang. Hetkel toetatakse kombineeritud identifitseerimisnumbri vastuvõtmiseks ainult [likvideerimiskoode](/dynamics365/supply-chain/service-management/set-up-disposition-codes), mille puhul on **Tegevuse** välja väärtuseks seatud *Krediit* või *Praak*.
