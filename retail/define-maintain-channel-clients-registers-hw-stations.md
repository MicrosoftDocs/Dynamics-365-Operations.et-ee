---
title: "Määratleda ja hallata kanali klientidele, registreid ja riistvara jaamad"
description: "See viki käsitleb välisseadmete ühendamist Retail POS-iga."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 92383
ms.assetid: 83f31ea6-f0a2-4501-9d4d-a37b6eec2599
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: dee5745670ad86000795f2913f99f49c0f123a00
ms.lasthandoff: 03/31/2017


---

# <a name="define-and-maintain-channel-clients-registers-and-hardware-stations"></a>Määratleda ja hallata kanali klientidele, registreid ja riistvara jaamad

See viki käsitleb välisseadmete ühendamist Retail POS-iga.

**Märkus.** Konkreetsed paigaldusjuhised leiate jaotistest [Jaemüügi riistvarajaama konfigureerimine ja installimine](retail-hardware-station-configuration-installation.md) ja [Retail Modern POS-i iseteeninduse allalaadimine/installimine ja Modern POS-i ning pilvekassa seadme aktiveerimine](retail-modern-pos-device-activation.md).

## <a name="key-components"></a>Põhikomponendid
Mitut komponenti kasutatakse seoste määratlemiseks kaupluse, kassaregistri või kaupluse kanalite ja jaemüügi välisseadmete hulgas, mida need registrid või kanalid kannete töötlemiseks kasutavad. Selles jaotises kirjeldatakse iga komponenti ja selgitatakse, kuidas seda tuleks jaekaupluse juurutuses kasutada.

### <a name="pos-registers"></a>Kassaregistrid

Navigeerimine: Klõpsake **hulgi- ja kaubanduse**&gt;**kanali seaded**&gt;**POS seadistus**&gt;**registreerib**. POS register on üksus, mis teil määratleda konkreetsete juhtude kohta tootjaorganisatsioonide omadused. Need omadused on riistvaraprofiili või setup jaemüügi välisseadmed, mida kasutatakse kasutaja sisse loginud, et registreerida registrisse, registri vastendatud laos ja visuaalne kogemus.

### <a name="devices"></a>Seadmed

Navigeerimine: Klõpsake **hulgi- ja kaubanduse**&gt;**kanali seaded**&gt;**POS seadistus**&gt;**seadmed**. Seade on üksus, mis kajastab kassaregistriga vastendatud seadme füüsilist eksemplari. Seadme loomisel vastendatakse see kassaregistriga. Seadmeüksus jälgib teavet selle kohta, millal kassaregister aktiveeritakse, kasutatava kliendi tüübi kohta ja rakenduse paketi kohta, mis on konkreetse seadme puhul juurutatud. Seadmed võivad olla kahte tüüpi: **Retail Modern POS** (MPOS) või **Retail Cloud POS** (pilvekassa).

#### <a name="mpos"></a>MPOS

MPOS on POS-i klientrakendus, mis on installitud operatsioonisüsteemi Windows 8.1 või uuemasse PC-põhisesse operatsioonisüsteemi. Kui rakenduse tüüp **Retail Modern POS** vastendatakse seadmega, saab konkreetsele seadmele määrata allalaadimispaketi. Allalaadimispaketti saab kohandada nii, et see sisaldaks installipaketi erinevaid versioone. Võimalus juurutada erinevaid pakette tagab paindlikkuse olukordades, kus erinevad kassaregistrid võivad nõuda erinevaid integratsioone. MPOS juurutatakse koos integreeritud riistvarajaamaga.

#### <a name="cloud-pos"></a>Cloud POS

POS pilv on veebipõhine POS. Sest see töötab brauser, pilve POS ei nõua Windows 8.1 või uuem PC-põhine operatsioonisüsteem. Kui rakenduse tüüp **Retail Cloud POS** vastendatakse varukontoris konkreetse seadmega, saab seda seadet kasutada brauseri kaudu, ilma et oleks vaja paketti alla laadida või installida. Cloud POS nõuab riistvarajaama, et kasutada riistvara üle klaviatuurikiilul põhineva vöötkoodi skannimise.

### <a name="hardware-profile"></a>Riistvaraprofiil

Navigeerimine: Klõpsake **kaubanduse**&gt;**kanali seaded**&gt;**POS seadistus**&gt;**POS profiilid**&gt;**riistvara profiilid**. Riistvaraprofiil tähistab riistvara, mis on ühendatud kassaregistri või riistvarajaamaga. Riistvaraprofiili abil määratakse ka makseprotsessori parameetrid, mida tuleb maksetarkvara arenduskomplektiga (SDK) suhtlemisel kasutada. (Makse SDK juurutatakse riistvarajaama osana.)

### <a name="hardware-station"></a>Riistvarajaam

