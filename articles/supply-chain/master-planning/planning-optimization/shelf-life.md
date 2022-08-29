---
title: Piiratud kõlblikkusajaga toodete koondplaneerimine
description: See artikkel kirjeldab, kuidas seadistada ja kasutada planeerimise funktsioone, mis võtavad arvesse kõlblikkusajaga tooteid.
author: t-benebo
ms.date: 08/10/2022
ms.topic: article
ms.search.form: ReqPlanSched, CustTable, EcoResProductDetailsExtended, InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 95c905cbcc3c057dbccf2b7d6e894b1e99ddfba5
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337356"
---
# <a name="master-planning-for-products-with-limited-shelf-life"></a>Piiratud kõlblikkusajaga toodete koondplaneerimine

[!include [banner](../../includes/banner.md)]

Kõlblikkusaeg on aeg, mille jooksul saab toodet ladustada, kuni seda ei saa enam kasutada ega müüa. Piiratud kõlblikkusajaga toodete puhul kasutate tõenäoliselt esimest aegumisajaga laostrateegiat (FEFO), mis tähtsuseerib kaupade tarbimist ja müüki järelejäänud kõlblikkusaja alusel. See laostrateegia on oluline toiduainete, ekspordi ja muude kaupade puhul, mida iseloomustab lühike ladustamisaeg. VASTAVALT FEFO-le ladustatakse laos olevad kaubad nagu kaubad kaupluse riiulil. Tooted, mille kõlblikkusaeg on pikk, pannakse riiulitele sügavus, nii et kõigepealt tarnitakse lühema säilivusajaga tooted.

## <a name="using-shelf-life-in-master-planning"></a>Kõlblikkusaja kasutamine koondplaneerimises

See jaotis selgitab, kuidas koondplaneerimine soovitab kõlblikkusajaga kaupade tarnimist.

Kui käitate koondplaani, loob see soovitatud plaanitud tellimused (pakkumine), mis vastavad teie nõudlusele ja minimeerivad viivitusi. Kui teie plaan hõlmab kaupu, mille kõlblikkusiga on piiratud, muutuvad plaanikalkulatsioonid keerukamaks, sest plaan ei tohi mitte üksnes vähendada viivitusi, vaid kasutada enne selle aegumist ka olemasolevat tarnet. Plaan peab proovima kasutada tarnet, mis on aegumiskuupäevale kõige lähem, enne kui tarne aegub hiljem. Seetõttu püütakse koondplaneerimisel saavutada järgmised eesmärgid selles järjekorras:

1. Viivituste summa minimeerimine.
1. Suurendage FEFO tarne summat.
1. Minimeerige varude täiendamist.

Mõnel juhul võib esimese kahe eesmärgi vahel olla konflikt ja tuleb valida: kas soovite saadetisega viivitada või soovite kasutada tarnet, mis aegub hiljem, selle asemel, et tarne aeguks kiiremini? Selle konflikti lahendamiseks koondplaneerimise ajal seadistab süsteem viivituste tähtsusastet, kasutades aegunud tarneid. Üldiselt esineb seda tüüpi konflikt siis, kui võib esineda viivitusi ja laovarusid perioodi alusel. Seetõttu on soovitatav kasutada laovarude perioodi, mis on lühem kui kauba kõlblikkusaeg. Muud tüüpi laovarud (nt vajadus) on seda tüüpi konflikti korral ebatõenäolised.

## <a name="set-up-shelf-life"></a>Seadista kõlblikkusaeg

### <a name="configure-each-master-plan-to-consider-shelf-life"></a>Konfigureerige iga koondplaan kõlblikkusaja arvesse võtma.

Vaikimisi ei arvesta koondplaanid kõlblikkusiga. Kasutage järgmist protseduuri, et lubada kõlblikkusaja kalkulatsioone iga koondplaani puhul, mis neid nõuab.

1. Minge koondplaneerimise **seadistusplaanide \>\> koondplaanide \> juurde**.
1. Valige loendipaanil olemasolev plaan või looge uus.
1. Seadke kiirkaardi **Üldine** suvand Kasuta kõlblikkusaja **kuupäevi väärtusele** *Jah*.

### <a name="configure-tracking-dimension-groups-to-track-the-batch-dimension"></a>Jälgimisdimensioonigruppide konfigureerimine partiidimensiooni jälgimiseks

