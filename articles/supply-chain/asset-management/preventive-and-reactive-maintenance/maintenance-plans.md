---
title: Hoolduskavad
description: Selles teemas tutvustatakse hoolduskavasid varahalduses.
author: johanhoffmann
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectType, EntAssetCounterType, EntAssetWorkOrderLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 143b9337dc9ca530383575e0f9bb16e4313ce96b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839603"
---
# <a name="maintenance-plans"></a>Hoolduskavad

[!include [banner](../../includes/banner.md)]

Hoolduskava määratleb, millal teostatakse vara etteplaneeritud ennetav hooldustöö. Hoolduskavad võivad olla seotud varade, vara tüüpide või töö asukohatüüpidega, kuid kõigepealt loote oma ettevõttes kasutatavad hoolduskavad.

Hoolduskaval võib olla mitmeid hoolduskava ridu. Hooldustöö tüüp ja intervall määratletakse hoolduskava real. On kahte tüüpi hoolduskava ridu.

- Aeg
- Loendur

Hoolduskava "Aeg" tüüpi ridu kasutatakse korduvateks planeeritud hooldusteks, mis toimuvad fikseeritud ajavahemiku tagant. Hoolduskava "Loendur" tüüpi ridu kasutatakse planeeritud hoolduseks või reageerivaks hoolduseks, mida teostatakse vastavalt vara loenduri registreerimisele. Hoolduskava võib sisaldada mitmeid mõlemat tüüpi hoolduskavasid.

>[!NOTE]
>Kui loenduri väärtuseid ei ole vara loenduri tüübi kohta registreeritud, siis jäetakse hoolduskava read välja.

Kõigepealt loote need hoolduskavad, mida vajate oma ennetavate hooldustööde jaoks ja valite iga hoolduskava jaoks vara tüübid, varad, töö asukohatüübid ja töö asukohad. Pärast saate vajadusel lisada hoolduskavasid ka varale või töö asukohale, mida tehakse jaotises **Kõik varad** \> vara valik \> kiirkaart **Vara hoolduskavad** või **Kõik töö asukohad** \> töö asukoha valik \> kiirkaart **Hoolduskavad**.

Kui lisate hoolduskava vara tüüpidele või töö asukohatüüpidele, tähendab see, et kui loote nende vara tüüpide või töö asukohatüüpidega uusi varasid või töö asukohti, lisatakse see vara või töö asukoht automaatselt hoolduskavasse. Hoolduskavaga seotud alguskuupäevaks saab praegune kuupäev, mida võib olla vajalik kohandada.

## <a name="set-up-maintenance-plans"></a>Hoolduskavade seadistamine

Selles jaotises kirjeldatakse hoolduskavade ridade seadistamist ja antakse näiteid nende kasutamise kohta.

1. Avage **Varahaldus \> Seadistus \> Ennetav hooldus \> Hooldusplaanid**.

1. Valige uue järjestuse loomiseks **Uus**.

1. Sisestage ID väljale **Hooldusjärjestus** ja nimi väljale **Nimi**.

1. Sisestage väljale **Planeerimiskuupäev** alguskuupäev, millest alates saab planeerida hoolduskava. Pange tähele, et ajapõhistel hoolduskava ridadel võivad olla teised planeerimiskuupäevad.

1. Valige hoolduskava aktiveerimiseks tumblernupu **Aktiivne** väärtuseks "Jah".

    >[!NOTE]
    >Kui hoolduskava inaktiveerite, ei looda hoolduskavas kavandatud postitusi, kui käivitate hoolduskava ajastamise töö.

1. Väljad **Tolerantsi päevad enne** ja **Tolerantsi päevad pärast** on seotud hoolduskava ridadega, milles on valitud märkeruut **Keela kattuvad hooldustööd** (vaadake etappi 17). Välju "Tolerants" kasutatakse intervalli päevade arvu pikendamiseks, millal mitme hoolduskava kattumisel luuakse kõige mitmekülgsem / suurem töö hoolduskava ajastamise käigus hoolduskava reana, samas kui sagedasemad kattuvad tööd jäetakse hoolduskava ajastamisel välja. Sisestage väljale **Tolerantsi päevad enne** päevade arv, näiteks "2".

