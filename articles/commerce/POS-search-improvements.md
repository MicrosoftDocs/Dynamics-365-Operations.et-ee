---
title: Tooteotsing ja kliendiotsing kassas
description: Selles teemas antakse ülevaade toote ja kliendi otsingufunktsiooni täiustustest rakenduses Dynamics 365 Commerce.
author: ShalabhjainMSFT
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: 1392b767815722c17b1cc72d27fe2bb8a7c32281
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796362"
---
# <a name="product-search-and-customer-search-in-the-point-of-sale-pos"></a>Tooteotsing ja kliendiotsing kassas

[!include [banner](includes/banner.md)]

Modern Point of Sale (MPOS) ja pilvekassa (CPOS) pakuvad hõlpsasti kasutatavat otsingufunktsiooni toodete ja klientide otsimiseks. Kuna MPOS-i ja CPOS-i akende ülaosas on otsinguriba alati nähtav, saavad töötajad tooteid ja kliente kiiresti otsida.

Töötajad saavad otsida tooteid sortimentidest ja kataloogidest, mis on seostatud praeguse kauplusega. Nad saavad ka otsida sortimentidest ja kataloogidest, mis on seostatud ettevõtte teiste kauplustega. Seega saavad kassapidajad müüa ja tagastada ka kaupluse sortimendist väljaspool olevaid tooteid. Samamoodi saavad töötajad otsida praeguse kaupluse või ettevõtte mõne teise kauplusega seotud kliente. Lisaks saavad töötajad otsida emaorganisatsiooni teise ettevõttega seostatud kliente.

## <a name="product-search"></a>Toote otsing

Vaikimisi toimuvad tooteotsingud kaupluse sortimendist. Seda tüüpi otsingut nimetatakse *kohalikuks tooteotsinguks*. Kuid töötajad saavad minna hõlpsasti üle mis tahes selle kauplusega seotud kataloogi või otsida teisest kauplusest. Seda tüüpi otsingut nimetatakse *toote kaugotsinguks*. Kataloogi vahetamiseks valige lehe vasakult poolelt nupp **Kategooriad**. Valige kuvatava paani ülaosast nupp **Vaheta kataloogi** ja valige siis sirvimiseks mõni saadaolev kataloog. Süsteem otsib tooteid valitud kataloogist.

Lehel **Vaheta kataloogi** saavad töötajad valida hõlpsasti mis tahes kaupluse või otsida tooteid kõigist kauplustest.

![Kataloogi muutmine](./media/Changecatalog.png "Kataloogi muutmine")

Kohalik tooteotsing otsib järgmistest tooteatribuutidest.

- Toote number
- Toote nimetus
- Kirjeldus
- Dimensioonid
- Vöötkood
- Otsi nime

### <a name="additional-local-product-search-capabilities"></a>Täiendavad kohaliku tooteotsingu võimalused

- Mitme märksõnaga otsingute puhul (st otsingusõnu kasutavate otsingute puhul) saavad jaemüüjad konfigureerida, kas otsingutulemused sisaldavad *mõnele* või ainult *kõigile* otsingusõnadele vastavaid tulemusi. Selle funktsiooni säte on saadaval kassa funktsiooniprofiilis uues grupis, mille nimi on **Tooteotsing**. Vaikesäte on **Mis tahes otsingusõnade vastendamine**. See säte on ka soovitatav säte. Sätte **Mis tahes otsingusõnade vastendamine** kasutamisel antakse tulemuseks kõik tooted, mis vähemalt ühele otsingusõnale vastavad. Tulemused sorditakse automaatselt, lisades kasvavas järjestuses tooted, millel on kõige rohkem märksõnade (täielikke või osalisi) vasteid.

    Säte **Kõigi otsingusõnade vastendamine** annab ainult tooted, mis vastavad kõigile otsingusõnadele (täielikult või osaliselt). Sellest sättest on abi, kui toodete nimed on pikad ja töötajad soovivad näha otsingutulemustes ainult piiratud tooteid. Kuid seda tüüpi otsingul on kaks piirangut.

    - Otsing toimub eraldi tooteatribuutidel. Näiteks antakse tulemuseks ainult need tooted, millel on vähemalt ühes tooteatribuudis kõik otsitud märksõnad.
    - Dimensioonidest ei otsita.

- Nüüd saavad jaemüüjad konfigureerida tooteotsingut nii, et kui kasutajad tootenimesid tipivad, kuvatakse otsingusoovitused. Selle funktsiooni uus säte on saadaval kassa funktsiooniprofiilis grupis, mille nimi on **Tooteotsing**. Sätte nimi on **Näita tippimise ajal otsingusoovitusi**. See funktsioon aitab töötajatel otsitavat toodet kiiresti leida, kuna nad ei pea kogu nime käsitsi tippima.
- Tooteotsingu algoritm otsib nüüd otsitud sõnu toote atribuudist **Otsingunimi**.

