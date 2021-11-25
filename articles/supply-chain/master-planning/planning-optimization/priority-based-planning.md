---
title: Prioriteedipõhine planeerimine
description: Selles teemas kirjeldatakse Microsofti prioriteedipõhise planeerimise funktsiooni Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 10/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 41c4f3e9bd41735b213743bd8b4cdd8d9657a073
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/09/2021
ms.locfileid: "7777885"
---
# <a name="priority-based-planning"></a>Prioriteedipõhine planeerimine

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Selles teemas kirjeldatakse Microsofti prioriteedipõhise planeerimise funktsiooni Dynamics 365 Supply Chain Management. See funktsioon toetab nõudlusepõhist planeerimist, mis on üks samm nõudlusepõhiste materjalinõuete planeerimisest (DDMRP). Prioriteedipõhine planeerimine võimaldab planeerimise optimeerimisel luua plaanitud tellimusi, mis põhinevad vajaduse kuupäevade asemel plaanimise prioriteetidel.

Prioriteedipõhine planeerimine võimaldab teil prioriteerida varude täiendamise tellimusi nii, et tagada pakilise nõudluse tähtsusjärjekorras väiksem nõudlus. Näiteks laovarude täiendamise tellimusele täidetakse standardne taastäitmise varude täiendamise tellimus. Süsteem saab suuremad tellimused automaatselt tükeldada eraldi väiksemateks tellimusteks, kus tellimuseread on grupeeritud prioriteedi alusel. Seejärel saab esimesena töödelda kõiki kõrge prioriteediga tellimusi.

