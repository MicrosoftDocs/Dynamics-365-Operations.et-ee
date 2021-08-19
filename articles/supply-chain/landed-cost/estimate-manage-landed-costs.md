---
title: Väljalaadimiskulude hindamine ja haldamine
description: Süsteem kasutab väljalaadimiskulude hinnangu määratlemiseks teie automaatset kuluhäälestust. Selles teemas selgitatakse, kuidas saate täpsema prognoosi andmiseks määratleda erinevaid stsenaariumeid.
author: sherry-zheng
ms.date: 01/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMCostTemplateTable, ITM CostEstimateDialog, ITMCostEstimateTable, SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-26
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: a30c1efd2fa37a5fb192156ab6edf1d57be8cad36c781f236385fc6884bda097
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736691"
---
# <a name="estimate-and-manage-landed-costs"></a>Väljalaadimiskulude hindamine ja haldamine

[!include [banner](../../includes/banner.md)]

Süsteem kasutab väljalaadimiskulude hinnangu määratlemiseks teie [automaatset kuluhäälestust](auto-cost-setup.md). Lisaks saate täpsema prognoosi andmiseks määratleda erinevaid stsenaariumeid. Need stsenaariumid salvestatakse. Seetõttu saate need hiljem üle vaadata ja võrrelda neid aruande tegelike andmetega. Samuti saate kauba hinda värskendada.

## <a name="set-up-cost-estimates"></a>Kuluhinnangute häälestamine

### <a name="set-up-cost-templates"></a>Saate häälestada kulumalle.

Kulumallidega pannakse paika vaikesätted, mida hinnangu saavad kasutajad ei pruugi tingimata teada. Mallid aitavad vähendada hindamisprotsessi keerukust, minimeerides valikud, mille kasutajad peavad täpse prognoosi saamiseks määrama. Kui kasutate standardsed kulumudelit, saate kaupade maksumuse häälestamisel kasutada kulumalle.

Kulumallide häälestamiseks valige **Väljalaadimiskulu \> Kuluarvutuse häälestamine \> Kulumallid**. Lehel **Kulumallid** on vasakpoolsel loendipaanil kuvatud kõik praegused kulumallid. Toimingupaani nuppude abil saate malle luua, kustutada ja redigeerida.

Järgmises tabelis kirjeldatakse iga malli jaoks saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Kulumall | Sisestage kulumalli kordumatu nimi. Nimi kirjeldab tavaliselt malli tegurit või kulu kordajat. |
| Kirjeldus | Sisestage kulumalli kirjeldus. |
| Saatmisettevõte | Valige saatmisettevõte, mis tuleks malli kasutamisel rakendada. |
| Tarneviis | Valige tarneviis (nt mere- või õhutransport), mis tuleks malli kasutamisel rakendada. See väli aitab määratleda kuluhinnangus kaupadega seostatud automaatsed kulud. |
| Saatmiskonteineri tüüp | Valige saatmiskonteineri tüüp, mis tuleks malli kasutamisel rakendada. See väli aitab määratleda kuluhinnangus kaupadega seostatud automaatsed kulud. |
| Tollimaakler | Tollimaakler (hankija), mis tuleks malli kasutamisel rakendada. See väli aitab määratleda kuluhinnanguga seostatud automaatsed kulud. |
| Tegur | Sisestage kordaja (protsent), mis tuleks malli kasutamisel automaatselt kuluhinnangule rakendada. Näiteks arvutatud kuluhinnangule 10 protsendi lisamiseks sisestage *1,10*. |

### <a name="create-a-cost-estimate"></a>Kuluhinnangu loomine

Dialoogiboksis **Kuluhinnang** saate genereerida uue kuluhinnangu, mis põhineb valitud kulumallil, valitud kaubakomplektil ja muudel teekonna üksikasjadel. Neid sätteid kasutatakse seejärel kaupade hinnanguliste väljalaadimiskulude määratlemiseks. Neid kuluhinnanguid kasutatakse peamiselt standardkuluga kaupadega töötamiseks. Kui lisate hinnangulised väljalaadimiskulud laos olevate kaupade standardkulule, peaksite kaupade lisamisel teekonnale kogema väiksema hälbega kandeid, kuna standardkulu kajastab nende väljalaadimiskulude hinnanguid.

