---
title: "Kanban tööde planeerimisega kulusäästlik töötamine"
description: "Selles artiklis antakse teavet visuaalse kontrolli kohta kanban-tööde ajastamisel ja kanban-tööde ajastamise erinevate viiside kohta."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-02-24 15 - 02 - 36
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KanbanBoardScheduleJobForward, KanbanBoardShowJobs, KanbanJobSchedulingListPage
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 52961
ms.assetid: fe3b4822-6140-4b02-bebb-1fc17be2bce8
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 062cbbc8a4fd3b4dc738f24ee0606a3741736377
ms.lasthandoff: 03/29/2017


---

# <a name="kanban-job-scheduling-for-lean-manufacturing"></a>Kanban tööde planeerimisega kulusäästlik töötamine

Selles artiklis antakse teavet visuaalse kontrolli kohta kanban-tööde ajastamisel ja kanban-tööde ajastamise erinevate viiside kohta.  

Leht **Kanban-töö planeerimine** pakub visuaalset kontrolli lean manufacturingi töörakkude graafikute üle. See annab ülevaate kõikidest kanban-töödest ja pakub mitmeid filtreerimisvõimalusi. Sellelt lehelt saate liikuda kõikidele muudele lehtedele, mis on seotud kanbani konfiguratsiooni ja käivitamisega.

## <a name="automatic-scheduling-of-kanban-jobs"></a>Kanban-tööde automaatne planeerimine
Planeerimise saab käivitada automaatselt kui on **automaatne planeerimine kogus** parameeter kanban reegli. Kui seate **automaatne planeerimine kogus** et **1**, iga kanban töö on planeeritud kohe see loomise. Tulemuseks on tõmbasmiste järjekorras täidetud operatsioonide seeria. Kui määrate parameetrile **Automaatse plaanimise kogus** väärtuse, mis on suurem kui 1, rühmitatakse kanban-tööd enne plaanimist. See idee võimaldab kanbani suurusi vähendada allapoole tegelikke majanduslikke partiisuurusi. Näiteks on kindla kauba (või kauba tootepere) majandusliku suurusega 30. Kasutada toote kogust, 30, kanbans loomise asemel saate konfigureerida kanban reegel, et tal toote kogusest 10 ja on ** automaatne planeerimine kogus ** väärtus **3**. Ehkki automaatne plaanimine ajastab kanban-tööd tööraku jaoks ainult siis, kui olemas on kolm plaanimata tööd, on plaanijale ja tööde järelevaatajale täiesti nähtav, et kaks plaanimata tööd võivad täitmist oodata. Plaanija või tööde juhataja saab siis viia need kaks tööd tootmisse, plaanides need käsitsi või luues täiendavaid kanbane.

## <a name="manual-scheduling"></a>Käsitsi plaanimine
Käsitsi plaanimiseks võttis Microsoft Dynamics AX 2012 kasutusele kanbani plaanimise tahvli. Käsitsi plaanimise saab ühendada automaatse plaanimisega. Kanbani plaanimistahvel võimaldab teil töid plaanida ja plaanidest eemaldada, järjestada neid või teisaldada neid perioodist perioodi. Kanban-reeglil põhinevaid töid, mille puhul parameetri **Automaatne plaanimine** väärtus on suurem kui **0**, saab käsitsi plaanidest eemaldada. Kuid neid töid plaanitakse uuesti, kui ilmneb järgmine automaatne plaanimine (st kui luuakse uus kanban). Käsitsi plaanimiseks on saadaval järgmised suvandid.

-   **Graafik** plaanib valitud töid vastavalt nende tähtajale. (See suvand sarnaneb automaatse plaanimisega.)
-   **Ajakavasta kuupäevast edasi** püüab ajastada valitud tööd vastavalt nende tähtajale, kuid piirab tulemust, kasutades määratud varaseimat alguskuupäeva.
-   **Tagasi** teisaldab valitud ajastatud tööd tagasi perioodi järjestusse.
-   **Edasi** teisaldab valitud ajastatud tööd edasi perioodi järjestusse.
-   **Eelmine periood** teisaldab valitud ajastatud tööd eelmise perioodi algusesse või lõppu.
-   **Järgmine periood** teisaldab valitud ajastatud tööd järgmise perioodi algusesse või lõppu.
-   **Plaan**&gt;**tagasi töö olek** saate unschedule plaanitud projekti.

## <a name="lean-scheduling-groups"></a>Säästliku plaanimise grupid
Iga värv esindab säästliku plaanimise gruppi. Säästliku plaanimise gruppe saab vabalt määratleda üldiste gruppidena või ühele töörakule kuuluvate gruppidena. Kaupu ja dimensioone saab vabalt graafiku gruppidele määrata. Näiteks rakus Värvimine võib graafiku grupp esindada toote värvi. Töö puhul, mis põhineb kindlatel tööriistanõuetel, võidakse kaupu rühmitada tööriista nõude alusel, ja pakendamise töörakk võib rühmitada kaupu pakendamismalli järgi. Säästliku graafiku gruppide jaoks värvide kasutamine on valikuline, kuid soovitatav. See parandab nähtavust plaani olek. Näiteks on väga lihtne näha, milliseid värve toodetakse millise päevaga ning võite öelda lühidalt, kuidas see töö saab optimeerida.

## <a name="work-cell-capacity-and-period-capacity"></a>Tööraku võimsus ja perioodi võimsus
Säästliku tööraku võimsus on alati samaaegne võimsus. Teisisõnu saab töörakus olla samaaegselt mitu aktiivset tööd. Võimsust saab jälgida kahes režiimis: läbilaskevõime ja tunnid.

### <a name="throughput"></a>Läbilaskevõime

Tööraku võimsust määratletakse viiteperioodi (standardne tööpäev, nädal või kuu) keskmise läbilaskevõime koguse järgi. Tegelik võimsus päeva või nädala kohta arvutatakse siis töörakule määratud kalendri tööaegade alusel. Töö laaditud võimsus on töö kogus, mida on korrigeeritud töörakus oleva kauba läbilaskemääraga.

### <a name="hours"></a>Tunnid

Saadaoleva võimsuse päeva või nädala järgi määratleb töörakule määratud kalender. Töö laaditud võimsus on tegevuse tsükli aeg, mida on korrigeeritud töörakus oleva kauba koguse (tegevuse vaikekogus vs tegelik töö kogus) ja läbilaskemääraga.

#### <a name="period-capacity-factbox"></a>Perioodi võimsuse kiirinfo

Loendileht **Kanban-töö plaanimine** sisaldab kiirinfot, mis näitab valitud tööraku saadaolevat ja reserveeritud perioodi võimsust. Tootmisvoo mudelis valitud graafikuperioodidest olenevalt näitavad perioodid kas päevi või nädalaid.

<a name="see-also"></a>Vt ka
--------