![Tootesoovitused](./media/Productsuggestions.png "Tootesoovitused")

## <a name="customer-search"></a>Kliendi otsing

Kliendiotsingut kasutatakse klientide otsimiseks mitmesugusel eesmärgil. Näiteks võib kassapidajatel olla vaja vaadata kliendi soovinimekirja või ostuajalugu või lisada klienti kandesse. Otsingu algoritm vastab otsinguterminitele järgmistes kliendi atribuutides olevate väärtuste suhtes.

- Nimi
- Meiliaadress
- Telefoninumber
- Kliendikaardi number
- Kontaktaadress
- Konto number

Nende atribuutide hulgas annab nimi mitme märksõnaga otsingutel kõige suurema paindlikkuse, kuna algoritm annab tulemuseks kõik kliendid, kes vastavad mõnele otsitavale märksõnale. Kliendid, kes vastavad enamikule märksõnadest, kuvatakse tulemuste alguses. See käitumine aitab kassapidajaid olukordades, kus nad otsivad täieliku nime sisestamise kaudu, kuid perekonnanimi ja eesnimi läksid algsel andmete sisestamisel vahetusse. Jõudluse huvides säilitavad kõik teised atribuudid siiski otsingu märksõnade järjekorra. Seega kui otsingu märksõnad ei ühti andmete salvestamise järjekorraga, siis ühtegi tulemust ei anta.

Vaikimisi toimub kliendiotsing kauplusega seotud klientide aadressiraamatutest. Seda tüüpi otsingut nimetatakse *kohalikuks kliendiotsinguks*. Kuid töötajad saavad otsida kliente ka globaalselt. Teisisõnu saavad nad otsida kõigist ettevõtte kauplustest või teistest juriidilistest isikutest. Seda tüüpi otsingut nimetatakse *kliendi kaugotsinguks*.

Globaalseks otsimiseks saavad töötajad valida nupu **Filtreeri tulemusi** lehe alumisest osast ja siis valiku **Otsing kõigist kauplustest**, nagu on näidatud järgmisel illustratsioonil. Sellisel juhul ei kuvata tulemustes ainult kliente. Kuvatakse ka kõik osapoolte tüübid, kes mõnda peakontori aadressiraamatusse kuuluvad. Nende osapoolte hulka kuuluvad töötajad, hankijad, kontaktid ja konkurendid.

> [!NOTE]
> Selleks, et kliendi kaugotsing annaks tulemusi, tuleb sisestada vähemalt neli märki.

Kliendi kaugotsingus ei kuvata kliendi ID-d teistest juriidilistest isikutest pärinevate klientide puhul, kuna nendele osapooltele pole selles ettevõttes kliendi ID-d loodud. Kuid kui töötaja avab kliendi andmete lehe, loob süsteem sellele osapoolele automaatselt kliendi ID ja seostab kliendiga ka kaupluse klientide aadressiraamatud. Seega on see klient hiljem toimuvates kaupluse kohalikes otsingutes nähtav.

![Globaalne kliendi otsing](./media/Globalcustomersearch.png "Globaalne kliendi otsing")

### <a name="additional-local-customer-search-capabilities"></a>Täiendavad kohaliku tooteotsingu võimalused

Kui kautaja otsib telefoninumbrit, eirab süsteem erimärke nagu tühikud, sidekriipsud ja sulud, mis võidi lisada kliendi loomise ajal. Seetõttu ei pea kassapidajad enam otsides muretsema telefoninumbri vormingu pärast. Näiteks kui kliendi telefoninumber sisestati kujul **123-456-7890**, saab kassapidaja klienti otsida, tippides **1234567890** või sisestades telefoninumbrist paar esimest numbrit.

> [!NOTE]
> Kliendil võib olla mitu telefoninumbrit ja meiliaadressi. Kliendiotsingu algoritm otsib ka teiseste meiliaadressite ja telefoninumbrite seast, kuid kliendiotsingutulemuste lehel kuvatakse ainult esmane meiliaadress ja telefoninumber. See võib põhjustada segadust, kuna tagastatud kliendiotsingutulemustes ei kuvata otsitud meiliaadressi või telefoninumbrit. Tulevases väljalaskes plaanime selle teabe kuvamiseks parandada kliendiotsingutulemuste vaadet.

Tavaline kliendiotsing võib olla aeganõudev, sest selle käigus otsitakse mitmest väljast. Selle asemel saavad kassapidajad otsida ühest kliendi atribuudist, nagu nimi, meiliaadress või telefoninumber. Kliendiotsingu algoritmi kasutatavaid atribuute tuntakse ühiselt nimega *kliendi otsingukriteeriumid*. Süsteemiadministraator saab hõlpsalt konfigureerida ühe või mitu kriteeriumi kiirklahvidena, mis kuvatakse kassas. Kuna otsing on piiratud ühe kriteeriumiga, kuvatakse ainult asjakohased otsingutulemid ja jõudlus on palju parem kui tavapärase kliendiotsingu korral. Järgmisel illustratsioonil on näidatud kliendiotsingu kiirklahve kassas.