Dialoogiboksi **Kuluhinnang** avamiseks valige **Väljalaadimiskulu \> Perioodilised ülesanded \> Kuluhinnang**. Seejärel häälestage järgmistes alljaotistes kirjeldatud väljad. Lõpuks valige hinnangu loomiseks **OK**. Seejärel kuvatakse leht **Kuluhinnang** (**Väljalaadimiskulu \> Päringud \> Kuluhinnangud**), kus on kuvatud teie uus hinnang, seda on lähemalt kirjeldatud selles teemas allpool.

### <a name="settings-on-the-parameters-tab"></a>Sätted vahekaardil Parameetrid

Järgmises tabelis kirjeldatakse dialoogiboksi **Kuluhinnang** vahekaardil **Parameetrid** asuvaid välju.


| Field | Kirjeldus |
|---|---|
| Kulumall | Valige kulumall. Valitud malliga seostatud sätteid kasutatakse rakendatud automaatsete kulude määratlemiseks. |
| Prognoosi kuupäeva | Vaikimisi on selle välja väärtuseks seatud tänane kuupäev, kuid väärtust saate muuta. Määratud kuupäeva kasutatakse asjakohaste müügihindade, ostuhindade, automaatsete kulude ja vahetuskursi valimiseks, kui kasutatakse tarnemäära. |
| Mõõtmine | Kulud võivad sõltuda mõnest mõõdust. Õhutranspordi kasutamise korral võib kehtida näiteks mahupõhine hinnakujundus. Kui kulu sõltub mõnest mõõdust, sisestage selle mõõdu väärtus. Muul juhul soovitame seada selle välja väärtuseks *1*, välja arvatud juhul, kui olete kindel, et mõõtude põhjal ei toimu jaotamisi. Sisestage kümnendväärtus. Kasutatav mõõtühik on määratletud rakendatavas automaatsete kulude kirjes. |
| Teekonna mall | Valige [teekonna mall](multi-leg-journey-setup.md). Seda välja kasutatakse õigete rakendatavate automaatsete kulude määratlemiseks. |
| Lähtesadam | Sadam, kust kaubad teele saadetakse. Selle välja väärtus määratakse valitud teekonnamalli põhjal. |
| Sihtsadam | Sadam, kuhu kaubad saadetakse. Selle välja väärtus määratakse valitud teekonnamalli põhjal. |
| Currency | Valige kaupade ostmiseks kasutatav valuuta. |
| Konteinerid | Kui tavaliselt kasutatakse mitut konteinerit, määrake konteinerite arv. Seejärel kasutab süsteem hinnanguliste kulude arvutamisel mitme konteineri kulusid. |
| Fooliod | Kui tavaliselt kasutatakse mitut fooliot, määrake kogus. (Kogus on enamasti *1*.) |
| Laoala | Määrake koht, kuhu kaup tarnitakse. |

### <a name="settings-on-the-items-tab"></a>Sätted vahekaardil Kaubad

Vahekaardil **Kaubad** saate hinnangusse lisada nii palju üksusi, kui vaja. Kaupade lisamiseks ruudustikku või kaupade eemaldamiseks kasutage tööriistariba. Valige tööriistaribal **Varud \> Kuva dimensioonid**, et avada dialoogiboks, kus saate dimensiooniveerge ruudustikku lisada või veerge eemaldada.

Järgmises tabelis kirjeldatakse iga kauba jaoks saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Kaubakood | Valige kaup, mille jaoks hind määratleda. (Kui süsteemis pole kaupa veel olemas, looge fiktiivne kaup, lisage see soovi korral teekonna kauba kulugrupile ja jätke siis hind tühjaks, looge uus hind või muutke hinda.) |
| Hankija konto | Valige selle kauba hinnangu jaoks kasutatav hankija. Kui kaubale on määratud vaikehankija, määratakse see väli automaatselt. |
| Kogus | Valige kogus, mille kavatsete osta. |
| Omahind | Süsteem kasutab alghinna leidmiseks hinnakujunduse reegleid, kuid vajadusel saate selle hinna alistada. |
| Müügihind | Sisestage kauba eeldatav müügihind. |
| Mõõtmine | Sisestage kaupade mõõdu kümnendväärtus. Mõõtühik on sama, mis on häälestatud asjakohase vabastatud toote jaoks. |
| Uuenda kauba kaalu/mahtu | Märkige see ruut, et uuendada vabastatud toote kaalu- või mahumõõtu nii, et see vastaks selle rea jaoks sisestatud väärtusele **Mõõt**. |
| (Muud dimensioonid) | Sõltuvalt sellest, milliste dimensioonide kuvamise olete valinud, võite iga kauba kohta näha ka täiendavaid teabeveerge. |

