---
title: Koondplaneerimine koos tarneprognoosidega
description: See artikkel kirjeldab, kuidas tarneprognoose koondplaneerimisel loetakse.
author: t-benebo
ms.date: 09/21/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-21
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 2bac9355bb1ac00f697ec459f494a64553e0eacc
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740137"
---
# <a name="master-planning-with-supply-forecasts"></a>Koondplaneerimine koos tarneprognoosidega

[!include [banner](../../includes/banner.md)]

Tarneprognoosid lasevad teil määratleda tarne, mida te mõne tulevase perioodi jooksul eeldate. Tavaliselt on hinnangu aluseks eelmise aasta müügiajalugu ja seejärel kasutatakse eelarvete kalkulatsiooni jaoks eelarvet. Saate seadistada ka oma koondplaanid, et planeerimisel prognoose arvestada.

## <a name="set-up-a-master-plan-to-consider-supply-forecasts"></a>Tarneprognooside arvestamist arvestav koondplaan

Saate määrata, kas iga koondplaan peaks eelarveid käitamisel arvesse võtma. Kasutage järgmist protseduuri, et seadistada igale plaanile prognoosi valikud.

1. Avage **Koondplaneerimine \> Seadistus \> Plaanid \> Koondplaanid**.
1. Valige loendipaanil olemasolev koondplaan või valige **uue** plaani loomiseks tegevuspaanil uus.
1. Määrake kiirkaardil **Üldine** järgmised väljad.

    - **Prognoosimudel** – valige mudel, mis sisaldab pakkumise ja/või nõudluse prognoose, mida koondplaan peaks arvesse võtma.
    - **Kaasa tarneprognoos** – määrake selle suvandi väärtuseks *Jah,* kui koondplaan peaks võtma arvesse tarneprognoose.
    - **Kaasa nõudluse prognoos** – määrake selle suvandi väärtuseks *Jah*, kui koondplaan peaks arvestama nõudluse prognoosidega. Kuigi see säte ei sõltu sättest **Kaasa tarneprognoos**, kehtivad mõned muud sätted lehel nii tarneprognooside kui ka nõudluse prognooside puhul. Lisateavet nõudluse prognoosidega arvestamist arvestav planeerimise kohta vt koondplaneerimisest [nõudluse prognoosidega](demand-forecast.md).
    - **Eelarvenõuete vähendamiseks kasutatav meetod** – valige meetod, mida kasutada eelarvenõuete vähendamiseks koondplaneerimise ajal:

        - *Pole* – eelarvenõudeid koondplaneerimisel ei vähendata.
        - *Protsent – plaanimisvõti* – eelarve vajadusi vähendatakse vastavalt plaanimisvõtmes määratletud protsentidele ja perioodidele.
        - *Kanded – vähendamisvõti* – eelarve vajadusi vähendatakse vähendusvõtmes määratletud ajaperioodidel tehtud kannete võrra.
        - *Kanded – dünaamiline* periood – prognoosinõudeid vähendatakse dünaamilise perioodi jooksul tehtud tellimusekannete võrra. Dünaamiline periood katab praeguse eelarve kuupäevi ja see lõpeb järgmise eelarve algusaja. *Kanded – dünaamilise* perioodi meetod ei kasuta või nõua vähendamise võtit, ja selle kasutamisel kehtivad järgmised tingimused:

            - Prognoosi täielikul vähendamisel muutub praeguse prognoosi eelarvevajaduseks 0 (null).
            - Kui tulevasi prognoose pole, vähendatakse eelarvevajadusi viimati sisestatud prognoosist.
            - Prognoosi vähenduse arvutamisse kaasatakse ajapiirid.
            - Prognoosi vähenduse arvutamisse kaasatakse positiivne päevade arv.
            - Kui tellimuse tegelikud kanded ületavad eelarvevajadusi, ei edastata järelejäänud kandeid järgmisse prognoosiperioodi.

        > [!NOTE]
        > Eelarvenõuete **vähendamiseks kasutatav meetod** rakendub ka nõudluse prognoosidele, kui olete need koondplaani jaoks lubanud ja see mõjutab neid sarnasel viisil. Lisateavet vt koondplaneerimisest [nõudluse prognoosidega](demand-forecast.md).

## <a name="set-reduction-options-for-coverage-groups"></a>Laovarude gruppide vähendamisvalikute määramine

