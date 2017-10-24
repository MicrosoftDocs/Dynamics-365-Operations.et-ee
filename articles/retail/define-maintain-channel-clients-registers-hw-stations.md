---
title: "Kanaliklientide, registrite ja riistvarajaamade määratlemine ning haldamine"
description: "See teema käsitleb välisseadmete ühendamist Retail POS-iga."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 92383
ms.assetid: 83f31ea6-f0a2-4501-9d4d-a37b6eec2599
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f87293a105caf9327183e170aebd6978ffbd4a74
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="define-and-maintain-channel-clients-registers-and-hardware-stations"></a>Kanaliklientide, registrite ja riistvarajaamade määratlemine ning haldamine

[!include[banner](includes/banner.md)]


See teema käsitleb välisseadmete ühendamist Retail POS-iga.

**Märkus.** Konkreetsed paigaldusjuhised leiate jaotistest [Jaemüügi riistvarajaama konfigureerimine ja installimine](retail-hardware-station-configuration-installation.md) ja [Retail Modern POS-i iseteeninduse allalaadimine/installimine ja Modern POS-i ning pilvekassa seadme aktiveerimine](retail-modern-pos-device-activation.md).

## <a name="key-components"></a>Põhikomponendid
Mitut komponenti kasutatakse seoste määratlemiseks kaupluse, kassaregistri või kaupluse kanalite ja jaemüügi välisseadmete hulgas, mida need registrid või kanalid kannete töötlemiseks kasutavad. Selles jaotises kirjeldatakse iga komponenti ja selgitatakse, kuidas seda tuleks jaekaupluse juurutuses kasutada.

### <a name="pos-registers"></a>Kassaregistrid

Navigeerimine: klõpsake valikuid **Jaemüük** &gt; **Kanali häälestus** &gt; **Kassa häälestus** &gt; **Registrid**. Kassaregister on olem, mida kasutatakse kassa konkreetse eksemplari omaduste määratlemiseks. Nende omaduste hulka kuuluvad riistvaraprofiil või jaemüügi välisseadmed, mida registris kasutatakse, kauplus, millega register on vastendatud, ja sellesse registrisse sisse logiva kasutaja visuaalne kogemus.

### <a name="devices"></a>Seadmed

Navigeerimine: klõpsake valikuid **Jaemüük** &gt; **Kanali häälestus** &gt; **Kassa häälestus** &gt; **Seadmed**. Seade on üksus, mis kajastab kassaregistriga vastendatud seadme füüsilist eksemplari. Seadme loomisel vastendatakse see kassaregistriga. Seadmeüksus jälgib teavet selle kohta, millal kassaregister aktiveeritakse, kasutatava kliendi tüübi kohta ja rakenduse paketi kohta, mis on konkreetse seadme puhul juurutatud. Seadmed võivad olla kahte tüüpi: **Retail Modern POS** (MPOS) või **Retail Cloud POS** (pilvekassa).

#### <a name="mpos"></a>MPOS

MPOS on POS-i klientrakendus, mis on installitud operatsioonisüsteemi Windows 8.1 või uuemasse PC-põhisesse operatsioonisüsteemi. Kui rakenduse tüüp **Retail Modern POS** vastendatakse seadmega, saab konkreetsele seadmele määrata allalaadimispaketi. Allalaadimispaketti saab kohandada nii, et see sisaldaks installipaketi erinevaid versioone. Võimalus juurutada erinevaid pakette tagab paindlikkuse olukordades, kus erinevad kassaregistrid võivad nõuda erinevaid integratsioone. MPOS juurutatakse koos integreeritud riistvarajaamaga.

#### <a name="cloud-pos"></a>Cloud POS

Cloud POS on brauseripõhine kassa. Kuna see töötab brauseris, ei nõua Cloud POS operatsioonisüsteemi Windows 8.1 ega uuemat PC-põhist operatsioonisüsteemi. Kui rakenduse tüüp **Retail Cloud POS** vastendatakse kaupluse halduses konkreetse seadmega, saab seda seadet kasutada brauseri kaudu, ilma et oleks vaja paketti alla laadida või installida. Cloud POS nõuab riistvarajaama, et kasutada riistvara üle klaviatuurikiilul põhineva vöötkoodi skannimise.

