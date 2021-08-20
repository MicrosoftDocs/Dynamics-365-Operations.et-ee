---
title: Müügitellimuste vahetu sünkroonimine rakenduse Sales ja rakenduse Supply Chain Management vahel
description: Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse müügitellimuste sünkroonimise käivitamiseks rakenduste Dynamics 365 Sales ja Dynamics 365 Supply Chain Management vahel.
author: ChristianRytt
ms.date: 05/09/2019
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
ms.openlocfilehash: 9e95ba361bddf4e43b205fe580bb6f4a91dd88248a0c059ad65e66ef07de83c0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753224"
---
# <a name="synchronization-of-sales-orders-directly-between-sales-and-supply-chain-management"></a>Müügitellimuste vahetu sünkroonimine rakenduse Sales ja rakenduse Supply Chain Management vahel

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse müügitellimuste sünkroonimise käivitamiseks rakenduste Dynamics 365 Sales ja Dynamics 365 Supply Chain Management vahel.

## <a name="data-flow-in-prospect-to-cash"></a>Andmevoog lahenduses Potentsiaalne klient sularahaks

Lahendus Potentsiaalne klient sularahaks kasutab andmete integreerimise funktsiooni andmete sünkroonimiseks rakenduste Supply Chain Management ja Sales vahel. Andmeintegratsiooni funktsiooniga saadaolevad Prospect to cash mallid võimaldavad andmevahetust kontode, kontaktide, toodete, müügihindade, müügitellimuste ja müügiarvete kohta Supply Chain Managementi ja Salesi vahel. Järgmine illustratsioon näitab, kuidas sünkroonitakse andmeid rakenduste Supply Chain Management ja Sales vahel.

