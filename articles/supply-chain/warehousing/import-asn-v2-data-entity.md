---
title: Sissetulevate ASN-ide importimine andmeolemi V2 kaudu
description: Selles teemas selgitatakse, kuidas hallata sissetulevate täpsemate saatmisteadete (ASN-ide) importi sissetuleva ASN V2 andmeolemi kaudu.
author: GalynaFedorova
ms.date: 05/31/2021
ms.topic: article
ms.search.form: WHSInboundASNV2Entity, WHSInboundASNEntity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-04
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 470cc0c39f211a5d0f106c4c6e193867388e2b53
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249087"
---
# <a name="import-inbound-asns-through-the-v2-data-entity"></a><span data-ttu-id="ee945-103">Sissetulevate ASN-ide importimine andmeolemi V2 kaudu</span><span class="sxs-lookup"><span data-stu-id="ee945-103">Import inbound ASNs through the V2 data entity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ee945-104">Täpsemad saatmisteated (ASN-id) teavitavad teid hankija tarnetest.</span><span class="sxs-lookup"><span data-stu-id="ee945-104">Advanced shipping notices (ASNs) notify you about vendor deliveries.</span></span> <span data-ttu-id="ee945-105">Need aitavad saatjal kirjeldada saadetise sisu ja lisateavet selle kohta (nt kaubad ja pakendid).</span><span class="sxs-lookup"><span data-stu-id="ee945-105">They help the sender describe the contents of a shipment and additional information about it, such as the items and packaging.</span></span>

<span data-ttu-id="ee945-106">ASNid aitavad laotöötajatel teada saada, mis millal saabub.</span><span class="sxs-lookup"><span data-stu-id="ee945-106">ASNs can help warehouse workers learn what is arriving when.</span></span> <span data-ttu-id="ee945-107">Seetõttu saavad nad selleks valmistuda.</span><span class="sxs-lookup"><span data-stu-id="ee945-107">Therefore, they can prepare.</span></span> <span data-ttu-id="ee945-108">Lisaks saavad laotöötajad kasutada ASN-e, et sobitada saadetise üksikasjad varem loodud seotud ostutellimusega.</span><span class="sxs-lookup"><span data-stu-id="ee945-108">In addition, warehouse workers can use ASNs to match the details of a shipment to the related purchase order that was previously created.</span></span>

<span data-ttu-id="ee945-109">Selles teemas kirjeldatakse hulka stsenaariumeid, mis illustreerivad näidete abil, kuidas töötada ASN-failidega.</span><span class="sxs-lookup"><span data-stu-id="ee945-109">This topic presents a collection of scenarios that show, through examples, how to work with ASN files.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ee945-110">*Sissetulev ASN*-i import rakendub ainult kaupadele, mis on lubatud täpsemaks laohalduseks (WMS).</span><span class="sxs-lookup"><span data-stu-id="ee945-110">*Inbound ASN* import applies only to items that are enabled for advanced warehouse management (WMS).</span></span> <span data-ttu-id="ee945-111">Enne ASN-i saamist tuleb süsteemis registreerida ostutellimus selle hankija vastu, kes ASN-i saadab.</span><span class="sxs-lookup"><span data-stu-id="ee945-111">Before you receive an ASN, a purchase order must be registered in the system against the vendor who is sending that ASN.</span></span>

## <a name="inbound-asn-v2-entity"></a><span data-ttu-id="ee945-112">Sissetulev ASN V2 olem</span><span class="sxs-lookup"><span data-stu-id="ee945-112">Inbound ASN V2 entity</span></span>

<span data-ttu-id="ee945-113">Impordite sissetulevad ASN-id *sissetuleva ASN V2* liitandmeolemi abil.</span><span class="sxs-lookup"><span data-stu-id="ee945-113">You import inbound ASNs by using the *Inbound ASN V2* composite data entity.</span></span> <span data-ttu-id="ee945-114">*Sissetulev ASN V2* kasutab järgmisi üksusi:</span><span class="sxs-lookup"><span data-stu-id="ee945-114">*Inbound ASN V2* takes advantage of the following entities:</span></span>

