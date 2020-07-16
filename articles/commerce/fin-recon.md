---
title: Finantsvastavusseviimine kauplustes
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Commerce'i kassa finantsvastavusseviimist kauplustes.
author: anpurush
manager: AnnBe
ms.date: 06/09/2020
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
ms.openlocfilehash: 5d0520f35391f76b52fd8a333033b0d7ba4f7fe1
ms.sourcegitcommit: 1e6a7b50596eaf9d965e0155f3f2c50f7f50747e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/22/2020
ms.locfileid: "3498009"
---
# <a name="financial-reconciliation-in-retail-stores"></a>Finantsvastavusseviimine kauplustes

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce'i versioonis 10.0.10 ja varasemas, võimaldab kassa kliendi pakutav päevalõpu toimingute funktsioon teha kaupluste ja kaupluse kassapidajatel ja juhtidel teha päevalõpu toiminguid. Neil on võimalik teha näiteks päevakassasid, pimedalt suletud vahetusi, viia vahetuse kandeid vastavusse ja sulgeda vahetusi. Kuid kassas ei ole võimalust vahetuste finantsteabe lõpetamiseks, et seda saaks kasutada Commerce'i peakontoris finantside sisestamiseks. Tavaliselt vastutavad selle ülesande lõpule viimise eest kaupluse juhid. Enne, kui nad saavad vahetust välja registreerida, peavad nad teabe üle vaatama, tegema nõutavad parandused ja lõpetama selle vahetuse kogusummad. Seejärel tuleks lõpetatud kogusummad sisestada Commerce'i peakontori finantsmoodulisse.

Lisaks saavad kaupluse juhid Commerce'i versioonis 10.0.10 ja varasemas vaadata üle ja teha korrigeerimisi Commerce'i peakontori väljavõtteridadele. Kuid see võimalus on piiratud ja kaupluse juhtidel pole üldjuhul juurdepääsu Commerce'i peakontori kliendile. Lisaks saab jaemüügi finantsaruande ülevaadet ja korrigeerimist teha ainult siis, kui avaldused luuakse Commerce-i peakontoris. Kuid see toiming toimub tavaliselt öösiti. Seetõttu peavad kaupluse juhid ootama vahetuse väljaregistreerimiseni, kui jaemüügi finantsaruanded luuakse Commerce'i peakontoris.

Commerce'i versioonis 10.0.11 ja hilisemas saavad kaupluse juhid üle vaadata, korrigeerida ja lõpetada oma vahetusi otse kassa kliendis. Seejärel kasutatakse neid andmeid Commerce'i peakontoris jaemüügi finantsaruannete loomiseks ja sisestamiseks.

> [!NOTE]
> See kaupluse finantsvastavusseviimisega seotud funktsioon töötab ainult siis, kui vähehaaval toimuv tellimuse loomine on sisse lülitatud. Lisateavet leiate teemast [Vähehaaval toimuv tellimuse loomine kaupluse kannete jaoks](trickle-feed.md).

## <a name="set-up-financial-reconciliation"></a>Finantsvastavusseviimise seadistamine

Järgige neid etappe finantsvastavusseviimise funktsiooni kasutamiseks.

1. Lülitage tööruumis **Funktsioonihaldus** sisse funktsioon **Jaemüügi väljavõtted – vähehaaval toimuv**.
1. Määrake vastava kaupluse kassafunktsiooni profiilis suvandi **Luba finantsvastavusseviimine kaupluses** väärtuseks **Jah**.

## <a name="more-information-about-financial-reconciliation"></a>Lisateave finantsvastavusseviimise kohta

Kui finantsvastavusseviimise funktsioon on sisse lülitatud, sünkroonitakse osad Commerce'i peakontori lehe **Kauplused** kiirkaardil **Aruanne/sulgemine** määratletud parameetrid kanali andmebaasi. Jõustatakse samasid arvutuskriteeriumeid ja summa lävesid nagu jaemüügiaruannete puhul.

Toimingu **Sule vahetus** käivitatamisel kontrollib süsteem, et süsteemi arvutatud summad ja deklareeritud summad ühtiksid. Kui need erinevad ja erinevus ületab määratletud läve, palutakse kasutajal teha vajalikud korrigeerimised.

Korrigeerimisi saab teha iga maksevahendi puhul. Maksevahendi valimisel saab kasutaja vaadata erinevate kandetüüpide kogusummasid ja muuta kindla kandetüübi kogusummasid. Redigeerimisel kuvab süsteem selle kandetüübi algset arvutatud summat ja alistatud summat. Kasutaja saab jäädvustada märkmeid redigeerimistoimingu ajal. Märkmeid saab kasutada auditeerimise eesmärgil.

Kasutajad saavad eirata kinnituse viipasid ja teateid ning jätkata vahetuse sulgemist. Kuid kui kasutaja eirab kinnitamise viipasid, ilmnevad samad probleemid vahetuse finantsaruannete sisestamisel Commerce'i peakontoris ja need tuleb parandada.

Kassatoiming **Sule vahetus** kinnitab ka, et kõik võrguühenduseta andmebaasi kanded sünkroonitakse kanali andmebaasiga. Kui ühtegi kannet ei sünkroonita, saab kasutaja hoiatusteate, kuna selline olukord võib põhjustada süsteemi summade valesti arvutamist. Sellisel juhul saab kasutaja lõpetada toimingu **Sule vahetus** ja proovida võrguühenduseta kannete sünkroonimist kanali andmebaasi. Kasutaja saab süsteemi arvutatud summasid ka käsitsi korrigeerida, et võtta arvesse kandeid, mida ei sünkroonitud, et õige finantsarvude kogum lõpetatakse ja sisestatakse. 

Kui kasutatakse vähehaaval toimuvat aruande sisestamist, et kannete sisestamine eraldatakse finantside sisestamisest, saate valida, kas korrigeerida süsteemi arvutatud summasid puuduvatel võrguühenduseta kannetel. Sedasi tagate, et finantse arvestatakse ja sisestatakse alati õigesti, hoolimata puuduvatest kannetest. Võrguühenduseta kandeid saab sünkroonida kanali andmebaasi ja Commerce'i peakontorisse ning seejärel sisestada hiljem eraldi finantsilistesse sisestustesse.

Vahetuse finantsvastavusseviimise üksikasjad sünkroonitakse Commerce'i peakontorisse P-töö abil.

Commerce'i peakontori jaemüügi finantsaruanded ei arvuta kogusummasid väljavõtteridadel üksikasjade kuvamiseks. Kassa kliendi lõplikke summasid kasutatakse selle asemel jaemüügi finantsaruannete loomiseks ja sisestamiseks.
