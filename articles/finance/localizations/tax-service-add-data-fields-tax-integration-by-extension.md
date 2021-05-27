---
title: Maksuintegratsiooni andmeväljade lisamine laiendite abil
description: See teema kirjeldab X++ laiendite kasutamist maksuintegratsioonile andmeväljade lisamiseks.
author: qire
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a3da8e1b8176eb25fe4e0a320aa3e907c06e09c5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021388"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a><span data-ttu-id="fe960-103">Maksuintegratsiooni andmeväljade lisamine laiendite abil</span><span class="sxs-lookup"><span data-stu-id="fe960-103">Add data fields in the tax integration by using extension</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="fe960-104">See teema kirjeldab X++ laiendite kasutamist maksuintegratsioonile andmeväljade lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="fe960-104">This topic explains how to use X++ extensions to add data fields in the tax integration.</span></span> <span data-ttu-id="fe960-105">Neid välju saab laiendada maksuteenuse maksuandmete mudelile ja kasutada maksukoodide määramiseks.</span><span class="sxs-lookup"><span data-stu-id="fe960-105">These fields can be extended to the tax data model of the tax service and used to determine tax codes.</span></span> <span data-ttu-id="fe960-106">Lisateavet vt teemast [Maksukonfiguratsioonides andmeväljade lisamine](tax-service-add-data-fields-tax-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="fe960-106">For more information, see [Add data fields in tax configurations](tax-service-add-data-fields-tax-configurations.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="fe960-107">Andmemudel</span><span class="sxs-lookup"><span data-stu-id="fe960-107">Data model</span></span>

<span data-ttu-id="fe960-108">Andmemudeli andmeid teostatakse objektides ja neid rakendatakse klassides.</span><span class="sxs-lookup"><span data-stu-id="fe960-108">The data in the data model is carried by objects and implemented by classes.</span></span>

<span data-ttu-id="fe960-109">Suurimad objektid on järgmised.</span><span class="sxs-lookup"><span data-stu-id="fe960-109">Here is a list of the major objects:</span></span>

* <span data-ttu-id="fe960-110">AxClass/TaxIntegration **Document** Object</span><span class="sxs-lookup"><span data-stu-id="fe960-110">AxClass/TaxIntegration **Document** Object</span></span>
* <span data-ttu-id="fe960-111">AxClass/TaxIntegration **Line** Object</span><span class="sxs-lookup"><span data-stu-id="fe960-111">AxClass/TaxIntegration **Line** Object</span></span>
* <span data-ttu-id="fe960-112">AxClass/TaxIntegration **TaxLine** Object</span><span class="sxs-lookup"><span data-stu-id="fe960-112">AxClass/TaxIntegration **TaxLine** Object</span></span>

<span data-ttu-id="fe960-113">Järgmine illustratsioon näitab, kuidas need objektid on seotud.</span><span class="sxs-lookup"><span data-stu-id="fe960-113">The following illustration shows how these objects are related.</span></span>

