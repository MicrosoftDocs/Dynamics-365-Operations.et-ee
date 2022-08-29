---
title: Globaalse kinnipeetava maksu valuuta vahetuskursi tüübi ja kuupäevatüübi häälestuse lubamine
description: See artikkel selgitab, kuidas lubada kinnipeetava maksu valuuta vahetuskursi tüübi ja kuupäeva tüübi globaalne seadistus.
author: kailiang
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 41f12a33651c14439f3a59c5c2f2d34019dada2d
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229978"
---
# <a name="enable-the-global-withholding-tax-currency-exchange-rate-type-and-date-type-setup"></a>Globaalse kinnipeetava maksu valuuta vahetuskursi tüübi ja kuupäevatüübi häälestuse lubamine

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

See artikkel selgitab, kuidas lubada kinnipeetava maksu valuuta vahetuskursi tüübi ja kuupäeva tüübi globaalne seadistus. Nüüd saate kinnipeetava maksu valuutale valida sihtotstarbelise vahetuskursi tüübi ja vahetuskursi arvutamise kuupäeva tüübi. Need valikud määravad välisvaluuta vahetuskursi, mida kasutatakse kinnipeetava maksu summa arvutamiseks maksekannetes kinnipeetava maksu valuutas.

See funktsioon on saadaval versioonis Microsoft Dynamics 365 Finantsversioon 10.0.29 ja uuemas versioonis.

1. Minge maksu **seadistamise** \> **parameetrite** \> **pearaamatu** \> **parameetritesse.**
2. Seadke vahekaardil **Kinnipeetav** maks suvandi Luba **täiustatud kinnipeetava maksu valuuta väärtuseks** **Jah**.
3. **Väljal Vahetuskursi tüüp** valige kinnipeetava maksu valuutale vahetuskursi tüüp.
4. Väljal Arvutuskuupäeva **tüüp** valige arvutamiskuupäeva tüüp, mis määratleb kinnipeetava maksu valuuta vahetuskursi.

    - **Maksekuupäev** – määrake maksetöölehe sisestuskuupäeval põhinev vahetuskurss.
    - **Arve** kuupäev – määrake arve töölehe arvekuupäeval põhinev vahetuskurss. Kui kande arvekuupäev on tühi, kasutatakse arve sisestamise kuupäeva. 
    - **Dokumendi kuupäev** – määrake vahetuskurss maksetöölehe dokumendikuupäeva alusel. Kui kande dokumendikuupäev on tühi, kasutatakse maksekuupäeva.

5. Valige käsk **Salvesta**.

Kui kande valuuta erineb kinnipeetava maksu koodis määratletud kinnipeetava maksu valuutast, arvutatakse kinnipeetava maksu valuuta summa kande valuutast eelnevate sätete alusel ja salvestatakse sisestatud kinnipeetava maksu kannetesse.
