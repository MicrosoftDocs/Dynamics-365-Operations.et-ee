---
title: Andmebaasi logimise konfigureerimine ja haldamine
description: Andmebaasi logimise abil saate jälgida rakenduses Microsoft Dynamics 365 Human Resources tabelite ja väljade muudatusi.
author: twheeloc
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8faf0be5f094f18b75f2263fa622c9b7f3983274
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899759"
---
# <a name="configure-and-manage-database-logging"></a>Andmebaasi logimise konfigureerimine ja haldamine


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Andmebaasi logimise abil saate jälgida rakenduses Microsoft Dynamics 365 Human Resources tabelite ja väljade muudatusi. See artikkel kirjeldab, kuidas:

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
2. Valige päise **kaasamiseks kirjetes** suvand **Filter**.
3. Valige kustutamislogide valimiseks kasutatav meetod. Sisestage üks järgmistest suvanditest:

   - Tabeli kood
   - Logi tüüp
   - Loodud kuupäev ja kellaaeg

4. Kasutage vahekaarti **Andmebaasilogi puhastamine**, et määrata, millal käitada logi puhastamise ülesanne. Vaikimisi on andmebaasilogid saadaval 30 päeva.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
