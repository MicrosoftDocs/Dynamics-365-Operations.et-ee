---
title: Välisseadmete ühendamine kassaga (POS)
description: See teema käsitleb välisseadmete ühendamist Retail POS-iga.
author: BrianShook
ms.date: 03/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTerminalTable, RetailDevice
audience: Application User
ms.reviewer: josaw
ms.custom: 92383
ms.assetid: 83f31ea6-f0a2-4501-9d4d-a37b6eec2599
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f1c53c7215d3a5a182f345d5e040274ae06f9b12
ms.sourcegitcommit: 116898def829c0f78bda8a117242aa308793465d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/01/2022
ms.locfileid: "8370947"
---
# <a name="connect-peripherals-to-the-point-of-sale-pos"></a>Välisseadmete ühendamine kassaga (POS)

[!include [banner](includes/banner.md)]

See teema käsitleb välisseadmete ühendamist Retail POS-iga.

> [!NOTE]
> Täpsemate installimisjuhiste saamiseks vaadake jaotiseid [Jaemüügi riisvarajaama konfigureerimine ja installimine](retail-hardware-station-configuration-installation.md) ja [Kaasaegse kassa (MPOS) konfigureerimine, installimine ja aktiveerimine](retail-modern-pos-device-activation.md).

## <a name="key-components"></a>Põhikomponendid

Mitut komponenti kasutatakse seoste määratlemiseks kaupluse, kassaregistri või kaupluse kanalite ja välisseadmete hulgas, mida need registrid või kanalid kannete töötlemiseks kasutavad. Selles jaotises kirjeldatakse iga komponenti ja selgitatakse, kuidas seda tuleks kaupluse juurutuses kasutada.

### <a name="pos-registers"></a>Kassaregistrid

Navigeerimine: klõpsake **Jaemüük ja kaubandus** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Registrid**.

Kassaregister on olem, mida kasutatakse kassa konkreetse eksemplari omaduste määratlemiseks. Nende omaduste hulka kuuluvad registris kasutatav riistvaraprofiil või välisseadmed, registriga vastendatud pood ja sellesse registrisse sisse logiva kasutaja visuaalne kogemus.

### <a name="devices"></a>Seadmed

Navigeerimine: klõpsake **Jaemüük ja kaubandus** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Seadmed**.

Seade on üksus, mis kajastab kassaregistriga vastendatud seadme füüsilist eksemplari. Seadme loomisel vastendatakse see kassaregistriga. Seadmeüksus jälgib teavet selle kohta, millal kassaregister aktiveeritakse, kasutatava kliendi tüübi kohta ja rakenduse paketi kohta, mis on konkreetse seadme puhul juurutatud. Seadmed võivad olla kahte tüüpi: **Retail modern POS** (MPOS) või **Retail Cloud POS** (pilvekassa).

#### <a name="mpos"></a>MPOS

MPOS on POS-i klientrakendus, mis on installitud operatsioonisüsteemi Windows 8.1 või uuemasse PC-põhisesse operatsioonisüsteemi. Kui rakenduse tüüp **Retail modern POS** vastendatakse seadmega, saab konkreetsele seadmele määrata allalaadimispaketi. Allalaadimispaketti saab kohandada nii, et see sisaldaks installipaketi erinevaid versioone. Võimalus juurutada erinevaid pakette tagab paindlikkuse olukordades, kus erinevad kassaregistrid võivad nõuda erinevaid integratsioone. MPOS juurutatakse koos integreeritud riistvarajaamaga.

#### <a name="cloud-pos"></a>Cloud POS

Cloud POS on brauseripõhine kassa. Kuna see töötab brauseris, ei nõua Cloud POS operatsioonisüsteemi Windows 8.1 ega uuemat PC-põhist operatsioonisüsteemi. Kui rakenduse tüüp **Retail Cloud POS** vastendatakse Headquarters'is konkreetse seadmega, saab seda seadet kasutada brauseri kaudu, ilma et oleks vaja paketti alla laadida või installida. Cloud POS nõuab riistvarajaama, et kasutada riistvara üle klaviatuurikiilul põhineva vöötkoodi skannimise.

### <a name="hardware-profile"></a>Riistvaraprofiil

Navigeerimine: minge jaemüügi ja **ärikanali häälestamise \> kassa häälestuse \>\> kassaprofiilide \> riistvaraprofiilidele**.

Riistvaraprofiil tuvastab riistvara, mis on ühendatud kassaregistriga integreeritud või ühiskasutatava riistvarajaama kaudu. Riistvaraprofiili abil määratakse ka makseprotsessori parameetrid, mida tuleb maksetarkvara arenduskomplektiga (SDK) suhtlemisel kasutada. Makse SDK juurutatakse riistvarajaama osana.

