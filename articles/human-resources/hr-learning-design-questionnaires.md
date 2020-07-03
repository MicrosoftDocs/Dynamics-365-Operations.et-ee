---
title: Küsimustike kujundamine
description: See artikkel kirjeldab küsimustiku koostamise protsessi. Esimene samm on küsimustiku kavandamine. Küsimustiku kavandamisel ei kirjutata ainult küsimusi ja vastuseid, vaid luuakse ka struktuur, mis võimaldab vastuste salvestamise ja tabelisse paigutamise.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KCMCollectionType, KMAnswerCollection, KMCollection, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 17341
ms.assetid: b27e2f12-c7a0-4a54-b8d8-17819f8a1c72
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: da4250b281438c29c82150af8db9cb8cca41c6c9
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429562"
---
# <a name="design-questionnaires"></a>Küsimustike kujundamine

See artikkel kirjeldab küsimustiku koostamise protsessi. Esimene samm on küsimustiku kavandamine. Küsimustiku kavandamisel ei kirjutata ainult küsimusi ja vastuseid, vaid luuakse ka struktuur, mis võimaldab vastuste salvestamise ja tabelisse paigutamise. 

Hoolikalt koostatud küsimustik võib aidata tõsta kogutavate andmete kvaliteeti. Hoolika kavandamise kaudu saate küsimustiku jaoks sobival ajal paremini sobivaid võimalusi valida. Järgmised punktid aitavad tulemuslikku küsimustikku kavandada.

-   Määratlege selgelt küsimustiku eesmärk, et tagada küsimustega eesmärgi toetamine.
-   Määrake inimene või inimeste grupp, kes peaksid küsimustiku täitma.
-   Kirjutage küsimustikus sisalduvad küsimused üles ja lisage valikvastused, kui vaja.
-   Veenduge, et küsimustik kulgeb loogiliselt, et vastajate huvi püsiks.
-   Pange küsimused ja vastused vastajale esitamise järjekorda.
-   Otsustage vajaduse korral, kuidas tuleks tulemusi hinnata.
-   Otsustage, kas on vaja lisafunktsioone. Näiteks määrake, kas ja kuidas tuleks tulemused kategooriatesse jagada, kas on vaja ajapiirangut või kas kõik küsimused on kohustuslikud.

Kavandamise faas sisaldab nelja ülesannete kategooriat, mis tuleb läbida järgmises järjekorras.

1.  Seadistage vajalikud eeltingimused.
2.  Seadistage vajaduse korral vastusegrupid ja vastused.
3.  Seadistage küsimused ja nende seosed vastusegruppidega.
4.  Seadistage küsimustik ja lisage sellele küsimused.

## <a name="prerequisites"></a>Eeltingimused 
Mõned eeltingimused peavad olema kehtestatud enne, kui saate küsimustikke, vastuseid ja küsimusi luua. Kuid kõigi funktsioonide kasutamiseks pole kohustuslikud kõik eeltingimused.

### <a name="required"></a>Nõutav

| Eeltingimus        | Kirjeldus                |
|---------------------|----------------------------|
| Küsimustike tüübid | Saate küsimustikud kategooriatesse jagada. |
| Küsimuste tüübid      | Saate küsimused kategooriatesse jagada.      |

### <a name="optional"></a>Valikuline

| Eeltingimus             | Kirjeldus                                                    |
|--------------------------|----------------------------------------------------------------|
| Küsimustiku parameetrid | Saate muuta küsimustike peamisi juhtelemente ja vaikesätteid. |

### <a name="questionnaire-types"></a>Küsimustike tüübid

Küsimustike tüübid on kohustuslikud ja need tuleb määrata küsimustiku koostamisel. Küsimustike tüübid aitavad küsimustikke hõlpsamini hallata ja klassifitseerida. Kasutage küsimustike tüüpe küsimustike klassifitseerimiseks ja üksteisest eristamiseks. Näiteks kui teil on mitu küsimustikku, mille vahel valida, võite neid tüübi järgi filtreerida, et konkreetset küsimustikku oleks lihtsam leida. Siin on mõned näited küsimustike tüüpide kohta.

-   inimressursside areng,
-   kliendiülevaated,
-   Protsessi ülevaade

### <a name="question-types"></a>Küsimuste tüübid

Küsimuse tüübid on kohustuslikud ja need tuleb määrata küsimuse koostamisel. 

