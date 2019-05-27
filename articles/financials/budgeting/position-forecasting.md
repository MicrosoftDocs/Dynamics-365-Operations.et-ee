---
title: Ametikoha prognoosimine
description: Töötajatega seotud kulud moodustavad tihti suure osa organisatsiooni kuludest. Ametikoha prognoosimine võimaldab teil neid kulusid planeerida ja kaasata need eelaarvete planeerimisse.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPositionForecast
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 64413
ms.assetid: 35e791d2-1905-4808-a579-7f181ddddd91
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bcd7363ba50f1c3a20d9823333df65eab9868d67
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553710"
---
# <a name="position-forecasting"></a>Ametikoha prognoosimine

[!include [banner](../includes/banner.md)]

Töötajatega seotud kulud moodustavad tihti suure osa organisatsiooni kuludest. Ametikoha prognoosimine võimaldab teil neid kulusid planeerida ja kaasata need eelaarvete planeerimisse.

## <a name="position-forecasting-in-budget-planning"></a>Ametikoha prognoosimine eelarve planeerimisel

[![Graafiku ülaosa](./media/graphic-top.png)](./media/graphic-top.png) 

Ametikoha prognoosimine kasutab kolme põhikomponenti, et anda ametikoha kulude kohta täpsed eelarvesummad. Need summad saab siis tuua eelarveplaani eelarve arvutamiseks. 

Esmane komponent on **prognoositav ametikoht**, mis esindab kõiki ühe ametikohaga seotud kuluandmeid. Saate luua prognoositavast ametikohast mitu versiooni, määrates igale versioonile erinva eelarveplaani stsenaariumi. Mitu versiooni võimaldavad eelarve koostamisele iteratiivselt läheneda ja teil võimalikke stsenaariume võrrelda. Igal prognoositaval ametikohal on inimressurssides vastav positsioon.

**Eelarve kuluelement** on häälestuskomponent, mis esindab konkreetset kulu, mis on ametikohaga seostatud, näiteks põhipalk, tööandja makstud tervisekindlustus, mobiiltelefoni kasutamise kulud jne. Eelarve kuluelement sisaldab põhikontot, mida kasutatakse kulude puhul, ja arvutamissuvandeid. Iga eelarve kuluelemendi saab määrata mitmele prognoositavale ametikohale. 

**Hüvitusgrupp** on valikuline häälestuskomponent, mida kasutatakse eelarve kuluelementide kogumi rakendamiseks ja tasu arvutamiseks sarnaste tasu näitajatega ametikohtade puhul. Hüvitusgrupp võib hõlmata tasumäärade hüvitusruudustikku. Kui grupp määratakse prognoositavale ametikohale, võib ruudustiku tase ja etapp määrata prognoositava ametikoha töötasu. Kuluelementide kogum lisatakse automaatselt.

### <a name="position-forecasting-processes"></a>Ametikoha prognoosimise protsessid

[![graphic1b](./media/graphic1b.png)](./media/graphic1b.png) 

Tavapärase ametikoha prognoosimise protsessis loote esmalt häälestuskomponendid (eelarve kuluelemendid ja hüvitusgrupid). Seejärel luuakse olemasolevate ametikohtade alusel prognoositavad ametikohad. Seejärel saate korrigeerida. Näiteks saate ametikohti lisada või lõpetada, muuta tasumäärasid ja soodustusi ning lisada palgatõuse. Saate luua prognoositavast ametikohast mitu versiooni, et lihtsustada erinevate eelarve koostamise stsenaariumide võrdlemist. Seejärel saate lisada prognoositavad ametikohad eelarveplaanidesse ja tuua sisse prognoostavate ametikohtade kulud eelarveplaani ridadena.

Eelarveplaanide läbivaatusel saate luua täiendavaid prognoositava ametikoha versioone. Uued versioonid on paranduste aluseks.

## <a name="position-forecasting-setup"></a>Ametikoha prognoosimise häälestamine
[![graphic2](./media/graphic2-1024x327.png)](./media/graphic2.png)

### <a name="budget-cost-elements"></a>Eelarve kuluelemendid

