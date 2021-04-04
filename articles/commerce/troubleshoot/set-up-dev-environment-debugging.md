---
title: E-kaubanduse arenduskeskkonna häälestamine, et siluda järguga 1 jaemüügiserveri virtuaalmasin
description: E-kaubanduse arenduskeskkonna häälestamine, et siluda järguga 1 jaemüügiserveri virtuaalmasin (VM).
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 35380a559a4f1b22bdf04ff25cb2bbfc51aff45b
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585276"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a>E-kaubanduse arenduskeskkonna häälestamine, et siluda järguga 1 jaemüügiserveri virtuaalmasin

[!include [banner](../../includes/banner.md)]

E-kaubanduse arenduskeskkonna häälestamine, et siluda järguga 1 jaemüügiserveri virtuaalmasin (VM).

## <a name="description"></a>Kirjeldus

Microsoft Dynamics 365 Commerce Järgu 1 keskkonnad juurutatakse tavaliselt Commerce Runtime'i (CRT) ja kassa laienduse arendamiseks. Need on eraldiseisev keskkond. Teenuse (SaaS) olemuse tõttu ei sisalda need e-kaubanduse komponente.

Mõne stsenaariumi korral võite soovida katsetada laiendeid järguga 1 keskkonnas, nii et saate siluda laiendusi e-äri komponentidest. Üldiste juhiste saamiseks vaadake artiklit [Esimese järgu Commerce'i arenduskeskkonna silumine](../e-commerce-extensibility/debug-tier-1.md).

Järgu 1 keskkonna suhtes silumisel, kuna sait kutsub nüüd teist jaemüügiserverit, võivad ristserveri kutsed põhjustada mitmesuguseid sisu turbepoliitikaga seotud tõrkeid.

Järgmisel joonisel on toodud näide tõrkest, mis võib ilmneda, kui toote üksikasjade lehel on valitud variant.

![Tõrge, kui toote üksikasjade lehel on valitud variant](media/unhandled-rejection-error.jpg)

Järgmisel joonisel on näidatud sarnane tõrke näide brauseri siluritööriistades (F12 Arendustööriistad). Veateade sisaldab sisu turbepoliitika direktiivi rikkumisi.

![Siluritööriistade tõrge](media/debugger-tools-error.JPG)

## <a name="resolution"></a>Eraldusvõime

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a>Commerce'i saidikonstruktori saidi jaoks sisu turbepoliitika keelamine

1. Valige sait, millel te töötate.
1. Valige **Saidi sätted** ja seejärel valige suvand **Laiendused**.
1. Valige vahekaardil **Sisu turbepoliitika** suvand **Keela sisu turbepoliitika**.
1. Valige käsk **Salvesta ja avalda**.

> [!NOTE]
> Ettevõtetesse ja tarbekaupadesse (B2C) sisselogimine ei tööta kohalikus arenduskeskkonnas. Kuid saate kasutada külalisi väljaregistreerimist või koostada lehekülje m nii, et simuleerida kasutaja sisselogimist vastavalt vajadusele.

## <a name="additional-resources"></a>Lisaressursid

[E-kaubanduse võrgupõhise laiendatavuse arendamise alustamine](../e-commerce-extensibility/sdk-getting-started.md)

[Sisu turbepoliitika (CSP) haldamine e-äri saidil](../manage-csp.md)
