---
title: "Koosluse- ja valemiridade lattu väljastamine"
description: "Selles teemas kirjeldatakse koosluseridade ja valemiridade toormaterjali lattu väljastamise protsessi."
author: johanhoffmann
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: johanho
ms.search.validfrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 83648a93f367510d7b04bbd04a9f37689ecfaa59
ms.openlocfilehash: 2bccabb033f5ba142b145e69930ce516aad596f2
ms.contentlocale: et-ee
ms.lasthandoff: 05/23/2018

---

# <a name="release-bom-and-formula-lines-to-the-warehouse"></a>Koosluse- ja valemiridade lattu väljastamine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse koosluseridade ja valemiridade toormaterjali lattu väljastamise protsessi. Koosluse- või valemirea väljastamisel lattu tuvastab süsteem kõigepealt selle, kas materjal on juba saadaval tootmise sisendasukohas tööde juhtimise moodulis, kus materjali tarbitakse tootmisprotsessi jaoks.

- Kui materjal on tootmise sisendasukohas saadaval, komplekteeritakse see sellest asukohast kohe, kui antakse signaal materjali väljastamiseks lattu.
- Kui materjal pole tootmise sisendasukohas saadaval, näitab materjali väljastamine, et materjal tuleb liigutada lao asukohtadest tootmise sisendasukohta. Materjal liigutatakse laotöö kaudu toormaterjali komplekteerimiseks. Seetõttu peavad olema konfigureeritud laoprotsessid toormaterjali komplekteerimiseks. Lisateavet vaadake teemadest [Täiendamine](../warehousing/replenishment.md) ja [Laotöö juhtimine, kasutades töömalle ja asukohadirektiive](../warehousing/control-warehouse-location-directives.md).

## <a name="methods-for-releasing-bom-and-formula-lines"></a>Koosluse- ja valemiridade väljastamise meetodid

Koosluse- ja valemiridade väljastamise saate konfigureerida nii, et see toimub tootmistellimuse või partiitellimuse väljastamise osana. Väljastamist saab juhtida ka pakett-tööna või teha käsitsi interaktsioonina.

Meetodit, mida kasutatakse koosluse- ja valemiridade väljastamiseks, juhitakse parameetriga **Tootmisrea väljastamine**. Leiate selle parameetri jaotisest **Tootmise juhtimine** \> **Seadistus** \> **Tootmise parameetrid**.

- **Koosluse- ja valemiridade väljastamine tootmis- või partiitellimuse väljastamise osana** – selle meetodi puhul väljastatakse koosluse- ja valemiread tootmis- või partiitellimuse puhul osana tellimuse väljastamise protsessist. Tavaliselt väljastatakse tootmistööd tootmis- või partiitellimuse väljastamisel tööde juhtimise mooduli töötajatele ja prinditakse tootmisdokumendid. Selle protsessi käigus muudetakse selle tellimuse olekuks **Väljastatud**.
- **Koosluse- ja valemiridade väljastamine pakett-töö kaudu või käsitsi interaktsioonina** – selle meetodi puhul saab koosluse- ja valemiridu väljastada ainult pakett-töö **Koosluse- ja valemiridade automaatne väljastamine** kaudu või käsitsi interaktsioonina. Koosluse- ja valemiridade käsitsi väljastamiseks valige toimingupaanil tootmistellimuse loendilehel või tootmistellimuse üksikasjade lehel käsk **Väljasta lattu**.

