---
title: NF-e kohandatud serdi kontrollimine
description: Selles teemas antakse teavet NF-e kohandatud serdi lubamise ja kasutamise kohta.
author: gionoder
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 895513f51798a797ebf59f8a5be4f5cde006726d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813964"
---
# <a name="nf-e-custom-certificate-validation"></a>NF-e kohandatud serdi kontrollimine

[!include [banner](../includes/banner.md)]

NF-e kohandatud serdi kontrollimise funktsiooni sisselülitamisel lubab kohandatud kontrollimine ühenduse veebiteenustega. See ühendus on vajalik, et edastada NF-e ja lasta SEFAZ-il see autoriseerida.

Serdi V5 atribuudi **Serveri autentimise eesmärk** väljastab Brasiilia juurserdiamet. See atribuut on vaikimisi välja lülitatud ja tuleb lubada käsitsi. Mõnel juhul võib automaatne serdi värskendamine selle atribuudi ära keelata. Sellisel juhul on TLS-ühendus mõjutatud ning pole enam usaldusväärne. Samuti on mõjutatud võime väljastada NF-e-sid tootmiskeskkondades maakondade Minas Gerais (MG) ja Paraná (PR) jaoks.

See värskendus võimaldab serte kontrollida teisel viisil, mis tähendab, et on võimalik luua turvaline ühendus.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]