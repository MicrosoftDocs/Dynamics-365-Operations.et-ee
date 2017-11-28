---
title: "Rakenduse Finance and Operations müügiarve päiste ja ridade vahetu sünkroonimine rakendusega Sales"
description: "See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse müügiarvete päiste ja ridade vahetuks sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition rakendusse Microsoft Dynamics 365 for Sales."
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
ms.openlocfilehash: e9d7e756c56932372ed931620016973c794fb3fc
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Rakenduse Finance and Operations müügiarve päiste ja ridade vahetu sünkroonimine rakendusega Sales

[!include[banner](../includes/banner.md)]

See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse müügiarvete päiste ja ridade vahetuks sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition rakendusse Microsoft Dynamics 365 for Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Andmevoog lahenduses Potentsiaalne klient sularahaks

Lahendus Potentsiaalne klient sularahaks kasutab andmete integreerimise funktsiooni andmete sünkroonimiseks rakenduste Finance and Operations ja Sales vahel. Andmete integratsiooniga saadaolevad lahenduse Potentsiaalne klient sularahaks mallid võimaldavad kontode, kontaktide, toodete, müügipakkumiste, müügitellimuste ja müügiarvete andmete liikumist rakenduste Finance, Operations ja Sales. Järgmine illustratsioon näitab, kuidas sünkroonitakse andmeid rakenduste Finance and Operations ja Sales vahel.