### <a name="hardware-profile"></a>Riistvaraprofiil

Navigeerimine: klõpsake valikuid **Kaubandus** &gt; **Kanali häälestus** &gt; **Kassa häälestus** &gt; **Kassaprofiilid** &gt; **Riistvaraprofiilid**. Riistvaraprofiil tähistab riistvara, mis on ühendatud kassaregistri või riistvarajaamaga. Riistvaraprofiili abil määratakse ka makseprotsessori parameetrid, mida tuleb maksetarkvara arenduskomplektiga (SDK) suhtlemisel kasutada. (Makse SDK juurutatakse riistvarajaama osana.)

### <a name="hardware-station"></a>Riistvarajaam

Navigeerimine: klõpsake valikuid **Jaemüük** &gt; **Kanalid** &gt; **Jaemüügikanalid** &gt; **Kõik jaekauplused**. Valige kauplus ja klõpsake siis kiirkaarti **Riistvarajaamad**. Riistvarajaam on äriloogika eksemplar, mis juhib kassa välisseadmeid. Riistvarajaam paigaldatakse automaatselt koos MPOS-iga. Teine võimalus on paigaldada riistvarajaam eraldi komponendina ja kasutada seda siis MPOS-i või Cloud POS-i jaoks veebiteenuse kaudu. Riistvarajaam tuleb määratleda kanali tasemel.

### <a name="hardware-station-profile"></a>Riistvarajaama profiil

Navigeerimine: klõpsake valikuid **Kaubandus** &gt; **Kanali häälestus** &gt; **Kassa häälestus** &gt; **Kassaprofiilid** &gt; **Riistvarajaama profiilid**. Kui kanali tasemel määratletud riistvarajaam ise sisaldab eksemplaripõhist teavet nagu riistvarajaama URL, sisaldab riistvarajaama profiil teavet, mis võib olla staatiline või mida võidakse jagada mitme riistvarajaama vahel. Staatiline teave sisaldab porti, mida tuleks kasutada, riistvarajaama paketti ja riistvaraprofiili. Staatiline teave sisaldab ka juurutatava riistvarajaama tüübi kirjeldust (nt **Maksmine** või **Tagastused**), olenevalt riistvarast, mida iga konkreetse riistvarajaama puhul vaja on.

## <a name="scenarios"></a>Stsenaariumid
### <a name="mpos-with-connected-peripheral-devices"></a>Ühendatud välisseadmetega MPOS

[![Tavapärane fikseeritud kassa](./media/traditional-300x279.png)](./media/traditional.png) 

MPOS-i ühendamiseks POS-i välisseadmetega tavapärases, fikseeritud kassa stsenaariumis liikuge kõigepealt registri enda juurde ja määrake sellele riistvaraprofiil. Leiate kassaregistrid, valides **Jaemüük** &gt; **Kanali häälestus** &gt; **Kassa häälestus** &gt; **Registrid**. Kui olete riistvaraprofiili määranud, sünkroonige muudatused kanali andmebaasis, kasutades jaotusgraafikut Registrid. Jaotusgraafikud leiate, valides **Jaemüük** &gt; **Jaemüügi IT** &gt; **Jaotusgraafik**. Järgmisena seadistage kanalil „kohalik” riistvarajaam. Klõpsake valikuid **Jaemüük** &gt; **Kanalid** &gt; **Jaekauplused** &gt; **Kõik jaekauplused** ja valige kauplus. Seejärel klõpsake kiirkaardil **Riistvarajaamad** käsku **Lisa** riistvarajaama lisamiseks. Sisestage kirjeldus, sisestage hosti nimeks **localhost** ja sünkroonige siis kanali muudatused, kasutades jaotusgraafikut Kanali konfigureerimine. Jaotusgraafikud leiate, valides **Jaemüük** &gt; **Jaemüügi IT** &gt; **Jaotusgraafik**. Lõpuks kasutage MPOS-is toimingut **Riistvarajaama valimine** riistvarajaama **localhost** valimiseks. Määrake riistvarajaama olekuks **Aktiivne**. Selles stsenaariumis kasutatav riistvaraprofiil peaks pärinema kassaregistrist enesest. Selle stsenaariumi puhul pole riistvarajaama profiil vajalik. **Märkus.** Mõned riistvaraprofiili muudatused (nt kassasahtlite vahetused) nõuavad uue vahetuse avamist pärast muudatuste sünkroonimist kanaliga. **Märkus.** Cloud POS peab kasutama jaemüügi välisseadmetega suhtlemiseks eraldiseisvat riistvarajaama.

