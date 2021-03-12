---
title: Tootmiskeskkonnas standardkulude värskendamine
description: Selles artiklis antakse juhiseid tootmiskeskkonnas standardsete kulude värskendamise kohta.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7bc203176967fbe6c20f4f687fe36fdcf3157b20
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983821"
---
# <a name="update-standard-costs-in-a-manufacturing-environment"></a>Tootmiskeskkonnas standardkulude värskendamine

[!include [banner](../includes/banner.md)]

Selles artiklis antakse juhiseid tootmiskeskkonnas standardsete kulude värskendamise kohta. 

Värskendused võivad kajastada uusi kaupu, kulukategooriaid või kaudse kulu kalkulatsiooni valemeid. Samuti võivad need kajastada parandusi ja kulumuutusi. Värskendamise tüüp mõjutab etappe, mille peate läbima standardsete kulude värskendamiseks, ja seda illustreerivad järgmised juhtumid.

-   Sisestage ostetud kauba eeldatavad standardse kulu muutmised ja muutke seejärel asjakohasel kuupäeval kauba kulukirjete olekuks **Aktiivne**. Ärge siiski arvutage uuesti toodetavate kaupade kulusid, mille puhul kasutatakse ostetud kaupu.
-   Sisestage standardsed kulud uue ostetud kauba jaoks, kuid ärge arvutage uuesti toodetavate kaupade kulud koosluste versiooniga, mis sisaldab komponendina uusi ostetud kaupu.
-   Parandage või muutke ostetud kauba kulu või muutke ostetud kaubale määratud kulugruppi ning arvutage kõigi toodetavate kaupade kulu koosluse versiooniga, mis sisaldab komponendina uut kaupa.
-   Muutke kulukategooria kulu ja arvutage kõigi toodetavate kaupade kulu protsessi versiooniga, mis sisaldab kulukategooriat kasutavaid protsessi operatsioone.
-   Muutke protsessioperatsioonidele määratud kulukategooriaid või kulukategooriatele määratud kulugruppi. Seejärel arvutage kõigi toodetavate kaupade kulu protsessi versiooniga, mis sisaldab kulukategooriat kasutavaid protsessi operatsioone.
-   Muutke kaudse kulu kalkulatsiooni valemit ja arvutage kõigi muudatusest mõjutatud toodetavate kaupade kulu.
-   Muutke või lisage toodetava kauba tootmiskoht ja arvutage kauba tootmiskulu selle jaoks.
-   Arvutage (või arvutage uuesti) toodetava kauba kulu ja arvutage uuesti kõigi toodetavate kaupade kulu koosluse versiooniga, mis sisaldab komponendina toodetavat kaupa.
-   Arvutage kulud uue toodetava kauba jaoks, mis põhineb määratud, kinnitatud ja aktiivse koosluse ja protsessi teabel.

Iga juhtum nõuab hoolikat kaalumist selle osas, kuidas standardseid kulusid värskendada.



