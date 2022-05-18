---
title: TDS-i grupi, PAN-i ja TAN-i teabe häälestus hankijatele ja klientidele
description: See teema kirjeldab, kuidas seadistada teavet maksu kohta allika (TDS) grupis, püsikonto numbri (PAN) ja maksukonto numbri (TAN) kohta hankijatele ja klientidele.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 83ec532e95bde553c3a339e2ca103ebaacdb52ae
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726945"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a>TDS-i grupi, PAN-i ja TAN-i teabe häälestus hankijatele ja klientidele

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas seadistada teavet maksu kohta allika (TDS) grupis, püsikonto numbri (PAN) ja maksukonto numbri (TAN) kohta hankijatele ja klientidele.

1. Minge **Ostureskontro \> Hankijatele \> Kõik hankijad** või **Müügireskontro \> kliendid \> Kõik kliendid**.

    [![Kõigi hankijate leht.](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)

2. Tegevuspaanil valige **Uus** TDS-ile kinnipeetava maksu grupi loomiseks ja sisestage nõutavad üksikasjad. Teise võimalusena valige olemasolev hankija või klient.
3. Määrake suvandi **Arve ja tarne** kiirkaardil **Kinnipeetava maksu** jaotises **Kinnipeetava maksu arvutamine** väärtuseks **Jah** et arvutada hankijale või kliendile kinnipeetav maks, TDS või mks, mis on kogutud allikasse (TCS).
4. Ostuarve TDS arvutatakse hankijale või kliendile määratud TDS-i vaikegrupi alusel. Valige TDS grupp väljal **TDS grupp**.

    > [!NOTE]
    > Kui valite TDS grupi **TDS-i grupp** väljal, muutuvad **Kinnipeetava maksu grupp** ja **TCS-grupp** kättesaamatuks.

5. Valige **Maksuteabe** kiirkaardi **PAN-teabe** jaotises **Olek** hankija või kliendi püsikonto jaoks olek püsiv:

    - **Pole saadaval** – hankijal või kliendil ei ole PAN-i.
    - **Saadud** – hankijal või kliendil on PAN.
    - **Rakendatud** – hankija või klient on taotlenud PAN-i.
    - **Kehtetu** – hankijal või kliendil on PAN, kuid see ei kehti.

6. Kui valisite **Saadud** **Olek** väljal et näidata hankijale või kliendile PAN-i omamist, sisestage PAN **Numbri** väljale. PAN peab koosnema viiest tähestikumärgist, seejärel neljast numbrimärgist ja seejärel ühest tähestikumärgist. Siin on näide: : **ABCDE1260A**.
7. Kui valisite **Saadud** **Olek** väljal et näidata hankijale või kliendile PAN-i omamist, sisestage viitenumber **Viitenumbri** väljale.
8. Vaadake hankija või kliendi hinnalepete kategooria olemust Kinnipeetava maksu väljal, mis on **Hinna hindamise** väljagrupis:

    - Ettevõte
    - HUF
    - Kinnita
    - Üksikisik
    - AOP
    - BOI
    - Kohalik omavalitsus
    - Muud

    [![Maksuteabe kiirkaart.](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)

9. Seejärel, tegevuspaani **Hankija** vahekaardil, grupis **Kvaliteedijuhtimine**, valige **Registreerumine IDs**, et avada leht **Hallata aadresse**.
10. **Aadresside haldamise** lehel **Maksuteabe** kiirkaardil valige **Lisa** või **Redigeeri** et avada **Maksuteabe haldamine** leht, kus saate maksu registreerimiskirjet hallata.
11. **Maksuteabe haldamine** lehel **Kinnipeetava maksu** kiirkaardil **Maksukonto number (TAN)** väljal, sisestage TAN. TAN peab koosnema viiest tähestikumärgist, seejärel neljast numbrimärgist ja seejärel ühest tähestikumärgist. Siin on näide: **AFGH54821T**.
12. Sulgege leht.
