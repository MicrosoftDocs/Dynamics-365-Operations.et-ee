---
title: Maksuintegratsiooni andmeväljade lisamine laiendite abil
description: See teema kirjeldab X++ laiendite kasutamist maksuintegratsioonile andmeväljade lisamiseks.
author: qire
ms.date: 04/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 64c68ef6804297f86b5d9dc1933b0c16a0d42aae
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695384"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a>Maksuintegratsiooni andmeväljade lisamine laiendite abil

[!include [banner](../includes/banner.md)]


See teema kirjeldab X++ laiendite kasutamist maksuintegratsioonile andmeväljade lisamiseks. Neid välju saab laiendada maksuteenuse maksuandmete mudelile ja kasutada maksukoodide määramiseks. Lisateavet vt teemast [Maksukonfiguratsioonides andmeväljade lisamine](tax-service-add-data-fields-tax-configurations.md).

## <a name="data-model"></a>Andmemudel

Andmemudeli andmeid teostatakse objektides ja neid rakendatakse klassides.

Suurimad objektid on järgmised.

* AxClass/TaxIntegration **Document** Object
* AxClass/TaxIntegration **Line** Object
* AxClass/TaxIntegration **TaxLine** Object

Järgmine illustratsioon näitab, kuidas need objektid on seotud.

