---
title: " Jaemüügi väljavõtete kauplusekonfiguratsioonid"
description: See protseduur selgitab jaekaupluse konfiguratsioone, mis mõjutavad jaemüügi väljavõtete loomise ja sisestamise viisi.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9fddeb8434d916df1613d61da88110dec8fb4465
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563640"
---
# <a name="store-configurations-for-retail-statements"></a> Jaemüügi väljavõtete kauplusekonfiguratsioonid

[!include[task guide banner](../includes/task-guide-banner.md)]

See protseduur selgitab jaekaupluse konfiguratsioone, mis mõjutavad jaemüügi väljavõtete loomise ja sisestamise viisi. Jaekaupluste finantsdimensioone käsitletakse teises protseduuris. See protsess kasutab demoettevõtte USRT-i andmeid.

1. Avage Jaemüük ja kaubandus > Kanalid > Jaemüügikauplused > Kõik jaemüügikauplused.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake loendis valitud real olevat linki.
    * Jaotise Väljavõte/sulgemine sätted mõjutavad väljavõtte loomist, kinnitamist ja sisestamist kaupluse jaoks.  Avage jaotis Väljavõte/sulgemine.  
    * Valige meetod, mille järgi soovite väljavõtte ridu grupeerida.  
    * Valige suvand Jah, kui väljavõtte loomise pakett-tööst väljavõtete loomisel tuleb päevas luua vaid üks väljavõte.  
    * Väli Päevakassa arvutamine määratleb, kas päevakassad tuleb kokku liita või kasutada viimast.  
    * Valige pearaamatukonto, millesse ümardamiserinevused sisestada.  
    * Väljal Maksimaalsne ümardamiserinevus saate sisestada maksimaalse lubatud ümardamiserinevuse.  
    * Väljale Sisestamine saate sisestada väljavõtte puhul lubatud maksimaalne sisestamise koguerinevuse.  
    * Väljale Vahetus saate sisestada väljavõtte maksimaalne vahetuse koguerinevuse.  
    * Väljale Kanne saate sisestada väljavõtterea maksimaalne koguerinevuse.  
    * Väljal Sulgemismeetod saate määratleda, kas väljavõttesse kaasatavad kanded peaksid olema osa suletud vahetusest või võivad need olla mis tahes kanded määratletud kuupäeva-/kellaajavahemikus.  
    * Väljale Tööpäeva lõpp saate sisestada kellaaja, kui pärast keskööd toimuvad kanded tuleb sisestada koos eelmise päevaga.  
    * Valige suvand Jah, kui pärast keskööd toimuvad kanded tuleb sisestada eelmise päeva osana.  
    * Valige suvand Jah, kui soovite määratleda iga väljavõttemeetodi jaoks loodavaid väljavõtteid. Sellest on abi, kui sisestusjõudlust tuleb suurte kandemahtudega kaupluste puhul suurendada, kuna see loob palju väiksemaid väljavõtteid, mida saab korraga töödelda.  
    * Väljal Vaikeklient saate valida kliendikonto, mida kasutada kohale tulevatele klientidele müümisel.  

