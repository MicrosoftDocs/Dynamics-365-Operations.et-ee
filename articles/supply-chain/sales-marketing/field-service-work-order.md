---
title: "Rakenduse Field Service töökäskude sünkroonimine rakenduse Finance and Operations müügitellimustega"
description: "See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse rakenduse Field Service töökäskude sünkroonimiseks rakenduse Finance and Operations müügitellimustega."
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
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
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 854240bef9d6193c8f0f608687b68e6842fe272c
ms.contentlocale: et-ee
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-work-orders-in-field-service-to-sales-orders-in-finance-and-operations"></a>Rakenduse Field Service töökäskude sünkroonimine rakenduse Finance and Operations müügitellimustega

[!include[banner](../includes/banner.md)]

See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse rakenduse Microsoft Dynamics 365 for Field Service töökäskude sünkroonimiseks müügitellimustega rakenduses Microsoft Dynamics 365 for Finance and Operations.

[![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/field-service-integration.png)](./media/field-service-integration.png)

See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse rakenduse Field Service töökäskude sünkroonimiseks rakenduse Finance and Operations müügitellimustega.

## <a name="templates-and-tasks"></a>Mallid ja ülesanded

Järgmisi malle ja aluseks olevaid ülesandeid kasutatakse rakenduse Field Service töökäskude rakenduse Finance and Operations müügitellimustega sünkroonimise käivitamiseks.

### <a name="names-of-the-templates-in-data-integration"></a>Mallide nimed andmeintegratsioonis