Kauba mahu ja/või kaalu üksikasjade vaatamiseks või korrigeerimiseks valige kaup ruudustikust ja kasutage seejärel lehekülje allosas asuvaid välju.

## <a name="manage-estimated-costs"></a>Hinnanguliste kulude haldamine

Loodud kuluhinnangute vaatamiseks ja redigeerimiseks valige **Väljalaadimiskulu \> Päringud \> Kuluhinnangud**. Lehel **Kuluhinnangud** on vasakpoolsel loendipaanil kuvatud kõik praegused kuluhinnangud. Valitud hinnanguga saate töötada toimingupaani nuppude abil. Võtke arvesse, et te ei saa lehel **Kuluhinnangud** uut kuluhinnangut luua. Kasutage selle asemel dialoogiboksi **Kuluhinnang** (**Väljalaadimiskulu \> Perioodilised ülesanded \> Kuluhinnang**), nagu käesolevas teemas eespool kirjeldatud.

Lehel **Kuluhinnangud** on kuvatud iga hinnangulise kulu tuletamise viis. Samuti kuvatakse selles iga kauba hinnanguline väljalaadimiskulu. Kuluhinnangu muutmiseks saate muuta mitmesuguste kaupadega seostatud omahinda ja/või valuutat. Samuti saate muuta seostuvaid teekonnakulusid nii teekonna tasemel kui ka konteineri tasemel. Kui kasutate seda lehte kulude muutmiseks, palutakse teil kuluhinnangusse kaasatud kaupade hinnangulised kulud ümber arvutada. Kui olete valmis, saate hinnanguid kasutada kaupade omahinna uuendamiseks kulumallis.

### <a name="information-on-the-header"></a>Teave päises

Lehe **Kuluhinnangud** ülaosas kuvatakse sätted, mida kasutati valitud kuluhinnangu genereerimiseks, nagu kirjeldatud eelmises jaotises. 

### <a name="settings-and-buttons-on-the-lines-fasttab"></a>Kiirkaardi Read sätted ja nupud

Kiirkaardil **Read** loetletakse kõik praegusesse hinnangusse kaasatud kaubad. Järgmises tabelis kirjeldatakse iga real jaoks saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Hankija konto | Kaubaga seotud hankijakonto. |
| Kaubakood | Kaubakood. |
| Kogus | Kaupade arv, mida kasutatakse kulu määramiseks. |
| Omahind | Omahind vastavalt kaubandusleppele. See väärtus kuvatakse kohalikus valuutas. |
| Mõõtmine | Üksikmõõtmine. Mõõtühik on sama, mis on määratletud asjakohase vabastatud toote jaoks. |
| Eeldatavad väljalaadimiskulud | Kogukoguse hinnanguline väljalaadimiskulu. |
| Ühiku kohta | Hinnanguline väljalaadimiskulu jagatud kogusega. |
| (Muud dimensioonid) | Sõltuvalt sellest, milliste dimensioonide kuvamise olete valinud, võite iga kauba kohta näha ka täiendavaid teabeveerge. |

Järgmises tabelis kirjeldatakse kiirkaardi **Read** tööriistaribal olevaid nuppe.

| Nupp | Kirjeldus |
|---|---|
| Lisamine | Saate kaupu kuluhinnangusse lisada. Pärast kaupade lisamist peate toimingupaanil valima **Arvuta uuesti**. |
| Eemaldamine | Saate kaupu kuluhinnangust eemaldada. Pärast kaupade eemaldamist peate toimingupaanil valima **Arvuta uuesti**. |
| Reisikulud | Avatakse leht, kus saate vaadata ja redigeerida mitmesuguseid kaubaga seotud teekonnakulusid. |
| Varud \> Kuva dimensioonid | Avatakse dialoogiboks, kus saate dimensiooniveerge ruudustikku lisada või veerge eemaldada. |

### <a name="settings-on-the-general-fasttab"></a>Kiirkaardi Üldine sätted

