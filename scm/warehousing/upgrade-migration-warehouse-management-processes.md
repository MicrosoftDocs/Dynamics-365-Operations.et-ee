---
title: Migreerimine AX 2012-st rakendusse Finance and Operations
description: "See artikkel annab ülevaate toote ja laohalduse migreerimisvalikutest rakenduses Dynamics 365 for Finance and Operations."
author: BibiSp
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.custom: 1714054
ms.assetid: 79a1a3b9-3a36-4162-8839-ec39b5e26602
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 5ab19faddedae8cf61222762714609601b0ae96f
ms.contentlocale: et-ee
ms.lasthandoff: 06/20/2017

---

# <a name="migrate-from-ax-2012-to-finance-and-operations"></a>Migreerimine AX 2012-st rakendusse Finance and Operations

See teema annab ülevaate toote ja laohalduse migreerimisvalikutest rakenduses Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.

<a name="introduction"></a>Sissejuhatus
------------

Versioonitäienduse käigus Finance and Operationsiks blokeeritakse tooted, kui need on seotud mõne laoala dimensioonigrupiga, millel on sätteid, mis ei vasta Finance and Operationsi laoala dimensioonigrupi sätete nõuetele. Kuid pärast versioonitäiendust võite kasutada migreerimisvalikute komplekti protsessis **Kaupade laoala dimensioonigrupi muutmine** versioonitäienduse ajal blokeeritud toodetelt blokeeringu eemaldamiseks. Seejärel saate nende toodete kandeid töödelda. Mõned kaubad võivad juba olla seostatud laoala dimensioonigruppidega, kus dimensioonid Laoala, Ladu ja Asukoha varud on aktiivselt ja füüsiliselt jälgitavad. Sellisel juhul võite kasutada protsessi **Kaupade laoala dimensioonigrupi muutmine**, et võimaldada nende kaupade kasutamist laohalduse protsessides. See funktsioon on kasulik, kui soovite kasutada olemasolevate kaupade puhul laoala halduse funktsiooni.

