---
title: Konfiguratsiooni kujundamine dokumentide loomiseks Exceli vormingus
description: See artikkel kirjeldab, kuidas kujundada elektroonilise aruandluse (ER) vormingut Exceli malli täitmiseks ja seejärel luua väljaminevad Exceli vormingu dokumendid.
author: kfend
ms.date: 05/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.form: EROperationDesigner, ERParameters
ms.openlocfilehash: 2feadf8e196936220cf557989cae40b742447d99
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280920"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a>Konfiguratsiooni kujundamine dokumentide loomiseks Exceli vormingus

[!include[banner](../includes/banner.md)]

Saate kujundada elektroonilise [aruandluse (ER)](general-electronic-reporting.md) vormingu konfiguratsiooni, mis sisaldab ER-vormingu komponenti, mida saate konfigureerida väljamineva dokumendi loomiseks töövihiku Microsoft Excel vormingus. Sellel otstarbel tuleb kasutada kindlaid ER-vormingu komponente.

Selle funktsiooni kohta lisateabe saamiseks järgige artikli samme. [Kujundage konfiguratsiooni aruannete loomiseks OPENXML-vormingus](tasks/er-design-reports-openxml-2016-11.md).

## <a name="add-a-new-er-format"></a>Uue ER-vormingu lisamine

Kui lisate uue ER-vormingu konfiguratsiooni Exceli töövihiku vormingus väljamineva dokumendi loomiseks, peate valima väärtuse **Excel** vormingu atribuudi **Vormingu tüüp** jaoks või jätma atribuudi **Vormingu tüüp** tühjaks.

- Kui teete valiku **Excel**, saate konfigureerida vormingu väljamineva dokumendi loomiseks ainult Exceli vormingus.
- Kui jätate atribuudi tühjaks, saate konfigureerida vormingu väljamineva dokumendi loomiseks mis tahes vormingus, mida ER-i raamistik toetab.

Konfiguratsiooni ER-vormingu komponendi konfigureerimiseks valige Toimingupaanil **Kujundaja** ja avage ER-vormingu komponent selle redigeerimiseks ER-i toimingu koostajas.

