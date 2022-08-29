---
title: Aruannetel ja dokumentidel summade kuvamisviisi värskendamine
description: See artikkel annab teavet selle kohta, kuidas uuendada summade kuvamist eesti, Läti, Leedu, Poola, Tšehhi Vabariigi, Ungari ja Venemaa aruannetes ja teistes dokumentides.
author: AdamTrukawka
ms.date: 01/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: atrukawk
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 264254
ms.search.form: Currency
ms.openlocfilehash: f9ddb4e2616c858bf8d68e485b88bf4fb7d9d5c3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273814"
---
# <a name="update-how-amounts-are-displayed-on-reports-and-documents"></a>Aruannetel ja dokumentidel summade kuvamisviisi värskendamine

[!include [banner](../includes/banner.md)]

See artikkel annab teavet selle kohta, kuidas uuendada summade kuvamist eesti, Läti, Leedu, Poola, Tšehhi Vabariigi, Ungari ja Venemaa aruannetes ja teistes dokumentides.

Juriidiliste isikute puhul Eestis, Lätis, Leedus, Poolas, Tšehhi Vabariigis, Ungaris ja Venemaal saate seadistada valuutaühikute ning allühikute jaoks täielikud ja lühinimed. Neid nimesid saab kasutada dokumentidel ja aruannetes summade kuvamisviisi määramiseks. Näiteks kuvatakse summa **LTL 100,20** arvetes või aruannetes kui **100 Litas 20 Centas**.

## <a name="set-up-full-and-short-names-for-currency-units-and-subunits"></a>Valuutaühikute ja allühikute täielike ning lühinimede seadistamine
Valuutaühikute ja allühikute täielike ning lühinimede seadistamiseks valitud keele puhul tehke järgmist.

1. Avage leht **Valuutad**.
2. Valige valuuta.
3. Toimingupaanil valige nupp **Käänamine**.
4. Keele täis- ja lühinime lisamiseks valige valik **Uus** ja sisestage teave järgmistesse väljadesse.

   |             Field                                                           |                        Kirjeldus                                                                                                                                                                                                                                                |
   |------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |                       <strong>Keel</strong>                        |                                                                                                               Valige praeguse teksti keel.                                                                                                                |
   |    <strong>Ainsuse nimetav (ühikunimede väljagrupp)</strong>    |                                                                                       Sisestage valuuta ainsusevorm. Näiteks on sõna Litas ainsuse nimetav vorm Litas.                                                                                       |
   |     <strong>Mitmuse nimetav (ühikunimede väljagrupp)</strong>     | Sisestage valuuta mitmusevorm. Näiteks sisestage Litai. <strong>Märkus</strong>. Väljad <strong>Ainsuse omastav</strong> ja <strong>Mitmuse omastav</strong> on saadaval olenevalt väljal <strong>Keel</strong> valitud keelest. |
   | <strong>Ainsuse nimetav (allühiku nimede väljagruppi)</strong> |                                                                                                        Sisestage valuuta allühiku ainsusevorm.                                                                                                         |
   |     <strong>Mitmuse nimetav (allühiku nimede väljagrupp)</strong>     |                                                                                                         Sisestage valuuta allühiku mitmusevorm.                                                                                                          |
   |    <strong>Ühikute lühinimi (Lühinime väljagrupp)</strong>    |                                                                                         Sisestage valuutat tuvastav ISO-kood. Näiteks littide tuvastamiseks sisestage LTL.                                                                                         |
   |   <strong>Ühikute lühinimi (Lühinime väljagrupp)</strong>    |                                                                                               Sisestage valuuta allühiku üldnimetus. Näiteks sisestage Centas.                                                                                               |
   |       <strong>Sidesõna „ja” ühikute ja allühikute vahel</strong>       |                                     Märkige ruut , et printida ühikute ja allühikute vahel sidesõna „ja”. Näiteks kuvatakse summa LTL 100,20 arvetel või aruannetes kui „100 Litas and 20 Centas”.                                      |
   |       <strong>Sugu</strong>       |  Valige **Mehelik**, **Naiselik** või **Kesksoost**. See näitaja võib mõjutada summa käänet, mida näidatakse kassaorderi kohalikus keeles. Näiteks **kui** **seadistate Valuuta Sugu EUR-i jaoks Neuter-ina**, kirjutatakse *summa 1,01 EUR kassaorderi Thhi keeles 01 senti Jedno eurona*.  |

5. Valige käsk **Salvesta**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
