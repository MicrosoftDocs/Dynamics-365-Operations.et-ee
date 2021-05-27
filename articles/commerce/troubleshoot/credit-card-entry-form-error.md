---
title: Krediitkaardi sisestamise lehel kuvatakse väljaregistreerimisel tõrge
description: See teema annab tõrkeotsingu juhised, mis aitavad, kui makseviisi jaotist ei laadita ja kuvatakse tõrketeade.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ea9105481e6c5812565f0d3604906c905bcb5443
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018502"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>Krediitkaardi sisestamise lehel kuvatakse väljaregistreerimisel tõrge

[!include [banner](../../includes/banner.md)]

See teema annab tõrkeotsingu juhised, mis aitavad, kui **makseviisi jaotist** ei laadita ja kuvatakse tõrketeade.

## <a name="description"></a>Kirjeldus

Kui avate e-poe väljaregistreerimise lehekülje, ei laadita **makseviisi jaotist** ja kuvatakse järgmine tõrketeade: "Midagi läks valesti. Proovige hiljem uuesti.”

![Maksemooduli tõrge](media/payment-module-error.jpg)

## <a name="resolution"></a>Eraldusvõime

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>Oodake, kuni Commerce Scale Unit vahemälu aegub

E-poe väljaregistreerimise lehel olevad makseteenuse sätted salvestatakse vahemällu Commerce Scale Unit ja selle kuvamiseks e-kaubanduse saidil võib aega võtta kuni 15 minutit. Need makseteenuse sätted hõlmavad kaupmehe konto ID, pilve API võtme ja erinevate makseviisiga seotud konfiguratsioonisätete muudatusi.

## <a name="additional-resources"></a>Lisaressursid

[Võrgukanali häälestamine](../channel-setup-online.md)