Et seadistada valikud, mis kontrollivad, kuidas laovarude grupp vähendab oma eelarve vajadusi koondplaanide puhul, mis kasutavad kandepõhist vähendamist, järgige neid samme.

1. Valige **Koondplaneerimine \> Seadistus \> Plaanid \> Laovarude grupid**.
1. Valige loendipaanil olemasolev laovarude grupp või **valige** uue loomiseks tegevuspaanil uus.
1. Määrake **kiirkaardil** **Muu** kiirkaart väljal Prognoosi vähendamine, kuidas tarneprognoosi vajadusi laovarude grupi kaupade puhul vähendada, nende koondplaanide puhul, **kus** eelarvenõuete vähendamiseks kasutatava meetodi välja väärtuseks on seatud Kanded *–* *planeerimise klahv või kanded – dünaamiline periood.* Valige üks järgmistest väärtustest.

    - *Kõik kanded* – kõik kanded peaksid vähendama prognoosi.
    - *Tellimused* – eelarvet peaksid vähendama ainult sama tüüpi tellimused.

    Näiteks näitab kauba tellimuste vaikesätted, et need tuleb toota. Tarneprognoosi rida on kogusele 50 ja olemasolev ostutellimus kogusele 20. Kui välja **Vähenda prognoosi** alus väärtuseks on *seatud* Tellimused, luuakse plaanitud tootmistellimus kogusele 50. Kui selle väärtuseks on seatud *Kõik* kanded, vähendatakse plaanitud tootmistellimust koguseni 30.

    See säte kehtib ka nõudluse prognoosimise vähendamise kohta. Lisateavet vt koondplaneerimisest [nõudluse prognoosidega](demand-forecast.md).

## <a name="enter-a-supply-forecast-for-a-product"></a>Sisestage toote tarneprognoos.

Toote tarneprognoosi sisestamiseks järgige neid samme.

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Valige toode, mille kohta soovite eelarve sisestada.
1. Valige tegevuspaani vahekaardil **Plaan** tarneprognoos **·**.
1. Valige tarneprognoosi **lehel** tegevuspaanil **uus**, et lisada prognoos ruudustikku.
1. Saate uuel real sisestada eelarve määramiseks nõutava teabe.

## <a name="plan-for-an-item-with-supply-forecast-lines"></a>Tarneprognoosi ridadega kauba plaan

Kui käivitate koondplaani, mis sisaldab kaupa, mille kohta on olemas tarneprognoos, loob süsteem ostutellimuse juba sisestatud tarneridadele. Kauba tellimuse vaikesätteid täidetakse. Kui need vaiketellimuse **sätted** *määravad* ostutellimuse vaiketüübi väärtuse ja tarneprognoosi real pole hankija kontot määratud, kasutab süsteem kauba puhul vaike hankijat.

## <a name="check-whether-a-planned-order-is-a-supply-forecast-order"></a>Kontrollige, kas plaanitud tellimus on tarneprognoosi tellimus.

Kasutage järgmist protseduuri, et teada saada, kas tarneprognoosi tulemusena loodi plaanitud tellimus.

1. Avage **Koondplaneerimine \> Koondplaneerimine \> Plaanitud tellimused**.
1. Avage plaanitud tellimus, mida soovite üle vaadata.
1. **Vaadake kiirkaardil** Üldine tarneprognoosi **välja** väärtust. Kui tellimus loodi tarneprognoosi katmiseks, seatakse selle välja väärtuseks *Jah*.

## <a name="examples-of-master-planning-with-supply-forecasts"></a>Tarneprognooside koondplaneerimise näited

See jaotis pakub mitut näidet, mis näitavad, kuidas tarneprognoos mõjutab koondplaneerimist.

### <a name="example-1-supply-forecast-for-an-item"></a>Näide 1: kauba tarneprognoos

Teil on kaup, mille vaiketüüp on *Ostutellimus ja* vaike hankija on *US-002*. Sellel on järgmine tarneprognoosi rida.

| Mudel    | Kuupäev     | Hankija konto | Hankijagrupp | Kogus | Ühik | Sait | Ladu |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| PraeguneF | 10/10/22 |                |              | 35       | iga   | 1    | 11        |

Koondplaneerimise käivitamisel luuakse plaanitud *ostutellimus 35* *ea jaoks hankijalt US-002*.