[![Andmevoog lahenduses Potentsiaalne klient sularahaks](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Mallid ja ülesanded

Saadaolevatele mallidele juurdepääsemiseks avage [PowerApps administreerimiskeskus](https://preview.admin.powerapps.com/dataintegration). Valige **Projektid** ja seejärel paremas ülanurgas **Uus projekt**, et valida avalikud mallid.

Müügiarvete päiste ja ridade sünkroonimiseks rakendusest Finance and Operations rakendusse Sales kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

- **Andmete integratsioon malli nimi:** müügiarved (rakendusest Fin and Ops rakendusse Sales) – otse
- **Ülesannete nimed andmete integratsiooni projektis.**

    - SalesInvoiceHeader
    - SalesInvoiceLine

Enne müügiarvete päiste ja ridade sünkroonimist on nõutavad järgmised sünkroonimisülesanded.

- Tooted (rakendusest Sales rakendusse Fin and Ops) – otse
- Kontod (rakendusest Sales rakendusse Fin and Ops) – otse (kui on kasutusel)
- Kontaktid (rakendusest Sales rakendusse Fin and Ops) – otse (kui on kasutusel)
- Müügitellimuse päis ja read (rakendusest Fin and Ops rakendusse Sales) – otse

## <a name="entity-set"></a>Üksuste komplekt

| Finance and Operations                               | Müük          |
|------------------------------------------------------|----------------|
| Väliselt hallatava kliendi müügiarve päised | Arved       |
| Väliselt hallatava kliendi müügiarve read   | InvoiceDetails |

## <a name="entity-flow"></a>Üksuse voog

Müügiarved luuakse rakenduses Finance and Operations ja sünkroonitakse rakendusega Sales.

> [!NOTE]
> Müügiarve päises olevate tasudega seotud maksu ei arvestata praegu Finance and Operationsi ja Salesi sünkroonimisel. Sales ei toeta maksuteavet päise tasandil. Sünkroonimine hõlmab aga makse, mis on seotud rea tasemel tasudega.

## <a name="prospect-to-cash-solution-for-sales"></a>Lahendus Potentsiaalne klient sularahaks rakendusele Sales

- Väli **Arve number** lisati üksusesse **Arve** ja kuvatakse lehel.
- Nupp **Arve koostamine** lehel **Müügitellimus** on peidetud, kuna arved koostatakse Finance and Operationsis ja sünkroonitakse Salesiga. Lehte **Arve** ei saa redigeerida, kuna arved sünkroonitakse Finance and Operationsist.
- Väärtus **Müügitellimuse olek** asendatakse automaatselt olekuga **Arveldatud**, kui seotud arve Finance and Operationsist on Salesiga sünkroonitud. Samuti määratakse selle müügitellimuse omanik, millest arve loodi, arve omanikuks. Seetõttu saab müügitellimuse omanik arvet vaadata.

## <a name="preconditions-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

Enne müügiarvete sünkroonimist on oluline värskendada süsteemides järgmisi sätteid.

### <a name="setup-in-sales"></a>Seadistus rakenduses Sales

Avage jaotis **Sätted** > **Administreerimine** > **Süsteemisätted** > **Sales** ja veenduge, et kasutusel oleks järgmised sätted.

- Suvand **Kasuta süsteemi hinna arvutamise süsteemi** on seatud väärtusele **Jah**.
- Väli **Allahindluse arvutamise meetod** on seatud väärtusele **Rea kaup**.

### <a name="setup-in-the-data-integration-project"></a>Seadistus andmeintegratsiooni projektis

#### <a name="salesinvoiceheader-task"></a>Toiming SalesInvoiceHeader

- Veenduge, et atribuutide **InvoiceCountryRegionId** ja **BillingAddress\_Country** vahel oleks olemas nõutav vastendus.

    Malli väärtus on väärtuste kaart, kus on vastendatud mitu riiki või regiooni.

- Hinnakiri on vajalik arvete koostamiseks rakenduses Sales. Värskendage üksuse **pricelevelid.name \[Hinnakirja nimi\]** väärtuskaarti hinnakirja alusel, mida kasutatakse rakenduses Sales valuuta kohta. Saate ühe valuuta puhul kasutada vaikehinnakirja. Kui teil on mitmes valuutas hinnakirju, saate kasutada väärtuskaarti.

    Atribuudi **pricelevelid.name \[Hinnakirja nimi\]** malli väärtus on valuutal põhinev väärtuskaart, kus USA dollar = USA CRM-i teenus (näide).  
    
#### <a name="salesinvoiceline-task"></a>Toiming SalesInvoiceLine

- Veenduge, et atribuudi **Unit of measure** jaoks oleks olemas nõutav vastendus.
- Veenduge, et üksuse **SalesUnitSymbol** nõutav väärtuskaart oleks rakenduses Finance and Operations olemas.

    Üksuste **SalesUnitSymbol** ja **Quantity\_UOM** jaoks on määratletud väärtuskaardiga malli väärtus.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

> [!NOTE]
> Väljad **Maksetingimused**, **Veosetingimused**, **Tarnetingimused**, **Saatmisviis** ja **Tarneviis** ei ole vaikevastenduste osa. Nende väljade vastendamiseks peate seadistama väärtuskaardi, mis on kohane neis organisatsioonides olevatele andmetele, mille vahel üksust sünkroonitakse.

Järgmisel joonisel on toodud näide malli vastendusest andmete integratsioonis. 

> [!NOTE]
> Vastendamine näitab, millise välja teave sünkroonitakse rakendusest Sales rakendusse Finance and Operations.

### <a name="salesinvoiceheader"></a>SalesInvoiceHeader

![Malli vastendamine andmete integratsioonis](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a>SalesInvoiceLine

![Malli vastendamine andmete integratsioonis](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>Seotud dokumendid

[Potentsiaalne klient sularahaks](prospect-to-cash.md)

[Rakenduse Sales kontode vahetu sünkroonimine rakenduse Finance and Operations klientidega](accounts-template-mapping-direct.md)

[Rakenduse Finance and Operations toodete vahetu sünkroonimine rakenduse Sales toodetega](products-template-mapping-direct.md)

[Rakenduse Sales kontaktide vahetu sünkroonimine rakenduse Finance and Operations kontaktide või klientidega](contacts-template-mapping-direct.md)

[Rakenduse Finance and Operations müügitellimuse päiste ja ridade vahetu sünkroonimine rakendusega Sales](sales-order-template-mapping-direct.md)







