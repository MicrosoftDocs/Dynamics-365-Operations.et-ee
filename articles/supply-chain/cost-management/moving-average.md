---
title: Liikuv keskmine
description: "Liikuv keskmine on pidev keskmise põhimõttel tuginev kuluarvestusmeetod, mille puhul ostuhinna muutumisel lao väljaminekute kulud ei muutu. Erinevus on kapitaliseeritud ja põhineb proportsionaalsel arvutusel. Ülejäänud summa kantakse kuludesse."
author: AndersGirke
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 65531
ms.assetid: dfd10099-8f7f-44b1-917e-df37c2fe8773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c1f8a8cf4a58177d423709f245760a5ba9ca7e4e
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="moving-average"></a>Liikuv keskmine

[!include[banner](../includes/banner.md)]

Liikuv keskmine on pidev keskmise põhimõttel tuginev kuluarvestusmeetod, mille puhul ostuhinna muutumisel lao väljaminekute kulud ei muutu. Erinevus on kapitaliseeritud ja põhineb proportsionaalsel arvutusel. Ülejäänud summa kantakse kuludesse. 

Kui kasutate liikuvat keskmist, ei toetata varude tasakaalustusi ega varude märkimist. Varude sulgemine ei mõjuta liikuval keskmisel põhineva laomudeligrupiga tooteid ja see ei loo kannete vahel tasakaalustusi.

Allpool on toodud eeltingimused, kui kasutate kulumeetodina liikuvat keskmist kulu.

1.  Seadistage lehel **Kauba mudelgrupid** kauba mudeligrupp, mille väljal **Laomudel** on valitud suvand Liikuv keskmine. **Märkus.** Kui valitud on suvand Liikuv keskmine, on vaikimisi valitud ka väljad **Sisesta füüsilised varud** ja **Sisesta finantsilised varud**. 

2.  Määrake lehel **Sisestamine** vahekaardil **Varud** kontod suvandites **Liikuva keskmise hinnaerinevus** ja **Liikuva keskmise kulu ümberhindamine**. Kui kulu tuleb proportsionaalselt jaotada, kasutage kontot **Liikuva keskmise hinnaerinevus**. Selle põhjuseks on kulude erinevus ostu sissetuleku ja ostuarve vahel ning erinevus algse varude koguse ja praegu laos oleva koguse vahel. Kasutage kontot **Liikuva keskmise kulu ümberhindamine**, kui soovite korrigeerida toote liikuvat keskmist kulu uuele ühikuhinnale.
3.  Määrake lehel **Väljastatud tooted** tootele liikuva keskmise kauba mudeligrupp. **Märkus.** Varude sulgemise protsess suleb ainult arvestusperioodi. See ei mõjuta tooteid, millele on määratud liikuv keskmine kauba mudeligrupina.

## <a name="convert-to-the-moving-average-costing-method"></a>Liikuva keskmise kuluarvestusmeetodile teisendamine
Tooteid saab teisendada liikuva keskmise varude hinnamääramise meetodi kasutamiseks. Seda tüüpi teisendamist tehakse tavaliselt aasta lõpus pärast praeguse aasta viimase kuu sulgemist. Seda tehakse toote praegust kuluarvutusmudelit kasutades. Saate muuta oma varude kuluarvestusmeetodi keskmisel kulul või standardkulul põhinevalt kuluarvutusmeetodilt liikuval keskmisel põhinevale meetodile. 

Kui muudate oma kuluarvestusmeetodi standardselt kuluarvutusmeetodilt liikuva keskmise meetodile, peate täitma järgmised ülesanded.

1.  Varude koguste ja väärtuste korrigeerimine nulli (0).
2.  Kui varude väärtus ja kogus on null (0), muutke kauba mudeligrupp liikuvale keskmisele.
3.  Korrigeerige kogus ja väärtus tagasi varudesse.

Varude kuluarvutusmeetodit ei saa muuta liikuva keskmise meetodilt FIFO-meetodile, LIFO-meetodile ega kaalutud keskmise meetodile.

**Märkus.** Teisendamine standardkulult liikuvale kaalutud keskmisele on käsitsi protsess.

Järgmised näited selgitavad liikuva keskmise kuluarvutusmeetodi kasutamise mõju. Konfiguratsioone on neli.
-   Ostutellimuse ja proportsionaalselt jaotatud kulu erinevus
-   Liikuva keskmise toote ja varude korrrigeerimine
-   Liikuv keskmine koos tootmisega
-   Liikuva keskmise tagasiulatuva kandega

## <a name="purchase-order-and-proportionally-expensed-cost-difference"></a>Ostutellimuse ja proportsionaalselt jaotatud kulu erinevus
Liikuva keskmisega määrab toote kulu ostu sissetulek. Kui pärast ostuarve sisestamist on ostu sissetuleku ja ostuarve kulud erinevad, korrigeeritakse erinevust proportsionaalselt praegu laos olevate toodetega ja kogu ülejäänud summa kajastatakse kuluna. 

Selles näites luuakse ja võetakse ostutellimus vastu ühe kuluga ning ostuarve sisestatakse teise kuluga.

1.  Looge ostutellimus kogusele 2 ühikuhinnaga 10,00.
2.  Looge toote ostu sissetulek.
3.  Looge müügitellimus kogusele 1 ühikuhinnaga 10,00.
4.  Looge ostuarve kogusele 2 ühikuhinnaga 12,00.