Eelarve kuluelemente kasutatakse prognoostava ametikoha kuluüksikasjade määratlemiseks. Üksikasjad hõlmavad kulu tüüpi, kulu arvutamise viisi ja seda, kas kulu on eraldatud mitmele kuupäevale, kui prognoositav ametikoht on kaasatud eelarveplaani. 

Kindlad väljad määratlevad eelarve kuluelemendi käitumise. Igale eelarve kuluelemendile määatakse eelarve kulu tüüp **Tulu**, **Soodustus**, **Maksud** või **Muu**. Eelarve kulu tüüpe kasutatakse peamisel kogusummade arvutamiseks. Väärtus **Prognoositava ametikoha alistamine** määrab, kas elemendi summasid saab prognoositaval ametikohal muuta. Välja **Eraldamismeetod** kasutatakse, kui prognoositav ametikoht lisatakse eelarveplaani. Saate jaotada kulu summa eelarveplaani eraldi ridadele, millel on erinevad kuupäevad, kuu, kvartali, nädala või poole nädala alusel. Alguskuupäeva valides määrate kulu ühe summana prognoositavale ametikohale määratud alguskuupäevale. 

Eelarve kuluelemendi kulu summa arvutamine kasutab jõustumiskuupäevi, et võimaldada sama kuluelemendi kasutamist erinevatel perioodidel. Üks põhikonto määratakse igal perioodil koos protsendi või iga-aastase summaga, mis näitab kulu summat. Eelarve kuluelement saab kasutada muude kuluelementide või iga-aastase summa protsenti, kuid mitte mõlemat. Saate määrata ka aastalimiidi. 

Kui kuluelement põhineb protsendil, peate määrama eelarve kuluelemendid, mida kasutatakse arvutuse alusena.

**Näide** 

Jodi organisatsioon pakub koolitushüvitist, mis on 5% töötaja põhipalgast. Jodi soovib luua selle kulu kohta eelarve kuluelementi. Ta loob uue eelarve kuluelemendi ja määrab eelarve kulu tüübiks **Soodustus**.

Jodi ei soovi, et haldurid soodustuse summat muudaksid. Seetõttu valib ta suvandi **Ära luba kulu muuta** väljal **Prognoositava ametikoha alistamine**. Organisatsioon soovib, et seda kulu määrataks iga kuu kohta võrdselt. Seetõttu valib Jodi suvandi **Kord kvartalis** väljal **Eraldamismeetod**. 

järgmisena lisab Jodi kulu arvutamise rea, määrab kuupäevad ja põhikonto ning sisestab protsendiks **5,00**. Tema organisatsioonil on selle soodustuse jaoks aastas 5000 USA dollarit katet. Seetõttu sisestab Jodi selle summa aastalimiidiks. 

Lõpuks lisab Jodi kõik tulu kuluelemendid, mida kasutatakse põhipalga puhul arvutamise alusena. Tema eelarve kuluelement on nüüd kasutamiseks valmis.

### <a name="compensation-groups"></a>Hüvitusgrupid

Hüvitusgruppe saab kasutada sarnaste hüvitusatribuutidega prognoositavate ametikohtade rühmitamiseks. Neid saab kasutada ka prognoositava ametikoha tulu ja iga-aastase tõusu määratlemiseks ning tavapäraste eelarve kuluelementide määramiseks. 

Hüvitusgruppide põhifunktsioon on prognoositavale ametikohale eelarve kuluelementide kogumi määramine. Seetõttu saab hüvitusgruppe kasutada üldkulude, nagu soodustusplaanid ja maksud, lisamiseks. Prognoositavat ametikohta loov juht ei pea teadma kõiki lisatavaid kuluelemente. Selle asemel saab kuluelemente lisada hüvitusgrupi valimisel. Elemendid lisatakse hüvitusgrupi häälestusse vahekaardil **Eelarve kuluelemendid**. 

Hüvitusgrupid võivad määrata prognoositava ametikoha tulumäärad. Seadistate grupi prognoositava ametikoha tulu arvutamisel kasutama kas tunni- või aastapalgapõhisust. Vahekaardil **Hüvitusmäära tabelid** määrab tasumäärade hüvitusruudustik määatud taseme ja häälestuse alusel tulud, mis lisatakse prognoositavale ametikohale. Ruudustikud võivad põhineda inimressurssides olemasolevatel hüvitusruudustikel. Teise võimalusena saate luua eelarve planeerimiseks uued hüvitusruudustikud. 