Kiiret demonstratsiooni selle kohta, kuidas väljastada koosluse- ja valemiridasid tootmisse, kasutades pakett-tööd, saate vaadata järgmisest lühikesest YouTube’i videost: [Tootmise komplekteerimise väljastamine partiis olevasse lattu](https://www.youtube.com/watch?v=8urAJn50dQ8).

## <a name="releasing-the-bom-and-formula-lines-by-using-a-batch-job"></a>Koosluse- ja valemiridade väljastamine pakett-töö abil

Pakett-töö **Koosluse- ja valemiridade automaatne väljastamine** liigub läbi valitud koosluse- ja valemiridade, millel on väljastamiseks järelejäänud kogus. Töö võtab arvesse ainult tellimusi, mille olek on **Väljastatud**, **Alustatud** või **Lõpetatuna teatatud**. Kui koosluse- või valemireal on väljastamiseks järelejäänud kogus, väljastab töö kuni koguse, mille saab katta kogusega, mis on juba füüsiliselt reserveeritud, ja kogusega, mis on füüsiliselt saadaval.

### <a name="example-of-a-batch-job-release"></a>Pakett-töö kaudu väljastamise näide

| Stsenaarium | Väljastamiseks järelejäänud kogus | Füüsiliselt reserveeritud kogus | Füüsiliselt saadaolev kogus | Pakett-tööga väljastatud kogus |
|----------|-------------------------------|------------------------------|-------------------------------|------------------------------------|
| 1        | 100                           | 20                           | 90                            | 100                                |
| 2        | 100                           | 20                           | 70                            | 90                                 |
| 3        | 100                           | 0                            | 90                            | 90                                 |
| 4        | 100                           | 0                            | 110                           | 100                                |
| 5        | 100                           | 20                           | 0                             | 20                                 |

### <a name="batch-job-setup"></a>Pakett-töö seadistamine

Pakett-töö **Koosluse- ja valemiridade automaatne väljastamine** päringus saate seadistada filtreerimiskriteeriumid, et määrata, kui palju päevi eelnevalt peaks töö otsima ridu, millel on väljastamata koguseid. Töö päringus kasutage väljal **Toormaterjali kuupäev** filtreerimiskriteeriumina funktsiooni **(LessThanDate())**.

Järgmisel joonisel on kujutatud tootmistellimus, millel on kaks tööd, 10 ja 20, mis hõlmavad tootmistellimuse koostamist ja pakkimist. Iga töö seadistatakse tarbima materjalikogust. Selles näites võrdub ajajoone all rohelise allanoolega tähistatud väljastamise ajapiir kriteeriumis **(LessThanDate())** määratud päevade arvuga. Näiteks **(LessThanDate(2))** näitab, et töö peaks otsima väljastamata koguseid ainult kahepäevases ajavahemikus.

![Kahe pakett-tööga tootmistellimuse näide](media/bach-job-setup.PNG)

## <a name="releasing-material-per-operation-number-or-in-proportion-to-the-amount-of-finished-goods"></a>Materjali väljastamine toimingu numbri järgi või proportsionaalselt lõpetatud kaupade hulgaga.

Kui väljastate käsitsi väljastamise ajal materjale, kasutades parameetrisätet **Tootmistellimuse väljastamisel**, on teil materjali väljastamise juhtimiseks kaks võimalust.

- Materjali väljastamine toimingu numbri järgi.
- Materjali väljastamine proportsionaalselt lõpetatud kaupade hulgaga.

### <a name="release-material-per-operation-number"></a>Materjali väljastamine toimingu numbri järgi

Toimingute juhtimiseks, millele tuleb materjali väljastada, kasutage lehte **Lattu väljastamine**.

- Valige suvandid **Tootmise juhtimine** \> **Tootmistellimused** \> **Kõik tootmistellimused**, seejärel valige tootmistellimus ja siis valige vahekaardil **Ladu** suvand **Lattu väljastamine**. Seejärel kasutage välju **Toimingu nr-st** ja **Toimingu nr-ni**, et määrata toimingunumbrite vahemik.

Järgmisel joonisel on kujutatud tootmistellimus, millel on kaks toimingut, 10 ja 20. Kui piirate selles näites väljastamise toiminguga 10, väljastatakse ainult materjal M9203.

![Materjali väljastamise näide toimingu numbri järgi](media/two-operations.PNG)

Kiiret demonstratsiooni selle kohta, kuidas väljastada materjali proportsionaalselt lõpetatud kaupade hulgaga, saate vaadata järgmisest lühikesest YouTube’i videost: [Tootmistellimuse väljastusprotsessi täiustused rakenduses Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=Rm3ojAz6Zu0)

### <a name="release-material-in-proportion-to-the-amount-of-finished-goods"></a>Materjali väljastamine proportsionaalselt lõpetatud kaupade hulgaga

Saate väljastada toormaterjali lõpetatud kaupade osalise koguse jaoks või kindlates ühikutes.

- Toormaterjali väljastamiseks lõpetatud kaupade osalise koguse jaoks valige suvandid **Tootmise juhtimine** \> **Tootmistellimused** \> **Kõik tootmistellimused**, seejärel valige tootmistellimus ja siis valige vahekaardil **Ladu** suvand **Lattu väljastamine**. Seejärel sisestage kogus väljale **Kogus**.

    Näiteks luuakse tootmistellimus ja kavandatakse 1000 tükki (tk). Tööde juhtimise mooduli järelevaataja planeerib järgmises vahetuses 100 tk tootmist ja soovib väljastada materjale ainult selle vahetuse jaoks. Sel juhul saab ülevaataja kasutada välja **Kogus**, et väljastada 100 tk. materjale, mis on järgmise vahetuse jaoks planeeritud.

- Toormaterjali väljastamiseks kindlates ühikutes valige suvandid **Tootmise juhtimine** \> **Tootmistellimused** \> **Kõik tootmistellimused**, seejärel valige tootmistellimus ja siis valige vahekaardil **Ladu** suvand **Lattu väljastamine**. Seejärel kasutage välja **Ühik**, et valida lõpetatud kaupade ühik, milles materjali väljastada.

    Saadaolevad ühikud on määratletud lõpetatud kauba ühiku seeriagrupi ID-s.

    Näiteks on lõpetatud kaubal järgmised ühikuteisendused kilogrammide (kg) ja kaubaaluste (PL) vahel: 1 PL = 100 kg. Tootmistellimuse loomiseks 10 000 kg lõpetatud kauba jaoks saate väljastada toormaterjale kaubaaluste arvule, mida plaanite toota. Valige ühikuna **PL** ja siis valige vastav arv väljal **Kogus**.

