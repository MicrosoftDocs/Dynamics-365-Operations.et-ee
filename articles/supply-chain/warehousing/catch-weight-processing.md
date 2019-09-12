---
title: Tegeliku kaalu toote protsess laohalduse abil
description: Selles teemas kirjeldatakse, kuidas kasutada töömalle ja asukohakorraldusi määramaks, kuidas ja kus laos tööd tehakse.
author: perlynne
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCatchWeightTag, WHSCatchWeightItemHandlingPolicy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-1-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: d5e9f8e4d154e5f56ee7ceae666cd935d6ceb460
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887131"
---
# <a name="catch-weight-product-processing-with-warehouse-management"></a>Tegeliku kaalu toote protsess laohalduse abil

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/pivate-preview-banner.md)]


## <a name="feature-exposure"></a>Funktsiooni esiletõstmine

Laohalduse abil tegeliku kaaluga toodete haldamiseks peate selle funktsiooni litsentsi konfiguratsioonivõtme abil sisse lülitama. (Valige suvandid **Süsteemihaldus \> Seadistamine \> Litsentsi konfiguratsioon**. Seejärel laiendage vahekaardil **Konfiguratsioonivõtmed** jaotist **Kaubandus \> Lao- ja transpordihaldus** ja märkige ruut **Tegelik kaal lao jaoks**).

> [!NOTE]
> Sisse peab lülitama ka litsentsi konfiguratsioonivõtmed **Lao- ja transpordihaldus** ning **Protsessi jaotus \> Tegelik kaal**.

Kui litsentsi konfiguratsioonivõti on sisse lülitatud ja loote väljastatud toote, saate valida suvandi **Tegelik kaal**. Samuti saate seostada väljastatud toote laoala dimensiooni rühmaga, mille puhul on valitud parameeter **Kasuta laohalduse protsesse**.

Enne toote kasutamist laohalduses peate tegema tootekohase põhiseadistuse tegeliku kaalu kohta.

- Määratlege ühikuteisenduse määratluse osana nominaalse kaalu teisendamine tegeliku kaalu ühiku (karp) ja laoühiku (kilogramm \[kg\]) vahel.
- Määratlege tegeliku kaalu ühiku seadistuse osana minimaalne ja maksimaalne kaaluhälve.
- Seadistage ühiku seeriagrupp, milles tegeliku kaalu ühik on määratletud madalaima varude arvestusühikuna (SKU).
- Seadistage tegeliku kaalu kauba käitlemispoliitika.

Lisateabe saamiseks vt jaotist [Tegeliku kaalu kaupade seadistamine ja haldamine](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items).

## <a name="transaction-adjustments"></a>Kande korrigeerimised

Kuna lattu saabuvate varude kaal võib erineda laost väljastatavate varude kaalust, peab tegeliku kaalu toote protsess varusid korrigeerima.

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

Kui tegelik kaal registreeritakse pakkimisjaamas konteineri pakkimisprotsesside ajal, ei paluta laotöötajatel kaalu komplekteerimistöö ajal registreerida. Selle asemel kasutatakse pakkimisalale minevate komplekteeritud varude kaaluna füüsiliste varude keskmist kaalu.

Sisemiste laohaldusprotsesside, nagu inventuur ja korrigeerimisparandused, puhul on võimalik määratleda, kas kaal tuleb registreerida või mitte. Kui seda ei registreerita, kasutatakse nominaalset kaalu.

Saate ka määratleda kaalu registreerimise viisi. Ühes kahest põhivoost jälgitakse ja kasutatakse kaalu registreerimiseks tegeliku kaalu silte. Teises voos tegeliku kaalu silte ei jälgita.

- **Jah** – kaup kasutab tegeliku kaalu silte. Iga sildi number tähistab üht tegeliku kaalu ühikut (kast) ning kaal ja muu teave seostatakse sildiga. Väljaminevate protsesside puhul kasutatakse sildiga seotud kaalu.
- **Ei** – kaup ei kasuta tegeliku kaalu silte. Sissetulevad ja väljaminevad kaalumisprotsessid põhinevad tegelikul kaalul, mis registreeritakse iga protsessi käigus.

Tegeliku kaalu siltide jälgimise protsessi saab kasutada kaupade jälgimiseks, mille kaal ladustamisperioodi jooksul ei muutu. Kaal registreeritakse ainult sissetuleva laoprotsessi käigus. Väljamineva protsessi käigus tegeliku kaalu sildid lihtsalt skannitakse ja väljaminevate kannete töötlemisel kasutatakse siltidega seostatud kaale.

### <a name="how-to-capture-catch-weight"></a>Tegeliku kaalu registreerimine

Tegeliku kaalu sildi jälgimise kasutamisel tuleb silt alati luua iga sissetuleva tegeliku kaalu ühiku jaoks ja iga silt tuleb alati seostada kaaluga.

Näiteks on tegeliku kaalu ühik **kast** ja te saate ühe kaubaaluse kaheksa kastiga. Sel juhul tuleb luua kaheksa kordumatut tegeliku kaalu silti ja kaal tuleb seostada iga sildiga. Olenevalt sissetuleva tegeliku kaalu sildist saab registreerida kas kõigi kaheksa kasti kaalu ja jaotada igale kastile keskmise kaalu või registreerida iga kasti jaoks kordumatu kaalu.

