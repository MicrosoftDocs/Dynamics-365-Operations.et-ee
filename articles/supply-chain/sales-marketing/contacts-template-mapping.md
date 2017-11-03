---
title: "Rakenduse Sales kontaktide sünkroonimine rakenduse Finance and Operations kontaktide või klientidega"
description: "See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse kontakti (kontaktid) ja kontakti (kliendid) sünkroonimiseks rakendusest Microsoft Dynamics 365 for Sales rakendusse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
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
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 41e27776b94df059ada13efb9a3dbf6a29d67f36
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>Rakenduse Sales kontaktide sünkroonimine rakenduse Finance and Operations kontaktide või klientidega

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Enne kui saate lahendust Potentsiaalne klient sularahaks kasutada, tutvuge [Dynamics 365 andmeintegratsiooniga](/common-data-service/entity-reference/dynamics-365-integration). 

See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse kontakti (kontaktid) üksuste ja kontakti (kliendid) sünkroonimiseks rakendusest Microsoft Dynamics 365 for Sales (Sales) rakendusse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).

## <a name="templates-and-tasks"></a>Mallid ja ülesanded

Kontakti (kontaktid) sünkroonimiseks rakendusest Sales kontaktiga (kliendid) rakenduses Finance and Operations kasutatakse järgmisi malle ja aluseks olevaid ülesandeid.

- **Mallide nimed:**

    - Kontaktid (Salesist Fin and Opsi)
    - Kontaktid kliendiga (Salesist Fin and Opsi)

- **Ülesannete nimed projektis:**

    - Kontaktid
    - ContactToCustomer

Enne kontakti sünkroonimist on nõutav järgmine sünkroonimisülesanne: kontod (Salesist Fin and Opsi)

## <a name="entity-sets"></a>Üksuste komplektid

| Müük    | CDS     | Finance and Operations |
|----------|---------|------------------------|
| Kontaktid | Kontakt | CDS-i kontaktid           |
| Kontaktid | Konto | Kliendid V2           |

## <a name="entity-flow"></a>Üksuse voog

Kontakte hallatakse rakenduses Sales ning sünkroonitakse teenuse Common Data Service (CDS) ja rakendusega Finance and Operations.

Kontakt rakenduses Sales saab kontaktiks CDS-is ja rakenduses Finance and Operations. Teise võimalusena saab see kontoks CDS-is ja kliendiks rakenduses Finance and Operations. Selleks et määrata, kas kontakt tuleb võtta rakendusest Sales sünkroonimiseks CDS-i ja rakendusega Finance and Operations (näiteks kontaktid rakenduses Sales &gt; kontakt teenuses CDS &gt; kontaktid rakenduses Finance and Operations), vaatab süsteem rakenduse Sales kontakti puhul järgmisi atribuute:

- **Sünkroonimine kontoga CDS-is ja kliendiga rakenduses Finance and Operations:** kontaktid, mille puhul suvandi **On aktiivne klient** sätteks on seatud **Jah**
- **Sünkroonimine kontaktiga CDS-is ja kontaktiga rakenduses Finance and Operations:** kontaktid, mille puhul suvandi **On aktiivne klient** sätteks on seatud **Ei** ja **Ettevõte** (Peakonto/kontakt) osutab kontole (mitte kontaktile)

## <a name="prospect-to-cash-solution-for-sales"></a>Lahendus Potentsiaalne klient sularahaks rakendusele Sales 

Kontaktile on lisatud uus väli **On aktiivne klient**. Seda välja kasutatakse müügitegevusega kontaktide eristamiseks müügitellimuseta kontaktidest. Suvandi **On aktiivne klient** sätteks on seatud **Jah** ainult kontaktide puhul, kellel on seotud pakkumisi, tellimusi või arveid. Ainult need kontaktid sünkroonitakse rakendusega Finance and Operations klientidena.

Kontaktile on lisatud uus väli **IsCompanyAnAccount**. Selle väljaga näidatakse, kas kontakt on lingitud ettevõttega (peakonto/kontakt), mille tüüp on **Konto**. Seda teavet kasutatakse kontaktide tuvastamiseks, kes tuleb sünkroonida rakendusega Finance and Operations kontaktidena.

Kontaktile on lisatud uus väli **Kontakti number**, et tagada integratsiooni jaoks loomulik ja kordumatu võti. Kui uus kontakt on loodud, luuakse numbriseeria abil automaatselt väärtus **Kontakti number**. Väärtus sisaldab sõnet **CON**, millele järgneb suurenev numbriseeria ja seejärel kuuest tähemärgist koosnev järelliide. Näide: **CON-01000-BVRCPS**

Kui rakendusele Sales on lisatud integratsioonilahendus, seab täiendusskript välja **Kontakti number** olemasolevatele kontaktidele, kasutades eespool kirjeldatud numbriseeriat. Täiendusskript seab ka välja **On aktiivne klient** sätteks **Jah** kõigi müügitegevusega kontaktide puhul.

## <a name="in-finance-and-operations"></a>Rakenduses Finance and Operations 

