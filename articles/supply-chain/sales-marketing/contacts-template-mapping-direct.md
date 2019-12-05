---
title: Rakenduse Sales kontaktide sünkroonimine otse rakenduse Supply Chain Management kontaktide või klientidega
description: Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse üksuste Kontakt (kontaktid) ja Kontakt (kliendid) sünkroonimiseks rakendusest Dynamics 365 Sales rakendusse Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 141464f2ce7cb4ccfd2a8fb7a266e657e8f52015
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814117"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-supply-chain-management"></a>Rakenduse Sales kontaktide sünkroonimine otse rakenduse Supply Chain Management kontaktide või klientidega

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Enne kui saate kasutada lahendust Potentsiaalne klient sularahaks, tutvuge [andmete integreerimisega teenusesse Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).

Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse üksuste Kontakt (kontaktid) ja Kontakt (kliendid) sünkroonimiseks rakendusest Dynamics 365 Sales otse rakendusse Dynamics 365 Supply Chain Management.

## <a name="data-flow-in-prospect-to-cash"></a>Andmevoog lahenduses Potentsiaalne klient sularahaks

Lahendus Potentsiaalne klient sularahaks kasutab andmete integreerimise funktsiooni andmete sünkroonimiseks rakenduste Supply Chain Management ja Sales vahel. Andmete integratsiooniga saadaolevad lahenduse Potentsiaalne klient sularahaks mallid võimaldavad kontode, kontaktide, toodete, müügipakkumiste, müügitellimuste ja müügiarvete andmete liikumist rakenduste Supply Chain Management ja Sales. Järgmine illustratsioon näitab, kuidas sünkroonitakse andmeid rakenduste Supply Chain Management ja Sales vahel.

