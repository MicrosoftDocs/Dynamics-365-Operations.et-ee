---
title: Puhvri profiil ja tasemed
description: See artikkel annab teavet puhverprofiilide ja tasemete kohta, mis määravad minimaalsed ja maksimaalsed laotasemed, mida tuleb iga dekodeerimispunkti puhul säilitada.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ReqItemDecoupledLeadTime
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 57ee6206da926d0dbf62f562197538bfcdd41148
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428140"
---
# <a name="buffer-profile-and-levels"></a>Puhvri profiil ja tasemed

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Pärast dekodeerimispunktide tuvastamist (võtmeüksused, mida strateegiliselt laos hoiate), peate otsustama, kui palju varusid (puhver) igas neist alles hoiate. See ülesanne on nõudlusepõhiste materjalide ressursiplaanimise (DDMRP) teine samm.

## <a name="buffer-levels-and-zones"></a>Puhvritasemed ja tsoonid

DDMRP-s määratakse iga laopuhver kolme väärtuse abil: minimaalne kogus, maksimaalne kogus ja järeltellimuse punkt. Need väärtused määratlevad kolme erinevusega tsooni, mida määratlevad järgmised värvikoodid:

- **Punane tsoon** – ala alla miinimumkoguse. Miinimumkogusele viidatakse ka kui "punase ülemisele kogusele" ja teie planeerimisstrateegia peaks olema loodud tagamaks, et laotasemed on alati sellest punktist kõrgemal.
- **Kollane tsoon** – minimaalse koguse ja järeltellimuse punkti vaheline ala. Kordustellimuse punkti nimetatakse ka "kollase ülaosaks". Kui see punkt on saavutatud, peaks süsteem ümbertellimuse tegema.
- **roheline tsoon** – ümberjärjestava punkti ja maksimaalse koguse vaheline ala; Maksimaalset kogust nimetatakse ka "rohelise ülaosaks". See punkt on maksimaalne tase, milleni varusid täiendatakse.

Järgmine näide näitab kolme värvitsooni ning selle kohta, kuidas need on seotud miinimumkoguse, suurima koguse ja lisatellimusepunktiga.

![DDMRP puhvertsoonid ja -tasemed.](media/ddmrp-buffer-levels.png "DDMRP puhvertsoonid ja -tasemed")

## <a name="calculating-the-buffer-zones"></a>Puhvertsoonide arvutamine

See jaotis selgitab, kuidas iga puhvertsooni kõrgust arvutatakse.

Kollane tsoon arvutatakse tavaliselt esimesena. See tsoon tähistab kogust, mida tarbite alates tellimuse tellimise ajast kuni tellimuse saabumiseni. Teisisõnu on see täiendamise täitmisaja eeldatav tarbimine. See arvutatakse järgmise võrrandi abil:

- **Kollase tsooni** = *keskmine igapäevane kasutus (ADU)* × dekodeeritud *täitmisaeg*

Dekodeeritud *täitmisaeg* näitab aega, mis on kauba tootmiseks või vastuvõtuks vajalik, kui dekodeerimise punktid on alati laos. Tavaliselt on see palju lühem kui koondplaneerimises *tavaliselt* kasutatav kumulatiivne täitmisaeg. Õiged puhvrisätted on võtmeks, kindlustades, et dekodeerimise punktid on alati laos, kuid mitte ülekaupa.

Punane tsoon arvutatakse järgmiste võrrandite abil:

- **Punane alus** = *ADU* × Dekodeeritud *täitmisaeg* × täitmisaja *faktoriga*
- **Punane ohutus** = *punane ×* hälbetegur *·*
- **Punane tsoon** = *Punane alus* + *, punane ohutus*

Roheline tsoon arvutatakse järgmise kolme võrrandi maksimaalse tulemusena:

- *Minimaalne tellimusekogus*
- *Tellimuse ×* ADU *·*
- *ADU* × *dekodeeritud täitmisaeg* × täitmisaja *faktoriga*

## <a name="calculating-average-daily-usage"></a>Keskmise päevase kasutuse arvutamine

Süsteem kasutab ühte kolmest lähenemisest, et arvutada päeva kohta tarbitav summa:

