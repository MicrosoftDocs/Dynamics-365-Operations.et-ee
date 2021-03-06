---
title: Aadressimuudatuste vaatamine ja haldamine
description: Selles teemas selgitatakse, kuidas vaadata ja hallata aadressimuudatusi rakenduses Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-07
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 751e903b011b74fad584a1a22b574134610aa3d2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051757"
---
# <a name="view-and-manage-address-changes"></a>Aadressimuudatuste vaatamine ja haldamine

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas selgitatakse, kuidas saate vaadata ja hallata aadressimuudatusi töövõtja iseteeninduse lehel **Isikuandmete redigeerimine** või **Töötaja** üksikasjade lehel rakenduses Dynamics 365 Human Resources.

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

1. Valige oma avalehel paan **Töövõtja iseteenindus**.

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

3. Valige töötaja ja seejärel **Aadressid**.

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

Personaliosakonna töötajad saavad vaadata ja jälgida muudatusi tööruumis **Personalihaldus**. Aadressimuudatuste vaatamiseks avage **Avalehel** paan **Personalihaldus**. Aadressimuudatused kuvatakse paanil ülemises parempoolses nurgas. Jaotise **Aadressimuudatused** kohal olev arv näitab, mitu korda muudeti aadressi lehel **Inimressursside parameetrid** täpsustatud päevade jooksul. 

Kui valite paani **Aadressimuudatused**, kuvatakse uuel leheküljel iga aadressimuudatuse üksikasjad. Soovi korral saate valida ülemises parempoolses nurgas suvandi **Kaasa tulevased aadressimuudatused**, et kuvada tulevase kuupäevaga aadressimuudatused.

> [!NOTE]
> Kui soovite aadressimuudatuste puhul saada teatist või e-kirja, saate toimingupaani vahekaardil **Suvandid** luua uue teatisereegli. Lisateavet teatisereeglite kohta leiate teemast [Teatisereeglite loomine](../fin-ops-core/fin-ops/get-started/create-alerts.md).<br><br>

> Kui soovite aadressimuudatuste jaoks konfigureerida töövoogu, saate valida oma teatisereeglis suvandi **Saada väliselt** ning kasutada seejärel ärisündmuse käivitamiseks ja töövoo konfigureerimiseks rakendust Power Automate. Lisateavet leiate teemast [Teatised ärisündmustena](../fin-ops-core/fin-ops/get-started/create-alerts.md#alerts-as-business-events).


[!INCLUDE[footer-include](../includes/footer-banner.md)]