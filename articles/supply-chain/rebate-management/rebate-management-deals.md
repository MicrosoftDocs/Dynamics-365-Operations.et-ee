---
title: Tagasimaksehalduse tehingud
description: Selles teemas kirjeldatakse, kuidas luua tagasimaksehalduse tehinguid. Tehinguid kasutatakse tagasimaksete ja autoritasude arvutamise erinevate meetodite ja aluste kontrollimiseks. Need sisaldavad reegleid kaasamiseks ja väljajätmiseks.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 76cdbf21cfbc0db7b363d0fbf60a1ecd0046efc1
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689659"
---
# <a name="rebate-management-deals"></a>Tagasimaksehalduse tehingud

[!include [banner](../includes/banner.md)]

Tagasimakse tehinguid kasutatakse tagasimaksete ja autoritasude arvutamise erinevate meetodite ja aluste kontrollimiseks. Need sisaldavad reegleid kaasamiseks ja väljajätmiseks. Tagasimaksete haldust on kolme tüüpi: kliendi tagasimaksed, kliendi autoritasud ja hankija tagasimaksed. Kõigi kolme tüübi puhul kasutatakse sarnaseid sätteid. See teema toob välja nende erinevused.

## <a name="create-a-deal"></a>Tehingu loomine

1. Minge **Tagasimaksehaldus \> Tagasimaksete haldusse tehingud \> Kõik tagasimaksehalduse tehingud**. Loendilehel **Kõik tagasimaksehalduse tehingud** saate luua ja töötada kõigi kolme tüüpi tehingutega.

    Alternatiivselt järgige ühte järgnevatest toimingutest. Igal juhul annab kuvav loendileht kõik samad sätted nagu loendilehe **Kõik tagasimaksehalduse tehingud** puhul, kuid on filtreeritud kuvama ainult ühe tüübiga tehinguid.

    - Minge **Tagasimaksehalduse \> Tagasimaksehalduse tehingud \> Kliendi tagasimakse tehingud**, et luua ainult kliendi tagasimakse tehinguid.
    - Minge **Tagasimaksehalduse \> Tagasimaksehalduse tehingud \> Kliendi litsentsitasud**, et luua ainult kliendi litsentsitasusid.
    - Minge **Tagasimaksehalduse \> Tagasimaksehalduse tehingud \> Müüja tagasimakse tehingud**, et luua ainult müüja tagasimakse tehinguid.

1. Valige toimingupaanil nupp **Uus**.
1. Dialoogiboksis **Uue tehingu loomine** määrake järgmised väljad.

    - **Tagasimaksehalduse tehing** – kui olete tagasimaksete jaoks [numbriseeria seadistanud](rebate-management-parameters.md), seatakse sellele väljale automaatselt kordumatu süsteemi loodud ID. Muuljuhul sisestage ainulaadne ID.
    - **Kirjeldus** – sisestage tehingu kirjeldus.
    - **Moodul** – valige partneri tüüp, kellele tehingut rakendatakse (*Klient* või *Müüja*). Sõltuvalt lehest, kust alustasite, võidakse see väli automaatselt määrata vastavalt valitud tehingu tüübile. Sel juhul on väli kirjutuskaitstud.
    - **Tüüp** – valige tehingu tüüp (*Tagasimakse* või *Litsents*). Sõltuvalt lehest, kust alustasite, võidakse see väli automaatselt määrata vastavalt valitud tehingu tüübile. Sel juhul on väli kirjutuskaitstud.
    - **Vastavusseviimise aluseks** – valige, kuidas tehingut arvutada ja vastavusse viia.

        - *Tehing* – tehingus kõigi tagasimaksete ja mahaarvamiste puhul tuleb töödelda ühte tagasimakset.
        - *Rida* – tagasimakseid tuleb töödelda tehingu iga rea puhul.

    - **Sisestusprofiil** – valige [sisestusprofiil](rebate-management-posting.md), mida kasutada kannete puhul, millele tehing rakendub. See väli on saadaval ainult juhul, kui välja **Vastavusseviimine** väärtuseks on valitud *Tehing*. Kui see on seatud väärtusele *Rida*, määrate te profiili hiljem igale reale, mille tehingule lisate.
    - **Garantii sisestusprofiil** – valige [sisestusprofiil](rebate-management-posting.md), mida kasutada garantii kannete puhul. Sisestusprofiilid on garantiitehingute jaoks vajalik ainult juhul, kui garantii kehtib autoritasu kohta. Vastasel juhul, kui sisestusprofiil ei ole kohustuslik, kuvatakse garantiide sisestamisel tõrketeade, kui sisestusprofiil ei ole määratud. See väli on saadaval ainult juhul, kui välja **Tüüp** väärtuseks on valitud *Litsents*. 
    - **Tagasimakse väljund** – valige, kuidas tagasimakse või autoritasu tasutakse.

        - *Finants* – looge vabas vormis krediitmärge või võlgnetav võlateade, et rahasid saaks hiljem maksta või kätte saada. Arvestage, et sätteid **saab** kasutada tagasimaksetega, kui see suvand on valitud. See valik on ainus saadaval olev valik, kui välja **Tüüp** väärtuseks on valitud *Litsents*.
        - *Üksus* – looge kaupade müügitellimus vastavalt tehingu seadistusele. Sellele müügitellimusele määratakse igale üksusele hinnaks 0 (null). Arvestage, et sätteid **ei saa** kasutada tagasimaksetega, kui see suvand on valitud.

    - **Tagasimakse valuuta** – valige valuuta, mida kasutada tagasimakse, mahaarvamise või autoritasude eest maksmiseks.
    - **Dokumendi märkused** – sisestage tehingu märkused, nagu on nõutud.
    - **Kumulatiivne garantii** – selle valiku saate seada väärtusele *Jah* ainult siis, kui välja **Tüüp** väärtuseks on määratud *Litsents*. See valik mõjutab garanteeritud mahaarvamiste arvutamist. Siin on näide.

        - Tehingu tagatiseks on väärtuse müümine, mille tulemusel makstakse kvartalis 10 000 dollarit.
        - Kaupu müüv organisatsioon müüb väärtuse, mis põhjustab 1. kvartalis 12 000 dollari suuruse mahaarvamise makse. Tulemuseks on $12000, mis makstakse, miinus $10000 garantii.
        - Kui **kumulatiivse garantii** suvand on seatud valikule *Jah*, $2000 1. kvartalis makstud autoritasude täiendav summa rakendub 2. kvartalile. Seetõttu on kliendile tagatud $8000 (garantii $10000 miinus $2000 lisamakse).
        - 2. kvartalis registreerite müügi, mis tagab $5000 autoritasu.
        - Süsteem tuvastab $3000 makse (garantii $8000 miinus makstud $5000 autoritasu).
        - Kui valiku **Kumulatiivne garantii** väärtuseks on seatud *Ei*, on kogu $10000 tagatud igas kvartalis. See garantii vastab soovitatud maksele $5000 2. kvartalis (10 000 dollari suurune garantii, millest on lahutatud 5000 dollarit makstud autoritasud).

