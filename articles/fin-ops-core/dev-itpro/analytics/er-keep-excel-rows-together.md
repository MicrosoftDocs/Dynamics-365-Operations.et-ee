---
title: Elektroonilise aruandluse vormingu loomine ridade samal Exceli lehel kooshoidmiseks
description: See artikkel selgitab, kuidas kujundada elektroonilise aruandluse (ER) vormingut, mis hoiab read kokku samal Microsoft Excel leheküljel.
author: NickSelin
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-03-01
ms.dyn365.ops.version: Version 10.0.26
ms.openlocfilehash: 98e6dd4f926908f65239f3e4f3608f9c9408f9d1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854665"
---
# <a name="design-an-er-format-to-keep-rows-together-on-the-same-excel-page"></a>Elektroonilise aruandluse vormingu loomine ridade samal Exceli lehel kooshoidmiseks

[!include [banner](../includes/banner.md)]


See artikkel selgitab [, kuidas kasutaja süsteemiadministraatoris või elektroonilise aruandluse funktsiooninõustaja rollis](general-electronic-reporting.md) saab konfigureerida elektroonilise aruandluse (ER) [...](er-overview-components.md#format-component)Microsoft Excel vormingut, mis loob väljaminevaid dokumente ja hallata dokumendi lehekülgede saalimise süsteemi nii, et loodud read hoitakse samal lehel.

Selles näites muudate Microsofti esitatud ER-vormingut, mida kasutatakse vabas vormis arvete printimiseks Excelis. Teie muudatused lasevad teil hallata loodud vabas vormis arve aruande lehekülgede saalimist nii, et kõik ühe arve rea read hoitakse võimalusel samal lehel.

Selle artikli protseduurid saab USMF-ettevõttes **lõpule** viia. Koodi pole vaja kirjutada.

Selles näites loote nõutavad ER konfiguratsioonid [näidisettevõttele](general-electronic-reporting.md#Configuration) **Litware, Inc**. Veenduge, et konfiguratsioonipakkuja **Litware, Inc.** (`http://www.litware.com`) näidisettevõttele on esitatud ER raamistikus ja et see on märgitud **aktiivseks**. Kui seda konfiguratsioonipakkujat pole loendis või **kui** see pole märgitud aktiivseks, [järgige konfiguratsioonipakkuja loomise juhiseid ja märkige see aktiivseks](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="enter-a-new-free-text-invoice"></a>Uue vabas vormis arve sisestamine

1. Vabas vormis arve [lisamiseks järgige vabas vormis](../../../finance/accounts-receivable/create-free-text-invoice-new.md#create-a-free-text-invoice-1) arve loomise juhiseid.

    1. Saate lisada arvele ühe rea.
    2. Saate lisada arvereale viis märkust.

    ![Arverea märkuste ülevaatamine lehel Manused](./media/er-keep-excel-rows-together-notes.png)

2. Järgige kopeerimisridade [samme](../../../finance/accounts-receivable/create-free-text-invoice-new.md#copy-lines), et luua viis täiendavat arverida, mis kopeeritakse eelmises sammus lisatud arvereale.

    ![Vabas vormis arve ridade ülevaatamine vabas vormis arve lehel.](./media/er-keep-excel-rows-together-invoice.png)

## <a name="configure-the-er-framework"></a>ER-raamistiku konfigureerimine

Minimaalsete [ER-i parameetrite konfigureerimine](er-quick-start2-customize-report.md#ConfigureFramework), mis on vajalikud ER-i raamistiku kasutamiseks. Enne ER-raamistiku kasutamist standardse ER-vormingu kohandatud versiooni loomiseks peate selle häälestuse lõpule viima.

## <a name="import-the-standard-er-format-configuration"></a>Standardse ER‑vormingu konfiguratsiooni importimine

Järgige standardse ER-vormingu [konfiguratsiooni importimise etappe](er-quick-start2-customize-report.md#ImportERSolution1), et lisada praegusele Dynamics 365 Finance'i eksemplarile standardsed ER-konfiguratsioonid. Näiteks saate importida versiooni **252.116** vabas **vormis arve (Exceli) vormingu** konfiguratsioonist. Arve põhimudeli **konfiguratsiooni baasversioon 252** **imporditakse** automaatselt hoidlast koos nõutava arvemudeli vastendamise **konfiguratsiooniga**.

## <a name="set-up-print-management-to-use-the-standard-er-format"></a>Seadista prindihaldus standardse ER-vormingu kasutamiseks

Järgige prindihalduse [seadistuse samme](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement1)**müügireskontro** mooduli prindihalduse konfigureerimiseks nii, et standardset ER-vormingut kasutatakse vabas vormis arvete printimiseks.

## <a name="configure-a-format-destination-for-the-standard-er-format"></a>Standardse ER-vormingu vormingu sihtkoha konfigureerimine

[Järgige ekraani eelvaate vormingu sihtkoha konfigureerimise samme standardse ER-vormingu ekraani ER sihtkoha konfigureerimiseks nii, et loodud aruanded teisendatakse PDF-vormingusse](er-quick-start1-new-solution.md#ConfigureDestination)[ja](er-destination-type-screen.md) kuvatakse eelvaated uuel brauseri vahekaardil.

## <a name="print-a-free-text-invoice-by-using-the-standard-er-format"></a>Vabas vormis arve printimine standardse ER-vormingu abil

1. Lisatud arve jaoks vabas [vormis arve aruande](er-embed-images-header-footer-excel-reports.md#ProcessInvoice1) loomiseks Exceli vormingus järgige standardse ER-vormingu printimise samme.
2. Laadige loodud Exceli töövihik alla ja vaadake see üle Exceli töölauarakenduses.

    Pange tähele, et arve kuues rida algab aruande esimesel leheküljel ja jätkub teisel leheküljel. Viimane märkus kuvatakse teisel leheküljel ja ei soovita, et see kuulub kuuele arvereale. Seetõttu muudab arverea sisu keskosas leheküljepiir seda dokumenti keerulisemaks.

    ![Loodud vabas vormis arve lehekülgede saalimise ülevaatamine Exceli töölauarakenduses](./media/er-keep-excel-rows-together-invoice1.gif)

Selle artikli ülejäänud protseduurid näitavad, kuidas häälestada standardset ER-vormingut, et parandada arve aruande ilmet ja loetavust, säilitades samal leheküljel ühe arverea kogu sisu.

## <a name="create-a-custom-format"></a>Kohandatud vormingu loomine

Järgige kohandatud vormingu [loomise](er-embed-images-header-footer-excel-reports.md#DeriveProvidedFormat) samme, et tuletada vorming imporditud ER-vormingust **ja luua vabas vormis arve (Excel)** kohandatud ER konfiguratsioon, mis on redigeerimiseks ja muutmiseks saadaval.

## <a name="edit-the-custom-format"></a>Redigeerige kohandatud vormi

1. Tuletatud [ER-vormingu avamiseks](er-embed-images-header-footer-excel-reports.md#ConfigureDerivedFormat) ER-vormingu kujundajas redigeerimiseks järgige juhiseid jaotises Kohandatud vormingu loomine.
2. Laiendage **vormingukujundaja lehel** vasakul **\>\> paanil vormingu komponendipuus valikut Vabas vormis arveleht InvoiceLines** **ja valige InvoiceLines_Values** komponent.
3. Seadke vahekaardil **Vorming** suvandi Säilita **read koos väärtuseks** **Jah**.

    ![Ridade kokku hoiamise suvandi seadmine redigeeritava ER-vormingu jaoks vormingukujundaja lehel](./media/er-keep-excel-rows-together-format.png)

4. Valige **Salvesta** ja sulgege leht.

## <a name="mark-the-custom-format-as-runnable"></a>Kohandatud vormingu märkimine käitatavaks

Kohandatud vormingu käitusajaks [märkimiseks](er-embed-images-header-footer-excel-reports.md#MarkFormatRunnable) järgige juhiseid, et muuta kohandatud ER-vormingu muudetud versioon käivitatavaks.

## <a name="set-up-print-management-to-use-the-custom-er-format"></a>Saate häälestada prindihaldust kohandatud ER-vormingu kasutamiseks.

Järgige prindihalduse [seadistuse samme](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement2)**müügireskontro** mooduli prindihalduse konfigureerimiseks nii, et kohandatud ER-vormingut kasutatakse vabas vormis arvete printimiseks.

## <a name="configure-a-format-destination-for-the-custom-er-format"></a>Vormingu sihtkoha konfigureerimine kohandatud ER-vormingu jaoks

[Järgige kohandatud ER-vormingu ekraani ER sihtkoha konfigureerimiseks ekraani eelvaate vormingu sihtkoha konfigureerimiseks nii, et loodud aruanded teisendatakse PDF-vormingusse](er-quick-start1-new-solution.md#ConfigureDestination)**ja** kuvatakse eelvaated uuel brauseri vahekaardil.

## <a name="print-a-free-text-invoice-by-using-the-custom-er-format"></a>Vabas vormis arve printimine standardse ER-vormingu abil

1. Lisatud arve jaoks vabas [vormis arve aruande](er-embed-images-header-footer-excel-reports.md#ProcessInvoice2) loomiseks Exceli vormingus järgige kohandatud ER-vormingu printimiseks toodud samme.
2. Laadige loodud Exceli töövihik alla ja vaadake see üle Exceli töölauarakenduses.

    Pange tähele, et arve kuues rida algab teisel leheküljel ja kõik seda arve rida tähistavad Exceli read ilmuvad sellel leheküljel koos.

    ![Loodud vabas vormis arve värskendatud lehekülgede saalimine Exceli töölauarakenduses](./media/er-keep-excel-rows-together-invoice2.gif)

## <a name="additional-resources"></a>Lisaressursid

[Konfiguratsiooni kujundamine dokumentide loomiseks Exceli vormingus](er-fillable-excel.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
