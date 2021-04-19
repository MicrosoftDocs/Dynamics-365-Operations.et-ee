---
title: Rakenduse Supply Chain Management toodete sünkroonimine otse rakenduse Sales toodetega
description: Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse toodete sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management otse rakendusse Dynamics 365 Sales.
author: ChristianRytt
ms.date: 06/10/2019
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
ms.openlocfilehash: 29bb9d05aa939ec82595e153faf03f290e219589
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817817"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a>Rakenduse Supply Chain Management toodete sünkroonimine otse rakenduse Sales toodetega

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> Enne kui saate kasutada lahendust Potentsiaalne klient sularahaks, tutvuge [andmete integreerimisega teenusesse Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).

Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse toodete sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management otse rakendusse Dynamics 365 Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Andmevoog lahenduses Potentsiaalne klient sularahaks

Lahendus Potentsiaalne klient sularahaks kasutab andmete integreerimise funktsiooni andmete sünkroonimiseks rakenduste Supply Chain Management ja Sales vahel. Andmete integratsiooniga saadaolevad lahenduse Potentsiaalne klient sularahaks mallid võimaldavad kontode, kontaktide, toodete, müügipakkumiste, müügitellimuste ja müügiarvete andmete liikumist rakenduste Supply Chain Management ja Sales. Järgmine illustratsioon näitab, kuidas sünkroonitakse andmeid rakenduste Supply Chain Management ja Sales vahel.