- **Keskmine igapäevane kasutus (minevikus)** – selline lähenemine põhineb tegelikul mineviku tarbimisel.
- **Keskmine igapäevane kasutus (edasi)** – selline lähenemine põhineb prognoositud tulevasel tarbimisel.
- **Keskmine igapäevane kasutus (kombineeritud)** – selline lähenemine põhineb möödunud ja prognoositud tarbimise kaalutud segamist.

### <a name="average-daily-usage-past"></a>Keskmine igapäevane kasutus (minevikus)

Möödunud ADU arvutatakse keskmisena, lisades kogused, mida kasutatakse igal päeval määratud arvu möödunud päevade kohta ja jagades seejärel kogusumma päevade arvuga. Järgnev näide näitab, kuidas see lähenemine toimib, kui kalkulatsioon näeb kolme päeva tagasi.

![Keskmise päevakasutuse (möödunud) diagramm.](media/ddmrp-adu-past.png "Keskmise päevase kasutamise (möödunud) diagramm")

Eelmise näite korral, kui täna on 11. juuni hommikul, on eelmise kolme päeva (8. juuni, 9. ja 10. juuni) ADU 21.

- **ADU (minevikus)** = (29 + 11 + 23) ÷ 3 = 21

Keskmise päevase kasutuse (möödunud) arvutamisel võetakse arvesse järgmisi kandeid:

- Kanded, mis vähendavad kauba kogust (tabelis `inventtrans`, kus kogus on väiksem kui null)
- Kanded olekuga Tellimusel *, Reserveeritud* *tellitud, Füüsiliselt* *reserveeritud*, Komplekteeritud *·*, *Maha* arvatud või *Müüdud*
- Kanded, mille kuupäev jääb valitud tagasisuunas perioodi (keskmine igapäevane kasutus möödunud perioodiks)
- Kanded, mis pole laotöö, vahelaod, müügipakkumised või väljavõtted (`WHSWork`, `WHSQuarantine``SalesQuotation` või`Statement`)
- Kanded, mis ei ole üleviimistöölehed, mis on samas laovarude dimensioonis

### <a name="average-daily-usage-forward"></a>Keskmine igapäevane kasutus (edasi)

Uue toote puhul ei pruugi teil olla möödunud kasutusandmeid. Seetõttu võite selle asemel kasutada prognoositud ADU-d, mis läheb edasi (nt prognoositud nõudluse alusel). Järgnev näide näitab, kuidas selline lähenemine toimib, kui arvutus ilmub kolm päeva ette (kaasa arvatud täna).

![Keskmine päevase kasutuse (edasi) diagramm.](media/ddmrp-adu-forward.png "Keskmise päevase kasutuse (edasi) diagramm")

Eelmise näite korral, kui täna on 11. juuni hommikul, on järgmise kolme päeva (11. juuni, 12. ja 13. juuni) ADU 21,66.

- **ADU (edasi)** = (18 + 18 + 29) ÷ 3 = 21,66

Keskmise päevase kasutuse (edasi) arvutamisel võetakse arvesse järgmisi kandeid:

- Eelarvekanded selle kauba kohta, mille eelarve on koondplaanil valitud
- Kanded, mille kuupäev jääb valitud tähtpäeva perioodi (keskmine päevane kasutus edasisuunas periood)

### <a name="average-daily-usage-blended"></a>Keskmine igapäevane kasutus (kombineeritud)

Kombineeritud ADU kombineerib keskmise möödunud kasutust ja keskmist edasikasutust, nagu näha järgmises illustratsioonis.

![Keskmise päevase kasutuse (kombineeritud) diagramm.](media/ddmrp-adu-blended.png "Keskmise päevase kasutuse (kombineeritud) diagramm")

Eelmise näite korral, kui täna on 11. juuni hommikul, on eelmise ja järgmise kolme päeva ADU (8. juuni kuni 13. juuni) 21,33.

- **Kombineeritud ADU** = (*ADU möödunud* + *ADU edasi*) ÷ 2<br>= (21 + 21,66) ÷ 2<br>= 21,33

## <a name="buffer-calculation-factors"></a>Puhvri arvutustegurid

Iga kauba puhul saate määrata kaks tegurit, et korrigeerida, kui suured peaksid olema punased ja rohelised tsoonid. Sel viisil saate kompenseerida eeldatavat täitmisaega ja nõudluse hälbeid.

![Täitmisaja ja hälbe tegurid.](media/ddmrp-zone-factors.png "Täitmisaja ja hälbe tegurid")

