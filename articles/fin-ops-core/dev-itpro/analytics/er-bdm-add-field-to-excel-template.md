---
title: Äridokumendi mallile uute väljade lisamine Microsoft Excelis
description: See teema annab teavet selle kohta, kuidas lisada äridokumendi halduse funktsiooni kasutades Microsoft Excelis äridokumendi malli uusi välju.
author: NickSelin
manager: AnnBe
ms.date: 11/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 8c3a905c90f5dd4ad3487f004a958c0dcd52115d
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893243"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a>Äridokumendi mallile uute väljade lisamine Microsoft Excelis

[!include[banner](../includes/banner.md)]

Saate lisada uusi välju mallile, mida kasutatakse Microsoft Exceli vormingus äridokumentide koostamiseks. Neid välju saab lisada kohatäidetena, mida kasutatakse loodud dokumentide täitmiseks rakendusest nõutava teabega. Iga lisatava välja kohta saate määrata ka sidumise andmeallikatega, et määrata, millised rakenduse andmed väljale sisestatakse, kui malli kasutatakse äridokumentide loomiseks.

Lisateabe saamiseks selle funktsiooni kohta läbige siinse teema näide. Selles näites kirjeldatakse, kuidas värskendada malli, et täita vabas vormis arves loodud väljad.

## <a name="configure-business-document-management-to-edit-templates"></a>Mallide muutmiseks äridokumentide halduse konfigureerimine

Kuna äridokumentide haldus (BDM) on ehitatud raamistiku [elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md) peale, peate enne BDM-iga töötamise alustamist konfigureerima nõutud ER-i ja BDM-i parameetrid.

1.  Logige Microsoft Dynamics 365 Finance’i eksemplari süsteemiadministraatorina sisse.
2.  Läbige näidise järgmised etapid teemas [Äridokumentide halduse ülevaade](er-business-document-management.md).

    1.  Konfigureerige elektroonilise aruandluse parameetrid.
    2.  Lülitage BDM sisse.

Nüüd saate hakata kasutama BDM-i äridokumentide mallide redigeerimiseks.

## <a name="import-er-solutions-that-contain-a-template"></a>Malli sisaldavate elektroonilise aruandluse lahenduste importimine

Selle protseduuri näites kasutatakse ametlikult avaldatud elektroonilise aruandluse lahendust. Peate importima selle lahenduse elektroonilise aruandluse konfiguratsioonid oma praegusesse Finance’i eksemplari.

Selle lahenduse elektroonilise aruandluse konfiguratsioon **Vabas vormis arve (Excel)** sisaldab Exceli vormingus äridokumendi malli, mida saab BDM-i kasutades redigeerida. Importige selle elektroonilise aruandluse vormingu konfiguratsiooni uusim versioon portaalist Microsoft Dynamics Lifecycle Service (LCS). Vastav ER-i andmemudel ja ER-i mudelivastenduse konfiguratsioonid imporditakse automaatselt.

Elektroonilise aruandluse konfiguratsioonide importimise kohta lisateabe saamiseks vt [ER-seadistuse töötsükli haldamine](general-electronic-reporting-manage-configuration-lifecycle.md).

