---
title: Tooteotsing ja kliendiotsing kassas
description: Selles teemas antakse ülevaade toote ja kliendi otsingufunktsiooni täiustustest rakenduses Microsoft Dynamics 365 for Retail.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 03/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: a1593445af41cba30bdc35933302d0873e313585
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1530772"
---
# <a name="product-search-and-customer-search-in-the-point-of-sale-pos"></a>Tooteotsing ja kliendiotsing kassas

[!include [banner](includes/banner.md)]

Modern Point of Sale (MPOS) ja pilvekassa (CPOS) pakuvad hõlpsasti kasutatavat otsingufunktsiooni toodete ja klientide otsimiseks. Kuna MPOS-i ja CPOS-i akende ülaosas on otsinguriba alati nähtav, saavad töötajad tooteid ja kliente kiiresti otsida.

Töötajad saavad otsida tooteid sortimentidest ja kataloogidest, mis on seostatud praeguse kauplusega. Nad saavad ka otsida sortimentidest ja kataloogidest, mis on seostatud ettevõtte teiste kauplustega. Seega saavad kassapidajad müüa ja tagastada ka kaupluse sortimendist väljaspool olevaid tooteid. Samamoodi saavad töötajad otsida praeguse kaupluse või ettevõtte mõne teise kauplusega seotud kliente. Lisaks saavad töötajad otsida emaorganisatsiooni teise ettevõttega seostatud kliente.

## <a name="product-search"></a>Toote otsing

Vaikimisi toimuvad tooteotsingud kaupluse sortimendist. Seda tüüpi otsingut nimetatakse *kohalikuks tooteotsinguks*. Kuid töötajad saavad minna hõlpsasti üle mis tahes selle kauplusega seotud kataloogi või otsida teisest kauplusest. Seda tüüpi otsingut nimetatakse *toote kaugotsinguks*. Kataloogi vahetamiseks valige lehe vasakult poolelt nupp **Kategooriad**. Valige kuvatava paani ülaosast nupp **Vaheta kataloogi** ja valige siis sirvimiseks mõni saadaolev kataloog. Süsteem otsib tooteid valitud kataloogist.

Lehel **Vaheta kataloogi** saavad töötajad valida hõlpsasti mis tahes kaupluse või otsida tooteid kõigist kauplustest.

![Kataloogi vahetamine](./media/Changecatalog.png "Kataloogi vahetamine")
 
Kohalik tooteotsing otsib järgmistest tooteatribuutidest.

- Toote number
- Toote nimi
- Kirjeldus
- Dimensioonid
- Vöötkood
- Otsingunimi

### <a name="enhancements-to-local-product-searches"></a>Kohalike tooteotsingute täiustused

Kohalike tooteotsingute kogemus on nüüd kasutajasõbralikum. Tehtud on ka järgmised täiustused.

- Otsinguribale on lisatud toote ja kliendi rippmenüüd, et töötajad saaksid valida enne otsimist **toote** või **kliendi**. Vaikimisi on valitud **Toode**, nagu on näha järgmisel illustratsioonil.
- Mitme märksõnaga otsingute puhul (st otsingusõnu kasutavate otsingute puhul) saavad jaemüüjad konfigureerida, kas otsingutulemused sisaldavad *mõnele* või ainult *kõigile* otsingusõnadele vastavaid tulemusi. See säte on saadaval kassa funktsiooniprofiilis uues grupis, mille nimi on **Tooteotsing**. Vaikesäte on **Mis tahes otsingusõnade vastendamine**. See säte on ka soovitatav säte. Sätte **Mis tahes otsingusõnade vastendamine** kasutamisel antakse tulemuseks kõik tooted, mis vähemalt ühele otsingusõnale vastavad. Tulemused sorditakse automaatselt, lisades kasvavas järjestuses tooted, millel on kõige rohkem märksõnade (täielikke või osalisi) vasteid.

    Säte **Kõigi otsingusõnade vastendamine** annab ainult tooted, mis vastavad kõigile otsingusõnadele (täielikult või osaliselt). Sellest sättest on abi, kui toodete nimed on pikad ja töötajad soovivad näha otsingutulemustes ainult piiratud tooteid. Kuid seda tüüpi otsingul on kaks piirangut.

    - Otsing toimub eraldi tooteatribuutidel. Näiteks antakse tulemuseks ainult need tooted, millel on vähemalt ühes tooteatribuudis kõik otsitud märksõnad.
    - Dimensioonidest ei otsita.