Erinevus ühikuhinnas (2,00) sisestatakse ostuarve sisestamisel kontole Liikuva keskmise hinnaerinevus. Selle põhjus on, et tooted osteti hinnaga 20,00. Üks toode müüdi ühikuhinnaga 10,00. Ostuarve sisestati ühikuhinnaga 12.00 ja kogusega 2. Toote ühikuhinnana ei saa sisestada 14.00.

## <a name="moving-average-product-and-inventory-adjustment"></a>Liikuva keskmise toote ja varude korrrigeerimine
Kui teil on vaja korrigeerida toote liikuva keskmise kulu, on varude korrigeerimised lubatud alates tänasest kuupäevast. Toote liikuva keskmise korrigeerimiseks ei saa varude korrigeerimist teha tagasiulatuvalt. Kuluvoogu ei saa olla järjestikuste kannete kaudu. 

Selles näites korrigeeritakse toote liikuva keskmise kulu.

1.  Valige toode, mille puhul soovite liikuva keskmise kulu korrigeerida. **Märkus.** Lehel **Liikuva keskmise ümberhindamine** analüüsitakse toote jaoks saadaolevaid varusid. Valitud toote sisestatud kogus on 1, sisestatud väärtus 12,00, sisestatud ühikuhind 12,00 ja ühikuhind 12,00.
2.  Määrake välja **Ühikuhind** väärtuseks 16,00. Süsteem arvutab ülejäänud väljad.
3.  Korrektsioon on sisestatud.

**Märkus.** Saate korrigeerida ainult liikuva keskmise kulu alates tänasest kuupäevast.

Lehel **Kande tasakaalustamised** näete korrektsiooni 4,00 kontol Liikuva keskmise kulu ümberarvutamine.

## <a name="moving-average-with-production"></a>Liikuv keskmine koos tootmisega
Liikuv keskmine toetab toodetud kaupu. Kui kavatsete kasutada liikuvat keskmist tootmiskeskkonnas, tuleb valida lehel **Tootmise juhtimise parameetrid** liugur **Kasuta eeldatavat omahinda**. See tähendab, et tegeliku koosluse arvutuse omahinna asemel kasutatakse hindamise ajal arvutatud omahinda.

## <a name="moving-average-with-a-backdated-transaction"></a>Liikuva keskmise tagasiulatuva kandega
Tagasiulatuvad kanded määratakse praegusele liikuva keskmise kulule ja toote füüsilist kogust värskendatakse, kuid toote liikuva keskmise kulu see ei mõjuta. Selles liikuva keskmise näites sisestatakse liikuva keskmise toote tagasiulatuv kanne.

1.  Looge liikuva keskmise toote varude korrektsioon koguse 1 ja kulu 20,00 puhul.
2.  Toote varude kannete ajalugu sarnaneb järgmisele.
    -   Laokanne 1, hind 16,00, sisestuskuupäev 15. jaanuar ja kande kuupäev 15. jaanuar.
    -   Varude korrigeerimine 1, hind 20,00, sisestuskuupäev 1. jaanuar ja kande kuupäev 15. jaanuar.
3.  Sisestage korrigeerimine.

Lehel **Laokanded** näete, et kulutatud on 4,00, kuna toote praegune liikuv keskmine on 16,00. Saate sisestada minevikku, kuid kuluerinevus kantakse kuludesse, seega liikuva keskmise kulu see ei mõjuta.

## <a name="inventory-value-report"></a>Laoväärtuse aruanne
Selles liikuva keskmise näites prinditakse varude väärtuse aruanne, et toetada toote praeguse liikuva keskmise arvutamist. Varude väärtuse aruande saate printida kannete kronoloogilises järjestuses koos kuluga, et toetada toote liikuva keskmise kulu arvutamist. Aruandes kuvatakse toote liikuv keskmine kulu. Dialoogiboksis **Varude väärtuse aruanded** võimaldab kuupäevaintervall valida teil aruande sortimise aluseks **Kande kellaaeg** või **Sisestuskuupäev**. Suvand **Sisestuskuupäev** näitab aruande tavalist printimisviisi. Suvand **Kande kellaaeg** on tegelik kuupäev, millal kandest teatatakse ja toote liikuva keskmise kulu värskendatakse. Saate varude väärtuse aruande printida, kasutades suvandit**Kande kellaaja järgi sortimine**, kui soovite näha liikuva keskmise kulu arvutamist aja lõikes. Järgmises tabelis kuvatakse toote kanded, mille kohta aruanne prinditakse, kui kasutatakse suvandit **Kande kellaaja järgi sortimine**.

| Kande aeg | Kuupäev         | Kande tüüp           | Kogus | Summa | Keskmine ühikukulu |
|------------------|--------------|----------------------------|----------|--------|-------------------|
|                  | 1. oktoober    | Algsaldo          | 0        | 0,00   | 0,00              |
| 8. oktoober        | 28. september | Tagasiulatuv sissetulek          | 1        | 16.00  | 16.00             |
| 3. oktoober        | 3. oktoober    | Ostu sissetulek           | 2        | 20,00  | 12.00             |
| 5. oktoober        | 5. oktoober    | Müügitellimus                | –1       | -10,00 | 13.00             |
| 7. oktoober        | 7. oktoober    | Ostuarve           |          | 2.00   | 14.00             |
| 8. oktoober        | 8. oktoober    | Liikuva keskmise ümberhindamine |          | 4,00   | 16.00             |
|                  | 31. oktoober   | Kokku                      | 2        | 32.00  | 16.00             |

 **Märkus.** Pearaamatut ei saa varudega vastavusse viia, kasutades suvandit **Kande kellaaja järgi sortimine**. Aruanne tuleb printida, kasutades suvandit **Sisestuskuupäev**.






