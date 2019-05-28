---
title: Arve tasumise stsenaariumide seadistamine
description: Selles teemas kirjeldatakse, kuidas konfigureerida rakendust Dynamics 365 for Retail, et see toetaks arve maksetega seotud erinevaid stsenaariume.
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 158d8ca8a97c473e940f76dd3f35cecc4e9dd7f4
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517044"
---
# <a name="set-up-pay-invoice-scenarios"></a>Arve tasumise stsenaariumide seadistamine

[!include [banner](includes/banner.md)]

Arve maksmise funktsiooni rakenduses Dynamics 365 for Retail on laiendatud, et see toetaks järgmist.

- Mitme müügitellimuse arve tasumine ühe kassakandega.
- Mitme kliendiarve tüübi makse, sh vabas vormis arved, projektipõhised arved ja kreeditarved.

Nende stsenaariumide lubamiseks tuleb kaupluste funktsiooniprofiili konfigureerida allpool kirjeldatud viisil.

1. Valige suvandid **Jaemüük \> Kanali seadistus \> Kassa seadistus \> Kassa profiilid \> Funktsiooniprofiilid** ja valige profiil, mis on seotud kauplustega, mida soovite muuta.
2. Konfigureerige vahekaardil **Funktsioonid** vajaduse järgi järgmisi parameetreid.

    - **Müügitellimuse arve** – valige väärtus **Jah**, et lasta kasutajatel maksta üks või mitu müügitellimisel põhinevat arvet ühes kassakandes.
    - **Vabas vormis arve** – valige väärtus **Jah**, et lasta kasutajatel maksta üks või mitu vabas vormis arvet ühes kassakandes.
    - **Projektiarve** – valige väärtus **Jah**, et lasta kasutajatel maksta üks või mitu projektiarvet ühes kassakandes.
    - **Müügitellimuse kreeditarve** – valige väärtus **Jah**, et lasta kasutajatel tasakaalustada mitu müügitellimusel põhinevat kreeditarvet avatud arvete suhtes või töödelda tagasimakset kliendile avatud kreeditarve jaoks.

> [!NOTE]
> Osaliste summade makset või tasakaalustamist veel ei toetata.