Navigeerimine: Klõpsake **hulgi- ja kaubanduse**&gt;**kanalite**&gt;**kauplustes**&gt;**kõik kauplustes**. Valige kauplus ja klõpsake siis kiirkaarti **Riistvarajaamad**. Riistvarajaam on äriloogika eksemplar, mis juhib kassa välisseadmeid. Riistvarajaam paigaldatakse automaatselt koos MPOS-iga. Teine võimalus on paigaldada riistvarajaam eraldi komponendina ja kasutada seda siis MPOS-i või Cloud POS-i jaoks veebiteenuse kaudu. Riistvarajaam tuleb määratleda kanali tasemel.

### <a name="hardware-station-profile"></a>Riistvarajaama profiil

Navigeerimine: Klõpsake **kaubanduse**&gt;**kanali seaded**&gt;**POS seadistus**&gt;**POS profiilid**&gt;**riistvara station profiilid**. Kui kanali tasemel määratletud riistvarajaam ise sisaldab eksemplaripõhist teavet nagu riistvarajaama URL, sisaldab riistvarajaama profiil teavet, mis võib olla staatiline või mida võidakse jagada mitme riistvarajaama vahel. Staatiline teave sisaldab porti, mida tuleks kasutada, riistvarajaama paketti ja riistvaraprofiili. Staatiline teave sisaldab ka juurutatava riistvarajaama tüübi kirjeldust (nt **Maksmine ** või **Tagastused**), olenevalt riistvarast, mida iga konkreetse riistvarajaama puhul vaja on.

## <a name="scenarios"></a>Stsenaariumid
### <a name="mpos-with-connected-peripheral-devices"></a>Ühendatud välisseadmetega MPOS

[![Traditsioonilised, fikseeritud Müügikoht](./media/traditional-300x279.png)](./media/traditional.png) MPOS ühendamiseks POS välisseadmete traditsioonilised, fikseeritud POS stsenaariumi esmalt Navigeerige ise registrisse ja riistvara profiili määramiseks. Leiad POS registrite kell **hulgi- ja kaubanduse**&gt;**kanali seaded**&gt;**POS seadistus**&gt;**registreerib**. Kui olete riistvaraprofiili määranud, sünkroonige muudatused kanali andmebaasis, kasutades jaotusgraafikut Registrid. Leiad distribution plaanid kell **hulgi- ja kaubanduse**&gt;**jaemüügi see**&gt;**jaotus ajakava**. Järgmisena seadistage kanalil „kohalik” riistvarajaam. Klõpsake **hulgi- ja kaubanduse**&gt;**kanalite**&gt;**kauplustes**&gt;**kõik kauplustes**, ja valida pood. Seejärel klõpsake kiirkaardil **Riistvarajaamad** käsku **Lisa** riistvarajaama lisamiseks. Sisestage kirjeldus, sisestage hosti nimeks **localhost** ja sünkroonige siis kanali muudatused, kasutades jaotusgraafikut Kanali konfigureerimine. Leiad distribution plaanid kell **hulgi- ja kaubanduse**&gt;**jaemüügi see**&gt;**jaotus ajakava**. Lõpuks kasutage MPOS-is toimingut **Riistvarajaama valimine** riistvarajaama **localhost** valimiseks. Määrake riistvarajaama olekuks **Aktiivne**. Selles stsenaariumis kasutatav riistvaraprofiil peaks pärinema kassaregistrist enesest. Selle stsenaariumi puhul pole riistvarajaama profiil vajalik. **Märkus.** Mõned riistvaraprofiili muudatused (nt kassasahtlite vahetused) nõuavad uue vahetuse avamist pärast muudatuste sünkroonimist kanaliga. **Märkus.** Cloud POS peab kasutama jaemüügi välisseadmetega suhtlemiseks eraldiseisvat riistvarajaama.

### <a name="mpos-or-cloud-pos-with-a-stand-alone-hardware-station"></a>MPOS või Cloud POS koos eraldi riistvarajaamaga

