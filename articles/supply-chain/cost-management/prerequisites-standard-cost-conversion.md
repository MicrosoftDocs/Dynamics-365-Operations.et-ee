---
title: Standardkulu teisendamise eeltingimused
description: See teema käsitleb ülesandeid, mis tuleb täita enne standardkulu teisendamist.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: 50891
ms.assetid: 73af66cf-c924-45be-837a-a648dbd05a31
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2eefb305f12996eb8fe1b72715f7e8e2509c551ff1e6abb3656221a8dbc76461
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6734303"
---
# <a name="prerequisites-for-a-standard-cost-conversion"></a>Standardkulu teisendamise eeltingimused

[!include [banner](../includes/banner.md)]

See teema käsitleb ülesandeid, mis tuleb täita enne standardkulu teisendamist. 

Enne standardkulu teisendamise käivitamist toimige järgmiselt.

1.  Määratlege standardkuludele **kauba mudeligrupp**. Lehe Kauba mudeligrupid abil saate luua kauba mudeligrupi, mis kasutab standardkulu laomudelit. Standardkulu teisendamise seadistamisel määrate selle kauba mudeligrupi teisendatavatele kaupadele.
2.  Määrake igale kaubale **kulugrupp**.
    -   Ostetud kaubale määratud kulugrupp saab toimida standardkuludega seotud pearaamatukontode määramise alusena. See võib hõlmata pearaamatukontode määramist ostuhinnahälvetele. Tootmiskeskkonnas annab ostetud komponentidele määratud kulugrupp ka tootetud kauba arvutatud kulude segmentimise.
    -   Toodetud kaubale määratud kulugrupp suudab toimida standardkuludega seotud pearaamatukontode määramise alusena, nt pearaamatu kontode määramisel tootmise hälvete puhul.

3.  Määrake **standardne tellimiskogus** toodetavale kaubale, kui sellel on püsikulud. Toodetud kauba standardne tellimiskogus toimib raamatupidamisliku saatepartii suurusena püsikulude amortiseerimiseks või proportsionaalseks jaotamiseks. Need võivad hõlmata seadistusaegu protsessi operatsioonides või komponentide püsikogust koosluses.
4.  Määrake **pearaamatukontod**, mis on seotud standardkuludega, eelkõige ümberhindluse hälbega. Kasutage standardkuludega seotud pearaamatukontode määramiseks lehte **Sisestamine** (**Varude haldus** &gt; **Seadistus**). Standardkulu teisendusprotsessi korral peate vähemalt määrama ümberhindluse hälbe konto kõikidele kaupadele ja kulugruppidele. Määratlege lehel **Kontoplaan** standardkulude puhul vajalikud pearaamatukontod. Lubage lehel **Kandekombinatsioonid** kulusuhted (tabelites, gruppides ja mõlemas) enne kauba sisestusreeglite määratlemist.
5.  Määrake standardkuludele vastavad laoparameetrid. Määrake lehe **Varude ja laohalduse parameetrid** vahekaardil **Numbriseeriad** ümberhindamiskannetele numbriseeria. Ümberhindamiskanne luuakse siis, kui standardkulude teisendamine toob kaasa kauba laoväärtuse muutuse. Määratlege lehe **Varude ja laohalduse parameetrid** vahekaardil **Laoarvestus** kulujuhtimise parameetrid standardkuludega seotud kahe parameetri määratlemiseks.
    -   Valige väljalt **Kulujaotus** suvand Ei või Alamraamat. Suvandi Alamraamat valikut nimetatakse aktiivse kulu jaotamiseks. Aktiivse kulu jaotamine on standardkulu kaupade mitmetasemelises tootestruktuuris kulugruppide segmentimise arvutamiseks, säilitamiseks ja vaatamiseks väga oluline toiming. Kui kulu jaotamine on aktiivne, saate aru anda ja analüüsida ühetasandilises, mitmetasandilises või koguvormingus järgmist.
        1.  Varud
        2.  Lõpetamata toodang (WIP)
        3.  Tuletusreegel (GOGS) kulugrupi kohta

        Aktiivne kulu jaotamine tähendab seda, et toodetud kauba kulu lubamine põhjustab kulugrupi segmentimise talletamise kauba kulukirjes. Kui te ei sisesta väljale **Kulu jaotamine** väärtust, siis kulugrupi kaupade puhul kulugrupi segmentimist ei hallata. Toodetud kauba standardkulu arvutatakse ja talletatakse ühe summana ilma kulugrupi segmenteerimiseta ja toodetud kaupade kulu osad koondatakse ühele summale.
    -   Valige väljalt **Standardi hälbed** grupp summa või kulu alusel. Kulu alusel grupi valimine võimaldab tuvastada ostuhinna hälbeid ja tootmise hälbeid kulugruppide kaupa. See võimaldab tuvastada nelja tüüpi tootmishälbeid (partii suuruse, koguse-, hinna- ja asendushälbed). Summa alusel grupi valimisel ei saa te tuvastada hälbeid kulugrupi alusel nelja tüüpi tootmishälbeid. Te saate vaadata vaid summeeritud tootmiskulude hälbeid. Standardi hälvete poliitika töötab kulujaotumise poliitikast sõltumatult. Te saate valida kulujaotumise poliitika ja erinevused kulugrupi alusel, nii et kulugrupi tootmiskulude hälbed hõlmatakse ikkagi.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]