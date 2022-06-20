---
title: Kliendimaksete prognoosimise kasutamine
description: Selles artiklis läbitakse eeltingimused ja laiad sammud, mis on vajalikud finantside vihjete prooviversiooni kasutamiseks.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-11-16
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 330642624b55a6772ef149b70873021401a6bd83
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901398"
---
# <a name="use-customer-payment-predictions"></a>Kliendimaksete prognoosimise kasutamine

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas kasutada kliendi makseprognoose. Enne selle funktsiooni kasutamist veenduge, et olete lõpetanud selle seadistustoimingud. Lisateabe saamiseks vt [Kliendimaksete prognooside lubamine](enable-cust-paymnt-prediction.md).

Kliendi makseprognoose saate vaadata kliendi **krediidi ja sissenõuete haldamise tööruumis** ja kahel uuel loendile lehel: **·** **kande maksete prognoosid ja kliendi makse prognoosid**.

### <a name="manage-customer-credit-and-collections-workspace"></a>Klientide krediidi ja võlanõuete halduse tööruum

Kliendi **krediidi ja sissenõuete haldamise tööruum** sisaldab kahte uut paani: **kande makseprognoosid ja** kliendi **makseprognoosid**.

### <a name="transaction-payment-predictions-list-page"></a>Kande makseprognooside loendileht

Kande makseprognooside loendilehel saate vaadata avatud kannete makse tõenäosust ajal, **·** **hilja** **ja väga hilja vahemikes.** **·** Ruudustiku iga kande puhul näitab veerg **Õigeaegsuse tõenäosus** tõenäosust, et arve makstakse tähtaegselt või enne seda. Kui tähtajalise makse tõenäosus on väiksem kui 50 protsenti, kuvatakse veeru **Õigeaegsuse tõenäosus** protsendi kõrval punast ringi, mis näitab hilinenud makse riski.

[![Leht makseprognoosid tehingu kohta.](./media/payment-predictions-per-transaction.png)](./media/payment-predictions-per-transaction.png)

Lehe paremas servas asuval paanil **Seotud teave** kuvatakse prognooside kohta rohkem üksikasju.

- Ruudustikus valitud tehingu kohta kuvab kiirkaart **Makseprognoos** makseprognoosi üksikasju vahemikes **Õigeaegne**, **Hilinenud** ja **Väga hilinenud**. Jaotises **Peamised tegurid** kuvatakse peamisi prognoose mõjutanud tegureid. Peamised tegurid on valitud tehingu ja/või selle tehingu kliendi atribuudid.
- Kiirkaardil **Kliendi ülevaated** kuvatakse valitud tehingu praegust kliendi arvet, makset ja võlanõuete statistikat.
- Kiirkaardil **Kliendi ajalugu** kuvatakse kliendi makseajalugu vahemikes **Õigeaegne**, **Hilinenud** ja **Väga hilinenud**.

Andmed jaotises **Peamised tegurid** ning kiirkaartidel **Kliendi ülevaated** ja **Kliendi ajalugu** aitavad makseprognoose selgitada. See võib aidata suurendada teie usaldust prognooside efektiivsuse vastu.

[![Makseprognooside graafilised näidikud seostuva teabe paanil.](./media/payment-prediction-gauges.png)](./media/payment-prediction-gauges.png)

### <a name="customer-payment-predictions-list-page"></a>Kliendi makseprognooside loendileht

Kliendi **makseprognooside** loendileht näitab kogu avatud saldot ja summat, **mis** on prognoositud maksta õigeaegselt, **·** **hilja ja väga** hilja vahemikes.

[![Leht Makseprognoosid kliendi kohta.](./media/payment-predictions-per-transaction-02.png)](./media/payment-predictions-per-transaction-02.png)

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

- Ruudustikus valitud tehingu kohta kuvab kiirkaart **Makseprognoos** makseprognoosi üksikasju vahemikes **Õigeaegne**, **Hilinenud** ja **Väga hilinenud**.
- Kiirkaardil **Kliendi ülevaated** kuvatakse valitud tehingu praegust kliendi arvet, makset ja võlanõuete statistikat.
- Kiirkaardil **Kliendi ajalugu** kuvatakse kliendi makseajalugu vahemikes **Õigeaegne**, **Hilinenud** ja **Väga hilinenud**.

Kliendi vihjete **ja kliendi ajaloo kiirkaartide** **andmed** aitavad selgitada makseprognoose. See võib aidata suurendada teie usaldust prognooside efektiivsuse vastu.

## <a name="improving-the-accuracy-of-payment-predictions"></a>Makseprognooside täpsuse parandamine

Makseprognooside täpsust saate vaadata, minnes jaotisse **Krediidihaldus ja võlanõuded \> Seadistamine \> Finantsülevaated \> Finantsülevaadete parameetrid**. Vahekaardi **Kliendi maksete ülevaated** jaotises **Prognoosi mudel** kuvatakse prognoosi mudeli täpsus protsendina.

Kui teid ei ole täpsusega täidetud, **valige laienduse kogemuse avamiseks** link Parandada mudeli täpsust AI Builder. Laiendikogemuses AI Builder saate valida või tühistada väljade valiku seni, kuni olete valinud väljad, mis on teie jaoks kõige olulisemad makse tõenäosuste täpseks prognoosimiseks. Kui olete lõpetanud, saate prognoosimismudelit hõlpsalt ümber koolitada ja oma muudatused avaldada. Dynamics 365 Finance prognooside jaoks komplektetakse automaatselt vastloodud ennustuse mudel.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
