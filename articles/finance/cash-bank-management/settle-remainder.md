---
title: Jäägi tasakaalustus
description: Võite tasakaalustada tasakaalustamistegevusest järelejäänud summa kandes selle summa pearaamatukontole.
author: mikefalkner
manager: aolson
ms.date: 10/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 52b0b456a6d9879c480ac3f076a32e382426a89c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977787"
---
# <a name="settle-remainder"></a>Jäägi tasakaalustus

[!include [banner](../includes/banner.md)]

Võite tasakaalustada tasakaalustamistegevusest järelejäänud summa kandes selle summa pearaamatukontole või teisele kliendile. Võite ülejäägi tasakaalustada, kui tasakaalustate töölehele sisestatud summasid või kui tasakaalustate ainult avatud kandeid.

## <a name="setting-up-defaults"></a>Vaikesätete seadistamine 
Peate lubama funktsiooni Tasakaalusta jääk ja enne jäägi tasakaalustamise kasutamist seadistama vaikesötted

1)  Klõpsake **Müügireskontro > Parameetrid > Tasakaalustused** või **Ostureskontro > Parameetrid > Tasakaalustused**
2)  Valige vahekaart **Tasakaalustamine** ja klõpsake **Luba jäägi tasakaalustus**
3)  Jaotises **Põhjuse vaikekood** valige põhjuse vaikekood. Põhjusekoodid peavad olema juba seadistatud jaotises **Müügireskontro > Seadistus > Kliendi mahakandmise põhjuse koodid** või **Ostureskontro > Seadistus > Kliendi mahakandmise põhjuse koodid**. **Jäägi tasakaalustamise vaikekonto** lähtestatakse mahakandmise põhjusekoodi kontole.
3)  Värskendage **Jäägi tasakaalustamise vaikekontot** vastavalt vajadusele.
4)  Valige **Vaiketöölehe nimi**alt maksetööleht, mida kasutatakse siis, kui soovite luua maksetöölehe, kui te vaid tasakaalustate avatud kandeid. Kui lubate jäägi tasakaalustuse funktsiooni, peate lisama töölehe vaikenime.

## <a name="settle-remainder-from-a-journal"></a>Tasakaalustage jääk töölehelt
Kuil te ei luba funktsiooni **Jäägi tasakaalustamine**, võite siiski sisestada kande töölehele ja seejärel tasakaalustada see kannetega, nagu olete teinud varem. Kui klõpsate nupule **OK**, vähendatakse arve avatud saldot sularaha summa võrra. Kui sularaha arvet täielikult ei tasakaalusta, jäetakse arve avatuks ning ülejäänud summa tasakaalustatakse hiljem.

Kui funktsioon **Jäägi tasakaalustamine** on lubatud, saate tasakaalustada ülejäänud summa pearaamatukontosse. Võite arve avatuks jätmise asemel kanda jäägi ka teise kliendi kontole (kliendikanneteks) või teisele hankijale (hankijate kanneteks). 

Jäägi tasakaalustamiseks leheküljelt **Tasakaalustamine**, tehke järgmist.

1)  Märkige leheküljel **Tasakaalustamine** arved või kanded, mida soovite tasakaalustada.
2)  Klõpsake nuppu **Jäägi tasakaalustamine**.
3)  Kuvatakse dialoogiboks, mis näitab summat, mida pearaamatu vastu tasakaalustatakse, jäägei tasakaalustamisel kasutatavat kuupäeva, põhjuse vaikekoodi parameetritest ja vaikekontot parameetritest. 
4)  Kui sooviti vaikepõhjust muuta, valige uus tasakaalustuse põhjus. Tasakaalustuskonto muudetakse põhjusekoodiga seotud kontoks.
5)  Redigeerige tasakaalustuskontot, kui soovite seda muuta.
6)  Kui tasakaalustate kliendikandeid ja soovite jäägi liigutada teisele kliendile, valige klient jaotisest **Tasakaalusta jääk kliendi konto suhtes**. Kui tasakaalustate hankijakandeid ja soovite jäägi liigutada teisele hankijale, valige klient jaotisest **Tasakaalusta jääk hankija konto suhtes**.
6)  Klõpsake valikul **Jäägi tasakaalustamine**.
7)  Kuvatakse lehekülge **Tööleht**. Töölehele lisatakse lisanduv töölehe rida, kus summaks on tasakaalustamise jäägi summa ja vastaskontoks on jäägi tasakaalustamise konto. Kui lisasite kliendile või hankija, et saaksite liigutada tasakaalustussumma teisele kliendile või hankijale, siis lisatakse töölehele lisanduv rida jäägi summa liigutamiseks sellele kliendile või hankijale.

Kui töölehe sisestate, tasakaalustatakse avatud kanne täielikult. 

## <a name="settle-remainder-when-you-are-only-settling-open-transactions"></a>Tasakaalustage jääk, kui tasakaalustate ainult avatud kandeid
Saate jääki tasakaalustada ka siis, kui tasakaalustate avatud kandeid ilma tööleheta.

Jäägi tasakaalustamiseks toimige järgmiselt.

1)  Märkige leheküljel **Tasakaalustamine** arved või kanded, mida soovite tasakaalustada
2)  Klõpsake valikul **Jäägi tasakaalustamine**
3)  Kuvatakse dialoogiboks, mis näitab summat, mida pearaamatu vastu tasakaalustatakse, jäägei tasakaalustamisel kasutatavat kuupäeva, põhjuse vaikekoodi parameetritest ja vaikekontot parameetritest. 
4)  Kui sooviti vaikepõhjust muuta, valige uus tasakaalustuse põhjus. Tasakaalustuskonto muudetakse põhjusekoodiga seotud kontoks.
5)  Redigeerige **tasakaalutuskontot**, kui soovite seda muuta.
6)  Kui tasakaalustate kliendikandeid ja soovite jäägi liigutada teisele kliendile, valige klient jaotisest **Tasakaalusta jääk kliendi konto suhtes**. Kui tasakaalustate hankijakandeid ja soovite jäägi liigutada teisele hankijale, valige klient jaotisest **Tasakaalusta jääk hankija konto suhtes**
7)  Võita ka luua tasakaalustamise jäägiga maksetöölehe või lihtsalt sisestada selle ilma tööleheta. Valige **Yes** **Redigeeri töölehel** jaoks, et luua maksetööleht. Saate redigeerida oma loodud maksetöölehte.
8)  Klõpsake valikul **Jäägi tasakaalustamine**. Kui valisite töölehe loomise, muutub nupp nupuks **Töölehe loomine**. Klõpsake selle asemel nuppu **Töölehe loomine**.
9)  Kui kõite maksetöölehe, avaneb töölehe lehekülg pärast seda, kui klõpsate nupul **Jäägi tasakaalustus**. Töölehele lisatakse töölehe rida, kus summaks on tasakaalustamise jäägi summa ja vastaskontoks on jäägi tasakaalustamise konto. Kui lisasite kliendile või hankija, et saaksite liigutada tasakaalustussumma teisele kliendile või hankijale, siis lisatakse töölehele lisanduv rida jäägi summa liigutamiseks sellele kliendile või hankijale.
