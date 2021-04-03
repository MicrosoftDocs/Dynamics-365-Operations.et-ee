---
title: Laokannete arhiivimine
description: Selles teema kirjeldatakse, kuidas arhiveerida laokannete andmeid süsteemi jõudluse parandamiseks.
author: sherry-zheng
manager: tfehr
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 3a0fa65eb728e4ce96bdfc3f7a0f04901551ccea
ms.sourcegitcommit: 70b1567d316f19c15a4b032b4897f15c8dcdca09
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/08/2021
ms.locfileid: "5556415"
---
# <a name="archive-inventory-transactions"></a>Laokannete arhiivimine

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Laokannete tabel (`InventTrans`) kasvab aja jooksul pidevalt ja kasutab aina rohkem andmebaasiruumi. Seetõttu muutuvad tabeli kohta tehtud päringud järk-järgult aeglasemaks. Selles teemas kirjeldatakse, kuidas te saate kasutada *laokannete arhiivi* funktsiooni laokannete andmete arhiveerimiseks, et parandada süsteemi jõudlust.

> [!NOTE]
> Valitud suletud pearaamatu perioodi jooksul saab arhiveerida ainult finantsiliselt värskendatud laokandeid. Arhiivimiseks peavad finantsiliselt uuendatud väljaminevate laokannete väljamineku olek olema *Müüdud* ja sissetulevate laokannete sissetuleku olek peab olema *Ostetud*.

Laokannete arhiivimisel teisaldatakse kõik seonduvad kanded tabelisse `InventTransArchive`. Lao väljaminekukanded ja lao sissetulekukanded arhiveeritakse eraldi kauba ID (`itemId`) ja laodimensiooni ID (`inventDimId`) kombinatsiooni alusel ning pannakse summeeritud väljamineku ja summeeritud sissetuleku kannete hulka.

Kui üks `itemId` ja `inventDimId` kombinatsioon sisaldab ainult ühte sissetuleku- või väljaminekukannet, siis kannet ei arhiivita.

## <a name="turn-on-the-feature-in-your-system"></a>Funktsiooni sisselülitamine teie süsteemis