- Nüüd saavad jaemüüjad konfigureerida tooteotsingu nii, et kui kasutajad tootenimesid tipivad, siis kuvatakse otsingusoovitused. Selle funktsiooni uus säte on saadaval kassa funktsiooniprofiilis grupis, mille nimi on **Tooteotsing**. Sätte nimi on **Näita tippimise ajal otsingusoovitusi**. See funktsioon aitab töötajatel otsitavat toodet kiiresti leida, kuna nad ei pea kogu nime käsitsi tippima.
- Tooteotsingu algoritm otsib nüüd otsitud sõnu toote atribuudist **Otsingunimi**.

    ![Tootesoovitused](./media/Productsuggestions.png "Tootesoovitused")

## <a name="customer-search"></a>Kliendi otsing

Kliendiotsingut kasutatakse klientide otsimiseks mitmesugusel eesmärgil. Näiteks võib kassapidajatel olla vaja vaadata kliendi soovinimekirja või ostuajalugu või lisada klienti kandesse. Otsingu algoritm vastab otsinguterminitele järgmistes kliendi atribuutides olevate väärtuste suhtes: nimi, meiliaadress, telefon, kliendikaardi number, aadress ja konto number. Nende hulgas pakub nimeatribuut mitme märksõnaga otsingute puhul kõige enam paindlikkust, kuna algoritm annab tulemuseks kõik kliendid, kes mõnele otsitud märksõnale vastavad, ja kliendid, kes vastavad suurimale märksõnade hulgale, kuvatakse tulemuste eesotsas. See käitumine aitab kassapidajaid olukordades, kus nad otsivad täieliku nime sisestamise kaudu, kuid perekonnanimi ja eesnimi läksid algsel andmete sisestamisel vahetusse. Jõudluse huvides säilitavad kõik teised atribuudid siiski otsingu märksõnade järjekorra, mis tähendab, et kui otsingu märksõnad ei ühti andmete salvestamise järjekorraga, siis ühtegi tulemust ei anta.

Vaikimisi toimub kliendiotsing kauplusega seotud klientide aadressiraamatutest. Seda tüüpi otsingut nimetatakse *kohalikuks kliendiotsinguks*. Kuid töötajad saavad otsida kliente ka globaalselt. Teisisõnu saavad nad otsida kõigist ettevõtte kauplustest või teistest juriidilistest isikutest. Seda tüüpi otsingut nimetatakse *kliendi kaugotsinguks*.

Globaalseks otsimiseks saavad töötajad valida nupu **Filtreeri tulemusi** lehe alumisest osast ja siis valiku **Otsing kõigist kauplustest**, nagu on näidatud järgmisel illustratsioonil. Sellisel juhul ei kuvata tulemustes ainult kliente. Kuvatakse ka kõik osapoolte tüübid, kes mõnda peakontori aadressiraamatusse kuuluvad. Nende osapoolte hulka kuuluvad töötajad, hankijad, kontaktid ja konkurendid.

> [!NOTE]
> Selleks, et kliendi kaugotsing annaks tulemusi, tuleb sisestada vähemalt neli märki.

Kliendi kaugotsingus ei kuvata kliendi ID-d teistest juriidilistest isikutest pärinevate klientide puhul, kuna nendele osapooltele pole selles ettevõttes kliendi ID-d loodud. Kuid kui töötaja avab kliendi andmete lehe, loob süsteem sellele osapoolele automaatselt kliendi ID ja seostab kliendiga ka kaupluse klientide aadressiraamatud. Seega on see klient hiljem toimuvates kaupluse kohalikes otsingutes nähtav.