Kauba kõlblikkusaega saab jälgida ainult siis, kui seda kaupa jälgitakse partii dimensioonis. See tähendab, et partii viide ja nõutavad kuupäevad tuleb kirjendada sissetuleku või tootmise ajal ja läbi iga kauba laokande. Selle suvandi haldamiseks seadistage üks või mitu jälgimisdimensiooni gruppi nõutud jälgimiseks ja seejärel määrake nendele gruppidele vajalikud kaubad vastavalt vajadusele.

Kasutage järgmist protseduuri jälgimisdimensioonigrupi häälestamiseks partii dimensiooni jälgimiseks.

1. Minge tooteteabe **halduse häälestuse \> dimensiooni \>- ja variandigruppide jälgimisdimensioonigruppidesse \>**.
1. Järgige üht neist sammudest.

    - Tegevuspaanil valige uue **jälgimisdimensioonigrupi** loomiseks uus. Sisestage nimi ja kirjeldus ning seejärel valige **tegevuspaanil** salvestamine.
    - Valige loendipaanil olemasolev jälgimisdimensioonigrupp, mille soovite seadistada pakett-töö dimensiooni jälgimiseks.

1. Märkige jälgimisdimensiooni kiirkaardi real **Partii number** ruudud veergudes **Aktiivne** ja **Füüsiline laovaru**.**·**

### <a name="set-up-shelf-life-for-a-product"></a>Toote kõlblikkusaja seadistamine

Kasutage järgmist protseduuri, et seadistada toote kõlblikkusaeg.

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Looge või avage toode, mida soovite seadistada.
1. Kõlblikkusaja sätete kasutamiseks seadke kiirkaardi Üldine kiirkaardil jälgimisdimensiooni grupi väli jälgimisdimensiooni grupile, **mis** on **seadistatud** partii dimensiooni jälgimiseks. Selle välja saate seada ainult toote loomisel. Olemasolevate toodete väärtust ei saa muuta.
1. Seadke kiirkaardil **Varude** haldamine järgmised väljad:

    - **Säilivusatriksi** periood päevades – määrake periood (päevades), millega kontrollida selle toote partiid, et tagada selle sobivs tarbimiseks või edasimüügiks. Selle välja väärtus lisatakse partii tootmiskuupäevale, et *määrata* selle säilivusatriksi *kuupäev*. Saate konfigureerida süsteemi kvaliteettellimuste loomiseks, kui partii läheneb säilivusaviisi kuupäevale.
    - **Kõlblikkusaja** periood päevades – määrake päevade arv enne selle toote partii aegumist. Aegumiskuupäeva määratlemiseks lisatakse *see väärtus tootmiskuupäevale* *.* Pärast seda kuupäeva peetakse partii kasutamiskõlbmatuks.
    - **Parim enne perioodi päevades** – määrake periood (päevades), pärast mida peetakse selle toote partii veel müütavaks, kuid ei saa enam säilitada osa selle algsetest atribuutidest. See väärtus lisatakse tootmise kuupäevale *, et* määrata parim *enne kuupäev*. Saate käivitada aruandeid, et tuvastada kaubavarud, mis on möödunud selle parim enne kuupäevast. 

### <a name="set-a-sellable-days-rule-for-each-customer"></a>Määrake igale kliendile müümispäevade reegel.

*Müümispäevade* funktsioon tagab, et varsti aeguva partii tooteid ei saadeta klientidele. Lisaks sellele tagab see, et kui tooted saadetakse kliendile, jääb pärast tarnimist alles piisav arv müümispäevi.

Müümispäevade funktsiooni kasutamiseks peate igale kliendile määrama müümispäevade arvu. Peate selle protsessi käsitsi lõpule viima, kuna selle jaoks pole andmeüksust.

Kasutage järgmist protseduuri, et seadistada igale kliendile iga toote kohta müümispäevad.

