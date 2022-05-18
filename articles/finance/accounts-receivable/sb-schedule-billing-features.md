---
title: Arveldusgraafiku funktsioonid
description: Käesolev teema selgitab arveldusgraafikute funktsioone, nt hinnameetodeid, laiendusi ja allahindlusi, joonduse kuupäevi, mõõduseadeid, tühista arveldust ja kaubagruppide tükeldamist.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 0ce323565a94e8e70d90a65b7a3143e984a1c159
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8696645"
---
# <a name="billing-schedule-features"></a>Arveldusgraafiku funktsioonid

[!include [banner](../includes/banner.md)]

See teema selgitab arveldusgraafikute funktsioone ja arveldusgraafiku ridu. See kirjeldab erinevaid hinnakujunduses kasutatavaid meetodeid, laienduste ja allahindluste kasutamist ning arveldusperioodi tagasipööramist. See sisaldab ka proration kalkulatsioonide ja kaubagruppide tükeldamise näiteid.

## <a name="pricing-methods"></a>Hinnakujundusmeetodid

Kauba ühiku hinna arvutamiseks saate kasutada ühte järgmistest hinnakujundusmeetoditest:

* Ühekordne makse
* Standardne
* Järk
* Ühtne aste

### <a name="flat-pricing"></a>Kindla hinnakujunduse

Kui kasutatakse lamehinna meetodit, **saab** kõigil arveldusgraafikute lehel oleva arveldusgraafiku rea kauba ühikuhinda redigeerida mis tahes väärtusele, mida soovite. Hinnaühiku **väärtus** on alati **1**. Seega on **ühiku hinna** ja **netosumma** väärtused kauba puhul samad.

### <a name="standard-pricing-without-a-trade-agreement"></a>Standardne hinnakujundus (ilma kaubanduslelepinguta)

Kui standardset hinnakujundusmeetodit kasutatakse **ilma kaubanduslelepinguta, seadistage arveldusgraafiku rea kauba ühikuhind,** valides tooteteabe **halduse väljastamistoote üksikasjade lehel**. Ühiku hind kuvatakse jaotises **Baasmüügihind**. See arvutatakse hinna *kogusena*&divide;*·*.

### <a name="standard-pricing-with-a-trade-agreement"></a>Standardne hinnakujundus (kaubanduslelepinguga)

Järgmised näited näitavad standardse hinnakujunduse arvutusi, kui kaubandusle leping on olemas. Kaubandusleppeid saate luua lehelt **Toote üksikasjade väljalase**.

Mõlemad näited kasutavad kaupa, mille hinnal on järgmised sulgud.

| Kogus alates | Kogus kuni | M/M | Hind | Hinnaühik |
|---|---|---|---|---|
| 0 | 100 | Iga | 1.50 | 1 |
| 100 | 200 | Iga | 1.25 | 1 |
| 200 | 999999 | Iga | 1.00 | 1 |

**Näide 1**

Arve kogus on 250 ja kasutatakse standardset hinnakujundusmeetodit. Kuna kogus on vahemikku 200–999 999, on ühiku hind 1,00. 

Netosumma arvutatakse järgmiselt:

*netosumma* = (*koguse*&times;*hind*) &divide;*hinnaühik* = (250 &times; 1,00) &divide; 1 = 250

**Näide 2**

Arve kogus on 100 ja kasutatakse standardset hinnakujundusmeetodit. Kuna arve kogus on 0–100 hinna kogusevahemikus, on ühiku hind 1,50.

> [!NOTE]
> Arve kogus on vahemikus 0–100, mitte 100–200, sest standardse koguse vastendamise käitumise puhul vastab kogus kogusele, *kui* see on suurem või võrdne kogusega Alates *ja* väiksem kui "Kuni" kogus.

Netosumma arvutatakse järgmiselt:

*netosumma* = (100 &times; 1,50) &divide; 1 = 150,

### <a name="tier-pricing"></a>Järgu hinnakujundus

Järgmises näites on kaubal järgmised hinnasulud.

| Kogus alates | Kogus kuni | M/M | Hind | Hinnaühik |
|---|---|---|---|---|
| 0 | 100 | Iga | 1.50 | 10 |
| 100 | 200 | Iga | 1.25 | 10 |
| 200 | 999999 | Iga | 1.00 | 10 |

Kui arve kogus on 250 ja kasutatakse järgu hinnakujundusmeetodit, arvutatakse kaupade hinnad hinnakujunduse sulgude alusel järgmiselt:

