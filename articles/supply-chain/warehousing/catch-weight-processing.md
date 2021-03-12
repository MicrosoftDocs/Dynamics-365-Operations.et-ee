---
title: Tegeliku kaalu toote protsess laohalduse abil
description: Selles teemas kirjeldatakse, kuidas kasutada töömalle ja asukohakorraldusi määramaks, kuidas ja kus laos tööd tehakse.
author: perlynne
manager: tfehr
ms.date: 08/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCatchWeightTag, WHSCatchWeightItemHandlingPolicy, TMSLoadBuildWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-1-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 6ecadb06adce5a0cbf1614c7da8fc65cb801e249
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001170"
---
# <a name="catch-weight-product-processing-with-warehouse-management"></a>Tegeliku kaalu toote protsess laohalduse abil

[!include [banner](../includes/banner.md)]


## <a name="feature-exposure"></a>Funktsiooni esiletõstmine

Laohalduse abil tegeliku kaaluga toodete haldamiseks peate selle funktsiooni litsentsi konfiguratsioonivõtme abil sisse lülitama. Valige suvandid **Süsteemihaldus \> Seadistamine \> Litsentsi konfiguratsioon**. Seejärel laiendage vahekaardil **Konfiguratsioonivõtmed** jaotist **Kaubandus \> Lao- ja transpordihaldus** ja märkige ruut **Tegelik laokaal**.

> [!NOTE]
> Sisse peab lülitama ka litsentsi konfiguratsioonivõtmed **Lao- ja transpordihaldus** ning **Protsessi jaotus \> Tegelik kaal**. Tegeliku kaalu konfiguratsioonivõtmete määramiseks peate funktsiooni ka sisse lülitama, kasutades selleks tööruumi **Funktsioonihaldus**. Peamine funktsioon, mis peab olema sisse lülitatud, on **Tegeliku kaalu toote töötlemine laohaldusega**. Kaks seotud, kuid valikulised funktsioonid, mida te võite soovida sisse lülitada on **Varude oleku muudatused tegeliku kaaluga toodetel** ja **Kasutada olemasolevaid tegeliku kaalu silte tootmistellimuste kinnitamisel lõpetatuna**.

Kui litsentsi konfiguratsioonivõti on sisse lülitatud ja loote väljastatud toote, saate valida suvandi **Tegelik kaal**. Samuti saate seostada väljastatud toote laoala dimensiooni rühmaga, mille puhul on valitud parameeter **Kasuta laohalduse protsesse**.

Enne toote kasutamist laohalduses peate tegema tootekohase põhiseadistuse tegeliku kaalu kohta.

- Määratlege ühikuteisenduse määratluse osana nominaalse kaalu teisendamine tegeliku kaalu ühiku (karp) ja laoühiku (kilogramm \[kg\]) vahel.
- Määratlege tegeliku kaalu ühiku seadistuse osana minimaalne ja maksimaalne kaaluhälve.
- Seadistage ühiku seeriagrupp, milles tegeliku kaalu ühik on määratletud madalaima varude arvestusühikuna (SKU).
- Seadistage tegeliku kaalu kauba käitlemispoliitika.

Lisateabe saamiseks vt jaotist [Tegeliku kaalu kaupade seadistamine ja haldamine](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items).

## <a name="transaction-adjustments"></a>Kande korrigeerimised

Kuna lattu saabuvate varude kaal võib erineda laost väljastatavate varude kaalust, peab tegeliku kaalu toote protsess varusid korrigeerima.

> [!NOTE]
> Mobiilse seadme tegevus käivitab kande korrigeerimised ainult juhul, kui toote tegeliku kaaluga käsitlemise poliitika väljuva kaaluhälbe meetod on **Luba kaaluhälve**.

**Näide 1**

Tootmisprotsessi **Kinnita lõpetamine** ajal registreeritakse kaheksat kasti tegeliku kaalu toodet sisaldava litsentsiplaadi sissetuleva kaaluna 80,1 kg. Seejärel ladustatakse litsentsiplaat lõpetatud kaupade alast eemale ja ladustamisperioodi ajal kaob osa kaalust õhku.

Hiljem, osana müügitellimuse komplekteerimisprotsessist, registreeritakse sama litsentsiplaadi kaaluna 79,8 kg. Seetõttu on teil nüüd süsteemis füüsilise dimensioonikogumi osana kaaluerinevus.

