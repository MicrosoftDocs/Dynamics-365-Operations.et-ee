---
title: Uue ER-i konfiguratsiooni loomine Wordi vormingus aruannete loomiseks
description: See teema selgitab, kuidas kasutajad saavad konfigureerida uut elektroonilise aruandluse (ER) vormingu looma aruanded Microsoft Word dokumentidena.
author: NickSelin
ms.date: 12/17/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 7790d7e581b9b4260a4c57af84b02a182dde953d
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894072"
---
# <a name="design-a-new-er-configuration-to-generate-reports-in-word-format"></a>Uue ER-i konfiguratsiooni loomine Wordi vormingus aruannete loomiseks

[!include [banner](../includes/banner.md)]

Aruannete Microsoft Wordi dokumentidena loomiseks peate kujundama aruannete jaoks malli, kasutades näiteks Wordi töölauarakendust. Järgmisel joonisel on näidatud kontrollaruande näidismall, mille saab luua, et näidata töödeldud hankija maksete üksikasju.

![Näidismalli kontrollaruanne Wordi töölauarakenduses](./media/er-design-configuration-word-image1.png)

Wordi vormingus aruannete Wordi dokumendi mallina kasutamiseks saate konfigureerida uue [elektroonilise aruandluse (ER)](general-electronic-reporting.md) [lahenduse](er-quick-start1-new-solution.md). See lahendus peab sisaldama ER-i [konfiguratsiooni](general-electronic-reporting.md#Configuration), mis sisaldab ER-i [vormingu](general-electronic-reporting.md#FormatComponentOutbound) komponenti.

> [!NOTE]
> Kui loote Wordi vormingus aruannete loomiseks uue ER-vormingu konfiguratsiooni, peate valima kas suvandi **Word** dialoogiboksi **Konfiguratsiooni loomine** vormingutüübiks või jätma välja **Vormingu tüüp** tühjaks.

![Vormingu konfiguratsiooni loomine lehel Konfiguratsioonid](./media/er-design-configuration-word-image2.gif)

Lahenduse ER-vormingu komponent peab sisaldama vormingu elementi **Excel\\Fail** ja see vorminguelement peab olema lingitud Wordi dokumendiga, mida kasutatakse käitusajal aruannete loomise mallina. ER-vormingu komponendi konfigureerimiseks peate ER-i vormingu kujundajas avama loodud ER-i konfiguratsiooni [mustandi](general-electronic-reporting.md#component-versioning) versiooni. Seejärel lisage element **Excel\\Fail**, lisage redigeeritavale ER-vormingule oma Wordi mall ja linkige see mall lisatud elemendile **Excel\\Fail**.

> [!NOTE]
> Malli manustamisel peate kasutama [dokumendi tüüpi](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types), mis on varem selleks otstarbeks ER-i parameetrites [konfigureeritud](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).

![Malli lisamine vormingukujundaja lehele](./media/er-design-configuration-word-image3.gif)

Saate lisada pesastatud elemendid **Excel\\Vahemik** ja **Excel\\Lahter** elemendile **Excel\\Fail**, et määrata andmestruktuur, mis sisestatakse käitusajal loodud aruannetesse. Seejärel peate need elemendid siduma redigeeritavate ER-vormingu andmeallikatega, et määrata tegelikud andmed, mis sisestatakse käitusajal loodud aruannetesse.

![Pesastatud elementide lisamine vormingu kujundaja lehel](./media/er-design-configuration-word-image4.gif)

Kui salvestate oma muudatused kujundamise ajal ER-vormingusse, talletatakse hierarhilise vormingu struktuur manustatud Wordi mallis [kohandatud XML-i osana](/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019), mille nimi on **Aruanne**. Peate avama muudetud malli, laadima selle rakendusest Finance alla, salvestama selle kohalikult ning avama selle Wordi töölauarakenduses. Järgmisel joonisel on näidatud kohalikult salvestatud näidismall kontrollaruande jaoks, mis sisaldab kohandatud XML-i osa **Aruanne**.

![Näidisaruande malli eelvaade Wordi töölauarakenduses](./media/er-design-configuration-word-image5.gif)

Kui vorminguelementide **Excel\\Vahemik** ja **Excel\\Lahter** sidumised toimuvad käitusajal, lisatakse iga sidumise edastatud andmed loodud Wordi dokumenti kohandatud XML-i osa **Aruanne** individuaalse väljana. Loodud dokumendis kohandatud XML-i osa väljadelt väärtuste sisestamiseks peate lisama oma Wordi mallile sobivad [sisukontrollid](/office/client-developer/word/content-controls-in-word), mis toimivad käitusajal täidetud andmete kohatäidetena. Sisukontrollide täitmise määratlemiseks vastendage iga sisukontroll kohandatud XML-i osa **Aruanne** vastava väljaga.

![Sisukontrollide lisamine ja vastendamine Wordi töölauarakenduses](./media/er-design-configuration-word-image6.gif)

Seejärel peate asendama redigeeritavas ER-vormingus Wordi originaalmalli muudetud malliga, mis sisaldab nüüd Wordi sisukontrolle, mis vastendati kohandatud XML-i osa **Aruanne** väljadega.

![Malli asendamine vormingukujundaja lehel](./media/er-design-configuration-word-image7.gif)

Konfigureeritud ER-vormingu käivitamisel kasutatakse uue aruande loomiseks lisatud Wordi malli. Tegelikud andmed talletatakse Wordi aruandes kohandatud XML-i osana nimega **Aruanne**. Loodud aruande avamisel täidetakse Wordi sisukontrollid kohandatud XML-i osa **Aruanne** andmetega.

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

**Küsimus.** Ma konfigureerisin ER-vormingu, et printida Wordi dokument, mis sisaldab ettevõtte aadressi. Wordi dokumendis lisasin selle ER-vormingu jaoks RTF-teksti sisukontrolli ettevõtte aadressi esitlemiseks. Rakenduses Finance sisestasin ettevõtte aadressi mitmerealise tekstina ja vajutasin **sisestusklahvi**, et lisada igale sisestatud reale kaubatagastuse. Seega ma eeldan, et ettevõtte aadress ilmub loodud dokumentides mitmerealise tekstina. Selle asemel ilmub aadress ühe tekstireana, mis sisaldab kaubatagastuste asemel erisümboleid. Mis mu sätetel viga on?

**Vastus.** RTF-teksti sisukontrolli asemel peate kasutama lihtteksti sisukontrolli ja valima juhtelemendi atribuutides märkeruudu **Luba kaubatagastused (mitu paragrahvi)**.

## <a name="additional-resources"></a>Lisaressursid

- [Exceli mallidega ER-i konfiguratsioonide taaskasutamine Wordi vormingus aruannete loomiseks](./tasks/er-design-configuration-word-2016-11.md)
- [Manustatud pildid ja kujutised ER-iga loodud dokumentides](electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]