---
title: Nõudluse prognoosi seadistus
description: Selles teemas kirjeldatakse seadistustoiminguid, mida tuleb nõudluse prognoosimiseks valmistumiseks teha.
author: ChristianRytt
ms.date: 11/23/2021
ms.topic: article
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f53171361b655ab4ae05894d098203df0af8d60
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920769"
---
# <a name="demand-forecasting-setup"></a>Nõudluse prognoosi häälestus

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas seadistada nõudluse prognoosimist.  

## <a name="item-allocation-keys"></a>Kauba eraldamisvõtmed

Kauba eraldamisvõtmed loovad kaubagrupid. Nõudluse prognoosi arvutatakse kaubale ja selle dimensioonidele ainult siis, kui kaup on osa kauba eraldamisvõtmest. See reegel jõustatakse, et grupeerida suur hulk kaupu, nii et nõudluse prognoose saab luua kiiremini. Prognoose luuakse ainult ajalooliste andmete põhjal.

Kui prognoosi loomisel kasutatakse kauba eraldamisvõtit, peab kaup ja selle dimensioonid kuuluma ainult ühe kauba eraldamisvõtme juurde.

Kauba eraldamisvõtmete loomiseks ja neile varude ühikute (SKU) lisamiseks järgige neid samme.

1. Avage **Koondplaneerimine \> Seadistus \> Nõudluse prognoos \> Kauba jaotamise võtmed**.
1. Valige loendipaanil kauba eraldamisvõti või valige uue loomiseks **tegevuspaanil** uus. Uue või valitud võtme päises seadke järgmised väljad:

    - **Kauba** eraldamisvõti – sisestage võtmele kordumatu nimi.
    - **Nimi:** sisestage võtme kirjeldav nimi.

1. Valitud kauba eraldamisvõtmele kaupade lisamiseks või kaupade eemaldamiseks järgige ühte järgmistest sammudest:

    - Kasutage kauba eraldamise kiirkaardil tööriistariba nuppe Uued ja Kustuta, et **kaupu vajaduse korral lisada või** **·** **eemaldada**. Valige iga rea jaoks kaubakood ja seejärel määrake dimensiooniväärtused teistes veergudes vastavalt vajadusele. **Ruudustikus** kuvatavate dimensiooniveergude kogumi muutmiseks valige tööriistaribal kuva dimensioonid. (Väärtus väljal **Nõudluse** prognooside loomisel eiratakse protsendi veergu.)
    - Kui soovite võtmele lisada suure hulga kaupu, valige tegevuspaanil suvand Määra kaubad, et avada lehekülg, kus saate valitud võtmele mitu üksust **leida** ja määrata.

> [!IMPORTANT]
> Igal kauba eraldamisvõtmel peab olema ettevaatlik olema ainult vastavate kaupade kaasamist. Mittevajalike kaupadega võivad Microsoft Azure’i masinõppe kasutamisel suurenenud kulud kaasneda.

## <a name="intercompany-planning-groups"></a>Kontsernisisesed plaanimisgrupid

Nõudluse prognoos võib luua ettevõtteülesi prognoose. Dynamics 365 Supply Chain Management Ettevõttes, mis on plaanitud koos, grupeeritakse samasse kontsernisisesesse plaanimisgruppi. Ettevõtte kaupa kauba eraldamisvõtmete määramiseks, mida nõudluse prognoosimiseks arvesse võtta, seostage kauba eraldamisvõti kontsernisisese plaanimisgrupi liikmega.

> [!IMPORTANT]
> Plaanimine ei toeta praegu kontsernisiseseid plaanimisgruppe. Plaanimise optimeerimist kasutav kontsernisisene planeerimine seadistage koondplaneerimise pakett-tööd, mis sisaldavad kõigi asjakohaste ettevõtete koondplaane.

Oma kontsernisiseste plaanimisgruppide seadistamiseks järgige neid samme.

1. Minge **kontsernisiseste \>\> plaanimisgruppide koondplaneerimise seadistuse** juurde.
1. Valige plaanimisgrupp loendipaanil või valige uue loomiseks **tegevuspaanil** Uus. Uue või valitud grupi päises seadke järgmised väljad:

    - **Nimi:** sisestage plaanimisgrupi kordumatu nimi.
    - **Kirjeldus** – sisestage plaanimisgrupi lühikirjeldus.

1. Kasutage **kontsernisisese plaanimisgrupi liikmete kiirkaardil tööriistariba nuppe, et lisada rida igale ettevõttele (juriidilisele isikule), mis** peaks gruppi kuuluma. Määrake igas reas järgmised väljad.

    - **Juriidiline** isik: valige ettevõtte (juriidiline isik) nimi, mis on valitud grupi liige.
    - **Planeerimisjärjestus** – määrake tellimus, mida ettevõte peaks töötlema teiste ettevõtete suhtes. Väheväärtusi töödeldakse esimesena. See tellimus võib olla oluline, kui ühe ettevõtte nõudlus mõjutab teisi ettevõtteid. Sellisel juhul tuleb nõudlust tarniv ettevõte viimasena töödelda.
    - **Koondplaan** – valige praeguse ettevõtte käivitamiseks koondplaan.
    - **Automaatne kopeerimine staatilisse** plaani – märkige see ruut plaani tulemuse kopeerimiseks staatilisse plaani.
    - **Automaatne kopeerimine** dünaamilisse plaani – märkige see ruut plaani tulemuse kopeerimiseks dünaamilisse plaani.

