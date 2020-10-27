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
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c644f118e0bdb46b296cec7e4a3ea89031f2d52
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981130"
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

