---
title: Kliendimaksete prognooside kasutamine (eelvaade)
description: See teema selgitab eeltingimusi ja üldisi samme, mis on vajalikud Finance'i ülevaadete prooviversiooni kasutamiseks.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-11-16
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 1349521d65511864747de6c2fed3a904dea8917e
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186560"
---
# <a name="use-customer-payment-predictions-preview"></a>Kliendimaksete prognooside kasutamine (eelvaade)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

See teema selgitab, kuidas kasutada kliendimaksete prognoose. Enne selle funktsiooni kasutamist veenduge, et olete lõpetanud selle seadistustoimingud. Lisateabe saamiseks vt [Kliendimaksete prognooside lubamine](enable-cust-paymnt-prediction.md).

Kliendimaksete prognoose näete tööruumis **Klientide krediidi ja võlanõuete haldus** ja kahel uuel loendi lehel - **Makseprognoosid tehingu kohta** ja **Makseprognoosid kliendi kohta**.

### <a name="manage-customer-credit-and-collections-workspace"></a>Klientide krediidi ja võlanõuete halduse tööruum

Tööruum **Klientide krediidi ja võlanõuete haldus** sisaldab kahte uut paani, **Makseprognoosid tehingu kohta** ja **Prognoositava kõrge hilinenud saldoga kliendid**.

- Paanil **Makseprognoosid tehingu kohta** kuvatakse avatud klienditehingute arv, mille **tähtaegselt** maksmise tõenäosus, on vähem kui 50 protsenti. Saate valida selle paani, et avada loendi leht **Makseprognoosid tehingu kohta**.
- Paanil **Prognoositava kõrge hilinenud saldoga kliendid** kuvatakse nende klientide arv, kelle puhul prognoositakse, et lõppsaldost rohkem kui pool (50 porotsenti) makstakse hilja ja/või väga hilja. Saate valida selle paani, et avada loendi leht **Makseprognoosid kliendi kohta**.

[![Kliendtide krediidi ja võlanõuete halduse tööruum](./media/manage-customer-credit-collections.png)](./media/manage-customer-credit-collections.png)

### <a name="payment-predictions-per-transaction-list-page"></a>Loendileht Makseprognoosid tehingu kohta

Loendilehel **Makseprognoosid tehingu kohta** saate vaadata avatud tehingute makse tõenäosust vahemikes **Õigeaegne**, **Hilinenud** ja **Väga hilinenud**. Ruudustiku iga kande puhul näitab veerg **Õigeaegsuse tõenäosus** tõenäosust, et arve makstakse tähtaegselt või enne seda. Kui tähtajalise makse tõenäosus on väiksem kui 50 protsenti, kuvatakse veeru **Õigeaegsuse tõenäosus** protsendi kõrval punast ringi, mis näitab hilinenud makse riski.

[![Leht makseprognoosid tehingu kohta](./media/payment-predictions-per-transaction.png)](./media/payment-predictions-per-transaction.png)

Lehe paremas servas asuval paanil **Seotud teave** kuvatakse prognooside kohta rohkem üksikasju.

- Ruudustikus valitud tehingu kohta kuvab kiirkaart **Makseprognoos** makseprognoosi üksikasju vahemikes **Õigeaegne**, **Hilinenud** ja **Väga hilinenud**. Jaotises **Peamised tegurid** kuvatakse peamisi prognoose mõjutanud tegureid. Peamised tegurid on valitud tehingu ja/või selle tehingu kliendi atribuudid.
- Kiirkaardil **Kliendi ülevaated** kuvatakse valitud tehingu praegust kliendi arvet, makset ja võlanõuete statistikat.
- Kiirkaardil **Kliendi ajalugu** kuvatakse kliendi makseajalugu vahemikes **Õigeaegne**, **Hilinenud** ja **Väga hilinenud**.

Andmed jaotises **Peamised tegurid** ning kiirkaartidel **Kliendi ülevaated** ja **Kliendi ajalugu** aitavad makseprognoose selgitada. See võib aidata suurendada teie usaldust prognooside efektiivsuse vastu.

[![Makseprognooside graafilised näidikud seostuva teabe paanil](./media/payment-prediction-gauges.png)](./media/payment-prediction-gauges.png)

### <a name="payment-prediction-per-customer-list-page"></a>Loendileht Makseprognoosid kliendi kohta

Loendilehel **Makseprognoosid kliendi kohta** kuvatakse kogu avatud saldo ja summa, mille maksmist prognoositakse vahemikes **Õigeaegne**, **Hilinenud** ja **Väga hilinenud**.

[![Leht Makseprognoosid kliendi kohta](./media/payment-predictions-per-transaction-02.png)](./media/payment-predictions-per-transaction-02.png)

