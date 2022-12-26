---
title: Aastalõpu tegevuste KKK
description: Selles artiklis käsitletakse küsimusi, mis võivad tekkida rahandusaasta sulgemisel, ja vastuseid, mis võivad aidata rahandusaasta sulgemise tegevuste korral.
author: moaamer
ms.date: 12/01/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2e33c1dcbfa4da74f2e8acc6e29f04fda3abd185
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853036"
---
# <a name="year-end-activities-faq"></a>Aastalõpu tegevuste KKK 

[!include [banner](../includes/banner.md)]

Selles artiklis käsitletakse küsimusi, mis võivad tekkida rahandusaasta sulgemisel, ja vastuseid, mis võivad aidata rahandusaasta sulgemise tegevuste puhul. Selle artikli teave keskendub põhiliselt pearaamatu ja ostureskontro rahandusaasta sulgemise tegevustele.

## <a name="general-ledger-year-end-enhancements"></a>Pearaamatu aastalõpu täiustused

Microsoft Dynamics 365 Finance’i versioonis 10.0.20 võeti kasutusele aastalõpu sulgemise täiustus. See täiustus on vaikimisi lubatud alates versioonist 10.0.25 ja kohustuslik alates versioonist 10.0.29. Kui teie organisatsioon kasutab varasemat versiooni kui 10.0.25, soovitame lubada selle funktsiooni enne aastalõpu sulgemistoimingute alustamist. Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada **funktsioonihalduse** tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Seega on funktsioon loetletud järgmisel viisil.

- **Moodul:** Pearaamat
- **Funktsiooni nimi:** Pearaamatu aastalõpu täiustused

Rahandusaasta sulgemise mallide häälestamine on viidud uuele häälestuslehele **Aastalõpu sulgemise malli häälestus**. Olemasolev aastalõpu sulgemise leht muutub sarnaseks **pearaamatu välisvaluuta ümberarvutamise** lehega, kus kuvatakse loend iga kord, kui aastalõpu sulgemine käivitatakse või tühistatakse. Lehel ei kuvata ajaloolist teavet aastalõpu sulgemiste kohta, mis tehti enne funktsiooni lubamist. Raamatupidaja saab käivitada aastalõpu sulgemise uuelt lehelt.

Aastalõpu sulgemise tagasivõtmiseks valige vastava juriidilise isiku kõige hiljutisem finantsaasta ja seejärel valige **Aastalõpu sulgemise tühistamine**. Tagasivõtmine kustutab eelmise aastalõpu sulgemise raamatupidamiskirjed ega käivita aastalõpu sulgemist automaatselt uuesti. Kui lubate funktsiooni **Pearaamatu aastalõpu täiustused** pärast aastalõpu sulgemist ja soovite ajaloolised aastalõpu tulemused tühistada, käivitage ajalooline aastalõpu sulgemine uuesti pärast seda, kui olete lubanud pearaamatu parameetri **Olemasolevate aastalõpu kirjete kustutamine aasta uuesti sulgemisel**.

Aastalõpu sulgemise uuesti käivitamiseks taaskäivitage see protsess finantsaasta ja juriidilise isiku jaoks. Protsess jätkab pearaamatu parameetri sätte kasutamist määramaks, kas aastalõpu sulgemise uuesti käivitamine võtab arvesse ainult uusi või muudetud kandeid või kas see protsess käivitatakse uuesti kõigi kannete jaoks ja võtab seega eelmise sulgemise täielikult tagasi.

## <a name="general-ledger-the-general-ledger-year-end-enhancements-feature-is-enabled-why-cant-i-view-my-previous-year-closings-in-the-history-section-of-the-year-end-close-page"></a>Pearaamat: pearaamatu aastalõpu täiustuste funktsioon on lubatud. Miks ei saa ma vaadata oma eelmise aasta sulgemisi aastalõpu sulgemise lehe jaotises Ajalugu?

Enne funktsiooni **Pearaamatu aastalõpu täiustused** lubamist jälgitakse viimase aastalõpu sulgemisprotsessi käituse kuupäeva ja kellaaega. See funktsioon ei jälginud iga aastalõpu sulgemise käitamise ajalugu. Seetõttu pole iga aastalõpu sulgemise käituse üksikasjad kuvamiseks saadaval. Pärast funktsiooni lubamist säilitatakse järgneva aastalõpu sulgemise protsessi teave. Kõigi aastalõpu sulgemisprotsesside kandeid, isegi neid, mis käitati enne funktsiooni lubamist, saab vaadata lehel **Pearaamatu kanded**. 