\[caption id = "manuse\_340041" viia = "alignleft" width = "300"\][![jagatud välisseadmete](./media/shared-300x254.png)](./media/shared.png) jagatud välisseadmete\[/caption\] sel puhul jagatakse eraldi riistvara station MPOS ja pilve POS klientide hulgas. See stsenaarium nõuab riistvarajaama profiili loomist allalaadimispaketi, pordi ja riistvaraprofiili määramiseks, mida riistvarajaam kasutab. Leiad station riistvaraprofiili kell **hulgi- ja kaubanduse**&gt;**kanali seaded**&gt;**POS seadistus**&gt;**POS profiilid**&gt;**riistvara station profiilid**. Pärast riistvara station profiili loomist liikuge konkreetseid kanal (**hulgi- ja kaubanduse**&gt;**kanalite**&gt;**kauplustes**&gt;**kõik kauplustes**), ja lisada uusi riistvara station. Vastendage see uus riistvarajaam varem loodud riistvarajaama profiiliga. Järgmiseks sisestage kirjeldus, mis aitab kassiiril riistvarajaama tuvastada. Aastal ning **hosti nimi** vastuvõtva masin URL sisestage järgmises vormingus: **https://&lt;MachineName:Port&gt;/HardwareStation**. (Asendada **&lt;MachineName:Port&gt;** koos tegelik nimi riistvara station ja määratud riistvaraprofiili station port.) Eraldi riistvara jaama te täpsustama ka elektroonilise rahaülekande (EFT) terminali ID-d. See väärtus tähistab EFT terminali, mis on riistvarajaamaga ühendatud, kui makseühendus maksepakkujaga suhtleb. Järgmiseks minge tegelikust riistvarajaamast kanali juurde ja valige riistvarajaam. Siis klõpsake valikut **Allalaadimine** ja installige riistvarajaam. Järgmiseks kasutage MPOS-i või Cloud POS-i toimingut **Riistvarajaama valimine** varem installitud riistvarajaama valimiseks. Valige **Seo** turvalise seose loomiseks kassa ja riistvarajaama vahel. See toiming tuleb teha iga kassa ja riistvarajaama kombinatsiooni puhul üks kord. Pärast riistvarajaama sidumist kasutatakse sama toimingut riistvarajaama aktiveerimiseks selle kasutamise ajal. Selle stsenaariumi puhul tuleks määrata riistvaraprofiili riistvaraprofiili station, mitte ise registrisse. Kui mingil põhjusel ei ole riistvara station otse määratud riistvaraprofiili, seejärel registri määratud riistvaraprofiili kasutatakse

## <a name="client-maintenance"></a>Kliendi hooldus
### <a name="registers"></a>Registrid

Kassaregistreid hallatakse peamiselt registrite endi kaudu ning samuti registritele määratud profiilide kaudu. Konkreetse eraldi registri põhiseid atribuute hallatakse registri tasandil. Need atribuudid hõlmavad kauplust, kus registrit kasutatakse, registri numbrit, kirjeldust ja EFT terminali ID-d, mis on registri enese põhine.

### <a name="pos-profiles"></a>Kassa profiilid

Leiad POS profiilid kell **hulgi- ja kaubanduse**&gt;**kanali seaded**&gt;**POS seadistus**&gt;**POS profiilid**. Paljusid registri aspekte tasub hallata profiilide kaudu, kuna profiile saab paljude registrite vahel jagada. Profiile saab vastendada eraldi registriga või, kui profiil kehtib üle kogu kaupluse, siis jaekauplusega. Järgmistes punktides kirjeldatakse kassaprofiile ja nende kasutamist.

#### <a name="offline-profile"></a>Ühendusväline profiil

Ühenduseta profiil määratakse kaupluse tasandil. Seda kasutatakse kassaregistris tehtavate kannete üleslaadimissätete määramiseks, kui see register pole kanali andmebaasiga ühendatud.

#### <a name="functionality-profile"></a>Funktsiooniprofiil

Funktsiooni profiil määratakse kaupluse tasandil. Seda kasutatakse kell tootjaorganisatsioonid sooritatavate funktsioonide kohta poe hõlmavate sätete määramiseks. Funktsiooni profiili kaudu hallatakse järgmisi võimalusi. Need võimalused on paigutatud kiirkaardi abil.

-   Kiirkaart **Üldine**.
    -   Rahvusvaheline Standardiorganisatsioon (ISO).
    -   Kliendi loomine ühenduseta režiimis.
    -   Meilikviitungi profiil.
    -   Keskne personali sisselogimise autentimine.
-   Kiirkaart **Funktsioonid**.
    -   Sisselogimise ja laiendatud sisselogimise haldamine.
    -   Kassa rahalised ja valuutaga seotud aspektid, nt võimalus sisestada hindu ja see, kas peenraha puhul on kümnendkohad nõutavad.
    -   Aja registreerimine kassa kaudu.
    -   Toodete ja maksete kuvamise viis kassas ja kviitungitel.
    -   Päeva lõpetamise haldamine.
    -   Kanali andmebaasi kande säilitamise parameetrid.
    -   Klientide otsimise ja loomise viis kassast.
    -   Allahindluste arvutamise viis.
-   Kiirkaart **Summa**.
    -   Lubatud maksimum- ja miinimumhinnad.
    -   Allahindluse rakendamine ja arvutamine.
-   Kiirkaart **Teabekoodid**.
    -   Kuidas info koodide tootjaorganisatsioonid hallatakse kõiki aspekte. Täpsemalt vaata [Info koodide](info-codes-retail.md).
