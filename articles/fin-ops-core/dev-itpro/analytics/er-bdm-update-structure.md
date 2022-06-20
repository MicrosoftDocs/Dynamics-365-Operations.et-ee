---
title: Äridokumendimalli struktuuri värskendamine
description: See artikkel selgitab äridokumendi malli struktuuri värskendust äridokumendi halduse funktsiooni abil.
author: NickSelin
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 2adecba4e988bfe04de2c181501b6c3ef8491dcf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880279"
---
# <a name="update-the-structure-of-a-business-document-template"></a>Äridokumendimalli struktuuri värskendamine 

[!include[banner](../includes/banner.md)]

**Malli struktuuri** paanil [äridokumendi halduse](er-business-document-management.md) malli redaktoris saate muuta äridokumendi malli, [lisades uued väljad](er-bdm-add-field-to-excel-template.md) Microsoft Exceli mallile. Seejärel uuendatakse malli struktuur automaatselt Dynamics 365 Finance'is nii, **et see peegeldab mallistruktuuri paanil tehtud** muudatusi.

Samuti saate malli muuta, kasutades Office 365 veebipõhiseid funktsioone. Näiteks saate lisada muudetavale töölehele uue nimega üksuse (nt pildi või kujundi). Sel juhul malli struktuuri rakenduses Finance automaatselt ei värskendata ja lisatud üksus ei ilmu paanil **Malli struktuur**. Värskendage malli struktuuri rakenduses Finance käsitsi, klõpsates malli redaktori lehel suvandi **Värskenda struktuuri**.

Lisateabe saamiseks selle funktsiooni kohta läbige järgmine näide.

## <a name="example-update-the-structure-of-a-business-document-template"></a>Näide. Äridokumendimalli struktuuri värskendamine

See näide näitab, kuidas süsteemiadministraator saab värskendada äridokumendi malli struktuuri rakenduses Finance pärast seda, kui mall on Office Online’is muudetud. Järgmised jaotised selgitavad kaasatud etappe.

### <a name="prepare-a-business-document-template-for-editing"></a>Äridokumendi malli redigeerimiseks ettevalmistamine

Tehke [äridokumendi halduse ülevaates](er-business-document-management.md) järgmised protseduurid.

1. [Elektroonilise aruandluse parameetrite konfigureerimine](er-business-document-management.md#configure-er-parameters)
2. [Impordi ER-lahendused](er-business-document-management.md#import-er-solutions)
3. [Lubage äridokumentide haldus](er-business-document-management.md#enable-business-document-management)
4. [Seadistage parameetrid](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a>Äridokumendimallide redigeerimine

1. Valige **Äridokumentide halduse** tööruumis **Uus dokument**.
2. Valige lehel **Uue malli loomine** mall **Vabas vormis arve (ER-i näidis) (Excel)**.
3. Valige **Loo dokument**.
4. Väljale **Pealkiri** sisestage väärtus **FTI näidis, Litware**.
5. Valige uue malli loomiseks **OK**.

    > [!NOTE]
    > Kui te pole veel Office Online’i sisse loginud, [suunatakse teid Office 365 sisselogimise lehele](er-business-document-management.md#frequently-asked-questions). Rakenduse Finance keskkonda naasmiseks valige brauseris nupp **Tagasi**.

    Uus mall on redigeerimiseks avatud Excel Online’i malli redaktori lehel manustatud juhtelemendis.

[![Äridokumentide halduse tööruumi kasutamine äridokumendi malli redigeerimise alustamiseks.](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)

### <a name="review-the-current-structure-of-the-editable-template"></a>Redigeeritava malli praeguse struktuuri läbivaatamine

1. Klõpsake rakenduses Excel Online ribal vahekaardi **Vaade** grupi **Kuvamine** suvandit **Ruudujooned**.
2. Valige redigeeritavas mallis malli pealkirja kohal olev ristkülik. See ristkülik on pilt, mille nimi on **rptHeaderCompLogo**.
3. Kui paan **Malli struktuur** on peidetud, valige **Kuva struktuur**.
4. Laiendage paanil **Malli struktuur** suvandit **Aruanne \> Arve \> rptHeader \> rptHeaderPart1**.
5. Pange tähele, et rakenduse Finance malli struktuuris on üksus **rptHeaderCompLogo** esitatud suvandi **Aruanne \> Arve \> rptHeader \> rptHeaderPart1** allüksusena.

[![Äridokumentide halduse tööruumi kasutamine redigeeritud malli praeguse struktuuri läbivaatamiseks.](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a>Äridokumendimalli struktuuri värskendamine kustutades pildi

1. Valige Excel Online’is redigeeritav mall, valige pilt **rptHeaderCompLogo**.
2. Valitud pildi redigeeritavast mallist kustutamiseks järgige üht järgmistest sammudest.

    - Valige klaviatuurilt klahv **Kustuta**.
    - Valige ja hoidke (või paremklõpsake) pilti ning valige seejärel suvand **Lõika**.

    > [!NOTE]
    > Üksus **RptHeaderCompLogo** on praegu rakenduse Finance malli struktuuris endiselt alles, olgugi pilti enam Exceli malli ei lisata.

3. Valige **Värskenda struktuuri**, et sünkroonida redigeeritava malli struktuuri rakendustes Excel ja Finance.
4. Laiendage paanil **Malli struktuur** suvandit **Aruanne \> Arve \> rptHeader \> rptHeaderPart1**.
5. Pange tähele, et üksus **rptHeaderCompLogo** ei sisaldu enam rakenduse Finance malli struktuuris.

[![Äridokumentide halduse tööruumi kasutamine äridokumendi mallist pildi kustutamiseks.](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a>Äridokumendimalli struktuuri värskendamine lisades pildi

1. Klõpsake rakenduses Excel Online ribal vahekaardi **Lisamine** grupi **Illustratsioonid** suvandit **Pilt**.
2. Valige käsk **Vali fail**, sirvige pildini, mille soovite lisada, valige see ja seejärel valige **OK**.
3. Valige nupp **Sisesta**.
4. Liigutage uut pilti, kuni see on õiges kohas. Vaikimisi paneb pildile nime Excel. Näiteks võib see panna pildi nimeks **Pilt 2**.
5. Valige **Värskenda struktuuri**, et sünkroonida redigeeritava malli struktuuri rakendustes Excel ja Finance.
6. Laiendage paanil **Malli struktuur** suvandit **Aruanne \> Arve \> rptHeader \> rptHeaderPart1**.
7. Pange tähele, et uus pilt on nüüd lisatud üksusena rakenduse Finance malli struktuuri.

[![Äridokumentide halduse tööruumi kasutamine äridokumendi mallile pildi lisamiseks.](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)

## <a name="related-links"></a>Seotud lingid

[Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)

[Äridokumentide halduse ülevaade](er-business-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]