### <a name="example-2-several-supply-forecast-lines-with-and-without-a-vendor"></a>Näide 2: mitu tarneprognoosi rida hankijaga ja ilma

Teil on kaup, mille vaiketüüp on *Ostutellimus ja* vaike hankija on *US-002*. Sellel on järgmised tarneprognoosi read.

| Mudel    | Kuupäev     | Hankija konto | Hankijagrupp | Kogus | Ühik | Sait | Ladu |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| PraeguneF | 10/10/22 |                |              | 35       | iga   | 1    | 11        |
| PraeguneF | 10/10/22 | US-101         |              | 25       | iga   | 1    | 11        |

Sel juhul käsitleb süsteem rida, mis ei määra hankijat üldiseks prognoosiks, ja eeldab, et hankijat määrav rida tuleb üldisest prognoosist lahutada. Seepärast loob koondplaneerimine kaubale järgmised plaanitud ostutellimused:

- Plaanitud ostutellimus kogusele *25 ea* hankijalt *US-101* (Kasutatakse hankijat ja eelarvereal määratud kogust.)
- Plaanitud ostutellimus *kogusele 10 ea* *hankijalt US-002* (Kuna teisel eelarvereal pole hankijat määratud, kasutatakse vaike hankijat ja selle eelarverea kogust vähendatakse hankijaspetsiifilise eelarverea koguse võrra.)

### <a name="example-3-plans-that-use-the-transactions---dynamic-period-reduction-method-in-a-single-forecast-period"></a>Näide 3: plaanid, mis kasutavad kandeid – dünaamilise perioodi vähendamise meetod üksikus eelarveperioodis

Koondplaanide puhul, mis *kasutavad* kanded – dünaamiline periood prognoosi vähendamise meetodina, vähendab koondplaneerimine prognoosi koguseid, kui on olemas sellistele tarneomadustele vastavad kanded.

Näiteks on teil kaup, mille vaiketüüp on *Ostutellimus*. Sellel on järgmine tarneprognoosi rida.

| Mudel    | Kuupäev     | Hankija konto | Hankijagrupp | Kogus | Ühik | Sait | Ladu |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| PraeguneF | 10/10/22 | US-101         |              | 25       | iga   | 1    | 11        |

Kuna tarneprognoosi rida on ainult üks, on eelarveperiood ainult üks.

Kannete kasutamiseks seadistatud *koondplaani käivitamisel –* vähendusmeetodina dünaamiline periood, võib ilmneda üks järgmistest tulemustest:

- Kui ostutellimus on hankijale US-101 ja kogus on 10 ea *ning* *tarneprognoosi* välja väärtuseks on seatud Jah **,** loob koondplaneerimine uue plaanitud ostutellimuse järelejäänud kogusele 10 ea *.* *·* Eelarverida vähendatakse, kuna hankija vastab olemasolevale ostutellimusele.
- *Kui hankijale US-102*, saidile 1 *,* *laole 11* *ja kogusele 10 ea* ning **tarneprognoosi** välja väärtuseks on *seatud Jah*, *loob koondplaneerimine uue plaanitud ostutellimuse koguseks 25 ea.* Eelarverida ei saa vähendada, kuna sellel on olemasolevast ostutellimusest erinev hankija.

> [!NOTE]
> Selline olukord võib tekkida plaanitud ostutellimuste puhul, kuna hankija on nendega seostatud. Üleviimistellimuste ja tootmistellimuste puhul vähendatakse tarneprognoosi summasid alati olemasolevate tellimuste võrra, kuna seda tüüpi tellimuste jaoks pole hankijat määratud.

### <a name="example-4-plans-that-use-the-transactions---dynamic-period-reduction-method-over-several-forecast-periods"></a>Näide 4: plaanid, mis kasutavad kandeid – dünaamilise perioodi vähendamise meetod mitme eelarveperioodi jooksul

Teil on kaup, mille vaiketüüp on *Ostutellimus*. Sellel on järgmised tarneprognoosi read.

| Mudel    | Kuupäev     | Hankija konto | Hankijagrupp | Kogus | Ühik | Sait | Ladu |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| PraeguneF | 10/10/22 | US-101         |              | 25       | iga   | 1    | 11        |
| PraeguneF | 10/15/22 | US-101         |              | 25       | iga   | 1    | 11        |

