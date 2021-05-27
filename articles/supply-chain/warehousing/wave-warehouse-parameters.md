---
title: Voo töötlemise laoparameetrid
description: Teemas kirjeldatakse, kuidas häälestada lao parameetreid voo töötlemiseks. Voo töötlus võimaldab teil rühmitada mitme töötellimuse komplekteerimistöö üheks vooks.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: b120c24ad3289f5f46119d70c8cb7124546e41b1
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019174"
---
# <a name="warehouse-parameters-for-wave-processing"></a>Voo töötlemise laoparameetrid

[!include [banner](../includes/banner.md)]

Teemas kirjeldatakse, kuidas häälestada lao parameetreid voo töötlemiseks. Voo töötlus võimaldab teil rühmitada mitme töötellimuse komplekteerimistöö üheks vooks.

Voo töötlemise kasutamiseks määrake lehel **Laohalduse parameetrid** järgmised parameetrid.

- Voogude töötlemine pakett-tööna.
- Voogude töötlemise teabe kogumine logifaili.

## <a name="set-up-warehouse-management-parameters-for-wave-processing"></a>Voo töötluse jaoks laohalduse parameetrite häälestamine

Voo töötluse jaoks lao parameetrite häälestamiseks tehke järgmist.

1. Avage **Laohaldus** \> **Seadistus** \> **Laohalduse parameetrid**.

1. Looge kiirkaardil **Voo töötlemine** järgmised sätted.

    - **Voo töötlemise partiigrupp** - valige partiitööde grupp, mida kasutada voogude töötlemiseks partiitöödena. Pakett-tööde grupp määrab serveri, milles pakett-töid käitatakse.
    - **Voogude töötlemine partiina** – valige, kas lubada voogude automaatne töötlemine partiitööna. Paralleeltöötluse kasutamiseks peate selle määrama väärtusele *Jah*. Partiitööd saab häälestada lehel **Voogude käitlemine**. (Vt ka selle loendi lõpus märget.)
    - **Voo progressilogi loomine**- valige, kas süsteem peaks looma logikirje iga kord, kui kauba eraldamine ja selle dimensioonid algavad ja lõppevad. Lubage see logi ainult siis, kui vajate seda nt algsel testimisel või tõrkeotsingul. Lisateavet vt teemast [Vooetapi eraldamine](wave-allocation-method.md).
    - **Voo töötlemise ajaloo logi loomine** - valige, kas salvestada automaatselt teavet voo kohta logifaili pärast voo töötlemist, kaasa arvatud ootel eralduste paralleeltöötluse ajal. Tavaliselt peaksite selle lubama ainult tõrkeotsingu ajal, kuna see lisab täiendavat üldkulu. Logi vaatamiseks minge **Laohaldus \> Väljaminevate vood \> Voo töötluse ajaloo logi**. Lisateavet voo töötlemise kohta leiate jaotisest [Voo loomine ja töötlemine](wave-processing.md).
    - **Konteinerite loomise ajaloo logi loomine** – valige, kas salvestada konteinerite loomise voo teave logifaili pärast voo töötlemist automaatselt. Logi vaatamiseks minge **Laohaldus \> Pakendamine ja konteinerite loomine \> Konteinerite loomise ajalugu**.
    - **Lukustuse ooteaeg (ms)** - sisestage aeg (millisekundites), mille jooksul ootab eraldamise etapp süsteemiressurssi, mille on lukustanud muu eraldamise etapp. Kui aeg ületatakse, siis voogu ei töödelda ja kuvatakse tõrketeade.

1. Tehke kiirkaardil **Lattu väljaandmine** järgmine säte.

    - **Tõrge partii nurjumisel** – valige, kas luua tõrge lao partiitöö nurjumisel. Kui see on lubatud, lõpevad nurjunud tööd olekuga *Tõrge*. Kui see on keelatud, lõpevad nurjunud tööd olekuga *Lõpetatud*.

> [!NOTE]
> Voo töötlemiseks kasutataval voomallil saate määrata voo töötluse automatiseerimissätted. Kui häälestate pakett-töö graafiku, tuleb teil koordineerida ajastus voomalli automatiseerimise sätetega. Lisateavet vt teemast [Voomalli loomine](wave-templates.md).
>
> Kui kasutate sätteid *Transpordihaldus* ja *Täpsem laohaldus*, saate määrata, kas koormad konsolideeritakse voo töötlemisel. See on kasulik näiteks juhul, kui korraga saab lähetada mitu väikest koormat. Koormate konsolideerimiseks voo töötlemise ajal märkige vahekaardil **Koormad** ruut **Konsolideeri koormad voo töötlemise ajal**.</P>

## <a name="set-up-full-or-partial-reservation-for-production-waves"></a>Tootmisvoogude täieliku või osalise reserveerimise häälestamine

Müügitellimuste ja kanban-tellimuste puhul tuleb varud reserveerida enne tellimuse väljastamist lattu. Vastasel korral ei saa kaupu ega eraldamisridu voos töödelda. Tootmistellimused on siiski veidi paindlikumad. Tootmistellimuste puhul saate määrata järgmist.

- Lubage tootmistellimuste väljastamine lattu, kuigi kõiki materjale ei saa reserveerida. Kui valite selle suvandi, peate lattu väljastamise protsessi käsitsi kordama, kui täiendavad materjalid kättesaadavaks muutuvad. Näiteks on see kasulik, kui teil on olemas tootmise alustamiseks vajalikud materjalid ja on võimalik oodata, kuni täiendavad materjalid kättesaadavaks muutuvad.
- Nõudke kõikide materjalide reserveerimist enne tellimuse lattu väljastamist.

Täieliku reserveerimise nõudmiseks või osalise reserveerimise lubamiseks tehke järgmist.

1. Avage **Tootmise juhtimine** \> **Seadistus** \> **Tootmise juhtimise parameetrid**.
1. Valige vaikesäte vahekaardi **Üldine** väljal **Lattu väljaandmine**.
