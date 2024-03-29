---
title: Teksti kärpimise vältimine positsioonihierarhias ja eksportimine Visiosse
description: See artikkel selgitab, kuidas parandada inimeste ja positsioonide kärbitud nimede ja positsioonide probleemi Microsofti positsioonihierarhias Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3663f5689fc0109caad01a285185f9f4ffa6fcca
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865378"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a>Teksti kärpimise vältimine positsioonihierarhias ja eksportimine Visiosse


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Väljastamine**

Kui klient vaatab ametikoha hierarhiat rakenduses Microsoft Dynamics 365 Human Resources, siis üksikisikute ja ametikohtade nimesid kärbitakse. Seetõttu võib kuvatõmmise tegemine või hierarhia printimine ja jaotamine olla keeruline.

![Ametikoha hierarhia.](media/position-h.png)

**Põhjus**

Selline käitumine on nii kavandatud.

**Lahendus**

Kahjuks ei saa kasutajad hõlpsalt teksti suurust muuta. Samas saate ametikoha hierarhia rakendusest Human Resources välja eksportida ja seejärel selle Microsoft Visiosse importida. Kuigi järgmine artikkel kirjutati Microsoft Dynamics AX 2012 jaoks, kehtib see ka rakenduse Human Resources puhul: [Ametikoha hierarhia eksportimine Microsoft Visiosse](/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).

Järgige neid samme, et eksportida Visiosse.

1. Avage rakenduses Human Resources loendi **Ametikohad** leht.

    Organisatsiooni struktuuri diagrammi lisateabe lisamiseks lisage loendisse **Ametikohad** välju, et need oleksid saadaval, kui kasutate selles protseduuris hiljem **Organisatsiooni skeemi viisardit**.

2. Valige toimingupaanil nupp **Ava Microsoft Office’is** ja seejärel valige jaotises **Ekspordi Excelisse** suvand **Ametikohad**. Või vajutage klahvikombinatsiooni Ctrl+T.

    ![Ametikohtade loendilehe eksportimine Excel`isse.](media/org-admin.png)

3. Salvestage eksporditud Exceli fail.

    ![Eksport Exceli dialoogiboksi.](media/export-excel.png)

4. Visios valige **Visio – loo uus** ja valige mallikategooria **Ettevõte**.

    ![Uus diagramm.](media/new.png)

5. Valige **Organisatsiooni skeemi viisard** ja seejärel valige **Loo**.

    ![Organisatsiooni skeemi viisard dialoogiboks.](media/orgchart-wizard.png)

6. Valige **Teave, mis on juba faili või andmebaasi talletatud** ja seejärel valige **Edasi**.

    ![Organisatsiooni skeemi viisard 1.](media/orgchart-wizard7.png)

7. Valige **Tekst, Org Plus (\*.txt), või Exceli fail** ja seejärel valige **Edasi**.

    ![Organisatsiooni skeemi viisard 2.](media/orgchart-wizard3.png)

8. Sirvige, et valida eksporditud Exceli fail, mis sisaldab ametikoha hierarhiat ja seejärel valige **Edasi**.

    ![Organisatsiooni skeemi viisard 3.](media/orgchart-wizard2.png)

9. Määrake välja **Nimi** väärtuseks **Ametikoht**, määrake välja **Aruannete sihtkoht** väärtuseks **Aruanded ametikohale** ja seejärel valige **Edasi**.

    ![Organisatsiooni skeemi viisard 4.](media/orgchart-wizard1.png)

10. Valige väljad, mida tuleks igas sõlmes kuvada ja seejärel valige **Edasi**.

    ![Organisatsiooni skeemi viisard 5.](media/orgchart-wizard5.png)

11. Lisage veerg **Ametikoht** loendisse **Kujundi andmeväljad** ja seejärel valige **Edasi**.

    ![Organisatsiooni skeemi viisard 6.](media/orgchart-wizard6.png)

12. Pildid ei ole praegu saadaval. Seetõttu valige järgmisel lehel **Edasi**.
13. Valige **Soovin, et viisard jaotaks mu organisatsiooniskeemi erinevate lehtede vahel**.

    ![Organisatsiooni skeemi viisard 7.](media/orgchart-wizard4.png)

14. Valige **Lõpeta**.

    Kui on ametikohti, mis pole struktuuris, palutakse teil need diagrammi lisada.

Visios loodud diagramm kuvab iga halduri eraldi töölehel.

Väljade põhjal, mille valisite, et soovite diagrammi lisada, kuvab iga sõlm Visio faili loomisel vastava teabe.

![Hierarhiaskeem.](media/hierarchy.png)

**Lisasuvand**

Rakenduses Human Resources saate võib-olla kasutada ka tööruumi **Inimesed**, et vaadata hierarhiaga seotud teavet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
