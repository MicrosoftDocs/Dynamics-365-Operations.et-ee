---
title: Projekti tegelike näitajate sünkroonimine otse Project Service Automationist projekti integratsiooni töölehele Finance and Operationsis sisestamiseks
description: Selles teemas kirjeldatakse malle ja aluseks olevaid ülesandeid, mida kasutatakse projekti tegelike näitajate sünkroonimiseks rakendusest Microsoft Dynamics 365 Project Service Automation otse rakendusse Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0aeaa1ee4c35ca42a5382b3c7ff3519cba52996c
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250526"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Projekti tegelike näitajate sünkroonimine otse Project Service Automationist projekti integratsiooni töölehele Finance and Operationsis sisestamiseks

[!include[banner](../includes/banner.md)]

Selles teemas kirjeldatakse malle ja aluseks olevaid ülesandeid, mida kasutatakse projekti tegelike näitajate sünkroonimiseks rakendusest Dynamics 365 Project Service Automation otse rakendusse Dynamics 365 Finance.

Mall sünkroonib kanded Project Service Automationist Finance’i vahetabelisse. Kui sünkroonimine on lõpule jõudnud, **peate** importima andmed vahetabelist integratsiooni töölehele.

> [!NOTE]
> - Projekti tegelike näitajate integratsioon on saadaval rakenduse versioonis 8.0.1 või uuemas.
> - Kui kasutate rakendust Enterprise Edition 7.3.0, saate pärast KB 4132657 ja KB 4132660 installimist kasutada projektiülesannete, kulukannete kategooriate, tunnihinnangute, kuluhinnangute ja tegelike näitajate integreerimiseks ning funktsionaalsuse lukustamise konfigureerimiseks malle. Kui peate lähtestama arvestuse jaotusi, soovitame installida KB 4131710.
> - Kui kasutate versiooni 7.3.0 ja toote tasukanded rakendusest Project Service Automation üle, peate installima KB 4345320, et need tasud projekti arvesse kaasata.
> - Kui sisestate Project Service Automationis käibemaksusummasid aja- või kulukannete kohta, peate installima Project Service Automationi värskenduse 7. Vastasel juhul ei lingita maksu tegelikke näitajaid seostatud aja- või kuluandmete tegelike näitajatega ega sünkroonita rakendusse Finance. Lisateabe saamiseks võtke ühendust tugiteenusega.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automationi andmevoog rakendusse Finance

Rakendusest Project Service Automation rakendusse Finance integratsiooni lahendus kasutab andmeintegratsiooni funktsiooni, et sünkroonida andmeid Project Service Automationi ja Finance’i eksemplaride vahel. Andmeintegratsiooni funktsioonis saadaolevad integratsioonimallid võimaldavad andmevoogu projekti tegelike näitajate kohta Project Service Automationist rakendusse Finance.

Järgmine illustratsioon näitab, kuidas andmeid Project Service Automationi ja Finance’i vahel sünkroonitakse.