1. Avage jaotis **Müük ja turundus \> Kliendid \> Kõik kliendid**.
1. Otsige ja valige klient, kellele soovite seadistada.
1. Valige tegevuspaani vahekaardi Müümine jaotises Seadistus **suvand** Müümispäevad **·** **.\>**
1. Kliendilehe **müümispäevadel loetleb** ruudustik iga toote või tootegrupi olemasolevad müümispäevade reeglid. Kasutage tegumiriba nuppe ruudustiku ridade lisamiseks või redigeerimiseks vastavalt vajadusele. Saadaval **on** filter, mis aitab leida olemasolevaid ridu.
1. Määrake igas reas järgmised väljad.

    - **Kaubakood** : valige üks järgmistest väärtustest, et määrata mõjutatud kaupade ulatus:

        - *Tabel* – rida kehtib konkreetse kauba kohta.
        - *Grupp* – rida kehtib konkreetse kaubagrupi kohta.
        - *Kõik* – rida kehtib kõigi kaupade kohta.

    - **Kauba seos** – kui seate välja **Kaubakood** väärtuseks *Tabel*, valige kindel kaup. Kui seate välja **Kaubakood** väärtuseks *Grupp*, valige kaubagrupp. Kui seate välja **Kaubakood** väärtuseks *Kõik*, pole see väli saadaval.
    - **Müümispäevad** – sisestage minimaalne päevade arv, mille jooksul peab klient müüma vastavaid tooteid enne partii aegumist. Müümispäevade väärtus põhineb taotletud vastuvõtukuupäeval (või kinnitatud vastuvõtukuupäeval, kui see on määratud) vastavate toodete puhul müügitellimusel.
    - *(Muud tootedimensioonid)* – rea ulatuse täiendavaks piiramiseks määrake soovitud dimensiooniväärtused (nt **Suurus** **ja** Värv). Ruudustikus kuvatavate dimensioonide avamiseks valige **tegevuspaanil** kuva dimensioonid.

### <a name="set-up-all-relevant-products-so-that-they-are-fefo-date-controlled"></a>Seadistage kõik asjakohased tooted nii, et nad on FEFO kuupäevakontrolliga

Müümispäevade tööks peab iga asjakohane **kaup kuuluma kauba mudeligruppi, kus on märgitud FEFO** kuupäevakontrolliga märkeruut.

Kasutage järgmist protseduuri kauba mudeligrupi häälestamiseks nii, et see toetab müümispäevade funktsiooni.

1. Avage **Varude haldus \> Seadistus \> Varud \> Kauba mudeligrupid**.
1. Valige loendipaanil olemasolev grupp või looge uus, valides tegevuspaanil **valiku** Uus.
1. Varude poliitikate **kiirkaardil** valige **FEFO kuupäevakontrolliga** märkeruut.
1. Seadistage grupile muud väljad, nagu on nõutud.

Kasutage järgmist protseduuri, et vaadata või seadistada kauba mudeligruppi, kuhu toode kuulub.

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Avage toode, mida soovite üle vaadata või redigeerida.
1. Seadke üldisel **kiirkaardil** kauba **mudeligrupi väli** grupile, kus **on valitud FEFO kuupäevakontrolliga** märkeruut.

## <a name="example-1-simple-fefo-10-day-period-zero-days-of-lead-time"></a>Näide 1: Simple FEFO, 10-päevane periood, null päeva täitmisaega

See näide näitab kõlblikkusaja põhi näidet, kus tarnetellimuste ja nõudluse vahel toimub sidumine süsteemi järgmiste eesmärkide täitmiseks:

- Viivituste summa minimeerimine.
- Suurendage FEFO tarne summat.
- Minimeerige varude täiendamist.

Süsteemil on järgmised üksuse ja koondplaani sätted:

- **Laovarude kood (täiendusstrateegia):** periood 
- **Laovarude periood:** 10 päeva (võrdub kõlblikkusajaga)
- **Kõlblikkusaeg:** 10 päeva
- **Müümispäevad:** 0 päeva
- **Täitmisaeg:** 0 päeva
- **Negatiivsed päevad:** 0 päeva
- **Plaanitud tellimuse tüüp (kauba tellimuse vaikesätted):** ostutellimus

Süsteemis on kauba kohta järgmised müügitellimused:

- **SO1:** kogus (kogus) = 2, nõutav tarnekuupäev = täna + 1 päev
- **SO2:** Kogus = 1, nõutav tarnekuupäev = täna + 4 päeva
- **SO3:** Kogus = 1, nõutav tarnekuupäev = täna + 5 päeva

Kõik need müügitellimused loovad kaubale nõudluse.

Kaubal on olemas järgmine tarne:

- **Vaba kaubavaru: kogus** = 1, aegumiskuupäev = täna + 5 päeva
- **Ostutellimus 1 (PO1): vastuvõtukuupäev** = täna + 2 päeva, kogus = 1, aegumiskuupäev = täna + 4 päeva

