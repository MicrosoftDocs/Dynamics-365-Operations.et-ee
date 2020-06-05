---
title: Kontsernisisesed kulud
description: Töötaja, kes töötab ühes organisatsiooni juriidilises isikus, võib teha tööd sama organisatsiooni teise juriidilise isiku heaks. Selles olukorras võite kontsernisisese kulu funktsiooni abil määrata töötaja kulud sellele juriidilisele isikule, kelle heaks töö tehti.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 07e425707eb20730f10246a27799f4deeef93f97
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/21/2020
ms.locfileid: "3390880"
---
# <a name="intercompany-expenses"></a>Kontsernisisesed kulud

[!include [banner](../includes/banner.md)]

Töötaja, kes töötab ühes organisatsiooni juriidilises isikus, võib teha tööd sama organisatsiooni teise juriidilise isiku heaks. Selles olukorras võite kontsernisisese kulu funktsiooni abil määrata töötaja kulud sellele juriidilisele isikule, kelle heaks töö tehti. Juriidilist isikut, mis töötajale tööd annab, nimetatakse välja laenavaks juriidiliseks isikuks. Juriidilist isikut, millele töötaja kulusid tekitab, nimetakse laenavaks juriidiliseks isikuks. 

Enne, kui töötaja saab luua ja esitada kulusid töö kohta, mida tehakse teise juriidilise isiku heaks, tehke välja laenavas juriidilises isikus lehel **Kuluhalduse parameetrid** valik **Luba kontsernisiseseid kuluridu**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Kontsernisiseste kulude maksu sisestamine

[!include [banner](../includes/banner.md)]

Kui soovite kasutada kuluaruandes välja laenava (algne) juriidilise isiku maksugruppe laenava (sihtisik) juriidilise isiku asemel, peate selle konfigureerima pearaamatu käibemaksu seadistamisel. Kui pearaamatu parameetri **Kontsernisisese maksu sisestamise juriidiline isik** väärtuseks on seatud **Algne** ja **Rakenda käibemaksuga maksustamise reeglid** väärtuseks **Ei**, kasutatakse välja laenava juriidilise isiku maksukombinatsiooni. Kui selle parameetri väärtuseks on seatud **Sihtisik**, kasutatakse laenava juriidilise isiku maksukombinatsiooni. Kui Ameerika Ühendriikide juriidilise isiku puhul on parameetri väärtuseks seatud **Algne**, peab ka väli **Saadaolev käibemaks** olema konfigureeritud uuel lehel **Pearaamatu sisestamisgrupid**. Raamatupidamise mootor kasutab selle välja teavet maksuga seotud raamatupidamise kirje jaoks.   
See käitumine on kooskõlas kuluridadega, mis on sisestatud projektiga või ilma.  
