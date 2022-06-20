---
title: TDS-i eraldamisega maksegraafikute häälestamine
description: See artikkel selgitab, kuidas seadistada maksegraafikuid allika (TDS) eraldamisel mahaarvatud maksuga.
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
ms.openlocfilehash: 48891c32f39b743ce26e265c5682dab28ecb4b27
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868308"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a>TDS-i eraldamisega maksegraafikute häälestamine

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas seadistada maksegraafikuid allika (TDS) eraldamisel mahaarvatud maksuga.

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
