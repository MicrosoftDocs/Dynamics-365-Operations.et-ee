---
title: Lean manufacturingi visuaalne plaanimine
description: Selles teemas antakse teavet Kanbani plaanimistahvli kohta, mida tootmise plaanija saab kasutada kanban-tööde puhul tootmisplaani juhtimiseks ja optimeerimiseks.
author: johanhoffmann
manager: tfehr
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoard, KanbanJobSchedulingListPage, LeanProductionFlowVisualization, KanbanBoardUnplannedJobs
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 45a63ab0f5baadf6bef646224b3f0bf5327ee923
ms.sourcegitcommit: 4a32634690a741535f3f4babfd753f7c227ad6fe
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/05/2020
ms.locfileid: "3958737"
---
# <a name="visual-scheduling-for-lean-manufacturing"></a>Lean manufacturingi visuaalne plaanimine

[!include [banner](../includes/banner.md)]

Selles teemas antakse teavet Kanbani plaanimistahvli kohta, mida tootmise plaanija saab kasutada kanban-tööde puhul tootmisplaani juhtimiseks ja optimeerimiseks.

Selles teemas antakse teavet Kanbani plaanimistahvli kohta, mida tootmise plaanija saab kasutada kanban-tööde puhul tootmisplaani juhtimiseks ja optimeerimiseks.

Kanbani plaanimistahvel võimaldab tootmise plaanijal kanban-tööde puhul tootmisplaani juhtida ja optimeerida. See muudab kanban-tööd läbipaistvaks ja annab tootmise plaanijale tööriista, mis optimeerib ja kohandab tootmisplaani lean manufacturingi tööraku puhul.

## <a name="visual-scheduling-of-kanban-jobs"></a>Kanban-tööde visuaalne plaanimine
Kanban-töö võib koosneda vähemalt ühest kanban-tööst. Kanban-töid on kaht tüüpi.

-   Töötle
-   Ülekanne

Plaanida saab ainult töid, mille tüüp on **Protsess**. Kanban-töö ja selle atribuudid, nt tegevuse aeg, määratletakse tootmise kanban-voos. Tootmise kanban-voos määratakse kanban-töö ka töörakule. Tööraku igapäevane võimsus arvutatakse ressursigrupis määratud tööraku võimsuse põhjal. Seda kohandatakse seotud kalendris igapäevase tööajaga. Kui kanban-töö on plaanitud, laadib töö tööraku võimsuse. Kanbani plaanimistahvel annab järgmised põhifunktsioonid.

-   Graafiline ülevaade tootmisplaanist säästlikus töörakus. See ülevaade näitab plaanitud kanban-protsessi töid määratletud perioodidel.
-   Tööriist, mis võimaldab plaanida plaanimata kanban-töid ja plaanida ümber varem plaanitud töid.

## <a name="kanban-schedule-board"></a>Kanbani plaanimistahvel
Lehel **Kanbani plaanimistahvel** on mitu põhielementi, mis on näidatud järgmisel illustratsioonil. 

![Kanbani plaanimistahvel](./media/kanban-schedule-board-1024x554.png)
1.  Tegumiriba
2.  Väljade filtreerimine
3.  Plaanimata tööde nupp
4.  Perioodi sõlm
5.  Kanban-töö
6.  Võimsusriba
7.  Ajaskaala

### <a name="view-the-time-scale"></a>Ajaskaala kuvamine

Tahvel on jagatud perioodideks, millest igaühte tähistab sõlm (4). Perioodi sõlmed on loetletud vertikaalteljel ja horisontaalne telg kujutab ajaskaalat (7), mis näitab perioodi pikkust. Perioodi pikkus on üks päev või üks nädal. Perioodi pikkus määratakse Kanbani plaanimistahvli (2) jaoks valitud tööraku konfiguratsiooniga. Iga perioodisõlme puhul näitab Kanbani plaanimistahvel, kui palju plaanitud kanban-tööd perioodil laadivad. Näidatud on ka perioodi maksimaalne läbilaskevõime. Kui plaanitud läbilaskevõime ületab maksimaalse läbilaskevõime, käsitletakse perioodi üle koormatuna ja kuvatakse punane hoiatussümbol. Plaanitud kanban-töö kuvatakse perioodil, millel on plaanitud algus- ja lõpuaeg (5). Töö pikkus on võrdne tegevuse ajaga. Kanban-tööd kuvatakse perioodil kattuvana, kui nende tegevuse ajad ületavad tööraku ülesande aja.