- **Esimesed 100 üksust:** 100 &times; 1,50 = 150,00
- **Teine 100 üksust:** 100 &times; 1,25 = 125,00
- **Ülejäänud kaubad:** 50 &times; 1,00 = 50,00

Netosumma arvutatakse järgmiselt:

*netosumma* = (150,00 &divide; 10) + (125,00 &divide; 10) + (50,00 &divide; 10) = 15,00 + 12,50 + 5,00 = 32,50,

Pärast netosumma arvutamist arvutatakse ühiku hind, jagades netosumma kogusega:

*Ühiku hind* = 32,50 &divide; 250 = 0,13

### <a name="flat-tier-pricing"></a>Kindla järguga hinnakujundus

Järgmises näites on kaubal järgmised hinnasulud.

| Kogus alates | Kogus kuni | M/M | Ühtse astme summa | Hinnaühik |
|---|---|---|---|---|
| 0 | 50 | Iga | 100.00 | 50 |
| 50 | 200 | Iga | 150.00 | 200 |

Järgmises tabelis on näidatud arved ja ühikuhinnad erinevate ostetud koguste puhul. Netosumma arvutatakse esimesena ja seejärel arvutatakse ühiku hind.

| Arve | Ostetud kogus | Ühiku hind | Netosumma |
|---|---|---|---|
| 1 | 25 | 2,00 &divide; 25 = 0,08 | 100 &divide; 50 = 2,00 |
| 2 | 20 | 2,00 &divide; 20 = 0,10 | 100 &divide; 50 = 2,00 |
| 3 | 50 | 2,00 &divide; 50 = 0,04 | 100 &divide; 50 = 2,00 |
| 4 | 60 | 0,75 &divide; 60 = 0,0125 = 0,01. | 150 &divide; 200 = 0,75. |

## <a name="escalations-and-discounts"></a>Laiendused ja allahindlused

*Eskaleerimine* on hinnatõus tuleviku arveldusperioodiks, mille jaoks arvet pole veel loodud. *Allahindlus* on hinna alandamine tuleviku arveldusperioodiks, mille jaoks arvet pole veel loodud.

Kordustellimuse arvelduses ei saa laiendusi ja allahindlusi arveldusgraafikule tagasiulatuvalt rakendada. Näiteks ei saa te rakendada laiendust arveldusgraafikule kolm kuud tagasi ja seda töödelda. Teiste sõnadega, ei saa te rakendada hinnatõusu, mis toimus kolm kuud tagasi.

Saate rakendada eskalatsiooni või allahindlust arveldusgraafikule või arveldusgraafiku reale ühel järgmistest kohtadest:

- Kõigi **/aktiivsete arveldusgraafikute loendileht**
- Konkreetne arveldusgraafik
- Konkreetne arveldusgraafiku rida

### <a name="apply-an-escalation-or-discount"></a>Eskalatsiooni või allahindluse rakendamiseks

Eskalatsiooni või allahindluse rakendamiseks arveldusgraafikus järgige neid samme.

1. Valige arveldusgraafik või arveldusgraafiku rida.
2. Valige **laiendus ja allahindlus** vahekaardil Laiendus **ja allahindlus või** arveldusgraafiku real.
3. Kui laienduse või allahindluse arvutamiseks kasutatakse tarbijahinna indeksit, valige **väärtus väljal Tarbimishinna indeks.**
4. Laiendus **-** või allahindlusrea lisamiseks valige väärtus Uus.
5. Allahindluse puhul märkige ruut **Allahindlus**. Laienduse puhul jätke ruut **Allahindlus** tühjaks.
6. Seadke väljad **Alguskuupäev ja** **Sagedus**.
7. Viitvõlaüksuste puhul, mis kasutavad segmentimata tulu funktsiooni, seadistage **väli** Lõppkuupäev.
8. Seadke väli **Protsent**, **Summa või** Tarbimishinna **indeksi** graafik.
9. Seadke väli **Lõppkuupäev**.
10. Valige nupp **OK**.
11. Korrake samme 4 kuni 10 iga täiendava laienduse või allahindluse rea puhul, mida vajate.

### <a name="fields-on-the-billing-schedule-lines-page"></a>Väljad arveldusgraafiku ridade lehel

Arveldusgraafiku **ridade leht** sisaldab järgmisi välju.