Saate kasutada küsimuste tüüpe aruandluse eesmärgil küsimuste kategoriseerimiseks. Küsimuste tüübid muudavad ka küsimuste leidmise lihtsamaks, kuna saate tüüpe lehel **Küsimused** filtritena kasutada. Siin on mõned näited küsimuste tüüpide kohta.

-   Inimressursid
-   Ärijuhtimine
-   Kursuse hindamine

### <a name="questionnaire-parameters"></a>Küsimustiku parameetrid

Küsimustiku parameetrid on valikulised. Te ei pruugi neid kasutada, olenevalt teie ettevõtte vajadustest. 

Küsimustiku parameetrid määratlevad küsimustiku anonüümsuse, numbriseeriakoodid ja viitetüübid. Kui organisatsioon küsimustiku laiali saadab, võib olla vaja võimaldada kasutajatel anonüümseks jääda. 

Küsimuste ja vastuste korraldamiseks kasutatakse numbriseeriakoode. Nende numbriseeriakoodide põhjal määratakse kaupadele automaatselt väärtused. 

Kõik parameetrid tuleks määratleda enne andmete loomise alustamist. Küsimustiku parameetri sätteid saab igal ajal muuta.

## <a name="questionnaire-components"></a>Küsimustiku osad
Küsimustikud hõlmavad kolme põhielementi: vastusegruppe, mis sisaldavad valikvastustega küsimuste vastuseid, küsimusi ja küsimustikku ennast. Soovi korral saab küsimustiku küsimused tulemusegruppidesse jagada. Tulemusegrupid võimaldavad küsimusi kategoriseerida ja küsimustikku edasi analüüsida. 

[![QuestionnaireComponents](./media/questionnairecomponents-1024x615.png)](./media/questionnairecomponents.png)

### <a name="answer-groups-and-answers"></a>Vastusegrupid ja vastused

Olenevalt küsimuse teemast saavad vastajad küsimustele vastata kahel viisil.

-   Avatud küsimused ei vaja teatud vormis vastuseid. Vastajad saavad tippida vastuse tekstina, numbritega, kuupäeva või kellaajana. Need küsimused nõuavad vastajatelt vastustes tavaliselt subjektiivset teavet, nt arvamust, kirjeldust, hinnangut või prognoosi.
-   Suletud küsimused nõuavad, et vastaja valiks vastuse võimalike õigete vastuste hulgast.

Võimaliku vastuste loendi esitamiseks suletud küsimustele võite luua vastused lehel **Vastusegrupid**. 

Vastusegrupid ja vastused on komponendid, mis moodustavad küsimuste aluseks oleva teabe põhiosa. Pärast vastusegrupi loomist saate seostada selle vastusegrupi küsimusega väljal **Vastusegrupp** lehel **Küsimused**. 

Vastusegruppi saab kasutada samas küsimustikus rohkem kui ühe küsimuse puhul ja ka rohkem kui ühes küsimustikus. 

> [!NOTE]
> Kui muudate vastuste rühmas vastuse teksti, mida on juba kasutatud täidetud küsimustikes, võib andmete hindamine osutuda raskeks ja küsimustiku tulemused ei pruugi enam kehtida. Kui teil on vaja vastusegruppi muuta, kaaluge olemasoleva grupi muutmise asemel uue vastusegrupi loomist. Küsimuse või vastusega seotud või vastatud vastusegruppe ei saa kustutada.

### <a name="questions"></a>Küsimused

Küsimustik peab sisaldama küsimusi. Küsimused võivad olla avatud või suletud.

-   Avatud küsimuste vastuseid ei kontrollita ja vastajad saavad oma vastused tippida.
-   Suletud küsimused nõuavad eelnevalt määratud vastusevalikute loendit ja küsimusi saab ehitada üles nii, et vastaja võib valida mitu vastust. Küsimused tuleks kavandada nii, et nende abil saaks vastajalt konkreetset teavet, ja need tuleb siduda vastusegrupiga, mis annab igale suletud küsimusele vastusevariandid. 

    > [!NOTE]
    > Enne suletud küsimuste seadistamist peate looma vastuserühmad ja vastused.

Küsimused saab paigutada tingimuslikku küsimuste hierarhiasse, nii et sekundaarsed küsimused sõltuvad vastusest, mille vastaja eelmisele küsimusele valib. Saate kõigepealt küsimused kirjutada ja siis need hiljem hierarhiasse paigutada.

