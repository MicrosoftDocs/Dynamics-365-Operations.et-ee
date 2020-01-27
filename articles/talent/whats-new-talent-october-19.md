---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent Core HR (16. oktoober 2018)
description: Selles teemas kirjeldatakse funktsioone, mis on kas uued või muutunud rakenduses Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d5f2aea5fcc81d0b4c1d8a392a3e56c888440a94
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897392"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-16-2018"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent Core HR (16. oktoober 2018)

**Järk 8.1.1067**

Teema kirjeldab funktsioone, mis on Core HR-is kas uued või muudetud.

## <a name="allow-managers-to-update-time-off-requests"></a>Lubage juhatajatel värskendada vabade päevade taotluseid

Töövõtjate vabade päevade taotlused võivad pärast töövoos heakskiitmist uuendamist vajada. Paljudel juhtudel teeb juhataja need uuendused töövõtja nimel. See uus funktsioon võimaldab juhatajatel värskendada või tühistada vabade päevade taotlusi oma töövõtjate nimel. Seda võimalust juhib **Töötamine kellegi nimel** parameeter, mida saab seadistada **Inimressursside parameetrite** lehel. 
 
## <a name="allow-hr-to-update-time-off-requests"></a>Lubage personaliosakonnal värskendada vabade päevade taotluseid

Sarnaselt ülalolevale funktsioonile saab personaliosakond värskendada vabade päevade taotlused, kui need on eelnevalt läbi töövoo heaks kiidetud. See funktsioon võimaldab personaliosakonna kasutajatel värskendada vabade päevade taotlusi. Võimaluse saab lubada **Inimeste** tööruumis ja **Töötaja** lehel, kasutades uut suvandit nimega **Kuva vabad päevad**. Nendel lehtedel saavad personaliosakonna kasutajad vaadata ja värskendada vabade päeavade kandeid, sarnaselt sellele, kuidas juhatajad neid tegevusi teevad.

Turbekohustus, mis kontrollib selle funktsionaalsuse ligipääsu on järgmine.
- Kohustus: töötajapõhiste puhkuste ja puudumiste protsesside haldamine.
- Privileeg: kõigi töötajate puhkuste ja puudumiste taotluste haldamine.

## <a name="other-changes"></a>Muud muudatused
Selles väljaandes on tehtud järgmised uuendused.
- Muutused töötaja palkamise toimingutes, et nad ei ole enam "kinni" **Töövoog on lõpetatud** olekus.
- Töösuhte kirje saab nüüd luua ilma töösuhte alguskuupäevata.
- Dynamics 365 Talenti registreerimiskuupäev Töövõtja iseteeninduses kuvatud kursusele rakendab nüüd ajavööndi nihke kuupäeva.
- Exceli faile saab importida mitu korda ilma vigadeta, kasutades **Töötaja üksust**.

## <a name="known-issue"></a>Teadaolev probleem

- **Probleemi**: uuele töötajale seotuse lisamisel on nupud **Uus** ja **Redigeeri** hallid. 
- **Lahendus:** veenduge enne manuse lehe avamist, et **Töötaja** lehe kiirinfod oleksid suletud. Kui kiirinfod on lehe **Töötaja** laadimisel suletud, on manuste nupud lubatud. (See probleem lahendatakse järgmisel platvormivärskendusel.)
