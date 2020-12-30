---
title: Klientidele krediidihalduse andmete lisamine
description: See teema selgitab, kuidas lisada kliendile krediidihalduse andmeid.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 919aa50136f02a44eb69146589496ad1284721f2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442335"
---
# <a name="add-credit-management-information-for-customers"></a>Klientidele krediidihalduse andmete lisamine

[!include [banner](../includes/banner.md)]

Pärast seda, kui olete seadistanud parameetrid, mis kontrollivad krediidihaldust, saate iga kliendi kohta lisada rohkem üksikasju. Need üksikasjad juhivad kreeditihalduse protsesse ja annavad ka täiendavat teavet, mis aitab sissenõuete töörühmal kliente hallata.

## <a name="customer-information"></a>Klienditeave

Kliendi üksikasju saate lisada kiirkaardil **Krediit ja võlanõuded** lehel **Kõik kliendid** (**Müügireskontro \> Kliendid \> Kõik kliendid**).

1. Määrake suvand **Piiramatu krediidilimiit** väärtusele **Jah**, kui klienti ei tohiks piirata ühegi krediidilimiidi testiga.
2. Määrake suvand **Välista krediidihaldusest** väärtusele **Jah**, et välistada klient mistahes tegevustest, mis tavaliselt krediidihalduse protsessides aset leiavad.
3. Kliendile krediidihalduse grupi valimine.
4. Krediidilimiidi arvutamiseks kliendi valuutas sisestage kliendi krediidilimiit väljale **Krediidilimiit kliendi valuutas**. Krediidilimiit ettevõtte valuutas teisendatakse, kasutades valuutakursse, mis on määratletud kreeditilimiiti vahetuskursi tüübi poolt, mis on valitud krediidihalduse parameetrites.
5. Sisestage väljale **Viimase ülevaatuse kuupäev** kuupäev, millal kliendi krediidilimiit viimati krediidihalduri poolt üle vaadati.
6. Sisestage väljale **Järgmise plaanitud ülevaatuse kuupäev** kuupäev, millal on planeeritud kliendi krediidi üle vaatamine ja värskendamine.
7. Sisestage väljale **Lubatud krediidilimiit** kõrgeim võimalik krediidilimiit, mille saab kliendile vastavalt selle kliendi krediidiajaloo ülevaatusele määrata. Kõlblik krediidilimiit võib erineda krediidilimiidist, mis kuvatakse kiirkaardil **Krediit ja võlanõuded**.
8. Sisestage väljale **Lubatud krediidilimiidi valuuta** lubatud krediidilimiidi valuuta.
9. Sisestage väljale **Lubatud krediidilimiidi kuupäev** see kuupäev, millal lubatud krediidilimiit loodi.
10. Sisestage väljale **Krediidikonto olek** kliendi krediidikonto olek.
11. Sisestage väljale **Oleku põhjus** konto olekuga seotud põhjus.
12. Seadistage suvand **Asutusega** väärtusele **Jah**, et näidata, et klient on praegu krediidiasutusele määratud. Sellel väärtusel on ainult informatiivne eesmärk. Seda ei kasutata krediidihalduse protsessides.
13. Seadistage suvand **Tiitel hoitud** väärtusele **Jah**, et näidata hoitakse ettevõtte tiitlit. Sellel väärtusel on ainult informatiivne eesmärk. Seda ei kasutata krediidihalduse protsessis.
14. Sisestage väljale **Äritegevuse alguskuupäev** kuupäev, millal klient alustas äritegevust. Seda teavet kasutatakse riskiskooride loomisel.
15. Sisestage väljale **Klient alates** kuupäev, millal töödeldi esimesed selle kliendi kanded. Seda teavet kasutatakse riskiskooride loomisel.
16. Sisestage märkused, mida krediidimeeskond saab kasutada kliendi krediidivõime täiendavaks hindamiseks.

Võtke arvesse, et osa teabest, mis kuvatakse leheküljel **Klient** on loodud muu protsessi poolt.

- Väli **Krediidilimiit aegumiskuupäev** kuvab krediidilimiidi aegumise kuupäeva. Kui te seda ruutu ei seadista, siis kliendi krediidilimiit ei aegu.
- Väli **Krediidilimiidi kuupäev** kuvab krediidilimiidi loomise kuupäeva. Seda välja uuendatakse iga kord, kui krediidilimiiti korrigeeritakse.
- Ajutised krediidilimiidid alistavad kliendi krediidilimiiti perioodil. Neid kasutatakse krediidilimiidi asemel kogu krediidilimiidi arvutamiseks. Seda teavet kuvatakse ainult siis, kui eksisteerib aktiivne krediidilimiit. Krediidilimiidi korrigeerimise kaudu saate lisada ajutisi krediidilimiite.
- Väli **Kindlustus ja garantiid** näitab kindlustuse ja garantiide koguväärtust, mis võib suurendada kliendi krediidilimiiti.
- Väli **Krediidilimiit kokku** kuvab kliendi lõplikku krediidilimiiti. Kogu krediidilimiit hõlmab kindlustust ja garantiisid ning ajutisi krediidilimiite.

