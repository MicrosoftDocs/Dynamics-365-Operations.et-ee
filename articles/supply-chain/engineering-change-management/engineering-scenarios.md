---
title: Tehnilise muudatuse haldamise funktsiooni juhis
description: See teema on põhjalik juhis, milles näidatakse, kuidas töötada tehnilise muudatuse haldamisega.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4c1c67559a8f2e9d0abb512f4231aea495d1957c
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573989"
---
# <a name="engineering-change-management-feature-walkthrough"></a>Tehnilise muudatuse haldamise funktsiooni juhis

[!include [banner](../includes/banner.md)]

See teema on põhjalik juhis, milles näidatakse, kuidas töötada tehnilise muudatuse haldamisega. See läbib iga kõige olulisema stsenaariumi.

- Põhiline funktsiooni konfigureerimine
- Kuidas tehnikaettevõte uut tehnilist toodet loob
- Kuidas tehnikaettevõte väljastab tehnilise toote kohalikule ettevõttele
- Kuidas kohalik ettevõte saab üle vaadata ja aktsepteerida toote, mille tehnikaettevõte talle väljastas
- Kuidas kohalik ettevõte saab kasutada tehnilist toodet tavalistes kannetes
- Kuidas lisada tehnilist toodet müügitellimusele
- Kuidas taotleda tehnilise toote muudatusi, luues tehnilise muudatuse taotluse
- Kuidas planeerida ja rakendada nõutud muudatusi, luues tehnilise muudatuse tellimuse
- Kuidas väljastada muudetud toodet

Kõik selle teema harjutused kasutavad standardseid näidisandmeid, mis on mõeldud Microsoft Dynamics 365 Supply Chain Managementi jaoks. Lisaks põhineb iga järgmine harjutus eelmisel harjutusel. Seetõttu soovitame, et te töötate harjutused läbi järjekorras algusest lõpuni, eriti juhul, kui te pole kunagi varem tehnilise muudatuse haldamise funktsiooni kasutanud. Sel viisil saate funktsioonist täieliku ülevaate.

## <a name="set-up-for-the-sample-scenario"></a>Näidisstsenaariumi seadistamine

Selleks, et järgida selles teemas esitatud näidisstsenaariumi, peate esmalt funktsiooni ette valmistama, tehes demoandmed kättesaadavaks ja lisades mõned kohandatud kirjed.

Enne kui püüate läbi teha teisi selle teema harjutusi, järgige juhiseid kõigis järgmistes alajaotistes. Need alajaotised toovad esile ka mitu olulist sätete lehte, mida hakkate kasutama, kui seadistate oma organisatsiooni jaoks tehnilise muudatuste haldamist.

### <a name="make-standard-demo-data-available"></a>Standardsete demoandmete kättesaadavaks tegemine

