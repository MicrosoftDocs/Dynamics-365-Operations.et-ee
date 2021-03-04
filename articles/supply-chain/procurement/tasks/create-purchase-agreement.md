---
title: Ostulepingu loomine
description: Selles teemas jagatakse juhiseid, kuidas luua ostulepingut.
author: mkirknel
manager: tfehr
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1edfd4e56910376d0596eec5eff2af888f7dc98d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426201"
---
# <a name="create-a-purchase-agreement"></a>Ostulepingu loomine

[!include [banner](../../includes/banner.md)]

Selles teemas jagatakse juhiseid, kuidas luua ostulepingut. Seda teeb tavaliselt ostujuht. Saate selle protseduuriga tutvuda demoettevõtte USMF või oma andmeid kasutades. Enne alustamist peate seadistama ostulepingu klassifikatsioonid. Kui olete lepingu loonud, saate seda kasutada ostutellimuse loomisel ning sellega kopeeritakse ostulepingu tingimused lepinguga seotud tellimuse päisesse ja kõigile ridadele.


## <a name="create-a-new-purchase-agreement"></a>Uue ostulepingu loomine
1. Avage **Navigeerimispaan > Moodulid > Hanked > Ostulepingud > Ostulepingud**.
2. Klõpsake valikut **Uus**.
3. Väljal **Hankija konto** valige rippmenüü ja valige soovitud kirje rida.
4. Väljal **Ostulepingu klassifikatsioon** valige rippmenüü ja valige soovitud kirje rida.
5. Suurendage vahekaarti **Üldine**.
6. Väljale **Aegumiskuupäev** sisestage kuupäev.

    - Aegumiskuupäev kehtib vaikimisi kõigile kohustuseridadele ja määratleb, kui kaua konkreetne kohustus kehtib.  

7. Väljale **Dokumendi pealkiri** sisestage oma ostulepingu nimi.

    - Jätke välja **Vaikekohustus** seadistuseks **Toote koguse kohustus** (või muutke see, kui see pole nii seadistatud).  
    - Vaikekohustuse väärtus määratleb teie suvandid lepingu ridadel. Kui vajate lepingu ridade loomisel uut kohustuse tüüpi, peate muutma päises vaikekohustust. Kohustusi on 4 tüüpi: **Toote koguse kohustus** - konkreetse tootekoguse jaoks; **Toote väärtuse kohustus** - konkreetse toote valuuta summa jaoks; **Toote kategooria väärtuse kohustus** - konkreetse toote valuuta summa jaoks hankekategoorias, kus summa võib olla kataloogikauba või kataloogivälise kauba jaoks; **Väärtuse kohustus** - konkreetse valuuta summa jaoks, mille võib täita mis tahes toode või hankekategooria.  

8. Valige nupp **OK**.

## <a name="add-a-commitment"></a>Kommentaari lisamine
1. Valige **Lisa rida**.
2. Väljal **Kaubakood** valige rippmenüüst soovitud kirje.
3. Sisestage arv väljale **Kogus**. See on lõplik kogus, mille ostmises oma hankijalt olete kokku leppinud.  
4. Sisestage arv väljale **Ühiku hind**.
5. Laiendage jaotist **Rea üksikasjad**.
6. Määrake suvandi **Maksimaalne on jõustatud** väärtuseks **Jah**. Suvand **Maksimaalne on jõustatud** piirab kohustuse kasutust. Saate osta ainult kuni rea väljal **Kogus** määratud koguseni.  

## <a name="add-header-conditions"></a>Päise tingimuste lisamine
1. Toimingupaanil valige **Suvandid**.
2. Valige **Muuda vaadet**.
3. Valige **Päise vaade**.
4. Laiendage jaotist **Tingimused**.
5. Väljal **Makseviis** valige rippmenüüst soovitud kirje. Maksetingimused hankija kontolt kuvatakse siin vaikimisi.  
6. Väljal **Tarneviis** valige rippmenüüst soovitud kirje.
7. Väljal **Tarnetingimused** valige rippmenüü nupp, et avada otsing.

## <a name="confirm-and-activate-the-agreement"></a>Leppe kinnitamine ja aktiveerimine
1. Toimingupaanil valige **Ostuleping**.
2. Valige **Kinnitus**. Määrake suvandi **Märgi leping kehtivaks** väärtuseks **Jah**.  
3. Valige nupp **OK**.
4. Toimingupaanil valige **Ostuleping**.
5. Valige **Ostulepingu kinnitused**. Suvand **Eelvaade/prindi** lubab teil luua ostulepingu jaoks dokumendi, mille saate seejärel printida või hankijale saata. Lepingu hiljem muutmisel ja uuesti kinnitamisel kuvatakse siin mõlemad versioonid.  
6. Sulgege leht.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]