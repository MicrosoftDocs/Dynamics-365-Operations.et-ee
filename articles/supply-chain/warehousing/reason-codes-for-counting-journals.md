---
title: Varude inventuuri põhjusekoodid
description: Selles teemas kirjeldatakse põhjusekoodide seadistamist ja rakendamist inventuuriülesannete jaoks.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCountingReasonCodePolicy, InventCountingReasonCode
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 66e1fb9f32aa31221f85180339b8b6ee55836be1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996144"
---
# <a name="reason-codes-for-inventory-counting"></a>Varude inventuuri põhjusekoodid

[!include [banner](../includes/banner.md)]

Põhjusekoodide abil saate analüüsida inventuuriprotsessi tulemusi ja protsessi käigus tekkivaid võimalikke lahknevusi. Saate määrata inventuuri tegemise põhjuse, nagu katkine kaubaalus või varude korrigeerimine, mis põhineb varude näidistel.

## <a name="recommendation"></a>Soovitamine

Enne süsteemi häälestamist on soovitatav määratleda põhjusekoodidega töötamise strateegia. Proovige näiteks vastata järgmistele küsimustele.

- Kas põhjusekoodid peaksid ladudes olema kohustuslikud?
- Kas põhjusekoodid peaksid mõningate kaupade jaoks olema kohustuslikud või valikulised?
- Mitu põhjusekoodi te vajate?
- Kuidas peaksid vöötkoodilugejate kasutajad põhjusekoode kasutama? Kas põhjusekoodid peaksid olema eelvalitud, kohustuslikud või mitteredigeeritavad?
- Kas laotöötajad vajavad mobiilse seadme skannerites erinevat põhjusekoodi käitumist? Kui vastus on jah, saate luua rohkem menüükäske ja määrata need erinevatele inimestele.

## <a name="where-reason-codes-apply"></a>Kus põhjusekoode rakendatakse

Saate luua mitu põhjusekoodi poliitikat ja igal põhjusekoodi poliitikal saab olla kaks inventuuri põhjusekoodi poliitikat. Inventuuri põhjusekoodi poliitikaid saab kasutada lao või kauba tasemel.

## <a name="set-up-reason-code-policies"></a>Põhjusekoodi poliitikate seadistamine

1. Valige **Varude haldus** \> **Seadistus** \> **Varud** \> **Inventuuri põhjusekoodi poliitikad** ja looge uus põhjusekoodi poliitika.
2. Väljal **Inventuuri põhjusekoodi tüüp** valige kas **Kohustuslik** või **Valikuline**, et määrata, kas põhjusekoodi valimine peaks ühel järgmistest inventuuritöölehtedest olema valikuline või kohustuslik tegevus.

    - Tsükliline inventuur (mobiilne seade)
    - Punktinventuur (mobiilne seade)
    - Läveinventuur (mobiilne seade)
    - Saabumise korrigeerimine (mobiilne seade)
    - Väljastuse korrigeerimine (mobiilne seade)
    - Inventuuritööleht (rikas klient)

Põhjusekoode saate ka seadistada üksikute ladude ja toodete jaoks. Toodete põhjusekoodi seadistus saab eirata ladude seadistust.

## <a name="mandatory-reason-codes"></a>Kohustuslikud põhjusekoodid

Kui ladude või kaupade põhjusekoodide konfiguratsioonis on määratud parameeter **Kohustuslik**, ei saa inventuuritöölehte enne põhjusekoodi sisestamist lõpule viia ega sulgeda.

### <a name="set-up-reason-codes-for-warehouses"></a>Ladude põhjusekoodide häälestamine

1. Valige **Varude haldus** \> **Seadistus** \> **Laovarude jaotamine** \> **Laod**.
2. Vahekaardil **Ladu** väljal **Inventuuri põhjusekoodi poliitika** valige üks järgmistest suvanditest.

    - **Tühi** – kauba jaoks seadistatud parameetrit kasutatakse määratlemiseks, kas inventuuritöölehed on toote jaoks kohustuslikud.
    - **Kohustuslik** – põhjusekood on lao inventuuritöölehtedel alati nõutav.
    - **Valikuline** – põhjusekood pole lao inventuuritöölehtedel nõutav.

### <a name="set-up-reason-codes-for-products"></a>Toodete põhjusekoodide häälestamine

1. Valige **Tooteteabe haldus** \> **Tooted** \> **Väljastatud tooted**.
2. Vahekaardil **Toode** valige **Inventuuri põhjusekoodi poliitika** ja seejärel valige üks järgmistest suvanditest.

    - **Tühi** – lao jaoks seadistatud parameetrit kasutatakse määratlemiseks, kas inventuuritöölehed on toote jaoks kohustuslikud.
    - **Kohustuslik** – põhjusekood on toote inventuuritöölehtedel alati nõutav. See säte alistab laotaseme põhjusekoodi sätted.
    - **Valikuline** – põhjusekood pole toote inventuuritöölehtedel nõutav. See säte alistab laotaseme põhjusekoodi sätted.

### <a name="use-reason-codes-in-counting-journals"></a>Põhjusekoodide kasutamine inventuuritöölehtedel

