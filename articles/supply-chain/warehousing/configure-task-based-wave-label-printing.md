---
title: Voo sildi printimise plaanimine voo ajal
description: See artikkel kirjeldab, kuidas seadistada ja kasutada funktsioone ülesandepõhise voo sildi printimiseks.
author: perlynne
ms.date: 06/09/2021
ms.topic: article
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: ac2bc4cce42bada43334b82301d716414cd6d654
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889453"
---
# <a name="schedule-wave-label-printing-during-wave"></a>Voo sildi printimise plaanimine voo ajal

[!include [banner](../../includes/banner.md)]

Kasutage funktsiooni *Ülesandel põhinev voo sildi printimine* voo protsessi osana efektiivsuse parandamiseks ning selleks, et süsteem looks voo silte ja töötaks eraldi ülesannetes.

Voo siltide printimise konfigureerimine on keerukas ning põhineb täpsel konfiguratsioonil ja koondandmetel. Voo sildikirjete loomise nurjumine pole ebatavaline ja kui see juhtub, siis kogu voo töötlemine pööratakse tagasi. *Ülesandepõhise voo sildi printimise* funktsioon aitab teil vältida töö ja tööridade uuesti loomist iga kord, kui voo silt on valesti prinditud.

*Ülesandel põhineva voo sildi printimise* funktsiooni kasutamisel loob süsteem esmalt töö ja tööread. Seejärel loob ja prindib see voosildid. Kui voo sildid on korrektselt loodud, vabastab see komplekteerimise töö ja voo.

## <a name="turn-on-the-task-based-wave-label-printing-feature-in-feature-management"></a>Lülitage funktioon Ülesandepõhine voo sildi printimine funktsioonihalduses sisse

Selles artiklis kirjeldatud funktsioonide kasutamiseks peavad need olema teie süsteemi jaoks sisse lülitatud. Kasutage [Funktsioonide halduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et lülitada sisse funktsioonid järgmises järjekorras:

1. *Voo sildi printimine* – see funktsioon on vajalik voo protsessi meetodi lubamiseks voo sildi printimisel.
1. *Üleorganisatsioonilise töö blokeerimine* - see funktsioon on vajalik plaanitud töö loomise nii käsitsi kui ka automaatseks konfigureerimiseks. (Tarneahela halduse versiooni 10.0.21 kohaselt on see funktsioon kohustuslik, seega on see vaikimisi sisse lülitatud ja seda ei saa enam välja lülitada.)
1. *Ülesandel põhineva voo sildi printimine* – see funktsioon on vajalik voo sildi printimise tükeldamiseks eraldi kande raames.

## <a name="manually-enable-the-new-wave-step-method"></a>Luba uus voo etapi meetod käsitsi

Kõigepealt peate looma uue voo etapi meetodi ja lubama selle paralleelse, asünkroonse ülesande töötlemiseks.

1. Avage jaotis **Laohaldus \> Seadistus \> Vood \> Voo protsessi meetodid**.
1. Valige toimingupaanil suvand **Meetodi uuesti loomine**. Pange tähele, et *waveLabelPrinting* lisatakse vooprotsessi meetodite loendisse, mida saate kasutada oma saadetise voo mallides.
1. Valige kirje, kus **meetodi nime** väljaks on määratud *waveLabelPrinting* ja seejärel valige tegumiribal suvand **Ülesande konfiguratsioon**.
1. Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida. Seejärel määrake uuel real järgmised väljad.

    - **Ladu** – valige ladu, mida töö loomise töötlemise plaanimiseks kasutate. (Kui kasutate testimiseks demoandmeid, saate valida lao *24*.)
    - **Pakett-tööde maksimaalne arv** – määrake pakett-tööde maksimaalne arv. Enamasti peaks väärtus olema *8*-*16*. Ent me soovitame katsetada, et leida oma stsenaariumite jaoks optimaalne seadistus.
    - **Voo töötlemise partii rühm** – valige partii järjekorra töötlemise optimeerimiseks sihtotstarbeline voo töötlemise partii grupp.

Nüüd saate värskendada olemasolevat voomalli nii, et see kasutab *Voo sildi printimise* voo töötlemise meetodit. Teise võimalusena saate luua uue voomalli, mis seda kasutab.

1. Avage **Laohaldus \> Seadistus \> Vood \> Voomallid**.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Valige loendi paanis värskendatav voomall. (Kui kasutate testimiseks demoandmeid, saate valida *24 vaikimisi saatmine*.)
1. Valige kiirkaardi **Meetodid** veerust **Järelejäänud meetodid** rida, mille välja **Nimi** väärtuseks on seatud *waveLabelPrinting*.
1. **Valitud meetodid** veeru valitud rea teisaldamiseks **lisa** (paremnoole nupp).
1. Sisestage voo etapi koodi väljale **Voo etapi kood**, mida kasutatakse voo malli ühendamiseks voo sildi malliga.

## <a name="set-wave-task-processing-threshold-data"></a>Voo ülesande töötlemise lävendi andmete määramine

Esimest korda, kui voo protsess töötab mis tahes ülesandepõhise töötlemise abil, loob süsteem voogude vaiketöötluse vaikelävi andmed. Andmeid kasutatakse voo töötluse asünkroonse ja ülesandepõhise töötluse juhtimiseks, mis võimaldab sellel töödelda ja luua voo silte paralleelselt.

Vaikeandmed kasutavad algselt töö ID-de minimaalse arvu läviväärtusena väärtust *1* (`MinimumWorkThresholdForLabelPrinting`). Seega, kui süsteem töötleb voogu, mil on rohkem kui üks töö ID, kasutab see ülesandepõhist voosiltide töötlemist eraldi kandes. Neid andmeid saate katsekeskkonnas `WHSWaveTaskProcessingThresholdParameters` tabelisse käsitsi sisestada või värskendada. Sätte muutmiseks tootmiskeskkonnas peate uuendamiseks ühendust võtma Microsoft Support'ga.

## <a name="changes-to-the-wave-processing-logic-when-task-based-wave-label-printing-is-used"></a>Voo töötlemisloogika muudatused ülesandepõhise voo sildi printimise kasutamisel

Kui voo sildi töötlemine ületab voo ülesande töötlemise läve, käivitatakse toimingupõhine töötlemine. Järgmises voo töötluses, mis vastab voomallile, käivitatakse voo sildi printimine eraldi kandes *ttsbegin*/*ttscommit* kohe pärast töö loomist. Kui voo mallis on konfigureeritud töö väljaandmine (blokeering) automaatselt käivituma, toimub see alles pärast voo sildi printimise protsessi edukat lõpetamist.

Kui voo sildi loomine ebaõnnestub (nt kui töö koguse teisendamine voo sildi koguseks ebaõnnestub ja ilmneb viga), nurjub ainult asjakohane kanne. Eelnevalt loodud töö jääb külmutatuks. Vigade parandamiseks ja voo siltide printimiseks järgige neid samme.

1. Avage **Laohaldus \> Väljaminevad vood \> Saadetise vood \> Kõik vood**.
1. Valige ruudustikust asjakohane voog.
1. Valige roimingupaani vahekaardil **Voog** grupis **Printimine** suvand **Voo sildid**.
1. Järgige ekraanil olevaid juhiseid siltide printimiseks saatmiseks.
1. Valitud voo töö käsitsi vabastamiseks valige tegevuspaani vahekaardil **Voog** grupis **Voog** **Väljaandmine**.

## <a name="additional-resources"></a>Lisaressursid

- [Voosildi printimine](configure-wave-label-printing.md)
- [Voo ajal töö loomise plaanimine](configure-wave-schedule-work-creation.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
