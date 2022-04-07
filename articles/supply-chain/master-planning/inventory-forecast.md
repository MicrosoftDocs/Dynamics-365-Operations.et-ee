---
title: Varude prognoosid
description: Selles teemas kirjeldatakse pakkumise ja nõudluse prognoosi funktsioone, mida saab kasutada Varude prognooside loomiseks rakenduses Microsoft Dynamics 365 Supply Chain Management.
author: t-benebo
ms.date: 06/08/2021
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ForecastSales, ForecastPurch, ForecastInvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: abc827139c71f7942335cd2b7e2c7502f7fc1cfe
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469366"
---
# <a name="inventory-forecasts"></a>Varude prognoosid

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas vaadata ja luua varude prognoose. Saate luua ja vaadata kaupade, kaubagruppide, kauba eraldamisvõtmete, kliendikontode, kliendigruppide, hankijakontode ja hankijagruppide pakkumise ja nõudluse prognoosi ridu.

Saate valida iga rea jaoks prognoosmudeli, mida kasutatakse. Seejärel saate määrata kauba või kaubagrupi, millele on lisatud kogus või kandesumma. Saate prognoosi eraldamiseks määrata ka ajahorisondi ja ajaintervallid.

Pakkumise ja nõudluse prognoosi read annavad varude prognoosi sama kaubakombinatsiooni ja mudeli jaoks. Varude prognoos kajastab samale kaubale sisestatud pakkumise ja nõudluse vahelist saldot. Seda ei saa muuta. Varude prognoos aitab laohalduse töörühmal üle vaadata eeldatavad muudatused kauba vabas kaubavarus prognoositud eeloleval perioodil.

Kui on seadistatud, saate materjalide ja tarnevõimsuse brutovajaduste arvutamiseks ning plaanitud tellimuste loomiseks käivitada eelplaneerimise.

## <a name="view-and-manually-enter-forecast-lines"></a><a name="manual-entry"></a>Saate vaadata ja käsitsi sisestada prognoosi ridu

Kasutage seda protseduuri toodetele manuaalselt prognoosiridade lisamiseks.

Eelarveridade loomiseks on ka teisi viise:

- [Statistilise alusprognoosi loomine](generate-statistical-baseline-forecast.md).
- [Nõudluse prognooside ajalooliste andmete importimine](import-historical-data.md).
- [Prognoosi loomiseks kasuta Microsoft Azure masinõppe veebiteenust](demand-forecasting-setup.md).
- [Importige nõudluse või pakkumise prognoosi read andmehalduse raamistiku abil (ForecastDemandForecastEntryStaging ja ForecastSupplyForecastEntryStagingi andmeüksused)](../../dev-itpro/data-entities/data-entities-data-packages.md).

Nagu 1. sammu tabel näitab, on kasutusel lehtedele juurdepääsuks eri viise.

1. Sõltuvalt üksuse tüübist, millele soovite prognoosi luua ja sellest, mis tüüpi eelarvet soovite luua, avage pakkumine, nõudlus või varude eelarve leht, nagu kirjeldatud järgmises tabelis.

    | Üksus | Juhised |
    |---|---|
    | Väljastatud tooted | <ol><li>Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.</li><li>Valige toode, mille jaoks eelarvet luua.</li><li>Valige tegevuspaani vahekaardil **Plaan** jaotises **Prognoos** suvand **Nõudluse prognoos**, **Tarneprognoos**, **Varude prognoos** sõltuvalt tüübist, millist eelarvet soovite kasutada.</li></ol> |
    | Väljastatud tootevariandid | <ol><li>Avage **Tooteteabe haldus \> Tooted \> Väljastatud tootevariandid**.</li><li>Valige variant, mille jaoks eelarvet luua.</li><li>Valige tegevuspaani vahekaardil **Plaan** jaotises **Prognoos** suvand **Nõudluse prognoos**, **Tarneprognoos**, **Varude prognoos** sõltuvalt tüübist, millist eelarvet soovite kasutada.</li></ol> |
    | Kaubagrupid | <ol><li>Avage **Varude haldus \> Seadistus \> Varud \> Kaubagrupid**.</li><li>Valige toote grupp, mille jaoks eelarvet luua.</li><li>Valige tegevuspaani vahekaardil **Plaan \> Nõudluse prognoos**, **Prognoos \> Tarne prognoos** või **Prognoos \> Varude prognoos** sõltuvalt tüübist, millist eelarvet soovite kasutada.</li></ol> |
    | Kauba eraldamisvõtmed | <ol><li>Avage **Varude haldus \> Seadistus \> Eelarve**.</li><li>Prognoosi loomiseks valige üksuse jaotusvõti.</li><li>Valige toimingupaanil **Nõudluse prognoos**.</li></ol> |
    | Kliendid | <ol><li>Avage **Koondplaneerimine \> Prognoosimine \> Käsitsi prognoosisisend \> Kliendid**.</li><li>Valige toode, mille jaoks eelarvet luua.</li><li>Valige toimingupaanil **Defineeri nõudluse prognoos**.</li></ol> |
    | Kliendigrupid | <ol><li>Avage **Koondplaneerimine \> Prognoosimine \> Käsitsi prognoosisisend \> Kliendigrupid**.</li><li>Valige kliendigrupp, mille jaoks eelarvet luua.</li><li>Valige toimingupaanil **Defineeri nõudluse prognoos**.</li></ol> |
    | Hankijad | <ol><li>Avage **Koondplaneerimine \> Prognoosimine \> Käsitsi prognoosisisend \> Hankijad**.</li><li>Valige hankija, kelle jaoks eelarvet luua.</li><li>Valige toimingupaanil **Sisesta** leht **Tarne prognoos** avamiseks.</li></ol> |
    | Hankijagrupid | <ol><li>Avage **Koondplaneerimine \> Prognoosimine \> Käsitsi prognoosisisend \> Hankegrupid**.</li><li>Valige hankija grupp, mille jaoks eelarvet luua.</li><li>Valige toimingupaanil **Sisesta** leht **Tarne prognoos** avamiseks.</li></ol> | 
    | Kõik read | <ul><li>Minge **Koondplaneerimine \> Prognoos \> Nõudluse prognoosi read** või **Koondplaneerimine \> Prognoos \> pakkumise prognoosi read** sõltuvalt sellest, millise tüübiga soovite töötada.</li></ul> |

    Sõltuvalt valikust kuvatakse **Pakkumise prognoosi** või **Nõudluse prognoosi** leht. See näitab mis tahes olemasolevaid eelarveridu kirje kohta, mille valisite enne lehekülje avamist.

