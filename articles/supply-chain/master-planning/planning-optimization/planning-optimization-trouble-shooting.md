---
title: Planeerimise optimeerimise tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada planeerimise optimeerimisega töötamisel tekkivaid probleeme.
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: c3dd0bf262f65aac2359c05ff954bdfbd294353f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426038"
---
# <a name="troubleshoot-planning-optimization"></a>Planeerimise optimeerimise tõrkeotsing 

[!include [banner](../../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas lahendada planeerimise optimeerimisega töötamisel tekkivaid levinumaid probleeme.

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a>Planeerimise optimeerimise lisandmooduli installimist ei saa lõpule viia

Planeerimise optimeerimine nõuab Lifecycle Servicesi (LCS) loaga suure kättesaadavusega keskkonda, järk 2 või kõrgem, (mitte OneBoxi keskkond) koos Dynamics 365 Supply Chain Managementi versiooniga 10.0.7 või hilisem. Kui proovite installida lisandmoodulit OneBoxi keskkonnas, ei viida installimist lõpule.

**Lahendus**: tühistage installimine ja kasutage suure kättesaadavusega keskkonda, järk 2 või kõrgem (mitte Oneboxi keskkond).

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a>Pakett-tööde planeerimine nurjub, kui planeerimise optimeerimine on lubatud

Planeerimise optimeerimise lubamisel keelatakse automaatselt sisseehitatud koondplaneerimise mootor. Koondplaneerimise pakett-tööd, mis loodi sisseehitatud Supply Chain Managementi planeerimismootori jaoks, nurjuvad käivitamisel, kui planeerimise optimeerimine on lubatud. Teile võidakse kuvada tõrketeadet, nt *See toiming käivitas koondplaneerimise, mida ei toetata, kui planeerimise optimeerimine on lubatud*.

**Lahendus**: tühistage kõik koondplaneerimise pakett-tööd, mis loodi sisseehitatud Supply Chain Managementi planeerimismootori jaoks.

## <a name="planning-optimization-results-are-different-from-earlier-results"></a>Planeerimise optimeerimise tulemused erinevad varasematest

Planeerimise optimeerimine erineb sisseehitatud koondplaneerimise kujundusest mõnel alal. Seda võivad põhjustada ka ootel funktsioonid.

**Lahendus**: käivitage planeerimise optimeerimise sobivuse analüüs ja analüüsige selle mõju mõistmiseks tulemusi, viidates sellega seotud dokumentatsioonile. Lisateavet vt [Planeerimise optimeerimise sobivuse analüüs](planning-optimization-fit-analysis.md).

## <a name="master-planning-doesnt-respect-the-coverage-time-fence"></a>Koondplaneerimine ei arvesta laovarude ajapiiri

Seda põhjustab planeerimise optimeerimise ootel olev funktsioon.

**Lahendus**: senikaua, kuni ootel funktsiooni pole saadaval, filtreerige või kustutage planeeritud tellimused, et eemaldada laovarude ajapiirist väljapoole jäävad varude soovitused.

## <a name="cant-enable-planning-optimization"></a>Planeerimise optimeerimist ei saa lubada

Suvandi **Ühenduse olek** väärtuseks peab olema määratud **Ühendatud** enne, kui saate määrata suvandi **Plaanimise optimeerimise kasutamine** väärtuseks **Jah**. Lisateavet vt [Planeerimise optimeerimise kasutamise alustamine](get-started.md).

**Lahendus**: veenduge, et planeerimise optimeerimise lisandmoodul on edukalt installitud.

## <a name="error-message-is-shown-during-ctp"></a>CTP ajal kuvatakse tõrketeade

Kui proovite käivitada müügitellimusest funktsiooni võimeline lubama (CTP), kui planeerimise optimeerimine on lubatud, kuvatakse järgmine tõrketeade: *See toiming käivitas koondplaneerimise, mida ei toetata, kui planeerimise optimeerimine on lubatud*.

See on seotud ootel oleva funktsiooniga, mis on planeeritud tootmistellimuste toe osana.

**Lahendus:** vältige CTP arvutamisi, kui planeerimise optimeerimine on lubatud, kuni CTP tugi on saadaval.

## <a name="additional-resources"></a>Lisaressursid

[Planeerimise optimeerimisega alustamine](get-started.md)

[Planeerimise optimeerimise sobivuse analüüs](planning-optimization-fit-analysis.md)
