---
title: "Eelarve planeerimise põhjendus dokumentide"
description: "Põhjendus dokumentide saadakse jutustav taotleda eelarve selgitada koondeelarve vajalikkust."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: c86d01fec3d8d7c210c7e73a034f4e9e384a0dcf
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-justification-documents"></a>Eelarve planeerimise põhjendus dokumentide

Põhjendus dokumentide saadakse jutustav taotleda eelarve selgitada koondeelarve vajalikkust. 

Eelarve kava malli eelarve manager Microsoft Wordis loodud ja määratud praegune eelarve planeerimise protsessi. Eelarve omanikud siis avage Mall ja on andmed täidetakse automaatselt Wordi vastavalt nende eelarve taotluse. Seejärel saate nad lisada täiendava teksti või andmete salvestamine ja oma isikupärastatud põhjendus dokumendi seotud nende eelarve plaan enne.

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>Saate seadistada Microsoft Dynamics Office Add-in Microsoft Wordi

1.  Uue Microsoft Wordi dokumendi avamiseks.
2.  Klõpsake **lisada** lint ja klõpsake **poe**.
3.  Otsi Microsoft Dynamics Office'i lisandmoodul ja klõpsake **lisa**.
4.  Parempoolsel paanil klõpsake Wordis **lisa info**.
5.  Tippige või kleepige serveri URL ja klõpsake **OK**.

##### <a name="define-the-justification-template-in-microsoft-word"></a>Määratleda põhjenduse malli Microsoft Wordis

1.  Klõpsake **projekti** in Microsoft Dynamics Office'i lisandmooduli pärast.
2.  Päises olevat teavet, kasutada selle **väljade** nuppu.
3.  Valige olemi andmete allikas BudgetPlanJustification ja klõpsake **järgmise**. **Märkus:** see ettevõte kohustatud dokumentidega põhjendus. Teiste üksuste kasutamist aga üleslaadimise tagasi Microsoft Dynamics 365 operatsioonide nurjub, kui selle olemi ei sisaldu.
4.  Lisada BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter ja DocumentNumber siltide ja väärtuste Wordi dokumendis. **Märkus:** abil saate kohandatud sildid, mitte standardsilte, kui vaja.
5.  Klõpsake **teha** lõpetamiseks päisesse.
6.  Klõpsake rea tasandil detail kava eelarvesummad, **lisa tabelis**.
7.  Uuesti, valige olemi andmete allikas BudgetPlanJustification ja klõpsake **järgmise**.
8.  Lisage väljad, EffectiveDate, ScenarioName, AccountDisplayValue ja AccountingCurrencyExpenseAmount. **Märkus:** kommentaarid on saadaval lisa jooksul üksikutele eelarveridadele kava, kui need saab lisada tabelis siin.
9.  Lisada täiendavaid juhiseid anda lõppkasutajale ja teha vajalikud vormingu või juuksuris dokumendile.
10. Dokumendi salvestamiseks oma arvutisse ja sulgege see enne jätkamist.

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>Saate seadistada eelarve planeerimise protsessi põhjenduse malli

1.  Minge Microsoft Dynamics 365 toiminguteks, **eelarve koostamise**&gt;**install**&gt;**eelarve planeerimise**&gt;**põhjendus dokumendimallid**.
2.  Klõpsake **uus** ja liikuge äsja loodud Microsoft Wordi dokumenti.
3.  Sisestage malli kuvatav nimi ja kirjeldus. Click **OK**.
4.  Mine **eelarve koostamise**&gt;**install**&gt;**eelarve****planeerimine**&gt;**eelarve planeerimise protsessi**.
5.  Valige protsess, kus põhjenduse malli võib kasutada, ja klõpsake **muuta**.
6.  Aastal ning **põhjendus dokumendimalli** välja, valige asjakohane mall ja salvestage.

##### <a name="edit-and-save-personalized-justification-documents"></a>Redigeerige ja salvestage isikupärastatud põhjendus dokumentide

1.  Dynamics 365 toiminguteks, luua uus eelarve või avada olemasoleva eelarve plaani.
2.  Aastal ning **põhjendus** vaikimisi, valige **luua uus põhjendus**.
3.  Kui andmed on täidetud, valige laadida isikustatud dokument: selle **põhjendus** vaikimisi.