![Kliendiotsingu kiirklahvid](./media/SearchShortcutsPOS.png "Kliendiotsingu kiirklahvid")

Otsingukriteeriumide määramiseks kiirklahvidena peab administraator rakenduses Commerce avama lehe **Kaubanduse parameetrid** ja seejärel vahekaardil **Kassa otsingukriteeriumid** valima kriteeriumid, mis tuleks kuvada kiirklahvidena.

![Otsingu kiirklahvide konfigureerimine](./media/ConfigureShortcutsAX.png "Otsingu kiirklahvide konfigureerimine")

> [!NOTE]
> Kui lisate liiga palju kiirklahve, muutub kassa otsinguriba rippmenüü ülekoormatuks ja töötajate otsingu tõhusus võib väheneda. Soovitame lisada vaid nii palju kiirklahve, kui vaja.

Väli **Kuvamisjärjestus** määratleb, millises järjekorras kiirklahve kassas kuvatakse. Näidatud kriteeriumid on valmisatribuudid, mida kliendiotsingu algoritm kasutab klientide otsimiseks. Kuid partnerid saavad lisada kohandatud atribuute otsingu kiirklahvidena. Kohandatud atribuutide lisamiseks otsingu kiirklahvidena peab süsteemiadministraator laiendama laiendavat loetelu, mida kasutatase kliendiotsingu kriteeriumiks ja seejärel märkima partneri kohandatud atribuudid kiirklahvidena. Kui otsingute jaoks kasutatakse partnerite kohandatud kiirklahve, on partnerid vastutavad tulemeid leidva koodi kirjutamise eest.

> [!NOTE]
> Loetellu lisatud kohandatud atribuut ei mõjuta standardset kliendiotsingu algoritmi. Teisisõnu, kliendiotsingu algoritm ei otsi kohandatud atribuudist. Kasutajad saavad kohandatud atribuuti otsingute jaoks kasutada ainult siis, kui kohandatud atribuut on lisatud kiirklahvina või otsingu vaikealgoritm on alistatud.

Jaemüüjad saavad kassas seada kliendi vaikeotsingu režiimiks ka **Kõigi kaupluste otsing**. See konfiguratsioon võib olla kasulik olukordades, kus väljaspool kassat loodud kliente tuleb otsida kohe (nt enne levitamise töö käitamist). Selleks peab jaemüüja kassa funktsiooniprofiilis **Kliendi vaikeotsingu režiimi** suvandi sisse lülitama. Kui see on seatud **Jah**, iga kliendi otsingu katse saadab seejärel peakontorisse reaalajas taotluse.

Ootamatute jõudlusprobleemide vältimiseks on see konfiguratsioon peidetud eelväljaande lipu taha, mille nimi on **CUSTOMERSEARCH_ENABLE_DEFAULTSEARCH_FLIGHTING**. Seega kasutajaliidese seadistuse **Kliendiotsingu režiimi vaiketüüp** kuvamiseks peaks jaemüüja looma kasutaja vastuvõtu testimise (UAT) ja tootmiskeskkonnas tugiteenusepileti. Pärast pileti kättesaamist teeb inseneride töörühm jaemüüjaga koostööd, et kindlustada, et jaemüüja testiks oma mitte-tootmiskeskkondades, et hinnata jõudlust ja rakendada vajalikud optimeerimised.

## <a name="cloud-powered-customer-search"></a>Pilvepõhine kliendiotsing

Kliendiotsingu võimaluse avalik eelvaade Azure'i Cognitive Searchi teenuse abil on välja antud Commerce 10.0.18 väljalaske osana. Lisaks jõudluse parendustele on teenuse kasutajatel kasulik ka rikas täiendus ja täiustatud tähtsuse võimalused. Jõudluse parendused on eriti ilmnevad, kui kasutatakse müügikoha globaalse otsingu funktsiooni ("Otsi kõiki kauplusi").. Seda seetõttu, et Commerce Headquartersi andmetest päringute asemel toodatakse Azure'i otsinguindeksist otsingutulemused. 

### <a name="enable-the-cloud-powered-search-feature"></a>Luba pilve võimsusega otsingu funktsioon

> [!NOTE]
> Nii Commerce headquarters kui ka Commerce Scale Unit uuendatakse versiooniks 10.0.18. Müügikoha uuendamine ei ole nõutav.

Pilvepõhise otsingufunktsiooni lubamiseks Commerce'i headquarters`is, toimige järgmiselt.

