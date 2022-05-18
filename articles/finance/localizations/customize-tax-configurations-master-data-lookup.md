---
title: Maksukonfiguratsioonide kohandamine koondandmete otsinguks
description: See teema kirjeldab, kuidas kohandada maksukonfiguratsioone koondandmete otsingufunktsiooni laiendamiseks.
author: kai-cloud
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 69541316ad4c6c4bb404ea142844ce596b5502b9
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689124"
---
# <a name="customize-tax-configurations-for-master-data-lookup"></a>Maksukonfiguratsioonide kohandamine koondandmete otsinguks

[!include [banner](../includes/banner.md)]

Järgi neid teemas kirjeldatavaid samme, kuidas kohandada maksukonfiguratsioone koondandmete otsingufunktsiooni laiendamiseks.

## <a name="import-a-tax-configuration-provided-by-microsoft"></a>Microsoft`i esitatud maksukonfiguratsiooni importimine

1. Valige Regulatory Configuration Service (RCS) teenuses **Elektroonilise aruandluse** tööruumis konfiguratsioonipakkujana **Microsoft**.
2. Valige **Hoidlad**.
3. Valige **Globaalne** ja seejärel valige **Ava**.
4. Valige maksukonfiguratsioon, näiteks **Maksuarvestuse konfiguratsioon** ja seejärel **Versioonid** vahekaardil valige versioon.
5. Valige **Impordi**.

> [!NOTE]
> Vaikimisi imporditakse Dataverse mudeli vastendamine. Kui saate konfiguratsiooni importimise protsessi ajal hoiatusteateid, lubage virtuaalsed üksused Dataverse üksuses. Lisateavet leiate [Luba Dataverse virtuaalsed jaotised](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

## <a name="create-a-customized-data-model-configuration"></a>Kohandatud andmemudeli konfiguratsiooni loomine

1. **Elektroonilise aruandluse** tööruumis valige **maksukonfiguratsioonid** ja seejärel valige laiendamiseks andmemudeli konfiguratsioon. Näiteks valige **maksu arvutamise andmemudel**.
2. Valige **Konfiguratsiooni loomine**.
3. Valige **Tuletatud maksustatav dokumendimudel: maksuarvutuse andmemudel, Microsoft**.
4. Tippige väljale **Nimi** tekst **Kohandatud andmemudel**.
5. Valige **Konfiguratsiooni loomine**.

## <a name="create-customized-reference-models"></a>Kohandatud viitemudelite loomine

1. **Maksukonfiguratsioonide** lehel valige **kohandamise andmemudeli** suvand ja seejärel valige **Kujundaja**.
2. Valige mooduli kolmikpunkti nupp (**...**) ja seejärel valige **Viitemudeli** vaade.

    [![Viitemudel.](./media/pic2.png)](./media/pic2.png)

3. Kohandatud viitemudeli loomine. Kohandatud mudel on juurmudel. Kohandatud üksus on kirje loend. Kohandatud väli on stringiväli, mida soovite otsingus kasutada. Vajadusel saate välju juurde lisada.
4. Valige mooduli kolmikpunkti nupp (**...**) ja seejärel valige **Maksudokumendi** vaade.
5. Valige atribuut, mida siduda kohandatud viitemudeliga. Näiteks valige **kohandatud atribuut** ja järgige seejärel neid samme:

    1. Valige **Vali viitemudel**.
    2. Valige **kohandatud mudel** ja seejärel valige **OK**. Viitemudeli nimi uuendatakse välja **Loomulik väärtus** väärtuseks.

        [![Saate valida viitemudeli dialoogiboksi.](./media/pic5.png)](./media/pic5.png)

    3. Valige nupp **Salvesta** ja seejärel suvand **Lõpeta**.

## <a name="create-a-customized-model-mapping-configuration"></a>Kohandatud mudeli vastenduse konfiguratsiooni loomine

1. **Elektroonilise aruandluse** tööruumis valige **maksukonfiguratsioonid** ja valige seejärel **Dataverse mudelvastendamise** konfiguratsioon.
2. Väljal **Mudelivastenduse vaikeväärtus** valige **Ei**.
3. Valige **Konfiguratsiooni loomine**.
4. Valige **Maksustatav dokumendi vastendamise mudeli tuletatud nimi: Dataverse mudelvastendamine, Microsoft**.
5. Tippige väljale **Nimi** tekst **Kohandatud mudelvastendamine**.
6. Valige **sihtmudeli** väljal **kohandusandmete mudeli** andmemudel.
7. Valige **Konfiguratsiooni loomine**.

    [![Konfiguratsiooni loomise rippmenüü dialoogiaken.](./media/pic6.png)](./media/pic6.png)

8. Valige **kohandusmudeli vastendamine** ja seadistage **ühendatud rakenduse** väli ühenduseks, mis loodi etapis 8 [koondandmete otsingu keskkonna häälestamisel](tax-service-set-up-environment-master-data-lookup.md).
9. Seadistage **Vaikimisi mudeli vastendamise** suvand väärtusele **Jah**.

## <a name="create-customized-model-mappings"></a>Kohandatud mudelivastenduste loomine

1. **Maksukonfiguratsioonide lehel** valige **kohandamismudeli vastendamine**.
2. Valige **Kujundaja** ja seejärel valige **kohandatud mudel**.

    [![Kohandusmudel.](./media/pic8.png)](./media/pic8.png)

## <a name="map-a-model-mapping-to-a-dataverse-entity"></a>Vastenda vastendamismudel Dataverse üksusega

1. **Vastendusmudeli kujundaja** lehel valige **kohandamismudel** ja seejärel valige **Kujundaja**.
2. Valige **Andmeallika tüübi** puus **Dataverse Tabel**.
3. Valige **Lisa juur** suvand **Andmeallikad** vahekaardil.
4. Sisestage väljale **Nimi** tekst **Kohandatud Dataverse**.
5. Valige üksus teisel **Nimi** väljal.
6. Valige nupp **OK**.

    [![Andmeallika atribuutide dialoogiboks.](./media/pic9.png)](./media/pic9.png)

7. Valige **kohandatud Dataverse** ja **kohandatud üksus** ning seejärel valige **sidumine**.

    [![Kohandatud Dataverse ja kohandatud üksuse sidumine.](./media/pic10.png)](./media/pic10.png)

8. Valige **kohandatud Dataverse** ja **kohandatud välji** väljal väli ning seejärel valige **sidumine**.

    [![Kohandatud Dataverse ja kohandatud välja sidumine.](./media/pic11.png)](./media/pic11.png)

9. Valige nupp **Salvesta** ja seejärel suvand **Lõpeta**.

## <a name="create-a-customized-tax-configuration"></a>Kohandatud maksekonfiguratsiooni loomine

1. **Elektroonilise aruandluse** tööruumis valige **maksukonfiguratsioonid** ja valige seejärel **maksukalkulatsiooni konfiguratsioon**.
2. Valige **Konfiguratsiooni loomine**.
3. Valige **Maksuteenuse konfiguratsioon tuletatud nimest: maksuarvestuse konfiguratsioon, Microsoft**.
4. Tippige väljale **Nimi** tekst **Kohandatud konfiguratsioon**.
5. Valige **Konfiguratsiooni loomine**.
6. Valige **Kohandatud konfiguratsioon** ja seejärel valige **Kujundaja**.
7. Valige **Andmemudel** väljal suvand **Kohandamise andmemudel**.
8. Valige väljal **Andmemudeli versioon** vastav andmemudeli versioon.

    [![Atribuutide jaotis.](./media/pic13.png)](./media/pic13.png)

9. Valige **Lõpeta**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
