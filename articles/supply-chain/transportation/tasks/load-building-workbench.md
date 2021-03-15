---
title: Koorma koostamise töölaud
description: Selles teemas kirjeldatakse, kuidas töötada koorma koostamise töölauaga.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSLoadBuildWorkbench,TMSLoadBuildTemplateCreate,TMSLoadBuildStrategy,TMSLoadBuildTemplateApply
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d1ed91adba5c7accf9a18d7a754d33b2b35b848f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974218"
---
# <a name="load-building-workbench"></a>Koorma koostamise töölaud

Koorma koostamise töölaud võimaldab teil koormate loomisel rakendada koorma koostamise strateegiaid.

## <a name="create-a-load-building-strategy"></a>Koorma koostamise strateegia loomine

Koorma koostamise strateegiad saate kasutada koormate automaatseks koostamiseks. See võimalus võib olla kasulik järgmistes olukordades.

- Kui saadate regulaarselt kindlaid tooteid, aitavad koormastrateegiad säästa aega, sest te ei pea iga kord sama koormat koostama.
- Kui soovite tõhususe maksimeerimiseks välistada poolikud koormad, võivad koormastrateegiad aidata koormaid võimalikult palju täita.

Koorma koostamise strateegia klass nimega `TMSLoadBuildingVolumeStrategy` annab koorma koostamise strateegia nimega *Mahupõhine koorma koostamise strateegia*. See strateegia võimaldab kasutada koorma mallil kõrguse ja kaalu kohta määratud maksimumväärtusi või alistada sätted, sisestades uusi väärtusi. See strateegia on ainus valmiskujul strateegia. (Võib-olla soovite siiski ka kohandatud strateegiaid kasutada.)

Valmiskujul strateegiat *Mahupõhine koorma koostamise strateegia* kasutamiseks valige koorem lehe **Koorma koostamise töölaud** väljal **Koorma koostamise strateegia** (**Transpordihaldus &gt; Planeerimine &gt; Koorma koostamise töölaud**).

Koorma koostamise strateegia loomiseks tehke järgmist.

1. Valige **Transpordihaldus &gt; Häälestus &gt; Koorma koostamine &gt; Koorma koostamise strateegiad**.
1. Tehle toimingupaanil valik **Loo klassiloend**, et veenduda, kas teil on kõigi saadaolevate klasside uusimad versioonid.
1. Valige toimingupaanil nupp **Uus**.
1. Sisestage strateegiale kordumatu nimi, valige koorma koostamise strateegia klass ja sisestage kirjeldus.
1. Valige toimingupaanil nupp **Salvesta**.
1. Valige toimingupaanil **Parameetrid**.
1. Tehke lehel **Koorma koostamise strateegia parameetrid** loendis valik **Mahuhulk** ja sisestage siis väljale **Väärtus** koorma kogu mahuhulga protsent, mida tuleks uuele koorma koostamise strateegiale rakendada.
1. Tehke loendis valik **Kaaluhulk** ja sisestage siis väljale **Väärtus** koorma kogu kaaluhulga protsent, mida tuleks uuele koorma koostamise strateegiale rakendada.
1. Sulgege leht **Koorma koostamise strateegia parameetrid**.
1. Sulgege leht **Koorma koostamise strateegiad**.

Nüüd saate koorma koostamise mallile määrata koorma koostamise strateegia. Võite seda kasutada ka koorma planeerimise töölaual.

## <a name="use-a-load-building-strategy-in-the-load-building-workbench"></a>Koorma koostamise strateegia kasutamine koorma koostamise töölaual

1. Valige **Transpordihaldus &gt; Planeerimine &gt; Koorma koostamise töölaud**.
1. Järgige üht neist sammudest.

    - Valige strateegia väljal **Koorma koostamise strateegia**.
    - Kui olete määranud koorma koostamise malli ja määranud sellele koorma koostmaise strateegia, valige toimingupaanilpaani vahekaardil **Mallide haldamine** käsk **Rakenda mall**. Seejärel valige rippmenüü dialoogiaknas **Koorma koostamise malli rakendamine** mall väljal **Koorma koostamise malli nimi**.

1. Kiirkaardil **Koormamallide järjestus** valige [koormamall](load-template.md). Töölaud proovib koormat sobitada seda tüüpi konteineritega siin määratud järjestuses. Tavaliselt tuleks loendi algusesse panna väikseimad konteinerid, et esimesena valitaks kindlasti väikseim võimalik konteiner.
1. Tehke toimingupaanil valik **Soovita koormaid**.
1. Vaadake üle pakutud koormad ja pakutud koormaread.
1. Tehke toimingupaanil valik **Loo koormad**, et luua kiirkaardi **Pakutud koormaread** lähtedokumentide ridadel põhinevad koormad.
1. Sulgege leht **Koorma koostamise töölaud**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]