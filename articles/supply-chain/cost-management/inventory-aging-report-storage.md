---
title: Varude ajalise jaotuse aruande talletamine
description: See artikkel kirjeldab funktsioone, mis võimaldab teil käivitada varude aegumisaruande ning muuta toodangu kättesaadavaks vormi ja diagrammina.
author: JennySong-SH
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1d810ec90c85f2f7758ec01ef4b24611e026cc80
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875564"
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]