Kiirkaardil **Üldine** kuvatakse praegu kiirkaardil **Read** valitud kauba üksikasjad. Suur osa sellest teabest kordub kiirkaardil **Read** ja seda saab redigeerida ükskõik kummas kohas. Siiski on siin saadaval ka täiendavad üksikasjad. Lisaväljade väärtused põhinevad asjakohase väljastatud toote häälestusel.

### <a name="settings-on-the-dimension-fasttab"></a>Kiirkaardi Dimensioon sätted

Kiirkaardil **Dimensioon** kuvatakse kõigi kiirkaardil **Read** valitud kauba jaoks saadaolevate varude dimensioonide väärtused olenemata sellest, millised dimensioonid olete seal kuvamiseks valinud. Kõik siin kuvatavad väärtused pärinevad asjakohasest kuluhinnangumallist. Kuluhinnangumallis on need valikulised.

### <a name="buttons-on-the-action-pane"></a>Toimingupaani nupud

Lehe **Kuluhinnangud** toimingupaani nuppe saate kasutada valitud kuluhinnanguga töötamiseks. Järgmises tabelis on saadaolevaid nuppe lähemalt kirjeldatud.

| Tegevus | Kirjeldus |
|---|---|
| Kulupäring | Kuvatakse kõik teekonna kulud. Kulusid saate vastavalt vajadusele vaadata üksiku kauba tasemel. |
| Uuenda standardkulu | <p>Standardkulu uuendamiseks saate kasutada kuluarvutuse vaikeversiooni, mis on määratletud lehel **Väljalaadimiskulu parameetrid**. Selle versiooni saate alistada.</p><p>**Märkus.** Kui kaubal on mitu kaubadimensiooni (nt erinevad suurused, värvid ja konfiguratsioonid), kuid neid dimensioone pole hinnangu jaoks valitud, loob süsteem iga kombinatsiooni jaoks ootel hinna.</p><p>**NB!** Luuakse hinnajaotus, mida kasutatakse standardkulu hälbe määratlemiseks väljalaadimiskulu kohta.</p> |
| Reisikulud | Siin saate vaadata ja redigeerida saadetise kõigi kaupade teekonnakulusid. |
| Arvuta uuesti | Pärast teekonnakulude värskendamist, lisamist või eemaldamist saate hinnangulised väljalaadimiskulud uuendada. |
| Lukusta | Saate kuluhinnangukirje lukustada, et rohkem muudatusi ei saaks teha. |

## <a name="item-cost-price-update"></a>Kauba omahinna uuendus

Perioodiline ülesanne **Kauba omahinna uuendus** uuendab kõik kuluhinnangud, mis vastavad ülesande käivitamisel teie poolt määratud filtritele. Selle töö mõju sarnaneb ühe hinnangu korral toimingupaanil käsu **Standardkulu värskendamine** valimisega. Käesoleval juhul uuendatakse aga kõik filtritele vastavad hinnangud.

Perioodilise ülesande käivitamiseks täitke järgmised juhised.

1. Valige **Väljalaadimiskulu \> Perioodilised ülesanded \> Kauba omahinna uuendus**.
1. Dialoogiboksis **Omahinna uuendamine hinnangu põhjal** määrake uuenduse ulatuse piiritlemiseks järgmised väljad.

    - **Versioon** – uuendatakse ainult määratud kuluarvutuse versiooni kasutavad hinnangud.
    - **Koht** – uuendatakse ainult määratud kohta kasutavad hinnangud.
    - **Kulumall** – uuendatakse ainult määratud malli kasutavad hinnangud.
    - **Sihtsadam** – uuendatakse ainult määratud sihtsadamat kasutavad hinnangud.
    - **Hinnangu kuupäev** – uuendatakse ainult määratud kuupäevaga hinnangud.

1. Määrake kiirkaartide **Kaasatavad kirjed** ja **Käivita taustal** käsud nii, nagu perioodiliste ülesannete jaoks ikka.
1. Ülesande käivitamiseks valige **OK**.

> [!NOTE]
> Selle perioodilise ülesande käitamine õnnestub üksnes juhul, kui saadaval on järgmine teave.
>
> - **Kogumaht**, **Kogulaius** ja **Kogukõrgus** peavad olema määratud iga asjakohase toote jaoks.
> - Iga asjakohase hankija jaoks peab **Lähtesadam** olema määratud.