Esimene tegur on täitmisaja *tegur*. Väärtus on kümnendväärtus 0-st 1-ni. Mida pikem on täitmisaeg, seda madalam peaks väärtus olema. Demand Driven Institute soovitab järgmisi vahemikeid:

- **Pikk täitmisaeg:** 0,20–0,40
- **Keskmine täitmisaeg:** 0,41–0,60
- **Lühike täitmisaeg:** 0,61–1,00

Teine tegur on *hälbetegur*. Väärtus on kümnendväärtus 0-st 1-ni. Mida kõrgem on nõudluse hälve, seda madalam peaks väärtus olema. Demand Driven Institute soovitab järgmisi vahemikeid:

- **Väike hälve:** 0,20–0,40
- **Keskmine hälve:** 0,41–0,60
- **Kõrge hälve:** 0,61–1,00

## <a name="buffer-calculation-examples"></a>Puhvri arvutamise näited

See näide jätkub tootmisse, mida pakub Varude [paigutamises toodud tootmisnäide](ddmrp-inventory-positioning.md). Selles näites valisite dekodeerimispunktid, mis vähendasid täitmisaega 21 päevalt viiele päevale, nagu näha järgmises illustratsioonis.

![Dekodeeritud täitmisaja näide.](media/ddmrp-bom-decoupled-lead-time-example.png "Dekodeeritud täitmisaja näide")

Näiteks oletame, et ADU on arvutatud 23 ühikuna, ja nagu eelmises illustratsioonis näidatud, on dekodeeritud täitmisaeg viis päeva. Nende väärtuste abil saate arvutada kollase tsooni, kasutades järgmist võrrandit:

- **Kollase tsooni** = *ADU* × dekodeeritud *täitmisaeg* = 115

![Kollase tsooni arvutamise näide.](media/ddmrp-example-calc-yellow.png "Kollase tsooni arvutamise näide")

Punase tsooni kalkulatsioon sarnaneb kollase tsooni arvutusega, kuid see on täidis hälbe ja täitmisaja jaoks. Oletame näiteks, et olete jälginud keskmist täitmisaega (tegur = 0,50) ja kõrget nõudluse hälbet (tegur = 0,8). Neid väärtusi kasutades koos kollase tsooni võrrandi komponentidega saate arvutada punase tsooni, kasutades järgmisi võrrandeid:

- **Punane alus-ADU** = *·* × dekodeeritud *täitmisaeg* × *=* 57,5
- **Punane ohutus** = *punane ×* hälbetegur *·* = 46
- **Punane tsoon** = *Punane alus* + *Punane ohutus* = 103,5

Süsteem ümardab punase tsooni 104 tükini (ea), kuna tükki loendatakse täisarvudena.

![Punase tsooni arvutamise näide.](media/ddmrp-example-calc-red.png "Punase tsooni arvutamise näide")

Roheline tsooni arvutus sisaldab ka kollase tsooni võrrandi komponente, kuid see võimaldab tellimuse minimaalset suurust, tellimistsüklit ja täitmisaja tegurit. Näiteks oletame, et ei ole tellimistsüklit (seega puuduvad teil ajapiirangud selle kohta, kui sageli tellite) ja tellimuse miinimumkogus on 10 tk. Roheline tsoon arvutatakse seejärel järgmise kolme võrrandi maksimaalse tulemusena:

- *Minimaalne tellimusekogus* = 10
- *Tellimuse × ADU* *·* = 0
- *ADU* × dekodeeritud *täitmisaeg* × täitmisaja *tegur* = 57,5

Süsteem ümardab rohelise tsooni 58 tükini (ea), kuna tükid loendatakse täisarvudena.

![Punane roheline kalkulatsiooni näide.](media/ddmrp-example-calc-green.png "Roheline tsooni arvutuse näide")

Järgmine näide võtab need tsooni arvutustulemused kokku, kasutades lehtergraafikut, mida kasutatakse sageli DDMRP-s.

![Tsooni arvutustulemuste kokkuvõte.](media/ddmrp-example-calc-summary.png "Tsooni arvutustulemuste kokkuvõte")

## <a name="dynamic-adjustments"></a><a name="dynamic-adjustments"></a> Dünaamilised korrigeerimised

