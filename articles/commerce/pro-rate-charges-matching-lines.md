---
title: Päisekulude proportsionaalselt jaotamine vastavatele müügiridadele
description: See teema kirjeldab täiendavaid võimalusi automaatsete kulude arvutamise ja kaubanduskanali tellimustele rakendamise kohta, kasutades täpsemate automaatsete kulude funktsiooni.
author: hhaines
manager: annbe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 048885cac7a316e144b2df072da405d74096203f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411548"
---
# <a name="prorate-header-charges-to-matching-sales-lines"></a>Päisekulude proportsionaalselt jaotamine vastavatele müügiridadele


[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse päisetasemel automaatsete kulude rühmitamise ja nende kaubanduse müügiridadele proportsionaalselt jaotamise funktsionaalsust. See funktsioon on saadaval kannetele, mis on loodud kassas (POS) rakenduse Retail versioonis 10.0.1 ja müükides, mis on loodud rakenduse Retail 10.0.2 versiooni kõnekeskuses.

See funktsioon on saadaval ainult siis, kui funktsioon [täpsemad automaatsed kulud](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges) on lehel **Kaubanduse parameetrid** olevat suvandit kasutades sisse lülitatud. Samuti saab automaatsete kulude täiustatud arvutusviisi rakendada ainult müügitellimustele, mis on loodud kaubanduskanalite kaudu (kassa, kõnekeskus ja Dynamicsi e-Commerce’i platvorm).

See uus funktsioon pakub organisatsioonidele päisetasemel automaatsete kulude arvutamisel ja nende müügikannetele rakendamisel suuremat paindlikkust.

Rakenduse versioonides, mis on varasemad kui 10.0.1, arvutatakse päisetasemel automaatsed kulud, millel on kindel tarneviisi seos, ainult siis, kui tarneviisis esineb vastavus, mis on määratletud müügitellimuse päises.

Näiteks on päisetasemel automaatsed kulud määratletud tarneviisi **99** ja **11** puhul. Luuakse müügitellimus ja tarneviis **99** määratletakse tellimuse päises. Siiski on osa müügiridu seadistatud viisil, et nad saadetakse tarneviisiga **11**. Sellisel juhul arvestatakse ja rakendatakse müügitellimusele ainult päisetasemel kulud, mis on seotud tarneviisiga **99**.

Rakenduses Commerce on päisetasemel kuludel täiendav funktsioon, mis võimaldab teil määratleda [mitmetasemelise tasu konfiguratsiooni](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery), mis põhineb tellimuse väärtusel. Näiteks kui tellimuse väärtus on vahemikus $50,00 ja $200,00, võib ettevõte võtta veokulude eest tasu $5,00. Kui tellimuse väärtus jääb vahemikku $200,01 ja $500,00, võiks veokulu olla $4,00.

Mõned ettevõtted soovivad mitmetasandilise tasu arvutamisega kaasnevaid eeliseid, mida pakuvad päisetasemel kulud. Siiski, stsenaariumites, kus on lubatud segatarneviisid, soovivad ettevõtted veenduda, et arvutatud kulud põhinevad tarneviisi vastavusel, mis on määratletud igal müügitellimuse real.

Nüüd saate konfigureerida päisetasemel automaatseid kulusid nii, et kulude arvutamisel arvestatakse kõiki tarneviise. See funktsioon nõuab päisetasemel kulude arvutamiseks keerukamat arvutusloogikat. Loogika rühmitab kokku kõik sama tarneviisi kasutavad saadetavad kaubad ja käsitleb seda gruppi kaupade jaoks päisetaseme automaatsete kulude arvutamisel kalkulatsioonigrupina. Sama tarneviisiga kaupade puhul arvutatakse automaatsed kulud kaupade kombineeritud müügiväärtuse alusel. Sel viisil määratakse sobiv automaatse kulu järk.

Pärast seda, kui sobivad päisetasemel kulud on sama tarneviisiga saadetavate müügiridade jaoks toodud, jaotatakse arvutatud kulud proportsionaalselt müügirea tasemele. Kuna need kulud on reatasemel ja neid ei hoita päisetasemel, moodustatakse kauba ja selle jaoks arvutatud kulu väärtuse vahel spetsiifilisem link. Selline käitumine võib olla kasulik osaliste tagastuste stsenaariumite korral, kus ettevõte soovib tagastada terve tasu asemel ainult osa tasust, kui tagastatakse ainult mõned kaubad.

## <a name="scenarios"></a>Stsenaariumid

Järgmised kaks näidisstsenaariumit annavad ülevaate nende kulude arvutamisest nii uue funktsiooni kasutamisel kui ka mittekasutamisel.

### <a name="scenario-1"></a>1. stsenaarium

See stsenaarium kirjeldab käitumist, kui suvand **Proportsionaalselt vastavatele müügiridadele jaotamine** on automaatse kulu seadistuses määratud väärtusele **Ei**. (Käitumine on võrdne päisetasemel kuludega rakenduse versioonides, mis on varasemad kui versioon 10.0.1)

Selles stsenaariumis on ettevõte määratlenud päisetasemel kulud tarneviisi seostele **99** ja **11**. Tarneviisile **21** pole konfigureeritud ühtegi automaatset kulu.

![Tarneviisi 99 automaatsed kulud, kui vastenduv rea proportsionaalne arvestus on välja lülitatud](media/99_disabled.png)

![Tarneviisi 11 automaatsed kulud, kui vastenduv rea proportsionaalne arvestus on välja lülitatud](media/11_disabled.png)

Kõnekeskuses luuakse müügitellimus ja tarneviisiks määratakse **99**. See tellimus sisaldab viit kaupa. Kaks tellimuserida on konfigureeritud kasutama tarneviisi **99**, kaks rida on konfigureeritud kasutama tarneviisi **11** ja üks rida on konfigureeritud kasutama tarneviisi **21**, nagu on näidatud järgmises tabelis.

| Kaup  | Rea kogus | Tarneviis | Hind ühiku kohta |
|-------|---------------|---------------|----------------|
| 81331 | 1             | 11            | $10            |
| 81332 | 1             | 99            | 50 dollarit            |
| 81333 | 2             | 11            | $30            |
| 81334 | 3             | 99            | $10            |
| 81334 | 3             | 21            | $5             |

Selles stsenaariumis hinnatakse kogu tellimust tarneviisi **99** automaatse kulu tabeli suhtes. Kõigi müügiridade kogusummat kasutatakse automaatse kulu konfiguratsioonis vastava järgu määramiseks ja see tasu rakendatakse tellimuse päisetasemel. Selles näites on tellimuse kogusumma $165,00 ja tellimuse päisele rakendatakse veokulu $15,00. Automaatsetele kuludele, mis konfigureeritakse tarneviisile **11**, ei viidata ja neid ei rakendata kunagi.

Selles stsenaariumis, kui klient tagastab mõned tellimuse kaubad ja kui [tasukood on konfigureeritud nii, et see makstakse tagasi](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2), rakendatakse tagasimaksele süstemaatiliselt päisetaseme kulude kogusumma, isegi kui tagastatakse ainult mõned kaubad.

### <a name="scenario-2"></a>2. stsenaarium

Selles stsenaariumis määratletakse päisetasemel kulud tarneviisi seostele **99** ja **11**. Kuid nende automaatse kulu tabelite puhul on suvand **Proportsionaalselt vastavatele müügiridadele jaotamine** määratud väärtusele **Jah**.

![Tarneviisi 99 automaatsed kulud, kui vastenduv rea proportsionaalne arvestus on sisse lülitatud](media/99_enabled.png)

![Tarneviisi 11 automaatsed kulud, kui vastenduv rea proportsionaalne arvestus on sisse lülitatud](media/11_enabled.png)

Stsenaarium kasutab sama müügitellimust, mis sisaldab viit rida. Tellimuse päises on tarneviisi väärtuseks **99**, kuid müügitellimuses on iga kauba tarneviis konfigureeritud järgmises tabelis näidatud viisil.

| Kaup  | Rea kogus | Tarneviis | Hind ühiku kohta |
|-------|---------------|---------------|----------------|
| 81331 | 1             | 11            | $10            |
| 81332 | 1             | 99            | 50 dollarit            |
| 81333 | 2             | 11            | $30            |
| 81334 | 3             | 99            | $10            |
| 81334 | 3             | 21            | $5             |

Kuna automaatse kulu konfiguratsioon on määratud proportsionaalsele jaotamisele vastavate müügiridade vahel, teeb süsteem järgmised arvutusetapid.

1. Kõik kaubad, millel on sama tarneviis, rühmitatakse kokku ja süsteem arvutab rühmas olevate toodete jaoks toodete koguväärtuse.

    **Tarneviis 11**

    - Kaup 81331, kogus 1 = $10
    - Kaup 81333, kogus 2 = $60 neto ($30 ühiku kohta)
    - **Tarneviisi 11 toodete koguväärtus = $70**

    **Tarneviis 99**

    - Kaup 81332, kogus 1 = $50
    - Kaup 81334, kogus 3 = $30 neto
    - **Tarneviisi 99 toodete koguväärtus = $80**

    **Tarneviis 21**

    - Kaup 81334, kogus 3 = $15 neto
    - **Tarneviisi 21 toodete koguväärtus = $15**

2. Süsteem otsib päisetasemel automaatsete kulude konfiguratsiooni, mis vastab iga kaubarühma puhul kliendi ja tarneviisi sätetele. Kui konfiguratsioon leitakse, otsib süsteem mitmetasandilisest konfiguratsioonist tasu, mis tuleks rakendada, seda tarneviisi grupis olevate kaupade koguväärtuse põhjal.

    **Tarneviis 11**

    - Toodete koguväärtus = $70
    - **Tasu väärtus = $7**

    **Tarneviis 99**

    - Toodete koguväärtus = $80
    - **Tasu väärtus = $15**

    **Tarneviis 21**

    - Toodete koguväärtus = $15
    - **Tasu väärtus = $0** (Sellise kliendi ja tarneviisi kombinatsiooni jaoks pole automaatseid kulusid konfigureeritud.)

    ![Tarneviisi 11 tasud kuuluvad esiletõstetud järku](media/step2mode11.png)

    ![Tarneviisi 99 tasud kuuluvad esiletõstetud järku](media/step2mode99.png)

3. Süsteem arvutab kulu väärtuse, mis tuleb rakendada igale reale, võttes aluseks proportsionaalse arvestuse loogika, mis arvestab rea proportsionaalset väärtust grupi toodete koguväärtusega seoses.

    **Tarneviis 11**

    - Tasu väärtus = $7
    - Grupi tooteväärtus = $70
    - Rea 1 väärtus = $10 (= 14,2857 protsenti grupi väärtusest)
    - Rea 3 väärtus = $60 (= 85,7143 protsenti grupi väärtusest)
    - **Rea 1 reatasu = $1**
    - **Rea 3 reatasu = $6**

    **Tarneviis 99**

    - Tasu väärtus = $15
    - Grupi tooteväärtus = $80
    - Rea 2 väärtus = $50 (= 62,5 protsenti grupi väärtusest)
    - Rea 4 väärtus = $30 (= 37,5 protsenti grupi väärtusest)
    - **Rea 2 reatasu = $9,38**
    - **Rea 4 reatasu = $5,62**

    **Tarneviis 21**

    - Tasu väärtus = $0
    - Grupi tooteväärtus = $15
    - Rea 5 väärtus = $15 (= 100 protsenti grupi väärtusest)
    - **Rea 5 reatasu = $0**

Seetõttu määratakse selles näites kaubale 81334 veokulu summas $5,62. Neid tasusid saate vaadata müügitellimuse rea lehel **Tasude haldamine**. Järgmisel joonisel on näidatud, kuidas see leht kauba 81334 jaoks välja näeb.

![Müügirea proportsionaalselt jaotatud tasud kauba 81334 puhul](media/proratedlinecharge.png)

Kui seda arvutamismeetodit kasutatakse osalise tagastuse stsenaariumi korral, kui tasukood on tagasimakstav, makstakse kauba tagastamisel tagasi ainult see tasu osa, mis on eraldatud sellele reale.

## <a name="additional-resources"></a>Lisaressursid

[Omnikanali täpsemad automaatsed kulud](omni-auto-charges.md)

[Automaatsete tasude lubamine ja konfigureerimine kanali kaupa](auto-charges-by-channel.md)
