---
title: "Rakenduse Sales kontode sünkroonimine rakenduse Finance and Operations klientidega"
description: "Teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse kontode sünkroonimiseks rakendusest Microsoft Dynamics 365 for Sales rakendusse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1fdbeaaba53cd439d9872be78b1cf67cbc5a57b9
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a>Rakenduse Sales kontode sünkroonimine rakenduse Finance and Operations klientidega

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Enne kui saate lahendust Potentsiaalne klient sularahaks kasutada, tutvuge [Dynamics 365 andmeintegratsiooniga](/common-data-service/entity-reference/dynamics-365-integration). 

Teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse kontode sünkroonimiseks rakendusest Microsoft Dynamics 365 for Sales (Sales) rakendusse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).

## <a name="template-and-task"></a>Mall ja ülesanne

Kontode sünkroonimiseks rakendusest Sales rakendusse Finance and Operations kasutatakse järgmisi malle ja aluseks olevaid ülesandeid.

- **Malli nimi:** Kontod (Salesist Fin and Opsi)
- **Ülesande nimi projektis:** Kontod – Konto – Kliendid

Nõutavad sünkroonimisülesanded enne konto/kliendi sünkroonimist: pole

## <a name="entity-set"></a>Üksuste komplekt

| Müük    | CDS     | Finance and Operations |
|----------|---------|------------------------|
| Kontod | Konto | Kliendid              |

## <a name="entity-flow"></a>Üksuse voog

Kontosid hallatakse rakenduses Sales ja need sünkroonitakse rakendusega Finance and Operations klientidena. Nende klientide atribuudi **On väliselt hallatav** sätteks on määratud **Jah**, et jälgida rakendusest Sales pärit kliente. Arveldamise ajal kasutatakse seda teavet rakendusega Sales sünkroonitud arvete filtreerimiseks.

## <a name="prospect-to-cash-solution-for-sales"></a>Lahendus Potentsiaalne klient sularahaks rakendusele Sales

Väli **Konto number** on saadaval lehel **Konto**. See on loomulik ja korduvatu võti, et toetada integratsiooni. Kliendisuhete halduse (CRM) lahenduse loomuliku võtme funktsioon võib mõjutada kliente, kes juba kasutavad välja **Konto number**, kuid ei kasuta iga konto puhul atribuudi **Konto number** kordumatuid väärtusi. Praegu ei toeta integratsioonilahendus seda juhtumit.

Kui uue konto loomisel ei ole atribuudi **Konto number** väärtust veel olemas, luuakse see automaatselt numbriseeriat kasutades. Väärtus sisaldab sõnet **ACC**, millele järgneb suurenev numbriseeria ja seejärel kuuest tähemärgist koosnev järelliide. Näide: **ACC-01000-BVRCPS**

Kui rakendatakse integratsioonilahendust rakendusele Sales, seab täiendusskript välja **Konto number** olemasolevatele kontodele rakenduses Sales. Kui ühtki atribuudi **Konto number** väärtust ei ole, kasutatakse varem kirjeldatud numbriseeriat.

## <a name="preconditions-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

- Atribuudi **CustomerGroupId** vastendus jaotisest **CDS &gt; Sihtkoht** tuleb värskendada rakenduses Finance and Operations kehtivale väärtusele. Saate määrata vaikeväärtuse või määrata väärtuse väärtuskaardi abil. Malli vaikeväärtus on **10**.
- Väli **Aadress, riik, piirkonnakood** on rakenduses Finance and Operations nõutav. Sünkroonimistõrgete vältimiseks saate määrata vastendusest **CDS &gt; Sihtkoht** vaikeväärtuse. Sel juhul kasutatakse seda vaikeväärtust, kui väli on rakenduses Sales tühjaks jäetud.

    - Malli vaikeväärtus atribuudi **AddressCountryRegionISOCode** puhul on **USA**.
    - Atribuudi **DeliveryAddressCountryRegionISOCode** jaoks on malli vaikeväärtus **USA**.

- Lisades järgmised vastendused vastendusest **CDS &gt; Sihtkoht**, saate vähendada rakenduses Finance and Operations nõutavate käsitsi värskenduste arvu. Saate kasutada vaikeväärtust või väärtuskaarti näiteks valikust **Riik/piirkond** või **Linn**.

    - **SiteId** – sait on vajalik pakkumiste ja müügitellimuse ridade loomiseks rakenduses Finance and Operations. Vaikesaidi võib võtta kas tootelt või kliendilt tellimuse päises. Atribuudi **SiteId** jaoks on malli vaikeväärtus **1**.
    - **WarehouseId** – ladu on vajalik pakkumiste ja müügitellimuse ridade töötlemiseks rakenduses Finance and Operations. Vaikelao võib võtta kas tootelt või kliendilt tellimuse päises rakenduses Finance and Operations. Atribuudi **WarehouseId** jaoks on malli vaikeväärtus **13**.
    - **LanguageId** – keel on vajalik pakkumiste ja müügitellimuste loomiseks rakenduses Finance and Operations. Vaikimisi kasutatakse kliendilt saadud tellimuse päises olevat keelt. Malli vaikeväärtus atribuudi **LanguageId** puhul on **en-us**.

- CDS-i organisatsiooni ID värskendamine (**Organization_OrganizationId**) vastenduses **Allikas &gt; CDS**. Malli vaikeväärtus on **ORG001**.

## <a name="template-mapping-in-data-integrator"></a>Malli vastendamine andmeintegraatoris

> [!NOTE]
> Väljad **Maksetingimused**, **Veosetingimused**, **Tarnetingimused**, **Saatmisviis** ja **Tarneviis** ei ole vaikevastenduste osa. Nende väljade vastendamiseks peate seadistama väärtuste vastendamise. Väärtuse vastendused on kohased neis organisatsioonides olevatele andmetele, mille vahel üksust sünkroonitakse.

Järgmisel joonisel on toodud näide malli vastendusest andmeintegraatoris.

![Malli vastendamine andmeintegraatoris](./media/accounts-template-mapping-data-integrator-1.png)

![Malli vastendamine kontode puhul andmeintegraatoris](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Seotud dokumendid

[Rakenduse Finance and Operations toodete sünkroonimine rakenduse Sales toodetega](products-template-mapping.md)

[Rakenduse Sales kontaktide sünkroonimine rakenduse Finance and Operations kontaktide või klientidega](contacts-template-mapping.md)

[Rakenduse Sales müügipakkumise päiste ja ridade sünkroonimine rakendusega Finance and Operations](sales-quotation-template-mapping.md)

[Rakenduse Finance and Operations müügitellimuse päiste ja ridade sünkroonimine rakendusega Sales](sales-order-template-mapping.md)

[Rakenduse Finance and Operations müügiarve päiste ja ridade sünkroonimine rakendusega Sales](sales-invoice-template-mapping.md)




