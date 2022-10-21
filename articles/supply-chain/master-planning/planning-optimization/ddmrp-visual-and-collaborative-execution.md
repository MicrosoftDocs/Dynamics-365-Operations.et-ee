---
title: Visuaalne ja koostööd võimaldav täitmine
description: See artikkel kirjeldab, kuidas jälgida oma nõudlusepõhiste materjalinõuete planeerimist (DDMRP) dekodeerimispunkte, puhvertsoone, planeeritud tellimusi ja ajalugu.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ReqDDMRPWorkspace, ReqDecouplingPointsStatusByNetFlow, ReqDecouplingPointStatusByOnHand, ReqPlannedOrderForm, ReqItemDecoupledLeadTime
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 92e38c6ea19b60ae0a61e55f240ff52698e06933
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689772"
---
# <a name="visual-and-collaborative-execution"></a>Visuaalne ja koostööd võimaldav täitmine

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

See artikkel kirjeldab, kuidas jälgida oma nõudlusepõhiste materjalinõuete planeerimist (DDMRP) dekodeerimispunkte, puhvertsoone, planeeritud tellimusi ja ajalugu.

## <a name="visually-track-buffers-and-quantities-for-a-selected-item"></a>Jälitage visuaalselt valitud kauba puhvereid ja koguseid.

Microsoftis Dynamics 365 Supply Chain Management saate visuaalselt jälgida, kuidas mis tahes valitud väljastatud toote puhvrid, vabad kogused ja netovoo tasemed aja jooksul muutuvad. Järgige neid samme diagrammide avamiseks ja ülevaatamiseks.

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Valige vabastatud kaup, mis on seadistatud dekodeerimispunktina. (Lisateavet vt teemast [Lao paigutamine](ddmrp-inventory-positioning.md).)
1. Valige tegevuspaani vahekaardil **Plaan kauba laovarud** **.**
1. Kauba laovarude **lehel** valige kauba laovarude kirje, mis loob dekodeerimispunkti. (Kirje näitab nende laovarude grupi nime, mis on seadistatud looma dekodeerimispunkte.)
1. **Valige vahekaart Vabad**. See vahekaart sisaldab diagrammi, mis näitab, kuidas vabad kogused aja jooksul muutusid, koos väärtusega vabas kaubavaru tasemes, mis salvestati kindlal perioodil iga kord, kui optimeerimist käitatakse. Vahekaart sisaldab ka tabelit, mis näitab, millistesse järgnevatesse kategooriatesse iga kirjendatud vaba kaubavaru tase langeb:

    - **Kriitiliselt madal** – väiksem kui pool perioodi miinimumi.
    - **Madal** – poole miinimumi ja miinimumi vahel.
    - **Keskmine vaba –** miinimumi ja miinimumi ning rohelise tsooni vahel.
    - **Keskmisest kõrgem** – keskmisest kõrgem.

    ![Vahekaardil Vaba kaubavaru ajaloolised tasemed.](media/ddmrp-on-hand-graph.png "Vaba kaubavaru ajaloolised tasemed vahekaardil")

    > [!NOTE]
    > Vahekaardil Vabad vabad värvid **tähistavad** sarnaseid värve **, mida kasutatakse vahekaardil Puhverväärtused**.

1. Selleks, et vaadata, kuidas teie puhverväärtused aja jooksul muutusid ja kuidas neid võrreldakse vabade ja netovoo tasemetega, valige **vahekaart Puhverväärtused**.

    ![Ajalooline vaba ja netovoo tasemed puhverväärtuste vahekaardil](media/ddmrp-buffer-values-graph.png "Ajalooline vaba ja netovoo tasemed puhverväärtuste vahekaardil")

## <a name="track-the-status-and-planned-orders-for-all-decoupling-points"></a>Kõikide dekodeerimispunktide oleku ja plaanitud tellimuste jälgimine

