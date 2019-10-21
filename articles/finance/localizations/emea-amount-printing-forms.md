---
title: Aruannetel ja dokumentidel summade kuvamisviisi värskendamine
description: Selles teemas antakse teavet aruannetel ja muudel dokumentidel summade kuvamisviisi värskendamiseks Eesti, Leedu, Poola, Tšehhi Vabariigi, Ungaris ja Venemaa puhul.
author: anasyash
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Currency
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 264254
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 29d9369aaeef8cb62d4dd8f9eb8fcc171a28ca6a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175740"
---
# <a name="update-how-amounts-are-displayed-on-reports-and-documents"></a>Aruannetel ja dokumentidel summade kuvamisviisi värskendamine

[!include [banner](../includes/banner.md)]

Selles teemas antakse teavet aruannetel ja muudel dokumentidel summade kuvamisviisi värskendamiseks Eesti, Leedu, Poola, Tšehhi Vabariigi, Ungaris ja Venemaa puhul.

Juriidiliste isikute puhul Eestis, Lätis, Leedus, Poolas, Tšehhi Vabariigis, Ungaris ja Venemaal saate seadistada valuutaühikute ning allühikute jaoks täielikud ja lühinimed. Neid nimesid saab kasutada dokumentidel ja aruannetes summade kuvamisviisi määramiseks. Näiteks kuvatakse summa **LTL 100,20** arvetes või aruannetes kui **100 Litas 20 Centas**.

## <a name="set-up-full-and-short-names-for-currency-units-and-subunits"></a>Valuutaühikute ja allühikute täielike ning lühinimede seadistamine
Valuutaühikute ja allühikute täielike ning lühinimede seadistamiseks valitud keele puhul tehke järgmist.

1. Avage leht **Valuutad**.
2. Valige valuuta.
3. Toimingupaanil valige nupp **Käänamine**.
4. Keele täis- ja lühinime lisamiseks valige valik **Uus** ja sisestage teave järgmistesse väljadesse.

   |                                                                        |                                                                                                                                                                                                                                                                        |
   |------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |                         <strong>Väli</strong>                         |                                                                                                                      <strong>Kirjeldus</strong>                                                                                                                      |
   |                       <strong>Keel</strong>                        |                                                                                                               Valige praeguse teksti keel.                                                                                                                |
   |    <strong>Ainsuse nimetav (ühikunimede väljagrupp)</strong>    |                                                                                       Sisestage valuuta ainsusevorm. Näiteks on sõna Litas ainsuse nimetav vorm Litas.                                                                                       |
   |     <strong>Mitmuse nimetav (ühikunimede väljagrupp)</strong>     | Sisestage valuuta mitmusevorm. Näiteks sisestage Litai. <strong>Märkus</strong>. Väljad <strong>Ainsuse omastav</strong> ja <strong>Mitmuse omastav</strong> on saadaval olenevalt väljal <strong>Keel</strong> valitud keelest. |
   | <strong>Ainsuse nimetav (allühiku nimede väljagruppi)</strong> |                                                                                                        Sisestage valuuta allühiku ainsusevorm.                                                                                                         |
   |     <strong>Mitmuse nimetav (allühiku nimede väljagrupp)</strong>     |                                                                                                         Sisestage valuuta allühiku mitmusevorm.                                                                                                          |
   |    <strong>Ühikute lühinimi (Lühinime väljagrupp)</strong>    |                                                                                         Sisestage valuutat tuvastav ISO-kood. Näiteks littide tuvastamiseks sisestage LTL.                                                                                         |
   |   <strong>Ühikute lühinimi (Lühinime väljagrupp)</strong>    |                                                                                               Sisestage valuuta allühiku üldnimetus. Näiteks sisestage Centas.                                                                                               |
   |       <strong>Sidesõna „ja” ühikute ja allühikute vahel</strong>       |                                     Märkige ruut , et printida ühikute ja allühikute vahel sidesõna „ja”. Näiteks kuvatakse summa LTL 100,20 arvetel või aruannetes kui „100 Litas and 20 Centas”.                                      |
   |       <strong>Sugu</strong>       |  Valige **Mehelik**, **Naiselik** või **Kesksoost**. See näitaja võib mõjutada summa käänet, mida näidatakse kassaorderi kohalikus keeles. Näiteks, kui määrate EUR valuuta **sooks** **Kesksugu**, siis summa 1,01 EUR on tšehhikeelsel kassaorderil, kui *Edno euro 01 cent*.  |

5. Valige käsk **Salvesta**.

