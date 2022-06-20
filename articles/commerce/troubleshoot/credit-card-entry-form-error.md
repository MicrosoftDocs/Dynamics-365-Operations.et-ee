---
title: Krediitkaardi sisestamise lehel kuvatakse väljaregistreerimisel tõrge
description: See artikkel annab tõrkeotsingu juhised, mis aitavad, kui makseviisi jaotist ei laadita ja kuvatakse tõrketeade.
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
ms.openlocfilehash: 6d1f7ba2d1a63430431af94ed4bed3222c85f14d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910439"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>Krediitkaardi sisestamise lehel kuvatakse väljaregistreerimisel tõrge

[!include [banner](../../includes/banner.md)]

See artikkel annab tõrkeotsingu juhised, mis aitavad, **kui makseviisi** jaotist ei laadita ja kuvatakse tõrketeade.

## <a name="description"></a>Kirjeldus

Kui avate e-poe väljaregistreerimise lehekülje, ei laadita **makseviisi jaotist** ja kuvatakse järgmine tõrketeade: "Midagi läks valesti. Proovige hiljem uuesti.”

![Maksemooduli tõrge.](media/payment-module-error.jpg)

## <a name="resolution"></a>Lahendus

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>Oodake, kuni Commerce Scale Unit vahemälu aegub

E-poe väljaregistreerimise lehel olevad makseteenuse sätted salvestatakse vahemällu Commerce Scale Unit ja selle kuvamiseks e-kaubanduse saidil võib aega võtta kuni 15 minutit. Need makseteenuse sätted hõlmavad kaupmehe konto ID, pilve API võtme ja erinevate makseviisiga seotud konfiguratsioonisätete muudatusi.

## <a name="additional-resources"></a>Lisaressursid

[Võrgukanali häälestamine](../channel-setup-online.md)
