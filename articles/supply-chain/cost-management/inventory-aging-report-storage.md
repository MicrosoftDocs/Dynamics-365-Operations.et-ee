---
title: Varude ajalise jaotuse aruande talletamine
description: Selles teemas kirjeldatakse funktsiooni, mis võimaldab teil käitada varude ajalise jaotuse aruannet ja muuta tulemus kättesaadavaks nii vormi kui ka diagrammi kujul.
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8a292bd7a7ccbb09af1955e1e253b45e230c1009
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005423"
---
# <a name="inventory-aging-report-storage"></a>Varude ajalise jaotuse aruande talletamine

[!include [banner](../includes/banner.md)]

Rakenduses Microsoft Dynamics 365 Supply Chain Management saate käitada **Varude ajalise jaotuse aruande talletamise** aruande ja muuta tulemuse kättesaadavaks nii vormi kui ka diagrammi kujul. Vormis reguleeritakse veerge ja koondsaldosid dünaamiliselt olenevalt konfigureeritud paigutusele. Diagramm annab visuaalse ülevaate, mis toetab filtreerimist ja võimaldab teil üksikasjadesse süvitsi minna. Lisaks võimaldab andmeüksus **Varude ajalise jaotuse aruanne** eksportida **Varude ajalise jaotuse aruande talletamise** aruande käivitamise tulemusi vormingus, nagu Microsoft Exceli fail või PDF-fail.

Selline **Varude ajalise jaotuse aruande talletamise** aruande käivitamise meetod on kasulik juhul, kui väljund sisaldab palju ridu. Näiteks sisaldab väljund palju ridu, kui teil on 50 000 kaupa ja 300 poodi, mis on loodud ladudena, ning taotlete varude ajalist jaotumist kauba, tegevuskoha ja lao järgi.

## <a name="enable-the-inventory-value-storage-report-feature"></a>Lubage funktsioon „Varude väärtuse talletuse aruanne”

Enne selle funktsiooni kasutamist peate selle oma süsteemis lubama. Administraatorid saavad kasutada [funktsioonide halduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja vajaduse korral see lubada. Siin on funktsioon loetletud järgmiselt.

- **Moodul** – kuluhaldus
- **Funktsiooni nimi** – varude ajalise jaotuse aruande talletamine

## <a name="run-an-inventory-aging-report-storage"></a>Varude ajalise jaotuse aruande talletamise käitamine

1. Avage **Kuluhaldus \> Päringud ja aruanded \> Lao varude ajalise jaotuse aruanne**.
1. Valige suvand **Uus**.
1. Väljale **Protsessi ID – nimi** sisestage aruandele kordumatu nimi.
1. Valige aruanne **Identimine – ID** ja filtreerige seda vastavalt vajadusele.

    Aruande käivitamine toimub alati pakett-töös.

1. Pärast pakett-töö lõpetamist kuvatakse väljund lehel **Lao varude ajalise jaotuse aruanne**.
1. Kui soovite vaadata väljundit vormina, millel on traditsiooniline ruudustiku paigutus, valige **Kuva üksikasjad**. Väljundi koonddiagrammina vaatamiseks valige **Kuva diagramm**.

    > [!NOTE]
    > Vorm ei sisalda aruande paigutuses määratletud vahesummasid.

Andmeüksus **Varude ajalise jaotuse aruanne** võimaldab teil eksportida **Varude ajalise jaotuse aruande talletamise** aruande väljundi, rakendades välja **Protsessi ID – nimi** filtri mis tahes vormile, mida andmehaldus toetab.
