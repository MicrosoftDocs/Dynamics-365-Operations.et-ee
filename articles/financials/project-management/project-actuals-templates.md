---
title: "Projekti tegelike näitajate sünkroonimine Project Service Automationist otse projekti integratsiooni töölehele Finance and Operationsis sisestamiseks"
description: "See teema kirjeldab malle ja aluseks olevaid ülesandeid, mida kasutatakse projekti tegelike näitajate sünkroonimiseks rakendusest Microsoft Dynamics 365 for Project Service Automation otse rakendusse Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 05/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 85ff049852e0b00623f47a12fb66e2c9bb9c4151
ms.contentlocale: et-ee
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-actuals-from-project-service-automation-directly-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Projekti tegelike näitajate sünkroonimine Project Service Automationist otse projekti integratsiooni töölehele Finance and Operationsis sisestamiseks

See teema kirjeldab malle ja aluseks olevaid ülesandeid, mida kasutatakse projekti tegelike näitajate sünkroonimiseks rakendusest Microsoft Dynamics 365 for Project Service Automation otse rakendusse Dynamics 365 for Finance and Operations.

Mall sünkroonib kanded Project Service Automationist Finance and Operationsi vahetabelisse. Kui sünkroonimine on lõpule jõudnud, peate importima vahetabelist integratsiooni töölehele.

> [!NOTE]
> Projekti tegelike näitajate integratsioon on saadaval rakenduse Dynamics 365 for Finance and Operations versioonis 8.01.

> [!NOTE]
> Kui sisestate Project Service Automationis käibemaksusummasid aja- või kulukannete kohta, peate installima Project Service Automationi värskenduse 7. Kui värskendust ei installita, ei lingita maksu tegelikke näitajaid seostatud aja- või kuluandmete tegelike näitajatega ega sünkroonita Finance and Operationsisse. Lisateabe saamiseks võtke ühendust tugiteenusega.


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Andmevoog Project Service Automationist Finance and Operationsisse

Project Service Automationist Finance and Operationsisse integreerimise lahendus kasutab andmete sünkroonimiseks Project Service Automationi ja Finance and Operationsi eksemplaride vahel andmeintegratsiooni funktsiooni. Andmeintegratsiooni funktsioonis saadaolevad integratsioonimallid võimaldavad andmevoogu projekti tegelike näitajate kohta Project Service Automationist Finance and Operationsisse.

Järgmine joonis näitab, kuidas sünkroonitakse andmeid Project Service Automationi ja Finance and Operationsi vahel.

