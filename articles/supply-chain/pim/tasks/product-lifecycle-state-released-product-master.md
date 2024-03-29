---
title: Toote elutsükli oleku määramine väljastatud tooteetalonile
description: See protseduur näitab, kuidas määrata toote elutsükli olek väljastatud tooteetalonile ja selle variantidele.
author: t-benebo
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 217bab38544c2794d2e57410f8c2a979605106b0
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567003"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]