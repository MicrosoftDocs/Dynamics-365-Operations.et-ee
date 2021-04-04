---
title: Voo ajal töö loomise plaanimine
description: Selles teemas kirjeldatakse, kuidas häälestada ja kasutada töö loomise plaanimise voo töötlemismeetodit.
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 36a450f78695f617056875f8d236fe46bc66aaaf
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501218"
---
# <a name="schedule-work-creation-during-wave"></a>Voo ajal töö loomise plaanimine

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Kasutage funktsiooni *Töö loomise plaanimine* osana oma voo loomisprotsessist, et aidata suurendada voo töötlemise läbilasku, võimaldades süsteemil luua tööd paralleeltöötlust kasutades.

Kui see funktsioon on lubatud, luuakse plaanitud töö automaatselt, mida süsteem lõpuks töötleb, et luua tegelik töö. Kui voo laadimise ridade arv saavutab ettemääratud läviväärtuse, loob süsteem tegeliku töö palju kiiremini, rakendades paralleelset asünkroonset töötlemist.

## <a name="enable-the-schedule-work-creation-feature"></a>Töö loomise plaanimise funktsiooni lubamine

### <a name="enable-the-feature-in-feature-management"></a>Funktsiooni lubamine funktsioonihalduses

Enne funktsiooni *Töö loomise plaanimine* kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Seega on funktsioon loetletud järgmisel viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *Töö loomise plaanimine*

> [!NOTE]
> Enne *töö loomise plaanimise* lubamist peab funktsioon *Organisatsiooniülene töö blokeerimine* olema sisse lülitatud.

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

1. Valige nool, mis osutab veerule **Valitud meetodid**, et teisaldada valitud rida sellesse veergu. (Teil saab olla korraga ainult üks valitud meetod, mis kasuab kas suvandit *WHSScheduleWorkCreationWaveStepMethod* või *createWork*, seega olemasolev rida **meetodi nimega** *createWork* teisaldatakse aytomaatselt ruudustikku **Ülejäänud meetodid**.)

## <a name="set-wave-task-processing-threshold-data"></a>Voo ülesande töötlemise lävendi andmete määramine

Voo töötlemise esimest korda käitamisel kasutades mis tahes ülesandepõhist töötlemist loob süsteem vaikimisi voo ülesande töötlemise lävendi andmed. Andmeid kasutatakse voo töötluse asünkroonse ja ülesandepõhise töötluse juhtimiseks, mis võimaldab sellel töödelda ja luua tööd paralleelselt.

Vaikeandmed kasutavad algselt koormusridade minimaalse arvu läviväärtusena väärtust 15 (MINIMUMWAVELOADLINES). See tähendab, et kui süsteem töötleb voogu enam kui 15 koormusreaga, kasutab see asünkroonset ülesande töötlemist. Saate neid andmeid katsekeskkonnas tabelisse **WHSWaveTaskProcessingThresholdParameters** käsitsi sisestada/värskendada, kuid kui peate seda sätet töökeskkonnas muutma, peate värskendamise taotlemiseks võtma ühendust Microsofti toega.

## <a name="work-with-the-feature"></a>Funktsiooniga töötamine

Kui funktsioon *Töö loomise plaanimine* on lubatud, loob voo töötlemine plaanitud töö, mida kasutatakse lõpuks uue töö loomisprotsessi poolt. Töö loomise ajal töö blokeeritakse, kasutades funktsiooni *Organisatsiooniülene töö blokeerimine*.

Järgmine vooskeem näitab, kuidas plaanitud tööd laine töötlemise ajal luuakse.

![Töö loomise graafik](media/schedule-work-creation-process.png)

### <a name="planned-work"></a>Plaanitud töö

Leht **Plaanitud töö üksikasjad** (**Laohaldus \> Töö \> Plaanitud töö üksikasjad**) näitab teavet plaanitud töö kohta, mis voo töötlemise ajal algselt luuakse. Saadaval on järgmised suvandi **Protsessi olek** väärtused.

- **Järjekorras** – plaanitud töö on töö loomiseks kasutamiseks ootel.
- **Lõpetatud** – plaanitud töä on töö loomiseks kasutatud.
- **Nurjus** – voo töötlemine nurjus. Pange tähele, et plaanitud töö võib olla olekus **Nurjunud** koos või ilma seotud tegeliku tööta. Kui tegeliku töö loomise protsess nurjub, jääb tegelik töö olekusse *Tühistatud*.

### <a name="batch-job-for-the-work-creation-process"></a>Töö loomisprotsessi pakett-töö

Töötlemise voogude pakett-tööde vaatamiseks valige tegevuspaanil **Pakett-tööd** lehel **Kõik vood**.

Siit saate vaadata iga pakett-töö ID kohta kõiki partii ülesande üksikasju.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]