## <a name="general-ledger-the-year-end-close-process-is-failing-because-of-the-following-error-the-year-end-close-cant-be-run-because-one-or-more-ledger-transactions-posted-into-the-fiscal-year-that-you-are-closing-were-settled-to-a-ledger-transaction-in-a-different-fiscal-year-what-does-this-error-mean"></a>Pearaamat: aastalõpu sulgemisprotsess nurjub järgmise tõrke tõttu: „Aastalõpu sulgemist ei saa käivitada, kuna üks või mitu pearaamatu tehingut, mis on sisestatud teie suletavasse finantsaastasse, arveldati pearaamatu tehinguga erineval finantsaastal.“ Mida see tõrge tähendab?

Kuna funktsioon **Teadlikkus pearaamatu tasakaalustamise ja aastalõpu sulgemise vahel** on lubatud, jäetakse algsaldost välja ainult suletava finantsaasta tasakaalustatud pearaamatukanne. Sellise käitumise tõttu on deebet ja kreedit tasakaalust väljas. Lisateavet leiate artiklist [Teadlikkus pearaamatu tasakaalustamise ja aastalõpu sulgemise vahel](awareness-between-ledger-settlement-year-end-close.md).

## <a name="general-ledger-reversal-of-the-year-end-close-process-is-failing-because-of-the-following-error-the-year-end-close-for-112022-cant-be-reversed-because-beginning-balance-transaction-have-been-ledger-settled-in-fiscal-year-112023-what-does-this-error-mean"></a>Pearaamat: aastalõpu sulgemisprotsessi tühistamine nurjub järgmise tõrke tõttu: „Aastalõpu sulgemist ei saa 1/1/2022 puhul tühistada, kuna algsaldo kanded on finantsaastal 1/1/2023 pearaamatus tasakaalustatud.“ Mida see tõrge tähendab?

Kuna funktsioon **Teadlikkus pearaamatu tasakaalustamise ja aastalõpu sulgemise vahel** on lubatud, pole aastalõpu töötlemise tühistamine lubatud juhul, kui avamiskanded on tasakaalustatud uuel finantsaastal. Enne 1. jaanuari 2022 aastalõpu sulgemist tühistage pearaamatu tasakaalustus uuel finantsaastal 2023. Teise võimalusena sulgege aasta 1. jaanuari 2022 seisuga uuesti, kuid ainult uute korrigeerimiskirjete jaoks. Aasta uuesti sulgemiseks ainult korrigeerimiste jaoks keelake pearaamat parameeter **Olemasolevate aastalõpu kirjete kustutamine aasta uuesti sulgemisel**.

## <a name="general-ledger-why-isnt-the-ledger-settlement-automation-processing-decembers-ledger-settlement-transactions"></a>Pearaamat: miks ei töötle pearaamatu tasakaalustamise automaatika detsembri pearaamatu tasakaalustuskandeid?

Funktsioon **Pearaamatu tasakaalustuste automatiseerimine** käivitab automatiseerimise selliste kannete jaoks, mille kuupäev on vahemikus finantsaasta esimesest päevast kuni selle toimingu tegemise päevani. 31. detsembril lõppeva finantsaasta korral on võimalik, et peate toimingu teostamise kuupäeva ise korrigeerima, tagamaks, et see käivitatakse detsembris. Automatiseerimine on häälestatud käivituma näiteks iga kuu esimesel päeval. Sel juhul käivitatakse automaatika 1. detsembril 2022 ja on seejärel ajastatud käivituma 1. jaanuaril 2023. Soovitame 1. jaanuari 2023 käivituskorra ära vahetada nii, et automaatika käivitatakse hoopis 31. detsembril 2022. See muudatus tagab, et 2. detsembrist kuni 31. detsembrini tehtud kanded võetakse automaatseks tasakaalustamiseks arvesse.