Dünaamilised korrigeerimised lasevad teil rakendada *nõudluse korrigeerimise* tegurit suure või madala nõudluse perioodidel. See tegur korrutab valitud perioodi kõigi arvutuste väärtusega ADU. Puhvertsoone muudetakse seejärel omakorda. Tavaliselt rakendate seda tegurit pärast esmaste puhverväärtuste genereerimist, nii et saate neid aja jooksul ja reageerides tingimuste muutmisele trahvida. See ülesanne on DDMRP kolmas etapp.

Näiteks võib klientide puhkusel olemise tõttu olla nõudlust taamaale lisatud toote järele. Seetõttu on müügi eeldatavalt kõrgem. Sel juhul saate muuta nõudluse korrigeerimisteguri **toote** väärtust *1,5-ks* kõigi nädalate puhul augustil.

Sel viisil saate aja jooksul arvutada puhverväärtusi ja seejärel korrigeerida neid rohkem kui ainult süsteemi teabe põhjal. Täielikus DDMRP rakendamises arvutate pakett-töö kaudu iga päev uued puhverväärtused ja aktsepteerite väärtused automaatselt. Seejärel käivitate planeerimise pakett-tööna ja vaatate plaanitud tellimused iga päev uuesti puhvrite täitmise üle.

## <a name="implement-buffers-in-supply-chain-management"></a>Puhvrite juurutamine tarneahela halduses

See jaotis kirjeldab, kuidas rakendada Microsofti puhvertsooni strateegiat Dynamics 365 Supply Chain Management. See eeldab, et olete juba teinud analüüse ja arvutusi, mis on toodud selle artikli esimeses pooles.

### <a name="set-up-buffers-for-a-decoupling-point-item"></a><a name="set-up-buffers"></a> Saate häälestada dekodeerimispunkti kauba puhvereid.

Järgige neid samme, et seadistada dekodeerimispunkti puhverväärtused.

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Valige vabastatud kaup, mis on seadistatud dekodeerimispunktina. (Lisateavet vt teemast [Lao paigutamine](ddmrp-inventory-positioning.md).)
1. Valige tegevuspaani vahekaardil **Plaan kauba laovarud** **.**
1. Kauba laovarude **lehel** valige kauba laovarude kirje, mis loob dekodeerimispunkti. (Kirje näitab nende laovarude grupi nime, mis on seadistatud looma dekodeerimispunkte.)
1. Valige vahekaart **Üldine**.
1. Kui soovite, et süsteem arvutaks puhverväärtused iga päev või iga nädal ümber, võttes aluseks teie müügiajaloo, eelarved ja laovarude grupi sätted, järgige neid samme.

    1. Seadke **puhvriväärtused aja jooksul** valikule *Jah*.
    1. Teateväli teavitab teid, et jätkamisel lähtestatakse käsitsi puhvrisätted (**Miinimum**, **·** **Lisatellimuse** punkt ja Maksimum). Valige **Jah,** et säilitada uus säte.

    Kui eelistate puhversätteid arvutada või sisestada vaid ühe korra, järgige neid samme.

    1. Seadke **puhvriväärtused aja jooksul** valikule *Ei*.
    1. Seadistage **minimaalne**, **lisatellimuse punkt** **ja** maksimaalne väljad puhverväärtustele, mille olete kauba jaoks arvutanud, nagu on kirjeldatud selles artiklis.

1. Seadistage järgmised väljad, et lõpetada kauba DDMRP-arvutuste seadistamine:

    - **Tellimuse** tsükkel – määrake päevade arv, mis peab kauba ostutellimuste vahel mööduma. Kui tellimusepiiranguid pole *, seadistage väärtuseks 0* (null). See väli mõjutab maksimaalse koguse puhvrit, nagu selles artiklis varem nimetatud.
    - **Keskmine igapäevane** kasutus – võite valikuliselt sisestada kauba hinnangulise ADU. Sellel väljal on ainult informatiivne eesmärk. Tavaliselt arvutatakse väärtus automaatselt puhverarvutuste osana.
    - **Tellimuse tellimise** lävi – määrake kauba päevase müügi miinimumarv, mis kvalifitseerub müügikaupa (olulige nõudlus). Süsteem kasutab seda välja, et suurendada plaanitud tellimuste ümberjärjestuskogust suure nõudluse perioodidel. Lisateabe saamiseks vt nõudlusele [suunatud planeerimist](ddmrp-planning.md).

