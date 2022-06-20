---
title: Koondplaneerimine koos nõudluse prognoosidega
description: See artikkel selgitab, kuidas kaasata nõudluse prognoosid koondplaneerimisel plaanimise optimeerimise ajal.
author: t-benebo
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup, ReqReduceKey, ForecastModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 63221b5270416cad9cdfb586c697d7700f3b561b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878986"
---
# <a name="master-planning-with-demand-forecasts"></a>Koondplaneerimine koos nõudluse prognoosidega

[!include [banner](../../includes/banner.md)]

Saate kasutada nõudluse prognoosi koos planeerimise optimeerimisega, et võtta arvesse koondplaneerimises eeldatavat nõudlust. Saate luua käsitsi nõudluse prognoosi, importida selle või luua selle rakenduse Microsoft Dynamics 365 Supply Chain Management nõudluse prognoosi funktsiooni abil. Lisateavet nõudluse prognoosi kohta leiate teemast [Nõudluse prognoosi ülevaade](../introduction-demand-forecasting.md).

> [!NOTE]
> Planeerimise optimeerimise korral ei toetata eraldi prognoosi planeerimist. Seetõttu ei ole sättel **Praegune eelarveplaan**, mis asub lehel **Koondplaneerimise parameetrid**, mingit mõju, kui kasutate planeerimise optimeerimist.

## <a name="set-up-a-master-plan-to-include-a-demand-forecast"></a>Koondplaani seadistamine nõudluse prognoosi kaasamiseks

Järgige neid juhiseid, et konfigureerida koondplaan nii, et see hõlmaks nõudluse prognoosi.