## <a name="setting-up-questionnaires"></a>Küsimustike seadistamine

> [!NOTE]
> Enne küsimustiku seadistamist peate üles seadma vastused, küsimused ja eeltingimused. 

Iga küsimustiku jaoks saate määrata järgmised andmed.

-   Kohustuslikele küsimustele vastamise aeg kokku või ajapiir.
-   Kas kõik küsimused on kohustuslikud.
-   Kas arvestada küsimustiku puhul punkte.
-   Kuidas kategoriseerida tulemusi.
-   Kas küsimustik on saadaval piiratud vastajate grupile.
-   Kas iga küsimustiku lehe taustana tuleks kuvada vormimall.
-   Kas on vaja lisamärkusi, et selgitada vastajatele küsimustiku eesmärki.
-   Kas on vaja kuvada küsimused kindlas järjestuses või valida need kaustast juhuslikult.
-   Kas küsimusi esitatakse ainult juhul, kui eelmiste puhul anti teatud vastuseid.

### <a name="set-up-a-questionnaire"></a>Küsimustiku seadistamine

Peamine leht, mida küsimustiku seadistamiseks kasutatakse, on leht **Küsimustikud**. Küsimustiku seadistamiseks tehke järjest järgmised toimingud.

1.  Looge küsimustik.
2.  Järgige ühte neist toimingutest küsimustikule küsimuste lisamiseks.
    -   Tulemusegruppide kasutamisel saate lisada küsimustikule küsimusi tulemusegruppide abil. Seadistage esmalt küsimustikule tulemusegrupid ja seejärel lisage tulemusegruppidesse küsimusi.
    -   Kui te tulemusegruppe ei kasuta, võite lisada küsimused otse küsimustikku.

3.  Vajaduse korral seadistage tingimuslike küsimuste hierarhia.
4.  Testige küsimustikku.

Klõpsake lehel **Küsimustikud** valikut **Kinnita** testimiseks, kas küsimustik on õigesti koostatud. Kuid samuti tasub täita küsimustik ja testida seda ise enne laiali saatmist.

### <a name="modify-a-questionnaire"></a>Küsimustiku muutmine

Lehel **Küsimustikud** saab teha järgmisi toiminguid.

-   Muuta küsimustiku teavet (nt tulemusegruppe ja küsimusi).
-   Kustutada ja lisada küsimusi.
-   muuta tulemustegruppe ja järjekorranumbreid. 

> [!CAUTION]
> Olge ettevaatlik, kui muudate küsimustikke, millele on juba vastatud. Muudatused võivad vähendada statistika täpsust ja seetõttu muuta selle hindamiseks ebapiisavaks. Vastatud küsimuse muutmise asemel võiksite luua uue küsimuse.

Küsimustikus ei saa kustutada järgmist tüüpi küsimusi.

-   Küsimustikuga seotud küsimused
-   Juba vastatud küsimused, mis seetõttu kuvatakse dialoogiboksis **Vastused**.

### <a name="result-groups"></a>Tulemustegrupid

Tulemusegrupid on valikulised, kui seote küsimused küsimustikega. 

Tulemusegruppi kasutatakse punktide arvestamiseks ja küsimustiku tulemuste kategooriatesse jagamiseks. Kui kasutate tulemusegruppe, saate teha järgmist.

-   Hinnata küsimustiku tulemusi punktide statistika alusel.
-   Hinnata vastaja skoori iga seadistatud tulemusegrupi puhul.
-   Tulemuste analüüsimise hõlbustamiseks tehke iga tulemustegruppi kohta statistikat.
-   Printida aruande, milles kuvatakse iga tulemusegrupi tulemused ja ka valikulised punktid/tekstid, mis põhinevad igas tulemusegrupis teenitud punktidel.

> [!NOTE]
> Enne tulemusrühmade seadistamist peate täitma järgmised ülesanded.

-   Seadistage suletud küsimused. Suletud küsimuste puhul peab sisendi tüüp lehel **Küsimused** olema **Märkeruut**, **Alternatiivne nupp** või **Liitboks**.
-   Määrake vastusegrupis iga küsimuse juurde vastuse punktide arv.
-   Seadistage küsimustik.

Küsimuste sidumiseks küsimustikega tulemusegruppide abil seadistage kõigepealt küsimustiku tulemusegrupid ja lisage siis tulemusegruppidesse küsimusi. Kui te tulemusegruppe ei kasuta, võite siduda küsimused otse küsimustikuga. 

