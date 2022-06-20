---
title: CHANGETIMEZONE ER-i funktsioon
description: See artikkel annab teavet SELLE kohta, kuidas CHANGETIMEZONE'i elektroonilise aruandluse (ER) funktsiooni kasutatakse.
author: NickSelin
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: AX 10.0.23
ms.openlocfilehash: be94f57cfcb6115ea386a279c379662f7d401d11
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903581"
---
# <a name="changetimezone-er-function"></a>CHANGETIMEZONE ER funktsioon

[!include [banner](../includes/banner.md)]

`CHANGETIMEZONE` funktsioon tagastab *[DateTime](er-formula-supported-data-types-primitive.md#datetime)* väärtuse koordineeritud maailmaajas (Greenwichi aeg \[GMT\]), mis teisendatakse antud kellaaja/kuupäeva väärtusest ühes tsoonis kuupäeva/kellaaja väärtuseks teises tsoonis.

## <a name="syntax"></a>Süntaks

```vb
CHANGETIMEZONE (datetime, base time zone, target time zone)
```

## <a name="arguments"></a>Argumendid

`datetime`: *kuupäev ja kellaaeg*

Kuupäeva/kellaaja väärtus koordineeritud maailma ajavööndis, mis tähistab teisendamise kuupäeva/kellaaja väärtust.

`base time zone`: *[String](er-formula-supported-data-types-primitive.md#string)*

Ajavööndi nimi, kus antud kuupäeva/kellaaja väärtus nihutatakse enne teisendamist.

`target time zone`: *string*

Ajavööndi nimi, kuhu teisendatud kuupäeva/kellaaja väärtus nihutatakse teisendamise ajal.

## <a name="return-values"></a>Tagastusväärtused

*DateTime*

Tulemuseks saadud kuupäeva/kellaaja väärtus koordineeritud maailmaaja ajavööndis.

## <a name="usage-notes"></a>Kasutamise märkused

Allika ja sihtkoha ajavööndite määramiseks saate kasutada ajavööndi nimesid, mida [pakub](https://data.iana.org/time-zones/releases/) [nternet Assigned Numbers Authority (IANA) poolt](https://www.iana.org/) või mida [toetab](/windows-hardware/manufacture/desktop/default-time-zones) Microsoft Windows.

Käitusajal ilmneb erand "Ajavöönd '\<time zone name\>' pole olemas" kui antud nime ei leita IANA loendist või Windows`i registrist.

Ajavööndite puhul, kus jälgitakse suveaega, võtab teisendus arvesse koordineeritud maailmaaja suveaja nihke. Värskeimat saadaolevat teavet selle tasakaalustuse kohta kasutatakse teisendamise ajal.

## <a name="example-1"></a>Näide 1

Selles näites kasutatakse Windowsi ajavööndi nimesid.

Konfigureerite **DSX** andmeallika tüübi **Arvutatud väli**. See sisaldab järgmisi väljendeid.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "E. Europe Standard Time", "Hawaiian Standard Time"), "O")
)
```

Kui konfigureerite arvutatud väljatüübiga **DSY** andmeallika **Arvutatud väli** tüüp kui `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")` **DSX** andmeallika teksti tagastus **2021-06-01T12:55:00.0000000+00:00 -> 2021-05-31T23:55:00.0000000+00:00**. See tekst näitab, et kahe antud ajavööndi vaheline ajaerinevus 1. juunil on üle 24 tunni. Seepärast on teisendatud kuupäeva/kellaaja väärtus üks päev varasem kui antud kuupäeva/kellaaja väärtus, kuna baasajavöönd on sihtajatsoonist ees.

Kui konfigureerite arvutatud väljatüübiga **DSY** andmeallika **Arvutatud väli** tüübi kui `DATETIMEVALUE ("01-Dec-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")` **DSX** andmeallika teksti tagastus on **2021-12-01T12:55:00.0000000+00:00 -> 2021-12-01T00:55:00.0000000+00:00**. See tekst näitab, et kahe antud ajavööndi vaheline ajaerinevus 1. detsembril on vähem kui 24 tundi. Seepärast võrdub teisendatud kuupäeva/kellaaja väärtus antud kuupäeva/kellaaja väärtusega.

> [!NOTE]
> Sama avaldis tagastab sama ajavööndipaari esitatud ja teisendatud kuupäeva/kellaaja väärtuste vahel erineva hälbe, sest antud kuupäeval/kellaajal järgitakse esitatud ajavööndite puhul erinevat maailmaaja suveaja salvestamist.

## <a name="example-2"></a>Näide 2

Selles näites on kasutatud IANA ajavööndi nimesid.

Konfigureerite **DSX** andmeallika tüübi **Arvutatud väli**. See sisaldab järgmisi väljendeid.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "Europe/Athens", "US/Hawaii"), "O")
)
```

Kui konfigureerite arvutatud väljatüübiga **DSY** andmeallika **Arvutatud väli** tüüp kui `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")` **DSX** andmeallika teksti tagastus **2021-06-01T12:55:00.0000000+00:00 -> 2021-05-31T23:55:00.0000000+00:00**. See tekst näitab, et kahe antud ajavööndi vaheline ajaerinevus 1. juunil on üle 24 tunni. Seepärast on teisendatud kuupäeva/kellaaja väärtus üks päev varasem kui antud kuupäeva/kellaaja väärtus, kuna baasajavöönd on sihtajatsoonist ees.

