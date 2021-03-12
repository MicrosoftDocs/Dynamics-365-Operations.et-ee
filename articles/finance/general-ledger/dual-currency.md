---
title: Topeltvaluuta
description: Selles teemas antakse teavet topeltvaluuta kohta, kui kasutatakse rakenduses Microsoft Dynamics 365 Finance kasutatakse teise arvestusvaluutana aruandlusvaluutat.
author: kweekley
manager: AnnBe
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, Ledger, AssetTransReportingCurrencyAmountsWizard,BankAccountTransReportingCurrencyAmountsWizard, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 04126c0cddd1242e9607274e35f4b7626ad573d2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990460"
---
# <a name="dual-currency"></a>Topeltvaluuta

[!include [banner](../includes/banner.md)]

Rakenduse Microsoft Dynamics 365 for Finance and Operations versioonis 8.1 (oktoober 2018) kasutusele võetud funktsionaalsus võimaldab aruandlusvaluuta ümberkorraldamist ja teise arvestusvaluutana kasutamist. Sellele funktsioonile viidatakse ka kui *topeltvaluutale*. Topeltvaluuta muudatusi ei saa konfiguratsioonivõtme või parameetri kaudu välja lülitada. Kuna aruandlusvaluutat kasutatakse teise arvestusvaluutana, on aruandlusvaluuta arvestamise meetodi sisestusloogika muutunud.

Lisaks on täiustatud mitmeid mooduleid aruandlusvaluuta jälgimiseks, aruandluseks ja kasutamiseks erinevates protsessides. Mõjutatud moodulid on järgmised:

- Pearaamat 
- Finantsaruandlus 
- Ostureskontro
- Müügireskontro 
- Sularaha- ja pangahaldus 
- Põhivarad 
- Konsolideerimised

Pärast uuendamist peate täitma teatud sularaha- ja pangahalduse ning põhivara etapid. Seega lugege ja mõistke kindlasti selle teema asjakohaseid jaotisi.

## <a name="posting-process"></a>Sisestamise protsess

Kõigi pearaamatusse raamatupidamiskirjeid loovate kannete sisestamise loogika on muutunud. Aruandlusvaluuta arvutati eelnevalt järgmiselt.

Kandevaluuta summa \> Arvestusvaluuta summa \> Aruandlusvaluuta summa

Näiteks on kanne sisestatud valuutas Kanada dollar (CAD). CAD-summa teisendatakse arvestusvaluutasse, mis on USA dollar (USD). USD-summa teisendatakse siis aruandlusvaluutasse, mis on euro (EUR). Seega peavad CAD ja USD ning USD ja EUR vahel olema vahetuskursid.

Uus arvutuskäik on järgmine.

Kandevaluuta summa \> Arvestusvaluuta summa

Kandevaluuta summa \> Aruandlusvaluuta summa

Selle muutuse tõttu peavad nüüd CAD ja USD ning CAD ja EUR vahel olema vahetuskursid.

## <a name="reports-and-inquiries"></a>Aruanded ja päringud

Erinevad aruanded ja päringud näitavad nüüd nii aruandlusvaluuta summasid kui ka arvestusvaluuta summasid. Kõiki aruandeid ja päringuid ei ole uuendatud. Näiteks aruanded, mis näitavad summasid ainult kandevaluutas, ei ole muutunud.

Muudatused järgivad ühte kahest mustrist.

- Kui aruandes või päringus oli piisavalt ruumi summade näitamiseks nii arvestusvaluutas kui ka aruandlusvaluutas, lisati aruandlusvaluuta summad.
- Kui aruandes või päringus ei olnud piisavalt ruumi summade näitamiseks mõlemas valuutas, lisati valik, et kasutajad saaksid valida, millist valuutat näidatakse.

Erinevate aruannete ja päringute korral lisati ka loogika, kus aruandlusvaluuta summad peidetakse, kui aruandlusvaluuta on sama kui arvestusvaluuta, või kui juriidilise isiku pearaamatus ei olnud aruandlusvaluutat määratletud.

## <a name="financial-journals"></a>Finantstöölehed

