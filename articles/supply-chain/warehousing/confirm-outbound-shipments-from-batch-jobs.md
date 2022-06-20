---
title: Pakett-töös väljuvate saadetiste kinnitamine
description: See artikkel kirjeldab, kuidas seadistada pakett-tööd, mis kinnitab automaatselt väljaminevad üleviimistellimuse saadetised valmissaadetise koormate jaoks.
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
ms.openlocfilehash: 00749a69b17b0064290d7b41ccb2171386716302
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875097"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>Pakett-töös väljuvate saadetiste kinnitamine

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas seadistada pakett-tööd, mis kinnitab automaatselt väljaminevad üleviimistellimuse saadetised valmissaadetise koormate jaoks. Siin kirjeldatud pakett-tööd rakendatakse ainult üleviimistellimuste saadetiste, mitte müügitellimuste puhul.

## <a name="turn-the-confirm-outbound-shipments-from-batch-jobs-feature-on-or-off"></a>Pakett-töödest väljaminevate saadetiste kinnitamise funktsiooni sisse- või väljalülitamine

Selles artiklis kirjeldatud funktsioonide kasutamiseks peab *funktsioon* Pakett-töödest väljaminevate saadetiste kinnitamine olema teie süsteemi jaoks sisse lülitatud. Tarneahela halduse versiooni 10.0.21 puhul on see funktsioon vaikimisi sisse lülitatud. Tarneahela halduse 10.0.25 puhul on see funktsioon kohustuslik ja seda ei saa välja lülitada. Kui käitate versiooni, mis on *vanem kui 10.0.25, saavad administraatorid selle funktsiooni sisse või välja lülitada, otsides funktsioonihalduse tööruumi pakett-tööde*[funktsioonist](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) Väljaminevate saadetiste kinnitust.

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