Hüvitusmäära tabelites olevad kehtivuskuupäevad ja aegumiskuupäevad võimaldavad teil muuta tasumäärasid mis tahes kuupäeval. See funktsioon on kasulik, kui keset eelarvetsüklit on kaubandusüksus kokku leppinud üldises tõusus. Sellisel juhul muudate olemasoleva tabeli aegumiskuupäeva määra muutmisele eelnenud kuupäevaks ja lisate uue määratabeli, mis algab uuel kuupäeval. Kui valite uue määratabeli loomisel suvandi **Loo uus hüvitusruudustik olemasolevast ruudustikust**, saate valida inimressurssidest olemasoleva määratabeli. Loodud määratabelis võimaldab suvand **Massmuudatus** rakendada kõikidele ruudustikus olevatele määradele protsendi või kindla summa võrra tõusu või langust. 

Hüvitusgrupi välju **Tõusu graafik** ja **Tõusu kuupäev** kasutatakse, kui peate looma tasu tõusu, sest ametikohad lähevad ühelt etapilt järgmisele. Iga-aastane tasu tõus on tavapärane stsenaarium. Tõusu graafik määrab, kas etapi tõusuks kasutatakse ametikoha aastapäeva või üht ühist kuupäeva. Tõusu graafik rakendub kõikidele hüvitusgrupi prognoositavatele ametikohtadele. 

Hüvitusgrupis valitud tulu kuluelementi kasutatakse grupi prognoositavate ametikohtade tulude loomisel, sh nende põhipalk ja mis tahes etapi tõusud. Väli **Hüvituse fikseeritud plaan** seob inimressurssides hüvitusgrupi põhipalgaplaaniga. See seos võib määrata prognoositavale ametikohale töötaja põhipalgateabe ja saab seega muuta eelarve planeerimise täpsemaks. Pidage meeles, et hüvitusgrupi hüvitusruudustiku struktuur (tasemed ja etapid) peavad sobima põhipalgaplaani struktuuriga. Muidu ei saa süsteem hüvitusgruppi ja põhipalgaplaani õigesti siduda.

## <a name="creating-forecast-positions"></a>Prognoositavate ametikohtade loomine
[![graphic3](./media/graphic3-1024x327.png)](./media/graphic3.png)

### <a name="creating-forecast-positions-for-existing-positions"></a>Olemasolevatele ametikohtadele prognoositavate ametikohtade loomine

Kõige täpsema eelarve planeerimise jaoks saate luua prognoositavaid ametikohti, kasutades üksikasju olemasolevatest ametikohtadest Microsoft Dynamics 365 for Finance and Operationsis, olenemata sellest, kas ametikoht on praegu täidetud või mitte. 

Funktsioon **Lisa olemasolevad ametikohad** kuvab kõik organisatsiooni ametikohad. Seadistades kuupäeva **Seisuga**, saate muuta ametikohtade loendit, nii et see sisaldab ametikohti, mis olid olemas kuupäeval minevikus või enamasti tulevikus (näiteks järgmise eelarvetsükli algus). Valige eelarve plaanimise protsess ja eelarveplaani stsenaarium, valige loendist ametikohad ja klõpsake siis nuppu **OK**, et luua valitud ametikohtadele prognoositavad ametikohad. Arvestage sellega, et saate luua igale eelarve plaanimise protsessi ja eelarveplaani stsenaariumis olemasolevale ametikohale ainult ühe prognoositava ametikoha. Sellegipoolest saate luua lisaversioone, määrates erinevaid eelarveplaani stsenaariume. 

Kui jaotises Inimressursid on ametikohale määratud eelarve kuluelemendid, on need eelarve kuluelemendid määratud ka prognoositavale ametikohale ja kasutavad vaikesummasid. Prognoositava ametikoha väljale **Määratud töötaja** on sisestatud ametikohale määratud töötaja nimi, kui töötaja on määratud. See väli on lihtne tekstiväli. Otsest seost ei ole loodud. 

