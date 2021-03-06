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
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 69e61e1c04dd72efbe1d2f028c078100e07176f6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838438"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>Pakett-töödes väljaminevate saadetiste kinnitamine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas seadistada pakett-tööd, mis kinnitab automaatselt väljaminevad üleviimistellimuse saadetised saatmisvalmis koorma jaoks. Siin kirjeldatud pakett-tööd rakendatakse ainult üleviimistellimuste saadetiste, mitte müügitellimuste puhul.

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a>Funktsiooni „Pakett-töödes väljaminevate saadetiste kinnitamine” lubamine

Enne selle funktsiooni kasutamist tuleb see teie süsteemis lubada. Administraatorid saavad kasutada [funktsioonide halduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lehte, et kontrollida funktsiooni olekut ja vajaduse korral see lubada. Funktsioon on loetletud järgmiselt.

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