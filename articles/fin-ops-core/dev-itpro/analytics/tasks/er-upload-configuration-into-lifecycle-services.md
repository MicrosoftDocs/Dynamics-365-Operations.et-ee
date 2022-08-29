---
title: Konfiguratsiooni üleslaadimine teenusesse Lifecycle Services
description: See artikkel selgitab, kuidas luua uus elektroonilise aruandluse (ER) konfiguratsioon ja laadida see üles elutsükli Microsoft Dynamics teenustesse (LCS).
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
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
ms.openlocfilehash: 28ad20956b4b621abdb74332187d8601c10ac164
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290060"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a>Konfiguratsiooni üleslaadimine teenusesse Lifecycle Services

[!include [banner](../../includes/banner.md)]

See artikkel selgitab [, kuidas kasutaja süsteemiadministraatoris või elektroonilise aruandluse arendaja rollis saab luua uue elektroonilise aruandluse (ER)](../general-electronic-reporting.md#Configuration)[konfiguratsiooni ja laadida selle üles projekti tasemel](../../lifecycle-services/asset-library.md)Microsoft Dynamics varateeki elutsükli teenustes (LCS).

> [!IMPORTANT]
> LCS kasutamine elektroonilise aruandluse (ER) konfiguratsiooni talletushoidlana on [aegunud](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Lisateavet vt jaotisest [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) ladustamise amortiseerimine](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).

Selles näites loote konfiguratsiooni näidisettevõttele Litware, Inc. ja laadite selle üles LCS-i. Neid etappe saab teha mis tahes ettevõttes, kuna ER-konfiguratsioonid on ettevõtetel ühised. Etappide lõpuleviimiseks, peate esmalt läbima etapid teemas [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](er-configuration-provider-mark-it-active-2016-11.md). Samuti on nõutav juurdepääs LCS-ile.

1. Logige rakendusse sisse, kasutades üht järgmistest rollidest.

    - Elektroonilise aruandluse arendaja
    - Süsteemiadministraator

2. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
3. Valige **Litware, Inc.** ja sejärel valige **Aktiivne**.
4. Valige **Konfiguratsioonid**.

<a name="accessconditions"></a>
> [!NOTE]
> Veenduge, et praegune Dynamics 365 Finance kasutaja on ER-i konfiguratsioonide importimiseks kasutatavat varateeki sisaldava LCS-projekti [liige](../../lifecycle-services/asset-library.md#asset-library-support).
>
> Te ei pääse LCS-i projektile juurde ER-hoidlast, mis esindab rakenduses Finance kasutatavast domeenist erinevat domeeni. Kui proovite, kuvatakse LCS-i projektide tühi loend ja te ei saa importida ER-konfiguratsioone LCS-i projekti tasandi varade teegist. Projekti tasandi varade teekidele juurde pääsemiseks ER-konfiguratsioonide importimiseks kasutatavast ER-hoidlast logige rakendusse Finance sisse selle kasutaja mandaadi abil, kes kuulub rentnikku (domeeni), kelle jaoks praegune rakenduse Finance eksemplar on ette valmistatud.

## <a name="create-a-new-data-model-configuration"></a>Uue andmemudeli konfiguratsiooni loomine

1. Minge jaotisse **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Konfiguratsioonid**.
2. Rippmenüü dialoogiboksi avamiseks valige lehel **Konfiguratsioonid** käsk **Loo konfiguratsioon**.

    Selles näites loote konfiguratsiooni, mis sisaldab elektrooniliste dokumentide andmemudeli näidist. Selle andmemudeli konfiguratsioon laaditakse hiljem LCS-i.

3. Tippige väljale **Nimi** tekst **Mudeli konfiguratsiooni näide**.
4. Tippige väljale **Kirjeldus** tekst **Mudeli konfiguratsiooni näide**.
5. Valige **Konfiguratsiooni loomine**.
6. Valige **Mudeli koostaja**.
7. Valige suvand **Uus**.
8. Väljale **Nimi** sisestage **Sisenemiskoht**.
9. Valige **Lisa**.
10. Valige käsk **Salvesta**.
11. Sulgege leht.
12. Valige käsk **Muuda olekut**.
13. Valige **Lõpeta**.
14. Valige nupp **OK**.
15. Sulgege leht.

## <a name="register-a-new-repository"></a>Uue hoidla registreerimine

1. Avage **Organisatsiooni haldamine \> Tööruumid \> Elektrooniline aruandlus**.

2. Valige jaotises **Konfiguratsiooni pakkujad** paan **Litware, Inc.**.

3. Valige paanil **Litware, Inc.** suvand **Hoidlad**.

    See võimaldab avada ettevõtte Litware, Inc. konfiguratsioonipakkuja hoidlate loendi.

4. Valige **Lisa**, et avada rippmenüü dialoogiaken.

    Nüüd saate lisada uue hoidla.

5. Sisestage väljale **Konfiguratsioonihoidla** valik **LCS**.
6. Valige käsk **Loo hoidla**.
7. Valige või sisestage väärtus väljal **Projekt**.

    Selle näite korral valige soovitud LCS-i projekt. Teil peab olema [juurdepääs](#accessconditions) projektile.

8. Valige nupp **OK**.

    Täitke uus hoidla kirje.

9. Märkige loendis valitud rida.

    Selle näite korral valige **LCS**-i hoidla kirje.

    Pange tähele, et registreeritud hoidla on praeguse pakkuja poolt märgitud. Teisisõnu saab sellesse hoidlasse panna ainult selle pakkuja omanduses olevaid konfiguratsioone ja seetõttu valitud LCS-i projekti üles laadida.

10. Valige **Avamine**.

    Avage hoidla ER-i konfiguratsioonide loendi vaatamiseks. Loend on tühi, kui valitud projekti pole veel kasutatud ER-i konfiguratsioonide ühiskasutuseks.

11. Sulgege leht.
12. Sulgege leht.

## <a name="upload-a-configuration-into-lcs"></a>Konfiguratsiooni üleslaadimine LCS-i

1. Minge jaotisse **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Konfiguratsioonid**.
2. Valige lehe **Konfiguratsioonid** konfiguratsioonide puult suvand **Mudeli konfiguratsiooni näide**.

    Peate valima loodud konfiguratsiooni, mis on juba lõpule viidud.

3. Otsige loendist ja valige soovitud kirje.

    Valige selles näites valitud konfiguratsiooni versioon, mille olek on **Lõpule viidud**.

4. Valige käsk **Muuda olekut**.
5. Valige **Anna ühiskasutusse**.

    Kui konfiguratsioon avaldatakse LCS-is, muudetakse konfiguratsiooni olek **Lõpule viidud** olekuks **Ühiskasutuses**.

6. Valige nupp **OK**.
7. Otsige loendist ja valige soovitud kirje.

    Valige selles näites selle konfiguratsiooni versioon, mille olek on **Ühiskasutuses**.

    Pange tähele, et valitud versiooni olek **Lõpule viidud** muudeti olekuks **Ühiskasutuses**.

8. Sulgege leht.
9. Valige **Osad**.

    See võimaldab avada ettevõtte Litware, Inc. konfiguratsioonipakkuja hoidlate loendi.

10. Valige **Avamine**.

    Selle näite korral valige **LCS**-i hoidla ja avage see.

    Pange tähele, et valitud konfiguratsiooni näidatakse valitud LCS-i projekti varana.

11. Avage LCS, minnes saidile <https://lcs.dynamics.com>.
12. Avage projekti, mida kasutati varem hoidla registreerimiseks.
13. Avage projekti varade teek.
14. Valige **GER-i konfiguratsiooni** vara tüüp.

    Teie üleslaaditud ER-konfiguratsioon peaks olema loetletud.

    Pange tähele, et üleslaaditud LCS-i konfiguratsiooni saab importida teise eksemplari, kui teenuse pakkujatel on juurdepääs sellele LCS-i projektile.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