Sel juhul korrigeerib süsteem erinevuse automaatselt, sisestades kande puuduva 0,3 kg kohta.

**Näide 2**

Toote määratluses on seadistatud toode tolereerima tegeliku kaalu ühiku **Kast** puhul minimaalse kaaluna 8 kg ja maksimaalse kaaluna 12 kg.

Nüüd on teil kaks kasti toodet, mille registreeritud kaal on 16 kg. Kui laotöötaja võtab ja kaalub ühe neist kastidest ning selle kaaluna registreeritakse 9 kg, kaalub teine kast 7 kg. Kuna aga 7 kg on alla minimaalse kaalu, teeb süsteem automaatse korrigeerimise, et suurendada vaba kaubavaru kaalu 1 kg võrra.

Selleks et seadistada kontod, kuhu need korrigeerimised sisestatakse, minge jaotisse **Kuluhaldus \> Pearaamatu integratsioonipoliitikate seadistus \> Sisestamine**. Seejärel määratlege vahekaardil **Varud** järgmised kontod.

- Tegeliku kaalu kahjumikonto
- Tegeliku kaalu kasumikonto

## <a name="catch-weight-item-handling-policy"></a>Tegeliku kaalu kauba käitlemispoliitika

Tegeliku kaalu kauba käitlemispoliitika määratleb kaupadele kaks peamist laohaldusvoogu: kauba kaalu registreerimise aeg ja viis.

Saate määratleda kaalu registreerimise aja müügi- ja üleviimistellimuse protsessis. Kaalu saab registreerida ühe järgmise protsessi ajal.

- **Komplekteerimine** – kaal registreeritakse tellimustöö algsete komplekteerimisrea ridadel.
- **Pakkimine** – kaal registreeritakse käsitsi pakkimise ajal. (Peate need kaubad saatma pakkimisjaama.)

Kui tegelik kaal registreeritakse pakkimisjaamas konteineri pakkimisprotsesside ajal, ei paluta laotöötajatel kaalu komplekteerimistöö ajal registreerida. Selle asemel kasutatakse pakkimisalale minevate komplekteeritud varude kaaluna füüsiliste varude keskmist kaalu. Seda kontseptsiooni rakendatakse ka tegeliku kaaluga toodete juures, mida jälgitakse siltidega. Sildiga jälgitud kaupade puhul määratlevad need parameetrid, millal silt hõivatakse. Silti saab hõivata kas komplekteerimise ajal, kasutades mobiilset seadet, või käsitsi pakkimise ajal.

> [!NOTE]
> Kuna suvand **Pakkimine** põhjustab varude värskendamist keskmise komplekteeritud kaaluga, võib see põhjustada lahknevuse, mis võib põhjustada tegeliku kaalu kasumi/kahjumi korrigeerimise ja/või erinevuse vaba kaubavaru kaalu ja tegeliku kaalu sildi kaalu vahel.

Sisemiste laohaldusprotsesside, nagu inventuur ja korrigeerimisparandused, puhul saate määratleda, kas kaal tuleb registreerida või mitte. Kui seda ei registreerita, kasutatakse nominaalset kaalu. Muud valikud võimaldavad teil hõivata kaalu ühe tegeliku kaalu ühiku kohta ja arvestusliku koguse kohta.

Saate ka määratleda kaalu registreerimise viisi. Ühes kahest põhivoost jälgitakse ja kasutatakse kaalu registreerimiseks tegeliku kaalu silte. Teises voos tegeliku kaalu silte ei jälgita.

- **Jah** – kaup kasutab tegeliku kaalu silte. Iga sildi number tähistab üht tegeliku kaalu ühikut (kast) ning kaal ja muu teave seostatakse sildiga. Väljaminevate protsesside puhul kasutatakse sildiga seotud kaalu.
- **Ei** – kaup ei kasuta tegeliku kaalu silte. Sissetulevad ja väljaminevad kaalumisprotsessid põhinevad tegelikul kaalul, mis registreeritakse iga protsessi käigus.

Tegeliku kaalu siltide jälgimise protsessi saab kasutada kaupade jälgimiseks, mille kaal ladustamisperioodi jooksul ei muutu. Kaal registreeritakse ainult sissetuleva laoprotsessi käigus. Väljamineva protsessi käigus tegeliku kaalu sildid lihtsalt skannitakse ja väljaminevate kannete töötlemisel kasutatakse siltidega seostatud kaale.