Finantstöölehed nagu päevaraamat ja hankija arvete tööleht on uuendatud nii, et nad sisaldavad lisateavet aruandlusvaluuta kohta. Kande ja töölehe kogusummad kuvatakse nüüd aruandlusvaluutas. Lisaks kuvatakse nüüd aruandlusvaluuta vahetuskursi andmeid töölehe ridade vahekaardil **Üldine**. Seega saate kandeid sisestades aruandlusvaluuta vahetuskursi alistada.

## <a name="vendor-invoices-sales-orders-and-sales-agreements"></a>Hankijaarved, müügitellimused ja müügilepingud
Hankijaarved, müügitellimused ja müügilepingud on uuendatud, et kaasata aruandlusvaluuta jaoks fikseeritud vahetuskurss. Fikseeritud vahetuskurssi saab määratleda nii arvestusvaluuta kui ka aruandevaluuta puhul, kui kandevaluuta on erinev. Kui arvestusvaluuta ja aruandevaluuta on samad, hoitakse fikseeritud vahetuskurssi sünkroonis, kasutades aruandlusvaluuta fikseeritud määra arvestusvaluuta fikseeritud määrana. Selle konfiguratsiooni puhul ei saa muuta aruandlusvaluuta fikseeritud vahetuskurssi. Kui arvestusvaluuta ja aruandlusvaluuta erinevad, siis saab fikseeritud vahetuskurssi määratleda nii arvestusvaluuta kui ka aruandlusvaluuta puhul kandekirje ajal. Kui aruandlusvaluuta ei ole pearaamatus määratletud, pole väli **Aruandlusvaluuta fikseeritud vahetuskurss** lubatud ja ühtegi aruandlusvaluuta summat ei arvutata.

## <a name="module-changes"></a>Mooduli muudatused

Järgmised moodulid kasutavad aruandlusvaluutat teise arvestusvaluutana.

