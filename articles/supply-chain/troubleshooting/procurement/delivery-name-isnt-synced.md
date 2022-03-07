---
title: Pärast ostutellimuse tarneaadressi muutmist tarne aadressi ei sünkroonita
description: Pärast tarneaadressi muutmist ostutellimuse päisel ei sünkroonita tarne nime
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
ms.openlocfilehash: 588d1ef6250d249aa4fc9da4f5125e9a34c0255f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476088"
---
# <a name="the-delivery-name-isnt-synced-after-changing-a-purchase-order-delivery-address"></a>Pärast ostutellimuse tarneaadressi muutmist tarne aadressi ei sünkroonita

## <a name="symptoms"></a>Sümptomid

Ostutellimuse päises olev aadress muudetakse aadressiks, mis pole tarneaadress. Kuigi aadressi värskendatakse ostutellimusel, ei värskendata tarne nime värskendatud aadressi alusel.

## <a name="resolution"></a>Lahendus

Selline käitumine on nii kavandatud. Valitud aadress tuleb märkida tarneaadressina. Muidu ei värskendata tarne nime valitud aadressi alusel.