| Väli | Kirjeldus |
|---|---|
| Kaubakood | Arveldusgraafiku rea kaubakood. See väli on saadaval ainult siis, kui leht avatakse arveldusgraafiku rea kauba kaudu. |
| Tarbijahinnaindeksi arvutamine | <p>Valige meetod, mida kasutatakse tarbimishinna indeksi laienduse arvutamiseks:</p><ul><li>**Eelnev tarbimishinna indeks** – kasutage laiendusarvutuses eelmise tarbijahinna indeksi väärtust.</li><li>**Baaskliendi hinnaindeks** – kasutage laiendusarvutuses tarbija baashinna indeksi väärtust.</li></ul> |
| **Rea ruudustik** | |
| Allahindlus | <p>Märkige see ruut määramaks, kas summa muudatus on laiendus või allahindlus:</p><ul><li>**Valitud** – muudatus rakendab allahindluse arveldusgraafikule või arveldusgraafiku reale.</li><li>**Tühjendatud** – muudatus rakendub eskalatsioonile arveldusgraafikul või graafiku real.</li></ul><p>Selle märkeruudu sätet ei saa muuta kaupade puhul, mis kasutavad selle arveloleva tulu funktsiooni. Lisaks ei saa allahindlusi rakendada kaupadele, mis kasutavad tulu tükeldamist.</p> |
| Alguskuupäev | Valige laienduse või allahindluse alguskuupäev. |
| Sagedus | Valige laienduse või allahindluse sagedus: **Puudub**, **Kuu**, Kvartal **·**, **Poolaasta** või **Iga-aastane**. |
| Protsent | Määrake laienduse või allahindluse protsent. |
| Summa | Määrake laienduse või allahindluse summa. |
| Tarbijahinnaindeksi graafik | Valige arvutustes kasutatav tarbijahinna indeksi graafik. |
| Lõpukuupäev | <p>Valige laienduse või allahindluse lõppkuupäev.</p><p>**Märkus:** see väli on nõutav kaupade puhul, mis kasutavad segmentimata tulu funktsiooni.</p> |
| Edasilükkamise graafiku number | <p>Viitvõlagraafiku number.</p><p>See väli on saadaval ainult siis, kui leht avatakse arveldusgraafiku realt.</p> |
| Töölehe partiinumber | <p>Töölehe partiinumber.</p><p>See väli on saadaval ainult siis, kui leht avatakse arveldusgraafiku realt.</p> |
| Lõppallahindluse summa | <p>Kõigi ruudustiku ridade allahindluse summade summa.</p><p>See väli on saadaval ainult siis, kui leht avatakse arveldusgraafiku realt.</p> |
| Praegune lühiajaline tasumata tulusumma | <p>Praegune lühiajaliselt tasumata tulusumma.</p><p>See summa ilmub, kui korduva lepingu arveldusparameetrite lehel on **valitud** lühiajaline viitvõlameetod ja reaüksuse kontod **seadistatakse** arveldamata tulu seadistamise lehel.</p> |
| Praegune pikaajaline tasumata tulusumma | <p>Praegune pikaajaline tasumata tulusumma.</p><p>See summa ilmub, kui korduva lepingu arveldusparameetrite lehel on **valitud** lühiajaline viitvõlameetod ja reaüksuse kontod **seadistatakse** arveldamata tulu seadistamise lehel.</p> |

## <a name="proration-examples"></a>Mõõdunäited

Kalkulatsioonid mõõdu jaoks võivad põhineda päevade arvul või kuude arvul. Meetod, mida kasutatakse prorationi arvutamiseks, on seatud korduva lepingu **arveldusparameetrite** lehel. Proration method mõjutab seda, kuidas summasid arveldusgraafiku jaoks arvutatakse järgmistes olukordades:

- Algne loomine
- Laienduse või allahindluse rakendamine
- Lõpetamine
- Ooteluse paigutus või eemaldamine
- Toe lisamine või uuendamine

Mõõdumeetod mõjutab ka igakuise korduva tulu (MRR) aruande kalkulatsioone.

### <a name="example-1"></a>Näide 1

Arveldusgraafiku aastane summa on $5,000. Alguskuupäev on 12. august 2019 ja lõppkuupäev on 22. detsember 2019. Arveldussagedus on iga-aastane. Prorated summa arvutatakse järgmiselt, sõltuvalt sellest, kas kasutatakse päeva või kuu arvutusmeetodit:

- **Kord päevas**

    - *Päevade arv* = *Lõppkuupäev –* Alguskuupäev *·* + 1 = 133 päeva
    - *Päevade arv aastas* = 11. august 2020 – 12. august 2019 + 1 = 366 päeva
    - *Prorated summa* = 5000 &times; (133 &divide; 366) = 1816,94

