---
title: Automaatkinnitamine planeerimise optimiseerimisega
description: Selles teemas selgitatakse, kuidas kasutada automaatkinnitamist koos planeerimise optimeerimisega.
author: ChristianRytt
manager: tfehr
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: e412ccbc7c44d41e0a70ef8b5436901e01c671e6
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383684"
---
# <a name="auto-firming-with-planning-optimization"></a>Automaatkinnitamine planeerimise optimiseerimisega

[!include [banner](../../includes/banner.md)]

Automaatkinnitamine võimaldab teil kinnitada (st vabastada) plaanitud tellimused koondplaneerimise protsessi osana. Kui plaanitud tellimused on kinnitatud, teisendatakse need tegelikeks ostutellimusteks, üleviimistellimuseks või tootmistellimuseks. Optimeerimise planeerimise kasutamisel kinnitatakse tellimused koondplaneerimise käitamise ajal, kui tellimuse kuupäev (st alguskuupäev) on kinnitamise ajapiiris.

> [!NOTE]
> Plaanitud ostutellimuse automaatkinnitamine saab aset leida ainult siis, kui üksus on hankijaga seostatud.

## <a name="turn-on-auto-firming"></a>Automaatkinnitamise sisselülitamine

Automaatkinnitamise sisselülitamiseks toimige järgmiselt.

1. Valige tööruumis **Funktsiooni haldus** vahekaardil**Uus** loendist suvand **Automaatkinnitus planeerimise optimeerimine**. Kui funktsioon vahekaardile **Uus** ei ilmu, vaadake vahekaartidelt **Pole lubatud** ja **Kõik**.
1. Valige **Luba kohe**. Teise võimalusena valige **Graafik**ja seejärel valige kellaaeg, millal soovite funktsiooni sisse lülitada.

## <a name="set-up-the-firming-time-fence"></a>Kinnitamise ajalimiidi häälestamine

Kinnitamise ajapiir arvutatakse koondplaneerimise käivitamise kuupäevast edasi. See määratletakse sisestatud päevase arvu järgi. Saate kinnitamise ajapiiri juhtida järgmistel viisidel.

- Katvusgrupi vaikimisi kinnitamise ajapiiri määramiseks avage **Koondplaneerimine** \> **Seadistus** \> **Laovarud** \> **Katvusgrupid** ja valige katvusgrupp. Seejärel sisestage kiirkaardil **Muu** väljale **Automaatse kinnitamise ajapiir (päevades)** päevade arv.
- Konkreetse kauba katvusgrupi jaoks märatud kinnitamise ajapiiri ülekirjutamiseks avage **Tooteteabe haldus** \> **Väljastatud tooted**, seejärel valige Toimingupaanil **Plaan** ja valige seejärel **Kauba laovarud**. Seejärel valige vahekaardil **Üldine** suvand **Ajapiiride alistamine** ja sisestage väljale **Automaatse kinnitamise ajapiir (päevad)** päevade arv.
- Konkreetse koondplaani katvusgrupi ja laovarude haldamise jaoks määratletud kinnitamise ajapiiri ülekirjutamiseks avage **Koondplaneerimine** \> **Seadistus** \> **Koonplaanid** ja valige koondplaan. Seejärel määrake kiirkaardil **Ajapiir päevades** suvand **Külmuta** olekusse **Jah** ja sisestage päevade arv.

Kui planeerimise optimeerimist kasutava koondplaneerimise käivitamise automaatne kinnitamine on sisse lülitatud, tehakse automaatse kinnitamise protsess vastavalt automaatse kinnitamise seadistusele. Kui automaatne kinnitamine ei ole sisse lülitatud või kui planeerimine käivitatakse lehelt **Netonõuded**, jäetakse automaatse kinnitamise protsess vahele.

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a>Planeerimise optimeerimine vs. sisseehitatud tarneahela halduse planeerimismootor.

Nii planeerimise optimeerimine kui ka rakendusse Microsoft Dynamics 365 Supply Chain Management sisseehitatud planeerimismootorit saab planeeritud tellimuste automaatseks kinnitamiseks. Kuid on ka olulisi erinevusi. Näiteks kui planeerimise optimeerimine kasutab tellimuse kuupäeva (s.o alguskuupäev), et määrata, millised plaanitud tellimused kinnitada, siis sisseehitatud tarneahela halduse planeerimismootor kasutab vajaduse kuupäeva (s.o lõppkuupäev). Siin on erinevuste kokkuvõte.

**Planeerimise optimeerimine**

- Automaatne kinnitamine põhineb tellimuse kuupäeval (alguskuupäev).
- Kuna tellimuse kuupäev (alguskuupäev) käivitab kinnituse, ei pea te täitmisaega kinnitamise aja osana arvestama.
- Kui soovite kinnitada kõik tellimused, mis peavad jooksval nädalal algama, peab kinnitamise ajapiir olema üks nädal.

**Sisseehitatud tarneahela halduse planeerimismootor**

- Automaatne kinnitamine põhineb nõude kuupäeval (lõppkuupäev).
- Tellimuste tähtajaks kinnitamise tagamiseks peab kinnitamise ajapiir olema pikem kui täitmisaeg.
- Kui soovite kinnitada kõik tellimused, mis peavad jooksval nädalal algama, peab kinnitamise ajapiir olema täitmisaeg pluss üks nädal.
