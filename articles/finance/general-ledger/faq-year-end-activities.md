---
title: Aastalõpu tegevuste KKK
description: Selles artiklis esitletakse küsimusi, mis võivad tekkida rahandusaasta sulgemisel, ja vastuseid, mis võivad aidata aasta lõpu sulgemistegevuste puhul.
author: moaamer
ms.date: 11/08/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2a75d1e3e68837a437b2369ba369b0063e015b12
ms.sourcegitcommit: 78cbb125f20a33df38bda0546203b8f837cbcd93
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/09/2022
ms.locfileid: "9751927"
---
# <a name="year-end-activities-faq"></a>Aastalõpu tegevuste KKK 

[!include [banner](../includes/banner.md)]

Selles artiklis esitletakse küsimusi, mis võivad tekkida rahandusaasta sulgemisel, ja vastuseid, mis võivad aidata aasta lõpu sulgemistegevuste puhul. Selle artikli teave keskendub põhiliselt pearaamatu ja ostureskontro rahandusaasta sulgemistegevustele.

## <a name="general-ledger-year-end-enhancements"></a>Pearaamatu aastalõpu täiustused 
Versioonis 10.0.20 avaldati aastalõpu sulgemise täiustus, mis lubatakse vaikimisi alates versioonist 10.0.25. Kui teie organisatsioon kasutab varasemat versiooni kui 10.0.25, soovitame lubada selle funktsiooni enne aastalõpu sulgemistoimingute alustamist. Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada funktsioonihalduse tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Seega on funktsioon loetletud järgmisel viisil.

 - Moodul: Pearaamat
 - Funktsiooni nimi: Pearaamatu aastalõpu täiustused

Rahandusaasta sulgemise mallide seadistamine on viidud uuele seadistuslehele **Aastalõpu sulgemise malli seadistus**. Olemasolev aastalõpu sulgemise leht muutub sarnaselt pearaamatu välisvaluuta ümberarvutamisega, kus loendit kuvatakse iga kord, kui aastalõpu sulgemist käitatakse või tagasi võetakse. Raamatupidaja saab käivitada aastalõpu sulgemise uuelt lehelt. 

Aastalõpu sulgemise tagasivõtmiseks valige vastava juriidilise isiku kõige hiljutisem rahandusaasta ja valige nupp **Aastalõpu sulgemise tagasivõtmine**. Tagasivõtmine kustutab eelmise aastalõpu sulgemise raamatupidamiskirjed ja ei käivita aastalõpu sulgemist automaatselt uuesti. 

Saate käivitada aastalõpu sulgemise uuesti, taaskäivitades finantsaasta ja juriidilise isiku protsessi. Protsess jätkab pearaamatu parameetri sätte kasutamist määramaks, kas aastalõpu sulgemise uuesti käivitamine arvestab ainult uusi või muudetud kandeid või võtab eelmise sulgemise täielikult tagasi, käivitades protsessi kõigi kannete jaoks uuesti.  

## <a name="general-ledger-how-do-i-know-that-were-running-year-end-close-and-not-undoing-year-end-close"></a>Pearaamat: kuidas ma tean, et me teeme aastalõpu sulgemise käivitamise ja mitte tagasivõtmise?
Olen näinud, kuidas organisatsioon proovib aastalõpu sulgemist käivitada, kuid teeb selle asemel aastalõpu sulgemise tagasivõtmise. Kui aastalõpu sulgemine jõuab liiga kiiresti lõpule või aastalõpu sulgemine ei tekita algsaldosid, kontrollige sätet **Eelmise sulgemise tagasivõtmine** jaotises **Aastalõpu sulgemine** (**Pearaamat > Perioodi sulgemine > Aastalõpu sulgemine > Rahandusaasta sulgemise käivitamine**). 

[![Aastalõpu sulgemise käivitamine vs aastalõpu sulgemise tagasivõtmine.](./media/faq-2020-yr-end-01.png)](./media/faq-2020-yr-end-01.png)

Kui valik **Eelmise sulgemise tagasivõtmine** on määratud olekusse **Jah**, siis eelmine aastalõpu sulgemine tühistatakse. Tagasivõtmise käivitamisel kustutatakse kõik sulgemissaldo ja algsaldo kirjed, justkui aastalõpu sulgemist ei oleks kunagi käivitatud. Kanded kustutatakse. Aastalõpu sulgemist ei käivitata automaatselt uuesti. Peate ise protsessi uuesti käivitama, määrates valiku **Eelmise sulgemise tagasivõtmine** olekuks nüüd **Ei**. 

