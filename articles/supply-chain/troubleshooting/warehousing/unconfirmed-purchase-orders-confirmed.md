---
title: Toote sissetulekute ülesande värskendamine kinnitab kinnitamata tellimused
description: Pärast toote sissetulekute värskendamise käivitamist kinnitab süsteem kinnitamata tellimused, mille olekuks on märgitud registreeritud. Lugege funktsiooni kohta, mis selle probleemi parandab.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 171a978efc6b55b92f429381e72036cb1b3296c6
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476085"
---
# <a name="unconfirmed-purchase-orders-are-confirmed-after-running-update-product-receipts"></a>Kinnitamata ostutellimused kinnitatakse pärast toote sissetulekute värskendamise käitamist

## <a name="symptoms"></a>Sümptomid

Pärast seda, kui käivitate *Toote sissetulekute uuendamise* perioodilise ülesande, kinnitab süsteem automaatselt kinnitamata ostutellimused, millel on lao kande olek *Registreeritud*.

## <a name="resolution"></a>Lahendus

Uus sissetuleva koorma käitlemise funktsioon *Koorma koguste ülelaekumine* lahendab selle probleemi. Selle funktsiooni sisselülitamiseks minge [Funktsioonihaldus](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) tööruumi ja lülitage sisse järgmised funktsioonid samas järjekorras nagu need on loetletud:

1. Ostutellimuse varude kannete seostamine koormusega
2. Koorma koguste liigne vastuvõtt

Lisateavet vt teemast [Registreeritud toodete koguste sisestamine ostutellimuste eest](/dynamics365/supply-chain/warehousing/inbound-load-handling).
