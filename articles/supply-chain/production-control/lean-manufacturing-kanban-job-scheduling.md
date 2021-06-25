---
title: Kanban-töö plaanimine lean manufacturingi jaoks
description: Selles artiklis antakse teavet visuaalse kontrolli kohta kanban-tööde ajastamisel ja kanban-tööde ajastamise erinevate viiside kohta.
author: cvocph
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardScheduleJobForward, KanbanBoardShowJobs, KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 52961
ms.assetid: fe3b4822-6140-4b02-bebb-1fc17be2bce8
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d0cbaf6b8440dbbb71146a34cbbe949cfe78d0c
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6190036"
---
# <a name="kanban-job-scheduling-for-lean-manufacturing"></a>Kanban-töö plaanimine lean manufacturingi jaoks

[!include [banner](../includes/banner.md)]

Selles artiklis antakse teavet visuaalse kontrolli kohta kanban-tööde ajastamisel ja kanban-tööde ajastamise erinevate viiside kohta.  

Leht **Kanban-töö planeerimine** pakub visuaalset kontrolli lean manufacturingi töörakkude graafikute üle. See annab ülevaate kõikidest kanban-töödest ja pakub mitmeid filtreerimisvõimalusi. Sellelt lehelt saate liikuda kõikidele muudele lehtedele, mis on seotud kanbani konfiguratsiooni ja käivitamisega.

## <a name="automatic-scheduling-of-kanban-jobs"></a>Kanban-tööde automaatne planeerimine
Plaanimise saab käivitada automaatselt, kui määrate kanban-reeglile parameetri **Automaatse plaanimise kogus**. Kui määrate parameetri **Automaatse plaanimise kogus** väärtuseks **1**, plaanitakse iga kanban-töö kohe selle loomisel. Tulemuseks on tõmbasmiste järjekorras täidetud operatsioonide seeria. Kui määrate parameetrile **Automaatse plaanimise kogus** väärtuse, mis on suurem kui 1, rühmitatakse kanban-tööd enne plaanimist. 

See idee võimaldab kanbani suurusi vähendada allapoole tegelikke majanduslikke partiisuurusi. Näiteks on kindla kauba (või kaubapere) tasuv partii suurus 30. Selle asemel et luua kanbane, mis kasutavad toote kogust (30), saate konfigureerida kanban-reegli, mille toote kogus on 10 ja parameetri **Automaatse plaanimise kogus** väärtus on **3**. Ehkki automaatne plaanimine ajastab kanban-tööd tööraku jaoks ainult siis, kui olemas on kolm plaanimata tööd, on plaanijale ja tööde järelevaatajale täiesti nähtav, et kaks plaanimata tööd võivad täitmist oodata. Plaanija või tööde juhataja saab siis viia need kaks tööd tootmisse, plaanides need käsitsi või luues täiendavaid kanbane.

## <a name="manual-scheduling"></a>Käsitsi plaanimine
Käsitsi plaanimiseks võttis Microsoft Dynamics AX 2012 kasutusele kanbani plaanimise tahvli. Käsitsi plaanimise saab ühendada automaatse plaanimisega. Kanbani plaanimistahvel võimaldab teil töid plaanida ja plaanidest eemaldada, järjestada neid või teisaldada neid perioodist perioodi. Kanban-reeglil põhinevaid töid, mille puhul parameetri **Automaatne plaanimine** väärtus on suurem kui **0**, saab käsitsi plaanidest eemaldada. Kuid neid töid plaanitakse uuesti, kui ilmneb järgmine automaatne plaanimine (st kui luuakse uus kanban). Käsitsi plaanimiseks on saadaval järgmised suvandid.

-   **Graafik** plaanib valitud töid vastavalt nende tähtajale. (See suvand sarnaneb automaatse plaanimisega.)
-   **Ajakavasta kuupäevast edasi** püüab ajastada valitud tööd vastavalt nende tähtajale, kuid piirab tulemust, kasutades määratud varaseimat alguskuupäeva.
-   **Tagasi** teisaldab valitud ajastatud tööd tagasi perioodi järjestusse.
-   **Edasi** teisaldab valitud ajastatud tööd edasi perioodi järjestusse.
-   **Eelmine periood** teisaldab valitud ajastatud tööd eelmise perioodi algusesse või lõppu.
-   **Järgmine periood** teisaldab valitud ajastatud tööd järgmise perioodi algusesse või lõppu.
-   **Plaan** &gt; **Töö oleku taastamine** võimaldab plaanitud töö graafikust eemaldada.

## <a name="lean-scheduling-groups"></a>Säästliku plaanimise grupid
Iga värv esindab säästliku plaanimise gruppi. Säästliku plaanimise gruppe saab vabalt määratleda üldiste gruppidena või ühele töörakule kuuluvate gruppidena. Kaupu ja dimensioone saab vabalt graafiku gruppidele määrata. Näiteks rakus Värvimine võib graafiku grupp esindada toote värvi. Töö puhul, mis põhineb kindlatel tööriistanõuetel, võidakse kaupu rühmitada tööriista nõude alusel, ja pakendamise töörakk võib rühmitada kaupu pakendamismalli järgi. Säästliku graafiku gruppide jaoks värvide kasutamine on valikuline, kuid soovitatav. See parandab plaani oleku nähtavust. Näiteks on väga lihtne näha, millised värvid millisel päeval loodud on, ja saate hea ülevaate, kuidas seda tööd optimeerida saab.

## <a name="work-cell-capacity-and-period-capacity"></a>Tööraku võimsus ja perioodi võimsus
Säästliku tööraku võimsus on alati samaaegne võimsus. Teisisõnu saab töörakus olla samaaegselt mitu aktiivset tööd. Võimsust saab jälgida kahes režiimis: läbilaskevõime ja tunnid.

### <a name="throughput"></a>Läbilaskevõime

Tööraku võimsust määratletakse viiteperioodi (standardne tööpäev, nädal või kuu) keskmise läbilaskevõime koguse järgi. Tegelik võimsus päeva või nädala kohta arvutatakse siis töörakule määratud kalendri tööaegade alusel. Töö laaditud võimsus on töö kogus, mida on korrigeeritud töörakus oleva kauba läbilaskemääraga.

### <a name="hours"></a>Tunnid

Saadaoleva võimsuse päeva või nädala järgi määratleb töörakule määratud kalender. Töö laaditud võimsus on tegevuse tsükli aeg, mida on korrigeeritud töörakus oleva kauba koguse (tegevuse vaikekogus vs tegelik töö kogus) ja läbilaskemääraga.

#### <a name="period-capacity-factbox"></a>Perioodi võimsuse kiirinfo

Loendileht **Kanban-töö plaanimine** sisaldab kiirinfot, mis näitab valitud tööraku saadaolevat ja reserveeritud perioodi võimsust. Tootmisvoo mudelis valitud graafikuperioodidest olenevalt näitavad perioodid kas päevi või nädalaid.

## <a name="additional-resources"></a>Lisaressursid





[!INCLUDE[footer-include](../../includes/footer-banner.md)]