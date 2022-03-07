---
title: Vaikemaksugruppi ja vaikesularaha kontot ei täideta arve konto põhjal
description: Vaikemaksugruppi ja vaikesularahakontot ei täideta arve konto põhjal
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
ms.openlocfilehash: bb984eb17209dc92e336df5ad475bb0f70c6e35c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476113"
---
# <a name="default-tax-group-and-cash-discount-arent-filled-in-from-the-invoice-account"></a>Vaikemaksugruppi ja vaikesularaha kontot ei täideta arve konto põhjal

## <a name="symptoms"></a>Sümptomid

Kui kasutate arve kontot, mis erineb kliendi kontost, siis ei täideta ostutellimuse loomisel arvekonto põhjal vaikemaksugruppi ja -skontot.

## <a name="resolution"></a>Lahendus

Selline käitumine on nii kavandatud. Maksugrupi ja skontode vaikeväärtused ning muu hinnateave põhineb kliendi kontol, mitte arve kontol.
