---
title: Konfiguratsiooni kujundamine dokumentide loomiseks Exceli vormingus
description: Selles teemas antakse teavet selle kohta, kuidas kujundada elektroonilise aruandluse (ER) vormingut Exceli malli täitmiseks ja seejärel luua väljaminevaid Exceli vormingus dokumente.
author: NickSelin
manager: AnnBe
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d5733e40c67f9c97b04f126f7c3cfea9d4f8f5b5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686534"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a>Konfiguratsiooni kujundamine dokumentide loomiseks Exceli vormingus

[!include[banner](../includes/banner.md)]

Saate luua [Elektroonilise aruandluse (ER)](general-electronic-reporting.md) vormingu konfiguratsiooni, millel on ER-i [vormingu komponent](general-electronic-reporting.md#FormatComponentOutbound), mida saate konfigureerida väljamineva Microsoft Exceli töövihiku vormingus dokumendi loomiseks. Sellel otstarbel tuleb kasutada kindlaid ER-vormingu komponente.

Lisateabe saamiseks selle funktsiooni kohta, järgige teemas [Konfiguratsiooni kujundamine aruannete loomiseks OPENXML-vormingus](tasks/er-design-reports-openxml-2016-11.md) toodud etappe.

## <a name="add-a-new-er-format"></a>Uue ER-vormingu lisamine

Kui lisate uue ER-vormingu konfiguratsiooni Exceli töövihiku vormingus väljamineva dokumendi loomiseks, peate valima väärtuse **Excel** vormingu atribuudi **Vormingu tüüp** jaoks või jätma atribuudi **Vormingu tüüp** tühjaks.

- Kui teete valiku **Excel**, saate konfigureerida vormingu väljamineva dokumendi loomiseks ainult Exceli vormingus.
- Kui jätate atribuudi tühjaks, saate konfigureerida vormingu väljamineva dokumendi loomiseks mis tahes vormingus, mida ER-i raamistik toetab.

Konfiguratsiooni ER-vormingu komponendi konfigureerimiseks valige Toimingupaanil **Kujundaja** ja avage ER-vormingu komponent selle redigeerimiseks ER-i toimingu koostajas.

![Konfiguratsioonide leht](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a>Exceli faili komponent

### <a name="manual-entry"></a>Käsitsi kirje

Peate lisama konfigureeritud ER-vormingule komponendi **Excel\\File**, et luua Exceli vormingus väljaminev dokument.

![Komponent Excel\File](./media/er-excel-format-add-file-component.png)

Väljamineva dokumendi paigutuse määramiseks lisage Exceli töövihik, millel on laiend .xlsx, komponendile **Excel\\File** väljaminevate dokumentide mallina kasutamiseks.

> [!NOTE]
> Malli käsitsi manustamisel peate kasutama [dokumendi tüüpi](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types), mis on konfigureeritud selleks otstarbeks [ER-i parameetrites](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).

![Komponendile Excel\fail manuse lisamine](./media/er-excel-format-add-file-component2.png)

Selleks, et määrata, kuidas lisatud mall täidetakse konfigureeritud ER-vormingu käitamisel, tuleb teil lisada pesastatud komponendid **Leht**, **Vahemik** ja **Lahter** komponendile **Excel\\File**. Iga pesastatud komponent peab olema seostatud Exceli nimega üksusega.

### <a name="template-import"></a>Malli importimine

Saate valida Toimingupaani **Excelist importimine** vahekaardi **Importimine**, et importida uus mall tühja ER-vormingusse. Selles näites luuakse komponent **Excel\\File** automaatselt ja sellele manustatakse imporditud mall. Kõik nõutavad ER-komponendid luuakse samuti automaatselt, võttes aluseks leitud Exceli nimega üksuste loendi.

![Suvandi Excelist importimine valimine](./media/er-excel-format-import-template.png)

> [!NOTE]
> Kui soovite luua redigeeritavas ER-vormingus valikulise elemendi **Leht** seadke suvandi **Exceli vorminguelemendi Leht loomine** väärtuseks **Jah**.

## <a name="sheet-component"></a>Lehe komponent

Komponent **Leht** tähistab manustatud Exceli töövihiku töölehte, mis tuleb ära täita. Exceli malli töölehe nimi määratletakse selle komponendi atribuudis **Leht**.

> [!NOTE]
> See komponent on valikuline Exceli töövihikute puhul, mis sisaldavad ühte töölehte.

ER-i toimingu koostaja vahekaardil **Vastendamine** saate konfigureerida komponendi **Leht** jaoks atribuudi **Lubatud**, et määrata, kas komponent tuleks lisada loodud dokumenti.

- Kui atribuudi **Lubatud** avaldis on konfigureeritud tagastama käitusajal väärtuse **Tõene** või kui ühtegi avaldist pole konfigureeritud, lisatakse loodud dokumenti vastav tööleht.
- Kui atribuudi **Lubatud** avaldis on konfigureeritud tagastama käitusajal väärtuse **Väär**, ei sisalda loodud dokument töölehte.

![Lehe komponendi näide](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a>Vahemiku komponent

Komponent **Vahemik** tähistab Exceli vahemikku, mida selle ER-komponendiga tuleb juhtida. Vahemiku nimi määratletakse selle komponendi atribuudis **Exceli vahemik**.

Atribuut **Edastamise suund** määrab, kas ja kuidas vahemik kordub loodud dokumendis.

- Kui atribuudi **Edastamise suund** värtuseks on seatud **Andmeedastust pole**, ei korrata loodud dokumendis vastavat Exceli vahemikku.
- Kui atribuudi **Edastamise suund** värtuseks on seatud **Vertikaalne**, korratakse loodud dokumendis vastavat Exceli vahemikku. Iga edastatud vahemik lisatakse Exceli mallis algse vahemiku alla. Korduste arv määratletakse tüübi **Kirje loend** andmeallika kirjete arvu põhjal, mis seotakse selle ER-komponendiga.
- Kui atribuudi **Edastamise suund** värtuseks on seatud **Horisontaalne**, korratakse loodud dokumendis vastavat Exceli vahemikku. Iga edastatud vahemik lisatakse Exceli mallis algsest vahemikust paremale. Korduste arv määratletakse tüübi **Kirje loend** andmeallika kirjete arvu põhjal, mis seotakse selle ER-komponendiga.

Horisontaalse edastamise kohta lisateabe saamiseks järgige teemas [Horisontaalselt laiendatavate vahemike kasutamine Exceli aruannete veergude lisamiseks dünaamiliselt](tasks/er-horizontal-1.md) toodud etappe.

Komponendil **Vahemik** võib olla muid pesastatud ER-komponente, mida kasutatakse vastavate Exceli nimega vahemike väärtuste sisestamiseks.

- Kui mõnda grupi **Tekst** komponenti kasutatakse väärtuste sisestamiseks, sisestatakse väärtus Exceli vahemikku teksti väärtusena.

    > [!NOTE]
    > Saate kasutada seda mustrit sisestatud väärtuste vormindamiseks rakenduses määratletud lokaadi alusel.

- Kui grupi **Excel** komponenti **Lahter** kasutatakse väärtuste sisestamiseks, sisestatakse väärtus Exceli vahemikku andmetüübi väärtusena, mis määratletakse selle komponendi **Lahter** sidumisega (nt **String**, **Tegelik** või **Täisarv**).

    > [!NOTE]
    > Saate kasutada seda mustrit, et lubada Exceli rakendusel vormindada sisestatud väärtusi kohaliku arvuti lokaadi alusel, mis avab väljamineva dokumendi.

ER-i toimingu koostaja vahekaardil **Vastendamine** saate konfigureerida komponendi **Vahemik** jaoks atribuudi **Lubatud**, et määrata, kas komponent tuleks lisada loodud dokumenti.

- Kui atribuudi **Lubatud** avaldis on konfigureeritud tagastama käitusajal väärtuse **Tõene** või kui ühtegi avaldist pole konfigureeritud, täidetakse loodud dokumedis vastav vahemik.
- Kui atribuudi **Lubatud** avaldis on konfigureeritud tagastama käitusajal väärtuse **Väär** ja see vahemik ei esinda terveid ridu või veerge, ei täideta loodud dokumedis vastavat vahemikku.
- Kui atribuudi **Lubatud** avaldis on konfigureeritud tagastama käitusajal väärtuse **Väär** ja see vahemik esindab terveid ridu või veerge, sisaldab loodud dokument neid ridu ja veerge peidetud ridade ja veergudena.

## <a name="cell-component"></a>Lahtri komponent

Komponenti **Lahter** kasutatakse Exceli nimega lahtrite, kujundite ja piltide täitmiseks. Selleks, et näidata Exceli nimega objekti, mille peab täitma ER-komponent **Lahter**, peate määrama selle objekti nime komponendi **Lahter** atribuudis **Exceli vahemik**.

ER-i toimingu koostaja vahekaardil **Vastendamine** saate konfigureerida komponendi **Lahter** jaoks atribuudi **Lubatud**, et määrata, kas objekt tuleks täita loodud dokumendis.

- Kui atribuudi **Lubatud** avaldis on konfigureeritud tagastama käitusajal väärtuse **Tõene** või kui ühtegi avaldist pole konfigureeritud, täidetakse loodud dokumedis vastav objekt. Selle komponendi **Lahter** sidumine määrab väärtuse, mis lisatakse vastavale objektile.
- Kui atribuudi **Lubatud** avaldis on konfigureeritud tagastama käitusajal väärtuse **Väär**, ei täideta loodud dokumendis vastavat objekti.

Kui komponent **Lahter** konfigureeritakse sisestama väärtust lahtrisse, saab seda siduda andmeallikaga, mis tagastab primitiivse andmetüübi väärtuse (nt **String**, **Tegelik** või **Täisarv**). Sellisel juhul sisestatakse väärtus lahtrisse sama andmetüübi väärtusena.

Kui komponent **Lahter** konfigureeritakse sisestama väärtust Exceli kujundisse, saab seda siduda andmeallikaga, mis tagastab primitiivse andmetüübi väärtuse (nt **String**, **Tegelik** või **Täisarv**). Sellisel juhul sisestatakse väärtus Exceli kujundisse selle kujundi tekstina. Andmetüüpide väärtused, mis ei ole **String**, teisendatakse tekstiks automaatselt.

> [!NOTE]
> Saate konfigureerida komponendi **Lahter** täitma kujundit ainult juhul, kui kujundi teksti atribuuti toetatakse.

Kui komponent **Lahter** konfigureeritakse sisestama väärtust Exceli pilti, saab seda siduda andmeallikaga, mis tagastab andmetüübi **Konteiner** väärtuse, mis esindab pilti binaarvormingus. Sellisel juhul sisestatakse Exceli pildil olev väärtus pildina.

> [!NOTE]
> Kõik Exceli pildid ja kujundid on mõeldud kindla Exceli lahtri või vahemiku vasakusse ülanurka ankurdamiseks. Kui soovite Exceli pilti või kujundit kopeerida, peate konfigureerima lahtri või vahemiku, millele see on ankurdatud, kopeeritud lahtri või vahemikuna.

Lisateavet piltide ja kujundite manustamise kohta leiate teemast [Piltide ja kujundite manustamine ER-i abil loodud dokumentidesse](electronic-reporting-embed-images-shapes.md).

## <a name="page-break-component"></a>Lehepiiri komponent

Komponent **PageBreak** sunnib Excelit uut lehte alustama. See komponent pole nõutav, kui soovite kasutada Exceli vaikimisi lehekülgede saalimist, kuid peaksite seda kasutama juhul, kui soovite, et Excel järgiks teie ER-vormingut lehekülgede saalimise struktureerimisel.

## <a name="edit-an-added-er-format"></a>Lisatud ER-vormingu redigeerimine

### <a name="update-a-template"></a>Malli värskendamine

Saate valida Toimingupaani **Excelist värskendamine** vahekaardi **Importimine**, et importida värskendatud mall redigeeritavasse ER-vormingusse. Selle protsessi käigus asendatakse valitud komponent **Excel\\File** uue malliga. Redigeeritava ER-vormingu sisu sünkroonitakse värskendatud ER-i malli sisuga.

- Uus ER-vormingu komponent luuakse automaatselt iga Exceli nime kohta, kui redigeeritavast vormist ei leida ER-vormingu komponenti.
- Redigeeritavast ER-vormingust kustutatakse kõik ER-vormingu komponendid, mille kohta ei ei leita sobivat Exceli nime.

> [!NOTE]
> Seadke suvandi **Exceli vorminguelemendi Leht loomine** väärtuseks **Jah**, kui soovite luua redigeeritavas ER-vormingus valikulise elemendi **Leht**.
>
> Kui redigeeritav ER-vorming sisaldas algselt elemente **Leht**, soovitame teil värskendatud malli importimisel määdata suvandi **Exceli vorminguelemendi Leht loomine** väärtuseks **Jah**. Vastasel juhul luuakse kõik algse elemendi **Leht** pesastatud elemendid nullist. Seetõttu lähevad kõik uuesti loodud vorminguelementide sidumised värskendatud ER-vormingus kaotsi.

![Exceli vorminguelemendi Leht suvandi loomine dialoogiboksis Excelist värskendamine](./media/er-excel-format-update-template.png)

Selle funktsiooni kohta lisateabe saamiseks järgige teemas [Elekrtoonilise aruandluse muutmine Exceli mallide uuesti rakendamise teel](modify-electronic-reporting-format-reapply-excel-template.md) toodud etappe.

## <a name="validate-an-er-format"></a>ER-vormingu kinnitamine

Kui kinnitate redigeeritavat ER-vormingut, tehakse järjepidevuse kontroll, et veenduda, kas Exceli nimi on praegu kasutatavas Exceli mallis olemas. Teid teavitatakse kõigist vastuoludest. Osade vastuolude korral pakutakse probleemi automaatse lahendamise valikut.

![Kinnitamise tõrketeated](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a>Exceli valemite arvutamise juhtimine

Kui luuakse väljaminev töövihikuvormingus Microsoft Exceli dokument, võivad mõned selle dokumendi lahtrid sisaldada Exceli valemeid. Kui funktsioon **Luba EPPlusi teegi kasutamine elektroonilise aruandluse raamistikus** on lubatud, saate kontrollida, millal valemid arvutatakse, muutes kasutatavas Exceli mallis **arvutamise valikute** [parameetrit](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows).

- Valige suvand **Automaatne**, et arvutada kõik sõltuvad valemid iga kord uuesti, kui loodud dokumendile lisatakse uued vahemikud, lahtrid jne.
    >[!NOTE]
    > See võib põhjustada mitut seotud valemit sisaldavate Exceli mallide korral jõudlusprobleemi.
- Valige **Käsitsi**, et vältida dokumendi loomisel valemi uuesti arvutamist.
    >[!NOTE]
    > Valemi uuesti arvutamine tehakse käsitsi, kui loodud dokument avatakse Excelit kasutades eelvaateks.
    > Ärge kasutage seda valikut, kui konfigureerite ER-i sihtkohta, mis eeldab loodud dokumendi kasutamist ilma selle eelvaateta Excelis (PDF-i teisendamine, meilimine jne)., kuna loodud dokument ei pruugi omada valemeid sisaldavates lahtrites väärtusi.

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)

[OPENXML-vormingus aruannete loomiseks konfiguratsiooni koostamine](tasks\er-design-reports-openxml-2016-11.md)

[Elektroonilise aruandluse vormingute muutmine Exceli malle uuesti rakendades](modify-electronic-reporting-format-reapply-excel-template.md)

[Horisontaalselt laiendatavate vahemike kasutamine veergude dünaamiliseks lisamiseks Exceli aruannetes](tasks/er-horizontal-1.md)

[Manustatud pildid ja kujutised ER-iga loodud dokumentides](electronic-reporting-embed-images-shapes.md)

[Elektroonilise aruandluse (ER) konfigureerimine andmete tõmbamiseks Power BI-sse](general-electronic-reporting-report-configuration-get-data-powerbi.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]