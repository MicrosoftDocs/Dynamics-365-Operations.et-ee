---
title: Varude ajalise jaotuse aruanne
description: Selles teemas kirjeldatakse funktsiooni, mis võimaldab teil käitada varude ajalise jaotuse aruannet ja muuta tulemus kättesaadavaks nii vormi kui ka diagrammi kujul.
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 790c8fe3a52bce652227f1cef97eff6496476100
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201614"
---
# <a name="inventory-aging-report"></a>Varude ajalise jaotuse aruanne


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Rakenduses Microsoft Dynamics 365 Supply Chain Management saate käitada **Varude ajalise jaotuse** aruannet ja muuta tulemuse kättesaadavaks nii vormi kui ka diagrammi kujul. Vormis reguleeritakse veerge ja koondsaldosid dünaamiliselt olenevalt konfigureeritud paigutusele. Diagramm annab visuaalse ülevaate, mis toetab filtreerimist ja võimaldab teil üksikasjadesse süvitsi minna. Lisaks võimaldab andmeüksus **Varude ajalise jaotuse aruanne** eksportida **Varude ajalise jaotuse** aruande käivitamise tulemusi vormingus, nagu Microsoft Exceli fail või PDF-fail.

Selline **Varude ajalise jaotuse** aruande käivitamise meetod on kasulik juhul, kui väljund sisaldab palju ridu. Näiteks sisaldab väljund palju ridu, kui teil on 50 000 kaupa ja 300 poodi, mis on loodud ladudena, ning taotlete varude ajalist jaotumist kauba, tegevuskoha ja lao järgi.

## <a name="run-an-inventory-aging-report"></a>Varude ajalise jaotuse aruande käivitamine

1. Avage **Kuluhaldus \> Päringud ja aruanded \> Lao varude ajalise jaotuse aruanne**.
1. Valige suvand **Uus**.
1. Väljale **Protsessi ID – nimi** sisestage aruandele kordumatu nimi.
1. Valige aruanne **Identimine – ID** ja filtreerige seda vastavalt vajadusele.

    Aruande käivitamine toimub alati pakett-töös.

1. Pärast pakett-töö lõpetamist kuvatakse väljund lehel **Lao varude ajalise jaotuse aruanne**.
1. Kui soovite vaadata väljundit vormina, millel on traditsiooniline ruudustiku paigutus, valige **Kuva üksikasjad**. Väljundi koonddiagrammina vaatamiseks valige **Kuva diagramm**.

    > [!NOTE]
    > Vorm ei sisalda aruande paigutuses määratletud vahesummasid.

Andmeüksus **Varude ajalise jaotuse aruanne** võimaldab teil eksportida **Varude ajalise jaotuse** aruande väljundi, rakendades välja **Protsessi ID – nimi** filtri mis tahes vormile, mida andmehaldus toetab.
