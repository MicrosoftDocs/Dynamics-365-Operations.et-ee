---
title: Kinnipeetava maksu aruandluskoodide häälestamine TDS-i maksutüübi jaoks
description: Kinnipeetava maksu aruandluskoode kasutatakse vormi 26Q ja vormi 27Q väljavõtete loomiseks allikas mahaarvatud maksude jaoks (TDS). Käesolev teema kirjeldab, kuidas seadistada kinnipeetava maksu aruandluskoodide samme nii, et saate seadistada TDS-i aruandluskoode.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 1f9325d182f89b98e8b943ae047c55e7e1aeb02f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023188"
---
# <a name="set-up-withholding-tax-reporting-codes-for-the-tds-tax-type"></a>Kinnipeetava maksu aruandluskoodide häälestamine TDS-i maksutüübi jaoks

[!include [banner](../includes/banner.md)]

Kinnipeetava maksu aruandluskoode kasutatakse vormi 26Q ja vormi 27Q väljavõtete loomiseks allikas mahaarvatud maksude jaoks (TDS). Käesolev teema kirjeldab, kuidas seadistada kinnipeetava maksu aruandluskoodide samme nii, et saate seadistada TDS-i aruandluskoode.

1. Minge **Maks \> Seadistus \> Kinnipeetav maks \> Kinnipeetava maksu aruandluskoodid**.

    [![Kinnipeetava maksu aruandluskoodide leht](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)

2. Väljal **Maksu tüüp** valige **TDS** kinnipeetava maksu aruandluskoodide TDS maksutüübi häälestamiseks.
3. Väljal **Kinnipeetava maksu komponent** valige TDS-i komponent, mille jaoks te kinnipeetava maksu aruandluskoodi määratlete. Väljal **Kinnipeetava maksu komponendigrupp** kuvatakse TDS-i komponendi grupp, mis määratleti teie määratleva TDS-i komponendi jaoks.

    Väljal **sektsioonikood** kiirkaardil **Üldine** näitab sektsiooni koodi, mis on seotud TDS-i komponendigrupiga.

4. Valige kiirkaardil **Üldine**, väljal **Aruandluskood** sobiv TDS aruandlus kood:

    - TDS
    - TCS
    - Lisatasu
    - PE\_Cess
    - SHE\_Cess

5. Sulgege leht.
