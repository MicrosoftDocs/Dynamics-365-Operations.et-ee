---
title: Varude sisestamine
description: See teema selgitab varude sisestusprofiili lehel varude sisestamise vahekaarti.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 464ffccd658003271b517038f430914fd5d8d50e
ms.sourcegitcommit: 6744cc2971047e3e568100eae338885104c38294
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/20/2022
ms.locfileid: "8783328"
---
# <a name="inventory-posting"></a>Varude sisestamine

Vahekaardil **Varud** profiilide **lehes** Varud kasutatakse laokannete pearaamatusse sisestamise juhtimiseks. Laokanded on kanded, mis ei ole loodud müügitellimustest, ostutellimustest või tootmistellimustest. Need sisestavad automaatselt füüsilised ja finantsiliselt laouuendused samaaegselt. Üks erand on üleviimistellimused, mis eraldavad füüsilisi ja finantsilisi uuendusi varude lähetamisel ja vastuvõtul.

Järgmises tabelis on toodud mõned laokannete näited.

| Kande tüüp | Vastuvõtmine või väljamine | Füüsiline sisestamine, finantsiline sisestamine või mõlemad | Kirjeldus |
|---|---|---|---|
| Liikumine | Mõlemad | Mõlemad | <p>Liikumise tööleht on lao tööleht, mida saate kasutada varude lisamiseks või eemaldamiseks. See toimib nagu varude korrigeerimist tööleht. Üks võtmeerinevus on siiski see, et põhikonto, mis kande tasakaalustab, on määratletud.</p><p>Liikumise tööleht sisestab algsaldod ja mahakkorrektsioonid, mis tuleb kuludesse esitada. Seda kasutatakse näiteks lao eemaldamisel müügi näidisena.</p><p>Töölehe sisestamisel toimuvad füüsilised ja finantsuuendused samaaegselt.</p><p>Tööleheridadel olevad positiivsed kogused tähistavad sissetulekuid ja negatiivsed kogused tähistavad väljamineki.</p> |
| Varude korrigeerimine | Mõlemad | Mõlemad | Varude korrigeerimise töölehte kasutatakse varude lisamiseks või eemaldamiseks. See ei luba teil vastaskontot valida. Pearaamatukande uuendamiseks kasutatakse ainult **kontosid**, mis on määratud lao sisestusreeglite lehel. |
| Ülekanne (tööleht) | Mõlemad | Mõlemad | <p>Üleviimistöölehte kasutatakse varude teisaldamiseks ühest asukohast teise (ladustamisdimensioonide abil). See värskendab tooteteavet laokannetel uute toote- või jälgimisdimensioonidega.</p><p>Üleviimistööleht loob ühe rea kauba liikumiseks. Sellel real on varude dimensioonide jaoks väljad Alates ja Kuni. Üleviimistöölehe iga rida loob kaks laotehingut. Varude dimensioonide "alates" jaoks luuakse üks kanne. See tähistab väljaminek ja selle kogus on negatiivne. Teine kanne luuakse "kuni" varude dimensioonide jaoks. See tähistab sissetulekut ja sellel on positiivne kogus.</p><p>Ülekandetöölehed ei pruugi kannet luua, kui lao liikumist peetakse mittefinantsilisteks ülekanneteks. Laodimensioone, mis erinevad väärtuste "alates" ja "kuni" **·** **·** **jaoks, ei märgita laoala dimensioonigrupis või jälgimisdimensiooni grupi lehel suvandiga Finantsiline laovaru.** Näiteks kui varude finantsiline **valik** ei ole **asukohadimensioonis** märgitud ja te teisaldate varud ühest asukohast teise samal saidil ja laos, siis kannet ei looda.</p><p>Üleviimistöölehed erinevad üleviimistellimustest selles osas, et liikumiseks pole ühtegi dokumenti. Uuendamine toimub töölehe sisestamisel ühe kandega. Vastandina võib üleviimistellimus luua komplekteerimis- ja lähetusdokumente ning nõuab kande töötlemiseks kahte uuendust.</p> |
| Üleviimistellimuse saadetis | Probleem | Mõlemad | <p>Uue üleviimistellimuse loomisel on igal rea ja varude dimensiooni kombinatsioonil kaks laotehingut: üks üleviimistellimuse saadetise ja teine üleviimistellimuse sissetuleku kohta. Üleviimistellimuse lähetamisel uuendatakse kaks laotehingut ja kaupade transiidi jaoks luuakse kaks täiendavat laotehingut kokku nelja laokande kohta.</p><ol><li>Esimest laokannet kasutatakse kauba eemaldamiseks lähtelaost ja -asukohast. Selle kande väljaminek on **müüdud**, näitamaks, et kaup ei ole enam laos saadaval.</li><li>Teist laokannet kasutatakse kauba lisamiseks transiitlattu, mis on valitud lao jaoks, millelt kaup üle viiakse. Selle kande sissetuleku olek on **Ostetud**.</li><li>Kolmas laokanne on ette ülekanne transiitlaost sihtlattu. Selle kande väljaminek on füüsiliselt **reserveeritud**. See olek tagab, et kaupa ei saa muu protsess tarbida, kui see on veel transiidis.</li><li>Neljas laokanne on kaupade sissetulekuks sihtlaos. Selle kande sissetuleku olek on **Tellitud**.</li></ol> |
| Üleviimistellimuse tarne | Sissetulek | Mõlemad | Kui üleviimistellimus on sihtlaos vastu võetud, uuendatakse transiitlaos (eelmises näites number 3) **·** **tehtud laokande varude olek väärtusele Müüdud ja sihtlao laokande varude olek uuendatakse olekule Ostetud.** |
| Kooslused | Mõlemad | Mõlemad | Saate kasutada koosluse töölehte, et teatada toote lõpetatuna ja tarbida protsessi käigus tarbitud toormaterjale ilma tootmistellimuseta. Koosluse tööleht sisaldab tavaliselt vähemalt ühte positiivset rida lõpetatud kauba kohta ja üht või enamat negatiivset rida tarbitava toormaterjali kohta. Valmis heade kaupade rida on lao sissetulekuks, samas kui negatiivsed read on toormaterjalide laost väljaminek. Koosluse töölehe loomisel on esimene rida koosluse päis ja järgnevad lisatud read koosluse read. |
| Varude omandiõiguse muutmine | Mõlemad | Mõlemad | Varude omaniku muudatuste töölehte kasutatakse varude omaniku muutmiseks hankijalt teie organisatsioonile. Varude omaniku muudatuste töölehed sarnanevad lao üleviimistöölehtedega, kus kaks laotehingut on seotud iga rea ja varude dimensiooni kombinatsiooniga. Üks laokanne eemaldab varud **hankijalt** omandiõiguse dimensioonis ja teine lisab kauba juriidilisele isikule omandiõiguse **dimensioonis**. |
| Kauba saabumine | Sissetulek | Füüsiline | Saabuva kauba töölehte kasutatakse varude sissetuleku oleku uuendamiseks olekusse **Registreeritud**. Seda kasutatakse tavaliselt kaupade ostutellimuse kaupade sissetulekul ja müügitellimuse tagastustel. |
| Materjalid tootmisse | Sissetulek | Füüsiline | Tootmissisendi tööleht sarnaneb kauba saabumise töölehega. Tootmissisendit kasutatakse laos tootmistellimuselt lõpetatud kaupade vastuvõtuks. Kui tööleht on sisestatud, uuendatakse laokande olek väärtusele **Registreeritud**. |
| Inventuur | Mõlemad | Mõlemad | Inventuuritöölehte kasutatakse nende kaupade koguse kirjendamiseks, mida loendati varude dimensioonide konkreetse kombinatsiooni puhul. Laokanded luuakse siis, kui töölehe real on loenduserinevus. Rida, mille inventeeritud kogus on suurem, põhjustab sissetuleku varudesse. Rida, mille inventeeritud kogus on väiksem, põhjustab lao väljaminek. Ridadel, kus inventeeritud kogus vastab eeldatud kogusele, pole laokandeid. |
| Märgistusega inventuur | Pole kohaldatav | Pole kohaldatav | Sildiga inventuuri töölehte kasutatakse määratud ja täielikus inventuuris kasutatud lao siltide jälgimiseks. Saate kasutada töölehte, et määrata sildi number kauba ja varude dimensiooni konkreetsele kombinatsioonile ning jälgida selle sildi olekut kogu kaubavaru jooksul. Sildiga inventuuritööleht ei loo laokandeid. |
| Kvaliteettellimused | Probleem | Füüsiline | <p>Kvaliteettellimust kasutatakse antud partii katsetulemuste salvestamiseks laos. Iga kvaliteettellimus on seotud olemasoleva laokande või laokande osaga.</p><p>Kvaliteettellimus loob uue laokande kahel juhul:</p><ul><li>Kvaliteettellimus on märgitud vahekaardil **Üldine väljapurustuskatsena** **·**.</li><li>Kvaliteettellimus märgitakse vahekaardil **Üldine valideerimise nurjumisel** **vahelaoks** ja testi kinnitamine nurjub. Sel juhul luuakse kaks laotehingut. Üks laokanne eemaldab kauba algsest varude dimensiooni kombinatsioonist ja asukohast ning teine lisab kauba vahelattu.</li></ul> |
| Vahelaoorderid | Mõlemad | Mõlemad | <p>Vahelaoorderite laokanded on nagu üleviimistellimused. Vaheladu kasutatakse varude jälgimiseks. On olemas kaks sissetulekutehingut ja kaks väljaminektehingut.</p><p>Tellimuse algsel loomisel luuakse kaks tehingut. Sissetulekukande olek on vahelao puhul **tellitud**, mis on seotud laoga, kus kaup asub. Väljaminekkande olek **laos, kus** kaupa hoitakse, on tellimusel.</p><p>Vahelaoorderi käivitamisel luuakse kaks täiendavat kandet ja uuendatakse olemasolevad kanded. Vahelao sissetulekukande olek **uuendatakse olekule Vastu võetud ja ladustamislao väljaminek kande olek värskendatakse olekule Mahaarvatud** **.**</p><p>Neid kahte uut kandet kasutatakse ladustamise lattu tagasi te vaheldamise näitamiseks. Sissetulekukande olek laolao **jaoks** **on** Tellitud ja selle väljaminekkande olek vahelaos on Füüsiliselt reserveeritud.</p><p>Kui teatate vahelaoorderi lõpetatuna, näitab see operatsioon vahelaoorderi füüsilist uuendamist. Laolaos uuendatakse sissetuleku olekuks **Vastu võetud**.</p><p>Vahelaoorderi lõpetamisel näitab see operatsioon vahelaoorderi finantsi värskendamist. Väljastamiskannete olek värskendatakse olekusse **Müüdud** ja sissetulekukannete olek värskendatakse olekusse **Ostetud**.</p><p>Vahelaoorderi saate ka praagiks määrata. See toiming eemaldab kauba laost. Vahelaoorderi mahakandmisel jäävad alles ainult kolm tehingut. Ladustamislao sissetulekukanne eemaldatakse ja järelejäänud sissetulekukande olek uuendatakse olekuks **Ostetud**. Kahe väljaminekkande olek uuendatakse olekuks **Müüdud**. See toiming on tellimuse füüsiline ja finantsiline värskendus.</p> |

