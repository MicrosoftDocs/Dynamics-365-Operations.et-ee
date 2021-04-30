---
title: Laohalduse uuendamine rakendusest Microsoft Dynamics AX2012 rakendusse Supply Chain Management
description: Selles teemas antakse ülevaade toodete ja laohalduse migreerimise võimalustest.
author: perlynne
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocationWHSProcessEnablement, WHSLocationProfile, InventTableStorageDimensionGroupChange, InventUpdateBlockedItem, WHSParameters, WHSReservationHierarchy, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1714054
ms.assetid: 79a1a3b9-3a36-4162-8839-ec39b5e26602
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31bfc203e9db28acee4b5b52b36f64d90dc4f714
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909251"
---
# <a name="upgrade-warehouse-management-from-microsoft-dynamics-ax-2012-to-supply-chain-management"></a>Laohalduse uuendamine rakendusest Microsoft Dynamics AX2012 rakendusse Supply Chain Management 


[!include [banner](../includes/banner.md)]

Selles teemas antakse ülevaade täiendamisest rakenduselt Microsoft Dynamics AX 2012 R3, mis käitab moodulit WMSII, rakendusele Supply Chain Management.

Supply Chain Management ei toeta enam pärandmoodulit **WMSII** rakendusest Microsoft Dynamics AX 2012. Selle asemel saab kasutada moodulit **Laohaldus**. WMSII moodulis saab finantsilisteks varudeks valida varude dimensioonid Asukoht ja Aluse ID, kuid varude dimensiooni Aluse ID ei saa kasutada finantsilisteks varudeks rakenduses Supply Chain Management.

Versioonitäienduse käigus tuvastatakse ja märgitakse blokeerituks kõik tooted, mis on seotud laoala dimensioonigrupiga, mis kasutab varude dimensiooni Aluse ID, ja neid ei töödelda versioonitäienduse jaoks.

## <a name="upgrading-to-supply-chain-management-when-ax-2012-r3-wmsii-is-used"></a>Supply Chain Managementile värskendamine, kui kasutatakse AX 2012 R3 WMSII
Pärast versioonitäiendust võite kasutada valikute komplekti vormis **Kaupade laoala dimensioonigrupi muutmine**, et versioonitäienduse ajal blokeeritud toodetelt blokeering eemaldada ja seejärel nende toodete kandeid töödelda.

### <a name="enabling-items-in-supply-chain-management"></a>Kaupade lubamine Supply Chain Managementis 
See muudatus on vajalik, kuna rakenduses Supply Chain Management kuulub kauba jälgimine laohalduse protsesside hulka. Nende protsesside puhul tuleb kõik laod ja nende asukohad seostada asukohaprofiiliga. Kui soovite kasutada laohalduse protsesse, tuleb teha järgmine konfiguratsioon.
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
3.  Lisage lehel **Luba lao seadistus** laod, mis tuleks lubada. Selle toimingu saate teha otse lehel või Microsoft Office’i integratsiooni kasutades.
4.  Asukohaprofiili määramine kõigile asukohtadele. Selle toimingu saate teha hõlpsasti otse lehel Microsoft Office’i integratsiooni kasutades. Võite andmed eksportida ja importida või kasutada andmeüksuse töötlemist jaotises [Andmehaldus](../../fin-ops-core/dev-itpro/data-entities/data-entities.md).
5.  Valideerige muudatused. Valideerimisprotsessi käigus toimuvad mitmesugused andmete terviklikkuse valideerimised. Suurema versioonitäienduse protsessi käigus võib olla vaja ilmnevaid probleeme allika juurutamisel korrigeerida. Sellisel juhul on vajalik täiendav andmete versioonitäiendus.
6.  Töödelge muudatused.

### <a name="change-the-storage-dimension-group-for-items-so-that-it-uses-warehouse-management-processes"></a>Muutke kaupade laoala dimensioonigruppi, nii et see kasutaks laohaldusprotsesse

1.  Looge uus väärtus **Varude olek** ja määrake see väärtuseks **Varude oleku vaike-ID** sätetes **Laohalduse parameetrid**.
2.  Looge uus laoala dimensioonigrupp, kus on valitud parameeter **Kasuta laohaldusprotsesse**.
3.  Määratlege lehel **Reserveerimishierarhia** kauba ladustamise ja jälgimisdimensiooni gruppide kohaselt uus reserveerimishierarhia.
4.  Looge vähemalt üks kauba seeriagrupp, mis sisaldab vähemalt samu ühikuid, mida kasutatakse kauba laoühikutena.
5.  Klõpsake valikuid **Laohaldus** &gt; **Seadistus** &gt; **Luba laohaldusprotsessid** &gt; **Kaupade laoala dimensioonigrupi muutmine**.
6.  Lisage lehel **Kaupade laoala dimensioonigrupi muutmine** kaubakoodid, laoala dimensioonigrupid ja ühiku seeriagrupid. Selle toimingu saate teha otse lehelt, kasutades Microsoft Office’i integratsiooni, või kasutades andmeüksuse protsessi jaotises [Andmehaldus](../../fin-ops-core/dev-itpro/data-entities/data-entities.md).
7.  Valideerige muudatused. Valideerimisprotsessi käigus toimuvad mitmesugused andmete terviklikkuse valideerimised. Suurema versioonitäienduse protsessi käigus võib olla vaja ilmnevaid probleeme allika juurutamisel korrigeerida. Sellisel juhul on vajalik täiendav andmete versioonitäiendus.
8.  Töödelge muudatused. Kõigi varude dimensioonide uuendamine võib veidi aega võtta. Saate edenemist pakett-tööde toimingute abil jälgida.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]