Süsteem loob pakkumise loendi, mis võib seda nõudlust katta ja sordib loendi aegumiskuupäeva järgi (kasutades FEFO-t).

Koondplaneerimine loob nõutava sidumise pakkumise ja nõudluse vahel. See loob ka mis tahes nõutava nõudluse, mis põhineb tarneloendil (kasutades FEFO-t) ja võtab arvesse kättesaadavuse kuupäeva.

- So1 saab täita vaba kogusega, kuid seda ei saa täita PO1-ga, kuna OSTUTELLIMUSE 1 saadavuskuupäev on üks päev hiljem, kui soet-1 nõuab. Seetõttu loob SO1 nõudluse ühele kaubaühikule.
- So2 võib olla po1-ga kaetud, kuna ostutellimus 1 saabub nõutavaks ajaks ja aegumiskuupäev on endiselt kehtiv. Seetõttu on SO2 nõue PO1-ga täielikult kaetud.
- SO3 ei ole kaetud, kuna ressursid pole saadaval. Seetõttu loob SO3 nõudluse ühele kaubaühikule.

Kõigi ülejäänud nõuete katmiseks peab süsteem looma järgmise plaanitud ostutellimuse:

- **PPO1: vastuvõtukuupäev** = täna, kogus = 2, aegumiskuupäev = täna + 10 päeva

Järgmine tabel võtab tulemuse kokku.

| Nõudlus | Sidumine |
|---|---|
| **SO1:** tarnekuupäev = täna + 1 päev, kogus = 2 | <p>**Laoseis: kogus** = 1, aegumiskuupäev = täna + 5 päeva</p><p>**PPO1: vastuvõtukuupäev** = täna, kogus = 1, aegumiskuupäev = täna + 10 päeva</p> |
| **SO2:** tarnekuupäev = täna + 4 päeva, kogus = 1 | **PO1:** sissetuleku kuupäev = täna + 2 päeva, 1 kogus, aegumiskuupäev = täna + 4 päeva |
| **SO3:** tarnekuupäev = täna + 5 päeva, kogus = 1 | **PPO1: vastuvõtukuupäev** = täna, kogus = 2, aegumiskuupäev = täna + 10 päeva |

Järgmine näide näitab selle näite ajajoont.

![Näide 1: Simple FEFO, 10-päevane periood, null päeva täitmisaega.](media/fefo-example-1.png "Näide 1: Simple FEFO, 10-päevane periood, null päeva täitmisaega")

## <a name="example-2-simple-fefo-requirement-three-days-of-lead-time"></a>Näide 2: Simple FEFO, nõue, kolm täitmisaega

See näide näitab, kuidas süsteemi püüe viivitusi vähendada võib vahel põhjustada ületellimuse tegemist.

Süsteemil on järgmised üksuse ja koondplaani sätted:

- **Laovarude kood (täiendusstrateegia):** vajadus
- **Kõlblikkusaeg:** 10 päeva
- **Müümispäevad:** 0 päeva
- **Täitmisaeg:** määratud järgmiste hankija kaubandusleppetega:

    - **Kaubandusleleping 1:** kui kogus = 1, täitmisaeg = 4
    - **Kaubandusleleping 2:** kui kogus = 2, täitmisaeg = 3

- **Negatiivsed päevad:** 0 päeva
- **Plaanitud tellimuse tüüp (kauba tellimuse vaikesätted):** ostutellimus

Süsteemis on olemas järgmine müügitellimus:

- **SO1:** Kogus = 2, nõutav tarnekuupäev = täna + 3 päeva

See nõudlus hõlmab olemasolevat pakkumist ja kinnitatud ostutellimust:

- **Vaba kaubavaru: vaba** = täna, kogus = 1, aegumiskuupäev = täna + 2 päeva
- **PO1:** sissetuleku kuupäev = täna + 3 päeva, kogus = 1, aegumiskuupäev = täna + 4 päeva

Laoseisu SO1 ei saa täita vaba kaubavaruga, kuna varude aegumiskuupäev on saatmiskuupäevast varem. Po1 võib katta SO1 nõude ainult 1-st kogusest. Seetõttu loob SO1 nõudluse ühele kaubaühikule. Selle vajaduse katmiseks loob süsteem plaanitud ostutellimuse (PPO1).