1. Kui kontsernisisese plaanimisgrupi liikmetele ei ole määratud ühtki kauba eraldamisvõtit, arvutatakse nõudluse prognoos vaikimisi kõigile kaupadele, mis on määratud kõikidele kauba eraldamisvõtmetele kõigis ettevõtetes. Dialoogiboksis Statistilise alusprognoosi loomine (koondplaneerimine Nõudluse prognoosimine looge statistiline alusprognoos) on saadaval ettevõtete ja kauba eraldamisvõtmete **täiendavad** **\>\>\> filtreerimisvalikud.** Kauba eraldamisvõtmete määramiseks valitud kontsernisisese plaanimisgrupi ettevõttele valige ettevõte ja seejärel valige kontsernisisese plaanimisgrupi liikmete kiirkaardil tööriistaribal **kauba** **eraldamisvõtmed**.

> [!IMPORTANT]
> Ärge lisage igasse kontsernisisesesse plaanimisgruppi ainult asjakohaseid kauba eraldamisvõtmeid. Mittevajalikud kaubad võivad põhjustada suurenenud kulusid, kui kasutate Azure'i masinaõppimist.

## <a name="set-up-demand-forecasting-parameters"></a><a name="parameters"></a> Häälestage nõudluse prognoosimise parameetrid

Kasutage nõudluse **prognoosimise parameetrite** lehte, et seadistada mitu võimalust, mis kontrollivad, kuidas nõudluse prognoos teie süsteemis töötab.

### <a name="open-the-demand-forecasting-parameters-page"></a>Avage nõudluse prognoosimise parameetrite leht

Nõudluse prognoosimise parameetrite seadistamiseks minge koondplaneerimise seadistuse **\> nõudluse \> prognoosimise nõudluse \> prognoosimise parameetrid.** Seadistus on globaalne, kuna nõudluse prognoosimine toimub ettevõteteüleselt. See kehtib kõigi juriidiliste isikute (ettevõtete) kohta.

### <a name="general-settings"></a>Üldsätted

Kasutage **nõudluse** prognoosimise **parameetrite lehe vahekaarti** Üldine, et määratleda nõudluse prognoosimise üldsätted.

#### <a name="demand-forecast-unit"></a>Nõudluse prognoosi ühik

Nõudluse prognoosimine loob koguselise prognoosi. Seetõttu peab väljal **Nõudluse prognoosi ühik** olema määratud mõõtühik, milles kogus peaks olema väljendatud. See väli määratleb ühiku, mida kasutatakse kõigi nõudluse prognooside jaoks, olenemata iga toote tavalistest laoühikutest. Järjepidevat eelarveüksust kasutades tagate, et liitmine ja protsendi jaotus on loogilised. Kogumi ja protsentide jaotuse kohta vt lisateavet artiklist [Alusprognoosi käsitsi korrigeerimine](manual-adjustments-baseline-forecast.md).

Iga mõõtühiku puhul, mida kasutatakse nõudluse prognoosimises kaasatud STU-de puhul, veenduge, et mõõtühiku jaoks on teisendusreegel ja siin valitud üldine prognoosi mõõtühik. Eelarve loomisel logitakse kaupade loend, mille mõõtühiku teisendamist pole. Seega saate seadistust hõlpsasti parandada. Lisateavet mõõtühikute ja nende vahel teisendamise kohta vt [mõõtühikute](../pim/tasks/manage-unit-measure.md) haldamine.

#### <a name="transaction-types"></a>Kandetüübid

Kasutage kiirkaardi Kande tüübid välju kandetüüpide valimiseks, mida **kasutatakse** statistilise alusprognoosi loomisel.

Nõudluse prognoosimist saab kasutada nii sõltuva nõudluse kui ka sõltumatu nõudluse prognoosimiseks. Näiteks kui ainult müügitellimuse valik on seatud valikule Jah ja kõik kaubad, mida peetakse nõudluse prognoosimiseks, on müüdud kaubad, arvutab süsteem **sõltumatu** *nõudluse*. Kauba eraldamisvõtmetele ja nõudluse prognoosimisse saab siiski lisada olulisi alamkomponente. Sel juhul arvutatakse sõltuv eelarve, kui tootmisrea **valiku** *väärtuseks* on seatud Jah.

Saate kauba eraldamisvõtmete vahekaardil alistada ühe või mitme konkreetse kauba **eraldamisvõtme** kandetüübid. Vahekaardil on sarnased väljad.

#### <a name="choose-how-to-create-the-baseline-forecast"></a>Valige, kuidas alusprognoosi luua

Väli **Prognoosi** loomise strateegia võimaldab teil valida meetodi, mida kasutatakse alusprognoosi loomiseks. Saadaval on kolm meetodit:

- *Kopeeri ajalooline nõudlus* ümber – looge prognoosid ajalooliste andmete kopeerimise abil.
- *Azure Machine Learning Service* – kasutage prognoosimudelit, mis kasutab Azure'i masina õppeteenust. Azure'i masina õppeteenus on praegune masina õppelahendus Azure'ile. Seetõttu on soovitatav seda kasutada siis, kui soovite eelarvemudelit kasutada.
- *Azure Machine Learning* – kasutage prognoosimudelit, mis kasutab Azure Machine Learning Studiot (prognoos). Azure Machine Learning Studio (varundus) on aegunud ja eemaldatakse varsti Azure'ist. Seetõttu soovitame teil valida *Azure Machine Learning Service, kui* seadistate nõudluse prognoosimise esmakordselt. Kui kasutate praegu Azure Machine Learning Studiot (the), peaksite plaanima lülituda Azure Machine Learning Service'ile võimalikult kiiresti.

Saate alistada ühe või mitme kindla kauba eraldamisvõtme prognoosi loomise meetodi, kasutades vahekaarti **Kauba eraldamisvõtmed.** Vahekaardil on sarnased väljad.