[![Andmevoog lahenduses Potentsiaalne klient sularahaks](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Mallid ja ülesanded

Saadaolevatele mallidele juurdepääsemiseks avage [Power Apps administreerimiskeskus](https://admin.powerapps.com/dataintegration). Valige **Projektid** ja seejärel paremas ülanurgas **Uus projekt**, et valida avalikud mallid.

Toodete sünkroonimiseks rakendusest Supply Chain Management rakendusse Sales kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

- **Andmete integratsioon malli nimi:** Tooted (rakendusest Fin and Ops rakendusse Sales) – otse
- **Ülesande nimi andmete integratsiooni projektis:** Tooted

Enne toodete sünkroonimist ei ole vaja teha ühtki sünkroonimisülesannet.

## <a name="entity-set"></a>Üksuste komplekt

| Supply Chain Management    | Müük    |
|----------------------------|----------|
| Müüdavad väljastatud tooted | Tooted |

## <a name="entity-flow"></a>Üksuse voog

Tooteid hallatakse rakenduses Supply Chain Management ja need sünkroonitakse rakendusega Sales. Andmeüksus **Müüdavad väljastatud tooted** rakenduses Supply Chain Management ekspordib ainult tooted, mille olek on *Müüdav*. Müüdavad tooted hõlmavad müügitellimuses kasutamiseks vajalikku teavet. Samad reeglid kehtivad, kui toode valideeritakse funktsiooniga **Valideeri** lehel **Vabastatud toode**.

Tootenumbrit kasutatakse võtmena. Kui tootevariandid sünkroonitakse rakendusega Sales, on igal tootevariandil seega individuaalne toote ID.

## <a name="prospect-to-cash-solution-for-sales"></a>Lahendus Potentsiaalne klient sularahaks rakendusele Sales

Rakenduses Sales lisatakse toodetele uus väli **On väliselt hallatav**, mis näitab, et kõnealust toodet hallatakse väliselt. Vaikimisi seatakse rakendusse Sales importimise ajal selle väärtuseks **Jah**. Saadaval on järgmised väärtused:

- **Jah**: toode pärineb rakendusest Supply Chain Management ja seda ei saa rakenduses Sales muuta.
- **Ei**: toode sisestati otse rakendusse Sales.
- **(Tühi)**: toode oli rakenduses Sales olemas enne lahenduse Potentsiaalne klient sularahaks lubamist.

Väli **On väliselt hallatav** aitab tagada, et ainult väliselt hallatavate toodetega pakkumised ja müügitellimused sünkroonitakse rakendusega upply Chain Management.

Väliselt hallatavad tooted lisatakse automaatselt esimesse kehtivasse hinnakirja, millel on sama valuuta. Hinnakirjad on korraldatud tähestikulises järjekorras nime alusel. Toote müügihinda rakendusest Supply Chain Management kasutatakse hinnakirja hinnana. Seega peab rakenduses Sales olema hinnakiri iga toote müügivaluuta kohta rakenduses Supply Chain Management. Vabastatud müüdavate toodete valuutaks on määratud selle juriidilise isiku arvestusvaluuta, millest toode eksporditakse.

> [!NOTE]
> - Toote sünkroonimine ei õnnestu, kui vastava valuutaga hinnakiri puudub.
> - Saate kontrollida integratsioonis kasutatud hinnakirja, vastendades andmeintegratsiooni projektis atribuudi pricelevelid.name [Vaikehinnakiri (nimi)]. Sisend peab olema väiketähtedes. Näiteks oleksid rakenduses Sales hinnakirja „Standard” vaikeväärtused järgmised: sihtväli: pricelevelid.name [Vaikehinnakiri (nimi)] ja vastenduse tüüp: [ { "transformType": "Default", "defaultValue": "standard" } ].

## <a name="preconditions-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

- Enne kui saate esimese sünkroonimise käivitada, peate olemasolevate toodete puhul rakenduses Supply Chain Management täitma tabeli Eristatav toode. Olemasolevaid tooteid ei sünkroonita, enne kui see töö on lõpule viidud.

    1. Kasutage rakenduses Supply Chain Management otsingufunktsiooni, et otsida suvandit **Asusta eristuva toote tabel**.
    2. Valige töö käivitamiseks nupp **Asusta eristuva toote tabel**. Seda tööd tohib käitada ainult üks kord.

- Veenduge, et müügi mõõtühiku (UOM) puhul nõutav väärtuskaart rakenduse Supply Chain Management ja rakenduse Sales vahel oleks üksuste **SalesUnitSymbol** ja **DefaultUnit (nimi)** vastenduses olemas.
- Värskendage suvandi **Ühikugrupp** väärtuskaarti (**defaultuomscheduleid.name**), nii et see kattuks rakenduse Sales suvandiga **Ühikugrupid**.

    Malli vaikeväärtus on **Vaikeühik**.

- Veenduge, et kõigi toodete müügi mõõtühikud rakendusest Supply Chain Management oleksid rakenduses Sales olemas.
- Veenduge, et hinnakirjad oleksid rakenduses Sales olemas iga toote müügivaluuta kohta rakenduses Supply Chain Management.
- Rakenduses Sales tooteid luues võib nende olek olla **Mustand** või **Aktiivne**. Käitumist saab juhtida rakenduse Sales jaotises **Sätted** > **Administreerimine** > **Süsteemisätted** > **Sales**.

    Olekuga **Mustand** loodud tooted tuleb esmalt aktiveerida, enne kui neid saab pakkumistesse või müügitellimustesse lisada.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmistel joonistel on toodud näide malli vastendusest andmete integreerimises. 

> [!NOTE]
> Vastendamine näitab, millise välja teave sünkroonitakse rakendusest Sales rakendusse Supply Chain Management.

![Malli vastendamine andmeintegraatoris](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a>Seotud dokumendid

[Potentsiaalne klient sularahaks](prospect-to-cash.md)

[Rakenduse Sales kontode sünkroonimine otse rakenduse Supply Chain Management klientidega](accounts-template-mapping-direct.md)

[Rakenduse Sales kontaktide sünkroonimine otse rakenduse Supply Chain Management kontaktide või klientidega](contacts-template-mapping-direct.md)

[Müügitellimuste vahetu sünkroonimine rakenduse Sales ja rakenduse Supply Chain Management vahel](sales-order-template-mapping-direct-two-ways.md)

[Rakenduse Supply Chain Management arve päiste ja ridade sünkroonimine otse rakendusega Sales](sales-invoice-template-mapping-direct.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]