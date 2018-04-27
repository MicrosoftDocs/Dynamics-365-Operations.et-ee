---
title: Transpordikoorma osaline saadetis
description: "Selles teemas selgitatakse, kuidas saate koorma lähetada osaliselt ja koorma võimsuse planeerimise edasi lükata."
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSTransportLoad
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2a1fb66ddb956b9e248ebc6ca6cf71d7b32b4705
ms.openlocfilehash: 77b713e7d55e06c89dd175dfea7e7ade9734b656
ms.contentlocale: et-ee
ms.lasthandoff: 04/09/2018

---

# <a name="partial-shipment-of-a-transport-load"></a>Transpordikoorma osaline saadetis

[!include[banner](../includes/banner.md)]

Koormate osalise saadetise loomisel saate käsitleda koormaid, kus võimsust ei saa määrata enne, kui kõik müügiread on koormale lisatud. Protsessi saab lõpule viia, kui täpne kaubaaluste arv on teada. Seega peate otsustama, millise kaubaaluseid määratakse millisele transpordile, alles siis, kui transporti laaditakse füüsiliselt etapiviisilistest varudest välja.

See funktsioon pakub alternatiivi jäigema struktuuri rakendamisele, kus peate juba enne komplekteerimis- või laadimistöö loomist otsustama, milliseid kaubaaluseid määratakse millisele transpordile. Selle asemel saavad kasutajad konfigureerida individuaalseid koormaid osalise saadetise kinnituse jaoks. Seejärel saavad toimuda nende koormate transpordi laadimise protsessid. Seetõttu saab transpordi planeerimise osakond planeerida koormaid ilma individuaalsete transportide võimsusi arvestamata.

Laadimise ajal saavad töötajad määratleda uue transpordikoorma, millele saab laadida kaubaaluse. Teise võimalusena saavad tuvastada olemasoleva transpordikoorma. Neid andmeid saab salvestada mobiilse seadme kaudu. Seetõttu saavad erinevad laotöötajad laadida varusid samast või erinevatest koormatest samale veokile. Koormaid saab seejärel lähetada täielikult või osaliselt.

> [!NOTE] 
> Varude laadimiseks koormast kindlasse transpordikoormasse ja koorma osaliseks lähetamiseks tuleb luua töö, kasutades töömallis laadimisklassi. Tavalist komplekteerimistööd tüübiga **Komplekteerimine** ei saa transpordikoormale (nt veok) laadida.

## <a name="set-up-transport-loads-for-partial-shipment"></a>Transpordikoorma seadistamine osalise saadetise jaoks

Koormate seadistamine osalise saadetise jaoks koosneb kahest järgmisest protseduurist.

### <a name="set-the-loading-strategy"></a>Laadimisstrateegia määramine

Peate lubama osalise laadimise, määrates laadimisstrateegia. Laadimisstrateegia saate määrata pärast koorma loomist.

1. Valige **Laohaldus** \> **Koormad** \> **Kõik koormad**.
2. Valige koorem ja klõpsake suvandil **Päis**.
3. Väljal **Laadimisstrateegia** valige **Osalise koorma lähetamine on lubatud**.

### <a name="create-a-menu-item-for-loading-of-transport-loads"></a>Menüükäsu loomine transpordikoormate laadimiseks

Peate looma uue menüükäsu, mis lubab laadida transpordikoormaid. Transpordikoorem võimaldab grupeerida tööridu ühest või mitmest koormast. Kõik, mis on lisatud transpordikoormale, saab seejärel lähetada mobiilse seadme skanneri abil.

1. Valige **Laohaldus** \> **Seadistus** \> **Mobiilne seade** \> **Mobiilse seadme menüü-üksused**.
2. Valige **Uus** ja tehke siis väljal **Olek** valik **Töö**.
3. Valige suvandi **Kasuta olemasolevat tööd** sätteks **Jah**.
4. Vahekaardil **Üldine** valige väljal **Juhtija:** suvand **Transpordi laadimine**.
5. Saadetise kinnituse lubamiseks mobiilse seadme skanneris valige väljal **Lubatud lähetuskinnituse tüüp** suvand **Transpordikoorem**.

## <a name="confirm-shipment-of-a-transport-load-from-the-client"></a>Kliendilt tulnud transpordikoorma saadetise kinnitamine

Selle seadistuse abil saate kinnitada transpordikoorma, mis sisaldab saadetavat täielikku või osaliselt laaditud koormat.

1. Valige **Laohaldus** \> **Koormad** \> **Transpordikoormad**.
2. Paani Tegumiriba vahekaardil **Läheta ja võta vastu** grupis **Kinnita** valige suvand **Transport**.

