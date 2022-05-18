---
title: TDS-i eraldamisega maksegraafikute häälestamine
description: See teema kirjeldab, kuidas seadistada maksegraafikuid allika (TDS) eraldamisel mahaarvatud maksuga.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 63628e84da4e430df236f3afa89110b652110fcb
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726601"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a>TDS-i eraldamisega maksegraafikute häälestamine

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas seadistada maksegraafikuid allika (TDS) eraldamisel mahaarvatud maksuga.

1. Avage **Ostureskontro \> Makse seadistus \> Maksegraafikud**.

    [![Maksegraafikute leht.](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)

2. Tegevuspaanil valige **Uus** TDS-ile kinnipeetava maksu grupi loomiseks ja sisestage nõutavad üksikasjad.
3. Valige **Eraldamine** väljal meetod, mida kasutada makse eraldamiseks maksegraafiku jaoks:

    - Kokku
    - Fikseeritud summa
    - Fikseeritud kogus
    - Määratud

    **Kinnipeetava maksu eraldamise** väljal kuvatakse maksegraafiku TDS-i eraldamismeetod. Kui valite **Kokku** väljal **Eraldamine**, seatakse **Kinnipeetava maksu eraldamise** väljal automaatselt **Kokku**. Kui valite väljal **Fikseeritud summa**, **Fikseeritud kogus**, või **i Määratud** **Eraldamise** väljal, seatakse **Eraldamise** väärtuseks automaatselt **Proportsionaalne**.

    > [!NOTE]
    > Kui **Kinnipeetava maksu eraldamise** väli on seatud **Kokku**, siis arvutatakse makse osamaksed brutosumma alusel, mis sisaldabTDS-summat. Kui **Kinnipeetava maksu eraldamise** väli on seatud **Proportsionaalne**, siis arvutatakse makse osamaksed brutosumma alusel, mis sisaldabTDS-summat.

4. Sisestage vormile nõutavad üksikasjad ja siis sulgege leht.
