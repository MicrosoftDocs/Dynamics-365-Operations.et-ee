---
title: Kaupade registreerimine üldiseks ladustamiseks lubatud kauba puhul saabuva kauba töölehe abil
description: Selle protseduuriga selgitatakse kaupade registreerimist, kasutades kauba saabumise töölehte mooduli Laohaldus üldise ladustamise kasutamisel.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c36513587754939da4e1791b687871f71e7e8fa3d3e9990609cb7ede1c32cc6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760222"
---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-an-item-arrival-journal"></a>Kaupade registreerimine üldiseks ladustamiseks lubatud kauba puhul saabuva kauba töölehe abil

[!include [banner](../../includes/banner.md)]

Selle protseduuriga selgitatakse kaupade registreerimist, kasutades kauba saabumise töölehte mooduli Laohaldus üldise ladustamise kasutamisel. Seda teeb üldjuhul vastuvõtuametnik. Saate käitada selle protseduuri demoandmete ettevõttes USMF näidatud näidisväärtusega.  Kui te USMF-i ei kasuta, peate enne selle juhendi käivitamist olema kinnitanud avatud ostutellimuse reaga ostutellimuse. Real olev kaup peab olema ladustatav. Samuti peavad kaubad olema seostatud laoala dimensioonigrupiga, kus sait ja ladu on aktiivsed.


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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]