---
title: Lean manufacturingi ülevaade
description: See artikkel annab ülevaate ja kirjeldab lean manufacturingi funktsioone rakenduses Dynamics 365 Supply Chain Management.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob, KanbanBoardWorkCell, KanbanJobSchedulingListPage, LeanProductionFlow, Kanban, KanbanQuantityOverview, KanbanAssignCard, KanbanCirculatingCards, KanbanRules, WHSKanbanWaveTableManagePickingListPool
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "19371"
- intro-internal
ms.assetid: 026c5605-6be7-4fdb-a6f2-8e37a806796c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e0c8b5ec4d4a391773e32a61a321c28868678baa
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985932"
---
# <a name="lean-manufacturing-overview"></a>Lean manufacturingi ülevaade

[!include [banner](../includes/banner.md)]

See artikkel annab ülevaate ja kirjeldab lean manufacturingi funktsioone rakenduses Dynamics 365 Supply Chain Management.

Lean manufacturing pakub tööriistu, mida saate säästlike operatsioonide modelleerimiseks kasutada. Nende tööriistad toetavad ja soodustavad järgmisi mõisteid ning äritegevusi.
-   Lean manufacturingi aluse loomine, modelleerides tootmis- ja logistikaprotsesse tootmisvoogudena.
-   Säästliku tõmbesüsteemi rakendamine, kasutades kanbane nõudluse nõuete tähistamiseks.
-   Kanban-tööde jälgimine ja haldamine.

Lean manufacturingi arhitektuur koosneb tootmisvoogudest, tegevustest ja kanban-reeglitest. Need struktuurid on Supply Chain Managementi protsessidega täielikult integreeritud. Saate kasutada lean manufacturingi kombineeritud tootmiskeskkonnas, mis ühendab mitmesugused tarne-, tootmis- ja hankestrateegiad. Need strateegiad hõlmavad tootmistellimusi, protsessi haru partiitellimusi, ostutellimusi ja üleviimistellimusi.

| **Oluline**                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Supply Chain Managementi abil saate toetada lean manufacturingi rakendamist kanbanidega. Kuid kulusäästlike põhimõtete edukas rakendamine sõltub siiski sisemistest äriprotsessidest, mida kasutatakse, ning tegelikest tootmistingimustest ja -keskkonnast. |

## <a name="modeling-manufacturing-and-logistics-processes-as-production-flows"></a> Tootmis- ja logistikaprotsesside modelleerimine tootmisvoogudena
Lean manufacturingi aluse loomiseks modelleerige tootmis- ja logistikaprotsessid tootmisvoogudena. Selle tegevus koosneb järgmistest ülesannetest.
1.  Protsesside tuvastamine, mille puhul soovite kulusäästlikku täiendamisstrateegiat kasutada, ja seejärel nende protsesside modelleerimine tootmisvoogudena. Seejärel saate protsesse analüüsida ja täiustada. Üks kulusäästliku rakendamise eesmärke on jäätmete vähendamine, parandades materjali- ja teabevoogu.
2.  Saate määratleda tootmisvoo materjalivoogu kirjeldava tegevuste jadana. Üleviimistegevus määratleb toote või toodete liikumise ühest kohast teise. Protsessi tegevus määratleb tootele rakendatava väärtust lisava toimingu.
3.  Saate luua tootmisvoo versiooni, mis määratleb takti aja nõuded. Neid nõudeid kasutatakse tootmisvoo iga tegevuse tsükli aja arvutamiseks. Saate luua tootmisvoogudest mitu versiooni ja kasutada neid versioone siis protsesside täiustamiseks.