## <a name="upgrading-to-finance-and-operations-when-ax-2012-r3-wmsii-is-used"></a>Versioonitäiendus Finance and Operationsiks, kui kasutatakse rakendust AX 2012 R3 WMSII
Finance and Operations ei toeta enam pärandmoodulit **WMSII** rakendusest Microsoft Dynamics AX 2012. Selle asemel saab kasutada uut moodulit **Laohaldus**. Lisateavet leiate jaotisest [Laohalduse koduleht](https://ax.help.dynamics.com/en/wiki/warehouse-management/). Varasemates versioonides sai finantsilisteks varudeks valida varude dimensioonid Asukoht ja Aluse ID. Kuid versioonitäienduse protsessi käigus ei saa varude dimensiooni Aluse ID enam finantsiliste varude puhul lubada. Kõik tooted, mis on seotud laoala dimensioonigrupiga, mis kasutab varude dimensiooni Aluse ID, blokeeritakse ja neid ei töödelda.

### <a name="enabling-items-in-finance-and-operations"></a>Kaupade aktiveerimine Finance and Operationsis

Finance and Operationsis tuleb kaubad, mida laohalduse protsessides kasutatakse, seostada laoala dimensioonigrupiga, kus on valitud parameeter **Kasuta laohaldusprotsesse**. Kui see säte on valitud, muutuvad varude dimensioonid Laoala, Ladu, Varude olek, Asukoht ja Litsentsiplaat aktiivseks. Sellele laoala dimensioonigrupile saab minna üle ainult nende kaupade puhul, mis on juba seostatud laoala dimensioonigruppidega, kus on aktiivne asukoha varude dimensioon.

### <a name="items-that-are-blocked-for-inventory-updates"></a>Varude uuendamiseks blokeeritud kaubad

Selleks, et kuvada loend väljastatud toodetest, mis versioonitäienduse käigus blokeeriti ja mida töödelda ei saa, klõpsake valikuid **Varude haldus** &gt; **Seadistus** &gt; **Varud** &gt; **Varude uuendamiseks blokeeritud kaubad**.

### <a name="reapplying-blocked-products"></a>Blokeeritud toodete uuesti rakendamine

Selleks, et eemaldada versioonitäienduse käigus blokeeritud kaupadelt blokeering, tuleb valida toodetele uus laodimensioonide grupp. Pange tähele, et laodimensioonide gruppi saab muuta, isegi kui on olemas avatud laokandeid. Versioonitäienduse ajal blokeeritud kaupade kasutamiseks on kaks võimalust.

-   Muutke kauba laoala dimensioonigrupp selliseks laoala dimensioonigrupiks, mis kasutab ainult dimensioone Laoala, Ladu ja Asukoha varud. Selle muudatuse tulemusena ei kasutata enam varude dimensiooni Aluse ID.
-   Muutke kauba laoala dimensioonigrupp selliseks laoala dimensioonigrupiks, mis kasutab laohalduse protsesse. Selle muudatuse tulemusena kasutatakse nüüd varude dimensiooni Litsentsiplaat.

### <a name="migration-processes"></a>Migratsiooniprotsessid

Finance and Operationsis kuulub kauba jälgimine laohalduse protsesside hulka. Nende protsesside puhul tuleb kõik laod ja nende asukohad seostada asukohaprofiiliga. Põhimõtteliselt, kui soovite kasutada laohalduse protsesse, tuleb tegeleda kahe protsessiga.

-   Olemasolevatel ladudel peab olema lubatud kasutada laohaldusprotsesse.
-   Olemasolevad väljastatud tooted peavad olema seostatud uue laoala dimensioonigrupiga, mis kasutab laohalduse protsesse.

Kui laoala dimensioonigrupid kasutavad varude dimensiooni Aluse ID, tuleb olemasolevate vabade kaubavarude asukohad, mis kasutavad varude dimensiooni Aluse ID, seostada asukohaprofiiliga, millel on valitud parameeter **Kasuta litsentsiplaadi jälgimist**. Kui olemasolevates ladudes ei peaks laohaldusprotsesside kasutamine lubatud olema, võite muuta olemasolevad vaba kaubavaru laoala dimensioonigrupid gruppideks, mis käsitlevad ainult varude dimensioone Laoala, Ladu ja Asukoha varud.

### <a name="using-the-warehouse-management-processes"></a>Laohaldusprotsesside kasutamine

Enne väljastatud toodete kasutamist moodulis **Laohaldus** peavad tooted kasutama laoala dimensioonigruppi, kus on valitud parameeter **Kasuta laohaldusprotsesse**.

#### <a name="enable-warehouses-to-use-warehouse-management-processes"></a>Olemasolevatel ladudel laohaldusprotsesside kasutamise lubamine

1.  Looge vähemalt üks uus asukohaprofiil.
2.  Klõpsake valikuid **Laohaldus** &gt; **Seadistus** &gt; **Luba laohaldusprotsessid** &gt; **Luba lao seadistus**.
3.  Lisage lehel **Luba lao seadistus** laod, mis tuleks lubada. Selle toimingu võib teha otse lehel või Microsoft Office’i integratsiooni kasutades.
4.  Asukohaprofiili määramine kõigile asukohtadele. Selle toimingu võib teha hõlpsasti otse lehel Microsoft Office’i integratsiooni kasutades. Võite andmed eksportida ja importida või kasutada andmeüksuse töötlemist jaotises [Andmehaldus](https://ax.help.dynamics.com/en/wiki/data-management-and-integration-through-data-entity/).
5.  Valideerige muudatused. Valideerimisprotsessi käigus toimuvad mitmesugused andmete terviklikkuse valideerimised. Suurema versioonitäienduse protsessi käigus võib olla vaja ilmnevaid probleeme allika juurutamisel korrigeerida. Sellisel juhul on vajalik täiendav andmete versioonitäiendus.
6.  Töödelge muudatused.

#### <a name="change-the-storage-dimension-group-for-items-so-that-it-uses-warehouse-management-processes"></a>Muutke kaupade laoala dimensioonigruppi, nii et see kasutaks laohaldusprotsesse

1.  Looge uus väärtus **Varude olek** ja määrake see väärtuseks **Varude oleku vaike-ID** sätetes **Laohalduse parameetrid**.
2.  Looge uus laoala dimensioonigrupp, kus on valitud parameeter **Kasuta laohaldusprotsesse**.
3.  Määratlege lehel **Reserveerimishierarhia** kauba ladustamise ja jälgimisdimensiooni gruppide kohaselt uus reserveerimishierarhia.
4.  Looge vähemalt üks kauba seeriagrupp, mis sisaldab vähemalt samu ühikuid, mida kasutatakse kauba laoühikutena.
5.  Klõpsake valikuid **Laohaldus** &gt; **Seadistus** &gt; **Luba laohaldusprotsessid** &gt; **Kaupade laoala dimensioonigrupi muutmine**.
6.  Lisage lehel **Kaupade laoala dimensioonigrupi muutmine** kaubakoodid, laoala dimensioonigrupid ja ühiku seeriagrupid. Selle toimingu saab teha otse lehelt, kasutades Microsoft Office’i integratsiooni, või kasutades andmeüksuse protsessi jaotises [Andmehaldus](https://ax.help.dynamics.com/en/wiki/data-management-and-integration-through-data-entity/).
7.  Valideerige muudatused. Valideerimisprotsessi käigus toimuvad mitmesugused andmete terviklikkuse valideerimised. Suurema versioonitäienduse protsessi käigus võib olla vaja ilmnevaid probleeme allika juurutamisel korrigeerida. Sellisel juhul on vajalik täiendav andmete versioonitäiendus.
8.  Töödelge muudatused. Kõigi varude dimensioonide uuendamine võib veidi aega võtta. Saate edenemist pakett-tööde toimingute abil jälgida.


