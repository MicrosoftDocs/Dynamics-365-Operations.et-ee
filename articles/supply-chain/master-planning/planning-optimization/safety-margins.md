---
title: Ohutuspiirid
description: Selles teemas kirjeldatakse, kuidas saab kasutada ohutuspiire Microsoft Dynamics 365 Supply Chain Managementi planeerimise optimeerimise lisandmooduliga.
author: ChristianRytt
ms.date: 09/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-9-14
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 7eb5128f3a337bd728cfe8e6d8d3deb0b6b5ef88
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8074963"
---
# <a name="safety-margins"></a>Ohutuspiirid

[!include [banner](../../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas saab kasutada ohutuspiire Microsoft Dynamics 365 Supply Chain Managementi planeerimise optimeerimise lisandmooduliga.

## <a name="safety-margins-overview"></a>Ohutuspiiride ülevaade

Ohutuspiiride eesmärk on lubada seadistus, mis annab tavalisele täitmisajale lisaks veidi rohkem puhveraega. Näiteks kui materjal tuleb pärast hankijalt saabumist pakendist lahti pakkida või üle vaadata, ei saa te lihtsalt lisaaega ostu täitmisajale lisada, sest see lähenemine annab tarnijale täiendava puhveraja. Selles näites saab sissetuleku ohutusvaru kasutada selleks, et tarnija tarniks varem. Selline lähenemine annab puhveraja, et kaupu saaks ettevõttesiseselt käsitleda.

Ohutuspiire on kolme tüüpi.

- **Lisatellimuse ohutusvaru** – tarne tellimuse tegemise puhveraeg
- **Sissetuleku ohutusvaru** – sissetuleva tarne käsitlemise puhveraeg
- **Väljamineku ohutusvaru** – saadetiste käsitlemise puhveraeg

Järgmisel illustratsioonil on näidatud, kuidas need ohutuspiirid aja jooksul rakenduvad.

![Ohutuspiirid.](media/safety-margins-1.png)

Kõik piirid määratletakse päevades. Vaikeväärtus *0* (null) tähendab, et piire pole rakendatud. Kui seadistate mitu piiri, lisatakse need kõik koondajale alates pakkumise *tellimuse kuupäevast* kuni nõudluse *vajaduse kuupäevani*. Näiteks pole seadistusel täitmisaega ja kõigi kolme piiri tüübi väärtuseks on määratud üks päev. Sel juhul on tarne tellimuse kuupäeva ja nõudluse vajaduse kuupäeva vahel kolm päeva, seega kui tellimuse kuupäev on 1. juuli, siis on vajaduse kuupäev 4. juuli.

### <a name="receipt-margin"></a>Sissetuleku ohutusvaru

Sissetuleku ohutusvaru on kolmest ohutuspiirist tõenäoliselt kõige kasutatavam. See rakendatakse *tarnekuupäevale* ja *vajaduse kuupäevast* tagasi. Teisisõnu tuleks tooted kätte saada kindlaksmääratud arv ohutusvaru päevi enne nende nõudmist.

Järgmine illustratsioon tõstab esile sissetuleku ohutusvaru.

![Sissetuleku ohutusvaru.](media/safety-margins-2.png)

Sissetuleku ohutusvaru kasutatakse tavaliselt puhvrina, et varuda aega lao registreerimiseks või muudeks aeganõudvateks protsessideks, mida ei arvestata süsteemis üldise täitmisaja osana. Ostude korral on üheks eeliseks see, et ostutellimuse *tarnekuupäev* lükatakse edasi sellele vastavalt. Kui suurendate täitmisaega ohutuspiiri kasutamise aja asemel, palutakse viimasel minutil hankijal tarnida.

Pange tähele, et sissetuleku ohutusvaru ei muuda tarne *vajaduse kuupäeva*. Seetõttu pole sissetuleku ohutusvaru nõudluse ja pakkumise vajaduse kuupäevade võrdlemisel otseselt nähtav (nt lehel **Netovajadused**). Näiteks, kui sissetuleku varuks on seatud neli päeva ja ostutellimuse rida on planeeritud sissetulekuks 15. kuupäeval, siis koondplaneerimine arvutab korrigeeritud sissetuleku ajaks 19. kuupäeva.

Pange tähele, et sissetuleku ohutusvaru ei rakendata, kui varuna kasutatakse vaba kaubavaru. Eeldatakse, et kogu vaba kaubavaru on saadaval kohe, olenemata sellest, millal see tegelikult vastu võeti.

### <a name="reorder-margin"></a>Lisatellimuse ohutusvaru

Järgmine illustratsioon tõstab esile lisatellimuse ohutusvaru.

![Lisatellimuse ohutusvaru.](media/safety-margins-3.png)

Lisatellimuse ohutusvaru lisatakse koondplaneerimise käigus kõigile plaanitud tellimustele enne kauba täitmisaega. Seetõttu tagab see lisaaja tarne tellimuse tegemiseks. Seda varu kasutatakse tavaliselt puhvrina, et tagada piisavalt aega kinnitamisprotsessideks või muudeks sisemisteks protsessideks, mis on vajalikud tarnetellimuste loomisel. Lisatellimuse ohutusvaru lisatakse tarne *tellimuse kuupäeva* ja *alguskuupäeva* vahele.

### <a name="issue-margin"></a>Väljamineku ohutusvaru

Järgmine illustratsioon tõstab esile väljamineku ohutusvaru.

![Väljamineku ohutusvaru.](media/safety-margins-4.png)

Väljamineku ohutusvaru arvestatakse koondplaneerimise käigus nõudluse vajaduse kuupäevast. See aitab tagada, et teil on piisavalt aega reageerimiseks ja sissetulevatele nõudlustellimuste tarnimiseks. Seda ohutusvaru kasutatakse tavaliselt puhvrina, et varuda aega saadetise saatmiseks ja sellega seotud väljaminevateks laoprotsessideks.

Pange tähele, et väljamineku ohutusvaru rakendamisel ei ühti seotud nõudluse ja pakkumise vajaduse kuupäevad. Selle asemel erinevad nende väljamineku ohutusvarud, kuna väljamineku ohutusvaru lisatakse tarne *vajaduse kuupäeva* ja nõudluse *vajaduse kuupäeva* vahele.

## <a name="set-up-safety-margins"></a>Ohutuspiiride seadistamine

### <a name="turn-on-safety-margins-in-feature-management"></a>Ohutuspiiride sisselülitamine funktsioonihalduses

Enne selle funktsiooni kasutamist koos planeerimise optimeerimisega peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Seega on funktsioon loetletud järgmisel viisil.

- **Moodul:** _Koondplaneerimine_
- **Funktsiooni nimi:** _planeerimise optimeerimise ohutuspiirid_

### <a name="define-safety-margins"></a>Ohutuspiiride määratlemine

Ohutuspiirid on paindlikult seadistatud. Neid saab seada nii *laovarude grupis* kui ka *koondplaanis*. Oluline on mõista, et ohutuspiire lisatakse üksteise peale. Näiteks laovarude grupi kahe päeva ja koondplaani kolme päeva sissetuleku ohutusvaru annab efektiivse sissetuleku ohutusvaru viieks päevaks.

Võimalus määrata koondplaanile ohutuspiir võib olla kasulik, kui soovite simuleerida mõne kindla plaani pikemaid täitmisaegu või määramatust igapäevast planeerimist mõjutamata.

#### <a name="coverage-group-safety-margins"></a>Ohutusvarudega laovarude grupp

Ohutusvaru rakendamiseks laovarude grupile toimige järgmiselt.

1. Valige **Koondplaneerimine \> Seadistus \> Laovarude grupid**.
1. Valige loendipaanil soovitud laovarude grupp.
1. Kasutage kiirkaardi **Muu** jaotises **Ohutuspiirid päevades** nõutavate ohutuspiiride (päevades) seadmiseks järgmisi välju.

    - Vajaduse kuupäevale lisatud sissetuleku ohutusvaru
    - Vajaduse kuupäevast maha arvatud väljamineku ohutusvaru
    - Kauba täitmisajale lisatud lisatellimuse ohutusvaru

#### <a name="master-plan-safety-margins"></a>Ohutusvarudega koondplaan

Ohutusvaru rakendamiseks koondplaanile toimige järgmiselt.

1. Avage **Koondplaneerimine \> Seadistus \> Plaanid \> Koondplaanid**.
1. Valige loendipaanil soovitud koondplaan.
1. Kasutage kiirkaardil **Ohutuspiirid päevades** nõutavate ohutuspiiride (päevades) seadmiseks järgmisi välju.

    - Vajaduse kuupäevale lisatud sissetuleku ohutusvaru
    - Vajaduse kuupäevast maha arvatud väljamineku ohutusvaru
    - Kauba täitmisajale lisatud lisatellimuse ohutusvaru

### <a name="define-whether-calculations-are-based-on-calendar-days-or-work-days"></a>Saate määratleda, kas arvutused põhinevad kalendripäevadel või tööpäevadel

Saate seada kõik ohutuspiirid nii, et need arvutatakse kas kalendripäevade või tööpäevade põhjal.

1. Avage **Koondplaneerimine \> Seadistus \> Koondplaneerimise parameetrid**.
1. Ohutuspiiride arvutamiseks tööpäevade põhjal seadke vahekaardi **Üldine** jaotises **Ohutuspiirid päevades** suvandi **Tööpäevad** väärtuseks *Jah*. Ohutuspiiride arvutamiseks kalendripäevade põhjal seadke suvandi väärtuseks *Ei*.

Näiteks on kalender avatud esmaspäevast reedeni ja suletud laupäevast pühapäevani. Kui olemas on ühe päeva sissetuleku ohutusvaru, loob esmaspäevane vajaduse kuupäev tarnekuupäeva elmise reede jaoks, kuna laupäev ja pühapäev pole tööpäevad.

Tööpäevade määramiseks kasutatav kalender sõltub seadistusest ja tarne tüübist. Seda saab juhtida laovarude grupi, lao- ja hankijakalendriga.

> [!NOTE]
> Kui *ladu* ei kuulu laovarude dimensiooni (teisisõnu, planeerimine põhineb ainult *saidil*), siis laokalendrit ei kasutata.

Süsteem saab hallata seadistust, kus on määratletud üks või mitu kalendrit. Järgmistes alamjaotistes kirjeldatakse võimalikke kombinatsioone, mida saab tulemuse juhtimiseks kasutada.

#### <a name="calendar-that-is-used-for-the-duration"></a>Kestuse jaoks kasutatav kalender

Määratletud kalendrid juhivad tegelikku summaarset kalendripäevades täitmisaega alates tarne tellimuse kuupäevast kuni nõudluse vajaduse kuupäevani. Kasutatakse järgmist kalendri prioritiseerimist.

- **Ostu täitmisaeg** – võetakse arvesse ainult laovarude grupi kalendrit.
- **Sissetuleku ohutusvaru** – kasutatakse laovarude grupi kalendrit, kui see on määratletud. Muul juhul kasutatakse laovarude kalendrit.
- **Väljamineku ohutusvaru** – kasutatakse laovarude grupi kalendrit, kui see on määratletud. Muul juhul kasutatakse laovarude kalendrit.
- **Lisatellimuse ohutusvaru** – võetakse arvesse ainult laovarude grupi kalendrit.

#### <a name="calendar-that-is-used-for-the-final-date"></a>Lõppkuupäeva jaoks kasutatav kalender

Selleks et teha kindlaks, kas planeerimismootor saab kasutada antud kuupäeva teatud kuupäeva tüübi korral, rakendatakse järgmisi reegleid.

- **Ostu sissetuleku kuupäev** – kasutatakse hankijakalendrit, kui see on määratletud. Muul juhul kasutatakse laovarude grupi kalendrit, kui see on määratletud. Kui ükski neist kalendritest pole määratletud, kasutatakse laokalendrit.
- **Üleviimistarne kuupäev** – kasutatakse laovarude grupi kalendrit, kui see on määratletud. Muul juhul kasutatakse laovarude kalendrit.
- **Tootmise sissetuleku kuupäev** – kasutatakse laovarude grupi kalendrit, kui see on määratletud. Muul juhul kasutatakse laovarude kalendrit.
- **Nõutava väljamineku avatud kuupäev** – kasutatakse laokalendrit, kui see on määratletud. Muul juhul kasutatakse laovarude grupi kalendrit.
- **Tellimuse avatud päev** – kasutatakse laovarude grupi kalendri ja hankijakalendri kombinatsiooni (ühisosa). Kuupäeva kasutamiseks peavad mõlemad kalendrid olema avatud. Kui ainult üks kalendritest on määratletud, kasutatakse ainult seda kalendrit.

#### <a name="calendar-setup-overview-matrix"></a>Kalendri seadistamise ülevaatlik maatriks

Järgmisel illustratsioonil on kujutatud maatriks, mis annab kokkuvõtlikku teavet selle kohta, milliseid kalendreid ohutuspiiride arvutamisel rakendatakse. (Valige pilt, et avada selle suure eraldusvõimega versioon.) Iga kalendritüübi asukoha näitamiseks kasutatakse järgmiseid lühendeid ja värve.

- **Laovarude grupp (CG):** roheline
- **Ladu (WH):** kollane
- **Hankija (V):** sinine

[![Kalendri seadistamise ülevaatlik maatriks.](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)

## <a name="calculating-delays"></a>Hilinemiste arvutamine

Kui süsteem määrab, kas tellimus hilineb või mitte, kaasatakse kõik kolm ohutuspiiri tüüpi.

Näiteks on kaubal tarneaeg üks päev ja sissetuleku ohutusvaru kolm päeva. Selle kauba müügitellimus on seatud nõutavaks täna. Sel juhul arvutatakse hilinemine järgmiselt: *täitmisaeg* + *sissetuleku ohutusvaru* = neli päeva. Seega, kui täna on 14. august, on tarneaeg neljapäevase hilinemise tõttu 18. august. Järgmisel illustratsioonil on toodud see näide.

![Hilinemise arvutamise näide.](media/safety-margins-delays.png)

## <a name="additional-resources"></a>Lisaressursid

[Planeerimise optimeerimise kasutamise alustamine](get-started.md)

[Planeerimise optimeerimise sobivuse analüüs](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]