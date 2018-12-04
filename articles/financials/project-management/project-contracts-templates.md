---
title: "Projektilepingute ja projektide sünkroonimine otse Project Service Automationist rakendusse Finance and Operations"
description: "See teema kirjeldab malle ja aluseks olevaid ülesandeid, mida kasutatakse projektilepingute ja projektide sünkroonimiseks rakendusest Microsoft Dynamics 365 for Project Service Automation otse rakendusse Microsoft Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 10/25/2018
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
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: 0889bc233674cb80dd056ac77edb5c936c6633a7
ms.contentlocale: et-ee
ms.lasthandoff: 11/01/2018

---

# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Projektilepingute ja projektide sünkroonimine otse Project Service Automationist rakendusse Finance and Operations

[!include[banner](../includes/banner.md)]

See teema kirjeldab malle ja aluseks olevaid ülesandeid, mida kasutatakse projektilepingute ja projektide sünkroonimiseks rakendusest Microsoft Dynamics 365 for Project Service Automation otse rakendusse Microsoft Dynamics 365 for Finance and Operations.

> [!NOTE] 
> Kui kasutate rakendust Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0, peate installima KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Andmevoog Project Service Automationist Finance and Operationsisse

> [!NOTE]
> Enne kui saate kasutada Project Service Automationist Finance and Operationsisse integreerimise lahendust, peate olema tuttav Microsoft Dynamics 365 andmeintegratsiooni funktsiooniga.

Project Service Automationist Finance and Operationsisse integreerimise lahendus kasutab andmete sünkroonimiseks Project Service Automationi ja Finance and Operationsi eksemplaride vahel andmeintegratsiooni funktsiooni. Andmeintegratsiooni funktsiooniga saadaolev integratsioonimall võimaldab andmevoogu projektilepingute, projektide, projektilepingu ridade ja projektilepingu rea vahekokkuvõtete kohta Project Service Automationist Finance and Operationisse.

Järgmine joonis näitab, kuidas sünkroonitakse andmeid Project Service Automationi ja Finance and Operationsi vahel.

