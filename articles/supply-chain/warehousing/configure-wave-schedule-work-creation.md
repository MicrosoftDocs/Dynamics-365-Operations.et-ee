---
title: Voo ajal töö loomise plaanimine
description: Selles teemas kirjeldatakse, kuidas häälestada ja kasutada töö loomise plaanimise voo töötlemismeetodit.
author: perlynne
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 358f5a87cdb42f0ff646948da8d38475cf49e3f2
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577908"
---
# <a name="schedule-work-creation-during-wave"></a>Voo ajal töö loomise plaanimine

[!include [banner](../../includes/banner.md)]

Kasutage funktsiooni *Töö loomise plaanimine* osana oma voo loomisprotsessist, et aidata suurendada voo töötlemise läbilasku, võimaldades süsteemil luua tööd paralleeltöötlust kasutades.

Kui see funktsioon on lubatud, luuakse plaanitud töö automaatselt, mida süsteem lõpuks töötleb, et luua tegelik töö. Kui voo laadimise ridade arv saavutab ettemääratud läviväärtuse, loob süsteem tegeliku töö palju kiiremini, rakendades paralleelset asünkroonset töötlemist.

## <a name="turn-on-the-scheduled-work-creation-features-in-feature-management"></a>Lülitage funktsioonihalduses sisse planeeritud töö loomise funktsioonid.