## <a name="general-ledger-whats-the-difference-between-the-reverse-year-end-close-action-and-the-delete-existing-year-end-entries-when-reclosing-parameter-for-year-end-close"></a>Pearaamat: mis vahe on aastalõpu tühistamise toimingul ja olemasolevate aastalõpu kirjete uuesti sulgemise parameetril aastalõpu sulgemise jaoks?

Kasutajates võib tekitada segadust ja küsimusi see, mille poolest erinevad omavahel toiming **Aastalõpu sulgemise tühistamine** ja pearaamatu parameeter **Olemasolevate aastalõpu kirjete kustutamine aasta uuesti sulgemisel** (**Pearaamat \> Pearaamatu seadistamine \> Üldised pearaamatu parameetrid**).

Aastalõpu sulgemise protsessi käivitamisel valige toiming **Aastalõpu sulgemise tühistamine**, kui soovite kustutada kõik sulgemissaldo ja algsaldo kirjed nii, nagu poleks aastalõpu sulgemist üldse käivitatud. Sel juhul kanded kustutatakse. Aastalõpu sulgemist ei käivitata automaatselt uuesti. Aastalõpu sulgemise käivitamiseks valige toiming **Aastalõpu sulgemise käivitamine**.

Pearaamatu parameetrit **Olemasolevate aastalõpu kirjete kustutamine aasta uuesti sulgemisel** kasutatakse üksnes juhul, kui käivitate (mitte ei tühista) aastalõpu sulgemise. Kui parameetri olekuks on määratud **Jah**, kustutatakse kõik sulgemissaldo ja algsaldo kirjed ning aastalõpu sulgemine käivitatakse uuesti. Seda varianti kasutatakse siis, kui organisatsioon soovib sisestada kõik kanded (sh pärast eelmist aastalõpu sulgemist tehtud korrigeerimised) sulgemissaldo ja algsaldo kirjete ühte raamatupidamise kirjesse. Kui parameetri olekuks on määratud **Ei**, jäävad kõik sulgemissaldo ja algsaldo kirjed alles. Neid ei kustutata. Selle asemel luuakse uus sulgemissaldo ja algsaldo kirje ainult delta- või uute kannete jaoks, mis on sisestatud pärast selle finantsaasta viimast aastalõpu sulgemist.

> [!NOTE]
> Sulgemissaldo kirje luuakse suletavas aastas. See juhtub ainult siis, kui pearaamatu parameeter **Sulgemiskannete loomine ülekande ajal** on määratud olekusse **Jah**. Algsaldo kirje luuakse alati, kuna see on järgmise aasta algne saldo.

## <a name="general-ledger-what-is-the-difference-between-close-all-and-close-single-options-on-the-transfer-profit-and-loss-dimension-section-of-the-year-end-close-process"></a>Pearaamat: mis vahe on aastalõpu sulgemisprotsessi jaotises „Kasumi ja kahjumi dimensioonide ülekandmine“ käskudel „Sule kõik“ ja „Sule üksik“?

Käsk **Sule kõik** säilitab algsed finantsdimensiooni väärtused sisestatud kannetest ja kasutab neid jaotamata kasumi konto jaoks algsaldode loomiseks. Iga unikaalse finantsdimensiooni väärtuste unikaalse kombinatsiooni jaoks luuakse eraldi jaotamata kasumi algsaldod. Valiku **Sule üksik** tegemisel võetakse kõik selle finantsdimensiooniga sisestatud kanded kokku jaotamata kasumi algsaldosse valiku **Sule üksik** tegemise järel kuvatavale väljale sisestatud dimensiooniväärtuse jaoks. 

Oletagem näiteks, et kõik finantsaasta kanded sisestati kontostruktuuriga Põhikonto – osakond. Malli finantsdimensioonis Osakond valitakse variant **Sule üksik** ja dimensiooniväärtusena sisestatakse 100. Kui kõigi osakondadesse 200, 300 ja 400 sisestatud kannete kogutulu on 100 000 dollarit, luuakse jaotamata kasumi jaoks üks algsaldo – 100. Kui teete valiku **Sule üksik** ja jätate finantsdimensiooni väärtuse tühjaks, sisestatakse kõik kanded jaotamata kasumisse nii, et dimensiooni väärtus jääb tühjaks.