### <a name="mpos-or-cloud-pos-with-a-stand-alone-hardware-station"></a>MPOS või Cloud POS koos eraldi riistvarajaamaga
[![Ühiskasutusega välisseadmed](./media/shared-300x254.png)](./media/shared.png)

Selles stsenaariumis jagavad MPOS-i ja Cloud POS-i kliendid eraldiseisvat riistvarajaama. See stsenaarium nõuab riistvarajaama profiili loomist allalaadimispaketi, pordi ja riistvaraprofiili määramiseks, mida riistvarajaam kasutab. Riistvarajaama profiili leiate, valides **Jaemüük** &gt; **Kanali häälestus** &gt; **Kassa häälestus** &gt; **Kassaprofiilid** &gt; **Riistvarajaama profiilid**. Pärast riistvarajaama profiili loomist minge konkreetse jaemüügikanali juurde (**Jaemüük** &gt; **Kanalid** &gt; **Jaekauplused** &gt; **Kõik jaekauplused**) ja lisage uus riistvarajaam. Vastendage see uus riistvarajaam varem loodud riistvarajaama profiiliga. Järgmiseks sisestage kirjeldus, mis aitab kassiiril riistvarajaama tuvastada. Sisestage väljale **Hosti nimi** hostseadme URL järgmises vormingus: **https://&lt;MachineName:Port&gt;/HardwareStation**. (Asendage **&lt;MachineName:Port&gt;** riistvarajaama tegeliku seadmenime ja pordiga, mis on määratud riistvarajaama profiilis.) Eraldi riistvarajaama puhul tuleks täpsustada ka elektroonilise rahaülekande (EFT) terminali ID-d. See väärtus tähistab EFT terminali, mis on riistvarajaamaga ühendatud, kui makseühendus maksepakkujaga suhtleb. Järgmiseks minge tegelikust riistvarajaamast kanali juurde ja valige riistvarajaam. Siis klõpsake valikut **Allalaadimine** ja installige riistvarajaam. Järgmiseks kasutage MPOS-i või Cloud POS-i toimingut **Riistvarajaama valimine** varem installitud riistvarajaama valimiseks. Valige **Seo** turvalise seose loomiseks kassa ja riistvarajaama vahel. See toiming tuleb teha iga kassa ja riistvarajaama kombinatsiooni puhul üks kord. Pärast riistvarajaama sidumist kasutatakse sama toimingut riistvarajaama aktiveerimiseks selle kasutamise ajal. Selle stsenaariumi puhul tuleks määrata riistvaraprofiil riistvarajaama profiilile, mitte registrile endale. Kui mingil põhjusel pole riistvarajaamale otse riistvaraprofiili määratud, kasutatakse registrile määratud riistvaraprofiili.

## <a name="client-maintenance"></a>Kliendi hooldus
### <a name="registers"></a>Registrid

Kassaregistreid hallatakse peamiselt registrite endi kaudu ning samuti registritele määratud profiilide kaudu. Konkreetse eraldi registri põhiseid atribuute hallatakse registri tasandil. Need atribuudid hõlmavad kauplust, kus registrit kasutatakse, registri numbrit, kirjeldust ja EFT terminali ID-d, mis on registri enese põhine.

### <a name="pos-profiles"></a>Kassa profiilid

Leiate kassaprofiilid, valides **Jaemüük** &gt; **Kanali häälestus** &gt; **Kassa häälestus** &gt; **Kassaprofiilid**. Paljusid registri aspekte tasub hallata profiilide kaudu, kuna profiile saab paljude registrite vahel jagada. Profiile saab vastendada eraldi registriga või, kui profiil kehtib üle kogu kaupluse, siis jaekauplusega. Järgmistes punktides kirjeldatakse kassaprofiile ja nende kasutamist.

