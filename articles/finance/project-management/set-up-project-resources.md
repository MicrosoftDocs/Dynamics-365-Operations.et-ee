---
title: Projekti ressursside seadistamine
description: Selles teemas antakse teavet projekti ressursside seadistamise või taotlemise kohta.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c882e23794e3937f85b3e73774b36deaf28ac3ed
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760528"
---
# <a name="set-up-project-resources"></a>Projekti ressursside seadistamine

[!include [banner](../includes/banner.md)]

Peate seadistama kalendri ja seostama selle töötajaga. Kalendrit kasutatakse projekti ja sellele reserveeritud ressursside tööaja plaanimiseks. Kalendri seadistamisel saavad projektijuhid ressursside optimeerimise käigus ressursse ühtlustada. Kalendrigraafiku alusel saab ressurssidele piiranguid seada. Kalendri saab seadistada lehel **Kalendrid**.

Töötaja seadistamisel projekti ressursina saate valida töötajate hulgast, kes töötavad ettevõttes, millele ressursse seadistate. Teine võimalus on valida töötajaid oma organisatsiooni teistest ettevõtetest. Neid töötajaid nimetatakse kontsernisisesteks ressurssideks.

Järgmistes protseduurides selgitatakse, kuidas seadistada töötajat ettevõttes projektiressursina ja kuidas seadistada kontsernisisest projektiressurssi.

## <a name="set-up-a-worker-as-a-project-resource"></a>Töötaja seadistamine projekti ressursina

1. Valige lehel **Töötajad** loendist **Töötajad** töötaja, kelle projekti ressursina lisate, ja avage töötaja kirje..
2. Valige tegumiribalt **Projekt** &gt; **Seadistus** &gt; **Projekti seadistus**.
3. Valige kalender ja sulgege siis leht.

Saate määrata eelmäärangu tüübina ressursile ka vaikeprojekte. Eelmääranguid saab kasutada, kui ressursihaldur või projektijuht teab ette, milliste projektidega ressurss töötama hakkab. Eelmäärangud võivad põhineda ka projekti sponsori või kliendi soovil. Projekti eelmääramiseks valige lehelt **Projektide määramine** vahekaardil **Projektid** loendis **Järelejäänud projektid** sobiv projekt.

## <a name="set-up-an-intercompany-resource"></a>Kontsernisisese ressursi seadistamine

Töötaja seadistamisel kontsernisisese ressursina peate tegema seadistuse nii välja laenavas ettevõttes kui ka laenuks võtvas ettevõttes.

### <a name="in-the-lending-company"></a>Välja laenavas ettevõttes tehke järgmist

1. Kontrollige Finance’is, kas välja laenav ettevõte on valitud, ja läbige siis eelmises jaotises kirjeldatud protseduur „Töötaja seadistamine projekti ressursina“.
2. Tehke lehel **Kontserni raamatupidamine** valik **Uus**.
3. Valige väljalt **Juriidilise isiku ID** välja laenav ettevõte. Täitke vajalikul viisil ülejäänud väljad ja valige siis **Salvesta**.
4. Tehke lehel **Ülekande hind** valik **Uus**.
5. Valige väljalt **Laenav juriidiline isik** sobiv ettevõte.
6. Selleks, et laenata laenuks võtvale ettevõttele ainult see ressurss, mille jaotise alguses väljal **Ressurss** lõite, valige loodud ressursi nimi. Selleks, et teha välja laenavale ettevõttele kättesaadavaks kõik ettevõtte ressursid, jätke väli **Ressurss** tühjaks.
7. Määrake lehe **Projektihalduse ja raamatupidamise parameetrid** vahekaardil **Kontsernisisene** valiku **Luba kontsernisisene ressursside plaanimine ja ajatabelid** väärtuseks **Jah**.

### <a name="in-the-borrowing-company"></a>Laenuks võtvas ettevõttes tehke järgmist

- Sisestage lehel **Ressursside loend** otsingufiltrisse välja laenava ettevõtte jaoks loodud ressursi nimi, et kontrollida, kas see nimi sisaldub laenuks võtva ettevõtte ressursiloendis.

## <a name="request-project-resources"></a>Projekti ressursside taotlemine
Projekti ressursi plaanimise funktsioon võimaldab ressursihalduritel ainult komplekteeritud ressursse tegevustele või projektidele jagada. Selle funktsiooni lubamiseks tehke järgmised toimingud või veenduge, et need oleksid tehtud.

- Häälestage numbriseeriad.
- Seadistage projektihalduse ja raamatupidamise töövood.
- Luba ressursi taotluse töövood.

Pärast eelmiste toimingute tegemist võite teha vajaduse järgi järgmised toimingud.

- Luua esialgselt reserveeritud komplekteeritud ressursist ressursitaotlust.
- Jälgida ressursitaotlusi.
- Täita ressursitaotlusi.
- Taotleda WBS-ilt komplekteeritud ressurssi.
- Reserveerida projektile ressursse ilma komplekteeritud ressursi taotluseta.