Teine oluline parameeter, mis on seotud tegeliku kaalu siltide töötlemisega on **Tegeliku kaalu sildi mõõtme jälgimise meetod**. Silte saab kas osaliselt jälgida või täielikult jälgida. Kui silt on osaliselt jälgitav, siis jälgitakse toote dimensioone, jälgimise dimensioone ja varude olekut. Kui silt on täielikult jälgitav, siis jälgitakse toote dimensioone, jälgimisdimensioone ja **kõiki** laoala dimensioone.

Lisaks, kui kaup on sildiga jälgitav, on olemas parameeter **Väljamineva sildi hõivamise meetod**. Saate seada selle parameetri nii, et teilt küsitakse alati mobiilsest seadmest väljaminevatel kannetel silti. Teise võimalusena saate seadistada parameetri nii, et teilt küsitakse silte ainult siis, kui need on kohustuslikud. Näiteks on antud litsentsiplaadil laos olemas viis tegeliku kaalu silti ja te olete märkinud, et soovite komplekteerida litsentsiplaadi kõik viis silti. Sel juhul, kui parameeter **Väljamineva sildi hõivamise meetod** on seadistatud väärtusele **Küsi silti ainult vajadusel**, komplekteeritakse viis silti automaatselt. Te ei pea iga silti skannima. Kui parameetri väärtuseks on seatud **Küsi alati silti**, peate skannima iga sildi, isegi kui komplekteeritakse kõik viis silti.

> [!NOTE]
> Reeglina hõivatakse sildid värskendatakse ainult mobiilse seadme menüü-üksustest. Sellegipoolest on mõned stsenaariumid, kus sildid hõivatakse kuskil mujal (nt käsitsi pakkimisjaamas). Kuid üldiselt tuleks mobiilse seadme menüükäske kasutada kõigi laotegevuse puhul, kus kasutatakse silte.

### <a name="how-to-capture-catch-weight"></a>Tegeliku kaalu registreerimine

**Tegeliku kaalu jälgimise kasutamisel** tuleb silt alati luua iga sissetuleva tegeliku kaalu ühiku jaoks ja iga silt tuleb alati seostada kaaluga.

Näiteks on tegeliku kaalu ühik **kast** ja te saate ühe kaubaaluse kaheksa kastiga. Sel juhul tuleb luua kaheksa kordumatut tegeliku kaalu silti ja kaal tuleb seostada iga sildiga. Olenevalt sissetuleva tegeliku kaalu sildist saab registreerida kas kõigi kaheksa kasti kaalu ja jaotada igale kastile keskmise kaalu või registreerida iga kasti jaoks kordumatu kaalu.
Kui kasutate funktsiooni **Kasuta olemasolevaid tegeliku kaalu silte tootmistellimuste kinnitamisel lõpetatuna** , kui protsess on lubatud mobiilseadme menüükäsuga, uuendatakse varud olemasoleva tegeliku kaalu sildi teabe alusel. Selle tulemusena ei viipa laorakendus hõivata tegeliku kaalu sildi andmeid tootmisaruande osa lõpetatud toiminguna.

**Kui tegeliku kaalu sildi jälgimist ei kasutata**, saab kaalu registreerida iga dimensioonikogumi kohta (nt iga litsentsiplaadi ja jälgimisdimensiooni kohta). Samuti on võimalik kaal registreerida koondtaseme, näiteks viie litsentsiplaadi (kaubaaluse), põhjal.

Väljamineva kaalu hõivamise meetodite puhul saate määrata suvandi **Tegeliku kaalu ühiku kohta** abil, et kaalumist tuleks teha iga tegeliku kaalu ühiku jaoks (nt karbi kohta). Valik **Komplekteerimisüksuse kohta** laseb teil määrata, et kaal tuleb hõivata vastavalt komplekteeritavale kogusele (nt kolm kasti). Pange tähele, et tootmisrea komplekteerimise ja siseliikumise protsesside puhul kasutatakse keskmist kaalu, kui kasutusel on suvand **Ei jäädvustata**.