Nõudluse **juhitud MRP** tööruum pakub mitmeid tööriistu, koos tulemuslikkuse võtmenäidikutega (KPI-d) ja ülevaated dekodeerimise punktis kaupade ja seotud plaanitud tellimuste olekust. Selle avamiseks minge koondplaneerimise **tööruumide \> nõudluse juhitav \> MRP-sse**.

![Nõudluse juhitud MRP tööruum.](media/ddmrp-workspace.png "Nõudluse juhitud MRP tööruum")

## <a name="get-overviews-of-decoupling-points-and-planned-orders"></a>Hankige ülevaade dekodeerimise punktide ja plaanitud tellimuste kohta

Lisaks nõudluse juhitud **MRP tööruumile** pakub tarneahela haldus mitut lehekülge, kus saate vaadata teavet oma DDMRP häälestuse, punktide ja planeeritud tellimuste dekodeerimise kohta. Mõned neist lehtedest pakuvad ka mugavaid nuppe tegumiribal, mis võimaldab hallata puhvereid, käitada koondplaneerimist ja avada teisi seotud vaateid.

- Dekodeerimispunkti oleku vaatamiseks netovoo taseme järgi minge **\>\> koondplaneerimise DDMRP-i \> punktide dekodeerimise olekusse netovoo järgi**.
- Dekodeerimispunkti oleku vaatamiseks vaba kaubavaru taseme järgi minge **\>\> koondplaneerimise DDMRP \> dekodeerimispunktide olekusse laos.**
- Selleks, et vaadata planeeritud tellimusi punktide dekodeerimise jaoks, **\>\> minge koondplaneerimise DDMRP-i \> plaanitud tellimustele punktide dekodeerimise jaoks.**
- Dekodeeritud täitmisaegade vaatamiseks minge koondplaneerimise **\>\> DDMRP \> dekodeeritud täitmisajale**.

## <a name="clean-up-decoupling-point-buffer-values"></a>Dekodeerimispunkti puhvriväärtuste puhastamine

Aja jooksul loob süsteem hulga ajaloolisi andmeid, mis on seotud jooksvate puhverarvutustega. Ajaloolised andmed põhjustavad andmemahtu kasvu ja võivad mõjutada teie süsteemi jõudlust. Seetõttu soovitame aeg-ajalt puhastada vanad dekodeerimispunkti puhverväärtused.

> [!WARNING]
> Puhastustöö eemaldab ajaloolised puhverväärtuse sätted ja ajaloolise vaba/netovoo teabe. See ei ole tühistatav.

Järgige neid samme dekodeerimispunkti puhverväärtuste puhastamiseks.

1. Minge koondplaneerimise **koondplaneerimise \>\> DDMRP-i puhastage \> dekodeerimispunkti puhverväärtused**.
1. Seadke dialoogiboksis **Dekodeerimispunkti puhverväärtuste** puhastamine järgmised väljad:

    - **Kustuta kirjed, mis on vanemad kui (päevades)** – määrake vanima säilitamispäevade vanima kirje vanus. Kustutatakse kõik sellest väärtusest vanemad dekodeerimispunkti puhvriväärtuse kirjed.
    - **Koondplaan** – valige koondplaan, mis sisaldab üksusi, mida see puhastus peaks mõjutama. Puhastus rakendub kõigile plaani üksustele pärast **selles** dialoogiboksis määratud filtrisätete rakendamist.

1. Kui soovite piirata kirjekogumi, kus pakett-tööd peaks käitama, **valige** kiirkaardi Kaasamiseks kirjetes suvand Filter **,** et avada dialoogiboks **Päring**. See dialoogiboks töötab samuti nagu tarneahela halduses teist [tüüpi](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) taustatööde puhul.
1. **Määrake kiirkaardil** Käivita taustal, kuidas, millal ja kui sageli puhastamist tuleks teha. Väljad töötavad samamoodi nagu muud tüüpi [taustatööl](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) Supply Chain Management puhul.
1. Valige **OK**, et lisada uus töö pakktöötluse järjekorda käivitamiseks.
