---
title: NF-e kohandatud serdi kontrollimine
description: See artikkel annab teavet NF-e kohandatud serdi lubamise ja kasutamise kohta.
author: gionoder
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: f78fdbd133aecaf9dbf8abe0006abd6deb1b1b15
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288540"
---
# <a name="nf-e-custom-certificate-validation"></a>NF-e kohandatud serdi kontrollimine

[!include [banner](../includes/banner.md)]

Omadus **Serveri autentimise eesmärk** Brasiilia juursertifikaadi väljaandjatest väljastatud sertifikaatidest on vaikimisi välja lülitatud ja see peab olema käsitsi lubatud. Mõnel juhul võib automaatne serdi värskendamine selle atribuudi ära keelata. Sellisel juhul on TLS-ühendus mõjutatud ning pole enam usaldusväärne. See mõjutab võimalust väljastada Brasiilia elektroonilise fiskaaldokumendi mudelit 55 (NF-e) Minas Gerais (MG) ja Paraná (PR) osariikide tootmiskeskkondade kohta.

**NF-e kohandatud serdi kinnitamise paranduse** lubamiseks minge **funktsioonihaldusesse**. See funktsioon võimaldab alternatiivset lahendust V5 ja V10 serdi valideerimiseks ning võimaldab usaldusväärset ühendust veebiteenustega, mis on vajalikud NF-e turvaliseks edastamiseks ja SEFAZ autoriseerimise saamiseks.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
