---
title: "Rakenduse Sales kontode vahetu sünkroonimine rakenduse Finance and Operations klientidega"
description: "See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse kontode sünkroonimiseks rakendusest Microsoft Dynamics 365 for Sales rakendusse Microsoft Dynamics 365 for Finance and Operations."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: a0cabdab63d4d44010e52303d6f487db1e910059
ms.contentlocale: et-ee
ms.lasthandoff: 11/01/2018

---

# <a name="synchronize-accounts-directly-from-sales-to-customers-in-finance-and-operations"></a>Rakenduse Sales kontode sünkroonimine otse rakenduse Finance and Operations klientidega

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Enne lahenduse Potentsiaalne klient sularahaks kasutamist peaksite läbi lugema artikli [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).

See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse kontode sünkroonimiseks otse rakendusest Microsoft Dynamics 365 for Sales rakendusse Microsoft Dynamics 365 for Finance and Operations.

## <a name="data-flow-in-prospect-to-cash"></a>Andmevoog lahenduses Potentsiaalne klient sularahaks

Lahendus Potentsiaalne klient sularahaks kasutab andmete integreerimise funktsiooni andmete sünkroonimiseks rakenduste Finance and Operations ja Sales vahel.  Andmete integratsiooniga saadaolevad lahenduse Potentsiaalne klient sularahaks mallid võimaldavad kontode, kontaktide, toodete, müügipakkumiste, müügitellimuste ja müügiarvete andmete liikumist rakenduste Finance, Operations ja Sales. Järgmine illustratsioon näitab, kuidas sünkroonitakse andmeid rakenduste Finance and Operations ja Sales vahel.

[![Andmevoog lahenduses Potentsiaalne klient sularahaks](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Mallid ja ülesanded

Saadaolevatele mallidele juurdepääsemiseks avage [PowerApps administreerimiskeskus](https://preview.admin.powerapps.com/dataintegration). Valige **Projektid** ja seejärel paremas ülanurgas **Uus projekt**, et valida avalikud mallid.

Kontode sünkroonimiseks rakendusest Sales rakendusse Finance and Operations kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

- **Andmete integratsioon malli nimi:** Kontod (rakendusest Sales rakendusse Fin and Ops) – otse
- **Ülesande nimi projektis:** Kontod – Kliendid

Enne konto/kliendi sünkroonimist ei ole vaja teha ühtki sünkroonimisülesannet.

## <a name="entity-set"></a>Üksuste komplekt

| Müük    | Finance and Operations |
|----------|------------------------|
| Kontod | Kliendid V2           |

## <a name="entity-flow"></a>Üksuse voog

Kontosid hallatakse rakenduses Sales ja need sünkroonitakse rakendusega Finance and Operations klientidena. Nende klientide atribuudi **On väliselt hallatav** sätteks on määratud **Jah**, et jälgida rakendusest Sales pärit kliente. Arveldamise ajal kasutatakse seda teavet rakendusega Sales sünkroonitud arvete filtreerimiseks.

## <a name="prospect-to-cash-solution-for-sales"></a>Lahendus Potentsiaalne klient sularahaks rakendusele Sales

Väli **Konto number** on saadaval lehel **Konto**. See on loomulik ja kordumatu võti, et toetada integratsiooni. Kliendisuhete halduse (CRM) lahenduse loomuliku võtme funktsioon võib mõjutada kliente, kes juba kasutavad välja **Konto number**, kuid ei kasuta iga konto puhul atribuudi **Konto number** kordumatuid väärtusi. Praegu ei toeta integratsioonilahendus seda juhtumit.

Kui uue konto loomisel ei ole atribuudi **Konto number** väärtust veel olemas, luuakse see automaatselt numbriseeriat kasutades. Väärtus sisaldab sõnet **ACC**, millele järgneb suurenev numbriseeria ja seejärel kuuest tähemärgist koosnev järelliide. Näide: **ACC-01000-BVRCPS**

Kui rakendatakse integratsioonilahendust rakendusele Sales, seab täiendusskript välja **Konto number** olemasolevatele kontodele rakenduses Sales. Kui ühtki atribuudi **Konto number** väärtust ei ole, kasutatakse varem mainitud numbriseeriat.

## <a name="preconditions-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

- Atribuudi **CustomerGroupId** vastendust tuleb värskendada rakenduses Finance and Operations kehtivale väärtusele. Saate määrata vaikeväärtuse või määrata väärtuse väärtuskaardi abil.

    Malli vaikeväärtus on **10**.

- Kui lisate järgmised vastendused, saate vähendada rakenduses Finance and Operations nõutavate käsitsi värskenduste arvu. Saate kasutada vaikeväärtust või väärtuskaarti näiteks valikust **Riik/piirkond** või **Linn**.

    - **SiteId** – sait on vajalik pakkumiste ja müügitellimuse ridade loomiseks rakenduses Finance and Operations. Vaikesaidi võib võtta kas tootelt või kliendilt tellimuse päises.

        Malli vaikeväärtus on **1**.

    - **WarehouseId** – ladu on vajalik pakkumiste ja müügitellimuse ridade töötlemiseks rakenduses Finance and Operations. Vaikelao võib võtta kas tootelt või kliendilt tellimuse päises rakenduses Finance and Operations.

        Malli vaikeväärtus on **13**.

    - **LanguageId** – keel on vajalik pakkumiste ja müügitellimuste loomiseks rakenduses Finance and Operations. Vaikimisi kasutatakse kliendilt saadud tellimuse päises olevat keelt.

        Malli vaikeväärtus on **en-us**.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

> [!NOTE]
> Väljad **Maksetingimused**, **Veosetingimused**, **Tarnetingimused**, **Saatmisviis** ja **Tarneviis** ei ole vaikevastenduste osa. Nende väljade vastendamiseks peate seadistama väärtuskaardi, mis on kohane neis organisatsioonides olevatele andmetele, mille vahel üksust sünkroonitakse.

Järgmisel joonisel on toodud näide malli vastendusest andmete integratsioonis. 

> [!NOTE]
> Vastendamine näitab, millise välja teave sünkroonitakse rakendusest Sales rakendusse Finance and Operations.

![Malli vastendamine andmete integratsioonis](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a>Seotud dokumendid


[Potentsiaalne klient sularahaks](prospect-to-cash.md)

[Rakenduse Sales kontode vahetu sünkroonimine rakenduse Finance and Operations klientidega](accounts-template-mapping-direct.md)

[Rakenduse Sales kontaktide vahetu sünkroonimine rakenduse Finance and Operations kontaktide või klientidega](contacts-template-mapping-direct.md)

[Rakenduse Finance and Operations müügitellimuse päiste ja ridade sünkroonimine otse rakendusega Sales](sales-order-template-mapping-direct-two-ways.md)

[Rakenduse Finance and Operations müügiarve päiste ja ridade vahetu sünkroonimine rakendusega Sales](sales-invoice-template-mapping-direct.md)