Mitu kaalu hõivamise meetodit määratletakse tegeliku kaalu kauba käitlemise poliitikas. Iga kaalu hõivamise meetodi parameetrit kasutavad mitmed kanded. Järgmine tabel võtab kokku, milliseid parameetreid millised kanded kasutavad.

| Meetod                                     | Kanne                                |
|--------------------------------------------|--------------------------------------------|
| Väljamineva kaalu jäädvustamise meetod           | Müügi komplekteerimine, üleviimise komplekteerimine            |
| Tootmise komplekteerimise kaalu jäädvustamise meetod | Tootmiste komplekteerimine, Tootmise tarbimine |
| Muutuva kaalu jäädvustamise meetod           | Liikumine                                   |
| Millal jäädvustada kaalu parandamine       | Korrigeerimised, inventuur                      |
| Loenduskaalu jäädvustamise meetod           | Inventuur                                   |
| Lao ülekandekaalu jäädvustamise meetod | Edastus laos                         |

Selleks et laohalduse komplekteerimisprotsessid ei jäädvustaks kaale, mis annavad tulemuseks tegeliku kaalu kasumi/kahjumi korrigeerimised, saate kasutada väljamineva kaalu hälbe meetodit. Väljamineva kaalu hälbe meetodit rakendatakse järgmiste mobiilsete seadmete protsesside puhul: komplekteerimine, üleviimiseks komplekteerimine, tootmisse komplekteerimine, liikumised, inventuur ja lao üleviimised. Saate kasutada valikut **Piira kaalu hälvet**, kui tegeliku kaalu kauba kaal ei kõigu laos ladustamise ajal ja kui tegeliku kaalu kasumi/kahjumi korrigeerimisi ei nõuta. Saate kasutada valikut **Luba kaalu hälve**, kui kaal võib kõikuda ja kui tegeliku kaalu kasumi/kahjumi korrigeerimine on vajalik kaalu kõikumise kirjendamisel.

## <a name="unsupported-scenarios"></a>Ilma toeta stsenaariumid

Kõik töövood ei toeta tegeliku kaalu toote protsessi laohalduse abil. Praegu kehtivad järgmised piirangud. Need kehtivad kõigi tegeliku kaalu kaupade kohta, olenemata sellest, kas need on sildistatud.

### <a name="configuring-catch-weight-products-for-warehouse-management-processes"></a>Tegeliku kaalu toodete konfigureerimine laohalduseprotsesside puhul

- Tegeliku kaalu toodete puhul toetatakse ainult valemitöötlust (mitte kooslust).
- Tegeliku kaalu tooteid ei saa seostada jälgimisdimensiooni grupiga, kasutades omanikudimensiooni.
- Tegeliku kaalu tooteid ei saa kasutada teenustena.
- Tegeliku kaalu tooteid saab kasutada ladustatavate toodetena ainult kauba tootemudeligrupi osana.
- Tegeliku kaalu tooteid ei saa kasutada koos jälgimisfunktsiooniga Aktiivne müügiprotsessis.
- Tegeliku kaalu tooteid ei saa kasutada koos seerianumbrite registreerimise funktsiooniga. Seetõttu ei saa tooteid komplekteerimis-/pakkimisprotsessi osana kanda üle tühjalt väärtuselt seerianumbrile.
- Tegeliku kaalu tooteid ei saa kasutada koos enne tarbimist seerianumbrite registreerimise protsessiga.
- Tegeliku kaalu tooteid, millel on variandid lubatud, ei saa kasutada koos variandi mõõtühikute teisendamise funktsiooniga.
- Tegeliku kaaluga tooteid ei saa märgistada kaubandusliku "tootekomplektina".
- Tegeliku kaalu tooteid saab kasutada ainult ühiku seeriagrupiga, millel on tegeliku kaalu materjali käsitlemisühikud ja millel on madalaimaks seeriaks tegeliku kaalu ühik.
- Tegeliku kaalu toodete puhul saab laoühiku teisendada tegeliku kaalu ühikuks ainult siis, kui teisendamine annab tulemuseks nominaalkoguse, mis on suurem kui 1.
- Tegeliku kaalu toodete vöötkoodide seadistus ei toeta muutuva kaalu seadistamist.

### <a name="order-processing"></a>Tellimuse töötlemine

- Saadetise eelteatise (ASN/pakendistruktuurid) loomine ei toeta kaaluteavet.
- Tellimuse kogus tuleb säilitada tegeliku kaalu ühiku alusel.

