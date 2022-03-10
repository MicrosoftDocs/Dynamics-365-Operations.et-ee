---
title: Päritoluriik
description: Paljud organisatsioonid väljastavad oma hankijatele sertifikaate, et tagada toodete vastavuse kindlatele sertifitseerimisstandarditele. Need sertifikaadid sõltuvad sageli päritoluriigist. Selles teemas antakse teavet päritoluriigi funktsiooni kohta, mis võimaldab teil seostada toodet selle päritoluriigiga ja jälgida toote sertifikatsioone.
author: t-benebo
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: COOVendorCerts
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: a2740f6b1ccb52073b013e613d8ab779cc088180
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/09/2021
ms.locfileid: "7777617"
---
# <a name="country-of-origin"></a>Päritoluriik

[!include [banner](../includes/banner.md)]

Paljud organisatsioonid väljastavad oma hankijatele sertifikaate, et tagada toodete vastavuse kindlatele sertifitseerimisstandarditele. Need sertifikaadid sõltuvad sageli päritoluriigist. Päritoluriigi funktsioon võimaldab teil seostada toodet selle päritoluriigiga ja jälgida toote sertifikatsioone.

## <a name="turn-on-the-country-of-origin-feature"></a>Päritoluriigi funktsiooni sisselülitamine

Tarneahela halduse versiooni 10.0.21 puhul on see funktsioon vaikimisi sisse lülitatud. Administraatorid saavad funktsioonihalduse [lehte](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) kasutada, et kontrollida funktsiooni olekut ja lubada või keelata see, kui vaja. Siin on funktsioon loetletud järgmiselt.

- **Moodul:** *Tooteteabe haldus*
- **Funktsiooni nimi:** *päritoluriigi haldamise funktsioon*

## <a name="configure-source-and-destination-countries"></a>Lähte- ja sihtkriikide konfigureerimine

Enne tootele sertifikatsiooni väljastamist, peate linkima toote selle sihtriigi ja päritoluriigiga.

1. Avage jaotis **Tooteteabe haldus \> Seadistamine \> Toote vastavus \> Päritoluriik \> Päritoluriigi reeglid**.
2. Valige redigeerimiseks olemasolev riigi häälestus või valige toimingupaanilt **Uus** uue riigi häälestuse loomiseks.
3. Määrake valitud või uue riigi jaoks järgmised väärtused.

    | Väli | Kirjeldus |
    |---|---|
    | Kauba number | Valige toote kaubakood. |
    | Sihtriik | Valige riik, kuhu te toote saadate. |
    | Päritoluriik | Valige riik, kust te toodet saadate. |

Selle seadistuse eesmärk on aidata teil luua koosluste aruanne, kus saate lisada päritoluriigi igale osale, mille jaoks lähte-ja sihtriigid määratakse. See aruanne aitab teil saada terviklikku ülevaadet sellest, kust teie osad pärit on ja kuhu need lähevad.

## <a name="keep-track-of-vendor-certificates"></a>Hankija sertifikaatide jälgimine

Saate kasutada lehte **Päritoluriigi hankija sertifikaadid**, et jälgida hankijatele väljastatavaid sertifikaate.

Peate otsustama, milliseid sertifikaadi dokumente te väljastate ja kuidas te neid klientidele teatate. See funktsioon annab teile sertifikaatidest ülevaate. Samuti saate valida, kas vastavad sertifikaadi numbrid kuvatakse arvetel, saatelehtedel ja/või tellimuse kinnitustel.

Sertifikaadi teabe häälestamiseks toimige järgmiselt.

1. Avage jaotis **Tooteteabe haldus \> Seadistamine \> Toote vastavus \> Päritoluriik \> Päritoluriigi hankija sertifikaadid**.
2. Valige redigeerimiseks olemasolev sertifikaadi häälestus või valige toimingupaanilt **Uus** uue sertifikaadi häälestuse loomiseks.
3. Määrake valitud või uue sertifikaadi jaoks järgmised sätted.

    | Väli | Kirjeldus |
    |---|---|
    | Hankija konto | Valige hankija, kellele väljastasite sertifikaadi. |
    | Kauba number | Valige kaup, millele väljastasite sertifikaadi. |
    | Riik/regioon | Sihtriik või -piirkond, kus peate seda sertifikaati kasutama. |
    | Serdi number | Sisestage väljastatud sertifikaadi ID-number. |
    | Jõustunud | Valige praeguse sertifikaadi kehtivuse esimene kuupäev.|
    | Aegumine | Valige praeguse sertifikaadi kehtivuse viimane kuupäev. |
    | Arvele printimine | Märkige see ruut, et printida sertifikaadi number arvetele, mis on adresseeritud määratud riigile kindlal kuupäevavahemikul. |
    | Saatelehele printimine | Märkige see ruut, et printida sertifikaadi number saatelehtedele, mis on adresseeritud määratud riigile kindlal kuupäevavahemikul. |
    | Müügitellimusele printimine | Märkige see ruut, et printida sertifikaadi number müügitellimustele, mis on adresseeritud määratud riigile kindlal kuupäevavahemikul. |

## <a name="include-the-country-of-origin-on-bom-reports"></a>Päritoluriigi koosluse aruannete lisamine

Kui loote koosluse aruande, saate lisada päritoluriigi igale osale, millele määrasite lähte- ja sihtriiriigid lehel **Päritoluriigi reeglid**.

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Valige või looge toode, et avada selle leht **Väljastatud toote üksikasjad**.
1. Tehke tegumiriba vahekaardil **Projekteeri** grupis **Kooslus** valik **Kujundaja**.
1. Valige kuvatava lehe toimingupaanilt **Kooslus \> Prindi**.
1. Määrake dialoogiboksi **Koosluse read** väljale **Sihtriik** see sihtriik, mida soovite oma aruandes kuvada.
1. Valige nupp **OK**.

Luuakse ja kuvatakse aruanne teabega iga osa päritoluriigi kohta. Siin on aruande näide.

![Päritoluriigi aruanne.](media/country-of-origin-report.png "Päritoluriigi aruanne")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]