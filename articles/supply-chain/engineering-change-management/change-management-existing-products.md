---
title: Luba olemasolevate toodete muudatuste haldamine
description: See artikkel selgitab, kuidas lubada olemasolevate toodete muudatusehaldust. Selles kirjeldatakse ka juhtumeid, kus teie võime muudatusehaldust lubada on piiratud.
author: t-benebo
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-05-02
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 9f99529abebdf5490f158c6f0a7be4519449e9f0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893464"
---
# <a name="enable-change-management-on-existing-products"></a>Luba olemasolevate toodete muudatuste haldamine

[!include [banner](../../includes/banner.md)]

See artikkel selgitab, kuidas lubada olemasolevate toodete muudatusehaldust. Selles kirjeldatakse ka juhtumeid, kus teie võime muudatusehaldust lubada on piiratud.

Kui lubate olemasoleva toote muudatusehalduse, saate luua selle toote versioone ja jälgida muudatusi, mis tehakse selle kogu eluea jooksul. Seetõttu saate neid muudatusi jälgida muudatustellimuste abil. Muudatusehalduse lubamiseks peate teisendama vastavad tooted *tehnilisteks kaupadeks* (nimetatakse ka tehnilisteks toodeteks). Tehnilised tooted on tooted, mis on versioonitud ja mida hallatakse muudatusehalduse kaudu. Teisendusprotsessi juhendamiseks on ette nähtud viisard.

## <a name="turn-this-feature-on-or-off"></a>Selle funktsiooni sisse- või väljalülitamine

Selles artiklis kirjeldatud funktsioonid nõuavad, et nii *Tehnika muutmise haldus* *kui ka luba olemasolevate toodete* funktsioonide muudatusehaldus lülitatakse teie süsteemi jaoks sisse. Üksikasju selle kohta, kuidas neid funktsioone sisse või välja lülitada, vt tehnika [muudatusehalduse ülevaadet](product-engineering-overview.md).

## <a name="restrictions-and-limitations"></a>Piirangud

Kõiki tootetüüpe ei saa kõigiks muudeks tüüpideks teisendada. Kehtivad järgmised piirangud:

- Toote teisendamisel tehniliseks tooteks jääb see *tooteks*. See ei muutu *tooteetaloniks*.
- Kindla dimensioonikogumiga tooteetaloni teisendamisel säilitatakse need dimensioonid pärast muudatust. Näiteks kui teisendate suurusedimensiooniga tooteetaloni, jääb see suurusedimensioon alles.

Seega, kui teil on eristatav toode, saate seda muuta ainult tehniliseks tooteks, mis ei jälgi kannete tootedimensiooni (st versioonidimensiooni ei kasutata). Lisateabe saamiseks nende probleemide kohta vaadake selle artikli ülejäänud jaotisi.

## <a name="prepare-for-conversion-by-creating-all-required-engineering-product-categories"></a>Valmistuge teisendamiseks, luues kõik nõutud tehnilise toote kategooriad

Igale tehnilisele tootele tuleb määrata *tehnilise toote kategooria*. See määramine tuleb teha viisardi **Teisenda tehniliseks tooteks** käitamisel. Tehnilise toote kategooriad peavad *enne* nende toodete teisendamist olemas olema kõigi asjakohaste standardtoodete puhul.

Tehnilise toote kategooria annab aluse tehnilise toote loomiseks ning see loob vaikeväärtuste ja -poliitikate komplekti. Tehnika atribuute ja nende vaikeväärtusi (nagu on määratletud tehnika kategoorias) rakendatakse ka tulenevale tehnikatootele. Saate redigeerida atribuudiväärtusi ja/või lisada tulemuseks saadud tootele vajaduse korral rohkem tehnika atribuute.

Tehnilise toote kategooria peab vastama tootele, millele te selle määrate. Näiteks tootetüüp ja dimensioonigrupp peavad vastama nii tootele kui ka selle tehnilise toote kategooriale. Lisateavet vt teemast [Tehnilised versioonid ja tehniliste toodete kategooriad](engineering-versions-product-category.md).

> [!IMPORTANT]
> Viisard **Teisenda tehniliseks tooteks** saab teisendada toote ainult tehnilisteks toodeteks, mille puhul versiooni kannetes ei jälgita. Seepärast tuleb suvandi **Jälgi kannete versiooni** väärtuseks olemasolevate toodete teisendamiseks loodavate tehnilise toote kategooriate puhul seada *Ei*.

Teavet tehniliste toodete kategooriate loomise kohta leiate teemast [Tehnilised versioonid ja tehniliste toodete kategooriad](engineering-versions-product-category.md).

## <a name="run-the-convert-to-engineering-product-wizard"></a>Tehnilise toote teisendamise viisardi käitamine

Viisard **Teisenda tehniliseks tooteks** aitab teisendada ühe või mitu olemasolevat toodet tehnilisteks toodeteks. See teisendab tooted tehnilisteks toodeteks (versioonitud toodeteks), mille puhul versiooni kannetes ei jälgita (st versioonidimensiooni ei kasutata). Pärast teisendamise lõpuleviimist saate tooteid hallata tehnilise muudatuse halduse abil.

Teisendus on jääv. Seetõttu ei saa te seda hiljem tagasi pöörata. 

Iga teisendatud tehnilist toodet väljastatakse jätkuvalt välja samadest ettevõtetest, kust algne toode väljastati. Siiski ei väljastata tehnilist kooslust (BOM) ja marsruute automaatselt nendele ettevõtetele.

