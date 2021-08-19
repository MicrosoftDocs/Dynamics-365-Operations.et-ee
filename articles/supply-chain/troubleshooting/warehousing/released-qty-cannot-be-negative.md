---
title: Koormusrida ei saa värskendada, sest vabastatud kogus oleks negatiivne
description: See probleem ilmneb siis, kui koormusrea värskendamine või kustutamine põhjustaks negatiivse vabastatud koguse.
author: GalynaFedorova
ms.date: 6/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSLoadLineUnShipQty,WHSLoadTable_WHSLoadLineUnShipQty,WHSLoadPlanningWorkbench_WHSLoadLineUnShipQty,WHSShipmentDetails_WHSLoadLineUnShipQty,WHSLoadPlanningListPage_DeleteButtonLoadLine,WHSLoadTable_DeleteButtonLoadLine,WHSLoadPlanningWorkbench_DeleteButtonLoadLine,WHSShipmentDetails_DeleteButtonShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a6325a632e1f68a0a3a9cb6b6091c48da014a405e8ce9ad69ea841f5cceb216f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728455"
---
# <a name="cant-update-a-load-line-because-the-released-quantity-would-be-negative"></a>Koormusrida ei saa värskendada, sest vabastatud kogus oleks negatiivne

Tõrkekood: @WAX:ReleasedQtyCannotBeNegative

## <a name="symptoms"></a>Sümptomid

See probleem ilmneb siis, kui koormusrea värskendamine või kustutamine põhjustaks negatiivse vabastatud koguse. Sellisel juhul, kui proovite koormusrida värskendada või kustutada, kuvab süsteem järgmise tõrketeate:

> Vabastatud kogus ei saa olla kauba %1, saatepartii %2 jaoks negatiivne.

Seetõttu ei saa värskendada ega kustutada koormusrida.

## <a name="cause"></a>Põhjus

Pärast laadimisrea värskendamist või kustutamist uuendab süsteem seotud müügirea (*whsSalesLine.ReleaseQty*) vabastatud koguse. Süsteem hindab vabastatud kogust ja kui ta leiab, et rea vabastatud kogus oleks pärast värskendamist negatiivne, ei lase see teil rida värskendada ega kustutada. See valideerimine toimub alati, kui proovite värskendada koormusjoone kogust või mõõtühikut erinevate toimingute abil, näiteks laadimisjoone kustutamine, saadetise kustutamine, laadimisjoone koguse muutmine, valitud koguse vähendamine ja lühike valimine.

Selle probleemi kõige tavalisem algpõhjus on avatud koormusjoonte jaoks kasutatava ühiku teisenduse muutus. Näiteks ühiku konverteerimine müügitellimuse vabastamisel oli *50 Ea = 1 PL*. Kuid enne seotud lastisaadetise lõpetamist muudeti ühiku teisendamine *100 Ea = 1 PL*.

## <a name="resolution"></a>Lahendus

Lahenduseks on ühiku teisenduse muudatuste ennistamine, koormusrea värskendamine või kustutamine ja seejärel teisenduse uuesti rakendamine. Peate vältima muude koormuste, mis sisaldavad probleemi põhjustanud üksuse töötlemist kuni probleemi lahendamist. Vastasel juhul võidakse uusi teisendusi kasutada muude juba avatud koormuste puhul.

Selle probleemi lahendamiseks täitke üks järgmistest toimingutest:

1. Vaadake üle koormusrea jaoks kasutatud ühiku teisendus.
2. Vaadake üle kauba praegune ühikuteisendus ja tehke kohandusi, mis võimaldavad koormusrida uuendada või kustutada.
3. Uuendage või kustutage koormusrida ja taastage ühiku teisenduse korrigeerimised.

### <a name="review-the-unit-conversion-that-was-used-for-the-load-line"></a>Vaadake üle koormusrea jaoks kasutatud ühiku teisendus

Kasutage koormusridade ülevaatamiseks ja koormusrea jaoks kasutatud ühikuteisenduse kohta märkusi järgmise toimingu abil.

1. Avage **Laohaldus \> Koormad \> Kõik koormad**.
1. Valige koormus, mis sisaldab laadimisrida, mida ei saa kustutada ega värskendada.
1. Toimingupaani vahekaardil **Ladu** grupis **Seotud teave** valige **Töö**.
1. Valige ülemises ruudustikus vastav töö ID.
1. Arvutage lehe allosas vahekaardil **Üldine** **varude töökoguse** väärtuse ja **töökoguse** väärtuse vaheline teisenduskurss. Märkige määr üles.
1. Korrake seda toimingut kõigi asjakohaste töö ID-de puhul veendumaks, et kasutati sama teisendust.

### <a name="review-the-current-unit-conversion-for-the-item-and-make-adjustments"></a>Vaadake üle kauba praegune ühikuteisendus ja tehke korrigeerimisi

Kasutage järgmist protseduuri, et vaadata üle oma toote ühikute teisendamine ja teha kohandusi, et tagada ühikute teisendamine koormusjoonega.

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Avage asjakohane toode, et minna selle lehele **Väljaantud toote üksikasjad**.
1. Tehke Toimingupaani vahekaardil **Toode** grupis **Häälesta** valik **Ühiku teisendused**.
1. Valige ühikutevaheline teisendus ja tehke eelmisest jaotisest leitud teisenduse abil täpsustusi.

### <a name="update-or-delete-the-load-line-and-revert-the-unit-conversion-adjustments"></a>Uuendage või kustutage koormusrida ja taastage ühiku teisenduse korrigeerimised

Koormusrea töötlemiseks vastavalt vajadusele ja ühikute teisenduste taastamiseks kasutage järgmist toimingut.

1. Avage **Laohaldus \> Koormad \> Kõik koormad**.
1. Avage koormus, mis sisaldab laadimisrida, mida ei saa kustutada ega värskendada.
1. Valige kiirkaardil **Koormaread** koormarida.
1. Jätkake vajalike toimingutega vastavalt vajadusele. (Näiteks kustutage koormusrida või muutke selle kogust.)
1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Avage asjakohane toode, et minna selle lehele **Väljaantud toote üksikasjad**.
1. Tehke Toimingupaani vahekaardil **Toode** grupis **Häälesta** valik **Ühiku teisendused**.
1. Valige ühikute vaheline teisendus ja tühistage eelmises jaotises tehtud kohandused.
