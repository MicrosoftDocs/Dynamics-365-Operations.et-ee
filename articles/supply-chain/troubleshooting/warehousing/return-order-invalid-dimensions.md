---
title: Kehtetute laodimensioonide tõttu ei saa koormusrida luua
description: Kui proovite tagastatud müügitellimust lattu välja saata, võite saada veateate kehtetute varude dimensioonide kohta. Eemalda need tellimuse realt.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac58
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 3cb728f6a989cdac63c91d49baaea094bace59e4
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476136"
---
# <a name="cant-create-load-line-for-return-sales-order-due-to-invalid-inventory-dimensions"></a>Varude sobimatute dimensioonide tõttu ei saa tagastatud müügitellimuse jaoks koormusrida luua

## <a name="symptoms"></a>Sümptomid

Kui proovite tagastatud müügitellimust lattu vabastada, võidakse kuvada järgmine tõrketeade:

> Te ei saa selle tellimuserea jaoks koorma rida luua, kuna see sisaldab varude dimensioone, mis on kehtetud. Te ei saa viidata varude dimensioonidele, mis asuvad reserveerimise hierarhias asukoha dimensiooni all. Eemaldage tellimuse realt kehtetud dimensioonid.

## <a name="resolution"></a>Lahendus

Kahjuks ei toeta toode koorma töötlemist müügiks tagastamise protsessiks. Seetõttu ei saa väljastada lattu tagastamise müügitellimust.

Müügitellimuste tehingutes ei saa viidata varude dimensioonidele, mis asuvad reserveerimise hierarhias **Location** dimensiooni all. Lahenduseks on eemaldada tellimuse realt kehtetud dimensioonid.
