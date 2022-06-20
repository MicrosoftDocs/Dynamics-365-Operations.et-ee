---
title: ER-i konfiguratsioonide kujundamine loodud failides baidijärjestuse märkide alistamiseks
description: See artikkel selgitab, kuidas konfigureerida elektroonilise aruandluse (ER) vormingut, et luua aruandeid, mis tõkestavad byte order mark (BOM) märke.
author: NickSelin
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d54ed105e4ff44ac2c48e2d1a4b8e12fbf6f9591
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847426"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a>ER-i konfiguratsioonide kujundamine loodud failides baidijärjestuse märkide alistamiseks

[!include [banner](../includes/banner.md)]

Saate kujundada [elektroonilise aruandluse (ER)](general-electronic-reporting.md) [lahendused](er-quick-start1-new-solution.md) looma väljaminevaid dokumente. Dokumentide loomiseks teksti- või XML-failidena peab lahendus sisaldama ER-vormingu [komponenti](general-electronic-reporting.md#Configuration) sisaldavat ER-konfiguratsiooni. Loodud failides märgikomplekti esindava [märkide kodeerimise](/windows/win32/intl/character-sets) määratlemiseks peab ER-vorming sisaldama vormingu elementi **Üldine\\Fail**. ER-vormingu komponendi konfigureerimiseks avage ER-i vormingu kujundajas ER-i konfiguratsiooni [mustandi](general-electronic-reporting.md#component-versioning) versioon ja lisage element **Üldine\\Fail**. Määrake väljal **Kodeering** väljaminevate failide kodeering, mis luuakse käitusajal, kasutades seda komponenti.

> [!NOTE]
> Kui vorming sisaldab valet kodeerimisnime, ilmneb vormingu sätete muudatuste salvestamisel tõrge.

![Juurelemendi lisamine vormingu kujundaja lehel.](./media/er-suppress-bom-characters-image1.gif)

Kui määrate kodeeringuks **UTF-8**, **UTF-16** või **UTF-32**, muutub valik **Alista BOM-i tärgid** kättesaadavaks. Määrake see suvand valikule **Jah**, et alistada sissetulevates failides [baidijärjestuse märgid (BOM)](/globalization/encoding/byte-order-mark), mis luuakse käitusajal, kui redigeeritav ER-vorming töötab.

> [!NOTE]
> Kui jätate välja **Kodeering** tühjaks, kasutatakse vaikimisi kodeerimist **UTF-8**.

![Vormingu kujundaja lehel BOM-i tärkide alistamise suvandi häälestamine.](./media/er-suppress-bom-characters-image2.gif)

Käitusajal funktsioonide läbivaatamiseks läbige vastav protseduur. Näiteks viige lõpule XML-elementide [käivitamise edasilükkamise sammud ER-vormingu artiklis](er-defer-xml-element.md). Kui olete vormingu muutmise sammud [läbinud](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output), järgige neid lisatoiminguid, et arvutus põhineks selle artikli loodud väljundi jaotisel.

1. Määrake UTF-i kodeering.

    1. Valige element **Aruanne** tüübis **Üldine\\Fail**.
    2. Väljal **Kodeerimine** määrake kodeering **UTF-8**.

2. Looge XML-fail, mis sisaldab BOM-i tärki.

    1. Määrake suvand **Alista BOM-i tärgid** valikule **Ei**, et kaasata BOM-i tärgid loodud XML-failidesse.
    2. [Viige lõpule XML-i](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used)[koondelemendi täitmise edasilükkamine, et arvutatud kogusummat kasutataks XML-elementide täitmise edasilükkamise jaotises ER-vormingute](er-defer-xml-element.md) artiklis ja **salvestage loodud fail kui SampleXmlReport.xml**.

3. Looge XML-fail, mis ei sisalda BOM-i tärki.

    1. Määrake suvand **Alista BOM-i tärgid** valikule **Jah**, et alistada BOM-i tärgid loodud XML-failides.
    2. [Viige lõpule XML-i](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used)[koondelemendi täitmise edasilükkamine, et arvutatud kogusummat kasutataks XML-elementide täitmise edasilükkamise jaotises ER-vormingute](er-defer-xml-element.md) artiklis ja **salvestage loodud fail sampleXmlReport-ina (1.xml**).

4. Võrrelge failide võrdlemise utiliidis loodud faile.

    Esimene erinevus, mida te märkate, on faili päis. SampleXmlReport.xml file sisaldab BOM-i tärki, samas kui fail SampleXmlReport (1).xml ei sisalda.

    ![Loodud failide võrdlemine faili võrdlemise utiliiti kasutades.](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a>Vt ka

- [Elektroonilise aruandluse vormingus XML-elementide käivitamise edasilükkamine](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