1. Valige tehingu loomiseks ja dialoogiboksi sulgemiseks **OK**.

See protseduur loob uue tehingu päise taseme. Edasi lisate tehingule ridu.

## <a name="add-lines-to-a-deal"></a>Lisa read tehingule

Kui olete loonud tehingu eelmises jaotises kirjeldatud viisil, saate selle avada loendi leheküljelt. Seejärel saate lisada ridu klientide või müüjate tuvastamiseks, üksused, ajaraamid, tehingu alus ja arvutusmeetodid. Tehingul võib olla üks või mitu rida. Kui tehingul on mitu rida, on need üldiselt sama tüüpi või nendega on seotud samad parameetrid. Kuni tehingule ridu lisate, ei tee tehing tegelikult midagi.

1. Avage sobiv tagasimakse tehingute loendileht, nagu on kirjeldatud eelmises jaotises.
1. Leidke ja avage tehing, millega soovite koostööd teha.
1. Valige kiirkaardil **Tagasimakse haldus** üks järgmistest nuppudest, et lisada tabelile tehingu rida.

    - **Lisa rida** – lisage uus tühi tehingu rida.
    - **Kopeeri rida** – kui olemasolev tehingu rida sarnaneb tehingu reaga, mida soovite lisada, saate valida selle nupu, et kopeerida koopia sellest. Uus tehingu rida hõlmab kõiki seotud tagasimakse halduse üksikasjade sätteid. Seejärel saate sätteid redigeerida. Näiteks värskendate tavaliselt üksuse seost ja tagasimakse protsenti.

