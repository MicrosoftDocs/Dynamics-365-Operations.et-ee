---
title: Konfiguratsiooni importimine teenusest Lifecycle Services
description: See artikkel kirjeldab, kuidas importida elutsükli teenustest (LCS) elektroonilise aruandluse (ER) Microsoft Dynamics konfiguratsiooni uut versiooni.
author: kfend
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
ms.openlocfilehash: 92c5d010430b38cb6c11a87283a2f7d4c29484f8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290360"
---
# <a name="import-a-configuration-from-lifecycle-services"></a>Konfiguratsiooni importimine teenusest Lifecycle Services

[!include [banner](../../includes/banner.md)]

See artikkel selgitab [, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli kasutaja saab importida elektroonilise aruandluse (ER)](../general-electronic-reporting.md#Configuration)[konfiguratsiooni uut versiooni projektitaseme](../../lifecycle-services/asset-library.md)Microsoft Dynamics varateegist elutsükli teenustes (LCS).

> [!IMPORTANT]
> LCS kasutamine elektroonilise aruandluse (ER) konfiguratsiooni talletushoidlana on [aegunud](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Lisateavet vt jaotisest [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) ladustamise amortiseerimine](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).

Selles näites valite soovitud ER-i konfiguratsiooni ja impordite selle näidisettevõttele Litware, Inc. Neid etappe saab läbida mis tahes ettevõttes, kuna ER-konfiguratsioonid on ettevõtete seas ühiskasutuses. Etappide lõpule viimiseks, peate esmalt läbima protseduuri [Konfiguratsiooni üleslaadimine teenusesse Lifecycle Services](er-upload-configuration-into-lifecycle-services.md) etapid. Samuti on nõutav juurdepääs LCS-ile.

1. Logige rakendusse sisse, kasutades üht järgmistest rollidest.

    - Elektroonilise aruandluse arendaja
    - Süsteemiadministraator

2. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
3. Valige **Konfiguratsioonid**.

<a name="accessconditions"></a>
> [!NOTE]
> Veenduge, et praegune Dynamics 365 Finance kasutaja on LCS-i [projekti](../../lifecycle-services/asset-library.md#asset-library-support) liige, mis sisaldab varateeki, mille kasutaja soovib ER-i konfiguratsioonide importimiseks kasutada.
>
> Te ei pääse LCS-i projektile juurde ER-hoidlast, mis esindab rakenduses Finance kasutatavast domeenist erinevat domeeni. Kui proovite, kuvatakse LCS-i projektide tühi loend ja te ei saa importida ER-konfiguratsioone LCS-i projekti tasandi varade teegist. Projekti tasandi varade teekidele juurde pääsemiseks ER-konfiguratsioonide importimiseks kasutatavast ER-hoidlast logige rakendusse Finance sisse selle kasutaja mandaadi abil, kes kuulub rentnikku (domeeni), kelle jaoks praegune rakenduse Finance eksemplar on ette valmistatud.

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a>Andmemudeli konfiguratsiooni ühiskasutuses versiooni kustutamine

1. Valige lehe **Konfiguratsioonid** konfiguratsioonide puult suvand **Mudeli konfiguratsiooni näide**.

    Lõite andmemudeli konfiguratsiooni esimese versiooni ja avaldasite selle LCS-is, kui täitsite protsessi [Konfiguratsiooni üleslaadimine teenusesse Lifecycle Services](er-upload-configuration-into-lifecycle-services.md) etappe. Selle protseduuri käigus kustutate selle ER-i konfiguratsiooni versiooni. Seejärel impordite selle versiooni LCS-st hiljem selles artiklis.

2. Otsige loendist ja valige soovitud kirje.

    Valige selles näites selle konfiguratsiooni versioon, mille olek on **Ühiskasutuses**. See olek näitab, et konfiguratsioon on avaldatud LCS-is.

3. Valige käsk **Muuda olekut**.
4. Valige nupp **Katkesta**.

    Muutes valitud versiooni oleku **Ühiskasutuses** olekuks **Katkestatud** muudetakse see kustutamiseks kättesaadavaks.

5. Valige nupp **OK**.
6. Otsige loendist ja valige soovitud kirje.

    Valige selles näites selle konfiguratsiooni versioon, mille olek on **Katkestatud**.

7. Valige **Kustuta**.
8. Valige **Jah**.

    Pange tähele, et nüüd on saadaval ainult valitud andmemudeli konfiguratsiooni mustandversioon 2.

9. Sulgege leht.

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a>Andmemudeli konfiguratsiooni ühiskasutuses versiooni importimine LCS-ist

1. Avage **Organisatsiooni haldamine \> Tööruumid \> Elektrooniline aruandlus**.

2. Valige jaotises **Konfiguratsiooni pakkujad** paan **Litware, Inc.**.

3. Valige paanil **Litware, Inc.** suvand **Hoidlad**.

    See võimaldab avada ettevõtte Litware, Inc. konfiguratsioonipakkuja hoidlate loendi.

4. Valige **Avamine**.

    Selle näite korral valige **LCS**-i hoidla ja avage see. Teil peab olema [juurdepääs](#accessconditions) LCS-i projektile ja varade teegile, millele valitud ER-hoidla juurde pääseb.

5. Märkige loendis valitud rida.

    Valige selles näites versiooni loendist suvandi **Mudeli konfiguratsiooni näide** esimene versioon.

6. Valige **Impordi**.
7. Valige **Jah**, et kinnitada valitud versiooni import LCS-ist.

    Teade kinnitab, et valitud versioon on imporditud.

8. Sulgege leht.
9. Sulgege leht.
10. Valige **Konfiguratsioonid**.
11. Valige puul väärtus **Mudeli konfiguratsiooni näide**.
12. Otsige loendist ja valige soovitud kirje.

    Valige selles näites selle konfiguratsiooni versioon, mille olek on **Ühiskasutuses**.

    Pange tähele, et nüüd on saadaval ka valitud andmemudeli konfiguratsiooni ühiskasutatav versioon 1.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
