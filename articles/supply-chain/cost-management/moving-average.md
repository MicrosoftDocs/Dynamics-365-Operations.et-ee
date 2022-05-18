---
title: Liikuv keskmine
description: Liikuv keskmine on pidev keskmise põhimõttel tuginev kuluarvestusmeetod, mille puhul ostuhinna muutumisel lao väljaminekute kulud ei muutu. Erinevus on kapitaliseeritud ja põhineb proportsionaalsel arvutusel. Ülejäänud summa kantakse kuludesse.
author: JennySong-SH
ms.date: 08/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 65531
ms.assetid: dfd10099-8f7f-44b1-917e-df37c2fe8773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0be72c8ba3c123300be83513531d2f805dc8f5e3
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676099"
---
# <a name="moving-average"></a>Liikuv keskmine

[!include [banner](../includes/banner.md)]

Liikuv keskmine on pidev keskmise põhimõttel tuginev kuluarvestusmeetod, mille puhul ostuhinna muutumisel lao väljaminekute kulud ei muutu. Erinevus on kapitaliseeritud ja põhineb proportsionaalsel arvutusel. Ülejäänud summa kantakse kuludesse.

Kui kasutate liikuvat keskmist, ei toetata varude tasakaalustusi ega varude märkimist. Varude sulgemine ei mõjuta liikuval keskmisel põhineva laomudeligrupiga tooteid ja see ei loo kannete vahel tasakaalustusi.

Allpool on toodud eeltingimused, kui kasutate kulumeetodina liikuvat keskmist kulu.

1. Seadistage lehel **Kauba mudelgrupid** kauba mudeligrupp, mille väljal **Laomudel** on valitud suvand **Libisev keskmine**.

    > [!NOTE]
    > Kui valitud on suvand **Libisev keskmine**, on vaikimisi valitud ka väljad **Sisesta füüsilised varud** ja **Sisesta finantsilised varud**.

1. Määrake lehel **Sisestamine** kontod suvandi **Libiseva keskmise hinnaerinevus** jaoks. Kui kulu tuleb proportsionaalselt jaotada, kasutage kontot **Libiseva keskmise hinnaerinevus**. See toimub järgmise kahe stsenaariumi korral.
    - Esineb kulude erinevus ostu sissetuleku ja ostuarve vahel ning erinevus algse varude koguse ja praegu laos oleva koguse vahel.
    - Kanded suurendavad lao negatiivse väärtuse nulliks ning kandekulu ja praeguse keskmise libiseva kulu väärtused erinevad.

1. Määrake lehe **Sisestamine** vahekaardil **Varud** kontod suvandi **Libiseva keskmise kulu ümberarvutamine** jaoks. Kui soovite korrigeerida toote libisevat keskmist kulu uue ühiku hinnaga, kasutage kontot **Libiseva keskmise kulu ümberarvutamine**.

1. Määrake lehel **Väljastatud tooted** tootele libiseva keskmise kauba mudeligrupp.

    > [!NOTE]
    > Varude sulgemise protsess suleb ainult arvestusperioodi. See ei mõjuta tooteid, millele on määratud liikuv keskmine kauba mudeligrupina.

## <a name="convert-to-the-moving-average-costing-method"></a>Liikuva keskmise kuluarvestusmeetodile teisendamine

Tooteid saab teisendada liikuva keskmise varude hinnamääramise meetodi kasutamiseks. Seda tüüpi teisendamist tehakse tavaliselt aasta lõpus pärast praeguse aasta viimase kuu sulgemist. Seda tehakse toote praegust kuluarvutusmudelit kasutades. Saate muuta oma varude kuluarvestusmeetodi keskmisel kulul või standardkulul põhinevalt kuluarvutusmeetodilt liikuval keskmisel põhinevale meetodile.

Kui muudate oma kuluarvestusmeetodi standardselt kuluarvutusmeetodilt liikuva keskmise meetodile, peate täitma järgmised ülesanded.

1. Varude koguste ja väärtuste korrigeerimine nulli (0).
1. Kui varude väärtus ja kogus on null (0), muutke kauba mudeligrupp liikuvale keskmisele.
1. Korrigeerige kogus ja väärtus tagasi varudesse.

Varude kuluarvutusmeetodit ei saa muuta liikuva keskmise meetodilt FIFO-meetodile, LIFO-meetodile ega kaalutud keskmise meetodile.

