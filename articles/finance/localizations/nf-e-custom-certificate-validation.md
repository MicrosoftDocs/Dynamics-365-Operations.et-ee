---
title: NF-e kohandatud serdi kontrollimine
description: Selles teemas antakse teavet NF-e kohandatud serdi lubamise ja kasutamise kohta.
author: gionoder
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 3efa05f49748f6bbff680f322a77cec24da46c0c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240575"
---
# <a name="nf-e-custom-certificate-validation"></a>NF-e kohandatud serdi kontrollimine

[!include [banner](../includes/banner.md)]

NF-e kohandatud serdi kontrollimise funktsiooni sisselülitamisel lubab kohandatud kontrollimine ühenduse veebiteenustega. See ühendus on vajalik, et edastada NF-e ja lasta SEFAZ-il see autoriseerida.

Serdi V5 atribuudi **Serveri autentimise eesmärk** väljastab Brasiilia juurserdiamet. See atribuut on vaikimisi välja lülitatud ja tuleb lubada käsitsi. Mõnel juhul võib automaatne serdi värskendamine selle atribuudi ära keelata. Sellisel juhul on TLS-ühendus mõjutatud ning pole enam usaldusväärne. Samuti on mõjutatud võime väljastada NF-e-sid tootmiskeskkondades maakondade Minas Gerais (MG) ja Paraná (PR) jaoks.

See värskendus võimaldab serte kontrollida teisel viisil, mis tähendab, et on võimalik luua turvaline ühendus.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]