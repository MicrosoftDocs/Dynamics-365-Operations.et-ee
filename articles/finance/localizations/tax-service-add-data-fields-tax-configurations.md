---
title: Andmeväljade lisamine maksukonfiguratsioonidesse
description: See artikkel selgitab, kuidas kohandada maksu konfiguratsioone andmeväljade lisamisega.
author: Kai-Cloud
ms.date: 10/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 894c42f444d27b807288b84c7b9c620ad0121fa9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872322"
---
# <a name="add-data-fields-in-tax-configurations"></a>Andmeväljade lisamine maksukonfiguratsioonidesse

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas kohandada maksu konfiguratsioone, [kasutades andmevälju, mis on maksude integreerimises lisatud](tax-service-add-data-fields-tax-integration-by-extension.md).

## <a name="customize-the-tax-data-model"></a>Maksuandmete mudeli kohandamine

1. Finantsis Microsoft Dynamics 365 minge elektroonilise aruandluse **maksu** > **konfiguratsioonidesse**.
2. Konfiguratsioonipuus valige **Käibemaksuandmete mudel**. Valige toimingupaanilt suvand **Loo konfiguratsioon**. 

  > [!NOTE] 
  > Kui konfiguratsioonipakkujat pole saadaval, looge see ja muutke see oma maksukonfiguratsiooni jaoks aktiivseks. Lisateabe saamiseks vaadake teemat [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
  
3. Valige ripploendist valik **Tuletatud maksustatav dokumendimudel nimest: Maksuarvestuse andmemudel, Microsoft**, sisestage uue maksuandmete mudeli nimi ja seejärel valige käsk **Loo konfiguratsioon**.
4. Valige äsja loodud maksuandmete mudel ja seejärel valige tegevuspaanil suvand **Kujundaja**.
5. Laiendage andmemudelipuud, valige **Read** ja seejärel valik **Uus**.
6. Dialoogiboksis **Sõlme loomine** sisestage nimi, määrake kauba tüüp ja seejärel valige käsk **Lisa**.
7. Lisage kõik nõutavad veerud.
8. Valige toimingupaanil käsk **Salvesta** ja seejärel **Lõpeta**.
9. Sulgege leht ja vaadake oma maksuandmete mudeli lõpetatud versiooni.

## <a name="customize-the-tax-configuration"></a>Maksukonfiguratsiooni kohandamine

1. Jaotises Finants avage menüü **Elektrooniline aruandlus** > **Maksukonfiguratsioonid**.
2. Konfiguratsioonipuus valige **Maksuarvestuse konfiguratsioon**. Valige toimingupaanilt suvand **Loo konfiguratsioon**.
3. Valige ripploendist **Tuletatud maksuteenuse konfiguratsioon nimest: Maksuarvestuse konfiguratsioon, Microsoft**, sisestage uue maksukonfiguratsiooni nimi ja seejärel valige käsk **Loo konfiguratsioon**.
4. Valige äsja loodud maksukonfiguratsioon ja seejärel valige tegevuspaanil suvand **Kujundaja**.
5. Valige jaotises **Atribuudid** väljal **Andmemudel** varem loodud kohandatud maksuandmete mudel.
6. Valige väljal **Andmemudeli versioon** maksuandmete mudeli lõpetatud versioon.
7. Valige **Lisa** ja lisage nõutavad maksumeetmed.
8. Valige toimingupaanil käsk **Salvesta** ja seejärel **Lõpeta**.
9. Sulgege leht ja vaadake oma maksukonfiguratsiooni lõpetatud versiooni.

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a>Rakendage maksufunktsioone kohandatud maksukonfiguratsioonis

1. Jaotises Regulatory Configuration Service (RCS) avage **Globaliseerumise funktsioonid** > **Maksud**.
2. Valige **Lisa**, sisestage uue funktsiooni kohta teave ja seejärel valige käsk **Loo funktsioon**.
3. Valige funktsioon vahekaardil **Versioon** ja seejärel käsk **Redigeeri**.
4. Valige vahekaardi **Üldine** väljal **Konfiguratsiooni versioon** kohandatud maksukonfiguratsioon ja versioon.
5. Dialoogiboksis **Veergude haldamine** valige päise- ja reaveerud, mida soovite oma kohandatud maksumeetmesse kaasata ja seejärel valige paremnoolenupp nende lisamiseks loendisse **Valitud veerud**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