Iga vahemiku maksesumma arvutatakse tehingu saldo kaalutud keskmise summana. See summa arvutatakse iga vahemiku makse tõenäosuse alusel.

Näiteks on kliendil kolm avatud tehingut, millel on igas vahemikus järgmised makse tõenäosused.

| Kanne | Summa | Õigeaegse makse tõenäosus | Hilinenud makse tõenäosus | Väga hilinenud makse tõenäosus |
|-------------|--------|-----------------------------|--------------------------|-------------------------------|
| T1          | 100    | 10 protsenti                  | 50 protsenti               | 40 protsenti                    |
| T2          | 1000  | 50 protsenti                  | 30 protsenti               | 20 protsenti                    |
| T3          | 10,000 | 1 protsenti                   | 4 protsenti                | 95 protsenti                    |

Sellel juhul prognoositakse iga vahemiku maksed järgmiselt.

| Vahemikud   | Tehing T1      | Tehing T2         | Tehing T3            | Kokku |
|-----------|---------------------|------------------------|---------------------------|-------|
| Õigeaegne   | 100 × 10 ÷ 100 = 10 | 1000 × 50 ÷ 100 = 500 | 10000 × 1 ÷ 100 = 100    | 610   |
| Hilja      | 100 × 50 ÷ 100 = 50 | 1000 × 30 ÷ 100 = 300 | 10000 × 4 ÷ 100 = 400    | 750   |
| Väga palju hilinenud | 100 × 40 ÷ 100 = 40 | 1000 × 20 ÷ 100 = 200 | 10000 × 95 ÷ 100 = 9,500 | 9,740 |

Lehe paremas servas asuvas jaotises **Seotud teave** kuvatakse prognooside kohta rohkem üksikasju.

- Ruudustikus valitud tehingu kohta kuvab kiirkaart **Makseprognoos** makseprognoosi üksikasju vahemikes **Õigeaegne**, **Hilinenud** ja **Väga hilinenud**. Jaotises **Peamised tegurid** kuvatakse peamisi makseid mõjutanud tegureid. Peamised tegurid on valitud tehingu ja/või selle tehingu kliendi atribuudid.
- Kiirkaardil **Kliendi ülevaated** kuvatakse valitud tehingu praegust kliendi arvet, makset ja võlanõuete statistikat.
- Kiirkaardil **Kliendi ajalugu** kuvatakse kliendi makseajalugu vahemikes **Õigeaegne**, **Hilinenud** ja **Väga hilinenud**.

Andmed jaotises **Peamised tegurid** ning kiirkaartidel **Kliendi ülevaated** ja **Kliendi ajalugu** aitavad makseprognoose selgitada. See võib aidata suurendada teie usaldust prognooside efektiivsuse vastu.

## <a name="improving-the-accuracy-of-payment-predictions"></a>Makseprognooside täpsuse parandamine

Makseprognooside täpsust saate vaadata, minnes jaotisse **Krediidihaldus ja võlanõuded \> Seadistamine \> Finantsülevaated \> Finantsülevaadete parameetrid**. Vahekaardi **Kliendi maksete ülevaated** jaotises **Prognoosi mudel** kuvatakse prognoosi mudeli täpsus protsendina.

[![Makseprognooside täpsus](./media/finance-insights-parameters-accuracy-2nd.png)](./media/finance-insights-parameters-accuracy-2nd.png)

Kui te pole täpsusega rahul, valige link **Mudeli täpsuse parandamine**, et avada AI Builderi Builderi laienduskogemus. AI Builderi laienduskogemuses saate valida või tühistada väljade valiku, kuni olete valinud väljad, mis on teie arvates on kõige olulisemad makse tõenäosuse täpseks prognoosimiseks. Kui olete lõpetanud, saate prognoosimismudelit hõlpsalt ümber koolitada ja oma muudatused avaldada. Äsja koolitatud prognoosimismudel võetakse prognooside jaoks automaatselt vastu rakenduses Dynamics 365 Finance.

[![AI Builderi laienduskogemus](./media/ai-builder.png)](./media/ai-builder.png)

## <a name="release-details"></a>Väljastuse üksikasjad

Finantsülevaadete avalik eelversioon on kasutuselevõtu proovimiseks saadaval Ameerika Ühendriikides, Euroopas ja Ühendkuningriigis. Microsoft lisab astmeliselt juurde täiendavate piirkondade tuge.

Avaliku eelvaate funktsioone saab ja tuleb sisse lülitada ainult Järgu 2 liivakasti keskkondades. Liivakasti keskkonnas loodud seadistust ja AI mudeleid ei saa migreerida töökeskkonda. Lisateavet leiate teemast [Microsoft Dynamics 365 eelversioonide täiendavad kasutustingimused](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