### <a name="view-job-status"></a>Töö oleku kuvamine

Lisateavet kanban-töö kohta saate kohtspikrist, mis kuvatakse, kui hoiate kursorit töö kohal. Sümbol annab teavet töö oleku kohta. Näiteks kella sümbol näitab, et kanban-töö on tähtaja ületanud.

### <a name="use-colors-to-view-the-kanban-schedule-board"></a>Värvide kasutamine Kanbani plaanimistahvli vaatamiseks

Kanbani plaanimistahvli antava ülevaate täiustamiseks võite kasutada kanban-tööde eristamiseks värve. Kanban-töö värv konfigureeritakse säästliku graafiku grupis, kus saate koondada tooteid, mis tuleks toota samas järjekorras. Nupp **Kasuta kujundusvärve** toimingupaani vahekaardil **Tahvel** võimaldab vahetada rakenduse kujunduse värve ja säästliku graafiku grupis konfigureeritud värve. Iga perioodi puhul näitab võimsusriba (6), kui palju perioodi vabu tunde on kanban-töödega laaditud. Kui periood on üle koormatud, kuvatakse võimsusriba paksemana ja punasega. Kõik need funktsioonid on saadaval toiminguriba (1) vahekaardil **Tahvel** lehe **Kanbani plaanimistahvel** ülaosas.

## <a name="plan-unplanned-jobs"></a>Plaanimata tööde plaanimine
Plaanimata kanban-töid saab plaanida dialoogiboksist **Plaanimata tööde plaanimine**. Klõpsake selle dialoogiboksi avamiseks nuppu **Plaanimata tööd**, mis näitab praegust plaanimata tööde arvu. Teine võimalus on klõpsata nuppu **Plaanimata tööde plaanimine** toimingupaani vahekaardil **Tahvel**. Dialoogiboksis kuvatakse tööraku plaanimata kanban-tööd. Võite kasutada välja **Filter** kõigi tabeli väljade filtreerimiseks. Näiteks saate filtreerida konkreetse toote kanban-tööde alusel. Kui teil on olemas filtreeritud loend töödest, mida soovite plaanida, valige need loendist ja klõpsake siis nuppu **OK**. Automaatse plaanimise kasutamiseks tööde plaanimisel määrake valiku **Automaatne plaanimine** olekuks **Jah**. Sel juhul plaanitakse tööd perioodile tähtaja järgi. Töid saab ka perioodi kaupa plaanida. Valige lihtsalt periood väljalt **Periood**. Järgmisel joonisel on näide dialoogiboksist **Plaanimata tööde plaanimine**. 

![Plaanimata tööde plaanimise dialoogiboks](./media/plan-unplanned-jobs-1024x564.png)

## <a name="sequence-kanban-jobs-within-the-same-period"></a>Kanban-tööde järjestamine samal perioodil
Saate muuta perioodil vähemalt ühe valitud töö järjestust. See funktsioon võib olla abiks, kui soovite perioodil mõningaid töid prioritiseerida. Alternatiivina võib olla vaja järjestada töö läbiviimiseks töid, millel on samad tooteatribuudid. Järjestust saab muuta pukseerimistoimingu kaudu või menüüelementide **Tagasi** ja **Edasi** kaudu toimingupaani vahekaardil **Tahvel**.

## <a name="reassign-kanban-jobs-across-periods"></a>Kanban-tööde ümbermääramine perioodide lõikes
Töid saab määrata ümber ühest perioodist teise. See funktsioon võib olla abiks, kui periood on üle koormatud ja soovite jagada koormuse ühtlaselt perioodidele, millel on vaba võimsust. Töid saab määrata ümber pukseerimistoimingu kaudu või menüüelementide **Järgmine periood** ja **Eelmine periood** kaudu toimingupaani vahekaardil **Tahvel**.

## <a name="open-the-kanban-schedule-board"></a>Kanbani plaanimistahvli avamine
Kanbani plaanimistahvli saab avada menüüelemendi abil järgmistel lehtedel.

-   Leht **Tootmisala**
-   Leht **Kanban-tööde plaanimine**
-   Leht **Tootmisvoo visualiseerimine**


<a name="additional-resources"></a>Lisaressursid
--------

[Lean manufacturingi kanban-töö plaanimine](lean-manufacturing-kanban-job-scheduling.md)

