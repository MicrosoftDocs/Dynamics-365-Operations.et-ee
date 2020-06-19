---
title: Seerianumbriga kaupadega töötamine kassas
description: Selles teemas on selgitatud, kuidas hallata seerianumbriga kaupu kassarakenduses.
author: boycezhu
manager: annbe
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eedb64ae04345cb94bdd8cc68de833cfcfd40119
ms.sourcegitcommit: 39981582778b0a62567324452485a6721ca18284
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/27/2020
ms.locfileid: "3407494"
---
# <a name="work-with-serialized-items-in-the-pos"></a>Seerianumbriga kaupadega töötamine kassas

[!include [banner](includes/banner.md)]

Paljud jaemüüjad müüvad kaupu, mis nõuavad seerianumbri kontrollimist. Selliseid kaupasid nimetatakse *seerianumbriga kaupadeks*. Mõned jaemüüjad võivad kasutada seerianumbreid jälgimisotstarbel. Teised võivad rakendada seerianumbreid müügiprotsessi ajal teeninduse ja garantii otstarbel. Selles teemas on selgitatud, kuidas saate hallata seerianumbriga kaupu Microsoft Dynamics 365 Commerce'i kassarakenduses.

## <a name="serial-number-configurations"></a>Seerianumbrite konfiguratsioonid

Kaupa loetakse seerianumbriga kaubaks, kui sellele on määratud jälgimisdimensiooni grupp, millel on lubatud seerianumbrite säte. Valige Commerce'i peakorteris lehel **Jälgimisdimensiooni grupid** suvand **Aktiivne**, et lubada laoprotsessi jaoks seerianumbrid. Müügiprotsessi jaoks seerianumbrite lubamiseks valige suvand **Aktiivne müügiprotsessis**.

Kui suvand **Määramata sissetulekud lubatud** on kiirkaardil **Jälgimisdimensioonid** sisse lülitatud, siis on seerianumber lao sissetulekute protsessis valikuline sisend. Kui suvand on välja lülitatud, siis on seerianumber kohustuslik.

Kui suvand **Seerianumbri juhtimine** on kiirkaardil **Seerianumbrid** sisse lülitatud, siis peab ühe üksuse seerianumber olema ainulaadne. Teisisõnu, seerianumbrite duplikaadid ei ole lubatud.

## <a name="serialized-items-in-the-receiving-process"></a>Seerianumbriga kaubad vastuvõtuprotsessis

Kassarakenduse toiming **Sissetulevad varud** võimaldab kasutajatel teostada seerianumbriga kaupade osas järgmisi ülesandeid.

- Seerianumbrite registreerimine seerianumbriga kaupade põhjal, kui antud kaubad on poes vastu võetud ostutellimuse alusel.
- Eelregistreeritud seerianumbrite kinnitamine seerianumbriga kaupade põhjal, kui antud kaubad on poes vastu võetud ostutellimuse või üleviimistellimuse alusel.

> [!NOTE]
> Kui seerianumbriga kauba registreerimiseks või kinnitamiseks soovitakse kasutada toimingut **Sissetulevad varud**, siis tuleb kaup määrata jälgimisdimensiooni gruppi, milles on lubatud seerianumbrite suvand **Aktiivne**, kuid mitte suvand **Aktiivne müügiprotsessis**.

Vastuvõtuprotsessi käivitamiseks toimingu **Sissetulevad varud** all, võite käivitada vaate **Praegu vastuvõtmisel**, skannides kauba vöötkoodi või sisestades kauba ID. Teise võimalusena võite käivitada vaate **Täielik tellimuste loend**, klõpsates käsitsi kaubal.

Kui valitav või vastuvõetav kaup on seerianumbriga kaup, siis on kauba paanil **Üksikasjad** toodud link **Seerianumbri haldamine**, mis avab lehe **Seerianumbri haldamine**. Teise võimalusena võite avada lehe **Seerianumbri haldamine**, valides tellimuse üksikasjade rakendusribal suvandi **Seerianumber** või valides vastuvõtuprotsessi käigus ilmunud dialoogiaknas suvandi **Seerianumbri haldamine**. Lehel **Seerianumbri haldamine** on toodud kõik registreerimise või kinnituse ootel avatud seerianumbri read. Sellel lehel võib olla kaks vahekaarti: üks käesoleva kauba kohta ja üks kõigi loetelus sisalduvate seerianumbriga kaupade kohta.

