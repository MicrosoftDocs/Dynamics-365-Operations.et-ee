---
title: "Projekti tegelike näitajate sünkroonimine otse Project Service Automationist projekti integratsiooni töölehele Finance and Operationsis sisestamiseks"
description: "See teema kirjeldab malle ja aluseks olevaid ülesandeid, mida kasutatakse projekti tegelike näitajate sünkroonimiseks otse rakendusest Microsoft Dynamics 365 for Project Service Automation rakendusse Microsoft Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 0a965e8de596decf39a15977e6df8a6aa9dd35b0
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Projekti tegelike näitajate sünkroonimine otse Project Service Automationist projekti integratsiooni töölehele Finance and Operationsis sisestamiseks

[!include[banner](../includes/banner.md)]

See teema kirjeldab malle ja aluseks olevaid ülesandeid, mida kasutatakse projekti tegelike näitajate sünkroonimiseks otse rakendusest Microsoft Dynamics 365 for Project Service Automation rakendusse Microsoft Dynamics 365 for Finance and Operations.

Mall sünkroonib kanded Project Service Automationist Finance and Operationsi vahetabelisse. Kui sünkroonimine on lõpule jõudnud, **peate** importima andmed vahetabelist integratsiooni töölehele.

> [!NOTE]
> - Projekti tegelike näitajate integratsioon on saadaval rakenduse Microsoft Dynamics 365 for Finance and Operations versioonis 8.01 või uuemas.
> - Kui kasutate rakendust Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0, saate pärast KB 4132657 ja KB 4132660 installimist kasutada malle projektiülesannete, kulukannete kategooriate, tunnihinnangute, kuluhinnangute ja tegelike näitajate integreerimiseks ning funktsionaalsuse lukustamise konfigureerimiseks. Kui peate lähtestama arvestuse jaotusi, soovitame installida KB 4131710.
> - Kui kasutate rakendust Finance and Operations 7.3.0 ja toote tasukanded rakendusest Project Service Automation üle, peate installima KB 4345320, et need tasud projekti arvesse kaasata.
> - Kui sisestate Project Service Automationis käibemaksusummasid aja- või kulukannete kohta, peate installima Project Service Automationi värskenduse 7. Vastasel juhul ei lingita maksu tegelikke näitajaid seostatud aja- või kuluandmete tegelike näitajatega ega sünkroonita rakendusse Finance and Operations. Lisateabe saamiseks võtke ühendust tugiteenusega.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Andmevoog Project Service Automationist Finance and Operationsisse

Project Service Automationist Finance and Operationsisse integreerimise lahendus kasutab andmete sünkroonimiseks Project Service Automationi ja Finance and Operationsi eksemplaride vahel andmeintegratsiooni funktsiooni. Andmeintegratsiooni funktsioonis saadaolevad integratsioonimallid võimaldavad andmevoogu projekti tegelike näitajate kohta Project Service Automationist Finance and Operationsisse.

Järgmine joonis näitab, kuidas sünkroonitakse andmeid Project Service Automationi ja Finance and Operationsi vahel.

