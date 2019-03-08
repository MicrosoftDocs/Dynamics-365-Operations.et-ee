---
title: PowerAppsi rakenduste manustamine Core HR-is
description: Selles teemas selgitatakse, kuidas lahendada probleemi, mille käigus PowerAppsi menüükäsk on süsteemihalduse moodulist kadunud.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 197b553f0b202ee29ad42274e2c0e03446ec782c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "304081"
---
# <a name="embed-powerapps-apps-in-core-hr"></a>PowerAppsi rakenduste manustamine Core HR-is

[!include [banner](includes/banner.md)]

**Probleem**

Menüükäsk **PowerApps** on moodulist **Süsteemihaldus** kadunud.

**Põhjus**

Kasutajaliidese (UI) kujundust muudeti ja Microsoft PowerApps on nüüd kaasatud standardsesse isikupärastamismudelisse.

**Eraldusvõime**

Muudeti PowerAppsi rakenduste manustamise viisi. PowerAppsi rakendusi lisatakse nüüd isikupärastamismudeli kaudu. Rakenduses Microsoft Dynamics 365 for Talent saab PowerAppsi rakendusi lisada peaaegu kõigile lehtedele.

Üksikasjalikku teavet PowerAppsi rakenduse manustamise kohta Talentis vt jaotisest [PowerAppsi rakenduste manustamine](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).

Enne muutust rakendused manustanud PowerAppsi kliendid tuleb viia vastavusse uue mudeliga.

Nupp **PowerApps** asub peaaegu igas Talenti lehe ülemises parempoolses nurgas. Seda nuppu saab kasutada PowerAppsi rakenduse sisestamiseks.

Siin on näide.

1. Minge jaotisse **Personalihaldus \> Lingid \> Töötajad \> Töövõtjad**.
2. Valige nupp **PowerApps** ja seejärel valige **Lisa PowerApp**.

    ![Nupp PowerApps](media/png.png)

3. Täitke väljad dialoogiboksis **Lisa PowerApp**.

    ![Dialoogiboks Lisa PowerApp](media/insert-powerapp.png)

Teise võimalusena tehke järgmist.

1. Tehke lehe toimingupaani vahekaardi **Suvandid** grupis **Isikupärasta** valik **Vormi isikupärastamine**.

    ![Grupp Isikupärasta vahekaardil Suvandid](media/options.png)

    Ilmub isikupärastamise tööriistariba.

2. Valige tööriistaribal **Lisa \> PowerApp**.

    ![PowerAppsi rakenduse lisamine isikupärastamise tööriistariba kasutades](media/powerapp-bar.png)
