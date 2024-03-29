---
title: Laovarude ajapiirid
description: See artikkel kirjeldab, kuidas seadistada laovarude ajapiire. Laovarude ajapiir näitab teie plaaniperioodi ja limiiti.
author: t-benebo
ms.date: 01/18/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2021-01-18
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 987dea4c1b693fc1bb687f97d51288d5e51e7d4c
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740109"
---
# <a name="coverage-time-fences"></a>Laovarude ajapiirid

[!include [banner](../../includes/banner.md)]

See artikkel kirjeldab, kuidas seadistada laovarude *ajapiire*. Plaanijad saavad määraa plaaniperioodi (laovarude ajapiiri päevades) ning välistada pakkumise ja nõudluse, mis jääb sellest väljapoole. Seega aitavad laovarude ajapiirid ennetada nn müra, mida põhjustavad tarnesoovitused, millele te ei pea kuude kaupa reageerima. Näited hõlmavad järgmise aasta prognoosi ja klienditellimusi, mis esitatakse kaugelt üle tavalise täitmisaja.

Laovarude ajapiir on päevade arv pärast tänast kuupäeva (või täpsemalt kuupäeva, millal planeerimise käitate), mil pakkumine ja jõydlus on välja jäetud. Viivituste vältimiseks peate tagama, et laovarude ajapiir on pikem kui täitmisaeg kokku. Süsteemi vaikeväärtus on 100 päeva.

Laovarude ajapiiri saate määrata kõigil järgmistel tasemetel.

- **Laovarude grupp** – saate määrata laovarude ajapiiri vaikeväärtuse igale laovarude grupile.
- **Kauba laovarud** – saate alistada kaubale määratud laovarude grupist päritud laovarude ajapiiri.
- **Koondplaan** – saate alistada laovarude grupist ja eseme laovarude sätetest päritud laovarude ajapiirid.

Järgmistes jaotistes selgitatakse, kuidas määratleda laovarude gruppi igal tasandil.

## <a name="set-a-coverage-time-fence-for-a-coverage-group"></a>Laovarude grupile laovarude ajapiiri määramine

Kui määrate laovarude grupile laovarude ajapiiri, rakendub säte kõigile kaupadele (toodetele), mis kuuluvad sellesse gruppi. Samas saate konkreetsete üksuste ja konkreetsete koondplaanide sätte alisatada.

Laovarude grupi laovarude ajapiiri määramiseks tehke järgmist.

1. Valige **Koondplaneerimine \> Seadistus \> Laovarud \> Laovarude grupid**.
1. Valige loenist olemasolev laovarude grupp või looge uus laovarude grupp.
1. Kiirkaardil **Üldine** määrake väli **Laovarude ajapiir (päevad)** päevade arvule, mida soovite laovarude grupi laovarude ajapiirina kasutada.

## <a name="set-a-coverage-time-fence-for-a-specific-item"></a>Konkreetsele kaubale laovarude ajapiiri määramine

Iga üksus (toode) kuulub laovarude rühma. Kui kaubale ei ole eraldi laovarude rühma määratud, kohaldub laovarude vaikerühm. Iga kaup pärib oma laovarude rühmalt laovarude ajapiiri. Samas saate selle ajapiiri vastavalt vajadusele konkreetsete kaupade jaoks alistada.

Konkreetse kauba laovarude ajapiiri määramiseks tehke järgmist.

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Valige ruudustikus toode.
1. Toimingupaani vahekaardil **Plaan** rühmas **Laovarud** valige suvand **Kauba laovarud**.
1. Lehel **Kauba laovarud** vahekaardil **Ülevaade** valige või looge rida saidi jaoks, kus soovite laovarude ajapiiri määrata.
1. Valige vahekaart **Üldine**, et avada valitud saidi sätted.
1. Valige märkeruut **Tühista laovarude rühma sätted**.
1. Määrake väli **Laovarude ajapiir (päevad)** päevade arvule, mida soovite kauba laovarude ajapiirina kasutada.

## <a name="set-a-coverage-time-fence-for-a-specific-master-plan"></a>Konkreetsele koondplaanile laovarude ajapiiri määramine

Saate määrata laovarude ajapiiri koondplaani tasemel. Nii saate määrata päevade arvu, mil koondplaneerimise arvutus koonplaani katab. See säte alistab kõik laovarude ajasätted, mis on määratletud iga vastava kauba ja laovarude grupi jaoks.

Konkreetse koondplaani laovarude ajapiiri määramiseks tehke järgmist.

1. Avage **Koondplaneerimine \> Seadistus \> Plaanid \> Koondplaanid**.
1. Valige loendist olemasolev koondplaan või looge uus.
1. Määrake kiirkaardil **Ajapiirid päevades** suvand **Laovarud** valikule *Jah*. Seejärel sisestage suvandi all olevale väljale päevade arv, mida soovite koondplaani laovarude ajapiirina kasutada.

## <a name="considerations-for-coverage-time-fences"></a>Laovarude ajapiiride kaalutlused

Laovarude ajapiiride häälestamisel arvestage järgmiste punktidega.

- Laovarude ajapiirid mõjutavad ainult koondplaneerimise sisendandmeid. Viivituste ilmnemisel võib tulemuseks saadud plaanitud tellimustel olla kuupäev, mis on pärast tänast kuupäeva pluss laovarude ajapiir.
- Laovarude ajapiirid määratakse kalendripäevades. Tööpäevi kasutavad kalendrid ei mõjuta ajapiiri arvutamist. Näiteks loetakse nädalat alati seitsmest päevast koosnevaks, isegi kui nädalavahetused on tööajakalendris häälestatud suletud päevadena.
- Nõude kanded ei looda ühegi pakkumise ega nõudluse jaoks, mis langeb laovarude ajapiirist väljapoole.
- Kui mõni kinnitatud pakkumine ja nõudlus langeb laovarude ajapiirist väljapoole, siis seda mootorisse ei laadita. Seega ei käivita see ühtegi täiendamist ja viivitusi ei arvestata. Sellest hoolimata ei tohiks seda pakkumist ja nõudlust süsteemist eemaldada.
- Minimaalse laokoguse variatsioone (miinimumkoefitsiendist) eiratakse, kui need jäävad väljapoole laovarude ajapiiri.
- Kontsernisisest nõudlust eiratakse, kui arvutatud taotletud lähetuskuupäev ei jää laovarude ajapiiri sisse. Pidage meeles, et taunitud koondplaneerimise mootori puhul ei piira kontsernisisest nõudlust laovarude ajapiir.
- Nõudluse prognoose eiratakse, kui eelarvekuupäev ei ole laovarude ajapiiri sees. Pidage meeles, et taunitud koondplaneerimise mootori puhul ei ole nõudluse prognoosid laovarude ajapiiriga piiratud.
- Planeerimise optimeerimine arvestab ajavööndiga. See arvestab pakkumise ja nõudluse saitid ajavööndiga ning planeerimise käitamise ajaga. Näiteks käivitatakse koondplaneerimine 15. oktoobril kell 11 Taani saidilt (ajavööd GMT +1) ja kasutatakse kümnepäevast laovarude ajapiiri. Sel juhul kaasatakse pakkumise ja nõudluse nõue saidilt Seattle’is (ajavöönd GMT –8) kuni kl 14.00 25. oktoobrini (= kümme 24-tunnist päeva pärast koondplaneerimise käivitamist, miinus ajavööndi erinevus üheksa tundi). Pidage meeles, et taunitud koondplaneerimise mootor võtab arvesse ainult ajapiiri kuupäeva. Seega võivad tulemused erineda.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]