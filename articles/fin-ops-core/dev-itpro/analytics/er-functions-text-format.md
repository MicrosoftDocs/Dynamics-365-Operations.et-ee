---
title: ER-i funktsioon FORMAT
description: See artikkel annab teavet selle kohta, kuidas vormingu elektroonilise aruandluse (ER) funktsiooni kasutatakse.
author: NickSelin
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce9dd95dc347416f6f9c3024b0b1de3f60f88bfb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876772"
---
# <a name="format-er-function"></a>ER-i funktsioon FORMAT

[!include [banner](../includes/banner.md)]

Funktsioon `FORMAT` tagastab määratud stringi *stringi* väärtusena pärast seda, kui see vormindati, asendades **%N** esinemiskorrad *N.* argumendiga.

## <a name="syntax"></a>Süntaks

```vb
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a>Argumendid

`string`: *string*

Viide tüübi *String* andmeallikale, mis tuleb vormindada. See argument on kohustuslik.

`argument 1`: *string*

Esimene argument, mida kasutatakse **%1** esinemiste asendamiseks. See argument on kohustuslik.

`argument N`: *string*

*N*. argument, mida kasutatakse **%2**, **%3** jne esinemiste asendamiseks. Need täiendavad argumendid on valikulised.

## <a name="return-values"></a>Tagastusväärtused

*String*

Tulemiks saadud teksti väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Kui parameetril ei ole argumenti, tagastatakse parameeter stringis kui **"%N"**. Tüübi *Tõeline* väärtuste puhul on vaikimisi stringi teisendamine piiratud kahe kümnendkohaga.

## <a name="example"></a>Näide

Järgmisel joonisel tagastab andmeallikas **PaymentModel** kliendi kirjete loendi, kasutades komponenti **Klient**. See tagastab töötlemiskuupäeva väärtuse, kasutades välja **ProcessingDate**.

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

Elektroonilise aruandluse (ER) vormingus, mis on mõeldud looma valitud klientidele elektroonilist faili, valitakse **PaymentModel** andmeallikana ja see juhib protsessi voogu. Kui valitud klient on peatatud kuupäeval, millal aruannet töödeldaks, ilmub kasutaja teavitamiseks erand. Seda tüüpi töötlemise juhtimiseks koostatud valem saab kasutada järgmisi ressursse.

- Silt SYS70894, millel on järgmine tekst.

    - **Inglise keeles:** "Nothing to print"
    - **Saksa keeles:** Nichts zu drucken

- Silt SYS18389, millel on järgmine tekst.

    - **USA inglise keeles:** „Customer %1 is stopped for %2.”
    - **Saksa keeles:** „Debitor '%1' wird für %2 gesperrt.”

Koostada saab järgmise avaldise.

```vb
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

Kui töödeldakse kliendi **Litware Retaili** aruannet 17. detsembril 2015 kultuuris **ET-EE** ja keeles **ET-EE**, annab see valem vastuseks järgmise teksti, mida saab kasutajale erandliku teatena esitada.

*Pole midagi printida. Litware Retaili klient on peatatud 17.12.2015.*

Kui sama aruannet töödeldakse kliendi **Litware Retail** jaoks 17. detsembril 2015 kultuuris **DE** ja keeles **DE**, tagastab valem järgmise teksti, mis kasutab erinevat andmevormingut:

*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*

>[!NOTE]
> Siltidele mõeldud ER-i valemites rakendatakse järgmist süntaksit.
>
> - **Ressurssidest siltide jaoks Microsoft Dynamics rakenduse 365 Finance:** **\@ X jaoks,** kus X **on** sildi ID rakendusobjektide puus (AOT)
> - **ER-i konfiguratsioonides asuvate siltide puhul:** **@„GER_LABEL:X”**, kus **X** on sildi ID ER-i konfiguratsioonis

## <a name="additional-resources"></a>Lisaressursid

[Tekstifunktsioonid](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]