Kui eelarve kuluelement on valitud, on põhipalga aastane summa määratud prognoositavale ametikohale, kasutades valitud kuluelementi, eeldades, et määratud töötajal on põhipalgaplaan. Kui töötajal ei ole põhipalgaplaani või kui töötajat ei ole määratud, kasutatakse eelarve kuluelemendi jaoks vaikesummat. 

Kui suvand **Määra hüvitusgrupp** on seatud olekusse **Jah**, kui ametikohale määratud töötajal on etapipõhine põhipalgaplaan, mis on seotud hüvitusgrupiga (nagu varem kirjeldatud), määratakse töötaja tase ja etapp prognoositavale ametikohale koos hüvitusgrupiga. Hüvitusgrupi tulude eelarve kuluelement lisatakse prognoositavale ametikohale ning kasutatakse taseme tasumäära ja hüvitusgrupi etappi. 

Suvandi **Määra hüvitusgrupp** säte alistab sätte **Eelarve kuluelemendi määramine**. Kahte sätet saab kasutada korraga. 

[![graphic4](./media/graphic4.png)](./media/graphic4.png) 

Teine võimalus on määrata tähtpäeva kuupäev. Määratud töötaja valitud kuupäev (kohandatud alguskuupäev, töötaja alguskuupäev, töösuhte alguskuupäev või staaži kuupäev) määratakse prognoositava ametikoha tähtpäeva kuupäevaks ja seda kasutatakse teabe saamiseks ja palgatõusu loomisel.

### <a name="creating-new-forecast-positions"></a>Uute prognoositavate ametikohtade loomine

Saate luua uusi prognoositavaid ametikhti kahel viisil: kopeerides olemasoleva prognoositava ametikoha ja luues täiesti uue prognoositava ametikoha. 

Kui prognoositav ametikoht on valitud, valige suvand **Kopeeri valitud prognoositav ametikoht**, et luua uus prognoositav ametikoht, mille prognoosi olek on **Soovitatud**. Sellel prognoositaval ametikohal on kõik samad andmed mis kopeeritud prognoositaval ametikohal, välja arvatud määratud töötaja ja märkused eelarve kuluelementide kohta. Arvestage sellega, et jaotises Inimressursid luuakse ka vastav uus ametikoht. Ametikohal on kirjeldus **Prognoosi loodud**. 

Saate luua ka täiesti uue prognoositava ametikoha. Valige olemasolev töö, eelarve plaanimise protsess ja eelarveplaani stsenaarium. Seejärel saate lisada mis tahes muud soovitud üksikasjad. Tuletame veel kord meelde, et samal ajal luuakse jaotises Inimressursid uus ametikoht.

## <a name="working-with-forecast-positions"></a>Prognoositavate ametikohtadega töötamine
[![graphic5](./media/graphic5-1024x327.png)](./media/graphic5.png)

### <a name="multiple-versions-of-a-forecast-position"></a>Prognoositava ametikoha mitu versiooni

Saate muuta prognoositavaid ametikohti eelarvetsüklile teadaolevate muudatuste rakendamiseks või soovitatavate muudastuste mudeldamiseks. Levinud tava on luua prognoositavate ametikohtade aluskomplekt, luua nende prognoositavate ametikohtade koopiad ja kasutada koopiaid erinevate muudatuste komplektide mudelsamiseks. Koopiad määratakse erinevatele eelarveplaani stsenaariumidele, kuid vähemalt kuni muudatuste tegemiseni on need muus osas identsed prognoositavate ametikohtadega, kust need kopeeritud on. Originaalid ja koopiad ühiskasutavad funktsioonis Inimressursid sama positsiooni. 

Seda funktsionaalsust pakub funktsioon **Kopeeri stsenaariumi**. Arvestage sellega, et positsioonil Inimressursid saab olla ainult üks prognoositav ametikoht igas eelarveplaani stsenaariumis.

### <a name="modifying-forecast-positions"></a>Prognoositavate ametikohtade muutmine

