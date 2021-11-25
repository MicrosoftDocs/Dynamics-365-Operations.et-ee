---
title: Pakett-töödes väljaminevate saadetiste kinnitamine
description: Selles teemas kirjeldatakse, kuidas seadistada pakett-tööd, mis kinnitab automaatselt väljaminevad üleviimistellimuse saadetised saatmisvalmis koorma jaoks.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 4af84383fe1d214849d5d05463bd0cbfad7d0536
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778469"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>Pakett-töödes väljaminevate saadetiste kinnitamine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas seadistada pakett-tööd, mis kinnitab automaatselt väljaminevad üleviimistellimuse saadetised saatmisvalmis koorma jaoks. Siin kirjeldatud pakett-tööd rakendatakse ainult üleviimistellimuste saadetiste, mitte müügitellimuste puhul.

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a>Funktsiooni „Pakett-töödes väljaminevate saadetiste kinnitamine” lubamine

Tarneahela halduse versiooni 10.0.21 puhul on see funktsioon vaikimisi sisse lülitatud. Administraatorid saavad funktsioonihalduse [lehte](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) kasutada, et kontrollida funktsiooni olekut ja lubada või keelata see, kui vaja. Siin on funktsioon loetletud järgmiselt.

- **Moodul** - *laohaldus*
- **Funktsiooni nimi** - *Pakett-töödes väljaminevate saadetiste kinnitamine*

## <a name="process-outbound-shipments"></a>Väljaminevate saadetiste töötlemine

Selleks, et seadistada planeeritud pakett-töö kinnitama väljaminevaid saadetisi koormate jaoks, mis on saatmiseks valmis, tehke järgmist.

1. Avage **Laohaldus \> Perioodilised ülesanded \> Väljaminevate saadetiste töötlemine**.
1. Avaneb dialoogiboks **Saadetise kinnitamine**. Valige kiirkaardil **Kaasatavad kirjed** suvand **Filter**.
1. Avaneb päringuredaktori dialoogiboks. Lisage vahekaardil **Vahemik** järgmiste väärtustega uus rida.
    - **Tabel** - *Koormad*
    - **Tuletatud tabel** - *Koormad*
    - **Väli** - *Koorma olek*
    - **Kriteerium** - *Laaditud*
1. Valige **OK**, et naasta dialoogiboksi **Saadetise kinnitamine**.
1. Seadke kiirkaardil **Käivita taustal** suvandi **Pakktöötlus** väärtuseks **Jah**.
1. Valige kiirkaardil **Käivita taustal** suvand **Kordumine**.
1. Avaneb dialoogiboks **Kordumise määratlemine**. Seadistage käivitusgraafik oma ettevõtte vajaduste järgi.
1. Valige **OK**, et naasta dialoogiboksi **Saadetise kinnitamine**.
1. Valige **OK** dialoogiboksis **Saadetise kinnitamine**, et lisada pakett-töö pakktöötluse järjekorda.

Lisateavet leiate teemast [Pakktöötluse ülevaade](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]