[![Andmevoog lahenduses Potentsiaalne klient sularahaks.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Mallid ja ülesanded

Saadaolevatele mallidele juurdepääsemiseks avage [Power Apps administreerimiskeskus](https://preview.admin.powerapps.com/dataintegration). Valige **Projektid** ja seejärel paremas ülanurgas **Uus projekt**, et valida avalikud mallid.

Müügitellimuste sünkroonimiseks rakenduste Sales ja Supply Chain Management vahel kasutatakse järgmisi malle ja aluseks olevaid ülesandeid.

- **Mallide nimed andmete integratsioonis.** 

    - Müügitellimused (rakendusest Sales rakendusse Supply Chain Management) – otse
    - Müügitellimused (Supply Chain Managementist Salesi) – otse

- **Ülesannete nimed andmete integratsiooni projektis.**

    - OrderHeader
    - OrderLine

Enne müügiarvete päiste ja ridade sünkroonimist on nõutavad järgmised sünkroonimisülesanded.

- Tooted (rakendusest Supply Chain Management rakendusse Sales) - otse
- Kontod (rakendusest Sales rakendusse Supply Chain Management) - otse (kui kasutatakse)
- Kontaktid klientidesse (Salesist Supply Chain Managementi) - otse (kui kasutatakse)

## <a name="entity-set"></a>Üksuste komplekt

| Supply Chain Management  | Müük             |
|-------------------------|-------------------|
| Dataverse’i müügitellimuse päised | SalesOrders       |
| Dataverse’i müügitellimuse read   | SalesOrderDetails |

## <a name="entity-flow"></a>Üksuse voog

Müügitellimused luuakse rakenduses Sales ja sünkroonitakse rakendusega Supply Chain Management, kui mallil **Müügitellimused (rakendusest Sales rakendusse Supply Chain Management) – otse** põhinevas projektis käivitatakse käsk **Käita projekti**. Saate rakenduses Sales müügitellimusi aktiveerida ja sünkroonida ainult juhul, kui jaotis **Tellimuse tooted** hõlmab ainult väliselt hallatavaid tooteid. Seetõttu ei saa seal olla sissekirjutatud tooteid. Pärast tellimuse aktiveerimist on müügitellimus kasutajaliideses kirjutuskaitstud. Sel ajal tehakse värskendused rakendusest Supply Chain Management. Kui müügitellimuse olek on **Kinnitatud**, saab mallil **Müügitellimused (rakendusest Supply Chain Management rakendusse Sales) – otse** põhinevat projekti kasutada värskenduste või täitmisoleku sünkroonimiseks rakendusest Supply Chain Management rakendusse Sales.

Te ei pea rakenduses Sales tellimusi looma. Võite selle asemel luua uued müügitellimused rakenduses Supply Chain Management. Kui müügitellimuse olek on **Kinnitatud**, sünkroonitakse see rakendusega Sales eelmises lõigus kirjeldatud moel.

Malli filtrid aitavad rakenduses Supply Chain Management tagada ainult asjakohaste müügitellimuste kaasamise sünkroonimisse.

- Müügitellimuse puhul peavad nii müügitellimuse esitanud klient kui ka arvelduse klient pärinema rakendusest Sales, et nad lisataks sünkroonimisse. Rakenduses Supply Chain Management kasutatakse veerge **OrderingCustomerIsExternallyMaintained** ja **InvoiceCustomerIsExternallyMaintained** andmetabelitest müügitellimuste filtreerimiseks.
- Rakenduses Supply Chain Management olev müügitellimus tuleb kinnitada. Rakendusega Sales sünkroonitakse ainult kõrgema töötlemisolekuga kinnitatud müügitellimused, nt olekuga **Saadetud** või **Arveldatud**.
- Pärast müügitellimuse loomist või muutmist tuleb käitada pakett-töö **Müügi kogusummade arvutamine** rakenduses Supply Chain Management. Rakendusega Sales sünkroonitakse vaid need müügitellimused, mille müügi kogusummad on arvutatud.

## <a name="freight-tax"></a>Transpordimaks

Rakendus Sales ei toeta maksu päise tasandil, kuna maksud talletatakse rea tasemel. Selleks et toetada rakendusest Supply Chain Management pärit maksu (nt transpordimaks) päise tasemel, sünkroonib süsteem rakendusega Sales sissekirjutatud tootena, mille nimetus on **Transpordimaks** ja mis sisaldab maksusummat rakendusest Supply Chain Management. Nii saab standardset hinnakalkulatsiooni rakenduses Sales kasutada summade arvutamiseks isegi siis, kui rakenduses Supply Chain Management on maks päise tasandil.

## <a name="discount-calculation-and-rounding"></a>Allahindluse arvutamine ja ümardamine

Rakenduse Sales allahindluse arvutamise mudel erineb rakenduse Supply Chain Management allahindluse arvutamise mudelist. Rakenduses Supply Chain Management võib müügirea lõplik allahindluse summa olla allahindluse summade ja allahindluse protsentide kombinatsiooni tulemus. Kui lõplik allahindluse summa jagatakse real oleva kogusega, võib ilmneda ümardamine. Ümardamist ei võeta aga arvesse, kui ümardatav ühikupõhise allahindluse summa sünkroonitakse rakendusega Sales. Selleks et rakenduse Supply Chain Management müügirea kogu allahindluse summa rakendusega Sales õigesti sünkroonida, tuleb kogusumma sünkroonida rea kogusega jagamata. Seetõttu peate rakenduses Sales määratlema suvandi **Allahindluse arvutamise meetod** väärtuseks **Rea kaup**.

Kui müügitellimus sünkroonitakse rakendusest Sales rakendusega Supply Chain Management, kasutatakse terve rea allahindluse summat. Kuna rakenduses Supply Chain Management pole ühtegi välja, millele saab salvestada rea kogu allahindluse summa, jagatakse summa kogusega ja salvestatakse väljale **Rea allahindlus**. Selles jaotises esinev ümardamine talletatakse müügirea väljale **Müügitasud**.

### <a name="example"></a>Näide

**Sünkroonimine Salesist Supply Chain Managementi**

- **Sales:** kogus = 3, allahindlus rea kohta = 10.00 USA dollarit
- **Supply Chain Management:** kogus = 3, rea allahindluse summa = $3.33, müügisumma =-$0.01 

**Sünkroonimine rakendusest Supply Chain Management rakendusse Sales**

- **Supply Chain Management:** kogus = 3, rea allahindluse summa = $3.33, müügisumma =-$0.01
- **Sales:** kogus = 3, allahindlus rea kohta = (3 × 3.33) + 0.01 = 10.00 USA dollarit

## <a name="prospect-to-cash-solution-for-sales"></a>Lahendus Potentsiaalne klient sularahaks rakendusele Sales

Tabelile **Tellimus** lisati uued veerud ja need kuvatakse lehel:

- **Hallatakse väliselt**: seadke see valik väärtusele **Jah**, kui tellimus tuleb rakendusest Supply Chain Management.
- **Töötlemise olek**: selles veerus kuvatakse tellimuse töötlemise olek rakenduses Supply Chain Management. Saadaval on järgmised väärtused:

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

Sätet **Sisaldab ainult väliselt hallatavaid tooteid** kasutatakse tellimuse aktiveerimise ajal, et jälgida järjepidevalt, kas müügitellimus sisaldab ainult väliselt hallatavaid tooteid. Kui müügitellimus sisaldab ainult väliselt hallatavaid tooteid, hallatakse neid rakenduses Supply Chain Management. See säte aitab tagada, et te ei aktiveeriks ega püüaks sünkroonida müügitellimuse ridu, mis hõlmavad rakenduse Supply Chain Management jaoks tundmatuid tooteid.

Nupud **Arve koostamine**, **Tellimuse tühistamine**, **Ümberarvutamine**, **Toodete toomine** ja **Aadressi otsimine** lehel **Müügitellimus** on väliselt hallatavate tellimuste puhul peidetud, kuna arved luuakse rakenduses Supply Chain Management ja sünkroonitakse rakendusega Sales. Neid tellimusi ei saa muuta, kuna müügitellimuse teave sünkroonitakse pärast aktiveerimist rakendusest Supply Chain Management.

Müügitellimuse olek on ka edaspidi **Aktiivne**, et rakendusest Supply Chain Management pärit muudatused saaksid liikuda rakenduses Sales olevasse müügitellimusse. Määrake selle käitumise juhtimiseks andmeintegratsiooni projektis vaikeväärtuse **Olekukood \[[Olek]\]** väärtuseks **Aktiivne**.

## <a name="preconditions-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

Enne müügitellimuste sünkroonimist on oluline värskendada süsteemides järgmisi sätteid.

### <a name="setup-in-sales"></a>Seadistus rakenduses Sales

- Veenduge, et load oleks seadistatud töörühma jaoks, kuhu rakenduses Sales häälestatud ühendusest pärit kasutaja on määratud. Demoandmete kasutamisel on kasutajal tavaliselt administraatori juurdepääs, kuid töörühmal mitte. Kui töörühmal ei ole administraatorijuurdepääsu, ilmub andmete integratsioonis projekti käivitamisel veateade, mis annab teada, et peamine töörühm puudub.

    Valige jaotisest **Sätted** &gt; **Turve** &gt; **Töörühmad** asjakohane töörühm, valige käsk **Halda rolle** ja valige soovitud lubadega roll, näiteks **Süsteemiadministraator**.

- Et tagada allahindluste õige arvutamine rakendustes Sales ja Supply Chain Management tuleb väli **Allahindluse arvutamise meetod** seada väärtusele **Rea kaup**.
- Avage jaotis **Sätted** &gt; **Administreerimine** &gt; **Süsteemisätted** &gt; **Sales** ja veenduge, et kasutusel oleks järgmised sätted.

    - Suvand **Kasuta süsteemi hinna arvutamise süsteemi** on seatud väärtusele **Jah**.
    - Veerg **Allahindluse arvutamise meetod** on seatud väärtusele **Rea kaup**.

### <a name="setup-in-supply-chain-management"></a>Seadistamine rakenduses Supply Chain Management

- Avage jaotis **Müük ja turundus** &gt; **Perioodilised ülesanded** &gt; **Müügi kogusummade arvutamine** ja seadistage töö pakett-tööna. Valige suvandi **Müügitellimuste kogusummade arvutamine** väärtuseks **Jah**. See toiming on oluline, kuna Salesiga sünkroonitakse ainult need müügitellimused, mille müügi kogusummad on arvutatud. Pakett-töö sagedus tuleks sobitada müügitellimuse sünkroonimise sagedusega.

Kui kasutate ka töötellimuse integratsiooni, peate seadistama müügiallika. Müügiallikat kasutatakse, et eristada müügitellimusi rakendusest Supply Chain Management, mis on loodud rakenduse Field Service töökäskudest. Kui müügitellimuse müügiallika tüübiks on **Töökäsu integratsioon**, kuvatakse müügitellimuse päises väli **Välise töö tellimuse olek**. Lisaks aitab müügiallikas tagada, et rakenduse Field Service töökäskudest loodud müügitellimused filtreeritakse välja müügitellimuse sünkroonimisel rakendusest Supply Chain Management rakendusse Field Service.

1. Avage **Müük ja turundus** \> **Seadistus** \> **Müügitellimused** \> **Müügiallikas**.
2. Uue müügiallika loomiseks valige **Uus**.
3. Sisestage veerus **Müügiallikas** müügiallika nimi, näiteks **Müügitellimus**.
4. Sisestage veergu **Kirjeldus** kirjeldus, näiteks **Müügitellimus müügist**.
5. Valige märkeruut **Päritolu tüübi määramine**.
6. Seadke veeru **Müügi päritolu tüüp** väärtuseks **Müügitellimuse integratsioon**.
7. Valige käsk **Salvesta**.

### <a name="setup-in-the-sales-orders-sales-to-supply-chain-management---direct-data-integration-project"></a>Seadistamine müügitellimustes (rakendusest Sales rakendusse Supply Chain Management) – andmete integratsiooni otseprojekt

- Veenduge, et atribuutide **Shipto\_country** – **DeliveryAddressCountryRegionISOCode** vahel oleks olemas nõutav vastendamine. Väärtuste kaardil võite määrata vaikesätteks tühja väärtuse, et te ei peaks riigisiseste tellimuste puhul riiki sisestama. Valige vasakul säte „Tühi” ja paremal pool soovitud riik või regioon.

    Malli väärtus on väärtuste kaart, kus on vastendatud mitu riiki või regiooni ja mille puhul „Tühi” = Ameerika Ühendriigid.

### <a name="setup-in-the-sales-orders-supply-chain-management-to-sales---direct-data-integration-project"></a>Seadistamine müügitellimustes (rakendusest Supply Chain Management rakendusse Sales) – andmete integratsiooni otseprojekt

#### <a name="salesheader-task"></a>Ülesanne SalesHeader

- Hinnakiri on vajalik tellimuste koostamiseks rakenduses Sales. Värskendage üksuse **pricelevelid.name \[Hinnakirja nimi\]** väärtuskaarti hinnakirja alusel, mida kasutatakse rakenduses Sales valuuta kohta. Saate ühe valuuta puhul kasutada vaikehinnakirja. Kui teil on mitmes valuutas hinnakirju, saate kasutada väärtuskaarti.

    Üksuse **pricelevelid.name \[Hinnakirja nimi\]** malli vaikeväärtus on **USA CRM-i teenus (näidis)**.

#### <a name="salesline-task"></a>Ülesanne SalesLine

- Veenduge, et üksuse **SalesUnitSymbol** nõutav väärtuskaart oleks rakenduses Supply Chain Management olemas.
- Veenduge, et rakenduses Sales oleks nõutud ühikud määratletud.

    Üksuste **SalesUnitSymbol** ja **oumid.name** jaoks on määratletud väärtuskaardiga malli väärtus.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

> [!NOTE]
> Veerud **Maksetingimused**, **Veosetingimused**, **Tarnetingimused**, **Saatmisviis** ja **Tarneviis** ei ole vaikevastenduste osa. Nende veergude vastendamiseks peate seadistama väärtuskaardi, mis on kohane neis organisatsioonides olevatele andmetele, mille vahel tabelit sünkroonitakse.

Järgmisel joonisel on toodud näide malli vastendusest andmete integratsioonis.

> [!NOTE]
> Vastendamine näitab, millise veeru teave sünkroonitakse rakendusest Sales rakendusse Supply Chain Management või vastupidi.

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderheader"></a>Müügitellimused (Supply Chain Managementist Salesi) – otse: OrderHeader

[![Malli vastendamine andmete integratsioonis.](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderline"></a>Müügitellimused (Supply Chain Managementist Salesi) - otse: OrderLine

[![Malli vastendamine andmete integratsioonis.](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderheader"></a>Müügitellimused (Salesist Supply Chain Managementi) – otse: OrderHeader

[![Malli vastendamine andmete integratsioonis.](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderline"></a>Müügitellimused (Salesist Supply Chain Managementi) – otse: OrderLine

[![Malli vastendamine andmete integratsioonis.](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>Seotud dokumendid

[Potentsiaalne klient sularahaks](prospect-to-cash.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]