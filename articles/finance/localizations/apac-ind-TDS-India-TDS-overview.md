---
title: India maksu mahaarvamise allikast (TDS) ülevaade
description: Selles teemas antakse üksikasjalikku teavet mahaarvatava India maksu (TDS) kohta. TDS-dokumentatsioon hõlmab selle võimaluse funktsioone.
author: kailiang
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 28ee843036e11bd37b97a065ce53d2eb860c79d9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023191"
---
# <a name="indian-tax-deducted-at-source-tds-overview"></a>India maksu mahaarvamise allikast (TDS) ülevaade

[!include [banner](../includes/banner.md)]

Selles teemas antakse üksikasjalikku teavet mahaarvatava India maksu (TDS) kohta.

TDS-dokumentatsioon hõlmab selle võimaluse funktsioone. See selgitab ka TDS-i põhiseadistuse sooritamist, TDS-i arvutamist kannetel, TDS-i tasakaalustusprotsessi lõpule viimist, TDS-i serdinumbrite kirjendamist ja TDS-päringute, TDS-lausete ja TDS-i sertide genereerimist. See jaotis hõlmab järgmisi teemasid:

- [TDS-i põhihäälestus](apac-ind-TDS-TDS-ledger-accounts-setup.md)
- [TDS-i arvutuse valemikoostaja ja lävelimiit](apac-ind-TDS-Formula-designer.md)
- [Arvete, maksete, võlatähtede ja kontsernisiseste kannete TDS-i arvutamine](apac-ind-TDS-Calculate-TDS-on-invoices-using-journals.md)
- [TDS-i perioodiline tasakaalustusprotsess ja TDS-i summade tasakaalustus TDS-i asutusele hankijatele](apac-ind-TDS-Run-the-periodic-TDS-settlement-process.md)
- [TDS-i sertifikaadinumbrite ja kuupäevade kirjendamine ja uuendamine](apac-ind-TDS-Record-TDS-concession-certificate-numbers.md)

## <a name="introduction-to-tds"></a>Sissejuhatus TDS-i

1961. aasta tulumaksuseaduse alusel on teenuse saaja allikalt maha arvatud tulumaks ettemakse või krediidiarvestuse ajal, olenevalt sellest, kumb toimub esimesena. Makse sooritanud isik peab maksusumma maha arvama ja maksma teenuse pakkujale ainult netosaldo. TDS-i rakendatakse valitsuse täpsustatud teenustele ja maks arvatakse maha valitsuse poolt perioodi jaoks määratud määrade alusel. Mahaarvamise määr põhineb üksuse olekul, mis võtab makse vastu või pakub teenust. Olekud hõlmavad **Isikut**, **Hindu jagamata peret** (**HUF**) **Ettevõtet**, **Firmat**, **isikute seost** (**AOP**), **Üksiisikute kehasid** (**BOI**), ja **Kohalikku isikut**.

Järgmistes jaotistes loetletakse teenused, mille puhul TDS-i rakendatakse, nagu on määranud India valitsus.

**Elanikud**

- Tulu palgast (jaotis 192 all)
- Tulu väärtpaberide intressilt (jaotis 193)
- Tulu dividendidelt (jaotis 194 all)
- Tulu intressidelt (jaotis 194 all)
- Tulu loteriidest või mõistatustest (jaotis 194B all)
- Võidud võiduajamistelt jne (jaotis 194BB all)
- Peatöövõtjad ja alamtöövõtjad (jaotis 194C all)
- Kindlustuse komisjonitasu (jaotis 194D all)
- Sissetulek deposiidilt riikliku salvestamisskeemi alusel (jaotis 194EE all)
- Tulu investeerimisfondist või UTI-st (jaotis 194F all)
- Komisjonitasu, vahendustasu, auhind jne, müügil või loteriil (jaotis 194G all)
- Komisjonitasu või maakleritasu (jaotis 194H all)
- Renditasu (jaotis 194I all)
- Professionaalne teenus (jaotis 194J all)
- Tulu intressidelt (jaotis 194K all)
- Teatud kinnisvara omandamisel hüvitise maksmine (jaotis 194LA all)

**Mitteresidendid**

