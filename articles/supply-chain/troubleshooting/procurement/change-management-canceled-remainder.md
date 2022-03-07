---
title: Tarnejäägi tühistamisel teisaldatakse ostutellimus kinnitatud olekusse
description: Kui tarnejääk tühistatakse ostutellimusel, mille puhul on muudatuste haldus sisse lülitatud, määratakse ostutellimuse olekuks kinnitatud
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
ms.openlocfilehash: 1d8b331bc5699487dff3491d65daa36293f3212f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476132"
---
# <a name="cancelling-delivery-remainder-moves-purchase-order-to-a-confirmed-state"></a>Tarnejäägi tühistamisel teisaldatakse ostutellimus kinnitatud olekusse

## <a name="symptoms"></a>Sümptomid

Muudatuste haldust kasutava ostutellimuse puhul määratakse selle olekuks otse *Kinnitatud* ja töölehte ei looda, kui ainus taotletud muudatus on tarnejäägi tühistamine ühel või mitmel real.

## <a name="resolution"></a>Lahendus

Tarnejäägi tühistamine ei mõjuta kinnitustöölehe sisu. Seda funktsiooni tuleks kasutada siis, kui rida on osaliselt vastu võetud ja järelejäänud kogus tuleks tühistada protsessi etapis, mis toimub pärast seda, kui hankija on ostutellimuse kinnitanud.

Kui see peaks kajastuma ostutellimuse kinnitusel, tuleb kogust ostutellimuse real korrigeerida, nii et kinnitus oleks vajalik. Kui rea puhul pole midagi vastu võetud, on võimalik teise võimalusena kogus eemaldada. Sellisel juhul on vajalik taaskinnitus.
