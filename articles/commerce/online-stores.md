---
title: Võrgupoe kanali häälestamine
description: See artikkel annab teavet kaupluste veebipoodide kanalite kohta ja kuidas neid rakenduses Dynamics 365 Commerce seadistada.
author: kfend
manager: AnnBe
ms.date: 03/02/2019
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
ms.openlocfilehash: b719e40720b091eec879edf332ab63db710a1ebc
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096890"
---
# <a name="set-up-an-online-store-channel"></a>Võrgupoe kanali häälestamine

[!include [banner](includes/banner.md)]

See artikkel annab teavet kaupluste veebipoodide kanalite kohta ja kuidas neid rakenduses Dynamics 365 Commerce seadistada.

Commerce toetab mitut jaemüügikanalit. Need kanalid hõlmavad võrgupoode, kõnekeskusi ja jaekauplusi (neid nimetatakse ka füüsilisteks kauplusteks). Võrgupoed annavad jaemüüjale kohaloleku võrgus, nii et tema kliendid saavad lisaks jaekauplusest osta tooteid ka võrgupoest. Kui kliendid ostavad tooteid võrgupoest, saab need tooted neile tarnida või võivad nad tooted kätte saada kohalikust kauplusest. 

Võrgupoe saate luua Commerce’i kliendis. Seejärel avaldatakse võrgupood kolmanda poole võrgupoele, mis on integreeritud Commerce’iga. Muu osapoole võrgupood toimib võrgupoe fassaadina (kasutajaliidesena) ning võimaldab teil valida kliendihaldussüsteemi (CMS) ja kasutajaliidese võimalusi. Mitu seda tüüpi integratsiooni on saadaval. 

Atribuudid, mida saate võrgupoe jaoks määratleda, juhivad võrgupoe toimimist. Näiteks määratlete navigeerimiskategooria hierarhia ja määrate selle võrgupoele. Võrgupoe avaldamisel muu osapoole võrgupoele kuvatakse navigeerimiskategooria hierarhia kaupluse võrguversioonis. Ostjad kasutavad navigeerimiskategooria hierarhiat võrgupoe sisu sirvimiseks ja toodete otsimiseks. 

Võrgupoe loomiseks peate seadistama komponendid, mis võimaldavad kaupluse jaoks kannete töötlemist. Näiteks tuleb lisada sortimentid, rakendada atribuudid ning seadistada makseviisid ja tarneviisid. Samuti saate määrata hindu, kampaaniaid, allahindlusi, kaubandusleppeid ja võrgupoes kehtivaid tarnetingimusi. 

Pärast võrgupoe avaldamist muu poole võrgupoele saate võrgupoe jaoks luua tootekatalooge. Kataloogi toodetest saavad võrgupoe tooteloendid. Kui klient ostab võrgupoest tooteid, värskendatakse ja sünkroonitakse saadaolevad varud klientrakenduses. Samuti luuakse ostude kohta müügitellimused ning saadetakse tellimuse täitmiseks ja töötlemiseks klientrakendusse.

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

## <a name="commerce-channel-navigation-hierarchies"></a>Commerce’i navigeerimishierarhiad

Enne võrgupoe loomist peate määrama kaubanduskanali navigeerimishierarhia, mida soovite kasutada. Kanali navigeerimishierarhia tähistab kategooriahierarhiat, mis kuvatakse võrgupoes pärast poe avaldamist. Võrgupoe tootekataloogide avaldamisel vastendatakse kataloogis olevad tooted kanali navigeerimishierarhia kategooriatega. Seejärel kasutavad ostjad hierarhiat võrgupoes navigeerimiseks.

## <a name="organization-hierarchies"></a>Organisatsiooni hierarhiad

Organisatsiooni hierarhiaid kasutatakse kaubanduskanalite struktureerimiseks ja seoste tähistamiseks ettevõtet moodustavate organisatsioonide vahel. Võrgupoodide seadistamisel saate neid organisatsiooni hierarhiasse lisada. Poed jagavad seejärel sortimentide, täiendamise ja aruandluse jaoks kasutatavaid andmeid. 

Organisatsiooni hierarhia loomisel peate määrama sellele eesmärgi. Eesmärk näitab, kuidas hierarhiat ettevõtte struktuuris kasutatakse. Saate poe toimingute jaoks luua ühe organisatsiooni hierarhia ja kasutada seda sortimentide, täiendamise ja aruannete jaoks. 

Teise võimalusena saate iga eesmärgi jaoks luua eraldi organisatsiooni hierarhia. Samuti saate luua mitu sama eesmärgiga hierarhiat ja määrata igale neist eraldi kanali. Kui kavatsete avaldada võrgupoes tootekataloogid, peaksite võrgupoe lisama vähemalt sortimendi organisatsioonihierarhiasse. Kataloogis olevad tooted on valitud võrgupoele määratud sortimentidest. Kataloogi avaldamisel võrdleb avaldamisprotsess võrgupoele määratud sortimendi ja kataloogi kaasatud toodete kehtivuskuupäevi, et kindlaks teha, milliseid tooteid võrgupoes kättesaadavaks muuta.

## <a name="additional-resources"></a>Lisaressursid

[Domeeninime konfigureerimine](configure-your-domain-name.md)

[Uue e-kaubanduse saidi juurutamine](deploy-ecommerce-site.md)

[E-kaubanduse saidi loomine](create-ecommerce-site.md)

[Veebisaidi seostamine kanaliga](associate-site-online-store.md)

[robots.txt-failide haldamine](manage-robots-txt-files.md)

[URL-i hulgiümbersuunamiste üleslaadimine](upload-bulk-redirects.md)

[B2C rentniku seadistus Kaubanduses](set-up-B2C-tenant.md)

[Kasutaja sisselogimiseks kohandatud lehtede seadistamine](custom-pages-user-logins.md)

[Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas](configure-multi-B2C-tenants.md)

[Sisuedastusvõrgu (CDN) toe lisamine](add-cdn-support.md)

[Asukohapõhise poetuvastuse lubamine](enable-store-detection.md)