Lehe **Seerianumbri haldus** väli **Olek** annab teavet iga seerianumbri praeguse etapi kohta.

- **Pole registreeritud** – seerianumbrit ei ole esitatud või eelregistreeritud seerianumbrit ei ole veel kinnitatud.
- **Registreerimine** – seerianumber on registreeritud ja salvestatud poe kohaliku kanali andmebaasi või eelregistreeritud seerianumber on kinnitatud. Ainult olekuga **Registreerimine** seerianumbrid esitatakse pärast vastuvõtu lõpetamist Commerce'i peakontorile.

### <a name="register-serial-numbers-against-serialized-items"></a>Seerianumbrite registreerimine seerianumbriga kaupade põhjal

Ostutellimuse korral on seerianumbriga kauba vastuvõtuprotsessi käigus avanenud dialoogiaknas valik **Seerianumbri haldamine**. Te võite valida selle suvandi, et avada leht **Seerianumbri haldamine** ja alustada seerianumbrite registreerimist. Samuti saate selle etapi vastuvõtuprotsessi käigus vahele jätta ja esitada sisendi hiljem, enne sissetuleku sisestamist.

Vaikesättena kuvatakse käesoleva kauba vahekaart. Kõikide seerianumbriridade seerianumbri väärtus on tühi ja olek on **Pole registreeritud**. Seerianumbrite dialoogiaknas järjest sisestamiseks võite skannida seerianumbrite vöötkoodid või valida rakenduspaanil **Seerianumber**. Sisestatud seerianumbrid kuvatakse loetelus ja seerianumbriridade oleku väärtuseks saab **Registreerimine**. Suurim võimalik registreeritavate seerianumbrite arv on võrdne vastuvõetava kogusega. Kui teete vea, siis võite sisestatud seerianumbrite muutmiseks valida paanil **Üksikasjad** suvandi **Redigeerimine** või **Eemaldamine**.

Samuti võite registreerida seerianumbreid lehe **Seerianumbri haldamine** vahekaardil **Kõik seerianumbriga kaubad**. Valige loetelust kaup, mille suhtes soovite seerianumbreid registreerida.

Sellel lehel seerianumbrite registreerimisel toimub dubleerimise kinnitamine. Kui soovite sisestada dubleeritud seerianumbrit sellise kauba suhtes, mille seerianumbri juhtimine on sisse lülitatud, siis saate tõrketeate ning peate valima muu numbri.

### <a name="validate-serial-numbers-on-serialized-items"></a>Seerianumbriga kaupade seerianumbrite kinnitamine

Üleviimistellimuse puhul tuleb seerianumbriga kaupade seerianumbrid eelnevalt tarneprotsessi käigus väljamineku poole poolt registreerida. Ostutellimuse puhul võib tarnija esitada seerianumbri teabe saadetise eelteatise kaudu ning te saate eelnevalt registreerida tarnimisele kuuluvate kaupade numbrid. Mõlemal juhul on seerianumbrid enne vastuvõttu teada. Seetõttu peate vastuvõtu poolel vaid kinnitama, et saite kätte kauba, mille pidite kätte saama.

Seerianumbrite kinnitamiseks võite avada vastuvõtuprotsessi ajal või mis tahes muul ajal enne vastuvõtu sisestamist lehe **Seerianumbri haldus**. Sellel lehel on kõigi eelregistreeritud seerianumbriga kaupade seerianumbrid automaatselt määratud esialgsesse olekusse **Pole registreeritud**. Seerianumbrite kinnitamiseks saate need skannida või sisestada. Kui seerianumber on sisestatud, siis rakendus kontrollib, kas see vastab eelregistreeritud seerianumbrile. Kui need ühtivad, muudetakse nende olekuks **Registreerimine**. Vastasel juhul kuvatakse tõrketeade. Suurim võimalik kinnitatavate seerianumbrite arv on võrdne vastuvõetava kogusega.

Samuti võite kinnitada seerianumbreid lehe **Seerianumbri haldamine** vahekaardil **Kõik seerianumbriga kaubad**. Valige loetelust kaup, mille suhtes soovite seerianumbreid kinnitada.

## <a name="additional-resources"></a>Lisaressursid

[Sissetulev laooperatsioon kassas](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)
