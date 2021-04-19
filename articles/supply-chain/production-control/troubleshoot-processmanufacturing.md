---
title: Protsesstootmise tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada protsesstootmisega töötamisel tekkivaid probleeme.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 938820b6cd2bb470b440fea7b70124efc0faf7f8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824986"
---
# <a name="troubleshoot-process-manufacturing"></a>Protsesstootmise tõrkeotsing

Selles teemas kirjeldatakse, kuidas lahendada protsesstootmisega töötamisel tekkivaid probleeme.

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a>Kui ma kasutan töökaardi seadet, et teatada osalisest kogusest tootmistellimuse viimasel tööl, lõpetatakse automaatselt kõik selle tellimuse varasemad tööd, mille olekuks on seatud pooleli.

Selline käitumine on nii kavandatud. **Tootmistellimuse vaikesätted** lehel **Kinnita lõpetatuks** vahekaardil on suvand nimega **Lõpp-märgistuse protsess**. Kui see teema on seatud väärtusele *Jah*, sisestatakse protsessikaardi tööleht, kui töötaja kasutab viimase operatsiooni kohta töökaardi seadet või töökaardi terminali. See tööleht märgib kõik operatsioonid lõpetatuks ja lõpetab kõik tootmistööd. Kui **Lõpp-märgistamise protsessi** suvandi väärtuseks on seatud *Jah*, ei arvesta süsteem töö olekut, mille töötaja valis viimase operatsiooni käigus. Süsteem ei võta arvesse ka seda, kas töötaja teatab täielikust või osalisest kogusest.

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a>Kui ma proovin ladu sulgeda, kuvatakse järgmine hoiatusteade: "Omahinna tagasiarvestuse arvutuse teostamist %1 kuupäevaga ühtiva perioodi lõpuga ei ole registreeritud."

Kui kasutate varasemat versiooni kui 10.0.13, siis kui te ei kasuta minimaalsete tootmiskulude voogu, kuvatakse lao sulgemisel järgmine ekslik hoiatusteade.

> Olete käivitamas lao sulgemist kuupäevaga %1. Perioodi lõpukuupäevaga %1 sobivat omahinna tagasiarvestust ei ole registreeritud. Palun teostage perioodi lõpukuupäevaga %1 sobiv omahinna tagasiarvestus. Varude hindamine, müüdud kaupade kulu ja erinevused ei pruugi olla abiraamatu või pearaamatu puhul õiged, kuni see on teostatud.

See probleem on parandatud versioonis 10.0.13 ja hilisemates versioonides. Lisateavet leiad teemast [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]