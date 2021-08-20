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
ms.openlocfilehash: 8f3c42e28b01afd3b7ca8b1af8381dd5377e17eb31da655a397bd7805779f879
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751693"
---
# <a name="import-inbound-asns-through-the-v2-data-entity"></a>Sissetulevate ASN-ide importimine andmeolemi V2 kaudu

[!include [banner](../../includes/banner.md)]

Täpsemad saatmisteated (ASN-id) teavitavad teid hankija tarnetest. Need aitavad saatjal kirjeldada saadetise sisu ja lisateavet selle kohta (nt kaubad ja pakendid).

ASNid aitavad laotöötajatel teada saada, mis millal saabub. Seetõttu saavad nad selleks valmistuda. Lisaks saavad laotöötajad kasutada ASN-e, et sobitada saadetise üksikasjad varem loodud seotud ostutellimusega.

Selles teemas kirjeldatakse hulka stsenaariumeid, mis illustreerivad näidete abil, kuidas töötada ASN-failidega.

> [!IMPORTANT]
> *Sissetulev ASN*-i import rakendub ainult kaupadele, mis on lubatud täpsemaks laohalduseks (WMS). Enne ASN-i saamist tuleb süsteemis registreerida ostutellimus selle hankija vastu, kes ASN-i saadab.

## <a name="inbound-asn-v2-entity"></a>Sissetulev ASN V2 olem

Impordite sissetulevad ASN-id *sissetuleva ASN V2* liitandmeolemi abil. *Sissetulev ASN V2* kasutab järgmisi üksusi:

- Sissetuleva koorma päis
- Sissetuleva saadetise päis
- Sissetuleva koorma pakendistruktuurid
- Sissetuleva koorma pakendistruktuuri juhtumid
- Sissetuleva koorma pakendistruktuuri juhtumiread
- Sissetuleva koorma pakendistruktuuri read

*Sissetuleva ASN V2* liitandmeolem on mõeldud asünkroonsete integratsioonistsenaariumide jaoks, kus kasutatakse XML-failipõhist importi.

## <a name="xml-format-for-importing-asns"></a>XML-vorming ASN-ide importimiseks

Microsoft Dynamics 365 Supply Chain Management toetab ASN-ide importimiseks järgmist XML-vormingut. XML-faili iga sõlm tähistab üksiku olemi atribuuti.

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

## <a name="examples"></a>Näited

Järgmistes alajaotistes on toodud näited hankija saadetiste ASN XML-impordifailide kohta.

### <a name="example-1"></a>Näide 1

Järgmises näites kuvatakse XML-fail hankija saadetiste importimiseks ühe ostutellimuse jaoks, kui teenindusjuhtumi üksikasju pole kaasatud.

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

### <a name="example-2"></a>Näide 2

Järgmises näites kuvatakse XML-fail hankija saadetiste importimiseks ühe ostutellimuse jaoks, kui teenindusjuhtumi üksikasjad on kaasatud.

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

### <a name="example-3"></a>Näide 3

Järgmises näites kuvatakse XML-fail hankija saadetiste importimiseks mitme ostutellimuse jaoks, kui teenindusjuhtumi üksikasjad on kaasatud.

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

## <a name="inspect-the-results-of-importing-an-asn-file"></a>ASN-faili importimise tulemuste kontrollimine

ASN-faili importimise tulemuste kontrollimiseks toimige järgmiselt.

1. Avage **Laohaldus \> Koormad \> Kõik koormad**.
1. Saate otsida ja avada ASN-impordi osana loodud koormuse.
1. Kiirkaardil **Laadimine** peaksite nägema XML-failil põhinevaid väärtusi.
1. Kiirkaardil **Laadimise read** peaksite nägema XML-failil põhinevaid ostutellimuse numbreid ja kauba üksikasju.
1. Koormuse pakkimisstruktuuri läbivaatamiseks valige toimingupaani vahekaardi **Saatmine ja vastuvõtmine** jaotises **Vastuvõtmine** valik **Pakkimisstruktuur**.
1. Kiirkaardil **Kaubaalused** peaksite nägema XML-failil põhinevaid litsentsiplaate.
1. Kiirkaardil **Kastid** peaksite nägema XML-failil põhinevaid juhtumeid.
1. Kiirkaardil **Kaubad** peaksite nägema XML-failil põhinevaid kaupu ja koguseid.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