![Konfiguratsioonide leht.](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a>Exceli faili komponent

### <a name="manual-entry"></a>Käsitsi kirje

Peate lisama konfigureeritud ER-vormingule komponendi **Excel\\File**, et luua Exceli vormingus väljaminev dokument.

![Komponent Excel\Fail.](./media/er-excel-format-add-file-component.png)

Väljamineva dokumendi paigutuse määramiseks lisage Exceli töövihik, millel on laiend .xlsx, komponendile **Excel\\File** väljaminevate dokumentide mallina kasutamiseks.

> [!NOTE]
> Malli käsitsi manustamisel peate kasutama [dokumendi tüüpi](../../../fin-ops-core/fin-ops/organization-administration/configure-document-management.md#configure-document-types), mis on konfigureeritud selleks otstarbeks [ER-i parameetrites](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).

![Komponendile Excel\fail manuse lisamine.](./media/er-excel-format-add-file-component2.png)

Selleks, et määrata, kuidas lisatud mall täidetakse konfigureeritud ER-vormingu käitamisel, tuleb teil lisada pesastatud komponendid **Leht**, **Vahemik** ja **Lahter** komponendile **Excel\\File**. Iga pesastatud komponent peab olema seostatud Exceli nimega üksusega.

### <a name="template-import"></a>Malli importimine

Saate valida Toimingupaani **Excelist importimine** vahekaardi **Importimine**, et importida uus mall tühja ER-vormingusse. Selles näites luuakse komponent **Excel\\File** automaatselt ja sellele manustatakse imporditud mall. Kõik nõutavad ER-komponendid luuakse samuti automaatselt, võttes aluseks leitud Exceli nimega üksuste loendi.

![Excelist importimise valimine.](./media/er-excel-format-import-template.png)

> [!NOTE]
> Kui soovite luua redigeeritavas ER-vormingus valikulise elemendi **Leht** seadke suvandi **Exceli vorminguelemendi Leht loomine** väärtuseks **Jah**.

## <a name="sheet-component"></a>Lehe komponent

Komponent **Leht** tähistab manustatud Exceli töövihiku töölehte, mis tuleb ära täita. Exceli malli töölehe nimi määratletakse selle komponendi atribuudis **Leht**.

> [!NOTE]
> See komponent on valikuline Exceli töövihikute puhul, mis sisaldavad ühte töölehte.

ER-i toimingu koostaja vahekaardil **Vastendamine** saate konfigureerida komponendi **Leht** jaoks atribuudi **Lubatud**, et määrata, kas komponent tuleks lisada loodud dokumenti.

- Kui atribuudi **Lubatud** avaldis on konfigureeritud tagastama käitusajal väärtuse **Tõene** või kui ühtegi avaldist pole konfigureeritud, lisatakse loodud dokumenti vastav tööleht.
- Kui atribuudi **Lubatud** avaldis on konfigureeritud tagastama käitusajal väärtuse **Väär**, ei sisalda loodud dokument töölehte.

![Lehe komponendi näide.](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a>Vahemiku komponent

### <a name="nested-components"></a>Pesastatud komponendid

#### <a name="data-typing"></a>Andmete tippimine

**Vahemiku** komponendil võivad olla teised pesastatud ER-komponendid, mida kasutatakse väärtuste sisestamiseks sobivasse vahemikku.

- Kui mõnda grupi **Tekst** komponenti kasutatakse väärtuste sisestamiseks, sisestatakse väärtus Exceli vahemikku teksti väärtusena.

    > [!NOTE]
    > Saate kasutada seda mustrit sisestatud väärtuste vormindamiseks rakenduses määratletud lokaadi alusel.

- Kui Exceli **grupi** **lahtrikomponenti** kasutatakse väärtuste sisestamiseks, sisestatakse väärtus Exceli vahemikku andmetüübi väärtusena, mis määratletakse selle lahtrikomponendi **sidumisega**. Näiteks võib andmetüüp olla String **, Reaalarv** või **Täisarv**. **·**

    > [!NOTE]
    > Saate kasutada seda mustrit, et lubada Exceli rakendusel vormindada sisestatud väärtusi kohaliku arvuti lokaadi alusel, mis avab väljamineva dokumendi.

#### <a name="row-handling"></a>Rea käsitsemine

**Vahemiku** komponenti saab konfigureerida vertikaalselt kopeeritult, nii et Exceli töölehel luuakse mitu rida. Ridu saab luua emavahemiku **komponendi või** pesastatud vahemiku **komponentide** alusel.

Versioonis 10.0.26 ja uuemas saate sundida loodud töölehte hoidma loodud read samal leheküljel. Seadke ER-vormingu kujundajas **ridade kokku** **·** **hoiamissuvand** emavahemiku komponendi jaoks redigeeritavas ER-vormingus suvandile Jah. ER proovib säilitada kogu selle vahemiku loodud sisu samal leheküljel. Kui sisu kõrgus ületab praeguse lehekülje ülejäänud ruumi, lisatakse leheküljepiir ja sisu algab järgmise uue lehekülje ülaosas.

> [!NOTE]
> Soovitame teil konfigureerida suvand Säilita **read koos** ainult vahemike jaoks, mis ulatuvad kogu loodud dokumendi laiuseni.
>
> Suvand **Säilita read koos** kehtib ainult Exceli faili **komponentidele \>**, mis on konfigureeritud kasutama Exceli töövihiku malli.
>
> Valikut **Säilita read koos** saab kasutada ainult siis, **kui on lubatud funktsioon EP Andmebaasi teegi kasutamine elektroonilise aruandluse** raamistikus.
>
> Seda funktsiooni saab kasutada lehe **komponendis** paiknevate vahemiku **komponentide** puhul. Kuid puudub garantii, et lehe [jaluse kogusummad](er-paginate-excel-reports.md#add-data-sources-to-calculate-page-footer-totals) arvutatakse õigesti andmekogumi [andmeallikate](er-data-collection-data-sources.md) abil.

Selle suvandi kasutamise kohta lisateabe saamiseks järgige [ER-vormingu kujundamise näiteid, et read samal Exceli lehel koos olla](er-keep-excel-rows-together.md).

### <a name="replication"></a>Andmeedastus

Andmeedastussuuna **atribuut** määrab, kas ja kuidas vahemikku loodud dokumendis korratakse:

- **Andmeedastus puudub** – sobivat Exceli vahemikku ei korrata loodud dokumendis.
- **Vertikaalne** – sobivat Exceli vahemikku korratakse loodud dokumendis vertikaalselt. Iga kopeeritud vahemik pannakse Exceli mallis algse vahemiku alla. Korduste arv määratletakse tüübi **Kirje loend** andmeallika kirjete arvu põhjal, mis seotakse selle ER-komponendiga.
- **Horisontaalne** – loodud dokumendis korratakse horisontaalselt sobivat Exceli vahemikku. Iga kopeeritud vahemik pannakse Exceli mallis algsest vahemikust paremale. Korduste arv määratletakse tüübi **Kirje loend** andmeallika kirjete arvu põhjal, mis seotakse selle ER-komponendiga.

    Horisontaalse edastamise kohta lisateabe saamiseks järgige teemas [Horisontaalselt laiendatavate vahemike kasutamine Exceli aruannete veergude lisamiseks dünaamiliselt](tasks/er-horizontal-1.md) toodud etappe.

### <a name="enabling"></a>Lubamine

ER-i toimingu koostaja vahekaardil **Vastendamine** saate konfigureerida komponendi **Vahemik** jaoks atribuudi **Lubatud**, et määrata, kas komponent tuleks lisada loodud dokumenti.

- Kui atribuudi **Lubatud** avaldis on konfigureeritud tagastama käitusajal väärtuse **Tõene** või kui ühtegi avaldist pole konfigureeritud, täidetakse loodud dokumedis vastav vahemik.
- Kui atribuudi **Lubatud** avaldis on konfigureeritud tagastama käitusajal väärtuse **Väär** ja see vahemik ei esinda terveid ridu või veerge, ei täideta loodud dokumedis vastavat vahemikku.
- Kui atribuudi **Lubatud** avaldis on konfigureeritud tagastama käitusajal väärtuse **Väär** ja see vahemik esindab terveid ridu või veerge, sisaldab loodud dokument neid ridu ja veerge peidetud ridade ja veergudena.

### <a name="resizing"></a>Suuruse muutmine

Te saate konfigureerida oma Exceli malli, et kasutada lahtrid tekstiandmete esitlemiseks. Tagamaks, et kogu tekst lahtris on loodud dokumendis nähtav, saate selle lahtri konfigureerida automaatselt selle sees oleva teksti vormindama. Kui tekstiline tekst ei ole täielikult nähtav, saate seda lahtrit sisaldava rea konfigureerimisel automaatselt selle kõrgust korrigeerida. Lisateavet vt jaotisest "Lahtri teksti mähkimine", mis asub [lahtrites katkestatud andmete fikseerimiseks](https://support.microsoft.com/office/fix-data-that-is-cut-off-in-cells-e996e213-6514-49d8-b82a-2721cef6144e).

> [!NOTE]
> [Teadaoleva](https://support.microsoft.com/topic/you-cannot-use-the-autofit-feature-for-rows-or-columns-that-contain-merged-cells-in-excel-34b54dd7-9bfc-6c8f-5ee3-2715d7db4353) Exceli piirangu tõttu, isegi kui konfigureerite lahtrid teksti vormindama ja konfigureerite neid lahtriid sisaldavad read korrigeerima automaatselt nende kõrgust nii, et need sobiksid tekstiga, **·** **ei** pruugi te ühendatud lahtrite ja neid sisaldavate ridade puhul kasutada automaatset ja vormindatud Exceli funktsioone. 

Dynamics 365 Finantsversiooni 10.0.23 puhul saate loodud dokumendiga töötamisel sundida ER-i arvutama iga rea kõrgust, mis on konfigureeritud automaatselt mahtuma selle kõrgusega pesastatud lahtrite sisule, kui see rida sisaldab vähemalt üht ühendatud lahtrit, mis selles teksti sees vormindati. Arvutatud kõrgust kasutatakse siis rea muutmiseks, kindlustamaks, et kõik rea lahtrid on loodud dokumendis nähtavad.

> [!NOTE]
> Võtke arvesse, et see funktsioon ei pruugi ühendatud lahtri vormindamisel kohandatud fondi kasutamisel õigesti töötada. Kuna Excel ei kaasa kohandatud fonte, ei anna see teavet kohandatud fondi suuruse kohta. Seega saab ühendatud lahtri suurust valesti hinnata.

Selle funktsiooni kasutamiseks, kui käitate mis tahes ER-vormingut, mis on konfigureeritud kasutama Exceli malle väljaminevate dokumentide loomiseks, järgige neid samme.

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Seostatud lingid** paan **Elektroonilise aruandluse parameetrid**.
3. Seadke elektroonilise **aruandluse parameetrite lehe** vahekaardil **Käitusaeg** rea kõrguse **automaatseks** muutmiseks suvand **Jah**.

Kui soovite seda reeglit üksiku ER-vormingu jaoks muuta, värskendage selle vormingu mustandversiooni järgmiste sammude abil.

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Konfiguratsioonid** suvand **Aruandluse konfiguratsioonid**.
3. **Valige konfiguratsioonilehe** vasakpoolse paani konfiguratsioonipuus ER-i konfiguratsioon, mis on loodud kasutama väljaminevate dokumentide loomiseks Exceli malli.
4. Valige kiirkaardil **Versioonid** konfiguratsiooni versioon, mille olek on **Mustand**.
5. Valige toimingupaanil valik **Koostaja**.
6. Valige vormingukujundaja **lehel** vasakul paanil olevas vormingupuus Exceli komponent, mis on lingitud Exceli malliga.
7. **Valige vahekaardi Vorming** **väljal** Rea kõrguse korrigeerimine väärtus, et määrata, kas käitusajal peaks ER olema sundrea kõrguse muutmiseks väljaminevas dokumendis, mille on loonud redigeeritud ER-vorming:

    - **Vaikimisi** : kasutage üldist sätet, mis on konfigureeritud **automaatse rea kõrguse väljal** elektroonilise **aruandluse parameetrite** lehel.
    - **Jah** – alistage üldsäte ja muutke käitusajal rea kõrgust.
    - **Ei** – alistage üldsäte ega muuda rea kõrgust käitusajal.

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

## <a name="page-component"></a><a name="page-component"></a>Lehekülje komponent

### <a name="overview"></a>Ülevaade

Saate kasutada **Lehekülje** komponenti, kui soovite, et Excel järgiks teie ER-vormingut ja struktuuri lehekülgede saalimist loodud väljaminevas dokumendis. Kui ER-vorming käitab komponente, mis on **Lehekülje** komponendi all, lisatakse nõutavad leheküljepiirid automaatselt. Selle protsessi käigus kaalutakse loodud sisu suurust, Exceli malli lehekülje seadistust ja Exceli mallis valitud paberi suurust.

Kui peate dokumendi tükeldama erinevatesse sektsioonidesse, millest igaühel on erinev lehekülgede saalimine, saate konfigureerida mitu **Lehekülje** komponenti iga [Lehe](er-fillable-excel.md#sheet-component) komponendis.

### <a name="structure"></a><a name="page-component-structure"></a>Struktuur

Kui **Lehekülje** komponendi esimene komponent on [Vahemiku](er-fillable-excel.md#range-component) komponent, kus **Andmeedastuse suuna** atribuut on seatud valikule **Andmeedastust pole**, loetakse see vahemik lehekülgede saalimiseks lehekülje päiseks, mis põhineb praeguse **Lehekülje** komponendi sätetel. Selle vormingu komponendiga seostatud Exceli vahemikku korratakse iga lehe ülaosas, mis luuakse praeguse **Lehekülje** komponendi sätteid kasutades.

> [!NOTE]
> Õige lehekülgede saalimiseks, kui [ülemises vahemikus korduvad read](https://support.microsoft.com/office/repeat-specific-rows-or-columns-on-every-printed-page-0d6dac43-7ee7-4f34-8b08-ffcc8b022409) on konfigureeritud Exceli mallis, peab selle Exceli vahemiku aadress olema võrdne eelnevalt kirjeldatud vahemiku komponendiga seotud Exceli **Vahemiku** aadressiga.

Kui **Lehekülje** komponendi viimane komponent on **Vahemiku** komponent, kus **Andmeedastuse suuna** atribuut on seatud valikule **Andmeedastust pole**, loetakse see vahemik lehekülgede saalimiseks lehekülje jalamiks, mis põhineb praeguse **Lehekülje** komponendi sätetel. Selle vormingu komponendiga seostatud Exceli vahemikku korratakse iga lehe alaosas, mis luuakse praeguse **Lehekülje** komponendi sätteid kasutades.

> [!NOTE]
> Õige lehekülgede saalimiseks ei tohi **Vahemiku** komponentidega seostatud Exceli vahemikke käitusajal muuta. Me ei soovita teil vormindada selle vahemiku lahtrid **Vormindades teksti lahtrina** ja **Automaatse rea kõrguse** Exceli [suvanditega](https://support.microsoft.com/office/wrap-text-in-a-cell-2a18cff5-ccc1-4bce-95e4-f0d4f3ff4e84).

Saate lisada valikuliste **Vahemiku** komponentide vahele mitmeid teisi **Vahemiku** komponente, et määrata, kuidas loodud dokument täidetakse.

Kui **Lehe** komponendi pesastatud **Vahemiku** komponentide kogum ei vasta eelnevalt kirjeldatud struktuurile, ilmneb ER-i vormingukujundaja ajal [kinnitamistõrge](er-components-inspections.md#i17). Veateade teavitab teid, et probleem võib käitusajal põhjustada probleeme.

> [!NOTE]
> Õige väljundi loomiseks ärge määrake **Lehekülje** komponendi all mis tahes **Vahemiku** komponendi sidumist, kui selle **Vahemiku** komponendi **Andmeedastussuuna** atribuut on seatud valikule **Andmeedastus puudub** ja vahemik on konfigureeritud lehe päiste või lehe jaluste loomiseks.

Kui soovite lehekülgedega seotud summeerimist ja loendamist, et arvutada jooksvaid kogusummasid ja kogusummasid lehekülje kohta, on soovitatav konfigureerida nõutavad [Andmete kogum](er-data-collection-data-sources.md) andmeallikad. Selleks, et teada saada, kuidas kasutada **Lehe** komponenti loodud Exceli dokumendi lehekülgede saalimiseks, viige lõpule toimingud [ER-vormingu kujundamisel, et luua loodud dokument Exceli vormingus](er-paginate-excel-reports.md).

### <a name="limitations"></a><a name="page-component-limitations"></a>Kitsendused

Exceli **Lehekülgede** nummerdamiseks lehekülje komponendi kasutamisel ei saa te teada loodud dokumendi lõplikke lehti enne, kui lehekülgede saalimine on lõpule viidud. Seetõttu ei saa ER valemite abil lehtede koguarvu arvutada ja printida loodud dokumendi õige arv leheküljed mis tahes leheküljele enne viimast lehekülge.

> [!TIP]
> Selle tulemuse saavutamiseks Exceli päises või jaluses, kasutades spetsiaalset Exceli [vormingut](/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers) päiste ja jaluste jaoks.

Konfigureeritud **lehe** komponente ei peeta Exceli malli värskendamisel Redigeeritavas vormingus Dynamics 365 Finantside versioonis 10.0.22. Seda funktsiooni kaalutakse finantside täiendavateks väljalaseteks.

Kui konfigureerite Exceli malli [tingimusliku vormingu](/office/dev/add-ins/excel/excel-add-ins-conditional-formatting) kasutamiseks, ei pruugi see mõnel juhul nii hästi töötada.

### <a name="applicability"></a>Kohaldatavus

**Lehe** komponent töötab [Exceli failivormingu](er-fillable-excel.md#excel-file-component) komponendiga ainult siis, kui see komponent on konfigureeritud malli kasutama Excelis. Kui [asendate](tasks/er-design-configuration-word-2016-11.md) Exceli malli Wordi malliga ja käivitate siis redigeeritava ER-vormingu, eiratakse **Lehekülje** komponenti.

Komponent **Leht** töötab ainult siis, kui **EPPlus Teekide kasutamise lubamine elektroonilise aruandluse raamistikus** on lubatud. Käitusajal ilmneb erand, kui ER püüab **Lehe** komponenti töödelda, kui see funktsioon on keelatud.

> [!NOTE]
> Käitusajal ilmneb erand, kui ER-vorming töötleb **Lehe** komponenti Exceli malli jaoks, mis sisaldab vähemalt üht kehtetule lahtrile viivitud valemit. Käitusaja vigade vältimiseks parandage Exceli mall, nagu on kirjeldatud jaotises [Kuidas parandada #REF! viga](https://support.microsoft.com/office/how-to-correct-a-ref-error-822c8e46-e610-4d02-bf29-ec4b8c5ff4be).

## <a name="footer-component"></a>Jaluse komponent

**Jaluse** komponenti kasutatakse jaluste täitmiseks Exceli töövihikus loodud töölehe allservas.

> [!NOTE]
> Saate lisada selle komponendi igale **lehe** komponendile, et määrata erinevad jalused erinevatele töölehtedele genereeritud Exceli töövihikus.

Kui konfigureerite üksiku **jaluse** komponendi, saate kasutada **päise/jaluse** välimuse atribuuti, et täpsustada lehekülgi, mille jaoks komponenti kasutatakse. Saadaval on järgmised väärtused:

- **Mistahes** - käivitage konfigureeritud **jaluse** komponent Exceli ematöölehe mis tahes lehekülje jaoks.
- **Esimene** - käivitage konfigureeritud **jaluse** komponent Exceli ematöölehe esimese lehekülje jaoks.
- **Võrdne** - käivitage konfigureeritud **jaluse** komponent Exceli võrdsete ematöölehtede jaoks.
- **Juhuslik** - käivitage konfigureeritud **jaluse** komponent juhusliku Exceli ematöölehe lehekülje jaoks.

Üksiku **lehe** komponendile saate lisada **jaluse** komponendi, millest igaühel on **päise/jaluse välimuse atribuudi** jaoks erinev väärtus. Sel viisil saate Exceli töölehel luua eri tüüpi lehekülgede jaoks erinevaid jaluseid.

> [!NOTE]
> Veenduge, et **jaluse** komponent, mille te lisate üksikule **lehe** komponendile, oleks erinev väärtus **päise/jaluse välimuse** atribuudi jaoks. Vastasel juhul [ilmneb](er-components-inspections.md#i16) kinnitamistõrge. Tõrketeade, mille saate, teavitab teid vastuolust.

Lisage lisatud **jaluse** komponendi alla, vajalikud pesastatud komponendid **Tekst\\Tekstiring**, **Tekst\\KuupäevKellaaeg** või muu tüüp. Konfigureerige nende komponentide sidumised, et määratleda, kuidas teie lehekülg jalus täidetakse.

Loodud jaluse sisu [õigeks](/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers) vormindamiseks saate kasutada ka erilisi vorminduskoode. Et teada saada, kuidas seda lähenemist kasutada, järgige näites [1](#example-1) toodud samme selles artiklis allpool.

> [!NOTE]
> ER-vormingute konfigureerimisel arvestage kindlasti Exceli [piirangut](https://support.microsoft.com/office/excel-specifications-and-limits-1672b34d-7043-467e-8e27-269d656771c3) ja suurimat ühe päise või jaluse tähemärkide arvu.

## <a name="header-component"></a>Päise komponent

**Päise** komponenti kasutatakse päiste täitmiseks Exceli töövihikus loodud töölehe allservas. Seda kasutatakse **jaluse** komponendina.

## <a name="edit-an-added-er-format"></a>Lisatud ER-vormingu redigeerimine

### <a name="update-a-template"></a>Malli värskendamine

Saate valida Toimingupaani **Excelist värskendamine** vahekaardi **Importimine**, et importida värskendatud mall redigeeritavasse ER-vormingusse. Selle protsessi käigus asendatakse valitud komponent **Excel\\File** uue malliga. Redigeeritava ER-vormingu sisu sünkroonitakse värskendatud ER-i malli sisuga.

- Uus ER-vormingu komponent luuakse automaatselt iga Exceli nime kohta, kui redigeeritavast vormist ei leida ER-vormingu komponenti.
- Redigeeritavast ER-vormingust kustutatakse kõik ER-vormingu komponendid, mille kohta ei ei leita sobivat Exceli nime.

> [!NOTE]
> Seadke suvandi **Exceli vorminguelemendi Leht loomine** väärtuseks **Jah**, kui soovite luua redigeeritavas ER-vormingus valikulise elemendi **Leht**.
>
> Kui redigeeritav ER-vorming sisaldas algselt elemente **Leht**, soovitame teil värskendatud malli importimisel määdata suvandi **Exceli vorminguelemendi Leht loomine** väärtuseks **Jah**. Vastasel juhul luuakse kõik algse elemendi **Leht** pesastatud elemendid nullist. Seetõttu lähevad kõik uuesti loodud vorminguelementide sidumised värskendatud ER-vormingus kaotsi.

![Exceli vorminguelemendi Leht suvandi loomine dialoogiboksis Excelist värskendamine.](./media/er-excel-format-update-template.png)

Versioonis 10.0.28 ja uuemas saate **kasutada Suvandit Värskenda Exceli päist ja Exceli vormingu elemente**.

- Kui seadistate valikuks **Ei**, jäävad Exceli päise ja Exceli jaluse vormingu elemendid muutmata, isegi kui vastavad päised või jalused on uuendatud imporditud malli töölehtedel Exceli töövihiku vormingus.
- Kui seadistate selle valiku väärtuseks **Jah**, muutuvad Exceli päise ja Exceli jaluse vormingu elemendid vastavate päiste või jaluste uuendamisel imporditud malli töölehtedel Exceli töövihiku vormingus.

    - Kui töölehe päise või jaluse struktuuri pole muudetud või kui see on ainult lisatud, uuendatakse vastava Exceli päise või Exceli jaluse vormingu elemendi struktuuri. Selle Exceli päise või Exceli jaluse vorminguelemendi alla pesastatud vorminguelementide sidumised säilitatakse.
    - Kui töölehe päise või jaluse struktuuri on muudetud, luuakse uuesti vastav Exceli päis või Exceli jaluse vormingu element. Selle Exceli päise või Exceli jaluse vorminguelemendi alla pesastatud vorminguelementide sidumised eemaldatakse.

![Exceli päise ja Exceli jaluse vormingu elementide suvandi värskendamine dialoogiboksis Uuenda Excelist.](./media/er-excel-format-update-template2.png)

Selle funktsiooni kohta lisateabe saamiseks järgige teemas [Elekrtoonilise aruandluse muutmine Exceli mallide uuesti rakendamise teel](modify-electronic-reporting-format-reapply-excel-template.md) toodud etappe.

## <a name="validate-an-er-format"></a>ER-vormingu kinnitamine

Kui kinnitate redigeeritavat ER-vormingut, tehakse järjepidevuse kontroll, et veenduda, kas Exceli nimi on praegu kasutatavas Exceli mallis olemas. Teid teavitatakse kõigist vastuoludest. Osade vastuolude korral pakutakse probleemi automaatse lahendamise valikut.

![Tõrketeadete kinnitamine.](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a>Exceli valemite arvutamise juhtimine

Kui luuakse väljaminev töövihikuvormingus Microsoft Exceli dokument, võivad mõned selle dokumendi lahtrid sisaldada Exceli valemeid. Kui funktsioon **Luba EPPlusi teegi kasutamine elektroonilise aruandluse raamistikus** on lubatud, saate kontrollida, millal valemid arvutatakse, muutes kasutatavas Exceli mallis **arvutamise valikute** [parameetrit](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows).

- Valige suvand **Automaatne**, et arvutada kõik sõltuvad valemid iga kord uuesti, kui loodud dokumendile lisatakse uued vahemikud, lahtrid jne.

    > [!NOTE]
    > See võib põhjustada mitut seotud valemit sisaldavate Exceli mallide korral jõudlusprobleemi.

- Valige **Käsitsi**, et vältida dokumendi loomisel valemi uuesti arvutamist.

    > [!NOTE]
    > Valemi uuesti arvutamine tehakse käsitsi, kui loodud dokument avatakse Excelit kasutades eelvaateks.
    > Ärge kasutage seda valikut, kui konfigureerite ER-i sihtkohta, mis eeldab loodud dokumendi kasutamist ilma selle eelvaateta Excelis (PDF-i teisendamine, meilimine jne)., kuna loodud dokument ei pruugi omada valemeid sisaldavates lahtrites väärtusi.

## <a name="example-1-format-footer-content"></a><a name="example-1"></a>Näide 1: jaluse sisu vormindamine

1. Kasutage antud ER-i konfiguratsioone [loomiseks](er-generate-printable-fti-forms.md) prinditava vabas vormis arve (FTI) dokumenti.
2. Vaadake üle loodud dokumendi jalus. Pange tähele, et see sisaldab teavet praeguse leheküljenumbri ja dokumendi lehtede koguarvu kohta.

    ![Vaadake üle loodud dokumendi jalus Exceli vormingus.](./media/er-fillable-excel-footer-1.gif)

3. ER-vormingu kujunduses [avage](er-generate-printable-fti-forms.md#features-that-are-implemented-in-the-sample-er-format) läbivaatamiseks ER-näidisvorming.

    **Arve** jaluses luuakse kahe töölehe sätete põhjal **stringi** komponendi all oleva **jaluse** komponent:

    - Esimene **Stringi** komponent täidab järgmised vormindamise erikoodid, et Excel rakendaks kindlat vormingut:

        - **&C** – joondage jaluse tekst keskele.
        - **&"Segoe UI,Regulaarne"&8** – esitage jaluse tekst "Segoe UI Regular" fondis 8 punkti suuruses.

    - Teine **Stringi** komponent sisestab teksti, mis sisaldab praegust leheküljenumbrit ja praeguse dokumendi lehtede koguarvu.

    ![ER-i vormingu komponendi kinnitamine vormingu kujundaja lehel.](./media/er-fillable-excel-footer-2.png)

4. Praeguse lehe jaluse muutmiseks saate kohandada ER-näidisvormingut:

    1. [Looge](er-quick-start2-customize-report.md#DeriveProvidedFormat) tuletatud **vabas vormis arve (Excel) kohandatud** ER-vorming, mis põhineb ER-näidisvormingul.
    2. Lisage arve töölehe jaluse **Rida** komponendile **jalus** komponent **arve** töölehel:

        1. Lisage **Stringi** komponent, mis joondab ettevõtte nime vasakul ja esitab selle 8-punkti fondis "Segoe UI Regular" font (**"&L&"Segoe UI,Regular"&8"**).
        2. Lisage **Stringi** komponent, mis täidab ettevõtte nime (**model.InvoiceBase.CompanyInfo.Name**).

    3. Lisage teine uus paar **Rida** komponendile **jalus** komponent **arve** töölehel:

        1. Lisage **Stringi** komponent, mis joondab ettevõtte nime vasakul ja esitab selle 8-punkti fondis "Segoe UI Regular" font (**"&L&"Segoe UI,Regular"&8"**).
        2. Lisage **Stringi** komponent, mis täidab töötlemiskuupäeva kohandatud vormingus (**&nbsp;&DATEFORMAT(SESSIONTODAY(), "aaaa-KK-pp")**).

        ![ER-i vormingu komponendi vaatamine vormingu kujundaja lehel.](./media/er-fillable-excel-footer-3.png)

    4. [Viige](er-quick-start2-customize-report.md#CompleteDerivedFormat) lõpule tuletatud **vabas vormis arve (Exceli) kohandatud** ER-vormingu mustandversioon.

5. [Konfigureerige](er-generate-printable-fti-forms.md#configure-print-management) prindihaldus kasutama tuletatud **vabas vormis arve (Excel) kohandatud** ER-vormingut ER-näidisvormingu asemel.
6. Looge prinditav FTI-dokument ja vaadake üle loodud dokumendi jalus.

    ![Vaadake üle Exceli vormingus loodud dokumendi jalus.](./media/er-fillable-excel-footer-4.gif)

## <a name="example-2-fixing-the-merged-cells-epplus-issue"></a><a name="example-2"></a> Näide 2: ühendatud lahtrite EP Väljamineku parandamine

Väljamineva dokumendi loomiseks Exceli töövihiku vormingus saate käitada ER-vormingut. **Kui funktsioonihalduse tööruumis on lubatud EPRaamatuteegi EPRaamatu** **kasutamine** elektroonilise aruandluse raamistikus, [kasutatakse EP Andmebaasiteeki](https://www.nuget.org/packages/epplus/4.5.2.1) Exceli väljundi loomiseks. Teadaoleva Exceli käitumise ja [EP](https://answers.microsoft.com/en-us/msoffice/forum/all/deleting-a-range-of-cells-that-includes-merged/8601462c-4e2c-48e0-bd23-848eecb872a9)-teegi piirangu tõttu võib siiski tekkida järgmine erand: "Ühendatud elemente ei saa kustutada/üle kirjutada. Vahemik on osaliselt ühendatud teise ühendatud vahemikuga." Et teada saada, millised Exceli mallid võivad seda erandt põhjustada ja kuidas saate probleemi lahendada, viige järgmine näide lõpule.

1. Looge Exceli töölauarakenduses uus Exceli töövihik.
2. Lisage töölehele **Sheet1** lahtri **A2 ReportTitle** **nimi**.
3. Ühenda lahtrid **A1** ja **A2**.

    ![Vaadake üle ühendamisrakkude A1 ja A2 tulemused Exceli töölauarakenduses loodud Exceli töövihikus.](./media/er-fillable-excel-example2-1.png)

3. Lisage konfiguratsioonide **lehele** uus [ER-vorming,](er-fillable-excel.md#add-a-new-er-format) et luua väljaminev dokument Exceli töövihiku vormingus.
4. Vormingukujundaja **lehel** importige [loodud](er-fillable-excel.md#template-import) Exceli töövihik lisatud ER-vormingusse väljaminevate dokumentide mallina.
5. **Vahekaardil Vastendamine** konfigureerige sidumine **lahtritüübi Aruandetüübi** Aruandetüübi [komponendile](er-fillable-excel.md#cell-component).
6. Käivitage konfigureeritud ER-vorming. Pange tähele, et ilmnes järgmine erand: "Ühendatud lahtrid ei saa kustutada/üle kirjutada. Vahemik on osaliselt ühendatud teise ühendatud vahemikuga."

    ![Konfigureeritud ER-vormingu käivitamistulemuste ülevaatamine vormingukujundaja lehel.](./media/er-fillable-excel-example2-2.png)

Probleemi saate lahendada järgmistel viisidel:

- **Lihtsam, kuid mitte soovitatav:** lülitage **funktsioonihalduse** tööruumis **välja EPTööteegi kasutus lubamine elektroonilise aruandluse raamistiku funktsioonis**. Kuigi see lähenemine on lihtsam, võivad teil selle kasutamisel tekkida muud probleemid, sest mõningaid ER-funktsioone **toetatakse ainult siis, kui EPKogu** teegi kasutamise lubamine elektroonilise aruandluse raamistiku funktsioonis on lubatud.
- **Soovitatav:** järgige neid samme.

    1. Muutke Exceli töölauarakenduses Exceli töövihikut ühel järgmistest viisidest.

        - Eemaldage **töölehel Sheet1** lahtrid **A1 ja** **A2**.
        - Muutke atribuudi **ReportTitle nime viide väärtuselt** **=Sheet1!$A$2** **=Sheet1!$A$1**.

        ![Viite muutmise tulemuste ülevaatamine Exceli töölauarakenduses kujundatud Exceli töövihikus.](./media/er-fillable-excel-example2-3.png)

    2. Importige **vormingu** kujundaja [lehel](er-fillable-excel.md#template-import) muudetud Exceli töövihik olemasoleva malli värskendamiseks redigeeritavasse ER-vormingusse.
    3. Saate käivitada muudetud ER-vormingu.

        ![Genereeritud dokumendi ülevaatamine Exceli töölaua rakenduses.](./media/er-fillable-excel-example2-4.png)

## <a name="limitations"></a>Kitsendused

### <a name="known-epplus-library-limitations"></a>Teadaolevad EP Saateteegi piirangud

#### <a name="external-data-sources"></a>Välisandmete allikad

Kui üks teie mallidest sisaldab PivotTable’i, PowerPivot mis põhineb välisele andmeallikale viitaval mudelil ja EPTekstiteegi [kasutamise lubamine elektroonilise aruandluse raamistiku funktsioonis](https://support.microsoft.com/office/create-a-pivottable-with-an-external-data-source-db50d01d-2e1c-43bd-bfb5-b76a818a927b)**on** lubatud, saate järgmise tõrketeate, kui käitate ER-vormingut, mis kasutab seda malli väljamineva dokumendi loomiseks Exceli vormingus: "Vahemäluallikas pole tööleht." Probleemi lahendamiseks on teil järgmised võimalused:

- **Soovitatav:** kujundage ümber exceli lahendus, mida kasutate:

    1. Eraldage osa, mis sisaldab pivoteid eraldi Exceli töövihikus (töövihik A). 
    2. Kasutage ER-i, et luua finantsidest teine Exceli töövihik (töövihik B), kus on nõutavad üksikasjad. 
    3. Viide töövihikule B töövihikus A kohe, kui töövihik B on loodud.

- Saate funktsiooni välja lülitada, **lubades ELEKTROONILISE aruandluse raamistikus EP Peale** EP Peale EP Peale teegi EP Peale teegi kasutamise. 

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)

[OPENXML-vormingus aruannete loomiseks konfiguratsiooni koostamine](tasks\er-design-reports-openxml-2016-11.md)

[Elektroonilise aruandluse vormingute muutmine Exceli malle uuesti rakendades](modify-electronic-reporting-format-reapply-excel-template.md)

[Horisontaalselt laiendatavate vahemike kasutamine veergude dünaamiliseks lisamiseks Exceli aruannetes](tasks/er-horizontal-1.md)

[Manustatud pildid ja kujutised ER-iga loodud dokumentides](electronic-reporting-embed-images-shapes.md)

[Elektroonilise aruandluse (ER) konfigureerimine andmete tõmbamiseks Power BI-sse](general-electronic-reporting-report-configuration-get-data-powerbi.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