### <a name="hardware-station"></a>Riistvarajaam

Navigeerimine: minge jaemüügi **ja äri kanalite \>\> juurde, \>** valige kauplus ja seejärel valige **kiirkaart Riistvara** kiirkaart.

Riistvarajaam on äriloogika eksemplar, mis juhib kassa välisseadmeid. Riistvarajaam paigaldatakse automaatselt koos MPOS-iga. Teine võimalus on paigaldada riistvarajaam eraldi komponendina ja kasutada seda siis MPOS-i või Cloud POS-i jaoks veebiteenuse kaudu. Riistvarajaam tuleb määratleda kanali tasemel.

## <a name="scenarios"></a>Stsenaariumid

### <a name="mpos-with-connected-peripheral-devices"></a>Ühendatud välisseadmetega MPOS

[![Tavapärane, fikseeritud kassa.](./media/traditional-300x279.png)](./media/traditional.png)

MPOS-i ühendamiseks POS-i välisseadmetega tavapärases, fikseeritud kassa stsenaariumis liikuge kõigepealt registri enda juurde ja määrake sellele riistvaraprofiil. Leiate kassaregistrid, valides **Jaemüük ja kaubandus** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Registrid**. 

Kui olete riistvaraprofiili määranud, sünkroonige muudatused kanali andmebaasis, kasutades jaotusgraafikut **Registrid**. Jaotusgraafikud leiate, valides **Jaemüük ja kaubandus** &gt; **Jaemüügi ja kaubanduse IT** &gt; **Jaotusgraafik**. 

Seejärel seadistage kanalile sihtotstarbeline riistvarajaam. Minge jaemüügi **ja äri kanalite \> kõikidesse \>\> kauplustesse** ja valige kauplus. 

Seejärel valige kiirkaardil **Riistvara** kiirkaart Riistvarajaama **lisamiseks** suvand Lisa. Valige **riistvarajaama** tüübiks sihtotstarbeline ja sisestage seejärel kirjeldus. Riistvaraprofiili **väli** võib olla tühi, sest selles stsenaariumis kasutatav riistvaraprofiil tuleb kassaregistrist endast. Seejärel sünkroonige muudatused kanaliga, kasutades kanali konfiguratsiooni **jaotuse** graafikut. Jaotusgraafikud leiate jaemüügi ja rakenduse **Commerce Retail ja Commerce \> IT jaotusgraafikust \>**. 

Lõpuks kasutage MPOS-i riistvarajaama valimiseks riistvarajaama toimingut, **mis** vastab kirjelduse jaoks sisestatud väärtusele, ja määrake riistvarajaama **väärtuseks Aktiivne**. 

> [!NOTE]
> - Mõned riistvaraprofiili muudatused (nt kassasahtlite vahetused) nõuavad uue vahetuse avamist pärast muudatuste sünkroonimist kanaliga.
> - Cloud POS peab kasutama välisseadmetega suhtlemiseks eraldiseisvat riistvarajaama.

### <a name="mpos-or-cloud-pos-with-a-stand-alone-hardware-station"></a>MPOS või Cloud POS koos eraldi riistvarajaamaga

[![Ühiskasutusega välisseadmed.](./media/shared-300x254.png)](./media/shared.png)

Selles stsenaariumis jagatakse eraldi riistvarajaam MPOS- ja Cloud POS-i klientide vahel. See stsenaarium nõuab, et loote ühise riistvarajaama ja määrate allalaaditava paketi, pordi ja riistvaraprofiili, mida riistvarajaam kasutab. Uue riistvarajaama määratlemiseks **valige** kindlas kanalis kiirkaart Riistvara kiirkaart (**Jaemüügi \>\>\>**- ja ärikanalite kauplused kõik kauplused) **ja lisage uus ühiskasutatava tüübiga riistvarajaam.** 

Järgmiseks sisestage kirjeldus, mis aitab kassiiril riistvarajaama tuvastada. Sisestage väljale **Hosti nimi** hostseadme URL järgmises vormingus: `https://<MachineName:Port>/HardwareStation`. (Asenda **&lt; MachineName:port&gt;** riistvarajaama tegeliku masinanimega.) Eraldi riistvarajaama jaoks peaksite määrama ka elektroonilise ülekande (EFT) terminali ID. See väärtus tähistab EFT terminali, mis on riistvarajaamaga ühendatud, kui makseühendus maksepakkujaga suhtleb. 

