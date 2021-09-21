---
title: Toote sissetuleku kande number kasutatakse ära ka siis, kui kannet ei looda
description: Toote sissetuleku kandenumbrit tarbitakse isegi siis, kui toote sissetuleku käigus ei looda ühtegi finantskannet
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 0556969950c45e80d177a0e96096c4157d690ae3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476114"
---
# <a name="a-product-receipt-voucher-number-is-consumed-even-when-not-generating-a-voucher"></a>Toote sissetuleku kande number kasutatakse ära ka siis, kui kannet ei looda

## <a name="symptoms"></a>Sümptomid

Toote sissetuleku kandenumbrit tarbitakse isegi siis, kui toote sissetuleku käigus ei looda ühtegi finantskannet.

## <a name="resolution"></a>Lahendus

Kui suvandi **Kumuleerimise kohustus toote sissetulekul** väärtuseks on kauba mudeligrupi puhul seatud *Ei*, siis pearaamatusse sisestusi ei tehta. Sellegi poolest kirjendatakse füüsiline sündmus raamatupidamise otstarbel alammoodulis ja selle sündmuse jaoks on vaja kandenumbrit. See kandenumber on laokannetes viidatud kandenumber.

Me soovitame seada suvandi **Kumuleerimise kohustus toote sissetulekul** väärtuseks *Jah*, nagu on kirjeldatud ajaveebipostituses [Lisakulude sisestamine toote sissetuleku ajal](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).
