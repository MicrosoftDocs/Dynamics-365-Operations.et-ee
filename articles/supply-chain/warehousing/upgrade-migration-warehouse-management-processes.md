---
title: Laohalduse uuendamine rakendusest Microsoft Dynamics AX2012 rakendusse Supply Chain Management
description: See artikkel annab toote- ja laohalduse migreerimissuvandite ülevaate.
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
ms.openlocfilehash: 7a88c5a615ec860890578873eaee736fabbeaf08
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065806"
---
# <a name="upgrade-warehouse-management-from-microsoft-dynamics-ax-2012-to-supply-chain-management"></a>Laohalduse uuendamine rakendusest Microsoft Dynamics AX2012 rakendusse Supply Chain Management 


[!include [banner](../includes/banner.md)]

See artikkel annab ülevaate Microsoft Dynamics AX 2012 R3-st uuendamise protsessist, käitades WMSII-moodulit tarneahela haldusse.

Supply Chain Management ei toeta enam pärandmoodulit **WMSII** rakendusest Microsoft Dynamics AX 2012. Selle asemel saab kasutada moodulit **Laohaldus**. WMSII moodulis saab finantsilisteks varudeks valida varude dimensioonid Asukoht ja Aluse ID, kuid varude dimensiooni Aluse ID ei saa kasutada finantsilisteks varudeks rakenduses Supply Chain Management.

Versioonitäienduse käigus tuvastatakse ja märgitakse blokeerituks kõik tooted, mis on seotud laoala dimensioonigrupiga, mis kasutab varude dimensiooni Aluse ID, ja neid ei töödelda versioonitäienduse jaoks.

## <a name="upgrading-to-supply-chain-management-when-ax-2012-r3-wmsii-is-used"></a>Supply Chain Managementile värskendamine, kui kasutatakse AX 2012 R3 WMSII
Pärast versioonitäiendust võite kasutada valikute komplekti vormis **Kaupade laoala dimensioonigrupi muutmine**, et versioonitäienduse ajal blokeeritud toodetelt blokeering eemaldada ja seejärel nende toodete kandeid töödelda.

### <a name="enabling-items-in-supply-chain-management"></a>Kaupade lubamine Supply Chain Managementis 
See muudatus on vajalik, kuna tarneahela halduses on kauba jälgimine osa laohaldusprotsessidest (WMS). Nende protsesside puhul tuleb kõik laod ja nende asukohad seostada asukohaprofiiliga. Kui soovite kasutada WMS-i, peab olema konfigureeritud järgmine:
-   WMS-i kasutamiseks peavad olemasolevad laod olema lubatud 
-   Olemasolevad väljastatud tooted peavad olema seostatud WMS-i kasutav laoala dimensiooni grupiga 

Kui laoala dimensioonigrupid kasutavad varude dimensiooni Aluse ID, tuleb olemasolevate vabade kaubavarude asukohad, mis kasutavad varude dimensiooni Aluse ID, seostada asukohaprofiiliga, kus on valitud parameeter **Kasuta litsentsiplaadi jälgimist**. Kui olemasolevate ladude puhul ei tohiks WMS-i kasutamist lubada, saate olemasoleva vaba kaubavaru laodimensioonigruppe muuta gruppideks, mis käsitsevad ainult laoala, lao ja asukoha varude dimensioone. 

> [!NOTE] 
>  Laodimensioonide gruppi saab kaupade jaoks muuta, isegi kui on olemas avatud laokandeid.

## <a name="find-products-that-were-blocked-because-of-pallet-id"></a>Aluse ID tõttu blokeeritud toodete leidmine
Selleks, et kuvada loend väljastatud toodetest, mis versioonitäienduse käigus blokeeriti ja mida töödelda ei saa, klõpsake valikuid **Varude haldus** &gt; **Seadistus** &gt; **Varud** &gt; **Varude uuendamiseks blokeeritud kaubad**.

## <a name="change-storage-dimension-group-for-blocked-products"></a>Blokeeritud toodete laoala dimensioonigrupi muutmine 
 
Selleks et kaupa kasutataks osana laohalduse protsessist, peab kaup olema seostatud laoala dimensioonigrupiga, kus asukoha varude dimensioon on aktiivne ja parameeter **Kasuta laohaldusprotsesse** on valitud. Kui see säte on valitud, muutuvad varude dimensioonid Laoala, Ladu, Varude olek, Asukoht ja Litsentsiplaat aktiivseks.