Töötage süsteemis, kuhu on [installitud standardsed demoandmed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Standardsed demoandmed lisavad mitme juriidilise isiku demoandmed (ettevõtted ja organisatsioonid). Harjutusi läbi töötades kasutate navigeerimisriba paremal pool olevat ettevõttevalijat, et lülituda ühe ettevõtte (*DEMF*), mis on seadistatud *tehnikaorganisatsioonina*, ja teise ettevõtte vahel (*USMF*), mis on seadistatud *operatiivorganisatsioonina*.

### <a name="set-up-an-engineering-organization"></a>Tehnikaorganisatsiooni seadistamine

Tehnikaorganisatsioon omab tehnilisi andmeid ning vastutab toote kujunduse ja toote muudatuste eest. Tehnikaorganisatsioonide seadistamiseks toimige järgmiselt.

1. Valige **Tehnilise muudatuse haldamine &gt; Seadistus &gt; Tehnikaorganisatsioonid**.
1. Valige **Uus**, et lisada ruudustikku rida, ja seejärel määrake sellele järgmised väärtused.

    - **Tehnikaorganisatsioon:** *DEMF*
    - **Organisatsiooni nimi:** *Contoso Entertainment System Germany*

    ![Tehnikaorganisatsiooni lisamine.](media/engineering-org.png "Tehnikaorganisatsiooni lisamine")

### <a name="set-up-the-version-product-dimension-group"></a>Versiooni tootedimensiooni grupi seadistamine

1. Avage **Tooteteabe haldus &gt; Seadistus &gt; Dimensioonid ja variandigrupid &gt; Tootedimensioonigrupid**.
1. Valige uue tootedimensioonigrupi loomiseks **Uus**.
1. Seadke välja **Nimi** väärtuseks *Versioon*.
1. Valige **Salvesta**, et salvestada uus dimensioon ja laadida väärtused kiirkaardile **Tootedimensioonid**.
1. Seadke kiirkaardil **Tootedimensioonid** dimensioon **Versioon** aktiivseks tootedimensiooniks.

    ![Tootedimensioonigrupi lisamine.](media/product-dimension-groups.png "Tootedimensioonigrupi lisamine")

### <a name="set-up-product-lifecycle-states"></a>Toote elutsükli olekute seadistamine

Tähtis on, et saaksite kontrollida, millised kanded on igas töötsükli olekus lubatud, kui tehniline toode töötsüklit läbib. Toote töötsükli olekute seadistamiseks tehke järgmist.

1. Valige **Tehnilise muudatuse haldamine &gt; Seadistus &gt; Toote töötsükli olek**.
1. Valige **Uus**, et lisada töötsükli olek, ja seejärel määrake sellele järgmised väärtused.

    - **Olek:** *operatiivne*
    - **Kirjeldus:** *operatiivne*

1. Valige **Salvesta**, et salvestada uus töötsükli olek ja laadida väärtused kiirkaardile **Lubatud äriprotsessid**.
1. Valige kiirkaardil **Lubatud äriprotsessid** sellised äriprotsessid, mis peaksid saadaval olema. Selle näite puhul jätke kõigi äriprotsesside korral välja **Poliitika** väärtuseks *Lubatud*.

    ![Töötsükli oleku jaoks äriprotsesside lubamine.](media/product-lifecycle-states-1.png "Töötsükli oleku jaoks äriprotsesside lubamine")

1. Valige **Uus**, et lisada veel üks töötsükli olek, ja seejärel määrake sellele järgmised väärtused.

    - **Olek:** *prototüüp*
    - **Kirjeldus:** *prototüüp*

1. Valige **Salvesta**, et salvestada uus töötsükli olek ja laadida väärtused kiirkaardile **Lubatud äriprotsessid**.
1. Valige kiirkaardil **Lubatud äriprotsessid** sellised äriprotsessid, mis peaksid saadaval olema. Selle näite puhul määrake kõigi äriprotsesside korral välja **Poliitika** väärtuseks *Lubatud koos hoiatusega*.

    ![Töötsükli oleku jaoks äriprotsesside lubamine (koos hoiatustega).](media/product-lifecycle-states-2.png "Töötsükli oleku jaoks äriprotsesside lubamine (koos hoiatustega)")

### <a name="set-up-a-version-number-rule"></a>Versiooninumbri reegli seadistamine

1. Valige **Tehnilise muudatuse haldamine &gt; Seadistus &gt; Tooteversiooni numbri reegel**.
1. Valige **Uus**, et lisada reegel, ja seejärel määrake sellele järgmised väärtused.

    - **Nimi:** *automaatne*
    - **Numbri reegel:** *automaatne*
    - **Vorming:** *V-\#\#*

    ![Tooteversiooni numbri reegli lisamine.](media/version-number-rule.png "Tooteversiooni numbri reegli lisamine")

### <a name="set-up-a-product-release-policy"></a>Toote väljastamise poliitika seadistamine

1. Valige **Tehnilise muudatuse haldamine &gt; Seadistus &gt; Toote väljastamise poliitikad**.
1. Valige **Uus**, et lisada väljastamise poliitika, ja seejärel määrake sellele järgmised väärtused.

    - **Nimi:** *komponendid*
    - **Kirjeldus:** *komponendid*

1. Määrake kiirkaardil **Üldine** järgmised väärtused.

    - **Toote tüüp:** *Kaup*
    - **Rakenda malle:** *alati*
    - **Aktiivne:** *jah*

1. Valige kiirkaardil **Kõik tooted** suvand **Lisa**, et lisada rida, ja seejärel seadke sellele järgmised väärtused.

    - **Ettevõte:** *DEMF*
    - **Väljastatud toote mall:** *D0006*

1. Valige **Lisa**, et lisada uus rida, ja määrake sellele järgmised väärtused.

    - **Ettevõtte kontode ID:** *USMF*
    - **Väljastatud toote mall:** *D0006*
    - **Võta kooslus vastu:** märkige see märkeruut.
    - **Kopeeri koosluse kinnitus:** märkige see märkeruut.
    - **Kopeeri koosluse aktiveerimine:** märkige see märkeruut.
    - **Võta protsess vastu:** märkige see märkeruut.
    - **Kopeeri protsessi kinnitus:** märkige see märkeruut.
    - **Kopeeri protsessi aktiveerimine:** märkige see märkeruut.

    ![Toote väljastamise poliitika lisamine.](media/product-release-policy.png "Toote väljastamise poliitika lisamine")

### <a name="set-up-an-engineering-product-category"></a>Tehnilise toote kategooria seadistamine 

Tehnilise toote kategooriad on alused tehniliste toodete loomiseks (st toodeteks, mille versioone luuakse ja mida juhitakse tehnilise muudatuse haldamise kaudu). Tehnilise toote kategooriate seadistamiseks toimige järgmiselt.

1. Minge jaotisse **Tehnilise muudatuse haldamine &gt; Tehnilise toote kategooria üksikasjad**.
1. Valige uue kategooria loomiseks **Uus**.
1. Määrake kiirkaardil **Üksikasjad** järgmised väärtused.

    - **Nimi:** *komponendid*
    - **Tehnikaorganisatsioon:** *DEMF*
    - **Toote tüüp:** *Kaup*
    - **Jälgi kannetes versiooni:** *jah*
    - **Tootedimensioonigrupp:** *Versioon*
    - **Toote töötsükli olek loomisel:** *operatiivne*
    - **Versiooninumbri reegel:** *automaatne*
    - **Kehtivuse jõustamine:** *ei*
    - **Kasuta numbrireegli nomenklatuuri:** *ei*
    - **Kasuta nimereegli nomenklatuuri:** *ei*
    - **Kasuta kirjeldusereegli nomenklatuuri:** *ei*

1. Seadke kiirkaardil **Väljastamise poliitika** välja **Toote väljastamise poliitika** väärtuseks *Komponendid*.
1. Valige käsk **Salvesta**.

    ![Tehnilise toote kategooria lisamine.](media/product-category-details.png "Tehnilise toote kategooria lisamine")

### <a name="set-up-product-acceptance-conditions"></a>Toote heakskiitmise tingimuste seadistamine

1. Kasutage navigeerimisriba parempoolsel küljel asuvat ettevõttevalijat, et lülituda ümber juriidilisele isikule *USMF* (ettevõte).
1. Valige **Tehnilise muudatuse haldamine &gt; Seadistus &gt; Tehnilise muudatuse haldamise parameetrid**.
1. Seadke vahekaardil **Väljastamise juhtimine** jaotises **Toote heakskiitmine** välja **Toote heakskiitmine** väärtuseks *Käsitsi*.

    ![Toote heakskiitmise tingimuste seadistamine.](media/engineering-change-management-parameters.png "Toote heakskiitmise tingimuste seadistamine")

## <a name="create-a-new-engineering-product"></a>Uue tehnilise toote loomine

Tehniline toode on toode, mille versioone luuakse ja mida juhitakse tehnilise muudatuse haldamise kaudu. Teisisõnu saate muudatusi selle elu jooksul juhtida ning muudatuste teave salvestatakse tehnilise muudatuse tellimuste abil. Tehniliste toodete loomiseks toimige järgmiselt.

1. Veenduge, et oleksite oma tehnikaorganisatsiooni juriidilises isikus (*DEMF* selle näite puhul). Kasutage vajadusel navigeerimisriba parempoolsel küljel asuvat ettevõttevalijat.
1. Avage leht **Väljastatud tooted** ühel järgmistest viisidest.

    - Avage **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**.
    - Valige **Tehnilise muudatuse haldamine &gt; Ühine &gt; Väljastatud tooted**.

1. Valige toimingupaani vahekaardi **Toode** grupis **Uus** suvand **Tehniline toode**.
1. Dialoogiboksis **Uus toode** määrake järgmised väärtused.

    - **Tehnilise toote kategooria:** *komponendid*
    - **Toote number:** *Z0001*
    - **Toote nimi:** *kõlarid*

    ![Tehnilise toote lisamine.](media/new-product-dialog.png "Tehnilise toote lisamine")

    Võtke arvesse, et väli **Versioon** määratakse automaatselt, kasutades varem seadistatud tooteversiooni numbri reeglit.

1. Valige toote loomiseks ja dialoogiboksi sulgemiseks **OK**.
1. Avatakse uue toote üksikasjade leht. Pange tähele, et mõne välja, nt **Laoala dimensiooni grupp**, **Jälgimisdimensiooni grupp** ja/või **Kauba mudeligrupp**, väärtused on juba määratud. Need väljad määrati automaatselt, kuna toode väljastatakse juriidilises isikus *DEMF* ja see kasutab toote väljastamise poliitikat *Komponendid*, mis on seotud tehnilise toote kategooriaga *Komponendid*. Kuna kasutasite varem mallina üksust *D0006*, et seadistada rida juriidilise isiku *DEMF* jaoks, võeti täidetud väärtused üksusest *D0006*.

    ![Väljastatud toote üksikasjad.](media/product-details.png "Väljastatud toote üksikasjad")

1. Valige toimingupaanil vahekaardil **Projekteerimine** grupis **Tehnilise muudatuse haldamine** suvand **Tehnilised versioonid**, et vaadata toote versioone.

    ![Tehnilised versioonid.](media/engineering-versions-list.png "Tehnilised versioonid")

1. Pange tähele, et lehel **Tehnilised versioonid** on toote jaoks on ainult üks versioon ja see on aktiivne.
1. Valige versioon selle üksikasjade kuvamiseks.

    ![Tehnilise versiooni üksikasjad.](media/engineering-version-details.png "Tehnilise versiooni üksikasjad")

1. Valige lehel **Tehniline versioon** kiirkaardil **Kooslus** suvand **Loo kooslus**.
1. Määrake dialoogiboksis **Koosluse loomine** järgmised väärtused.

    - **Koosluse number:** Z0001
    - **Nimi:** kõlarid
    - **Tegevuskoht:** 1

    ![BOM-i loomine.](media/create-bom.png "Koosluse loomine")

1. Valige koosluse lisamiseks ja dialoogiboksi sulgemiseks **OK**.
1. Valige kiirkaardil **Kooslused** suvand **Kooslus**.
1. Lisage lehel **Kooslus** kiirkaardil **Koosluseread** kolm rida, üks igale järgmisele kaubakoodile: *D0001*, *D0003* ja *D0006*.

    ![Koosluseridade lisamine.](media/bom.png "Koosluseridade lisamine")

1. Valige käsk **Salvesta**.
1. Sulgege leht.
1. Valige lehel **Tehniline versioon** kiirkaardil **Kooslus** suvand **Kinnita**.
1. Kuvatavas dialoogiboksis tehke valik **OK**.

    ![Koosluse kinnitamine.](media/approve-dialog.png "Koosluse kinnitamine")

1. Valige lehel **Tehniline versioon** kiirkaardil **Kooslus** suvand **Aktiveeri**.
1. Pange tähele, et koosluse jaoks on valitud märkeruudud **Aktiivne** ja **Kinnitatud**.

    ![Aktiivne ja kinnitatud kooslus.](media/approved-bom.png "Aktiivne ja kinnitatud kooslus")

1. Sulgege leht.

## <a name="release-an-engineering-product-to-a-local-company"></a><a name="release"></a>Tehnilise toote väljastamine kohalikule ettevõttele

Tehniline osakond on nüüd toote kujundanud. Selle näite puhul on toode prototüüp, mida on tehniline osakond kliendi jaoks loonud. Kuna klient on juriidilise isiku *USMF* klient, tuleb toode väljastada sellele juriidilisele isikule.

1. Las juriidiline isik olla *DEMF*. (Kasutage vajadusel navigeerimisriba parempoolsel küljel asuvat ettevõttevalijat.)
1. Avage **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**.
1. Valige toode *Z0001*.
1. Valige toimingupaanil vahekaardil **Toode** grupis **Haldamine** suvand **Väljasta tootestruktuur**, et avada viisard **Toodete väljastamine**.
1. Valige lehel **Väljastatavate tehniliste toodete valimine** toote **Z0001** korral märkeruut *Vali*.

    ![Väljastatavate tehniliste toodete valimine.](media/select-eng-product-to-release.png "Väljastatavate tehniliste toodete valimine")

1. Valige **Väljastamise üksikasjad**.
1. Kuvatakse leht **Toote väljastamise üksikasjad**, kus saate vaadata väljastatud toote üksikasju ja selle struktuuri. Pange tähele, et suvandi **Saada kooslus** väärtuseks on valitud *Jah*. Seetõttu väljastatakse nii toode *Z0001* kui ka kõik kooslusest pärit tütarüksused.

    Saate valida mis tahes tütarüksuse vasakul paanil selle üksikasjade ülevaatamiseks. Kui mis tahes tütarüksusel on kooslus, saate väljastada ka selle tütarüksuse koosluse.

    ![Toote väljastamise üksikasjade ülevaatamine.](media/product-release-details.png "Toote väljastamise üksikasjade ülevaatamine")

1. Sulgege leht, et naasta viisardi **Toodete väljastamine** juurde.
1. Valige **Järgmine**, et avada leht **Väljastatavate toodete valimine**. Kui valisite mõne standardse (mitte tehnilise) toote, kuvatakse need sellel lehel. Võtke arvesse, et kui te väljastate standardse toote suvandi **Väljasta tootestruktuur** kaudu, väljastatakse ka selle kooslus ja protsess.

    ![Väljastatavate standardsete toodete valimine.](media/select-std-product-to-release.png "Väljastatavate standardsete toodete valimine")

1. Valige **Järgmine**, et avada leht **Väljastatavate tootevariantide valimine**. Selle näite korral variandid puuduvad.
1. Valige **Järgmine**, et avada leht **Ettevõtete valimine**.
1. Valige ettevõtted, millele toode tuleb väljastada. Selle näite korral valige märkeruut ettevõtte **USMF** jaoks.

    ![Ettevõtete valimine neile väljastamiseks.](media/select-release-companies.png "Ettevõtete valimine neile väljastamiseks")

1. Valige **Järgmine**, et avada leht **Valiku kinnitamine**.
1. Valige **Lõpeta**.

## <a name="review-and-accept-the-product-before-you-release-it-in-the-local-company"></a><a name="accept"></a>Toote ülevaatamine ja heakskiitmine enne kohalikule ettevõttele väljastamist

Tehniline osakond on nüüd teabe väljastanud kohalikele ettevõtetele, kus toodet kasutatakse. Selles näites on kohalik ettevõte *USMF*.

Kuna seadsite välja **Toote heakskiitmine** väärtuseks *Käsitsi* ettevõtte **USMF** lehel *Tehnilise muudatuse haldamise parameetrid*, tuleb tooted enne sellele ettevõttele väljastamist käsitsi heaks kiita. Teisisõnu tuleb need üle vaadata ja heaks kiita, enne kui need muutuvad väljastatud toodeteks.

Toote ülevaatamiseks ja väljastamiseks ettevõttes *USMF* toimige järgmiselt.

1. Määrake juriidiliseks isikuks *USMF*. (Kasutage navigeerimisriba parempoolsel küljel asuvat ettevõttevalijat.)
1. Avage jaotis **Tehnilise muudatuse haldamine &gt; Ühine &gt; Tooteväljastused &gt; Avatud tooteväljastused**.

    Lehel **Avatud tooteväljastused** on toode *Z0001*, mille olek on *Heakskiitmise ootel*.

    ![Avatud tooteväljastused.](media/open-product-releases.png "Ava tooteväljastused")

1. Valige veeruus **Tootenumber** olev väärtus, et avada leht **Toote väljastamise üksikasjad**. Pange tähele järgmiseid üksikasju.

    - Vahekaardil **Üldine** on teave toote väljastamise kohta, nt väljastav ettevõte (*DEMF* selles näites), väljastav tegevuskoht (*1*) ja vastuvõttev tegevuskoht (*1*). Kuna te ei määranud vastuvõtvat tegevuskohta viisardis **Toodete väljastamine**, kopeeritakse väljastava tegevuskoha väärtus vastuvõtva tegevuskoha väljale.
    - Kiirkaardil **Väljastamise üksikasjad** on teave toote ja väljastatud versiooni kohta. Siin saate muuta sätteid, nt kehtivuskuupäevi.
    - Kiirkaardil **Protsess** on toote protsess. Kuid selle näite puhul ei väljastanud te ühtegi protsessi.

    ![Tooteväljastuse üksikasjad.](media/product-release-details-2.png "Tooteväljastuse üksikasjad")

1. Kui olete teabe läbivaatamise lõpetanud, olete valmis tooted heaks kiitma ja sel viisil väljastama selle ettevõttes *USMF*. Valige toimingupaanil **Tegevused &gt; Kiida heaks**.
1. Toode väljastatakse nüüd ettevõttele *USMF*. Avage **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**. Peaksite nägema kaupa *Z0001*.

## <a name="use-the-product-in-transactions-in-the-local-company"></a>Toote kasutamine kohaliku ettevõtte kannetes

Ettevõtte *USMF* koondandmete haldur soovib veenduda , et toote olek on *Prototüüp*, tagamaks, et kasutajaid hoiatatakse, kui nad lisavad selle kogemata protsessi, millega nad töötavad.

1. Avage **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**.
1. Valige toode *Z0001*, et avada selle üksikasjade leht. (Saate kasutada toote leidmiseks filtrit.)
1. Valige toimingupaanil vahekaardil **Projekteerimine** grupis **Tehnilise muudatuse haldamine** suvand **Tehnilised versioonid**.
1. Lehel **Tehnilised versioonid** valige versiooninumber *V-01*, et avada selle üksikasjade leht.
1. Valige toimingupaanil vahekaardil **Toode** grupis **Töötsükli olek** suvand **Muuda töötsükli olekut**.
1. Määrake rippmenüüs **Töötsükli oleku muutmine** välja **Olek** väärtuseks *Prototüüp* ja seejärel valige **OK**.

    ![Töötsükli oleku muutmine.](media/change-lifecycle-state.png "Töötsükli oleku muutmine")

## <a name="add-the-engineering-product-to-a-sales-order"></a>Tehnilise toote lisamine müügitellimusele

Toodet saab nüüd kliendile müüa. Toote lisamiseks müügitellimusele järgige neid juhiseid.

1. Avage **Müük ja turundus &gt; Müügitellimused &gt; Kõik müügitellimused**.
1. Valige toimingupaanil nupp **Uus**.
1. Määrake dialoogiboksis **Müügitellimuse loomine** välja **Kliendi konto** väärtuseks *US-0002* ja siis valige **OK**.
1. Avatakse uus müügitellimus. Lisage kiirkaardil **Müügitellimuse read** uus rida ja määrake selle välja **Kaubakood** väärtuseks *Z000*.
1. Valige toimingupaanil nupp **Salvesta**.

    Kuvatakse hoiatusteade, mis teavitab teid, et kauba olek on *Prototüüp*. Kuid kuna see on ainult hoiatus, loodi müügitellimus ikkagi.

    ![Tehnilise toote müügitellimus.](media/sales-order-eng-product.png "Tehnilise toote müügitellimus")

## <a name="request-changes-in-the-engineering-product"></a>Tehnilise toote muudatuste taotlemine

Toode saadeti kliendile, kuid klient ei olnud täielikult rahul ja annab tagasisidet, mis sisaldab soovitusi täiustuste kohta. Ajal, mil klient kõneleb telefonis müüjaga, võib müüja taotleda kliendi kirjeldatud muudatusi.

1. Avage **Müük ja turundus &gt; Müügitellimused &gt; Kõik müügitellimused**.
1. Otsige üles ja avage eelmises harjutuses loodud müügitellimus.
1. Valige kiirkaardil **Müügitellimuse read** jaotis **Tehnilise muudatuse haldamine &gt; Uus tehnilise muudatuse taotlus**.

    ![Tehnilise muudatuse taotluse loomine müügitellimuse põhjal.](media/sales-order-eng-change-request.png "Tehnilise muudatuse taotluse loomine müügitellimuse põhjal")

1. Täitke tehnilise muudatuse taotlus, mis põhineb kliendi tagasisidel. Seadke selle näite korral järgmised väärtused.

    - **Muudatuse taotlus:** *555*
    - **Pealkiri:** *Z0001 kliendi muudatus*
    - **Prioriteet:** *madal*
    - **Kategooria:** muudatuse määramine
    - **Raskusaste:** *keskmine*

1. Valige kiirkaardil **Teave** suvand **Uus &gt; Märkus**, et lisada märkus ruudustikku.
1. Näidake uue märkuse väljal **Kirjeldus**, et kaup *D0003* tuleks kooslusest kustutada. Kui peate märkusele lisama lisateavet, saate sisestada teksti väljale **Märkused**.

    ![Tehnilise muudatuse taotlus.](media/eng-change-request.png "Tehnilise muudatuse taotlus")

1. Valige toimingupaanil nupp **Salvesta**.
1. Pange tähele, et kaup on automaatselt lisatud kiirkaardile **Tooted** ja tehnilise muudatuse taotluse allikas (müügitellimus) on lisatud kiirkaardile **Allikas**.

## <a name="make-changes-to-the-product-by-using-an-engineering-change-order"></a>Toote muutmine tehnilise muudatuse tellimuse abil

Müüja teab, et toode on oluline ja kavandatud spetsiaalselt sellele kliendile. Seetõttu helistab müüja ettevõtte *DEMF* insenerile, et teavitada teda muudatuse taotlusest. Sel viisil saab insener protsessi kiiremaks muuta.

Insener vaatab nüüd kliendi taotluse üle ja loob toote jaoks muudatuse tellimuse.

1. Kuna insener töötab ettevõttes *DEMF*, määrake juriidiliseks isikuks *DEMF*. (Kasutage navigeerimisriba parempoolsel küljel asuvat ettevõttevalijat.)
1. Valige **Tehnilise muudatuse haldamine &gt; Ühine &gt; Tehnilise muudatuse taotlused**.
1. Avage muudatuse taotlus *555*.
1. Vaadake teave üle ja seejärel kinnitage muudatus. Valige toimingupaani vahekaardil **Muudatuse taotlus** grupis **Muudatuse olek** suvand **Kinnita**.
1. Valige **Tehnilise muudatuse haldamine &gt; Ühine &gt; Tehnilise muudatuse tellimused**.
1. Valige toimingupaanil **Uus**, et luua muudatuse tellimuse, ja määrake sellele järgmised väärtused.

    - **Muudatuse tellimus:** *555*
    - **Pealkiri:** *Z0001 kliendi muudatus*
    - **Kategooria:** *kliendi muudatus*
    - **Prioriteet:** *madal*
    - **Raskusaste:** *keskmine*

1. Valige kiirkaardil **Mõjutatud tooted** suvand **Uus &gt; Lisa olemasolev toode**, et lisada ruudustikku uus rida, ja määrake selle jaoks järgmised väärtused.

    - **Toode:** *Z0001*
    - **Mõju:** *uus versioon*

    ![Tehnilise muudatuse tellimuse loomine.](media/eng-change-order.png "Tehnilise muudatuse tellimuse loomine")

1. Pange tähele, et kuna määrate välja **Mõju** väärtuseks *Uus versioon*, näitab väli **Uus versioon**, mis asub kiirkaardi **Toote üksikasjad** vahekaardil **Üksikasjad**, uue versiooni numbrit (*V-02* selle näite puhul).

    ![Tehnilise muudatuse tellimuse toote üksikasjad.](media/eng-change-order-product-details.png "Tehnilise muudatuse tellimuse toote üksikasjad")

1. Valige toimingupaanil nupp **Salvesta**.
1. Valige kiirkaardil **Toote üksikasjad** vahekaardil **Kooslus** suvand **Read**, et avada toote *Z0001* versioon *V-01*.

    ![Tehnilise toote koosluseread.](media/eng-product-bom-lines.png "Tehnilise toote koosluseread")

1. Valige kaubakoodi *D0003* rida ja seejärel valige toimingupaanil käsk **Kustuta**. Selle rea välja **Muudatuse tüüp** väärtuseks muutub *Kustutatud*.
1. Valige toimingupaanil nupp **Salvesta**.

    ![Muudetud tehnilise toote koosluseread.](media/eng-product-bom-lines-modified.png "Muudetud tehnilise toote koosluseread")

1. Sulgege leht **Koosluserida**, et naasta lehele **Tehnilise muudatuse tellimus**.
1. Pange tähele, et kiirkaardil **Toote üksikasjad** vahekaardil **Kooslus** on koosluse **Z0001** välja *Muudatuse tüüp* väärtus nüüd *Muudetud*.

    ![Tehnilise muudatuse tellimus, mis sisaldab muudetud kooslust.](media/eng-change-order-changed-bom.png "Tehnilise muudatuse tellimus, mis sisaldab muudetud kooslust")

    Tellimus tuleb enne muudatuste töötlemist kinnitada. Kui muudatusi töödeldakse, uuendatakse tooteid nii, nagu tehnilise muudatuse tellimuses kirjas. Selle näite puhul on kinnitajaks määratud isik, kes loob tehnilise muudatuse tellimuse.

1. Valige toimingupaani vahekaardil **Muudatuse tellimus** grupis **Muudatuse olek** suvand **Kinnita**.
1. Valige **Töötle**, et värskendada toote teavet.

## <a name="release-the-changed-product"></a>Muudetud toote väljastamine

Toote saab nüüd uuesti ettevõttele *USMF* väljastada ja seejärel kliendile saata. Toote väljastamiseks otse tehnilise muudatuse tellimusest toimige järgmiselt.

1. Avage eelmises harjutuses loodud tehnilise muudatuse tellimus, kui see ei ole juba avatud.
1. Valige toimingupaani vahekaardil **Muudatuse tellimus** grupis **Tooteväljastused** suvand **Otsi**.
1. Otsingutulemused näitavad, millistele ettevõtetel on mõjutatud tooted väljastatud. Sulgege otsingutulemused.
1. Valige toimingupaani vahekaardil **Muudatuse tellimus** grupis **Tooteväljastused** suvand **Kuva**, et avada dialoogiboks **Väljastamised**, kus saate vaadata eelmise otsingu tulemusi.
1. Valige iga ettevõte, millele soovite tooted väljastada.
1. Tehke dialoogiboksi **Väljastamised** sulgemiseks ja muudatuse tellimuse juurde naasmiseks valik **OK**.
1. Valige toimingupaani vahekaardil **Muudatuse tellimus** grupis **Tooteväljastused** suvand **Töötle**, et väljastada mõjutatud tooted valitud ettevõtetele. Võite väljastamise protsessi alustamiseks valida ka **Väljasta tootestruktuur**.

## <a name="complete-the-change-order"></a>Märgi muudatuse tellimus lõpuleviiduks

Muudatuse tellimuse lõpuleviiduks märkimiseks (see osutab, et rohkem pole vaja midagi teha) valige toimingupaanil **Vii lõpule**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
