---
title: "Microsoft Dynamics AX 2012 laohalduse täiendamine versioonile Finance and Operations"
description: "Selles teemas antakse ülevaade toodete ja laohalduse migreerimise võimalustest."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocationWHSProcessEnablement, WHSLocationProfile, InventTableStorageDimensionGroupChange, InventUpdateBlockedItem, WHSParameters, WHSReservationHierarchy, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1714054
ms.assetid: 79a1a3b9-3a36-4162-8839-ec39b5e26602
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e0ff3a22b89ce22096198d2e1dd1ea9ed10239a9
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="upgrade-warehouse-management-from-microsoft-dynamics-ax-2012-to-finance-and-operations"></a>Microsoft Dynamics AX 2012 laohalduse täiendamine versioonile Finance and Operations

[!include [banner](../includes/banner.md)]

Selles teemas antakse ülevaade WMSII moodulis töötava Microsoft Dynamics AX 2012 R3 täiendamisest versioonidel Microsoft Dynamics 365 for Finance and Operations.

Finance and Operations ei toeta enam pärandmoodulit **WMSII** rakendusest Microsoft Dynamics AX 2012. Selle asemel saab kasutada moodulit **Laohaldus**. WMSII moodulis saab finantsilisteks varudeks valida varude dimensioonid Asukoht ja Aluse ID, kuid varude dimensiooni Aluse ID ei saa kasutada finantsilisteks varudeks rakenduses Finance and Operations.

Versioonitäienduse käigus tuvastatakse ja märgitakse blokeerituks kõik tooted, mis on seotud laoala dimensioonigrupiga, mis kasutab varude dimensiooni Aluse ID, ja neid ei töödelda versioonitäienduse jaoks.

## <a name="upgrading-to-finance-and-operations-when-ax-2012-r3-wmsii-is-used"></a>Versioonitäiendus Finance and Operationsiks, kui kasutatakse rakendust AX 2012 R3 WMSII
Pärast versioonitäiendust võite kasutada valikute komplekti vormis **Kaupade laoala dimensioonigrupi muutmine**, et versioonitäienduse ajal blokeeritud toodetelt blokeering eemaldada ja seejärel nende toodete kandeid töödelda.

### <a name="enabling-items-in-finance-and-operations"></a>Kaupade aktiveerimine Finance and Operationsis
See muudatus on vajalik, kuna rakenduses Finance and Operations kuulub kauba jälgimine laohalduse protsesside hulka. Nende protsesside puhul tuleb kõik laod ja nende asukohad seostada asukohaprofiiliga. Kui soovite kasutada laohalduse protsesse, tuleb teha järgmine konfiguratsioon.
-   Olemasolevatel ladudel peab olema lubatud kasutada laohaldusprotsesse 
-   Olemasolevad väljastatud tooted peavad olema seostatud laoala dimensioonigrupiga, mis kasutab laohalduse protsesse 

Kui laoala dimensioonigrupid kasutavad varude dimensiooni Aluse ID, tuleb olemasolevate vabade kaubavarude asukohad, mis kasutavad varude dimensiooni Aluse ID, seostada asukohaprofiiliga, kus on valitud parameeter **Kasuta litsentsiplaadi jälgimist**. Kui olemasolevates ladudes ei peaks laohaldusprotsesside kasutamine lubatud olema, võite muuta olemasolevad vaba kaubavaru laoala dimensioonigrupid gruppideks, mis käsitlevad ainult varude dimensioone Laoala, Ladu ja Asukoha varud. 

> [!NOTE] 
>  Laodimensioonide gruppi saab kaupade jaoks muuta, isegi kui on olemas avatud laokandeid.

## <a name="find-products-that-were-blocked-because-of-pallet-id"></a>Aluse ID tõttu blokeeritud toodete leidmine
Selleks, et kuvada loend väljastatud toodetest, mis versioonitäienduse käigus blokeeriti ja mida töödelda ei saa, klõpsake valikuid **Varude haldus** &gt; **Seadistus** &gt; **Varud** &gt; **Varude uuendamiseks blokeeritud kaubad**.

## <a name="change-storage-dimension-group-for-blocked-products"></a>Blokeeritud toodete laoala dimensioonigrupi muutmine 
 
Selleks et kaupa kasutataks osana laohalduse protsessist, peab kaup olema seostatud laoala dimensioonigrupiga, kus asukoha varude dimensioon on aktiivne ja parameeter **Kasuta laohaldusprotsesse** on valitud. Kui see säte on valitud, muutuvad varude dimensioonid Laoala, Ladu, Varude olek, Asukoht ja Litsentsiplaat aktiivseks.