Kui teie süsteemis ei ole veel selles teemas kirjeldatud funktsioone, avage [Funktsioonihaldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja lülitage funktsioon *Laokannete arhiiv* sisse.

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a>Mida on vaja enne laokannete arhiivimist arvesse võtta

Enne laokannete arhiivimist peaksite arvestama järgmiste äristsenaariumiga, sest see toiming mõjutab neid:

- Kui auditeerite laokandeid seonduvatest dokumentidest, nt ostutellimuse ridadest, kuvatakse need arhiivitud kannetena. Arhiveeritud kannete ülevaatamiseks peate avama kausta **Laovarude haldus \> Perioodilised ülesanded \> Puhastamine \> Laokannete arhiiv**.
- Lao sulgemist ei saa arhiivitud perioodide puhul tühistada. Enne, kui saate lao sulgemise tühistada, peate tagasi pöörama laokannete arhiivi vastava perioodi kohta.
- Standardkulu teisendamist ei saa arhiivitud perioodideks teha. Enne, kui saate standardkulu teisendada, peate tagasi pöörama laokannete arhiivi vastava perioodi kohta.
- Laokannete arhiivimine mõjutab laokannetest hangitud laoaruandeid. Need aruanded sisaldavad laovarude ajalise jaotuse aruannet ja laovarude väärtuse aruandeid.
- Laovarude prognoose võib mõjutada nende käitamine arhiveeritud perioodide perioodi jooksul.

## <a name="prerequisites"></a>Eeltingimused

Laokandeid saab arhiveerida ainult neil perioodidel, mille puhul on täidetud järgmised tingimused:

- Pearaamatu periood peab olema suletud.
- Lao sulgemine peab olema käitatud arhiivi perioodi lõppkuupäeval või pärast seda.
- Periood peab olema vähemalt üks aasta enne arhiivi perioodi alguskuupäeva.
- Varude ümberarvutusi ei tohi olla.

## <a name="archive-inventory-transactions"></a>Laokannete arhiivimine

Laokannete arhiivimiseks toimige järgmiselt.

1. Avage kaust **Varude haldus** \> **Perioodilised ülesanded** \> **Puhastamine** \> **Laokannete arhiiv**.

    Kuvatakse leht **Laokannete arhiiv** ja sellel kuvatakse arhiivitud protsessikirjete loend.

    ![Laokannete arhiivi leht](media/archive-inventory-empty.png "Laokannete arhiivi leht")

1. Valige tegevuspaanil laokannete arhiivi loomiseks **Laokannete arhiiv**.
1. Seadke dialoogiboksis **Laokannete arhiiv** kiirkaardil **Parameetrid** järgmised väljad:

    - **Suletud pearaamatu perioodi alguskuupäev** – valige varaseim kande kuupäev arhiivi kaasamiseks.
    - **Suletud pearaamatu perioodi lõppkuupäev** – valige hiliseim kande kuupäev arhiivi kaasamiseks.

    ![Laokannete arhiivi dialoogiboks](media/archive-inventory-dates.png "Laokannete arhiivi dialoogiboks")

    > [!NOTE]
    > Valida saab ainult [eeltingimustele](#prerequisites) vastavad perioodid.

1. Seadistage kiirkaardil **Käivita taustal** pakett-töötluse üksikasjad vastavalt vajadusele. Järgige teenuse Microsoft Dynamics 365 Supply Chain Management tavalisi pakett-tööde etappe.
1. Valige nupp **OK**.
1. Saate teate, mis palub teil kinnitada, et soovite jätkata. Lugege teade hoolikalt läbi ja valige vastus **Jah**, kui soovite jätkata.

    Saate teate, et teie laokannete arhiivitöö on lisatud pakett-töötluse järjekorda. Töö alustab nüüd valitud perioodi laokannete arhiivimist.

## <a name="view-archived-inventory-transactions"></a>Kuva arhiivitud varude kanded

Lehel **Laokannete arhiiv** kuvatakse teie täielik arhiivimisajalugu. Igal ruudustiku real kuvatakse selline teave nagu arhiivi loomise kuupäev, arhiivi loonud kasutaja ja selle olek.

![Arhiivimisajalugu lehel Laokannete arhiivimine](media/archive-inventory-full.png "Arhiivimisajalugu lehel Laokannete arhiivimine")

Valige ruudustikus kuvatavate arhiivide filtreerimiseks lehe ülaosas asuvast ripploendist üks järgmistest väärtustest:

- **Aktiivne** – kuvatakse ainult aktiivsed arhiivid, mitte tagasipööratud arhiivid.
- **Kõik** – kuvatakse kõik arhiivid, nii aktiivsed kui ka tagasipööratud.

Iga arhiivi kohta ruudustikus esitatakse järgmine teave:

- **Aktiivne** – märge näitab, et arhiiv on aktiivne.
- **Alguskuupäev** – vanima kande kuupäev, mille saab arhiivi kaasata.
- **Lõppkuupäev** – uusima kande kuupäev, mille saab arhiivi kaasata.
- **Planeerija** – arhiivi loonud kasutajakonto.
- **Teostatud** – arhiivi loomise kuupäev.
- **Tagasipööratud** – märge näitab, et arhiiv on tagasi pööratud.
- **Peata praegune uuendus** – märge näitab, et arhiivimine on pooleli, kuid see on peatatud.
- **Olek** – arhiivi töötlemise olek. Võimalikud väärtused on *Ootel*, *Pooleli* ja *Lõpetatud*.

Ruudustiku kohal tööriistaribal on järgmised nupud, mida saate kasutada valitud arhiiviga töötamiseks:

- **Arhiivitud kanded** – saate vaadata valitud arhiivi kõiki üksikasju. Ilmuval lehel **Arhiivitud kanded** kuvatakse kõik arhiivis olevad kanded.

    ![Leht Arhiivitud kanded](media/archive-inventory-transactions.png "Leht Arhiivitud kanded")

    Konkreetse kande kohta lisateabe vaatamiseks lehel **Arhiveeritud kanded** valige see ruudustikus ja seejärel valige tegevuspaanil **Arhiivitud kande üksikasjad**. Ilmuval lehel **Arhiivitud kande üksikasjad** kuvatakse selline teave nagu pearaamatu sisestamine, seotud alammooduli viited ja finantsdimensioonid.

- **Peata arhiivimine** – saate peatada praegu töödeldava valitud arhiivi. Peatamine jõustub alles pärast arhiivimisülesande loomist. Seega võib peatamise jõustumine toimuda viivitusega. Kui arhiiv on peatatud, kuvatakse väljal **Peata praegune uuendus** märge.
- **Jätka arhiivimist** – saate jätkata praegu peatatud valitud arhiivi töötlemist.
- **Pööra tagasi** – saate valitud arhiivi tagasi pöörata. Arhiivi saate tagasi pöörata ainult siis, kui selle välja **Olek** väärtuseks on seatud *Lõpetatud*. Kui arhiiv on tagasi pööratud, kuvatakse väljal **Tagasipööratud** märge.