Malli **Töökäsud müügitellimusteks (Field Service'ist Fin and Opsi)** kasutatakse sünkroonimise käivitamiseks.

### <a name="names-of-the-tasks-in-the-data-integration-project"></a>Ülesannete nimed andmete integratsiooni projektis

- WorkOrderHeader
- WorkOrderServiceLineEstimate
- WorkOrderServiceLineUsed
- WorkOrderProductLineEstimate
- WorkOrderProductLineUsed

Enne müügitellimuse päiste ja ridade sünkroonimist on nõutavad järgmised sünkroonimisülesanded.

- Field Service’i tooted (Fin and Opsist Field Service’isse)
- Kontod (Salesist Fin and Opsi) – otse

## <a name="entity-set"></a>Üksuste komplekt

| **Field Service** | **Finance and Operations** |
|-------------------------|-------------------------|
| msdyn_workorders        | CDS-i müügitellimuse päised |
| msdyn_workorderservices | CDS-i müügitellimuse read   |
| msdyn_workorderproducts | CDS-i müügitellimuse read   |

## <a name="entity-flow"></a>Üksuse voog

Töökäsud luuakse rakenduses Field Service. Kui töökäsud sisaldavad ainult väliselt hallatavaid tooteid ja kui välja **Töökäsu olek** väärtuseks ei ole **Avatud – ajastamata** või **Suletud – tühistatud**, saab töökäsud CDS-i andmeintegratsiooni projekti kaudu rakendusega Finance and Operations sünkroonida. Töökäskude värskendused sünkroonitakse rakendusse Finance and Operations müügitellimustena. Need värskendused sisaldavad päritolu tüübi ja oleku teavet.

## <a name="estimated-versus-used"></a>Eeldatav vs kasutatud

Rakenduses Field Service on toodete ja teenuste töökäskudel koguste ja summade jaoks mõlemad väärtused, nii väärtus **Eeldatav** kui ka **Kasutatud**. Siiski ei ole rakenduse Finance and Operations müügitellimustel samasuguseid väärtusi **Eeldatav** ja **Kasutatud**. Toetamaks toote eraldamist, mille puhul kasutatakse rakenduse Finance and Operations müügitellimusel eeldatud kogust, kuid hoidmaks kasutatud kogust, mida tuleks tarbida ja arveldada, sünkroonivad töökäskude tooteid ja teenuseid kaks ülesannete komplekti. Üks komplekt ülesandeid on väärtuste **Eeldatav** ja teine ülesannete komplekt on väärtuste **Kasutatud** jaoks.

See käitumine võimaldab kasutada stsenaariume, kus eeldatavaid väärtusi kasutatakse rakenduses Finance and Operations eraldamiseks või reserveerimiseks, samas kui kasutatud väärtusi kasutatakse tarbimiseks ja arveldamiseks.

### <a name="estimated"></a>Hinnanguline

Tooteridade sünkroonimiseks kasutatakse väärtusi **Eeldatav**, kui on väärtus **Rea olek** on **Eeldatav**, suvandi **Eraldatud** väärtuseks on määratud **Jah** ja valiku **Süsteemi olek** väärtuseks pole **Suletud – sisestatud**.

Teenusridade sünkroonimiseks kasutatakse väärtusi **Eeldatav**, kui on väärtus **Rea olek** on **Eeldatav** ja valiku **Süsteemi olek** väärtuseks pole **Suletud – sisestatud**.

### <a name="used"></a>Kasutatud

Väärtusi **Kasutatud** kasutatakse tarbimiseks ja arveldamiseks. Sellistel juhtudel sünkroonitakse väärtused **Kasutatud**.

Järgmine tabel annab ülevaate mitmesugustest tooteridade kombinatsioonidest.

| Süsteemi olek <br>(Field Service) | Rea olek <br>(Field Service) | Eraldatud <br>(Field Service) |Sünkroonitud väärtus <br>(Finance and Operations) |
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

| Süsteemi olek <br>(Field Service) | Rea olek <br>(Field Service) | Sünkroonitud väärtus <br>(Finance and Operations) |
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

    Selle näite puhul sünkroonitakse rakendusse Finance and Operations toote välja **Kasutatud kogus** väärtus **0** (null) ja teenuse välja **Eeldatav kogus** väärtus **2h**.

2. Tooted eraldatakse rakenduses Field Service.

    **Süsteemi oleku** väärtus on **Avatud – ajastatud**.

    - **Tooterida:** Eeldatav kogus = 5ühikut, Kasutatud kogus = 0ühikut, Rea olek = Eeldatav, Eraldatud = Jah
    - **Teenusrida:** Eeldatav kogus = 2h, Kasutatud kogus = 0h, Rea olek = Eeldatav

    Selle näite puhul sünkroonitakse rakendusse Finance and Operations toote välja **Eeldatav kogus** väärtus **5ühikut** ja teenuse välja **Eeldatav kogus** väärtus **2h**.

3. Hooldustehnik alustab töökäsuga tööd ja registreerib 6 materjali kasutamise.

    **Süsteemi oleku** väärtus on **Avatud – pooleli**.

    - **Tooterida:** Eeldatav kogus = 5ühikut, Kasutatud kogus = 6ühikut, Rea olek = Kasutatud, Eraldatud = Jah
    - **Teenusrida:** Eeldatav kogus = 2h, Kasutatud kogus = 0h, Rea olek = Eeldatav

    Selle näite puhul sünkroonitakse rakendusse Finance and Operations toote välja **Kasutatud kogus** väärtus **6** ja teenuse välja **Eeldatav kogus** väärtus **2h**.

4. Hooldustehnik lõpetab töökäsu ja registreerib kasutatud ajaks 1,5 tundi.

    **Süsteemi oleku** väärtus on **Avatud – lõpule viidud**.

    - **Tooterida:** Eeldatav kogus = 5ühikut, Kasutatud kogus = 6ühikut, Rea olek = Kasutatud, Eraldatud = Jah
    - **Teenusrida:** Eeldatav kogus = 2h, Kasutatud kogus = 1,5h, Rea olek = Kasutatud

    Selle näite puhul sünkroonitakse rakendusse Finance and Operations toote välja **Kasutatud kogus** väärtus **1,5h** ja teenuse välja **Eeldatav kogus** väärtus **2h**.

## <a name="sales-order-origin-and-status"></a>Müügitellimuse päritolu ja olek

### <a name="sales-origin"></a>Müügi allikas

Töökäskudest pärinevate müügitellimuste jälgimiseks rakenduses Finance and Operations saate luua müügiallika, kus suvandi **Päritolu tüübi määramine** väärtuseks on määratud **Jah** ja väljaks **Müügi päritolu tüüp** on seatud **Töökäsu integratsioon**.

Vaikimisi valib vastendamine müügiallika jaoks kõigi töökäskudest loodud müügitellimuste puhul müügi päritolu tüübiks **Töökäsu integratsioon**. See käitumine võib olla kasulik, kui töötate müügitellimusega rakenduses Finance and Operations. Peaksite veenduma, et töökäskudest pärinevaid müügitellimusi ei sünkroonita rakendusse Field Service tagasi töökäskudena.

Üksikasju õige müügi päritolu seadistamiseks rakenduses Finance and Operations vaadake selle teema jaotisest Eeltingimused ja vastendamise seadistamine.

### <a name="status"></a>Olek

Kui müügitellimus pärineb töökäsust, kuvatakse müügitellimuse päises vahekaardil **Seadistus** väli **Välise töö tellimuse olek**. Sellel väljal kuvatakse süsteemi olek töökäsust rakenduses Field Service, et aidata jälgida sünkroonitud müügitellimuste töökäsu olekut rakenduses Finance and Operations. See väli aitab ka rakenduse Finance and Operations kasutajal määrata, millal müügitellimus tuleks lähetada või arveldada.

Väljal **Välise töö tellimuse olek** võivad olla järgmised väärtused.

- Avatud – ajastatud
- Avatud – pooleli
- Avatud – lõpule viidud
- Suletud – sisestatud

## <a name="field-service-crm-solution"></a>Rakenduse Field Service CRM lahendus

Rakenduste Field Service ja Finance and Operations vahelise integratsiooni toetamiseks on vajalikud rakenduse Field Service CRM lahenduse lisafunktsioonid. Lahendus sisaldab järgmisi muudatusi.

### <a name="work-order-entity"></a>Töökäsu olem

**Töökäsu** olemile on lisatud väli **Sisaldab ainult väliselt hallatavaid tooteid**, mis ilmub lehel. Seda kasutatakse, et jälgida pidevalt, kas töökäsk sisaldab ainult väliselt hallatavaid tooteid. Töökäsk sisaldab ainult väliselt hallatavaid tooteid, kui kõiki seotud tooteid hallatakse rakenduses Finance and Operations. See väli aitab tagada, et kasutaja ei püüaks sünkroonida töökäske, mis hõlmavad rakenduse Finance and Operations jaoks tundmatuid tooteid.

### <a name="work-order-product-entity"></a>Töökäsu tooteüksus

- **Töökäsu tooteüksusele** on lisatud väli **Tellimus sisaldab ainult väliselt hallatavaid tooteid**, mis ilmub lehel. Seda kasutatakse, et jälgida pidevalt, kas töökäsu toodet hallatakse rakenduses Finance and Operations. See väli aitab tagada, et kasutaja ei püüaks sünkroonida töökäsu tooteid, mis hõlmavad rakenduse Finance and Operations jaoks tundmatuid tooteid.
- **Töökäsu tooteüksusele** on lisatud väli **Päise süsteemi olek**, mis ilmub lehel. Seda kasutatakse, et jälgida pidevalt töökäsu süsteemi olekut ja see aitab tagada, et töökäsu toodete sünkroonimisel rakendusse Finance and Operations kasutatakse õiget filtreerimist. Kui filtrid on integratsiooni ülesannete jaoks määratud, kasutatakse eeldatavate või kasutatud väärtuste sünkroonimisvajaduse määramiseks välja **Päise süsteemi olek** teave.
- Väljal **Arveldatud ühikusumma** kuvatakse tegeliku kasutatud ühiku arveldatud summa. Väärtus arvutatakse selliselt, et välja **Kogusumma** väärtus jagatakse välja **Tegelik kogus** väärtusega. Välja kasutatakse integratsiooniks süsteemidega, mis ei toeta eri väärtusi kasutatud koguse ja arveldatud koguse jaoks. Seda välja ei kuvata kasutajaliideses (UI). 
- Välja **Arveldatud allahindluse summa** arvutatakse selliselt, et välja **Allahindluse summa** väärtusele liidetakse välja **Arveldatud ühikusumma** arvutuse ümardatud väärtus. Seda välja kasutatakse integratsiooniks ja ei kuvata kasutajaliideses.
- Väljal **Kümnendkogus** säilitatakse välja **Kogus** väärtus kümnendarvuna. Seda välja kasutatakse integratsiooniks ja ei kuvata kasutajaliideses. 
- Välja **Kasutatud** väärtus lähtestatakse väärtuseni **0** (null), kui töökäsu toote välja **Rea olek** väärtus **Kasutatud** muudetakse väärtuseks **Eeldatav**. See muudatus aitab ennetada olukordi, kus ekslikult sisestatud kasutatud kogust kasutatakse sünkroonimiseks, kui välja **Rea olek** väärtus on **Eeldatav** ja suvandi **Eraldatud** väärtuseks on määratud **Ei**.

### <a name="work-order-service-entity"></a>Töökäsu teenusüksus

- **Töökäsu teenusüksusele** on lisatud väli **Tellimus sisaldab ainult väliselt hallatavaid tooteid**, mis ilmub lehel. Seda kasutatakse, et jälgida pidevalt, kas töökäsu teenust hallatakse rakenduses Finance and Operations. See väli aitab tagada, et kasutaja ei püüaks sünkroonida töökäsu teenuseid, mis hõlmavad rakenduse Finance and Operations jaoks tundmatuid teenuseid.
- **Töökäsu teenusüksusele** on lisatud väli **Päise süsteemi olek**, mis ilmub lehel. Seda kasutatakse, et jälgida pidevalt töökäsu süsteemi olekut, ja see aitab tagada, et töökäsu teenuste sünkroonimisel rakendusse Finance and Operations kasutatakse õiget filtreerimist. Kui filtrid on integratsiooni ülesannete jaoks määratud, kasutatakse eeldatavate või kasutatud väärtuste sünkroonimisvajaduse määramiseks välja **Päise süsteemi olek** teave.
- Väljal **Kestus tundides** säilitatakse välja **Kestus** väärtus pärast minutitest tundideks teisendamist. Seda välja kasutatakse integratsiooniks ja ei kuvata kasutajaliideses.
- Väljal **Eeldatav kestus tundides** säilitatakse välja **Eeldatav kestus** väärtus pärast minutitest tundideks teisendamist. Seda välja kasutatakse integratsiooniks ja ei kuvata kasutajaliideses.
- Väljal **Arveldatud ühikusumma** säilitatakse tegeliku kasutatud ühiku arveldatud summa. Väärtus arvutatakse selliselt, et välja **Kogusumma** väärtus jagatakse välja **Tegelik kogus** väärtusega. Seda välja kasutatakse integratsiooniks süsteemidega, mis ei toeta eri väärtusi kasutatud koguse ja arveldatud koguse jaoks. Välja ei kuvata kasutajaliideses.
- Välja **Arveldatud allahindluse summa** arvutatakse selliselt, et välja **Allahindluse summa** väärtusele liidetakse välja **Arveldatud ühikusumma** arvutuse ümardatud väärtus. Seda välja kasutatakse integratsiooniks ja ei kuvata kasutajaliideses.
- Väli **Väline reatellimus** on arvutatud reatellimuse negatiivne number, mida saab kasutada välissüsteemides, kus töökäsu toote- ja teenusread on ühendatud. See väli võimaldab sisestatud töökäsu toodetele positiivseid reanumbreid ja töökäsu teenustele negatiivseid reanumbreid lisada. Selle välja väärtuse arvutamiseks korrutatakse välja **Rea tellimuse** -1-ga. Seda välja ei kuvata kasutajaliideses.
- Välja **Kasutatud** väärtus lähtestatakse väärtuseni **0** (null), kui töökäsu teenuse välja **Rea olek** väärtus **Kasutatud** muudetakse mingil põhjusel väärtuseks **Eeldatav**. See muudatus aitab ennetada olukordi, kus ekslikult sisestatud kasutatud kogust kasutatakse sünkroonimiseks, kui välja **Rea olek** väärtus on **Eeldatav** ja suvandi **Päise süsteemi olek** väärtuseks on määratud **Suletud – sisestatud**.

## <a name="preconditions-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

Enne töökäskude sünkroonimist on oluline värskendada süsteemides järgmisi sätteid.

### <a name="setup-in-field-service"></a>Rakenduse Field Service seadistus

- Veenduge, et numbriseeria, mida kasutatakse rakenduses Field Service töökäskude jaoks, ei kattuks numbriseeriaga, mida kasutatakse müügitellimuste jaoks rakenduses Finance and Operations. Muidu võidakse olemasolevaid müügitellimusi rakenduses Field Service või Finance and Operations valesti värskendada.
- Väli **Töökäsu arve loomine** väärtuseks peab olema seatud **Mitte kunagi**, sest arveldamiseks kasutatakse rakendust Finance and Operations. Avage **Field Service** \> **Sätted** \> **Haldus** \> **Field Service’i sätted** ja veenduge, et välja **Töökäsu arve loomine** väärtuseks oleks seatud **Mitte kunagi**.

### <a name="setup-in-finance-and-operations"></a>Seadistus rakenduses Finance and Operations

Töökäsu integratsiooni puhul on vajalik seadistada müügiallikas. Müügiallikat kasutatakse, et eristada müügitellimusi rakendusest Finance and Operations, mis on loodud rakenduse Field Service töökäskudest. Kui müügitellimuse müügiallika tüübiks on **Töökäsu integratsioon**, kuvatakse müügitellimuse päises väli **Välise töö tellimuse olek**. Lisaks aitab müügiallikas tagada, et rakenduse Field Service töökäskudest loodud müügitellimused filtreeritakse välja müügitellimuse sünkroonimisel rakendusest Finance and Operations rakendusse Field Service.

1. Avage **Müük ja turundus** \> **Seadistus** \> **Müügitellimused** \> **Müügiallikas**.
2. Uue müügiallika loomiseks valige **Uus**.
3. Sisestage väljal **Müügiallikas** müügiallika nimi, näiteks **WorkOrder**.
4. Sisestage väljale **Kirjeldus** kirjeldus, näiteks **Field Service’i töökäsk**.
5. Valige märkeruut **Päritolu tüübi määramine**.
6. Seadke välja **Müügi päritolu tüüp** väärtuseks **Töökäsu integratsioon**.
7. Valige **Salvesta**.

### <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

(Peagi tulekul)

