---
title: Dynamics 365 Supply Chain Management-i (varahalduse) integreerimine Dynamics 365 Guides-iga
description: Selles teemas selgitatakse, kuidas integreerida Microsoft Dynamics 365 Supply Chain Management-i varahalduse moodulit Dynamics 365 Guides-iga, et saada võimalus kasutada virtuaaljuhendite võimalusi oma igapäevastes teeninduse ja hoolduse töövoogudes.
author: kamaybac
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 3793dca681e28b90e96469256f368620393704f2
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344266"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a>Dynamics 365 Supply Chain Management-i (varahalduse) integreerimine Dynamics 365 Guides-iga

Te saate integreerida Microsoft Dynamics 365 Supply Chain Management-i **varahalduse** moodulit Dynamics 365 Guides-iga, et saada võimalus kasutada virtuaaljuhendite võimalusi oma igapäevastes teeninduse ja hoolduse töövoogudes. Kui juhend on seotud varahalduse töökäsuga, siis näeb mobiilirakenduses Supply Chain Management (Dynamics 365) töökäsu hoolduse kontrollnimekirja avav töötaja, et saadaval on juhend. Seejärel saab töötaja juhendi tuvastada ja avada rakenduses Dynamics 365 Guides HoloLens.

## <a name="prerequisites"></a>Eeltingimused

Enne kui saate lisada juhendid varahalduse töökäskudele, peate täitma järgmised eeltingimused.

- [Seadistage Dynamics 365 Supply Chain Management-i](../../fin-ops-core/fin-ops/index.md) versioon 10.0.9 või uuem versioon.
- [Lülitage Supply Chain Managementi rakendustes sisse topeltkirjutamine](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).
- [Lülitage sisse eelväljaande funktsioon](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) **MRGuidesFeature** jaoks. (Tootmiskeskkondade puhul peate esmalt esitama tugipileti, et teie rentnik lisataks eelväljaande gruppi.)
- [Lülitage sisse järgmised konfiguratsioonivõtmed](/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) lehel **Litsentsi konfiguratsioon**.

    - Varahaldus \> Virtuaalne varahaldus
    - Virtuaalne \> Virtuaalne juhend

- [Seadistage Dynamics 365 Guides-i](/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) versioon 200.0.0.96 või uuem versioon.

## <a name="use-dynamics-365-guides-with-asset-management"></a>Dynamics 365 Guides-i kasutamine varahaldusel

Juhendi seostamiseks kasutate varahalduse real hoolduse kontrollnimekirja. Te saate seose luua hoolduse kontrollnimekirja malli, hooldustöö tüübi või töökäsu kaudu, kuna kõik kolm sisaldavad hoolduse kontrollnimekirja ridu. Malli kasutamine aitab aega säästa, kuna malli saab seostada kõigi hooldustöö tüüpidega, mis seda kasutavad. Näiteks seostatakse hooldustöö tüübiga seostatud juhend automaatselt ka kõigi seda töötüüpi täpsustavate töökäskudega. Seevastu otse töökäsuga seostatud juhend on saadaval vaid selle konkreetse töökäsu jaoks.

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a>Juhendi seostamine hoolduse kontrollnimekirja malliga

Juhendi seostamiseks hoolduse kontrollnimekirja malliga toimige järgmiselt.

1. Looge rakenduste Dynamics 365 Guides PC ja HoloLens abil juhend. Juhendi loomise kohta lisateabe saamiseks vaadake järgmisi teemasid.

    - [Kasutage juhendi loomiseks arvutirakendust](/dynamics365/mixed-reality/guides/pc-app-overview)
    - [Kasutage hologrammide paigutamiseks HoloLens-i rakendust](/dynamics365/mixed-reality/guides/hololens-app-overview)

