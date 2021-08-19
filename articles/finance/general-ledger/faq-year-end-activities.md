---
title: Aastalõpu tegevuste KKK
description: See teema on koostatud selleks, et aidata teil teha vajalikud aastalõpu sulgemistegevused.
author: kweekley
ms.date: 01/25/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1b7606314b9cf7050a565822b5b9e23beb0cb4978b20e88596c5002d918cfcd9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725070"
---
# <a name="year-end-activities-faq"></a>Aastalõpu tegevuste KKK 

[!include [banner](../includes/banner.md)]

See teema on koostatud selleks, et aidata teil teha vajalikud aastalõpu sulgemistegevused. Selle teema teave keskendub põhiliselt pearaamatu ja ostureskontro aastalõpu sulgemistegevustele.

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
Aastalõpu sulgemise mall võimaldab organisatsioonil valida finantsdimensiooni taseme, mida hoitakse kasumi- ja kahjumisaldode ülekandmisel jaotamata kasumisse. Sätted võimaldavad organisatsioonil saldode jaotamata kasumisse teisaldamisel hoida alles üksikasjalikke finantsdimensioone (**Sule kõik**) või summeerida summad ühele dimensiooniväärtusele (**Sule üks**). Selle saab määratleda iga finantsdimensiooni jaoks. Lisateavet nende sätete kohta vt teemast [Aastalõpu sulgemine](year-end-close.md).

Soovitame teil hinnata oma organisatsiooni vajadusi ja jõudluse täiustamiseks sulgeda võimaluse korral nii palju dimensioone kui võimalik, kasutades aastalõpu suvandit **Sule üks**. Sulgedes ühele dimensiooniväärtusele (mis võib olla ka tühi väärtus), arvutab süsteem jaotamata kasumi konto kirjete saldode määratlemisel vähem üksikasju.

### <a name="10013-update-or-later"></a>10.0.13 või uuem värskendus
Kui olete pärast organisatsiooni viimast aastalõpu sulgemist teinud värskenduse versioonile 10.0.13 või uuemale versioonile, võib aastalõpu sulgemise protsess kesta kauem, kuna toimub [RäsiV2 funktsiooni juurutamine](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/verify-hash-function-changes-after-update-to-dynamics-365-finance-2020-release-wave-2). Mõiste *räsi* viitab väljale, mis arvutatakse teiste stringiväljade alusel. Turvalisuse täiustamiseks värskendati räsi GUID-väärtuse arvutamise API-t. Aastalõpu sulgemise protsessi kiirendamiseks soovitame enne aastalõpu sulgemise käivitamist dimensioonikogumite saldod uuesti luua. Kui olete pärast versioonile 10.0.13 värskendamise tegemist dimensioonikogumi saldod juba uuesti loonud, ei ole vaja uuesti loomist korrata.
 
## <a name="general-ledger--what-does-the-period-close--year-end-close-do"></a>Pearaamat – mida Perioodi sulgemine - Aastalõpu sulgemine teeb?
 
[![Perioodi sulgemine, aastalõpu sulgemine.](./media/faq-2020-yr-end-05.png)](./media/faq-2020-yr-end-05.png)

### <a name="performance-improvements-for-rebuilding-financial-dimension-sets-new-feature"></a>Jõudluse täiustused finantsdimensioonikogumite uuesti loomiseks (uus funktsioon)
Versioonile 10.0.16 lisatud uus funktsioon parendab aastalõpu sulgemise ja konsolideerimise protsesside jõudlust. Funktsiooni nimeks on Jõudluse täiustused finantsdimensioonikogumite uuesti loomiseks. See funktsioon muudab dimensioonikogumite uuesti loomise viisi nii, et need luuakse uuesti ainult asjakohase ajavahemiku jaoks. Eelmistes versioonides loodi dimensioonikogumid uuesti kõigi kuupäevade jaoks. Näiteks kui sulgete aasta 2020, loob süsteem uuesti ainult 2020. rahandusaasta kannete saldod. Kui käivitate konsolideerimise kuupäevavahemikule 1. november 2020 kuni 30. november 2020, loob süsteem uuesti saldod ainult selle kuupäevavahemiku jaoks.

Kuna seda funktsiooni loetakse murranguliseks muudatuseks, peate selle **funktsioonihalduse** tööruumi kaudu lubama.
 
