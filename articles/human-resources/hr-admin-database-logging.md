---
title: Andmebaasi logimise konfigureerimine ja haldamine
description: Andmebaasi logimise abil saate jälgida rakenduses Microsoft Dynamics 365 Human Resources tabelite ja väljade muudatusi.
author: andreabichsel
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d22ff9f3ce68c81f37840342c795d7d162eb027b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801331"
---
# <a name="configure-and-manage-database-logging"></a>Andmebaasi logimise konfigureerimine ja haldamine

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Andmebaasi logimise abil saate jälgida rakenduses Microsoft Dynamics 365 Human Resources tabelite ja väljade muudatusi. Selles teemas käsitletakse järgmist.

- Andmebaasi logimise turbe ja jõudluse haldamine
- Andmebaasi logimise seadistamine
- Andmebaasilogide puhastamine

## <a name="overview-of-database-logging"></a>Andmebaasi logimise ülevaade

Andmebaasi logimine jälgib rakenduse Microsoft Dynamics 365 Human Resources tabelite ja väljade muudatusi. Need muudatused hõlmavad lisamist, värskendamist või kustutamist. Andmebaasi logimine salvestab tabeli või väljade muudatused andmebaasilogi tabelisse.

Andmebaasi logimise äriline kasutus hõlmab järgmist.

- Auditikirje loomine kindlate tundlikku teavet sisaldavate tabelite muudatuste kohta.
- Üksikute kannete jälgimine. Andmebaasi logimine ei ole mõeldud pakett-töödes tehtavate automatiseeritud kannete jälgimiseks.

## <a name="security-for-database-logging"></a>Andmebaasi logimise turve

Andmebaasilogid võivad sisaldada tundlikke andmeid. Andke juurdepääs ainult sellistele turberollidele, mis vajavad logiandmetele juurdepääsu.

## <a name="database-logging-and-performance"></a>Andmebaasi logimine ja jõudlus

Kuigi see on väärtuslik ärilisest vaatenurgast, võib andmebaasi logimine olla kulukas ressursikasutuse ja -halduse mõttes. Andmebaasi logimise jõudluse tagajärjed hõlmavad järgmist.

- Andmebaasilogi tabel võib kasvada kiiresti ja põhjustada andmebaasi suurenemise. Kasv sõltub logitud andmete hulgas, mida te otsustate säilitada. Andmebaasilogi tabel säilitab vaikimisi ainult 30 päeva logiandmed. 

- Andmebaasi logimine võib negatiivselt mõjutada pikaajalisi automatiseeritud protsesse, näiteks pikaajalist andmete importimist.

### <a name="best-practices"></a>Head tavad

Jõudluse parandamiseks piirake logikirjeid, valides logimiseks tervete tabelite asemel konkreetsed väljad. Üldise jõudluse säilitamiseks saab andmebaasi logimine logida kuni 20 tabelit.

> [!NOTE]
> Üksikute väljade puhul saab logisse kanda ainult värskendusi.

## <a name="set-up-database-logging"></a>Andmebaasi logimise seadistamine

Andmebaasi logimise seadistamiseks saate kasutada viisardit **Andmebaasi muudatuste logimine**. Viisard pakub paindlikku viisi tabelite või väljade logimise seadistamiseks.

1. Avage **Süsteemihaldus > Lingid > Andmebaas > Andmebaasilogi seadistus**. Valige **Uus**, et käivitada viisard **Andmebaasi muudatuste logimine**.
2. Valige **Edasi**. 
3. Viisardi **Tabelite ja väljade** lehel valige tabelid ja väljad, millel soovite andmebaasi logimist toetada ja valige **Edasi**.

   > [!Note]
   > Andmebaasi logimine ei ole saadaval kõigis inimressursside andmebaasi tabelites. Valides **Näita kõiki tabeleid** loendi all laiendab tabelite ja väljade loendit, et näidata kõiki andmebaasi tabeleid, mille jaoks andmebaasi logimine on kättesaadav, aga see on täieliku andmebaasi tabelite alamkogum.

4. Viisardi **Muutuse tüübid** lehel valige andmeoperatsioonid mille jaoks te soovite iga tabeli ja välja jaoks muudatusi jälgida ja valige **Edasi**. Logimiseks saadavalolevate andmetoimingute kirjeldusi vt järgmisest tabelist.
5. Lehel **Lõpeta** vaadake tehtud muudatused üle ja valige **Lõpeta**.

| Toiming | Kirjeldus |
| -- | -- |
| Jälgi uusi kandeid | Looge logi uutele tabelis loodud kirjetele. |
| Värskendus | Looge logi tabelikirjete uuenduste jaoks või värskendage tabeli üksikult valitud väljad. Kui valite tabeli uuenduste logimise, luuakse logikirje iga kord, kui uuendatakse mis tahes tabeli kirje välja. Kui valite logi uuendused konkreetsetele väljadele, luuakse logikirje ainult siis, kui neid tabelikirjete välju uuendatakse. |
| Kustutamine | Looge tabelist kustutatud kirjete logi. |
| Nimeta võti ümber | Logikirje loomine tabelivõtme ümbernimetamise korral. |


## <a name="clean-up-database-logs"></a>Andmebaasilogide puhastamine

Järgmiste võimaluste abil saate kustutada kõik andmebaasilogid või osa neist.

- Valige kõik logid kindla tabeli jaoks.
- Valige kindlat tüüpi andmebaasilogid.
- Valige logi loomise kuupäev ja kellaaeg.

Andmebaasilogi puhastamise seadistamiseks järgige neid samme. 

1. Avage **Süsteemihaldus > Lingid > Andmebaas > Andmebaasilogi**. Valige **Puhasta logi**.

2. Valige kustutamiseks mõeldud logide valimise meetod, sisestades ühe järgmistest valikutest.

   - Tabeli kood
   - Logi tüüp
   - Loomise kuupäev ja kellaaeg

3. Kasutage vahekaarti **Andmebaasilogi puhastamine**, et määrata, millal käitada logi puhastamise ülesanne. Vaikimisi on andmebaasilogid saadaval 30 päeva.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
