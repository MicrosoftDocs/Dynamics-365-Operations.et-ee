---
title: "Hankija koostöö mobiilne tööruum"
description: "See teema annab teavet hankija koostöö mobiilse tööruumi kohta. See tööruum võimaldab hankijatel olla kursis ostutellimustega, mis on neile kinnitamiseks saadetud. Nad saavad vaadata teavet ka uute ja muudetud ostutellimuste ning kontaktide kohta."
author: mkirknel
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 267074
ms.assetid: 1d293b3a-2fa2-418d-9347-78c2809d67fe
ms.search.region: global
ms.author: mkirknel
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: 6028f6007cf2fd3f21c2e6cf3f5fac85c6e0da0a
ms.contentlocale: et-ee
ms.lasthandoff: 12/01/2017

---

# <a name="vendor-collaboration-mobile-workspace"></a>Hankija koostöö mobiilne tööruum

[!include[banner](../includes/banner.md)]

See teema annab teavet **hankija koostöö** mobiilse tööruumi kohta. See tööruum võimaldab hankijatel olla kursis ostutellimustega, mis on neile kinnitamiseks saadetud. Nad saavad vaadata teavet ka uute ja muudetud ostutellimuste ning kontaktide kohta.

See mobiilne tööruum on mõeldud kasutamiseks mobiilirakendusega Microsoft Dynamics 365 for Unified Operations.

## <a name="overview"></a>Ülevaade 
**Hankija koostöö** mobiilne tööruum teavitab hankijaid uutest ostutellimustest, et nad saaksid ostutellimusi rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition veebikliendis vaadata ja neile siis reageerida. 

>[!NOTE]
> Mobiilset tööruumi tuleb kasutada hankija koostöö veebiliidese lisana, kuid mitte selle asemel. 

Teie hankijad saavad kasutada **hankija koostöö** mobiilset tööruumi neile kinnitamiseks saadetud uute ostutellimuste vaatamiseks. See kuvab ostutellimuse teabe, nagu tooted, kogused ja nõutavad tarnekuupäevad. Hinnateave on samuti saadaval, olenevalt iga hankija konfiguratsioonist. 

Kasutaja, kes logib hankijana sisse, näeb, millistele ostutellimustele on vastatud ja millised ostutellimused ootavad endiselt kliendi tegevust. Näiteks võib ostutellimus oodata kliendi tegevust, kuna hankija soovitas teist tarnekuupäeva, kuid klient pole selle kuupäevaga veel nõustunud. Hankija näeb ka loendit ostutellimustest, mis on kinnitatud, kuid pole veel kohale toimetatud. 

Ostutellimusele vastamiseks peab hankija kasutama hankija koostöö veebiliidest, mis on saadaval veebikliendis. Seal saab hankija tellimuse kohta ka rohkem teavet, nagu dokumendimanused, tarneaadress rea kohta ja hankijaga seotud kulud. 

Spetsiaalse turberolliga hankijad saavad vaadata, millised kontaktisikud on hankijakonto jaoks registreeritud. Sama turberolliga saab hankija vaadata kasutaja edastatud taotluste olekut. 

Uute kontaktide loomiseks ja uute kasutajataotluste esitamiseks tuleb kasutada veebikliendi hankija koostöö veebiliidest. 

**Hankija koostöö** mobiilne tööruum võimaldab hankijal teha järgmisi toiminguid.

-   Vaadata hankijale saadetud uusi ostutellimusi.
-   Vaadata ostutellimusi, millele hankija on vastanud ja mis ootavad kliendipoolset tegevust.
-   Vaadata ostutellimusi, mis on kinnitatud, kuid mida pole veel täielikult vastu võetud.
-   Kuvada hankija kontole registreeritud kontaktisiku andmeid. (See toiming nõuab täiendavat turberolli.)
-   Kuvada teavet kasutaja taotluse kohta, mille hankija esitas, ja jälgida taotluse olekut. (See toiming nõuab täiendavat turberolli.)

