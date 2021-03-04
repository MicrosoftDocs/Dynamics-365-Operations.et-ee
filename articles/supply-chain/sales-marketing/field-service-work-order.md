---
title: Sünkroonige rakenduse Field Service töötellimused rakenduse Supply Chain Management müügitellimustega
description: See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse rakenduse Field Service töökäskude sünkroonimiseks rakenduse Supply Chain Management müügitellimustega.
author: ChristianRytt
manager: tfehr
ms.date: 04/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: d8051e21c731213e2d74ab6eeb80c239ca9932e6
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528919"
---
# <a name="synchronize-work-orders-in-field-service-to-sales-orders-in-supply-chain-management"></a>Sünkroonige rakenduse Field Service töötellimused rakenduse Supply Chain Management müügitellimustega

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse projekti numbriga töökäskude sünkroonimiseks rakendusest Dynamics 365 Field Service müügitellimusse rakenduses Dynamics 365 Supply Chain Management.

[![Äriprotsesside sünkroniseerimine rakenduste Supply Chain Management ja Field Service vahel](./media/field-service-integration.png)](./media/field-service-integration.png)


## <a name="templates-and-tasks"></a>Mallid ja ülesanded

Järgmisi malle ja aluseks olevaid ülesandeid kasutatakse rakenduse Field Service töökäskude rakenduse Supply Chain Management müügitellimustega sünkroonimise käivitamiseks.

### <a name="names-of-the-templates-in-data-integration"></a>Mallide nimed andmeintegratsioonis

Malli **Töökäsud müügitellimusteks (Field Service rakendusele Supply Chain Management)** kasutatakse sünkroonimise käivitamiseks.

### <a name="names-of-the-tasks-in-the-data-integration-project"></a>Ülesannete nimed andmete integratsiooni projektis

- WorkOrderHeader
- WorkOrderServiceLineEstimate
- WorkOrderServiceLineUsed
- WorkOrderProductLineEstimate
- WorkOrderProductLineUsed

Enne müügitellimuse päiste ja ridade sünkroonimist on nõutavad järgmised sünkroonimisülesanded.