> [!NOTE]
> Sulgemissaldo kirje luuakse suletavas aastas valikuliselt. See juhtub ainult siis, kui pearaamatu parameeter **Sulgemiskannete loomine ülekande ajal** on määratud olekusse **Jah**. Algsaldo kirje luuakse alati, kuna see on järgmise aasta algne saldo.  
 
## <a name="general-ledger-what-is-the-difference-between-undo-and-delete-gl-parameter-for-year-end-close"></a>Pearaamat: mille poolest erinevad pearaamatu aastalõpu sulgemise parameetrid Tagasivõtmine ja Kustutamine?
Parameetri **Eelmise sulgemise tagasivõtmine**, mis asub dialoogiboksis **Aastalõpu sulgemine**, ja pearaamatus asuva parameetri **Aasta lõpetamise kannete kustutamine ülekandmisel** (**Pearaamat > Perioodi sulgemine > Aastalõpu sulgemine > Rahandusaasta sulgemise käivitamine**) eristamine võib tekitada segadust.  

[![Pearaamatu aastalõpu sulgemise parameetrite Tagasivõtmine ja Kustutamine erinevus.](./media/faq-2020-yr-end-02.png)](./media/faq-2020-yr-end-02.png)

Aastalõpu sulgemise protsessi käivitamisel valige rippdialoogis **Eelmise sulgemise tagasivõtmine**, et kustutada kõik sulgemissaldo ja algsaldo kirjed, justkui aastalõpu sulgemist poleks käivitatud. Kanded kustutatakse. Aastalõpu sulgemist ei käivitata automaatselt uuesti. Aastalõpu sulgemise käivitamiseks peate selle protsessi uuesti algatama, määrates valiku **Eelmise sulgemise tagasivõtmine** olekuks nüüd **Ei** (**Pearaamat > Pearaamatu seadistamine > Pearaamatu parameetrid**). 

[![Pearaamatu parameetri seadistamine.](./media/faq-2020-yr-end-03.png)](./media/faq-2020-yr-end-03.png)

Pearaamatu parameetrit **Aasta lõpetamise kannete kustutamine ülekandmisel** kasutatakse ainult siis, kui käivitatakse (mitte ei võeta tagasi) aastalõpu sulgemine (valiku **Eelmise sulgemise tagasivõtmine** on määratud olekusse **Ei**). Kui selle parameetri olekuks on määratud **Jah**, kustutatakse kõik sulgemissaldo ja algsaldo kirjed ning aastalõpu sulgemine käivitatakse uuesti. Seda protsessi kasutatakse siis, kui organisatsioon soovib sisestada kõik kanded (sh pärast eelmist aastalõpu sulgemist tehtud korrigeerimised) sulgemissaldo ja algsaldo kirjete ühte raamatupidamise kirjesse. 

Kui see valik on määratud olekusse **Ei**, jäävad kõik sulgemissaldo ja algsaldo kirjed alles. Neid ei kustutata. Selle asemel luuakse uus sulgemissaldo ja algsaldo kirje ainult delta või uute kannete jaoks, mis on sisestatud pärast selle rahandusaasta viimast aastalõpu sulgemist.  

> [!NOTE]
> Sulgemissaldo kirje luuakse suletavas aastas. See juhtub ainult siis, kui pearaamatu parameeter **Sulgemiskannete loomine ülekande ajal** on määratud olekusse **Jah**. Algsaldo kirje luuakse alati, kuna see on järgmise aasta algne saldo. 

## <a name="general-ledger-what-can-be-changed-to-enhance-performance-of-year-end-processing"></a>Pearaamat: mida saab muuta, et aastalõpu töötlemise jõudlus oleks tõhusam? 
Aastalõpu sulgemise jõudluse parendamiseks saate teha mitmeid muudatusi. Soovitame teil neid ettepandud muudatusi hinnata ning otsustada, kas iga muudatus on teie organisatsiooni jaoks sobiv.  

### <a name="dimension-sets"></a>Dimensioonikogumid
Aastalõpu sulgemisel käivitamisel luuakse iga dimensioonikogumi saldo uuesti ja see mõjutab otseselt jõudlust. Mõned organisatsioonid loovad dimensioonikogumeid tarbetult, kuna neid on ühel hetkel kasutatud või võidakse ühel hetkel kasutada.  Need tarbetud dimensioonikogumid luuakse aastalõpu sulgemise käigus siiski uuesti ja see aeglustab protsessi. Võtke aega, et oma dimensioonikogumid üle vaadata, ja kustutage kõik tarbetud dimensioonikogumid.