Prognoositavatele ametikohtadele tehtavad muudatused on nendele prognoositavatele ametikohtadele piiratud. Muudatused ei mõjuta ametikoha kirjeid väljal Inimressursid. Enamik muudatusi on piiratud prognooistava ametikohaga, mida redigeeritakse. Teisisõnu on muudatused määratud eelarve plaanimise protsessi ja eelarveplaani stsenaariumi põhised. Erandid on muudatused väljadel, mida ühiskasutatakse ametikoha puhul protsessides ja stsenaariumides. Need väljad hõlmavad välju vahekaardil **Üldine** ja vahekaardil **Finantsdimensioonid**. Kui neid välju muudetakse, rakenduvad uued väärtused ametikohale kõikides eelarveplaani stsenaariumides. Seega võimaldavad need välja teil kiiresti kõiki versioone värskendada.

#### <a name="budget-cost-elements"></a>Eelarve kuluelemendid

Eelarve kuluelemendid pakuvad põhiteavet eelarveplaanide kohta: eelarvesumma ja põhikonto. Eelarvesumma on summa, mis saadetakse eelarveplaani, kui prognoositav ametikoht on plaani kaasatud. Eelarvesumma arvutatakse ja seda ei saa otse muuta. See summa on kas aastane summa või aastase summa põhielementide protsendi arvutus (nagu on määratletud eelarve kuluelemendi seadistuses). Summa arvestab siis elemendi kuupäevavahemiku päevade arvuga (alguskuupäev kuni lõppkuupäev) ja ka prognoositava töökoha väärtusega **Täistööaja vaste** (FTE). 

Näiteks eelarve kuluelemendi rida alates 1. jaanuarist 2017 kuni 30. juunini 2017, mille aastane summa on 100 000 ja väärtus FTE on **0,50**, arvutatakse järgmiselt: 100 000 × (181 päeva ÷ 365 päeva) × 0,50 = 24 794,52. 

Eelarve kuluelemendi read tuleb uuesti arvutada, kui prognoositava ametikoha puhul muudetakse FTE väärtust. Read tuleb uuesti arvutada ka siis, kui muudetakse aktiveerimis- või lõpetamiskuupäevi. Muudatused nendes kuupäevades võivad põhjustada värskendusi eelarve kululemendi algus- ja lõppkuupäevades, mis peavad jääma prognoositava ametikoha kuupäevavahemikku. Kui ümberarvutamine on nõutav, muutub kättesaadavalks nupp **Arvuta uuesti** ja kuvatakse teade Vajab arvutamist. Ümerarvutamine on nõutav ka siis, kui lisate või eemaldate eelarve kuluelemendi.

**Näide** 

Organisatsioon kaalub raamatupidaja ametikoha kulude vähendamiseks kahte võimalust. Üks võimalus on lõpetada amerikoht mingiks osaks aastast. Teine võimalus on muuta ametikoht kogu aastaks osalise tööajaga ametikohaks. Brad lõi põhistseanaariumis olemasolevale raamatupidaja ametikohale prognoositava ametikoha. Ta kopeerib selle põhilise prognoositava ametikoha stsenaariumisse A, määrab lõpetamise kuupäevaks 31. mai ja arvutab uuesti. Seejärel kopeerib Brad põhilise prognoositava ametikoha stsenaaiumisse B, muudab FTE väärtuseks **0,50** ja arvutab siis uuesti. Bradil on nüüd kolm versiooni, millest igaühel on kulude kogusummad, mis on tema võimalustega joondatud.

#### <a name="assigning-a-compensation-group"></a>Hüvitusgrupi määramine

Kui määrate esimest korda prognoositavale ametikohale hüvitusgrupi, lisatakse hüvitusgrupist eelarve vaikekuluelemendid. Kui prognoositavale ametikohale on juba määratud kuluelemendid, jäävad need kuluelemendid alles. Kui hüvitusgrupp on juba määratud ja seda muudetakse, siis olemasolevad eelarve kuluelemendid eemaldatakse ja asendatakse komplektiga hüvitusgrupist. 

Kui valite hüvituse taseme ja etapi, lisatakse tulude eelarve kuluelement (nagu on määratletud hüvitusgrupis). Aastane summa arvutatakse, kasutades valitud taseme ja etapi määra ja aastaseid tunde hüvitusgrupis (või aastapalga puhul taseme ja etapi kogu summa). Kordame veel kord, et see summa arvestab kuluelemendi rea kuupäevavahemikuga ja prognoositava ametikoha FTE väärtusega.

