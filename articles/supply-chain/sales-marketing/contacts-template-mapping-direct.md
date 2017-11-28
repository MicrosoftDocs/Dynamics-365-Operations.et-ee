---
title: "Rakenduse Sales kontaktide vahetu sünkroonimine rakenduse Finance and Operations kontaktide või klientidega"
description: "See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse üksuste Kontakt (kontaktid) ja Kontakt (kliendid) sünkroonimiseks rakendusest Microsoft Dynamics 365 for Sales rakendusse Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
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
ms.openlocfilehash: 8de9a920f384b69c9b3764a0431208bbdcb395bf
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>Rakenduse Sales kontaktide vahetu sünkroonimine rakenduse Finance and Operations kontaktide või klientidega

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Enne kui saate kasutada lahendust Potentsiaalne klient sularahaks, tutvuge [Dynamics 365 andmeintegratsiooniga](/common-data-service/entity-reference/dynamics-365-integration).

See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse üksuste Kontakt (kontaktid) ja Kontakt (kliendid) sünkroonimiseks rakendusest Microsoft Dynamics 365 for Sales rakendusse Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.

## <a name="data-flow-in-prospect-to-cash"></a>Andmevoog lahenduses Potentsiaalne klient sularahaks

Lahendus Potentsiaalne klient sularahaks kasutab andmete integreerimise funktsiooni andmete sünkroonimiseks rakenduste Finance and Operations ja Sales vahel. Andmete integratsiooniga saadaolevad lahenduse Potentsiaalne klient sularahaks mallid võimaldavad kontode, kontaktide, toodete, müügipakkumiste, müügitellimuste ja müügiarvete andmete liikumist rakenduste Finance, Operations ja Sales. Järgmine illustratsioon näitab, kuidas sünkroonitakse andmeid rakenduste Finance and Operations ja Sales vahel.

