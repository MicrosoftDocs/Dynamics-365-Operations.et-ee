---
title: "Rakenduse Finance and Operations müügitellimuse päiste ja ridade sünkroonimine rakendusega Sales"
description: "See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse müügitellimuste päiste ja ridade sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations, Enterprise edition rakendusse Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c7b2ff6430e99661ee284f65089086df9fa5a1ad
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a>Rakenduse Finance and Operations müügitellimuse päiste ja ridade sünkroonimine rakendusega Sales

[!include[banner](../includes/banner.md)]

See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse müügitellimuste päiste ja ridade sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations, Enterprise edition rakendusse Microsoft Dynamics 365 for Sales. 

## <a name="template-and-tasks"></a>Mall ja ülesanded

Müügitellimuste päiste ja ridade sünkroonimiseks rakendusest Finance and Operations rakendusse Sales kasutatakse järgmisi malle ja aluseks olevaid ülesandeid.

- **Malli nimi andmete integratsioonis** 

    - Müügtellimused (Fin and Opsist Salesi)
    
- **Ülesannete nimed andmete integratsiooni projektis**

    - OrderHeader
    - OrderLine

Enne Salesi müügiarve päise ja ridade sünkroonimist vajalikud sünkroonimistoimingud.

- Tooted (Fin and Opsist Salesi)
- Kontod (Salesist Fin and Opsi) (kui kasutatakse)
- Kontaktid klientideks (Salesist Fin and Opsi) (kui kasutatakse)

## <a name="entity-set"></a>Üksuste komplekt

| Finance and Operations |    Common Data Service (CDS)         |     Müük      |
|------------------------|----------------|----------------|
| CDS-i müügitellimuste päised CDS| SalesOrder     | SalesOrders |
| CDS-i müügitellimuse read  | SalesOrderLine | SalesOrderDetails|

## <a name="entity-flow"></a>Üksuse voog

Müügitellimused luuakse rakenduses Finance and Operations ja sünkroonitakse rakendusega Sales.

Malli filtrid tagavad ainult asjakohaste müügitellimuste kaasamise sünkroonimisse.

- Sünkroonimisse lisatakse nii tellimuse kui ka arvelduse klient rakenduse Sales müügitellimuselt. Rakenduses Finance and Operations kasutatakse välju **OrderingCustomerIsExternallyMaintained** ja **InvoiceCustomerIsExternallyMaintained** andmeüksustes sünkroonimise jälgimiseks.

- Üksuse **Müügitellimus** rakenduses Finance and Operations peab kinnitama. Rakendusega Sales sünkroonitakse ainult kõrgema töötlemisolekuga kinnitatud müügitellimused, nt olekuga Saadetud või arveldatud.

- Pärast müügitellimuse loomist või muutmist tuleb käivitada pakett-töö **Müügi kogusummade arvutamine** rakenduses Finance and Operations. CDS-i ja Salesiga sünkroonitakse ainult need müügitellimused, mille müügi kogusummad on arvutatud.

> [!NOTE]
> Jaotises **Müügitellimuse päis** olevate tasudega seotud maksu ei arvestata praegu Finance and Operationsi ja Salesi sünkroonimisel. See on nii, kuna Sales ei toeta maksuteavet päise tasandil. Rea tasandil tasudega seotud maksu arvestatakse.

## <a name="prospect-to-cash-solution-for-sales"></a>Lahendus Potentsiaalne klient sularahaks rakendusele Sales

Üksusele **Tellimus** lisatakse uued väljad ja need kuvatakse järgmisel lehel.

- **Hallatakse väliselt** – seadke väärtusele **Jah**, kui tellimus rakendusest Finance and Operations tuleb.

- **Töötlemise olek** – kasutatakse tellimuse töötlemise oleku kuvamiseks rakenduses Finance and Operations. Väärtused on järgmised.

    - Aktiivne
    - Kinnitatud
    - Saateleht
    - Arveldatud
    - Komplekteeritud
    - Osaliselt komplekteeritud
    - Osaliselt pakitud
    - Välja saadetud
    - Osaliselt tarnitud
    - Osaliselt arvele kantud
    - Tühistatud

Sätet **Sisaldab ainult väliselt hallatavaid tooteid** kasutatakse teistes müügitellimuse stsenaariumides (rakendusest Sales rakendusse Finance and Operations sünkroonimisel), et jälgida, kas müügitellimus koosneb täielikult **väliselt hallatavatest toodetest**, millisel juhul tooteid hallatakse rakenduses Finance and Operations. See tagab, et te ei püüa sünkroonida müügitellimuse ridu toodetega, mis on rakendusele Finance and Operations tundmatud.
 
Nupud **Arve koostamine**, **Tellimuse tühistamine**, **Ümberarvutamine**, **Toodete toomine** ja **Aadressi otsimine** lehel **Müügitellimus** on väliselt hallatavate tellimuste puhul peidetud, kuna arved luuakse rakenduses Finance and Operations ja sünkroonitakse rakendusega Sales. Tellimuse lehte ei saa redigeerida, müügitellimuse teave sünkroonitakse Finance and Operationsist.
 
**Müügitellimuse olek** jääb aktiivseks, et rakenduse Finance and Operations muudatused saaksid liikuda rakenduses Sales jaotisse **Müügitellimus**. Seda juhitakse, määrates andmeintegratsiooni projektis vaikeväärtuse **Olekukood [olek]** väärtuseks **Aktiivne**.

## <a name="preconditions-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine 

Enne müügitellimuste sünkroonimist on oluline värskendada süsteeme järgmise sättega.

### <a name="setup-in-sales"></a>Seadistus rakenduses Sales