1. Määrake uuel tehingu real järgmised väljad.

    - **Tagasimaksehalduse number** – kui olete tagasimaksete halduse numbrite jaoks [numbriseeria seadistanud](rebate-management-parameters.md), seatakse sellele väljale automaatselt kordumatu süsteemi loodud ID. Muuljuhul sisestage ainulaadne ID.
    - **Tüüp** – tehingu tüüp, mille suhtes rida kehtib (*Tagasimakse* või *Litsents*). Väärtus kopeeritakse päisest ja seda ei saa muuta.
    - **Kirjeldus** – sisestage tehingu rea kirjeldus.
    - **Ettevõte** – valige ettevõte (juriidiline isik), mille suhtes tehingu rida kehtib. Töötlemise ajal saavad kasutajad töödelda ainult tehingu ridu, mis on määratud ettevõttele, mida nad praegu kasutavad. Loendileht **Kliendi tagasimaksete tehingud** pakub mitme ettevõttega vaadet, mis põhineb kasutaja turvalisel juurdepääsul. Kuid tagasimakseid saate redigeerida ja töödelda ainult ettevõttele, mida praegu kasutate.
    - **Konto kood** – valige klientide või müüjate ulatus, mille suhtes tehingurida kehtib:

        - *Tabel* – tehingu rida kehtib konkreetse kliendi või müüja kohta.
        - *Grupp* – tehingu rida kehtib kliendi- või müüjate grupile. Komponendigruppide seadistamise kohta vt lisateavet teemast .[Tagasimaksehalduse grupid](rebate-management-groups.md).
        - *Kõik* – tehingu rida kehtib kõikidele klientidele või müüjatele.

    - **Konto suhe** – kui valisite väljal *Konto kood* suvandi **Tabel**, siis valige klient või müüja, kellele tehing rakendub. Valiku *Grupp* korral valige kliendi- või müüja grupp. See väli ei ole saadaval, kui valisite *Kõik*.
    - **Üksuse kood** – valige üksuste ulatus, mille suhtes tehingurida kehtib.

        - *Tabel* – tehingu rida kehtib konkreetse üksuse kohta.
        - *Grupp* – tehingu rida kehtib üksuste grupi kohta. Komponendigruppide seadistamise kohta vt lisateavet teemast .[Tagasimaksehalduse grupid](rebate-management-groups.md).
        - *Kõik* – tehingu ridarakendub kõikidele üksustele.

    - **Üksuse suhe** – kui valisite väljal *Üksuse kood* suvandi **Tabel**, siis valige üksus, millele tehingu rida rakendub. Valiku *Grupp* korral valige kaubagrupp. See väli ei ole saadaval, kui valisite *Kõik*.
    - **Ühiku tüüp** – valige tehingureale rakendatava ühiku tüüp ( *laoühik* või *tegeliku kaalu ühik*). Pange tähele, et see väli võib olla vanemate kirjete puhul tühi. Sel juhul eeldatakse *varude ühiku* väärtust.
    - **(Varude halduse parameetrid)** – määrake tehingu rea ülejäänud väljadel varude halduse parameetrite väärtused, mida kasutatakse tehingusse kaasatud kaupade määramiseks (nt kauba suurus, värv, stiil, piirkond ja ladu). Dimensioonide lisamiseks või eemaldamiseks valige tegevuspaanil **Kuva dimensioonid**.

1. Valige toimingupaanil nupp **Salvesta**.
1. Kui soovite veelgi piirata kaupade komplekti, millele tehingu rida rakendub, valige rida ja seejärel valige kiirkaardil **Tagasimakse haldus** **Filter**, et avada standardse **Päringu** dialoogiboks.
1. Iga lisatava tehingu rea puhul seadistage kalkulatsiooni üksikasjad ja muud üksikasjad kiirkaardil **Tagasimaksehalduse üksikasjad**, nagu on kirjeldatud järgmises jaotises.

## <a name="add-rebate-management-details-to-a-deal-line"></a>Tagasimaksehalduse üksikasjade lisamine tehingu reale

Iga tehingu rea jaoks peate häälestama üksikasjad kiirkaardil **Tagasimaksehalduse üksikasjad**. Esiteks valige tehingu rida kiirkaardil **Tagasimaksehaldus**. Seejärel määrake selle tehingu rea jaoks väärtused, kasutades kiirkaardi **Tagasimaksehalduse üksikasjad** erinevaid vahekaarte. Järgmised alamjaotised kirjeldavad, kuidas igat vahekaarti kasutada.

### <a name="settings-on-the-general-tab"></a>Vahekaardi Üldine sätted

