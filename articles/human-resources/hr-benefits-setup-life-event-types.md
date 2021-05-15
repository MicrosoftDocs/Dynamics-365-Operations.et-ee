---
title: Elusündmuse tüüpide konfigureerimine
description: Microsoft Dynamics 365 Human Resources kasutab elusündmuse tüüpe sündmuste määratlemiseks, kus kehtib töövõtja soodustuste registreerimise värskendamine.
author: andreabichsel
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8f04be1c0852970db337766757ff6f412bbf5c38
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921113"
---
# <a name="configure-life-event-types"></a>Elusündmuse tüüpide konfigureerimine

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources kasutab elusündmuse tüüpe sündmuste määratlemiseks, kus kehtib töövõtja soodustuste registreerimise värskendamine, nagu näiteks abiellumine või lapse saamine. Iga elusündmuse tüübi ID võib olla seotud ainult ühe elusündmuse tüübiga. Näiteks kui loote elusündmuse ID nimega aadressi muutus, mis on seotud elusündmuse tüübiga Töövõtja aadressi muutus, ei saa te luua teist ID-d sildiga Töövõtja aadressi muutus ega seostada seda elusündmuse tüübiga Töövõtja aadressi muutus. Kui elusündmuse tüüp ei ole plaani tüübiga seotud, ei käivita elusündmuse tüüp elusündmust. Lisateabe saamiseks vt [Plaani tüüpide loomine](hr-benefits-setup-plan-types.md).

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
| **Tööhõive oleku muutus** | Töötaja > Tööhõive<br>Tööhõive ajaloo leht | Olemasoleva tööhõive üksikasjaga töötaja jaoks käivitab uue tööhõive üksikasja ja erineva tööhõiveolekuga elusündmuse.  Olemasoleva tööhõive üksikasjade uuendamine erineva tööhõiveolekuga käivitab lisaks ka elusündmuse.  |
| **Töövõtja aadressi muutumine** | Töötaja > Profiil > Aadressid<br>Töötaja > Isikuandmed > Isiklikud kontaktid > Aadress | Aadressi muutmine. Elusündmuse käivitamiseks peab aadress olema esmane. |
| **Sõltuva muutus** | Töötaja > Profiil > Isikuandmed > Isiklikud kontaktid<br>Töövõtja iseteenindus | Lisage isiklik kontakt, mis on määratletud kui sõltuv isik ja määratlege **kehtivus** alates. Värskendage isikliku kontakti sõltuvat isikut **kehtiv kuni** teavet. Isikliku kontakti suhe peab olema laps, abikaasa, elukaaslane või endine abikaasa.  |
| **Sünd või lapsendamine (sõltuv)** | Töötaja > Profiil > Isikuandmed > Isiklikud kontaktid<br>Töötaja iseteenindus > Isiklike andmete redigeerimine > Isiklikud kontaktid | **Sünnikuupäev** või **Adopteerimiskuupäev** lisatakse või värskendatakse. Nõutav on lapse **sünnikuupäev**. |
| **Katvuse kadumine (abikaasa/elukaaslane)** | Töötaja > Profiil > Isikuandmed > Isiklikud kontaktid > Sõltuva üksikasjad > Katvuse kadumine | **Katvuse kadumine** on valitud isiklikuks kontaktiks, koos suvandiga **Kehtivuse algus** |
| Elukaaslase töökohavahetus | Töötaja > Profiil > Isikuandmed > Isiklikud kontaktid > Sõltuva isiku üksikasjad > Tööle võetud | Isikliku kontakti loomine ja säte **Tööle võetud** väärtuseks tuleb määrata **Jah**. Isikliku kontakti värskendamine ja sätte **Tööle võetud** muutmine.  |
| **Puhkus (abikaasa/elukaaslane)** | Töötaja > Profiil > Isikuandmed > Isiklikud kontaktid > Sõltuva üksikasjad > Puhkus | Määratud on isiklik kontakt **ja puhkuse kehtivuse alguskuupäev**. Uuendatakse isikliku kontakti **puhkuse** teavet. Uuendatakse isikliku kontakti **puhkuse alguskuupäeva** teavet.  |
| **Katvuse muutus (ametikoht)** | Töötaja > Ametikoha määramine > Töötaja ametikoha määrangud<br>Ametikoht > Ametikohad | Ametikoha muutus töötaja ametikoha määrangute kirjetes. Töötaja ametikoha määrangu muutus. |
| **Kindlustuskaitse muutus (palk)** | Töötaja > Kompensatsioon > Põhipalk<br>Töötaja > Isikuandmed > Aastased soodustused | Kui soodustuste haldus > Inimressursside jagatud parameetrid > Soodustused > Aastased soodustused ei ole lubatud, loob Töötaja > Tasu > Fikseeritud plaani värskendamine elusündmuse. Kui soodustuste haldus > Inimressursside jagatud parameetrid > Soodustused > Aastased soodustused on lubatud, loob Töötaja > Isiklik teave > Aastased soodustused värskendamine elusündmuse. |
| **Tervisekindlustus (töövõtja/sõltuv)** | Töötaja > Profiil > Isikuandmed > Isiklikud kontaktid > Sõltuva üksikasjad > Tervisekindlustuse jõustumise kuupäev | **Medicare'i kehtivuse** kuupäeva lisamine või uuendamine isikliku kontakti puhul loob elusündmuse. |
| **Kohtuga määratud tugi** | Töötaja > Profiil > Isikuandmed > Isiklikud kontaktid > Sõltuv > Kohtuga määratud tugi (QMSCO/QDRO) ja jõustumise kuupäevad | Isikliku kontakti loomisel luuakse elusündmus, kui **kohtuga tellitud toe** väärtus on **Jah**. **Kohtu poolt määratud toe** või **kohtu poolt määratud aegumiskuupäeva** värskendamine käivitab samuti elusündmuse. |
| **Surnud** | Töötaja > Profiil > Isikuandmed > Surmakuupäev | Surmakuupäev on sisestatud või uuendatud. |
| **Kindlustustõend** | Töötaja > Töötaja > Versioonid > Tööhõive ajalugu > Kuupäevahaldur > Soodustuse üksikasjad | **Kindlustatavuse tõendus** on seatud väärtusele **Jah**. Määratletakse **kindlustamatuse tõendamise kuupäev**. |
| **Kasusaaja** | Töötaja > Profiil > Isikuandmed > Isiklikud kontaktid | Isiku kontakt lisatakse ja väljad **Kasusaaja** ja **Kehtivuse algus** on täidetud. Isiklik kontakt peab olema tüübiga **Laps**, **Abikaasa**, **Elukaaslane**, **Õde/vend**, **Perekondlik**, **Muu kontakt** või **lapsevanem**. |
| **Töövõtja ravikindlustus** | Töötaja > Töötaja > Versioonid > Tööhõive ajalugu > Kuupäevahaldur > Soodustuse üksikasjad | Olem **Medicare Eligibile** on seatud väärtusele **Jah**. Olem **Medicare Eligibility Date** on muudetud. |
| **Sünnipäev** | Soodustuste haldus > Elusündmuse muudatuste töötlemine | Need elusündmused luuakse **elusündmuse muudatuste töötlemisest**. Protsess analüüsib valitud perioodi ja juriidilist isikut ning leiab seostatud töötajad. See arvutab välja nende viimase sünnipäeva ja loob sünnipäeva sündmuse juhul, kui seda pole veel loodud. |
| **Töötaja sobivuse muudatus (mitte USA spetsiifiline)** | Töötaja > Tööhõive<br>Töötaja > Töötaja > Versioonid > Tööhõive ajalugu | Elusündmuse tüübi loomine juhul, kui:<br><ul><li>Uue töösuhte loomine ja olemas on eelnev töösuhe ning töötaja tüüp muutub.</li><li>Uue töösuhte detaili loomine ja olemas on eelneva töösuhte detailteave ning tööhõive tüüp või tööhõive kategooria muutub.</li><li>Tööhõivekirje ja erineva töötajatüübi värskendamine on määratletud.</li><li>Tööhõive üksikasjade kirje ja muu tööhõive tüübi või kategooria värskendamine on määratud.</li></ul> |
| **Uus sobivuse tühistamine (mitte USA-spetsiifiline)** | Täpsustatud inimressursid > Soodustused > Plaanid > Soodustused > Sobivusreegli tühistamine | Elusündmuse töötlemise kasutamine<br>Uue soodustusplaani kõlblikkuse alistamise töötaja puhul käivitab selle elusündmuse.<br>BenefitEligibilityRuleOverride.ValidFrom. |
| **Sobivusreegli tühistamise muudatus (mitte USA-spetsiifiline)** | Täpsustatud inimressursid > Soodustused > Plaanid > Soodustused > Sobivusreegli tühistamine | Soodustusplaani **kehtiv alates** või **kehtiv kuni** väärtuse uuendamise alistamine käivitab selle elusündmuse. |
| **Sobivusreegli tühistamise aegumine (mitte USA-spetsiifiline)** | Soodustuste haldus > Elusündmuse muudatuste töötlemine  | Need elusündmused luuakse **elusündmuse muudatuste töötlemisest**. Protsess analüüsib valitud perioodi ja juriidilist isikut ning leiab seostatud soodustuste plaani kehtivuse alistamised. See loob elusündmused, kui alistamised on aegunud. |
| **Uus soodustuse plaan (mitte USA-spetsiifiline)** | Täiustatud inimressursid > Soodustused > Plaanid > Uus | Sobivuse suvandid lisatakse praegusele plaanile. Lisatakse uus plaan, millele on lisatud sobivuse suvandid.</br></br>Inimressursside töötajad peaksid käitama selles eksemplaris elusündmuse sobivuse töötlemise. |
| **Sobivusreegli muudatus (mitte USA-spetsiifiline)** | Soodustuste haldus > Sobivuse reeglid | Elusündmuse sobivuse töötlemise kasutamine. Logitakse, kui kirjetel **BenefitEligibilityRule** muudetakse järgmisi väärtusi: **UseEmplCategory**, **UseEmplStatus** või **UseEmplType**. Värskendab ainult elusündmuste kandeid, mis on muudetud reegli või sobivuse kriteeriumide jaoks juba olemas. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]