---
title: Finantsanalüüs
description: Finantsülevaated kasutavad Microsoft Power BI-d finantsvaldkonna juhtimismõõdikute (KPI-de), diagrammide ja finantsaruannete koondamiseks.
author: kweekley
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 21d7d045c812c54d6776394ad9a0b025b55df8e1
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/01/2022
ms.locfileid: "9109108"
---
# <a name="financial-analysis"></a>Finantsanalüüs

[!include [banner](../includes/banner.md)]

**Finantsülevaated** kasutavad Microsoft Power BI-d finantsvaldkonna juhtimismõõdikute (KPI-de), diagrammide ja finantsaruannete koondamiseks. Power BI on rakendusse manustatud. Fookus **Finantsülevaadetes** on analüütilisel aruandlusel. Organisatsiooni isikud saavad seda vaadata, uurida, mõista ja tegutseda. 

**Finantsülevaated** ühendavad pearaamatu ja selle allammoodulid, et anda põhjalikumat ülevaadet organisatsiooni finantsseisu kohta.

> [!NOTE]
> See dokument kasutab järgmist Power BI terminoloogiat.
> 
> - **Aruanne** – üks PBIX-fail, kuhu kõigi vahekaartide visuaalid on salvestatud.
> - **Leht** – ühe PBIX-faili vahekaart. Iga leht võib sisaldada üht või mitut visuaali.
> - **Visuaal** – üks andmeallikas, näiteks kaart, KPI, diagramm, graafik, maatriks või finantsaruanne. Lehel, millel on visuaalina finantsaruanne, ei saa raporteeritava andmemahu tõttu olla rohkem visuaale.

**Finantsanalüüsi** tööruum keskendub olemasolevate aruannete andmete vaatamisele ja filtreerimisele. Tulevastes väljaannetes saate lisada uusi visuaale **finantsülevaadete** tööruumi. **Finantsanalüüsi** tööruum on saadaval nii praeguse ettevõtte kui ka kõigi ettevõtete jaoks, et näidata andmeid kõigi juriidiliste isikute kohta, olenemata sellest, millistele juriidilistele isikutele rollile juurdepääs on.

- [Visualiseeringute Power BI lisamine või redigeerimine armatuurlaudal](/powerapps/user/add-powerbi-dashboards)

## <a name="dynamics-365-finance-setup"></a>Dynamics 365 finantside häälestus
**Pearaamat**

Põhikonto tüüpi ja põhikonto kategooriaid kasutatakse **finantsülevaadete** **bilansi** finantsaruande ja paljude **kasumiaruande** finantsaruannete sobivate vaike- ja põhikontode täitmiseks.

Lehel **Põhikontod** peate määratlema oma põhikonto nii, et sellele on määratud üks järgmistest tüüpidest.

- Tulu
- Expense
- Varad
- Passiva
- Omakapital

Ärge määrake põhikontole muud tüüpi, näiteks **bilanss** või **kasum ja kahjum**. Aruandlus ei saa põhikonto tüüpi määrata, kui määratud on muid põhikonto tüüpe, kuna need ei ole piisavalt üksikasjalikud. Põhikonto tüüp peab olema määratud nii, et see näitaks kohustusi ja tulu finantsaruannetel positiivsete summadena.

Selleks, et põhikontot finantsaruannetel kuvataks jamuudele visuaalidele (nt KPI-d) kaasataks, tuleb igale põhikontole määrata põhikonto kategooria. Põhikonto kategooriaid on täiustatud nii, et need hõlmavad kuvamisjärjestust. Kuvamisjärjestust kasutatakse **finantsülevaadete** finantsaruannetel erinevalt. Pärast uue põhikonto kategooria redigeerimist või lisamist saate muuta **kuvamisjärjestuse** väärtust, et määrata järjekord, milles põhikonto kategooriaid finantsaruandel näidatakse. Kui peate muutma mitme põhikonto kategooria kuvamisjärjestust, saate muudatuste kiireks redigeerimiseks ja rakenduses avaldamiseks kasutada funktsiooni Ava Excelis.

