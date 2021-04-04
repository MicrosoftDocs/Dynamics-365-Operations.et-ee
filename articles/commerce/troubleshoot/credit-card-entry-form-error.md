---
title: Krediitkaardi sisestamise lehel kuvatakse väljaregistreerimisel tõrge
description: See teema annab tõrkeotsingu juhised, mis aitavad, kui makseviisi jaotist ei laadita ja kuvatakse tõrketeade.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: f0751fc76e6eb4320f766886b4c1efcb1042e996
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585280"
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