Mittevajalikud dimensioonikogumid mõjutavad ka pakett-tööd **BudgetDimensionFocusInitializeBalance** (**Pearaamat > Kontoplaan > Dimensioonid > Finantsdimensioonikogumid**).

[![Finantsdimensioonikomplektid.](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Aastalõpu sulgemise malli konfigureerimine
Aastalõpu sulgemise mall võimaldab organisatsioonil valida finantsdimensiooni taseme, mida hoitakse kasumi- ja kahjumisaldode ülekandmisel jaotamata kasumisse. Sätted võimaldavad organisatsioonil saldode jaotamata kasumisse teisaldamisel hoida alles üksikasjalikke finantsdimensioone (**Sule kõik**) või summeerida summad ühele dimensiooniväärtusele (**Sule üks**). Selle saab määratleda iga finantsdimensiooni jaoks. Lisateavet nende sätete kohta vt artiklist [Aastalõpu sulgemine](year-end-close.md).

Soovitame teil hinnata oma organisatsiooni vajadusi ja jõudluse täiustamiseks sulgeda võimaluse korral nii palju dimensioone kui võimalik, kasutades aastalõpu suvandit **Sule üks**. Sulgedes ühele dimensiooniväärtusele (mis võib olla ka tühi väärtus), arvutab süsteem jaotamata kasumi konto kirjete saldode määratlemisel vähem üksikasju.

## <a name="degenerate-dimensions"></a>Dimensioonide degenereerimine

Dimensiooni degenereerimisega on eraldiseisev või teiste dimensioonidega koos taaskasutamine peaaegu olematu. Dimensioonide degenereerimist on kahte tüüpi. Esimene tüüp on eraldiseisvalt degenereeriv dimensioon. Tavaliselt kuvatakse seda tüüpi degenereerivat dimensiooni ainult ühel kandel või väikesel hulgal kannetel. Teine tüüp on dimensioon, mis degenereerib vähemalt ühe lisadimensiooniga, millel on sama potentsiaal võimalike genereeritavate permutatsioonide põhjal. Degenereeriv dimensioon võib märkimisväärselt mõjutada aastalõpu sulgemise protsessi jõudlust. Jõudlusprobleemide vähendamiseks määratlege kõik degenereerivad dimensioonid aastalõpu sulgemise seadistuses olekusse **Sule üks** eelmises jaotises kirjeldatud viisil.

## <a name="general-ledger-what-does-the-period-close-year-end-close-do"></a>Pearaamat: mida perioodi sulgemine, aastalõpu sulgemine teeb?
 
[![Perioodi sulgemine, aastalõpu sulgemine.](./media/faq-2020-yr-end-05.png)](./media/faq-2020-yr-end-05.png)

### <a name="performance-improvements-for-rebuilding-financial-dimension-sets"></a>Finantsdimensioonide komplektide uuestiloomise jõudlustäiustused
Versioonile 10.0.16 lisatud uus funktsioon parendab aastalõpu sulgemise ja konsolideerimise protsesside jõudlust. Funktsiooni nimeks on Jõudluse täiustused finantsdimensioonikogumite uuesti loomiseks. See funktsioon muudab dimensioonikogumite uuesti loomise viisi nii, et need luuakse uuesti ainult asjakohase ajavahemiku jaoks. Eelmistes versioonides loodi dimensioonikogumid uuesti kõigi kuupäevade jaoks. Näiteks kui sulgete aasta 2020, loob süsteem uuesti ainult 2020. rahandusaasta kannete saldod. Kui käivitate konsolideerimise kuupäevavahemikule 1. november 2020 kuni 30. november 2020, loob süsteem uuesti saldod ainult selle kuupäevavahemiku jaoks.

Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada funktsioonihalduse tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Seega on funktsioon loetletud järgmisel viisil.
 
- Moodul: Pearaamat
- Funktsiooni nimi: Jõudluse täiustused finantsdimensioonikogumite uuesti loomiseks

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2021"></a>Ostureskontro: millised muudatused on tehtud 1099 aastalõpu aruandluse toetamiseks 2021. aastal?

2021. aastal on vorme DIV, NEC ja MISC pisut muudetud ning lisatud täiendavaid välju.

#### <a name="div-new-box2e-2f"></a>DIV: uus väli 2e, 2f
 
- Väli 2e. Näitab lahtri 1a summa osa, mis on jaotise 897 omandatav tulu USA kinnisvara intresside likvideerimisel (USRPI).  
- Väli 2f. Näitab lahtri 2a summa osa, mis on jaotise 897 omandatav tulu USRPI likvideerimisel. Pidage meeles, et väljad 2e ja 2f kehtivad ainult välismaalastele ja üksustele, kelle sissetulekud säilitatavad selle olemuse otsestele või kaudsetele omanikele või kasusaajatele edastamisel või jaotamisel. Üldiselt käsitletakse seda faktiliselt Ameerika Ühendriikides asuva valdkonna või ettevõttega seonduvalt. Vaadake oma maksudeklaratsiooni juhiseid. 
 
#### <a name="nec-new-box-2"></a>NEC: uus väli 2 
 
Kui ruut 2 on märgitud, teatage vähemalt 5000 $ väärtuses tarbekaupadest, mis müüdi teile edasimüügiks, ostu-müügi, sissemaksu-komisjonitasu või muul alusel. Üldiselt peate teatama kõigist nende toodete müügist saadud tuludest Graafikus C (Vorm 1040). 
 
Samas on muudetud NEC-vormi suurust. Printimisel on kolm vormi lehe kohta. 
 
#### <a name="misc-new-box-11"></a>MISC: uus väli 11 
 
Väljal 11 kuvatakse kala edasimüügiks ostetud toote eest makstud summa mis tahes isikule, kes tegutseb kala püüdmise valdkonnas. Vaadake oma maksudeklaratsiooni juhiseid selle tulu esitamiseks. 
 
#### <a name="electronic-filing"></a>Elektrooniline esitamine 
Elektroonilise esitamise kohta lisateabe saamiseks vt [Elektroonilise esitamise nõuete väljaanne](https://www.irs.gov/pub/irs-pdf/p1220.pdf).

Vormingu spetsifikatsioonide ja kirje paigutuste värskendamine 2021 e-aruande jaoks 
- Jaot. 2 Väljastaja A-kirje. 
- Summakoodid – suurendati Välja asukoht 28–45, Pikkus 18-le. 
 
#### <a name="sec-2-issuer-a-record-for-reporting-payments-on-form-1099-div"></a>Jaot. 2 Väljastaja A-kirje, Maksete esitamiseks Vormil 1099-DIV: 
- Summa tüüp – lisati Jaotis 897 tavalised dividendid ja lisati Summakood H. 
- Summa tüüp – lisati Jaotis 897 kapitalitulu ja lisati Summakood H. 
 
#### <a name="sec-3-payee-b-record"></a>Jaot. 3 Makse saaja B-kirje 
- Üldteabe kirjed – värskendati kolmandat loetelupunkti 16 kuni 18 väljad Maksesumma. 
- Välja pealkiri Makse H – uuendati Välja paigutus 247–258, Välja pealkiri, Pikkus ja Välja üldine kirjeldus. 
- Välja pealkiri Makse J – uuendati Välja paigutus 259–270, Välja pealkiri, Pikkus ja Välja üldine kirjeldus. 
- Väli Tühi uuendati Välja asukohale 271–286. 
- Välismaa näidik uuendati Välja asukohale 287. 
- Esimese makse saaja nime rea välja uuendati Välja asukohale 288–327. 
- Teise makse saaja nime rea välja uuendati Välja asukohale 328–367. 
- Kirje paigutuse asukohad, Vorm 1099-MISC – kustutati Välja asukoht 548 ja Välja pealkirja FATCA esitamise nõude näidik. 
- Kirje paigutuse asukohad, Vorm 1099-NEC – uuendati 545–546 väärtusele Tühi, uuendati väli 547 väärtusele Otsemüügi Indikaator, uuendati Pikkus ja Kirjeldus ning Kommentaarid 548–722 väärtusele Tühi. 
 
#### <a name="sec-4-end-of-issuer-c-record"></a>Jaot. 4 Väljastaja lõpp C-kirje 
- Välja pealkiri Makse H – uuendati Välja paigutus 304–321, Välja pealkiri, Pikkus ja Välja üldine kirjeldus. 
- Välja pealkiri Makse J – uuendati Välja paigutus 322–339, Välja pealkiri, Pikkus ja Välja üldine kirjeldus. 
- Välja pealkiri 340–499 – uuendati pikkust 160-ni. 
 
#### <a name="sec-5-state-totals-k-record"></a>Jaot. 5 Osariigi kogusummad K-kirje 
- Välja pealkiri Makse H – uuendati Välja paigutus 304–321, Välja pealkiri, Pikkus ja Välja üldine kirjeldus. 
- Välja pealkiri Makse J – uuendati Välja paigutus 322–339, Välja pealkiri, Pikkus ja Välja üldine kirjeldus. 
- Välja pealkiri 340–499 – uuendati pikkust 160-ni.  

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Ostureskontro: 1099 – kuidas muuta välja 1099 ja selle väärtusi hankijal, kes ei jälginud aasta vältel 1099 teavet?
Kasutage funktsiooni Uuenda 1099 (**Ostureskontro > Hankijad>Kõik hankijad > Valige hankija > Hankija vahekaart lindil > Uuenda 1099**), et sirvida läbida varem makstud arve kanded, et määrata 1099-andmed uuesti ja õigesti vastavalt vahekaardi **Maks 1099** sätetele lehel **Hankija**.

## <a name="can-i-run-the-update-1099-for-all-my-vendors-at-once"></a>Kas saan käivitada funktsiooni Uuenda 1099 kõigi hankijate jaoks korraga?
Ei. Uuenda 1099 protseduur tehakse ühele hankijale korraga. Kui teie organisatsioon vajab seda nõuet, siis andke oma hääl ettepanekule [Hankija 1099 andmete uuendamise pakktöötlus](https://experience.dynamics.com/ideas/idea/?ideaid=5493d608-350e-eb11-b5d9-0003ff68ded8).

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-versus-update-all-in-the-update-1099-utility"></a>Ostureskontro: 1099 – „Olemasolevate 1099 summade uuesti arvutamine“ vs. „Kõikide uuendamine“ utiliidis Uuenda 1099.
Märkeruut **Olemasolevate 1099 summade uuesti arvutamine** lähtestab 1099 summa kokku tasustatud väärtustele, kui seda kasutatakse koos märkeruuduga **Kõikide uuendamine**. 

[![Maksu 1099 kanded: enne uuendamisprotseduuri käivitamist.](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

Märkeruut **Olemasolevate 1099 summade uuesti arvutamine** tuleb mängu alles siis, kui arvel on osalisi 1099 väärtusi või seda muudeti Maksu 1099 vormil. Oletagem näiteks, et teil on arve väärtusega 1000.00 $, kuid kasutaja tipib käsitsi 1099-summa 500.00 $ suurusele arvele.

[![Maksu 1099 kanded: valikute Kõikide uuendamine ja Olemasolevate 1099 summade uuesti arvutamine korraga märkimine.](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Selle tasumisel on 500.00 $ tasutud 1099-summa. Kui teete ümberarvutamisprotseduuri, muudab süsteem 1099-summa väärtuseks 1000.00 $, mis on tasutud kogusumma.

[![Maksu 1099 kanded: pärast 1099-protseduuri käivitamist.](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Ostureskontro: 1099 – 1099-kannete käsitsi loomine
Organisatsioonil võib olla vaja luua käsitsi 1099-kandeid, mis pole arvega seostatud. 1099 kannete käsitsi lisamiseks valige **Ostureskontro > Perioodilised ülesanded > Maks 1099 > 1099-te hankija tasakaalustus**. Valige nupp **Käsitsi 1099 kanded**. 

Käsitsi loodud 1099 kandeid ei uuendata utiliidis **Uuenda 1099** protsessiga **Kõikide uuendamine** ega protsessiga **Olemasolevate 1099 summade uuesti arvutamine**.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Ostureskontro: 1099 – kas Dynamics 365 Finance toetab 1096 vormi? 

Dynamics 365 Finance ei prindi 1096 aastakokkuvõtte ja USA teabetagastuste edastamise vormi.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Ostureskontro: 1099 – kas on uusi funktsioone, mis toetavad 1099-aruandlust avalikus sektoris? 
Lisatud on uus avaliku sektori funktsioon **1099-teabe uuendamine põhikonto järgi**, mille saate lubada **funktsioonihalduse** tööruumis. See funktsioon võimaldab arvestuse jaotuses seostada hankija 1099-väärtused põhikonto järgi, mitte hankija kirje vaikekonto järgi.

Lisateavet vt teemast [Hankijate häälestamine aruande 1099 jaoks](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