1. Looge rakenduses Supply Chain Management [hoolduse kontrollnimekirja mall](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).
1. Loodud juhendi seostamine uue hoolduse kontrollnimekirja malli hoolduse kontrollnimekirja reaga.

    1. Valige kiirkaardil **Hoolduse kontrollnimekirja read** rida, mida soovite juhendiga seostada.
    1. Valige kiirkaardil **Seotud juhendid** suvand **Lisa juhend**.

        ![Seostage juhend hoolduse kontrollnimekirja reaga.](media/am-guides-integration-add-guide.png "Seostage juhend hoolduse kontrollnimekirja reaga")

    1. Valige juhend väljal **Nimi** ja seejärel valige suvand **Salvesta**.

        ![Valige nimeväljal juhend.](media/am-guides-integration-select-guide.png "Valige nimeväljal juhend")

1. Hoolduse kontrollnimekirja seostamine töötüübiga.

    1. [Looge hooldustöö tüüp](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type) või valige olemasolev hooldustöö tüüp.
    1. Valige tegevuspaanil suvand **Hooldustöö tüübi vaikesuvandid**.

        ![Hooldustöö tüübi vaikesuvandite nupp.](media/am-guides-integration-job-defaults.png "Hooldustöö tüübi vaikesuvandite nupp")

    1. Looge rida ja seejärel valige suvand **Salvesta**.

        ![Looge rida.](media/am-guides-integration-add-line.png "Looge rida")

    1. Valige toimingupaanil suvand **Hoolduse kontrollnimekiri**.

        ![Hoolduse kontrollnimekirja nupp.](media/am-guides-integration-maintenance-checklist.png "Hoolduse kontrollnimekirja nupp")

    1. Lisage rida kiirkaardil **Hoolduse kontrollnimekirja read** ja seejärel muutke välja **Tüüp** väärtuseks **Mall**.

        ![Muutke tüübi väärtus.](media/am-guides-integration-checklist-lines.png "Muutke tüübi väärtus")

    1. Valige kiirkaardil **Rea üksikasjad** väljal **Mall** see mall, mille seostasite juhendiga ja seejärel klõpsake **Salvesta**.

        ![Valige mall.](media/am-guides-integration-checklist-line-details.png "Valige mall")

1. [Looge töökäsk](work-orders/manually-created-workorders.md#create-work-order) ja seejärel valige hooldustöö tüüp, mis kasutab hoolduse kontrollnimekirja malli, mille seostasite juhendiga. See juhend on automaatselt töökäsuga seotud.

    ![Valige hooldustöö tüüp.](media/am-guides-integration-create-work-order.png "Valige hooldustöö tüüp")

1. Töökäsu ja töötajatega seotud juhendi kuvamine.

    1. Avage töökäsule ligi pääsemiseks [varahalduse mobiilne tööruum](asset-management-mobile-workspace.md).
    1. [Avage töökäsu hoolduse kontrollnimekiri](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job).
    1. Valige kontrollnimekirja rida, et näha sellega seotud juhendit.

        ![Kontrollnimekirja reaga seotud juhend.](media/am-guides-integration-show-guide.png "Kontrollnimekirja reaga seotud juhend")

    1. Avage juhend rakenduses HoloLens.

        ![Avage juhend rakenduses HoloLens.](media/am-guides-integration-hololens-select.png "Avage juhend rakenduses HoloLens")

> [!NOTE]
> Juhendi võite seostada ka otse töökäsu või töötüübi hoolduse kontrollnimekirjaga.

> [!IMPORTANT]
> On levinud probleem, et kui seostate hoolduse kontrollnimekirja hooldustöö tüübi vaikesättega, siis ei kajastu malliga seotud juhend lehe **Hooldustöö tüübi vaikesuvandid** kiirkaardil **Seotud juhendid**. Küll aga ilmub juhend nähtavale pärast seda, kui kiirkaardil **Seotud juhendid** on töökäsu suhtes rakendatud seda töötüüpi.

## <a name="see-also"></a>Vt ka

- [Topeltkirjutusega ülevaade](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [Varahalduse ülevaade](index.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]