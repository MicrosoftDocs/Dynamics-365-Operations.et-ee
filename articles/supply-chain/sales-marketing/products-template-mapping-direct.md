---
title: "Rakenduse Finance and Operations toodete vahetu sünkroonimine rakenduse Sales toodetega"
description: "See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse toodete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition rakendusse Microsoft Dynamics 365 for Sales."
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
ms.openlocfilehash: 6c68c4482cacf70f003669cf335e52e47425d2f7
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-products-directly-from-finance-and-operations-to-products-in-sales"></a>Rakenduse Finance and Operations toodete vahetu sünkroonimine rakenduse Sales toodetega

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Enne kui saate kasutada lahendust Potentsiaalne klient sularahaks, tutvuge [Dynamics 365 andmeintegratsiooniga](/common-data-service/entity-reference/dynamics-365-integration).

See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse toodete vahetuks sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition rakendusse Microsoft Dynamics 365 for Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Andmevoog lahenduses Potentsiaalne klient sularahaks

Lahendus Potentsiaalne klient sularahaks kasutab andmete integreerimise funktsiooni andmete sünkroonimiseks rakenduste Finance and Operations ja Sales vahel. Andmete integratsiooniga saadaolevad lahenduse Potentsiaalne klient sularahaks mallid võimaldavad kontode, kontaktide, toodete, müügipakkumiste, müügitellimuste ja müügiarvete andmete liikumist rakenduste Finance, Operations ja Sales. Järgmine illustratsioon näitab, kuidas sünkroonitakse andmeid rakenduste Finance and Operations ja Sales vahel.

[![Andmevoog lahenduses Potentsiaalne klient sularahaks](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Mallid ja ülesanded

Saadaolevatele mallidele juurdepääsemiseks avage [PowerApps administreerimiskeskus](https://preview.admin.powerapps.com/dataintegration). Valige **Projektid** ja seejärel paremas ülanurgas **Uus projekt**, et valida avalikud mallid.

Toodete sünkroonimiseks rakendusest Sales rakendusse Finance and Operations kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

- **Andmete integratsioon malli nimi:** Tooted (rakendusest Fin and Ops rakendusse Sales) – otse
- **Ülesande nimi andmete integratsiooni projektis:** Tooted

Enne toodete sünkroonimist ei ole vaja teha ühtki sünkroonimisülesannet.

## <a name="entity-set"></a>Üksuste komplekt

| Finance and Operations     | Müük    |
|----------------------------|----------|
| Müüdavad väljastatud tooted | Tooted |

## <a name="entity-flow"></a>Üksuse voog

Tooteid hallatakse rakenduses Finance and Operations ja need sünkroonitakse rakendusega Sales. Andmeüksus **Müüdavad väljastatud tooted** rakenduses Finaces and Operations ekspordib ainult tooted, mille olek on *Müüdav*. Müüdavad tooted hõlmavad müügitellimuses kasutamiseks vajalikku teavet. Samad reeglid kehtivad, kui toode valideeritakse funktsiooniga **Valideeri** lehel **Vabastatud toode**.

Tootenumbrit kasutatakse võtmena. Kui tootevariandid sünkroonitakse rakendusega Sales, on igal tootevariandil seega individuaalne toote ID.

## <a name="prospect-to-cash-solution-for-sales"></a>Lahendus Potentsiaalne klient sularahaks rakendusele Sales

Rakenduses Sales lisatakse toodetele uus väli **On väliselt hallatav**, mis näitab, et kõnealust toodet hallatakse väliselt. Vaikimisi seatakse rakendusse Sales importimise ajal selle väärtuseks **Jah**. Saadaval on järgmised väärtused:

- **Jah**: toode pärineb rakendusest Finance and Operations ja seda ei saa rakenduses Sales muuta.
- **Ei**: toode sisestati otse rakendusse Sales.
- **(Tühi)**: toode oli rakenduses Sales olemas enne lahenduse Potentsiaalne klient sularahaks lubamist.

Väli **On väliselt hallatav** aitab tagada, et ainult väliselt hallatavate toodetega pakkumised ja müügitellimused sünkroonitakse rakendusega Finance and Operations.

Väliselt hallatavad tooted lisatakse automaatselt esimesse kehtivasse hinnakirja, millel on sama valuuta. Hinnakirjad on korraldatud tähestikulises järjekorras nime alusel. Toote müügihinda rakendusest Finance and Operations kasutatakse hinnakirja hinnana. Seega peab rakenduses Sales olema hinnakiri iga toote müügivaluuta kohta rakenduses Finance and Operations. Vabastatud müüdavate toodete valuutaks on määratud selle juriidilise isiku arvestusvaluuta, millest toode eksporditakse.

> [!NOTE]
> Toote sünkroonimine ei õnnestu, kui vastava valuutaga hinnakiri puudub.

## <a name="preconditions-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

- Enne kui saate esimese sünkroonimise käivitada, peate olemasolevate toodete puhul rakenduses Finance and Operations täitma tabeli Eristatav toode. Olemasolevaid tooteid ei sünkroonita, enne kui see töö on lõpule viidud.

    1. Kasutage rakenduses Finance and Operations otsingufunktsiooni, et otsida suvandit **Asusta eristuva toote tabel**.
    2. Valige töö käivitamiseks nupp **Asusta eristuva toote tabel**. Seda tööd tohib käitada ainult üks kord.

- Veenduge, et müügi mõõtühiku (UOM) puhul nõutav väärtuskaart rakenduse Finance and Operations ja rakenduse Sales vahel oleks üksuste **SalesUnitSymbol** ja **DefaultUnit (nimi)** vastenduses olemas.
- Värskendage suvandi **Ühikugrupp** väärtuskaarti (**defaultuomscheduleid.name**), nii et see kattuks rakenduse Sales suvandiga **Ühikugrupid**.

    Malli vaikeväärtus on **Vaikeühik**.

- Veenduge, et kõigi toodete müügi mõõtühikud rakendusest Finance and Operations oleksid rakenduses Sales olemas.
- Veenduge, et hinnakirjad oleksid rakenduses Sales olemas iga toote müügivaluuta kohta rakenduses Finance and Operations.
- Rakenduses Sales tooteid luues võib nende olek olla **Mustand** või **Aktiivne**. Käitumist saab juhtida rakenduse Sales jaotises **Sätted** > **Administreerimine** > **Süsteemisätted** > **Sales**.

    Olekuga **Mustand** loodud tooted tuleb esmalt aktiveerida, enne kui neid saab pakkumistesse või müügitellimustesse lisada.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmistel joonistel on toodud näide malli vastendusest andmete integreerimises. 

> [!NOTE]
> Vastendamine näitab, millise välja teave sünkroonitakse rakendusest Sales rakendusse Finance and Operations.

![Malli vastendamine andmeintegraatoris](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a>Seotud dokumendid

[Potentsiaalne klient sularahaks](prospect-to-cash.md)

[Rakenduse Sales kontode vahetu sünkroonimine rakenduse Finance and Operations klientidega](accounts-template-mapping-direct.md)

[Rakenduse Sales kontaktide vahetu sünkroonimine rakenduse Finance and Operations kontaktide või klientidega](contacts-template-mapping-direct.md)

[Rakenduse Finance and Operations müügitellimuse päiste ja ridade vahetu sünkroonimine rakendusega Sales](sales-order-template-mapping-direct.md)

[Rakenduse Finance and Operations müügiarve päiste ja ridade vahetu sünkroonimine rakendusega Sales](sales-invoice-template-mapping-direct.md)




