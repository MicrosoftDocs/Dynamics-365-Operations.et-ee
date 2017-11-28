---
title: "Rakenduse Finance and Operations müügitellimuse päiste ja ridade vahetu sünkroonimine rakendusega Sales"
description: "See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse müügitellimuse päiste ja ridade vahetuks sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition rakendusse Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
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
ms.openlocfilehash: cc0be50552ae680ba5291e72b7c482ee67e1e70e
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Rakenduse Finance and Operations müügitellimuse päiste ja ridade vahetu sünkroonimine rakendusega Sales

[!include[banner](../includes/banner.md)]

See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse müügitellimuse päiste ja ridade vahetuks sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition rakendusse Microsoft Dynamics 365 for Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Andmevoog lahenduses Potentsiaalne klient sularahaks

Lahendus Potentsiaalne klient sularahaks kasutab andmete integreerimise funktsiooni andmete sünkroonimiseks rakenduste Finance and Operations ja Sales vahel. Andmete integratsiooniga saadaolevad lahenduse Potentsiaalne klient sularahaks mallid võimaldavad kontode, kontaktide, toodete, müügipakkumiste, müügitellimuste ja müügiarvete andmete liikumist rakenduste Finance, Operations ja Sales. Järgmine illustratsioon näitab, kuidas sünkroonitakse andmeid rakenduste Finance and Operations ja Sales vahel.