### <a name="inbound-warehouse-processing"></a>Sissetulevad laoprotsessid

- Litsentsiplaatide vastuvõtmine nõuab registreerimise ajal kaalude määramist, kuna kaaluteavet ei toetata saadetise eelteatise osana. Tegeliku kaalu sildi protsesside kasutamisel tuleb sildi number määrata käsitsi iga tegeliku kaalu ühiku kohta.
- Sissetuleva kvaliteedikontrolli tööd ei toetata tegeliku kaalu toodete puhul. Kui see on konfigureeritud, jäetakse kontrollimine vahele.

### <a name="inventory-and-warehouse-operations"></a>Varude ja lao toimingud

- Tegeliku kaalu toodete puhul ei toetata karantiinitellimuste käsitsi loomist.
- Tegeliku kaalu toodete puhul ei toetata avatud tööga seotud varude käsitsi liigutamist.
- Tegeliku kaalu toodete puhul ei toetata litsentsiplaadi laadimist laoseisu lähtestamiseks.
- Tegeliku kaalu toodete puhul ei toetata partii tasakaalustamise protsesse.
- Tegeliku kaalu toodete puhul ei toetata negatiivsete füüsiliste varude käsitlemist.
- Tegeliku kaalu toodete puhul ei toetata varude märgistamist.

### <a name="outbound-warehouse-processing"></a>Väljaminevad laoprotsessid

- Tegeliku kaalu toodete puhul ei toetata funktsiooni klastri komplekteerimisel.
- Tegeliku kaalu toodete puhul ei toetata lao komplekteerimis- ja pakkimisprotsesse.
- Tegeliku kaaluga toodete puhul ei saa töömallis määratletud tööd automaatselt käitada.
- Tegeliku kaalu toodete puhul ei toeta süsteem käsitsi pakkimisjaamas töötlemist, kus pakitud konteineri komplekteerimistöö luuakse pärast konteinerite sulgemist.
- Tegeliku kaalu toodete puhul ei toetata tükikaupa skannimise funktsiooni.

### <a name="production-processing"></a>Tootmisprotsessid

- Tegeliku kaalu kaupade puhul toetatakse ainult valemitoodete partiitellimusi.
- Tegeliku kaalu toodete puhul ei toetata kanbani funktsiooni.
- Tegeliku kaalu toodete puhul ei saa seerianumbreid enne tarbimist registreerida.
- Tegeliku kaalu toodete puhul ei toetata litsentsiplaatide tootmisest tagasivõtmise funktsiooni.
- Tegeliku kaalu toodete puhul ei saa lõpetatuna kinnitamist registreerida seerianumbri järgi.

### <a name="transportation-management-processing"></a>Transpordihalduse protsessid

- Tegeliku kaalu toodete puhul ei toetata koorma koostamise töölaua protsesse.
- Tegeliku kaalu toodete puhul ei toetata transpordinõude ridu.

### <a name="other-restrictions-and-behaviors-for-catch-weight-product-processing-with-warehouse-management"></a>Muud piirangud ja käitumised tegeliku kaalu toodete protsesside puhul laohaldusega

- Komplekteerimisprotsesside puhul, kus kasutajal ei paluta jälgimisdimensioone tuvastada, toimub kaalu määramine keskmise kaalu põhjal. See käitumine ilmneb näiteks siis, kui samas asukohas kasutatakse jälgimisdimensioonide kombinatsiooni ja pärast seda, kui kasutaja on komplekteerimisprotsessi lõpule viinud, jääb asukohta alles ainult üks jälgimisdimensioon.
- Kui varud reserveeritakse tegeliku kaalu tootele, mis on konfigureeritud laohaldusprotsesside jaoks, toimub reserveerimine määratletud minimaalse kaalu põhjal, isegi kui kogus on viimane laos olev käsitlemiskogus. See käitumine erineb käitumisest kaupade puhul, mis ei ole laohaldusprotsesside jaoks konfigureeritud. Sellele piirangule on üks erand. Tootmisse komplekteerimiseks, kui komplekteeritakse tegeliku kaalu toote viimase käitlemise kogus, mille seerianumber on kontrollitud, kasutatakse tegeliku kaalu.
- Protsessid, mis kasutavad kaalu võimsuse arvutuste osana (vooläved, maksimaalsed tööjaotused, konteineri maksimumväärtused, asukoha koormavõimsused jne), ei kasuta varude tegelikku kaalu. Selle asemel põhinevad protsessid toote jaoks määratletud füüsilisel käsitlemiskaalul.
- Üldiselt ei toetata tegeliku kaalu toodete puhul Commerce'i funktsionaalsust.
- Tegeliku kaalu toodete puhul ei saa varude olekut värskendada **Lao oleku muudatusest**.