Kui konfigureerite arvutatud väljatüübiga **DSY** andmeallika **Arvutatud väli** tüübi kui `DATETIMEVALUE ("01-Dec-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")` **DSX** andmeallika teksti tagastus on **2021-12-01T12:55:00.0000000+00:00 -> 2021-12-01T00:55:00.0000000+00:00**. See tekst näitab, et kahe antud ajavööndi vaheline ajaerinevus 1. detsembril on vähem kui 24 tundi. Seepärast võrdub teisendatud kuupäeva/kellaaja väärtus antud kuupäeva/kellaaja väärtusega.

## <a name="example-3"></a>Näide 3

Konfigureerite **DSX** andmeallika tüübi **Arvutatud väli**. See sisaldab järgmisi väljendeid.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "US/Hawaii", "Europe/Athens"), "O")
)
```

Kui konfigureerite väljendi **DSY** andmeallika **Arvutatud väli** tüübi kui `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")` **DSX** andmeallika teksti tagastuse **2021-06-01T12:55:00.0000000+00:00 -> 2021-06-02T01:55:00.0000000+00:00**. See tekst näitab, et kahe antud ajavööndi vaheline ajaerinevus 1. juunil on üle 24 tunni. Seepärast on teisendatud kuupäeva/kellaaja väärtus üks päev varasem kui antud kuupäeva/kellaaja tagastus, mis on baasajavööndi ajatsoonist ees.

## <a name="example-4"></a>Näide 4

Võite saada välisallikalt kuupäeva-/ajatempli ajavöönditeavet mitte sisaldava tekstina. Te võite siiski teada ajavööndit, kus allikat käitatakse. Näiteks saate kuupäeva-/aja templi **01/12/2021 12:55:00** teenuselt, mis on käitatud Hispaanias. Kuupäeva/kellaaja väärtuse õigeks salvestamiseks andmebaasi, viige järgmine teisendus lõpule:

- Konfigureerige **DSY** andmeallikas **arvutatud välja** tüübis, et teisendada kuupäeva/kellaaja tempel tekstist koordineeritud universaalaja kuupäeva/kellaaja väärtuseks.

    `DATETIMEVALUE ("01/12/2021 12:55:00", "dd/MM/yyyy HH:mm:ss", "ES")`

- Konfigureerige **DSX** andmeallikas **Arvutatud väli** tüübis, et nihutada teisendatud kuupäeva/kellaaja väärtus koordineeritud maailmaajaks välise allika ajavööndi kuupäeva/kellaaja väärtusena.

    `CHANGETIMEZONE(DSY, "Romance Standard Time", "GMT Standard Time")`

> [!NOTE]
> Kui kasutate `CHANGETIMEZONE` kuupäeva/kellaaja teisendamise funktsiooni, pange tähele, et mis tahes kuupäeva/kellaaja väärtus salvestatakse andmebaasi väärtusena koordineeritud maailmaaja ajavööndis. Enne selle väärtuse rakenduse lehtedel esitamis, see muudetakse. Teisendamine võtab arvesse ajavööndit, mis on [seadistatud](../../fin-ops/organization-administration/tasks/set-users-preferred-time-zone.md) praegu sisse logitud rakenduse kasutaja eelistatud tsooniks.

## <a name="additional-resources"></a>Lisaressursid

[Kuupäeva ja kellaaja funktsioonid](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