> [!NOTE]
> Teisendamine standardkulult libisevale kaalutud keskmisele on käsitsi protsess.

Järgmised näited selgitavad liikuva keskmise kuluarvutusmeetodi kasutamise mõju. Konfiguratsioone on neli.

- Ostutellimuse ja proportsionaalselt jaotatud kulu erinevus
- Liikuva keskmise toote ja varude korrrigeerimine
- Liikuv keskmine koos tootmisega
- Liikuva keskmise tagasiulatuva kandega

## <a name="purchase-order-and-proportionally-expensed-cost-difference"></a>Ostutellimuse ja proportsionaalselt jaotatud kulu erinevus

Liikuva keskmisega määrab toote kulu ostu sissetulek. Kui pärast ostuarve sisestamist on ostu sissetuleku ja ostuarve kulud erinevad, korrigeeritakse erinevust proportsionaalselt praegu laos olevate toodetega ja kogu ülejäänud summa kajastatakse kuluna.

Selles näites luuakse ja võetakse ostutellimus vastu ühe kuluga ning ostuarve sisestatakse teise kuluga.

1. Looge ostutellimus kogusele 2 ühikuhinnaga 10,00.
1. Looge toote ostu sissetulek.
1. Looge müügitellimus kogusele 1 ühikuhinnaga 10,00.
1. Looge ostuarve kogusele 2 ühikuhinnaga 12,00.

Erinevus ühikuhinnas (2,00) sisestatakse ostuarve sisestamisel kontole Liikuva keskmise hinnaerinevus. Selle põhjus on, et tooted osteti hinnaga 20,00. Üks toode müüdi ühikuhinnaga 10,00. Ostuarve sisestati ühikuhinnaga 12.00 ja kogusega 2. Toote ühikuhinnana ei saa sisestada 14.00.

## <a name="moving-average-product-and-inventory-adjustment"></a>Liikuva keskmise toote ja varude korrrigeerimine

Kui teil on vaja korrigeerida toote liikuva keskmise kulu, on varude korrigeerimised lubatud alates tänasest kuupäevast. Toote liikuva keskmise korrigeerimiseks ei saa varude korrigeerimist teha tagasiulatuvalt. Kuluvoogu ei saa olla järjestikuste kannete kaudu.

Selles näites korrigeeritakse toote liikuva keskmise kulu.

1. Valige toode, mille puhul soovite liikuva keskmise kulu korrigeerida. 

 > [!NOTE]
 > Lehel **Libiseva keskmise ümberhindamine** analüüsitakse toote jaoks saadaolevaid varusid. Valitud toote sisestatud kogus on 1, sisestatud väärtus 12,00, sisestatud ühikuhind 12,00 ja ühikuhind 12,00.
    
1. Määrake välja **Ühikuhind** väärtuseks 16,00. Süsteem arvutab ülejäänud väljad.
1. Korrektsioon on sisestatud.

> [!NOTE]
> Saate korrigeerida ainult libiseva keskmise kulu alates tänasest kuupäevast.

Lehel **Kande tasakaalustamised** näete korrektsiooni 4,00 kontol Libiseva keskmise kulu ümberarvutamine.

## <a name="moving-average-with-production"></a>Liikuv keskmine koos tootmisega

Liikuv keskmine toetab toodetud kaupu. Kui kavatsete kasutada libisevat keskmist tootmiskeskkonnas, tuleb valida lehel **Tootmise juhtimise parameetrid** liugur **Kasuta eeldatavat omahinda**. See tähendab, et tegeliku koosluse arvutuse omahinna asemel kasutatakse hindamise ajal arvutatud omahinda.

## <a name="moving-average-with-a-backdated-transaction"></a>Liikuva keskmise tagasiulatuva kandega

Tagasiulatuvad kanded määratakse praegusele liikuva keskmise kulule ja toote füüsilist kogust värskendatakse, kuid toote liikuva keskmise kulu see ei mõjuta. Selles liikuva keskmise näites sisestatakse liikuva keskmise toote tagasiulatuv kanne.

1. Looge liikuva keskmise toote varude korrektsioon koguse 1 ja kulu 20,00 puhul.
1. Toote varude kannete ajalugu sarnaneb järgmisele.
    - Laokanne 1, hind 16,00, sisestuskuupäev 15. jaanuar ja kande kuupäev 15. jaanuar.
    - Varude korrigeerimine 1, hind 20,00, sisestuskuupäev 1. jaanuar ja kande kuupäev 15. jaanuar.
