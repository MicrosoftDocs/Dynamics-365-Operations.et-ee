---
title: Võrgupoe kanali seadistamine
description: See artikkel annab teavet kaupluste veebipoodide kanalite kohta ja kuidas neid rakenduses Dynamics 365 Retail seadistada.
author: kfend
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelManagementWorkspace, RetailOnlineStoreList
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16161
ms.assetid: 646d560c-f856-4701-b4ca-44e357ef09b8
ms.search.region: Global
ms.search.industry: Retail
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e7932879aac6ea4054f6c35de99f11c2662dd472
ms.sourcegitcommit: 595a4ec63a32bd5d4321126bda7cf72a75a930a2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/30/2019
ms.locfileid: "2688805"
---
# <a name="set-up-an-online-store-channel"></a>Võrgupoe kanali seadistamine

[!include [banner](includes/banner.md)]

See artikkel annab teavet kaupluste veebipoodide kanalite kohta ja kuidas neid rakenduses Dynamics 365 Retail seadistada.

Retail toetab mitut jaemüügikanalit. Jaemüügikanalid hõlmavad võrgupoode, kõnekeskusi ja jaekauplusi (neid nimetatakse ka füüsilisteks kauplusteks). Võrgupoed annavad jaemüüjale kohaloleku võrgus, nii et tema kliendid saavad lisaks jaekauplusest osta tooteid ka võrgupoest. Kui kliendid ostavad tooteid võrgupoest, saab need tooted neile tarnida või võivad nad tooted kätte saada kohalikust jaekauplusest. Võrgupoe saate luua Retaili kliendis. Seejärel avaldatakse võrgupood muu osapoole võrgupoele, mis on integreeritud Retailiga. Muu osapoole võrgupood toimib võrgupoe fassaadina (kasutajaliidesena) ning võimaldab teil valida kliendihaldussüsteemi (CMS) ja kasutajaliidese võimalusi. Mitu seda tüüpi integratsiooni on saadaval. Atribuudid, mida saate võrgupoe jaoks määratleda, juhivad võrgupoe toimimist. Näiteks määratlete navigeerimiskategooria hierarhia Retailis ja määrate selle võrgupoele. Võrgupoe avaldamisel muu osapoole võrgupoele kuvatakse navigeerimiskategooria hierarhia kaupluse võrguversioonis. Ostjad kasutavad navigeerimiskategooria hierarhiat võrgupoe sisu sirvimiseks ja toodete otsimiseks. Võrgupoe loomiseks peate seadistama komponendid, mis võimaldavad kaupluse jaoks kannete töötlemist. Näiteks tuleb lisada sortimentid, rakendada atribuudid ning seadistada makseviisid ja tarneviisid. Samuti saate määrata hindu, kampaaniaid, allahindlusi, kaubandusleppeid ja võrgupoes kehtivaid tarnetingimusi. Pärast võrgupoe avaldamist muu osapoole võrgupoele saate võrgupoe jaoks luua jaemüügi tootekatalooge. Kataloogi toodetest saavad võrgupoe tooteloendid. Kui klient ostab võrgupoest tooteid, värskendatakse ja sünkroonitakse saadaolevad varud klientrakenduses. Samuti luuakse ostude kohta müügitellimused ning saadetakse tellimuse täitmiseks ja töötlemiseks klientrakendusse.

## <a name="set-up-an-online-store"></a>Võrgupoe seadistamine

Võrgupoe seadistamiseks täitke järgmised ülesanded.

1. Looge võrgupood.
2. Lisage võrgupood sobivatesse organisatsiooni hierarhiatesse.
3. Lisage sortimendid, mis sisaldavad võrgupoes saadavaid tooteid.
4. Määrake või looge võrgupoe jaoks hinnagrupid.
5. Seadistage tarneviisid, mis on võrgupoe jaoks saadaval.
6. Määrake võrgupoes kehtivad makseviisid.
7. Kui võimaldate toodete tellimist veebis ja kauba kättesaamist kohalikust kauplusest, määrake võrgupoele kaupluselokaatori grupid.
8. Määrake võrgupoele kanalite, toodete ja müügitellimuste atribuudid. Kanali atribuudid kehtivad kogu võrgupoele, toote atribuudid kehtivad võrgupoes pakutavatele toodetele ja müügitellimuse atribuudid kehtivad võrgupoes loodud müügitellimustele.
9. Vastendage atribuudid, et määratleda omadused, mis määravad, kuidas need atribuudid võrgupoes toimivad. Näiteks saab atribuudid määratleda kas nõutavaks või otsitavaks.
10. Avaldage võrgupood, et luua poe struktuur oma valitud muu osapoole võrgupoes.

    > [!IMPORTANT]
    > Tähtis! Enne võrgupoe avaldamist peate seadistama selle jaotusasukoha.

## <a name="retail-channel-navigation-hierarchies"></a>Jaemüügikanali navigeerimishierarhiad

Enne võrgupoe loomist peate määrama jaemüügikanali navigeerimishierarhia, mida soovite kasutada. Jaemüügikanali navigeerimishierarhia tähistab kategooriahierarhiat, mida kuvatakse võrgupoes pärast poe avaldamist. Jaemüügi tootekataloogide avaldamisel võrgupoes vastendatakse kataloogis olevad tooted jaemüügikanali navigeerimishierarhia kategooriatega. Seejärel kasutavad ostjad hierarhiat võrgupoes navigeerimiseks.

## <a name="organization-hierarchies"></a>Organisatsiooni hierarhiad

Organisatsioonihierarhiaid kasutatakse jaemüügikanalite struktureerimiseks. Organisatsiooni hierarhia kajastab ettevõttesse kuuluvate organisatsioonide vahelisi seoseid. Võrgupoodide seadistamisel saate neid organisatsiooni hierarhiasse lisada. Poed jagavad seejärel sortimentide, täiendamise ja aruandluse jaoks kasutatavaid andmeid. Organisatsiooni hierarhia loomisel peate määrama sellele eesmärgi. Eesmärk näitab, kuidas hierarhiat ettevõtte struktuuris kasutatakse. Saate poe toimingute jaoks luua ühe organisatsiooni hierarhia ja kasutada seda sortimentide, täiendamise ja aruannete jaoks. Teise võimalusena saate iga eesmärgi jaoks luua eraldi organisatsiooni hierarhia. Samuti saate luua mitu sama eesmärgiga hierarhiat ja määrata igale neist eraldi kanali. Kui kavatsete avaldada võrgupoes jaemüügi tootekataloogid, peaksite võrgupoe lisama vähemalt sortimendi organisatsioonihierarhiasse. Kataloogis olevad tooted on valitud võrgupoele määratud sortimentidest. Kataloogi avaldamisel võrdleb avaldamisprotsess võrgupoele määratud sortimendi ja kataloogi kaasatud toodete kehtivuskuupäevi, et kindlaks teha, milliseid tooteid võrgupoes kättesaadavaks muuta.