## <a name="general-ledger-when-i-select-close-single-option-on-the-transfer-profit-and-loss-dimension-section-of-the-year-end-close-process-will-my-detailed-transactional-information-be-lost"></a>Pearaamat: kui valida aastalõpu sulgemisprotsessi akna jaotises „Kasumi ja kahjumi dimensioonide ülekandmine“ variant „Sule üksik“, kas minu üksikasjalik kandeteave läheb kaotsi?

Käskudega **Sule kõik** ja **Sule üksik** saab määrata, millised kasumi- ja kahjumikontodele sisestatud kannete finantsdimensioonid kantakse üle jaotamata kasumi põhikontole. Ajaloolisi üksikasjalike sisestusi kasumi- ja kahjumikontodele see ei mõjuta ning need jäävad üksikasjalikuks. Valik mõjutab üksikasjataset, mis kantakse üle jaotamata kasumi kontodele uue aasta algsaldona. 

## <a name="general-ledger-the-year-end-close-process-is-failing-because-the-reporting-currency-for-the-year-does-not-balance-what-does-this-mean"></a>Pearaamat: aastalõpu sulgemisprotsess nurjub, kuna aasta aruandlusvaluutat ei saa tasakaalustada. Mida see tähendab?

See tõrge võib ilmneda pärast funktsiooni **Teadlikkus pearaamatu tasakaalustamise ja aastalõpu sulgemise vahel** (nn teadlikkusfunktsiooni) lubamist. Kui see funktsioon on lubatud, ei kaasata tasakaalustatud pearaamatukandeid enam pearaamatu aastalõpu sulgemise käitamisel järgmise finantsaasta algsaldosse. Kui pearaamatu jaoks on määratletud aruandlusvaluuta, võib tasakaalustatud pearaamatukannete välistamine tekitada klientidele aastalõpu sulgemisel probleeme.   
Pearaamatu tasakaalustamine tehakse ainult arvestusvaluutas.  Kui pearaamatukanded on tasakaalustatud, tagab kinnitamine ainult selle, et arvestusvaluuta deebetid on arvestusvaluuta kreedititega võrdsed. Nende pearaamatukannete aruandlusvaluuta summasid ei kinnitata ja on võimalik, et nende korral deebet = kreedit ei kehti.  Lisaks ei arvuta ega sisesta pearaamatu tasakaalustamine kasumit/kahjumit automaatselt aruandlusvaluutas.  Nende piirangute tõttu peab kasumi-/kahjumikanne pearaamatu tasakaalustamisel olema aruandlusvaluutas.  Kui pearaamatu tasakaalustamisse ei kaasata kasumit/kahjumit, põhjustab aastalõpu sulgemine teate tasakaalu puudumise kohta.  Lisateavet leiate artiklist [Teadlikkus pearaamatu tasakaalustusfunktsiooni ja aruandlusvaluuta vahel on tasakaalust väljas](reporting-currency-yec.md).

## <a name="general-ledger-what-can-be-changed-to-help-enhance-the-performance-of-year-end-processing"></a>Pearaamat: mida saab muuta, et aastalõpu töötlemise jõudlus oleks tõhusam?

Aastalõpu sulgemise jõudluse parendamiseks saate teha mitu muudatust. Soovitame teil neid ettepandud muudatusi hinnata ning otsustada, kas need on teie organisatsiooni jaoks sobivad.

### <a name="optimize-year-end-close-service"></a>Aastalõpu sulgemise optimeerimise teenus

Teenus **Aastalõpu sulgemise optimeerimine** annab Microsoft Dynamics 365 Finance’i klientidele võimaluse aastalõpu sulgemist kiirendada, kolides aeganõudva aastalõpu töötlemise üle mikroteenusesse. Tõhusa aastalõpu sulgemise kaudu säästetud aeg aitab igal Finance’i meeskonnal nõutavatele korrigeerimistele õigeaegselt reageerida ja finantsaruanded genereerida. Aastalõpu sulgemise töötlemine mikroteenuses vabastab väärtuslikke ressursse muudeks tegevusteks. Töötlemise ülendamine minimeerib SQL Serveri koormust ja annab klientide võimaluse aastalõpu sulgemise töötlemist kiirendada.

Teenus **Aastalõpu sulgemise optimeerimine** on saadaval versioonis 10.0.31, et rohkem kliente saaksid uut teenust kasutada juba 2022. aasta lõpu jaoks. Lisaks on teenus tagasiulatuvalt kasutusele võetud ka versioonides 10.0.30 ja 10.0.29. Lisateavet leiate artiklist [Aastalõpu sulgemise optimeerimine](optimize-year-end-close.md).

