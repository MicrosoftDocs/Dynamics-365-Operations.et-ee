---
title: Rakenduse Supply Chain Management müügiarvete päiste ja ridade sünkroonimine otse rakendusega Sales
description: Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse müügipakkumise päiste ning ridade sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Sales.
author: ChristianRytt
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 9076d04e71ceae41a4fbdd09bebd2db8e9ed298c2a318a64f2fea6fb71447e5b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736643"
---
# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Rakenduse Finance and Operations müügiarvete päiste ja ridade sünkroonimine otse rakendusega Sales

[!include [banner](../includes/banner.md)]

Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse müügipakkumise päiste ning ridade sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Andmevoog lahenduses Potentsiaalne klient sularahaks

Lahendus Potentsiaalne klient sularahaks kasutab andmete integreerimise funktsiooni andmete sünkroonimiseks rakenduste Supply Chain Management ja Sales vahel. Andmete integratsiooniga saadaolevad lahenduse Potentsiaalne klient sularahaks mallid võimaldavad kontode, kontaktide, toodete, müügipakkumiste, müügitellimuste ja müügiarvete andmete liikumist rakenduste Supply Chain Management ja Sales. Järgmine illustratsioon näitab, kuidas sünkroonitakse andmeid rakenduste Supply Chain Management ja Sales vahel.

[![Andmevoog lahenduses Potentsiaalne klient sularahaks.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Mallid ja ülesanded

Saadaolevatele mallidele juurdepääsemiseks avage [Power Apps administreerimiskeskus](https://preview.admin.powerapps.com/dataintegration). Valige **Projektid** ja seejärel paremas ülanurgas **Uus projekt**, et valida avalikud mallid.

Müügiarve päiste ja ridade sünkroonimiseks rakendusest Supply Chain Management rakendusse Sales kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

- **Andmete integratsioon malli nimi:** müügiarved (rakendusest Fin and Ops rakendusse Sales) – otse
- **Ülesannete nimed andmete integratsiooni projektis.**

    - SalesInvoiceHeader
    - SalesInvoiceLine

Enne müügiarvete päiste ja ridade sünkroonimist on nõutavad järgmised sünkroonimisülesanded.

- Tooted (rakendusest Supply Chain Management rakendusse Sales) - otse
- Kontod (rakendusest Sales rakendusse Supply Chain Management) - otse (kui kasutatakse)
- Kontaktid (rakendusest Sales rakendusse Supply Chain Management) - otse (kui kasutatakse)
- Müügitellimuse päis ja read (rakendusest Supply Chain Management rakendusse Sales) – otse

## <a name="entity-set"></a>Üksuste komplekt

| Supply Chain Management                              | Müük          |
|------------------------------------------------------|----------------|
| Väliselt hallatava kliendi müügiarve päised | Arved       |
| Väliselt hallatava kliendi müügiarve read   | InvoiceDetails |

## <a name="entity-flow"></a>Üksuse voog

Müügiarved luuakse rakenduses Supply Chain Management ja sünkroonitakse rakendusega Sales.

> [!NOTE]
> Müügiarve päises olevate tasudega seotud maksu ei arvestata praegu Supply Chain Managementi ja Salesi sünkroonimisel. Sales ei toeta maksuteavet päise tasandil. Sünkroonimine hõlmab aga makse, mis on seotud rea tasemel tasudega.

## <a name="prospect-to-cash-solution-for-sales"></a>Lahendus Potentsiaalne klient sularahaks rakendusele Sales

- Väli **Arve number** lisati üksusesse **Arve** ja kuvatakse lehel.
- Nupp **Arve koostamine** lehel **Müügitellimus** on peidetud, kuna arved koostatakse Supply Chain Managementis ja sünkroonitakse Salesiga. Lehte **Arve** ei saa redigeerida, kuna arved sünkroonitakse Supply Chain Managementist.
- Väärtus **Müügitellimuse olek** asendatakse automaatselt olekuga **Arveldatud**, kui seotud arve Supply Chain Managementist on Salesiga sünkroonitud. Samuti määratakse selle müügitellimuse omanik, millest arve loodi, arve omanikuks. Seetõttu saab müügitellimuse omanik arvet vaadata.

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

- Veenduge, et atribuudi **Mõõtühik** jaoks oleks olemas nõutav vastendus.
- Veenduge, et üksuse **SalesUnitSymbol** nõutav väärtuskaart oleks rakenduses Supply Chain Management olemas.

    Üksuste **SalesUnitSymbol** ja **Quantity\_UOM** jaoks on määratletud väärtuskaardiga malli väärtus.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

> [!NOTE]
> Väljad **Maksetingimused**, **Veosetingimused**, **Tarnetingimused**, **Saatmisviis** ja **Tarneviis** ei ole vaikevastenduste osa. Nende väljade vastendamiseks peate seadistama väärtuskaardi, mis on kohane neis organisatsioonides olevatele andmetele, mille vahel üksust sünkroonitakse.

Järgmisel joonisel on toodud näide malli vastendusest andmete integratsioonis. 

> [!NOTE]
> Vastendamine näitab, millise välja teave sünkroonitakse rakendusest Sales rakendusse Supply Chain Management.

### <a name="salesinvoiceheader"></a>SalesInvoiceHeader

![Malli vastendamine andmete integratsioonis.](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a>SalesInvoiceLine

![Malli vastendamine andmete integratsioonis.](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>Seotud dokumendid

[Potentsiaalne klient sularahaks](prospect-to-cash.md)

[Rakenduse Sales kontode sünkroonimine otse rakenduse Supply Chain Management klientidega](accounts-template-mapping-direct.md)

[Rakenduse Supply Chain Management toodete sünkroonimine otse rakenduse Sales toodetega](products-template-mapping-direct.md)

[Rakenduse Sales kontaktide sünkroonimine otse rakenduse Supply Chain Management kontaktide või klientidega](contacts-template-mapping-direct.md)

[Müügitellimuste vahetu sünkroonimine rakenduse Sales ja rakenduse Supply Chain Management vahel](sales-order-template-mapping-direct-two-ways.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]