#### <a name="override-default-forecast-algorithm-parameters-globally"></a>Alista globaalselt prognoosi vaikealgoritmi parameetrid

Prognoosi vaikealgoritmi parameetrid ja väärtused määratakse nõudluse prognoosimise parameetrite lehele (koondplaneerimise seadistus **nõudluse** **\>\> prognoosimise nõudluse \> prognoosimise parameetrid).** Te saate neid globaalselt alistada, kasutades nõudluse prognoosimise parameetrite lehe vahekaardi **Üldine** **·** **kiirkaarti Prognoosi algoritmi** parameetrid. (Saate neid ka konkreetsete eraldusvõtmete puhul alistada, kasutades selleks **Kauba** eraldamisvõtmete vahekaart **nõudluse prognoosimise parameetrite** lehel.)

Kasutage **tööriistariba** **nuppe** Lisa ja Eemalda, et luua parameetrite avate nõutav kogum. Valige iga loendi parameetri jaoks väärtus väljal Nimi ja sisestage **seejärel väljale Väärtus sobiv** **väärtus**. Kõik siin loetlemata parameetrid võtavad oma väärtused lehelt Nõudluse **prognoosimise** parameetrid sätetest. Lisateavet selle kohta, kuidas kasutada parameetrite standardkomplekti ja nende jaoks väärtusi valida, vaadake jaotisest Nõudluse prognoosimise mudelite [vaikeparameetrid ja](#model-parameters) väärtused.

### <a name="set-forecast-dimensions"></a>Prognoosi dimensioonide kogumid

Prognoosi dimensioon näitab prognoosile määratletud üksikasjade taset. Prognoosi dimensioonid on nõutavad ettevõtte, saidi ja kauba eraldusvõtme jaoks. Saate luua eelarveid ka laos, varude olekus, kliendigrupis, kliendikontos, riigis/regioonis, osariigi ja/või kauba tasemel ning kõigil kaubadimensiooni tasemetel. Kasutage nõudluse prognoosimise parameetrite lehe vahekaarti Prognoosi dimensioonid, et valida prognoosi dimensioonide kogum, mida kasutatakse **nõudluse** prognoosi **loomisel**.

Igal ajal saate nõudluse prognoosimiseks kasutatavate dimensioonide loendisse lisada prognoosi dimensioone. Samuti saate prognoosi dimensioone loendist eemaldada. Prognoosi dimensiooni lisamisel või eemaldamisel kaovad siiski käsitsi tehtud korrigeerimised.

### <a name="set-up-overrides-for-specific-item-allocation-keys"></a>Saate häälestada konkreetsete kauba eraldamisvõtmete alistamist.

Kõik kaubad ei tööta nõudluse prognoosimise perspektiivist samal viisil. Seega saate kehtestada eraldusvõtmele spetsiifilised alistamised enamiku vahekaardil Üldine määratud **sätete** puhul. Erand on nõudluse prognoosi ühik. Konkreetse kauba eraldamisvõtme aksessi loomiseks järgige neid samme.

1. Nõudluse prognoosimise parameetrite lehel kasutage kauba eraldamisvõtmete vahekaardil tööriistariba nuppe, et lisada kauba eraldamisvõtmeid vasakul olevale ruudustikule või **eemaldada** **need**, nagu vaja. Seejärel valige eraldusvõti, mille jaoks soovite alistamist seadistada.
1. Lubage kandetüüpide kiirkaardil kannete tüübid, mida soovite kasutada valitud eraldamisvõtmesse kuuluvate toodete statistilise **alusprognoosi** loomiseks. Sätted töötavad nii, nagu nad vahekaardil Üldine **töötavad**, kuid rakenduvad ainult valitud kauba eraldamisvõtmele. Kõik siinsed sätted (nii Väärtuse Jah kui ka Ei väärtused) alistavad kõik vahekaardil *Üldine* *·* **olevad** **kandetüübid**.
1. Prognoosi **algoritmi parameetrite kiirkaardil valige prognoosi loomise strateegia ja prognoosi algoritmi parameetrid valitud eraldamisvõtmele kuuluvate** toodete alistamiseks. Need sätted töötavad nii, nagu nad vahekaardil **Üldine** töötavad, kuid rakenduvad ainult valitud kauba eraldamisvõtmele. Kasutage **tööriistariba** **nuppe** Lisa ja Eemalda, et määrata parameetrite avate nõutav kogum. Valige iga loendi parameetri jaoks väärtus väljal Nimi ja sisestage **seejärel väljale Väärtus sobiv** **väärtus**. Lisateavet selle kohta, kuidas kasutada parameetrite standardkomplekti ja nende jaoks väärtusi valida, vaadake jaotisest Nõudluse prognoosimise mudelite [vaikeparameetrid ja](#model-parameters) väärtused.

### <a name="set-up-the-connection-to-the-azure-machine-learning-service"></a>Ühenduse loomine Azure'i masina õppeteenusega

Kasutage **vahekaarti Azure Machine Learning Service** ühenduse häälestamiseks Azure'i masina õppeteenusega. See lahendus on üks alusprognoosi loomise valikuid. Need sätted sellel vahekaardil mõjuvad ainult siis, kui prognoosi loomise strateegia väli on **seatud** väärtusele Azure Machine Learning *Service*.

Lisateavet Selle kohta, kuidas seadistada Azure'i masina õppeteenust ja seejärel kasutada sellega ühenduse loomiseks seadeid, vaadake jaotisest [Azure Machine Learning](#setup-amls) Service.

### <a name="set-up-the-connection-to-azure-machine-learning-studio-classic"></a>Ühenduse loomine Azure Machine Learning Studio'ga (varundus)

> [!IMPORTANT]
> Azure Machine Learning Studio (varundus) on aegunud. Seetõttu ei saa te enam Azure'is selle jaoks uusi tööruume luua. See on asendatud Azure Machine Learning Service'iga, mis pakub sarnaseid funktsioone ja muud. Kui te ei kasuta juba Azure Machine Learningi, peaksite kasutama azure'i masina õppeteenust. Kui teil on juba tööruum, mis loodi Azure Machine Learning Studio (s) jaoks, saate seda edasi kasutada, kuni funktsioon on Azure'ist täielikult eemaldatud. Soovitame teil siiski võimalikult kiiresti uuendada Azure'i masina õppeteenust. Kuigi rakendus jätkab hoiatamist, et Azure Machine Learning Studio (edaspidi) on taunitav, ei mõjutata prognoosimise tulemust. Lisateavet uue Azure Machine Learning Service'i ja selle häälestamise kohta vt jaotisest [Azure Machine Learning](#setup-amls) Service.
>
> Saate vabalt valida uue ja vana masina õppelahenduste kasutamise koos Tarneahela haldusega seni, kuni vana Azure Machine Learning Studio (virtuaal) tööruum on alles saadaval.

Kui teil on juba saadav Azure Machine Learning Studio (workspace) tööruum, saate seda kasutada prognooside loomiseks, ühendades selle tarneahela haldusega. Selle ühenduse saate luua, kasutades **vahekaarti Azure Machine Learning lehel Nõudluse** **prognoosimise** parameetrid. (Selle vahekaardi sätted jõustuvad vaid **siis, kui Prognoosi loomise strateegia** väli on seatud *väärtusele Azure Machine Learning* .) Sisestage järgmised üksikasjad oma Azure Machine Learning Studio (workspace) tööruumi jaoks:

- veebiteenuse rakenduse programmeerimisliidese (API) võti;
- veebiteenuse lõpp-punkti URL;
- Azure'i salvestuskonto nimi;
- Azure'i salvestuskonto võti.

> [!NOTE]
> Azure’i salvestuskonto nimi ja võti on vajalikud ainult siis, kui kasutate kohandatud salvestuskontot. Kui juurutate ettevõtte sees versiooni, peab teil olema Azure'is kohandatud salvestuskonto, et Machine Learning pääseks ajalooliste andmete juurde.

## <a name="default-parameters-and-values-for-demand-forecasting-models"></a><a name="model-parameters"></a> Nõudluse prognoosimise mudelite vaikeparameetrid ja väärtused

Kui kasutate masinaõppimist prognoosiplaanimise mudelite loomiseks, kontrollite masina õppevalikuid, seades prognoosi *algoritmi parameetritele* väärtused. Need väärtused saadetakse tarneahela haldustest Azure'i masinaõppimiseks. Kasutage prognoosi **algoritmi parameetrite lehte, et kontrollida, millised väärtused tuleb esitada ja millised väärtused** igal peaks olema.

Nõudluse prognoosimise mudelite jaoks kasutatavate vaikeparameetrite ja väärtuste seadistamiseks minge koondplaneerimise häälestamise nõudluse **\> prognoosi \> prognoosimise \> algoritmi** parameetrid. Antakse standardne parameetrite kogum. Igal parameetril on järgmised väljad:

- **Nimi** – parameetri nimi, nagu seda kasutab Azure. Tavaliselt ei tohiks seda nime muuta, kui te pole katset Azure Machine Learningis kohandanud.
- **Kirjeldus** – parameetri tavanimi. Seda nime kasutatakse parameetri tuvastamiseks süsteemi teistes kohtades (nt lehel **Nõudluse prognoosimise** parameetrid).
- **Väärtus** – parameetri vaikeväärtus. Väärtus, mida peate sisestama, sõltub redigeeri kasutatavast parameetrist. 
- **Selgitus** – parameetri lühikirjeldus ja selle kasutamise. See kirjeldus hõlmab tavaliselt soovitust väärtusevälja kehtivate **väärtuste** kohta.

Järgmised parameetrid on antud vaikimisi. (Kui peate selle standardloendi alati taastama, valige **Taasta** tegevuspaanil.)

- **Usaldusväärsuse taseme protsent** - Usaldusvahemik koosneb väärtuste vahemikust, mille järgi on nõudluse prognoosi hea hinnata. Usaldusväärsuse tase 95% näitab, et on olemas 5% tõenäosus, et tulev nõudlus jääb usaldusväärsusintervalli vahemikust välja.
- **Hooajalisus** ( Force seasonality) – määrab, kas mudel peab kasutama kindlat tüüpi hooajalist. See parameeter kehtib ainult ARIMA ja ETS-i puhul. Valikud: *AUTOMAATNE (vaikimisi)*, *POLE*, *LISAND,* *KORRUTATAV*.
- **Eelarvemudel** – määrab, millist eelarvemudelit kasutada. Valikud: *ARIMA*, *ETS*, *STL,* *ETS+ARIMA,* *ETS+STL,* *KÕIK*. Parima sobivuse mudeli valimiseks kasutage nuppu *KÕIK*.
- **Maksimaalne prognoositav väärtus** - määrab prognoosimiseks kasutatava maksimaalse väärtuse. Vorming: +1E [n] või arvuline konstant.
- **Minimaalne prognoositav väärtus** - Määrab prognoosimiseks kasutatava minimaalse väärtuse. Vorming: -1E [n] või arvuline konstant.
- **Puuduva väärtuse asendamine** - Määrab, kuidas varasemate andmete lüngad täidetakse. Valikud: *(arvuline väärtus)*, *KESKMINE*, *·* *EELMINE,VÄLJAMINEV* LINEAARNE, *MATEMAATILINE* ID.
- **Puuduva väärtuse asendamise ulatus** - Määrab, kas väärtuse asendus rakendub ainult iga üksiku granuleeritud atribuudi või tervele andmekomplektile. Järgmised valikud on saadaval, et luua kuupäevavahemik, mida süsteem kasutab ajalooliste andmete lünkade täitmisel:

    - *GLOBAALNE* – süsteem kasutab kõigi granulaarsuse atribuutide täielikku kuupäevavahemikku.
    - *HISTORY_DATE_RANGE määranud – süsteem kasutab kindlat kuupäevavahemikku, mille määratleb dialoogiboksi Statistilise alusprognoosi loomine jaotise Ajalooline vahemik väljadega Alates ja* **Kuni** **·** **·** **kuupäevani**.
    - *GRANULARITY_ATTRIBUTE –* süsteem kasutab praegu töödeldud granulaarsusatribuudi kuupäevavahemikku.

    > [!NOTE]
    > Granulaarsuse atribuut on prognoosi dimensioonide kombinatsioon, mille suhtes prognoos tehakse. Saate prognoosi dimensioonid määrata **Nõudluse prognoosimise parameetrid** lehel.

- **Hooajalisuse vihje** - Hooajaliste andmete puhul saate prognoosi täpsuse parandamiseks lisada vihje prognoosimise mudelile. Vorming– täisarv, mis näitab vahemike arvu, mille puhul nõudluse muster end kordab. Näiteks sisestage *6* andmete puhul, mis kordavad end iga kuue kuu järel.
- **Proovikogumi suuruse protsent** - Ajalooliste andmete protsent, mida kasutatakse proovikogumina prognoosi täpsuse arvutamiseks.

Nende parameetrite väärtused saate alistada, kui saadate koondplaneerimise seadistuse nõudluse **\>\> prognoosimise \> nõudluse prognoosimise** parameetrid. Nõudluse **prognoosimise parameetrite** lehel saate parameetrid alistada järgmistel viisidel:

- Kasutage **parameetri** globaalseks alistamiseks vahekaarti Üldine.
- Kasutage kauba **eraldamisvõtmete** vahekaarti, et alistada konkreetsete kauba eraldamisvõtmete parameetrid. Konkreetse kauba eraldamisvõtme alistatud parameetrid mõjutavad ainult selle kauba eraldamisvõtmega seotud kaupade eelarvet.

> [!NOTE]
> Prognoosi algoritmi parameetrite lehel saate kasutada tegumiriba nuppe, lisada loendisse parameetreid või eemaldada **parameetreid** loendist. Kuid tavaliselt ei tohiks te seda lähenemist kasutada, kui te pole katset kohandanud Azure Machine Learningis.

## <a name="set-up-the-azure-machine-learning-service"></a><a name="setup-amls"></a> Azure Machine Learning Service'i häälestamine

Tarneahela haldus arvutab nõudluse prognoosid Azure Machine Learning Service'i abil, mille peate seadistama ja käitama oma Azure'i kordustellimusel. See jaotis kirjeldab, kuidas seadistada Azure Machine Learning Service Azure'is ja seejärel ühendada see tarneahela haldamise keskkonnaga.

### <a name="enable-the-azure-machine-learning-service-in-feature-management"></a>Lubage Azure'i masinaõppimisteenus funktsioonihalduses

Enne Kui saate kasutada Azure Machine Learning Service'i nõudluse prognoosimiseks, peate integreerimise lubamiseks lülitama sisse tarneahela halduse funktsiooni. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *Koondplaneerimine*
- **Funktsiooni nimi:** *Azure Machine Learning Service nõudluse prognoosimiseks*

### <a name="set-up-machine-learning-in-azure"></a><a name="ml-workspace"></a> Saate häälestada masinaõppimist Azure'is.

Et Lubada Azure'is kasutada prognooside töötlemiseks masina õppet, peate selleks otstarbeks seadistama Azure'i masina õppe tööruumi. Teil on kaks valikut:

- Tööruumi häälestamiseks Microsofti antud skripti käivitamiseks järgige juhiseid [valikus 1: käivitage skript, et automaatselt seadistada oma arvuti õppe tööruumi](#ml-workspace-script) jaotis ja seejärel minge edasi [Azure'i masina õppeteenuse ühenduse parameetrite juurde tarneahela halduses](#demand-forecast-parameters).
- Tööruumi käsitsi häälestamiseks järgige juhendit [2. valik: käsitsi häälestage masina õppe tööruumi](#ml-workspace-manual) jaotis ja seejärel minge edasi [Azure Machine Learning Service'i ühenduse parameetrite häälestamiseks tarneahela halduses](#demand-forecast-parameters). See valik võtab rohkem aega, kuid annab teile rohkem kontrolli.

#### <a name="option-1-run-a-script-to-automatically-set-up-your-machine-learning-workspace"></a><a name="ml-workspace-script"></a> 1. valik: käivitage skript, et automaatselt seadistada oma masina õpperuum

See jaotis kirjeldab, kuidas seadistada masina õppe tööruumi, kasutades Microsofti antud automaatset skripti. Soovi korral saate kõik ressursid käsitsi seadistada, järgides juhiseid valikus 2: seadistage käsitsi oma masina [õppe tööruumi](#ml-workspace-manual) jaotis. Te ei pea mõlemat valikut lõpule viima.

1. Avage GitHubis malle nõudluse prognoosimiseks [Dynamics 365 Supply Chain Management Azure Machine](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) Learningi hoidlaga (repo) ja laadige alla järgmised failid:

    - quick_setup.ps1
    - sampleInput.csv
    - rc/parameters.py
    - src/api_trigger.lisa
    - rc/run.py
    - src/REntryScript/forecast.r

1. Avage powerShelli aken ja käivitage eelmises sammus alla laaditud **skript** quick_setup.ps1. Järgige ekraanil toodud juhiseid. Skript seadistab nõutava tööruumi, salvestuse, vaikeandmelao ja andmetöötlusressursse. Nõutavad konveierid tuleb siiski luua, järgides protseduuri järelejäänud etappe. (Müügivõimaluste abil saab käivitada tarneahela haldusskriptide prognoosimise.)
1. Azure Machine Learning Studios laadige üles sammus 1 allalaaditud **fail sampleInput.csv** konteinerisse nimega *virtuaalplan-azureml.* (Selle konteineri quick_setup.ps1 skript.) See fail on vajalik müügivõimaluste avaldamiseks ja katseprognoosi loomiseks. Juhiseid vt [blokeerimisbloki](/azure/storage/blobs/storage-quickstart-blobs-portal#upload-a-block-blob) üleslaadimine.
1. Azure Machine Learning Studios valige **navigaator** navigatsioonistuudios Arvutid.
1. Failistruktuuris leiate järgmise **asukoha**: **kasutajad/ \[praegune \] kasutaja/src.**
1. Laadige ülejäänud neli faili, mille sammus 1 alla laadisite eelmises sammus leitud asukohta.
1. Valige **äsja üleslaaditud api_trigger.meetri** fail ja käivitage see. See loob müügivõimaluste, mille saab API kaudu käivitada.
1. Teie tööruum on nüüd häälestatud. Jäta ette [jaotisest Azure Machine Learning Service ühenduse parameetrid Tarneahela](#demand-forecast-parameters) haldus.

#### <a name="option-2-manually-set-up-your-machine-learning-workspace"></a><a name="ml-workspace-manual"></a> 2. valik: seadistage käsitsi oma masina õpperuum

See jaotis kirjeldab, kuidas käsitsi seadistada oma masina õpperuumi. Käesoleva jaotise protseduurid peate lõpule viima ainult siis, kui otsustate automaatse installiskripti mitte käitada, nagu on kirjeldatud juhendis Valik 1. Käivitage skript, et seadistada oma masina õppe [tööruumi](#ml-workspace-script) jaotis.

##### <a name="step-1-create-a-new-workspace"></a><a name="create-workspace"></a> 1. etapp: uue tööruumi loomine

Kasutage järgmist protseduuri uue masina õppe tööruumi loomiseks.

1. Logige oma Azure'i portaali sisse.
1. Saate avada **masina** õppeteenuse.
1. Viisardi **Loomine** avamiseks valige **tööriistaribal käsk** Loo.
1. Viige viisard lõpule, järgides ekraanil kuvatavaid juhiseid. Pidage järgmisi punkte silmas, kui töötate:

    - Kasutage vaikesätteid, kui selles loendis ei soovitata erinevaid sätteid.
    - Valige kindlasti geograafiline piirkond, mis vastab regioonile, kus teie tarneahela halduseksemplari juurutatakse. Vastasel juhul võivad mõned teie andmed läbida regiooni piirid. Lisateabe saamiseks vt selles [teemas hiljem](#privacy) privaatsusteatist.
    - Kasutage sihtotstarbeliseid ressursse, nt ressursigruppe, salvestuskontosid, konteinerite registriid, Azure'i võtme vaulte ja ressursiressursse.
    - Viisardi **lehel Azure Machine Learning Service ühenduse parameetrite** häälestamiseks peate andma talletuskonto nime. Kasutage kontot, mis on seotud nõudluse prognoosimisega. Nõudluse prognoosimise sisend- ja väljundandmed talletatakse sellel ladustamiskontol.

Lisateavet vt teemast [Tööruumi](/azure/machine-learning/quickstart-create-resources#create-the-workspace) loomine.

##### <a name="step-2-configure-storage"></a><a name="config-storage"></a> 2. etapp: ladustamise konfigureerimine

Kasutage ladustamise häälestamiseks järgmist protseduuri.

1. Avage GitHub mallid nõudluse prognoosimiseks azure Machine Learningi taaspoga ja laadige [Dynamics 365 Supply Chain Management alla fail](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service)**sampleInput.csv.**
1. Avage ladustamiskonto, mille lõite [sammus 1: looge uus tööruumi](#create-workspace) jaotis.
1. Järgige juhendit [konteineri](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container) loomiseks, et luua konteiner nimega *laiendusplan-azureml.*
1. Laadige **sammus 1 alla laaditud fail sampleInput.csv äsja** loodud konteinerisse. See fail on vajalik müügivõimaluste avaldamiseks ja katseprognoosi loomiseks. Juhiseid vt [blokeerimisbloki](/azure/storage/blobs/storage-quickstart-blobs-portal#upload-a-block-blob) üleslaadimine.

##### <a name="step-3-configure-a-default-datastore"></a>3. etapp: vaikeandmekaupluse konfigureerimine

Kasutage järgmist protseduuri, et seadistada oma vaikeandmepood.

1. Valige Azure Machine Learning **Studios teesaatoris** andmekauplused.
1. Looge Uus Azure Bloobi mäluseadme tüübi andmekomplekt, mis osutab azureml azureml ladustamise konteinerile, mille *lõite* *·*[2. sammus: ladustamisjao](#config-storage) konfigureerimine. (Kui uue andmekaupluse autentimise tüüp on <a0/&) *Kontovõti* – sisestage loodud ladustamiskontole kontovõti. Juhiseid vt ladustamiskonto [juurdepääsuvõtmete haldamine](/azure/storage/common/storage-account-keys-manage?tabs=azure-portal) .)
1. Seadistage uus andme talletamis vaikimisi andme talletuseks, avades selle üksikasjad ja valides **käsu Seadista vaikeandmepoena.**

##### <a name="step-4-configure-compute-resources"></a><a name="config-compute-resources"></a> 4. etapp: andmetöötlusressursside konfigureerimine

Kasutage järgmist protseduuri andmetöötlusressursi häälestamiseks Azure Machine Learning Studios, et käivitada prognoosi loomise skriptid.

1. Avage 1. etapis loodud masina õppe tööruumi üksikasjade [leht: looge uus tööruumi](#create-workspace) jaotis. Leidke **Studio veebi** URL-i väärtus ja valige link selle avamiseks.
1. Valige **navigeerimispaanil** arvutamine.
1. Vahekaardil **Arvuta eksemplarid valige uus, et avada** **viisard**, mis aitab teil luua uue arvutuseksemplari. Järgige ekraanil toodud juhiseid. Andmetöötluseksemplari kasutatakse nõudluse prognoosimise müügivõimaluste loomiseks (Selle saab kustutada pärast müügivõimaluste avaldamist.) Kasutage vaikesätteid.
1. Vahekaardil **Kogumite** arvutamine valige suvand Uus, et **avada** viisard, mis aitab teil luua uue arvutuskogumi. Järgige ekraanil toodud juhiseid. Andmetöötluskogumit kasutatakse nõudluse prognooside loomiseks. Selle sätted mõjutavad käituse jõudlust ja paralleelsuse maksimaalset taset. Seadistage järgmised väljad, kuid kasutage kõigi muude väljade vaikesätteid:

    - **Nimi** – *sisestage e2ecpuruluster.*
    - **Virtuaalmasina** suurus – korrigeerige seda sätet vastavalt andmete mahule, mida eeldate kasutada sisendina nõudluse prognoosimiseks. Sõlmede arv ei tohi ületada 11, kuna nõudluse prognoosi loomise käivitamiseks on vaja ühte sõlme ja maksimumarv sõlmede arvu, mida saab seejärel prognoosi loomiseks kasutada, on 10. (Määrate sõlmede arvu ka parameters.py failis [5. etapp: konveierite](#create-pipelines) sektsiooni loomine.) Igas sõlmes on mitu töötajaprotsessi, mis käivitavad prognoosiskripte paralleelselt. Töötaja protsesside koguarv teie töös on tuumade arv, mida *sõlmel* × *loendada*. Näiteks kui teie arvutatud kobara tüüp on *Standardne D4 (kaheksa tuuma) ja kuni 11 sõlme ning kui parameters.py-failis on väärtuseks seatud 10, on paralleelsuse tegelik tase \_*`nodes_count`*80*.

##### <a name="step-5-create-pipelines"></a><a name="create-pipelines"></a> 5. etapp: müügivõimaluste loomine

Müügivõimaluste abil saab käivitada tarneahela haldamisest prognoosi skripte. Kasutage nõutavate konveierite loomiseks järgmist protseduuri.

1. Avage GitHubis malle nõudluse prognoosimiseks [Dynamics 365 Supply Chain Management rakendusega Azure Machine Learning](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) repo ja laadige alla järgmised failid:

    - rc/parameters.py
    - src/api_trigger.lisa
    - rc/run.py
    - src/REntryScript/forecast.r

1. Azure Machine Learning Studios valige **navigaator** navigatsioonistuudios Arvutid.
1. Failistruktuuris leiate järgmise **asukoha**: **kasutajad/ \[praegune \] kasutaja/src.**
1. Laadige üles neli faili, mille alla laadisite sammus 1 eelmises sammus leitud asukohta.
1. Azure'is avage ja vaadake **parameters.py** fail, mille äsja üles laadisite. Veenduge, et väärtus on üks väiksem kui väärtus, mille konfigureerisid arvutuskogumi jaoks sammus `nodes_count`[4: arvuta ressursside](#config-compute-resources) konfigureerimine. Kui `nodes_count` väärtus on suurem kui sõlmede arv arvutamiskogumis või sellega võrdne, võib müügivõimaluste käitamine olla võimeline käivituma. Kuid see lõpetab siis vastamise, kuni ootab nõutavaid ressursse. Lisateavet sõlmede arvu kohta vt sammust [4: andmetöötlusressursside](#config-compute-resources) konfigureerimine.
1. Valige **äsja üleslaaditud api_trigger.meetri** fail ja käivitage see. See loob müügivõimaluste, mille saab API kaudu käivitada.

### <a name="set-up-a-new-active-directory-application"></a><a name="aad-app"></a> Uue Active Directory rakenduse seadistamine

Active Directory rakendus on vajalik autentimiseks ressurssidega, mis on seotud nõudluse prognoosimisega teenuse subjekti abil. Seetõttu peaks rakendusel olema madalaim privileegitase, mis on prognoosi loomiseks vajalik.

1. Logige oma Azure'i portaali sisse.
1. Registreerige uus avaldus rentnikule Azure Active Directory Azure AD (). Juhiseid vt portaalist, et luua rakendus ja teenuse [Azure AD subjekt, mis pääseb juurde](/azure/active-directory/develop/howto-create-service-principal-portal) ressurssidele.
1. Järgige viisardi lõpuleviimisel ekraanil olevaid juhiseid. Kasutage vaikesätteid.
1. Andke oma uuele Active Directory rakendusele juurdepääs järgmistele ressurssidele, mille lõite [jaotises Azure'i seadme õppe](#ml-workspace) loonud. Juhiseid vt [Azure'i rollide määramine Azure'i portaali](/azure/role-based-access-control/role-assignments-portal?tabs=current) abil. See samm võimaldab süsteemil importida ja eksportida prognoosimisandmeid ja käivitada masina õppevõimaluste käivitamise tarneahela halduses.

    - Rolliroll masina õppe tööruumile
    - Rolli rolli sihtotstarbelisele ladustamiskontole
    - Talletus bloobiandmete rolli sihtotstarbelisele ladustamiskontole

1. Loodud **avalduse jaotises** Tunnistused &saladused looge avalduse jaoks saladus. Juhiseid vt teemast [Kliendisaladuse](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret) lisamine.
1. Märkige rakenduse ID ja selle saladus üle. Te vajate selle rakenduse üksikasju hiljem, kui häälestate tarneahela **halduses nõudluse** prognoosimise parameetrite lehe.

### <a name="set-up-azure-machine-learning-service-connection-parameters-in-supply-chain-management"></a><a name="demand-forecast-parameters"></a> Azure'i masina õppeteenuse ühenduse parameetrite seadistamine tarneahela halduses

Kasutage järgmist protseduuri, et ühendada tarneahela halduskeskkond masina õppeteenusega, mille äsja Azure'is seadistate.

1. Logige sisse rakendusse Supply Chain Management.
1. Minge **koondplaneerimise \> häälestamise \> nõudluse \> prognoosimise prognoosimise** parameetritesse.
1. Vahekaardil Üldine veenduge, et prognoosi loomise strateegia väli on seatud väärtusele **Azure** Machine **Learning** *Service*.
1. Vahekaardil Kauba eraldamisvõtmed veenduge, et prognoosi loomise strateegia väli on seadistatud valikule Azure Machine Learning Service igale eraldamisvõtmele, mis peaks kasutama Azure Machine Learning Service'i **nõudluse** **·** *prognoosimiseks*.
1. Seadke **vahekaardil Azure Machine Learning Service** järgmised väljad:

    - **Rentniku ID** – sisestage oma Azure'i rentniku ID. Tarneahela haldus kasutab seda ID-d autentimiseks Azure'i masinaõppimisteenusega. Oma rentniku ID leiate **Azure'i** portaali ülevaate Azure AD leheküljelt.
    - **Teenuse põhirakenduse ID** – sisestage rakenduse ID rakendusele, mille lõite [Active Directory rakenduse](#aad-app) jaotises. Seda väärtust kasutatakse API taotluste autoriseerimiseks Azure Machine Learning Service'ile.
    - **Teenuse subjekti saladus – sisestage teenuse põhirakenduse saladus rakenduse** jaoks, mille [lõite Active Directory rakenduse](#aad-app) jaotises. Seda väärtust kasutatakse juurdepääsu loa omandamiseks turbesubjekti jaoks, mille lõite autoriseeritud toimingute sooritamiseks Azure'i mälu ja Azure'i masinakeele tööruumi vastu.
    - **Salvestuskonto nimi** – sisestage Azure'i salvestuskonto nimi, mille määras häälestusviisardi oma Azure'i tööruumis. (Lisateavet vt teemast [Seadistage masina õppimine Azure'i](#ml-workspace) jaotises.)
    - **Müügivõimaluste** lõpp-punkti aadress – sisestage konveieri ÜLEJÄÄNUD lõpp-punkti URL oma Azure'i masina õppeteenuse jaoks. Te lõite selle müügivõimaluste viimase sammuna, kui seadistate masina [õppe Azure'is.](#ml-workspace) Müügivõimaluste URL-i loomiseks logige sisse Oma Azure'i portaali ja valige **navigeerimise** müügivõimalustest. Valige vahekaardil **Müügivõimaluste** lõpp-punkt nimega **TriggerDemandForecastGeneration.** Seejärel kopeerige näidatav lõpp-punkt REST.

    ![Parameetrid vahekaardil Azure Machine Learning Service lehel Nõudluse prognoosimise parameetrid.](media/azure-ml-service-parameters.png "Parameetrid nõudluse prognoosimise parameetrite lehe vahekaardil Azure Machine Learning Service")

## <a name="privacy-notice"></a><a name="privacy"></a>Privaatsusavaldus

Kui valite prognoosi loomise strateegiaks Azure Machine Learning Service, saadab tarneahela haldus automaatselt teie kliendiandmed ajaloolise nõudluse kohta, nt liidetud kogused, tootenimed ja nende tootedimensioonid, lähetus- ja vastuvõtukohad, kliendi identifikaatorid ja prognoosiparameetrid, selle geograafilises piirkonnas, kus asuvad teie masina õpperuum ja sellega seotud ladustamise *konto*, tulevaste nõuete prognoosimiseks. Azure Machine Learning Service võib olla erinevas geograafilises piirkonnas kui geograafiline piirkond, kus tarneahela haldus juurutatakse. Mõned kasutajad saavad kontrollida, kas see funktsioon on lubatud, valides prognoosi loomise strateegia lehel **Nõudluse prognoosimise** parameetrid.

## <a name="additional-resources"></a>Lisaressursid

- [Nõudluse prognoosimise ülevaade](introduction-demand-forecasting.md)
- [Statistilise alusprognoosi loomine](generate-statistical-baseline-forecast.md)
- [Alusprognoosis käsitsi korrigeerimiste tegemine](manual-adjustments-baseline-forecast.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