## <a name="fixed-receipt-price-posting"></a>Fikseeritud jaehinna sisestamine

Fikseeritud jaehind võimaldab teil kasutada toote puhul standardset kulu. See on alternatiivne valik **Standardne kulu** kauba **mudeligrupi** lehel. Peamine erinevus fikseeritud jaehinna kasutamisel on see, et praegu konfigureeritud omahinda kasutatakse kauba puhul lao sissetuleku sisestamisel. Fikseeritud jaehinna puhul puudub kulu ümberhindluse protsess. Finantsvärskenduse sisestamisel kasutatakse sisestamisel praegust omahinda. Kui sissetulekul ja arvel kasutatav omahind erineb, sisestatakse hälve fikseeritud vastuvõtuhinna kasumi- ja kahjumikontodele.

Fikseeritud jaehinna valikuliseks kasutamiseks toote puhul peate lõpule viima järgmise konfiguratsiooni:

- Märkige laokande **real** valitud kauba **puhul kauba mudeligrupi** lehel ruut Sisesta füüsilised varud.
- Märkige kauba **mudeligrupi** lehel ruut Fikseeritud **vastuvõtuhind**.
- Määratlege põhikontod järgmiste sisestustüüpide jaoks lao sisestusreeglite **lehel**:

    - Fikseeritud jaehinna kasum
    - Fikseeritud jaehinna kahjum