- <span data-ttu-id="ee945-115">Sissetuleva koorma päis</span><span class="sxs-lookup"><span data-stu-id="ee945-115">Inbound load header</span></span>
- <span data-ttu-id="ee945-116">Sissetuleva saadetise päis</span><span class="sxs-lookup"><span data-stu-id="ee945-116">Inbound shipment header</span></span>
- <span data-ttu-id="ee945-117">Sissetuleva koorma pakendistruktuurid</span><span class="sxs-lookup"><span data-stu-id="ee945-117">Inbound load packing structures</span></span>
- <span data-ttu-id="ee945-118">Sissetuleva koorma pakendistruktuuri juhtumid</span><span class="sxs-lookup"><span data-stu-id="ee945-118">Inbound load packing structure cases</span></span>
- <span data-ttu-id="ee945-119">Sissetuleva koorma pakendistruktuuri juhtumiread</span><span class="sxs-lookup"><span data-stu-id="ee945-119">Inbound load packing structure case lines</span></span>
- <span data-ttu-id="ee945-120">Sissetuleva koorma pakendistruktuuri read</span><span class="sxs-lookup"><span data-stu-id="ee945-120">Inbound load packing structure lines</span></span>

<span data-ttu-id="ee945-121">*Sissetuleva ASN V2* liitandmeolem on mõeldud asünkroonsete integratsioonistsenaariumide jaoks, kus kasutatakse XML-failipõhist importi.</span><span class="sxs-lookup"><span data-stu-id="ee945-121">The *Inbound ASN V2* composite data entity is intended for asynchronous integration scenarios where XML file–based imports are used.</span></span>

## <a name="xml-format-for-importing-asns"></a><span data-ttu-id="ee945-122">XML-vorming ASN-ide importimiseks</span><span class="sxs-lookup"><span data-stu-id="ee945-122">XML format for importing ASNs</span></span>

<span data-ttu-id="ee945-123">Microsoft Dynamics 365 Supply Chain Management toetab ASN-ide importimiseks järgmist XML-vormingut.</span><span class="sxs-lookup"><span data-stu-id="ee945-123">Microsoft Dynamics 365 Supply Chain Management supports the following XML format for importing ASNs.</span></span> <span data-ttu-id="ee945-124">XML-faili iga sõlm tähistab üksiku olemi atribuuti.</span><span class="sxs-lookup"><span data-stu-id="ee945-124">Each node in the XML file represents an attribute from an individual entity.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity>
        <WHSInboundShipmentHeaderEntity>
            <WHSInboundLoadPackingStructureEntity>
                <WHSInboundLoadPackingStructureCaseEntity>
                    <WHSInboundPackingStructureCaseLineV2Entity>
                    </WHSInboundPackingStructureCaseLineV2Entity>
                </WHSInboundLoadPackingStructureCaseEntity>
                <WHSInboundLoadPackingStructureLineV2Entity>
                </WHSInboundLoadPackingStructureLineV2Entity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="examples"></a><span data-ttu-id="ee945-125">Näited</span><span class="sxs-lookup"><span data-stu-id="ee945-125">Examples</span></span>

<span data-ttu-id="ee945-126">Järgmistes alajaotistes on toodud näited hankija saadetiste ASN XML-impordifailide kohta.</span><span class="sxs-lookup"><span data-stu-id="ee945-126">The following subsections provide examples of ASN XML import files for vendor shipments.</span></span>

### <a name="example-1"></a><span data-ttu-id="ee945-127">Näide 1</span><span class="sxs-lookup"><span data-stu-id="ee945-127">Example 1</span></span>

<span data-ttu-id="ee945-128">Järgmises näites kuvatakse XML-fail hankija saadetiste importimiseks ühe ostutellimuse jaoks, kui teenindusjuhtumi üksikasju pole kaasatud.</span><span class="sxs-lookup"><span data-stu-id="ee945-128">The following example shows an XML file for importing vendor shipments for one purchase order when no case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VENDORADDRESSSTREET = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="1" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-2"></a><span data-ttu-id="ee945-129">Näide 2</span><span class="sxs-lookup"><span data-stu-id="ee945-129">Example 2</span></span>