[![Andmevoog lahenduses Potentsiaalne klient sularahaks](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Mallid ja ülesanded

Saadaolevatele mallidele juurdepääsemiseks avage [PowerApps administreerimiskeskus](https://preview.admin.powerapps.com/dataintegration). Valige **Projektid** ja seejärel paremas ülanurgas **Uus projekt**, et valida avalikud mallid.

Müügitellimuste päiste ja ridade sünkroonimiseks rakendusest Finance and Operations rakendusse Sales kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

- **Andmete integratsioon malli nimi:** Müügitellimused (rakendusest Fin and Ops rakendusse Sales) – otse
- **Ülesannete nimed andmete integratsiooni projektis.**

    - OrderHeader
    - OrderLine

Enne müügiarvete päiste ja ridade sünkroonimist on nõutavad järgmised sünkroonimisülesanded.

- Tooted (rakendusest Sales rakendusse Fin and Ops) – otse
- Kontod (rakendusest Sales rakendusse Fin and Ops) – otse (kui on kasutusel)
- Kontaktid klientideks (rakendusest Sales rakendusse Fin and Ops) – otse (kui see on kasutusel)

## <a name="entity-set"></a>Üksuste komplekt

| Finance and Operations  | Müük             |
|-------------------------|-------------------|
| CDS-i müügitellimuste päised CDS | SalesOrders       |
| CDS-i müügitellimuse read   | SalesOrderDetails |

## <a name="entity-flow"></a>Üksuse voog

Müügitellimused luuakse rakenduses Finance and Operations ja sünkroonitakse rakendusega Sales.

Malli filtrid tagavad ainult asjakohaste müügitellimuste kaasamise sünkroonimisse.

- Müügitellimuse puhul peavad nii müügitellimuse esitanud klient kui ka arvelduse klient pärinema rakendusest Sales, et nad lisataks sünkroonimisse. Rakenduses Finance and Operations kasutatakse välju **OrderingCustomerIsExternallyMaintained** ja **InvoiceCustomerIsExternallyMaintained** andmeüksustes sünkroonimise jälgimiseks.
- Rakenduses Finance and Operations olev müügitellimus tuleb kinnitada. Rakendusega Sales sünkroonitakse ainult kõrgema töötlemisolekuga kinnitatud müügitellimused, nt olekuga **Saadetud** või **Arveldatud**.
- Pärast müügitellimuse loomist või muutmist tuleb käitada pakett-töö **Müügi kogusummade arvutamine** rakenduses Finance and Operations. Rakendusega Sales sünkroonitakse vaid need müügitellimused, mille müügi kogusummad on arvutatud.

> [!NOTE]
> Müügitellimuse päises olevate tasudega seotud maksu ei arvestata praegu Finance and Operationsi ja Salesi sünkroonimisel. Sales ei toeta maksuteavet päise tasandil. Sünkroonimine hõlmab aga makse, mis on seotud rea tasemel tasudega.

## <a name="prospect-to-cash-solution-for-sales"></a>Lahendus Potentsiaalne klient sularahaks rakendusele Sales

Üksusele **Tellimus** lisati uued väljad ja need kuvatakse järgmisel lehel.

- **Hallatakse väliselt**: seadke see valik väärtusele **Jah**, kui tellimus tuleb rakendusest Finance and Operations.
- **Töötlemise olek**: sellel väljal kuvatakse tellimuse töötlemise olek rakenduses Finance and Operations. Saadaval on järgmised väärtused:

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

Sätet **Sisaldab ainult väliselt hallatavaid tooteid** kasutatakse teistes müügitellimuse stsenaariumides (näiteks rakendusest Sales rakendusse Finance and Operations sünkroonimisel), et jälgida, kas müügitellimus koosneb täielikult väliselt hallatavatest toodetest. Kui müügitellimus sisaldab ainult väliselt hallatavaid tooteid, hallatakse neid rakenduses Finance and Operations. See säte aitab tagada, et te ei püüaks sünkroonida müügitellimuse ridu, mis hõlmavad rakenduse Finance and Operations jaoks tundmatuid tooteid.

Nupud **Arve koostamine**, **Tellimuse tühistamine**, **Ümberarvutamine**, **Toodete toomine** ja **Aadressi otsimine** lehel **Müügitellimus** on väliselt hallatavate tellimuste puhul peidetud, kuna arved luuakse rakenduses Finance and Operations ja sünkroonitakse rakendusega Sales. Tellimuse lehte ei saa muuta, kuna müügitellimuse teave sünkroonitakse rakendusest Finance and Operations.

Müügitellimuse olek on ka edaspidi **Aktiivne**, et rakendusest Finance and Operations pärit muudatused saaksid liikuda rakenduses Sales olevasse müügitellimusse. Määrake selle käitumise juhtimiseks andmeintegratsiooni projektis vaikeväärtuse **Olekukood \[[Olek]\]** väärtuseks **Aktiivne**.

## <a name="preconditions-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

Enne müügitellimuste sünkroonimist on oluline värskendada süsteemides järgmisi sätteid.

### <a name="setup-in-sales"></a>Seadistus rakenduses Sales

- Veenduge, et load oleks seadistatud töörühma jaoks, kuhu rakenduses Sales häälestatud ühendusest pärit kasutaja on määratud. Demoandmete kasutamisel on kasutajal tavaliselt administraatori juurdepääs, kuid töörühmal mitte. Kui töörühmal ei ole administraatorijuurdepääsu, ilmub andmete integratsioonis projekti käivitamisel veateade, mis annab teada, et peamine töörühm puudub.

    Valige jaotisest **Sätted** > **Turve** > **Töörühmad** asjakohane töörühm, valige käsk **Halda rolle** ja valige soovitud lubadega roll, näiteks **Süsteemiadministraator**.

- Avage jaotis **Sätted** > **Administreerimine** > **Süsteemisätted** > **Sales** ja veenduge, et kasutusel oleks järgmised sätted.

    - Suvand **Kasuta süsteemi hinna arvutamise süsteemi** on seatud väärtusele **Jah**.
    - Väli **Allahindluse arvutamise meetod** on seatud väärtusele **Rea kaup**.

### <a name="setup-in-finance-and-operations"></a>Seadistus rakenduses Finance and Operations

Avage jaotis **Müük ja turundus** > **Perioodilised ülesanded** > **Müügi kogusummade arvutamine** ja seadistage töö pakett-tööna. Valige suvandi **Müügitellimuste kogusummade arvutamine** väärtuseks **Jah**. See toiming on oluline, kuna Salesiga sünkroonitakse ainult need müügitellimused, mille müügi kogusummad on arvutatud. Pakett-töö sagedus tuleks sobitada müügitellimuse sünkroonimise sagedusega.

### <a name="setup-in-the-data-integration-project"></a>Seadistus andmeintegratsiooni projektis

#### <a name="salesheader-task"></a>Ülesanne SalesHeader

- Veenduge, et üksuste **InvoiceCountryRegionID** ja **BillingAddress\_Country** ning **DeliveryCountryRegionID** ja **DeliveryAddress\_Country** vahel oleks olemas vajalik vastendus.

    Malli väärtus on väärtuste kaart, kus on vastendatud mitu riiki või regiooni.

- Hinnakiri on vajalik tellimuste koostamiseks rakenduses Sales. Värskendage üksuse **pricelevelid.name \[Hinnakirja nimi\]** väärtuskaarti hinnakirja alusel, mida kasutatakse rakenduses Sales valuuta kohta. Saate ühe valuuta puhul kasutada vaikehinnakirja. Kui teil on mitmes valuutas hinnakirju, saate kasutada väärtuskaarti.

    Üksuse **pricelevelid.name \[Hinnakirja nimi\]** malli vaikeväärtus on **USA CRM-i teenus (näidis)**.

#### <a name="salesline-task"></a>Ülesanne SalesLine

- Veenduge, et üksuste **DeliveryCountryRegionId** ja **DeliveryAddress\_Country** vahel oleks olemas nõutav vastendamine.

    Malli väärtus on väärtuste kaart, kus on vastendatud mitu riiki või regiooni.

- Veenduge, et üksuse **SalesUnitSymbol** nõutav väärtuskaart oleks rakenduses Finance and Operations olemas.

    Üksuste **SalesUnitSymbol** ja **Quantity\_UOM** jaoks on määratletud väärtuskaardiga malli väärtus.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

> [!NOTE]
> Väljad **Maksetingimused**, **Veosetingimused**, **Tarnetingimused**, **Saatmisviis** ja **Tarneviis** ei ole vaikevastenduste osa. Nende väljade vastendamiseks peate seadistama väärtuskaardi, mis on kohane neis organisatsioonides olevatele andmetele, mille vahel üksust sünkroonitakse.

Järgmisel joonisel on toodud näide malli vastendusest andmete integratsioonis. 

> [!NOTE]
> Vastendamine näitab, millise välja teave sünkroonitakse rakendusest Sales rakendusse Finance and Operations.

### <a name="orderheader"></a>OrderHeader

![Malli vastendamine andmeintegraatoris](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a>OrderLine

![Malli vastendamine andmeintegraatoris](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>Seotud dokumendid

[Potentsiaalne klient sularahaks](prospect-to-cash.md)

[Rakenduse Sales kontode vahetu sünkroonimine rakenduse Finance and Operations klientidega](accounts-template-mapping-direct.md)

[Rakenduse Finance and Operations toodete vahetu sünkroonimine rakenduse Sales toodetega](products-template-mapping-direct.md)

[Rakenduse Sales kontaktide vahetu sünkroonimine rakenduse Finance and Operations kontaktide või klientidega](contacts-template-mapping-direct.md)

[Rakenduse Finance and Operations müügiarve päiste ja ridade vahetu sünkroonimine rakendusega Sales](sales-invoice-template-mapping-direct.md)