Selleks, et eemaldada versioonitäienduse käigus blokeeritud kaupadelt blokeering, tuleb valida toodetele uus laodimensioonide grupp. Pange tähele, et laodimensioonide gruppi saab muuta, isegi kui on olemas avatud laokandeid. Versioonitäienduse ajal blokeeritud kaupade kasutamiseks on kaks võimalust.

-   Muutke kauba laoala dimensioonigrupp selliseks laoala dimensioonigrupiks, mis kasutab ainult dimensioone Laoala, Ladu ja Asukoha varud. Selle muudatuse tulemusena ei kasutata enam varude dimensiooni Aluse ID.
-   Muutke kauba laoala dimensioonigrupp selliseks laoala dimensioonigrupiks, mis kasutab laohalduse protsesse. Selle muudatuse tulemusena kasutatakse nüüd varude dimensiooni Litsentsiplaat.

## <a name="configure-warehouse-management-processes"></a>Laohaldusprotsesside konfigureerimine
Enne väljastatud toodete kasutamist moodulis **Laohaldus** peavad tooted kasutama laoala dimensioonigruppi, kus on valitud parameeter **Kasuta laohaldusprotsesse**.

### <a name="enable-warehouses-to-use-warehouse-management-processes"></a>Olemasolevatel ladudel laohaldusprotsesside kasutamise lubamine

1.  Looge vähemalt üks uus asukohaprofiil.
2.  Klõpsake valikuid **Laohaldus** &gt; **Seadistus** &gt; **Luba laohaldusprotsessid** &gt; **Luba lao seadistus**.
3.  Lisage lehel **Luba lao seadistus** laod, mis tuleks lubada. Selle toimingu võib teha otse lehel või Microsoft Office’i integratsiooni kasutades.
4.  Asukohaprofiili määramine kõigile asukohtadele. Selle toimingu võib teha hõlpsasti otse lehel Microsoft Office’i integratsiooni kasutades. Võite andmed eksportida ja importida või kasutada andmeüksuse töötlemist jaotises [Andmehaldus](../../dev-itpro/data-entities/data-entities.md).
5.  Valideerige muudatused. Valideerimisprotsessi käigus toimuvad mitmesugused andmete terviklikkuse valideerimised. Suurema versioonitäienduse protsessi käigus võib olla vaja ilmnevaid probleeme allika juurutamisel korrigeerida. Sellisel juhul on vajalik täiendav andmete versioonitäiendus.
6.  Töödelge muudatused.

### <a name="change-the-storage-dimension-group-for-items-so-that-it-uses-warehouse-management-processes"></a>Muutke kaupade laoala dimensioonigruppi, nii et see kasutaks laohaldusprotsesse

1.  Looge uus väärtus **Varude olek** ja määrake see väärtuseks **Varude oleku vaike-ID** sätetes **Laohalduse parameetrid**.
2.  Looge uus laoala dimensioonigrupp, kus on valitud parameeter **Kasuta laohaldusprotsesse**.
3.  Määratlege lehel **Reserveerimishierarhia** kauba ladustamise ja jälgimisdimensiooni gruppide kohaselt uus reserveerimishierarhia.
4.  Looge vähemalt üks kauba seeriagrupp, mis sisaldab vähemalt samu ühikuid, mida kasutatakse kauba laoühikutena.
5.  Klõpsake valikuid **Laohaldus** &gt; **Seadistus** &gt; **Luba laohaldusprotsessid** &gt; **Kaupade laoala dimensioonigrupi muutmine**.
6.  Lisage lehel **Kaupade laoala dimensioonigrupi muutmine** kaubakoodid, laoala dimensioonigrupid ja ühiku seeriagrupid. Selle toimingu saab teha otse lehelt, kasutades Microsoft Office’i integratsiooni, või kasutades andmeüksuse protsessi jaotises [Andmehaldus](../../dev-itpro/data-entities/data-entities.md).
7.  Valideerige muudatused. Valideerimisprotsessi käigus toimuvad mitmesugused andmete terviklikkuse valideerimised. Suurema versioonitäienduse protsessi käigus võib olla vaja ilmnevaid probleeme allika juurutamisel korrigeerida. Sellisel juhul on vajalik täiendav andmete versioonitäiendus.
8.  Töödelge muudatused. Kõigi varude dimensioonide uuendamine võib veidi aega võtta. Saate edenemist pakett-tööde toimingute abil jälgida.

