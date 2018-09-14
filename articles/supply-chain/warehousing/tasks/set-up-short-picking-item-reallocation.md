--- 
title: "Kiirelt komplekteeritava kauba ümberjaotamise seadistamine"
description: "See protseduur näitab, kuidas lubada laotöötajatel kiiresti alternatiivseid asukohti leida, kui selles asukohas, kuhu nad suunati, pole piisavalt varusid."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorkException, WHSWorker
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b67965b6c8641b5d91ab3c5b0a7a7fd28a07cba6
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-short-picking-item-reallocation"></a>Kiirelt komplekteeritava kauba ümberjaotamise seadistamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas lubada laotöötajatel kiiresti alternatiivseid asukohti leida, kui selles asukohas, kuhu nad suunati, pole piisavalt varusid. Võimalik on kasutada automaatset ümberjaotamise protsessi, mis kasutab kaupade toomiseks asukohakorraldusi, kui need on teises asukohas olemas. Teise võimalusena näidatakse käsitsi ümberjaotamise kasutamisel mobiilsel seadmel loendit saadaoleva kogusega asukohtadest, mis võimaldab laotöötajal valida, millise asukoha varusid kasutada. Saate seda protseduuri kasutada demoandmete ettevõttes USMF. See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.


## <a name="set-up-work-exceptions"></a>Tööerandite häälestamine
1. Avage Laohaldus > Seadistus > Töö > Tööerandid.
2. Klõpsake valikut Uus.
    * Määratleda saab mitu tööerandit erinevate kauba ümberjaotamise poliitikatega, et laotöötaja saaks valida neist ühe töödeldava saadetise vajaduste põhjal.  
3. Tippige väärtus väljale Tööerandi kood.
    * Andke tööerandile pealkiri, mis näitaks, milleks seda kasutatakse. Näiteks Puuduva käsitsi valimine.  
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Tehke väljal Erandi tüüp valik Puuduva valimine.
6. Märkige ruut Varude korrigeerimine.
    * See valik tähendab, et varud reguleeritakse puuduva valimise asukohas automaatselt väärtusele 0.  
7. Valige või sisestage väärtus väljal Vaikimisi korrigeerimistüübi kood.
    * Näiteks ettevõtte USMF puhul võite teha valiku Remove Res Adj Out.  
8. Tehke väljal Kauba ümberjaotamine valik Käsitsi.
    * Kui teete valiku Käsitsi või Automaatne ja Käsitsi, peab laotöötajale olema antud võimalus kasutada käsitsi ümberjaotamist.  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Töötaja seadistamine käsitsi kauba ümberjaotamist kasutama
1. Sulgege leht.
2. Avage Laohaldus > Seadistus > Töötaja.
3. Klõpsake nuppu Redigeeri.
4. Valige loendist töötaja 24.
5. Laiendage jaotist Töö.
6. Tehke väljal Luba käsitsi kauba ümberjaotamine valik Jah.