Selle funktsiooni kohta kiire ülevaate saamiseks vaadake järgmist videot: prioriteedipõhise plaanimise planeerimise [toe plaanimine Dynamics 365 Supply Chain Management](https://youtu.be/GmMHzFETTQc).

## <a name="turn-on-priority-based-planning-in-your-system"></a>Lülita prioriteedipõhine planeerimine enda süsteemis sisse

Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *Koondplaneerimine*
- **Funktsiooni nimi:** *prioriteedile suunatud MRP tugi optimeerimise planeerimiseks*

## <a name="where-and-how-planning-priorities-are-assigned"></a>Kus ja kuidas määratakse planeerimise prioriteedid

*Pakkumise ja* nõudluse prioriteediteabe plaanimine on prioriteedipõhise planeerimise tagakaanel. Planeerimise prioriteet määratleb nõudluse või pakkumise rea tähtsuse. Planeerimise optimeerimine kasutab seda, kui **laovarude koodi** väli on seatud väärtusele *·* Prioriteet.

Planeerimis prioriteet on tavaliselt arv vahemikus 0 (null) ja 100 (kus 0 tähistab kõrgeimat tähtsust). See kuvatakse ja seadistatakse väljal **Plaanimise** prioriteet. Selle välja leiate järgmistelt lehtedelt: nõudluse prognoosi read, müügitellimuse üksikasjad, ostutellimuse **·** **·** **·** üksikasjad, **üleviimistellimuse üksikasjad** ja **plaanitud tellimuse** üksikasjad.

Kui asjakohase kauba või laovarude grupi laovarude koodi väli on seatud väärtusele Prioriteet, võtab plaanimine optimeerimise saldod nõudlusega pakkumisega, kasutades nõudlusepõhist lähenemist, nagu see arvutab plaanimise prioriteedi, ja võtab iga väljastatud toote puhul väärtused, mis on seadistatud minimaalne, järeltellimuse punkt ja maksimaalne väljadele kauba **·** *·* **·** **·** **·** **laovarude** lehel.

> [!NOTE]
> Prioriteetne *·* väärtus on saadaval laovarude koodi väljal ainult **·** siis, kui plaanimise optimeerimine on lubatud.

Seotud planeerimise *prioriteedimudelid kontrollivad* plaanimise prioriteeti ja jagavad plaanitud tellimused prioriteedivahemiku järgi. Samuti saavad need määrata igale pakkumise või nõudluse tüübile planeerimise vaike-prioriteedi väärtused ja määratleda prioriteedi arvutamise meetodi.

## <a name="types-of-priority-calculation-methods"></a>Prioriteedi arvutamise meetodite tüübid

Igal plaanimise prioriteedimudelil on **prioriteedi arvutamise meetodi** säte, mis kontrollib, kuidas koondplaneerimine plaanitud tellimustele prioriteeti kohaldab. Saadaolevad väärtused on *maksimaalse laokoguse ja* prioriteedi *vahemike* protsent. *·* Prioriteedivahemikud tähistavad maksimaalse varude koguse *meetodi täpsemat* versiooni.

### <a name="percent-of-maximum-inventory-quantity"></a>Maksimaalse laokoguse protsent

Maksimaalse varude koguse arvutamise meetodis leiab tarne prioriteedi arvutamine praeguse kogu saadaoleva *laovaru (netovoog) protsendina kaubale seadistatud maksimaalse* *·* **·** laokoguse väärtusest. Sel juhul luuakse üks plaanitud tellimus kauba ja hankija kohta (välja arvatud tükeldamise sunnil kasutatakse maksimaalset tellimuse kogust). Tellimuse planeerimise prioriteet arvutatakse protsendina maksimaalsest.

Arvutamisel kasutatakse järgmist valemit:

*Maksimumprotsent* = *(voo* netopositsioon × 100) ÷ laovarude laovarude *maksimaalne laokoguse väärtus*

Selles *valemis arvutatakse* netovoo positsioon järgmiselt:

*Puhasvoo* = *positsioon* + *vabas tellimuses* – *kvalifitseeritud nõudlus*

- *Ettetellimus on* eeldatav tarne.
- *Kvalifitseeritud* nõudlus kajastab netovajadusi, mille vajaduse kuupäev jääb plaanimise ajapiiri piiresse.

Koondplaneerimise käivitamisel luuakse uued plaanitud tellimused, kui voo netopositsioon on väiksem kui kauba lisatellimuse punktikogus. Plaanitud tellimuse kogus on kaubatasemel seadistatud maksimaalse **·** laokoguse väärtuse ja voo netopositsiooni vahe. Plaanitud tellimuse prioriteet arvutatakse maksimaalse *laokoguse väärtuse* voo **netopositsiooni** protsendina.

> [!NOTE]
> Arvutatud prioriteet ei saa olla negatiivne, isegi kui nõudlus ületab kogutarnet. Kui nõudlus ületab kogutarne, seatakse arvutatud prioriteediks 0 (null).

### <a name="priority-ranges"></a>Prioriteedivahemikud

Prioriteedivahemiku arvutamismeetod on täpsem kui maksimaalne varude koguse meetodi protsent ja see konfigureeritakse *·* *·* plaanimise prioriteedimudeli tasemel. Iga kauba nõudluse täitmiseks saab luua mitu uut plaanitud tarnetellimust. Plaanitud tarne prioriteedid järgivad väärtusi, mis on määratletud prioriteedi planeerimise **·** vahemike ruudustikus lehel **Plaanimise prioriteedi** mudelid.

Järgmised lisareeglid jõustub, kui prioriteedi **arvutamise meetodi** välja väärtuseks on seatud Prioriteedi *vahemikud:*

- Kui plaanitud prioriteedimudeli prioriteedi arvestamine valik on seatud väärtusele Jah, piirab igale nõudluse reale seatud prioriteet **·** *·* prioriteedivahemiku vahemikku. Mis tahes uue plaanitud pakkumise tellimuse prioriteet ei ole väiksem kui nõudluse prioriteet. Vahemiku kõrgemat väärtust peetakse läveks, millega nõudluse prioriteedi väärtust võrreldakse. Kui nõudluse prioriteet on kahe vahemiku ülemise läviväärtuse vahel täpselt keskel, valitakse kõrgeima prioriteediga vahemik (st madalaim prioriteedi väärtus).
- Kui plaanitud prioriteedimudeli plaanitud tellimuse loomise välja väärtuseks on seatud Kõige olulisema prioriteediga üks tarne, luuakse ainult üks tarne, et täita kõik viis **·** *·* maksimaalseni. Prioriteediks seatakse tarnet käivitava esimese vahemiku prioriteet.
- Kui vaba kaubavaru, pakkumine puudub ja nõudlus puudub, kasutatakse rida ruudustikus Plaanimise prioriteet, kus välja Alates koguse väärtuseks on **·** määratud **·** *·* Null.
- Kui nõudlus puudub, kuid vaba kaubavaru või eeldatav pakkumine puudub, kasutatakse planeerimise prioriteedi ruudustiku rida, kus välja Kogusest väärtuseks on määratud Null või **·** **·** *·* Väiksem.
- Kui hinnatakse vahemikku, mille osa nõudlus on, on suvandi **Arvesta nõudlus** prioriteeti säte veel mõjuma.

## <a name="differences-between-traditional-timeline-calculations-and-priority-based-planning"></a>Tavalise ajajoone arvutuste ja prioriteedipõhise planeerimise vahelised erinevused

Prioriteedipõhine planeerimine erineb traditsioonilistest ajajoonte arvutustest järgmistel viisidel:

- Kõik regulaarsed eelplaneerimineprotsessorid on endiselt jõus. Need eelprotsessorid hõlmavad kinnitatud plaanitud tellimuste sidumist müügi nõudluse, ostutaotluse vastendamise ja reserveerimisloogikaga. Töödeldakse ainult nõudlust, mida need eelprotsessorid ei täidab.
- Sidumise ajal peetakse kogu tarnet sõltumata selle prioriteedist. See tarne hõlmab vaba kaubavaru, vabastatud tarnet ja kinnitatud plaanitud tellimuste mitte seotud osa.
- "Negatiivseid päevi" nõudlust ei saa kogu laovaruaja jooksul tarnimisega seoda.
- Kui pakkumine on seotud nõudlusega, kasutatakse esimesena kõrgeima prioriteediga (st madalaima prioriteediga) pakkumist. Vaba kaubavaru puhul peetakse prioriteedi väärtuseks 0 (null). Seetõttu tarbitakse see kõige esimese allikana.
- Uued plaanitud tarneread luuakse vastavalt tellimuse minimaalse suuruse, maksimaalse tellimuse suuruse, koguse kordaja jne tavareeglitele.

## <a name="planning-priority-models"></a>Plaanimise prioriteedimudelid

*Planeerimise prioriteedi* mudelid määratakse laovarude gruppidele ja need kontrollivad plaanitud tellimuste plaanimise prioriteeti. Need määravad loogika, mis määrab, kuidas planeerimise prioriteedi väärtust iga plaanitud tellimuse puhul arvutatakse ning kuidas määratakse prioriteet plaanitud tellimustele, tarneridadele ja nõudluse ridadele.

Planeerimise prioriteedimudelitega tööks minge **koondplaneerimise seadistuse \>\> prioriteedimudelite** juurde. Nagu eelnevalt mainitud, on ühe mudeli üks olulisemaid sätteid prioriteedi **arvutamise meetodi** väärtus. See säte juhib arvutamismeetodit, mida kasutatakse siis, kui koondplaneerimine määrab plaanitud tellimustele prioriteedi väärtuse.

> [!NOTE]
> Plaanimise prioriteedimudelid kehtivad organisatsiooni hõlmavalt kõigi juriidiliste isikute lõikes.

### <a name="coverage-group"></a>Laovarude grupp

Seadistage uus laovarude grupp, mida plaanite kasutada prioriteedipõhiseks planeerimiseks, nagu kirjeldatud jaotises [Kauba laovarude reeglite määratlemine.](../tasks/define-coverage-rules-items.md) Kui olete laovarude grupi loonud, seadke järgmised lisaväljad:

- **Laovarude** kood: *valige* prioriteet, kui laovarude grupp kasutab prioriteedipõhist planeerimist.
- **Plaanimise** prioriteedimudel – valige mis tahes organisatsiooni hõlmav plaanimise prioriteedimudel.

### <a name="item-coverage"></a>Kauba laovarud

Seadistage kauba laovarude sätted, nagu on kirjeldatud [laovarude](../coverage-settings.md) sätetes. Vaikimisi kopeeritakse **laovarude** grupi jaoks valitud laovarude koodi väärtus kauba laovarude sätetesse. Kuid vaikeväärtuse saate vajaduse korral alistada. Mõnel juhul on kauba laovarude kirje laovarude koodi väli seatud valikule Planeerimine, kuid seotud laovarude grupi jaoks pole määratletud **·** ühtegi *·* plaanimise prioriteedimudelit. Sel juhul rakendatakse vaikimisi kõiki mudeleid, kus prioriteedi arvutamise meetodi välja väärtuseks on seatud Protsent maksimaalsest laokogusest ja välja Plaanitud tellimuse loomine väärtuseks on määratud Kõige olulisema prioriteediga **·** *·* **·** *·* üksiktarne.

Seadistage **väli** Laovarude kood *väärtusele* Prioriteet, et teha väli **·** Järeltellimuse punkt kauba laovarude sätetes kättesaadavaks. Sellele väljale sisestage lisatellimuse punkti kogus, mida süsteem peaks kasutama, kui määratleb, millal teha plaanitud tellimused, mille laovarude **koodi** väärtus on *·* Prioriteet.

Lisatellimuse punkti kogust arvutatakse sageli nii, et täitmisaja nõudlus pluss minimaalne väärtus (ohutusvaru). See peab olema miinimum- **ja** maksimumväärtuste **vaheline** väärtus.

Näiteks võite seada väljad järgmiselt:

- **Miinimum:** *10*
- **Lisatellimuse punkt:** *45*
- **Maksimum:** *60*

Selle näite puhul põhineb lisatellimuse punktikogus seitsmepäevase täitmisajal ja keskmisel päevasel kasutamisel 5. Seepärast on nõudlus täitmisaja jooksul 35. Kordustellimuse punkti 45 jaoks lisatakse siis minimaalne väärtus 10 (ohutusvaru). Kui seda seadistust kasutatakse, soovitatakse tarnet, kui prognoositud vaba kaubavaru tase on alla 45. Tellimuse prioriteet põhineb plaanimise prioriteedi häälestusel.

### <a name="manage-planning-priority-models"></a>Plaanimise prioriteedimudelite haldamine

Töötada planeerimise prioriteedimudelitega; Järgige neid samme.

1. Minge **koondplaneerimise seadistamise \>\> prioriteedimudelite** juurde.
1. Valige loendipaanil olemasolev mudel või valige **uue mudeli** loomiseks tegevuspaanil uus.
1. Määrake uue kirje päises järgmised väljad.

    - **Nimi:** sisestage mudeli nimi. Nimi peab olema kordumatu kõigi teie organisatsiooni juriidiliste isikute lõikes.
    - **Kirjeldus** – sisestage mudeli kirjeldus.
    - **Prioriteedi arvutamise meetod** – valige üks järgmistest väärtustest:

        - *Prioriteedivahemikud* – kui valite selle väärtuse, muutub **plaanimise prioriteedi vahemike** ruudustik kättesaadavaks. Seal peate plaanimise prioriteedi väärtuse määratlemiseks looma mitu prioriteedivahemikku.
        - *Maksimaalse laokoguse* protsent – arvutage plaanimise prioriteetväärtus protsendina, mis põhineb maksimaalset laokogust ületava varude tasemel.

    - **Plaanitud tellimuse** loomine – see väli on saadaval, kui välja Prioriteedi **·** arvutamismeetod väärtuseks on *seatud Prioriteedivahemikud.* Valige üks järgmistest väärtustest.

        - *Kõige olulisema prioriteediga üksiktarne* – ärge tükeldage prioriteedivahemikul põhinevaid plaanitud tellimusi. Plaanitud tellimuse planeerimis prioriteet põhineb kõige olulisemal prioriteedivahemikul (st madalaimal planeerimise prioriteediväärtusel).
        - *Tükelda vastavalt prioriteedivahemikule* – tükeldage nõudlus mitmeks plaanitud tellimuseks, mis põhineb plaanimise prioriteedi vahemikel. Üksikute plaanitud tellimuste plaanimise prioriteedi määratleb seotud plaanimise prioriteedivahemiku planeerimise prioriteet.

    - **Kaaluge nõudluse prioriteeti – määrake selle suvandi väärtuseks Jah, et piirata** *·* pakkumiseks loodud uue plaanitud tellimuse prioriteeti. (Prioriteet ei ole väiksem kui seotud nõudluse prioriteet.) Kui määrate selle valiku väärtuseks Ei, ei arvestata tarnetellimuse prioriteedi arvutamisel nõudlustellimuse *·* prioriteeti.

1. Kui seate prioriteedi arvutamise meetodi välja väärtuseks Prioriteedivahemikud, kasutage nuppe Lisamine ja Eemaldamine kiirkaardi Plaanimise prioriteedivahemikud **·** *·* **·** **·** **tööriistaribal,** et lisada või eemaldada vajaduse järgi prioriteedivahemiku ridu. Kui on olemas mitu rida ja sisestate uue rea, seatakse planeerimise prioriteediks automaatselt valitud rea ja selle kohal olnud rea keskmine. Määrake igas reas järgmised väljad.

    - **Plaanimise** prioriteet – sisestage mis tahes väärtus vahemikus 0,00 kuni 100,00. Väärtus näitab rea planeerimise prioriteeti. Madalaim prioriteediväärtus tähistab kõrgeimat prioriteeti. Vaikeväärtus on määratud, kuid saate seda vajaduse korral muuta. Sama planeerimise **prioriteedi väärtust ei saa sama** plaanimise prioriteedimudelis kasutada rohkem kui ühe plaanimise prioriteedivahemiku puhul.
    - **Kirjeldus–** sisestage plaanimise prioriteedivahemiku kirjeldus (nt *lisatellimuse punkt valikule* Maksimum).
    - **Alates** kogusest – plaanimise prioriteedivahemiku alumine limiit. See väärtus on kirjutuskaitstud ja põhineb eelmise plaanimise prioriteedivahemiku koguse kuni- ja **·** **·** protsendiväärtustel.
    - **Koguseni** – valige kauba laovarude väli, mida tuleks kasutada vahemiku ülempiiri määratlemiseks. Järgmise vahemiku väärtust Alates kogusest toetatakse **ja need mõjutavad järgmisi** väärtusi:

        - *Null* – see väärtus tähistab nullist negatiivset vahemikku *(null või väiksem kui* *·* null). Ridade puhul, kus see väärtus valitakse, on väli Protsent kogusest kirjutuskaitstud ja **·** seadistatud *alati 100* protsendile.
        - *Minimaalne* laokogus – see **väärtus näitab kauba** minimaalset väärtust kauba **laovarude** lehel. Ridade puhul, kus see väärtus on valitud, on väli Protsent kogusest redigeeritav ja seda kasutatakse järgmise vahemiku väärtuse Alates kogusest **·** **·** (nt *80% minimaalsest* laokogusest).
        - *Lisatellimuse* punkt – see väärtus näitab kauba laovarude lehel **oleva kauba** lisatellimuse punkti **·** väärtust. Ridade puhul, kus see väärtus on valitud, on väli Protsent kogusest redigeeritav ja seda kasutatakse järgmise vahemiku väärtuse Alates kogusest **·** **·** (nt *80% kordustellimuse* punktist).
        - *Maksimaalne* laokogus – see **väärtus** näitab kauba laovarude lehel oleva kauba **maksimaalset** väärtust. Ridade puhul, kus see väärtus on valitud, on väli Protsent kogusest redigeeritav ja seda kasutatakse järgmise vahemiku koguse Alates (nt **·** **·** *80% minimaalsest laokogusest)* määrata.
        - *Piiramatu* – see väärtus esindab vahemiku piiramatut ülemist taset *(Lõpmatus või* väiksem kui *·* Piiramatu). Ridade puhul, kus see väärtus valitakse, on väli Protsent kogusest kirjutuskaitstud ja **·** seadistatud *alati 100* protsendile.

    - **Koguseni – sisestage protsentväärtus, mida kasutatakse väljal Koguseni valitud väärtusel põhineva plaanimise prioriteedi** **vahemiku ülempiiri** arvutamiseks. Näiteks kui välja Koguseni väärtuseks on seatud Minimaalne laokogus ja välja Kuni koguse protsent väärtuseks on **·** seatud *·* **·** *·* 50, on ülempiir 50 protsenti minimaalsest laokogusest seotud kauba laovarudest.

1. Seadke planeerimise prioriteedi vaikeväärtuste kiirkaardil väljad vastavalt vajadusele määratleda iga pakkumise või nõudluse rea (müügitellimus, ostutellimus, üleviimistellimus või nõudluse prognoos) **vaikeplaneerimise** prioriteedid. Sisestada saab ainult positiivseid väärtusi.

## <a name="view-and-maintain-planning-priority"></a>Plaanimise prioriteedi vaadake ja säilitage seda.

Planeerimise prioriteeti näidatakse ja seatakse väljal **Plaanimise** prioriteet. See väli asub järgmises tabelis loetletud lehtedel. Prioriteet seatakse numbrina vahemikus 0 (null) kuni 100, kus 0 tähistab kõrgeimat tähtsust.

| Lehekülg | Välja asukoht | Väärtuse allikas |
|---|---|---|
| Nõudluse prognoosi read | <p>**Vahekaart** Kaup</p><p>(Valige ülemises jaotises rida ja seejärel valige **Vahekaart** Kaup.)</p> | Käsitsi seadistatud vaikeväärtus või väärtus |
| Müügitellimuse detailid | <p>**Tarne** vahekaart rea üksikasjade **·** kiirkaardil</p><p>(Valige rida väljal **Müügitellimuse ridade** kiirkaart ja seejärel valige **kiirkaardil** Rea üksikasjad vahekaart **·** Tarne.)</p> | Kontsernisisene vaikeväärtus, väärtus või käsitsi seadistatud väärtus |
| Ostutellimuse üksikasjad | <p>**Tarne** vahekaart rea üksikasjade **·** kiirkaardil</p><p>(Valige rida väljal **Ostutellimuse ridade** kiirkaart ja seejärel valige **kiirkaardil** Rea üksikasjad vahekaart **·** Tarne.)</p> | Plaanitud tellimustest, kontsernisisesest väärtusest või käsitsi seadistatud väärtusest sisestamisel määratav väärtus |
| Üleviimistellimuse üksikasjad | <p>**Tarne** vahekaart rea üksikasjade **·** kiirkaardil</p><p>(Valige rida väljal **·** Üleviimistellimuse ridade kiirkaart ja seejärel valige **kiirkaardil Rea üksikasjad vahekaart** **·** Tarne.)</p> | Väärtus, mis seatakse plaanitud tellimuste või käsitsi seadistatud väärtuse põhjal kindlustamisel |
| Plaanitud tellimuse detailid | **Üldine** kiirkaart | Koondplaneerimisel arvutatud väärtus või käsitsi seadistatud väärtus |

### <a name="intercompany-trade"></a>Kontsernisisene kaubavahetus

Kontsernisisese **pakkumise ja nõudluse ridade planeerimise prioriteedi väärtus on** lingitud üksuste vahel ühiskasutuses. Mõlema poole muutmine kajastub lingitud tellimusereal.

Järgmisena on toodud mõned näited.

- Kasutaja muudab kontsernisisese müügitellimuse rea planeerimis prioriteedi 20-st 30-ks. See muudatus kajastub lingitud kontsernisisese ostutellimuse real.
- Kasutaja muudab kontsernisisese ostutellimuse rea planeerimis prioriteedi 40-st 50-ks. See muudatus kajastub lingitud kontsernisisese müügitellimuse real.