### <a name="calculate-or-enter-decoupled-lead-times"></a><a name="calc-lead-time"></a> Saate arvutada või sisestada dekodeeritud täitmisajad.

Kaupade puhul, kus soovite lubada [süsteemil](#set-up-buffers) automaatselt puhvertsoone arvutada, järgige neid samme dekodeerimispunkti kauba dekodeeritud täitmisaegade arvutamiseks või sisestamiseks.

1. Avage oma dekodeerimispunkti **kauba** laovarude leht. (Lisateavet vt teemast [Saate häälestada dekodeerimispunkti kauba puhvereid](#set-up-buffers).)
1. Valige kauba laovarude kirje, mis loob dekodeerimispunkti.
1. Valige vahekaart **Puhverväärtused**.
1. Kui ruudustikus ei kuvata ühtegi ajaperioodi, valige **tegevuspaani vahekaardil Puhverväärtused** suvand Lisa **ajaperioodid**. Süsteem täidab ruudustiku ridadega iga igapäevase või nädalase ajaperioodi kohta, sõltuvalt sellest, kas laovarude grupi minimaalse, **·**[maksimaalse ja uuesti tellimise punkti perioodi väli on](ddmrp-inventory-positioning.md) seadistatud *väärtusele Igapäevane* või *Iga nädal.* Süsteem lisab piisavalt ridu, et saavutada kaubale määratud laovarude grupile määratud ajapiir.
1. Valige ajaperiood, mille kohta soovite dekodeeritud täitmisaja arvutada. (Tavaliselt on see ajaperiood periood, mis sisaldab tänast kuupäeva.)
1. Tegevuspaani vahekaardil Puhverväärtused **valige suvand** Arvuta dekodeeritud **täitmisaeg**.
1. Dialoogiboksis Dekodeeritud **täitmisaja** arvutamine seadke järgmised väljad:

    - **Kooslus** – valige kooslus, mille põhjal soovite kalkulatsiooni käivitada.
    - **Kuupäev** : valige kuupäev, millal soovite kalkulatsiooni käivitada. Vabade koosluste kogum filtreeritakse nii, et kuvataks ainult valitud kuupäevaks aktiivsed kooslusi.
    - **Kogus** : sisestage kogus, mille jaoks soovite kalkulatsiooni käivitada. Vabade koosluste kogum filtreeritakse nii, et kuvataks ainult määratud kogusele rakenduvad kooslusi.

1. Valige **OK** arvutuse käivitamiseks ja dekodeeritud **täitmisaja arvutamise dialoogiboksi** sulgemiseks. Valitud **ajaperioodi dekodeeritud** täitmisaja veerus kuvatakse nüüd arvutatud väärtus.

### <a name="calculate-or-enter-average-daily-usage"></a><a name="calc-adu"></a> Keskmise päevase kasutuse arvutamine või sisestamiseks

Kaupade puhul, kus soovite lubada [süsteemil](#set-up-buffers) automaatselt puhvertsoone arvutada, järgige neid samme dekodeerimispunkti kauba adu arvutamiseks või sisestamiseks.

1. Avage oma dekodeerimispunkti **kauba** laovarude leht. (Lisateavet vt teemast [Saate häälestada dekodeerimispunkti kauba puhvereid](#set-up-buffers).)
1. Valige kauba laovarude kirje, mis loob dekodeerimispunkti.
1. Valige vahekaart **Puhverväärtused**.
1. Kui ruudustikus ei kuvata ühtegi ajaperioodi, valige **tegevuspaani vahekaardil Puhverväärtused** suvand Lisa **ajaperioodid**. Süsteem täidab ruudustiku ridadega iga igapäevase või nädalase ajaperioodi kohta, sõltuvalt sellest, kas laovarude grupi minimaalse, **·**[maksimaalse ja uuesti tellimise punkti perioodi väli on](ddmrp-inventory-positioning.md) seadistatud *väärtusele Igapäevane* või *Iga nädal.* Lisaks võetakse täitmisaja teguri **vaikeväärtused ja** hälbeteguri **väljad** laovarude grupist. Neid väärtusi saate vajadusel iga rea puhul redigeerida.
1. Valige periood, millal soovite arvutada ADU.
1. Tegevuspaani vahekaardil Puhverväärtused **valige** suvand Arvuta keskmine **igapäevane kasutus**. Süsteem püüab koguda laovarude grupi määratletud ADU arvutamiseks vajalikke [andmeid](ddmrp-inventory-positioning.md).
1. Järgige üht neist sammudest.

    - Kui nõutud andmed on saadaval, lisatakse arvutustulemused veergu Keskmine **igapäevane** kasutus. Sellisel juhul pole tegevus vajalik.
    - Kui nõutud andmed pole saadaval, siis väärtusi automaatselt ei lisata. Sellisel juhul sisestage käsitsi iga puhverväärtust arvutama plaanilise rea hinnangulised väärtused.

### <a name="calculate-and-apply-buffer-values"></a>Arvuta ja rakenda puhverväärtused

Nende kaupade puhul, kus soovite lubada süsteemil [automaatselt](#set-up-buffers) puhvertsoone arvutada, saate järgmiste sammude abil käivitada käsitsi puhverväärtuste kalkulatsiooni.

1. Vastava dekodeerimise [punkti](#set-up-buffers) kauba puhul konfigureerige puhvri arvutus, [arvutage või sisestage dekodeeritud täitmisajad](#calc-lead-time)[ja](#calc-adu) arvutage või sisestage kõigi asjakohaste ajaperioodide keskmine igapäevane kasutus, nagu selles artiklis eelnevalt kirjeldatud.
1. Avage oma dekodeerimispunkti **kauba** laovarude leht.
1. Valige puhverväärtuste **vahekaart**, mis peaks juba kuvama ajaperioodide loendit.
1. Saate valida ajavahemiku, kus soovite puhverväärtusi arvutada. (Tavaliselt on selleks perioodiks tänane periood.) Teie valitud real peavad juba olema veergudes Keskmine igapäevane **kasutus** **ja Dekodeeritud täitmisaja nullväärtused.**
1. Redigeerige **vajaduse korral ühe või** mitme rea nõudluse korrigeerimisteguri välja. Süsteem rakendab seda tegurit keskmise päevase kasutuse **väärtusele** kõigis puhvri kalkulatsioonides, kus seda väärtust kasutatakse. See tegur võimaldab teil korrigeerida vastavalt vajaduse kõikumiskuupäevale (nt puhkuste või hooajaliste kaupade puhul).
1. Valige tegevuspaani vahekaardil Puhverväärtused **suvand** Arvuta miinimum **-, maksimum- ja järeltellimuse punktikogused**. Süsteem arvutab ja täidab **kauba** **laovarude** lehe ruudustiku veerud Arvutatud min, **Arvutatud** lisatellimuse punkt ja **Arvutatud maksimum.**
1. Kui olete arvutatud väärtuste ülevaatamise lõpetanud, peate need määrama. Vastasel juhul need ei oma mingit mõju. Kui rakendate kalkulatsiooni ühele või mitmele reale, **kopeeritakse väljade** Arvutatud miinimum **,** **·** **Arvutatud ümberjärjestatud ja Arvutatud maksimum väärtused vastavalt veergudesse Min**, **·** **Lisatellimuse** punkt ja Max. Tegevuspaani vahekaardil Puhverväärtused **grupi** Tegevus **jaoks** valige üks järgmistest nuppudest:

    - **Aktsepteeri kõik kalkulatsioonid** – rakendage ruudustikus kõik arvutatud väärtused.
    - **Aktsepteeri valitud ridade kalkulatsioonid** – rakendage ainult valitud ridade arvutatud väärtused.
    - **Hüljake kõik** kalkulatsioonid – tühistage kõik arvutatud väärtused miinimumkoguste, maksimumkoguste ja kordustellimuse punktide puhul ruudustikus.
    - **Tühista valitud ridade kalkulatsioonid** – tühistage valitud ridade kõik arvutatud väärtused miinimumkoguste, maksimumkoguste ja ümberjärjesarvutuste punktide puhul.

### <a name="schedule-automatic-buffer-value-calculations"></a>Automaatsete puhverväärtuse arvutuste plaanimine

Kui olete DDMRP sätted täielikult seadistanud ja kinnitanud, et need töötavad õigesti, soovite tõenäoliselt seadistada pakett-töö, et ADU ja seotud puhverväärtused vastavalt vajadusele ümber arvutada, võttes aluseks tegelikud tarbimisandmed ja/või uuendatud eelarved. See protseduur kehtib ainult nende kaupade puhul, mille puhul soovite lubada süsteemil puhvertsoone [automaatselt arvutada](#set-up-buffers).

Automaatsete puhvriväärtuse arvutuste plaanimiseks järgige neid samme.

1. Minge koondplaneerimise **koondplaneerimise \>\> DDMRP arvutama puhverväärtused \>**.
1. Seadke dialoogiboksis **Puhverväärtuste** arvutamine järgmised väljad:

    - **Arvutage keskmine igapäevane** kasutus: *seadke* see valik valikule Jah, et arvutada uuesti dekodeerimise punktis kaupade adu iga kord, kui töö käitatakse. Kui soovite arvutuse vahele jätta *,* määrake selle välja väärtuseks Ei. Tavaliselt tuleks selle suvandi väärtuseks seada *Jah*.
    - **Arvuta dekodeeritud täitmisaeg** – *tehke* see valik valikule Jah, et arvutada dekodeeritud täitmisajad uuesti iga kord, kui töö käitatakse. Kui soovite arvutuse vahele jätta *,* määrake selle välja väärtuseks Ei. Tavaliselt tuleks selle suvandi väärtuseks seada *Jah*.
    - **Arvuta puhverväärtused** : seadke see valik valikule *Jah*, et arvutada puhverväärtused uuesti iga kord, kui tööd käitatakse. Kui soovite arvutuse vahele jätta *,* määrake selle välja väärtuseks Ei. Tavaliselt tuleks selle suvandi väärtuseks seada *Jah*.
    - **Aktsepteeri miinimum-, maksimum**- ja järeltellimusepunkti arvutamine: *seadke* see valik väärtusele Jah, et automaatselt kinnitada ja rakendada ümberarvutatud puhverväärtused iga kord, kui tööd käitatakse. Ümberarvutatud *väärtuste* mitteliitmiseks määrake selle väärtuseks Ei. Sel juhul ei jõustuvad ümberarvutatud väärtused, välja arvatud juhul, kui käsitsi käsitsi neid igale toote laovarude lehele ei **rakendu**. Tavaliselt tuleks selle suvandi väärtuseks seada *Jah*.
    - **Koondplaan** – valige koondplaan, mis sisaldab kaupu, mida kalkulatsioon mõjutab. Arvutus rakendub kõigile plaani filtris olevatele üksustele, mida täiendavad valikud **Filtri** sätted selles dialoogiboksis piiravad.

1. Kirjekogumi piiramiseks, kus seda pakett-tööd peaks käitama, **valige** kiirkaardi Kaasamiseks kirjetes suvand Filter **,** et avada dialoogiboks **Päring**. See dialoogiboks töötab samuti nagu tarneahela halduses teist [tüüpi](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) taustatööde puhul.
1. Määrake kiirkaardil **Käivita taustas**, kuidas, millal ja kui sageli tuleb valitud kaupade jaoks valitud kalkulatsioone teha. Väljad töötavad samamoodi nagu muud tüüpi [taustatööl](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) Supply Chain Management puhul.
1. Valige **OK**, et lisada uus töö pakktöötluse järjekorda käivitamiseks.

### <a name="review-and-recalculate-decoupled-lead-times-for-all-items"></a>Kõigi kaupade dekodeeritud täitmisaegade ülevaatamine ja ümberarvutamine

Järgige neid samme, et üle vaadata ja ümber arvutada kõik dekodeeritud täitmisajad, mis on saadaval teie juriidilises isikus (ettevõttes).

1. Minge koondplaneerimise **koondplaneerimise \>\> DDMRP dekodeeritud \> täitmisajale**.
1. Sirvige **ja filtreerige dekodeeritud** täitmisaja lehel loend nii, nagu vaja, et leida otsitav teave. Kauba veelgi lisateabe vaatamiseks valige selle link veerus **Kaubakood**.
1. Kui soovite dekodeeritud täitmisaja ümber arvutada mis tahes kauba puhul, **valige kaup ja seejärel valige toimingupaanil arvutatud dekodeeritud** täitmisaeg. Ilmub **dialoogiboks Dekodeeritud täitmisaja** arvutamine. See dialoogiboks töötab samuti nagu siis, kui [arvutate dekodeeritud täitmisajad](#calc-lead-time) sama kauba kohta kauba **laovarude** lehel.