Selles näites on kaks eelarverida, millest igaühel on erinev kuupäev. Seetõttu kehtestatakse kuupäevad eelarveperioodide piirid. Esimene periood on 10. oktooberst 14. oktoober 2022 (10.10.2012–10.14.22). Teine on alates 15. oktooberst, 2022 (10/15/22) edasi.

Hankijale US-101 *,* kogusele 10 ea *ja* kuupäevale 10/12/22 (12 *. oktoober 2022) on olemas* ostutellimus. Kannete kasutamiseks seadistatud koondplaani *käivitamisel loob* see vähendusmeetodina dünaamilise perioodi, järgmised tellimused:

- Plaanitud tellimus *kogusele 15 ea* *ja kuupäevale 10/10/22* (kogust vähendatakse olemasoleva ostutellimuse võrra, mille kuupäev on sama eelarveperioodi jooksul.)
- Plaanitud tellimus kogusele *25 ea* *ja kuupäevale 10/15/22* (kogus on eelarve täielik kogus. )

### <a name="example-5-plans-that-use-no-reduction"></a>Näide 5: plaanid, mille puhul vähendamine puudub

Kui käivitate plaani, kus prognoosi vähendamise meetod on *Pole*, loob koondplaneerimine alati kõigi tarneprognoosi ridade plaanitud tarne. Kui plaanitud tarne on kinnitatud, vähendab see tulevasi plaanitud tellimusi. Ostutellimused ei vähenda tarneprognoosi ridu.

Näiteks on teil kaup, mille vaiketüüp on *Ostutellimus*. Sellel on järgmine tarneprognoosi rida.

| Mudel    | Kuupäev     | Hankija konto | Hankijagrupp | Kogus | Ühik | Sait | Ladu |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| PraeguneF | 10/10/22 | US-101         |              | 25       | iga   | 1    | 11        |

Hankijale *US-101, saidile 1*, *laole 11* *,* *kogusele 25 ea* *ja kuupäevale 10/10/22 on olemas ostutellimus.* 

Kui käivitate *koondplaani*, mis on seadistatud kasutama vähendusviisina Valikut Pole, *loob see plaanitud ostutellimuse hankijale US-101,* saidile *1*, *laole 11*, *kogusele 25 ea* ja *kuupäevale 10/10/22*. See tähendab, et olemasolevat ostutellimust ei vähendata, kuna prognoosi vähendamise meetod on *Pole*.

Nüüd redigeerite pärast viimast planeerimist loodud plaanitud ostutellimust ja *muudate koguseks 15 ea*. Seejärel kinnitate tellimuse. *Järgmisel koondplaani käivitamisel loob see plaanitud ostutellimuse hankijale US-101, saidile 1*, *laole* *11*, *kogusele 10 ea* ja *kuupäevale 10/10/22*. Sel korral vähendatakse kogust, et peegeldada eelmise planeerimise käituse olemasoleva kinnitatud tellimuse kogust.

## <a name="differences-between-planning-optimization-and-the-deprecated-master-planning-engine"></a>Erinevused plaanimise optimeerimise ja taunitud koondplaneerimise mootori vahel

Tarneprognoosid töötavad veidi teisiti, sõltuvalt kasutatavast plaanimismootorist (plaanimise optimeerimine või taunitud koondplaneerimise mootor). Selles jaotises kirjeldatakse erinevusi.

### <a name="vendor-groups"></a>Hankijagrupid

Eelarverea lisamisel saate määrata hankija ja hankijagrupi. Taunitud koondplaneerimise mootoris grupeeritakse loodud plaanitud tellimused hankija- ja hankijagrupi väärtuste kombinatsiooni alusel. Plaanimise optimeerimises grupeeritakse plaanitud tellimused hankija kaupa.

Järgmine tabel annab mõned näited kauba tarneprognoosi ridadest.

| Mudel    | Kuupäev     | Hankija konto | Hankijagrupp | Kogus | Ühik | Sait | Ladu |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| PraeguneF | 10/10/22 |                | HankijagruppA | 5        | iga   | 1    | 11        |
| PraeguneF | 10/10/22 |                | HankijagruppA | 6        | iga   | 1    | 11        |
| PraeguneF | 10/10/22 |                |              | 7        | iga   | 1    | 11        |

Hankija *VendorA* on hankijagrupi *VendorGroupA* vaike hankija. See on ka kauba vaike hankija.