Lisateavet vt jaotisest Fikseeritud [vastuvõtuhind](/supply-chain/cost-management/fixed-receipt-price.md).

## <a name="catch-weight-posting"></a>Tegeliku kaalu sisestamine

Tegeliku kaalu tooteid kasutatakse sageli sellistes majandusharudes, kus tooted võivad veidi erineda kaalu, suuruse või mõlema järgi. Tegeliku kaalu toodetel on kaks mõõtühiku ühikut: varude ühik ja tegeliku kaalu ühik. Lattu sisse saadud varude kaal võib lao väljaminekul laost erineda. Tegeliku kaalu tootetöötlus korrigeerib varusid.

Kui tegeliku kaalus on hälbeid, sisestatakse erinevused kontodele, **·** **mis** on **määratud varude sisestusreeglite lehel väljadel Tegeliku kaalu kahjum ja Tegeliku kaalu** tulu. Tavaliselt määratakse mõlemale väljale sama põhikonto.

Järgmine tabel näitab vaikimisi sisestamistüüpide näiteid ja sisaldab näidis põhikontosid ja kirjeldusi.

- Deebet/kreedit?" Veerg <a0/& näitab, kas kanne on tavaliselt deebet või kreedit. Mõnel juhul saab kanne sisestada deebeteid või kreediteid.
- Veerg Kliiringukonto näitab, et sisestamistüüp on kliiringukonto. See tähendab, et hilisema kande sisestamisel tühistatakse kontole sisestatud summa automaatselt.
- Veerus "P/F" kuvatakse sisestamistüüp. "P" tähistab füüsilist sisestamist ja "F" esindab finantsilist sisestamist.
- Veerg Järgi näitab, kas sisestamistüübi põhikonto on tavaliselt sama, mis mõne muu sisestustüübi põhikonto. See näitab tavaliselt sisestamisel kasutatavat sisestustüüpi.