Inventuuritöölehel saate lisada põhjusekoode järgmist tüüpi inventuuride jaoks:

- Tsükliline inventuur
- Punktinventuur
- Läveinventuur
- Saabumise korrigeerimine
- Väljastuse korrigeerimine

Põhjusekoodid lisatakse töölehe ridadele inventuuritöölehtedel tüübiga **Inventuuritööleht**.

1. Valige **Varude haldus** \> **Töölehe sisestused** \> **Kauba inventuur** \> **Inventuur**.
2. Inventuuritöölehe rea üksikasjades väljal **Inventuuri põhjusekood** valige suvand.

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a>Inventuurižurnaali kuvamine selle salvestamisel põhjusekoodide järgi

- Valige **Varude haldus** \> **Päringud ja aruanded** \> **Inventuurižurnaal** ja seejärel väljal **Inventuuri põhjusekood** vaadake inventuurižurnaali, mis on salvestatud põhjusekoodi kaudu.

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a>Põhjusekoodi kasutamine koguse korrigeerimiseks

1. Lehel **Vaba kaubavaru** valige **Koguse korrigeerimine**. Saate lehe **Vaba kaubavaru** avada mitmel viisil. Näiteks valige **Varude haldus** \> **Päringud ja aruanded** \> **Vaba kaubavaru**.
2. Valige **Koguse korrigeerimine** ja seejärel väljal **Inventuuri põhjusekood** valige põhjusekood.

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a>Põhjusekoodide konfigureerimine mobiilse seadme menüükäskude jaoks

Saate konfigureerida põhjusekoode iga inventuuritüübi jaoks mobiilse seadme menüükäsus. Mobiilse seadme menüükäsu konfiguratsioon sisaldab järgmist teavet.

- Kas põhjusekood kuvatakse inventuuri ajal mobiilse seadme töötajale.
- Vaikepõhjusekood, mis kuvatakse mobiilse seadme menüükäsus
- Kas kasutaja saab põhjusekoodi redigeerida.

### <a name="set-up-reason-codes-on-a-mobile-device"></a>Põhjusekoodide seadistamine mobiilses seadmes

1. Valige **Laohaldus** \> **Seadistus** \> **Mobiilne seade** \> **Mobiilse seadme menüü-üksused**.
2. Vahekaardil **Tsükliline inventuur** valige **Tsükliline inventuur**.
3. Väljal **Inventuuri vaikepõhjusekood** määrake vaikepõhjusekood, mis tuleks salvestada, kui inventuuri tehakse mobiilse seadme menüükäsu abil.
4. Väljal **Kuva inventuuri põhjusekood** valige **Rida**, et kuvada põhjusekood pärast iga hälbe salvestamist. Teise võimalusena valige **Peida**, kui põhjusekoodi ei tohiks kuvada.
5. Määrake suvandi **Redigeeri inventuuri põhjusekoodi** väärtuseks kas **Jah** või **Ei**. Kui määrate selle suvandi väärtuseks **Jah**, saab töötaja redigeerida põhjusekoodi, kui see kuvatakse inventuuri ajal mobiilses seadmes.

> [!NOTE]
> Nupu **Tsükliline inventuur** saab lubada igas mobiilse seadme menüükäsus, kus saab teha inventuuri. Näidete hulka kuuluvad menüükäsud punktinventuuride jaoks, kasutaja suunatud töö ja süsteemi suunatud töö.

## <a name="cycle-count-approvals"></a>Tsüklilise inventuuri kinnitused

Enne inventuuri kinnitamist saab kasutaja muuta selle inventuuriga seotud põhjusekoodi. Inventuuri kinnitamisel sisestatakse põhjusekood inventuuritöölehe ridadele.

### <a name="modify-cycle-count-approvals"></a>Tsüklilise inventuuri kinnituste muutmine

1. Valige **Laohaldus** \> **Tsükliline inventuur** \> **Ülevaatuse ootel tsüklilise inventuuri töö**.
2. Valige **Ülevaatuse ootel tsüklilise inventuuri töö** ja seejärel väljal **Põhjusekood** valige uus põhjusekood.

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a>Mobiilse seadme menüükäsu muutmine saabumise korrigeerimise ja väljastuse korrigeerimise jaoks

1. Valige **Laohaldus** \> **Seadistus** \> **Mobiilne seade** \> **Mobiilse seadme menüükäsud** ja seejärel valige **Saabumise ja väljastuse korrigeerimine**.
2. Valige suvandi **Kasuta olemasolevat tööd** sätteks **Ei**.
3. Väljal **Töö loomise protsess** valige **Saabumise korrigeerimine**.

Järgmised väljad lisatakse mobiilse seadme menüükäsule, kui töö loomise protsessi käigus on valitud **Saabumise korrigeerimine** või **Väljastuse korrigeerimine**:

- Inventuuri vaikepõhjusekood
- Kuva inventuuri põhjusekood
- Redigeeri inventuuri põhjusekoodi


[!INCLUDE[footer-include](../../includes/footer-banner.md)]