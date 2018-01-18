---
title: "Rakenduse Finance and Operations müügiarve päiste ja ridade sünkroonimine rakendusega Sales"
description: "See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse müügiarvete päiste ja ridade sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations, Enterprise edition rakendusse Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 22ab02555dcac850b18aac9564af41d6c627eade
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a>Rakenduse Finance and Operations müügiarve päiste ja ridade sünkroonimine rakendusega Sales

[!include[banner](../includes/banner.md)]

See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse müügiarvete päiste ja ridade sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations, Enterprise edition rakendusse Microsoft Dynamics 365 for Sales. 

## <a name="templates-and-tasks"></a>Mallid ja ülesanded

Müügiarvete päiste ja ridade sünkroonimiseks rakendusest Finance and Operations rakendusse Sales kasutatakse järgmisi malle ja aluseks olevaid ülesandeid.

- **Malli nimi andmete integratsioonis** 

     - Müügiarved (Fin and Opsist Salesi)

- **Ülesannete nimed andmete integratsiooni projektis**

    - SalesInvoiceHeader
    - SalesInvoiceLine

Enne Salesi müügiarve päise ja ridade sünkroonimist vajalikud sünkroonimistoimingud.
-   Tooted (Fin and Opsist Salesi)
-   Kontod (Salesist Fin and Opsi) (kui kasutatakse)
-   Kontaktid (Salesist Fin and Opsi) (kui kasutatakse)
-   Müügitellimuse päis ja read (Fin and Opsist Salesi)

## <a name="entity-set"></a>Üksuste komplekt

| Finance and Operations                               | Common Data Service (CDS)              | Müük          |
|------------------------------------------------------|------------------|----------------|
| Väliselt hallatava kliendi müügiarve päised | SalesInvoice     | Arved       |
| Väliselt hallatava kliendi müügiarve read   | SalesInvoiceLine | InvoiceDetails |

## <a name="entity-flow"></a>Üksuse voog

Müügiarved luuakse rakenduses Finance and Operations ja sünkroonitakse rakendusega Sales.

> [!NOTE]
> Jaotises **Müügiarve päis** olevate tasudega seotud maksu ei arvestata praegu Finance and Operationsi ja Salesi sünkroonimisel. See on nii, kuna Sales ei toeta maksuteavet päise tasandil. Rea tasandil tasudega seotud maksu arvestatakse.

## <a name="prospect-to-cash-solution-for-sales"></a>Lahendus Potentsiaalne klient sularahaks rakendusele Sales

-  **Arve numbri väli** lisatakse üksusele **Arve** ja kuvatakse lehel.
 
-  Nupp **Arve koostamine** lehel **Müügitellimus** on peidetud, kuna arved koostatakse Finance and Operationsis ja sünkroonitakse Salesiga. Lehte **Arve** ei saa redigeerida, kuna arved sünkroonitakse Finance and Operationsist.
 
-  **Müügitellimuse olek** muutub automaatselt olekuks **Arveldatud**, kui seotud arve Finance and Operationsist on Salesiga sünkroonitud. Samuti määratakse selle müügitellimuse omanik, millest arve loodi, arve omanikuks. See annab müügitellimuse omanikule võimaluse arvet vaadata.
 
## <a name="preconditions-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

Enne müügiarvete sünkroonimist on oluline värskendada süsteeme järgmise sättega.

### <a name="setup-in-sales"></a>Seadistus rakenduses Sales

- Veenduge, et jaotises **Sätted** > **Haldus** > **Süsteemisätted** > **Sales**, et valiku **Kasuta süsteemi hinna arvutamise süsteemi** väärtuseks oleks määratud **Jah**. 

- Veenduge, et jaotises **Sätted** > **Haldus** > **Süsteemisätted** > **Sales**, et valiku **Allahindluse arvutamise meetod** väärtuseks oleks määratud **Reaüksus**. 

### <a name="setup-in-the-data-integration-project"></a>Seadistus andmeintegratsiooni projektis

#### <a name="salesinvoiceheader-task"></a>Toiming SalesInvoiceHeader

