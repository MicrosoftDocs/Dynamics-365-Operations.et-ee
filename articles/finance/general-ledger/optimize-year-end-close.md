---
title: Aastalõpu sulgemise optimeerimine
description: See artikkel kirjeldab optimeerimise aasta lõpu sulgemise teenuse lisandmoodulit, mis on saadaval pearaamatu aasta lõpu sulgemise protsessis.
author: moaamer
ms.date: 11/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2022-11-28
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 41d0c2975341cf3d612cc36be348326e24e94f1b
ms.sourcegitcommit: 707957bb7bcd98faf2600eff1c98067901a0fb73
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/08/2022
ms.locfileid: "9749994"
---
# <a name="optimize-year-end-close"></a>Aastalõpu sulgemise optimeerimine

Optimeerimise aasta Microsoft Dynamics lõpu sulgemise teenuse lisandmoodul 365 Finantside jaoks võimaldab aasta lõpu sulgemise töötlust käitada väljaspool Rakendusobjekti serveri (AOS) eksemplari Dynamics 365 finantsressursside jaoks. See kasutab mikroteenuste tehnoloogia. Aasta lõpu sulgemise optimeerimise funktsiooniga seostatud soodustused hõlmavad täiustatud jõudlust ja minimeeritud mõju SQL-andmebaasile aasta lõpu sulgemise töötlemise ajal.

Aasta lõpu sulgemise optimeerimise funktsiooni kasutamiseks peate lõpule täitma järgmised ülesanded:

1. Installige oma projekti optimeerimise aasta lõpu sulgemise teenuse lisandmoodul elutsükli Microsoft Dynamics teenuses.
2. Funktsioonihalduses **aasta lõpu sulgemise** optimeerimise funktsiooni lubamine

> [!NOTE]
> Finantsressursside praeguse aasta lõpu sulgemise funktsiooni saate siiski **kasutada, keelates funktsioonihalduses aasta lõpu optimeerimise** funktsiooni.

## <a name="improved-performance"></a>Parem jõudlus

Optimeerimise **aasta lõpu sulgemise funktsioon** on loodud kiirendama aasta lõpu sulgemist, eriti klientide puhul, kellel on suuri andmekoguseid. Kui aasta lõpu sulgemine käitab teenust, laaditakse raske töötlus finantsressurssidest välja, et vähendada töötlemisaega ja ressursid vabastada, mis võivad mõjutada teiste kasutajate igapäevaseid toiminguid.

Optimeerimise **aasta lõpu sulgemise** funktsioon aitab teil saavutada järgmisi eesmärke:

- Parandage aasta lõpu sulgemise jõudlust käitusaja vähendamise abil.
- Vähendage mõju muudele protsessidele aasta lõpu sulgemise käituse ajal.
- Parandada aasta lõpu tulemuste aruandlust ja korrigeerimisi, kuna aasta lõpu sulgemine võtab vähem aega.

## <a name="new-options-and-visibility"></a>Uued valikud ja nähtavus

Kui optimeerimise **aasta lõpu sulgemise** funktsioon on lubatud, lisatakse kaks uut veergu, **·** **tulemused** ja olek järgmistesse kohtadesse:

- **Aasta lõpu sulgemislehel**
- Aasta lõpu **sulgemise tulemuste dialoogiboksis**
- Aasta lõpu **lõpu sulgemise mallilehe** finantsdimensiooni **ülekandmise valikutes**

Järgmine näide näitab näiteid Tulemuste ja **Olekuveergude** **kohta** aasta **lõpu sulgemislehel**. Aasta lõpu sulgemise **tulemuste** avamiseks **saate** valida veerus Tulemused lingi Kuva tulemused. Veerus **Olek** kuvatakse aasta lõpu sulgemise protsessi praegune olek. Seetõttu pakuvad uued veerud aasta lõpu sulgemise protsessi edenemise nähtavust.

[![Aasta lõpu sulgemislehe tulemused ja olekuveerud.](./media/Yearendclose.jpg)](./media/Yearendclose.jpg)

Lisaks, kui optimeerimise **aasta lõpu sulgemise** funktsioon on **lubatud,** **muutub bilansi finantsdimensioonide kiirkaart kättesaadavaks aasta lõpu sulgemise mallilehel**. Selle kiirkaardi abil saate aasta sulgemisel määrata üksikasjalikult bilansi finantsdimensioonid. See võimalus on paralleelselt võimalusega, mis on juba kasumi- ja kahjumikontode jaoks saadaval.

## <a name="architecture-and-data-flow"></a>Arhitektuur ja andmevoog

Optimeerimise **aasta lõpu sulgemise** **funktsiooni** kasutamiseks ja aasta lõpu sulgemise käivitamiseks mikroteenuses peate installima teenuse Optimeeri aasta lõpu sulgemise teenuse lisandmooduli elutsükli teenustest ja seejärel lubama aasta lõpu sulgemise optimeerimise funktsiooni Funktsioonihalduses.

Nagu järgmine näide näitab, kontrollib aasta lõpu lõpu sulgemine, kas lisandmoodul on installitud ja funktsioon lubatud. Kui mõlemad eeltingimused on täidetud, käitab aasta lõpu sulgemine mikroteenust.

[![Andmevoo diagramm.](./media/Lifecycle-services.jpg)](./media/Lifecycle-services.jpg)

## <a name="high-level-flow-for-year-end-close-processing"></a>Kõrgtasemeline voog aasta lõpu sulgemise töötlemiseks

1. Aasta lõpu sulgemisprotsess algab finantsis, pearaamatu perioodi **\> sulgemise aasta \> lõpu sulgemine**. Protsess loob sulgevatele juriidilistele isikutele pakett-tööde ja ülesannete sulgemise.
2. Aasta lõpu sulgemine määrab, kas aasta lõpu sulgemist peaks käitama mikroteenuses või praeguses sulgemisloogikas.

    - Kui optimeerimise aasta **lõpu** teenuse lisandmoodul on installitud elutsükli teenustes ja funktsioonihalduses on lubatud optimeerimise aasta lõpu sulgemise funktsioon, käitatakse aasta lõpu sulgemist mikroteenused.

        1. Optimeerimise aasta lõpu sulgemise funktsioon loob iga suletud juriidilise isiku kohta aasta lõpetamise teenusetöö ja käivitab seejärel aasta lõpu sulgemise loogika. Mikroteenused teeb aasta lõpu sulgemise.
        2. Finantsid kuulavad aasta lõpu sulgemist mikroteenusel, et määrata, millal mikroteenused on lõpetatud. Finantsid uuendatakse aasta lõpu **sulgemise** lehel aasta sulgemise tulemusi.

    - Vastasel juhul käivitatakse aasta lõpu sulgemine praeguses sulgemisloogikas.