Süsteemil on kaks kaubandusleppet (üks kogusele = 1, täitmisaeg = 4 päeva ja teine kogusele = 2, täitmisaeg = 3 päeva). Seetõttu püüab süsteem viivitusi vähendada, luues teise kaubanduslelepingule vastavad plaanitud ostutellimused (PPO1). Tulemuseks on ületarne (kogus = 2, aegumiskuupäev = täna + 10 päeva).

Järgmine tabel võtab tulemuse kokku.

| Nõudlus | Sidumine |
|---|---|
| **SO1:** tarnekuupäev = täna + 3 päeva, kogus = 2 | <p>**PO1:** sissetuleku kuupäev = täna + 3 päeva, kogus = 1, aegumiskuupäev = täna + 4 päeva</p><p>**PPO1: sissetuleku** kuupäev = täna + 3 päeva, kogus = 1, aegumiskuupäev = täna + 10 päeva</p> |

Järgmine näide näitab selle näite ajajoont.

![Näide 2: Simple FEFO, nõue, kolm täitmisaega.](media/fefo-example-2.png "Näide 2: Simple FEFO, nõue, kolm täitmisaega")

## <a name="example-3-simple-fefo-requirement-three-days-of-lead-time-five-sellable-days"></a>Näide 3: Simple FEFO, nõue, kolm täitmisaega, viis müümispäeva

See näide näitab, kuidas kõlblikkusiga toimib, kui kaubale lisatakse müümispäevad.

Süsteemil on järgmised üksuse ja koondplaani sätted:

- **Laovarude kood (täiendusstrateegia):** vajadus
- **Kõlblikkusaeg:** 10 päeva
- **Müümispäevad:** 5 päeva
- **Täitmisaeg:** 5 päeva
- **Negatiivsed päevad:** 0 päeva
- **Plaanitud tellimuse tüüp (kauba tellimuse vaikesätted):** ostutellimus

Süsteemis on järgmised müügitellimused:

- **SO1:** Kogus = 2, nõutav tarnekuupäev = täna + 2 päeva
- **SO2:** Kogus = 1, nõutav tarnekuupäev = täna + 3 päeva
- **SO3:** Kogus = 1, nõutav tarnekuupäev = täna + 5 päeva

Seda nõudlust saab katta olemasolev pakkumine ja kinnitatud ostutellimus:

- **Vaba kaubavaru: vaba** = täna, kogus = 1, aegumiskuupäev = Täna + 6 päeva
- **PO1:** sissetuleku kuupäev = täna + 2 päeva, kogus = 3, aegumiskuupäev = täna + 10 päeva

Süsteem loob sidumiskandidaatide loendi, mis põhineb pakkumise (FEFO) loendi ja kättesaadavuse kuupäevadel. Seega ei saa laoseisuga SO1 täita, kuna see ladu aegub enne kliendi nõutavate müümispäevade lõppu (nõutav sissetuleku kuupäev + 5 päeva). PO1 võib so 1 nõude katta kahe ühikuga ja so2 vajadus ühe ühikuga. Seetõttu on siiski katmata nõudlust ühe kaubaühiku järele ainult SO3 puhul. Selle vajaduse katmiseks loob süsteem järgmise plaanitud ostutellimuse:

- **PP01: sissetuleku** kuupäev = täna + 5 päeva, kogus = 1, aegumiskuupäev = täna + 10 päeva

Järgmine tabel võtab tulemuse kokku.

| Nõudlus | Sidumine |
|---|---|
| **SO1:** tarnekuupäev = täna + 2 päeva, kogus = 2 | **PO1:** sissetuleku kuupäev = täna + 2 päeva, kogus = 2, aegumiskuupäev = täna + 10 päeva |
| **SO2:** tarnekuupäev = täna + 3 päeva, kogus = 1 | **PO1:** sissetuleku kuupäev = täna + 2 päeva, kogus = 1, aegumiskuupäev = täna + 10 päeva |
| **SO3:** tarnekuupäev = täna + 5 päeva, kogus = 1 | **PPO1: sissetuleku** kuupäev = täna + 5 päeva, kogus = 1, aegumiskuupäev = täna + 10 päeva |

Järgmine näide näitab selle näite ajajoont.

![Näide 3: Simple FEFO, nõue, kolm täitmisaja päeva, viis müümispäeva.](media/fefo-example-3.png "Näide 3: Simple FEFO, nõue, kolm täitmisaega, viis müümispäeva")