- Maksed mitteresidendist sportlastele või spordiliitudele (jaotise 194E all)
- Muud summad (jaotise 195 all)
- Mitte-residentide ühikute tulu (jaotise 196A all)

    - Tulu välisvaluuta obligjonidelt või India ettevõtte aktsiatelt (jaotise 196C all)
    - Välismaised investeerijad väärtpaberidest (jaotise 196D all)
    - Palk ja kõik muud positiivsed sissetulekud mis tahes sissetulekul (jaotis 192)
    - Viivis väärtpaberilt (jaotis 193)
    - Viivis, mis pole viivis väärtpaberidelt (jaotis 194A)
    - Maksed peatöövõtjatele ja alamtöövõtjatele (jaotis 194C)
    - Võidud loteriidelt või ristsõna mõistatustelt (jaotis 194B)
    - Võidud võiduajamistelt (jaotis 194BB)
    - Kindlustus komisjonitasu, mis hõlmab kõiki kindlustuse hankimisega seotud makseid (jaotis 194D)
    - Mitteresidentidele või välisettevõttele makstavad intressid (sektsioon 195)
    - Makse mitteresidendist sportlasele, sealhulgas sportlasele, spordiliidule või asutusele. Mitteresidendist spordimehe puhul makstakse välja reklaamide ning artiklite kohta mis tahes Indias mängude/spordialade kohta ajalehtedes, ajakirjades jne. On kaasatud (jaotis 194E)
    - Deposiitide eest makstav maks NSS \[riikliku hoiuste skeemi\] alusel (jaotis 194EE)
    - Makse ühikute tagasiostuks ühisfondi või UTI alusel (jaotis 194F)
    - Komisjonitasu või maakleritasu (jaotis 194H)
    - Rendimakse (jaotis 194I)
    - Professionaalsete või tehniliste teenuste tasude maksmine (jaotis 194J)
    - Komisjonitasu aktsionäridele, levitajatele, ostjatele ja müüjatele, sh selliste piletite tasu või auhind (jaotis 194G)
    - Välisvaluutas ostetud ühikute tulu või pikaajaline kapitalikasum, mis tuleneb välisvaluutas ostetud ühikute ülekandmisest (jaotis 196B)
    - Mis tahes tulu maksmine mitteresidentidele seoses obligeeritud ja aktsiate intresside või dividendidega (sektsioon 196C)

TDS arvutatakse ostude, müükide, müügi tagastuste, kreeditarvete, põhivarade soetamise, ettemaksete, käsirahade, võlatähtede, tööde maksu ja kontsernisiseste kannete alusel.

> [!NOTE]
> Praeguse India maksustsenaariumis ei arvutata TDS-i müügikannetele. Süsteem sisaldab sätet müügitehingute, eriti ettevõtete vaheliste tehingute puhul kaetava TDS arvutamiseks.

TDS-i kalkulatsioon võtab alati arvesse lävendi ja erandi lävendi, mis on määratud TDS-i komponendile.

Peab käitama perioodilise TDS-i tasakaalustusprotsessi ja TDS-i maksed tuleb tasakaalustada TDS-i asutuse hankijatega.

Hankijatelt või klientidelt saadud TDS-tunnistuste serdi numbreid ja kuupäevi saab registreerida ja värskendada. Lisaks saab rakenduses Finance luua Form 26Q ja Form 27Q kvartaliväljavõtteid ja Form 16A tunnistuse TDS-i.

## <a name="setting-up-and-working-with-tds"></a>TDS-i seadistamine ja sellega töötamine

Siin on ülevaade TDS-i seadistamise ja sellega töötamise protsessist:

1. **TDS-i seadistus:**

    - Parameetrite seadistamine:

        - Aktiveerige pearaamatu parameetrites TDS-iga seotud parameetrid.
        - Pearaamatu parameetrites seadistage kinnipeetava maksu maksete numbriseeria.
        - TDS-i parameetrite määramine jaotises ostukontod ja müügikontod.

    - Põhihäälestus:

        - Seadistage TDS-i registreerimisnumbrid ettevõttele, klientidele ja hankijatele.
        - Kordustellimuste gruppide häälestus.
        - Seadistage TDS-i komponendid, lisage neile TDS-i komponendigrupid ning määratlege nende jaoks lävi ja erandi lävi.
        - Seadistage TDS-i asutused.
        - Käibemaksu tasakaalustusperioodide häälestamine.
        - Seadistage TDS-i maksukoodid ja s seostage nendega TDS-i komponendid.
        - Seadistage TDS-i maksukoodid ja s seostage nendega TDS-i komponendid.
        - TDS-grupi TDS-i arvutamiseks määratlege valemikoosturis.
        - TDS-i kontsessioonisertifikaatide numbrid.

    - Pearaamatukontod ja ettevõtteseadistus:

        - Seadistage TDS-i maksmis- ja saadaoleva pearaamatu kontod.
        - Seadistage ettevõttele maksu mahaarvamise ja kogumise konto number (TAN) ja mahaarvaja tüübi kategooria.

    - Muu seadistus:

        - Seadistage maksegraafik, mis sisaldab TDS-i eraldamist.
        - Seadistage TDS-asutusele tehtavate maksete jaoks maksetasu tüüp.
        - Saate seadistada teabe hankijate ja klientide TDS-gruppide, püsikontonumbrite ja TAN-ide kohta.

2. **TDS kalkulatsioonitehingud:**

    - Arved ja maksed
    - Võlatähed
    - Ettemaksed
    - Ettemaksed

3. **TDS tasumine:**

    - Perioodilise TDS-i tasumise käitamine
    - TDS-i maksete tasumine TDS-i halduri hankijatele ja TDS-i dokumendi loomine

4. **TDS-i päringud, väljavõtted ja sertifikaadid:**

    - TDS-i sertifikaadinumbrite ja kuupäevade kirjendamine ja uuendamine.
    - Looge TDS-i päring ja sisestatud TDS-i päring.
    - Looge Form 27A, Form 26Q ja Form 27Q TDS-i ja e-TDS-i kvartaliaruanded.
    - Form 16A serdi loomine.