## <a name="prerequisites"></a>Eeltingimused
Eeltingimused erinevad, olenevalt teie organisatsioonis juurutatud Microsoft Dynamics 365 versioonist.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Eeltingimused Microsoft Dynamics 365 for Finance and Operations, Enterprise Editioni kasutamisel 
Kui teie organisatsioonis on juurutatud Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, peab süsteemiadministraator avaldama **hankija koostöö** mobiilse tööruumi. Juhised leiate jaotisest [Mobiilse tööruumi avaldamine](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Eeltingimused Microsoft Dynamics 365 for Operationsi versiooni 1611 platvormivärskendusega 3 või uuema kasutamisel
Kui teie organisatsioonis on juurutatud Microsoft Dynamics 365 for Operationsi versioon 1611 platvormivärskendusega 3 või uuem, peab süsteemiadministraator täitma järgmised eeltingimused. 

<table>
<thead>
<tr class="header">
<th>Eeltingimus</th>
<th>Roll</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kui kasutate platvormivärskendust 3, tuleb juurutada KB 3216943.</td>
<td>Süsteemiadministraator</td>
<td>KB 3216943 on binaarne värskendus, mis on vajalik, kui kasutate platvormivärskendust 3. Selle KB juurutamiseks peab süsteemiadministraator tegema järgmist.
<ol>
<li>Laadima KB 3216943 alla Microsoft Dynamicsi elutsükliteenustest (LCS).</li>
<li>Installima binaarse värskenduse, mis toimetatakse kohale juurutatava paketina. Teavet juurutatava paketi kohta leiate jaotisest <a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Juurutatava paketi rakendamine</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Juurutatud peab olema KB 4013633.</td>
<td>Süsteemiadministraator</td>
<td>KB 4013633 on X++ värskendus või metaandmete kiirparandus, mis sisaldab mobiilset tööruumi <strong>Vaba kaubavaru</strong>. KB 4013633 juurutamiseks peab süsteemiadministraator toimima järgmiselt.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Metaandmete kiirparanduse allalaadimine LCS-ist</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installima metaandmete kiirparanduse</a>.</li><li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Looma juurutatava paketi</a>, mis sisaldab mudelit <strong>SCMMobile</strong>, ja seejärel laadima juurutatava paketi LCS-i üles.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Rakendage juurutatav pakett</a>.</li>
</ol></td>
</tr>
<tr class="odd">
<td><strong>Hankija koostöö</strong> mobiilne tööruum tuleb avaldada.</td><td>Süsteemiadministraator</td>
<td>Vt jaotist <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobiilse tööruumi avaldamine</a>.</td>
</tr>
<tr class="even">
<td>Hankija-kasutajal peab olema juurdepääs hankija koostöö veebiliidesele veebikliendis ja ta peab seadistama hankija koostöö kasutaja.</td><td>Ostuspetsialistid ja süsteemiadministraator</td>
<td>Järgige hankija koostöö veebiliidese seadistamiseks ja sellega töötamiseks järgmistes teemades antud juhiseid.
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">Hankija koostöö kasutamine väliste hankijatega töötamiseks</a></li>
<li><a href="manage-vendor-collaboration-users.md">Hankija koostöö kasutajate haldamine</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">Hankija koostöö seadistamine ja haldamine</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Hankija koostöö kasutamine klientidega töötamiseks rakenduses Finance and Operations</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Laadige alla ja installige mobiilirakendus

Laadige alla ja installige Dynamics 365 for Unified Operationsi mobiilirakendus.

-   [Androidi telefonidele](https://go.microsoft.com/fwlink/?linkid=850662)
-   [iPhone’idele](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Logige mobiilirakendusse sisse
1.  Käivitage rakendus oma mobiilses seadmes.
2.  Sisestage Microsoft Dynamics 365 URL.
4.  Esimesel sisselogimisel küsitakse teilt kasutajanime ja parooli. Sisestage oma identimisteave.
5.  Pärast sisselogimist kuvatakse teie ettevõtte jaoks saadaolevad tööruumid. Pange tähele, et teie süsteemiadministraator avaldab uue tööruumi hiljem ja teil on vaja mobiilsete tööruumide loendit uuendada.

    [![Tõmmake värskendamiseks](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="use-the-vendor-collaboration-mobile-workspace"></a>Hankija koostöö mobiilse tööruumi kasutamine
Kui valite **hankija koostöö** tööruumi, siis näete järgmisi valikuid.

![Hankija koostöö mobiilne tööruum](./media/vendor-collaboration-mobile-app.png)

**Hankija koostöö** tööruum sisaldab järgmisi lehti.

### <a name="contacts"></a>Kontaktid
Leht **Kontaktid** võimaldab teil näha kõiki kontakte, mis on hankija konto jaoks seadistatud. See kuvab kontaktisiku nime, peamise meiliaadressi ja kasutaja pseudonüümi, kui kontaktisikul on pseudonüüm. See leht näitab ka, kas kontaktisiku kasutajakonto on aktiivne. Kui valite kontakti, siis näete kontaktandmeid, nt juriidilisi isikuid, mille kontaktisik kasutaja on. Näete ka kontaktandmeid, nt telefoninumbrit või teist meiliaadressi.

### <a name="user-requests"></a>Kasutaja nõuded
Leht **Kasutaja taotlused** võimaldab teil näha kasutaja taotlusi, mille olete hankija koostöö veebiliidese kaudu edastanud. Saate ka nende taotluste olekut jälgida. Kasutajataotluse valimisel saate näha, mida taotleti, lisada või inaktiveerida kasutajat, muuta turvet ja näha, milliseid turberolle kasutajale taotleti.

### <a name="purchase-orders-ready-for-review"></a>Ülevaatamiseks valmis ostutellimused
Leht **Ülevaatamiseks valmis ostutellimused** võimaldab näha kõiki kliendi saadetud, kuid veel vastamata ostutellimusi. Saate vaadata tellimuse kohta valitud teavet, näiteks seda, milliseid tooteid taotleti ja millal need tooted tuleks kohale toimetada. Hinnateave on samuti saadaval, olenevalt hankija konfiguratsioonist.

Näete ka seda, kas ostutellimusel on märkusi või manuseid. Kuid märkuste ja manuste avamiseks tuleb kasutada veebikliendis hankija koostöö veebiliidest. Valige **Ostutellimuse rida**, et näha kõiki ridu koos nende üksikasjadega. Iga rea puhul kuvatakse tähis, mis näitab, kas on märkusi või manuseid või kas tarneaadress erineb päises näidatud tarneaadressist.

Ostutellimusele vastamiseks peate kasutama hankija koostöö veebiliidest veebikliendis.

### <a name="awaiting-customer-action"></a>Kliendi tegevuse ootel
Leht **Kliendi tegevuse ootel** võimaldab teil leida ostutellimusi, millele teie või keegi teine teie ettevõttes, kellel on juurdepääs hankija koostööle, on vastanud. Ostutellimused on selles loendis nähtavad ainult juhul, kui klient peab tegema ostutellimusel ühe järgmistest tegevustest.

-   Kui ostutellimus lükati tagasi, peab klient uuendama või tühistama algse tellimuse ja siis selle uuesti saatma. Kui ostutellimus saadetakse uuesti, ei kuvata seda enam lehel **Kliendi tegevuse ootel**.
-   Kui ostutellimus kinnitati muudatustega, peab klient algset tellimust uuendama ja saatma selle ülevaatamiseks uuesti või uuendama tellimust vastavalt muudatustele ja kinnitama selle siis kohe. Kummalgi juhul ei kuvata ostutellimust enam lehel **Kliendi tegevuse ootel**.
-   Kui ostutellimus kinnitati, aga see kuvatakse ikka lehel **Kliendi tegevuse ootel**, ei kinnitatud ostutellimust vastuvõtmisel automaatselt. See ootab nüüd, et ostuagent määraks tellimuse olekuks **Kinnitatud**. Tavaliselt käsitletakse ostutellimust kliendi ja hankija vahelise lepinguna kohe, kui hankija tellimuse kinnitab. Seetõttu on uuendamine olekusse **Kinnitatud** tavaliselt ainult formaalsus.

Kui valite ostutellimuse, kuvatakse vastuse kohta täiendavad üksikasjad. Saate näha rea üksikasju ja vastust iga rea kohta. Rea olek näitab, milline järgmistest vastustest on antud.

-   Aktsepteeritud
-   Tagasi lükatud
-   Aktsepteeritud koos muudatustega
-   Asendatud/asendaja
-   Tükeldamine graafikusse / graafiku rida

Pange tähele, et välja **Tarnimisel** olekuks määratakse **Jah** või **Ei**, et näidata, kas read tarnitakse. Rida ei pruugita tarnida järgmistel põhjustel.

- Rida lükati tagasi.
- Tehti asendus ja algse rea tarnimist saadud tellimuses ei oodata saadud tellimuse kohaselt.
- Rida jagati mitmeks graafikureaks ja algse rea tarnimist saadud tellimuses ei oodata saadud tellimuse kohaselt.

Kuvatakse tellimuse rea vastuses tehtud muudatused. Kuid üles laaditud märkusi ja manuseid ei kuvata. Märkuste ja manuste kuvamiseks tuleb kasutada veebikliendis hankija koostöö veebiliidest.

### <a name="open-confirmed-orders"></a>Avatud kinnitatud tellimused
Kui klient kinnitab ostutellimuse (st ostutellimuse olekuks määratakse **Kinnitatud**), kuvatakse see avatud kinnitatud tellimuses. See jääb loendisse, kuni registreeritakse, et klient on selle vastu võtnud.

