---
title: "Erinevate kuluelemendi dimensiooni liikmete vastendamine dimensiooni liikmete ühisele kogumile"
description: "Erinevate kuluelemendi dimensiooni liikmete vastendamisega kuluelemendi dimensiooni liikmete ühisele kogumile ühendate andmed analüüsi otstarbel ühisesse vormingusse."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-11-01 13 - 45 - 07
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CAMDimension, CAMDimensionMember
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: a1e9817b6ee596ad516531d7597a2a39e115749c
ms.lasthandoff: 03/31/2017


---

# <a name="map-different-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a>Erinevate kuluelemendi dimensiooni liikmete vastendamine dimensiooni liikmete ühisele kogumile

Erinevate kuluelemendi dimensiooni liikmete vastendamisega kuluelemendi dimensiooni liikmete ühisele kogumile ühendate andmed analüüsi otstarbel ühisesse vormingusse.

Kui olete globaalne ettevõtte ja järgite seadusjärgseid raamatupidamisnõudeid, võite kasutada mitut kontoplaani. Kuluelemendi dimensiooni liikmete importimisel erinevatest kontoplaanidest saate lõpuks kontode segu. Siiski võib nendel kontodel tegelikult olla sama struktuur ja võite soovi korral analüüsida ja eraldada kulud neile, kasutades ühist vormingut.

## <a name="map-cost-element-dimension-members-to-a-common-format"></a>Kuluelemendi dimensiooni liikmete vastendamine ühisele vormingule
Järgmine näide näitab teile, kuidas teie kulukontrollerina saate luua kuluarvestuses uue kuluelemendi dimensiooni, mis vastendab kuluelemendi dimensiooni liikmed USA ja Prantsuse kontoplaani struktuurist kuluelemendi dimensiooni liikmete ühisele kogumile. Seejärel saate kasutada kuluelemendi dimensiooni liikmete ühist kogumit, et analüüsida kahe juriidilise isiku kuluandmeid kuluarvestuse pearaamatus.

| Allikas: USA kontoplaan                                          | Allikas: Prantsuse kontoplaan                                          | Uus kuluelemendi dimensiooni liikmete ühine kogum                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| Imporditud kuluelemendi dimensiooni liikmed USA kontoplaanilt | Imporditud kuluelemendi dimensiooni liikmed Prantsuse kontoplaanilt | USA ja Prantsuse kuluelemendi dimensiooni liikmete vastendamine ühisele kogumile |
| 5001: Müük                                                           | 5001: Müük ja turundus                                               | 5000: Müük ja turundus                                             |
| 5030: Reklaam                                                     | 6390: Lao ost\*                                                    | 7000: Puhastuskulud                                                 |
| 7001: Puhastuskulud                                               | 7001: Reisikulu                                                      | 7001: Reisikulud                                                   |

\*Lao ostu Prantsuse kuluelemendi dimensiooni liiget ei vastendata.

## <a name="currency-conversion"></a>Valuutateisendus
Erinevaid kasutatavaid kontoplaane saab seadistada kasutama erinevaid valuutasid. Sellisel juhul määrake kindlasti valuutateisendus, et kuluandmeid töödeldaks õiget valuutat kasutades, nagu on määratletud kuluarvestuse pearaamatus, kus kasutatakse kuluelemendi dimensiooni liikmeid. Kui eeltoodud näites kasutatakse kuluarvestuse pearaamatus USA dollareid, peate looma valuutateisenduse USA dollarist eurodele (EUR), et töödelda kandeid vastendatud kuluelemendi dimensiooni liikmete jaoks.

## <a name="update-mappings-at-any-time"></a>Vastenduste värskendamine mis tahes ajal
Kuluelemendi dimensiooni vastendamise määratlusi saate igal ajal värskendada. Kuna vastendused ei ole kehtivuskuupäevaga, rakendatakse muudatused järgmine kord, kui töötlete kulukandeid või käitate kuluarvestusi.