## <a name="entity-store"></a>Üksuse kauplus
Andmed **Finantsülevaadeteks** tõmmatakse üksuse kauplusest (**Süsteemihaldus** \> **Seadistamine** \> **Üksuse kauplus**). Kui avate **CFO ülevaate** või **finantsülevaadete** tööruumi ja visuaalidel kuvatakse järgmine hoiatusteade, peate üksuseid uuendama.

![Hoiatus.](./media/Cantdisplay.png)

**Finantsülevaadete** tööruumide andmete nägemiseks peate uuendama järgmised üksused:

- Finantsaruandluse kandeandmete 3. versioon 
- Krediidihaldus ja võlanõuded V2
- LedgerCovLiquidityMeasurement
- Ostu kuup
- Müügi kuup

Üksustes olevate andmete korrapäraseks uuendamiseks saate määrata korduva partii. Kuna iga üksus luuakse uuenduse ajal täielikult uuesti, valige üksuste uuendamise aega ja sagedust hoolikalt. Finantsülevaadete jaoks kasutatav peamine üksus on FinancialReportingTransactionData. Seetõttu võite otsustada seda üksust sagedamini uuendada.

## <a name="security"></a>Turve
Praegu ei saa Power BI aruannete andmeid manustada juriidilistele isikutele, millele kasutajal on juurdepääs. Seetõttu juhitakse manustatud Power BI aruandeid turbeseadistuste kohustuste kaudu. Määratletud kohustused annavad juurdepääsu kõikidele juriidilistele isikutele või ainult aktiivsele ettevõttele. Järgmine tabel näitab olemasolevaid kohustusi ja rolle, millele need on määratud. Kohustusi saab eemaldada või määrata erinevatele rollidele teie ettevõtte vajaduste järgi.

| Lõiv                                    | Rollid | Kirjeldus |
|-----------------------------------------|-------|------------|
| Praeguse ettevõtte finantsülevaadete vaatamine | <ul><li>Raamatupidaja</li><li>Pearaamatupidaja</li><li>Raamatupidaja</li><li>Audiitor</li><li>Eelarvehaldur</li><li>Tegevjuht</li><li>Finantsdirektor</li><li>Finantskontroller</li></ul> | See kohustus võimaldab juurdepääsu finantsülevaatele. Vaikimisi kasutatakse filtrina aktiivset ettevõtet. Teisi juriidilisi isikuid ei saa lisada. |
| Kõikide ettevõtte finantsülevaadete vaatamine   | Finantsis Microsoft Dynamics 365, Enterprise edition 7.3, pole see kohustus määratud rollile. Järgmises väljaandes määratakse see kohustus finantsdirektori rollile. | See kohustus võimaldab juurdepääsu CFO ülevaate tööruumi menüükäsule. Vaikimisi kasutatakse filtrina aktiivset ettevõtet. Sellegipoolest saate lisada kõik juriidilised isikud, sõltumata sellest, kas kasutajal on juurdepääs teistele juriidilistele isikutele. |


## <a name="financial-reporting-vs-financial-analysis"></a>Financial reporting vs. finantsanalüüs
Kuigi **finantsanalüüs** hõlmab finantsaruandeid, ei asenda see Financial reporting rakendust. Vaike **Finantsülevaadete** finantsaruannete ulatus on piiratud ega hõlma igat tüüpi finantsaruanded. Finantsaruandlus on siiski seaduslike finantsaruannete kavandamise ja loomise peamine tööriist.

Järgmine võrdlusdiagramm selgitab kahe võimaluse vahelisi erinevusi.


