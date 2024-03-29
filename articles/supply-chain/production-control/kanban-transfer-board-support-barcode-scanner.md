---
title: Kanbani ülekandmise tahvli tugi vöötkoodilugejatele
description: Kanbani ülekandmise tahvel toetab vöötkoodiskanneri vidina sisendit toiminguteks Vali, Käivita, Lõpeta ja Tühjenda kanban-töö.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b18aad4dcdbf8c2d18960ae306556c3ea679d622
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566807"
---
# <a name="kanban-transfer-board-support-for-bar-code-scanners"></a>Kanbani ülekandmise tahvli tugi vöötkoodilugejatele

[!include [banner](../includes/banner.md)]

Kanbani ülekandmise tahvel toetab vöötkoodiskanneri vidina sisendit toiminguteks Vali, Käivita, Lõpeta ja Tühjenda kanban-töö.

## <a name="registration-modes"></a>Registreerimisrežiimid

Kiirkaardil **Skanneri registreerimine** saate valida registreerimisrežiimi, millega juhitakse tegevust, kui skannite kanban-kaardi numbri või sisestate numbri käsitsi väljale Kanban-kaardi number.

| Registreerimisrežiimi määramine | Kirjeldus                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| Algus                 | Registreerib kanbani ülekandetöö pooleliolevana.                                                 |
| Lõpule viidud              | Registreerib kanbani ülekandetöö lõpetatuna.                                                   |
| Tühi                 | Registreerib kanban-kaardi viidatud materjali käsitlemisühiku tühjana.              |
| Vali                | Registreerib kanban-kaardi numbri ja valib kanban-tööde loendist viidatud töö automaatselt. |

 
## <a name="registration-mode-select"></a>Registreerimisrežiimi valimine

Kui kasutate töö valimiseks vöötkoodilugejat, muutub kanban-tahvli kuvarežiim. Selles režiimis kehtivad järgmised tingimused.

-   Kuvatakse ainult skannitud kanban-töö.
-   Valitud töö üksikasjad kuvatakse kiirkaardil **Üksikasjad**.
-   Kiirkaardil **Teated** kuvatakse ainult teated valitud töö kohta.
-   Töö olekut saate muuta, kasutades funktsioone, mis on saadaval toimingupaanil. Kanbani ülekandmise tahvlil kuvatakse sel ajal ainult üht tööd.
-   Saate värskendada tööde loendis olevat teavet käsitsi, klõpsates toimingupaanil käsku **Värskenda** (Shift + F5). Pärast teabe värskendamist kuvatakse uuesti töö filtri täielikud tulemused.

## <a name="job-status-and-possible-actions"></a>Töö olek ja võimalikud tegevused
Valitud töö olek ja sündmuse kanbanide mis tahes kinnistatud tööde olek määravad, kas saate tööd edasi töödelda. Järgmises tabelis kuvatakse teave nende olekute ja ülesannete kohta.
-   Tööde jaoks või tööde viidatud materjali käsitlemisühikute jaoks saadaolevad olekud.
-   Iga ülesanne, mida saate töö puhul täita.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th>Töö tüüp</th>
<th>Töö olek või materjali käsitlemisühiku olek</th>
<th>Komplekteerimislehe värskendamine</th>
<th>Algus</th>
<th>Värskenda reserveeringut</th>
<th>Lõpule viidud</th>
<th>Tühi</th>
<th>Loo sündmuse kanbanid</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ülekanne</td>
<td><ul>
<li>Pole plaanitud</li>
<li>Kinnistatud töid pole või on kinnistatud tööd lõpule viidud</li>
</ul></td>
<td>Jah</td>
<td>Jah</td>
<td>Jah</td>
<td>Jah</td>
<td>Ei</td>
<td>Jah</td>
</tr>
<tr class="even">
<td>Ülekanne</td>
<td><ul>
<li>Pole plaanitud</li>
<li>Kinnistatud töö ei ole lõpule viidud</li>
</ul></td>
<td>Jah</td>
<td>Ei</td>
<td>Jah</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
</tr>
<tr class="odd">
<td>Ülekanne</td>
<td>Käimas</td>
<td>Jah</td>
<td>Ei</td>
<td>Jah</td>
<td>Jah</td>
<td>Ei</td>
<td>Ei</td>
</tr>
<tr class="even">
<td>Ülekanne</td>
<td>Valmis</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Jah</td>
<td>Ei</td>
</tr>
<tr class="odd">
<td>Ülekanne või protsess</td>
<td>Tühi</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
</tr>
<tr class="even">
<td>Ülekanne või protsess</td>
<td>Kanban-kaarti ei leitud</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
</tr>
<tr class="odd">
<td>Ülekanne või protsess</td>
<td>Kanban-kaart leiti, kuid see pole kanbanile määratud</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
</tr>
<tr class="even">
<td>Protsess</td>
<td><ul>
<li>Pole plaanitud</li>
<li>Ettevalmistatud</li>
<li>Käimas</li>
</ul></td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
</tr>
<tr class="odd">
<td>Protsess</td>
<td>Valmis</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
<td>Ei</td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]