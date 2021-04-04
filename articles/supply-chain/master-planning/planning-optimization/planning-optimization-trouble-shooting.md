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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 39583c244f09f54551d560e8b1dd9f1a5a1590cc
ms.sourcegitcommit: 72f70c81176e86cda714a4712525f73514c895b7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/16/2021
ms.locfileid: "5457325"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]