Edasi, masinast, mis hostib riistvarajaama, minge peakontori kanalisse ja valige riistvarajaam. Seejärel valige **laadi** alla riistvarajaama installeri allalaadimiseks ja installige riistvarajaam. Lisateavet riistvarajaama installimise kohta vt [jaemüügi riistvarajaama konfigureerimine ja installimine](retail-hardware-station-configuration-installation.md). 

Järgmiseks kasutage MPOS-i või Cloud POS-i toimingut **Riistvarajaama valimine** varem installitud riistvarajaama valimiseks. Valige **Seo** turvalise seose loomiseks kassa ja riistvarajaama vahel. See toiming tuleb teha iga kassa ja riistvarajaama kombinatsiooni puhul üks kord. 

Pärast riistvarajaama sidumist kasutatakse sama toimingut riistvarajaama aktiveerimiseks selle kasutamise ajal. Selle stsenaariumi puhul tuleb riistvaraprofiil määrata ühiskasutatava riistvarajaama, mitte kassaaparaat ise. Kui mingil põhjusel ei ole riistvarajaamale määratud ühtegi riistvaraprofiili, kasutatakse kassaaparaati määratud riistvaraprofiili.

## <a name="client-maintenance"></a>Kliendi hooldus

### <a name="registers"></a>Registrid

Kassaregistreid hallatakse peamiselt registrite endi kaudu ning samuti registritele määratud profiilide kaudu. Konkreetse eraldi registri põhiseid atribuute hallatakse registri tasandil. Need atribuudid hõlmavad kauplust, kus registrit kasutatakse, registri numbrit, kirjeldust ja EFT terminali ID-d, mis on registri enese põhine.

### <a name="pos-profiles"></a>Kassa profiilid

Leiate kassaprofiilid, valides **Jaemüük ja kaubandus** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Kassaprofiilid**. Paljusid registri aspekte tasub hallata profiilide kaudu, kuna profiile saab paljude registrite vahel jagada. Profiile saab vastendada eraldi registriga või, kui profiil kehtib üle kogu kaupluse, siis kauplusega. Järgmistes punktides kirjeldatakse kassaprofiile ja nende kasutamist.

#### <a name="offline-profile"></a>Ühendusväline profiil

Ühenduseta profiil määratakse kaupluse tasandil. Seda kasutatakse kassaregistris tehtavate kannete üleslaadimissätete määramiseks, kui see register pole kanali andmebaasiga ühendatud.

#### <a name="functionality-profile"></a>Funktsiooniprofiil

Funktsiooni profiil määratakse kaupluse tasandil. Seda kasutatakse kaupluseüleste sätete määramiseks funktsioonide kohta, mida saab kassas kasutada. Funktsiooniprofiili kaudu hallatakse järgmisi võimalusi. Need võimalused on paigutatud kiirkaardi abil.

- Kiirkaart **Üldine**.

    - Rahvusvaheline Standardiorganisatsioon (ISO).
    - Kliendi loomine ühenduseta režiimis.
    - Meilikviitungi profiil.
    - Keskne personali sisselogimise autentimine.

- Kiirkaart **Funktsioonid**.

    - Sisselogimise ja laiendatud sisselogimise haldamine.
    - Kassa rahalised ja valuutaga seotud aspektid, nt võimalus sisestada hindu ja see, kas peenraha puhul on kümnendkohad nõutavad.
    - Aja registreerimine kassa kaudu.
    - Toodete ja maksete kuvamise viis kassas ja kviitungitel.
    - Päeva lõpetamise haldamine.
    - Kanali andmebaasi kande säilitamise parameetrid.
    - Klientide otsimise ja loomise viis kassast.
    - Allahindluste arvutamise viis.

- Kiirkaart **Summa**.

    - Lubatud maksimum- ja miinimumhinnad.
    - Allahindluse rakendamine ja arvutamine.

- Kiirkaart **Teabekoodid**.

    - Kõik teabekoodide haldamise aspektid kassas. Üksikasju vaadake jaotisest [Teabekoodid ja teabekoodide rühmad](info-codes-retail.md).

- Kiirkaart **Kviitungi nummerdamine**.

    - Määrake kviitungi nummerdamise maskid, mis võivad sisaldada segmente kaupluse numbri, terminali numbri, konstantide ja kas müük, tagastused, müügitellimused ja pakkumised prinditakse eraldi seeriates või kas need kõik järgivad sama seeriat.

#### <a name="receipt-profiles"></a>Kviitungi profiilid