- Värskendage väärtuse **CDS-i organisatsiooni ID** vastendus jaotises **Allikas** > **CDS**. 

    -  Atribuudi **SalesOrder_Organization_OrganizationId** vaikemalli väärtus on ORG001.
    -  Atribuudi **Account_Organization_OrganizationId** malli vaikeväärtus on ORG001.
    -  Atribuudi **Organization_OrganizationId** malli vaikeväärtus on ORG001.

- Veenduge, et jaotise **Allikas** > **CDS atribuudile InvoiceCountryRegionId** ja **BillingAddress_Country** vahel oleks vajalik vastendus olemas.

    -  Malli väärtus on **ValueMap** koos vastendatud riikide arvuga.

- **Hinnakiri** on vajalik arvete koostamiseks rakenduses Sales. Värskendage parameetrit **ValueMap** jaotises **CDS** > **Üksuse pricelevelid.name [hinnakirja nimi] sihtkoht** väärtuseks **Hinnakiri**, mida kasutatakse jaotises Müük valuuta kohta. Võite kasutada vaikeväärtust **Hinnakiri** ühe valuuta kohta või parameetrit **ValueMap**, kui teil on erinevates valuutades **hinnakirjad**.

    -  Üksuse **pricelevelid.name [hinnakirja nimi]** malli väärtus on **ValueMap**, mis põhineb väärtusel **Valuuta**.
    -  usd: USA CRM-i teenus (näidis). 

#### <a name="salesinvoiceline-task"></a>Toiming SalesInvoiceLine

- Veenduge, et vajalik vastendus oleks olemas, jaotises **Allikas** > **CDS mõõtühikuna**.

- Veenduge, et vajalik **ValueMap** parameetrile **SalesUnitSymbol** rakenduses Finance and Operations oleks olemas jaotises **Allikas** > **CDS-i vastendus**. 
    
    - Malli väärtus parameetriga **ValueMap** määratletakse üksusele **SalesUnitSymbol to Quantity_UOM**.
    
-  Värskendage väärtuse **CDS-i organisatsiooni ID vastendus jaotises Allikas** > **CDS**. 

    -  Atribuudi **SalesInvoicer_Organization_OrganizationId** vaikemalli väärtus on ORG001.
    -  Atribuudi **Product_Organization_OrganizationId** malli vaikeväärtus on ORG001.
 
## <a name="template-mapping-in-data-integrator"></a>Malli vastendamine andmeintegraatoris

> [!NOTE]
> Väljad **Maksetingimused**, **Veosetingimused**, **Tarnetingimused**, **Saatmisviis** ja **Tarneviis** ei ole vaikevastenduste osa. Nende väljade vastendamiseks on vaja seadistada väärtuskaart, mis põhineb nende organisatsioonide andmetel, mille vahel üksust sünkroonitakse.

Järgmisel joonisel on toodud näide malli vastendusest andmeintegraatoris.

![Malli vastendamine andmeintegraatoris](./media/sales-invoice-template-mapping-data-integrator-1.png)

![Malli vastendamine andmeintegraatoris](./media/sales-invoice-template-mapping-data-integrator-2.png)

![Malli vastendamine andmeintegraatoris](./media/sales-invoice-template-mapping-data-integrator-3.png)

![Malli vastendamine andmeintegraatoris](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Seotud dokumendid

[Rakenduse Finance and Operations toodete sünkroonimine rakenduse Sales toodetega](products-template-mapping.md)

[Rakenduse Sales kontode sünkroonimine rakenduse Finance and Operations klientidega](accounts-template-mapping.md)

[Rakenduse Sales kontaktide sünkroonimine rakenduse Finance and Operations kontaktide või klientidega](contacts-template-mapping.md)

[Rakenduse Sales müügipakkumise päiste ja ridade sünkroonimine rakendusega Finance and Operations](sales-quotation-template-mapping.md)

[Rakenduse Finance and Operations müügitellimuse päiste ja ridade sünkroonimine rakendusega Sales](sales-order-template-mapping.md)