Järgige neid samme, et käivitada viisard **Teisenda tehniliseks tooteks** ja teisendada toode tehniliseks tooteks.

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Valige ruudustikus märkeruut iga toote puhul, mille soovite teisendada.
1. Valige toimingupaanil vahekaardil **Projekteerimine** grupis **Tehnilise muudatuse haldamine** suvand **Teisenda tehniliseks tooteks**, et avada viisard.
1. Viisardi esimene lehekülg on leht **Tere tulemast**. Kui te ei ole veel teisendusprotsessiga tutvunud, lugege hoolikalt läbi sellel lehel esitatud teave. Kui olete jätkamiseks valmis, valige **Järgmine**.
1. Lehel **Valige teisendatavate toodete üksikasjad** kuvatakse iga toode, mille valisite enne viisardi avamist. Kontrollige loendit. Kasutage tööriistaribal asuvaid nuppu **Uus** ja **Kustuta**, et lisada ja eemaldada tooteid vastavalt vajadusele.
1. Kasutage ruudustiku ülaosas järgmisi välju vaikeväärtuste määramiseks igale loendis loetletud tootele. (Neid väärtusi saate üksikute toodete puhul pärast teisenduse lõpuleviimist muuta.) Vaikeväärtusi ei määrata toodetele, millele on vastav väärtus juba määratud.

    - **Vaikimisi tehniline kategooria** – valige igale loetletud tootele määramiseks algne tehnilise toote kategooria. Teie valitud kategooria rakendatakse ainult sellega ühilduvatele toodetele.
    - **Vaikeversioon** – sisestage igale loetletud tootele määratav algne tooteversioon. Igal tehnilisel tootel on vähemalt üks tehniline versioon.
    - **Vaikimisi töötsükli olek** – valige igale loetletud tootele määratav algne toote töötsükli olek.
    - **Praegune kooslus on tehnilise toote osa** – märkige see ruut, kui iga loetletud toote praegust kooslust tuleks kasutada tehnilise toote kooslusena.

    Lisateavet tootesätete kohta leiate järgmisest etapist.

1. Vaadake üle kõik ruudustikus loetletud tooted ja hinnake, kui hästi teie määratud vaikeväärtused neile kohalduvad. Vaadake iga rea puhul üle järgmine teave ja määrake kõik asjakohased väljad:

    - **Toote number** – toote number.
    - **Toote nimi** – toote nimi.
    - **Tehniline kategooria** – valige tehnilise toote kategooria, kuhu toode peaks pärast teisendamist kuuluma. Igal tootel peab juba olema vastav kategooria, nagu on kirjeldatud selle artikli eelmises jaotises. Kategooria tuleb määrata igale tootele.
    - **Versioon** – sisestage igale loetletud tootele pärast teisendamist määratav tooteversioon. Näiteks võite valida numbri, mis sobib teie kategooria juba kasutatud numbriseeriasse. Igas tehnilises versioonis talletatakse tehnilisi asjakohaseid andmeid, mis on selle versiooniga seotud. Lisateavet vt teemast [Tehnilised versioonid ja tehniliste toodete kategooriad](engineering-versions-product-category.md).
    - **Toote töötsükli olek** – valige toote töötsükli olek, mis peaks tootel pärast teisendamist olema. Toote töötsükli olek võimaldab teil juhtida, millised kanded on antud tehnilise versiooni puhul lubatud. Lisateavet vt jaotisest [Toote töötsükli olekud ja kanded](product-lifecycle-state-transactions.md).
    - **Kooslusega** – valitud märkeruut näitab, et tootel on kooslus. Selle märkeruudu määramine aitab teil otsustada, kuidas määrata märkeruut **Praegune kooslus on tehnilise toote osa**.
    - **Praegune kooslus on tehnilise toote osa** – märkige see ruut, kui toote praegust kooslust tuleks kasutada tehnilise toote kooslusena. Seda kooslust haldab seejärel tehnilise muudatuse haldus. Kui tootel ei ole kooslust või eelistate teisendatud toote jaoks koosluse hiljem käsitsi luua, tühjendage see märkeruut.
    - **Sisaldab vigu** – valitud märkeruut näitab, et toote häälestuses on üks või mitu viga. Näiteks võib tootetüüp või dimensioonigrupp kategoorias mitte sobida. Vigadega tooted jäetakse vahele ja neid ei teisendata.

1. Kui olete lõpetanud, valige tootehäälestuse valideerimiseks tööriistaribal käsk **Valideeri**. Iga rea puhul uuendatakse märkeruutu **Sisaldab vigu**, et näidata toote olekut. Korrigeerige väärtusi, kuni iga toote häälestus on veatu.
1. Kui kõik tooted on õigesti häälestatud, valige jätkamiseks **Järgmine**.
1. Lehel **Kinnita valik** kuvatakse nende toodete arv, mille häälestuses pole vigu ja mis on seetõttu teisendamiseks valmis. Samuti kuvatakse seal vigade tõttu vahelejäetud toodete arv. Teisenduse käivitamiseks pakett-tööna seadke suvandi **Käivita pakett-tööna** väärtuseks *Jah*.
1. Valige sätete rakendamiseks **Vii lõpule** ja käivitage toodete teisendamine tehnilisteks toodeteks.

> [!NOTE]
> Kui teie süsteem on häälestatud toodete käsitsi aktseteerimiseks enne nende väljastamist, peate iga teisendatud toote aktsepteerima, kasutades vastava ettevõtte lehte **Avatud tooteväljastused**. Lisateavet vt teemast [Toote ülevaatamine ja heakskiitmine enne kohalikule ettevõttele väljastamist](engineering-scenarios.md#accept).
