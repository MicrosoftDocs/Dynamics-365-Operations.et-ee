---
title: "Projekti kulude tekkepõhisele ostutarnete"
description: "See teema kirjeldab, kuidas kogunenud kulud sissetulekuid saab jälgida rakenduses Microsoft Dynamics 365 operatsioonide ostust."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 27a0a71095dce46c0119b32a92f8c4dce0f42e43
ms.lasthandoff: 03/31/2017


---

# <a name="project-cost-accrual-on-purchase-receipts"></a>Projekti kulude tekkepõhisele ostutarnete

See teema kirjeldab, kuidas kogunenud kulud sissetulekuid saab jälgida rakenduses Microsoft Dynamics 365 operatsioonide ostust. 

Projekti arvete sageli saabuda pärast kauba ja teenuseid osutatakse, millel võib olla oluline mõju projekti tulemuslikkuse võtmenäitajate (KPI). See oluline et oleks võimalik jälgida nende tehingute finantsvaldkonda, projektide aruanded.

Järgmistel näide illustreerib seda. 

Contoso konsulteerimist on alanud uus pilve juurutamise projekti. Ostutellimus luuakse projekti arvuti osta. Arvuti maksab $1500 ja paigaldamise teenused maksab $150. Hankija on tarnitud ja paigaldatud arvuti, kuid arve ei ole veel jõudnud, Contoso konsulteerimist. Projektijuht tahaks näha projekti kulude tekkepõhisele $1650 enne, kui arve on esitatud. See kulu tuleks kajastada ka ettevõtte kuu lõpus finantsaruannetes. 

Tekkepõhine kulu peab rahalise taseme ja projektide finantsaruandluse registreerida. Dynamics 365 toiminguteks, finantsilise uuendamisega toote sissetulek saab jälgida kauba ja hangete kategooria. 

Üksuste kohta on **Ostureskontro parameetrid** avamiseks valige selle **konteerida pearaamatusse toote tarnet** võimalus.
[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png) 

Hanke kategooriate kohta ning **kategooria poliitika reegel** avamiseks valige **ostmine** poliitika ja valige seejärel **Accrue ostu kulu saamisel** hangete kaupa.
[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png) 

Selle **osta kulude un arveldatud** ja **ostu tekkepõhise** moodustab **kont** kanded, mis on seotud toote tarne konteerimisel kasutatakse.
[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png) 

Kasutades sama stsenaarium, vaatame, kuidas postitad toote sissetulek mõjutab pearaamatu ja projektiteavet. 

**1. samm:** Loo ja kinnitada projekti salvestada arvuti jaoks $150 $1500 ja paigaldusteenused ostmisel uue ostutellimuse.
[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png) 

Kui ostutellimus on kinnitatud, luuakse tehingute kooskõlastatud kulu projekti. 
[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png) 

> [!NOTE]
> Kooskõlastatud kulu kanded on selle **kande päritolu** väärtuseks **ostutellimuse**. Loomine ja kinnitades ostutellimus luua projekti kannetega. 

**2. samm:** kaupade ja teenuste toimetata ja toote sissetulek on registreeritud. 

Toote tarne konteerimise luua ja pärast kande pearaamatusse. Kanne debiteerida ostmise kulud, un arveldatud konto ja ostu viitvõla kontot. 
[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)

> [!NOTE]
> Toote tarne konteerimise kasutab sisestusseadistuse hanke kategooriate ja toodete ja mitte projekti kategooriate sisestamise seadistust. Viisil arvesse mõjuhinnangu ostu viitvõlad, peab see seadistus ühtlustada. 

Saab hanke kategooriad projektikategooriate kaart on **hanke kategooria** lehel.
[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)

**3. samm:** eelnõu hankija arve loomiseks. 

Dynamics 365 toiminguteks, postitad toote sissetulek ei mõjuta projektiteavet. Lahendusena võid luua eelnõu hankijaarve vahetult pärast postitamist ostutarne. Mine ning **ostutellimuse** leht &gt;**arve vahekaardi**&gt;**Loo**&gt;**arve**. See loob ootel arve dokumendi, mis värskendab projektiteavet. 

Loomise eelnõu hankijaarve loovad pooleli projekti kandeid. 
[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png) 

Aastal ning **kooskõlastatud kulud** leht, sammus 1 loodud kirjed suletakse ja luuakse uusi kirjeid kulu kohustuse pärit ootel hankija arve kajastamiseks. Selle **kande päritolu** välja jaoks kooskõlastatud kulu seatakse **hankija arve**.
[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)

Hankija arve jäävad ootele, kuni tegeliku hankija arve saabub.