[![Andmevoog Project Service Automationi integreerimiseks Finance and Operationsiga](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Projekti tegelikud näitajad rakendusest Project Service Automation

### <a name="template-and-tasks"></a>Mall ja ülesanded

Saadaolevatele mallidele juurdepääsuks valige Microsoft PowerAppsi halduskeskuses suvand **Projektid** ja seejärel valige paremast ülanurgast suvand **Uus projekt**, et valida avalikud mallid.

Projekti tegelike näitajate sünkroonimiseks Project Service Automationist rakendusse Finance kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

- **Andmeintegratsioon malli nimi:** projekti tegelikud näitajad (Project Service Automationist Finance and Operationsisse)
- **Ülesannete nimed projektis:**

    - Tegelikud
    - TransactionConnections

### <a name="entity-set"></a>Üksuste komplekt

| Project Service Automation | Finantsid                                   |
|----------------------------|----------------------------------------------------------|
| Tegelikud                    | Projekti tegelike väärtuste integratsiooniüksus                   |
| Kandeühendused    | Projekti kande seoste integratsiooniüksus |

### <a name="entity-flow"></a>Üksuse voog

Projekti tegelikke näitajaid hallatakse rakenduses Project Service Automation ja need sünkroonitakse projekti integratsiooni töölehele rakenduses Finance. Raamatupidamine rakendatakse vaike-finantsdimensioonide ja sisestuse seadistuse alusel.

### <a name="prerequisites"></a>Eeltingimused

Enne tegelike näitajate sünkroonimist peate konfigureerima Project Service Automationi integratsiooniparameetrid ja sünkroonima projektid, projektiülesanded ning projekti kulukande kategooriad.

### <a name="power-query"></a>Power Query

Projekti tegelike näitajate mallis peate kasutama Microsoft Power Queryt Exceli jaoks, et täita järgmised ülesanded.

- Project Service Automationis kandetüübi teisendamine õigeks kandetüübiks rakenduses Finance. See teisendus on juba määratletud projekti tegelike näitajate (Project Service Automationist Finance and Operationsisse) mallis.
- Project Service Automationis arveldustüübi teisendamine õigeks arveldustüübiks rakenduses Finance. See teisendus on juba määratletud projekti tegelike näitajate (Project Service Automationist Finance and Operationsisse) mallis. Seejärel vastendatakse arveldustüüp rea atribuudiga rakenduse **Project Service Automation integratsiooniparameetrite** lehel oleva konfiguratsiooni põhjal.
- Filtreerimine kindlate ressursi organisatsiooniüksuste alusel, mis tuleb selle malliga sünkroonida.
- Kui kontsernisisese aja või kontsernisisese kulu tegelikud näitajad sünkroonitakse rakendusega Finance, peate teisendama lepinguorganisatsiooni üksuse Finance’is õigeks juriidiliseks isikuks. Projekti tegelike näitajate (Project Service Automationist Finance and Operationsisse) mallis on demoandmete põhjal määratletud tingimuslik veerg. Peate värskendama viimati sisestatud tingimusveergu õigete juriidiliste isikutega. Vastasel korral võib esineda integratsioonitõrge või rakendusse Finance võidakse importida valed tegelikud näitajad.
- Kui kontsernisisese aja või kontsernisisese kulu tegelikke näitajaid ei sünkroonita Finance and Operationsiga, peate viimati sisestatud tingimusveeru oma mallist kustutama. Vastasel korral võib esineda integratsioonitõrge või rakendusse Finance võidakse importida valed tegelikud näitajad.

#### <a name="contract-organizational-unit"></a>Lepinguorganisatsiooni üksus
Sisestatud tingimusveeru värskendamiseks mallis klõpsake noolt **Vastendus**, et avada vastendus. Valige link **Täpsem päring ja filtreerimine**, et avada Power Query.

- Kui kasutate Projecti tegelike näitajate (Project Service Automationist Finance and Operationsisse) vaikemalli, valige rakenduses Power Query viimane **Sisestatud tingimus** jaotisest **Rakendatud etapid**. Asendage kirjes **Funktsioon** sõne **USSI** selle juriidilise isiku nimega, mida tuleb integratsioonis kasutada. Lisage vajadust mööda lisatingimused kirjesse **Funktsioon** ja värskendage tingimus **else** väärtuselt **USMF** õigele juriidilisele isikule.
- Uue malli loomisel peate lisama selle veeru, et toetada kontsernisisest aega ja kulu. Valige suvand **Lisa tingimusveerg** ja sisestage veerule nimi, nt **JuriidilineIsik**. Sisestage veerule tingimus, kus kui **msdyn\_contractorganizationalunitid.msdyn\_name** on \<organisatsiooniüksus\>, siis \<sisestage juriidiline isik\>, muidu null.

### <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmistel joonistel on toodud näide malliülesande vastendusest andmeintegratsioonis. Vastendamine näitab välja teavet, mis sünkroonitakse Project Service Automationist rakendusse Finance.

[![Malli vastendamine](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Malli vastendamine](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Vahetabelist importimine pärast rakendusest Project Service Automation integreerimist

Vahetabelist importimise perioodiline protsess tuleb käivitada pärast tegelike näitajate sünkroonimist Project Service Automationist rakendusse Finance. See protsess impordib projektikanded vahetabelist Project Service Automationi integratsiooni töölehele, kus rakendatakse raamatupidamine ja kuhu saab sisestada imporditud kandeid. Soovitame käitada seda protsessi pakettrežiimis ja soovi korral on võimalik seadistada käitus korduva pakett-tööna.

## <a name="update-actuals-from-finance"></a>Uuenda rakenduses Finance pärinevaid tegelikke näitajaid

### <a name="template-and-tasks"></a>Mall ja ülesanded

Sisestatud projektikannete kandenumbri ja käibemaksu sünkroonimiseks rakendusest Finance Project Service Automationisse kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

- **Andmeintegratsioon malli nimi:** projekti tegelike näitajate värskendus (Finance and Operationsist Project Service Automationisse)
- **Ülesannete nimed projektis:**

    - Tegelikud 
    - TransactionConnections

### <a name="entity-set"></a>Üksuste komplekt

| Finantsid                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Projekti tegelike väärtuste integratsiooniüksus                   | Tegelikud                    |
| Projekti kande seoste integratsiooniüksus | Kandeühendused    |

### <a name="entity-flow"></a>Üksuse voog

Projekti tegelikke näitajaid hallatakse rakenduses Project Service Automation ja need sünkroonitakse projekti integratsiooni töölehele rakenduses Finance. Kui tegelikud näitajad on rakendusse Finance sisestatud, värskendatakse neid Project Service Automationis kandenumbriga Finance’ist. Kui Finance’i lisati käibemaksud, luuakse Project Service Automationis uued maksu tegelikud näitajad.

### <a name="power-query"></a>Power Query

Projekti tegelike näitajate värskendamise mallis peate kasutama Power Queryt, et täita järgmised ülesanded.

- Project Service Automationis kandetüübi teisendamine õigeks kandetüübiks Finance’is. See teisendus on juba määratletud projekti tegelike näitajate värskenduse (Project Service Automationist Finance and Operationsisse) mallis.
- Project Service Automationis arveldustüübi teisendamine õigeks arveldustüübiks Finance’is. See teisendus on juba määratletud projekti tegelike näitajate värskenduse (Project Service Automationist Finance and Operationsisse) mallis.

### <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmisel joonisel on toodud näited malliülesande vastendustest andmeintegratsioonis. Vastendamine näitab välja teavet, mis sünkroonitakse Finance’ist rakendusse Project Service Automation.

[![Malli vastendamine](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Malli vastendamine](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)
