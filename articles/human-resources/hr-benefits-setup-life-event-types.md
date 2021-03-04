---
title: Elusündmuse tüüpide konfigureerimine
description: Microsoft Dynamics 365 Human Resources kasutab elusündmuse tüüpe sündmuste määratlemiseks, kus kehtib töövõtja soodustuste registreerimise värskendamine.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5286bcd940f4068531bae624876c8a35e64db4c3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418140"
---
# <a name="configure-life-event-types"></a>Elusündmuse tüüpide konfigureerimine

Microsoft Dynamics 365 Human Resources kasutab elusündmuse tüüpe sündmuste määratlemiseks, kus kehtib töövõtja soodustuste registreerimise värskendamine. Näiteks abiellumine või lapse saamine. Iga elusündmuse tüübi ID võib olla seotud ainult ühe elusündmuse tüübiga. Näiteks kui loote elusündmuse ID nimega aadressi muutus, mis on seotud elusündmuse tüübiga Töövõtja aadressi muutus, ei saa te luua teist ID-d sildiga Töövõtja aadressi muutus ega seostada seda elusündmuse tüübiga Töövõtja aadressi muutus. 

Pärast elusündmuse tüüpide loomist peate need seostama plaani tüüpidega. Lisateabe saamiseks vt [Plaani tüüpide loomine](hr-benefits-setup-plan-types.md).

   > [!NOTE]
   > Elusündmuse loomisel peate selle seostama plaani tüübiga. Lisateabe saamiseks vt [Plaani tüüpide loomine](hr-benefits-setup-life-event-types.md).

## <a name="create-a-life-event-type"></a>Elusündmuse tüübi loomine

1. Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Elusündmuse tüübid**.

2. Valige suvand **Uus**.

3. Määrake järgmiste väljade väärtused.

   | Väli | Kirjeldus |
   | --- | --- |
   | **Elusündmuse tüübi ID** | Elusündmuse tüübi kordumatu identifikaator. |
   | **Kirjeldus** | Elusündmuse tüübi kirjeldus. |
   | **Elusündmuse tüüp** | Töövõtja soodustuste registreerimise uuendamise katalüsaator. Elusündmuste loendit vt allpool teemast [Elusündmused](hr-benefits-setup-payment-frequencies.md?life-events). |

4. Valige käsk **Salvesta**.

## <a name="view-attached-plans"></a>Lisatud plaanide kuvamine

Saate vaadata valitud elusündmuse tüübile lisatud plaanide loendit. Elusündmused on lisatud plaani tüübile ja plaani tüübid on seostatud plaaniga. 

1. Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Elusündmuse tüübid**.

2. Valige suvand **Tegevused**.

3. Valige suvand **Lisatud plaanid**.

## <a name="life-events"></a>Elusündmused

Elusündmuse tüübi loomisel saate valida järgmiste elusündmuste seast.

