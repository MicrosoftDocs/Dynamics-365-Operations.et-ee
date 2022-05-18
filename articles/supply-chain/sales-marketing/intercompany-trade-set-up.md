---
title: Kontsernisisese kaubanduse seadistamine
description: Selles teemas kirjeldatakse kontsernisisese kaubanduse seadistamist
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage, InterCompanyTradingRelationSetupCustomer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 5080267568f4d0626d2c727efb533295e7d8e397
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669386"
---
# <a name="set-up-intercompany-trade"></a>Kontsernisisese kaubanduse seadistamine

[!include [banner](../../includes/banner.md)]

Süsteemi Microsoft Dynamics 365 Supply Chain Management kaubanduse käitamiseks kontsernisiseselt peate kliendid ja hankijad vastavalt seadistama. Samuti peate seadistama Võlgnevused, Müügireskontro, Soetamise ja hanked ning Müügi ja turunduse.

## <a name="before-you-set-up-intercompany-trade"></a>Enne kontsernisisese kaubanduse seadistamist

Enne kontsernisisese kaubanduse seadistamist peate otsustama, millised teie kliendid on kontsernisisesed kliendid ja millised teie tarnijad on kontsernisisesed tarnijad. Iga juriidilise isiku kohta rakenduses Microsoft Dynamics 365 Supply Chain Management peate otsustama, millist kaubanduspoliitikat rakendada kontsernisisesele kaubandussuhtele koos konkreetse kontsernisisese kliendi või tarnijaga.

Eriti soovitame teil ja teie organisatsioonil tutvuda kontsernisiseste parameetritega.

- Arutlege seadistuse mõju üle halduritega, kes vastutavad iga juriidilise isiku kontsernisisese kaubanduse eest.
- Seadistage sobivad väärtused iga juriidilise isiku jaoks.

## <a name="set-up-trading-relations"></a>Saate häälestada kaubandussuhteid.

Klientide ja hankijate kontserni kaubavahetuse seadistamiseks järgige neid samme.

1. Avage **Müügireskontro \> Kliendid \> Kõik kliendid**.
1. Valige kliendi konto.
1. Toimingupaani vahekaardil **Üldine** valige suvand **Kontsernisisene**.
1. Määrake kliendi konto kontsernisisese seadistuse parameetrid. Need parameetrid hõlmavad juriidilist isikut, mis sisaldab vastavat hankijat ja hankijakontot. Need parameetrid hõlmavad ka hankija juriidilist isikut ja kontot, ostutellimuse poliitikaid, müügitellimuse poliitikaid, väärtuste vastendamist ning müügilepingu ja ostulepingu poliitikaid. Samuti saate määrata, kas kasutada põhiandmete väärtusi kliendi kontolt või hankija kontolt teises juriidilises isikus.
1. Korrake samme 1 kuni 4 ülejäänud kontsernisiseste klientidega juriidilises isikus.
1. Avage **Ostureskonto \> Müüjad \> Kõik müüjad**.
1. Valige hankija konto.
1. Toimingupaani vahekaardil **Üldine** valige suvand **Kontsernisisene**.
1. Määrake hankija konto kontsernisisese seadistuse parameetrid. Need parameetrid hõlmavad juriidilist isikut, mis sisaldab vastavat klienti ja kliendi kontot. Need parameetrid hõlmavad ka müügitellimuse poliitikaid, ostutellimuse poliitikaid, väärtuste vastendamist ning müügilepingu ja ostulepingu poliitikaid. Samuti saate määrata, kas kasutada põhiandmete väärtusi hankija kontolt või kliendi kontolt teises juriidilises isikus.
1. Korrake samme 6 kuni 9 ülejäänud kontsernisiseste hankijatega juriidilises isikus.

## <a name="set-up-products"></a>Seadistage tooted

Klientide ja hankijate kontserni kaubavahetuse seadistamiseks järgige neid samme.

1. Avage **Tooteteabe haldus \> Tooted \> Kõik tooted ja tooteetalonid**.
1. Määratlege tooted, mis vabastatakse juriidilistele isikutele, kus soovite teha kontsernisisest kaubandust.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