Selleks, et eemaldada versioonitäienduse käigus blokeeritud kaupadelt blokeering, tuleb valida toodetele uus laodimensioonide grupp. Pange tähele, et laodimensioonide gruppi saab muuta, isegi kui on olemas avatud laokandeid. Versioonitäienduse ajal blokeeritud kaupade kasutamiseks on kaks võimalust.

-   Muutke kauba laoala dimensioonigrupp selliseks laoala dimensioonigrupiks, mis kasutab ainult dimensioone Laoala, Ladu ja Asukoha varud. Selle muudatuse tulemusena ei kasutata enam varude dimensiooni Aluse ID.
-   Muutke kauba laoala dimensiooni grupp laoala dimensiooni gruppi, mis kasutab WMS-i. Selle muudatuse tulemusena kasutatakse nüüd varude dimensiooni Litsentsiplaat.

## <a name="configure-wms"></a>WMS konfigureerimine
Enne väljastatud toodete kasutamist moodulis **Laohaldus** peavad tooted kasutama laoala dimensioonigruppi, kus on valitud parameeter **Kasuta laohaldusprotsesse**.

### <a name="enable-warehouses-to-use-wms"></a>Ladudel WMS-i kasutamise lubamine

1.  Looge vähemalt üks uus asukohaprofiil.
2.  Klõpsake valikuid **Laohaldus** &gt; **Seadistus** &gt; **Luba laohaldusprotsessid** &gt; **Luba lao seadistus**.
3.  Lisage lehel **Luba lao seadistus** laod, mis tuleks lubada. Selle toimingu saate teha otse lehel või Microsoft Office’i integratsiooni kasutades.
4.  Asukohaprofiili määramine kõigile asukohtadele. Selle toimingu saate teha hõlpsasti otse lehel Microsoft Office’i integratsiooni kasutades. Võite andmed eksportida ja importida või kasutada andmeüksuse töötlemist jaotises [Andmehaldus](../../fin-ops-core/dev-itpro/data-entities/data-entities.md).
5.  Valideerige muudatused. Valideerimisprotsessi käigus toimuvad mitmesugused andmete terviklikkuse valideerimised. Suurema versioonitäienduse protsessi käigus võib olla vaja ilmnevaid probleeme allika juurutamisel korrigeerida. Sellisel juhul on vajalik täiendav andmete versioonitäiendus.
6.  Töödelge muudatused.

### <a name="change-the-storage-dimension-group-for-items-so-that-it-uses-wms"></a>Muutke kaupade laoala dimensiooni gruppi, nii et see kasutab WMS-i

1.  Looge uus väärtus **Varude olek** ja määrake see väärtuseks **Varude oleku vaike-ID** sätetes **Laohalduse parameetrid**.
2.  Looge uus laoala dimensioonigrupp, kus on valitud parameeter **Kasuta laohaldusprotsesse**.
3.  Määratlege lehel **Reserveerimishierarhia** kauba ladustamise ja jälgimisdimensiooni gruppide kohaselt uus reserveerimishierarhia.
4.  Looge vähemalt üks kauba seeriagrupp, mis sisaldab vähemalt samu ühikuid, mida kasutatakse kauba laoühikutena.
5.  Klõpsake valikuid **Laohaldus** &gt; **Seadistus** &gt; **Luba laohaldusprotsessid** &gt; **Kaupade laoala dimensioonigrupi muutmine**.
6.  Lisage lehel **Kaupade laoala dimensioonigrupi muutmine** kaubakoodid, laoala dimensioonigrupid ja ühiku seeriagrupid. Selle toimingu saate teha otse lehelt, kasutades Microsoft Office’i integratsiooni, või kasutades andmeüksuse protsessi jaotises [Andmehaldus](../../fin-ops-core/dev-itpro/data-entities/data-entities.md).
7.  Valideerige muudatused. Valideerimisprotsessi käigus toimuvad mitmesugused andmete terviklikkuse valideerimised. Suurema versioonitäienduse protsessi käigus võib olla vaja ilmnevaid probleeme allika juurutamisel korrigeerida. Sellisel juhul on vajalik täiendav andmete versioonitäiendus.
8.  Töödelge muudatused. Kõigi varude dimensioonide uuendamine võib veidi aega võtta. Saate edenemist pakett-tööde toimingute abil jälgida.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]