[![Andmevoog lahenduses Potentsiaalne klient sularahaks](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Mallid ja ülesanded

Saadaolevatele mallidele juurdepääsemiseks avage [PowerApps administreerimiskeskus](https://preview.admin.powerapps.com/dataintegration). Valige **Projektid** ja seejärel paremas ülanurgas **Uus projekt**, et valida avalikud mallid.

Rakenduse Sales kontaktide (kontaktid) sünkroonimiseks rakenduse Finance and Operations kontaktidega (kliendid)kasutatakse järgmisi malle ja aluseks olevaid ülesandeid.

- **Mallide nimed andmete integratsioonis.**

    - Kontaktid (rakendusest Sales rakendusse Fin and Ops) – otse
    - Kontaktid kliendiga (rakendusest Sales rakendusse Fin and Ops) – otse

- **Ülesannete nimed andmete integratsiooni projektis.**

    - Kontaktid
    - ContactToCustomer

Enne kontakti sünkroonimist on nõutav järgmine sünkroonimisülesanne: kontod (Salesist Fin and Opsi)

## <a name="entity-sets"></a>Üksuste komplektid

| Müük    | Finance and Operations |
|----------|------------------------|
| Kontaktid | CDS-i kontaktid           |
| Kontaktid | Kliendid V2           |

## <a name="entity-flow"></a>Üksuse voog

Kontakte hallatakse rakenduses Sales ja need sünkroonitakse rakendusega Finance and Operations.

Kontakt rakenduses Sales võib olla rakenduses Finance and Operations kontakt või klient. Selleks et välja uurida, kas rakenduse Sales kontakt tuleks sünkroonida rakendusega Finance and Operations kontakti või kliendina, uurib süsteem rakenduses Sales kontakti järgmisi atribuute.

- **Sünkroonimine kliendiga rakenduses Finance and Operations:** kontaktid, mille puhul suvandi **On aktiivne klient** sätteks on seatud **Jah**
- **Sünkroonimine kontaktiga rakenduses Finance and Operations:** kontaktid, mille puhul suvandi **On aktiivne klient** sätteks on seatud **Ei** ja **Ettevõte** (peakonto/kontakt) osutab kontole (mitte kontaktile)

## <a name="prospect-to-cash-solution-for-sales"></a>Lahendus Potentsiaalne klient sularahaks rakendusele Sales

Kontaktile on lisatud uus väli **On aktiivne klient**. Seda välja kasutatakse müügitegevusega kontaktide eristamiseks müügitellimuseta kontaktidest. Suvandi **On aktiivne klient** sätteks on seatud **Jah** ainult kontaktide puhul, kellel on seotud pakkumisi, tellimusi või arveid. Ainult need kontaktid sünkroonitakse rakendusega Finance and Operations klientidena.

Kontaktile on lisatud uus väli **IsCompanyAnAccount**. See väli näitab, kas kontakt on lingitud ettevõttega (peakonto/kontakt), mille tüüp on **Konto**. Seda teavet kasutatakse kontaktide tuvastamiseks, kes tuleb sünkroonida rakendusega Finance and Operations kontaktidena.

Kontaktile on lisatud uus väli **Kontakti number**, et tagada integratsiooni jaoks loomulik ja kordumatu võti. Kui uus kontakt on loodud, luuakse numbriseeria abil automaatselt väärtus **Kontakti number**. Väärtus sisaldab sõnet **CON**, millele järgneb suurenev numbriseeria ja seejärel kuuest tähemärgist koosnev järelliide. Näide: **CON-01000-BVRCPS**

Kui rakendusele Sales on lisatud integratsioonilahendus, seab täiendusskript välja **Kontakti number** olemasolevatele kontaktidele, kasutades eespool mainitud numbriseeriat. Täiendusskript seab ka välja **On aktiivne klient** sätteks **Jah** kõigi müügitegevusega kontaktide puhul.

## <a name="in-finance-and-operations"></a>Rakenduses Finance and Operations

Kontaktid sildistatakse atribuuti **IsContactPersonExternallyMaintained** kasutades. See atribuut näitab, et kõnealust kontakti hallatakse väliselt. Sellisel juhul hallatakse väliselt hallatavaid kontakte rakenduses Müük.

## <a name="preconditions-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

### <a name="contact-to-customer"></a>Kontakt kliendiga

- Väli **CustomerGroup** on rakenduses Finance and Operations nõutav. Sünkroonimistõrgete vältimiseks saate määrata vastenduses vaikeväärtuse. Sel juhul kasutatakse seda vaikeväärtust, kui väli on rakenduses Sales tühjaks jäetud.

    Malli vaikeväärtus on **10**.

- Kui lisate järgmised vastendused, saate vähendada rakenduses Finance and Operations nõutavate käsitsi värskenduste arvu. Saate kasutada vaikeväärtust või väärtuskaarti näiteks valikust **Riik/piirkond** või **Linn**.

    - **SiteId**: rakenduses Finance and Operations saab toodetele määrata ka vaikesaidi. Sait on vajalik pakkumiste ja müügitellimuste loomiseks rakenduses Finance and Operations.

        Malli väärtus atribuudile **SiteId** pole määratletud.

    - **WarehouseId**: rakenduses Finance and Operations saab toodetele määrata ka vaikelao. Ladu on vajalik pakkumiste ja müügitellimuste loomiseks rakenduses Finance and Operations.

        Malli väärtus atribuudile **WarehouseId** pole määratletud.

    - **LanguageId** – keel on vajalik pakkumiste ja müügitellimuste loomiseks rakenduses Finance and Operations.
    
        Malli vaikeväärtus on **en-us**.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmisel joonisel on toodud näide malli vastendusest andmete integratsioonis. 

> [!NOTE]
> Vastendamine näitab, millise välja teave sünkroonitakse rakendusest Sales rakendusse Finance and Operations.

### <a name="contact-to-contact"></a>Kontakt kontaktiga

![Malli vastendamine andmeintegraatoris](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a>Kontakt kliendiga

![Malli vastendamine andmeintegraatoris](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a>Seotud dokumendid

[Potentsiaalne klient sularahaks](prospect-to-cash.md)

[Rakenduse Sales kontode vahetu sünkroonimine rakenduse Finance and Operations klientidega](accounts-template-mapping-direct.md)

[Rakenduse Finance and Operations toodete vahetu sünkroonimine rakenduse Sales toodetega](products-template-mapping-direct.md)

[Rakenduse Finance and Operations müügitellimuse päiste ja ridade vahetu sünkroonimine rakendusega Sales](sales-order-template-mapping-direct.md)

[Rakenduse Finance and Operations müügiarve päiste ja ridade vahetu sünkroonimine rakendusega Sales](sales-invoice-template-mapping-direct.md)



