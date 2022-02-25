---
title: Kehtetute laodimensioonide tõttu ei saa koormusrida luua
description: Kui proovite tagastatud müügitellimust lattu välja saata, võite saada veateate kehtetute varude dimensioonide kohta. Eemalda need tellimuse realt.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b02408b61b07b272a7e7d52004dc2492d60ef28c
ms.sourcegitcommit: 0d14c4a1e6cf533dd20463f1a84eae8f6d88f71b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/14/2022
ms.locfileid: "8119208"
---
# <a name="cant-create-load-line-for-return-sales-order-due-to-invalid-inventory-dimensions"></a>Varude sobimatute dimensioonide tõttu ei saa tagastatud müügitellimuse jaoks koormusrida luua

## <a name="symptoms"></a>Sümptomid

Kui proovite tagastatud müügitellimust lattu vabastada, võidakse kuvada järgmine tõrketeade:

> Te ei saa selle tellimuserea jaoks koorma rida luua, kuna see sisaldab varude dimensioone, mis on kehtetud. Te ei saa viidata varude dimensioonidele, mis asuvad reserveerimise hierarhias asukoha dimensiooni all. Eemaldage tellimuse realt kehtetud dimensioonid.

## <a name="resolution"></a>Lahendus

Kahjuks ei toeta toode koorma töötlemist müügiks tagastamise protsessiks. Seetõttu ei saa väljastada lattu tagastamise müügitellimust.

Müügitellimuste tehingutes ei saa viidata varude dimensioonidele, mis asuvad reserveerimise hierarhias **Location** dimensiooni all. Lahenduseks on eemaldada tellimuse realt kehtetud dimensioonid.