| Elusündmus | Koht | Käivitus |
| --- | --- | --- |
| **Perekonnaseisu muutus** | Töötaja > Profiil > Isikuandmed > Perekonnaseis| Perekonnaseisu muutus |
| **Tööhõive oleku muutus** | <ul><li>Töötaja > Tööhõive</li><li>Tööhõive ajaloo leht</li></ul> | Tööhõive oleku muutus |
| **Töövõtja aadressi muutumine** | <ul><li>Töötaja > Profiil > Aadressid </li><li>Töötaja > Isikuandmed > Isiklikud kontaktid > Aadress</li></ul> Lisatud, redigeeritud või kustutatud aadress |
| **Sõltuva muutus** | <ul><li>Töötaja > Profiil > Isikuandmed > Isiklikud kontaktid > Sõltuva lisamine või kustutamine</li><li>Töövõtja iseteenindus</li></ul> | Lisatud või kustutatud sõltuv. Isikliku kontakti suhe peab olema laps, abikaasa, elukaaslane või endine abikaasa. Kuupäeva **Kehtiv alates** värskendamine käivitab elusündmuse. Kui te seda kuupäeva ei uuenda, siis elusündmust ei käivitata. |
| **Sünd või lapsendamine (sõltuv)** | <ul><li>Töötaja > Profiil > Isikuandmed > Isiklikud kontaktid > Sõltuva üksikasjad</li><li>Töövõtja iseteenindus</li></ul> | Väli **Lapsendamise kuupäev** on täidetud. Nõutav on lapse sünnikuupäev. |
| **Katvuse kadumine (abikaasa/elukaaslane)** | Töötaja > Profiil > Isikuandmed > Isiklikud kontaktid > Sõltuva üksikasjad > Katvuse kadumine | **Katvuse kadumine** on valitud isiklikuks kontaktiks, koos suvandiga **Kehtivuse algus** |
| Elukaaslase töökohavahetus | Töötaja > Profiil > Isikuandmed > Isiklikud kontaktid > Sõltuva üksikasjad > Tööle võetud. | <ul><li>Loodud sõltuva üksikasjade kirje ja lahtri **Isiklik kontakt on tööle võetud** väärtus on Jah</li><li>Välja **Isiklik kontakt on tööle võetud** muudeti (Jah või Ei)</li></ul> |
| **Puhkus (abikaasa/elukaaslane)** | Töötaja > Profiil > Isikuandmed > Isiklikud kontaktid > Sõltuva üksikasjad > Puhkus | <ul><li>Sõltuva üksikasjade kirje on loodud ja **EhrLOAEffectiveDate** on täidetud</li><li>**personPrivateDetails.EhrIsLOA** on muudetud (Jah või Ei)</li><li>**personPrivateDetails.EhrLOAEffectiveDate** on muudetud</li></ul> |
| **Katvuse muutus (ametikoht)** | <ul><li>Töötaja > Ametikoha määramine > Töötaja ametikoha määrangud</li><li>Ametikoht > Ametikohad</li></ul> | <ul><li>Ametikoha muutus töötaja ametikoha määrangute kirjetes</li><li>Töötaja ametikoha määrangu muutus</li></ul> |
| **Tervisekindlustus (töövõtja/sõltuv)** | Töötaja > Profiil > Isikuandmed > Isiklikud kontaktid > Sõltuva üksikasjad > Tervisekindlustuse jõustumise kuupäev | Kui isiklik kontakt sisestab jõustumise kuupäeva, siis automaatselt ei käivitata. |
| **Kohtuga määratud tugi** | Töötaja > Profiil > Isikuandmed > Isiklikud kontaktid > Sõltuv > Kohtuga määratud tugi (QMSCO/QDRO) ja jõustumise kuupäevad | Automaatseid värskendusi ei käivita. See ei mõjuta sobivust; see registreerib elusündmuse. |
| **Surnud** | Töötaja > Profiil > Isikuandmed > Surmakuupäev | Sisestatud on surmakuupäev |
| **Kindlustustõend** | <ul><li>Töötaja > Töötaja > Versioonid > Tööhõive ajalugu > Kuupäevahaldur > Soodustuse üksikasjad</li><li> Töötaja > Tööhõive > Soodustuse üksikasjad > Kinnitamise kuupäev</li></ul> | <ul><li>Töötaja sisestab kontrollimise kuupäeva</li><li>Töötaja seab välja EvidenceOfInsurability väärtusele **Jah**</li></ul> |
| **Kasusaaja** | Töötaja > Profiil > Isikuandmed > Isiklikud kontaktid | Isiku kontakt lisatakse ja väljad **Kasusaaja** ja **Kehtivuse algus** on täidetud. Isiklik kontakt peab olema tüübiga **Laps**, **Abikaasa**, **Elukaaslane**, **Õde/vend**, **Perekondlik**, **Muu kontakt**, **Lapsevanem**, **Kasusaav kinnisvara**, **Kasusaav organisatsioon** või **Kasusaav kontsern**. |
| **Töövõtja ravikindlustus** | Töötaja > Töötaja > Versioonid > Tööhõive ajalugu > Kuupäevahaldur > Soodustuse üksikasjad | <ul><li>Olem **EhrMedicareEligibilityDate** on muudetud</li><li>Olem **MedicareEligibile** on seatud väärtusele **Jah**</li></ul> |
| **Sünnipäev** | Töötaja > Profiil > Isikuandmed > Isiklikud kontaktid > Sõltuva üksikasjad > Sünnikuupäev | Sünnikuupäev on lisatud või uuendatud (mitte pärast elusündmuse muudatuse töötlemist). Näide: kui lapse **Isikliku kontakti sobivuse valikud** suvandite väärtuseks on seatud Vanus: 26 suvandis Seadistus > Soodustused > Isikliku kontakti sobivuse suvandid ja kui personaliosakonna töötaja käitab elusündmuse muutmise töötluse mis tahes päeval pärast sõltuva 26-aastaseks saamist, kuvatakse neile teade, et sõltuv ei sobi enam katvuseks. |
| **Töötaja sobivuse muudatus (mitte USA spetsiifiline)** | <ul><li>Töötaja > Tööhõive</li><li>Töötaja > Töötaja > Versioonid > Tööhõive ajalugu</li></ul> | <ul><li>Töövõtja tüüp, Tööhõive kategooria või viis kasutaja poolt määratletavat sobivuse välja muutuvad</li><li>Olem **HcmEmploymentDetail.EhrEmploymentType** muutub (töödeldakse ainult *muudetud* tööhõive üksikasjade kirjete jaoks, ei töödelda *uute* tööhõive kirjete jaoks, nagu uuesti palkamine ja lepingu lõpetamine)</li></ul> |
| **Uus sobivuse tühistamine (mitte USA-spetsiifiline)** | Täpsustatud inimressursid > Soodustused > Plaanid > Soodustused > Sobivusreegli tühistamine | Elusündmuse töötlemise kasutamine | EhrBenefitEligibilityRuleOverride.ValidFrom |
| **Sobivusreegli tühistamise muudatus (mitte USA-spetsiifiline)** | Täpsustatud inimressursid > Soodustused > Plaanid > Soodustused > Sobivusreegli tühistamine | Elusündmuse töötlemise kasutamine (hangib ainult suvandi Sobivusreegli tühistamine muudatused väljadel **ValidFrom** ja **ValidTo**) |
| **Sobivusreegli tühistamise aegumine (mitte USA-spetsiifiline)** | Täpsustatud inimressursid > Soodustused > Plaanid > Soodustused > Sobivusreegli tühistamine | Elusündmuse muutuse töötlemise kasutamine. Näiteks kui redigeerite plaani sobivusreegli tühistamise aegumiskuupäeva, et see oleks täna kl 17.00, mis tahes ajal pärast kl 17.00 või järgmistel päevadel ning seejärel käivitate elusündmuse muutmise töötluse, kuvatakse teade, et sobivusreegli tühistamine on aegunud. |
| **Uus soodustuse plaan (mitte USA-spetsiifiline)** | Täiustatud inimressursid > Soodustused > Plaanid > Uus | <ul><li>Sobivuse suvandid lisatakse praegusele plaanile</li><li>Lisatakse uus plaan, millele on lisatud sobivuse suvandid</li></ul></br></br>Inimressursside töötajad peaksid käitama selles eksemplaris elusündmuse sobivuse töötlemise. |
| **Sobivusreegli muudatus (mitte USA-spetsiifiline)** | Täpsustatud inimressursid > Soodustused > Reeglid/suvandid > Sobivusreeglid | Elusündmuse sobivuse töötlemise kasutamine. Logitakse, kui kirjetel **EhrBenefitEligibilityRule** muudetakse järgmisi väärtusi: **UseEmplCategory**, **UseEmplStatus** või **UseEmplType**. Värskendab ainult elusündmuste kandeid, mis on muudetud reegli või sobivuse kriteeriumide jaoks juba olemas. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]