## <a name="temporary-credit-limits"></a>Ajutised krediidilimiidid

Ajutised krediidilimiidid alistavad kliendi krediidilimiidi määratud perioodil. Krediidilimiidi korrigeerimise kaudu saate lisada ajutisi krediidilimiite. Krediidilimiidi korrigeerimised lasevad krediidihalduritel värskendada ühe kliendi, kliendigrupi või kõigi klientide krediidilimiite ja aegumiskuupäevi.

Krediidilimiidi korrigeerimise kandeid saate luua lehel **Krediidilimiidi korrigeerimine** (**Krediidihaldus \> Krediidilimiidi korrigeerimine \> Krediidilimiidi korrigeerimine**).

## <a name="create-insurance-policies-and-guarantees"></a>Kindlustuspoliiside ja garantiide loomine

Igale kliendile saate luua ühe või enam kindlustuspoliisi ja garantii. Seejärel saate neid kasutada, et arvutada teie ettevõtte riskipositsiooni, kui ta pakub kliendile krediiti. Kindlustuspoliisid ja garantiid saab kaasata ka kliendi krediidilimiiti.

Kindlustuspoliise ja garantiisid saate luua lehel **Kõik kliendid** (**Müügireskontro \> Kliendid \> Kõik kliendid**). Valige klient ja seejärel valige toimingupaani vahekaardil **Krediidihaldus** suvand **Kindlustus ja garantiid**.

> [!NOTE]
> Järgmises protseduuris valite kindlustaja või käendaja globaalsest aadressiraamatust. Seetõttu peate enne selle protseduuri alustamist veenduma, et kindlustajad ja käendajad on lisatud globaalsesse aadressiraamatusse.

1. Sisestage väljale **Identifikaator** kas **Garantii** või **Kindlustus**.
2. Väljal **Garantii/kindlustuse tüüp** valige üks eelnevalt seadistatud garantii või kindlustuse tüübist.
3. Valige väljal **Kindlustaja/käendaja** kindlustaja või käendaja globaalsest aadressiraamatust. 
4. Kui valisite **Kindlustus** väljal **Identifikaator** valige väljal **Poliisi kindlustuskatte tüüp** üks eelnevalt seadistatud kindlustuskatte tüüpidest. Te ei saa garantii jaoks poliisi kindlustuskatte tüüpi valida.
5. Sisestage väljale **Identifikaator** poliisi ID. See ID on tavaliselt poliisi number.
6. Sisestage väljale **Jõustunud** kindlustuspoliisi või garantii alguskuupäev.
7. Sisestage väljale **Aegumine** kindlustuspoliisi või garantii aegumiskuupäev.
8. Sisestage väljale **Väärtus** kindlustuspoliisi või garantii väärtus. See väärtus on poliisi täielik väärtus.
9. Valige väljal **Valuuta** poliisi väärtuse valuuta. 
10. Määrake väljal **Värskenda krediidilimiiti** protsent vahemikus **0** kuni **100**. Seda protsenti rakendatakse poliisi väärtusele ja saadavat summat kasutatakse krediidilimiidi arvutustes kasutatava krediidilimiidi suurendamiseks. Arvutatud väärtust kuvatakse jaotises **Kogu krediidilimiit, kindlustus ja garantiid** kiirkaardil **Krediit ja võlanõuded** lehel **Kliendid**.

    Siin on näide.

    - Krediidilimiit (A) on 100 000.
    - Poliisi väärtus (B) on 50 000.
    - **Värskenda krediidilimiiti** protsent (C) on 50.00.
    
    Sel juhul on tegelik kehtiv krediidilimiit 125 000 (= A + \[B × C\]).

11. Märkige ruut **Kaasatud riski**, et vähendada krediidilimiiti, mida kasutatakse krediidilimiidi arvutustes poliisi täieliku väärtuse võrra. Kui see ruut on märgitud, ei kasutata krediidilimiidi arvutustes väärtust, mis arvutatakse, kui on määratud **Värskenda krediidilimiiti** protsent.

    Siin on näide.

    - Krediidilimiit (A) on 100 000.
    - Poliisi väärtus (B) on 50 000.
    - **Värskenda krediidilimiiti** protsent (C) on 50.00.

    Sel juhul on tegelik kehtiv krediidilimiit 125 000 (= A + \[B × C\]).
    
    Kui aga märgite ruudu **Kaasatud riski**, eemaldatakse **Värskenda krediidilimiiti** väärtus 50 000 (= 50.00 protsenti 100 000st) ja riski väärtus on 75 000 (= A + \[B × C\] – B).
