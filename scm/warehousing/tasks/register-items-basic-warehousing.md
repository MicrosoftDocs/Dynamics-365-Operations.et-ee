--- 
title: "Kaupade registreerimine üldiseks ladustamiseks lubatud kauba puhul saabuva kauba töölehe abil"
description: "Selle protseduuriga selgitatakse kaupade registreerimist, kasutades kauba saabumise töölehte mooduli Laohaldus üldise ladustamise kasutamisel."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 1c367ebcd57fc2dd534587aa96349e48756c1bb6
ms.contentlocale: et-ee
ms.lasthandoff: 07/28/2017

---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-arrival-journal"></a>Kaupade registreerimine üldiseks ladustamiseks lubatud kauba puhul saabuva kauba töölehe abil

[!include[task guide banner](../../includes/task-guide-banner.md)]

Selle protseduuriga selgitatakse kaupade registreerimist, kasutades kauba saabumise töölehte mooduli Laohaldus üldise ladustamise kasutamisel. Seda teeb üldjuhul vastuvõtuametnik. Saate käitada selle protseduuri demoandmete ettevõttes USMF näidatud näidisväärtusega.  Kui te USMF-i ei kasuta, peate enne selle juhendi käivitamist olema kinnitanud avatud ostutellimuse reaga ostutellimuse. Rea kaup peab olema ladustatav ja see ei tohi kasutada tootevariante ja sellel ei tohi olla jälgimisdimensioone. Samuti peavad kaubad olema seostatud laoala dimensioonigrupiga, kus sait ja ladu on aktiivsed.


## <a name="create-item-arrival-journal-header"></a>Kauba saabumise töölehe päise loomine
1. Avage Varude haldus > Töölehe sisestused > Kauba saabumine > Kauba saabumine.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Nimi.
    * Kui kasutate USMF-i, saate sisestada WHS-i. Kui kasutate muid andmeid, peavad töölehel, mille nime valite, olema järgmised atribuudid: Kontrolli komplekteerimiskohta peab olema seatud valikule Ei ja Vahelao haldus peab olema seatud valikule Ei.  
4. Sisestage väärtus väljale Saateleht.
    * See on hankija väljastatud saatelehelt pärinev saatelehe ID. Lisage kordumatu number.  
5. Valige ostutellimus väljalt Number.
6. Klõpsake nuppu OK.

## <a name="add-lines-to-item-arrival-journal"></a>Kauba saabumistöölehtede ridade lisamine
1. Klõpsake suvandit Funktsioonid.
2. Klõpsake suvandit Loo read.
    * Ridu saab sellele töölehele sisestada käsitsi või luua automaatselt. See näitab, kuidas seda automaatselt luua.  
3. Märkige või tühjendage ruut Lähtesta kogus.
    * See lähtestab töölehe ridadel oleva koguse registreerimata kogusega ostutellimuse realt.  
4. Klõpsake nuppu OK.

## <a name="post-the-journal"></a>Töölehe sisestamine
1. Klõpsake valikut Sisesta.
2. Klõpsake nuppu OK.

## <a name="generate-the-product-receipt"></a>Toote sissetuleku loomine
1. Klõpsake suvandit Funktsioonid.
2. Klõpsake valikut Toote sissetulek.
3. Klõpsake nuppu OK.