Kui tegeliku kaalu sildi jälgimist ei kasutata, saab kaalu registreerida iga dimensioonikogumi kohta (nt iga litsentsiplaadi ja jälgimisdimensiooni kohta). Samuti on võimalik kaal registreerida koondtaseme, näiteks viie litsentsiplaadi (kaubaaluse), põhjal.

Väljamineva kaalu registreerimisviisidena saate määratleda, kas kaalumine toimub iga tegeliku kaalu ühiku (st kasti) kohta või registreeritakse kaal komplekteeritava koguse (nt kolm kasti) põhjal. Pange tähele, et tootmisrea komplekteerimise ja siseliikumise protsesside puhul kasutatakse keskmist kaalu, kui kasutusel on suvand **Ei jäädvustata**.

Selleks et laohalduse komplekteerimisprotsessid ei jäädvustaks kaale, mis annavad tulemuseks tegeliku kaalu kasumi/kahjumi korrigeerimised, saab kasutada väljamineva kaalu hälbe meetodit.

## <a name="supported-scenarios"></a>Toetatud stsenaariumid

Kõik töövood ei toeta tegeliku kaalu toote protsessi laohalduse abil. Praegu kehtivad järgmised piirangud.
 
### <a name="configuring-catch-weight-products-for-warehouse-management-processes"></a>Tegeliku kaalu toodete konfigureerimine laohalduseprotsesside puhul

- Tegeliku kaalu toodete puhul ei saa laoala dimensioonigruppi kaupade puhul muuta (nii et nende puhul saab kasutada laohaldusprotsesse).
- Tegeliku kaalu toodete puhul toetatakse ainult valemitöötlust (mitte kooslust).
- Tegeliku kaalu tooteid ei saa seostada jälgimisdimensiooni grupiga, kasutades omanikudimensiooni.
- Tegeliku kaalu tooteid ei saa kasutada teenustena.
- Tegeliku kaalu tooteid saab kasutada ladustatavate toodetena ainult kauba tootemudeligrupi osana.
- Tegeliku kaalu tooteid ei saa kasutada koos jälgimisfunktsiooniga Aktiivne müügiprotsessis.
- Tegeliku kaalu tooteid ei saa kasutada koos seerianumbrite registreerimise funktsiooniga. Seetõttu ei saa tooteid komplekteerimis-/pakkimisprotsessi osana kanda üle tühjalt väärtuselt seerianumbrile.
- Tegeliku kaalu tooteid ei saa kasutada koos enne tarbimist seerianumbrite registreerimise protsessiga.
- Tegeliku kaalu tooteid, millel on variandid lubatud, ei saa kasutada koos variandi mõõtühikute teisendamise funktsiooniga.
- Tegeliku kaaluga tooteid ei saa märgistada jaemüügi tootekogumina.
- Tegeliku kaalu tooteid saab kasutada ainult ühiku seeriagrupiga, millel on tegeliku kaalu materjali käsitlemisühikud ja millel on madalaimaks seeriaks tegeliku kaalu ühik.
- Tegeliku kaalu toodete puhul saab laoühiku teisendada tegeliku kaalu ühikuks ainult siis, kui teisendamine annab tulemuseks nominaalkoguse, mis on suurem kui 1.
- Tegeliku kaalu toodete vöötkoodide seadistus ei toeta muutuva kaalu seadistamist.
 
### <a name="order-processing"></a>Tellimuse töötlemine

- Saadetise eelteatise (ASN/pakendistruktuurid) loomine ei toeta kaaluteavet.
- Tellimuse kogus tuleb säilitada tegeliku kaalu ühiku alusel.
 
### <a name="inbound-warehouse-processing"></a>Sissetulevad laoprotsessid

- Litsentsiplaatide vastuvõtmine nõuab registreerimise ajal kaalude määramist, kuna kaaluteavet ei toetata saadetise eelteatise osana. Tegeliku kaalu sildi protsesside kasutamisel tuleb sildi number määrata käsitsi iga tegeliku kaalu ühiku kohta.
 
### <a name="inventory-and-warehouse-operations"></a>Varude ja lao toimingud

- Tegeliku kaalu toodete puhul ei toetata karantiinitellimuste käsitsi loomist.
- Tegeliku kaalu toodete puhul ei toetata tööga seotud varude käsitsi liigutamist.
- Tegeliku kaalu toodete puhul ei toetata litsentsiplaadi laadimist laoseisu lähtestamiseks.
- Tegeliku kaalu toodete puhul ei toetata partii tasakaalustamise protsesse.
- Tegeliku kaalu toodete puhul ei toetata negatiivsete füüsiliste varude käsitlemist.
- Tegeliku kaalu toodete puhul ei toetata varude märgistamist.
 
### <a name="outbound-warehouse-processing"></a>Väljaminevad laoprotsessid