Taunitud koondplaneerimise mootor loob järgmised tellimused:

- Plaanitud ostutellimus hankija *VendorA*, hankijagrupi *VendorGroupA* ja koguse *11 jaoks*
- Plaanitud ostutellimus hankija HankijaA *jaoks* ja kogus *7*

Plaanimise optimeerimine loob ainult ühe tellimuse:

- Plaanitud ostutellimus hankija *VendorA*, hankijagrupi *VendorGroupA* ja koguse *18 jaoks*

### <a name="reduction-of-general-forecasts-by-more-specific-forecasts"></a>Üldiste eelarvete vähendamine kindlate eelarvete abil

Taunitud koondplaneerimise mootoris on tulemus ettearvamatu, kui mõnel prognoosil on hankija, kuid teistel mitte.

Planeerimise optimeerimisel vähendatakse üldiseid eelarveid alati kindlate prognooside võrra, nagu järgmises näites näha.

Järgmine tabel annab mõned näited kauba tarneprognoosi ridadest.

| Kuupäev       | Kogus | Hankija   | Hankijagrupp  |
|------------|----------|----------|---------------|
| 02/11/2022 | 5.00     | Hankija -A | Hankijagrupp –A |
| 02/11/2022 | 6,00     | Hankija -A | Hankijagrupp –A |
| 02/11/2022 | 15.00    |          |               |

Üldprognoosi (15,00 tk) vähendatakse kindlate prognooside võrra (5,00 + 6,00 = 11,00 tk). Jääk määratakse vaike hankijale. Järgmine tabel näitab plaanitud tellimusi.

| Kuupäev       | Kogus | Hankija   | Hankijagrupp  |
|------------|----------|----------|---------------|
| 02/11/2022 | 11.00    | Hankija -A | Hankijagrupp –A |
| 02/11/2022 | 4.00     | Hankija -A | Hankijagrupp –A |

### <a name="respect-for-default-order-settings-when-planned-orders-are-generated"></a>Plaanitud tellimuste loomisel arvesse võtta tellimuse vaikesätteid

Igal kaubal võivad olla tellimuste vaikesätted, nt ostutellimuse minimaalne kogus. Taunitud koondplaneerimise mootor ignoreerib neid sätteid ja teisendab seetõttu prognoosid plaanitud tellimusteks, mille kogus on sama. Planeerimise optimeerimine peab neid sätteid arvesse, kui plaanitud tellimused luuakse tarneprognooside alusel. 

### <a name="aggregation-of-planned-orders-as-a-result-of-reduction-by-approved-orders"></a>Plaanitud tellimuste kogum, mis on seotud vähendamisega kinnitatud tellimustega

Taunitud koondplaneerimise mootor eeldab, et olemasolevat tarneprognoosi vähendab ainult üks tellimus. Seega, kui tarneprognoosi reaga kattub mitu tellimust, siis ainult esimene tellimus seda vähendab. Planeerimise optimeerimises vähendavad seda kõik tarneprognoosi reale vastavad tellimused.

### <a name="reduction-of-forecasts-by-matching-vendors-only"></a>Prognooside vähendamine ainult ühtivate hankijate abil

Kui taunitud koondplaneerimise mootor vähendab prognoosi olemasolevate väljastatud ostutellimuste alusel, ei kindlusta see, et ostutellimuse hankija ühtib prognoosist hankijaga. Plaanimise optimeerimine vähendab prognoose ainult ostutellimuste alusel, mille hankijaväljal on vastav väärtus.

Üleviimis- ja tootmistellimuste puhul eiratakse hankija välja alati, kuna see ei ole nende tellimusetüüpide puhul asjakohane.

### <a name="reduction-of-forecasts-by-transfer-orders"></a>Eelarvete vähendamine üleviimistellimuste alusel

Kui kauba vaiketellimuse tüüp on Ülekanne, saab *eelarveid* vähendada ainult olemasolevate plaanitud üleviimistellimuste võrra. Tootmistellimuste ja ostutellimuste puhul vähendab tarneprognoosi siiski ainult vabastatud tellimused.

Taunitud koondplaneerimise mootor vähendab kõiki üleviimistellimuste olekuid, samas kui planeerimise optimeerimine vähendab prognoose ainult vabastatud olekus üleviimistellimuste *abil*.
