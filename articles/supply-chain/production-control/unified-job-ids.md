---
title: Töö ID-de ühtsed numbrijärjestused
description: See funktsioon pakub ühte ühtset numbriseeriat, mis loob töö ID-d tootmisjuhtimise, tootmise käivitamise ja aja ja kohaloleku moodulite jaoks.
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 301a4bb58f896a2dc0f0cddcd2e29344865ca898
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897541"
---
# <a name="unified-number-sequence-for-job-ids"></a>Töö ID-de ühtsed numbrijärjestused

[!include [banner](../includes/banner.md)]

See funktsioon pakub ühte ühtset numbriseeriat, mis loob töö ID-d tootmisjuhtimise, tootmise käivitamise ja aja ja kohaloleku moodulite jaoks. Varem oli teil võimalik valida iga mooduli jaoks erinev numbriseeria, mis võib põhjustada vastuolulisi töö ID-sid, kui vähemalt kaks nendest seeriatest kasutab identset vormingut. Selline konflikt võib põhjustada andmete rikkumist.

## <a name="turn-on-this-feature-for-your-system"></a>Selle funktsiooni sisselülitamine teie süsteemi jaoks

Kui teie süsteem ei kaasa juba selles artiklis [kirjeldatud funktsiooni,](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)*minge funktsioonihalduse ja lülitage* sisse töö ID-de funktsiooni ühtne numbriseeria.

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a>Töö ID-de jaoks seadistage ühtne numbrijada

Pärast selle funktsiooni lubamist tühistatakse tootmise juhtimise, tootmise teostamise ning aja ja kohaloleku moodulite parameetrite lehtedel olevad **Töö identifitseerimine** numbrijada sätted ja uus **Ühtne töö ID** väli lisatakse. **Ühtne töö ID** väärtus jagatakse kõigi kolme mooduliga, mis tagab, et kõik moodulid viitavad samale numbriseeriale. Töö ID-d on seetõttu kõigi kolme mooduli osas unikaalsed ja konflikti ei teki kunagi.

Töö ID-de jaoks ühtse numbrijada seadistamiseks toimige järgmiselt.

1. Lülitage funktsioon sisse, nagu kirjeldatud eelmises jaotises.
1. Määrake numbriseeria, mida soovite kasutada oma ühtsete töö ID-de jaoks, või looge uus. Lisateabe saamiseks vt teemat [Numbriseeriate ülevaade](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).
1. Minge **Tootmise juhtimise parameetrid**, **Tootmise käivitamise parameetrid** või **Kellaaja ja kohalviibimise parameetrid** lehele. Pole tähtis, kumba valite, sest kui teete selle sätte mõnel neist lehtedest, värskendatakse kõiki teisi lehti automaatselt.
1. Avage valitud parameetrite lehel vahekaart **Numbriseeriad**.
1. Määrake **numbriseeria kood**, mille määratlesite eelnevalt ruudustiku reale **Ühtne töö ID**.