<span data-ttu-id="fe960-114">[![Andmemudeli objekti seos](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span><span class="sxs-lookup"><span data-stu-id="fe960-114">[![Data model object relationship](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span></span>

<span data-ttu-id="fe960-115">**Dokumendi** objekt võib sisaldada palju **reaobjekte**.</span><span class="sxs-lookup"><span data-stu-id="fe960-115">A **Document** object can contain many **Line** objects.</span></span> <span data-ttu-id="fe960-116">Iga objekt sisaldab maksuteenuse metaandmeid.</span><span class="sxs-lookup"><span data-stu-id="fe960-116">Each object contains metadata for the tax service.</span></span>

- <span data-ttu-id="fe960-117">Objektil `TaxIntegrationDocumentObject` on metaandmed `originAddress`, mis sisaldavad teavet lähteaadressi kohta, ja metaandmeid `includingTax`, mis näitavad, kas rea summa sisaldab käibemaksu.</span><span class="sxs-lookup"><span data-stu-id="fe960-117">`TaxIntegrationDocumentObject` has `originAddress` metadata, which contains information about the source address, and `includingTax` metadata, which indicates whether the line amount includes sales tax.</span></span>
- <span data-ttu-id="fe960-118">Objektil `TaxIntegrationLineObject` on metaandmed `itemId`, `quantity` ja `categoryId`.</span><span class="sxs-lookup"><span data-stu-id="fe960-118">`TaxIntegrationLineObject` has `itemId`, `quantity`, and `categoryId` metadata.</span></span>

> [!NOTE]
> <span data-ttu-id="fe960-119">Objekt `TaxIntegrationLineObject` juurutab ka **Tasu** objekte.</span><span class="sxs-lookup"><span data-stu-id="fe960-119">`TaxIntegrationLineObject` also implements **Charge** objects.</span></span>

## <a name="integration-flow"></a><span data-ttu-id="fe960-120">Integratsiooni voog</span><span class="sxs-lookup"><span data-stu-id="fe960-120">Integration flow</span></span>

<span data-ttu-id="fe960-121">Vooandmeid manipuleeritakse tegevustega.</span><span class="sxs-lookup"><span data-stu-id="fe960-121">The data in the flow is manipulated by activities.</span></span>

### <a name="key-activities"></a><span data-ttu-id="fe960-122">Võtmetegevused</span><span class="sxs-lookup"><span data-stu-id="fe960-122">Key activities</span></span>

* <span data-ttu-id="fe960-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="fe960-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span></span>
* <span data-ttu-id="fe960-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="fe960-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span></span>
* <span data-ttu-id="fe960-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="fe960-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span></span>
* <span data-ttu-id="fe960-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="fe960-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span></span>
* <span data-ttu-id="fe960-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="fe960-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span></span>

<span data-ttu-id="fe960-128">Tegevused käivitatakse järgmises järjestuses.</span><span class="sxs-lookup"><span data-stu-id="fe960-128">Activities are run in the following order:</span></span>

1. <span data-ttu-id="fe960-129">Sätte toomine</span><span class="sxs-lookup"><span data-stu-id="fe960-129">Setting Retrieval</span></span>
2. <span data-ttu-id="fe960-130">Andmete toomine</span><span class="sxs-lookup"><span data-stu-id="fe960-130">Data Retrieval</span></span>
3. <span data-ttu-id="fe960-131">Arvutusteenus</span><span class="sxs-lookup"><span data-stu-id="fe960-131">Calculation Service</span></span>
4. <span data-ttu-id="fe960-132">Valuutavahetus</span><span class="sxs-lookup"><span data-stu-id="fe960-132">Currency Exchange</span></span>
5. <span data-ttu-id="fe960-133">Andmete püsivus</span><span class="sxs-lookup"><span data-stu-id="fe960-133">Data Persistence</span></span>

<span data-ttu-id="fe960-134">Näiteks laiendage valikut **Andmete toomine** enne **Arvutusteenust**.</span><span class="sxs-lookup"><span data-stu-id="fe960-134">For example, extend **Data Retrieval** before **Calculation Service**.</span></span>

#### <a name="data-retrieval-activities"></a><span data-ttu-id="fe960-135">Andmete toomise tegevused</span><span class="sxs-lookup"><span data-stu-id="fe960-135">Data Retrieval activities</span></span>

<span data-ttu-id="fe960-136">**Andmete toomise** tegevused toovad andmeid andmebaasist.</span><span class="sxs-lookup"><span data-stu-id="fe960-136">**Data Retrieval** activities retrieve data from the database.</span></span> <span data-ttu-id="fe960-137">Erinevate kannete adapterid on saadaval andmete toomiseks erinevatest kandetabelitest:</span><span class="sxs-lookup"><span data-stu-id="fe960-137">Adapters for different transactions are available to retrieve data from different transaction tables:</span></span>

- <span data-ttu-id="fe960-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="fe960-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span></span>
- <span data-ttu-id="fe960-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="fe960-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span></span>
- <span data-ttu-id="fe960-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="fe960-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span></span>
- <span data-ttu-id="fe960-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="fe960-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span></span>
- <span data-ttu-id="fe960-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="fe960-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span></span>
- <span data-ttu-id="fe960-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="fe960-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span></span>
- <span data-ttu-id="fe960-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="fe960-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span></span>

<span data-ttu-id="fe960-145">Nendes **Andmete toomise** tegevustes kopeeritakse andmed andmebaasist üksustesse `TaxIntegrationDocumentObject` ja `TaxIntegrationLineObject`.</span><span class="sxs-lookup"><span data-stu-id="fe960-145">In these **Data Retrieval** activities, data is copied from the database to `TaxIntegrationDocumentObject` and `TaxIntegrationLineObject`.</span></span> <span data-ttu-id="fe960-146">Kuna kõik need tegevused laiendavad abstraktset sama malliklassi, on neil tavalised meetodid.</span><span class="sxs-lookup"><span data-stu-id="fe960-146">Because all these activities extend the same abstract template class, they have common methods.</span></span>

#### <a name="calculation-service-activities"></a><span data-ttu-id="fe960-147">Arvutusteenuse jälgimine</span><span class="sxs-lookup"><span data-stu-id="fe960-147">Calculation Service activities</span></span>

<span data-ttu-id="fe960-148">**Arvutusteenuse** tegevus on link maksuteenuse ja maksuintegratsiooni vahel.</span><span class="sxs-lookup"><span data-stu-id="fe960-148">The **Calculation Service** activity is the link between the tax service and the tax integration.</span></span> <span data-ttu-id="fe960-149">See tegevus vastutab järgmiste funktsioonide eest.</span><span class="sxs-lookup"><span data-stu-id="fe960-149">This activity is responsible for the following functions:</span></span>

1. <span data-ttu-id="fe960-150">Taotluse koostamine.</span><span class="sxs-lookup"><span data-stu-id="fe960-150">Construct the request.</span></span>
2. <span data-ttu-id="fe960-151">Sisestage taotlus maksuteenusesse.</span><span class="sxs-lookup"><span data-stu-id="fe960-151">Post the request to the tax service.</span></span>
3. <span data-ttu-id="fe960-152">Saate vastuse maksuteenuselt.</span><span class="sxs-lookup"><span data-stu-id="fe960-152">Get the response from the tax service.</span></span>
4. <span data-ttu-id="fe960-153">Sõeluge vastus.</span><span class="sxs-lookup"><span data-stu-id="fe960-153">Parse the response.</span></span>

<span data-ttu-id="fe960-154">Andmeväli, mille lisate taotlusele, sisestatakse koos teiste metaandmetega.</span><span class="sxs-lookup"><span data-stu-id="fe960-154">A data field that you add to the request will be posted together with other metadata.</span></span> 

## <a name="extension-implementation"></a><span data-ttu-id="fe960-155">Laiendi rakendamine</span><span class="sxs-lookup"><span data-stu-id="fe960-155">Extension implementation</span></span>

<span data-ttu-id="fe960-156">Selles jaotises esitatakse üksikasjalikud sammud, mis selgitavad, kuidas laiendust rakendada.</span><span class="sxs-lookup"><span data-stu-id="fe960-156">This section provides detailed steps that explain how to implement the extension.</span></span> <span data-ttu-id="fe960-157">See kasutab näidetena **Kulukeskus** ja **Projekti** finantsdimensioone.</span><span class="sxs-lookup"><span data-stu-id="fe960-157">It uses the **Cost center** and **Project** financial dimensions as examples.</span></span>

### <a name="step-1-add-the-data-variable-in-the-object-class"></a><span data-ttu-id="fe960-158">Toiming 1.</span><span class="sxs-lookup"><span data-stu-id="fe960-158">Step 1.</span></span> <span data-ttu-id="fe960-159">Lisa andmemuutuja objektiklassi</span><span class="sxs-lookup"><span data-stu-id="fe960-159">Add the data variable in the object class</span></span>

<span data-ttu-id="fe960-160">Objektiklass sisaldab andmemuutujat ja andmete tooja/määraja meetodeid.</span><span class="sxs-lookup"><span data-stu-id="fe960-160">The object class contains the data variable and getter/setter methods for the data.</span></span> <span data-ttu-id="fe960-161">Lisage andmeväli kas objektile `TaxIntegrationDocumentObject` või `TaxIntegrationLineObject` olenevalt välja tasemest.</span><span class="sxs-lookup"><span data-stu-id="fe960-161">Add the data field to either `TaxIntegrationDocumentObject` or `TaxIntegrationLineObject`, depending on the level of the field.</span></span> <span data-ttu-id="fe960-162">Järgmises näites kasutatakse reataset ja faili nimi on `TaxIntegrationLineObject_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="fe960-162">The following example uses the line level, and the file name is `TaxIntegrationLineObject_Extension.xpp`.</span></span>

> [!NOTE]
> <span data-ttu-id="fe960-163">Kui lisatv andmeväli on dokumendi tasemel, muutke failinimi nimeks `TaxIntegrationDocumentObject_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="fe960-163">If the data field that you're adding is at the document level, change the file name to `TaxIntegrationDocumentObject_Extension.xpp`.</span></span>

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

<span data-ttu-id="fe960-164">**Kulukeskus** ja **Projekt** lisatakse privaatsete muutujatena.</span><span class="sxs-lookup"><span data-stu-id="fe960-164">**Cost center** and **Project** are added as private variables.</span></span> <span data-ttu-id="fe960-165">Looge nende andmeväljade jaoks tooja- ja määrajameetodid, et andmeid manipuleerida.</span><span class="sxs-lookup"><span data-stu-id="fe960-165">Create getter and setter methods for these data fields to manipulate the data.</span></span>

### <a name="step-2-retrieve-data-from-the-database"></a><span data-ttu-id="fe960-166">Toiming 2.</span><span class="sxs-lookup"><span data-stu-id="fe960-166">Step 2.</span></span> <span data-ttu-id="fe960-167">Tooge andmed andmebaasist</span><span class="sxs-lookup"><span data-stu-id="fe960-167">Retrieve data from the database</span></span>

<span data-ttu-id="fe960-168">Määrake kanne ja laiendage andmete toomiseks sobivad adapteriklassid.</span><span class="sxs-lookup"><span data-stu-id="fe960-168">Specify the transaction, and extend the appropriate adapter classes to retrieve the data.</span></span> <span data-ttu-id="fe960-169">Näiteks kui kasutate kannet **Ostutellimus**, peate laiendama objekte `TaxIntegrationPurchTableDataRetrieval` ja `TaxIntegrationVendInvoiceInfoTableDataRetrieval`.</span><span class="sxs-lookup"><span data-stu-id="fe960-169">For example, if you use a **Purchase order** transaction, you must extend `TaxIntegrationPurchTableDataRetrieval` and `TaxIntegrationVendInvoiceInfoTableDataRetrieval`.</span></span> 

> [!NOTE]
> <span data-ttu-id="fe960-170">Objekt `TaxIntegrationPurchParmTableDataRetrieval` on pärit asukohast `TaxIntegrationPurchTableDataRetrieval`.</span><span class="sxs-lookup"><span data-stu-id="fe960-170">`TaxIntegrationPurchParmTableDataRetrieval` is inherited from `TaxIntegrationPurchTableDataRetrieval`.</span></span> <span data-ttu-id="fe960-171">Seda ei tohi muuta, välja arvatud juhul, kui tabelite `purchTable` ja `purchParmTable` loogika on erinev.</span><span class="sxs-lookup"><span data-stu-id="fe960-171">It should not be changed unless the logic of the `purchTable` and `purchParmTable` tables differs.</span></span>

<span data-ttu-id="fe960-172">Kui andmeväli tuleb lisada kõigile kannetele, laiendage kõiki `DataRetrieval`i klasse.</span><span class="sxs-lookup"><span data-stu-id="fe960-172">If the data field should be added for all transactions, extend all `DataRetrieval` classes.</span></span>

<span data-ttu-id="fe960-173">Kuna kõik **Andmete toomise** tegevused laiendavad sama malliklassi, on klassistruktuurid, muutujad ja meetodid sarnased.</span><span class="sxs-lookup"><span data-stu-id="fe960-173">Because all **Data Retrieval** activities extend the same template class, the class structures, variables, and methods are similar.</span></span>

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

<span data-ttu-id="fe960-174">Järgmine näide näitab tabeli `PurchTable` kasutamise põhistruktuuri.</span><span class="sxs-lookup"><span data-stu-id="fe960-174">The following example shows the basic structure when the `PurchTable` table is used.</span></span>

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

<span data-ttu-id="fe960-175">Kui meetod `CopyToDocument` on kutsutud, siis on puhver `this.purchTable` juba olemas.</span><span class="sxs-lookup"><span data-stu-id="fe960-175">When the `CopyToDocument` method is called, the `this.purchTable` buffer already exists.</span></span> <span data-ttu-id="fe960-176">Selle meetodi eesmärk on kopeerida kõik nõutud andmed tabelist `this.purchTable` objekti `document`, kasutades määraja meetodid, mis loodi klassis `DocumentObject`.</span><span class="sxs-lookup"><span data-stu-id="fe960-176">The purpose of this method is to copy all the required data from `this.purchTable` to the `document` object by using the setter method that was created in the `DocumentObject` class.</span></span>

<span data-ttu-id="fe960-177">Samuti on puhver `this.purchLine` juba olemas meetodis `CopyToLine`.</span><span class="sxs-lookup"><span data-stu-id="fe960-177">Likewise, a `this.purchLine` buffer already exists in the `CopyToLine` method.</span></span> <span data-ttu-id="fe960-178">Selle meetodi eesmärk on kopeerida kõik nõutud andmed tabelist `this.purchLine` objekti `_line`, kasutades määraja meetodid, mis loodi klassis `LineObject`.</span><span class="sxs-lookup"><span data-stu-id="fe960-178">The purpose of this method is to copy all the required data from `this.purchLine` to the `_line` object by using the setter method that was created in the `LineObject` class.</span></span>

<span data-ttu-id="fe960-179">Kõige selgem lähenemine on laiendada meetodeid `CopyToDocument` ja `CopyToLine`.</span><span class="sxs-lookup"><span data-stu-id="fe960-179">The most straightforward approach is to extend the `CopyToDocument` and `CopyToLine` methods.</span></span> <span data-ttu-id="fe960-180">Soovitame siiski esmalt proovida meetodeid `copyToDocumentFromHeaderTable` ja `copyToLineFromLineTable`.</span><span class="sxs-lookup"><span data-stu-id="fe960-180">However, we recommend that you try the `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable` methods first.</span></span> <span data-ttu-id="fe960-181">Kui nad ei tööta nagu vaja, rakendage oma meetodit ja kutsuge see objektidele `CopyToDocument` ja `CopyToLine`.</span><span class="sxs-lookup"><span data-stu-id="fe960-181">If they don't work as you require, implement your own method, and call it in `CopyToDocument` and `CopyToLine`.</span></span> <span data-ttu-id="fe960-182">On kolm tavalist olukorda, kus võite kasutada seda lähenemist.</span><span class="sxs-lookup"><span data-stu-id="fe960-182">There are three common situations where you might use this approach:</span></span>

- <span data-ttu-id="fe960-183">Kohustuslik väli on objektil `PurchTable` või `PurchLine`.</span><span class="sxs-lookup"><span data-stu-id="fe960-183">The required field is in `PurchTable` or `PurchLine`.</span></span> <span data-ttu-id="fe960-184">Selles olukorras saate laiendada objekte `copyToDocumentFromHeaderTable` ja `copyToLineFromLineTable`.</span><span class="sxs-lookup"><span data-stu-id="fe960-184">In this situation, you can extend `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable`.</span></span> <span data-ttu-id="fe960-185">Siin on näidiskood.</span><span class="sxs-lookup"><span data-stu-id="fe960-185">Here is the sample code.</span></span>

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

- <span data-ttu-id="fe960-186">Nõutud andmed pole kande vaiketabelis.</span><span class="sxs-lookup"><span data-stu-id="fe960-186">The required data isn't in the default table of the transaction.</span></span> <span data-ttu-id="fe960-187">Siiski on mõned seosed vaiketabeliga ja väli on enamasti vajalik.</span><span class="sxs-lookup"><span data-stu-id="fe960-187">However, there are some join relationships with the default table, and the field is required on most lines.</span></span> <span data-ttu-id="fe960-188">Sellises olukorras asendage objektid `getDocumentQueryObject` või `getLineObject`, et teha tabelipäringuid liitseostega.</span><span class="sxs-lookup"><span data-stu-id="fe960-188">In this situation, replace `getDocumentQueryObject` or `getLineObject` to query the table by join relationship.</span></span> <span data-ttu-id="fe960-189">Järgmises näites on väli **Tarni kohe** integreeritud müügitellimusega rea tasemel.</span><span class="sxs-lookup"><span data-stu-id="fe960-189">In the following example, the **Deliver Now** field is integrated with the sales order at the line level.</span></span>

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

    <span data-ttu-id="fe960-190">Selles näites on puhver `mcrSalesLineDropShipment` deklareeritud ja päring on määratletud objektis `getLineQueryObject`.</span><span class="sxs-lookup"><span data-stu-id="fe960-190">In this example, a `mcrSalesLineDropShipment` buffer is declared, and the query is defined in `getLineQueryObject`.</span></span> <span data-ttu-id="fe960-191">Päring kasutab suhet `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`.</span><span class="sxs-lookup"><span data-stu-id="fe960-191">The query uses the relationship `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`.</span></span> <span data-ttu-id="fe960-192">Selles olukorras laiendamisel saate asendada objekti `getLineQueryObject` enda loodud päringuobjektiga.</span><span class="sxs-lookup"><span data-stu-id="fe960-192">While you're extending in this situation, you can replace `getLineQueryObject` with your own constructed query object.</span></span> <span data-ttu-id="fe960-193">Kuid arvestage järgmist.</span><span class="sxs-lookup"><span data-stu-id="fe960-193">However, note the following points:</span></span>

    * <span data-ttu-id="fe960-194">Kuna meetodi `getLineQueryObject` tagastusväärtus on `SysDaQueryObject`, peate selle objekti SysDa-lähenemist kasutades konstrueerima.</span><span class="sxs-lookup"><span data-stu-id="fe960-194">Because the return value of the `getLineQueryObject` method is `SysDaQueryObject`, you must construct this object by using the SysDa approach.</span></span>
    * <span data-ttu-id="fe960-195">Olemasolnud tabelit ei saa eemaldada.</span><span class="sxs-lookup"><span data-stu-id="fe960-195">Can't remove existed table.</span></span>

- <span data-ttu-id="fe960-196">Nõutud andmed on kandetabeliga seotud keeruka liitseosega või pole seos üks ühele (1:1) vaid üks mitmele (1:N).</span><span class="sxs-lookup"><span data-stu-id="fe960-196">The required data is related to the transaction table by a complicated join relationship, or the relation isn't one to one (1:1) but one to many (1:N).</span></span> <span data-ttu-id="fe960-197">Sellises olukorras muutuvad asjad veidi keerukamaks.</span><span class="sxs-lookup"><span data-stu-id="fe960-197">In this situation, things become a little complicated.</span></span> <span data-ttu-id="fe960-198">See olukord kehtib näiteks finantsdimensioonide puhul.</span><span class="sxs-lookup"><span data-stu-id="fe960-198">This situation applies to the example of financial dimensions.</span></span> 

    <span data-ttu-id="fe960-199">Sellises olukorras saate rakendada andmete toomiseks oma meetodit.</span><span class="sxs-lookup"><span data-stu-id="fe960-199">In this situation, you can implement your own method to retrieve the data.</span></span> <span data-ttu-id="fe960-200">Siin on faili `TaxIntegrationPurchTableDataRetrieval_Extension.xpp` näidiskood.</span><span class="sxs-lookup"><span data-stu-id="fe960-200">Here is the sample code in the `TaxIntegrationPurchTableDataRetrieval_Extension.xpp` file.</span></span>

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

### <a name="step-3-add-data-to-the-request"></a><span data-ttu-id="fe960-201">Toiming 3.</span><span class="sxs-lookup"><span data-stu-id="fe960-201">Step 3.</span></span> <span data-ttu-id="fe960-202">Taotlusele andmete lisamine</span><span class="sxs-lookup"><span data-stu-id="fe960-202">Add data to the request</span></span>

<span data-ttu-id="fe960-203">Laiendage meetodit `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` või `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` taotlusele andmete lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="fe960-203">Extend the `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` or `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method to add data to the request.</span></span> <span data-ttu-id="fe960-204">Siin on faili `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` näidiskood.</span><span class="sxs-lookup"><span data-stu-id="fe960-204">Here is the sample code in the `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` file.</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
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

<span data-ttu-id="fe960-205">Selles koodis `_destination` on ümbrisobjekt, mida kasutatakse järeltaotluse loomiseks ja `_source` on objekt `TaxIntegrationLineObject`.</span><span class="sxs-lookup"><span data-stu-id="fe960-205">In this code, `_destination` is the wrapper object that is used to generate the post request, and `_source` is the `TaxIntegrationLineObject` object.</span></span> 

> [!NOTE]
> * <span data-ttu-id="fe960-206">Määratlege võti, mida kasutatakse taotluse vormil kui käsku `private const str`.</span><span class="sxs-lookup"><span data-stu-id="fe960-206">Define the key that is used in the request form as `private const str`.</span></span>
> * <span data-ttu-id="fe960-207">Määrake meetodi `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` väli, kasutades meetodit `SetField`.</span><span class="sxs-lookup"><span data-stu-id="fe960-207">Set the field in the `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method by using the `SetField` method.</span></span> <span data-ttu-id="fe960-208">Teise parameetri andmetüüp peab olema `string`.</span><span class="sxs-lookup"><span data-stu-id="fe960-208">The data type of the second parameter should be `string`.</span></span> <span data-ttu-id="fe960-209">Kui andmetüüp ei ole `string`, teisendage see tüübiks `string`.</span><span class="sxs-lookup"><span data-stu-id="fe960-209">If the data type isn't `string`, convert it to `string`.</span></span>

## <a name="appendix"></a><span data-ttu-id="fe960-210">Lisa</span><span class="sxs-lookup"><span data-stu-id="fe960-210">Appendix</span></span>

<span data-ttu-id="fe960-211">Selles lisas kuvatakse reatasemel finantsdimensioonide (**Kulukeskus** ja **Projekt**) integreerimise täielik näidiskood.</span><span class="sxs-lookup"><span data-stu-id="fe960-211">This appendix shows the complete sample code for the integration of financial dimensions (**Cost center** and **Project**) at the line level.</span></span>

### <a name="taxintegrationlineobject_extensionxpp"></a><span data-ttu-id="fe960-212">TaxIntegrationLineObject_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="fe960-212">TaxIntegrationLineObject_Extension.xpp</span></span>

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

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a><span data-ttu-id="fe960-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="fe960-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span></span>

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

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a><span data-ttu-id="fe960-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="fe960-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
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
