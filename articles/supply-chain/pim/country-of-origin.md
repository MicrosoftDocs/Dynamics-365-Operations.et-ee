---
title: Päritoluriik
description: Paljud organisatsioonid väljastavad oma hankijatele sertifikaate, et tagada toodete vastavuse kindlatele sertifitseerimisstandarditele. Need sertifikaadid sõltuvad sageli päritoluriigist. Selles teemas antakse teavet päritoluriigi funktsiooni kohta, mis võimaldab teil seostada toodet selle päritoluriigiga ja jälgida toote sertifikatsioone.
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: fd234c57bf9893e9b8bcfa5ada7439a642f7a288
ms.sourcegitcommit: 70d0b4e6bdacc15ec75935550ae55fc02cb79624
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/15/2020
ms.locfileid: "3596222"
---
# <a name="country-of-origin"></a>Päritoluriik

[!include [banner](../includes/banner.md)]

Paljud organisatsioonid väljastavad oma hankijatele sertifikaate, et tagada toodete vastavuse kindlatele sertifitseerimisstandarditele. Need sertifikaadid sõltuvad sageli päritoluriigist. Päritoluriigi funktsioon võimaldab teil seostada toodet selle päritoluriigiga ja jälgida toote sertifikatsioone.

## <a name="configure-source-and-destination-countries"></a>Lähte- ja sihtkriikide konfigureerimine

Enne tootele sertifikatsiooni väljastamist, peate linkima toote selle sihtriigi ja päritoluriigiga.

1. Avage jaotis **Tooteteabe haldus \> Seadistamine \> Toote vastavus \> Päritoluriik \> Päritoluriigi reeglid**.
2. Valige redigeerimiseks olemasolev riigi häälestus või valige toimingupaanilt **Uus** uue riigi häälestuse loomiseks.
3. Määrake valitud või uue riigi jaoks järgmised väärtused.

    | Field | Kirjeldus |
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

    | Field | Kirjeldus |
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

![Päritoluriigi aruanne](media/country-of-origin-report.png "Päritoluriigi aruanne")