### <a name="catch-weight-tags"></a>Tegeliku kaalu sildid

Tegeliku kaalu sildi saab luua kas laorakenduse protsessiga, see võidakse vormil käsitsi luua, või saab seda luua andmeüksuse protsessiga. Kui tegeliku kaalu silt seostatakse sissetuleva lähtedokumendi reaga, näiteks ostutellimuse reaga, siis silt registreeritakse. Kui väljamineva töötlemise juures kasutatakse rida, värskendatakse silt lähetatud olekusse.

Lisaks piirangutele, mis praegu kehtivad tegeliku kaalu toodete puhul, on sildistatud tegeliku kaalu toodetel muud praegu kehtivad piirangud.

- Kõik varude käsitsi uuendused (st uuendused, mida ei ole mobiilse seadme abil tehtud) peavad sisaldama vastavaid tegeliku kaalu siltidega seotud käsitsi värskendusi, kuna neid värskendusi ei tehta automaatselt. Näiteks värskendavad käsitsi korrigeerimise töölehed varusid aga mitte nendega seotud tegeliku kaalu silte.
- Peate tegeliku kaalu sildid käsitsi värskendama, et need kajastaksid täiendamistöö liikumisi. Seda seetõttu, et süsteem ei suuda täiendamistöö töötlemise käigus kaalusid hõivata ja seega registreerib selle asemel keskmise kaalu.
- Kombineeritud litsentsiplaadi vastuvõtmist hetkel sildistatud tegeliku kaalu toodete juures ei toetata.
- Müügi tagastustellimuse vastuvõtmise töötlemine võib tegeliku kaalu sildid registreerida. Kuid protsess ei valideeri, et tagastatud silt on sama silt, mis algselt müügitellimusega lähetati.
- Mobiilse seadme menüükäsk, millel on toimingu kood **Materjali tarbimise registreerimine**, ei toeta praegu tegeliku kaalu siltide salvestamist.
- Ehkki inventuuri protsesse sildistatud tegeliku kaalu kaupade puhul toetatakse, on need piiratud. Näiteks saate kasutada mobiilse seadme suvandeid sildistatud tegeliku kaalu kaupade loendamiseks ja kasutatakse keskmist kaalu. Kuid tegeliku kaalu silte ei värskendata inventuuri kandega automaatselt. Pärast inventuuri kande lõpetamist tuleb tegeliku kaalu silte käsitsi värskendada, et need varusid kajastaksid. Kui kaubad, mida ei olnud algselt asukohas, loendatakse sellesse asukohta, kasutatakse nominaalkaalu.
- Litsentsiplaadi konsolideerimine ei toeta praegu sildistatud tegeliku kaaluga tooteid.
- Tühistatud töö funktsionaalsust ei toetata nende tegeliku kaalu kaupade puhul, mida jälgitakse sildi numbri järgi.

> [!NOTE]
> Tegeliku kaalu siltide eelnev teave kehtib ainult siis, kui tegeliku kaalu tootel on tegeliku kaalu sildi dimensiooni jälgimise meetod, mis on täielikult jälgitav (st kui **Tegeliku kaalu sildi dimensiooni jälgimise meetodi** parameeter tegeliku kaalu kauba käitlemise poliitikas on seatud olekusse **Tootedimensioonid, jälgimise dimensioonid ja laoala dimensioonid**). Kui tegeliku kaalu üksus on ainult osaliselt sildiga jälitatud (st kui **Tegeliku kaalu sildi dimensiooni jälgimise meetodi** parameeter tegeliku kaalu kauba käsitsemise poliitikas on seatud olekusse **Tootedimensioonid, Jälgimise dimensioonid ja Varude olek**), rakenduvad täiendavad piirangud. Kuna sildi ja varude vaheline nähtavus on sel juhul kadunud, ei toetata mõnda lisastsenaariumit.
