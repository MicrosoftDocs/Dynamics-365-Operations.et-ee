---
title: "Mittetootmiskeskkonna standardkulude värskendamine"
description: "Selles artiklis antakse juhiseid mittetootmiskeskkonna standardkulude värskendamise kohta."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79723
ms.assetid: 7ba0c408-2450-4042-9542-6fdf83c12e6c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: be3e5417341094caf0565c1c5ee4f9cbc40f8e76
ms.lasthandoff: 03/31/2017


---

# <a name="update-standard-costs-in-a-non-manufacturing-environment"></a>Mittetootmiskeskkonna standardkulude värskendamine

[!include[banner](../includes/banner.md)]


Selles artiklis antakse juhiseid mittetootmiskeskkonna standardkulude värskendamise kohta.

Järgmised juhised eeldavad, et kasutate kaheversioonilist lähenemist standardkulu värskendamiseks. Selles lähenemises sisaldab üks kuluarvutuse versioon standardkulusid, mis määratleti algselt külmutatud perioodiks, ja teine kuluarvutuse versioon sisaldab astmelisi värskendusi. Iga värskendus sisestatakse teise kuluarvutuse versiooni kuuluva kulukirjena ja lubatakse lõpuks. Teine võimalus on üheversiooniline lähenemine, mis kasutab algselt määratletud standardkulude kogumit. Kaheversiooniline lähenemine nõuab teise kuluarvutuse versiooni määratlemist. Siin on juhised selle kuluarvutuse versiooni määratlemiseks.

-   Määrake kulutüüp **Standardkulud**.
-   Määrake kirjeldav identifikaator, mis näitab kuluarvutuse versiooni sisu, nt **2016-VÄRSKENDUSED**.
-   Veenduge, et sisu sisaldab kulukirjeid.
-   Lubage kõigile laoaladele kulukirjete sisestamine. Laoala määramisel saab kulukirjeid sisestada ainult selle laoala jaoks.
-   Märkige taandepõhimõtteks **Pole**. Taandepõhimõte kehtib ainult toodetud kaupade kulukalkulatsioonidele.

Uute kaupade standardsete kulude parandamiseks, korrigeerimiseks või värskendamiseks järgige neid juhiseid.

1.  Kasutage **Kuluarvutuse versiooni** **seadistamise** lehte, et lubada kulu andmete sisestamine teise kuluarvutuse versiooni. Soovi korral saate vältida ootel kulude aktiveerimist, nii et aktiveerimine lubatakse pärast ootel kulude terviklikku ja täpset määramist. Soovi korral võite sisestada ka kuupäeva väljale **Alguskuupäev**. Üldjuhisena kasutage kuupäeva, millal kavatsete astmelised värskendused aktiveerida. Teine võimalus on jätta kuluarvutuse versiooni väli **Alguskuupäev** tühjaks ja sisestada siis kuupäev iga kulukirje väljale **Alguskuupäev**.
2.  Kasutage lehte **Kauba hind** värskenduste sisestamiseks kauba kulukirjetena, mis sisalduvad teises kuluarvutuse versioonis.
3.  Kasutage aruannet **Kauba hinnad** teises kuluarvutuse versioonis sisalduvate kauba kulukirjete terviklikkuse ja täpsuse kinnitamiseks.
4.  Kasutage lehte **Kuluarvutuse versiooni hooldus** blokeerimislipu muutmiseks, et lubada teises kuluarvutuse versioonis sisalduvate ootel kulukirjete aktiveerimine.
5.  Kasutage lehte **Hindade aktiveerimine** (mille saab avada lehelt **Kuluarvutuse versiooni hooldus**) kõigi teises kuluarvutuse versioonis sisalduvate ootel kauba kulukirjete aktiveerimiseks. Ootel kulukirjeid saab aktiveerida ka eraldi kaupade kohta, klõpsates nuppu **Ootel hinna aktiveerimine** lehel **Kauba hind**.
6.  Täiendava andmete hoolduse vältimiseks kasutage lehte **Kuluarvutuse versiooni seadistus** blokeerimislippude muutmiseks, et lubada teises kuluarvutuse versioonis sisalduvate ootel kulukirjete aktiveerimine. Blokeerimispoliitikad takistavad uute ootel kulude sisestamist ja ootel kulude aktiveerimist.