- [Pearaamat](#general-ledger)
- [Finantsaruandlus](#financial-reporting)
- [Ostureskontro](#accounts-payable-and-accounts-receivable)
- [Müügireskontro](#accounts-payable-and-accounts-receivable)
- [Sularaha- ja pangahaldus](#cash-and-bank-management)
- [Põhivarad](#fixed-assets)
- [Konsolideerimised](#consolidations)

### <a name="general-ledger"></a>Pearaamat

Kui pearaamatus oli aruandlusvaluuta määratud, jälgis pearaamat juba kõigi raamatupidamiskirjete aruandlusvaluuta summasid. Samas teisendatakse need summad nüüd kandevaluuta summadest.

Moodulile **Pearaamat** tehti järgmised lisamuudatused.

- Pearaamatus saab määratleda eraldi vahetuskursi tüübi aruandlusvaluutale. Kui organisatsioon ei soovi kasutada erinevat vahetuskursi tüüpi, võite aruandlusvaluuta vahetuskursi tüübi välja tühjaks jätta. Teise võimalusena saate valida sama vahetuskursi tüübi, mida kasutatakse arvestusvaluuta juures. Kui jätate välja tühjaks, kasutab süsteem arvestusvaluuta vahetuskursi tüüpi.
- Uus tööleht, aruandlusvaluuta korrigeerimise tööleht, võimaldab korrigeerimiste sisestamist pearaamatukontodele ainult aruandlusvaluutas. See tööleht lubab ainult pearaamatukontodele sisestamist.. See ei toeta kontsernisisest tööd ja valuuta peab olema selle juriidilise isiku aruandlusvaluuta, kus tööleht on sisestatud. Kui tööleht on sisestatud, on kandevaluuta ja arvestusvaluuta summad 0 (null) ning aruandlusvaluuta summa sisestatakse kandesse sisestatud summas. Kuna aruandlusvaluuta kasutamine moodulites **Ostureskontro**, **Müügireskontro** ja **Põhivara** on muutunud, saab seda töölehte pärast uuendamist korrigeerimiseks kasutada. Selle töölehe kasutamise näidete saamiseks vaadake nende moodulite jaotisi.
- Perioodi eraldamise protsess on uuendatud nii, et see eraldab kande-, arvestus- ja aruandlusvaluutade summad. Varem eraldati kande- ja arvestusvaluutade summad ja seejärel teisendati arvestusvaluuta summa aruandlusvaluutasse. Sellise käitumise tõttu võib pearaamatukontole jääda aruandlusvaluutas saldo. Kui nüüd summad arvutatakse ja konto kirjes kasutatakse, teisendust ei toimu.
- Välisvaluuta ümberarvutamise protsess arvutas summad juba aruandlusvaluutasse ümber. Siiski arvutatakse aruandlusvaluuta summat nüüd läbi kandevaluuta summa, nii nagu selles teemas eelnevalt jaotises [Sisestamise protsess](#posting-process) kirjeldati.
- Paljudes pearaamatu aruannetes ja päringutes oli juba aruandlusvaluuta, kuid mõnes ei olnud. Üheks selliseks näiteks on loendileht **Proovibilanss** loendilehe. See loendileht sisaldab nüüd nii arvestusvaluuta kui ka aruandlusvaluuta veerge. Pange tähele, et aruandlusvaluuta veerud on peidetud, kui arvestusvaluuta ja aruandlusvaluuta on samad või kui pearaamatus ei ole aruandlusvaluutat määratud.

### <a name="financial-reporting"></a>Finantsaruandlus

Moodul **Finantsaruandlus** võimaldab teil lisada aruandlusvaluuta summad finantsaruandele kahel viisil. Veerudefinitsioonis saate otse teatada pearaamatusse sisestatud aruandlusvaluuta summad (uus funktsionaalsus). Teise võimalusena võite jätkata summade teisendamist arvestusvaluutast aruandlusvaluutasse (olemasolev funktsionaalsus).

See muudatus on saadaval veerudefinitsiooni sätte **Valuutakuva** all. Kui valite **Aruandlusvaluuta pearaamatust**, veeru summasid ei teisandata. Selle asemel võetakse need otse pearaamatust. Kui soovite, et veerg näitaks teisendatud summasid, valige suvand **Teisenda valuutasse XXXX**, kus *XXXX* on aruandlusvaluuta, mida veerg peaks näitama. Sel juhul teisendatakse arvestusvaluuta summad valitud valuutasse kasutades olemasolevat teisendamise funktsionaalsust.

### <a name="accounts-payable-and-accounts-receivable"></a>Ostureskontro ja müügireskontro

Moodulid **Ostureskontro** ja **Müügireskontro** jälgisid juba aruandlusvaluuta summasid. Siiski ei näidatud ega kasutatud summasid erinevates protsessides. Tehti järgmised muudatused.

- Nüüd kuvatakse aruandlusvaluuta summad nii klientide kui hankijate kannetel. Aruandlusvaluuta summad kuvatakse ka iga kande avatud saldo jaoks.
- Ajalise jaotuse protsessi on uuendatud nii, et organisatsioon saab aegumisvahemikke näha nii arvestusvaluutas kui ka aruandlusvaluutas.
- Uuendati erinevaid päringuid ja aruandeid, et need näitaksid aruandlusvaluuta summasid. Näideteks on aruanded **Kliendi ja pearaamatu vastavusseviimine** ja **Hankija ja pearaamatu vastavusseviimine**.
- Välisvaluuta ümberarvutamise protsess arvutas summad juba aruandlusvaluutasse ümber. Siiski arvutatakse aruandlusvaluuta summat nüüd läbi kandevaluuta summa, nii nagu jaotises [Sisestamise protsess](#posting-process) kirjeldati.
- **Uuendamise kaalumine:** enne uuendamist arvutatakse dokumentide (arved, maksed, jne) aruandlusvaluuta summad läbi arvestusvaluuta. Näiteks, arve sisestatakse enne organisatsiooni uuendamist ja arve ei ole makstud. Uuenduse käigus arve raamatupidamiskirjet ei muudeta. Siiski, pärast uuendamist on topeltvaluuta muudatused jõustunud. Seetõttu, kui arve ära makstakse, arvutatakse nüüd makse aruandlusvaluuta summa kandevaluuta summa kaudu. Kui makse ja arve on tasakaalustatud, võidakse arvutada väike erinevus realiseeritud kasumi/kahjumi summas, sest aruandlusvaluuta summad arvutatakse nüüd erinevalt. Kui arvutatud erinevust peetakse oluliseks, saab realiseeritud kasumi/kahjumi ja ostureskonto/müügireskonto pearaamatukonto saldo korrigeerimiseks ainult aruandlusvaluutasse kasutada uut aruandlusvaluuta korrigeerimise töölehte.

### <a name="cash-and-bank-management"></a>Sularaha- ja pangahaldus

Eelnevalt ei jälginud moodul **Sularaha- ja pangahaldus** aruandlusvaluuta summasid kannetele, mis igale pangakontole sisestati. Pärast uuendamist jälgitakse mistahes uute sisestatud kannete aruandlusvaluuta summasid automaatselt. Siiski tuleb aruandlusvaluuta summad lisada alammooduli eelnevalt sisestatud kannetele.

- **Uuendamise kaalumine:** kuna pangakonto kanded ei jälginud varem alammooduli aruandlusvaluuta summasid, lisati viisard, et saaksite pangakonto kannetele aruandlusvaluuta summasid lisada. See viisard **ei** sisesta uuesti pearaamatusse. Selle asemel võtab see pearaamatust aruandlusvaluuta summad ja uuendab need alammooduli tabelites.

    - Viisardi käivitamiseks valige **Sularaha- ja pangahaldus** \> **Seadistus** \> **Aruandlusvaluuta summade lisamine pangakonto kannetele**.
    - Viisard kuvab kõigi käesoleva ettevõtte pangakontode kandeid, mille aruandlusvaluuta summa on 0 (null). Kaastakse ainult kanded, mis sisestati enne uuendamist.
    - Iga pangakonto kande jaoks leiab viisard vastavad pearaamatu raamatupidamiskirjed ja sisestab vaikimisi aruandlusvaluuta summa. Kuigi summasid saab redigeerida, soovitame, et te seda **ei** teeks. Vastasel korral ei pruugi olla võimalik pangakonto saldosid pearaamatuga vastavusse viia. Ainuke kord, millal peaksite summat muutma, on siis kui pearaamatust aruandlusvaluuta summat ei leita. Sel juhul näitab viisard, et aruandlusvaluuta summa on 0 (null).
    - Kui valite viisardis **Tühista**, salvestatakse kõik pangakonto kanded ja kõik aruandlusvaluuta summade muudatused kuni järgmise korrani, mil viisardi käivitate. Siiski ei uuendata pangakonto kannete aruandlusvaluuta summasid. See uuendus toimub ainult siis, kui valite viisardis **Lõpeta**. Te saate viisardit korduvalt kasutada. Seega saate parandada mistahes valed aruandlusvaluuta summad, kui olete teinud vea.

- Sularaha- ja pangahalduse protsesse ei muudetud, kuid uuendati erinevaid aruandeid ja päringuid, nii et need näitavad aruandlusvaluuta summasid. Erandiks on likviidsuse planeerimise aruanded. Neid ei uuendatud aruandlusvaluuta summasid sisaldama.

### <a name="fixed-assets"></a>Põhivarad

Eelnevalt ei jälginud moodul **Põhivara** iga põhivararaamatu kande aruandlusvaluuta summasid. Pärast uuendamist jälgitakse mistahes uute sisestatud kannete aruandlusvaluuta summasid automaatselt. Siiski tuleb aruandlusvaluuta summad lisada alammooduli eelnevalt sisestatud kannetele.

Lisaks tehti olulisi muudatusi kulumiarvestuse protsessis. Need muudatused nõuavad kasutajalt pärast uuendamist tegevusi. On oluline, et loete ja mõistate järgmiseid muudatusi, isegi kui te veel põhivara ei kasuta.

- Muutunud on see, kuidas kulumiarvestuse protsess määrab kindlaks aruandlusvaluuta summa. Järgnev stsenaarium võrdleb kuidas kulumiarvestus eelnevalt aruandlusvaluuta summa kindlaks määras ning kuidas see aruandlusvaluuta summat nüüd määrab.



    **Kulumi stsenaarium**

    Vara soetatakse ja sisestatakse järgmiste summadega. Pange tähele, et aruandlusvaluuta summa sisestatakse pearaamatusse, aga seda ei salvestada põhivara alammooduli tabelites.

    | Kande tüüp | Kandesumma | Valuutakurss | Arvestusvaluuta summa | Valuutakurss | Aruandlusvaluuta summa |
    |------------------|--------------------|---------------|----------------------------|---------------|---------------------------|
    | Soetus      | 1 000 000 taani krooni      | 2,0           | 500 000 USA dollarit                | 2,5           | 200 000 eurot               |

    **Eelnev kulumiarvestus aruandlusvaluutas**

    Aasta lõpus teostatakse kulumisoovitus ja see arvutab järgmised summad.

    | Kande tüüp | Kandesumma | Valuutakurss | Arvestusvaluuta summa | Valuutakurss | Aruandlusvaluuta summa |
    |------------------|--------------------|---------------|----------------------------|---------------|---------------------------|
    | Kulum     | 50 000 USA dollarit         | 1,0           | 50 000 USA dollarit                 | 2,6           | 19 230.77 eurot             |

    Kulumisoovituse teostamisel arvutab see arvestusvaluuta summa kasutades kulumiarvestuse meetodit. See summa teisendatakse aruandlusvaluutasse kasutades valuutade USD ja EUR vahetuskurssi. See teisendamine põhjustab probleeme, sest vara kuluarvestust ei saa aruandlusvaluutas täielikult teostada, kui kasutatakse hetkekurssi.

    **Uus aruandlusvaluuta kulumiarvestus**

    Kulumiarvestuse protsess on muudetud nii, et aruandlusvaluuta summa arvutatakse samuti kulumiarvestuse meetodit kasutades. Siin on vara kulumiarvestuse tulemused.

    | Kande tüüp | Kandesumma | Valuutakurss | Arvestusvaluuta summa | Valuutakurss                                                       | Aruandlusvaluuta summa |
    |------------------|--------------------|---------------|----------------------------|---------------------------------------------------------------------|---------------------------|
    | Kulum     | 50 000 USA dollarit         | 1,0           | 50 000 USA dollarit                 | 2,5<blockquote>[!NOTE] Kuigi seda vahetuskurssi näidatakse, ei kasutata seda aruandlusvaluutasse teisendamiseks.</blockquote> | 20 000 eurot                |

    Kulumisoovituse käivitamisel arvutab see välja nii arvestusvaluuta summa kui ka aruandlusvaluuta summa, kasutades kulumiarvestuse meetodit. Seejärel kasutatakse summasid pearaamatu raamatupidamiskirjes. Aruandlusvaluuta summa määramiseks ei kasutata teisendamist.

- **Uuendamise kaalumine:** kuna põhivararaamatu kanded ei jälginud varem alammooduli aruandlusvaluuta summasid, lisati viisard, et saaksite põhivararaamatu kannetele aruandlusvaluuta summasid lisada. See viisard **ei** sisesta uuesti pearaamatusse. Kuna kulumisoovituse aruandlusvaluuta summade arvutamine on muutunud, **peab** viisardit iga ettevõtte juures kasutama ja lõpetama enne kui organisatsioon saab mistahes kulumikandeid sisestada.

    - Viisardi käivitamiseks valige **Põhivara** \> **Seadistus** \> **Lisa aruandlusvaluuta summad põhivararaamatutele**.
    - Viisard kuvab kõigi käesoleva ettevõtte põhivara raamatute kandeid, mille aruandlusvaluuta summa on 0 (null). Kaastakse ainult kanded, mis sisestati enne uuendamist.
    - Viisard **ei** tõmba aruandlusvaluuta summasid pearaamatust. Nagu eelmises stsenaariums kirjeldatud, algselt pearaamatusse valesti sisestatud aruandlusvaluuta summad kasutasid hetkekurssi. Need summad ei tohiks olla põhivara alammoodulis, sest järgmine kulumiarvestus kasutab valesid summasid. Selle asemel leiab viisard esimese soetamise kuupäeva vahetuskursi. Seejärel kasutab ta seda vahetuskurssi, et soovitada aruandlusvaluuta summa, mis tuleks sisestada alammoodulisse. Näiteks võib viisard eelmise stsenaariumi järgi näidata järgmist.

        | Põhivara | Reserveerimine      | Kande tüüp | Kande kuupäev | Valuuta | Summa kandevaluutas | Summa  | Vahetuskurss | Aruandlusvaluuta summa |
        |-------------|-----------|------------------|------------------|----------|--------------------------------|---------|-----------|---------------------------|
        | BUIL-00001  | 200\_SLLT | Soetus      | 6/3/2016         | taani kroon      | 1 000 000                      | 500,000 | 2.5       | 250,000                   |
        | BUIL-00001  | 200\_SLLT | Kulum     | 6/3/2016         | USA dollar      | 50,000                         | 50,000  | 2.5       |  25,000                   |
        | BUIL-00001  | 200\_SLLT | Kulum     | 6/3/2016         | USA dollar      | 50,000                         | 50,000  | 2.5       |  25,000                   |
        | BUIL-00001  | 200\_SLLT | Kulum     | 6/3/2016         | USA dollar      | 50,000                         | 50,000  | 2.5       |  25,000                   |

    - Paljud kliendid jälgisid oma varade kannete üksikasju töövihikutes. Need üksikasjad sisaldavad vahetuskursse ja summasid. Kui teil on töövihikus need andmed, saate luua kohandatud vahetuskursi tüübi ja täiendada seda töövihikust pärit vahetuskurssidega. Seda vahetuskursi tüüpi kasutatakse seejärel soetamise kuupäeva vaikimisi vahetuskursi sisestamiseks ja aruandlusvaluuta summa arvutamiseks. Kui ühtki vahetuskursi tüüpi ei määratleta, kasutab viisard pearaamatus määratletud vahetuskursi tüüpi.
    - Vahetuskurssi ja aruandlusvaluuta summasid saab muuta. Vahetuskursi muutmisel arvutatakse aruandlusvaluuta summa uuesti kasutades uut kurssi.
    - Kui valite viisardis **Tühista**, salvestatakse kõik põhivara raamatu kanded ja kõik vahetuskursi või aruandlusvaluuta summade muudatused kuni järgmise korrani, mil viisardi käivitate. Siiski ei uuendata põhivara raamat kannete aruandlusvaluuta summasid. See uuendus toimub ainult siis, kui valite viisardis **Lõpeta**. Te saate viisardit korduvalt kasutada. Seega saate parandada mistahes valed aruandlusvaluuta summad, kui olete teinud vea.
    - Kui aruandlusvaluuta summad on alammoodulis täielikult uuendatud, **peate** seadistama **Kas olete kõik põhivara raamatu kannete aruandlusvaluuta summad uuendanud?** suvandi **Jah** peale ja seejärel valima **Lõpeta**. Kulumiarvestust ei saa lõpetada enne, kui määrate **Kas olete kõik põhivara raamatu kannete aruandlusvaluuta summad uuendanud?** suvandi **Jah** peale. Pärast suvandi seadistamist **Jah** peale ei ole viisard enam saadaval.
    - Pärast alammooduli põhivarakannete aruandlusvaluuta summade uuendamist ei kattu need summad algselt pearaamatusse sisestatud summadega. Siiski saab aruandlusvaluuta korrigeerimise töölehte kasutada pearaamatu kulumiarvestuse kirjete saldode uuendamiseks, et need vastaksid algselt sisestatud summadele.
    - **Andmehalduse** tööruumi lisatud uus üksus **Vara kande aruandlusvaluuta summad** laseb teil andmeid viisardist eksportida. Seejärel saate andmeid kasutada kulumikannetele põhivara alammooduli saldo määramiseks. Seejärel saab seda saldot kasutada aruandlusvaluuta korrigeerimise summa määramiseks pearaamatus.

- **Uuendamise kaalumine:** põhivarale on lisatud uued seadistusväljad ja neid kasutatakse kulumi arvutamisel. Teil võib olla vajalik neid välju enne järgmist kulumiarvestust uuendada.

    - Põhivara raamatus (**Põhivara** \> **Raamatud**) on FastTabil **Üldine** uus väli **Soetusmaksumus aruandlusvaluutas**.
    - Põhivara raamatus (**Põhivara** \> **Raamatud**) on FastTabil **Kulum** uus väli **Eeldatav mahakandmismaksumus aruandlusvaluutas**.
    - Põhivara parameetrites (**Põhivara** \> **Seadistus** \> **Põhivara parameetrid**) on FastTabil **Üldine** uus väli **Minimaalne kulumi summa aruandlusvaluutas**.
    - Raamatute (**Põhivara** \> **Seadistus** \> **Raamatud**) on FastTabil **Üldine** kaks uut välja: **Kulumi ümardamine aruandlusvaluutas** ja **Jäta arvestuslikuks jääkväärtuseks aruandlusvaluuta**.

- Kuna kulumisoovitus arvutab nüüd summad nii arvestusvaluutas kui ka aruandlusvaluutas, on põhivara tööleht nüüd uuendatud nii, et see näitab kulumisummasid aruandlusvaluutas. Kulumikannete korral on kande valuutaks alati arvestusvaluuta. Seetõttu kuvatakse need summad jätkuvalt veergudes **Deebet** ja **Kreedit**. Ruudustikku on lisatud kaks uut veergu, **Deebet aruandlusvaluutas** ja **Kreedit aruandlusvaluutas**.

    - Uued väljad on saadaval ainult siis, kui kande tüübiks on üks neljast kulumitüübist: **Kulum**, **Kulumi korrigeerimine**, **Plaaniväline kulum** või **Kulumi erihüvitis**.
    - Kui kulumi kande tüüp on põhivara töölehele sisestatud, kuvatakse uutes veergudes aruandlusvaluuta summasid. Neid summasid saab muuta.
    - Kui arvestusvaluuta ja pearaamatu aruandlusvaluuta on sama, hoitakse summasid sünkroonituna. Kui muudate **Kreediti** summa **Kreedit aruandlusvaluutas** all, muudetakse summa automaatselt sellele vastavaks.
    - Kui põhivara töölehele sisestatakse mistahes muu kandetüüp, ei näidata kunagi summasid **Deebet aruandlusvaluutas** ja **Kreedit aruandlusvaluutas**, ei enne ega pärast sisestamist. Arvestusvaluuta ja aruandlusvaluuta summad on siiski saadaval kandes, mis sisestatakse pearaamatusse.
    
### <a name="consolidations"></a>Konsolideerimised
    
Dynamics 365 Finance versioonis 10.0.5 (2019. aasta oktoober) saab funktsioone hallata funktsioonide halduse kaudu, et konsolideerimine ja topeltvaluuta oleksid veelgi paindlikumad. Selle funktsiooni lubamiseks minge tööruumi **Funktsioonide haldus** ja valige **Luba topeltvaluuta pearaamatu konsolideerimisel**.

Pearaamatu konsolideerimisel on nüüd võimalik konsolideerida lähteettevõtete arvestus- või aruandlusvaluuta summasid. Kui arvestus- või aruandlusvaluuta on sama, mis konsolideeritava ettevõte arvestus- või aruandlusvaluuta, siis summad kopeeritakse, selmet ümber arvutada.

-  Nüüd saate valida, kas kasutada lähteettevõtte arvestus- või aruandlusvaluutat konsolideeritava ettevõtte tehingu valuutana.

- Lähteettevõtte arvestus- või aruandlusvaluuta summad kopeeritakse ots konsolideeritava ettevõte arvestus- või aruandlusvaluuta summadele, kui üks neist on sama. Konsolideeritava ettevõte arvestus- ja aruandlusvaluuta summad arvutatakse vahetuskursi alusel, kui ükski neist valuutadest pole sama.