Kontaktid sildistatakse atribuuti **IsContactPersonExternallyMaintained** kasutades. See atribuut näitab, et kõnealust kontakti hallatakse väliselt. Sellisel juhul hallatakse väliselt hallatavaid kontakte rakenduses Müük.

## <a name="preconditions-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

### <a name="contact-to-contact"></a>Kontakt kontaktiga

- Värskendage välja **CDS-i organisatsiooni ID** vastenduses **Allikas &gt; CDS**.

    - Malli vaikeväärtus atribuudi **Organization_OrganizationId [organisatsiooni ID]** puhul on **ORG001**.
    - Malli vaikeväärtus atribuudi **PrimaryAccount_Organization_OrganizationId [organisatsiooni ID]** puhul on **ORG001**.

- Väli **Aadress, riik, piirkonnakood** on rakenduses Finance and Operations nõutav. Sünkroonimistõrgete vältimiseks saate määrata vastenduses **CDS &gt; Toimingud** vaikeväärtuse. Sel juhul kasutatakse seda vaikeväärtust, kui väli on rakenduses Sales tühjaks jäetud. Atribuudi **PrimaryAddressCountryRegionISOCode** jaoks on malli vaikeväärtus **USA**.
- Veenduge, et järgmise välja väärtus oleks rakenduses Finance and Operations olemas. Kui teave pole rakenduses Finance and Operations nõutav, saate vastenduse vastendusest **CDS &gt; Sihtkoht** eemaldada.

    - **Välja nimi rakenduses Finance and Operations:** Otsus
    - **Vastendamine:** PrimaryAccountRole = DecisionMakingRole

### <a name="contact-to-customer"></a>Kontakt kliendiga

- Värskendage välja **CDS-i organisatsiooni ID** vastenduses **Allikas &gt; CDS**. Malli vaikeväärtus atribuudi **Organization_OrganizationId [organisatsiooni ID]** puhul on **ORG001**.
- Väli **Aadress, riik, piirkonnakood** on rakenduses Finance and Operations nõutav. Sünkroonimistõrgete vältimiseks saate määrata vastenduses **CDS &gt; Sihtkoht** vaikeväärtuse. Sel juhul kasutatakse seda vaikeväärtust, kui väli on rakenduses Sales tühjaks jäetud. Atribuudi **PrimaryAddressCountryRegionISOCode** jaoks on malli vaikeväärtus **USA**.
- Väli **CustomerGroup** on rakenduses Finance and Operations nõutav. Sünkroonimistõrgete vältimiseks saate määrata vastenduses **CDS &gt; Sihtkoht** vaikeväärtuse. Sel juhul kasutatakse seda vaikeväärtust, kui väli on rakenduses Sales tühjaks jäetud. Atribuudi **CustomerGroupId** jaoks on malli vaikeväärtus **10**.
- Lisades järgmised vastendused vastendusest **CDS &gt; Sihtkoht**, saate vähendada rakenduses Finance and Operations olevate käsitsi värskenduste arvu. Saate kasutada vaikeväärtust või väärtuskaarti näiteks valikust **Riik/piirkond** või **Linn**.

    - **SiteId** – rakenduses Finance and Operations saab toodetele määrata ka vaikesaidi. Sait on vajalik pakkumiste ja müügitellimuste loomiseks rakenduses Finance and Operations. Malli väärtus atribuudile **SiteId** pole määratletud.
    - **WarehouseId** – rakenduses Finance and Operations saab toodetele määrata ka vaikelao. Ladu on vajalik pakkumiste ja müügitellimuste loomiseks rakenduses Finance and Operations. Malli väärtus atribuudile **WarehouseId** pole määratletud.
    - **LanguageId** – keel on vajalik pakkumiste ja müügitellimuste loomiseks rakenduses Finance and Operations. Malli vaikeväärtus atribuudi **LanguageId** puhul on **en-us**.

## <a name="template-mapping-in-data-integrator"></a>Malli vastendamine andmeintegraatoris

Järgmisel joonisel on toodud näide malli vastendusest andmeintegraatoris.

### <a name="contact-to-contact"></a>Kontakt kontaktiga

![Malli vastendamine andmeintegraatoris](./media/contacts-template-mapping-data-integrator-1.png)

![Malli vastendamine kontaktide puhul andmeintegraatoris](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a>Kontakt kliendiga

![Malli vastendamine andmeintegraatoris](./media/contacts-template-mapping-data-integrator-3.png)

![Malli vastendamine kontaktide puhul andmeintegraatoris](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Seotud dokumendid

[Rakenduse Finance and Operations toodete sünkroonimine rakenduse Sales toodetega](products-template-mapping.md)

[Rakenduse Sales kontode sünkroonimine rakenduse Finance and Operations klientidega](accounts-template-mapping.md)

[Rakenduse Sales müügipakkumise päiste ja ridade sünkroonimine rakendusega Finance and Operations](sales-quotation-template-mapping.md)

[Rakenduse Finance and Operations müügitellimuse päiste ja ridade sünkroonimine rakendusega Sales](sales-order-template-mapping.md)

[Rakenduse Finance and Operations müügiarve päiste ja ridade sünkroonimine rakendusega Sales](sales-invoice-template-mapping.md)

