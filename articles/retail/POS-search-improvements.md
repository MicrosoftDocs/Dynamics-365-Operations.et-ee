---
title: Tooteotsing ja kliendi otsing kassas
description: "Selles teemas antakse ülevaade toote ja kliendi otsingufunktsiooni täiustustest rakenduses Dynamics 365 for Retail."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 08/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 2af45de0d63b01e71b5009e2f62cfdff6844da7d
ms.contentlocale: et-ee
ms.lasthandoff: 02/07/2018

---

# <a name="overview-of-product-and-customer-search-in-point-of-sale"></a>Ülevaade toote ja kliendi otsingust kassas

[!include[banner](includes/banner.md)]

Modern Point of Sale (MPOS) ja pilvekassa (CPOS) pakuvad hõlpsasti kasutatavat otsingufunktsiooni, mis võimaldab kaupluse töötajatel kiiresti tooteid ja kliente otsida. MPOS-i ja CPOS-i ülaosas on alati otsinguriba, et töötajad saaksid tooteid ja kliente kiiresti otsida.

Töötajad saavad otsida tooteid praeguse kauplusega seostatud sortimentidest ja kataloogidest ning ettevõtte mõne teise kauplusega seostatud sortimentidest ja kataloogidest. Seega saavad kassapidajad müüa ja tagastada ka kaupluse sortimendist väljaspool olevaid tooteid. Samamoodi saavad töötajad otsida praeguse kaupluse või ettevõtte mõne teise kauplusega seotud kliente. Lisaks saavad töötajad otsida emaorganisatsiooni teise ettevõttega seostatud kliente.

## <a name="product-search"></a>Toote otsing 

Vaikimisi toimub tooteotsing kaupluse sortimendist. Seda tüüpi otsingut nimetatakse *kohalikuks tooteotsinguks*. Kuid töötajad saavad minna hõlpsasti üle mis tahes selle kauplusega seotud kataloogi või otsida teisest kauplusest. Seda tüüpi otsingut nimetatakse *toote kaugotsinguks*. Kataloogi vahetamiseks valige lehe vasakult poolelt nupp **Kategooriad**. Valige kuvatava paani ülaosast nupp **Vaheta kataloogi** ja valige siis sirvimiseks mõni saadaolev kataloog. Süsteem otsib tooteid valitud kataloogist.

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

Kohalike tooteotsingute kogemus on tehtud kasutajasõbralikumaks. Tehtud on ka järgmised täiustused.

- Otsinguribale on lisatud toote ja kliendi rippmenüüd, et töötajad saaksid valida enne otsimist **toote** või **kliendi**. Vaikimisi on valitud **Toode**, nagu on näha järgmisel illustratsioonil.
- Mitme märksõnaga otsingute puhul (st otsingusõnu kasutavate otsingute puhul) saavad jaemüüjad konfigureerida, kas otsingutulemused sisaldavad mõnele või ainult kõigile otsingusõnadele vastavaid tulemusi. See säte on saadaval kassa funktsiooniprofiilis uue grupi all, mille nimi on **Tooteotsing**. Vaikesäte on **Mis tahes otsingusõnade vastendamine**. See säte on ka soovitatav säte. Kui kasutatakse sätet **Mis tahes otsingusõnade vastendamine**, antakse tulemuseks kõik tooted, mis vähemalt ühele otsingusõnale vastavad, ja tulemused sorditakse automaatselt, lisades kasvavas järjestuses tooted, millel on kõige rohkem märksõnade (täielikke või osalisi) vasteid.

    Säte **Kõigi otsingusõnade vastendamine** annab ainult tooted, mis vastavad kõigile otsingusõnadele (täielikult või osaliselt). Sellest sättest on abi, kui toodete nimed on pikad ja töötajad soovivad näha otsingutulemustes ainult piiratud tooteid. Kuid seda tüüpi otsingul on kaks piirangut.

    - Otsing toimub eraldi tooteatribuutidel. Näiteks antakse tulemuseks ainult need tooted, millel on vähemalt ühes tooteatribuudis kõik otsitud märksõnad.
    - Dimensioonidest ei otsita.

