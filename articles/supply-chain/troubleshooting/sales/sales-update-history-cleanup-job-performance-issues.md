---
title: Müügi värskendamise ajaloo puhastustöö ebaõnnestub või on jõudlusprobleeme
description: Müügiajaloo puhastamine võib nurjuda või võtta väga kaua aega, kui müügi uuendamisandmeid on palju.
author: myvakalo
ms.date: 10/05/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c02273adf90afc67b7c0ae1b82c19d489bfbd3b1
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920070"
---
# <a name="sales-update-history-cleanup-job-fails-or-has-performance-issues"></a>Müügi värskendamise ajaloo puhastustöö ebaõnnestub või on jõudlusprobleeme

## <a name="symptoms"></a>Sümptomid

**Müügi värskendamise ajaloo puhastamine** töö ebaõnnestub või on jõudlusprobleeme.  

## <a name="cause"></a>Põhjus

See võib juhtuda, kui süsteem hõlmab suurt hulka müügiuuendusi, mille tulemusena võib kaasa tuua hulga müügi uuendamisandmeid. Puhastustöö püüab kõiki neid andmeid ühes kandes puhastada. Seetõttu võib töö käitamine või isegi nurjumine võtta väga kaua aega.

## <a name="resolution"></a>Lahendus

Uus **müügi värskendusajaloo puhastamise** töö versioon on saadaval Supply Chain Management versioonist 10.0.19 või uuemas. Vaikimisi pole see funktsioon lubatud. Üksikasju selle kohta, kuidas see toimib ja kuidas seda funktsioonihalduses lubada, vt [müügiajaloo puhastamisjõudluse parendust](../../sales-marketing/sales-update-history-cleanup-performance-improvements.md).