1. Avage **Koondplaneerimine \> Seadistus \> Plaanid \> Koondplaanid**.
1. Valige olemasolev plaan või looge uus plaan.
1. Määrake kiirkaardil **Üldine** järgmised väljad.

    - **Eelarvemudel** – valige rakendatav eelarvemudel. Seda mudelit võetakse arvesse, kui praeguse koondplaani jaoks luuakse tarnesoovitus.
    - **Kaasa nõudluse prognoos** – seadke selle suvandi väärtuseks *Jah*, et kaasata nõudluse prognoos praegusse koondplaani. Kui seate selle väärtuseks *Ei*, ei kaasata koondplaani nõudluse prognoosi kandeid.
    - **Prognoosinõuete vähendamiseks kasutatav meetod** – valige meetod, mida tuleks kasutada prognoosinõuete vähendamiseks. Lisateavet vt selle artikli jaotisest [Eelarve vähendamise](#reduction-keys) võtmed.

1. Kiirkaardil **Ajapiir päevades** saate seada järgmised väljad, et määrata periood, mille jooksul on nõudluse prognoos kaasatud.

    - **Eelarveplaan** – määrake selle suvandi väärtuseks *Jah*, et alistada üksikutest laovarude gruppidest pärinev eelarveplaani ajapiir. Seadke selle väärtuseks *Ei*, et kasutada praeguse koondplaani jaoks üksikute laovarude gruppide väärtuseid.
    - **Prognoosi ajavahemik** – kui seate suvandi **Eelarveplaan** väärtuseks *Jah*, määrake päevade arv (alates tänasest kuupäevast), mida nõudluse prognoosi korral rakendada.

    > [!IMPORTANT]
    > Planeerimise optimeerimise korral ei toetata praegu veel sätet **Eelarveplaan**.

## <a name="set-up-a-coverage-group-to-include-a-demand-forecast"></a>Laovarude grupi seadistamine nõudluse prognoosi kaasamiseks

Järgige neid juhiseid, et konfigureerida laovarude grupp nii, et see hõlmaks nõudluse prognoosi.

1. Valige **Koondplaneerimine \> Seadistus \> Plaanid \> Laovarude grupid**.
1. Valige olemasolev laovarude grupp või looge uus grupp.
1. Määrake kiirkaardil **Muu** järgmised väljad.

    - **Eelarveplaani ajapiir** – sisestage päevade arv (alates tänasest kuupäevast), mille korral tuleks nõudluse prognoosi rakendada. Selle väärtuse saab alistada koondplaani suvandi **Eelarveplaan** abil, nagu kirjeldati eelmises jaotises.
    - **Planeerimise koefitsient** – valige rakendatav planeerimise koefitsient. Lisateavet vt jaotisest Eelarve vähendamise [võtme loomine ja](#create-reduction-key)[seadistamine ning selles artiklis jaotiste](#use-reduction-key) Kasutamine vähendamisvõtme abil.
    - **Prognoosi vähendamisalus** – määratlege koondplaanide korral, kus suvandi **Prognoosinõuete vähendamiseks kasutatav meetod** väärtuseks on seatud *Kanded – planeerimise koefitsient* või *Kanded – dünaamiline periood*, millised kanded peaksid prognoosi vähendama. Valige üks järgmistest väärtustest.

        - **Kõik kanded** – kõik kanded peaksid vähendama prognoosi.
        - **Tellimused** – prognoosi peaks vähendama ainult müügitellimused.

        > [!NOTE]
        > Kui valite *Kõik kanded*, loetakse kanded, millel on samades varude dimensioonides nõudlus ja pakkumine, neutraalseks ja neid ignoreeritakse prognoosi vähendamisel. Näiteks kui planeerimise dimensioon on seatud ainult tegevuskohale, mitte laole, eiratakse üleviimistellimust tegevuskoha 1 laost 11 tegevuskoha 1 lattu 13 ega vähendata järelejäänud nõudluse prognoosi.

    - **Kaasa kontsernisisesed tellimused** – määrake selle suvandi väärtuseks *Jah*, kui prognoosi vähendamisel tuleks kaasata kontsernisisesed tellimused. Muul juhul seadke selle väärtuseks *Ei*.
    - **Kaasa kliendiprognoos nõudluse prognoosi** – määrake, kas kliendiprognoos tuleks kaasata üldisesse prognoosi. See valik määratleb, kuidas tegelik nõudlus prognoositud nõudlust vähendab. Saate seda kasutada tagamaks, et koondplaneerimine hõlmab kindlate klientide ostetud kaupade tarnet.

        - Seadistage selle suvandi väärtuseks *Jah*, et kaasata kliendiprognoos üldisesse prognoosi. Sel juhul vähendab kliendi tegelik nõudlus nii kliendi- kui ka üldist prognoosi. Koondplaneerimine loob plaanitud tellimused, mis hõlmavad ainult kogu prognoositavat kogust.
        - Seadistage selle suvandi väärtuseks *Ei*, kui te ei taha kliendiprognoosi üldisesse prognoosi kaasata. Sel juhul vähendab kliendi tegelik nõudlus ainult kliendiprognoosi. Koondplaneerimine loob plaanitud tellimused, mis hõlmavad nii üldist prognoositavat kogust kui ka iga kliendi koguse prognoosi.

## <a name="forecast-reduction-keys"></a><a name="reduction-keys"></a>Eelarve planeerimise koefitsiendid

Selles jaotises kirjeldatakse eri meetodeid, mida kasutatakse prognoosinõuete vähendamiseks. Iga meetodi tulemuste kohta on toodud näited. Samuti selgitatakse, kuidas eelarve planeerimise koefitsienti luua, seadistada ja kasutada. Mõni meetod kasutab eelarvevajaduste vähendamiseks eelarve planeerimise koefitsienti.

### <a name="methods-that-are-used-to-reduce-forecast-requirements"></a>Meetodid, mida kasutatakse eelarvevajaduste vähendamiseks

Kui kaasate koondplaani eelarve, saate valida, kuidas vähendatakse eelarvevajadusi, kui kaasatud on tegelik nõudlus. Pange tähele, et koondplaneerimine välistab mineviku eelarvevajadused ehk kõik eelarvevajadused enne tänast kuupäeva.

Selleks, et eelarve koondplaani kaasata ja eelarvevajaduste vähendamise meetod valida, valige **Koondplaneerimine \> Seadistus \> Plaanid \> Koondplaanid**. Valige väljal **Eelarvemudel** sobiv eelarvemudel. Valige väljal **Eelarvevajaduste vähendamiseks kasutatav meetod** sobiv meetod. Valikud on järgmised:

- Puudub
- Protsent – planeerimise koefitsient
- Kanded – planeerimise koefitsient
- Kanded – dünaamiline periood

Järgmised jaotised annavad iga suvandi kohta lisateavet.

#### <a name="none"></a>Puudub

Kui valite suvandi **Puudub**, siis ei vähendata koondplaneerimisel eelarvevajadusi. Sellisel juhul loob koondplaneerimine plaanitud tellimused, et täita prognoositud nõudlust (eelarvevajadusi). Need plaanitud tellimused hoiavad soovitatud kogust vaatamata teistele nõudlustüüpidele. Näiteks loob koondplaneerimine müügitellimuste esitamisel täiendavad plaanitud tellimused, et müügitellimusi täita. Eelarvevajaduste kogust ei vähendata.

#### <a name="percent--reduction-key"></a>Protsent – planeerimise koefitsient

Kui valite suvandi **Protsent – planeerimise koefitsient**, siis vähendatakse eelarvevajadusi planeerimise koefitsiendiga määratud protsentide ja perioodide kohaselt. Sellisel juhul loob koondplaneerimine plaanitud tellimusi, milles arvutatakse kogust iga perioodi jaoks valemiga hinnanguline kogus × planeerimise koefitsient. Kui teisi nõudlustüüpe pole, siis loob koondplaneerimine nõudluse täitmiseks ka plaanitud tellimused.

##### <a name="example-percent--reduction-key"></a>Näide: valik Protsent – planeerimise koefitsient

See näide selgitab, kuidas vähendab planeerimise koefitsient nõudluse prognoosi nõudeid planeerimise koefitsiendiga määratletud protsentide ja perioodide alusel.

Selle näite jaoks kaasate koondplaani järgmised nõudluse prognoosid.

| Kuu    | Nõudluse prognoos |
|----------|-----------------|
| Jaanuar  | 1000           |
| veebruar | 1000           |
| märts    | 1000           |
| aprill    | 1000           |

Seadistage lehel **Planeerimise koefitsiendid** järgmised read.

| Muutmine | Ühik  | Protsent |
|--------|-------|---------|
| 1      | Kuu | 100     |
| 2      | Kuu | 75      |
| 3      | Kuu | 50      |
| 4      | Kuu | 25      |

Määrake planeerimise koefitsient kauba laovarude grupile. Seejärel valige lehe **Koondplaanid** väljal **Eelarvevajaduste vähendamiseks kasutatav meetod** suvand **Protsent – planeerimise koefitsient**.

Kui käivitate sellisel juhul eelplaneerimise 1. jaanuaril, tarbitakse nõudluse prognoosi nõudeid lehel **Planeerimise koefitsiendid** seadistatud protsentide järgi. Koondplaani kantakse üle järgmised vajaduse kogused.

| Kuu                | Plaanitud tellimuse kogus | Kalkulatsioon    |
|----------------------|------------------------|----------------|
| Jaanuar              | 0                      | = 0% × 1000   |
| veebruar             | 250                    | = 25% × 1000  |
| märts                | 500                    | = 50% × 1000  |
| aprill                | 750                    | = 75% × 1000  |
| Mai kuni detsember | 1000                  | = 100% × 1000 |

#### <a name="transactions--reduction-key"></a>Kanded – planeerimise koefitsient

Kui seate välja **Eelarvenõuded vähendamiseks kasutatava meetodi** väärtuseks *Kanded – vähendamise klahv* vähendatakse eelarve vajadusi kvalifitseeritud nõudluse kannete võrra, mis toimuvad vähendamisvõtmega määratletud perioodidel.

Kvalifitseeritud nõudluse määratleb **Vähenda lprognoosi** väli **Katvusgrupid** leht. Kui seate **Vähenda prognoosi** välja seadeks *Tellimused*, ainult müügitellimuse kanded kvalifitseeritud nõudluseks. Kui seadistate selle *Kõigile kannetele*, peetakse kõiki mitte kontsernisiseseid väljamineku laokandeid kvalifitseeritud nõudluseks. Kui prognoosi vähendamisel tuleks kaasata kontsernisisesed tellimused, seadke suvandi **Kaasa kontsernisisesed tellimused väärtuseks** väärtuseks *Jah*.

Prognoosi vähendamine algab nõudluse esimese (varaseima) prognoosi kirjega vähendamisest võtme perioodil. Kui kvalifitseeritud laokannete kogus on suurem kui nõudluse prognoosi ridade kogus samas vähendamise võtme perioodis, kasutatakse laokannete koguse saldot nõudluse prognoosi koguse vähendamiseks eelmises perioodis (kui on kinnitamata prognoos).

Kui eelmisesse vähendusvõtme perioodi ei ole jäänud ühtegi kinnitamata eelarvet, kasutatakse laokannete koguse saldot eelarve koguse vähendamiseks järgmisel kuul (kui prognoosi pole kokkuleppinud).

**Protsendi** välja väärtus kui **eelarvenõuete vähendamiseks kasutatava meetodi** väli on seatud väärtusele *Kanded – vähendamisvõti*. Vähendusvõtme perioodi määratlemiseks kasutatakse ainult kuupäevi.

> [!NOTE]
> Kõiki tänasele kuupäevale või enne seda sisestatud eelarvet ignoreeritakse ja seda ei kasutata plaanitud tellimuste loomiseks. Näiteks kui teie kuu nõudluse prognoos on loodud 1. jaanuaril ja te käivitate koondplaanimise, mis hõlmab nõudluse prognoosi 2. jaanuaril, ignoreerib kalkulatsioon nõudluse prognoosi rida, mille kuupäev on 1. jaanuar.

##### <a name="example-transactions--reduction-key"></a>Näide: valik Kanded – planeerimise koefitsient

See näide selgitab, kuidas vähendavad planeerimise koefitsiendiga määratletud perioodide ajal tehtavad tegelikud tellimused nõudluse prognoosi nõudeid.

[![Tegelikud tellimused ja prognoosid enne koondplaneerimise käivitamist.](media/forecast-reduction-keys-1-small.png)](media/forecast-reduction-keys-1.png)

Selle näite jaoks valige lehe *Koondplaanid* väljal **Eelarvevajaduste vähendamiseks kasutatav meetod** suvand **Kanded – planeerimise koefitsient**.

1. aprillil on olemas järgmised nõudluse prognoosi read.

| Kuupäev     | Prognoositud tükkide arv |
|----------|-----------------------------|
| 5. aprill  | 100                         |
| 12. aprill | 100                         |
| 19. aprill | 100                         |
| 26. aprill | 100                         |
| 3. mai    | 100                         |
| 10. mai   | 100                         |
| 17. mai   | 100                         |

Järgmised müügitellimuse read on aprillis olemas.

| Kuupäev     | Taotletud tükkide arv |
|----------|----------------------------|
| 27. aprill | 240                        |

[![Aprilli tellimuste põhjal loodud plaanitud tarne.](media/forecast-reduction-keys-2-small.png)](media/forecast-reduction-keys-2.png)

Koondplaanimise käivitamisel 1. aprillil kantakse koondplaani üle järgmised vajaduse kogused. Nagu näete, vähendati aprilli eelarvekandeid järjest 240 nõudluse koguse võrra, alustades esimesest nimetatud kandest.

| Kuupäev     | Vajalik tükkide arv |
|----------|---------------------------|
| 5. aprill  | 0                         |
| 12. aprill | 0                         |
| 19. aprill | 60                        |
| 26. aprill | 100                       |
| 27. aprill | 240                       |
| 3. mai    | 100                       |
| 10. mai   | 100                       |
| 17. mai   | 100                       |

Oletame nüüd, et maiks imporditi uued tellimused.

Järgmised müügitellimuse read on mais olemas.

| Kuupäev   | Taotletud tükkide arv |
|--------|----------------------------|
| 4. mai  | 80                         |
| 11. mai | 130                        |

[![Aprilli ja mai tellimuste põhjal loodud plaanitud tarne.](media/forecast-reduction-keys-3-small.png)](media/forecast-reduction-keys-3.png)

Koondplaanimise käivitamisel 1. aprillil kantakse koondplaani üle järgmised vajaduse kogused. Nagu näete, vähendati aprilli eelarvekandeid järjest 240 nõudluse koguse võrra, alustades esimesest nimetatud kandest. Siiski, mai prognoosikandeid vähendati aga kokku 210 võrra, alustades esimesest mai nõudluse prognoosi kandest. Kuid, perioodi kogusummad säilitatakse (400 aprillis ja 300 mais).

| Kuupäev     | Vajalik tükkide arv |
|----------|---------------------------|
| 5. aprill  | 0                         |
| 12. aprill | 0                         |
| 19. aprill | 60                        |
| 26. aprill | 100                       |
| 27. aprill | 240                       |
| 3. mai    | 0                         |
| 4. mai    | 80                        |
| 10. mai   | 0                         |
| 11. mai   | 130                       |
| 17. mai   | 90                        |

#### <a name="transactions--dynamic-period"></a>Kanded – dünaamiline periood

Kui valite suvandi **Kanded – dünaamiline periood**, siis vähendatakse eelarvevajadusi dünaamilise perioodi jooksul toimuvate tegelike tellimuste kannete võrra. Dünaamiline periood katab praeguse eelarve kuupäevad ja lõpeb järgmise prognoosi algusega. Sellisel juhul loob koondplaneerimine plaanitud tellimused, et täita prognoositud nõudlust (eelarvevajadusi). Sellegipoolest vähendatakse eelarvevajadusi tegelike tellimuste kannete esitamisel. Tegelikud kanded tarbivad osa eelarvevajadustest.

Selle suvandi kasutamisel ilmneb järgmine käitumine.

- Planeerimise koefitsiendid pole vajalikud või neid ei kasutata. 
- Prognoosi täielikul vähendamisel muutub praeguse prognoosi eelarvevajaduseks 0 (null).
- Kui tulevasi prognoose pole, vähendatakse eelarvevajadusi viimati sisestatud prognoosist.
- Prognoosi vähenduse arvutamisse kaasatakse ajapiirid.
- Prognoosi vähenduse arvutamisse kaasatakse positiivne päevade arv.
- Kui tellimuse tegelikud kanded ületavad eelarvevajadusi, ei edastata järelejäänud kandeid järgmisse prognoosiperioodi.

##### <a name="example-1-transactions--dynamic-period"></a>Näide 1: valik Kanded – dünaamiline periood

Selles lihtsas näites demonstreeritakse, kuidas toimib meetod **Kanded – dünaamiline periood**.

Selle näite jaoks kaasate koondplaani järgmised nõudluse prognoosid.

| Kuupäev       | Nõudluse prognoos |
|------------|-----------------|
| 1. jaanuar  | 1000           |
| 1. veebruar | 1000             |

Samuti looge järgmised müügitellimused.

| Kuupäev        | Müügitellimuse kogus |
|-------------|----------------------|
| 15. jaanuar  | 200                  |
| 15. veebruar | 400                  |

Sellisel juhul luuakse järgmised plaanitud tellimused.

| Nõudluse prognoosi kuupäev | Kogus | Selgitus                           |
|--------------------- |----------|---------------------------------------|
| 1. jaanuar            | 800      | Eelarvevajadused (= 1000 – 200) |
| 15. jaanuar           | 200      | Müügitellimuste vajadus             |
| 1. veebruar           | 600      | Eelarvevajadused (= 1000 – 400) |
| 15. veebruar          | 400      | Müügitellimuste vajadus             |

##### <a name="example-2-transactions--dynamic-period"></a>Näide 2: valik Kanded – dünaamiline periood

Enamasti on süsteemid seadistatud nii, et kanded vähendavad nõudluse prognoosi teatud prognoosiperioodis (nädalad, kuud jne). Need perioodid on määratletud planeerimise koefitsiendis. Siiski võib ka kahe nõudluse perioodi rea vaheline aeg *tähendada* perioodi.

Selle näite jaoks looge nõudluse prognoos järgmiste kuupäevade ja koguste kohta.

| Kuupäev       | Nõudluse prognoos |
|------------|-----------------|
| 1. jaanuar  | 1000           |
| 5. jaanuar  | 500             |
| 12. jaanuar | 1000           |

Pange tähele, et selles prognoosis pole eelarve kuupäevade vahel kindlat perioodi. Esimese ja teise kuupäeva vahel on neljapäevane vahemik ning teise ja kolmanda kuupäeva vahel on seitsmepäevane vahemik. Need vahemikud on dünaamilised perioodid.

Samuti looge järgmised müügitellimuste read.

| Kuupäev                             | Müügitellimuse kogus |
|----------------------------------|----------------------|
| Eelmise aasta 15. detsember | 500                  |
| 3. jaanuar                        | 100                  |
| 10. jaanuar                       | 200                  |

Sellisel juhul vähendatakse prognoosi järgmiselt.

- Kuna esimene müügitellimus ei jää ühegi perioodi piiresse, ei vähenda see ühtki prognoosi.
- Kuna teine müügitellimus jääb 1. jaanuari ja 5. jaanuari vahele, vähendab see prognoosi 1. jaanuariks 100 võrra.
- Kuna kolmas müügitellimus jääb 5. jaanuari ja 12. jaanuari vahele, vähendab see prognoosi 5. jaanuariks 200 võrra.

Seega luuakse järgmised plaanitud tellimused.

| Nõudluse prognoosi kuupäev             | Kogus | Selgitus                                                         |
|----------------------------------|----------|---------------------------------------------------------------------|
| Eelmise aasta 15. detsember | 500      | Müügitellimuste vajadus                                            |
| 1. jaanuar                        | 900      | Eelarvevajaduse periood 1. jaanuarist kuni 5. jaanuarini (= 1000 – 100) |
| 3. jaanuar                        | 100      | Müügitellimuste vajadus                                            |
| 5. jaanuar                        | 300      | Eelarvevajaduse periood 5. jaanuarist kuni 10. jaanuarini (= 500 – 200)  |
| 12. jaanuar                       | 1000    | Eelarvevajaduse periood 12. jaanuarist lõpuni                      |

### <a name="create-and-set-up-a-forecast-reduction-key"></a><a name="create-reduction-key"></a>Eelarve planeerimise koefitsiendi loomine ja seadistamine

Meetodites **Kanded – planeerimise koefitsient** ja **Protsent – planeerimise koefitsient** kasutatakse eelarvevajaduste vähendamiseks eelarve planeerimise koefitsienti. Järgige neid samme, et luua ja seadistada planeerimise koefitsienti.

1. Valige **Koondplaneerimine \> Seadistus \> Laovarud \> Planeerimise koefitsiendid**.
2. Valige uue planeerimise koefitsiendi loomiseks **Uus**.
3. Sisestage väljale **Planeerimise koefitsient** eelarve planeerimise koefitsiendi jaoks kordumatu identifikaator. Seejärel sisestage nimi väljal **Nimi**. 
4. Määratlege iga perioodi jaoks perioodid ja planeerimise koefitsiendi protsent.

    - Väli **Jõustumiskuupäev** tähistab kuupäeva, millal perioodide loomine algab. Kui suvandi **Kasuta jõustumiskuupäeva** olekuks on määratud **Jah**, siis algavad perioodid jõustumiskuupäeval. Kui suvandi olek on **Ei**, siis algavad perioodid kuupäeval, mil koondplaneerimine käitatakse.
    - Määrake perioodid, mille jooksul eelarvevähendus peaks toimuma.
    - Määrake konkreetse perioodi jaoks protsendid, mille võrra eelarvevajadusi vähendama peaks. Vajaduste vähendamiseks saate sisestada positiivsed väärtused, suurendamiseks negatiivsed väärtused.

### <a name="use-a-reduction-key"></a><a name="use-reduction-key"></a>Planeerimise koefitsiendi kasutamine

Planeerimise koefitsient peab olema määratud kauba laovarude grupile. Järgige neid samme, et määrata kauba laovarude grupile planeerimise koefitsient.

1. Valige **Koondplaneerimine \> Seadistus \> Laovarud \> Laovarude grupid**.
2. Valige kiirkaardi **Muud** väljal **Planeerimise koefitsient** planeerimise koefitsient, mida laovarude grupile määrata. Planeerimise koefitsient rakendub seejärel kõikidele kaupadele, mis sellesse laovarude gruppi kuuluvad.
3. Selleks, et kasutada planeerimise koefitsienti koondplaneerimise ajal prognoosi vähendamise arvutamiseks, peate määratlema selle sätte koondplaani eelarveplaani seadistuses. Minge ühele järgmistest asukohtadest.

    - **Koondplaneerimine \> Seadistus \> Plaanid \> Eelarveplaanid**
    - **Koondplaneerimine \> Seadistus \> Plaanid \> Koondplaanid**

4. Valige lehe **Eelarveplaanid** või **Koondplaanid** kiirkaardi **Üldine** väljal **Eelarvevajaduste vähendamiseks kasutatav meetod** suvand **Protsent – planeerimise koefitsient** või **Kanded – planeerimise koefitsient**.

### <a name="reduce-a-forecast-by-transactions"></a>Eelarve vähendamine kannetega

Kui valite eelarvevajaduste vähendamise meetodiks **Kanded – planeerimise koefitsient** või **Kanded – dünaamiline periood**, siis saate määrata, millised kanded eelarvet vähendavad. Valige lehe **Laovarude grupid** kiirkaardi **Muud** väljal **Prognoosi vähendamisalus:** suvand **Kõik kanded**, kui prognoosi peaks vähendama kõik kanded, või **Tellimused**, kui prognoosi peaks vähendama ainult müügitellimused.

## <a name="forecast-models-and-submodels"></a>Prognoosimudelid ja alammudelid

Selles jaotises kirjeldatakse, kuidas luua prognoosimudeleid ja kuidas alammudelite seadistamisega mitut prognoosimudelit kombineerida.

*Prognoosimudel* nimetab ja määratleb kindla prognoosi. Pärast prognoosimudeli loomist saate sellele lisada prognoosiridu. Mitme kauba prognoosiridade lisamiseks kasutage lehte **Nõudluse prognoosi read**. Konkreetse valitud kauba prognoosiridade lisamiseks kasutage lehte **Väljastatud tooted**.

Prognoosimudel võib sisaldada muudest prognoosimudelitest pärit prognoose. Selle tulemuse saavutamiseks lisate ülemtaseme prognoosimudeli *alammudeliteks* muid prognoosimudeleid. Enne kui saate selle lisada ülemtaseme prognoosimudeli alammudelina, peate looma iga asjakohase mudeli.

Tulemuseks saadav struktuur annab teile prognooside juhtimiseks võimsa viisi, sest see võimaldab teil kombineerida (koondada) mitmete üksikute prognooside sisendeid. Seetõttu on planeerimise vaatepunktist prognoose lihtne simulatsioonide jaoks kombineerida. Näiteks võite seadistada simulatsiooni, mis põhineb regulaarse prognoosi kombinatsioonil kevadkampaania prognoosiga.

### <a name="submodel-levels"></a>Alammudeli tasemed

Ülemtaseme prognoosimudelile lisatavate alammudelite arv ei ole piiratud. Struktuur võib siiski olla ainult üks tase sügav. See tähendab, et teise prognoosimudeli alammudeliks oleval prognoosimudelil ei saa olla oma alammudeleid. Kui lisate prognoosimudelile alammudeleid, kontrollib süsteem, kas see prognoosimudel on juba mõne muu prognoosimudeli alammudel.

Kui koondplaneerimisel ilmneb alammudel, millel on oma alammudelid, saate tõrketeate.

#### <a name="submodel-levels-example"></a>Alammudeli tasemete näide

Prognoosimudelil A on alammudelina prognoosimudel B. Seetõttu ei saa prognoosimudelil B olla oma alammudeleid. Kui proovite lisada prognoosimudelile B alammudeli, kuvatakse järgmine tõrketeade: "Prognoosimudel B on mudeli A alammudel."

### <a name="aggregating-forecasts-across-forecast-models"></a>Prognooside koondamine prognoosimudelite üleselt

Samal päeval toimuvad prognoosiread koondatakse nende prognoosimudeli ja selle alammudelite alusel.

#### <a name="aggregation-example"></a>Koondamise näide

Prognoosimudelil A on alammudeliteks prognoosimudelid B ja C.

- Prognoosimudel A sisaldab nõudluse prognoosi 2 tk kohta 15. juunil.
- Prognoosimudel B sisaldab nõudluse prognoosi 3 tk kohta 15. juunil.
- Prognoosimudel C sisaldab nõudluse prognoosi 4 tk kohta 15. juunil.

Tulemuseks olev nõudluse prognoos on üks nõudlus 9 tk (2 + 3 + 4) järele 15. juunil.

> [!NOTE]
> Iga alammudel kasutab oma parameetreid, mitte ülemtaseme prognoosimudeli parameetreid.

### <a name="create-a-forecast-model"></a>Prognoosimudeli loomine

Prognoosimudeli loomiseks tehke järgmist.

1. Avage **Koondplaneerimine \> Seadistus \> Nõudluse prognoos \> Prognoosimudelid**.
1. Valige toimingupaanil nupp **Uus**.
1. Seadke uue prognoosimudeli jaoks järgmised väljad:

    - **Mudel** – sisestage mudeli kordumatu identifikaator.
    - **Nimi** – sisestage mudeli kirjeldav nimi.
    - **Peatatud** – tavaliselt tuleks selle suvandi väärtuseks seada *Ei*. Seadke selle väärtuseks *Jah* ainult juhul, kui soovite vältida kõigi sellele mudelile määratud prognoosiridade redigeerimist.

    > [!NOTE]
    > Väli **Kaasa likviidsuse planeerimisse** ja kiirkaardi **Projekt** väljad ei ole seotud koondplaneerimisega. Seetõttu võite neid selles kontekstis eirata. Neid tuleb arvestada ainult siis, kui töötate mooduli **Projektihaldus ja -arvestus** prognoosidega.

### <a name="assign-submodels-to-a-forecast-model"></a>Alammudelite määramine prognoosimudelile

Alammudelite määramiseks prognoosimudelile järgige neid samme.

1. Valige **Laohaldus \> Seadistus \> Prognoos \> Prognoosimudelid**.
1. Valige loendipaanil prognoosimudel, mille jaoks soovite alammudeli seadistada.
1. Valige kiirkaardil **Alammudel** käsk **Lisa**, et lisada uus rida tabelisse.
1. Määrake uuel real järgmised väljad.

    - **Alammudel** – valige alammudelina lisamiseks prognoosimudel. See prognoosimudel peab juba olemas olema ja sellel ei tohi olla oma alammudeleid.
    - **Nimi** – sisestage alammudeli kirjeldav nimi. Näiteks võib see nimi näidata alammudeli seost ülemtaseme prognoosimudeliga.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