## <a name="using-kanbans-to-signal-demand-requirements"></a> Kanbanide kasutamine nõudluse nõuete tähistamiseks
Tõmbesüsteem toodab kaupu ainult siis, kui kaupu on vaja. Selline süsteem lühendab tarneaegu ja vähendab liigseid varusid. Saate kasutada kanbane tootmisvoogudel põhinevate nõuete plaanimiseks, jälgimiseks ja töötlemiseks. Kanban-raamistiku loomiseks saate luua kanban-reegleid, mis määratlevad, millal kanbanid luuakse ja kuidas nõudeid täidetakse. Saate luua kahte tüüpi kanban-reegleid. Tootmisreeglid loovad protsessi kanban-tööd ja tagastamise kanban-reeglid loovad üleviimise kanban-tööd. Saate seadistada järgmised täiendamisstrateegiad.
-   **Fikseeritud kogusega** kanban-reeglid on seotud fikseeritud arvu materjali käsitlemisühikuid, mis tähendab, et aktiivsete kanbanide arv on konstantne. Alati, kui kõik kanbani tooted on tarbitud ja materjali käsitlemisühikud käsitsi tühjendatud, luuakse uus sama tüüpi kanban. Kui loote fikseeritud kogusega kanbani reeglid, saate arvutada optimaalsed kanbani kogused ja tootekogused, mida kasutatakse. Arvutamisel võetakse arvesse prognoosi, tegelikku nõudlust avatud tellimustest, kaupade täiendamiseks vajalikku aega ja varasemaid nõudlusi.
-   **Plaanitud** kanban-reeglid täiendavad koondplaneerimisega arvutatud nõudeid. Koondplaneerimine loob plaanitud kanbanid, mille saab kanbanideks kinnitada.
-   **Sündmuse** kanban-reeglid täiendavad nõudeid, mis pärinevad müügitellimuse ridadelt, tootmise koosluse ridadelt, kanbani ridadelt või minimaalsetest varude sätetest. Sündmuse kanbanide loomisel seotakse need lähtetingimustega.

Kanbanide loomisel luuakse kanban-reeglites määratletud kanban-voo tegevuste põhjal vähemalt üks kanban-töö.

## <a name="monitoring-and-maintaining-kanban-jobs"></a> Kanban-tööde jälgimine ja haldamine
Lean manufacturing annab ülevaate kanban-reeglitega hallatavate tootmis- ja logistikategevuste jooksvast olekust. Selle tulemusena saate plaanida ja prioritiseerida järgmisi ülesandeid.

-   Saate ülevaate kehtivast kanban-töö graafikust.
-   Saate kanban-töid plaanida ja ümber plaanida.
-   Saate kanban-tööde olekut jälgida ja registreerida.

Järgmises loendis kirjeldatakse spetsiaalseid kanban-tahvleid.
-   Kanban-töö plaanimine – annab ülevaate kanban-töödest. Plaadil kuvatakse kanban-tööd ja nende olek ühe või mitme tööraku puhul. Tööd on loetletud tootmisvoo mudelis määratletud plaanimisperioodide järgi (päevad või nädalad). Plaadil on kuvatud ka iga plaanimisperioodi võimsuse tarbimine, et saaksite plaanitud koormust jälgida. Saate kanban-tööde olekut muuta, neid teistesse plaanimisperioodidesse ümber plaanida ja teha muid toiminguid.
-   Kanban-tahvel ülekandetööde jaoks – see tahvel annab ülevaate jooksvatest ülekandetöödest. Saate komplekteerimislehti uuendada ja registreerida, ülekandetöid käivitada ja lõpetada ning teha muid toiminguid.
-   Kanban-tahvel protsessitööde jaoks – see tahvel on mõeldud tavalise tootmisvoo toetamiseks ja ülevaate andmiseks jooksvast olukorrast ühes või mitmes töörakus. Sellelt tahvlilt saab kanbane prioriseerida, komplekteerida või toota. Tahvel on mõeldud ka vöötkoodi skannimise toetamiseks Kanbanide aruande koostamisel.

## <a name="kanban-jobs-and-integration-with-supply-chain-management-processes"></a>Kanban-tööd ja integreerimine Supply Chain Managementi protsessidega
Kanban-tööd on täielikult integreeritud praeguste laokannete protsessidega Supply Chain Managementis.
-   Saate teha komplekteerimistegevusi kanban-tööde nõuete täitmiseks kasutatud materjali täiendamiseks.
-   Saate printida kanban-kaarte, ringlevaid kanban-kaarte ja komplekteerimislehti kanbanide kasutamise toetamiseks. Neid dokumente kasutatakse kanban-tööde kajastamiseks, jälgimiseks ja registreerimiseks laos ja tootmisosakonnas.
-   Laos toimuvaid komplekteerimis- ja ülekandetegevusi saab registreerida vöötkoode skannides.

Lisaks toetab lean manufacturing alltöövõtu tegevustega viidatud teenuste ostu- ja arveldusprotsesse.
-   Saate määrata alltöövõtu tegevustele ostulepingu ridu ja teenuseid.
-   Saate koostada perioodilisi ostutellimusi ja vastuvõtukinnitusi teenuste ostmise ja arveldamise toetamiseks.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]