---
title: Andmeväljade lisamine maksukonfiguratsioonidele
description: Käesolev teema kirjeldab maksukonfiguratsioonide kohandamist andmeväljade lisamise abil.
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 197a2d1605dd39188841aba02a71d228c7138c54
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921185"
---
# <a name="add-data-fields-in-tax-configurations"></a>Andmeväljade lisamine maksukonfiguratsioonidele

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas kohandada maksu konfiguratsioone, kasutades [andmevälju, mis on lisatud maksuintegratsioonis](tax-service-add-data-fields-tax-integration-by-extension.md).

## <a name="customize-the-tax-data-model"></a>Maksuandmete mudeli kohandamine

1. Avage rakenduses Microsoft Dynamics 365 Finance jaotis **Elektrooniline aruandlus** \> **Maksukonfiguratsioonid**.
2. Konfiguratsioonipuus valige **Maksuandmete mudel – Euroopa**. Valige toimingupaanilt suvand **Loo konfiguratsioon**.
3. Valige ripploendist valik **Tuletatud maksustatav dokumendimudel nimest: Maksu andmemudel -- Euroopa, Microsoft**, sisestage uue maksuandmete mudeli nimi ja seejärel valige käsk **Loo konfiguratsioon**.
4. Valige äsja loodud maksuandmete mudel ja seejärel valige tegevuspaanil suvand **Kujundaja**.
5. Laiendage andmemudelipuud, valige **Read** ja seejärel valik **Uus**.
6. Dialoogiboksis **Sõlme loomine** sisestage nimi, määrake kauba tüüp ja seejärel valige käsk **Lisa**.
7. Lisage kõik nõutavad veerud.
8. Valige toimingupaanil käsk **Salvesta** ja seejärel **Lõpeta**.
9. Sulgege leht ja vaadake oma maksuandmete mudeli lõpetatud versiooni.

## <a name="customize-the-tax-configuration"></a>Maksukonfiguratsiooni kohandamine

1. Jaotises Finants avage menüü **Elektrooniline aruandlus** \> **Maksukonfiguratsioonid**.
2. Konfiguratsioonipuus valige **Maksukonfiguratsioon – Euroopa**. Valige toimingupaanilt suvand **Loo konfiguratsioon**.
3. Valige ripploendist valik **Tuletatud maksuteenuse konfiguratsioon nimest: Maksukonfiguratsioon -- Euroopa, Microsoft**, sisestage uue maksukonfiguratsiooni nimi ja seejärel valige käsk **Loo konfiguratsioon**.
4. Valige äsja loodud maksukonfiguratsioon ja seejärel valige tegevuspaanil suvand **Kujundaja**.
5. Valige jaotises **Atribuudid** väljal **Andmemudel** varem loodud kohandatud maksuandmete mudel.
6. Valige väljal **Andmemudeli versioon** maksuandmete mudeli lõpetatud versioon.
7. Valige **Lisa** ja lisage nõutavad maksumeetmed.
8. Valige toimingupaanil käsk **Salvesta** ja seejärel **Lõpeta**.
9. Sulgege leht ja vaadake oma maksukonfiguratsiooni lõpetatud versiooni.

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a>Rakendage maksufunktsioone kohandatud maksukonfiguratsioonis

1. Jaotises Regulatory Configuration Services (RCS) avage **Globaliseerumise funktsioonid** \> **Maks**.
2. Valige **Lisa**, sisestage uue funktsiooni kohta teave ja seejärel valige käsk **Loo funktsioon**.
3. Valige funktsioon vahekaardil **Versioon** ja seejärel käsk **Redigeeri**.
4. Valige vahekaardi **Üldine** väljal **Konfiguratsiooni versioon** kohandatud maksukonfiguratsioon ja versioon.
5. Dialoogiboksis **Veergude haldamine** valige päise- ja reaveerud, mida soovite oma kohandatud maksumeetmesse kaasata ja seejärel valige paremnoolenupp nende lisamiseks loendisse **Valitud veerud**.