![Globaalne kliendi otsing](./media/Globalcustomersearch.png "Globaalne kliendi otsing")

### <a name="enhancements-to-local-customer-search"></a>Kohaliku kliendiotsingu täiustused

Telefoninumbritel põhinevaid otsinguid on lihtsustatud. Need otsingud eiravad nüüd erimärke, nagu tühikud, sidekriipsud ja sulud, mis võidi lisada kliendi loomise ajal. Seetõttu ei pea kassapidajad enam otsides muretsema telefoninumbri vormingu pärast. Nad saavad kliente otsida ka osalise telefoninumbri järgi. Kui telefoninumber sisaldab erimärke, saab selle leidmiseks otsida ka numbreid, mis ilmuvad pärast erimärke. Näiteks kui kliendi telefoninumber sisestati kujul **123-456-7890**, saab kassapidaja klienti otsida, tippides **123**, **456**, **7890** või **1234567890** või sisestades telefoninumbrist paar esimest numbrit.

Tavaline kliendiotsing võib olla aeganõudev, sest selle käigus otsitakse mitmest väljast. Selle asemel saavad kassapidajad nüüd otsida ühest kohandatud atribuudist, nagu nimi, meiliaadress või telefoninumber. Kliendiotsingu algoritmi kasutatavaid atribuute tuntakse ühiselt nimega *kliendi otsingukriteeriumid*. Süsteemiadministraator saab hõlpsalt konfigureerida ühe või mitu kriteeriumi kiirklahvidena, mis kuvatakse kassas. Kuna otsing on piiratud ühe kriteeriumiga, kuvatakse ainult asjakohased otsingutulemid ja jõudlus on palju parem kui tavapärase kliendiotsingu korral. Järgmisel illustratsioonil on näidatud kliendiotsingu kiirklahve kassas.

![Kliendiotsingu kiirklahvid](./media/SearchShortcutsPOS.png "Kliendiotsingu kiirklahvid")

Otsingukriteeriumide määramiseks kiirklahvidena peab administraator rakenduses Microsoft Dynamics 365 for Finance and Operations avama lehe **Jaemüügi parameetrid** ja seejärel vahekaardil **Kassa otsingukriteeriumid** valima kriteeriumid, mis tuleks kuvada kiirklahvidena.

![Otsingu kiirklahvide konfigureerimine](./media/ConfigureShortcutsAX.png "Otsingu kiirklahvide konfigureerimine")

> [!NOTE]
> Kui lisate liiga palju kiirklahve, muutub kassa otsinguriba rippmenüü ülekoormatuks ja töötajate otsingu tõhusus võib väheneda. Soovitame lisada vaid nii palju kiirklahve, kui vaja.

Väli **Kuvamisjärjestus** määratleb, millises järjekorras kiirklahve kassas kuvatakse. Näidatud kriteeriumid on valmisatribuudid, mida kliendiotsingu algoritm kasutab klientide otsimiseks. Kuid partnerid saavad lisada kohandatud atribuute otsingu kiirklahvidena. Kohandatud atribuutide lisamiseks otsingu kiirklahvidena peab süsteemiadministraator laiendama laiendavat loetelu, mida kasutatase kliendiotsingu kriteeriumiks ja seejärel märkima partneri kohandatud atribuudid kiirklahvidena. Kui otsingute jaoks kasutatakse partnerite kohandatud kiirklahve, on partnerid vastutavad tulemeid leidva koodi kirjutamise eest.

> [!NOTE]
> Loetellu lisatud kohandatud atribuut ei mõjuta standardset kliendiotsingu algoritmi. Teisisõnu, kliendiotsingu algoritm ei otsi kohandatud atribuudist. Kasutajad saavad kohandatud atribuuti otsingute jaoks kasutada ainult siis, kui kohandatud atribuut on lisatud kiirklahvina või otsingu vaikealgoritm on alistatud.