- Tegeliku kaalu toodete puhul ei toetata funktsiooni klastri komplekteerimisel.
- Tegeliku kaalu toodete puhul ei toetata lao komplekteerimis- ja pakkimisprotsesse.
- Tegeliku kaalu toodete puhul saab töömallis määratletud tööd automaatselt käitada.
- Tegeliku kaalu toodete puhul ei toetata käsitsi pakkimisjaama protsessi, kus töö luuakse pärast konteinerite sulgemist.
- Tegeliku kaalu toodete puhul ei toetata tükikaupa skannimise funktsiooni.
 
### <a name="production-processing"></a>Tootmisprotsessid

- Tegeliku kaalu kaupade puhul toetatakse ainult valemitoodete partiitellimusi.
- Tegeliku kaalu toodete puhul ei toetata kanbani funktsiooni.
- Tegeliku kaalu toodete puhul ei saa seerianumbreid enne tarbimist registreerida.
- Tegeliku kaalu toodete puhul ei toetata litsentsiplaatide tagasivõtmise funktsiooni.
- Tegeliku kaalu toodete puhul ei saa lõpetatuna kinnitamist registreerida seerianumbri järgi.

### <a name="transportation-management-processing"></a>Transpordihalduse protsessid

- Tegeliku kaalu toodete puhul ei toetata koorma koostamise töölaua protsesse.
- Tegeliku kaalu toodete puhul ei toetata transpordinõude ridu.
 
### <a name="other-restrictions-and-behaviors-for-catch-weight-product-processing-with-warehouse-management"></a>Muud piirangud ja käitumised tegeliku kaalu toodete protsesside puhul laohaldusega

- Komplekteerimisprotsesside puhul, kus kasutajal ei paluta jälgimisdimensioone tuvastada, toimub kaalu määramine keskmise kaalu põhjal. See käitumine ilmneb näiteks siis, kui samas asukohas kasutatakse jälgimisdimensioonide kombinatsiooni ja pärast seda, kui kasutaja on komplekteerimisprotsessi lõpule viinud, jääb asukohta alles ainult üks jälgimisdimensioon.
- Kui varud reserveeritakse tegeliku kaalu tootele, mis on konfigureeritud laohaldusprotsesside jaoks, toimub reserveerimine määratletud minimaalse kaalu põhjal, isegi kui kogus on viimane laos olev käsitlemiskogus. See käitumine erineb käitumisest kaupade puhul, mis ei ole laohaldusprotsesside jaoks konfigureeritud.
- Protsessid, mis kasutavad kaalu võimsuse arvutuste osana (vooläved, maksimaalsed tööjaotused, konteineri maksimumväärtused, asukoha koormavõimsused jne), ei kasuta varude tegelikku kaalu. Selle asemel põhinevad protsessid toote jaoks määratletud füüsilisel käsitlemiskaalul.
- Üldiselt ei toetata tegeliku kaalu toodete puhul Retaili funktsiooni.
 
### <a name="catch-weight-tags"></a>Tegeliku kaalu sildid

Praegu toetatakse tegeliku kaalu siltide funktsiooni ainult järgmiste stsenaariumide osana.

- Laorakenduses vastuvõetava ostutellimuse töötlemisel.
- Laorakenduse kaudu koorma töötlemisel.
- Kui ostutellimuse koormaga seotud litsentsiplaadi vastuvõtmisel taotletakse vastuvõtmisprotsessi käigus kaalu määramist. Seevastu üleviimistellimuse vastuvõtmisel kasutatakse üleviimistellimuse saadetise andmetes näidatud kaalu.
- Üleviimistellimuse kauba ja rea vastuvõtmisel, mis tuleb mittelaohalduse protsessi laost.
- Müügi tagastustellimuse vastuvõtmise protsess saab kirjendada tegeliku kaalu sildid, kuid protsessi ei valideerita, kui sildid on samad, mis saadeti konkreetse müügitellimuse rea puhul.
- Laorakenduse abil muudetud varude oleku töötlemisel.
- Laohaldusrakenduse abil lao üleviimise toimingul.
- Laorakenduse kaudu sisse ja välja korrigeerimise töötlemisel.
- Müügi- ja üleviimistellimuste puhul komplekteerimistöö töötlemisel. (Pange tähele, et tegeliku kaalu silte ei saa salvestada tootmiskomponendi komplekteerimiseks.)
- Komplekteeritud koguste vähendamisel koorma ridadelt olenemata sellest, kas konteinereid kasutatakse või mitte.
- Toodete pakkimisel konteineritesse pakkimisjaamas.
- Konteinerite uuesti avamisel.
- Laorakenduse abil valemitoodete lõpetatuna kinnitamisel.
- Laorakenduse abil transpordikoormate töötlemisel.

Tegeliku kaalu sildi saab luua kas laorakenduse protsessiga, vormil käsitsi või andmeüksuse protsessiga. Kui tegeliku kaalu silt seostatakse sissetuleva lähtedokumendi reaga, näiteks ostutellimuse reaga, siis silt registreeritakse. Kui rida kasutatakse väljaminevaks töötlemiseks. Silt värskendatakse olekule Saadetud.
