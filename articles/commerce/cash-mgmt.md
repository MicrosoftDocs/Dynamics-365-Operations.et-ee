---
title: Sularahahalduse parandused
description: Selles teemas kirjeldatakse sularahahalduse parandusi kassas rakenduses Dynamics 365 Commerce.
author: anpurush
manager: AnnBe
ms.date: 05/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0c561c39dfcbfa739c5a22394c05191e7f9bc107
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411639"
---
# <a name="cash-management-improvements"></a>Sularahahalduse parandused

[!include [banner](includes/banner.md)]


Sularahahaldus on füüsiliste poodide jaemüüjate põhifunktsioone. Jaemüüjad tahavad, et nende poodidel oleksid süsteemid, mis aitavad neil tagada täieliku jälgitavuse ja aruandekohustuse sularaha ning selle liikumise poe kõikides kassades ja kassapidajate juures. Nad peavad suutma vastavusse viia kõik erinevused ja määrama aruandekohustuse.


Rakendusel Microsoft Dynamics 365 Commerce on kassa (POS) rakenduses sularahahalduse võimalused. Kuid Retaili varasemates versioonides kui 10.0.3 ei ole sularahahalduse funktsioon piisavalt töökindel, et tagada sularaha liikumise täielikku jälgitavust poodides. Kuigi jaemüüjad saavad sularaha poes vastavusse viia, ei saa nad sularaha lahknevuse korral täpselt määrata aruandekohustust.


Retaili 10.0.3 või uuemas versioonis saavad jaemüüjad jälgida sularaha käsitsemist. Osana sellest jälgitavusest saavad jaemüüjad määrata seife, teha kahepoolseid sularahakandeid ja viia vastavusse sularahahalduse kandeid.

## <a name="set-up-traceability-and-define-safes"></a>Jälgitavuse seadistamine ja seifide määramine

Uue sularahahalduse funktsiooni seadistamiseks järgige poodidele funktsiooniprofiili konfigureerimiseks järgmisi etappe.

1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassa profiilid \> Funktsiooniprofiilid** ja valige funktsiooniprofiil, mis on seotud kauplustega, kus soovite saadaolevat sularahahaldust parandada.
2. Funktsiooniprofiili kiirkaardil **Funktsioonid** jaotises **Täpsem sularahahaldus** seadke suvand **Luba sularaha jälgitavus** valikule **Jah**.
3. Seifide seadistamiseks avage **Jaemüük ja kaubandus \> Kanalid \> Kauplused \> Kõik kauplused** ja valige kauplus.
4. Valige lehe **Kauplused** tegumiriba vahekaardi **Seadistamine** grupist **Seadistamine** valik **Seifid**. Seda suvandit kasutades saate kaupluse jaoks määrata ja hallata mitut seifi.
4. Enne kui saate funktsiooni kasutada, peate käivitama jaotusgraafiku töö **1070 kanali konfigureerimine**, et sünkroonida need konfiguratsioonid kanali andmebaasiga.

## <a name="additional-cash-management-changes"></a>Sularahahalduse täiendavad muudatused

Retaili versioonis 10.0.3 ja uuemates versioonides on saadaval ka järgmised sularahakannetega seotud võimalused.

- Kasutaja, kellel palutakse deklareerida algsumma, peab sisestama sularaha allika. Kasutaja saab otsida kaupluses määratud saadaolevaid seife ja valida seifi, kust sularaha välja võetakse, et seda kassasse panna.
- Kasutajal, kes teeb väljamakse, palutakse vahetusraha kirje kannete loendist valida kanne, mille suhtes tehing tehakse. Kui vastavat vahetusraha kirjet süsteemis pole, saab kasutaja luua mitteseotud väljamakse kande.
- Vahetusraha kirje toiming palub kasutajal valida avatud väljamakse kannete loendist kande, mille suhtes vahetusraha kirje tehing tehakse. Kui vastavat väljamakset süsteemis pole, saab kasutaja luua mitteseotud vahetusraha kirje kande.
- Kasutajal, kes raha seifi viib, palutakse valida seif, kuhu sularaha viiakse.
- Kaupluses määratud seifide korral saavad kasutajad hallata toiminguid, nagu algsumma deklareerimine, vahetusraha kirje, väljamakse ja raha hoiustamine panka.
- Sobivate kasutaja privileegidega kasutajatele näitavad vahetuste haldamise toimingud aktiivsete, peatatud ja pimesi suletud vahetuste sularahasaldosid.
- Sularahakannete vastavusse viimiseks vahetuse sees või vahetusteüleselt valige vastavusse viidav vahetus ja seejärel suvand **Vii vastavusse**. Avanevas vaates kuvatakse vastavusse viidud ja viimata kannete loend eraldi vahekaartidel. Selles vaates saavad kasutajad valida vastavusse viimata kanded ja need vastavusse viia või valida varem vastavusse viidud kanded ja need vastavusest välja viia.
- Kui vastavusse viimise ajal valitud kanne tasakaalu ei lähe, peab kasutaja sisestama tasakaalustamata vastavusse viimise põhjuse kirjelduse. Kasutajad saavad valida ühe kande ja viia selle vajaduse järgi vastavusse vastava põhjuse kirjeldusega.
- Kasutajad saavad jätkata kannete vastavusse ja vastavusest välja viimist, kuni vahetus suletakse. Kui vahetus on suletud, ei saa kandeid vastavusest välja viia.
- Kui kasutaja otsustab vahetuse sulgeda, kontrollib Commerce, et vahetuses poleks vastavusse viimata sularahahalduse kandeid. Kasutajad ei saa vahetust sulgeda, kui selles on vastavusse viimata kandeid.


[!INCLUDE[footer-include](../includes/footer-banner.md)]