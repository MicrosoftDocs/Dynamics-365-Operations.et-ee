---
title: Aadressimuudatuste vaatamine ja haldamine
description: See artikkel selgitab, kuidas vaadata ja hallata aadressi muudatusi Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-08-07
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 744ab532fcc663f25ce376817779924bbef15432
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899581"
---
# <a name="view-and-manage-address-changes"></a>Aadressimuudatuste vaatamine ja haldamine


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel selgitab, **kuidas** vaadata ja hallata aadressi muudatusi lehel Isiklike üksikasjade redigeerimine (**mille avate töötaja iseteeninduse** tööruumist) **või töötaja** üksikasjade lehel Dynamics 365 Human Resources.

Paljud organisatsioonid tahavad, et töövõtjad haldaksid oma isikuandmeid iseteeninduse kaudu. Saate lubada kasutajatel tööruumis **Töövõtja iseteenindus** oma aadressi värskendada. Seejärel saate muudatusi jälgida tööruumis **Personalihaldus**. Selle funktsiooni kasutamiseks peate määrama päevade arvu, mille jooksul soovite vaadata muudatusi lehel **Inimressursside parameetrid**.

## <a name="configure-address-change-parameters"></a>Aadressimuudatuse parameetrite konfigureerimine

Et konfigureerida päevade arv, mille jooksul soovite tööruumis **Personalihaldus** aadressimuudatusi kuvada, tehke järgmist.

1. Valige navigeerimispaanil **Personalihaldus**.
2. Valige **Lingid**.
3. Valige **Inimressursside parameetrid**.
4. Sisestage jaotises **Aadressimuutus** väljale **Päevade arv** päevade arv, mille jooksul soovite kuvada aadressimuudatusi tööruumis **Personalihaldus**.
5. Sulgege leht.

## <a name="create-or-change-an-employee-address"></a>Töövõtja aadressi loomine või muutmine

Töövõtjad saavad oma aadressi värskendada tööruumis **Töövõtja iseteenindus**. Aadressi loomiseks või muutmiseks toimige järgmiselt.

1. Valige Avalehelt **töötaja** iseteeninduspaan **·**.
2. Valige **Redigeeri isikuandmeid**.
3. Aadressi lisamiseks valige **Lisa**. Olemasoleva aadressi värskendamiseks valige loendist aadress ja seejärel valige **Redigeeri**.
4. Sisestage **Nimi või kirjeldus**.
5. Valige rippkast **Eesmärk** ja seejärel aadressi tüüp.
6. Sisestage **Riik/regioon**.
7. Sisestage **Sihtnumber**.
8. Sisestage **Tänav**.
9. Sisestage **Linn**, **Osariik** ja **Maakond**. Tavaliselt täidetakse need väljad automaatselt välja **Sihtnumber** alusel.
10. Võite valida ka välja **Esmane**, et määrata esmane aadress. Esmaseks saab märkida ainult ühe aadressi. Kui muu aadress on juba märgitud esmaseks aadressiks, peate kinnitama, et soovite seda aadressi esmasena kasutada.
11. Võite valida ka välja **Privaatne**, et näidata, et aadress on privaatne. Seda aadressi saavad vaadata ainult kasutajad, kellel on privaatse aadressi teabe vaatamiseks sõnaselge õigus.
12. Valige nupp **OK**.

## <a name="create-or-change-a-worker-address"></a>Töötaja aadressi loomine või muutmine

Aadressi saate värskendada tööruumis **Personalihaldus**. Aadressi loomiseks või muutmiseks toimige järgmiselt.

1. Valige tööruumis **Personalihaldus** suvand **Lingid** ja seejärel **Töötajad**.
2. Valige töötaja ja seejärel **Aadressid**.
3. Aadressi lisamiseks valige **Lisa**. Olemasoleva aadressi värskendamiseks valige loendist aadress ja seejärel valige **Redigeeri**.
4. Sisestage **Nimi või kirjeldus**.
5. Valige rippkast **Eesmärk** ja seejärel aadressi tüüp.
6. Sisestage **Riik/regioon**.
7. Sisestage **Sihtnumber**.
8. Sisestage **Tänav**.
9. Sisestage **Linn**, **Osariik** ja **Maakond**. Tavaliselt täidetakse need väljad automaatselt välja **Sihtnumber** alusel.
10. Võite valida ka välja **Esmane**, et määrata esmane aadress. Esmaseks saab märkida ainult ühe aadressi. Kui muu aadress on juba märgitud esmaseks aadressiks, peate kinnitama, et soovite seda aadressi esmasena kasutada.
11. Võite valida ka välja **Privaatne**, et näidata, et aadress on privaatne. Seda aadressi saavad vaadata ainult kasutajad, kellel on privaatse aadressi teabe vaatamiseks sõnaselge õigus.
12. Valige nupp **OK**.
 
## <a name="create-a-future-change-for-an-address"></a>Aadressi jaoks tulevase muudatuse loomine

Mõnel juhul võite soovida värskendada aadressi tulevikus. Näiteks tuleks see kasuks, kui töövõtja kolib järgmise kuu 15. kuupäeval.

1. Avage leht **Aadresside haldamine**, valides ükskõik millisest aadressiruudustikust **Rohkem suvandeid > Täpsemalt**.
2. Valige uue aadressi loomiseks **Uus**.
3. Sisestage aadressi üksikasjad.
4. Valige kiirkaart **Üldine**.
5. Valige väljal **Jõustumiskuupäev** kuupäev, mil uus aadress jõustub.
6. Võite väljal **Aegumiskuupäev** valida, millal aadress enam ei kehti.
7. Sulgege lehed.

## <a name="view-and-monitor-address-changes"></a>Aadressimuudatuste vaatamine ja jälgimine

Personaliosakonna töötajad saavad vaadata ja jälgida muudatusi tööruumis **Personalihaldus**. Aadressi muudatuste vaatamiseks valige Avalehelt **personalihalduse** paani **·**. Aadressi muudatused kuvatakse paanil ülemises parempoolses nurgas. Ülaltoodud aadressi **muutmisel** kuvatakse lehel **Inimressursid määratud päevade arvu jooksul toimunud aadressimuudatuste** arv. 

Kui valite paani **Aadressimuudatused**, kuvatakse uuel leheküljel iga aadressimuudatuse üksikasjad. Soovi korral saate valida ülemises parempoolses nurgas suvandi **Kaasa tulevased aadressimuudatused**, et kuvada tulevase kuupäevaga aadressimuudatused.

> [!NOTE]
> Kui soovite aadressimuudatuste puhul saada teatist või e-kirja, saate toimingupaani vahekaardil **Suvandid** luua uue teatisereegli. Lisateavet teatisereeglite kohta leiate teemast [Teatisereeglite loomine](../fin-ops-core/fin-ops/get-started/create-alerts.md).
>
> Kui soovite aadressimuudatuste jaoks konfigureerida töövoogu, saate valida oma teatisereeglis suvandi **Saada väliselt** ning kasutada seejärel ärisündmuse käivitamiseks ja töövoo konfigureerimiseks rakendust Power Automate. Lisateavet leiate teemast [Teatised ärisündmustena](../fin-ops-core/fin-ops/get-started/create-alerts.md#alerts-as-business-events).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
