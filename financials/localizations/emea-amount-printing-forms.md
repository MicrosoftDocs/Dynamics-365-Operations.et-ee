---
title: "Aruannetel ja dokumentidel summade kuvamisviisi värskendamine"
description: "Selles teemas antakse teavet aruannetel ja muudel dokumentidel summade kuvamisviisi värskendamiseks Eesti, Leedu, Poola, Tšehhi Vabariigi, Ungaris ja Venemaa puhul."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264254
ms.assetid: 70b32d8d-6fa7-4617-ba74-a74bc6568d6e
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: b92a2bd912421c28b39717ea42ebbbb67c261977
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="update-how-amounts-are-displayed-on-reports-and-documents"></a>Aruannetel ja dokumentidel summade kuvamisviisi värskendamine

[!include[banner](../includes/banner.md)]


Selles teemas antakse teavet aruannetel ja muudel dokumentidel summade kuvamisviisi värskendamiseks Eesti, Leedu, Poola, Tšehhi Vabariigi, Ungaris ja Venemaa puhul.

Juriidiliste isikute puhul Eestis, Lätis, Leedus, Poolas, Tšehhi Vabariigis, Ungaris ja Venemaal saate seadistada valuutaühikute ning allühikute jaoks täielikud ja lühinimed. Neid nimesid saab kasutada dokumentidel ja aruannetes summade kuvamisviisi määramiseks. Näiteks kuvatakse summa **LTL 100,20** arvetes või aruannetes kui **100 Litas 20 Centas**.

## <a name="set-up-full-and-short-names-for-currency-units-and-subunits"></a>Valuutaühikute ja allühikute täielike ning lühinimede seadistamine
Valuutaühikute ja allühikute täielike ning lühinimede seadistamiseks valitud keele puhul tehke järgmist.

1.  Avage leht **Valuutad**.
2.  Valige valuuta.
3.  Klõpsake toimingupaanil valikut **Käänamine**.
4.  Keele jaoks täieliku ja lühinime lisamiseks klõpsake valikut **Uus** ja täitke järgmised väljad.
    |                                                           |                                                                                                                                                                                                                    |
    |-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **Väli**                                                 | **Kirjeldus**                                                                                                                                                                                                    |
    | **Keel**                                              | Valige praeguse teksti keel.                                                                                                                                                                          |
    | **Ainsuse nimetav (ühikunimede väljagrupp)**       | Sisestage valuuta ainsusevorm. Näiteks on sõna Litas ainsuse nimetav vorm Litas.                                                                                                                         |
    | **Mitmuse nimetav (ühikunimede väljagrupp)**         | Sisestage valuuta mitmusevorm. Näiteks sisestage Litai. **Märkus**. Väljad **Ainsuse omastav** ja **Mitmuse omastav** on saadaval olenevalt väljal **Keel** valitud keelest. |
    | **Ainsuse nimetav (allühiku nimede väljagruppi)** | Sisestage valuuta allühiku ainsusevorm.                                                                                                                                                            |
    | **Mitmuse nimetav (allühiku nimede väljagrupp)**         | Sisestage valuuta allühiku mitmusevorm.                                                                                                                                                              |
    | **Ühikute lühinimi (Lühinime väljagrupp)**       | Sisestage valuutat tuvastav ISO-kood. Näiteks littide tuvastamiseks sisestage LTL.                                                                                                                             |
    | **Ühikute lühinimi (Lühinime väljagrupp)**      | Sisestage valuuta allühiku üldnimetus. Näiteks sisestage Centas.                                                                                                                                         |
    | **Sidesõna „ja” ühikute ja allühikute vahel**             | Märkige ruut , et printida ühikute ja allühikute vahel sidesõna „ja”. Näiteks kuvatakse summa LTL 100,20 arvetel või aruannetes kui „100 Litas and 20 Centas”.                      |

5.  Klõpsake käsku **Salvesta**.