## <a name="example-4-simple-fefo-period-lead-time-depends-on-the-quantity"></a>Näide 4: Simple FEFO, periood, täitmisaeg sõltub kogusest

See näide näitab, kuidas süsteemi püüe viivitusi vähendada võib vahel põhjustada ületellimuse tegemist.

Süsteemil on järgmised üksuse ja koondplaani sätted:

- **Laovarude kood (täiendusstrateegia):** periood
- **Laovarude periood:** 10 päeva (võrdub kõlblikkusajaga)
- **Kõlblikkusaeg:** 10 päeva
- **Müümispäevad:** 0 päeva
- **Täitmisaeg:** määratud järgmiste hankija kaubandusleppetega:

    - **Kaubandusleleping 1:** kui kogus = 1, täitmisaeg = 5
    - **Kaubandusleleping 2:** kui kogus = 2, täitmisaeg = 0

- **Negatiivsed päevad:** 0 päeva
- **Plaanitud tellimuse tüüp (kauba tellimuse vaikesätted):** ostutellimus

Süsteemis on järgmised müügitellimused:

- **SO1:** Kogus = 1, nõutav tarnekuupäev = täna
- **SO2:** Kogus = 1, nõutav tarnekuupäev = täna + 6 päeva

Seda nõudlust saab osaliselt katta järgmiste kinnitatud ostutellimuste olemasolev pakkumine:

- **PO1:** sissetuleku kuupäev = täna + 1 päev, kogus = 1, aegumiskuupäev = täna + 2 päeva
- **PO2:** sissetuleku kuupäev = täna + 3 päeva, kogus = 1, aegumiskuupäev = täna + 7 päeva

Süsteemil on kaks kaubandusleppet (üks kogusele = 1, täitmisaeg = 5 päeva ja teine kogusele = 2, täitmisaeg = 0 päeva). Seetõttu püüab süsteem vähendada viivitust, luues järgmise plaanitud ostutellimuse, mis vastab teisele kaubanduslepingule:

- **PP01: vastuvõtukuupäev** = täna, kogus = 2, aegumiskuupäev = täna + 10 päeva

SO1 kaetakse PPO1-st ühe ühikuga. SO2 hõlmab ostutellimust 2, kuna ostutellimuse2 aegub kiiremini kui PPO1.

Järgmine tabel võtab tulemuse kokku.

| Nõudlus | Sidumine |
|---|---|
| **SO1:** tarnekuupäev = täna, kogus = 1 | **PPO1: vastuvõtukuupäev** = täna, kogus = 1, aegumiskuupäev = täna + 10 päeva |
| **SO2:** tarnekuupäev = täna + 6 päeva, kogus = 1 | **PO2:** sissetuleku kuupäev = täna + 3 päeva, kogus = 1, aegumiskuupäev = täna + 7 päeva |

> [!NOTE]
> Ostutellimust PO1 ei kasutata, kuna see saabub S01 jaoks liiga hilja ja aegub enne S02 tarnimist. PPO1 on ülejärjestatud ühe ühiku järgi, et täitmisaeg oleks 0 (null) kaubanduslelepingu 2 kohta.

Järgmine näide näitab selle näite ajajoont.

![Näide 4: Simple FEFO, periood, täitmisaeg sõltub kogusest.](media/fefo-example-4.png "Näide 4: Simple FEFO, periood, täitmisaeg sõltub kogusest")

## <a name="example-5-simple-fefo-requirement-10-negative-days"></a>Näide 5: Simple FEFO, nõue, 10 negatiivset päeva

<!-- KFM: This is more of a negative days example than a shelf life example. We should point out more explicitly how shelf life affects this situation (or maybe otherwise remove this example). -->

See näide näitab, kuidas toimib kõlblikkusiga, kui kaubale lisatakse suur arv negatiivseid päevi. Negatiivsed päevad on päevade arv, mille võrra soovite oodata, enne kui tellite negatiivse laovaruga kauba varude täiendamist. Süsteem ei loo tarnet, kui negatiivsete päevade arv ei ole ületatud.

Süsteemil on järgmised üksuse ja koondplaani sätted:

- **Laovarude kood (täiendusstrateegia):** vajadus
- **Täitmisaeg:** 0 päeva
- **Negatiivsed päevad:** 10 päeva
- **Plaanitud tellimuse tüüp (kauba tellimuse vaikesätted):** ostutellimus

Süsteemis on olemas järgmine müügitellimus:

- **SO1:** Kogus = 1, nõutav tarnekuupäev = täna

Selle nõudluse saab katta olemasoleva pakkumisega järgmisest kinnitatud ostutellimusest:

- **PO1:** sissetuleku kuupäev = täna + 3 päeva, kogus = 1, aegumiskuupäev = täna + 5 päeva

Kuna süsteem on konfigureeritud lubama 10 negatiivset päeva, katab see SO1 nõudluse ostutellimusega 1, kuigi tulemuseks on kolme päeva viivitus, kuna SO1 loob negatiivse laovaru kuni ostutellimuse 1 saabumiseni. Plaanitud ostutellimust ei looda, kuigi täitmisaeg on 0 (null) ja plaanitud ostutellimuse loomine vähendaks viivitusi.

Järgmine tabel võtab tulemuse kokku.

| Nõudlus | Sidumine |
|---|---|
| **SO1:** tarnekuupäev = täna, kogus = 1 | **PO1:** sissetuleku kuupäev = täna + 3 päeva, kogus = 1, aegumiskuupäev = täna + 5 päeva |

Järgmine näide näitab selle näite ajajoont.

![Näide 5: Simple FEFO, nõue, 10 negatiivset päeva.](media/fefo-example-5.png "Näide 5: Simple FEFO, nõue, 10 negatiivset päeva")

## <a name="example-6-simple-fefo-requirement-five-negative-days"></a>Näide 6: Simple FEFO, nõue, viis negatiivset päeva

See näide näitab, kuidas toimib kõlblikkusaeg, kui kauba negatiivsete päevade arv on väiksem kui selle kõlblikkusaja periood.

Süsteemil on järgmised üksuse ja koondplaani sätted:

- **Laovarude kood (täiendusstrateegia):** vajadus
- **Müümispäevad:** 0 päeva
- **Täitmisaeg:** 0 päeva
- **Negatiivsed päevad:** 5 päeva
- **Plaanitud tellimuse tüüp (kauba tellimuse vaikesätted):** ostutellimus

Süsteemis on olemas järgmine müügitellimus:

- **SO1:** Kogus = 2, nõutav tarnekuupäev = täna

Selle nõudluse saab katta järgmiste kinnitatud ostutellimuste olemasolevate tarnete abil:

- **PO1:** vastuvõtukuupäev = täna, kogus = 1, aegumiskuupäev = täna + 1 päev
- **PO2:** sissetuleku kuupäev = täna + 2 päeva, kogus = 1, aegumiskuupäev = täna + 3 päeva

Süsteem peab siiski arvesse võtma piirangut, et saadetud kaupu ei saa lähetamise ajal aegunuks muuta. Seetõttu ei saa ostutellimuse 2 ja PO1 puhul soetud ostutellimust 1 kasutada, kuna ostutellimus 1 aegub enne ostutellimuse 2 saabumist. Süsteem loob järgmise plaanitud ostutellimuse nii, et see lõpetaks soostutellimuse nõudluse 1 puhul:

- **PPO1: vastuvõtukuupäev** = täna, kogus = 1, aegumiskuupäev = täna + 10 päeva

Süsteem saab kasutada viite negatiivset päeva ning kasutada SO1 katmiseks ostutellimusi PO2 ja PPO1. Kuid see lähenemine põhjustab tarne hilinemise po2 saabumiseni ja po1 aegub vahepeal. Seepärast katab süsteem SO1, kasutades PPO1-d ja OSTUTELLIMUSt 1.

Järgmine tabel võtab tulemuse kokku.

| Nõudlus | Sidumine |
|---|---|
| **SO1:** tarnekuupäev = täna, kogus = 2 | <p>**PO1:** vastuvõtukuupäev = täna, kogus = 1, aegumiskuupäev = täna + 1 päev</p><p>**PPO1: vastuvõtukuupäev** = täna, kogus = 1, aegumiskuupäev = täna + 10 päeva</p> |

Järgmine näide näitab selle näite ajajoont.

![Näide 6: Simple FEFO, nõue, viis negatiivset päeva.](media/fefo-example-6.png "Näide 6: Simple FEFO, nõue, viis negatiivset päeva")