#### <a name="offline-profile"></a>Ühendusväline profiil

Ühenduseta profiil määratakse kaupluse tasandil. Seda kasutatakse kassaregistris tehtavate kannete üleslaadimissätete määramiseks, kui see register pole kanali andmebaasiga ühendatud.

#### <a name="functionality-profile"></a>Funktsiooniprofiil

Funktsiooni profiil määratakse kaupluse tasandil. Seda kasutatakse kaupluseüleste sätete määramiseks funktsioonide kohta, mida saab kassas kasutada. Funktsiooniprofiili kaudu hallatakse järgmisi võimalusi. Need võimalused on paigutatud kiirkaardi abil.

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
    -   Kõik teabekoodide haldamise aspektid kassas. Üksikasjad leiate jaotisest [Teabekoodid](info-codes-retail.md).
-   Kiirkaart **Kviitungi nummerdamine**.
    -   Saate määrata kviitungite nummerdamise maskid, mis võivad sisaldada segmente kaupluse numbri, terminali numbri, konstantide jaoks ning seda, kas müük, tagastused, müügitellimused ja hinnapakkumised prinditakse eraldi seeriatena või kas nad kõik põhinevad ühel seerial.

#### <a name="receipt-profiles"></a>Kviitungi profiilid

Kviitungite profiilid määratakse printeritele riistvaraprofiilis. Neid kasutatakse konkreetsest printerist prinditavate kviitungitüüpide määramiseks. Profiilid hõlmavad kviitungivormingute sätteid ja sätteid, mis määravad, kas kviitung prinditakse alati või küsitakse kassiirilt, kas kviitung tuleb printida. Erinevates printerites võidakse samuti kasutada erinevaid kviitungiprofiile. Näiteks 1. printer on tavaline termopaberiga kviitungiprinter ja seetõttu on selle kviitungivormingud väiksemad. Kuid 2. printer on täissuuruses kviitungiprinter, mida kasutatakse ainult klienditellimuste kviitungite printimiseks, mis nõuavad rohkem ruumi.

#### <a name="hardware-profiles"></a>Riistvara profiilid

Riistvaraprofiile selgitatakse kliendi seadistuse komponendina selles artiklis eespool. Riistvaraprofiilid määratakse otse kassaregistrile või riistvarajaama profiilile. Neid kasutatakse seadmetüüpide määramiseks, mida konkreetne kassaregister või riistvarajaam kasutab. Riistvaraprofiilide abil määratakse ka makse SDK-ga suhtlemiseks kasutatavad EFT sätted.

#### <a name="visual-profiles"></a>Visuaalsed profiilid

Visuaalsed profiilid määratakse registri tasandil. Neid kasutatakse konkreetse registri kujunduse määramiseks. Profiilid hõlmavad kasutatava rakenduse tüübi sätteid (MPOS või Cloud POS), rõhuvärvi ja kujundust, fondiskeemi, sisselogimise tausta ja kassa tausta.

### <a name="custom-fields"></a>Kohandatud väljad

Saate luua kohandatud välju, et lisada välju, mida kassal valmiskujul pole. Lisateavet kohandatud väljade kasutamise kohta leiate ajaveebipostitusest [Kohandatud väljadega töötamine](https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/).

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
-   **Inaktiveeritud** – seade on kaupluse halduses või kassa kaudu inaktiveeritud.
-   **Keelatud** – seade on keelatud.

Aktiveerimist puudutav lisateave hõlmab töötajat, kes seadme aktiveerimisolekut muutis, aktiveerimise ajatemplit ja seda, kas seadme konfiguratsioon on kinnitatud.

### <a name="client-data-synchronization"></a>Kliendi andmete sünkroonimine

Kõik kassa kliendi muudatused, v.a seadme aktiveerimisoleku muudatused, tuleb nende jõustumiseks kanali andmebaasiga sünkroonida. Muudatuste sünkroonimiseks kanali andmebaasiga minge jaotisse **Jaemüük** &gt; **Jaemüügi IT** &gt; **Jaotusgraafik** ja käivitage nõutud jaotusgraafik. Kliendi muudatuste puhul tuleks käivitada jaotusgraafikud Registrid ja Kanali konfiguratsioon.