Kviitungi profiilid määratakse printeritele riistvaraprofiilis. Neid kasutatakse konkreetsest printerist prinditavate kviitungitüüpide määramiseks. Profiilid hõlmavad kviitungivormingute sätteid ja sätteid, mis määravad, kas kviitung prinditakse alati või küsitakse kassiirilt, kas kviitung tuleb printida. Erinevates printerites võidakse samuti kasutada erinevaid kviitungiprofiile. Näiteks 1. printer on tavaline termopaberiga kviitungiprinter ja seetõttu on selle kviitungivormingud väiksemad. Kuid 2. printer on täissuuruses kviitungiprinter, mida kasutatakse ainult klienditellimuste kviitungite printimiseks, mis nõuavad rohkem ruumi. Lisateavet vt kviitungi [profiili konfigureerimine](configure-emailed-receipt-formats.md#configure-a-receipt-profile).

#### <a name="hardware-profiles"></a>Riistvara profiilid

Riistvaraprofiile kirjeldatakse selles teemas varasema kliendi häälestuse komponendina. Riistvaraprofiilid on määratud otse kassaregistrisse või ühiskasutatavasse riistvarajaama ja neid kasutatakse teatud kassaregistri või riistvarajaama kasutatavate seadmete tüüpide määramiseks. Riistvaraprofiilide abil määratakse ka makse SDK-ga suhtlemiseks kasutatavad EFT sätted.

#### <a name="visual-profiles"></a>Visuaalsed profiilid

Visuaalseid profiile kasutatakse konkreetse registri kujunduse määramiseks ja need määratakse registri tasemel. Profiilid sisaldavad kasutatava rakenduse tüübi sätteid (MPOS või Cloud POS), rõhuvärvi ja kujundust, fondi skeemi, sisselogimise lehekülje tausta ja kassa tausta. Lisateavet vt müügikoha [(POS) visuaalsete profiilide loomine](tasks/create-pos-visual-profile-2016-02.md). 

### <a name="custom-fields"></a>Kohandatud väljad

Saate luua kohandatud välju, et lisada välju, mida kassal valmiskujul pole. Lisateavet kohandatud väljade kasutamise kohta leiate ajaveebipostitusest [Kohandatud väljadega töötamine](https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/).

### <a name="language-text"></a>Keeletekst

Saate kassas keele tekstisisestuse abil vaikestringe alistada. Stringi alistamiseks kassas lisage uus keele tekstirida. Seejärel määrake ID, vaikestring, mis tuleks alistada, ja tekst, mis tuleks vaikestringi asemel kassas kuvada.

### <a name="channel-reports-configuration"></a>Kanali aruannete konfiguratsioon

Jaemüügikanalis saadaolevaid aruandeid saate seadistada lehel **Kanali aruannete konfiguratsioon**. Saate luua uusi aruandeid, sisestades aruande XML-määratluse ja määrates aruande kassa konkreetsele õiguste grupile.

### <a name="devices"></a>Seadmed

Seadmeid selgitatakse selles artiklis eespool. Neid kasutatakse konkreetse kassaregistri aktiveerimise haldamiseks. Seadmeid kasutatakse ka konkreetse registri jaoks kasutatava rakenduse ja MPOS-i kliendi installimiseks kasutatava installipaketi määramiseks. Siin on seadme aktiveerimise olekud.

- **Ootel** – seade on aktiveerimiseks valmis.
- **Aktiveeritud** – seade on aktiveeritud.
- **Inaktiveeritud** – seade on Headquarters'is või kassa kaudu inaktiveeritud.
- **Keelatud** – seade on keelatud.

Aktiveerimist puudutav lisateave hõlmab töötajat, kes seadme aktiveerimisolekut muutis, aktiveerimise ajatemplit ja seda, kas seadme konfiguratsioon on kinnitatud.

### <a name="client-data-synchronization"></a>Kliendi andmete sünkroonimine

Kõik kassa kliendi muudatused, v.a seadme aktiveerimisoleku muudatused, tuleb nende jõustumiseks kanali andmebaasiga sünkroonida. Muudatuste sünkroonimiseks kanali andmebaasiga avage **Jaemüük ja kaubandus** &gt; **Jaemüügi ja kaubanduse IT** &gt; **Jaotusgraafik** ja käivitage vajalik jaotusgraafik. Kliendi muudatuste puhul tuleks käivitada jaotusgraafikud **Registrid** ja **Kanali konfiguratsioon**.

## <a name="additional-resources"></a>Lisaressursid

[Retail Hardware Stationi konfigureerimine ja installimine](retail-hardware-station-configuration-installation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