> [!NOTE]
> Tabelis on soovitused põhikontode ja põhikonto nimede kohta. Soovitame teil teha koostööd raamatupidajaga, et määratleda ärivajaduste jaoks parim konfiguratsioon.

| Sisestamistüüp | Põhikonto näide | Põhikonto nime näide | Konto tüüp | Deebet/kreedit? | Kliiringukonto | Ette/tagasi | Järgige | Kirjeldus |
|---|---|---|---|---|---|---|---|---|
| Tegeliku kaalu kahjumikonto | 510520 | Varude korrigeerimine | Kulu | | Nr | Mõlemad | Tegeliku kaalu kasumikonto | Seda kontot kasutatakse, kui sisestate varude kande, kus tegeliku kaalu summa on väiksem. |
| Tegeliku kaalu kasumikonto | 510520 | Varude korrigeerimine | Kulu | | Nr | Mõlemad | Tegeliku kaalu kahjumikonto | Seda kontot kasutatakse, kui sisestate varude kande, kus tegeliku kaalu summa on suurem. |

Lisateavet tegeliku kaalu toodete kohta vt tegeliku kaalu [kaupadest ja](/dynamicsax-2012/appuser-itpro/about-catch-weight-items.md)[tegeliku kaalu toote töötlemisest laohaldusega](/supply-chain/warehousing/catch-weight-processing.md).