#### <a name="generating-increases"></a>Tõusude loomine

Aastaseid tõuse (üks kalendriaasta kohta) saab luua automaatselt prognoositavate ametikohtade puhul, millele on määratud etapipõhine hüvitusgrupp. Klõpsake suvandit **Loo tõusud**, et lisada järgmisele kõrgeimale etapile tulude eelarve kuluelement. Uue tulude eelarve kuluelemendi alguskuupäev on plaanitud tõusu kuupäev, mida näidatakse prognoositava ametikoha puhul. See kuupäev on määratud hüvitusgrupist ühel kahest viisist. Kui hüvitusgrupi tõusu graafik on olekus **Ühine kuupäev**, siis on tõusu kuupäev määratud hüvitusgrupis. Kui tõusu graafik on olekus **Tähtpäeva kuupäev**, kasutatakse prognoositava ametikoha tähtpäeva kuupäeva välja ja eelarvetsükkel lisab aasta. Kui eelarvetsüklis on mitu kalendriaastat, lisatakse mitu tõusu. 

Praeguse tulude eelarve kuluelemendi lõppkuupäeva värskendatakse päev enne tõusu kuupäeva. Ümberarvutamise protsessi kasutatakse tõusude loomisel automaatselt. Seega ei pea tea ümberarvutusi käsitsi tegema. 

Kui klõpsate suvandit **Loo tõusud** teist korda, käitatakse protsessi uuesti, kuid rohkem kirjeid ei lisata. Luuakse ainult üks tõus kalendriaasta kohta.

#### <a name="changes-from-other-pages"></a>Muudatused muudelt lehtedelt

Prognoositavate ametikohtade värskendused võivad tulla ka muudelt aladelt, nagu eelarve kuluelemendi ja hüvitusgrupi häälestamise lehed. Prognoositavaid ametikohti saab muuta ka hulgivärskendamise protsessi kasutades. 

Seadistuslehel **Eelarve kuluelement** on saadaval kaks valikut: **Ametikohtadesse lisamine** ja **Ametikohtade värskendamine**. Suvand **Ametikohtadesse lisamine** lisab eelarve kuluelemendi valitud prognoositavatele ametikohtadele. Kui prognoositavale ametikohale on juba element määratud, jäetakse see prognoositav ametikoht vahele. Suvand **Ametikohtade värskendamine** rakendab praegused väärtused (põhikonto, protsent, aastane summa jne) valitud prognoositavatele ametikohtadele. 

Igal protsessil on sarnane leht, kus saate valida prognoositavaid ametikohti. Leht **Ametikohtadesse lisamine** näitab kõiki prognoositavaid ametikohti, mis on valimiseks saadaval ja leht **Ametikohtade värskendamine** näitab ainult neid prognoositavaid ametikohti, millele juba on määratud eelarve kuluelement. (Seega annab leht **Ametikohtade värskendamine** teile võimaluse teada saada, millistele prognoositavatele ametikohtadele on juba lisatud kuluelement.) Prognoositavate ametikohtade värskendamisse kaasamiseks liigutage need ülemiselt ruudustikult alumisele ruudustikule. 

Arvestage sellega, et funktsioon **Muuda kuupäevi** vahekaardil **Kulu arvutamine** muudab kohe eelarve kuluelemendi algus- ja lõppkuupäevi prognoositaval ametikohal. Valikuvõimalusi ei ole. 

Lehel **Hüvitusgrupp** rakendab funktsioon **Ametikoha määrade värskendamine** praguse hüvitusmäära tabeli määrad grupile määratud prognoositavatele ametikohtadele. Määrasid värskendatakse ja täiendavad kuluelemendi read lisatakse kõikidele uutele määrade tabeli ridadele (kuupäeva alusel). Kuid eelarve kuluelemente ja tõusu kuupäevi ei värskendata. Saate valida, millist eelarve plaanimise protsessi ja millist eelarveplaani stsenaariumi värskendada. Seega saate värskendada üht stsenaariumi, kuid jätta teise stsenaariumi võrdluseks muutmata. 

