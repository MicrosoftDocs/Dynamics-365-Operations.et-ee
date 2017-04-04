---
title: Avansisaaja kanded
description: "Juhised töötamiseks avansisaaja kanded Microsoft Dynamics 365 toiminguteks."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmWorkerAdvHolderTableListPage_RU
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 262554
ms.assetid: 84ff97bb-ae21-4d6d-8160-9325f64134ce
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: afa59439e06aad9d669eb352a9837a013f447249
ms.openlocfilehash: c819fbbb4a68dd5b8b192416fedb34827bbf3823
ms.lasthandoff: 03/31/2017


---

# <a name="advance-holder-transactions"></a>Avansisaaja kanded

Juhised töötamiseks avansisaaja kanded Microsoft Dynamics 365 toiminguteks.

Tehinguid nimetatud töötajatele, kes on eelnevalt omanike konteerimist eelnevalt omaniku kontot kasutades. Töötaja ID, mis määratakse iga Avansisaajate saab jälgida kõiki avansisaaja kanded. See number tuuakse kui avansisaaja kanded on kasutatav kontonumber on **Peažurnaalide** ja **ette avansisaaja kanded** lehti.

## <a name="create-and-post-a-purchase-order-with-advance-holder-details"></a>Luua ja sisestada ostutellimuse omaniku kohtumise üksikasjad
Üldine ostutellimuste kohta lisateavet [osta tellimuse ülevaade](/manufacturing/procurement/purchase-order-overview). Kui hankija arve loodud ja sisestatud kohtumise üksikasjad omanik, konteeritakse ettemaksu omaniku nõuded töötaja bilansikontoga hankija saldo konto asemel. Omaniku kohtumise üksikasjad ostutellimuse lisamiseks toimige järgmiselt.

-   Aastal ning **tegemise tingimused** välja ning **hind ja allahindlus**, maksetingimust märkige jaotises. <!---For more information about **Terms of payment**, see [Define vendor payment terms](http://ax.help.dynamics.com/en/wiki/define-vendor-payment-terms/).-->Valige maksetähtaeg, mis on selle **avansisaajalt** valitud suvand on **tegemise tingimused** lehekülg. Avansisaajate maksetingimused häälestamise kohta lisateabe saamiseks vt [omanikele ette](emea-advance-holders.md).
-   Linnas on **Avansisaajate** välja jäetud ning **hinna ja allahindluse** FastTab, valige ostutellimuse Avansisaajate.

Ostutellimuse sisestamisel loob kaks hankijakannete vastupidine summad ja eelnevalt omanik vastab ühele. Ilma omaniku kohtumise üksikasjad, luuakse ainult üks tarnija.

## <a name="settle-advance-holder-balances-via-a-bank"></a>Tasuda eelneva omaniku nõuded panga vahendusel
Kui teil tasakaalustada eelnevalt omaniku nõuded panga vahendusel, luuakse päevikukannete eelnevalt omanik saldode sulgemiseks peažurnaali. Saate seadistada töölehtede ja panga kood on **ette alused** jaotises selle **Ostureskontro parameetrid** lehel. Lisateabe saamiseks vaadake [omanikele ette](emea-advance-holders.md). Panga vahendusel on Avansisaaja saldo sulgemiseks Avage **arved**&gt;**ette alused**&gt;**omanikele ette**. Klõpsake selle **tasakaalu** Updatehagi paani ja seejärel valikut **Sule panga kaudu**. Järgmine teave on **Sule panga kaudu** lehel.

| Väli                    | Kirjeldus |
|------------------------------|-------------------|
| **Date of payment**          | Saate sisestada kuupäeva, mil makse tuleb konteerida.|
| **Saadetav summa** | Sisestage saldo summa samal ajal sulgemist. Summa, mis on märgitud selle **summa** välja ning **tasakaalu** Vaikimisi kuvatakse vorm. |
| **Automatic**                | Valige selle **automaatne** ruut Loo ja töölehe sisestamine seadistatud kohta ning **Ostureskontro parameetrid** lehel.|

## <a name="settle-advance-holder-balances-via-cash"></a>Tasuda eelneva omaniku nõuded Kassa kaudu
Kui eelnev omanik saldod Kassa kaudu lahendada, luuakse päevikukannete eelnevalt omanik saldode sulgemiseks saatelehe tööleht. Saate seadistada töölehtede ja raha kood on **ette alused** tabeldusklahviga ning **Ostureskontro parameetrid** lehel. Lisateabe saamiseks vaadake [omanikele ette](emea-advance-holders.md). Kassa kaudu on Avansisaaja saldo sulgemiseks Avage **arved**&gt;**ette alused**&gt;**omanikele ette**. Klõpsake selle **tasakaalu** Updatehagi paani ja seejärel valikut **Sule Kassa kaudu**. Järgmine teave on **Sule Kassa kaudu** lehel.

| Väli                    | Kirjeldus
|------------------------------|-----------------|
| **Date of payment**          | Saate sisestada kuupäeva, mil makse tuleb konteerida.|
| **Saadetav summa** | Sisestage saldo summa samal ajal sulgemist. Summa, mis on märgitud selle **summa** välja ning **tasakaalu** Vaikimisi kuvatakse vorm. |
| **Automatic**                | Valige selle **automaatne** ruut saate luua ja sisestada automaatselt žurnaali mis on tehases seadistatud kohta on **Ostureskontro parameetrid** lehel.     |

Pärast slip töölehe töödeldakse, kui summa on **summa kantakse** välja oli negatiivne, on väljaminekuorder on loodud eelnevalt omaniku suletud saldode puhul. Kui summa on **summa kantakse** välja oli positiivne, tagasi libisemine on loodud.