## <a name="inventory-to-fixed-asset-transfer-posting"></a>Varude põhivarasse ülekandmise sisestamine

Ladu põhivara töölehele (**Põhivarade** \> **·** \> **töölehed** Ladu põhivaratöölehele) kasutatakse kaupade laost välja viimiseks ja nende teisendamiseks põhivaraks. Lisateavet leiate jaotisest [Põhivarade integreerimine](/fixed-assets/fixed-asset-integration.md).

Järgmine tabel näitab vaikimisi sisestamistüüpide näiteid ja sisaldab näidis põhikontosid ja kirjeldusi.

- Deebet/kreedit?" Veerg <a0/& näitab, kas kanne on tavaliselt deebet või kreedit. Mõnel juhul saab kanne sisestada deebeteid või kreediteid.
- Veerg Kliiringukonto näitab, et sisestamistüüp on kliiringukonto. See tähendab, et hilisema kande sisestamisel tühistatakse kontole sisestatud summa automaatselt.
- Veerus "P/F" kuvatakse sisestamistüüp. "P" tähistab füüsilist sisestamist ja "F" esindab finantsilist sisestamist.
- Veerg Järgi näitab, kas sisestamistüübi põhikonto on tavaliselt sama, mis mõne muu sisestustüübi põhikonto. See näitab tavaliselt sisestamisel kasutatavat sisestustüüpi.

> [!NOTE]
> Tabelis on soovitused põhikontode ja põhikonto nimede kohta. Soovitame teil teha koostööd raamatupidajaga, et määratleda ärivajaduste jaoks parim konfiguratsioon.

| Sisestamistüüp | Põhikonto näide | Põhikonto nime näide | Konto tüüp | Deebet/kreedit? | Kliiringukonto | Ette/tagasi | Järgige | Kirjeldus |
|---|---|---|---|---|---|---|---|---|
| Põhivara väljaminek | 180100 | Materiaalsed põhivarad | Vara | Krediit | Nr | Mõlemad | Pole kohaldatav | Seda kontot kasutatakse, kui sisestate lao põhivara töölehele, et eemaldada kaup varudest ja teisendada see põhivaraks. |

## <a name="moving-average-posting"></a>Liikuv keskmise sisestamine

Liikuv keskmine on perpetual kuluarvestusmeetod, mis põhineb keskmise põhimõttel. Lao väljaminek ei muutu, kui ostukulu on muutunud. Erinevus on kapitaliseeritud ja põhineb proportsionaalsel arvutusel. Ülejäänud summa kantakse kuludesse.

Järgmine tabel näitab vaikimisi sisestamistüüpide näiteid koos näidis põhikontode ja kirjeldustega.

- Deebet/kreedit?" Veerg <a0/& näitab, kas kanne on tavaliselt deebet või kreedit. Mõnel juhul saab kanne sisestada deebeteid või kreediteid.
- Veerg Kliiringukonto näitab, et sisestamistüüp on kliiringukonto. See tähendab, et hilisema kande sisestamisel tühistatakse kontole sisestatud summa automaatselt.
- Veerus "P/F" kuvatakse sisestamistüüp. "P" tähistab füüsilist sisestamist ja "F" esindab finantsilist sisestamist.
- Veerg Järgi näitab, kas sisestamistüübi põhikonto on tavaliselt sama, mis mõne muu sisestustüübi põhikonto. See näitab tavaliselt sisestamisel kasutatavat sisestustüüpi.