[![Andmevoog Project Service Automationi integreerimiseks Finance and Operationsiga](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Projekti tegelikud näitajad rakendusest Project Service Automation

### <a name="template-and-tasks"></a>Mall ja ülesanded

Saadaolevatele mallidele juurdepääsuks valige Microsoft PowerAppsi halduskeskuses suvand **Projektid** ja seejärel valige paremast ülanurgast suvand **Uus projekt**, et valida avalikud mallid.

Projekti tegelike näitajate sünkroonimiseks Project Service Automationist Finance and Operationsisse kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

- **Andmeintegratsioon malli nimi:** projekti tegelikud näitajad (Project Service Automationist Finance and Operationsisse)
- **Ülesannete nimed projektis:**

    - Tegelikud
    - TransactionConnections

### <a name="entity-set"></a>Üksuste komplekt

| Project Service Automation | Finance and Operations                                   |
|----------------------------|----------------------------------------------------------|
| Tegelikud                    | Projekti tegelike väärtuste integratsiooniüksus                   |
| Kandeühendused    | Projekti kande seoste integratsiooniüksus |

### <a name="entity-flow"></a>Üksuse voog

Projekti tegelikke näitajaid hallatakse rakenduses Project Service Automation ja need sünkroonitakse projekti integratsiooni töölehele rakenduses Finance and Operations. Raamatupidamine rakendatakse vaike-finantsdimensioonide ja sisestuse seadistuse alusel.

### <a name="prerequisites"></a>Eeltingimused

Enne tegelike näitajate sünkroonimist peate konfigureerima Project Service Automationi integratsiooniparameetrid ja sünkroonima projektid, projektiülesanded ning projekti kulukande kategooriad.

### <a name="power-query"></a>Power Query

Projekti tegelike näitajate mallis peate kasutama Microsoft Power Queryt Exceli jaoks, et täita järgmised ülesanded.

- Project Service Automationis kandetüübi teisendamine õigeks kandetüübiks Finance and Operationsis. See teisendus on juba määratletud projekti tegelike näitajate (Project Service Automationist Finance and Operationsisse) mallis.
- Project Service Automationis arveldustüübi teisendamine õigeks arveldustüübiks Finance and Operationsis. See teisendus on juba määratletud projekti tegelike näitajate (Project Service Automationist Finance and Operationsisse) mallis. Seejärel vastendatakse arveldustüüp rea atribuudiga rakenduse **Project Service Automation integratsiooniparameetrite** lehel oleva konfiguratsiooni põhjal.
- Filtreerimine kindlate ressursi organisatsiooniüksuste alusel, mis tuleb selle malliga sünkroonida.
- Kui kontsernisisese aja või kontsernisisese kulu tegelikud näitajad sünkroonitakse Finance and Operationsiga, peate teisendama lepinguorganisatsiooni üksuse Finance and Operationsis õigeks juriidiliseks isikuks. Projekti tegelike näitajate (Project Service Automationist Finance and Operationsisse) mallis on demoandmete põhjal määratletud tingimuslik veerg. Peate värskendama viimati sisestatud tingimusveergu õigete juriidiliste isikutega. Vastasel korral võib esineda integratsioonitõrge või Finance and Operationsisse võidakse importida valed tegelikud näitajad.
- Kui kontsernisisese aja või kontsernisisese kulu tegelikke näitajaid ei sünkroonita Finance and Operationsiga, peate viimati sisestatud tingimusveeru oma mallist kustutama. Vastasel korral võib esineda integratsioonitõrge või Finance and Operationsisse võidakse importida valed tegelikud näitajad.

#### <a name="contract-organizational-unit"></a>Lepinguorganisatsiooni üksus
Sisestatud tingimusveeru värskendamiseks mallis klõpsake noolt **Vastendus**, et avada vastendus. Valige link **Täpsem päring ja filtreerimine**, et avada Power Query.

- Kui kasutate Projecti tegelike näitajate (Project Service Automationist Finance and Operationsisse) vaikemalli, valige rakenduses Power Query viimane **Sisestatud tingimus** jaotisest **Rakendatud etapid**. Asendage kirjes **Funktsioon** sõne **USSI** selle juriidilise isiku nimega, mida tuleb integratsioonis kasutada. Lisage vajadust mööda lisatingimused kirjesse **Funktsioon** ja värskendage tingimus **else** väärtuselt **USMF** õigele juriidilisele isikule.
- Uue malli loomisel peate lisama selle veeru, et toetada kontsernisisest aega ja kulu. Valige suvand **Lisa tingimusveerg** ja sisestage veerule nimi, nt **JuriidilineIsik**. Sisestage veerule tingimus, kus kui **msdyn\_contractorganizationalunitid.msdyn\_name** on \<organisatsiooniüksus\>, siis \<sisestage juriidiline isik\>, muidu null.

### <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmistel joonistel on toodud näide malliülesande vastendusest andmeintegratsioonis. Vastendamine näitab välja teavet. mis sünkroonitakse Project Service Automationist Finance and Operationsisse.

[![Malli vastendamine](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Malli vastendamine](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Vahetabelist importimine pärast rakendusest Project Service Automation integreerimist

Vahetabelist importimise perioodiline protsess tuleb käivitada pärast tegelike näitajate sünkroonimist Project Service Automationist Finance and Operationsisse. See protsess impordib projektikanded vahetabelist Project Service Automationi integratsiooni töölehele, kus rakendatakse raamatupidamine ja kuhu saab sisestada imporditud kandeid. Soovitame käitada seda protsessi pakettrežiimis ja soovi korral on võimalik seadistada käitus korduva pakett-tööna.

## <a name="update-actuals-from-finance-and-operations"></a>Tegelike näitajate värskendamine rakendusest Finance and Operations

### <a name="template-and-tasks"></a>Mall ja ülesanded

Sisestatud projektikannete kandenumbri ja käibemaksu sünkroonimiseks Finance and Operationsist Project Service Automationisse kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

- **Andmeintegratsioon malli nimi:** projekti tegelike näitajate värskendus (Finance and Operationsist Project Service Automationisse)
- **Ülesannete nimed projektis:**

    - Tegelikud 
    - TransactionConnections

### <a name="entity-set"></a>Üksuste komplekt

| Finance and Operations                                   | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Projekti tegelike väärtuste integratsiooniüksus                   | Tegelikud                    |
| Projekti kande seoste integratsiooniüksus | Kandeühendused    |

### <a name="entity-flow"></a>Üksuse voog

Projekti tegelikke näitajaid hallatakse rakenduses Project Service Automation ja need sünkroonitakse projekti integratsiooni töölehele rakenduses Finance and Operations. Kui tegelikud näitajad on Finance and Operationsisse sisestatud, värskendatakse neid Project Service Automationis kandenumbriga Finance and Operationsist. Kui Finance and Operationsis lisati käibemaksud, luuakse Project Service Automationis uued maksu tegelikud näitajad.

### <a name="power-query"></a>Power Query

Projekti tegelike näitajate värskendamise mallis peate kasutama Power Queryt, et täita järgmised ülesanded.

- Finance and Operationsis kandetüübi teisendamine õigeks kandetüübiks Project Service Automationis. See teisendus on juba määratletud projekti tegelike näitajate värskenduse (Project Service Automationist Finance and Operationsisse) mallis.
- Finance and Operationsis arveldustüübi teisendamine õigeks arveldustüübiks Project Service Automationis. See teisendus on juba määratletud projekti tegelike näitajate värskenduse (Project Service Automationist Finance and Operationsisse) mallis.

### <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmisel joonisel on toodud näited malliülesande vastendustest andmeintegratsioonis. Vastendamine näitab välja teavet. mis sünkroonitakse Finance and Operationsist Project Service Automationisse.

[![Malli vastendamine](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Malli vastendamine](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)

