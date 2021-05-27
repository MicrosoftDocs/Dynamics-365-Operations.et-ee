---
title: Aastalõpu sulgemisel puuduvad algsaldod
description: Selles teemas selgitatakse, miks algsaldod võivad aasta sulgemisel puududa ja kuidas neid saldosid taastada, kui need puuduvad.
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 045d0bf11b11c9a353858ce3ca82c698dbceea7c
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028559"
---
# <a name="year-end-close-missing-opening-balances"></a>Aastalõpu sulgemisel puuduvad algsaldod

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, miks algsaldod võivad aasta sulgemisel puududa ja kuidas neid saldosid taastada, kui need puuduvad.

### <a name="symptom"></a>Sümptom

Miks pärast pearaamatu aastalõpu sulgemist pole algsaldosid? 

### <a name="resolution"></a>Lahendus

Kui olete pearaamatus aasta sulgenud ja seejärel loonud proovibilansi, mis ei näita järgmise finantsaasta algsaldosid, tuleks kontrollida järgmist.

Kui välja **Eelmise sulgemise tagasivõtmine** väärtuseks on määratud **Jah**, siis eelmine sama finantsaasta aastalõpu sulgemine tühistatakse. Aastalõpu sulgemise tühistamisprotsessi käigus kustutatakse kõik sulgemissaldo ja algsaldo kirjed, justkui aastat ei oleks kunagi suletud. Kanded kustutatakse samuti. Aastalõpu sulgemise protsessi ei käivitata automaatselt uuesti. Peate ise protsessi uuesti käivitama, seades valiku **Eelmise sulgemise tagasivõtmine** olekuks nüüd **Ei**.

Seda stsenaariumit käsitletakse aastalõpu sulgemise KKK teemas. Lisateavet leiate artiklist [Aastalõpu tegevuste KKK](faq-year-end-activities.md).

### <a name="symptom"></a>Sümptom

Käitasin aastalõpu sulgemise ja valiku **Eelmise sulgemise tagasivõtmine** olekuks oli seatud **Ei**, kuid mul ei ole ikka veel oma finantsaasta algsaldosid.

### <a name="resolution"></a>Lahendus

Esmalt kontrollige pakett-töö olekut. Aasta sulgemine hõlmab mitmeid eraldi ülesandeid, kuid kõige kriitilisem samm on pakettülesanne kirjeldusega **Etapp 5.0.0**. Selle etapi käigus toimub avamiskannete (ja valikuliselt sulgemiskannete) sisestamine pearaamatusse. 

[![Pakett-tööde ajaloo loend](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)

Kui see etapp jõudis edukalt lõpule, kuid te ei näe algsaldosid lehel **Proovibilansi päring** (**Pearaamat > Päringud ja aruanded > Proovibilanss**), vaadake läbi aastalõpu sulgemise pakett-töö tulemused, et näha, kas saldode taastamise etapp jõudis edukalt lõpule.

[![Aastalõpu sulgemise pakett-töö tulemused](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)

Kui see etapp mingil põhjusel nurjus, sisestati avamiskanded (ja valikuliselt sulgemiskanded) tõenäoliselt edukalt. Te saate kontrollida pearaamatu kannete sisestamise edukust lehe **Pearaamatu kannete päring** abil, sisestades suletud aasta aastalõpu sulgemise dialoogis esitatud pearaamatu kande numbri ja kuupäeva (**Pearaamat > Päringud ja aruanded > Pearaamatu kanded**).

[![Pearaamatu kannete päring](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)

Kui avamiskanded (ja valikuliselt sulgemiskanded) on olemas, pole teil vaja aastalõpu sulgemist uuesti käitada. Selle asemel vaadake järgmisest jaotisest teavet selle kohta, kuidas edasi liikuda.

### <a name="symptom"></a>Sümptom

Aastalõpu sulgemise etapp „Saldode taastamine” nurjus. Kas ma pean kogu aastalõpu sulgemise protsessi uuesti käitama?

### <a name="resolution"></a>Lahendus

Saldode taastamise etapi käigus uuendatakse pearaamatu saldod, mida kasutatakse proovibilansi päringu loomisel.  See on aastalõpu sulgemise protsessi viimane etapp.  Kui see etapp on ainus nurjunud etapp, on pearaamatu kanded edukalt sisestatud.  Aastalõpu sulgemist ei ole vaja uuesti käitada. Saldode taastamise protsessi saate käsitsi käitada lehe **Finantsdimensioonikogumid** abil (**Pearaamat > Kontoplaan > Dimensioonid > Finantsdimensioonikogumid**).

[![Nupp Taasta saldod lehel Finantsdimensioonikogumid](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)

Kui selle etapi töötlemiseks kulub liiga palju aega, soovitame üle vaadata finantsdimensioonikogumite parimad tavad, mida kirjeldatakse artiklis [Finantsdimensioonide uuendamise parimad tavad](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets). 