1. Kui olete sisestanud väljale **Tolerantsi päevad enne** väärtuse, sisestage ka väljale **Tolerantsi päevad pärast** päevade arv, näiteks "2".

    >[!NOTE]
    >Selles ja eelmises etapis kirjeldatud näide tähendab, et kui mitu hoolduskava rida kattuvad ja ühele või rohkemale reale valitakse **Keela kattuvad hooldustööd**, pikendatakse hoolduskava ridade välja jätmist kokku viie päeva võrra (eeldatud alguskuupäev hoolduskava real *ja* kaks päeva enne *ja* kaks päeva pärast seda kuupäeva).

1. Väljad grupis **Üksikasjad** kiirkaardil **Üksikasjad** näitavad hoolduskavale seadistatud hoolduskava ridade arvu ja hoolduskavaga seotud varade ja töö asukohtade arvu.

1. Uue hoolduskava rea loomiseks valige kiirkaardil **Read** suvand **Lisa aja rida** või **Lisa vara loenduri rida**.

1. Sisestage rea kirjeldus väljale **Töökäsu kirjeldus**. Kirjeldus edastatakse soetud töökäskudele.

1. Valige väljal **Hooldustöö tüüp** see töö tüüp, millega hoolduskava rida seotud on.

1. Valige väljadel **Hooldustöö  tüübi variant** ja **Vahetus** hooldustöö tüübiga seotud variant ja vahetus.

1. Väljadele **Päevi lõpetamiseks** ja **Tunde lõpetamiseks** võite sisestada oodatava lõppkuupäeva päevade ja tundidena. Oodatav lõppkuupäev sisestatakse vastavalt oodatavale alguskuupäevale, mis arvutatakse välja hoolduskava ridade loomisel. Näiteks võite sisestada väljale **Päevi lõpetamiseks** numbri "7" näitamaks, et seotud töö tuleks lõpetada nädala jooksul alates oodatavast alguskuupäevast.