1. Prognoosi rea lisamiseks lehe ülaossa valige tegevuspaanil suvand **Uus**.
1. Valige uue rea väljal **Mudel**, et kasutadda eelarvemudelit. Seejärel sisestage nõutavad üksikasjad, nt kaup, kaubagrupp, kliendi- või hankijakonto või -grupp, kauba kogus või kande kogusumma. **Pakkumise prognoosi** ja **nõudluse prognoosi** lehtedel täielike saaddaval olevate üksikasjade saamiseks vaadake selle teema hilisemaid jaotisi.
1. Eelarve jaotamiseks perioodi peale valige vahekaardil **Ülevaade** tööriistaribal **Eralda eelarve**.
1. Seadistage väljade **Eraldama** abil ajahorisont ja ajaintervallid, mida kasutatakse eelarvekoguste jaotamiseks.

## <a name="supply-forecast-lines"></a>Tarneprognoosi rida

Tarneprognoos võimaldab teil luua plaani ostetud kaupadele. See teavitab hanke- ja ametnikele, mida nad eeldatavalt tellivad.

Tarneprognoosi saate sisestada kauba, kaubagrupi, kauba eraldusvõtme, hankija ja hankijagrupi kaupa. Teavet kõigi **tarneprognoosi** lehe erinevate üksuste ja kirjete jaoks avamiseks [vt selles prognoosiridade vaatamise ja käsitsi sisestamise jaotisest](#manual-entry) selles teemas eespool.

**Tarneprognoosi** lehe ülemine osa pakub tarneprognoosi ridade ruudustikku ja vahekaartide kogu, mida saate kasutada valitud eelarverea lisateabe vaatamiseks ja häälestamiseks. Lehe alumises osas on **Jaotis** ruudustik.

Järgmised alamjaotised kirjeldavad kõiki igal vahekaardil saadaolevaid välju ja kõiki käske, mis on saadaval lehekülje toimingupaanil ja tööriistariba **Ülevaade** vahekaardil.

### <a name="action-pane-commands-on-the-supply-forecast-page"></a>Tegevuspaani käsud tarneprognoosi lehel

Järgmises tabelis kirjeldatakse lehe **Tarneprognoosi** toimingupaanil olevaid käske.

| Käsk | Kirjeldus |
|---|---|
| Salvesta | Salvestage praegused sätted. |
| Redigeeri | Saate lubada lehekülje sätete redigeerimise. |
| New | Lisage prognoosi rida ülemisele ruudustikule. |
| Kustutamine | Saate valitud eelarverea ülemist ruudustikku eemaldada. |
| Prognoosisaldod | Saate vaadata praeguse rahandusaasta valitud rea mudeli ID jaoks arvutatud eelarvesaldosid. Saldod jagatakse perioodi (kuu) järgi. |
| Likviidsuse planeerimine | Saate vaadata pearaamatule eraldatud eelarvekandeid. Lisateavet vt teemast [Rahavoo planeerimine](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| Varud \> Kuva dimensioonid | Saate valida vahekaardil **Ülevaade** kuvatavas ruudustikus kuvatavad varude dimensioonid. |

### <a name="toolbar-commands-on-the-overview-tab-of-the-supply-forecast-page"></a>Tööriistariba käsud tarneprognoosi lehe ülevaate vahekaardil

Järgmises tabelis kirjeldatakse käske toimingupaanil lehel **Ülevaade** vahekaardil **Tarneprognoos**.

| Käsk | Kirjeldus |
|---|---|
| Eralda prognoos | Kui kasutate eraldamismeetodit, looge eelarvekandele individuaalsed graafiku read. Rea kogus jaotatakse seejärel kuupäeva (vastavalt valitud ajaintervallidele), koguse ja kogu ajavahemiku summa järgi. (Vaata [Määrake eelarve](#allocate-forecast) sektsioon selles teemas hiljem.) |
| Hulgivärskendamine | Saate avada **Eelarvekannete redigeerimine** lehe. (Vt [Eelarvekannete hulgivärskendus](#bulk-update) sektsioon selles teemas hiljem.) |
| Varude prognoos | Saate avada valitud **varude eelarve** lehe, mis on filtreeritud valitud toote/mudeli kombinatsioon. (Vt [Varude eelarve](#inventory-forecast) sektsioon selles teemas hiljem.) |
| Loo kaubavajadus | Saate avada dialoogiboksi, kus saate luua kauba vajadusi ning projektiga seotud eelarvekannete jaoks müügitellimusi või kaubatöölehe ridu. Kuigi see käsk on saadaval nii tarneprognoosi ridade kui ka nõudluse prognoosi ridade jaoks, ei saa seda kasutada **tarneprognoosi** lehel. |

### <a name="the-overview-tab-on-the-supply-forecast-page"></a>Tööriistariba käsud tarneprognoosi lehe ülevaate vahekaardil

Järgmises tabelis kirjeldatakse väljasid **Ülevaate** vahekaardil **Tarneprognoosi** lehel.

| Field | Kirjeldus |
|---|---|
| **Mudel** | Kandega seotud eelarvemudel. |
| **Kuupäev** | Kande alguskuupäev. |
| **Hankija konto** | Kandega seostatud hankijakonto. |
| **Hankijagrupp** | Kandega seostatud hankijakonto grupp. |
| **Kaubakood** | Kauba identifikaator. |
| **Kaubagrupp** | Kandega seotud kaubagrupp. |
| **Kauba eraldamisvõti** | Kauba eraldusvõti, mis on eelarvega seotud. |
| **Tegeliku kaalu kogus** | Eelarve kogus määratud tegeliku kaalu ühikus. |
| **Tegeliku kaalu ühik** | Saagi kaaluühik, milles toode on ostetud. Väärtus tuuakse automaatselt kauba seadistusest. |
| **Kogus** | Prognoositav kogus määratud ostuühikus. |
| **Üksus** | Prognoositav arv määratud ostuühikus. Väärtus tuuakse automaatselt kauba seadistusest. Ühikuteisenduste häälestamisel saate seda siiski muuta. |
| **summa** | Brutosumma, miinus allahindlused, mida prognoositav tehing prognoosida aitab. |
| **Currency** | Prognoositava tehingu jaoks kasutatav valuuta. Valuuta sisestatakse automaatselt, kuid kasutaja saab valida mõne muu valuuta. |
| (Muud mõõtmed) | Täiendavaid dimensioone saab kuvada võrgustiku veergudena. Valige toimingupaanil üksus **Kuva dimensioonid**, et valida lisadimensioon, mida kuvatakse. |

### <a name="the-general-tab-on-the-supply-forecast-page"></a>Lehe Tarneprognoos vahekaart Üldine

Vahekaardil **Üldine** kuvatakse lisateavet praegu valitud rea **Ülevaade** kohta. Osa sellest teabest korratakse vahekaardil **Ülevaade**. Järgmises tabelis kirjeldatakse vahekaardi **Üldine** kordumatuid välju.

| Field | Kirjeldus |
|---|---|
| Aruanne | Kande lisamiseks aruandesse märkige see valik *Jah*. |
| Kommentaarid | Siia saate sisestada eelarvekandega seotud kommentaarid. |
| Aktiivne | Kande lisamiseks eelarvearuandele märkige see ruut. |
| Kaasa likviidsuse plaanimises | Tehke see valik eelarvekande eraldamiseks pearaamatusse. Selle märkeruudu sätet ei saa aruandluskannete jaoks muuta. |
| Käibemaksugrupp | Eelarvegrupi maksu määramiseks kasutatav maksugrupp. |
| Kauba käibemaksugrupp | Eelarvegrupi maksu määramiseks kasutatav kauba maksugrupp. |
| Meetod | <p>Valige eelarvekande eraldamiseks kasutatav meetod:</p><ul><li>**Puudub** – eraldamist ei toimu.</li><li>**Periood** – prognoositakse iga perioodi sama kogus. Selle väärtuse valikul määrake väljale **Eel** kogus ja ajaühik **Ühik** väljale.</li><li>**Võti** – eelarve kogus määratakse vastavalt väljalmääratud **Perioodi eraldusvõtmele**. Seda meetodit kasutatakse juhul, kui soovite arvesse võtta ka hooajalisi kõikumisi.</li></ol>|
| Kohta | <p>Saate sisestada ajaintervallide arvu, mida prognoos tulevikus pikendab. See väli on saadaval ainult siis, kui valite väljal *Periood* suvandi **Meetod**.</p><p>Näiteks tehke valik *Periood* väljal **Meetod**, sisestage *1* väljale **Alus** ja valige *Kuud* väärtus **Ühik** väljal. Määrake väljal **Lõpp** lõppkuupäev, mis on ühe aasta pärast. Sellisel juhul luuakse eeloleva aasta igaks kuuks üks prognoosirida päise real määratud üksuse ja koguse põhjal.</p> |
| Ühik | Valige ajaintervalli ühik: *Päevad*, *Kuud*, või *Aastad*. Jaotus vastab siis päevade, kuude või aastate arvule, mille olete määranud väljale **Alus**.|
| Perioodi võti | Täpsusta perioodi eraldamisvõti. |
| Lõpp | Täpsusta väljade **Alus** ja **Ühik** kasutamise lõppkuupäev. |

### <a name="the-item-tab-on-the-supply-forecast-page"></a>Lehe Tarneprognoosi toote vahekaart

**Toode** vahekaart näitab rohkem toote infot valitud rea kohta vahekaardil **Ülevaade**.

Vahekaardi ülaosas oleval **Kaup** ruudustikul korratakse kauba teavet, mis kuvatakse ka **Ülevaade** vahekaardil. Lisaks sisaldab see välja **Ühiku hind** , mis näitab ostuhinda määratud ühikute arvule **Ühik** lehel. Ühikuhind leitakse automaatselt üksuse seadistamisest, kuid saate seda muuta.

Ruudustikus olevad väljad pakuvad rohkem üksikasju kauba kohta. Osa sellest teabest korratakse **Ülevaade** vahekaardil. Järgmises tabelis kirjeldatakse väljasid, mis on kordumatud **Kaup** vahekaardil.

| Field | Kirjeldus |
|---|---|
| Hinnaühik | Ühikute arv, millele ostuhind kehtib. See väärtus tuuakse kaubatabelist automaatselt, kuid seda saab muuta. |
| Ostukulud | Ostuhinna fikseeritud tasud. Lisakulud ei sõltu kogusest. |
| Allahindlusprotsent | Allahindlus protsendina. |
| Allahindluse summa | Müügiühiku summana väljendatud allahindlus. |
| Brutosumma | Summa, kui allahindlusi ei rakendata. |
| Kogus | Tehingu kogus toote varude üksuses. |
| Alamkooslus | Konkreetse alam-BOM-i materjalide arve number. |
| Alamprotsess | Määratud alamprotsessi protsessikood. |

### <a name="the-financial-dimensions-tab-on-the-supply-forecast-page"></a>Finantsmõõdud vahekaardil pakkumise prognoosil

Vahekaardil **Finantsdimensioonid** kuvatakse kõik vahekaardil **Ülevaade** praegu valitud rea finantsdimensiooni väärtused.

### <a name="the-inventory-dimensions-tab-on-the-supply-forecast-page"></a>Lehe Tarneprognoos vahekaart Varude mõõtmed

Vahekaardil **Varude dimensioonid** kuvatakse kõik vahekaardil **Ülevaade** praegu valitud rea varude dimensiooni väärtused.

### <a name="the-allocation-grid-on-the-supply-forecast-page"></a>Jaotusvõrk lehel Tarneprognoos

Kui kasutate kauba eraldusvõtit, või kui olete sisestanud kaubaeelarve ühe või mitme tulevase perioodi jaoks, saate eraldada eelarve valides **Eralda prognoos** vahekaardil **Ülevaade** tööriistaribal. Seejärel jaotatakse kogus nii nagu on näidatud ridadel **Eraldus** ruudustikus.

## <a name="demand-forecast-lines"></a>Nõudluse prognoosi read

Nõudluse prognoos võimaldab teil sisestada või luua kliendile nõudluse. See aitab müügi- ja turundusametnikke eeloleval prognoosiperioodil teavitada koondplaneerimise ametnikke eeldatavast nõudlusest.

Nõudluse prognoosi saate sisestada kauba, kaubagrupi, kauba eraldusvõtme, kliendi ja kliendigrupi kaupa. Teavet kõigi **Nõudluse prognoosi** lehe erinevate üksuste ja kirjete jaoks avamiseks [vt prognoosiridade vaatamise ja käsitsi sisestamise jaotisest](#manual-entry) selles teemas eespool.

**Nõudluse prognoosi** lehe ülemine osa pakub nõudluse prognoosi ridade ruudustikku ja vahekaartide kogu, mida saate kasutada valitud eelarverea lisateabe vaatamiseks ja häälestamiseks. Lehe alumises osas on **Jaotis** ruudustik.

Järgmised alamjaotised kirjeldavad kõiki igal vahekaardil saadaolevaid välju ja kõiki käske, mis on saadaval lehekülje toimingupaanil ja tööriistariba **Ülevaade** vahekaardil.

### <a name="action-pane-commands-on-the-demand-forecast-page"></a>Tegevuspaani käsud nõudluse prognoosi lehel

Järgmises tabelis kirjeldatakse lehe **Nõudluse prognoosi** toimingupaanil olevaid käske.

| Käsk | Kirjeldus |
|---|---|
| Salvesta | Salvestage praegused sätted. |
| Redigeeri | Saate lubada lehekülje sätete redigeerimise. |
| New | Lisage prognoosi rida ülemisele ruudustikule. |
| Kustutamine | Saate valitud eelarverea ülemist ruudustikku eemaldada. |
| Prognoosisaldod | Saate vaadata praeguse rahandusaasta valitud rea mudeli ID jaoks arvutatud eelarvesaldosid. Saldod jagatakse perioodi (kuu) järgi. |
| Likviidsuse planeerimine | Saate vaadata pearaamatule eraldatud eelarvekandeid, mis peavad olema. Lisateavet vt teemast [Rahavoo planeerimine](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| Dimensioonide kuvamine | Valige toode, salvestusruum, ja jälgimise mõõtmed mis peavad olema ruudustikus kuvatavad **Ülevaade** vahekaardil. |
| Pearaamatu eelvaade | Saate vaadata valitud kande pearaamatukirjeid. |
| Pakkumisridade ülekandmine | Viige hinnapakkumise read valitud projekti. |

### <a name="toolbar-commands-on-the-overview-tab-of-the-demand-forecast-page"></a>Tööriistariba käsud nõudeprognoosi lehe ülevaate vahekaardil

Järgmises tabelis kirjeldatakse käske toimingupaanil lehel **Ülevaade** vahekaardil **Nõudlusprognoos**.

| Käsk | Kirjeldus |
|---|---|
| Eralda prognoos | Kui kasutate eraldamismeetodit, looge eelarvekandele individuaalsed graafiku read. Rea kogus jaotatakse seejärel kuupäeva (vastavalt valitud ajaintervallidele), koguse ja kogu ajavahemiku summa järgi. (Vaata [Määrake eelarve](#allocate-forecast) sektsioon selles teemas hiljem.)|
| Hulgivärskendamine | Saate avada **Eelarvekannete redigeerimine** lehe. (Vt [Eelarvekannete hulgivärskendus](#bulk-update) sektsioon selles teemas hiljem.) |
| Varude prognoos | Saate avada valitud **varude eelarve** lehe, mis on filtreeritud valitud toote/mudeli kombinatsioon. (Vt [Varude eelarve](#inventory-forecast) sektsioon selles teemas hiljem.) |
| Loo kaubavajadus | Saate avada dialoogiboksi, kus saate luua kauba vajadusi ning projektiga seotud eelarvekannete jaoks müügitellimusi või kaubatöölehe ridu. |

### <a name="the-overview-tab-on-the-demand-forecast-page"></a>Tööriistariba käsud nõudlusprognoosi lehe ülevaate vahekaardil

Järgmises tabelis kirjeldatakse väljasid **Ülevaate** vahekaardil **Nõudlusprognoosi** lehel.

| Field | Kirjeldus |
|---|---|
| **Ülesande nimi** | Prognoosirea loomiseks kasutatud pakettülesande nimi. |
| **Mudel** | Kandega seotud eelarvemudel. |
| **Kuupäev** | Kande alguskuupäev. |
| **Kliendi konto** | Kandega seostuv kliendikonto. |
| **Kliendigrupp** | Kandega seostuv kliendigrupp. |
| **Kaubakood** | Kauba identifikaator. |
| **Toote nimetus** | Kauba kirjeldus. |
| **Kauba eraldamisvõti** | Kauba eraldamisvõti, mida kasutatakse lao eelarve eraldamisel. |
| **Müügikogus** | Prognoositav kogus määratud ostuühikus. |
| **Üksus** | Üksus, millele kaupa müüakse. |
| **summa** | Brutosumma, miinus allahindlused, mida prognoositav tehing prognoosida aitab. |
| **Müügihind** | Müügihind ühikute arvule, mis on määratud **Hinnaühik** väljal. Siia tuuakse automaatselt vastava kauba väärtus, kuid seda saab muuta. |
| **Müügivaluuta** | Prognoositava tehingu jaoks kasutatav valuuta. Valuuta sisestatakse automaatselt, kuid kasutaja saab valida mõne muu valuuta. |
| **Tegeliku kaalu kogus** | Eelarve kogus määratud tegeliku kaalu ühikus. |
| **Tegeliku kaalu ühik** | Saagi kaaluühik, millega toode on müüdud. Väärtus tuuakse automaatselt kauba seadistusest. |
| (Muud mõõtmed) | Täiendavaid toote, varude ja jälitamise dimensioone saab kuvada võrgustiku veergudena. Valige toimingupaanil üksus **Kuva dimensioonid**, et valida lisadimensioon, mida kuvatakse. |

### <a name="the-general-tab-on-the-demand-forecast-page"></a>Lehe Nõudluse prognoos vahekaart Üldine

Vahekaardil **Üldine** kuvatakse lisateavet praegu valitud rea **Ülevaade** kohta. Osa sellest teabest korratakse vahekaardil **Ülevaade**. Järgmises tabelis kirjeldatakse vahekaardi **Üldine** kordumatuid välju.

| Field | Kirjeldus |
|---|---|
| Nõudluse prognoosi seerianumber | Nõudluse prognoosi rea kordumatu number. See number luuakse kasutades numbriseeriat, mis on valitud nõudluse prognooside jaoks **Koondplaneerimise parameetrid** lehel. |
| Kaubagrupp | Kandega seotud kaubagrupp. |
| Aruanne | Kande lisamiseks aruandesse märkige see valik *Jah*. |
| Kommentaarid | Siia saate sisestada eelarvekandega seotud kommentaarid. |
| Aktiivne | Kande lisamiseks eelarvearuandele märkige see ruut. Selle märkeruudu sätet ei saa aruandluskannete jaoks muuta. |
| Kaasa likviidsuse plaanimises | Tehke see valik eelarvekande eraldamiseks pearaamatusse. Selle märkeruudu sätet ei saa aruandluskannete jaoks muuta. Lisateavet vt teemast [Rahavoo planeerimine](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| Käibemaksugrupp | Eelarvegrupi maksu määramiseks kasutatav maksugrupp. |
| Kauba käibemaksugrupp | Eelarvegrupi maksu määramiseks kasutatav kauba maksugrupp. |
| Meetod | <p>Valige eelarvekande eraldamiseks kasutatav meetod:</p><ul><li>**Puudub** – eraldamist ei toimu.</li><li>**Periood** – prognoositakse iga perioodi sama kogus. Selle väärtuse valikul määrake väljale **Eel** kogus ja ajaühik **Ühik** väljale.</li><li>**Võti** – eelarve kogus määratakse vastavalt väljalmääratud **Perioodi eraldusvõtmele**. Seda meetodit kasutatakse juhul, kui soovite arvesse võtta ka hooajalisi kõikumisi.</li><ul>|
| Kohta | <p>Saate sisestada ajaintervallide arvu, mida prognoos tulevikus pikendab. See väli on saadaval ainult siis, kui valite väljal *Periood* suvandi **Meetod**.</p><p>Näiteks tehke valik *Periood* väljal **Meetod**, sisestage *1* väljale **Alus** ja valige *Kuud* väärtus **Ühik** väljal. Määrake väljal **Lõpp** lõppkuupäev, mis on ühe aasta pärast. Sellisel juhul luuakse eeloleva aasta igaks kuuks üks prognoosirida päise real määratud üksuse ja koguse põhjal. |
| Ühik | Valige ajaintervalli ühik: *Päevad*, *Kuud*, või *Aastad*. Jaotus vastab siis päevade, kuude või aastate arvule, mille olete määranud väljale **Alus**.|
| Perioodi võti | Määrake perioodi eraldamisvõti, mida kasutatakse eelarve eraldamiseks. Lisateabe saamiseks vt jaotist [Eelarve planeerimise andmete eraldamine](../../finance/budgeting/budget-planning-data-allocation.md). |
| Lõpp | Täpsusta väljade **Alus** ja **Ühik** kasutamise lõppkuupäev. |

### <a name="the-item-tab-on-the-demand-forecast-page"></a>Lehe Nõudlusprognoosi toote vahekaart

Vahekaardil **Ühik** kuvatakse lisateavet praegu valitud rea **Ülevaade** kohta. Osa sellest teabest korratakse **Ülevaade** vahekaardil. Järgmises tabelis kirjeldatakse vahekaardi **Ühik** kordumatuid välju.

| Field | Kirjeldus |
|---|---|
| Hinnaühik | Müügiühikute arv, millele müügihind kehtib. See väärtus tuuakse kaubatabelist automaatselt, kuid seda saab muuta. |
| Müügitasud | Müügihinna fikseeritud tasud. Lisakulud ei sõltu kogusest. |
| Omahind | Praeguse eelarvekande kulu laoühiku kohta. Väärtus tuuakse kaubatabelist automaatselt, kuid seda saab muuta. |
| Allahindlusprotsent | Allahindlus protsendina. |
| Allahindluse summa | Müügiühiku summana väljendatud allahindlus. |
| Brutosumma | Summa, kui allahindlusi ei rakendata. |
| Laokogus | Tehingu kogus toote varude üksuses. |
| Kindla koosluse kasutamine | Konkreetse BOM-i BOM number. |
| Kindla protsessi kasutamine | Määratud alamprotsessi protsessikood. |

### <a name="the-project-tab-on-the-demand-forecast-page"></a>Lehe Nõudluse prognoos vahekaart Projekt

Vahekaardil **Projekt** kuvatakse lisateavet praegu valitud rea **Ülevaade** kohta. Osa sellest teabest korratakse vahekaardilt **Ülevaade**, **Üldine**, või **Ühik** vahekaardil. Järgmises tabelis kirjeldatakse vahekaardi **Projekt** kordumatuid välju.

| Field | Kirjeldus |
|---|---|
| Projekti kuupäev | Nõudluse prognoosi kande kuupäev. |
| Projekti ID | Praeguses kandes viidatud projekti ID. |
| Rahastamise allikas | Nõudluse prognoosiga seostatud rahastamise allikas. |
| Tegevuse number | Nõudluse prognoosi kandega seostatud tegevus. |
| Kategooria | Praeguse kande kulukategooria. |
| Rea atribuut | Kandega on seotud olek. |
| Kande ID | Nõudluse prognoosi kande süsteemi ID. |
| Omahind | Nõudluse prognoosi kande summa. |
| Ühiku hind | Hind ühiku kohta. |
| Muutja | Töötaja ID, kes viimati valitud kannet muutis. |
| Arve kuupäev | Sisestage eeldatav arve kuupäev. |
| Eemaldamiskuupäev | Vaadake või muutke eemaldamiskuupäeva. Eelarve loomisel määratakse eemaldamiskuupäevaks projekti lõppkuupäev. Kui projektil pole lõppkuupäeva, rakendatakse projekti kuupäeva. See väli kehtib ainult fikseeritud hinnaga projektide ja investeeringuprojektide puhul. |
| Kulu maksekuupäev | Siia saate sisestada ostumakse eeldatava kuupäeva. |
| Müügi maksekuupäev | Siia saate sisestada müügimakse eeldatava kuupäeva. |

### <a name="the-financial-dimensions-tab-on-the-demand-forecast-page"></a>Finantsmõõdud vahekaardil nõudluse prognoosi lehel

Vahekaardil **Finantsdimensioonid** kuvatakse kõik vahekaardil **Ülevaade** praegu valitud rea finantsdimensiooni väärtused.

### <a name="the-inventory-dimensions-tab-on-the-demand-forecast-page"></a>Varude mõõdud vahekaardil nõudluse prognoosi lehel

Vahekaardil **Varude dimensioonid** kuvatakse kõik vahekaardil **Ülevaade** praegu valitud rea varude dimensiooni väärtused.

### <a name="the-allocation-grid-on-the-demand-forecast-page"></a>Jaotusvõrk lehel Nõudluse prognoos

Kui kasutate kauba eraldusvõtit, või kui olete sisestanud kaubaeelarve ühe või mitme tulevase perioodi jaoks, saate eraldada eelarve valides **Eralda prognoos** vahekaardil **Ülevaade** tööriistaribal. Seejärel jaotatakse kogus nii nagu on näidatud ridadel **Eraldus** ruudustikus. (Vaata [Määrake eelarve](#allocate-forecast) sektsioon selles teemas hiljem.)

## <a name="inventory-forecast"></a><a name="inventory-forecast"></a>Varude prognoos

Pakkumise ja nõudluse prognoosi ridadel on nupp **Varude prognoos**, mis avab sama **Laoeelarve lehe** vaate, mida filtreeritakse kauba/mudeli kombinatsiooni puhul. Varude prognoos kajastab samale kaubale sisestatud pakkumise ja nõudluse vahelist saldot. Seda ei saa muuta. Varude prognoos aitab laohalduse töörühmal üle vaadata eeldatavad muudatused kauba vabas kaubavarus prognoositud eeloleval perioodil.

### <a name="the-action-pane-on-the-inventory-forecast-page"></a>Tegevuspaani käsud varude prognoosi lehel

Järgmises tabelis kirjeldatakse lehe **Nõudluse prognoosi** toimingupaanil olevaid käske.

| Tegevus | Kirjeldus |
|---|---|
| Tarneprognoos | Saate avada valitud **Tarneprognoos** lehe, mis on filtreeritud valitud toote/mudeli/kuupäeva kombinatsioon. |
| Nõudluse prognoos | Saate avada valitud **Nõudluse prognoosi** lehe, mis on filtreeritud valitud toote/mudeli/kuupäeva kombinatsioon. |
| Varud \> Kuva dimensioonid | Valige toode, salvestusruum, ja jälgimise mõõtmed mis peavad olema ruudustikus kuvatavad **Ülevaade** vahekaardil. |

### <a name="the-grid-on-the-inventory-forecast-page"></a>Ruudustik lehel varude prognoos

Järgmine tabel kirjeldab veerud ruudustikus **Varude prognoos** lehel.

| Field | Kirjeldus |
|---|---|
| **Mudel** | Kandega seotud eelarvemudel. |
| **Kaubakood** | Kauba identifikaator. |
| **Eelarve kuupäev** | Prognoositava tehingu kuupäev. |
| **Eelarve tüüp** | Kande allikas (*nõudluse prognoos* või *tarneprognoos*). |
| **Tegeliku kaalu kogus** | Prognoositav kogus saagi kaaluühikus. |
| **Kogus** | Prognoositav kogus inventuuriühikus. |
| **Akumuleeritud tegelik kaal** | Akumuleeritud eelarvekogus tegeliku kaalu ühikus, kui sama kauba kohta on akumuleeritud mitu eelarverida. |
| **Alamkooslus** | Määratud alamkoosluse kood. |
| **Alamprotsess** | Määratud alamprotsessi protsessikood. |
| (Muud mõõtmed) | Täiendavaid dimensioone saab kuvada võrgustiku veergudena. Valige toimingupaanil üksus **Varud \> Kuva dimensioonid** et valida lisadimensioon, mida kuvatakse. |

## <a name="allocate-forecast"></a><a name="allocate-forecast"></a>Eralda prognoos

Kasutage seda protseduuri valitud eelarvekande ridade töötlemiseks. Eelarve eraldamisel jaotatakse kogus nii, nagu on näidatud **Eralda** rida ruudustikus.

1. Sõltuvalt üksuse tüübist, millele soovite prognoosi luua ja sellest, mis tüüpi eelarvet soovite luua, avage pakkumine, nõudlus või varude eelarve leht, nagu kirjeldatud [Vaata ja lisa manuaalselt eelarve ridu](#manual-entry).
1. Pakkumise või nõudluse prognoosi ridade lehel valige prognoosi rida ja seejärel valige vahekaardil **Ülevaade** tööriistaribal **Eralda prognoos**.
1. Dialoogiboksis **Eralda eelarve** seadke väljad, mida kirjeldatakse järgmises tabelis. (Väärtus, mille valite väljal **Meetod** määratleb, et saadaval on ka teised väljad.)

    | Field | Kirjeldus |
    |---|---|
    | Meetod | <p>Valige eelarvekande eraldamiseks kasutatav meetod:</p><ul><li>**Puudub** – eraldamist ei toimu.</li><li>**Periood** – prognoositakse iga perioodi sama kogus. Selle väärtuse valikul määrake väljale **Eel** kogus ja ajaühik **Ühik** väljale.</li><li>**Võti** – eelarve kogus määratakse vastavalt väljalmääratud **Perioodi eraldusvõtmele**. Seda meetodit kasutatakse juhul, kui soovite arvesse võtta ka hooajalisi kõikumisi.</li><ul>|
    | Kohta | <p>Saate sisestada ajaintervallide arvu, mida prognoos tulevikus pikendab. See väli on saadaval ainult siis, kui valite väljal *Periood* suvandi **Meetod**.</p><p>Näiteks tehke valik *Periood* väljal **Meetod**, sisestage *1* väljale **Alus** ja valige *Kuud* väärtus **Ühik** väljal. Siis määrake väljal **Lõpp** lõppkuupäev, mis on ühe aasta pärast. Sellisel juhul luuakse eeloleva aasta igaks kuuks üks prognoosirida päise real määratud üksuse ja koguse põhjal. |
    | Ühik | Valige ajaintervalli ühik: *Päevad*, *Kuud*, või *Aastad*. Jaotus vastab siis päevade, kuude või aastate arvule, mille olete määranud väljale **Alus**.|
    | Perioodi võti | Määrake perioodi eraldamisvõti, mida kasutatakse eelarve eraldamiseks. Lisateabe saamiseks vt jaotist [Eelarve planeerimise andmete eraldamine](../../finance/budgeting/budget-planning-data-allocation.md). |
    | Lõpeta | Määratlege lõppkuupäev, mis rakendub teie sätetele väljadel **Kohta** ja **Üksus** väljal. |

1. Seadete kinnitamiseks valige **OK**.
1. Sama rea kohta saate tulemusi üle vaadata vahekaardil **Eraldamine**.

## <a name="bulk-update-forecast-transactions"></a><a name="bulk-update"></a>Eelarvekannete hulgivärskendus

Kasutage seda protseduuri olemasolevate eelarvekande ridade töötlemiseks. Saate kopeerida, muuta või kustutada eelarvekande ridu.

1. Pakkumise või nõudluse prognoosi ridade lehel valige **hulgivärskendus**.
1. Valige dialoogiboksis **Filtreeri**.
1. Valige vahekaardil **Vahemik** kriteeriumid, mis iseloomustavad eelarve allikaandmeid, mida te soovite kopeerida, muuta või kustutada. See võib hõlmata eelarvemudelit, kaubakoodi ja kliendi kontot.
1. Valiku kinnitamiseks valige **OK**.

    Pärast andmete valimist saate **Eelarvekannete redigeerimine** dialoogiboksi abil määratleda, kas soovite neid kopeerida, redigeerida või kustutada.

    > [!NOTE]
    > Filtreerimissamm on **Hulgi redigeerimise** funktsiooni kasutamise eeltingimus. Selle vahelejätmise korral valib ja uuendab programm **kõik** eelarveread. Seetõttu võite tahtmatult põhjustada tehingute dubleerimist või eemaldamist.

1. Jaotises **Haldus** valige, kas soovite valitud eelarvekandeid kopeerida, värskendada või kustutada.
1. Eelarve parameetrite muutmiseks kasutage jaotist **Muudatused väljal**. Märkige parameetri ruut ja valige seejärel olemasolevate suvandite hulgast. Näiteks märkige ruut **Mudel** ja seejärel valige eelarvemudeli number. Olemasolevad eelarvemudeli read kopeeritakse valitud eelarvemudelisse.
1. Kasutage **perioodi muutmise** jaotist, et nihutada prognoosi algus- ja lõppkuupäevi edasi või tagasi. Märkige ruut ja kasutage koguse ja perioodi välju eelarve kuupäevade nihutamise ajavahemiku määramiseks. Alguskuupäeva varasemaks nihutamiseks saate sisestada negatiivse koguse.

    Näiteks eelarvekande alguskuupäeva edasi lükkamiseks kuue kuu võrra märkige ruut, sisestage koguseks *6* ja perioodiks *Kuud*.

1. Praeguste eelarve andmete uuendamiseks kasutage väljagruppi **Korrektne väli**. Valige **Väli** väljal kriteerium, mida soovite muuta. Sisestage **Faktor** väljal korrutustegur, mida rakendada teie valitud kriteeriumi korral või sisestage liitmis- või lahutustehte konstant. Näiteks valige kriteeriumiks *Kogus* ning sisestage tegur *1,5* kauba koguse korrutamiseks 1,5-ga. Sisestage konstant *-25* kaubakoguse vähendamiseks 25 ühiku võrra.
1. Kasutage jaotist **Finantsdimensioonid** eelarveridade finantsdimensioonide värskendamiseks. Valige finantsdimensioonid, mida soovite muuta ja seejärel sisestage väärtus, mida valitud dimensioonide puhul rakendada.
1. Muudatuse rakendamiseks valige **OK**.

## <a name="use-forecasts-with-master-planning"></a>Koondplaneerimine koos prognoosiga

Pärast oma nõudluse prognoosi ja/või pakkumise prognoosi sisestamist saate koondplaneerimise käigus kaasata prognoosid, et arvestada oodatud nõudluse ja/või pakkumise üle koondplaneerimise käituse. Kui eelarved on koondplaneerimisesse kaasatud, arvutatakse materjalide ja mahu brutonõuded ja luuakse plaanitud tellimused.

### <a name="set-up-a-master-plan-to-include-an-inventory-forecast"></a>Koondplaani seadistamine laovaru prognoosi kaasamiseks

Järgige neid juhiseid, et seadistada koondplaan nii, et see hõlmaks laovaru prognoosi.

1. Avage **Koondplaneerimine \> Seadistus \> Plaanid \> Koondplaanid**.
1. Valige olemasolev plaan või looge uus plaan.
1. Määrake kiirkaardil **Üldine** järgmised väljad.

    - **Eelarvemudel** – valige rakendatav eelarvemudel. Seda mudelit võetakse arvesse, kui praeguse koondplaani jaoks luuakse tarnesoovitus.
    - **Kaasa tarneprognoos** – seadke selle suvandi väärtuseks *Jah*, et kaasata tarneprognoos praegusse koondplaani. Kui seate selle väärtuseks *Ei*, ei kaasata koondplaani tarneprognoosi kandeid.
    - **Kaasa nõudluse prognoos** – seadke selle suvandi väärtuseks *Jah*, et kaasata nõudluse prognoos praegusse koondplaani. Kui seate selle väärtuseks *Ei*, ei kaasata koondplaani nõudluse prognoosi kandeid.
    - **Prognoosinõuete vähendamiseks kasutatav meetod** – valige meetod, mida tuleks kasutada prognoosinõuete vähendamiseks. Lisateavet vt [Prognoosi vähendamise võtmed](planning-optimization/demand-forecast.md#reduction-keys).

1. Kiirkaardil **Ajapiirid päevades** saate seada järgmised väljad, et määrata periood, mille jooksul on prognoos kaasatud.

    - **Eelarveplaan** – määrake selle suvandi väärtuseks *Jah*, et alistada üksikutest laovarude gruppidest pärinev eelarveplaani ajapiir. Seadke selle väärtuseks *Ei*, et kasutada praeguse koondplaani jaoks üksikute laovarude gruppide väärtuseid.
    - **Prognoosi ajavahemik** – kui seate suvandi **Eelarveplaan** väärtuseks *Jah*, määrake päevade arv (alates tänasest kuupäevast), mida nõudluse prognoosi korral rakendada.

    > [!IMPORTANT]
    > Planeerimise optimeerimise korral ei toetata praegu veel valikut **Eelarveplaan**.

### <a name="run-a-master-plan-that-includes-an-inventory-forecast"></a>Koondplaani käivitamine, mis sisaldab laovaru prognoosi

Järgige neid juhiseid, et käivitada koondplaan nii, et see hõlmaks laovaru prognoosi.

1. Minge **Koondplaneerimise \>Tööruumid \> Koondplaneerimine**.
1. Sisestage või valige väljal **Koondplaan** koondplaan, mille eelmises protseduuris seadistate.
1. Valige paanil **Koonplaneerimine** **Käivita**.
1. Määrake dialoogiboksis **Koondplaneerimine** suvand **Jälgi töötlemisaega** väärtuseks *Jah*.
1. Väljale **Lõimede arv** sisestage arv.
1. Valige kiirkaardil **Kaasatavad kirjed** suvand **Filter**.
1. Kuvatakse standardne päringu redaktori dialoogiaken. Valige vahekaardil **Vahemik** rida, kus väli **Väli** on määratud üksusele *Kaubakood*.
1. Valige väljal **Kriteerium** kaubakood, mida plaani kaasata.
1. Valige nupp **OK**.

Arvutatud nõuete vaatamiseks avage leht **Brutonõue**. Näiteks valige toimingupaanil **Väljastatud tooted** lehel **Plaan** vahekaardil **Nõuded** grupis **Brutonõue**.

Loodud plaanitud tellimuste vaatamiseks minge **Koondplaneerimise \> Tava \> Plaanitud tellimused** ja valige sobiv eelarveplaan.

## <a name="additional-resources"></a>Lisaressursid

- [Nõudluse prognoosimise ülevaade](introduction-demand-forecasting.md)
- [Nõudluse prognoosi häälestus](demand-forecasting-setup.md)
- [Statistilise alusprognoosi loomine](generate-statistical-baseline-forecast.md)
- [Alusprognoosis käsitsi korrigeerimiste tegemine](manual-adjustments-baseline-forecast.md)
- [Koondplaneerimine koos nõudluse prognoosidega](planning-optimization/demand-forecast.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
