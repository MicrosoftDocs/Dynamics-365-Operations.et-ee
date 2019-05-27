---
title: Ostulepingu loomine
description: See protseduur selgitab, kuidas luua ostulepingut.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b317f0a0fc8f198bad9501f325557ac2a4796989
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547625"
---
# <a name="create-a-purchase-agreement"></a>Ostulepingu loomine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur selgitab, kuidas luua ostulepingut. Seda teeb tavaliselt ostujuht. Saate selle protseduuriga tutvuda demoettevõtte USMF või oma andmeid kasutades. Enne alustamist peate seadistama ostulepingu klassifikatsioonid. Kui olete lepingu loonud, saate seda kasutada ostutellimuse loomisel ning sellega kopeeritakse ostulepingu tingimused lepinguga seotud tellimuse päisesse ja kõigile ridadele.


## <a name="create-a-new-purchase-agreement"></a>Uue ostulepingu loomine
1. Avage Hanked > Ostulepingud > Ostulepingud.
2. Klõpsake valikut Uus.
3. Klõpsake väljal Hankija konto otsingu avamiseks ripploendi nuppu.
4. Otsige loendist ja valige soovitud kirje.
5. Klõpsake loendis valitud real olevat linki.
6. Klõpsake väljal Ostulepingu klassifikatsioon otsingu avamiseks ripploendi nuppu.
7. Otsige loendist ja valige soovitud kirje.
8. Klõpsake loendis valitud real olevat linki.
9. Laiendage jaotis Üldine.
10. Sisestage kuupäev väljale Aegumiskuupäev.
    * Aegumiskuupäev kehtib vaikimisi kõigile kohustuseridadele ja määratleb, kui kaua konkreetne kohustus kehtib.  
11. Sisestage väljale Dokumendi pealkiri oma ostulepingu nimi.
    * Jätke välja Vaikekohustus sätteks Toote koguse kohustus (või muutke seda, kui see on midagi muud).  
    * Vaikekohustuse väärtus määratleb teie suvandid lepingu ridadel. Kui vajate lepingu ridade loomisel uut kohustuse tüüpi, peate muutma päises vaikekohustust.  Kohustusi on nelja tüüpi: toote koguse kohustus – toote kindla koguse puhul; toote väärtuse kohustus – toote kindla valuutasumma kohta; tootekategooria väärtuse kohustus – kindla valuutasumma kohta hankekategoorias, kus summa võib kehtida kataloogikauba või mittekataloogikauba kohta; väärtuse kohustus – kindla valuutasumma puhul, mille saab täita mis tahes toote või mis tahes hankekategooriaga.  
12. Klõpsake nuppu OK.

## <a name="add-a-commitment"></a>Kommentaari lisamine
1. Klõpsake käsku Lisa rida.
2. Märkige loendis valitud rida.
3. Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.
4. Valige toode, mille puhul soovite kohustuse lisada.
5. Klõpsake loendis valitud real olevat linki.
6. Sisestage arv väljale Kogus.
    * See on lõplik kogus, mille ostmises oma hankijalt olete kokku leppinud.  
7. Sisestage arv väljale Ühiku hind.
8. Laiendage jaotis Rea üksikasjad.
9. Määrake suvandi Maksimaalne on jõustatud sätteks Jah.
    * Suvand Maksimaalne on jõustatud piirab kohustuse kasutamist. Saate osta ainult kuni koguseni, mis on määratud rea väljal Kogus.  
10. Ahendage jaotist Rea üksikasjad.

## <a name="add-header-conditions"></a>Päise tingimuste lisamine
1. Klõpsake toimingupaanil valikut Suvandid.
2. Klõpsake suvandit Muuda vaadet.
3. Klõpsake suvandit Päisevaade.
4. Laiendage jaotist Tingimused.
5. Klõpsake väljal Makseviis otsingu avamiseks ripploendi nuppu.
    * Maksetingimused hankija kontolt kuvatakse siin vaikimisi.       
6. Otsige loendist ja valige soovitud kirje.
7. Klõpsake loendis valitud real olevat linki.
8. Klõpsake väljal Tarneviis otsingu avamiseks ripploendi nuppu.
9. Klõpsake loendis valitud real olevat linki.
10. Klõpsake väljal Tarnetingimused otsingu avamiseks ripploendi nuppu.
11. Klõpsake loendis valitud real olevat linki.

## <a name="confirm-and-activate-the-agreement"></a>Leppe kinnitamine ja aktiveerimine
1. Klõpsake toimingupaanil suvandit Ostuleping.
2. Klõpsake suvandit Kinnitus.
    * Määrake suvandi Märgi lepe kehtivaks sätteks Jah.  
3. Klõpsake nuppu OK.
4. Klõpsake toimingupaanil suvandit Ostuleping.
5. Klõpsake suvandit Ostulepingu kinnitused.
    * Suvand Eelvaade/printimine võimaldab luua ostutellimuse kohta dokumendi, mille saate seejärel välja printida või hankijale saata. Lepingu hiljem muutmisel ja uuesti kinnitamisel kuvatakse siin mõlemad versioonid.  
6. Sulgege leht.