| Funktsioon                                                   | Financial Reporting                                               | Finantsanalüüs |
|----------------------------------------------------------|-------------------------------------------------------------------|--------------------|
| **Vaikearuannete redigeerimine**                                 | Jah                                                               | Ei |
| **Uute aruannete loomine**                                   | Jah                                                               | Ei |
| **Prindi aruanded**                                        | Jah                                                               | Ei |
| **Excelisse eksportimine**                                      | Jah                                                               | Limiteeritud Toorandmete Excelisse eksportimine, mitte vormindatud aruanne |
| **Aruandluse hierarhia / organisatsiooni hierarhia toetamine**   | Jah                                                               | Ei |
| **Alammoodulite andmete kuvamine**                             | Jah Limiteeritud ainult hankijale, kliendile                              | Jah Hankija, klient, hankija-/kliendigrupid, hankija/kliendi aadressid jne |
| **Aruandlusvaluuta**                                   | Jah Arvestusvaluuta ja aruandlusvaluutasse teisendamine       | Ei Ainult arvestusvaluuta |
| **Turve**                                             | Jah Järgib rakendust Rahandus ja aruandluspuu turvet | Piiratud kuva aruanded kõigi ettevõtete kohta (sõltumata finantside ja toimingute turvalisusest) või ainult aktiivse ettevõtte kohta |
| **Eri kontoplaanide ja rahandusaastate toetamine** | Jah                                                               | Ei |
| **välisandmete aruanne**                              | Ei                                                                | Ei |
| **Konsolideerimiste toetamine**                               | Jah                                                               | Limiteeritud Võimaldab aruandlust mitmele ettevõttele, aga kasutab ainult arvestusvaluutat |

Saadaval on järgmised finantsaruanded.

- Proovibilanss
- Bilanss
- Kasumiaruanne piirkonna järgi
- Kasumiaruanne – tegelik vs eelarve
- Hälvetega kasumiaruanne
- 12 kuu trendi kasumiaruanne
- Kulude kolme aasta trend
- Kulud hankija järgi
- Müük kliendi järgi

## <a name="edit-visuals"></a>Visuaalide redigeerimine
Eelmistes **Finantsülevaadete** väljaannetes, ei saanud visuaale redigeerida. Tulevastes väljaannetes saavad sobivate turbeõigustega kasutajad luua uusi visuaale ning olemasolevaid kopeerida ja redigeerida. Kuigi aruandeid sisaldavad PBIX-failid on allikatena kättesaadavad, ei soovita me vaikearuandeid redigeerida. Lisamuudatusi tehakse finantsaruannete loomiseks kasutatavale andmemudelile, vaikearuannetele ja kohandatud finantsaruannete visuaalile. Seetõttu peate järgmise väljaande uute funktsioonide ja muudatuste kasutamiseks Microsoft Power BI Desktop kaudu vaikearuannetele tehtud muudatused uuesti tegema.

## <a name="filtering"></a>Filtreerimine
Kasutajad saavad aruannet filtreerida vasakul asuva paani **Filter** abil. See paan on sama, mis Power BI Desktopi kaudu saadaolev paan. Filtreerimisel on eri tasemed, millest mõni ei pruugi olla saadaval olenevalt sellest, milliseid valikuid olete lehel (vahekaardil) teinud või kas kasutate süvitsimineku funktsiooni.

- **Aruandetaseme filtrid** – neid filtreid rakendatakse kõigi lehtede (vahekaartide) kõigile visuaalidele.
- **Lehetaseme filtrid** – neid filtreid rakendatakse aktiivse vahekaardi kõigile visuaalidele. Neid filtreid rakendatakse aruandetaseme filtritele lisaks.
- **Visuaalitaseme filtrid** – neid filtreid rakendatakse ainult valitud visuaalile. Neid filtreid rakendatakse lehetaseme filtritele lisaks.
- **Süvitsimineku filter** – see filter filtreerib lähtevisuaalist, mida rakendatakse praegusele visuaalile süvaaruande loomisel lähtevisuaalist praegusele visuaalile.

![Filtreerimissuvandid.](./media/filter.png)

Konkreetse filtriväärtuse eemaldamiseks valige selle kõrval asuv kustutuskummi sümbol. Ärge eemaldage filtrit, valides sümboli X. Sümboli X valimisel eemaldatakse filtreeritav väli filtrisuvandite hulgast. Kui eemaldate välja filtrist kogemata, sulgege tööruum ja avage see uuesti. Vaikefiltri sätted rakendatakse uuesti.