Selles teemas kirjeldatud funktsioonide kasutamiseks tuleb need teie süsteemi jaoks sisse lülitada. Kasutage [Funktsioonide halduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et lülitada sisse järgmised funktsioonid järgmises järjekorras:

1. **Üleorganisatsioonilise töö blokeerimine** - vajalik plaanitud töö loomise nii käsitsi kui ka automaatseks konfigureerimiseks.
1. **Planeeritud töö loomine** - vajalik plaanitud töö loomise nii käsitsi kui ka automaatseks konfigureerimiseks.
1. **Üleorganisatsioonilise "planeeritud töö loomise" voo meetod** - vajalik plaanitud töö loomise nii käsitsi kui ka automaatseks konfigureerimiseks. Kui kasutate ainult käsitsi konfigureerimist, siis seda funktsiooni ei vaja.

<a name="Auto-enable-schedule-work-creation"></a>

## <a name="automatically-configure-scheduled-work-creation"></a>Konfigureeri automaatselt planeeritud töö loomist

Kui lubate *Üleorganisatsiooniline "Töö loomise plaanimise" voomeetodi* funktsiooni, leiab süsteem automaatselt järgmise:

- *Plaanitud töö loomise* voomeetod (`WHSScheduleWorkCreationWaveStepMethod`) lisatakse paralleelselt kõigi juriidiliste isikute lõikes.
- Voo mallid kõigilt juriidilistelt isikutelt, kelle **voo malli tüüp** on määratud olekule *Lähetamine* ja **Malli olek** on määratud olekusse *Kehtiv*, on *töö loomise* meetod asendatud *paneeritud töö loomise* meetodiga. Kuid voomalle juriidilistelt isikutelt, kus *töö loomise* meetod on lubatud korrata, ei muudeta.
- *Töö loomise plaani* meetodi ülesande konfiguratsioonid luuakse kõigi juriidiliste isikute kõigi ladude jaoks, kelle puhul on lubatud **kasutada laohaldusprotsesse**. See tähendab, et *Töö plaani loomise* meetod käivitatakse nüüd vaikimisi paralleelselt. Olemasolevad laod, mille puhul muudate funktsiooni **Kasuta laohaldusprotsesse** väljalt *Ei* *Jah*, käitatakse seda meetodit vaikimisi paralleelselt.
- Kõik juriidilised isikud töötlevad voogusid partiides ja **Oota lukustus (ms)** seatakse vaikeväärtuseks *60 000* ms, kui selleks oli eelnevalt seatud *0* ms.
- Kõigil uutel teie loodud voomallidel on *töö loomise plaani* voomeetod *töö loomise* meetodi asemel.

Olemasolevaid ülesande ja voo töötlemise konfiguratsioone säilitatakse ka kõigi juriidiliste isikute puhul, kes on juba konfigureeritud töötlema laineid partiides, ja kõigi ladude puhul, mis on juba konfigureeritud kasutama *töö loomise plaani* meetodit paralleelselt.

Vajadusel saate käsitsi ennistada kõiki või kõiki automaatselt tehtud sätteid, kui lubate kogu *üleorganisatsioonilise töö loomise plaani voo meetodi* funktsiooni, toimides järgmiselt:

- Voomallideks avage **Laohaldus \> Seadistus \> Vood \> Voomallid**. Asendab *töö loomise plaani* meetodi *töö loomise* meetodiga.
- Laohalduse parameetriteks minge **Laohaldus \> Seadistus \> Laohalduse parameetrid**. Vahekaardil **Voo töötlemine** rakendatakse soovituslikud väärtused suvanditele **Voogude töötlemine pariina** ja **Lukustuse ooteaeg (ms)**.
- Voomeetoditeks avage jaotis **Laohaldus \> Seadistus \> Vood \> Voo protsessi meetodid**. Valige `WHSScheduleWorkCreationWaveStepMethod` ja valige tegumipaanilt **Ülesande konfiguratsioon**. Vajadusel muutke või kustutage iga loetletud lao partiiülesannete arv ja määratud voo grupp.

## <a name="manually-configure-scheduled-work-creation"></a>Konfigureeri käsitsi planeeritud töö loomist

Kui te ei aktiveerinud [*üleorganisatsioonilist "töö loomise plaani" voomeetodi* funktsiooni](#Auto-enable-schedule-work-creation), saate kasutada selles jaotises antud protseduure planeeritud töö loomise käsitsi konfigureerimiseks vastavalt vajadusele.

### <a name="manually-enable-batch-processing-of-waves"></a>Voogude pakett-töötluse käsitsi lubamine

Laotöö loomiseks paralleelse asünkroonse meetodi kasutamiseks peab teie voo protsess olema käivitatud partiina. Selle häälestamiseks tehke järgmist.

1. Avage  **Laohaldus\>Seadistus \> Laohalduse parameetrid**.
1. Vahekaardil **Üldine** määrake suvand **Töötle vooge pakett-töötlusega** valikule *Jah*. Soovi korral saate valida ka sihtotstarbelise **voo töötlemise pakett-tööde grupi**, et vältida pakett-töötluse järjekorra käitamist teiste protsessidega samal ajal.
1. Määrake syvandi **Oota lukustust (ms)** aeg, mis kohaldub, kui süsteem töötleb mitut voogu samal ajal. Enamike suuremate laine loomisprotsesside puhul soovitame väärtus *60 000*.

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a>Olemasolevate voomallide uue voo etapi meetodi käsitsi lubamine

Alustage uue voo etapi meetodi loomisega ja selle lubamisega paralleelse asünkroonse ülesande töötlemiseks.

1. Avage jaotis  **Laohaldus \>Seadistus \> Vood \> Voo töötlemise meetodid**.
1. Valige  **Meetodite uuesti loomine** ja pange tähele, et *WHSScheduleWorkCreationWaveStepMethod* on lisatud voo töötlemise meetodite loendisse, mida saate oma saatmise voomallides kasutada.
1. Valige kirje **meetodi nimega** *WHSScheduleWorkCreationWaveStepMethod* ja valige suvand **Ülesande konfiguratsioon**.
1. Ruudustikku uue rea loomiseks valige tegevuspaanil **Uus** ja kasutage järgmisi sätteid.

    - **Ladu** – valige ladu, mida töö loomise töötlemise plaanimiseks kasutate.
    - **Pakett-tööde maksimaalne arv** – määrake pakett-tööde maksimaalne arv. Enamasti peaks see väärtus olema vahemikus 8–16, kuid soovitame katsetada teie stsenaariumitel põhineva optimaalse seadistusega.
    - **Voo töötlemise partii rühm** – valige oma partii järjekorra töötlemise optimeerimiseks sihtotstarbeline voo töötlemise partii grupp.

Nüüd olete valmis värskendama olemasolevat voomalli (või looma uue), et kasutada voo töötlemismeetodit *Töö loomise plaanimine*.

1. Avage **Laohaldus\>Seadistus \> Vood \> Voomallid**.
1. Valige toimingupaanil nupp **Redigeeri**.
1. Valige loendipaanil voomall, mida soovite värskendada (kui testite demoandmeid kasutades, võite kasutada *24 saadetise vaikemalli*).
1. Laiendage kiirkaarti **Meetodid** ja valige rida **nimega** *Töö loomise plaanimine* ruudustikus **Ülejäänud meetodid**.
1. Valige nool, mis osutab veerule **Valitud meetodid**, et teisaldada valitud rida sellesse veergu. (Teil saab olla korraga ainult üks valitud meetod, mis kasuab kas suvandit `WHSScheduleWorkCreationWaveStepMethod` või `createWork`, seega olemasolev rida **meetodi nimega** `createWork` teisaldatakse automaatselt ruudustikku **Ülejäänud meetodid**.)

## <a name="set-wave-task-processing-threshold-data"></a>Voo ülesande töötlemise lävendi andmete määramine

Voo töötlemise esimest korda käitamisel kasutades mis tahes ülesandepõhist töötlemist loob süsteem vaikimisi voo ülesande töötlemise lävendi andmed. Andmeid kasutatakse voo töötluse asünkroonse ja ülesandepõhise töötluse juhtimiseks, mis võimaldab sellel töödelda ja luua tööd paralleelselt.

Vaikeandmed kasutavad algselt koormusridade minimaalse arvu läviväärtusena väärtust 15 (`MINIMUMWAVELOADLINES`). See tähendab, et kui süsteem töötleb voogu enam kui 15 koormusreaga, kasutab see asünkroonset ülesande töötlemist. Neid andmeid saate katsekeskkonnas `WHSWaveTaskProcessingThresholdParameters` tabelisse käsitsi sisestada/värskendada. Kui peate seda sätet tootmiskeskkonnas muutma, peate uuendamiseks ühendust võtma Microsoft Support'ga.

## <a name="work-with-the-scheduled-work-creation"></a>Plaanitud töö loomine

Lisateavet plaanitud töö loomise kohta vt [Voo loomine ja töötlemine](wave-processing.md). 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