[![Andmemudeli objekti seos.](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)

**Dokumendi** objekt võib sisaldada palju **reaobjekte**. Iga objekt sisaldab maksuteenuse metaandmeid.

- Objektil `TaxIntegrationDocumentObject` on metaandmed `originAddress`, mis sisaldavad teavet lähteaadressi kohta, ja metaandmeid `includingTax`, mis näitavad, kas rea summa sisaldab käibemaksu.
- Objektil `TaxIntegrationLineObject` on metaandmed `itemId`, `quantity` ja `categoryId`.

> [!NOTE]
> Objekt `TaxIntegrationLineObject` juurutab ka **Tasu** objekte.

## <a name="integration-flow"></a>Integratsiooni voog

Vooandmeid manipuleeritakse tegevustega.

### <a name="key-activities"></a>Võtmetegevused

* AxClass/TaxIntegration **Calculation** ActivityOnDocument
* AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument
* AxClass/TaxIntegration **DataPersistence** ActivityOnDocument
* AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument
* AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument

Tegevused käivitatakse järgmises järjestuses.

1. Sätte toomine
2. Andmete toomine
3. Arvutusteenus
4. Valuutavahetus
5. Andmete püsivus

Näiteks laiendage valikut **Andmete toomine** enne **Arvutusteenust**.

#### <a name="data-retrieval-activities"></a>Andmete toomise tegevused

**Andmete toomise** tegevused toovad andmeid andmebaasist. Erinevate kannete adapterid on saadaval andmete toomiseks erinevatest kandetabelitest:

- AxClass/TaxIntegration **PurchTable** DataRetrieval
- AxClass/TaxIntegration **PurchParmTable** DataRetrieval
- AxClass/TaxIntegration **PurchREQTable** DataRetrieval
- AxClass/TaxIntegration **PurchRFQTable** DataRetrieval
- AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval
- AxClass/TaxIntegration **SalesTable** DataRetrieval
- AxClass/TaxIntegration **SalesParm** DataRetrieval

Nendes **Andmete toomise** tegevustes kopeeritakse andmed andmebaasist üksustesse `TaxIntegrationDocumentObject` ja `TaxIntegrationLineObject`. Kuna kõik need tegevused laiendavad abstraktset sama malliklassi, on neil tavalised meetodid.

#### <a name="calculation-service-activities"></a>Arvutusteenuse jälgimine

**Arvutusteenuse** tegevus on link maksuteenuse ja maksuintegratsiooni vahel. See tegevus vastutab järgmiste funktsioonide eest.

1. Taotluse koostamine.
2. Sisestage taotlus maksuteenusesse.
3. Saate vastuse maksuteenuselt.
4. Sõeluge vastus.

Andmeväli, mille lisate taotlusele, sisestatakse koos teiste metaandmetega. 

## <a name="extension-implementation"></a>Laiendi rakendamine

Selles jaotises esitatakse üksikasjalikud sammud, mis selgitavad, kuidas laiendust rakendada. See kasutab näidetena **Kulukeskus** ja **Projekti** finantsdimensioone.

### <a name="step-1-add-the-data-variable-in-the-object-class"></a>Toiming 1. Lisa andmemuutuja objektiklassi

Objektiklass sisaldab andmemuutujat ja andmete tooja/määraja meetodeid. Lisage andmeväli kas objektile `TaxIntegrationDocumentObject` või `TaxIntegrationLineObject` olenevalt välja tasemest. Järgmises näites kasutatakse reataset ja faili nimi on `TaxIntegrationLineObject_Extension.xpp`.

> [!NOTE]
> Kui lisatv andmeväli on dokumendi tasemel, muutke failinimi nimeks `TaxIntegrationDocumentObject_Extension.xpp`.

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

**Kulukeskus** ja **Projekt** lisatakse privaatsete muutujatena. Looge nende andmeväljade jaoks tooja- ja määrajameetodid, et andmeid manipuleerida.

### <a name="step-2-retrieve-data-from-the-database"></a>Toiming 2. Tooge andmed andmebaasist

Määrake kanne ja laiendage andmete toomiseks sobivad adapteriklassid. Näiteks kui kasutate kannet **Ostutellimus**, peate laiendama objekte `TaxIntegrationPurchTableDataRetrieval` ja `TaxIntegrationVendInvoiceInfoTableDataRetrieval`. 

> [!NOTE]
> Objekt `TaxIntegrationPurchParmTableDataRetrieval` on pärit asukohast `TaxIntegrationPurchTableDataRetrieval`. Seda ei tohi muuta, välja arvatud juhul, kui tabelite `purchTable` ja `purchParmTable` loogika on erinev.

Kui andmeväli tuleb lisada kõigile kannetele, laiendage kõiki `DataRetrieval`i klasse.

Kuna kõik **Andmete toomise** tegevused laiendavad sama malliklassi, on klassistruktuurid, muutujad ja meetodid sarnased.

```X++
protected TaxIntegrationDocumentObject document;

/// <summary>
/// Copies to the document.
/// </summary>
protected abstract void copyToDocument()
{
    // It is recommended to implement as:
    //
    // this.copyToDocumentByDefault();
    // this.copyToDocumentFromHeaderTable();
    // this.copyAddressToDocument();
}
 
/// <summary>
/// Copies to the current line of the document.
/// </summary>
/// <param name = "_line">The current line of the document.</param>
protected abstract void copyToLine(TaxIntegrationLineObject _line)
{
    // It is recommended to implement as:
    //
    // this.copyToLineByDefault(_line);
    // this.copyToLineFromLineTable(_line);
    // this.copyQuantityAndTransactionAmountToLine(_line);
    // this.copyAddressToLine(_line);
    // this.copyToLineFromHeaderTable(_line);
}
```

Järgmine näide näitab tabeli `PurchTable` kasutamise põhistruktuuri.

```X++
public class TaxIntegrationPurchTableDataRetrieval extends TaxIntegrationAbstractDataRetrievalTemplate
{
    protected PurchTable purchTable;
    protected PurchLine purchLine;

    // Query builder methods
    [Replaceable]
    protected SysDaQueryObject getDocumentQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineQueryObject()
    [Replaceable]
    protected SysDaQueryObject getDocumentChargeQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineChargeQueryObject()

    // Data retrieval methods
    protected void copyToDocument()
    protected void copyToDocumentFromHeaderTable()
    protected void copyToLine(TaxIntegrationLineObject _line)
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    ...
}
```

Kui meetod `CopyToDocument` on kutsutud, siis on puhver `this.purchTable` juba olemas. Selle meetodi eesmärk on kopeerida kõik nõutud andmed tabelist `this.purchTable` objekti `document`, kasutades määraja meetodid, mis loodi klassis `DocumentObject`.

Samuti on puhver `this.purchLine` juba olemas meetodis `CopyToLine`. Selle meetodi eesmärk on kopeerida kõik nõutud andmed tabelist `this.purchLine` objekti `_line`, kasutades määraja meetodid, mis loodi klassis `LineObject`.

Kõige selgem lähenemine on laiendada meetodeid `CopyToDocument` ja `CopyToLine`. Soovitame siiski esmalt proovida meetodeid `copyToDocumentFromHeaderTable` ja `copyToLineFromLineTable`. Kui nad ei tööta nagu vaja, rakendage oma meetodit ja kutsuge see objektidele `CopyToDocument` ja `CopyToLine`. On kolm tavalist olukorda, kus võite kasutada seda lähenemist.

- Kohustuslik väli on objektil `PurchTable` või `PurchLine`. Selles olukorras saate laiendada objekte `copyToDocumentFromHeaderTable` ja `copyToLineFromLineTable`. Siin on näidiskood.

    ```X++
    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        next copyToLineFromLineTable(_line);
        // if we already added XXX in TaxIntegrationLineObject
        _line.setXXX(this.purchLine.XXX);
    }
    ```

- Nõutud andmed pole kande vaiketabelis. Siiski on mõned seosed vaiketabeliga ja väli on enamasti vajalik. Sellises olukorras asendage objektid `getDocumentQueryObject` või `getLineObject`, et teha tabelipäringuid liitseostega. Järgmises näites on väli **Tarni kohe** integreeritud müügitellimusega rea tasemel.

    ```X++
    public class TaxIntegrationSalesTableDataRetrieval
    {
        protected MCRSalesLineDropShipment mcrSalesLineDropShipment;

        /// <summary>
        /// Gets the query for the lines of the document.
        /// </summary>
        /// <returns>The query for the lines of the document</returns>
        [Replaceable]
        protected SysDaQueryObject getLineQueryObject()
        {
            return SysDaQueryObjectBuilder::from(this.salesLine)
                .where(this.salesLine, fieldStr(SalesLine, SalesId)).isEqualToLiteral(this.salesTable.SalesId)
                .outerJoin(this.mcrSalesLineDropShipment)
                .where(this.mcrSalesLineDropShipment, fieldStr(MCRSalesLineDropShipment, SalesLine)).isEqualTo(this.salesLine, fieldStr(SalesLine, RecId))
                .toSysDaQueryObject();
        }
    }
    ```

    Selles näites on puhver `mcrSalesLineDropShipment` deklareeritud ja päring on määratletud objektis `getLineQueryObject`. Päring kasutab suhet `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`. Selles olukorras laiendamisel saate asendada objekti `getLineQueryObject` enda loodud päringuobjektiga. Kuid arvestage järgmist.

    * Kuna meetodi `getLineQueryObject` tagastusväärtus on `SysDaQueryObject`, peate selle objekti SysDa-lähenemist kasutades konstrueerima.
    * Olemasolnud tabelit ei saa eemaldada.

- Nõutud andmed on kandetabeliga seotud keeruka liitseosega või pole seos üks ühele (1:1) vaid üks mitmele (1:N). Sellises olukorras muutuvad asjad veidi keerukamaks. See olukord kehtib näiteks finantsdimensioonide puhul. 

    Sellises olukorras saate rakendada andmete toomiseks oma meetodit. Siin on faili `TaxIntegrationPurchTableDataRetrieval_Extension.xpp` näidiskood.

    ```X++
    [ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
    final class TaxIntegrationPurchTableDataRetrieval_Extension
    {
        private const str CostCenterKey = 'CostCenter';
        private const str ProjectKey = 'Project';

        /// <summary>
        /// Copies to the current line of the document from.
        /// </summary>
        /// <param name = "_line">The current line of the document.</param>
        protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
        {
            Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
            if (dimensionAttributeMap.exists(CostCenterKey))
            {
                _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
            }
            if (dimensionAttributeMap.exists(ProjectKey))
            {
                _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
            }
            next copyToLineFromLineTable(_line);
        }
        private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
        {
            DimensionAttribute dimensionAttribute;
            DimensionAttributeValue dimensionAttributeValue;
            DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
            Map ret = new Map(Types::String, Types::String);

            select Name, RecId from dimensionAttribute
                join dimensionAttributeValue
                    where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
                join DimensionAttributeValueSetItem
                    where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                        && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;

            while(dimensionAttribute.RecId)
            {
                ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
                next dimensionAttribute;
            }
            return ret;
        }
    }
    ```

### <a name="step-3-add-data-to-the-request"></a>Toiming 3. Taotlusele andmete lisamine

Laiendage meetodit `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` või `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` taotlusele andmete lisamiseks. Siin on faili `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` näidiskood.

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define the field name in the request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';
    // private const str IOEnumExample = 'Enum Example';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());

        // If the field to be extended is an enum type, use enum2Symbol to convert an enum variable exampleEnum of ExampleEnumType to a string
        // _destination.SetField(IOEnumExample, enum2Symbol(enumNum(ExampleEnumType), _source.getExampleEnum()));
    }
}
```

Selles koodis `_destination` on ümbrisobjekt, mida kasutatakse taotluse loomiseks ja `_source` milleks on `TaxIntegrationLineObject` objekt.

> [!NOTE]
> Määratlege välja nimi, mida kasutatakse taotluses privaatse **konstnatuurina**. String peab olema täpselt sama mis maksukonfiguratsioonides andmeväljade lisamise teemas lisatud sõlme nimi ([mitte silt)](tax-service-add-data-fields-tax-configurations.md).
> 
> Seadke väli meetodis copyToTaxableDocumentLineWraümbrisFromTaxIntegrationLineObjectByLine **meetodiga** SetField **.** Teise parameetri andmetüüp peaks olema **string**. Kui andmetüüp ei ole **string**, teisendage see stringiks.
> Kui andmetüüp on X++ **enum** tüüp, **soovitame kasutada meetodit enum2Symbol**, et teisendada andmetüübiks string. Maksukonfiguratsioonis lisatav enum väärtus peab olema täpselt sama mis enum nimel. Järgnev on loetelu väärtuse, sildi ja nime erinevuste loend.
> 
>   - Enum nimi on koodis sümboelne nimi. **enum2Symbol()** võib teisendada enum väärtus selle nimeks.
>   - Enum väärtus on täisarv.
>   - Andmesildid võivad eri keeltes olla erinevad. **enum2Str()** saab teisendada enum enum väärtuse sildiks.

## <a name="model-dependency"></a>Mudeli sõltuvus

Projekti edukaks loomiseks lisage mudeli sõltuvuste jaoks järgmised viitemudelid:

- Vormi ApplicationPlatform
- Application Kuupäev
- Maksumootor
- Dimensioonid, kui kasutatakse finantsdimensiooni
- Teised koodis viidatud vajalikud mudelid

## <a name="validation"></a>Kinnitus

Pärast eelmiste sammude lõpule viimist saate oma muudatused kinnitada.

1. Finantsis minge ostureskontrosse **ja** lisage **URL-ile &debug=vsCconfirmExit%2&**. Näiteks. `https://usnconeboxax1aos.cloud.onebox.dynamics.com/?cmp=DEMF&mi=PurchTableListPage&debug=vs%2CconfirmExit&` Lõpp on **&** oluline.
2. Avage ostutellimuse **leht** ja valige **ostutellimuse** loomiseks uus.
3. Seadke kohandatud väljale väärtus ja seejärel valige **käibemaks**. Eesliitega tõrkeotsingu fail **TaxServiceTroubleshootingLog** laaditakse automaatselt alla. See fail sisaldab maksuarvutuse teenusesse sisestatud kandeteavet. 
4. Kontrollige, kas kohandatud väli on maksuteenuse arvutuse **sisendis JSON-i** jaotises olemas ja kas selle väärtus on õige. Kui väärtus ei ole õige, topeltkontrollige selle dokumendi samme.

