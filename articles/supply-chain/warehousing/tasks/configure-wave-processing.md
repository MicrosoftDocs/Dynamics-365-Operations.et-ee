---
title: Vootöötluse konfigureerimise näide
description: See artikkel annab näite, kuidas seadistada kriteeriumeid, mis määratlevad, milline töö luuakse laole laine töötlemisel ja kas laineid töödeldakse käsitsi või automaatselt.
author: Mirzaab
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSParameters, ProdParameters, whswavetablecreatenew, WHSWaveTable, WHSWaveAttributes, WHSKanbanWaveTable, WHSWaveTableListPage, WHSKanbanWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a9fc2b9f31bc9e2f73b53a900bc9b0924410768
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860344"
---
# <a name="configure-wave-processing-example"></a>Vootöötluse konfigureerimise näide

[!include [banner](../../includes/banner.md)]

See artikkel annab näite, kuidas seadistada kriteeriumeid, mis määratlevad, milline töö luuakse laole laine töötlemisel ja kas laineid töödeldakse käsitsi või automaatselt. Kriteeriumite määramiseks seadistage voomallid ja päringud, mis vastavad müügitellimuste, tootmistellimuste ja kanban-tellimuste väljastatud ridadega voole.

## <a name="enable-sample-data"></a>Luba näidisandmed

Selle stsenaariumi kasutamiseks siin määratud näidiskirjete ja -väärtuste abil, peate kasutama süsteemi, kuhu on installitud standardsed demoandmed. Enne alustamist peate valima ka **USMF-i** juriidilise isiku.

## <a name="example-scenario-configure-wave-processing"></a>Näidisstsenaarium: vootöötluse konfigureerimine

Selles näites stsenaarium sisaldab mitmeid eri sätteid, mis mõjutavad voogude loomist, täitmist, töötlemist ja väljaandmist.

1. Avage **Navigeerimispaan > Moodulid > Laohaldus > Häälestus > Vood > Voo mallid**.
1. Valige suvand **Uus**.
1. Sisestage väärtus väljale **Voomalli nimi**. Kui seadistate voomalli, määrate järjekorra, milles malle vastendatakse väljastatud ridadega müügitellimuste, tootmistellimuste või kanbanide puhul. Kui rida väljastatakse lattu või tootmisse, kasutab see esimese voo malli, mille kriteeriumidele see vastab. Soovitame loendi algusesse panna kõige konkreetsemate kriteeriumidega malli. Mida laiemad on kriteeriumid, seda suurema tõenäosusega täidab rida kriteeriume ja see võib põhjustada ridade määramist valele voole.  
1. Sisestage väärtus väljale **Voomalli kirjeldus**.
1. Sisestage või valige väärtus väljale **Sait**. Kui te kasutate USMF-i, saate valida saidi 2.  
1. Sisestage või valige väärtus väljale **Ladu**. Kui kasutate USMF-i, saate valida lao 24.  
1. Määrake välja **Automatiseeri voo loomine** väärtuseks **Jah**. Selle suvandi valimisel luuakse voog automaatselt, kui ostutellimus, tootmistellimus või kanban väljastatakse lattu.  
1. Määrake suvandi **Töötle voogu lattu vabastamisel** väärtuseks **Jah**. Valige see suvand voo automaatseks töötlemiseks ja töö loomiseks, kui rida väljastatakse lattu.  
1. Määrake välja **Automaatne laine loomine** väärtuseks **Jah**. Selle suvandi valimisel väljastatakse voog automaatselt. Luuakse komplekteerimistöö ja muudetakse see mobiilsetel seadmetel kättesaadavaks.  
1. Määrake välja **Määra avatud voogudele suvand** väärtuseks **Jah**. Read määratakse voogudele voomalli päringufiltri põhjal.  
1. Määrake suvandi **Töötle voogu lävele jõudes automaatselt** väärtuseks **Jah**. Selle suvandi valimisel töödeldakse voogu automaatselt, kui selle väärtused jõuavad väljagrupil **Vooläved** määratud kaalu, saadetise ja ridade läveni. See suvand on saadaval vaid siis, kui väljal **Voo mall** on valitud **Lähetamine**.  
1. Määrake suvandi **Automatiseeri täiendustöö väljastamine** väärtuseks **Jah**. Valige see suvand nõudlusel põhineva täiendustöö loomiseks ja selle automaatseks väljastamiseks. Selleks peab voomallile lisama täiendusvoo meetodi ja looma täiendamismalli tüübiga **Voo nõue**.  
1. Voo atribuutide kasutage **vaikeväärtuste** failigrupi sätteid. Voo atribuudid toimivad nagu filtrid, et piirata seda tüüpi kaupu, mis saavad voogu kasutada. Näiteks saate määrata kaubagrupi.  
1. Laiendage jaotist **Meetodid** ja seadke voomallis läbitud toimingud. Voomalli meetodid võimaldavad teil juhtida, millises järjekorras töödeldava voo tegevusi tehakse. Näiteks võib teil olla meetod voo täiendamiseks. Meetodi lisamisel viiakse see automaatselt etappide järjekorras õigesse asukohta. Kui olete määranud suvandi **Automatiseeri täiendustöö väljastamine** olekuks **Jah**, peate lisama siia täiendamismeetodi.  
1. Valige käsk **Salvesta**.
1. Sulgege leht.
1. Avage **Laohaldus > Seadistus > Laohalduse parameetrid**.
1. Laiendage jaotist **Voo töötlemine.**
1. Sisestage või valige väärtus väljal **Voo töötlemise partii rühm**.
1. Määrake suvandi **Töötle vooge pakktöötlusega** väärtuseks **Jah**.
1. Sisestage number väljale **Oota lukustust (ms)**. Sisestage aeg (millisekundites), mille jooksul ootab eraldamise etapp süsteemiressurssi, mille on lukustanud muu eraldamise etapp. Kui aeg ületatakse, siis voogu ei töödelda ja kuvatakse tõrketeade.  
1. Valige käsk **Salvesta**.
1. Sulgege leht.
1. Avage **Navigeerimispaan > Moodulid > Tootekontroll > Häälestus > Toote kontrolli parameetrid**.
1. Valige suvand väljal **Lattu väljastamine**.

    Müügitellimuste ja kanban-tellimuste puhul tuleb varud reserveerida enne tellimuse väljastamist lattu. Vastasel korral ei saa kaupu ega eraldamisridu voos töödelda. Tootmistellimuste puhul saate valida ka suvandi **Luba osaline reserveerimine**. Näiteks on see kasulik, kui teil on olemas tootmise alustamiseks vajalikud materjalid ja on võimalik oodata, kuni täiendavad materjalid kättesaadavaks muutuvad, et protsess lõpule viia. Kui valite selle suvandi, peate lattu väljastamise protsessi käsitsi kordama, kui täiendavad materjalid kättesaadavaks muutuvad.
1. Sulgege leht.

## <a name="additional-resources"></a>Lisaressursid

- [Voo loomine ja töötlemine](../wave-processing.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
