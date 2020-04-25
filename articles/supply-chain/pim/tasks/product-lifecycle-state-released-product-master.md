---
title: Toote elutsükli oleku määramine väljastatud tooteetalonile
description: See protseduur näitab, kuidas määrata toote elutsükli olek väljastatud tooteetalonile ja selle variantidele.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab8c4e02a064fe84446fa54cc05b9a6a902c1860
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213143"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a>Toote elutsükli oleku määramine väljastatud tooteetalonile

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas määrata toote elutsükli olek väljastatud tooteetalonile ja selle variantidele. Eeltingimus: teil tuleb esmalt esitada tegevuse juhist „Uue toote elutsükli oleku loomine” ja veenduda, et vähemalt üks toote elutsükli olek oleks loodud, et saaksite tegevuse juhist esitada.


## <a name="find-a-released-product-master"></a>Väljastatud tooteetaloni ülesotsimine
1. Avage Tooteteabe haldus > Tooted > Väljastatud tooted.
2. Otsige loendist ja valige soovitud kirje.

> [!NOTE]
> Tooteetaloni alamtüüp on Tooteetalon.  

## <a name="update-the-lifecycle-state"></a>Elutsükli oleku värskendamine
1. Klõpsake nuppu Redigeeri.
2. Väljal Toote elutsükli olek sisestage või valige väärtus.
3. Klõpsake nuppu Salvesta.
4. Klõpsake nuppu Jah.

> [!NOTE]
> Kui valitud on Jah, värskendatakse toote uue elutsükli oleku alusel ka kõiki seotud väljastatud tootevariante, millel on sama algne olek mis väljastatud tooteetalonil. Kui valitud on Ei, säilitatakse kõikide variantide praegune olek. Väljastatud tooteetalonist erineva elutsükli olekuga variante ei värskendata.  

## <a name="verify-the-lifecycle-state-of-the-variants"></a>Variantide elutsükli oleku kontrollimine
1. Klõpsake valikut Väljastatud tootevariandid.

> [!NOTE]
> Pange tähele, et kõik variandid pärivad väljastatud tooteetaloni jaoks valitud elutsükli oleku.  

2. Märkige loendis valitud rida.
3. Väljal Toote elutsükli olek sisestage või valige väärtus.