Kiirkaardi **Tagasimaksehalduse üksikasjad** vahekaart **Üldine** võimaldab seadistada kalkulatsiooni meetodi ja valitud tehingurea aluse. See seadistus kontrollib, kas on vaja minimaalset ostu, tehingureaga seotud sisestusprofiile ja arvutuse üksikasju. Järgmises tabelis on kirjeldatud saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Arvutamismeetod | Valige meetod, mida kasutada, kui valitud tehingu rida on ühendatud teiste tehingu ridadega (*Etapiline*, *Kumulatiivne*, *Ümardatud* või *Kokku*). Selle välja väärtus võib dramaatiliselt mõjutada tagasimaksete arvutuste tulemusi. Iga meetodi täieliku kirjelduse ja näidete kohta, mis näitavad, kuidas see tagasimakse kalkulatsiooni mõjutab, vaadake selles teemas allpool [tehingu ridade kalkulatsiooni meetodid](#calc-methods). |
| Alus | Valige, kas tagasimakset rakendatakse koguse (st ostetud või müüdud ühikute koguarvu) või väärtuse (st ostetud või müüdud kaupade koguhinna) alusel. |
| Kande tüüp | <p>Valige kalkulatsiooni toimumisprotsess.</p><ul><li>*Tellimus* – kasutage kalkulatsiooni alusena tellitud kogust või väärtust.</li><li>*Edastatud* – kasutage kalkulatsiooni alusena edastatud kogust või väärtust.</li><li>*Arve* – kasutage kalkulatsiooni alusena arvega edastatud kogust või väärtust.</li></ul> |
| Ühik | Kui valisite väljal *Alus* **Koguse**, valige ühik, mille jaoks kogus tuleb määrata. |
| Vähim summa | Sisestage miinimumsumma, mis tuleb perioodi kohta maksta. Negatiivsete tagasimaksete lubamiseks võite sisestada negatiivse väärtuse, kui kreeditarved ületavad perioodi müüki. |
| Tagasimakse vähendamise põhimõte | Valige [tagasimakse vähendamise põhimõte](rebate-reduction-principle.md), mis kehtib tehingu reale. |
| Variandi number | Kui tehingurida kehtib üksuse jaoks, millel on variante, valige variant, millega tehingurida kehtib. |
| Müüja tagasimakse alus | <p>See väli kuvatakse ainult müüja tagasimaksete puhul (st tehinguid, kus väli **Moodul** on määratud olekusse *Müüja*). Valige müüja tagasimakse alus.</p><ul><li>*Ostutellimus* – tagasimakse, mille müüja saab, põhineb ostutellimuse kogusel või väärtusel.</li><li>*Müügitellimus* – müüja saab tagasimakse alles pärast kaupade müümist. Tagasimakse põhineb müügitellimuse kogusel või väärtusel.</li></ul> |
| Hinna alus | <p>See väli kuvatakse ainult müüja tagasimaksete puhul (tehingud, kus väli **Moodul** on määratud olekusse *Müüja*). Kui valisite väljal *Hankija tagasimakse alus* **müügitellimuse**, valige rakendatav hinna alus:</p><ul><li><p>*FIFO* – tagasimakse arvutamiseks tuleb käivitada **FIFO ostuhinna arvutamise** perioodiline ülesanne. (Ülesande käivitamiseks minge **Tagasimaksete haldus \> Perioodilised ülesanded \> FIFO ostuhinna arvutamine**.) FiFO-reeglit kasutatakse müüdud laoväärtuse arvutamiseks. Seda väärtust kasutatakse seejärel müüja tagasimaksete arvutamiseks. Siin on näide.</p><ul><li>**Müüdud laoseis** 1000 ühikut iga $3.00 = $3000</li><li>**Praegune ostuhind FIFO alusel:** $2.00</li><li>**Töö kalkulatsioon:** *müüdud ühikud* × *praegune ostuhind* = 1000 × $2.00 = $2000</li></ul></li><li><p>*Viimane ostuhind* – viimase ostukande väärtust kasutatakse müüja tagasimaksete arvutamiseks. Siin on näide.</p><ul><li>**Müüdud laoseis** 1000 ühikut iga $3.00 = $3000</li><li>**Viimane ostuhind:** $2.00</li><li>**Töö kalkulatsioon:** *müüdud ühikud* × *viimane ostuhind* = 1000 × $2.00 = $2000</li></ul></li><li><p>*Keskmine ostuhind* – müüja tagasimaksete arvutamiseks kasutatakse möödunud *X* kuu kaalutud keskmist väärtust. Kui valite selle suvandi, peate sisestama kuude arvu väljale **Kuude arv** (mis on saadaval ainult siis, kui välja **Hinna alus** väärtuseks on seatud *Keskmine ostuhind*). Siin on näide.</p><ul><li>**Müüdud laoseis** 1000 ühikut iga $3.00 = $3000</li><li>**Keskmine ostuhind:** $2.00</li><li>**Töö kalkulatsioon:** *müüdud ühikud* × *keskmine ostuhind* = 1000 × $2.00 = $2000</li></ul></li><li><p>*Müügihind* – müügihinda kasutatakse müüja tagasimaksete arvutamiseks. Siin on näide.</p><ul><li>**Müüdud laoseis** 1000 ühikut iga $3.00 = $3000</li><li>**Keskmine ostuhind:** $2.00</li><li>**Töö kalkulatsioon:** *müüdud ühikud* × *müügihind* = 1,000 × $3.00 = $3,000</li></ul></li></ul> |
| Kuude arv | See väli kuvatakse ainult müüja tagasimaksete puhul (tehingud, kus väli **Moodul** on määratud olekusse *Müüja*). Kui valisite väljal *Hinna alus* väärtuseks **Keskmine ostuhind**, sisestage kasutatavate kuude arv. |
| Sisestusreeglid | Valige [sisestusprofiil](rebate-management-posting.md), mis kehtib valitud tehingu reale. Seda profiili kasutatakse ainult siis, kui tehingu päise välja **Vastavusseviimine** on seatud väärtusele *Rida*. Kui välja **Vastavusseviimine** väärtus on *Seotud*, kasutatakse alati tehingu päises seadistatud sisestusprofiili. Kui tehingureal pole sisestusprofiili määratud, kasutatakse tehingu päisel määratud sisestusprofiili. |
| Garantii sisestusprofiil | See väli töötab nagu väli **Sisestusprofiil**, kuid see rakendub ainult litsentsitasudele. |
| Makse tüüp | Tehingu jaoks valitud sisestusprofiili maksetüüp. |
| Käibemaks (k.a) | Valige, kas kanne on maksustatav. Maksustatavus on oluline ainult juhul, kui välja **Alus** väärtuseks on seatud *Väärtus*. Arve summat kasutatakse maksustatud summana. Kui tagasimakse arvutamine põhineb protsendil, korrutab süsteem tagasimakse protsendi maksustatava summaga. Arvestage, et arvutamisel kasutatakse tehingurea käibemaksuväärtust. |
| Kreeditarvete kaasamine | <p>Seadke selle valiku väärtuseks *Jah*, et kaasata kreeditarved tagasimakse arvutamisse.</p><p>Kui seate valiku väärtuseks *Jah*, muutub mõju sõltuvalt välja **Kande tüüp** väärtusest.</p><ul><li>Kui välja **Kande tüüp** väärtuseks on seatud *Arve*, kasutatakse kreeditarvetes arvutuse tegurit. See konfiguratsioon on tavaline konfiguratsioon.</li><li>Kui välja **Kande tüüp** väärtuseks on seatud *Tellimus*, kasutatakse nii negatiivsete väärtuste kui avatud tagastatud tellimustega müügitellimuste puhul kalkulatsiooni tegurit.</li></ul> |
| Allahindluse summa | Seadistage see valik valikule *Jah*, et arvutamine põhineb kauba või kaupade allahindluse summal, kui tehingurea allahindlused on antud. |
| Ainult makstud arved | Kui arvutuses tuleks arvestada ainult täielikult makstud arveid, määrake selle valikuks *Jah*. (See tähendab, et tagasimakseid ei arvutata osaliselt makstud arvete puhul.) See valik on saadaval ainult siis, kui välja **Kande tüüp** väärtuseks on seatud *Arve*. |
| Vaba vormi kaasamine | Seadke selle valiku väärtuseks *Jah*, et kaasata vabatekstilised arved arvutamisse. Vabas vormis arveid saab kaasata ainult nendega seotud ridade puhul, kus **kaubakoodi** välja väärtuseks on *Kõik*. |
| Arveldussoodustuse kaasamine | Määrake see suvand valikule *Jah*, et vähendada tagasimakset esimese arveldussoodustusega. Eeldatakse, et organisatsioon võtab esimese arveldussoodustuse. Arveldussoodustuse lubamiseks määrake selle valikuks *Ei* (hilisemaks kasutamiseks). |
| Dokumendi märkused | Saate sisestada märkusi, mida tuleks tagasimakse kande tööleheridadel kasutada kandetekstina. |

### <a name="settings-on-the-dates-tab"></a>Sätted vahekaardil Kuupäevad

Kiirkaardi **Tagasimaksehalduse üksikasjad** vahekaardil **Kuupäevad** olevad sätted määratlevad vahekaardil **Üldine** määratud arvutuste sageduse ja ajastuse. Need määravad, kuidas kalkulatsioon töötlemise ajal tehakse.

See vahekaart võimaldab teil määrata arvutamissageduse ja kuupäevade vahemiku, mille puhul valitud tehingurida kehtib. Lisaks saate määrata, kas garantii tuleks sisestada ja millal.

Saate kasutada tööriistariba nuppe, et lisada kuupäeva ridu ruudustikku või neid eemaldada. Kui on olemas mitu kuupäevarida, ei tohi kehtivad kuupäevavahemikud kattuda. Vastasel juhul saate veateate, kui proovite tehingut salvestada.

Järgmises tabelis kirjeldatakse iga kuupäeva rea jaoks saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Alates kuupäevast | Saate sisestada kuupäevarea kehtivuse alguskuupäeva. Kui tehingu päises on määratud kuupäevad "alates" ja "kuni", kasutatakse neid vaikeväärtustena iga uue kuupäevarea puhul. |
| Lõppkuupäev | Saate sisestada kuupäevarea kehtivuse lõpukuupäeva. Kui tehingu päises on määratud kuupäevad "alates" ja "kuni", kasutatakse neid vaikeväärtustena iga uue kuupäevarea puhul. |
| Kohta | Määrake, kui tihti tehingu rida arvutatakse. Sisestage siia täisarv ja seejärel valige ühik väljal **Kumuleeritud, kui**. Näiteks iga teise nädala arvutamiseks seadke välja **Mille kohta** väärtuseks *2* ja välja **Kumuleeritud, kui** väärtuseks *Nädalad*. |
| Kumuleeritud, kui | Valige ühik, mis rakendub **Mille kohta** sättele. Valige *Eluiga*, et arvutada tehingu rida kogu eluea jooksul. Valige *Kohandatud periood* pearaamatus määratletud perioodi valimiseks. Sellisel juhul peate määrama ka välja **Perioodi tüüp**. |
| Perioodi tüüp | See väli on saadaval ainult juhul, kui välja **Kumuleeritud kui** väärtuseks on valitud *Kohandatud periood*. Valikuks saadaolevad väärtused tulevad pearaamatus määratletud perioodi tüüpidest. |
| Nädala esimene päev | Saate määrata, kuidas määratakse nädalad perioodi jaoks. See väli on saadaval ainult juhul, kui välja **Kumuleeritud, kui** väärtuseks on valitud *Nädalad*. |
| Nõue, kui | Määrake, kui tihti saab tehingurea tagasimakseid nõuda. Sisestage siia täisarv ja seejärel valige ühik väljal **Nõutud, kui**. |
| Nõude esitaja | Valige ühik, mis rakendub **Nõue** sättele. Valige *Eluiga*, et lubada nõudeid just üks kord tehingurea kogu eluea jooksul. Valige *Kohandatud periood* pearaamatus määratletud perioodi valimiseks. Sellisel juhul peate määrama ka välja **Nõude perioodi tüüp**. |
| Nõude perioodi tüüp | See väli on saadaval ainult juhul, kui välja **Nõude esitaja** väärtuseks on valitud *Kohandatud periood*. Valikuks saadaolevad väärtused tulevad pearaamatus määratletud perioodi tüüpidest. |
| Sisestamise protsess | Märkige see ruut, kui nõude rida tuleb töödelda sisestamise ajal. See valik on saadaval ainult nendega seotud ridade puhul, kus vahekaardi **Üldine** välja **Kande tüüp** väärtuseks on määratud *Tarnitud* või *Arve*. Ettevalmistamise puhul sisestatakse eraldis siis, kui luuakse tarneteatis või arve. |
| Garantii kohta | See väli kehtib ainult litsentsitasudega tehingutele. Määrake, kui tihti tuleks litentsitasu garantiid välja arvutada sätte **Kumuleeritud, kui** perioodi jooksul. Sisestage siia täisarv ja seejärel valige makse aeg väljal **Makstud garantii**. |
| Makstud garantii | <p>See väli kehtib ainult litsentsitasudega tehingutele. Garantii arvutamissageduse määratlemiseks toimib see koos väljaga **Garantii**. Valige üks järgmistest väärtustest.</p><ul><li><p>*Perioodi algus* – garantii makstakse kuupäevareale määratud lepinguperioodi alguses. Täielikku garantiid töödeldakse esimesena. Maksimumsummat ületavad autoritasud sisestatakse autoritasudena. Siin on näide.</p><ul><li>**Garantii miinimum:** $10000 kahe kuu jooksul.</li><li>**1. kuu** $10000 sisestati garantiina ja $0 sisestati autoritasudeks.</li><li>**2. kuu** $2000 sisestati autoritasudeks ja $0 sisestati garantiideks.</li><li>**Töö arvutus:** *järelejäänud garantii* – *sisestatud autoritasud* = $0 – $2000 = -$2000.</li></ul><p>Kuna autoritasu $2000 on nõutud, luuakse selle jaoks tööleht $2000.</p><p>**Märkus:** garantii tuleks arvutada ja sisestada koos esimese perioodi mahaarvamiste eraldistega.</p></li><li><p>*Perioodi lõpp* – garantiid ei maksta enne mahaarvamiste lepingu lõppu, nagu on määratud kuupäevareal. Siin on näide.</p><ul><li>**Garantii miinimum:** $10000 kahe kuu jooksul.</li><li>**1. kuu:** $5000 sisestati autoritasudena ja loodi tööleht.</li><li>**2. kuu:** $7000 sisestati autoritasudena ja loodi tööleht.</li><li>**Tööarvutus:** kuna autoritasud ületavad garantiisumma, siis garantiile sisestatakse $0.</li></ul><p>**Märkus:** garantii tuleks arvutada ja sisestada ainult koos viimase perioodi mahaarvamiste ja tagasimaksete kannetega.</p></li></ul> |
| Garantii miinimum | See väli kehtib ainult litsentsitasudega tehingutele. Sisestage garantii miinimumsumma autoritasule valuutas, mis on määratud tehingu päises. |

### <a name="settings-on-the-lines-tab"></a>Sätted vahekaardil Read

Kiirkaardi **Tagasimaksehalduse üksikasjad** vahekaart **Read** võimaldab määratleda kalkulatsiooni read valitud tehingureale. Iga arvutusrida kehtestab koguse või väärtuse läve ja seotud kompensatsiooni summa või kaubad. Vahekaardi **Üldine** väljal **Alus** määratakse, kas iga kalkulatsioonirida põhineb kogusel või väärtusel.

Saate kasutada tööriistariba nuppe, et lisada kalkulatsiooni ridu ruudustikku või neid eemaldada. Teil võib olla mis tahes arv kalkulatsiooniridu. Kuid kui on olemas mitu kalkulatsioonirida, ei tohi "kuni" ja "alates" kogus või väärtusevahemikud kattuda.

Järgmises tabelis kirjeldatakse iga kalkulatsiooni rea jaoks saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Kogusest/väärtusest | Saate sisestada miinimumkoguse või -väärtuse, mille suhtes kalkulatsioonirida kehtib. |
| Kogusele/väärtusele | Saate sisestada maksimumkoguse või -väärtuse, mille suhtes kalkulatsioonirida kehtib. |
| Tagasimaksehalduse meetod | <p>See väli on saadaval ainult tehingutele, kus päises on välja **Tagasimakse väljund** väärtuseks seatud *Rahaline*. Siin saate valida tagasimakse arvutamiseks kasutatava makseviisi.</p><ul><li>*Fikseeritud* – rea puhul kasutatakse fikseeritud hinnaga summat.</li><li>*Protsent* – kasutatakse protsenti müügisummast.</li><li>*Määr* – kasutatakse fikseeritud hinnaga summat tellimuse kohta.</li></ul><p>**Oluline:** soovitame tungivalt kasutada sama meetodit vahekaardil **Read** iga arvutusrea puhul. Kui on vaja uut meetodit, looge uus tehingu rida. Pidage meeles, et saate kasutada nuppu **Kopeeri rida** kiirkaardil **Tagasimaksehaldus**, et luua olemasolevalt tehingurealt uus tehingurida.</p><p>**Märkus:** kui välja **Tagasimakse väljund** väärtuseks on *Üksus*, on selle välja väärtuseks alati seatud *Fikseeritud*. Lisateavet kaupade täpsustamise kohta vt sellele tabelile järgnevast tekstist. |
| Tagasimaksehalduse kogus | See väli on saadaval ainult tehingutele, kus päises on **Tagasimakse väljund** väärtuseks seatud *Rahaline*. Sisestage tagasimakse arvutamiseks kasutatav summa, mis põhineb tagasimakse halduse meetodil väljal **Tagasimaksehalduse meetod**. |

Nagu eelmises tabelis mainitud, peate määratlema need pakkumised, kus päise välja **Tagasimakse väljund** väärtuseks on seatud *Üksus* need kaubad, mida antakse iga arvutusrea jaoks vahekaardil **Read**. Üksuste määramiseks toimige järgmiselt.

1. Looge vahekaardil **Read** soovitud kalkulatsiooni rida, kui seda pole ja valige see.
1. Kui tehingut pole pärast kalkulatsiooni rea loomist salvestatud, valige tegevuspaanil käsk **Salvesta**.
1. Valige vahekaardil **Read** väärtuseks **Üksused**.
1. Kasutage **kaupade** lehel tegumiriba nuppe, et lisada kaupu ruudustikku või eemaldada kaupu vastavalt vajadusele. Määrake igas reas järgmised väljad.

    - **Üksuse number** – valige pakutava kauba kood.
    - **(Muud dimensioonid)** – kui peate kauba määratlemiseks kasutama rohkem dimensioone (nt kauba konfiguratsioon, suurus, värv, stiil, piirkond või ladu), määrake need. Saadaolevate dimensioonide lisamiseks või eemaldamiseks valige tegevuspaanil **Kuva dimensioonid**.
    - **Kogus** – sisestage kogus, mis antakse pärast valitud kalkulatsioonirea läve täitmist.
    - **Ühik** – valige ühik, mille kohta **kogus** on määratud.
    - **Kordne** – see väli toimib koos väljaga **Kogus**. Näiteks kaubareal seate välja **Kogus** väärtuseks *2* ja väljale **Kordne** väärtuseks *100*. Kui müügitellimuse kogusumma on 150, on kaks kaupa tasuta (kaks ühikut 100 kohta).

### <a name="settings-on-the-inventory-dimensions-tab"></a>Vahekaardi Varude dimensioonid sätted

Kiirkaardi **Tagasimakse halduse üksikasjad** vahekaardil **Inventuuri dimensioonid** kuvatakse kõik toote saadaolevad dimensiooniväärtused, mis on määratud valitud tehingureale. See sisaldab dimensioone, mida ei kuvata kiirkaardil **Tagasimaksehaldus**. Väärtusi saate redigeerida ainult nende dimensioonide puhul, mis kehtivad valitud toote puhul.

Saate lisada kiirkaardi **Tagasimaksehaldus** ruudustikule rohkem dimensioone, valides tegevuspaanil **Kuva dimensioonid**.

## <a name="calculation-methods-for-deal-lines"></a><a name="calc-methods"></a>Tehinguridade kalkulatsioonimeetodid

Iga kord, kui seadistate ühe oma tehingurea üksikasjad, nagu eelmises osas kirjeldatud, peate valima selle rea arvutusmeetodi. See jaotis selgitab iga arvutusmeetodit ja pakub näiteid, kuidas iga meetod arvutab tellimuste ja tehingu ridade kogu tagasimakse. Nendes näidetes on tellimused ja tehinguread identsed. Erinevad ainult arvutusmeetodid.

### <a name="stepped-calculation-method"></a>Astmeline arvutusmeetod

Astmeline arvutusmeetod arvutatakse samm-sammult, kus iga tehingu rida panustab järk-haaval tagasimaksesse, kuni müügikogus või väärtus on saavutatud. Sammud võivad põhineda kas müüdud kaupade kogusel või väärtusel, sõltuvalt välja **Alus** sättest kiirkaardi **Tagasimaksehalduse üksikasjad** vahekaardil **Üldine**.

Näiteks on tehingu rida seadistatud nii, et **arvutusmeetodi** välja väärtuseks on seatud *Astmeline* ja välja **Alus** väärtuseks on seatud *Väärtus*. See sisaldab arvutusridu, mis pakuvad järgmisi tagasimakseid.

- **Rida A:** 10 protsenti kuni $1000
- **Rida B:** 25 protsenti kuni $2500

Kui ostetud või müüdud kaupade väärtus $2000 arvutatakse kauba $350 tagasimaksest järgmiselt.

- **Tagasimakse (A):** *lävi (A)* × *protsent (A)* = $1000 × 10 protsenti = $100
- **Tagasimakse (B):** (*müüdud väärtus* – *lävi (A)*) × *protsent (B)* = ($2000 - $1000) × 25 protsenti = $250
- **Tagasimakse kokku:** *tagasimakse (A)* + *tagasimakse (B)* = $100 + $250 = $350

Kui välja **Alus** väärtuseks on *Väärtus* asemel on seatud *Kogus*, töötab etapiviisiline arvutusmeetod sarnasel viisil. Esimest etappi kasutatakse tuvastatud koguse jaoks, kuni saavutatakse teine ​​etapp. Seejärel kasutatakse teist sammu kogu esimese astme kohal oleva koguse jaoks, kuni saavutatakse kolmas etapp. Protsess jätkub siis läbi kõigi järgnevate etappide.

### <a name="cumulative-calculation-method"></a>Kumulatiivse kalkulatsiooni meetod

Kumulatiivne kalkulatsiooni meetod kasutab tagasimakse arvutamiseks ainult üht kalkulatsioonirida. Kui tehingu rea jaoks on saadaval mitu kalkulatsioonirida, kasutatakse suurimat või kõrgeima koguse arvutamise rida, milleni jõutakse, terve koguse või väärtuse puhul. Nagu teised kalkulatsioonimeetodid, kasutab kumulatiivne meetod kiirkaardi **Tagasimaksete halduse üksikasjad** vahekaardi **Üldine** välja **Alus** sätet, et määrata, kas tagasimaksete arvutamiseks kasutatakse müügikogust või -väärtust.

Näiteks on tehingu rida seadistatud nii, et **arvutusmeetodi** välja väärtuseks on seatud *Kumulatiivne* ja välja **Alus** väärtuseks on seatud *Väärtus*. See sisaldab arvutusridu, mis pakuvad järgmisi tagasimakseid.

- **Rida A:** 10 protsenti kuni $1000
- **Rida B:** 25 protsenti kuni $2500

Kui ostetud või müüdud kaupade väärtus on $2000, kasutab kalkulatsioon ainult rida B. Kauba $500 tagasimakset arvutatakse järgmiselt.

- **Tagasimakse kogusumma:** *müüdud väärtus* × *tagasimakse (B)* = $2000 × 25 protsenti = $500

### <a name="rolling-calculation-method"></a>Jooksev arvutusmeetod

Jooksev arvutusmeetod arvutab tehingu kõik võimalikud arvutusread. Kui kalkulatsiooniridu on mitu ja rohkem kui üks neist on saavutatud, kasutatakse kõiki kalkulatsiooniridu, milleni jõutakse, kuid iga protsendi puhul kehtivad ülemised läved. Nagu teised kalkulatsioonimeetodid, kasutab jooksev meetod kiirkaardi **Tagasimaksete halduse üksikasjad** vahekaardi **Üldine** välja **Alus** sätet, et määrata, kas tagasimaksete arvutamiseks kasutatakse müügikogust või -väärtust.

Näiteks on tehingu rida seadistatud nii, et **arvutusmeetodi** välja väärtuseks on seatud *Jooksev* ja välja **Alus** väärtuseks on seatud *Väärtus*. See sisaldab arvutusridu, mis pakuvad järgmisi tagasimakseid.

- **Rida A:** 10 protsenti kuni $1000
- **Rida B:** 25 protsenti kuni $2500

Kui ostetud või müüdud kaupade väärtus $2,000 arvutatakse kauba $600 tagasimaksest järgmiselt.

- **Tagasimakse (A):** *lävi (A)* × *protsent (A)* = $1000 × 10 protsenti = $100
- **Tagasimakse (B):** *müüdud väärtus* x *protsent (B)* = $2000 × 25 protsenti = $500
- **Tagasimakse kokku:** *tagasimakse (A)* + *tagasimakse (B)* = $100 + $500 = $600

### <a name="total-calculation-method"></a>Täielik kalkulatsioonimeetod

Täielik kalkulatsioonimeetod kasutab tagasimakse arvutamiseks kõiki kalkulatsiooniridu. Ta kasutab kogu saavutatud arvutusrea tagasimakse arvutamiseks üldkogust ja iga arvutusrida rakendab oma protsendi kogu summa ulatuses. Nagu teised kalkulatsioonimeetodid, kasutab täielik meetod kiirkaardi **Tagasimaksete halduse üksikasjad** vahekaardi **Üldine** välja **Alus** sätet, et määrata, kas tagasimaksete arvutamiseks kasutatakse müügikogust või -väärtust.

Näiteks on tehingu rida seadistatud nii, et **arvutusmeetodi** välja väärtuseks on seatud *Täielik* ja välja **Alus** väärtuseks on seatud *Väärtus*. See sisaldab arvutusridu, mis pakuvad järgmisi tagasimakseid.

- **Rida A:** 10 protsenti kuni $1000
- **Rida B:** 25 protsenti kuni $2500

Kui ostetud või müüdud kaupade väärtus $2,000 arvutatakse kauba $700 tagasimaksest järgmiselt.

- **Tagasimakse (A):** *müüdud väärtus* x *protsent (A)* = $2,000 × 10 protsenti = $200
- **Tagasimakse (B):** *müüdud väärtus* x *protsent (B)* = $2000 × 25 protsenti = $500
- **Tagasimakse kokku:** *tagasimakse (A)* + *tagasimakse (B)* = $200 + $500 = $700
