---
title: Mõõtühik ja ladustamispoliitikad
description: Selles artiklis kirjeldatakse, kuidas kasutada laoprotsessides vaikeühikuid, ühikuseeriaid ja ühikuteisendusi.
author: perlynne
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetails, EcoResProductDetailsExtended, EcoResStorageDimensionGroup, InventItemOrderSetup, UnitOfMeasureConversion, WHSRFMenuItem, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 29611
ms.assetid: 4b5ca875-9a06-416d-9ac0-cc3ab8f7338e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca1c18a293d66ab78f41cac857461249826ce4c9
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069118"
---
# <a name="unit-of-measure-and-stocking-policies"></a>Mõõtühik ja ladustamispoliitikad

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse, kuidas kasutada laoprotsessides vaikeühikuid, ühikuseeriaid ja ühikuteisendusi.

Ühiku seeriagrupid määratlevad laotoimingutes kasutatavate ühikute järjestuse. Need luuakse lehel **Ühiku seeriagrupid**. Järjestus näitab seost erinevate ühikute vahel. Näiteks saate hoiundada kaubaaluseid, mis sisaldavad üksikuid kaupu sisaldavaid kaste. Sellisel juhul peate sisestama kolm erinevat ühikut ja kihtide loogilise järjestuse. Ühiku seeriagrupid võimaldavad määratleda litsentsiplaatide grupeerimise poliitikad ja vaikeühikud, mida tuleks erinevate laoprotsesside puhul kasutada. See artikkel kehtib nii laohaldusprotsesside (WMS) puhul, mis on saadaval laohalduse moodulis, kui ka laohalduse moodulis saadaolevale baaslaolahendustele.

## <a name="unit-sequence-groups-for-released-products"></a>Väljastatud toodete ühiku seeriagrupid
Kui soovite kasutada väljastatud tooteid lao tööprotsessides, tuleb neile määrata seeriagrupp. Kui kinnitate toote, mis on seotud laoala dimensioonigrupiga, ja laoala dimensioonigrupi suvandi **Kasuta laohaldusprotsesse** sätteks on valitud **Jah**, kuvatakse tõrketeade, kui toote kohta pole määratletud ühiku seeriagrupi ID-d. Kui kasutatavad ühiku seeriagrupid sisaldavad mitut rida (ja seega mitut ühikut), peate ühikute vahel ühiku teisendamise seadistamise valima. Viige see seadistus lehel **Ühiku teisendused** lõpule. Seeriagrupi väikseim ühik, mille väljastatud tootega seostate, peab ühtima vastava toote jaoks määratletud varude ühikuga. Laoühik on vaba kaubavaru põhiarvutusteks kasutatav ühik. Saate ka seadistada mõõtühikute teisendused tooteetalonide tootevariantide kohta, kasutades suvandit **Luba mõõtühikute teisendused**.

## <a name="license-plate-grouping"></a>Litsentsiplaadi rühmitamine
Saate määrata, kas vähem või rohkem kui kindla ühikuga sissetulekud rühmitatakse ühele litsentsiplaadile või luuakse iga ühiku kohta eraldi litsentsiplaat. Selle seadistamiseks kasutage lehe **Ühiku seeriagrupid** vahekaardi **Rea üksikasjad** suvandit **Litsentsiplaadi rühmitamine**. Kui soovite kasutada litsentsiplaadi rühmitamist mobiilses seadmes töödeldava töö puhul, peate menüüelemendis **Mobiilne seade** valima suvandi **Litsentsiplaadi rühmitamine**. Näiteks registreerite mobiilse seadme abil kauba, mis on seostatud ühiku seeriagrupiga, millel on kaks rida. Esimene rida on mõeldud tükkide jaoks ja suvandi **Litsentsiplaadi rühmitamine** sätteks on valitud **Jah**. Teine rida on mõeldud kaubaaluste ühiku jaoks ja suvandi **Litsentsiplaadi rühmitamine** sätteks on valitud **Ei**. Sellisel juhul saab süsteem automaatselt tükelduse teha ja luua litsentsiplaadid iga 100 tüki kohta.

## <a name="units-for-cycle-counting"></a>Tsüklilise inventuuri ühikud
Selleks et määratleda, millised ühikuid tuleks tsüklilise inventuuri protsesside osana kasutada, valige lehel **Ühiku seeriagrupid** suvand **Kasuta ühikut tsükliliseks inventuuriks**. Saate seeriagrupis valida kuni neli ühikut. Kui valite rohkem kui neli ühikut, ei kuvata lisaühikuid mobiilses seadmes.

## <a name="default-units-for-mobile-device-receiving-processes"></a>Mobiilse seadme vastuvõtuprotsesside vaikeühikud
Selleks et määrata mobiilses seadmes vastuvõtuprotsesside jaoks kasutatavad vaikeühikud, lubage lehel **Ühiku seeriagrupid** suvandid **Ostu ja üleviimise vaikeühik** ja **Tootmise vaikeühik**. Näiteks saate määrata, et vaikimisi peaks süsteem kasutama kaubaaluse koguseid, kui mobiilse seadme abil võetakse vastu ostutellimuse vaba laovaru, kuid varude arvestusühik peaks olema Tükid. Igal kaubaalusel olevate tükkide arvu teisenduseks peate määratlema ühikuteisenduse, nt 100 tk = 1 kaubaalus.

## <a name="default-order-settings"></a>Tellimuse vaikesätted
Väljastatud toodete loomise osana peate valima vaikeühikud ostude, müükide ja varude jaoks, et töödelda erinevaid tellimusi. Saate määrata erinevate lähtedokumentide vaikeühikud ja -kogused lehtedel **Tellimuse vaikesätted** ja **Tellimuse tegevuskohapõhised sätted** pages. Pääsete neile lehtedele juurde lehelt **Väljastatud tooted**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]