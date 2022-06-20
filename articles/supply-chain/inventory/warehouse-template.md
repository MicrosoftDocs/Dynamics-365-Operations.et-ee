---
title: Lao häälestus lao konfiguratsioonimalli abil
description: See artikkel selgitab, kuidas seadistada ladu, kasutades lao konfiguratsiooni malli.
author: yufeihuang
ms.date: 11/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportEnhanced, DMFDefinitionGroupTemplate, DMFEntityTemplateDefinitionLoadDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 737b6f2f645ff270e5a49d54ca7542df3c075f94
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856102"
---
# <a name="set-up-a-warehouse-by-using-a-warehouse-configuration-template"></a>Lao häälestus lao konfiguratsioonimalli abil

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas seadistada ladu, kasutades lao konfiguratsiooni malli. Saate kasutada mitut eelmääratud konfiguratsioonimalli. Teavet nende mallide kasutamise kohta leiate teemast [„Konfigureerimisandmete mallid”](../../fin-ops-core/dev-itpro/data-entities/configuration-data-templates.md).

## <a name="scenarios-where-configuration-templates-can-be-helpful"></a>Stsenaariumid, mille puhul konfiguratsioonimallid võivad kasulikud olla

Konfiguratsioonimallid võivad kasulikud olla mitme stsenaariumi puhul. Järgmisena on toodud mõned näited.

- Olete konfiguratsiooni seadistamise lõpetanud ja seda testimiskeskkonnas testinud ning soovite nüüd seadistuse tootmiskeskkonda kopeerida.
- Soovite lao seadistuse mitmele juriidilisele isikule üle kanda või luua samale juriidilisele isikule uue lao.
- Soovite kiiresti ette valmistada lao funktsioonide demo.
- Soovite olemasolevate kaupade ja ladude puhul varude halduse funktsionaalsuse asemel kasutada laohalduse funktsionaalsust.

See artikkel keskendub esimesele neist stsenaariumidest. See näitab, kuidas konfiguratsioonimalli abil konfiguratsiooni seadistust testimiskeskkonnast tootmiskeskkonda kopeerida.

## <a name="copy-a-configuration-setup-from-a-test-environment-to-a-production-environment"></a>Konfiguratsiooni seadistuse kopeerimine testimiskeskkonnast tootmiskeskkonda

Selle stsenaariumi puhul on testimiskeskkonnas juba olemas lao ja mõne kande protsessi konfiguratsiooni seadistus. Nüüd soovite laohoone konfiguratsiooni seadistuse testimiskeskkonnast tootmiskeskkonda kopeerida.

> [!NOTE]
> Konfiguratsiooni seadistuse kopeerimisel on oluline kaasata muud seotud seadistuse andmed. Näiteks soovite testimiskeskkonnast seadistust kopeerides tooted seadistada. Siiski ei saa toote fikseeritud komplekteerimiskohta enne toote loomist seadistada. Kuigi üksikud konfiguratsioonimallid ei toeta seda tüüpi sõltuvust, on olemas seda toetavaid vaikeandmemalle. Saate need vaikeandmemallid hõlpsalt konfiguratsiooni protsessi kaasata.

### <a name="export-a-default-warehouse-template"></a>Lao vaikemalli eksportimine 

1. Avage tööruum **Andmehaldus**.

    > [!NOTE]
    > Kui kasutate seda tööruumi esimest korda, tuleb teil jätkamiseks kõik andmeüksused laadida.

2. Vaikemallide laadimiseks valige paan **Mallid** ja seejärel **Vaikemallide laadimine**.

    > [!NOTE]
    > Valik **Vaikemallide laadimine** on saadaval ainult **täiustatud** vaates. Valige **Raamistiku parameetrid** ja seejärel väli **Vaikeväärtuste kuvamine** ning tehke seal valik **Täiustatud vaade**.

3. Vaikemallide laadimise järel saate neid oma äri vajaduste kohaselt muuta.

    > [!NOTE]
    > Vaikemallide laadimiseks ja mallide importimiseks peab teil olema süsteemiadministraatori juurdepääs. See nõue aitab tagada kõikide üksuste korrektse malli laadimise.