- Tagage meeskonnale load, millele kasutaja (teie rakenduse Sales jaotisest **Ühendusekomplekt**) on määratud. Demoandmete kasutamisel on kasutajal tavaliselt administraatori juurdepääs, kuid töörühmal mitte. Ilma selleta saate tõrke, et peamine töörühm puudub, kui käivitate projekti andmete integraatorist. 

    - Valige jaotisest **Sätted** > **Turve** > **Töörühmad** asjakohane töörühm, klõpsake valikut **Rollide haldamine** ja valige soovitud õigustega roll, nt Süsteemiadministraator.

- Veenduge, et jaotises **Sätted** > **Haldus** > **Süsteemisätted** > **Sales**, et valiku **Kasuta süsteemi hinna arvutamise süsteemi** väärtuseks oleks määratud **Jah**. 

- Veenduge, et jaotises **Sätted** > **Haldus** > **Süsteemisätted** > **Sales**, et valiku **Allahindluse arvutamise meetod** väärtuseks oleks määratud **Reaüksus**. 

### <a name="setup-in-finance-and-operations"></a>Seadistus rakenduses Finance and Operations

Määrake **Müük ja turundus** > **Perioodilised ülesanded** > **Müügi kogusummade arvutamine** töötama pakett-tööna, nii et valiku **Müügitellimuste kogusummade arvutamine** väärtuseks on määratud **Jah**. See on oluline, kuna CDS-i ja Salesiga sünkroonitakse ainult need müügitellimused, mille müügi kogusummad on arvutatud. Pakett-töö sagedus tuleks sobitada müügitellimuse sünkroonimise sagedusega.

### <a name="setup-in-the-data-integration-project"></a>Seadistus andmeintegratsiooni projektis

#### <a name="salesheader-task"></a>Ülesanne SalesHeader

- Värskendage väärtuse **CDS-i organisatsiooni ID vastendus jaotises Allikas** > **CDS**.

    - Atribuudi **Account_Organization_OrganizationId** malli vaikeväärtus on ORG001.
    - Atribuudi **InvoiceAccount_Organization_OrganizationId** malli vaikeväärtus on ORG001.
    - Atribuudi **Organization_OrganizationId** malli vaikeväärtus on ORG001.

- Veenduge, et oleks olemas vajalik vastendus atribuutide **Allikas** > **CDS atribuudile InvoiceCountryRegionId ja BillingAddress_Country** ning **DeliveryCountryRegionId ja DeliveryAddress_Country** vahel.

    - Malli väärtus on **ValueMap** koos vastendatud riikide arvuga.

- **Hinnakiri** on vajalik tellimuste koostamiseks rakenduses Sales. Värskendage parameetrit **ValueMap** jaotises **CDS** > **Üksuse** **pricelevelid.name [hinnakirja nimi] sihtkoht** väärtuseks **Hinnakiri**, mida kasutatakse jaotises Müük valuuta kohta. Võite kasutada vaikeväärtust **Hinnakiri** ühe valuuta kohta või parameetrit **ValueMap**, kui teil on erinevates valuutades **hinnakirjad**.
    
    - Üksuse **pricelevelid.name [hinnakirja nimi]** malli vaikeväärtus on USA CRM-i teenus (näidis). 

#### <a name="salesline-task"></a>Ülesanne SalesLine

- Värskendage väärtuse **CDS-i organisatsiooni ID vastendus jaotises Allikas** > **CDS**. 
    
    - Atribuudi **SalesOrder_Organization_OrganizationId** vaikemalli väärtus on ORG001.
    - Atribuudi **Product_Organization_OrganizationId** malli vaikeväärtus on ORG001.

- Veenduge, et jaotise **Allikas** > **CDS** atribuudile **DeliveryCountryRegionId** ja **DeliveryAddress_Country** vahel oleks vajalik vastendus olemas.

    - Malli väärtus on **ValueMap** koos vastendatud riikide arvuga.
    
- Veenduge, et vajalik **ValueMap** parameetrile **SalesUnitSymbol** rakenduses Finance and Operations oleks olemas jaotises **Allikas** > **CDS-i vastendus**.

    - Malli väärtus parameetriga **ValueMap** määratletakse üksusele **SalesUnitSymbol to Quantity_UOM**.

## <a name="template-mapping-in-data-integrator"></a>Malli vastendamine andmeintegraatoris

> [!NOTE]
> Väljad **Maksetingimused**, **Veosetingimused**, **Tarnetingimused**, **Saatmisviis** ja **Tarneviis** ei ole vaikevastenduste osa. Nende väljade vastendamiseks peate seadistama väärtuskaardi, mis on kohane neis organisatsioonides olevatele andmetele, mille vahel üksust sünkroonitakse.

Järgmisel joonisel on toodud näide malli vastendusest andmeintegraatoris.

### <a name="orderheader"></a>OrderHeader

![Malli vastendamine andmeintegraatoris](./media/sales-order-template-mapping-data-integrator-1.png)

![Malli vastendamine andmeintegraatoris](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a>OrderLine

![Malli vastendamine andmeintegraatoris](./media/sales-order-template-mapping-data-integrator-3.png)

![Malli vastendamine andmeintegraatoris](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Seotud dokumendid

[Rakenduse Finance and Operations toodete sünkroonimine rakenduse Sales toodetega](products-template-mapping.md)

[Rakenduse Sales kontode sünkroonimine rakenduse Finance and Operations klientidega](accounts-template-mapping.md)

[Rakenduse Sales kontaktide sünkroonimine rakenduse Finance and Operations kontaktide või klientidega](contacts-template-mapping.md)

[Rakenduse Sales müügipakkumise päiste ja ridade sünkroonimine rakendusega Finance and Operations](sales-quotation-template-mapping.md)

[Rakenduse Finance and Operations müügiarve päiste ja ridade sünkroonimine rakendusega Sales](sales-invoice-template-mapping.md)