1. Avage **Süsteemihaldus \> Tööruumid \> Funktsioonihaldus**.
1. Leidke ja valige **(Eelvaade) pilve toetatud kliendi otsing** funktsioon ja seejärel valige **Luba kohe**.
1. Avage **Kauplused ja äri >Äri andmeedastaja > Lähtesta äri andmeedastaja** ja valige **OK** et kuvada uus **1010_CustomerSearch** töö **jaotusgraafiku** vormis.
1. Avage **Jaemüük ja kaubandus > Jaemüügi ja kaubanduse IT > Jaotusgraafik**.
1. Käivitage **1010_CustomerSearch** töö. See töö avaldab kuupäeva Azure'i otsinguindeksis. Kui indeksi avaldamine on lõpule viidud, seatakse töö olekuks **Rakendatud**.
1. Pärast **1010_CustomerSearch** on töö staatus seatud **Rakendatud**, käivitage **1110 - globaalne konfiguratsiooni** töö äsja lubatud funktsiooni **funktsioonihaldus** värskendamiseks.
1. Seejärel käivitage **1010_CustomerSearch** kliendivärskenduste saatmiseks otsinguindeksisse regulaarsete ajavahemike järel.

> [!NOTE]
> Algse indeksi avaldamiseks võib **1010_CustomerSearch** töö lõpule viimine võtta mitu tundi, kuni see saadab kõik kliendikirjed Azure'i otsinguindeksisse. Järgnevad uuendused peaksid kestma mõned minutid. Ajaperioodis, mil pilve toetatud otsingufunktsioon on lubatud, kuid indeksi avaldamine ei ole veel lõpetatud, läheb kliendi otsing kassast vaikimisi olemasolevale SQL-põhisele otsingule. See tagab, et operatsioonide talletamiseks ei ole katkestusi.

### <a name="functional-differences-from-the-existing-search"></a>Olemasoleva otsingu funktsioonierinevused

Järgmises loendis näidatakse, kuidas pilve toega kliendi otsingufunktsioon erineb olemasolevatest otsingufunktsioonidest. 

- Commerce Headquartersis loodud ja redigeeritud kliendid saadetakse Azure'i otsinguindeksisse **pärast 1010_CustomerSearch** käivitamist. Uuenduste uuendamiseks võtab aega vähemalt 15–20 minutit. Müügikoha kasutajad saavad uusi kliente (või uuendatud teabel põhinevat otsingut) otsida umbes 15–20 minutit pärast seda, kui Värskendused toimuvad Commerce Headquartersis. Kui teie äriprotsess nõuab, et Äri peakontoris loodud kliendid peavad kassas kohe otsima, ei pruugi see olla teie jaoks õige teenus.
- Kassas loodud uued kliendid saadetakse Azure'i otsinguindeksisse Commerce Scale Unit kaudu ja on kohe otsitavad igas kaupluses. Kui aga Async Kliendi loomise funktsioon on sisse lülitatud, ei avaldata uusi kliendikirjeid Azure'i otsinguindeksis rakenduses Commerce Scale Unit ja neid ei otsita kassast enne, kui klienditeave on sünkroonitud Commerce headquartersiga ja kliendi ID-d luuakse Async Klientide jaoks. Seejärel **1010_CustomerSearch** töö Async Customeri kirjed Azure otsinguindeksisse saata. Keskmiselt on see umbes 30 minutit enne, kui vastloodud Asynci kliente kassas otsida saab. See hinnang eeldab, et **1010_CustomerSearch**, **P-töö** ja **Sünkrooni kliendid ja äripartnerid asünkroonses reziimis** tööd plaanitakse käitada 15 minuti järel.
- Pilve toega otsing otsib ka teiseseid e-kirju ja klientide telefoninumbriid, kuid praegu kuvatakse kliendi otsingutulemustes ainult esmane telefoninumber ja klientide esmane meiliaadress. Kohe võib see näida, et asjatuid otsingutulemusi on tagastatud, kuid kliendi teisese e-kirja ja telefoninumbri kontrollimine otsingutulemustes võib aidata kontrollida, kas märksõna otsiti kliendi vastendamise tulemusena. Sellise segaduse vältimiseks plaanitakse otsingutulemuste lehte parandada, et kasutajad mõistaksid, miks otsingutulemus tagastati.
- Nõue otsida globaalses otsingus vähemalt 4 märki ("Otsi kõiki kauplusi") ei ole sellele teenusele kohaldatav.

> [!NOTE]
> Kliendi otsinguvõimalused Azure'i cotive search service'i abil on eelvaate jaoks saadaval piiratud regioonides. Kliendi otsinguvõimalused *pole* saadaval järgmistes regioonides:
> - Brasiilia
> - India
> - Kanada
> - Ühendkuningriik

[!INCLUDE[footer-include](../includes/footer-banner.md)]