-   Kiirkaart **Kviitungi nummerdamine**.
    -   Saate määrata kviitungite nummerdamise maskid, mis võivad sisaldada segmente kaupluse numbri, terminali numbri, konstantide jaoks ning seda, kas müük, tagastused, müügitellimused ja hinnapakkumised prinditakse eraldi seeriatena või kas nad kõik põhinevad ühel seerial.

#### <a name="receipt-profiles"></a>Kviitungi profiilid

Kviitungite profiilid määratakse printeritele riistvaraprofiilis. Neid kasutatakse konkreetsest printerist prinditavate kviitungitüüpide määramiseks. Profiilid hõlmavad kviitungivormingute sätteid ja sätteid, mis määravad, kas kviitung prinditakse alati või küsitakse kassiirilt, kas kviitung tuleb printida. Erinevates printerites võidakse samuti kasutada erinevaid kviitungiprofiile. Näiteks 1. printer on tavaline termopaberiga kviitungiprinter ja seetõttu on selle kviitungivormingud väiksemad. Kuid 2. printer on täissuuruses kviitungiprinter, mida kasutatakse ainult klienditellimuste kviitungite printimiseks, mis nõuavad rohkem ruumi.

#### <a name="hardware-profiles"></a>Riistvara profiilid

Riistvaraprofiile selgitatakse kliendi seadistuse komponendina selles artiklis eespool. Riistvaraprofiilid määratakse otse kassaregistrile või riistvarajaama profiilile. Neid kasutatakse seadmetüüpide määramiseks, mida konkreetne kassaregister või riistvarajaam kasutab. Riistvaraprofiilide abil määratakse ka makse SDK-ga suhtlemiseks kasutatavad EFT sätted.

#### <a name="visual-profiles"></a>Visuaalsed profiilid

Visuaalsed profiilid määratakse registri tasandil. Neid kasutatakse konkreetse registri kujunduse määramiseks. Profiilid hõlmavad kasutatava rakenduse tüübi sätteid (MPOS või Cloud POS), rõhuvärvi ja kujundust, fondiskeemi, sisselogimise tausta ja kassa tausta.

### <a name="custom-fields"></a>Kohandatud väljad

Saate luua kohandatud välju lisada välju, mis ei ole karbist tootjaorganisatsioonid. Kohandatud väljade kasutamise kohta lisateabe saamiseks vt ka [kohandatud välju blogi postitus töötamine](https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/).

### <a name="language-text"></a>Keeletekst

Saate kassas keele tekstisisestuse abil vaikestringe alistada. Stringi alistamiseks kassas lisage uus keele tekstirida. Seejärel määrake ID, vaikestring, mis tuleks alistada, ja tekst, mis tuleks vaikestringi asemel kassas kuvada.

### <a name="hardware-station-profiles"></a>Riistvarajaama profiilid

Riistvarajaama profiile selgitatakse selles artiklis eespool. Neid kasutatakse mitte-eksemplaripõhise teabe määramiseks riistvarajaamadele.

### <a name="channel-reports-configuration"></a>Kanali aruannete konfiguratsioon

Jaemüügikanalis saadaolevaid aruandeid saate seadistada lehel **Jaemüügikanali aruannete konfiguratsioon**. Saate luua uusi aruandeid, sisestades aruande XML-määratluse ja määrates aruande kassa konkreetsele õiguste grupile.

### <a name="devices"></a>Seadmed

Seadmeid selgitatakse selles artiklis eespool. Neid kasutatakse konkreetse kassaregistri aktiveerimise haldamiseks. Seadmeid kasutatakse ka konkreetse registri jaoks kasutatava rakenduse ja MPOS-i kliendi installimiseks kasutatava installipaketi määramiseks. Siin on seadme aktiveerimise olekud.

-   **Ootel** – seade on aktiveerimiseks valmis.
-   **Aktiveeritud** – seade on aktiveeritud.
-   **Inaktiveeritud** – seade on kontoris või kassa kaudu inaktiveeritud.
-   **Keelatud** – seade on keelatud.

Aktiveerimist puudutav lisateave hõlmab töötajat, kes seadme aktiveerimisolekut muutis, aktiveerimise ajatemplit ja seda, kas seadme konfiguratsioon on kinnitatud.

### <a name="client-data-synchronization"></a>Kliendi andmete sünkroonimine

Kõik kassa kliendi muudatused, v.a seadme aktiveerimisoleku muudatused, tuleb nende jõustumiseks kanali andmebaasiga sünkroonida. Kanali andmebaasi muudatusi sünkroonida, liikuge **hulgi- ja kaubanduse**&gt;**jaemüügi see**&gt;**jaotus ajakava**, ja käivitage nõutavaks levitamiseks ajakava. Kliendi muudatuste puhul tuleks käivitada jaotusgraafikud Registrid ja Kanali konfiguratsioon.