<span data-ttu-id="ee945-130">Järgmises näites kuvatakse XML-fail hankija saadetiste importimiseks ühe ostutellimuse jaoks, kui teenindusjuhtumi üksikasjad on kaasatud.</span><span class="sxs-lookup"><span data-stu-id="ee945-130">The following example shows an XML file for importing vendor shipments for one purchase order when case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity ESTIMATEDARRIVALDATETIME="2021-04-25T11:00:00+00:00">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="MVR_SNN_0004">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="MVR_SNN_0004" PACKEDTOTALQUANTITY="2.00">
                <WHSInboundLoadPackingStructureCaseEntity PARENTPACKINGSTRUCTURELICENSEPLATENUMBER="MVR_SNN_0004" LICENSEPLATENUMBER="MVR_SNN_0004A" PACKEDTOTALQUANTITY="2.00" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000175" ITEMNUMBER="A0001" PURCHASEORDERLINENUMBER="1" QUANTITY="2.00" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-3"></a><span data-ttu-id="ee945-131">Näide 3</span><span class="sxs-lookup"><span data-stu-id="ee945-131">Example 3</span></span>

<span data-ttu-id="ee945-132">Järgmises näites kuvatakse XML-fail hankija saadetiste importimiseks mitme ostutellimuse jaoks, kui teenindusjuhtumi üksikasjad on kaasatud.</span><span class="sxs-lookup"><span data-stu-id="ee945-132">The following example shows an XML file for importing vendor shipments for multiple purchase orders when case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="100" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_02" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="200" UNITSYMBOL="ea" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="P0004" QUANTITY="300" UNITSYMBOL="ea" ITEMBATCHNUMBER="BN0001" />
            </WHSInboundLoadPackingStructureEntity>
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_002">
                <WHSInboundLoadPackingStructureCaseEntity LICENSEPLATENUMBER="LP_ASN_002_C01">
                    <WHSInboundLoadPackingStructureCaseLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="400" UNITSYMBOL="ea" />
                </WHSInboundLoadPackingStructureCaseEntity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="inspect-the-results-of-importing-an-asn-file"></a><span data-ttu-id="ee945-133">ASN-faili importimise tulemuste kontrollimine</span><span class="sxs-lookup"><span data-stu-id="ee945-133">Inspect the results of importing an ASN file</span></span>

<span data-ttu-id="ee945-134">ASN-faili importimise tulemuste kontrollimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ee945-134">Follow these steps to inspect the results of importing an ASN file.</span></span>

1. <span data-ttu-id="ee945-135">Avage **Laohaldus \> Koormad \> Kõik koormad**.</span><span class="sxs-lookup"><span data-stu-id="ee945-135">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="ee945-136">Saate otsida ja avada ASN-impordi osana loodud koormuse.</span><span class="sxs-lookup"><span data-stu-id="ee945-136">Find and open a load that was created as part of an ASN import.</span></span>
1. <span data-ttu-id="ee945-137">Kiirkaardil **Laadimine** peaksite nägema XML-failil põhinevaid väärtusi.</span><span class="sxs-lookup"><span data-stu-id="ee945-137">On the **Load** FastTab, you should see values that are based on the XML file.</span></span>
1. <span data-ttu-id="ee945-138">Kiirkaardil **Laadimise read** peaksite nägema XML-failil põhinevaid ostutellimuse numbreid ja kauba üksikasju.</span><span class="sxs-lookup"><span data-stu-id="ee945-138">On the **Load lines** FastTab, you should see purchase order numbers and item details that are based on the XML file.</span></span>
1. <span data-ttu-id="ee945-139">Koormuse pakkimisstruktuuri läbivaatamiseks valige toimingupaani vahekaardi **Saatmine ja vastuvõtmine** jaotises **Vastuvõtmine** valik **Pakkimisstruktuur**.</span><span class="sxs-lookup"><span data-stu-id="ee945-139">On the Action Pane, on the **Ship and receive** tab, in the **Receive** group, select **Packing structure** to review the packing structure of the load.</span></span>
1. <span data-ttu-id="ee945-140">Kiirkaardil **Kaubaalused** peaksite nägema XML-failil põhinevaid litsentsiplaate.</span><span class="sxs-lookup"><span data-stu-id="ee945-140">On the **Pallets** FastTab, you should see license plates that are based on the XML file.</span></span>
1. <span data-ttu-id="ee945-141">Kiirkaardil **Kastid** peaksite nägema XML-failil põhinevaid juhtumeid.</span><span class="sxs-lookup"><span data-stu-id="ee945-141">On the **Cases** FastTab, you should see cases that are based on the XML file.</span></span>
1. <span data-ttu-id="ee945-142">Kiirkaardil **Kaubad** peaksite nägema XML-failil põhinevaid kaupu ja koguseid.</span><span class="sxs-lookup"><span data-stu-id="ee945-142">On the **Items** FastTab, you should see items and quantities that are based on the XML file.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