[![Aastalõpu sulgemine.](./media/faq-2020-yr-end-06.png)](./media/faq-2020-yr-end-06.png)

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2020"></a>Ostureskontro: millised muudatused on tehtud 1099 aastalõpu aruandluse toetamiseks 2020. aastal?

1099 aastalõpu muudatuste jaoks aastal 2020 on lisatud kaks uut regulatiivset funktsiooni. Esimene funktsioon **Muudatuste rakendamine 1099-NEC- ja 1099-MISC-vormi aasta 2020 jaoks** väljastati aasta keskel kohustusliku funktsioonina. Selle eesmärk on tagada, et 2020. aasta 1099 kandeandmeid saaks uues 1099-NEC-vormis jälgida. See funktsioon lisas 1099 väljad, mis on vajalikud uue 1099-NEC-i toetamiseks, ja värskendas 1099-MISC-välju. See värskendus uuendas ka hankija kirje andmeid 1099-välja teabe jaoks. 

Teine regulatiivne funktsioon **2020. aasta maksuseaduse jaoks värskendatud 1099-väljavõtted** sisaldab järgmisi muudatusi.

- 1099-OID – IRS on teisendanud vormi pidevaks kasutamiseks.
   - Printimisel tuleb täita aruandeaasta 3. ja 4. number. Kasutage **Aruandeaasta** välja 3. ja 4. numbrit valikust **Maksu 1099 prindivalikud**. 

- 1099-NEC – uus vorm 2020. aasta jaoks. See kajastab mittetöötaja hüvitust. 

-   1099-MISC – vormi 1099-NEC loomise tõttu on IRS üle vaadanud vormi 1099-MISC ja paigutanud ümber teatud tulude esitamise lahtrinumbrid.
Allpool on loetletud tuluaruandluses ja vormi lahtrinumbrites tehtud muutused.
   - Maksja tehtud otsemüügid summas 5000 $ või rohkem (märkeruut) väljal 7.
   - Saagi kindlustuse tulud esitatakse lahtris 9.
   - Advokaadi kogutulud on esitatakse lahtris 10.
   - Jaotise 409A viitvõlad esitatakse lahtris 12.
   - Kvalifitseerimata edasilükkunud hüvituse tulu esitatakse lahtris 14.
   - Väljad 15, 16 ja 17 esitavad vastavalt kinnipeetud osariiriigimaksud, osariigi ID-koodi ja osariigis teenitud tulu summa.

- 1099-DIV ja 1099-INT on 2020. aastal jäänud muutmata.

- Elektrooniline esitamine – vormingut on muudetud, et hõlmata uus NEC-vorm ja lahtri MISC ülalkirjeldatud muudatused. Täpset teavet elektroonilise esitamise nõuete kohta vt [IRS-i trükises 1220](https://www.irs.gov/pub/irs-pdf/p1220.pdf).

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Ostureskontro: 1099 – kuidas muuta välja 1099 ja selle väärtusi hankijal, kes ei jälginud aasta vältel 1099 teavet?
Kasutage funktsiooni Uuenda 1099 (**Ostureskontro > Hankijad>Kõik hankijad > Valige hankija > Hankija vahekaart lindil > Uuenda 1099**), et sirvida läbida varem makstud arve kanded, et määrata 1099-andmed uuesti ja õigesti vastavalt vahekaardi **Maks 1099** sätetele lehel **Hankija**.

## <a name="can-i-run-the-update-1099-for-all-my-vendors-at-once"></a>Kas saan käivitada funktsiooni Uuenda 1099 kõigi hankijate jaoks korraga?
Ei. Uuenda 1099 protseduur tehakse ühele hankijale korraga. Kui teie organisatsioon vajab seda nõuet, siis andke oma hääl ettepanekule [Hankija 1099 andmete uuendamise pakktöötlus](https://experience.dynamics.com/ideas/idea/?ideaid=5493d608-350e-eb11-b5d9-0003ff68ded8).

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-vs-update-all-in-the-update-1099-utility"></a>Ostureskontro: 1099 – „Olemasolevate 1099 summade uuesti arvutamine“ vs „Kõikide uuendamine“ utiliidis Uuenda 1099.
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