- **Kord kuus**

    - *Alguskuu osa* = (31 – 12 + 1) &divide; 31 = 20 &divide; 31
    - *Keskkuud* = 3
    - *Lõppkuu osa* = 22 &divide; 31
    - Prorated summa = 5000 &divide; 12 &times;\[(20 &divide; 31) + 3 + (22 &divide; 31)\] = 1814,52

### <a name="example-2"></a>Näide 2

Arveldusgraafiku aastane summa on $12,000. Alguskuupäev on 1. august 2019 ja lõppkuupäev on 31. detsember 2019. Arveldussagedus on iga-aastane. Erksatud summa arvutatakse järgmistel viisidel, sõltuvalt arvutamismeetodist:

- **Kord päevas**

    - *Päevade arv* = *Lõppkuupäev –* Alguskuupäev *·* + 1 = 153 päeva
    - *Päevade arv aastas* = 31. juuli 2020 – 1. august 2019 + 1 = 366 päeva
    - *Prorated summa* = 12 000 &times; (153 &divide; 366) = 5016,39

- **Kuu (terve kuu)**

    - *Kuude arv* = 5
    - *Kuud kokku* = 12
    - *Prorated summa* = (12 000 &times; 5) &divide; 12 = 5000

## <a name="reversing-a-period-billing"></a>Perioodi arvelduse tagasipööramine

Selles näites on arveldusgraafikul ainult üks rida:

- Arveldus tehakse kord kuus 12 kuu jooksul jaanuarist detsembrini.
- Arved on loodud kõigile perioodidele kuni aprillini.

Soovite tühistada aprilli arveldusperioodi arve.

Kui müügiarvet ei oleks aprilli arveldusperioodiks veel loodud, võiksite müügitellimuse kustutada. Sel juhul eemaldatakse **üksikasja** arveldatud olek. Kuna arve on loodud arveldusperioodiks, **ei saa** üksikasja arveldatud olekut kustutada. Seepärast peate aprilli arvelduse tühistamiseks looma rea jaoks lähtestava kreeditarve.

1. Looge leheküljel **Kõik arveldusgraafikud** samale kaubale graafikurida.
2. **Muutke kauba** koguse väärtus esialgse koguse negatiivseks.
3. Häälestage **arveldussageduse** väli **väärtusele One-time**.
4. Värskendage algus- ja lõppkuupäevi nii, et need ühtiksid arvelduse üksikasjarea kuupäevadega, millele soovite kreeditarvet luua. Näiteks seadistage alguskuupäev 1. aprillile 2019 ja lõppkuupäevaks 30. aprill 2019.
5. Salvestage muudatused.
6. Avage leht **Loo** arve ja looge müügitellimus, mille kreeditarve on määratud perioodiks.
7. Valikuline: sisestage arve.

Kui vaatate arveldusgraafiku ridu üle, märkate, et uuel real on seos kreeditarvega. Algsel real on siiski link aprilli originaalarvele.

## <a name="split-item-group-examples"></a>Kaubagrupi näidete tükeldamine

Selle näite puhul kasutatakse järgmist seadistust.

- Korduva lepingu **arveldusparameetrite lehel** on valitud **kaubagrupi alusel** tükeldamine ja **väli Kordumatu graafiku** tüüp on seatud väärtusele **Klient**.
- Loodud on kolm kaubagruppi: **PREFIX**, **DATAHUB** ja **SPP**.
- Kliendi US-001 on mitu arveldusgraafikut, kus kaubagrupp on PREFIX või DATAHUB.
- Kliendi US-002 on mitu arveldusgraafikut, kus kaubagrupp on PREFIX või SPP.

| Arveldusgraafiku number | Klient | Kaubagrupp |
|---|---|---|
| ID- JA ID | US-001 | EESLIIDE |
| ID- JA ID | US-001 | DATAHUB |
| SMAB | US-002 | EESLIIDE |
| IDB | US-002 | SPP |

Klient US-001 oste uuendamiskaupa, mis kuulub kaubagruppi PREFIX. See kanne on uus müügitellimus.

| Müügitellimus # | Klient | Põhikaup | Uuendatav kaup | Kaubagrupi uuendamine | Arveldusgraafiku number |
|---|---|---|---|---|---|
| So0001 (üks) | US-001 | D0001 | D0002 (uuendatud) | EESLIIDE | ID- JA ID |

