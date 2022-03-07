---
title: NF-e kohandatud serdi kontrollimine
description: Selles teemas antakse teavet NF-e kohandatud serdi lubamise ja kasutamise kohta.
author: gionoder
ms.date: 07/29/2021
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
ms.openlocfilehash: 8144e16b127bdbe954ef44f52c5ac71689a2036e6085e9a4ccc8bb17f91ae9b8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755587"
---
# <a name="nf-e-custom-certificate-validation"></a>NF-e kohandatud serdi kontrollimine

[!include [banner](../includes/banner.md)]

Omadus **Serveri autentimise eesmärk** Brasiilia juursertifikaadi väljaandjatest väljastatud sertifikaatidest on vaikimisi välja lülitatud ja see peab olema käsitsi lubatud. Mõnel juhul võib automaatne serdi värskendamine selle atribuudi ära keelata. Sellisel juhul on TLS-ühendus mõjutatud ning pole enam usaldusväärne. See mõjutab võimalust väljastada Brasiilia elektroonilise fiskaaldokumendi mudelit 55 (NF-e) Minas Gerais (MG) ja Paraná (PR) osariikide tootmiskeskkondade kohta.

**NF-e kohandatud serdi kinnitamise paranduse** lubamiseks minge **funktsioonihaldusesse**. See funktsioon võimaldab alternatiivset lahendust V5 ja V10 serdi valideerimiseks ning võimaldab usaldusväärset ühendust veebiteenustega, mis on vajalikud NF-e turvaliseks edastamiseks ja SEFAZ autoriseerimise saamiseks.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
