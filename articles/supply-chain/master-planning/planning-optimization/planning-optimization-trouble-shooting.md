---
title: Planeerimise optimeerimise tõrkeotsing
description: See artikkel kirjeldab, kuidas lahendada probleeme, mis võivad tekkida planeerimise optimeerimisega töötamisel.
author: t-benebo
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 37c38ab9cec8ae3c9d4decf8043b43ea2251083e
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739725"
---
# <a name="troubleshoot-planning-optimization"></a>Planeerimise optimeerimise tõrkeotsing 

[!include [banner](../../includes/banner.md)]

See artikkel kirjeldab, kuidas parandada tavaprobleeme, mis võivad tekkida planeerimise optimeerimisega töötamisel.

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a>Planeerimise optimeerimise lisandmooduli installimist ei saa lõpule viia

Planeerimise optimeerimine nõuab Lifecycle Servicesi (LCS) loaga suure kättesaadavusega keskkonda, järk 2 või kõrgem, (mitte OneBoxi keskkond) koos Dynamics 365 Supply Chain Managementi versiooniga 10.0.7 või hilisem. Kui proovite installida lisandmoodulit OneBoxi keskkonnas, ei viida installimist lõpule.

**Lahendus**: tühistage installimine ja kasutage suure kättesaadavusega keskkonda, järk 2 või kõrgem (mitte Oneboxi keskkond).

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a>Pakett-tööde planeerimine nurjub, kui planeerimise optimeerimine on lubatud

Kui lubate planeerimise optimeerimise, keelatakse automaatselt plaanimise taunitud koondplaanimise mootor. Koondplaneerimise pakett-tööd, mis loodi taunitud koondplaneerimise mootori jaoks, nurjuvad, kui need käivitatakse ajal, kui plaanimise optimeerimine on lubatud. Teile võidakse kuvada tõrketeadet, nt *See toiming käivitas koondplaneerimise, mida ei toetata, kui planeerimise optimeerimine on lubatud*.

**Parandus**: tühistage kõik koondplaneerimise pakett-tööd, mis loodi taunitud koondplaneerimise mootori jaoks.

## <a name="planning-optimization-results-are-different-from-earlier-results"></a>Planeerimise optimeerimise tulemused erinevad varasematest

Plaanimise optimeerimine erineb mõnel aladel taunitud koondplaanimise mootori kujundusest. Seda võivad põhjustada ka ootel funktsioonid.

**Lahendus**: käivitage planeerimise optimeerimise sobivuse analüüs ja analüüsige selle mõju mõistmiseks tulemusi, viidates sellega seotud dokumentatsioonile. Lisateavet vt [Planeerimise optimeerimise sobivuse analüüs](planning-optimization-fit-analysis.md).

## <a name="cant-enable-planning-optimization"></a>Planeerimise optimeerimist ei saa lubada

Suvandi **Ühenduse olek** väärtuseks peab olema määratud **Ühendatud** enne, kui saate määrata suvandi **Plaanimise optimeerimise kasutamine** väärtuseks **Jah**. Lisateavet vt [Planeerimise optimeerimise kasutamise alustamine](get-started.md).

**Lahendus**: veenduge, et planeerimise optimeerimise lisandmoodul on edukalt installitud.

## <a name="error-message-is-shown-during-ctp"></a>CTP ajal kuvatakse tõrketeade

Kui proovite käivitada müügitellimusest funktsiooni võimeline lubama (CTP), kui planeerimise optimeerimine on lubatud, kuvatakse järgmine tõrketeade: *See toiming käivitas koondplaneerimise, mida ei toetata, kui planeerimise optimeerimine on lubatud*.

See on seotud ootel oleva funktsiooniga, mis on planeeritud tootmistellimuste toe osana.

**Lahendus:** vältige CTP arvutamisi, kui planeerimise optimeerimine on lubatud, kuni CTP tugi on saadaval.

## <a name="additional-resources"></a>Lisaressursid

- [Koondplaneerimisega alustamine](get-started.md)
- [Planeerimise optimeerimise sobivuse analüüs](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]