4. Veenduge, et oleksite selle juriidilise isiku kontol, millele soovite ettevõttekohaseid andmeid eksportida.
5. Valige tööruumis käsk **Ekspordi**.
6. Looge uus eksportimisprojekt.
7. Valige **+ malli lisamine** ja leidke lao vaikemall **400 - WMS**. See mall lisab andmeüksused lao konfiguratsiooni.

    > [!NOTE]
    > Kui eksporditavaid andmeid tuleb filtrida (nt soovite eksportida ainult kindla laoga seotud andmeid), peate igat andmeüksust hindama ja lisama filtrimise päringu kaudu. Teise võimalusena võite eksportida kõik andmed ja seejärel kustutada kirjed, mida pole sihtfailides vaja.

8. Valige **Ekspordi**. Eksporditakse kõik projekti andmeüksustega seotud andmed.

Teil on võimalik andmed ZIP-failina alla laadida. See fail sisaldab kõiki valitud vormingus andmeid (nt Exceli vormingus). Nagu öeldud, tuleb võib-olla mõnda kirjet andmefailides enne tootmiskeskkonda importimist värskendada. Kirje värskendamisel veenduge, et te ei muudaks faili nime.

### <a name="import-a-warehouse-configuration-setup"></a>Lao konfiguratsiooni seadistuse importimine

1. Veenduge sihtkeskkonnas, et oleksite selle ettevõtte kontol, kuhu soovite laoandmed importida.

    > [!NOTE]
    > Enne importimist peaksite tuvastama andmete vahelised sõltuvused. Näiteks sisaldab mall **Laohaldus** andmeüksust nimega **Lao likvideerimiskoodid**. See üksus sisaldab andmeid, mis on seotud seadistuslehega **Likvideerimiskoodid** (**Laohaldus** > **Seadistamine** > **Mobiilne seade** > **Likvideerimiskoodid**). Kui olemasolev seadistus tegeleb juba müügitellimuste tagastusprotsessiga, sisaldab väli **Tagastamise likvideerimiskood** väärtust. Selle välja likvideerimiskood on seotud andmeüksusega **Likvideerimiskood**, mis kuulub malli **Müük ja turundus**. Kui andmeüksuse **Likvideerimiskood** andmeid ei impordita enne väljalt **Lao likvideerimiskoodid** andmete importimist, siis importimine nurjub.

2. Valige tööruumis **Andmehaldus** käsk **Impordi**.
3. Looge uus importimisprojekt.
4. Valige **+ lisa fail** ja laadige andmed üles ZIP-failina.
5. Valige **Impordi**. **Täiustatud** vaates saate importimisel tekkida võivatest probleemidest kiiresti ülevaate, kui kasutate suvandit **Filtreeri**.

Käsk **Kuva käivituslogi** annab üksikasjaliku teabe iga imporditud andmeüksuse kohta. Kiirelt sihtandmete juurde jõudmiseks saate kasutada andmete ajastamise vaadet. Sel viisil näete, kuidas imporditud andmed rakenduse seotud lehekülgedel välja näevad. Vaikeandmemallide kasutamisel töötab importimise järjestus iga andmeüksuse puhul eelmääratud viisil, tagamaks, et sõltuvad andmed imporditakse esimesena. Kui projekti kuuluvad kohandatud andmeüksused, peate veenduma, et õige järjekord oleks määratud. Lisateavet vaadake teemast [„Konfigureerimisandmete mallid”](../../fin-ops-core/dev-itpro/data-entities/configuration-data-templates.md).

Rohkem teavet selle kohta, kuidas kasutada laomalli, et kopeerida lao konfiguratsiooni ühest ettevõttest sama eksemplari uude ettevõttesse, leiate järgmisest 3-minutilisest YouTube’i videost: [Laomalli kasutamine konfiguratsiooni kopeerimiseks rakenduses Finance and Operations](https://www.youtube.com/watch?v=K2WIfFlqJYs).

## <a name="related-article"></a>Seostuv artikkel

[Konfigureerimisandmete mallid](../../fin-ops-core/dev-itpro/data-entities/configuration-data-templates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]