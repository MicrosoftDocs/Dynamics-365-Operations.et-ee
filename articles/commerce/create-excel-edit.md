---
title: Exceli töövihiku loomine jaemüügikannete redigeerimiseks
description: Selles artiklis kirjeldatakse, kuidas luua Exceli töövihikut, et saaksite Microsoft Dynamics 365 Commerce'is jaemüügikandeid redigeerida.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.industry: Retail
ms.openlocfilehash: 93e0053c38c9595cab59947e4b65b0b4aa966380
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270204"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a>Exceli töövihiku loomine jaemüügikannete redigeerimiseks

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse, kuidas luua Exceli töövihikut, et saaksite Microsoft Dynamics 365 Commerce'is jaemüügikandeid redigeerida.

## <a name="overview"></a>Ülevaade

Saadaval on eelmääratletud Exceli mall, mida kliendid saavad avada süsteemi eri osadest ning kasutada jaemüügikannete redigeerimiseks ja auditeerimiseks. Kuid kliendid saavad selleks otstarbeks luua ka kohandatud Exceli töövihiku.

## <a name="create-and-configure-an-excel-workbook"></a>Exceli töövihiku loomine ja konfigureerimine

Jaemüügikannete redigeerimiseks Exceli töövihiku loomiseks ja konfigureerimiseks toimige järgmiselt.

1. Avage Excel ja looge tühi töövihik.
1. Valige vahekaardil **Lisamine** suvand **Minu lisandmoodulid**.
1. Valige parempoolsel paanil link **Lisa serveriteave**.
1. Sisestage serveri URL ja seejärel valige **OK**.
1. Kui kuvatakse tõrketeade „Ühtegi apleti registreeringut ei leitud“, toimige probleemi lahendamiseks järgmiselt.

    1. Avage Commerce'is **Süsteemihaldus \> Seadistus \> Office'i rakenduse parameetrid**.
    1. Valige kiirkaardil **Rakenduse parameetrid** suvand **Lähtesta rakenduse parameetrid**.
    1. Valige kinnituse teateaknas **OK**.
    1. Valige kiirkaardil **Registreeritud apletid** suvand **Lähtesta apleti registreering**.
    1. Korrake vajadusel kolme eelmist sammu.

1. Valige **Kujundus** ja seejärel **Lisa tabel**.
1. Valige muudetavate andmete alusel üksused, mis tuleb redigeerimiseks Exceli töövihikusse lisada. Kasutage viitena järgmist tabelit.

    | Kande tüüp | Kasutatavad andmeüksused |
    |------------------|----------------------|
    | Selvehulgimüügikanded, veebitellimused, asünkroonsed klienditellimused, asünkroonsed kliendihinnapakkumised | Kanne (auditeeritav), müügikanne (auditeeritav), maksekanded (auditeeritav), maksukanded (auditeeritav), allahindluse kanded (auditeeritav), tasukanded (auditeeritav) |
    | Raha hoiustamine panka | Kanne (auditeeritav), panka hoiustatud maksevahendi kanded (auditeeritav) |
    | Seifi viidav raha | Kanne (auditeeritav), seifi hoiustatud maksevahendi kanded (auditeeritav) |
    | Päevakassa | Kanne (auditeeritav), päevakassakanded (auditeeritav) |
    | Tulu, kulu | Kanne (auditeeritav), tulu-/kulukanded (auditeeritav), maksetehingud (auditeeritav) |
    | Algsumma deklareerimine, maksevahendi eemaldamine, sularaha sissemakse, maksevahendi muutmine, arve maksmine, kliendi deposiit | Kanne (auditeeritav), maksekanded (auditeeritav) |

    > [!NOTE]
    > Oluline on lisada igasse Exceli töövihikusse ainult üks andmeüksus. Lisaks tuleb asjaomasesse töövihikusse lisada kõik võtmesümboliga tähistatud väljad.

1. Pärast töövihiku konfigureerimist rakendage nõutavad filtrid. Veenduge, et rakendaksite samu filtreid kõigi faili töölehtede korral. Ärge laadige Exceli faili väga suuri andmehulkasid. Muidu võib see jõudlust mõjutada ning Excel ja teie süsteem võivad aeglasemaks muutuda. Soovitame kasutada failis alati filtrit „Ettevõte“ ning kas filtrit „Väljavõtte number“ või filtrit „Kande number“.
1. Kui filtrid on konfigureeritud, valige andmete laadimiseks **Värskenda**.
1. Redigeerige vajalikke andmeid ja seejärel avaldage need. Kui nupp **Avalda** pole saadaval, ei lisatud Exceli töövihikusse tõenäoliselt olulisi välju.

## <a name="additional-resources"></a>Lisaressursid

[Selvehulgimüügi- ja kassahalduskannete redigeerimine ning auditeerimine](edit-cash-trans.md)

[Veebitellimuse ja asünkroonse klienditellimuse kannete redigeerimine ning auditeerimine](edit-order-trans.md)

[Jaemüügikannete finantsdimensioonide redigeerimine](edit-financial-dim.md)

[Väljade lisamine Exceli töövihikusse jaemüügikannete redigeerimiseks](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