Faili näide:

```
===Tax service calculation input JSON:===
{
  "TaxableDocument": {
    "Header": [
      {
        "Lines": [
          {
            "Line Type": "Normal",
            "Item Code": "",
            "Item Type": "Item",
            "Quantity": 0.0,
            "Amount": 1000.0,
            "Currency": "EUR",
            "Transaction Date": "2022-1-26T00:00:00",
            ...
            /// The new fields added at line level
            "Cost Center": "003",
            "Project": "Proj-123"
          }
        ],
        "Amount include tax": true,
        "Business Process": "Journal",
        "Currency": "",
        "Vendor Account": "DE-001",
        "Vendor Invoice Account": "DE-001",
        ...
        // The new fields added at header level, no new fields in this example
        ...
      }
    ]
  },
}
...
```

## <a name="appendix"></a>Lisa

Selles lisas kuvatakse täielik näidiskood finantsdimensioonide, **kulukeskuse ja projekti** **integreerimiseks** rea tasemel.

### <a name="taxintegrationlineobject_extensionxpp"></a>TaxIntegrationLineObject_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a>TaxIntegrationPurchTableDataRetrieval_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
final class TaxIntegrationPurchTableDataRetrieval_Extension
{
    private const str CostCenterKey = 'CostCenter';
    private const str ProjectKey = 'Project';

    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
        if (dimensionAttributeMap.exists(CostCenterKey))
        {
            _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
        }
        if (dimensionAttributeMap.exists(ProjectKey))
        {
            _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
        }
        next copyToLineFromLineTable(_line);
    }
    private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
    {
        DimensionAttribute dimensionAttribute;
        DimensionAttributeValue dimensionAttributeValue;
        DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
        Map ret = new Map(Types::String, Types::String);
        select Name, RecId from dimensionAttribute
            join dimensionAttributeValue
                where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
            join DimensionAttributeValueSetItem
                where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                    && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;
        while(dimensionAttribute.RecId)
        {
            ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
            next dimensionAttribute;
        }
        return ret;
    }
}
```

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a>TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define the field name in the request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```