Valides prognoositava ametikoha ja klõpsates siis suvandit **Hulgivärskendamine**, saate lisada või muuta korraga mitut prognoositavat ametikohta. Saadaval on mitmeid valikuid. Üks suvand vahekaardil **Finantsdimensioonid** erineb kergelt teostest ja on seotud eelarve kuluelementidega. Saate eelarve kuluelemente lisada, seades suvandi **Eelarve vaikeväärtused** olekuks **Jah**. Kui eelarve kuluelemente ei valita, kuid suvand **Eelarve vaikeväärtused** on olekus **Jah**, eemaldatakse kõik praegu määratud eelarve kuluelemendid. 

Ümberarvutamise protsessi kasutatakse automaatselt mis tahes muudetud prognoositava ametikoha puhul.

## <a name="bringing-forecast-positions-into-budget-plans"></a>Prognoositavate ametikohtade toomine eelarveplaanidesse

[![graphic6](./media/graphic6-1024x327.png)](./media/graphic6.png)

Prognoositavate ametikohtade loomise ja muutmise eesmärk on lisada need eelarveplaanidele, nii et eelarveplaanid kaasaksid kõige täpsemaid eelarvesummasid. Prognoositavate ametikohtade lisamiseks eelarveplaanidesse on kaks järgmist viisi. Saate kasutada eelarveplaanis kas loomise protsessi või valikuprotsessi.

### <a name="generating-a-budget-plan-from-forecast-positions"></a>Eelarveplaani loomine prognoositavatest ametikohtadest

Funktsioon **Eelarveplaani loomine prognoositavatest ametikohtadest** loob eelarveplaane või värskendab neid nii, et neil on eelarvesummad ja täistööaja vastete arv prognoositavatest ametikohtadest. Prognoositava ametikoha eelarvesummadest saavad eelarveplaani rea summad ning need koondatakse finantsdimensiooni väärtuste ja jõustumiskuupäevaga. Loomise protsess määrab eelarveplaani reale allikaks oleva prognoositava ametikoha. Ametikoha vaatamiseks saate lisada prognoositava ametikoha eelarveplaani paigutuse reana või kasutada päringut **Eelarveplaani read**. Selle määramise vahele jätmiseks määrake suvandi **Kaasa ametikoht eelarveplaani real** olekuks **Ei**. 

Saate valida eelarveplaani täistööaja vaste stsenaariumi, et lisada täistööaja vastete arv eelarveplaani. Saate valida ainult sellise koguse tüübiga stsenaariume, mis on kaasatud sihteelarveplaani paigutusse. Kui valite täistööaja vaste stsenaariumi, peate määrama ka täistööaja vaste põhikonto. Seda kontot kasutatakse koguse eelarveplaani ridade loomiseks. 

Allikas valitud eelarve plaanimise protsess ja eelarveplaani stsenaarium et määravad sihtstsenaariumi eelarve planeerimise protsessi ja stsenaariumi. Kuna need atribuudid on määratud prognoositavatele ametikohtadele, peavad need olema sünkroonitud eelarveplaaniga. Seega ei saa atribuute sihtkohas redigeerida. 

Muude loomisprotsesside puhul on saadaval kolm suvandit.

-   **Uue eelarveplaani loomine** – looge uus plaan, millel on atribuudid, mis on valitud jaotises **Sihtkoht**.
-   **Olemasoleva eelarveplaani stsenaariumi asendamine** – kustutage kõik andmed valitud eelarveplaani stsenaariumi sihteelarveplaanis ja looge uued read, millel on valitud prognoositava ametikoha andmed.
-   **Olemasoleva eelarveplaani stsenaariumi värskendamine ja uute andmete lisamine** – värskendage olemasolevaid ridu sihtplaanis, mis vastavad allika ridadele, ja lisage uute andmete jaoks ka uusi ridu. Vastendamine põhineb pearaamatukontol, kuupäeval, eelarveklassil ja muudel väärtustel, nagu prognoositav ametikoht. Kõik read, millel on ametikoha kood, mis vastab allika ametikoha koodile, asendatakse uute ridadega allikast.

### <a name="selecting-forecast-positions"></a>Prognoositavate ametikohtade valimine