> [!NOTE]
> Tabelis on soovitused põhikontode ja põhikonto nimede kohta. Soovitame teil teha koostööd raamatupidajaga, et määratleda ärivajaduste jaoks parim konfiguratsioon.

| Sisestamistüüp | Põhikonto näide | Põhikonto nime näide | Konto tüüp | Deebet/kreedit? | Kliiringukonto | Ette/tagasi | Järgige | Kirjeldus |
|---|---|---|---|---|---|---|---|---|
| Liikuva keskmise hinnaerinevus | 510600 | Liikuva keskmise hinna erinevus | Kulu | Mõlemad | Nr | Mõlemad | Pole kohaldatav | Seda kontot kasutatakse siis, kui sissetuleku ja arve kulu on erinev. |
| Liikuva keskmise ümberhindamine | 510610 | Liikuva keskmise ümberhindamine | Kulu | Mõlemad | Nr | Mõlemad | Pole kohaldatav | Seda kontot kasutatakse, kui korrigeerite toote liikuvat keskmist kulu |

## <a name="sample-posting-profile-configuration"></a>Sisestusprofiili näidiskonfiguratsioon

Järgmine tabel näitab vaikimisi sisestamistüüpide näiteid koos näidis põhikontode ja kirjeldustega.

| Sisestamistüüp | Põhikonto näide | Põhikonto nime näide | Konto tüüp | Deebet/kreedit? | Kliiringukonto | Ette/tagasi | Järgige | Kirjeldus |
|---|---|---|---|---|---|---|---|---|
| Lao väljaminek | 140100 | Materjalide laoseis | Vara | Krediit | Nr | Mõlemad | Lao sissetulek | Seda kontot kasutatakse siis, kui sisestatud laokanne on väljaminek (negatiivne kogus) ja see ei ole seotud müügi, ostude ega tootmisega. Selle konto vastaskonto on varude kulu, kahjumi konto. See konto tähistab tavaliselt bilansi varusid. |
| Laokulu, kahjum | 510100 | Lao kasum ja kahjum | Kulu | Deebet | Nr | Mõlemad | Varud, kulu, kasum | Seda kontot kasutatakse siis, kui sisestatud laokanne on väljaminek (negatiivne kogus) ja see ei ole seotud müügi, ostude ega tootmisega. Selle konto vastaskonto on lao väljaminek. |
| Lao sissetulek | 140100 | Materjalide laoseis | Vara | Deebet | Nr | Mõlemad | Lao väljaminek | Seda kontot kasutatakse siis, kui sisestatud laokanne on sissetulek (positiivne kogus) ja see ei ole seotud müügi, ostude ega tootmisega. Selle konto vastaskonto on Varude kulu, kasumikonto. See konto tähistab tavaliselt bilansi varusid. |
| Varud, kulu, kasum | 510100 | Lao kasum ja kahjum | Kulu | Krediit | Nr | Mõlemad | Laokulu, kahjum | Seda kontot kasutatakse siis, kui sisestatud laokanne on sissetulek (positiivne kogus) ja see ei ole seotud müügi, ostude ega tootmisega. Selle konto vastaskonto on lao sissetuleku konto. |
| Allüksustevaheline kohustus | 231500 | Kontsernisisene kohustus | Kohustus | Deebet | Nr | Mõlemad | | Seda kontot kasutatakse siis, kui varusid viiakse üle varude dimensioonide, näiteks laoala vahel, ning kauba hind on laoaladel erinev. |
| Allüksustevaheline nõue | 131500 | Saadaolev kontsernisisene | Vara | Krediit | Nr | Mõlemad | | Seda kontot kasutatakse siis, kui varusid viiakse üle varude dimensioonide, näiteks laoala vahel, ning kauba hind on laoaladel erinev. |
