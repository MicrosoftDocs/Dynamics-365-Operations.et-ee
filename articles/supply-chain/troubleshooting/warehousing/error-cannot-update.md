---
title: Komplekteerimislehe registreerimise ajal asukoha valimisel ilmneb tõrge
description: Komplekteerimislehe registreerimise ajal asukoha valimisel ilmneb tõrge.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b7fc579821f9a80d94aea949fcc0301b9d8f6935
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026423"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a>Komplekteerimislehe registreerimise ajal asukoha valimisel ilmneb tõrge

KB number: 4613106

## <a name="symptoms"></a>Sümptomid

See probleem ilmneb, kui süsteem on konfigureeritud müügitellimusi automaatselt reserveerima. Kui püüate valida asukohta komplekteerimislehe registreerimisreale, saate laohalduse (WMS) reserveerimisprotsesside kasutamisel järgmise tõrketeate:

> Kogust ei saa uute dimensioonidega värskendada

See probleem võib ilmneda, kuna teil ei ole määratud asukohas piisavalt vaba kaubavaru.

## <a name="resolution"></a>Eraldusvõime

Süsteem käitub kavandatud viisil.

Stsenaariumides, kus kasutate laotaseme reserveerimisprotsessi, kui vaba kaubavaru ei reserveerita kõigil varude dimensioonitasemetel ja teil ei ole määratud asukohas piisavalt vaba kaubavaru, on soovitatav kasutada komplekteerimisrealt käsitsi reserveerimisprotsessi. Seejärel saate kasutada funktsiooni *Reserveeri partii* et jaotada madalamad reserveeringud, nt asukoht, kõigi vabade koguste puhul.
