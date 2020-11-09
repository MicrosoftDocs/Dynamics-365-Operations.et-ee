---
title: " Jaemüügi väljavõtete kauplusekonfiguratsioonid"
description: See protseduur selgitab kaupluse konfiguratsioone, mis mõjutavad Commerce’i väljavõtete loomise ja sisestamise viisi.
author: jashanno
manager: AnnBe
ms.date: 08/08/2019
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
ms.openlocfilehash: e255c58997ed1c0ad5614b15867f14714a8bcfc8
ms.sourcegitcommit: 776758a0ff95c3c7398986095104d1d2b9814514
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/24/2020
ms.locfileid: "4107394"
---
# <a name="store-configurations-for-retail-statements"></a> Jaemüügi väljavõtete kauplusekonfiguratsioonid

[!include [banner](../includes/banner.md)]

See protseduur selgitab kaupluse konfiguratsioone, mis mõjutavad Commerce’i väljavõtete loomise ja sisestamise viisi. Kaupluste finantsdimensioone käsitletakse teises protseduuris. See protsess kasutab demoettevõtte USRT-i andmeid.

1. Avage **Navigatsioonipaneelil** suvand **Moodulid > Jaemüük ja kaubandus > Kanalid > Kauplused > Kõik kauplused**.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake loendis valitud real olevat linki.
4. Klõpsake valikut **Redigeeri**.
5. Kiirkaardi **Väljavõte/sulgemine** seadistused mõjutavad väljavõtte loomist, kinnitamist ja sisestamist kaupluse jaoks. Laiendage kiirkaarti **Väljavõte/sulgemine**.  
6. Valige väljal **Väljavõttemeetod** meetod, mille järgi soovite väljavõtte ridu grupeerida.  
7. Valige suvand Jah väljas **Üks väljavõte päevas** , kui väljavõtte loomise pakett-tööst väljavõtete loomisel tuleb päevas luua vaid üks väljavõte.  
8. Väli **Päevakassa arvutamine** määratleb, kas päevakassad tuleb kokku liita või kasutada viimast.  
9. Valige väljas **Ümardamine** pearaamatukonto, millesse ümardamiserinevused sisestada.  
10. Väljal **Maksimaalse ümardamiserinevus** saate sisestada maksimaalse lubatud ümardamiserinevuse.
11. Väljale **Sisestamine** saate sisestada väljavõtte puhul lubatud maksimaalse sisestamise koguerinevuse.
12. Väljale **Vahetus** saate sisestada väljavõtte maksimaalse vahetuse koguerinevuse.  
13. Väljale **Kanne** saate sisestada väljavõtterea maksimaalse koguerinevuse.  
14. Väljal **Sulgemismeetod** saate määratleda, kas väljavõttesse kaasatavad kanded peaksid olema osa suletud vahetusest või võivad need olla mis tahes kanded määratletud kuupäeva-/kellaajavahemikus.  
15. Väljale **Tööpäeva lõpp** saate sisestada kellaaja, kui pärast keskööd toimuvad kanded tuleb sisestada koos eelmise päevaga.  
16. Valige suvand Jah väljal **Sisesta tööpäevana** , kui pärast keskööd toimuvad kanded tuleb sisestada eelmise päeva osana.  
17. Valige suvand Jah väljal **Poolitatud väjavõttemeetodi järgi** , kui soovite määratleda iga väljavõttemeetodi jaoks loodavaid väljavõtteid. Sellest tegevusest on abi, kui sisestusjõudlust tuleb suurte kandemahtudega kaupluste puhul suurendada, kuna see loob palju väiksemaid väljavõtteid, mida saab korraga töödelda.  
18. Saate kiirkaardi **Üldine** väljal **Vaikeklient** valida kliendikonto, mida kasutada kohale tulevatele klientidele müümisel.  