[![Andmevoog lahenduses Potentsiaalne klient sularahaks](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Mallid ja ülesanded

Saadaolevatele mallidele juurdepääsemiseks avage [PowerAppsi administreerimiskeskus](https://preview.admin.powerapps.com/dataintegration). Valige **Projektid** ja seejärel paremas ülanurgas **Uus projekt**, et valida avalikud mallid.

Rakenduse Sales kontaktide (kontaktid) sünkroonimiseks rakenduse Supply Chain Management kontaktidega (kliendid)kasutatakse järgmisi malle ja aluseks olevaid ülesandeid.

- **Mallide nimed andmeintegratsioonis**

    - Kontaktid (Salesist Supply Chain Managementi) – otsene
    - Klientide kontaktid (Salesist Supply Chain Managementi) – otsene

- **Ülesannete nimed andmete integratsiooni projektis**

    - Kontaktid
    - ContactToCustomer

Enne kontakti sünkroonimist on nõutav järgmine sünkroonimisülesanne: kontod (Salesist Supply Chain Managementi)

## <a name="entity-sets"></a>Üksuste komplektid

| Müük    | Supply Chain Management |
|----------|------------------------|
| Kontaktid | CDS-i kontaktid           |
| Kontaktid | Kliendid V2           |

## <a name="entity-flow"></a>Üksuse voog

Kontakte hallatakse rakenduses Sales ja need sünkroonitakse rakendusega Supply Chain Management.

Kontakt rakenduses Sales võib olla rakenduses Supply Chain Management kontakt või klient. Selleks et välja uurida, kas rakenduse Sales kontakt tuleks sünkroonida rakendusega Supply Chain Management kontakti või kliendina, uurib süsteem rakenduses Sales kontakti järgmisi atribuute.

- **Sünkroonimine kliendiga rakenduses Supply Chain Management:** kontaktid, mille puhul suvandi **On aktiivne klient** sätteks on seatud **Jah**
- **Sünkroonimine kontaktiga rakenduses Supply Chain Management:** kontaktid, mille puhul suvandi **On aktiivne klient** sätteks on seatud **Ei** ja **Ettevõte** (peakonto/kontakt) osutab kontole (mitte kontaktile)

## <a name="prospect-to-cash-solution-for-sales"></a>Lahendus Potentsiaalne klient sularahaks rakendusele Sales

Kontaktile on lisatud uus väli **On aktiivne klient**. Seda välja kasutatakse müügitegevusega kontaktide eristamiseks müügitellimuseta kontaktidest. Suvandi **On aktiivne klient** sätteks on seatud **Jah** ainult kontaktide puhul, kellel on seotud pakkumisi, tellimusi või arveid. Ainult need kontaktid sünkroonitakse rakendusega Supply Chain Management klientidena.

Kontaktile on lisatud uus väli **IsCompanyAnAccount**. See väli näitab, kas kontakt on lingitud ettevõttega (peakonto/kontakt), mille tüüp on **Konto**. Seda teavet kasutatakse kontaktide tuvastamiseks, kes tuleb sünkroonida rakendusega Supply Chain Management kontaktidena.

Kontaktile on lisatud uus väli **Kontakti number**, et tagada integratsiooni jaoks loomulik ja kordumatu võti. Kui uus kontakt on loodud, luuakse numbriseeria abil automaatselt väärtus **Kontakti number**. Väärtus sisaldab sõnet **CON**, millele järgneb suurenev numbriseeria ja seejärel kuuest tähemärgist koosnev järelliide. Näide: **CON-01000-BVRCPS**

Kui rakendusele Sales on lisatud integratsioonilahendus, seab täiendusskript välja **Kontakti number** olemasolevatele kontaktidele, kasutades eespool mainitud numbriseeriat. Täiendusskript seab ka välja **On aktiivne klient** sätteks **Jah** kõigi müügitegevusega kontaktide puhul.

## <a name="in-supply-chain-management"></a>Rakenduses Supply Chain Management

Kontaktid sildistatakse atribuuti **IsContactPersonExternallyMaintained** kasutades. See atribuut näitab, et kõnealust kontakti hallatakse väliselt. Sellisel juhul hallatakse väliselt hallatavaid kontakte rakenduses Müük.

## <a name="preconditions-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

### <a name="contact-to-customer"></a>Kontakt kliendiga

- **CustomerGroup** on nõutav Supply Chain Managementis. Sünkroonimistõrgete vältimiseks saate määrata vastenduses vaikeväärtuse. Sel juhul kasutatakse seda vaikeväärtust, kui väli on rakenduses Sales tühjaks jäetud.

    Malli vaikeväärtus on **10**.

- Kui lisate järgmised vastendused, saate vähendada rakenduses Supply Chain Management nõutavate käsitsi värskenduste arvu. Saate kasutada vaikeväärtust või väärtuskaarti näiteks valikust **Riik/piirkond** või **Linn**.

    - **SiteId**: rakenduses Supply Chain Management saab toodetele määrata ka vaikesaidi. Sait on vajalik pakkumiste ja müügitellimuste loomiseks rakenduses Supply Chain Management.

        Malli väärtus atribuudile **SiteId** pole määratletud.

    - **WarehouseId**: rakenduses Supply Chain Management saab toodetele määrata ka vaikelao. Ladu on vajalik pakkumiste ja müügitellimuste loomiseks rakenduses Supply Chain Management.

        Malli väärtus atribuudile **WarehouseId** pole määratletud.

    - **LanguageId** – keel on vajalik pakkumiste ja müügitellimuste loomiseks rakenduses Supply Chain Management.
    
        Malli vaikeväärtus on **en-us**.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmisel joonisel on toodud näide malli vastendusest andmete integratsioonis. 

> [!NOTE]
> Vastendamine näitab, millise välja teave sünkroonitakse rakendusest Sales rakendusse Supply Chain Management.

### <a name="contact-to-contact"></a>Kontakt kontaktiga

![Malli vastendamine andmeintegraatoris](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a>Kontakt kliendiga

![Malli vastendamine andmeintegraatoris](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a>Seotud dokumendid

[Potentsiaalne klient sularahaks](prospect-to-cash.md)

[Rakenduse Sales kontode sünkroonimine otse rakenduse Supply Chain Management klientidega](accounts-template-mapping-direct.md)

[Rakenduse Supply Chain Management toodete sünkroonimine otse rakenduse Sales toodetega](products-template-mapping-direct.md)

[Müügitellimuste vahetu sünkroonimine rakenduse Sales ja rakenduse Supply Chain Management vahel](sales-order-template-mapping-direct-two-ways.md)

[Rakenduse Supply Chain Management arve päiste ja ridade sünkroonimine otse rakendusega Sales](sales-invoice-template-mapping-direct.md)


