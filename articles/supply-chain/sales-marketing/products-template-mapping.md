---
title: "Rakenduse Finance and Operations toodete sünkroonimine rakenduse Sales toodetega"
description: "See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse toodete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations, Enterprise edition rakendusse Microsoft Dynamics 365 for Sales."
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
ms.openlocfilehash: 063a20f133a00620bdf389b0a52a90bc61e2f7d4
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a>Rakenduse Finance and Operations toodete sünkroonimine rakenduse Sales toodetega

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Enne kui saate lahendust Potentsiaalne klient sularahaks kasutada, tutvuge [Dynamics 365 andmeintegratsiooniga](/common-data-service/entity-reference/dynamics-365-integration). 

See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse toodete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations, Enterprise edition rakendusse Microsoft Dynamics 365 for Sales.

## <a name="template-and-task"></a>Mall ja ülesanne

Toodete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) rakendusse Microsoft Dynamics 365 for Sales (Sales) kasutatakse järgmisi malle ja aluseks olevaid ülesandeid.

-   Malli nimi: Tooted (Fin and Opsist Salesi)

-   Ülesande nimi projektis: Tooted

Nõutavad sünkroonimisülesanded enne toote sünkroonimist: pole

## <a name="entity-set"></a>Üksuste komplekt

| **Finance and Operations** | **CDS** | **Müük**  |
|----------------------------|---------|------------|
| Müüdavad väljastatud tooted | Toode | Tooted   |

## <a name="entity-flow"></a>Üksuse voog

Tooteid hallatakse rakenduses Finance and Operations ja need sünkroonitakse rakendusega Sales. Andmeüksus **Müüdavad vabastatud tooted** rakenduses Finance and Operations ekspordib ainult müüdavaid tooteid, mis tähendab, et toodetel on teave, mis on nõutav müügitellimusel kasutamiseks. Samad reeglid kehtivad, kui toode valideeritakse funktsiooniga **Valideeri** lehel **Vabastatud toode**.

Atribuuti **Toote number** kasutatakse võtmena, mis tähendab, et tootevariandid sünkroonitakse CDS-i ja Salesiga eraldi **toote ID-dega** iga **tootevariandi** kohta.

## <a name="prospect-to-cash-solution-for-sales"></a>Lahendus Potentsiaalne klient sularahaks rakendusele Sales

Rakenduses Sales lisatakse toodetele uus väli **On väliselt hallatav**, mis näitab, et kõnealust toodet hallatakse väliselt. Vaikimisi seatakse rakendusse Sales importimise ajal selle väärtuseks **Jah**.

-   **On väliselt hallatav = jah**: toode pärineb rakendusest Finance and Operations ega ole rakenduses Sales redigeeritav.

-   **On väliselt hallatav = ei**: toode sisestatakse otse rakendusse Sales.

-   **On väliselt hallatav = tühi**: toode on rakenduses Sales olemas enne lahenduse Potentsiaalne klient sularahaks lubamist.

Välja **On väliselt hallatav** teavet kasutatakse tagamaks, et ainult **pakkumised** ja **müügitellimused** sättega **Väliselt hallatavad tooted** sünkroonitakse rakendusega Finance and Operations.

**Väliselt hallatavad toote** lisatakse automaatselt esimesse kehtivasse **hinnakirja**, millel on sama valuuta. Pange tähele, et loend on korraldatud tähestikuliselt **nime** järgi. Toote müügihinda rakendusest Finance and Operations kasutatakse **hinnakirja** hinnana. See tähendab, et rakenduses Sales peab olema **hinnakiri** igale **toote müügivaluutale** rakenduses Finance and Operations. Vabastatud müüdavate toodete valuutaks on määratud selle juriidilise isiku arvestusvaluuta, millest toode eksporditakse.

> [!NOTE]
> Toote sünkroonimine ei õnnestu ilma vastava valuutaga **hinnakirjata**.

## <a name="preconditions-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

-   Enne kui saate esimese sünkroonimise käivitada, peate olemasolevate toodete puhul rakenduses Finance and Operations asustama välja **Eristatava toote tabel**. Olemasolevaid tooteid ei sünkroonita, enne kui see töö on lõpule viidud.

    -   Kasutage rakenduses Finance and Operations otsingufunktsiooni, et otsida suvandit **Asusta eristuva toote tabel**.

    -   Klõpsake töö käivitamiseks nuppu **Asusta eristuva toote tabel**. See töö tuleb käivitada ainult üks kord.

-   Veenduge, et vajalik **ValueMap** müügi **mõõtühikuks** (UOM) rakenduses Finance and Operations oleks vastenduses **Allikas -\> CDS-i vastenduse SalesUnitSymbol / DefaultSellingUnitOfMeasure** olemas.

-   Värskendage väärtust **CDS-i organisatsiooni ID Organization_OrganizationId** vastenduses **Allikas -\> CDS**.

    -   Malli vaikeväärtus on ORG001.

-   Värskendage väärtust **ValueMap** suvandis **Ühikurühm** (**defaultuomscheduleid.name**) vastenduses **CDS -\> Sihtkoht**, et see vastaks suvandile **Ühikurühmad** rakenduses Sales.

    -   Malli vaikeväärtus on **Vaikeühik**.

-   Veenduge, et kõigi toodete müügi mõõtühikud rakendusest Finance and Operations oleksid rakenduses Sales olemas väärtusega **CDS-i märkeloendid**.

-   Veenduge, et **hinnakirjad** oleksid rakenduses Sales olemas iga toote müügivaluuta kohta rakenduses Finance and Operations.

-   Tooteid saab müüa rakenduses Sales olekuga **Mustand** või **Aktiivne**. Seda juhitakse rakenduse Sales menüü **Süsteemi sätted** jaotises **Müük**.

    -   Mustandina loodud tooted tuleb aktiveerida, enne kui need saab lisada **pakkumisele** või **müügitellimusele**.

## <a name="template-mapping-in-data-integrator"></a>Malli vastendamine andmeintegraatoris

Järgmisel joonisel on toodud näide malli vastendusest andmeintegraatoris.

![malli vastendamine andmeintegraatoris](./media/products-template-mapping-data-integrator-1.png)

![malli vastendamine toodete puhul andmeintegraatoris](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Seotud dokumendid

[Rakenduse Sales kontode sünkroonimine rakenduse Finance and Operations klientidega](accounts-template-mapping.md)

[Rakenduse Sales kontaktide sünkroonimine rakenduse Finance and Operations kontaktide või klientidega](contacts-template-mapping.md)

[Rakenduse Sales müügipakkumise päiste ja ridade sünkroonimine rakendusega Finance and Operations](sales-quotation-template-mapping.md)

[Rakenduse Finance and Operations müügitellimuse päiste ja ridade sünkroonimine rakendusega Sales](sales-order-template-mapping.md)

[Rakenduse Finance and Operations müügiarve päiste ja ridade sünkroonimine rakendusega Sales](sales-invoice-template-mapping.md)


