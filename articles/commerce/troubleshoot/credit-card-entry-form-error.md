---
title: Krediitkaardi sisestamise lehel kuvatakse väljaregistreerimisel tõrge
description: See artikkel annab tõrkeotsingu juhised, mis aitavad, kui makseviisi jaotist ei laadita ja kuvatakse tõrketeade.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 25f0dde83efff7c1d9a2a456270f5d48047f44ba
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269751"
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