Müügitellimuse arve sisestamisel lisatakse uuendamisüksus kliendi olemasolevasse arveldusgraafikusse (SCH001). See arveldusgraafik kasutab PREFIX-i kaubagruppi. Kõik samasse kaubagruppi kuuluvad uuendamisüksused pannakse samasse arveldusgraafikusse.

**Päis**
 
| Arveldusgraafiku number | Klient | Kaubagrupp |
|---|---|---| 
| ID- JA ID | US-001 | EESLIIDE |

**Rida**

| Arveldusgraafiku number | Klient | Kaubagrupp |
|---|---|---|
| ID- JA ID | US-001 | D0002 (uuendatud) |

Klient US-001 nüüd uuendamiskaupa, mis kuulub SPP kaubagruppi. See kanne on uus müügitellimus.

| Müügitellimus # | Klient | Põhikaup | Uuendatav kaup | Kaubagrupi uuendamine | Arveldusgraafiku number |
|---|---|---|---|---|---|
| SO0002 | US-001 | D0003 | D0004 (uuendatud) | SPP | |

Praegu ei US-001 kliendi kontol arveldusgraafikut, mis kasutab SPP kaubagruppi. Seetõttu luuakse uus arveldusgraafik.

**Päis**

| Arveldusgraafiku number| Klient | Kaubagrupp |
|---|---|---|
| ID- JA ID | US-001 | SPP |

**Rida**

| Arveldusgraafiku number | Klient | Kaubagrupp |
|---|---|---|
| ID- JA ID | US-001 | D0004 (uuendatud) |

### <a name="multiple-billing-schedules-for-the-same-end-user-and-customer"></a>Mitu arveldusgraafikut samale lõppkasutajale ja kliendile

Selle näite puhul kasutatakse järgmist seadistust.

- Korduva lepingu **arveldusparameetrite lehel** on valitud **kaubagrupi** **alusel tükeldamine ja kordumatu graafiku tüübi** väli on seatud väärtusele **Lõppkasutaja**.
- **Lehel Lõppkasutajad** on seadistatud järgmine kliendi- ja lõppkasutaja suhe.

    | Kliendi konto | Lõppkasutaja konto |
    |---|---|
    | US-001 | US-221 |

Kliendile ja lõppkasutaja kombinatsioonile luuakse mitu arveldusgraafikut. Kuna **korduva lepingu arveldusparameetrite** lehel on **valitud** tükeldamine kaubagrupi alusel, saab samale kliendile ja lõppkasutaja seosele luua mitu arveldusgraafikut.

| Arveldusgraafiku number | Klient | Lõppkasutaja konto | Kaubagrupi päis |
|---|---|---|---|
| ID- JA ID | US-001 | US-221 | IG1 (1) |
| IDB | US-001 | US-221 | IG2 |
| ID-DE ID | US-001 | US-221 | IG3 (IG3) |

Kaupade seadistamise **lehel saate** kaubaseost luua toe ja uuendada.

| Üksuse kood | Kauba seos | Kauba tugi | Uuendatav kaup | Kaubagrupi uuendamine |
|---|---|---|---|---|
| Tabel | D001 (uuendatud) | KAUP 27 | D007 (uuendatud) | IG1 (1) |
| Tabel | D002 (uuendatud) | KAUP 28 | D005 (uuendatud) | IG2 |
| Tabel | D003 (uuendatud) | KAUP 29 | D006 (uuendatud) | IG3 (IG3) |

Nüüd loote müügitellimuse kliendile US-001. Müügitellimusel on kaupu kauba seadistuse **lehelt**. Müügitellimuse loomisel avage toe **ja** uuendamise protsessi leht ning **seadistage** lõppkasutaja konto väli ja muu uuendamiseks vajalik teave.

Kui kande arve luuakse ja sisestatakse, luuakse kliendile/lõppkasutajale ja kaubagrupi kombinatsioonile erinevad arveldusgraafikud. Samale arveldusgraafikule saab määrata mitu rida samal müügitellimusel.

| Müügitellimus # | Klient | Lõppkasutaja konto | Põhikaup | Kauba tugi | Uuendatav kaup | Arveldusgraafiku number |
|---|---|---|---|---|---|---|
| So0001 (üks) | US-001 | US-221 | D001 (uuendatud) | KAUP 27 | D007 (uuendatud) | ID- JA ID |
| So0001 (üks) | US-001 | US-221 | D002 (uuendatud) | KAUP 28 | D005 (uuendatud) | IDB |
| So0001 (üks) | US-001 | US-221 | D003 (uuendatud) | KAUP 29 | D006 (uuendatud) | ID- JA ID |