Saate lisada prognoositava ametikoha eelarvesummad kas otse eelarveplaani. Kasutage eelarveplaani ridade kohal olevat funktsiooni **Ametikohtade lisamine**, et valida lisatav prognoositavad ametikohad. 

Allikana valitavad eelarveplaani stsenaariumid on piiratud stsenaariumidega, mis on kaastaud plaani paigutusse. Üks suvand vahekaardil **Sihtkoht** võimaldab teil määrata, et täistööaja vaste stsenaarium ja põhikonto on saadaval täistööaja vastete arvu lisamiseks, kuid need ei ole nõutavad. 

See valikuprotsess käitub nagu loomisprotsessi suvand **Olemasoleva eelarveplaani stsenaariumi värskendamine ja uute andmete lisamine**. Kõik olemasolevad eelarveplaani read, kuhu prognoositav ametikoht lisatakse, eemaldatakse ja asendatakse uute ridadega, mis põhinevad prognoositava ametikoha praegusel olekul.

#### <a name="date-options"></a>Kuupäevasuvandid

Nii loomis- kui ka valimisprotsessi puhul määrab eelarve kuluelemendi rea alguskuupäev vastava eelarveplaani rea jõustumiskuupäeva. Eelarve kuluelemendi häälestuslehe väli **Eraldamismeetod** määrab eraldamismeetodi.

-   **Alguskuupäev** – eelarve kuluelemendi alguskuupäeva kasutatakse eelarveplaani rea jõustumiskuupäevana.
-   **Igakuine** – eelarvesumma jaotub ühtlaselt kuupäevavahemiku kuude arvule, et toota tavapärane igakuine summa, mis määratakse iga kuu esimesel kuupäeval. Kui esimene periood on osaline kuu, arvestatakse kuu summa päevade arvu järgi, millal kulu sel kuul aktiivne on, ja tulemus määratakse alguskuupäevale. Viimase kuu summa on kogu eelarvesumma ja kõikide teiste kuude summa vaheline erinevus. Seega võib ümardamine eelmise kuu summat mõjutada.
-   **Kord kvartalis** – see meetod on sama mis **Kord kuus**, kuid arvutused tehakse kolmekuiste perioodide kohta.
-   **Kord nädalas** – loogika on sarnande meetodite **Kord kuus** ja **Kord kvartalis** loogikale. Eelarvesumma jaotub ühtlaselt kuupäevavahemiku nädalate arvule, et toota tavapärane iganädalane summa, mis määratakse iga nädala esimesel kuupäeval. Kui esimene periood on osaline nädal, arvestatakse nädala summa päevade arvu järgi, millal kulu sel nädalal aktiivne on, ja tulemus määratakse alguskuupäevale. Viimase nädala summa on kogu eelarvesumma ja kõikide teiste nädalate summa vaheline erinevus. Seega võib ümardamine eelmise nädala summat mõjutada.
-   **Üle nädala** – see meetod on sama mis **Kord nädalas**, kuid arvutused tehakse kahenädalaste perioodide kohta.

#### <a name="changing-budget-plan-lines-that-have-forecast-positions"></a>Prognoositavate ametikohtadega eelarveplaani ridade muutmine

Eelarveplaani read näitavad eelarvesummade allikat (prognoositava ametikoha number), kuid need ei ole seotud. Seega ei kuvata muudatusi prognoositavas ametikohas eelarveplaani real ja muudatusi eelarveplaani ral kuvatakse prognoositaval ametikohas. Kui muudate prognoositavat ametikohta ja soovite värskenduste kaasamist eelarveplaani, peate prognoositava ametikoha uuesti pöaani tooma. Kuid pidage meeles, et see protsess eemaldab kõik read, kuhu see prognoositav ametikoht määratud on. Seega eemaldatakse kõik nendes ridades tehtud muudatused. 

Nägemaks, millistesse eelarveplaanidesse prognoositav ametikoht kaasatud on, saate luua aruande **Prognoositavad ametikohad eelarveplaani järgi**. Teise võimalusena saate avada prognoositava ametikoha puhul plaanide vaaramiseks kiirinfo **Seostatud eelarveplaanid**.