- Nüüd saavad jaemüüjad konfigureerida tooteotsingu nii, et kui kasutajad tootenimesid tipivad, siis kuvatakse otsingusoovitused. Selle funktsiooni uus säte on saadaval kassa funktsiooniprofiilis grupi all, mille nimi on **Tooteotsing**. Sätte nimi on **Näita tippimise ajal otsingusoovitusi**. See funktsioon aitab töötajatel otsitavat toodet kiiresti leida, kuna nad ei pea kogu nime käsitsi tippima.
- Tooteotsingu algoritm otsib nüüd otsitud sõnu toote atribuudist **Otsingunimi**.

![Tootesoovitused](./media/Productsuggestions.png "Tootesoovitused")

## <a name="customer-search"></a>Kliendi otsing

Kliendiotsingut kasutatakse klientide otsimiseks mitmesugusel eesmärgil. Näiteks võib kassapidajatel olla vaja vaadata kliendi soovinimekirja või ostuajalugu või lisada klienti kandesse. Mitme märksõnaga otsingute puhul annab kliendiotsingu algoritm tulemuseks kõik kliendid, kes mõnele otsitud märksõnale vastavad. Kuid kliendid, kes vastavad enamikule märksõnadest, kuvatakse tulemuste alguses. See sarnaneb viisile, kuidas teised otsingumootorid tulemusi kuvavad. Esmalt kuvavad need tulemused, mis ühtivad enamiku otsingusõnadega, ja seejärel otsingu märksõnadele osaliselt vastavad tulemused. See aitab kassapidajaid olukordades, kus nad kasutavad otsingus mitut märksõna, kuid ühes märksõnas on kirjaviga.

Vaikimisi toimub kliendiotsing kauplusega seotud klientide aadressiraamatutest. Seda tüüpi otsingut nimetatakse *kohalikuks kliendiotsinguks*. Kuid töötajad saavad otsida kliente ka globaalselt. Teisisõnu saavad nad otsida kõigist ettevõtte kauplustest või teistest juriidilistest isikutest. Seda tüüpi otsingut nimetatakse *kliendi kaugotsinguks*.

Globaalseks otsimiseks saavad töötajad valida nupu **Filtreeri tulemusi** lehe alumisest osast ja siis valiku **Otsing kõigist kauplustest**, nagu on näidatud järgmisel illustratsioonil. Sellisel juhul ei kuvata tulemustes ainult kliente. Kuvatakse ka kõik osapoolte tüübid, kes mõnda peakontori aadressiraamatusse kuuluvad. Nende osapoolte hulka kuuluvad töötajad, hankijad, kontaktid ja konkurendid.

> [!NOTE]
> Selleks, et kliendi kaugotsing annaks tulemusi, tuleb sisestada vähemalt neli märki.

Kliendi kaugotsingus ei kuvata kliendi ID-d teistest juriidilistest isikutest pärinevate klientide puhul, kuna nendele osapooltele pole selles ettevõttes kliendi ID-d loodud. Kuid kui töötaja avab kliendi andmete lehe, loob süsteem sellele osapoolele automaatselt kliendi ID ja seostab kliendiga ka kaupluse klientide aadressiraamatud. Seega on see klient hiljem toimuvates kaupluse kohalikes otsingutes nähtav.

![Globaalne kliendi otsing](./media/Globalcustomersearch.png "Globaalne kliendi otsing")

### <a name="enhancements-to-local-customer-searches"></a>Kohalike kliendiotsingute täiustused

Kohalikud kliendiotsingud aitavad töötajatel kliente kiiresti telefoninumbri järgi leida. Töötajad ei pea tippima kliendi telefoninumbrisse lisatud erimärke, nt tühikuid, sidekriipse või sulge. Kuigi kassapidajad saavad salvestada telefoninumbreid igasuguses vormingus (nt saavad nad lisada sulge, sidekriipse, sümboleid jne), saavad nad otsida kliente, sisestades telefoninumbri osa. Kui kassapidaja lisas telefoninumbri sisestamisel erimärke, leiavad teised kassapidajad kliendi, tippides pärast erimärke kuvatavad numbrid. Näiteks kui kliendi telefoninumber sisestati kujul **123-456-7890**, saab kassapidaja klienti otsida, tippides **123**, **456**, **7890** või **1234567890** või sisestades telefoninumbrist paar esimest numbrit.