### <a name="dimension-sets"></a>Dimensioonikogumid

Aastalõpu sulgemise käivitamisel luuakse iga dimensioonikogumi saldo uuesti. Selline käitumine mõjutab otseselt jõudlust. Mõned organisatsioonid loovad dimensioonikogumeid tarbetult, kuna neid on ühel hetkel kasutatud või võidakse ühel hetkel kasutada. Kuna need tarbetud dimensioonikogumid luuakse aastalõpu sulgemise käigus uuesti, aeglustab see protsessi. Võtke aega, et oma dimensioonikogumid üle vaadata, ja kustutage kõik, mida pole vaja.

Mittevajalikud dimensioonikogumid mõjutavad ka pakett-tööd **BudgetDimensionFocusInitializeBalance** (**Pearaamat \> Kontoplaan \> Dimensioonid \> Finantsdimensioonikogumid**).

[![Finantsdimensioonikogumid.](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Aastalõpu sulgemise malli konfigureerimine

Aastalõpu sulgemise mall võimaldab organisatsioonil valida finantsdimensiooni taseme, mida hoitakse kasumi- ja kahjumisaldode ülekandmisel jaotamata kasumisse. Sätted võimaldavad organisatsioonil saldode jaotamata kasumisse teisaldamisel hoida alles üksikasjalikke finantsdimensioone (**Sule kõik**) või summeerida summad ühele dimensiooniväärtusele (**Sule üks**). Selle saab määratleda iga finantsdimensiooni jaoks. Lisateavet nende sätete kohta vt artiklist [Aastalõpu sulgemine](year-end-close.md).

Soovitame teil hinnata oma organisatsiooni vajadusi ja jõudluse täiustamiseks sulgeda võimaluse korral nii palju dimensioone kui võimalik, kasutades aastalõpu suvandit **Sule üks**. Sulgedes ühele dimensiooniväärtusele (mis võib olla ka tühi väärtus), arvutab süsteem jaotamata kasumi konto kirjete saldode määratlemisel vähem üksikasju.

### <a name="degenerate-dimensions"></a>Dimensioonide degenereerimine

Dimensiooni degenereerimisega on eraldiseisev või teiste dimensioonidega koos taaskasutamine peaaegu olematu. Dimensioonide degenereerimist on kahte tüüpi. Esimene tüüp on eraldiseisvalt degenereeriv dimensioon. Tavaliselt kuvatakse seda tüüpi degenereerivat dimensiooni ainult ühel kandel või väikesel hulgal kannetel. Teine tüüp on dimensioon, mis degenereerib vähemalt ühe lisadimensiooniga, millel on sama potentsiaal võimalike genereeritavate permutatsioonide põhjal. Degenereeriv dimensioon võib märkimisväärselt mõjutada aastalõpu sulgemise protsessi jõudlust. Jõudlusprobleemide vähendamiseks määratlege kõik degenereerivad dimensioonid aastalõpu sulgemise häälestuses eelmises jaotises kirjeldatud viisil olekus **Sule üks**.

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2022"></a>Ostureskontro: millised muudatused on tehtud 1099 aastalõpu aruandluse toetamiseks 2022. aastal?

#### <a name="update-to-all-1099-forms"></a>Kõigi 1099-vormide värskendus

2022. maksuaasta jaoks on kõigisse 1099-vormidesse tehtud järgmised muudatused.

- 2021. aastal oli 1099-vormides aasta fikseeritud. Alates 2022. aastast lisab aasta aruanne.

#### <a name="1099-misc"></a>1099-LISA

2022. maksuaasta jaoks on vormis 1099-LISA tehtud järgmised värskendused.

- Väli 13: näitab nüüd välismaiste kontode maksukuulekuse seaduse (FATCA) esitamisnõuet.
- Väli 14: kasutatakse nüüd liigsete kuldse langevarju maksete aruandluseks.
- Väli 15: kasutatakse nüüd mittekvalifitseeruvate edasilükatud hüvitise (NQDC) plaanide alusel tehtud makse aruandluseks.
- Väli 16: kasutatakse nüüd riigi kinnipeetavate maksude aruandluseks.
- Väli 17: kasutatakse nüüd maksja riiginumbri aruandluseks.
- Väli 18: kasutatakse nüüd riigitulu aruandluseks.

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Ostureskontro: 1099 – kuidas muuta välja 1099 ja selle väärtusi hankija jaoks, kes ei jälginud aasta vältel 1099 teavet?

Kasutage funktsiooni **Uuenda 1099** varem makstud arvekannete läbivaatamiseks ja määrake 1099 andmed asjakohasel viisil ümber, võttes aluseks lehe **Hankija** vahekaardi **Maks 1099** sätted. Funktsiooni **Uuenda 1099** kasutamiseks minge lehele **Ostureskontro \> Hankijad \> Kõik hankijad**, valige soovitud hankija ja seejärel valige toimingupaani vahekaardil **Hankija** nupp **Uuenda 1099**.

## <a name="can-i-run-the-update-1099-functionality-for-all-my-vendors-at-once"></a>Kas funktsiooni Uuenda 1099 saab käitada kõigi hankijate jaoks korraga?

Lehel **1099 teabe värskendamine mitme hankija jaoks** saate värskendada 1099 välja ühe hankija kirjel. Seejärel saate kanded sellelt 1099 väljalt pärineva teabega värskendada. Lehe avamiseks valige **Ostureskontro \> Perioodiline ülesanne \> Maks 1099**. Lehele juurdepääsuks peab teile olema määratud turbeõigus **Mitme hankija välja 1099 ja kannete värskendamine**.

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-versus-update-all-in-the-update-1099-utility"></a>Ostureskontro: 1099 – „Arvutab üle olemasolevad 1099 summad“ vs. „Uuenda kõik“ utiliidis Uuenda 1099.

Märkeruut **Arvutab üle olemasolevad 1099 summad** lähtestab 1099 summa kokku tasutud väärtustele, kui seda kasutatakse koos märkeruuduga **Uuenda kõik**.

[![Maksu 1099 kanded: enne uuendamisprotseduuri käivitamist.](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Märkeruut **Arvutab üle olemasolevad 1099 summad** tuleb mängu üksnes siis, kui arvel on osalisi 1099 väärtusi või kui arvet on vormil „Maks 1099“ muudetud. Oletagem näiteks, et teil on arve väärtusega 1000.00 $, kuid kasutaja sisestab arvele käsitsi 1099-summa väärtuses 500.00 $.

[![Maksu 1099 kanded: märkeruutude „Uuenda kõik“ ja „Arvutab üle olemasolevad 1099 summad“ korraga märkimine.](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

Selle arve tasumisel on 500.00 $ tasutud 1099-summa. Kui teete ümberarvutamisprotseduuri, muudetakse 1099-summa väärtuseks 1000.00 $, mis on tasutud kogusumma.

[![Maksu 1099 kanded: pärast 1099-protseduuri käivitamist.](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Ostureskontro: 1099 – 1099-kannete käsitsi loomine

Organisatsioonil võib olla vaja luua käsitsi 1099-kandeid, mis pole arvega seostatud. 1099 kannete käsitsi lisamiseks valige **Ostureskontro \> Perioodilised ülesanded \> Maks 1099 \> 1099-te hankija tasakaalustus**. Valige nupp **Manuaalsed 1099 kanded**.

Käsitsi loodud 1099 kandeid ei uuendata utiliidis **Uuenda 1099** protsessiga **Uuenda kõik** ega protsessiga **Arvutab üle olemasolevad 1099 summad**.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Ostureskontro: 1099 – kas Dynamics 365 Finance toetab 1096 vormi?

Dynamics 365 Finance ei prindi 1096 aastakokkuvõtte ja USA teabetagastuste edastamise vormi.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Ostureskontro: 1099 – kas on uusi funktsioone, mis toetavad 1099-aruandlust avalikus sektoris?

Lisatud on uus avaliku sektori funktsioon **1099-teabe uuendamine põhikonto järgi**, mille saate lubada **funktsioonihalduse** tööruumis. See funktsioon võimaldab arvestuse jaotuses seostada hankija 1099-väärtused põhikonto järgi, mitte hankija kirje vaikekonto järgi.

Lisateavet vt teemast [Hankijate häälestamine aruande 1099 jaoks](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