[![Andmevoog Project Service Automationi integreerimiseks Finance and Operationsiga](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Mallid ja ülesanded

Saadaolevatele mallidele juurdepääsuks valige Microsoft PowerAppsi halduskeskuses suvand **Projektid** ja seejärel valige paremast ülanurgast suvand **Uus projekt**, et valida avalikud mallid.

Projektilepingute ja projektide sünkroonimiseks Project Service Automationist Finance and Operationsisse kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

- **Andmeintegratsioon malli nimi:** projektid ja lepingud (Project Service Automationist Finance and Operationsisse)
- **Ülesannete nimed projektis:**

    - Projektilepingud Project Service Automationist Finance and Operationsisse
    - Projektid Project Service Automationist Finance and Operationsisse
    - Projektilepingute read Project Service Automationist Finance and Operationsisse
    - Projektilepingute ridade vahekokkuvõtted Project Service Automationist Finance and Operationsisse

Enne projektilepingute ja projektide sünkroonimist peate sünkroonima kontod.

## <a name="entity-set"></a>Üksuste komplekt

| Project Service Automation       | Finance and Operations                                 |
|----------------------------------|--------------------------------------------------------|
| Tellimused                           | Projektilepingu integratsiooniüksus                |
| Projektid                         | Projekti integratsiooniüksus                         |
| Tellimuse read                      | Projekti lepingurea integratsiooniüksus           |
| Projektilepingu rea vahekokkuvõtted | Projekti lepingurea vahekokkuvõtte integratsiooniüksus |

## <a name="entity-flow"></a>Üksuse voog

Projektilepinguid hallatakse Project Service Automationis ja need sünkroonitakse Finance and Operationsiga projektilepingutena. Integratsioonimalli osana saate määrata Finance and Operationsis projektilepingule integratsiooniallika.

Aja- ja materjalikulu projekte ning fikseeritud hinnaga projekte hallatakse Project Service Automationis ja need sünkroonitakse Finance and Operationsisse projektidena. Integratsioonimalli osana saate määrata Finance and Operationsis projektile integratsiooniallika.

Projektilepingu ridu hallatakse Project Service Automationis ja need sünkroonitakse Finance and Operationsisse projektilepingu arveldusreeglitena. Kui arveldusmeetod erineb vaike-projektitüübist, värskendab sünkroonimine lepingurea projekti ja projektirühma projektitüüpi.

Projektilepingu rea vahekokkuvõtteid hallatakse Project Service Automationis ja need sünkroonitakse Finance and Operationsisse projektilepingu arveldusreegli vahekokkuvõtetena.

## <a name="project-service-automation-to-finance-and-operations-integration-solution"></a>Project Service Automationi Finance and Operationsiga integratsiooni lahendus

Väli **Projektilepingu ID** on saadaval lehel **Projektilepingud**. See väli on loomulik ja kordumatu võti, et toetada integratsiooni.

Kui uue projektilepingu loomisel ei ole atribuudi **Projektilepingu ID** väärtust veel olemas, luuakse see automaatselt numbriseeriat kasutades. Väärtus sisaldab sõnet **ORD**, millele järgneb suurenev numbriseeria ja seejärel kuuest tähemärgist koosnev järelliide. Siin on näide: **ORD-01022-Z4M9Q0**.

Väli **Projekti number** on saadaval lehel **Projektid**. See väli on loomulik ja kordumatu võti, et toetada integratsiooni.

Kui uue projekti loomisel ei ole atribuudi **Projekti number** väärtust veel olemas, luuakse see automaatselt numbriseeriat kasutades. Väärtus sisaldab sõnet **PRJ**, millele järgneb suurenev numbriseeria ja seejärel kuuest tähemärgist koosnev järelliide. Siin on näide: **PRJ-01049-CCNID0**.

Kui Project Service Automation Finance and Operationsi integratsiooni lahendus on rakendatud<TO DO: link in the top level document link where we will be adding the instructions for applying the PSA solution>, määrab täiendusskript välja **Projektilepingu ID** olemasolevatele projektilepingutele ja välja **Projekti number** olemasolevatele projektidele Project Service Automationis.

## <a name="prerequisites-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

- Enne projektilepingute ja projektide sünkroonimist peate sünkroonima kontod.
- Lisage oma ühendusekogumis atribuudi **msdyn\_organizationalunits** väljale **msdyn\_name \[Nimi\]** integratsioonivõtme väljavastendus. Esmalt peate ühendusekogumile projekti lisama. Lisateabe saamiseks vt [Andmete integreerimine teenusesse Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).
- Lisage oma ühendusekogumis atribuudi **msdyn\_projects** väljale **msdynce\_projectnumber \[Projekti number\]** integratsioonivõtme väljavastendus. Esmalt peate ühendusekogumile projekti lisama. Lisateabe saamiseks vt [Andmete integreerimine teenusesse Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).
- Projektilepingute ja projektide atribuudi **SourceDataID** saab värskendada muule väärtusele või vastendusest eemaldada. Malli vaikeväärtus on **Project Service Automation**.
- Atribuudi **PaymentTerms** vastendust tuleb värskendada, nii et see kajastaks kehtivaid maksetingimusi Finance and Operationsis. Samuti saate vastenduse projektiülesandest eemaldada. Vaikeväärtuste kaardil on demoandmete jaoks vaikeväärtused. Järgmises tabelis on näidatud väärtused Project Service Automationis.

    | Väärtus | Kirjeldus   |
    |-------|---------------|
    | 1     | Neto 30        |
    | 2     | 2%10, neto 30 |
    | 3     | Neto 45        |
    | 4     | Neto 60        |

## <a name="power-query"></a>Power Query

Peate kasutama andmete filtreerimiseks Microsoft Power Queryt Exceli jaoks, kui täidetud on järgmised tingimused.

- Teil on rakenduses Microsoft Dynamics 365 for Sales müügitellimusi.
- Teil on Project Service Automationis mitu organisatsiooniüksust, mis vastendatakse Finance and Operationsis mitme juriidilise isikuga.

Kui peate kasutama Power Queryt, järgige järgmisi juhtnööre.

- Projektide ja lepingute (Project Service Automationist Finance and Operationsisse) mallil on vaikefilter, mis hõlmab ainult müügitellimusi tüübiga **Tööüksus (msdyn\_ordertype = 192350001)**. See filter aitab tagada, et Finance and Operationsis ei looda müügitellimuste jaoks projektilepinguid. Kui loote oma malli, peate selle filtri lisama.
- Peate looma Power Query filtri, mis hõlmab ainult lepinguorganisatsioone, mis tuleb sünkroonida integratsiooni ühendusekogumi juriidilise isikuga. Näiteks tuleb projektilepingud, mis teil on lepinguorganisatsiooni üksusega Contoso US, sünkroonida juriidilise isikuga USSI, kuid projektilepingud, mis teil on lepinguorganisatsiooni üksusega Contoso Global, tuleb sünkroonida juriidilise isikuga USMF. Kui te seda filtrit oma ülesandevastendusele ei lisa, sünkroonitakse kõik projektilepingud ühendusekogumi jaoks määratletud juriidilise isikuga olenemata lepinguorganisatsiooni üksusest.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

> [!NOTE] 
> Projektilepingute vaikevastendus ei sisalda välju **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** ja **AddressZipCode**. Saate vastendusi lisada, kui soovite, et need andmed sünkroonitakse projektilepingutega.
>
> Projektide vaikevastendus ei sisalda välju **Kirjeldus**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** ja **ProjectType**. Saate vastendusi lisada, kui soovite, et need andmed sünkroonitakse projektidega.

Järgmisel joonisel on toodud näited malliülesande vastendustest andmeintegratsioonis. Vastendamine näitab välja teavet. mis sünkroonitakse Project Service Automationist Finance and Operationsisse.

[![Malli vastendamine](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Malli vastendamine](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Malli vastendamine](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Malli vastendamine](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

