---
title: "Jälgida komisjonitasu müügigruppide kasutades POS"
description: "On jaemüügi tavaks jälgida müügi sidusettevõte, kes töötas kliendiga — abi, kuni müügi, müüki ja tehingu töötlemises."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: dfefdede8f3bc884b230109d6c915127a1361ecd
ms.lasthandoff: 03/31/2017


---

# <a name="track-commissions-in-pos-using-sales-groups"></a>Jälgida komisjonitasu müügigruppide kasutades POS

On jaemüügi tavaks jälgida müügi sidusettevõte, kes töötas kliendiga — abi, kuni müügi, müüki ja tehingu töötlemises.

Jälgimise müügi müügiesindaja mõõdetakse võimeid müük sidusettevõtete, samas müük kassapidaja on kiirus ja tõhusus. Vahendustasude või muude stiimulite arvutamisel kasutatakse sageli ka jälgida müügiesindaja müük.

## <a name="configuring-a-worker-to-be-a-sales-representative-in-pos"></a>Töötaja peab olema müügiesindaja POS seadistamine
Kui töötaja on lisatud müügigrupp, vastab komisjoni ja müügiesindaja võimalik kindlaks teha süsteemi. Töötaja, kes ei ole müügigrupp ei ole kõlblikud komisjoni ja ei kuvata Müügikoht (POS) taotluse punktis müügiesindajana. POS arvutatakse müügiesindajate nimekirja kõik müügigruppide, mis sisaldavad vähemalt ühele töötajale määratud poodi. Loend POS kui müügi grupi kood ja nimi (ID: nimi). Vaikimisi müügigrupi saab määrata töötajate toetamiseks stsenaariume, kus vahendaja soovib seada müügiesindaja POS read automaatselt. Kasutajad saavad valida töötaja kuulub müügigrupp.

## <a name="functionality-profile-settings"></a>Funktsiooni profiili seaded
On mitmeid funktsioone profiili sätteid määrab voolu ja protsessi POS, mis on seotud müügiesindajate pood.

|                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Profile**                           | **Description**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Default to cashier when available** | Kui see on lubatud, POS märgistab automaatselt koos praeguse Kassa vaikimisi müügigrupi ridu. Kui kassast pole määratud vaikimisi müügigrupi, ei seatud väärtus. Kasutaja võib käsitsi seada müügigrupi POS nupp grid.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Prompt for sales representative**   | See suvand on kolmest võimalikust väärtusest: ** nr **-kui see valik on märgitud, ei kasutajalt müügi rühma valimiseks. Väärtus võib seada veel on Kassa vaikimisi müügigrupi abil või käsitsi kasutades POS nuppu võrgu nuppu. **Tehingu algust** - kui see suvand on valitud, ja kas on **Kassa vaikimisi** ei ole lubatud või praeguse kassapidaja ei ole vaikimisi müügigrupi, kasutaja palutakse valida iga tehingu alguses müügigrupp. Valides müügigrupp viip vaikimisi kõik read valitud Müügigruppi. Kasutaja võib käsitsi seada müügigrupi POS nupp grid. **Iga rea** - kui see suvand on valitud, ja kas on **Kassa vaikimisi** ei ole lubatud või praeguse kassapidaja ei ole vaikimisi müügigrupi, kasutaja palutakse valida lisatakse iga rea müügigrupp. Kasutaja võib käsitsi seada vastava POS nupp grid. |
| **Nõuda**                           | See suvand on kohaldatav üksnes siis, kui POS on konfigureeritud viipama müügiesindaja. Kui lubatud, kasutajal peavad valida müügigrupp enne jätkamist. Muul juhul kasutaja küsitakse, kuid saate tühistada ja jätkata ilma valikut tegemata. Kui rida on lisatud, piisavate õigustega kasutaja võiks ikka eemaldada müügigrupi rida. Selles olukorras ei kehti "Nõuab müügiesindaja".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |

## <a name="displaying-the-sales-representative-information-on-the-pos-transactions-screen"></a>Pildiseeria müük representatiivne teave POS tehingute
POS tehingu paigutuse ja sisu on seadistatav ekraani paigutuse disainer ja määratud ekraani paigutusega kauplustes, registrite või töötajate abil. Selle **müügiesindaja** välja saate lisada saamise paani vahekaardi read.  Tehingu ekraanil kuvatakse määratud müügi rühma iga rea ID-d.

## <a name="adding-sales-representative-operations-to-pos-button-grids"></a>Lisades müügi esindaja toimingute POS nuppu võrgud
POS võimaldab kasutajatel nuppu võrgud, mis on ekraani paigutusega juurdepääsust POS toimingute konfigureerimiseks. POS järgmisi saab määrata nuppu grid nupud, mis on seotud müügi esindajad.

|                                           |                                                                                                                                                                                                                                                                                              |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Toiming**                             | **Description**                                                                                                                                                                                                                                                                              |
| Määra reale müügiesindaja          | Toiminguks POS kuvatakse abikõlblikud müügi sõprade (ID: nimi) poe. Valides müügi grupi loendist seab välja praeguse kandereal.                                                                                                            |
| Tühjenda realt müügiesindaja        | See POS toiming eemaldab praeguse müügi väärtus praeguse kandereaga.                                                                                                                                                                                                  |
| Määratud müügiesindaja tehingu   | Toiminguks POS kuvatakse abikõlblikud müügi sõprade (ID: nimi) poe. Valides müügi grupi loendist seatakse vaikimisi väärtus praeguse kandega. Kõik olemasolevad read ilma määratud müügigrupp on komplekt ning hiljem lisatud read. |
| Selge müügiesindaja tehingu | See POS toiming eemaldab praeguse vaikimisi müügi väärtus praeguse kande. Sellel ei ole mõju read, mis on tehingus juba olemas.                                                                                                                             |

## <a name="calculating-commissions"></a>Komisjonitasu arvutamine
Komisjoni arvutatakse töötajatele määratud müügigruppide ajal avalduse sisestamist või müügitellimuse konteerimist. Komisjonitasu summa määratakse kindlaks vastavalt töötaja komisjonitasu osa, Müügigruppide ja nendega seotud komisjoni arvutuste sätted kliendi ja/või toodete kandel.