Vaikimisi kasutatakse tööruumide esmakordsel avamisel aruandetasandi filtrina aktiivset juriidilist isikut. Olenevalt kasutajate turbeõigustest võib neil olla võimalik lisada teisi juriidilisi isikuid või muuta filtris vaikimisi valitud juriidilist isikut.

Filter **Rahanduskalender** on kohustuslik, et visuaali jaoks kasutataks õiget kalendrit. Vaikimisi määratakse aktiivse juriidilise isiku rahanduskalendrile aruandetaseme filter. Filtri muutmisel muu algus- või lõppkuupäevaga rahanduskalendrile algsaldosid ei kaasata. Seetõttu ei näita **bilansi** finantsaruanded õigeid saldosid. Filtris täiendava rahanduskalendri valimisel saate täiendava veergudekogumi. Iga täiendava veergudekogum näitab eri rahanduskalendri summasid.

Kohustuslik on ka filter **Sisestamiskiht**. Vaikimisi on filtri tüübiks määratud Praegune. Koondsummade kuvamiseks saate filtril valida täiendavaid sisestamiskihte.

Filtrid on saadaval ka väljade **Kuupäev** ja **Rahandusaasta** jaoks. Neid filtreid rakendatakse tavaliselt lehetasemel. Vaikimisi kasutab filter **Kuupäev** suhtelist kuupäeva, mida saate muuta. Suhtelise kuupäevafiltri saate ka eemaldada ja kasutada selle asemel filtrit **Rahandusaasta**.

## <a name="currency"></a>Valuuta

Kõik pearaamatu andmetes kuvatavad visuaalid näitavad summasid arvestusvaluutas. Seetõttu peate juriidilise isiku filtreerimisel kaasama ainult juriidilised isikud, kes kasutavad on sama arvestusvaluutat. Vastasel korral on koondate erinevates valuutades andmeid.

Kõik alammoodulite andmeid kuvavad visuaalid, nagu **Likviidsuse planeerimine** ja **10 parimat**, näitavad summasid süsteemi valuutas. Süsteemi valuuta ja süsteemi vahetuskursi tüüp on määratletud lehel **Süsteemiparameetrid**.

Visuaal **Saldo pangakonto järgi** kasutab summasid pangakonto valuutas.

## <a name="dimensions"></a>Dimensioonid

Vaike-finantsaruanded ei hõlma ühtegi finantsdimensiooni, vaid keskenduvad ainult põhikontole. Finantsdimensioonide toetus on saadaval tulevastes väljaannetes, mille aruandeid saab redigeerida. Seejärel saavad organisatsioonid finantsdimensiooni väärtusi filtreerida.

Mõned finantsdimensioonid sisaldavad dimensioone, mis põhinevad alammooduli kannetel. Uue finantsaruande eesmärk on võimaldada filtreerimist dimensioonides, mis ei ole finants dimensioonideks seadistatud. Näiteks võimaldab vaikearuanne Kulud hankija järgi laiendada põhikontost kaugemale, nii et saate vaadata saldosid hankija kaupa. Hankija ei ole seadistatud finantsdimensioonina. Selle asemel naaseb süsteem hankija leidmiseks algse alammooduli kande juurde.

Vaikearuannetes kasutatakse järgmisi dimensioone. Ükski neist dimensioonidest ei ole finantsdimensioonid.

- Tarnija
- Tarnijagrupp
- Klient
- Kliendigrupp
- Riik/regioon
- Osariik/provints
- Linn

> [!IMPORTANT] 
> Kui summeerite mitme hankija või kliendi kanded ühte kandesse finantstöölehtede abil, on andmed valed. Aruandlusprotsess ei suuda määrata, milline hankija või klient on töölehe sisestusel seotud konkreetse pearaamatukontoga, kuna seda teavet ei säilitata kusagil. Seetõttu ei soovita me sisestada ühte kandesse mitut hankijat, klienti, põhivara või projekti.

