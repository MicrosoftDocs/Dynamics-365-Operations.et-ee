---
title: Arve tasumise stsenaariumide seadistamine
description: Selles teemas kirjeldatakse, kuidas konfigureerida rakendust Dynamics 365 Commerce, et see toetaks arve maksetega seotud erinevaid stsenaariume.
author: josaw1
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9dc4ff9241cec4033b65f15449c233bdb43233c0dce1ab04a2cd66baf5272a6b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772981"
---
# <a name="set-up-pay-invoice-scenarios"></a>Arve tasumise stsenaariumide seadistamine

[!include [banner](includes/banner.md)]

Arve maksmise funktsiooni rakenduses Dynamics 365 Commerce on laiendatud, et see toetaks järgmist.

- Mitme müügitellimuse arve tasumine ühe kassakandega.
- Mitme kliendiarve tüübi makse, sh vabas vormis arved, projektipõhised arved ja kreeditarved.

Nende stsenaariumide lubamiseks tuleb kaupluste funktsiooniprofiili konfigureerida allpool kirjeldatud viisil.

1. Valige suvandid **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassa profiilid \> Funktsiooniprofiilid** ja valige profiil, mis on seotud kauplustega, mida soovite muuta.
2. Konfigureerige vahekaardil **Funktsioonid** vajaduse järgi järgmisi parameetreid.

    - **Müügitellimuse arve** – valige väärtus **Jah**, et lasta kasutajatel maksta üks või mitu müügitellimisel põhinevat arvet ühes kassakandes.
    - **Vabas vormis arve** – valige väärtus **Jah**, et lasta kasutajatel maksta üks või mitu vabas vormis arvet ühes kassakandes.
    - **Projektiarve** – valige väärtus **Jah**, et lasta kasutajatel maksta üks või mitu projektiarvet ühes kassakandes.
    - **Müügitellimuse kreeditarve** – valige väärtus **Jah**, et lasta kasutajatel tasakaalustada mitu müügitellimusel põhinevat kreeditarvet avatud arvete suhtes või töödelda tagasimakset kliendile avatud kreeditarve jaoks.

> [!NOTE]
> Osaliste summade makset või tasakaalustamist veel ei toetata.


[!INCLUDE[footer-include](../includes/footer-banner.md)]