1. Valige väljal **Intervalli tüüp** see intervalli tüüp, mida tuleks kasutada hoolduskava real, näiteks "Korduv..." või "Üks kord...". Intervalli tüüpide ja rea tüüpide vaheliste seosete kirjeldusi vaadake allolevast tabelist [Intervalli tüüpide ülevaade](#interval-types).

1. Väli **Periood** on seotud ainult ajapõhiste reatüüpidega. Valige perioodi tüüp, mis on seotud perioodi sagedusega.

1. Sisestage väljale **Perioodi sagedus** arv, mitu korda tuleks rida ennetavate hooldustööde planeerimisel kasutada. Näide: kui olete loonud rea tüübiga "Loendur" ja teie loenduriks on tootmiskogus, ning kui sisestate sellele väljale arvu "20000", luuakse uued hooldusjärjestuse read ennetava hoolduse ajastamise käigus iga kord, kui on oodata 20 000 või enama üksuse tootmist.

1. Märkeruut **Keela kattuvad hooldustööd** on seotud nii ajapõhiste kui ka loenduripõhiste reatüüpidega. Valige märkeruut, et kustutada hoolduskava kirjed, mis on loodud samal kuupäeval. See on asjakohane näiteks siis, kui olete loonud 1 kuu ülevaatuse rea, 6 kuu ülevaatuse rea ja 1 aasta ülevaatuse rea. 1 aasta ülevaatuse korral soovite ainult selle ülevaatuse teostamist, mitte ülejäänud kahe ülevaatuse, mis sobiksid ka sellesse ajavahemikku. Et seda näidet õigesti seadistada, seadistate 1 aasta ülevaatuse esimeseks reaks, 6 kuu rea teiseks reaks ja 1 kuu rea kolmandaks reaks ning valite 1 kuu ja 6 kuu ridade jaoks märkeruudu **Keela kattuvad hooldustööd**. Nii kindlustate, et kui jõuate 1 aasta märgini, jäetakse välja ühe kuu ja kuue kuu ülevaatused ning hoolduskava rida luuakse ainult 1 aasta ülevaatuse reale.

    >[!NOTE]
    >Selles etapis kirjeldatud näide näitab, et kõige põhjalikum töö, mis sisaldab suurimal arvul ülesandeid ja mida ei tehta eriti tihti, tuleks alati sisestada esimesele reale. Sagedamini teostatavad tööd sisestatakse eraldi ridadena sageduse järjekorras, asetades kõige sagedasemad tööd loendi lõppu.

1. Väli **Loendur** on seotud ainult loenduripõhiste reatüüpidega. Valige real kasutatava loenduri tüüp. Kui loenduri tüüp ei ole seotud vara juures aktiivne, jäetakse see hoolduskava rida välja.

1. Väli **Vara loenduri ajapiir päevades** on seotud ainult loenduripõhiste reatüüpidega. Sisestage arv, mis määratleb, mitu päeva tagasi loenduri registreerimisi pärast hoolduskava ajastamist kontrollitakse. See tähendab, kui kaugele tagasi hoolduskava ridade loomise arvu määratlemiseks andmeid (olemasolevaid loenduri registreerimisi) selle trendi arvutamise põhjana kasutatakse.

    >*Näide:* kui loenduri registreerimisi oodatakse korra kuus, võite sisestada sellele väljale arvu "365", sest hoolduskava ajastamine põhineb alati viimasel 12 kuul ja seega luuakse hoolduskava read põhinedes viimase aasta trendidele. Teisalt, kui sisestate sellele väljale arvu "10", ootate, et loenduri registreerimisi tehakse sagedamini, näiteks igapäevaselt. See tähendab, et kui ajastate hoolduskava, kasutatakse hoolduskava ridade ajastamise põhjana loenduri viimase 10 päeva registreerimisi.

1. Väli **Planeerimiskuupäev** on seotud ainult ajapõhiste reatüüpidega. Kui hoolduskava real on teine planeerimiskuupäev kui kogu hoolduskaval, valige kuupäev rea väljal **Planeerimiskuupäev**.

1. Väljal **Teenindustase** võite valida hoolduskava rea täiendava eraldajana töökäsu teenindustaseme, mida hakatakse kasutama töökäskude teenindustasemena.

1. Valige märkeruut **Automaatloomine**, kui soovite, et töökäsk luuakse hoolduskavade ajastamisel automaatselt vastavalt valitud hoolduskava reale.

1. Kui olete valinud märkeruudu **Automaatloomine**, võite valida väljal **Töökäsu tüüp** olevale automaatsele töökäsule töökäsu tüübi. Kui olete valinud märkeruudu **Automaatloomine** ja ei vali sellel väljal töökäsu tüüpi, kasutatakse töökäsu tüüpi, mis on valitud jaotise **Varahaldus \> Seadistus \> Varahalduse parameetrid \> Töökäsud** link \> väljal **Ennetava töökäsu tüüp**.

1. 12-kuulise perioodi jooksul korduva ajapõhise hoolduskava loomiseks kasutage välju **Hooaja algus** ja **Hooaja lõpp**. *Näide:* roheliste alade hooldamiseks kasutatavad vahendid vajavad igal kevadel eelmääratud ajavahemikul hooldust. Sisestage väljale **Hooaja algus** korratava ajavahemiku alguskuupäev.

1. Sisestage väljale **Hooaja lõpp** korratava ajavahemiku lõppkuupäev.

1. Väljal **Loodav ajavahemik** kuvatakse praegust korratavat ajavahemikku. Kui praegune ajavahemik on möödunud ja alustate uut aastat, värskendatakse selles väljas kuvatavat ajavahemikku, nii et see peegeldab korduva järjestuse järgmist ajavahemikku.

1. Valige kiirkaardil **Varad** need varad, mis peaksid olema hoolduskavaga seotud.

1. Valige kiirkaardil **Varatüübid** need varatüübid, mis peaksid olema hoolduskavaga seotud.

1. Valige kiirkaardil **Töö asukohad** need töö asukohad, mis peaksid olema hoolduskavaga seotud. Vajadusel saate muuta seadistuse spetsiifilisemaks, valides seotud vara tüübi, tootja ja mudeli.

1. Valige kiirkaardil **Töö asukohatüübid** need töö asukohatüübid, mis peaksid olema hoolduskavaga seotud.

>[!NOTE]
>Kui tarnija garantii alla käivatele varadele tehakse töökäsud käsitsi, kuvatakse dialoogikasti, et teavitada kasutajat garantiist. Siis saab töökäsu loomise tühistada. Automaatselt loodud töökäskudel on garantii seose kontrollimine välja jäetud.

<a id="interval-types"></a>

## <a name="interval-types-overview"></a>Intervalli tüüpide ülevaade

| Intervalli tüüp ja kirjeldus | Rea tüüp: aeg | Rea tüüp: loendur |
|---|---|---|
| **Intervalli tüüp: korratud planeerimiskuupäevast** Loendamine algab kasutatud planeerimiskuupäevast. Kui ajastate hoolduskavasid, luuakse intervalli saavutamisel hooldusgraafiku read. | Kasutatakse hoolduskava rea **Planeerimiskuupäeva**. Kui real ei ole planeerimiskuupäeva valitud, kasutatakse hoolduskava **Planeerimiskuupäeva**. Näide: kui väljale **Perioodi sagedus** on sisestatud number "3" ja väljale **Periood** on valitud "Aasta", luuakse uus hooldusgraafiku rida iga 3 aasta tagant. | Kasutatakse hoolduskava **Planeerimiskuupäeva**. Kui loendur on asendatud, kasutatakse planeerimiskuupäevana viimast asendamise kuupäeva. |
| **Intervalli tüüp: korduv alates alguskuupäevast** Lugemine algab vara seose alguskuupäevast. Kuupäev on valitud jaotises **Kõik varad** üksikasjade vaade \> kiirkaart **Vara hoolduskavad** \> väljal **Alguskuupäev** või jaotises **Kõik töö asukohad** üksikasjade vaade \> kiirkaart **Hoolduskavad** \> väljal **Alguskuupäev**. Kui ajastate hoolduskavasid, luuakse intervalli saavutamisel hooldusgraafiku rida. | Kasutatakse vara või töö asukohta hoolduskava rea alguskuupäeva. Kui see väli on tühi, kasutatakse hoolduskava **Planeerimiskuupäeva**. | Kasutatakse vara või töö asukohta hoolduskava rea alguskuupäeva. Kui see väli on tühi, kasutatakse hoolduskava **Planeerimiskuupäeva**. |
| **Intervalli tüüp: korduv alates viimasest töökäsust** Lugemine algab tegelikust vara konkreetse hooldustöö tüübi / hooldustöö variandi / vahetuse kombinatsiooni viimase lõpule viidud töökäsu tegelikust lõppkuupäevast ja -kellaajast. Kuupäeva ja kellaaega kuvatakse välja **Tegelik lõpp** üksikasjade vaates **Kõik töökäsud**. | Tegelik varaga lõpetatud töökäsu lõppkuupäeva ja -kellaaja ning konkreetse hooldustöö tüübi / hooldustöö tüübi variandi / vahetuse kombinatsioon. Kui lõpetatud töökäske ei leita, kasutatakse selle asemel ühte ülevalpool kirjeldatud intervalli tüübis "Korduv alates alguskuupäevast" kasutatud kuupäevadest. | Tegelik varaga lõpetatud töökäsu lõppkuupäeva ja -kellaaja *ning* hooldustöö tüübi / hooldustöö tüübi variandi / vahetuse kombinatsioon. on kasutatud. Kui töökäsul on lõppkuupäev ja -kellaaeg tühjaks jäetud, kasutatakse selle asemel ühte ülevalpool kirjeldatud intervallitüübis "Korduv alates alguskuupäevast" kasutatud kuupäevadest. |
| **Intervalli tüüp: üks kord alates planeerimiskuupäevast** vaadake eespool toodud intervallitüübi "Korduv alates planeerimiskuupäevast" kirjeldust. Ainuke vahe seisneb selles, et seda intervallitüüpi kasutatakse ainult üks kord. | Vaadake eespool toodud intervallitüübi "Korduv alates planeerimiskuupäevast" kirjeldust. Seda intervalli kasutatakse tavaliselt ühekordseteks hooldustöödeks. | Vaadake eespool toodud intervallitüübi "Korduv alates planeerimiskuupäevast" kirjeldust. Seda intervalli kasutatakse tavaliselt ühekordseteks hooldustöödeks. **Märkus 1:** see intervalli tüüp on asjakohane ainult siis, kui loendur asendatakse iga kord kui hooldustöid teostate. Kui mingil põhjusel on loendur enne plaanitud intervalli lõppu vahetatud, arvestatakse töö jaoks uus aeg alates loenduri asendamise ajast. **Märkus 2:** kui loendur asendatakse hooldustöö lõppedes, toimib see intervallitüüp eespool oleva intervallitüübina "Korduv alates planeerimiskuupäevast". |
| **Intervalli tüüp: üks kord alates alguskuupäevast** vaadake eespool toodud intervallitüübi "Korduv alates alguskuupäevast" kirjeldust. Ainuke vahe seisneb selles, et seda intervallitüüpi kasutatakse ainult üks kord. | Vaadake eespool toodud intervallitüübi "Korduv alates alguskuupäevast" kirjeldust. Seda intervalli kasutatakse tavaliselt ühekordseteks hooldustöödeks. | Vaadake eespool toodud intervallitüübi "Korduv alates alguskuupäevast" kirjeldust. Seda intervalli kasutatakse tavaliselt ühekordseteks hooldustöödeks. **Märkus 1** eeltoodu kehtib ka sellele intervallitüübile. **Märkus 3:** kui loendur asendatakse hooldustöö lõppedes, toimib see intervallitüüp eespool oleva intervallitüübina "Korduv alates alguskuupäevast". |
| **Intervalitüüp: kui on ületanud** see intervallitüüp on seotud ainult loenduritega ja seda kasutatakse hoolduskava reale määratud ülemise piiri näitamiseks. Hooldusgraafiku kirjetel on loenduri registreerimise oodatav alguskuupäev ja -kellaaeg, mis tähendab, et need kirjed luuakse oodatava alguskuupäevaga, mis on võrdne või varasem süsteemi kuupäevast. | Pole kohaldatav | Loenduri intervall näitab ülemist piiri. Kui see piir loenduri registreerimise ajal ületatakse, luuakse ennetava hoolduse ajastamise ajal hooldusgraafiku rida. |
| **Intervalitüüp: kui on jõudnud allapoole** see intervallitüüp on seotud ainult loenduritega ja seda kasutatakse hoolduskava reale määratud alumise piiri näitamiseks. Hooldusgraafiku kirjetel on loenduri registreerimise oodatav alguskuupäev ja -kellaaeg, mis tähendab, et need kirjed luuakse oodatava alguskuupäevaga, mis on võrdne või varasem süsteemi kuupäevast. | Pole kohaldatav | Loenduri intervall näitab alumist piiri. Kui see piir loenduri registreerimise ajal ületatakse, luuakse ennetava hoolduse ajastamise ajal hooldusgraafiku rida. |
| **Intervalli tüüp: seotud alguskuupäevast** See intervalli tüüp loob hooldusgraafiku rea ainult üks kord. Hoolduskava võib sisaldada rohkem selle intervallitüübiga hoolduskava ridu ja need read on seotud. Tavaliselt loote hoolduskava, mis sisaldab ainult selle intervallitüübiga ridu. Hooldusgraafiku read luuakse selle hoolduskava rea tuvastamisel, millel on kõige esimene oodatud alguskuupäev ja -kellaaeg. | Vaadake eespool olevat kirjeldust "Üks kord alates alguskuupäevast". Näide: Loote auto hooldustöö hoolduskavas kaks rida, üks ajapõhine rida 1-aastase perioodiga ja üks loenduripõhine rida 25 000 km piiriga. Hooldusgraafiku rida luuakse piirile, mis ületatakse esimesena. Selle reatüübi jaoks loote rea 1-aastase perioodiga. | Vaadake eespool olevat kirjeldust "Üks kord alates alguskuupäevast". Näide: Loote auto hooldustöö hoolduskavas kaks rida, üks ajapõhine rida 1-aastase perioodiga ja üks loenduripõhine rida 25 000 km piiriga. Hooldusgraafiku rida luuakse piirile, mis ületatakse esimesena. Selle reatüübi jaoks loote rea 25 000 km piiriga. Kahe loenduriga rea loomise näide: võite seadistada hoolduskava ka kahe seotud, loenduripõhise reaga, kus esimesel real on piiriks 10 000 toodetud üksust ja teine rida on seotud masina või töökeskusega, mis vajab hooldust pärast 3 000 tundi kestnud tööd. |
| **Intervalli tüüp: seotud viimasest töökäsust** See intervallitüüp loob pärast igat lõpetatud töökäsku uued hooldusgraafiku read. Hoolduskava võib sisaldada rohkem selle intervallitüübiga ja need read on seotud. Tavaliselt loote hoolduskava, mis sisaldab ainult selle intervallitüübiga hoolduskava ridu. Hooldusgraafiku read luuakse selle hoolduskava rea tuvastamisel, millel on kõige esimene oodatud alguskuupäev ja -kellaaeg. | See intervallitüüp toimib põhimõtteliselt nagu eespool kirjeldatud "Seotud alguskuupäevast". Ainuke vahe seisneb kuupäevas, millel intervallitüüp põhineb. Tegelik kasutatud kuupäev on tegeliku vara viimase töökäsu lõpetamise kuupäeva ja kellaaja *ning* hooldustöö tüübi / hooldustöö tüübi variandi / vahetuse kombinatsioon. | See intervallitüüp toimib põhimõtteliselt nagu eespool kirjeldatud "Seotud alguskuupäevast". Ainuke vahe seisneb kuupäevas, millel intervallitüüp põhineb. Tegelik kasutatud kuupäev on tegeliku vara viimase töökäsu lõpetamise kuupäeva ja kellaaja *ning* hooldustöö tüübi / hooldustöö tüübi variandi / vahetuse kombinatsioon. |
| **Intervalli tüüp: kordub koondväärtusel (ainult loendur)** Hooldusplaani käivitamisel luuakse planeeritud hooldusrida iga kord, kui varaloenduri akumuleeritud väärtus jõuab perioodisagedusele või isegi saavutab perioodisageduse kordse väärtuse. (Perioodi sagedus määratletakse hoolduskava real.)<p>Lisateavet selle funktsiooni lubamise ja kasutamise kohta vt selle teema hilisemast jaotisest [Loenduripõhise hoolduse täiustused](#counter-based-maintenance). | Pole kohaldatav | **Näide:** tunniloendur on häälestatud vara AK-101 jaoks. Vara jaoks on häälestatud ka põhivaraplaani rida. Selle rea intervallitüüp on *Korduv liidetud väärtus (ainult loendur)* ja perioodi sagedus on *1000*. Hooldusplaani käivitamisel luuakse plaanitud hooldusrida, kui loenduri koondväärtus ületab 1000 tundi. Seejärel kui loenduri koondväärtus ületab 2000 tundi, luuakse teine planeeritud hooldusrida jne iga täiendava 1000 tunni kohta. |
| **Intervalli tüüp: üks kord koondväärtusel (ainult loendur)** Hooldusplaani käivitamisel luuakse planeeritud hooldusrida, kui varaloenduri akumuleeritud väärtus jõuab perioodisagedusele, mis on hooldusplaani real määratletud.<p>Lisateavet selle funktsiooni lubamise ja kasutamise kohta vt jaotisest [Loenduripõhise hoolduse täiustused](#counter-based-maintenance). | Pole kohaldatav | **Näide:** tunniloendur on häälestatud vara AK-101 jaoks. Vara jaoks on häälestatud ka põhivaraplaani rida. Selle rea intervallitüüp on *Ühekordne liidetud väärtus (ainult loendur)* ja perioodi sagedus on *1000*. Hooldusplaani käivitamisel luuakse plaanitud hooldusrida, kui loenduri koondväärtus ületab 1000 tundi. |

>[!NOTE]
>Kui ajapõhistele hoolduskava ridadele luuakse hooldusgraafiku ridu, on oodatav aeg alati päeva alguses. Loenduripõhiste hoolduskava ridade korral võib oodatav aeg olla ükskõik millal päeva jooksul.

Allpool leiate näiteid ajapõhiste ja loenduripõhiste hoolduskava ridade seadistamise kohta.

**Näide 1 - ajapõhise hoolduskava rida:** määrimistöö võib seadistada fikseeritud intervalliga, toimudes korra nädalas. Selleks valige väljal **Intervalli tüüp** suvand „Korduv alates planeerimiskuupäevast”. Vt alloleval joonisel olevat näidet.

![Fikseeritud intervalliga hooldustöö, toimub kord nädalas](media/02-preventive-maintenance.png "Fikseeritud intervalliga hooldustöö, toimub kord nädalas")

**Näide 2 - ajapõhise hoolduskava rida:** ülevaatuse töö võib seadistada nii, et see teostatakse umbes korra nädalas. Selleks valige väljal **Intervalli tüüp** suvand „Korduv alates viimasest töökäsust”. Vt alloleval joonisel olevat näidet.

![Ligikaudu kord nädalas toimuma häälestatud ülevaatuse töö](media/03-preventive-maintenance.png "Ligikaudu kord nädalas toimuma häälestatud ülevaatuse töö")

**Näidis 3 - loenduripõhise hoolduskava rida:** järgmisel graafilisel joonisel on tundide loendur, mille jaoks luuakse iga kord 250 tunni möödudes uus hooldusgraafiku rida. Selle loenduripõhise rea intervalli tüüp on "Korduv alates alguskuupäevast". Alguskuupäevaks on seotus varade alguskuupäev jaotises **Kõik varad** üksikasjade vaade \> kiirkaardi **Vara hoolduskavad** \> väljal **Alguskuupäev** või jaotises **Töö asukoht** üksikasjade vaade \> kiirkaardi **Hoolduskavad** \> väljal **Alguskuupäev**. See on näide *ennetavast* hoolduskavast, sest hooldusgraafiku rida luuakse automaatselt iga kord läve (+ 250) ületamisel.

![Perioodiliselt hooldusgraafiku ridu loov tunniloendur](media/04-preventive-maintenance.png "Perioodiliselt hooldusgraafiku ridu loov tunniloendur")

**Näide 4 - loenduripõhise hoolduskava rida:** järgmisel graafilisel joonisel kujutatakse piduriklotsi kulumist mõõtva loenduri väärtuse langusest. Kui piduripadjale luuakse loenduri registreering, mis on alla 20 mm, luuakse hooldusgraafiku rida. Selle loenduripõhise rea intervalli tüüp on "Kui on jõudnud allapoole" või "Üks kord alates alguskuupäevast". See on näide *reageerivast* hoolduskavast, sest hooldusgraafiku rida ei looda enne, kui registreeritakse mõõtmistulemus, mis jääb alla 20 mm.

![Loenduri väärtuse vähenemine, piduriklotsi kulumise mõõtmine](media/05-preventive-maintenance.png "Loenduri väärtuse vähenemine, piduriklotsi kulumise mõõtmine")

**Näide 5 - loenduripõhise hoolduskava rida:** järgmisel graafilisel joonisel on loendur, mille lävi on -18° Celsiuse järgi. Hooldusgraafiku rida luuakse siis, kui loendur registreerib näidu temperatuuriga üle -18° Celsiuse järgi. Selle loenduripõhise rea intervalli tüüp on "Kui on ületanud". See on näide *reageerivast* hoolduskavast, sest hooldusgraafiku rida ei looda enne, kui registreeritakse mõõtmistulemus, on üle -18° Celsiuse järgi.

![Loendur läviväärtusega –18 °Celsius](media/06-preventive-maintenance.png "Loendur läviväärtusega –18 °Celsius")

- Kui loote uue vara ja see vara kasutab hoolduskavaga seotud vara tüüpi, sisestatakse hoolduskava automaatselt jaotise **Kõik objektid \> Vara hoolduskavad** kiirkaardile. Samuti sisestatakse seotud hoolduskavad automaatselt jaotise **Vaikimisi varatüübid** kiirkaardile **Hoolduskavad**.
- Kui lisate või eemaldate jaotises **Hoolduskavad** vara tüüpe või töö asukohatüüpe, peegeldub see muutus ainult uutel varadel, mis on loodud pärast muudatuse tegemist.
- Kui lisate või eemaldate varasid või töö asukohti jaotises **Hoolduskavad**, värskendatakse see muudatus automaatselt jaotises **Kõik varad \> Vara hoolduskavade** kiirkaardil või jaotise **Kõik töö asukohad \> Hoolduskavade** kiirkaardil.

Järgmisel joonisel on hoolduskava „Veoteenus” näide lehel **Hoolduskavad**.

![Veoauto hooldusplaani näide](media/07-preventive-maintenance.png "Veoauto hooldusplaani näide")

## <a name="add-a-maintenance-plan-to-an-asset"></a>Varale hoolduskava lisamine

1. Avage **Varahaldus \> Ühine \> Varad \> Kõik varad** või **Aktiivsed varad**.

1. Valige vara, millele soovite seadistada hoolduskava ja valige **Redigeeri**.

1. Valige kiirkaardil **Vara hoolduskavad** suvand **Lisa rida**, et lisada varale hoolduskava.

1. Valige väljal **Hoolduskava** asjakohane hoolduskava.

1. Valige väljalt **Alguskuupäev** see kuupäev, millal võib alustada ennetavate hooldustööde planeerimist. 

1. Valige käsk **Salvesta**. Väli **Aktiivne** värskendatakse automaatselt.

Järgmisel joonisel on vara alusel seadistatud hoolduskava näide lehel **Kõik varad**.

![Vara jaoks häälestatud hooldusplaanide näide](media/08-preventive-maintenance.png "Vara jaoks häälestatud hooldusplaanide näide")

<a id="counter-based-maintenance"></a>

## <a name="counter-based-maintenance-enhancements"></a>Loenduripõhise hoolduse täiustused

Funktsioon *Loenduripõhise hoolduse täiustused* lisab järgmised funktsioonid.

- Võimalus vara loomisel automaatselt sisestada loendur, mille väärtus on *0* (null). See valik võib olla kasulik, kui kasutate loenduritel põhinevat ennustushooldust. Kui funktsiooni *Loenduripõhise hoolduse täiustused* ei kasutata, tuleb loendurid, mille väärtus on *0* (null), sisestada käsitsi.
- Võimalus konfigureerida loendurit, et lähtestatakse töökäsu lõpuleviimisel automaatselt. See funktsioon on kasulik, kui soovite planeerida hoolduse alates viimase töökäsu lõpuleviidud koondväärtusest.
- Uut tüüpi hooldusplaani intervall, mille nimi on *Korduv koondväärtusel (ainult loendur)*. Seda tüüpi loendur käivitab hoolduse iga kord, kui koondloendur saavutab kindla väärtuse kordse. Näiteks hoolduse saab käivitada iga 10 000 tunni järel. Lisateavet leiate selle teema varasemast jaotisest [Intervalli tüüpide ülevaade](#interval-types).
- Teist uut tüüpi hooldusplaani intervall, mille nimi on *Ühekordne koondväärtusel (ainult loendur)*. Seda tüüpi loendur käivitab hoolduse, kui koondloendur saavutab kindla väärtuse, nagu 8000 tundi. Lisateavet leiate jaotisest [Intervalli tüüpide ülevaade](#interval-types).

### <a name="turn-on-the-counter-based-maintenance-enhancements-feature"></a>Loenduripõhise hoolduse täiustuste funktsiooni sisselülitamine

Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *varahaldus*
- **Funktsiooni nimi:** *Loenduripõhise hoolduse täiustused*

### <a name="create-and-initialize-counters-when-an-asset-is-created"></a>Loendurite loomine ja lähtestamine vara loomisel

Iga kord vara loomisel saab automaatselt luua väärtusega *0* (null) lähtestatud seotud varaloendurid, eeldusel, et seadistate oma süsteemi ja loote vara õigesti.

1. Avage **Varahaldus \> Seadistus \> Vara tüübid**.
1. Veenduge, et teil oleks vara tüüp, mida saab teie planeeritud uuele varale kohaldada. Nõutav on vara tüübi loomine. Veenduge, et kiirkaardil **Loendurid** oleks valitud kõik asjakohased loendurid.
1. Avage **Varahaldus \> Seadistus \> Vara tüübid \> Loendurid**.
1. Iga vastava loenduri puhul veenduge, et välja **Kogusumma** väärtuseks oleks määratud *Suma*.
1. Looge vara lehel **Kõik varad**.
1. Määrake väli **Vara tüüp** vara tüübile, mille 2. sammus tuvastasite või lõite.
1. Lõpetage uue vara seadistamine vastavalt vajadusele.
1. Avage **Varahaldus \> Päringud \> Varad \> Loendurid**. Peaksite saama otsida uue vara jaoks seadistatud lähtestatud loendurid.

> [!NOTE]
> Lähtestatud varaloendurite loomisel eeldatakse, et vara polnud enne süsteemi lisamist kunagi kasutatud. Kui hooldusgraafik käivitatakse esimest korda, kasutab arvutus tulevase hoolduse arvutamiseks alusena kuupäeva ja loenduri väärtust *0* (null). Kui vara polnud süsteemi lisatuna uus, saate loenduri väärtust käsitsi korrigeerida nii, et see vastaks tegelikule loenduri väärtusele. Loenduri väärtuse korrigeerimiseks avage vastav vara lehel **Kõik varad** ja seejärel valige tegevuspaani vahekaardil **Vara** grupis **Ennetav väärtus** suvand **Loendurid**. Valitud vara lehel **Varade loendurid** korrigeerige väärtust veerus **Väärtus** vastavalt vajadusele algse loendurikirje jaoks.

### <a name="automatically-reset-a-counter-value"></a>Loenduri väärtuse automaatne lähtestamine

Saate konfigureerida süsteemi automaatselt lähtestama loenduri iga kord, kui vastav töökäsk jõuab valitud oleku väärtuseni.

1. Avage **Varahaldus \> Seadistus \> Ennetav hooldus \> Hooldusplaanid**.
1. Valige loendipaanil hooldusplaan. Loenduri lähtestamine rakendub kõigile seda plaani kasutavatele varadele.
1. Leidke jaotises **Read** varaloenduri rida, mille loendurit soovite lähtestada, ja märkige selle rea puhul ruut **Lähtesta loendur**. (Varaloenduri ridadel on väärtus veerus **Loendur**. Selles veerus määratud loendur on loendur, mis lähtestatakse vastava vara jaoks.)
1. Avage **Varahaldus \> Seadistus \> Töökäsud \> Töötsükli olekud**.
1. Valige loendipaanil töötellimuse töötsükli olek, mille juures asjakohane loendur tuleks lähtestada.
1. Määrake kiirkaardil **Üldine** suvandi **Lähtesta loendur** olekuks *Jah*.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]