1. Sisestage korrigeerimine.

Lehel **Laokanded** näete, et kulutatud on 4,00, kuna toote praegune libisev keskmine on 16,00. Saate sisestada minevikku, kuid kuluerinevus kantakse kuludesse, seega liikuva keskmise kulu see ei mõjuta.

## <a name="negative-inventory-balances"></a>Negatiivsed varu saldod

Kandeid käsitletakse erinevalt sõltuvalt sellest, kas uus laos olev kogus pärast kannet on negatiivne, null või positiivne.

### <a name="new-balance-is-negative-or-zero"></a>Uus saldo on negatiivne või null

Kui uus laos olev kogus on negatiivne või null, arvutatakse kanne praeguste keskmiste kulude alusel. Kui ostuhinna ja praeguste keskmiste kulude vahel on erinevus, sisestatakse see väljale **Libiseva keskmise hinnaerinevus**.

### <a name="new-balance-is-positive"></a>Uus saldo on positiivne

Kui uus laos olev kogus on pärast kannet positiivne, tükeldatakse kanne kaheks osaks ja arvutatakse erinevalt, nagu on kokku võetud järgmises tabelis.

| Osa | Kirjeldus |
|---|---|
| Kogus negatiivsest nulli | Laoseis kasutab kauba praegust libisevat keskmist kulu, mitte sissetuleku koguse selle osa kandekulu, mis suurendab vaba saldot negatiivsest nulliks. Kandekulu ja praeguse keskmise libiseva kulu vaheline erinevus sisestatakse väljale **Libiseva keskmise hinnaerinevus**. |
| Kogus nullist positiivseks | Laoseis kasutab sissetuleku koguse selle osa kandekulu, mis suurendab vaba saldot nullist positiivseks.                                                  |

## <a name="inventory-value-report"></a>Laoväärtuse aruanne

Selles liikuva keskmise näites prinditakse varude väärtuse aruanne, et toetada toote praeguse liikuva keskmise arvutamist. Varude väärtuse aruande saate printida kannete kronoloogilises järjestuses koos kuluga, et toetada toote liikuva keskmise kulu arvutamist. Aruandes kuvatakse toote liikuv keskmine kulu. Dialoogiboksis **Varude väärtuse aruanded** võimaldab kuupäevaintervall valida teil aruande sortimise aluseks suvandi **Kande kellaaeg** või **Sisestuskuupäev**. Suvand **Sisestuskuupäev** näitab aruande tavalist printimisviisi. Suvand **Kande kellaaeg** on tegelik kuupäev, millal kandest teatatakse ja toote liikuva keskmise kulu värskendatakse. Saate varude väärtuse aruande printida, kasutades suvandit **Kande kellaaja järgi sortimine**, kui soovite näha liikuva keskmise kulu arvutamist aja lõikes. Järgmises tabelis kuvatakse toote kanded, mille kohta aruanne prinditakse, kui kasutatakse suvandit **Kande kellaaja järgi sortimine**.

| Kande aeg | Kuupäev         | Kande tüüp           | Kogus | Summa | Keskmine ühikukulu |
|------------------|--------------|----------------------------|----------|--------|-------------------|
|                  | 1. oktoober    | Algsaldo          | 0        | 0,00   | 0,00              |
| 8. oktoober        | 28. september | Tagasiulatuv sissetulek          | 1        | 16.00  | 16.00             |
| 3. oktoober        | 3. oktoober    | Ostu sissetulek           | 2        | 20,00  | 12.00             |
| 5. oktoober        | 5. oktoober    | Müügitellimus                | –1       | -10,00 | 13.00             |
| 7. oktoober        | 7. oktoober    | Ostuarve           |          | 2.00   | 14.00             |
| 8. oktoober        | 8. oktoober    | Liikuva keskmise ümberhindamine |          | 4.00   | 16.00             |
|                  | 31. oktoober   | Kokku                      | 2        | 32.00  | 16.00             |

> [!NOTE]
> Pearaamatut ei saa varudega vastavusse viia, kasutades suvandit **Kande kellaaja järgi sortimine**. Aruanne tuleb printida, kasutades suvandit **Sisestuskuupäev**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]