![LCS-i ühiste vahendite teegi leht](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a>Elektroonilise aruandluse lahenduse malli redigeerimine

1.  Logige sisse kasutajana, kellel on juurdepääs tööruumile **Äridokumentide haldus**.
2.  Avage tööruum **Äridokumentide halduse**.

    ![Äridokumentide halduse tööruum](./media/BDM-AddFldExcel-Workspace.png)

3.  Valige ruudustikus mall **Vabas vormis arve (Excel)**.
4.  Valige parempoolsel paanil **Uus mall**, et luua uus mall, mis põhineb valitud mallil.
5.  Sisestage väljale **Pealkiri** uue malli pealkirjaks **Contoso vabas vormis arve (Excel)**.
6.  Muutmis alustamise kinnitamiseks valige **OK**.

Kuvatakse BDM-i malli muutja leht. Saate kasutada rakendust Microsoft 365, et redigeerida valitud malli veebis manustatud juhtelemendis.

![BDM-i malli muutja leht](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a>Malli uuele väljale sildi lisamine

1.  Valige BDM-i malli muutja lehel Exceli lindil vahekaardil **Vaade** redigeeritava Exceli malli märkeruudud **Pealkirjad ja ruudujooned**.

    ![Märkeruudud Pealkirjad ja ruudujooned märgitud](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  Valige lahtrid **E8:F8**.
3.  Valige Exceli lindi vahekaardil **Avaleht** suvand **Ühenda ja joonda keskel**, et ühendada valitud lahtrid uueks ühendatud lahtriks **E8:F8**.
4.  Ühendatud lahtrisse **E8: F8** sisestage **URL**.
5.  Valige ühendatud lahter **E7:F7**, valige **Vormingupintsel** ja seejärel valige ühendatud lahter **E8:F8**, et vormindada see sarnaselt ühendatud lahtrile **E7:F7**.

    ![Mallile lisatud uue välja silt](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a>Malli vormindamine uue välja jaoks ruumi reserveerimiseks

1.  Valige lehel BDM-i malli muutja ühendatud lahter **G8:H8**.
2.  Valige Exceli lindi vahekaardil **Avaleht** suvand **Ühenda ja joonda keskel**, et ühendada valitud lahtrid uueks ühendatud lahtriks **G8:H8**.
3.  Valige ühendatud lahter **G7:H7**, valige **Vormingupintsel** ja seejärel valige ühendatud lahter **G8:H8**, et vormindada see sarnaselt ühendatud lahtrile **G7:H7**.

    ![Uue välja jaoks reserveeritud ruum](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  Boksiväljal **Nimi** valige **CompanyInfo**.

    Praeguse Exceli malli vahemik **CompanyInfo** sisaldab kõiki välju, mida kasutatakse loodud aruande päise täitmiseks koos praeguse ettevõtte kui müüja osapoole üksikasjadega.

    ![Vahemik CompanyInfo valitud](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a>Mallile uue välja lisamine

1.  Valige tegumiriba lehel **BDM-i malli muutja** suvand **Kuva vorming**.
2.  Valige paanil **Malli struktuur** suvand **Lisa**.

    > [!NOTE]
    > Peate kohandama malli sektsiooni, mida soovite uue väljana kasutada. Te juba tegite selle korrigeerimise ühendatud lahtri **G8:H8** vormindamisel.

    ![Mallile uue välja lisamine](./media/BDM-AddFldExcel-AddCell.png)

3.  Mallile uue välja lahtrina lisamiseks valige **Excel\lahter**.

    Kui soovite mallile lisada uue vahemiku, saate valida **Excel\vahemik**. Sisestatud vahemik võib sisaldada mitut lahtrit. Saate need lahtrid lisada hiljem.
    
    Pange tähele, et malli komponent **CompanyInfo** valitakse paanil**Malli struktuur** automaatselt, kuna see on praegu lisatava välja jaoks malli struktuuri kõige sobivam ülemkomponent.
    
4.  Sisestage väljal **Exceli vahemik** suvand **CompanyURL_Value**.
5.  Valige nupp **OK**.

    ![Väli CompanyURL_Value lisatud malli struktuuri](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  Paanil **Malli struktuur** valige kolmikpunkti nupp (...) ja seejärel valige **Kuva seosed**.

    ![Kuva seosed valitud](./media/BDM-AddFldExcel-ShowBindings.png)

    Paan **Malli struktuur** näitab andmeallikaid, mis on asjakohases ER-vormingus saadaval.

7.  Valige **CompanyInfo_Value** väljaks, mille plaanite asjakohase ER-vormingu andmeallikaga siduda.
8.  Jaotises **Andmeallikas** paanil **Malli struktuur** laiendage suvandit **Mudel \> InvoiceBase \> CompanyInfo**.
9.  Valige jaotises **CompanyInfo** üksus **WebsiteURI**.

    ![Üksus WebsiteURI valitud](./media/BDM-AddFldExcel-BindURL.png)

10. Valige **Seo**.
11. Valige paanil **Malli struktuur** suvand **Salvesta** ja seejärel sulgege BDM-i malli muutja leht.

Tööruumi **Äridokumendi haldus** paremal paanil asuv vahekaart **Mall** näitab värskendatud malli. Pange tähele, et ruudustikus on malli väli **Olek** muudetud suvandil **Mustand** ja väli **Redaktsioon** ei ole enam tühi. Need muudatused näitavad, et selle malli muutmise protsess on alanud.

![Muudetud mall tööruumis Äridokumentide haldus](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a>Ettevõtete sätete ülevaatamine

1.  Avage **Organisatsiooni haldus \> Organisatsioonid \> Juriidilised isikud**.
2.  Kontrollige kiirkaardil**Kontaktteave**, kas ettevõtte URL on sisestatud.

![Ettevõtte URL sisestatud lehele Juriidilised isikud](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a>Äridokumentide loomine värskendatud malli testimiseks

1.  Muutke rakenduses ettevõte valikule **USMF**ja avage **Müügireskontro \> Arved \> Kõik vabas vormis arved**.
2.  Valige arve **FTI-00000002** ja seejärel valige **Prindihaldus**.
3.  Vasakpoolsel paanil laiendage **Moodul – müügireskontro \> Dokumendid \> Vabas vormis arve**.
4.  Suvandis **Vabas vormis arve** valge tase **Algne dokument**, et määratleda töötlemiseks arvete ulatus.
5.  Valige paremal paanil väljal **Aruande vorming** mall **Contoso vabas vormis arve (Excel)** konkreetse dokumendi taseme jaoks.

    ![Mall Contoso vabas vormis arve (Excel) valitud](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  Praeguse lehe sulgemiseks vajutage **Paoklahvi (Esc)**.
7.  Valige **Prindi \> Valitud**.
8.  Laadige loodud dokument alla ja avage see Excelis.

    ![Vabas vormis arve Excelis](./media/BDM-AddFldExcel-PreviewReport.png)

Muudetud malliga luuakse valitud üksuse vabas tekstis arve aruanne. Selleks, et analüüsida, kuidas malli muudatused mõjutavad seda aruannet, käivitage aruanne ühes rakenduse seansis kohe pärast malli muutmist teises rakenduse seansis.

## <a name="related-links"></a>Seotud lingid

[Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)

[Äridokumentide halduse ülevaade](er-business-document-management.md)

[OPENXML-vormingus aruannete loomiseks konfiguratsiooni koostamine](tasks/er-design-reports-openxml-2016-11.md)
