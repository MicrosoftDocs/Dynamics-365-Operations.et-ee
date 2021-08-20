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
ms.openlocfilehash: 8ff8fae0bb20b11b15c7520fbb14727ff0372ca0255adc82599c6680a64671af
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748711"
---
# <a name="unified-number-sequence-for-job-ids"></a>Töö ID-de ühtsed numbrijärjestused

[!include [banner](../includes/banner.md)]

See funktsioon pakub ühte ühtset numbriseeriat, mis loob töö ID-d tootmisjuhtimise, tootmise käivitamise ja aja ja kohaloleku moodulite jaoks. Varem oli teil võimalik valida iga mooduli jaoks erinev numbriseeria, mis võib põhjustada vastuolulisi töö ID-sid, kui vähemalt kaks nendest seeriatest kasutab identset vormingut. Selline konflikt võib põhjustada andmete rikkumist.

## <a name="turn-on-this-feature-for-your-system"></a>Selle funktsiooni sisselülitamine teie süsteemi jaoks

Kui teie süsteemis ei ole veel selles teemas kirjeldatud funktsiooni, avage [Funktsioonihaldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja lülitage funktsioon *Töö ID-de ühtne numbrijärjestus* sisse.

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a>Töö ID-de jaoks seadistage ühtne numbrijada

Pärast selle funktsiooni lubamist tühistatakse tootmise juhtimise, tootmise teostamise ning aja ja kohaloleku moodulite parameetrite lehtedel olevad **Töö identifitseerimine** numbrijada sätted ja uus **Ühtne töö ID** väli lisatakse. **Ühtne töö ID** väärtus jagatakse kõigi kolme mooduliga, mis tagab, et kõik moodulid viitavad samale numbriseeriale. Töö ID-d on seetõttu kõigi kolme mooduli osas unikaalsed ja konflikti ei teki kunagi.

Töö ID-de jaoks ühtse numbrijada seadistamiseks toimige järgmiselt.

1. Lülitage funktsioon sisse, nagu kirjeldatud eelmises jaotises.
1. Määrake numbriseeria, mida soovite kasutada oma ühtsete töö ID-de jaoks, või looge uus. Lisateabe saamiseks vt teemat [Numbriseeriate ülevaade](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).
1. Minge **Tootmise juhtimise parameetrid**, **Tootmise käivitamise parameetrid** või **Kellaaja ja kohalviibimise parameetrid** lehele. Pole tähtis, kumba valite, sest kui teete selle sätte mõnel neist lehtedest, värskendatakse kõiki teisi lehti automaatselt.
1. Avage valitud parameetrite lehel vahekaart **Numbriseeriad**.
1. Määrake **numbriseeria kood**, mille määratlesite eelnevalt ruudustiku reale **Ühtne töö ID**.