Saate seadistada mitu tulemusegruppi, et hinnata punkte, mida vastaja igas kategoorias teenib. Pärast küsimustiku täitmist saate vaadata igas tulemusegrupis saadud punkte. 

> [!TIP]
> Küsimustiku hindamiseks punktide abil, kuid mitte eraldi kategooriaid kasutades, saate kõik küsimused lisada ühte tulemusrühma. 

Iga tulemusegrupi kohta saab seadistada ka vähemalt ühe punktidel põhineva teate, mille vastajad pärast küsimustiku täitmist saavad. Kuvatav tekst võib varieeruda, olenevalt punktisummast, mille vastaja tulemusegrupis saavutas. Punktidel põhinevate teadete kasutamiseks tuleb määratleda punktide intervallid ja iga intervalli kirjeldus. Kui vastaja saavutab punktisumma konkreetses intervallis, lisatakse tulemuste aruandesse selle intervalli tekst. 

Kuna tulemusegrupp on seotud konkreetsete küsimuseplokkide punktidega, saate kasutada küsimustiku puhul ainult konkreetset tulemusegruppi.

#### <a name="example-pointstexts-for-result-group-3"></a>Näiteks: punktid/tekstid tulemusegrupile 3

Kasutate juhtimisküsimustikku, milles on 15 küsimust kolmes kategoorias. Loote kolm tulemusegruppi ja lisate igasse tulemusegruppi viis küsimust. Seejärel summeeritakse punktid kolmes grupis. Kolm tulemusegruppi on järgmised.

-   Loovus
-   Juhivõimed
-   Tehnilised teadmised

Punktipõhiste sõnumite kasutamiseks seadistate igale tulemusegrupile tekstivahemikud. Igale küsimusele määratakse kaks punkti. Seetõttu on iga tulemustegrupi maksimaalse punktisumma 10. 

Järgmises tabelis on toodud punktipõhised sõnumid, mille määratlete tulemustegrupile „juhivõimed”.

| Punktivahemik | Tekst                                       |
|----------------|--------------------------------------------|
| 1 kuni 3         | Teil on keskmised juhivõimed.     |
| 4 kuni 7         | Teil on head juhivõimed.        |
| 8 kuni 10        | Teil on suurepärased juhivõimed. |

Saate seadistada punktivahemikud ja tekstid igale tulemusegrupile küsimustikus. Iga vastaja skooril põhinevad tekstid kuvatakse iga tulemusegrupi puhul. 

> [!NOTE]
> Saate intervalle ja tekste muuta. Kuid kui küsimustik on täidetud, võivad muudatused põhjustada eelmiste ja uute tulemusearuannete vahel erinevusi.

### <a name="conditional-question-hierarchies"></a>Tingimuslike küsimuste hierarhiad

Tingimuslike küsimuste hierarhiad on küsimustiku seadistamisel valikulised. 

> [!NOTE]
> Enne tingimusliku küsimuste hierarhia seadistamist peate lisama küsimustikule küsimused, millel on määratud vastusrühmad. 

Tingimuslike küsimuste kasutamiseks küsimustikus küsimuste hierarhia loomiseks võite luua küsimuste esitamise järjekorra sõltuvalt vastusest, mille vastaja iga küsimuse puhul valib. Võttes küsimuste järjestuse aluseks vastajate vastusevaliku, saate küsimustikku kohandada sel ajal, kui vastaja seda täidab.

#### <a name="examples"></a>Näited

Juriidiline isik pakub oma klientidele nii kaupu kui ka teenuseid. Nagu sellistel puhkudel tavaliselt juhtub, ostavad mõned kliendid ainult kaupu, mõned ainult teenuseid ja mõned nii kaupu kui ka teenuseid. Seega, kui juriidiline isik saadab laiali kliendirahulolu uuringu, rakendatakse küsimustikus tingimuslikku struktuuri, et kliendid, kes ostavad ainult teenuseid, ei peaks vastama kaupu puudutavatele küsimustele. 

Teine võimalus on seadistada küsimustik nii, et kui vastaja valib küsimusele 1 vastuse A, on küsimus 2 küsimuste järjekorras järgmine. Kuid kui vastaja valib küsimuse 1 puhul vastuse B, on järgmine küsimus 5.