---
title: "Müügitellimuste vahetu sünkroonimine rakenduste Sales ja Finance and Operations vahel"
description: "See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse müügitellimuste sünkroonimiseks rakenduste Microsoft Dynamics 365 for Sales ja Microsoft Dynamics 365 for Finance and Operations vahel."
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2018
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: e26244ffc380291a40edfbd2c2cb5911b0d8b3cb
ms.contentlocale: et-ee
ms.lasthandoff: 03/26/2018

---

# <a name="synchronization-of-sales-orders-directly-between-sales-and-finance-and-operations"></a>Müügitellimuste vahetu sünkroonimine rakenduste Sales ja Finance and Operations vahel

[!INCLUDE [banner](../includes/banner.md)]

See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse müügitellimuste sünkroonimiseks rakenduste Microsoft Dynamics 365 for Sales ja Microsoft Dynamics 365 for Finance and Operations vahel.

## <a name="templates-and-tasks"></a>Mallid ja ülesanded

Saadaolevatele mallidele juurdepääsemiseks avage [PowerApps administreerimiskeskus](https://preview.admin.powerapps.com/dataintegration). Valige **Projektid** ja seejärel paremas ülanurgas **Uus projekt**, et valida avalikud mallid.

Müügitellimuste sünkroonimiseks rakenduste Sales ja Finance and Operations vahel kasutatakse järgmisi malle ja aluseks olevaid ülesandeid.

- **Mallide nimed andmete integratsioonis.** 

    - Müügitellimused (rakendusest Sales rakendusse Fin and Ops) – otse
    - Müügitellimused (rakendusest Fin and Ops rakendusse Sales) – otse

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

Müügitellimused luuakse rakenduses Sales ja sünkroonitakse rakendusega Finance and Operations, kui mallil **Müügitellimused (rakendusest Sales rakendusse Fin and Ops) – otse** põhinevas projektis käivitatakse käsk **Käita projekti**. Saate rakenduses Sales müügitellimusi aktiveerida ja sünkroonida ainult juhul, kui jaotis **Tellimuse tooted** hõlmab ainult väliselt hallatavaid tooteid. Seetõttu ei saa seal olla sissekirjutatud tooteid. Pärast tellimuse aktiveerimist on müügitellimus kasutajaliideses kirjutuskaitstud. Sel ajal tehakse värskendused rakendusest Finance and Operations. Kui müügitellimuse olek on **Kinnitatud**, saab mallil **Müügitellimused (rakendusest Fin and Ops rakendusse Sales) – otse** põhinevat projekti kasutada värskenduste või täitmisoleku sünkroonimiseks rakendusest Finance and Operations rakendusse Sales.

Te ei pea rakenduses Sales tellimusi looma. Võite selle asemel luua uued müügitellimused rakenduses Finance and Operations. Kui müügitellimuse olek on **Kinnitatud**, sünkroonitakse see rakendusega Sales eelmises lõigus kirjeldatud moel.

Malli filtrid aitavad rakenduses Finance and Operations tagada ainult asjakohaste müügitellimuste kaasamise sünkroonimisse.

- Müügitellimuse puhul peavad nii müügitellimuse esitanud klient kui ka arvelduse klient pärinema rakendusest Sales, et nad lisataks sünkroonimisse. Rakenduses Finance and Operations kasutatakse välju **OrderingCustomerIsExternallyMaintained** ja **InvoiceCustomerIsExternallyMaintained** andmeüksustes müügitellimuste filtreerimiseks.
- Rakenduses Finance and Operations olev müügitellimus tuleb kinnitada. Rakendusega Sales sünkroonitakse ainult kõrgema töötlemisolekuga kinnitatud müügitellimused, nt olekuga **Saadetud** või **Arveldatud**.
- Pärast müügitellimuse loomist või muutmist tuleb käitada pakett-töö **Müügi kogusummade arvutamine** rakenduses Finance and Operations. Rakendusega Sales sünkroonitakse vaid need müügitellimused, mille müügi kogusummad on arvutatud.

## <a name="freight-tax"></a>Transpordimaks

Rakendus Sales ei toeta maksu päise tasandil, kuna maksud talletatakse rea tasemel. Selleks et toetada rakendusest Finance and Operatsions pärit maksu (nt transpordimaks) päise tasemel, sünkroonib süsteem rakendusega Sales sissekirjutatud tootena, mille nimetus on **Transpordimaks** ja mis sisaldab maksusummat rakendusest Finance and Operations. Nii saab standardset hinnakalkulatsiooni rakenduses Sales kasutada summade arvutamiseks isegi siis, kui rakenduses Finance and Operations on maks päise tasandil.

## <a name="discount-calculation-and-rounding"></a>Allahindluse arvutamine ja ümardamine

Rakenduse Sales allahindluse arvutamise mudel erineb rakenduse Finance and Operations allahindluse arvutamise mudelist. Rakenduses Finance and Operations võib müügirea lõplik allahindluse summa olla allahindluse summade ja allahindluse protsentide kombinatsiooni tulemus. Kui lõplik allahindluse summa jagatakse real oleva kogusega, võib ilmneda ümardamine. Ümardamist ei võeta aga arvesse, kui ümardatav ühikupõhise allahindluse summa sünkroonitakse rakendusega Sales. Selleks et rakenduse Finance and Operations müügirea kogu allahindluse summa rakendusega Sales õigesti sünkroonida, tuleb kogusumma sünkroonida rea kogusega jagamata. Seetõttu peate rakenduses Sales määratlema suvandi **Allahindluse arvutamise meetod** väärtuseks **Rea kaup**.

Kui müügitellimus sünkroonitakse rakendusest Sales rakendusega Finance and Operations, kasutatakse terve rea allahindluse summat. Kuna rakenduses Finance and Operations pole ühtegi välja, millele saab salvestada rea kogu allahindluse summa, jagatakse summa kogusega ja salvestatakse väljale **Rea allahindlus**. Selles jaotises esinev ümardamine talletatakse müügirea väljale **Müügitasud**.

### <a name="example"></a>Näide

**Sünkroonimine rakendusest Sales rakendusse Finance and Operations**

- **Sales:** kogus = 3, allahindlus rea kohta = 10.00 USA dollarit
- **Finance and Operations:** kogus = 3, rea allahindluse summa = 3.33 USA dollarit, müügitasu= –0.01 USA dollarit 

**Sünkroonimine rakendusest Finance and Operations rakendusse Sales**

- **Finance and Operations:** kogus = 3, rea allahindluse summa = 3.33 USA dollarit, müügitasu= –0.01 USA dollarit
- **Sales:** kogus = 3, allahindlus rea kohta = (3 × 3.33) + 0.01 = 10.00 USA dollarit

## <a name="prospect-to-cash-solution-for-sales"></a>Lahendus Potentsiaalne klient sularahaks rakendusele Sales

Üksusele **Tellimus** lisati uued väljad ja need kuvatakse järgmisel lehel.

- **Hallatakse väliselt**: seadke see valik väärtusele **Jah**, kui tellimus tuleb rakendusest Finance and Operations.
- **Töötlemise olek**: sellel väljal kuvatakse tellimuse töötlemise olek rakenduses Finance and Operations. Saadaval on järgmised väärtused:

    - **Mustand**: vaikeolek rakenduses Sales tellimuse loomisel. Rakenduses Sales saab muuta ainult selle töötlemisolekuga tellimusi.
    - **Aktiivne**: olek pärast rakenduses Sales tellimuse aktiveerimist nupuga **Aktiveeri**.
    - **Kinnitatud**
    - **Saateleht**
    - **Arveldatud**
    - **Komplekteeritud**
    - **Osaliselt komplekteeritud**
    - **Osaliselt pakitud**
    - **Välja saadetud**
    - **Osaliselt tarnitud**
    - **Osaliselt arvele kantud**
    - **Tühistatud**

Sätet **Sisaldab ainult väliselt hallatavaid tooteid** kasutatakse tellimuse aktiveerimise ajal, et jälgida järjepidevalt, kas müügitellimus sisaldab ainult väliselt hallatavaid tooteid. Kui müügitellimus sisaldab ainult väliselt hallatavaid tooteid, hallatakse neid rakenduses Finance and Operations. See säte aitab tagada, et te ei aktiveeriks ega püüaks sünkroonida müügitellimuse ridu, mis hõlmavad rakenduse Finance and Operations jaoks tundmatuid tooteid.

Nupud **Arve koostamine**, **Tellimuse tühistamine**, **Ümberarvutamine**, **Toodete toomine** ja **Aadressi otsimine** lehel **Müügitellimus** on väliselt hallatavate tellimuste puhul peidetud, kuna arved luuakse rakenduses Finance and Operations ja sünkroonitakse rakendusega Sales. Neid tellimusi ei saa muuta, kuna müügitellimuse teave sünkroonitakse pärast aktiveerimist rakendusest Finance and Operations.

Müügitellimuse olek on ka edaspidi **Aktiivne**, et rakendusest Finance and Operations pärit muudatused saaksid liikuda rakenduses Sales olevasse müügitellimusse. Määrake selle käitumise juhtimiseks andmeintegratsiooni projektis vaikeväärtuse **Olekukood \[[Olek]\]** väärtuseks **Aktiivne**.

## <a name="preconditions-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

Enne müügitellimuste sünkroonimist on oluline värskendada süsteemides järgmisi sätteid.

### <a name="setup-in-sales"></a>Seadistus rakenduses Sales

- Veenduge, et load oleks seadistatud töörühma jaoks, kuhu rakenduses Sales häälestatud ühendusest pärit kasutaja on määratud. Demoandmete kasutamisel on kasutajal tavaliselt administraatori juurdepääs, kuid töörühmal mitte. Kui töörühmal ei ole administraatorijuurdepääsu, ilmub andmete integratsioonis projekti käivitamisel veateade, mis annab teada, et peamine töörühm puudub.

    Valige jaotisest **Sätted** &gt; **Turve** &gt; **Töörühmad** asjakohane töörühm, valige käsk **Halda rolle** ja valige soovitud lubadega roll, näiteks **Süsteemiadministraator**.

- Et tagada allahindluste õige arvutamine rakendustes Sales ja Finance and Operations tuleb väli **Allahindluse arvutamise meetod** seada väärtusele **Rea kaup**.
- Avage jaotis **Sätted** &gt; **Administreerimine** &gt; **Süsteemisätted** &gt; **Sales** ja veenduge, et kasutusel oleks järgmised sätted.

    - Suvand **Kasuta süsteemi hinna arvutamise süsteemi** on seatud väärtusele **Jah**.
    - Väli **Allahindluse arvutamise meetod** on seatud väärtusele **Rea kaup**.

### <a name="setup-in-finance-and-operations"></a>Seadistus rakenduses Finance and Operations

- Avage jaotis **Müük ja turundus** &gt; **Perioodilised ülesanded** &gt; **Müügi kogusummade arvutamine** ja seadistage töö pakett-tööna. Valige suvandi **Müügitellimuste kogusummade arvutamine** väärtuseks **Jah**. See toiming on oluline, kuna Salesiga sünkroonitakse ainult need müügitellimused, mille müügi kogusummad on arvutatud. Pakett-töö sagedus tuleks sobitada müügitellimuse sünkroonimise sagedusega.

### <a name="setup-in-the-sales-orders-sales-to-fin-and-ops---direct-data-integration-project"></a>Seadistamine müügitellimustes (rakendusest Sales rakendusse Fin and Ops) – andmete integratsiooni otseprojekt

- Veenduge, et atribuutide **Shipto\_country** – **DeliveryAddressCountryRegionISOCode** vahel oleks olemas nõutav vastendamine. Väärtuste kaardil võite määrata vaikesätteks tühja väärtuse, et te ei peaks riigisiseste tellimuste puhul riiki sisestama. Valige vasakul säte „Tühi” ja paremal pool soovitud riik või regioon.

    Malli väärtus on väärtuste kaart, kus on vastendatud mitu riiki või regiooni ja mille puhul „Tühi” = Ameerika Ühendriigid.

### <a name="setup-in-the-sales-orders-fin-and-ops-to-sales---direct-data-integration-project"></a>Seadistamine müügitellimustes (rakendusest Fin and Ops rakendusse Sales) – andmete integratsiooni otseprojekt

#### <a name="salesheader-task"></a>Ülesanne SalesHeader

- Hinnakiri on vajalik tellimuste koostamiseks rakenduses Sales. Värskendage üksuse **pricelevelid.name \[Hinnakirja nimi\]** väärtuskaarti hinnakirja alusel, mida kasutatakse rakenduses Sales valuuta kohta. Saate ühe valuuta puhul kasutada vaikehinnakirja. Kui teil on mitmes valuutas hinnakirju, saate kasutada väärtuskaarti.

    Üksuse **pricelevelid.name \[Hinnakirja nimi\]** malli vaikeväärtus on **USA CRM-i teenus (näidis)**.

#### <a name="salesline-task"></a>Ülesanne SalesLine

- Veenduge, et üksuse **SalesUnitSymbol** nõutav väärtuskaart oleks rakenduses Finance and Operations olemas.
- Veenduge, et rakenduses Sales oleks nõutud ühikud määratletud.

    Üksuste **SalesUnitSymbol** ja **oumid.name** jaoks on määratletud väärtuskaardiga malli väärtus.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

> [!NOTE]
> Väljad **Maksetingimused**, **Veosetingimused**, **Tarnetingimused**, **Saatmisviis** ja **Tarneviis** ei ole vaikevastenduste osa. Nende väljade vastendamiseks peate seadistama väärtuskaardi, mis on kohane neis organisatsioonides olevatele andmetele, mille vahel üksust sünkroonitakse.

Järgmisel joonisel on toodud näide malli vastendusest andmete integratsioonis.

> [!NOTE]
> Vastendamine näitab, millise välja teave sünkroonitakse rakendusest Sales rakendusse Finance and Operations või vastupidi.

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderheader"></a>Müügitellimused (rakendusest Fin and Ops rakendusse Sales) – otse: OrderHeader

[![Malli vastendamine andmete integratsioonis](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderline"></a>Müügitellimused (rakendusest Fin and Ops rakendusse Sales) – otse: OrderLine

[![Malli vastendamine andmete integratsioonis](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderheader"></a>Müügitellimused (rakendusest Sales rakendusse Fin and Ops) – otse: OrderHeader

[![Malli vastendamine andmete integratsioonis](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderline"></a>Müügitellimused (rakendusest Sales rakendusse Fin and Ops) – otse: OrderLine

[![Malli vastendamine andmete integratsioonis](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>Seotud dokumendid

[Potentsiaalne klient sularahaks](prospect-to-cash.md)