[![Andmevoog Project Service Automationi integreerimiseks Finance and Operationsiga](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)


## <a name="templates-and-tasks"></a>Mallid ja ülesanded

Saadaolevatele mallidele juurdepääsuks valige Microsoft PowerAppsi halduskeskuses suvand **Projektid** ja seejärel valige paremast ülanurgast suvand **Uus projekt**, et valida avalikud mallid.

Projekti tegelike näitajate sünkroonimiseks Project Service Automationist Finance and Operationsisse kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

-  **Andmeintegratsioon malli nimi:** projekti tegelikud näitajad (Project Service Automationist Finance and Operationsisse)

-  **Ülesannete nimed projektis:** 
    - Tegelikud 
    - TransactionConnections

## <a name="entity-set"></a>Üksuste komplekt

| Project Service Automation      | Finance and Operations                                      |
|---------------------------------|-------------------------------------------------------------|
| Tegelikud                         | Projekti tegelike väärtuste integratsiooniüksus                      |
| Kandeühendused         | Projekti kande seoste integratsiooniüksus    |

## <a name="entity-flow"></a>Üksuse voog

Projekti tegelikke näitajaid hallatakse Project Service Automationis ja need sünkroonitakse Finance and Operationsisse projekti integratsiooni töölehele. Raamatupidamine rakendatakse vaike-finantsdimensioonide ja sisestuse seadistuse alusel.

## <a name="preconditions"></a>Eeltingimused

Enne tegelike näitajate sünkroonimist peate konfigureerima Project Service Automationi integratsiooniparameetrid ja sünkroonima projektid, projektiülesanded ning projekti kulukande kategooriad.

## <a name="power-query"></a>Power Query

Peate kasutama Microsoft Power Queryt projekti tegelike näitajate mallis järgmisel otstarbel.
- Project Service Automationi **kandetüübi** teisendamine õigeks **kandetüübiks** Finance and Operationsis. Projekti tegelike näitajate (Project Service Automationist Finance and Operationsisse) mallil on see teisendus juba määratletud.
- Project Service Automationi **arveldustüübi** teisendamine õigeks **arveldustüübiks** Finance and Operationsis. Projekti tegelike näitajate (Project Service Automationist Finance and Operationsisse) mallil on see teisendus juba määratletud. Seejärel vastendatakse arveldustüüp **rea atribuudiga** rakenduse Dynamics 365 for Project Service Automation integratsiooniparameetrite vormil oleva konfiguratsiooni põhjal.
- Filtreerimine kindlate **ressursi organisatsiooniüksuste** alusel, mis tuleb selle malliga sünkroonida.
- Kui **kontsernisisese aja või kontsernisisese kulu tegelikud näitajad** sünkroonitakse Finance and Operationsiga, peate teisendama **lepinguorganisatsiooni üksuse** Finance and Operationsis õigeks **juriidiliseks isikuks**. Projekti tegelike näitajate (Project Service Automationist Finance and Operationsisse) mallil on demoandmete põhjal määratletud tingimuslik veerg. Peate värskendama viimati sisestatud tingimusveergu õigete juriidiliste isikutega. Selle tegemata jätmine võib anda kas integratsioonitõrke või valede tegelike näitajate kannete importimise Finance and Operationsisse.
- Kui **kontsernisisese aja või kontsernisisese kulu tegelikke näitajaid** Finance and Operationsiga ei sünkroonita, peate viimati sisestatud tingimusveeru oma mallist kustutama. Selle tegemata jätmine võib anda kas integratsioonitõrke või valede tegelike näitajate kannete importimise Finance and Operationsisse.

### <a name="contract-organizational-unit"></a>Lepinguorganisatsiooni üksus
Sisestatud tingimusveeru värskendamiseks mallis klõpsake noolt **Vastendus**, et avada vastendus. Valige suvandi Täpsem päring ja filtreerimine avamiseks.
- Kui kasutate Microsoft Projecti tegelike näitajate (Project Service Automationist Finance and Operationsisse) vaikemalli, valige viimane **Sisestatud tingimus** jaotises **Rakendatud etapid**. Asendage kirjes **Funktsioon** sõne **USSI** selle **juriidilise isiku** nimega, mida tuleb integratsioonis kasutada. Lisage vajadust mööda lisatingimused kirjesse **Funktsioon** ja värskendage tingimus **muidu** väärtuselt **USMF** õigele **juriidilisele isikule**.
- Uue malli loomisel peate lisama selle veeru kontsernisisese aja ja kulu toetamiseks. Valige suvand **Lisa tingimusveerg** ja andke veerule nimi, nt JuriidilineIsik. Sisestage veerule tingimus, kus kui msdyn_contractorganizationalunitid.msdyn_name on <organizational unit>, siis <enter the Legal entity>; muidu null.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmisel joonisel on toodud näide malliülesande vastendusest andmeintegratsioonis. Vastendamine näitab välja teavet. mis sünkroonitakse Project Service Automationist Finance and Operationsisse.

[![Malli vastendamine](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Malli vastendamine](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table"></a>Impordi vahetabelist

Vahetabelist importimise perioodiline protsess tuleb käivitada pärast tegelike näitajate sünkroonimist Project Service Automationist Finance and Operationsisse. See protsess impordib projektikanded vahetabelist Project Service Automationi integratsiooni töölehele, kus rakendatakse raamatupidamine ja kuhu saab sisestada imporditud kandeid. Soovitatav on käitada seda protsessi pakettrežiimis ja soovi korral on võimalik seadistada käitus korduva pakett-tööna.

## <a name="update-actuals"></a>Tegelike näitajate värskendamine

Sisestatud projektikannete kandenumbri ja käibemaksu sünkroonimiseks Finance and Operationsist Project Service Automationisse kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

-  **Andmeintegratsioon malli nimi:** projekti tegelike näitajate värskendus (Finance and Operationsist Project Service Automationisse)
-  **Ülesannete nimed projektis:** 
     - Tegelikud 
     - TransactionConnections

## <a name="entity-set"></a>Üksuste komplekt

| Finance and Operations                                         | Project Service Automation        |
|----------------------------------------------------------------|-----------------------------------|
| Projekti tegelike väärtuste integratsiooniüksus                         | Tegelikud                           |
| Projekti kande seoste integratsiooniüksus       | Kandeühendused           |

## <a name="entity-flow"></a>Üksuse voog

Projekti tegelikke näitajaid hallatakse Project Service Automationis ja need sünkroonitakse Finance and Operationsisse projekti integratsiooni töölehele. Kui tegelikud näitajad on Finance and Operationsisse sisestatud, värskendatakse neid Project Service Automationis kandenumbriga Finance and Operationsist. Kui Finance and Operationsis lisati käibemaks, luuakse Project Service Automationis uued maksu tegelikud näitajad.

## <a name="power-query"></a>Power Query

Peate kasutama Microsoft Power Queryt projekti tegelike näitajate värskendamise mallis järgmisel otstarbel.
- Finance and Operationsi **kandetüübi** teisendamine õigeks **kandetüübiks** Project Service Automationis. Projekti tegelike näitajate värskenduse (Finance and Operationsist Project Service Automationisse) mallil on see teisendus juba määratletud.
- Finance and Operationsi **arveldustüübi** teisendamine õigeks **arveldustüübiks** Project Service Automationis. Projekti tegelike näitajate värskenduse (Finance and Operationsist Project Service Automationisse) mallil on see teisendus juba määratletud.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmisel joonisel on toodud näited malliülesande vastendustest andmeintegratsioonis. Vastendamine näitab välja teavet. mis sünkroonitakse Finance and Operationsist Project Service Automationisse.

[![Malli vastendamine](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Malli vastendamine](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)