- Rakenduse Field Service tooted (Supply Chain Managementist Field Service'isse)
- Kontod (Salesist Supply Chain Managementi) – otsene

## <a name="entity-set"></a>Üksuste komplekt

| **Field Service** | **Supply Chain Management** |
|-------------------------|-------------------------|
| msdyn_workorders        | CDS-i müügitellimuse päised |
| msdyn_workorderservices | CDS-i müügitellimuse read   |
| msdyn_workorderproducts | CDS-i müügitellimuse read   |

## <a name="entity-flow"></a>Üksuse voog

Töökäsud luuakse rakenduses Field Service. Kui töökäsud sisaldavad ainult väliselt hallatavaid tooteid ja kui välja **Töökäsu olek** väärtuseks ei ole **Avatud – ajastamata** ja **Suletud – tühistatud**, saab töökäsud rakenduse Common Data Service andmeintegratsiooni projekti kaudu rakendusega Supply Chain Management sünkroonida. Töökäskude värskendused sünkroonitakse rakendusse Supply Chain Management müügitellimustena. Need värskendused sisaldavad päritolu tüübi ja oleku teavet.

## <a name="estimated-versus-used"></a>Eeldatav vs kasutatud

Rakenduses Field Service on toodete ja teenuste töökäskudel koguste ja summade jaoks mõlemad väärtused, nii väärtus **Eeldatav** kui ka **Kasutatud**. Siiski ei ole rakenduse Supply Chain Management müügitellimustel samasuguseid väärtusi **Eeldatav** ja **Kasutatud**. Toetamaks toote eraldamist, mille puhul kasutatakse rakenduse Supply Chain Management müügitellimusel eeldatud kogust, kuid hoidmaks kasutatud kogust, mida tuleks tarbida ja arveldada, sünkroonivad töökäskude tooteid ja teenuseid kaks ülesannete komplekti. Üks komplekt ülesandeid on väärtuste **Eeldatav** ja teine ülesannete komplekt on väärtuste **Kasutatud** jaoks.

See käitumine võimaldab kasutada stsenaariume, kus eeldatavaid väärtusi kasutatakse rakenduses Supply Chain Management eraldamiseks või reserveerimiseks, samas kui kasutatud väärtusi kasutatakse tarbimiseks ja arveldamiseks.

### <a name="estimated"></a>Hinnanguline

Tooteridade sünkroonimiseks kasutatakse väärtusi **Eeldatav**, kui on väärtus **Rea olek** on **Eeldatav**, suvandi **Eraldatud** väärtuseks on määratud **Jah** ja valiku **Süsteemi olek** väärtuseks pole **Suletud – sisestatud**.

Teenusridade sünkroonimiseks kasutatakse väärtusi **Eeldatav**, kui on väärtus **Rea olek** on **Eeldatav** ja valiku **Süsteemi olek** väärtuseks pole **Suletud – sisestatud**.

### <a name="used"></a>Kasutatud

Väärtusi **Kasutatud** kasutatakse tarbimiseks ja arveldamiseks. Sellistel juhtudel sünkroonitakse väärtused **Kasutatud**.

Järgmine tabel annab ülevaate mitmesugustest tooteridade kombinatsioonidest.

| Süsteemi olek <br>(Field Service) | Rea olek <br>(Field Service) | Eraldatud <br>(Field Service) |Sünkroonitud väärtus <br>(Supply Chain Management) |
|--------------------|-------------|-----------|---------------------------------|
| Avatud – ajastatud   | Hinnanguline   | Jah       | Hinnanguline                       |
| Avatud – ajastatud   | Hinnanguline   | Ei        | Kasutatud                            |
| Avatud – ajastatud   | Kasutatud        | Jah       | Kasutatud                            |
| Avatud – ajastatud   | Kasutatud        | Ei        | Kasutatud                            |
| Avatud – pooleli | Hinnanguline   | Jah       | Hinnanguline                       |
| Avatud – pooleli | Hinnanguline   | Ei        | Kasutatud                            |
| Avatud – pooleli | Kasutatud        | Jah       | Kasutatud                            |
| Avatud – pooleli | Kasutatud        | Ei        | Kasutatud                            |
| Avatud – lõpule viidud   | Hinnanguline   | Jah       | Hinnanguline                       |
| Avatud – lõpule viidud   | Hinnanguline   | Ei        | Kasutatud                            |
| Avatud – lõpule viidud   | Kasutatud        | Jah       | Kasutatud                            |
| Avatud – lõpule viidud   | Kasutatud        | Ei        | Kasutatud                            |
| Suletud – sisestatud    | Hinnanguline   | Jah       | Kasutatud                            |
| Suletud – sisestatud    | Hinnanguline   | Ei        | Kasutatud                            |
| Suletud – sisestatud    | Kasutatud        | Jah       | Kasutatud                            |
| Suletud – sisestatud    | Kasutatud        | Ei        | Kasutatud                            |

Järgmine tabel annab ülevaate mitmesugustest teenusridade kombinatsioonidest.

| Süsteemi olek <br>(Field Service) | Rea olek <br>(Field Service) | Sünkroonitud väärtus <br>(Supply Chain Management) |
|--------------------|-------------|-----------|
| Avatud – ajastatud   | Hinnanguline   | Hinnanguline |
| Avatud – ajastatud   | Kasutatud        | Kasutatud      |
| Avatud – pooleli | Hinnanguline   | Hinnanguline |
| Avatud – pooleli | Kasutatud        | Kasutatud      |
| Avatud – lõpule viidud   | Hinnanguline   | Hinnanguline |
| Avatud – lõpule viidud   | Kasutatud        | Kasutatud      |
| Suletud – sisestatud    | Hinnanguline   | Kasutatud      |
| Suletud – sisestatud    | Kasutatud        | Kasutatud      |

Väärtuste **Eeldatav** vs **Kasutatud** sünkroonimist hallatakse kahe toote- ja teenusridade jaoks mõeldud ülesannete komplekti abil. Eelmääratletud filtrid käivitavad õige ülesande ja aluseks olev vastendamine aitab tagada, et sünkroonitakse õiged väärtused **Eeldatav** vs **Kasutatud**.

### <a name="example"></a>Näide

1. Rakenduses Field Service luuakse ja plaanitakse töökäsk.

    **Süsteemi oleku** väärtus on **Avatud – ajastatud**.

    - **Tooterida:** Eeldatav kogus = 5ühikut, Kasutatud kogus = 0ühikut, Rea olek = Eeldatav, Eraldatud = Ei
    - **Teenusrida:** Eeldatav kogus = 2h, Kasutatud kogus = 0h, Rea olek = Eeldatav

    Selle näite puhul sünkroonitakse rakendusse Supply Chain Management toote välja **Kasutatud kogus** väärtus **0** (null) ja teenuse välja **Eeldatav kogus** väärtus **2h**.

2. Tooted eraldatakse rakenduses Field Service.

    **Süsteemi oleku** väärtus on **Avatud – ajastatud**.

    - **Tooterida:** Eeldatav kogus = 5ühikut, Kasutatud kogus = 0ühikut, Rea olek = Eeldatav, Eraldatud = Jah
    - **Teenusrida:** Eeldatav kogus = 2h, Kasutatud kogus = 0h, Rea olek = Eeldatav

    Selle näite puhul sünkroonitakse rakendusse Supply Chain Management toote välja **Eeldatav kogus** väärtus **5ea** ja teenuse välja **Eeldatav kogus** väärtus **2h**.

3. Hooldustehnik alustab töökäsuga tööd ja registreerib 6 materjali kasutamise.

    **Süsteemi oleku** väärtus on **Avatud – pooleli**.

    - **Tooterida:** Eeldatav kogus = 5ühikut, Kasutatud kogus = 6ühikut, Rea olek = Kasutatud, Eraldatud = Jah
    - **Teenusrida:** Eeldatav kogus = 2h, Kasutatud kogus = 0h, Rea olek = Eeldatav

    Selle näite puhul sünkroonitakse rakendusse Supply Chain Management toote välja **Kasutatud kogus** väärtus **6** ja teenuse välja **Eeldatav kogus** väärtus **2h**.

4. Hooldustehnik lõpetab töökäsu ja registreerib kasutatud ajaks 1,5 tundi.

    **Süsteemi oleku** väärtus on **Avatud – lõpule viidud**.

    - **Tooterida:** Eeldatav kogus = 5ühikut, Kasutatud kogus = 6ühikut, Rea olek = Kasutatud, Eraldatud = Jah
    - **Teenusrida:** Eeldatav kogus = 2h, Kasutatud kogus = 1,5h, Rea olek = Kasutatud

    Selle näite puhul sünkroonitakse rakendusse Supply Chain Management toote välja **Kasutatud kogus** väärtus **6** ja teenuse välja **Kasutatud kogus** väärtus **1,5 h**.

## <a name="sales-order-origin-and-status"></a>Müügitellimuse päritolu ja olek

### <a name="sales-origin"></a>Müügi allikas

Töökäskudest pärinevate müügitellimuste jälgimiseks saate luua müügiallika, kus suvandi **Päritolu tüübi määramine** väärtuseks on määratud **Jah** ja väljaks **Müügi päritolu tüüp** on seatud **Töökäsu integratsioon**.

Vaikimisi valib vastendamine müügiallika jaoks kõigi töökäskudest loodud müügitellimuste puhul müügi päritolu tüübiks **Töökäsu integratsioon**. See käitumine võib olla kasulik, kui töötate müügitellimusega rakenduses Supply Chain Management. Peaksite veenduma, et töökäskudest pärinevaid müügitellimusi ei sünkroonita rakendusse Field Service tagasi töökäskudena.

Üksikasju õige müügi päritolu seadistamiseks rakenduses Supply Chain Management vaadake selle teema jaotisest Eeltingimused ja vastendamise seadistamine.

### <a name="status"></a>Olek

Kui müügitellimus pärineb töökäsust, kuvatakse müügitellimuse päises vahekaardil **Seadistus** väli **Välise töö tellimuse olek**. Sellel väljal kuvatakse süsteemi olek töökäsust rakenduses Field Service, et aidata jälgida sünkroonitud müügitellimuste töökäsu olekut rakenduses Supply Chain Management. See väli aitab ka kasutajal määrata, millal müügitellimus tuleks lähetada või arveldada.

Väljal **Välise töö tellimuse olek** võivad olla järgmised väärtused.

- Avatud – ajastatud
- Avatud – pooleli
- Avatud – lõpule viidud
- Suletud – sisestatud

## <a name="field-service-crm-solution"></a>Rakenduse Field Service CRM lahendus

Rakenduste Field Service ja Supply Chain Management vahelise integratsiooni toetamiseks on vajalikud rakenduse Field Service CRM lahenduse lisafunktsioonid. Lahendus sisaldab järgmisi muudatusi.

### <a name="work-order-entity"></a>Töökäsu olem

**Töökäsu** olemile on lisatud väli **Sisaldab ainult väliselt hallatavaid tooteid**, mis ilmub lehel. Seda kasutatakse, et jälgida pidevalt, kas töökäsk sisaldab ainult väliselt hallatavaid tooteid. Töökäsk sisaldab ainult väliselt hallatavaid tooteid, kui kõiki seotud tooteid hallatakse rakenduses Supply Chain Management. See väli aitab tagada, et kasutaja ei püüaks sünkroonida töökäske, mis hõlmavad tundmatuid tooteid.

### <a name="work-order-product-entity"></a>Töökäsu tooteüksus

- **Töökäsu tooteüksusele** on lisatud väli **Tellimus sisaldab ainult väliselt hallatavaid tooteid**, mis ilmub lehel. Seda kasutatakse, et jälgida pidevalt, kas töökäsu toodet hallatakse rakenduses Supply Chain Management. See väli aitab tagada, et kasutaja ei püüaks sünkroonida töökäsu tooteid, mis hõlmavad rakenduse Supply Chain Management jaoks tundmatuid tooteid.
- **Töökäsu tooteüksusele** on lisatud väli **Päise süsteemi olek**, mis ilmub lehel. Seda kasutatakse, et jälgida pidevalt töökäsu süsteemi olekut ja see aitab tagada, et töökäsu toodete sünkroonimisel rakendusse Supply Chain Management kasutatakse õiget filtreerimist. Kui filtrid on integratsiooni ülesannete jaoks määratud, kasutatakse eeldatavate või kasutatud väärtuste sünkroonimisvajaduse määramiseks välja **Päise süsteemi olek** teave.
- Väljal **Arveldatud ühikusumma** kuvatakse tegeliku kasutatud ühiku arveldatud summa. Väärtus arvutatakse selliselt, et välja **Kogusumma** väärtus jagatakse välja **Tegelik kogus** väärtusega. Välja kasutatakse integratsiooniks süsteemidega, mis ei toeta eri väärtusi kasutatud koguse ja arveldatud koguse jaoks. Seda välja ei kuvata kasutajaliideses (UI). 
- Välja **Arveldatud allahindluse summa** arvutatakse selliselt, et välja **Allahindluse summa** väärtusele liidetakse välja **Arveldatud ühikusumma** arvutuse ümardatud väärtus. Seda välja kasutatakse integratsiooniks ja ei kuvata kasutajaliideses.
- Väljal **Kümnendkogus** säilitatakse välja **Kogus** väärtus kümnendarvuna. Seda välja kasutatakse integratsiooniks ja ei kuvata kasutajaliideses. 
- Välja **Kasutatud** väärtus lähtestatakse väärtuseni **0** (null), kui töökäsu toote välja **Rea olek** väärtus **Kasutatud** muudetakse väärtuseks **Eeldatav**. See muudatus aitab ennetada olukordi, kus ekslikult sisestatud kasutatud kogust kasutatakse sünkroonimiseks, kui välja **Rea olek** väärtus on **Eeldatav** ja suvandi **Eraldatud** väärtuseks on määratud **Ei**.

### <a name="work-order-service-entity"></a>Töökäsu teenusüksus

- **Töökäsu teenusüksusele** on lisatud väli **Tellimus sisaldab ainult väliselt hallatavaid tooteid**, mis ilmub lehel. Seda kasutatakse, et jälgida pidevalt, kas töökäsu teenust hallatakse rakenduses Supply Chain Management. See väli aitab tagada, et kasutaja ei püüaks sünkroonida töökäsu teenuseid, mis hõlmavad rakenduse Supply Chain Management jaoks tundmatuid tooteid.
- **Töökäsu teenusüksusele** on lisatud väli **Päise süsteemi olek**, mis ilmub lehel. Seda kasutatakse, et jälgida pidevalt töökäsu süsteemi olekut ja see aitab tagada, et töökäsu teenuste sünkroonimisel rakendusse Supply Chain Management kasutatakse õiget filtreerimist. Kui filtrid on integratsiooni ülesannete jaoks määratud, kasutatakse eeldatavate või kasutatud väärtuste sünkroonimisvajaduse määramiseks välja **Päise süsteemi olek** teave.
- Väljal **Kestus tundides** säilitatakse välja **Kestus** väärtus pärast minutitest tundideks teisendamist. Seda välja kasutatakse integratsiooniks ja ei kuvata kasutajaliideses.
- Väljal **Eeldatav kestus tundides** säilitatakse välja **Eeldatav kestus** väärtus pärast minutitest tundideks teisendamist. Seda välja kasutatakse integratsiooniks ja ei kuvata kasutajaliideses.
- Väljal **Arveldatud ühikusumma** säilitatakse tegeliku kasutatud ühiku arveldatud summa. Väärtus arvutatakse selliselt, et välja **Kogusumma** väärtus jagatakse välja **Tegelik kogus** väärtusega. Seda välja kasutatakse integratsiooniks süsteemidega, mis ei toeta eri väärtusi kasutatud koguse ja arveldatud koguse jaoks. Välja ei kuvata kasutajaliideses.
- Välja **Arveldatud allahindluse summa** arvutatakse selliselt, et välja **Allahindluse summa** väärtusele liidetakse välja **Arveldatud ühikusumma** arvutuse ümardatud väärtus. Seda välja kasutatakse integratsiooniks ja ei kuvata kasutajaliideses.
- Väli **Väline reatellimus** on arvutatud reatellimuse negatiivne number, mida saab kasutada välissüsteemides, kus töökäsu toote- ja teenusread on ühendatud. See väli võimaldab sisestatud töökäsu toodetele positiivseid reanumbreid ja töökäsu teenustele negatiivseid reanumbreid lisada. Selle välja väärtuse arvutamiseks korrutatakse välja **Rea tellimuse** -1-ga. Seda välja ei kuvata kasutajaliideses.
- Välja **Kasutatud** väärtus lähtestatakse väärtuseni **0** (null), kui töökäsu teenuse välja **Rea olek** väärtus **Kasutatud** muudetakse mingil põhjusel väärtuseks **Eeldatav**. See muudatus aitab ennetada olukordi, kus ekslikult sisestatud kasutatud kogust kasutatakse sünkroonimiseks, kui välja **Rea olek** väärtus on **Eeldatav** ja suvandi **Päise süsteemi olek** väärtuseks on määratud **Suletud – sisestatud**.

## <a name="preconditions-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

Enne töökäskude sünkroonimist on oluline värskendada süsteemides järgmisi sätteid.

### <a name="setup-in-field-service"></a>Rakenduse Field Service seadistus

- Veenduge, et numbriseeria, mida kasutatakse rakenduses Field Service töökäskude jaoks, ei kattuks numbriseeriaga, mida kasutatakse müügitellimuste jaoks rakenduses Supply Chain Management. Muidu võidakse olemasolevaid müügitellimusi rakenduses Field Service või Supply Chain Management valesti värskendada.
- Väli **Töökäsu arve loomine** väärtuseks peab olema seatud **Mitte kunagi**, sest arveldamiseks kasutatakse rakendust Supply Chain Management. Avage **Field Service** \> **Sätted** \> **Haldus** \> **Field Service’i sätted** ja veenduge, et välja **Töökäsu arve loomine** väärtuseks oleks seatud **Mitte kunagi**.

### <a name="setup-in-supply-chain-management"></a>Seadistamine rakenduses Supply Chain Management

Töökäsu integratsiooni puhul on vajalik seadistada müügiallikas. Müügiallikat kasutatakse, et eristada müügitellimusi rakendusest Supply Chain Management, mis on loodud rakenduse Field Service töökäskudest. Kui müügitellimuse müügiallika tüübiks on **Töökäsu integratsioon**, kuvatakse müügitellimuse päises väli **Välise töö tellimuse olek**. Lisaks aitab müügiallikas tagada, et rakenduse Field Service töökäskudest loodud müügitellimused filtreeritakse välja müügitellimuse sünkroonimisel rakendusest Supply Chain Management rakendusse Field Service.

1. Avage **Müük ja turundus** \> **Seadistus** \> **Müügitellimused** \> **Müügiallikas**.
2. Uue müügiallika loomiseks valige **Uus**.
3. Sisestage väljal **Müügiallikas** müügiallika nimi, näiteks **WorkOrder**.
4. Sisestage väljale **Kirjeldus** kirjeldus, näiteks **Field Service’i töökäsk**.
5. Valige märkeruut **Päritolu tüübi määramine**.
6. Seadke välja **Müügi päritolu tüüp** väärtuseks **Töökäsu integratsioon**.
7. Valige **Salvesta**.


### <a name="setup-in-data-integration"></a>Seadistus andmete integratsioonis

Veenduge, et üksuse **msdyn_workorders** jaoks oleks olemas **integreerimisvõti**.
1. Avage andmete integratsioon
2. Valige vahekaart **Ühenduskomplekt**
3. Valige töökäsu sünkroonimiseks kasutatud ühenduskomplekt
4. Valige vahekaart **Integreerimisvõti**
5. Leidke msdyn_workorders ja kontrollige, kas võti **msdyn_name (töökäsu kood)** on lisatud. Kui seda ei kuvata, klõpsake selle lisamiseks lehe ülaosas valikut **Lisa võti** ja **Salvesta**

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderheader"></a>Töötellimused müügitellimuste juurde (Field Service rakendusele Supply Chain Management): WorkOrderHeader

Filter: (msdyn_systemstatus ne 690970005) ja (msdyn_systemstatus ne 690970000) ja (msdynce_hasexternallymaintainedproductsonly eq true)

[![Malli vastendamine andmete integratsioonis](./media/FSWorkOrder1.png )](./media/FSWorkOrder1.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderservicelineestimate"></a>Töötellimused müügitellimuste juurde (Field Service rakendusele Supply Chain Management): WorkOrderServiceLineEstimate

Filter: (msdynce_headersystemstatus ne 690970005) ja (msdynce_headersystemstatus ne 690970000) ja (msdynce_orderhasexternalmaintainedproductsonly eq true) ja (msdyn_linestatus eq 690970000) ja (msdynce_headersystemstatus ne 690970004)

[![Malli vastendamine andmete integratsioonis](./media/FSWorkOrder2.png )](./media/FSWorkOrder2.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderservicelineused"></a>Töötellimused müügitellimuste juurde (Field Service rakendusele Supply Chain Management): WorkOrderServiceLineUsed

Filter: (msdynce_headersystemstatus ne 690970005) ja (msdynce_headersystemstatus ne 690970000) ja (msdynce_orderhasexternalmaintainedproductsonly eq true) ja ((msdyn_linestatus eq 690970001) või (msdynce_headersystemstatus eq 690970004))

[![Malli vastendamine andmete integratsioonis](./media/FSWorkOrder3.png )](./media/FSWorkOrder3.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderproductlineestimate"></a>Töötellimused müügitellimuste juurde (Field Service rakendusele Supply Chain Management): WorkOrderProductLineEstimate

Filter: (msdynce_headersystemstatus ne 690970005) ja (msdynce_headersystemstatus ne 690970000) ja (msdynce_orderhasexternalmaintainedproductsonly eq true) ja (msdyn_linestatus eq 690970000) ja (msdynce_headersystemstatus ne 690970004) ja (msdyn_allocated eq true)

[![Malli vastendamine andmete integratsioonis](./media/FSWorkOrder4.png )](./media/FSWorkOrder4.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderproductlineused"></a>Töötellimused müügitellimuste juurde (Field Service rakendusele Supply Chain Management): WorkOrderProductLineUsed

Filter: (msdynce_headersystemstatus ne 690970005) ja (msdynce_headersystemstatus ne 690970000) ja (msdynce_orderhasexternalmaintainedproductsonly eq true) ja ((msdyn_linestatus eq 690970001) või (msdynce_headersystemstatus eq 690970004) või (msdyn_allocated ne true))

[![Malli vastendamine andmete integratsioonis](./media/FSWorkOrder5.png )](./media/FSWorkOrder5.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]