## <a name="drill-on-data"></a>Andmetega süvitsiminek

Power BI kaudu on saadaval süvitsimineku eri tasemed. Igal tasemel on oma nimi funktsioon. Süvitsi saate minna ka ridade ja veergudega. See jaotis käsitleb erinevaid valikuid, kasutades näitena finantsaruannet **Proovibilanss** ja näidates, kuidas ridadega süvitsi minna. Sama funktsioon on olemas ka veergude jaoks. Peate muutma sätet **Mine süvitsi üksusega**.

Järgmisel joonisel on aruanne **Proovibilanss** ahendatud reahierarhia kõrgeimale tasemele – põhikonto tüübile.

![Proovibilansi väljavõte.](./media/trial-balance.png)

Hierarhia järgmise taseme (põhikonto kategooriad) vaatamiseks saate välja **Mine süvitsi üksusega** väärtuseks määrata **Read** ja valida seejärel nupp **Laienda** (kolmas nupp väljast Mine süvitsi üksusega). Nüüd näete põhikonto kategooriad laiendatuna. Praegu ei luba Power BI teil laiendada ainult üht rida või veergu ning samal ajal näha kõiki teisi ridu ja veerge.

![Proovibilansi ridadesse süvitsi minek.](./media/trial-balance2.png)

Kõigi ridade põhikontode laiendamiseks saate uuesti kasutada nuppu **Laienda**. Põhikontodega süvitsi minekuks ainult ühe rea kaupa valige aga esmalt nupp **Mine süvitsi** (akna paremal pool asuv üksik allapoole osutav nool) ja valige seejärel rida, millega süvitsi minna. Järgmisel joonisel on kujutatud tulemus, kui pärast nupu **Drill Down** valimist on valitud rida **Müük**.

![Proovibilansi laiendamise nupp.](./media/trial-balance3.png)

Pärast ühe reaga süvitsiminekut tuleb täielikule proovibilansile naasmiseks teha mitu klõpsu. Nupp **Mine üldiseks** (Esimene nupp pärast välja **Mine süvitsi üksusega**) läheb üldiseks ainult kategooria **Müük** kontekstis, nagu alloleval pildil on näidatud.

![Proovibilansi üldiseks minemise nupp.](./media/trial-balance4.png)

Nuppu **Mine üldiseks** saate kasutada ridade kõrgeima taseme summeerimise juurde naasmiseks.

Power BI-l on ka nupp, mille abil saate hierarhia järgmisele tasemele liikuda (teine nupp pärast välja **Mine süvitsi üksusega**). Selle nupu mõju erineb nupu **Laienda** (kolmas nupp pärast välja **Mine süvitsi üksusega**) mõjust, mida kasutatakse hierarhia laiendamiseks. Hierarhia laiendamisel säilitatakse hierarhia aruandel. Nagu näitasime ka varem, siis kui laiendate näiteks põhikonto tüüpi, näete aruandel ikka põhikonto tüüpi. Kui aga lähete hierarhia järgmisele tasemele, ei näita aruanne enam hierarhia ülemüksust, nagu on näha järgmisel pildil.

![Proovibilansi süvenemisest naasmise nupp.](./media/trial-balance5.png)

Summeeritud saldote taga olevate kande üksikasjade vaatamiseks saate rakendusse Financial and Operations tagasi minna, valides mõned summad.

Finantsaruannetes süvitsi minemine viib teid lehele Arveldusallika uurija, mitte kannete juurde. Arveldusallika uurija ei kuva raamatupidamiskirjeid ainult pearaamatus. Selle asemel kuvab see alammooduli kande üksikasjad. Seetõttu saate algse kande kohta palju täpsemat teavet ning saate kasutada seda analüüsimiseks. Näiteks näete, kes oli hankija või klient, mida klient ostis või hankija müüs ning ka kandel olevat projekti.

