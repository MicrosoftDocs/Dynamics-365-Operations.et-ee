---
title: ER-i funktsioon FORMAT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni FORMAT.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b09efeb6b5d8bd2ea452dbf7a9ddaeec2ab75c92
ms.sourcegitcommit: 0455a024185f79ecb82df61e6d994bd71dee5c10
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/20/2020
ms.locfileid: "2974288"
---
# <a name="FORMAT">ER-i funktsioon FORMAT</a>

[!include [banner](../includes/banner.md)]

Funktsioon `FORMAT` tagastab määratud stringi *stringi* väärtusena pärast seda, kui see vormindati, asendades **%N** esinemiskorrad *N.* argumendiga.

## <a name="syntax"></a>Süntaks

```
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

```
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

Kui töödeldakse kliendi **Litware Retaili** aruannet 17. detsembril 2015 kultuuris **ET-EE** ja keeles **ET-EE**, annab see valem vastuseks järgmise teksti, mida saab kasutajale erandliku teatena esitada.

*Pole midagi printida. Litware Retaili klient on peatatud 17.12.2015.*

Kui sama aruannet töödeldakse kliendi **Litware Retail** jaoks 17. detsembril 2015 kultuuris **DE** ja keeles **DE**, tagastab valem järgmise teksti, mis kasutab erinevat andmevormingut:

*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*

>[!NOTE]
> Siltidele mõeldud ER-i valemites rakendatakse järgmist süntaksit.
>
> - **Rakenduse Microsoft Dynamics 365 Finance ressursside siltide puhul:** **\@X**, kus **X** on sildi ID rakendusobjektide puus (Application Object Tree (AOT))
> - **ER-i konfiguratsioonides asuvate siltide puhul:** **@„GER_LABEL:X”**, kus **X** on sildi ID ER-i konfiguratsioonis

## <a name="additional-resources"></a>Lisaressursid

[Tekstifunktsioonid](er-functions-category-text.md)