Järgmised finantsaruannete filtrid saadetakse Arveldusallika uurijale ning Arveldusallika uurija kuvab koondatud tehingud.

Filtreerimiseks on kohustuslikud järgmised väljad.

- Juriidiline isik
- Rahanduskalender
- Aasta
- Põhikonto ID

Filtreerimiseks on valikulised järgmised väljad.

- Kvartal
- Kuu
- Periood

Kui te ei laienda real piisavalt kaugele, siis süvitsiminek ei tööta. Kui te laiendate näiteks ainult põhikonto kategooriani, ei saa te süvitsi minna saldo arveldusallika uurijani, sest arveldusallika uurijas filtreerimiseks on kohustuslik põhikonto väli.

Kui laiendate real liiga kaugele, ei saadeta finantsaruannetel olevaid lisafiltreid arveldusallika uurijale. Seetõttu võib arvud erineda. Näiteks kui laiendate finantsaruande Kasumiaruanne piirkonna järgi ridadel riigi või piirkonnani, ei kaasata riiki või piirkonda arveldusallika uurijas filtrina.

> [!NOTE]
> Finantsaruande ridadel või veergudel saate kaugemale süvitsi minna, kui Arveldusallika uurija praegu filtreerimiseks toetab. Seetõttu ei vasta mõnes olukorras arveldusallika uurija üksikasjalike kannete summa saldole, mille osas süvitsi lähete. Seda funktsiooni täiustatakse tulevikus edasi.

## <a name="hierarchies"></a>Hierarhiad

Vaike-finantsaruanded kasutavad andmetega süvitsiminekuks ja nende laiendamiseks kaht hierarhiat. Üks hierarhia on ridade ja teine veergude kohta. Mõlemad hierarhiad on finantsaruande kavandis eelmääratletud. Enamiku finantsaruannete puhul on reahierarhia järgmine: **Põhikonto tüüp** \> **Põhikonto kategooriad** \> **Põhikonto**. Mõnel aruandel on aga lisaväljad, näiteks Riik ja Piirkond. Hierarhia lisasõlmed põhinevad iga kande alammooduli andmetel.

Veergude puhul keskendub hierarhia juriidilistele isikutele ja rahandusperioodidele. Enamiku finantsaruannete puhul on veeruhierarhia järgmine: **Juriidiline isiku** \> **Rahanduskalender** \> **Rahandusaasta** \> **Kvartal** \> **Periood**.

Praegu ei toeta finantsaruanded organisatsiooni hierarhiaid, mis võimaldavad andmeid koondada.

## <a name="data-limitations"></a>Andmepiirangud
Finantsaruande visuaalidel kuvatavate ridade arvul on piirang. Praegu on see piirang 30 000. Selle piirangu ületamisel kuvatakse visuaalil hoiatussümbol, mis teavitab olukorrast.

![Andmepiirangud.](./media/data-limit.png)

Kui maksimumpiir ületatakse, on finantsaruandel kuvatud kogusummad valed, kuna visuaalile ei laaditud kõiki ridu.

### <a name="empty-rows"></a>Tühjad read
Power BI-l ei ole tühjade ridade peitmise või kuvamise valikut. Kui real ei ole andmeid, ei kuvata seda visuaalil.


## <a name="additional-resources-for-power-bi"></a>Power BI lisaressursid

Järgmiste ressursside teave ei ole kohustuslik **finantsülevaadete** tööruumi manustatud aruannete lubamiseks tootmiskeskkonnas. Selle asemel on need kasulikud arendusväljade jaoks ja juhul, kui soovite oma Power BI aruandeid manustada.

- [Analüütikatööruumidele ja aruannetele juurdepääs valmiskeskkonnas](/archive/blogs/dynamicsaxbi/accessing-analytical-workspaces-on-1box-environment)

- [Analüütika lisamine tööruumidele teenuse Power BI Embedded abil](/dynamics365/unified-operations/dev-itpro/analytics/add-analytics-tab-workspaces)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

