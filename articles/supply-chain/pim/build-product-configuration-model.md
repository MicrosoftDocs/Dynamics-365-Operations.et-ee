---
title: Toote konfiguratsiooni ülevaade
description: Erinõuetele vastamiseks toodete konfigureerimise vajadus on saamas erandist reegliks nii ettevõtetevahelistes kui ka ettevõtte ja tarbija vahelistes suhetes.
author: cvocph
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails, ConfigPartOf
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 75083
ms.assetid: f08072b8-cb0b-43aa-9509-f5ec32caecd9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b7d1186b4141a18e1283505713e67018927672d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425919"
---
# <a name="product-configuration-overview"></a>Toote konfiguratsiooni ülevaade

[!include [banner](../includes/banner.md)]

Erinõuetele vastamiseks toodete konfigureerimise vajadus on saamas erandist reegliks nii ettevõtetevahelistes kui ka ettevõtte ja tarbija vahelistes suhetes.

Tootjal, kes toetab tellimisel konfigureeritav tüüpi stsenaariume, on võimalus paremini kliendi vajadustele vastata. Lisaks saab tootja vähendada varudega seotud kapitali, varudes valmistoodete asemel pooltooteid üldiste komponentidena.  

Edukas liikumine seadistuselt toodang lattu seadistusele tellimisel konfigureeritav nõuab hoolikat tootestruktuuride analüüsi, tootesarjade tuvastamist ja komponentiseerimist. Protsessis olevate osade arvu vähendamiseks ja kaupade arvu minimeerimiseks on väga oluline, et mõistate toote liideseid ja et kujundate korduvkasutust silmas pidades.  

On olemas mitmeid tootekonfiguratsiooni modelleerimise põhimõtteid, nagureeglipõhine, dimensioonipõhine ja piirangupõhine modelleerimine. Uuringud näitavad, et piirangupõhine meetod võib vähendada koodiridade arvu mudelites umbes 50 protsendi võrra võrrdeldes muude modelleerimispõhimõtetega. Seega võib see meetod vähendada omanduse kogukulu (TCO). Minnes reeglipõhiselt mudelilt, mille aluseks on kood X++, üle piirangupõhisele mudelile, ei ole teil enam vaja arendaja litsentsi tootemudelite säilitamiseks.

## <a name="product-configuration"></a>Toote konfiguratsioon
Industrialiseerimisajastu on viinud suurte saavutusteni kvaliteetsete ja funktsioonirohkete toodete tootmisel taskohase hinnaga. Mastaabisääst võimaldab enamikul industrialiseerunud riikide inimestel osta autosid, telereid, kodumasinaid ja muid kaupu, mida enamik meist peab igapäevaelu oluliseks osaks.  

Paljude toodete tarbeesemeteks muutumine tõstatab nende eristamise vajaduse. Tootjate kohene vastus sellele väljakutsele on olnud igale tootele variantide loomine, nii et klientidel on rohkem alternatiive. See strateegia on suurendanud väljakutseid prognoosidele, samuti on suurenenud kaubavarude kulud ning aegunud müümata toodete arv.  

Tellimisel konfigureeritava filosoofia kasutuselevõtul on tootjatel võimalus vastata kliendi nõudmistele ainulaadsete toodete osad, vähendades või kõrvaldades samas aegunud laokaupu. Kui toodang lattu filosoofia viiakse üle tellimisel konfigureeritavale filosoofiale, tõstatub kohe väljakutse, et vajadus lühikeste täitmisaegade järele tuleb tasakaalustada madalate kaubavarude tasemetega.  

Edu valem on siinkohal tooteportfoolio hoolikas analüüs ja mustrite otsimine tootefunktsioonides ning protsessides. Eesmärk on tuvastada üldiseid komponente, mida saab toota sama varustusega ja kasutada kõikide varantide puhul.  

Uus funktsioonikomplekt Toote konfigureerimine hõlmab kasutajaliidest (UI), mis annab toote konfiguratsioonimudeli struktuurist visuaalse ülevaate, ja deklaratiivset piirangusüntaksit, mis ei pea olema koostatud. Seetõttu on lihtsam alustada ettevõtetel, mis soovivad toetada konfigureerimistava. Nagu järgmises jaotises selgitatakse, ei vaja toote kujundaja enam arendaja tuge toote konfiguratsioonimudeli loomisel, selle testimisel ja müügiorganisatsioonile väljastamisel.

## <a name="building-a-product-configuration-model"></a>Toote konfiguratsioonimudeli koostamine
On mitmeid lähenemisi, mida kasutaja saab toote konfiguratsioonimudeli loomisel kasutada. Üks võimalus on järgida järjestikust voogu, luues esmalt kõik viiteandmed, nagu tooteetalonid, eristatavad tooted ja operatsiooniressursid, ning lisades need seejärel komponentidena, koosluse ridadena, protsessi operatsioonidena ja muude toote konfiguratsioonimudeli elementidena. Teise võimalusena saate valida iteratiivsema lähenemise, luues esmalt mudeli ja lisades vajaduse tekkimisel viiteandmed.

### <a name="components"></a>Komponendid

Toote konfiguratsioonimudel koosneb ühest või mitmest komponendist, mis on alamkomponendi suhte kaudu seotud. Komponendid määratletakse ühe korra ja neid saab siis mitu korda ühes või mitmes toote konfiguratsioonimudelis kasutada. Komponendid on toote konfiguratsioonimudeli peamised ehitusplokid ja peaaegu kogu teave mudeli kohta on nendega seotud.

### <a name="attributes"></a>Atribuudid

Igal komponendil on üks või mitu omadus(t), mille järgi tuvastada selle atribuute. Atribuute valivad kasutajad konfigureerimisprotsessi ajal. Atribuudid juhivad nii komponentidevahelisi kui ka komponendisiseseid suhteid piirangutesse või arvutustesse kaasamise teel. Koosluse ridadele rakendatud tingimuste kaudu saab atribuute kasutada, et määrata, millistest füüsilistest osadest konfigureeritud toode koosneb. Lisaks saab atribuut juhtida koosluse rea atribuuti vastendamismehhanismi kaudu. Sarnane funktsioon on olemas protsessi operatsioonide jaoks, puudutades nii kaasamist kui ka atribuudi sätteid.

>[!NOTE]
> Atribuuditüüpide loomisel vältige atribuudi tüübi domeenile suure hulga väärtuste loomist. See võib aeglustada toote konfigureerijat. 

### <a name="expression-constraints"></a>Avaldise piirangud

Piirangupõhise toote konfiguratsioonimudeli kasutamine tähendab, et on mõned piirangud, kui kasutaja valib väärtused erinevatele atribuutidele. Selliseid piiranguid saab juurutada avaldise piirangutena, kasutades optimeerimise modelleerimiskeelt (OML). Teise võimalusena saab piirangut juurutada tabelipiirangu vormis.

### <a name="table-constraints"></a>Tabeli piirajad

Tabelipiirangud võivad olla kas kasutaja või süsteemi määratletud.  

Kasutaja määratletud tabeli piirang on kasutaja loodud. Kasutaja valib tabeli veergude esindamiseks atribuuditüüpide kombinatsiooni ja sisestab siis väärtused valitud atribuuditüüpide domeenidest, et moodustada tabeli piirangus ridu.  

Süsteemi määratletud tabelipiirangu määratlemiseks valitakse, millist tabelit viitena kasutada, ja seejärel valitakse sellest tabelist väljad, et moodustada piirangu veerud. Tabelipiirangu read on tabeli Supply Chain Management read, mis on saadaval konfigureerimise ajal.  

Tabelipiirang on lisatud toote konfiguratsioonimudelile, viidates tabelipiirangu määratlusele ja vastendades asjakohased mudeli atribuudid tabelipiirangu veergudega.

### <a name="calculations"></a>Arvutamised

Arvutused näitavad artimeetiliste operatsioonide tegemise mehhanismi konfiguratsioonimudelis. Näiteks võib arvutus määrata toormaterhali kindla tüki pikkuse või poleerimistoimingu tööaja. Arvutused on kohustuslikud ja määravad sihtatribuudi väärtuse, kui kõik arvutamise avaldisse lisatud atribuudi väärtused saavad kättesaadavaks.

### <a name="subcomponents"></a>Alamkomponendid

Alamkomponendid näitavad toote konfiguratsioonimudeli struktuuri sõlmi. Iga alamkomponendi seose kohta tuleb määrata viide tooteetalonile, mille variandikonfiguratsiooni tehnoloogia on seadistatud piirangupõhisele konfiguratsioonile.

### <a name="user-requirements"></a>Kasutaja nõuded

Kasutajanõudel on kõik alamkomponendi koostisosad. Ainus erinevus on see, et kasutajanõue ei ole seotud tooteetaloniga. Selle erinevuse tegelik mõju on see, et kasutajanõude kontekstis määratletud mis tahes koosluse read või protsessi operatsioon ahendatakse emakomponendi koosluse struktuuri või protsessi. See käitumine sarnaneb fiktiivse koosluse käitumisele.

### <a name="bom-lines"></a>Koosluseread

Koosluse read lisatakse iga komponendi jaoks tootmiskoosluse tuvastamiseks. Koosluse rida peab viitama kaubake ja kõik kauba atribuudid saab seada fikseeritud väärtusele või vastendada atribuudiga.

### <a name="route-operations"></a>Protsessitoimingud

Protsessi operatsioonid lisatakse tootmisprotsessi tuvastamiseks. Protsessi operatsioon peab viitama määratletud operatsioonile ja kõigile operatsiooni atribuutidele saab määrata fikseeritud väärtuse. Kõiki atribuute, v.a ressursi nõudeid, saab vastendada väärtuse asemel atribuudiga.

## <a name="validating-and-testing-a-product-configuration-model"></a>Toote konfiguratsioonimudeli kinnitamine ja testimine
Toote konfiguratsioonimudeli kinnitamine võib ilmneda mudeli mitmel tasemel ja võib seega katta erinevaid ulatusi. Madalaim tase on ühe avaldise piirang. Sel juhul viib kinnitamise tavaliselt läbi toote koostaja kinnitamaks, et avaldise süntaks on õige.  

Sarnaselt saab koosluse rea või protsessi operatsiooni tingimust kinnitada eraldi.  

Kinnitada saab ka kasutaja määratletud tabelipiirangu definitsiooni. Sel juhul saab kasutaja kinnitada, et igale väljale sisestatud väärtused on vastavate atribuudi tüüpide domeenis.  

Viimase võimalusena saab kinnitada lõpule viidud toote konfiguratsioonimudelit kinnitamaks, et kogu süntaks on õige ja et kõiki nime panemise ja mudeldamise reegleid on järgitud.

### <a name="testing"></a>Testimine

Mudeli testimine sarnaneb tegeliku konfiguratsiooniseansi käitamisele. Kasutaja saab konfiguratsioonilehed läbi käia ja kinnitada, et mudeli struktuur toetab konfiguratsiooniprotsessi. Kasutaja saab kinnitada, et atribuudi väärtused on õiged ja et atribuudi kirjeldused juhivad kasutaja valima õigeid väärtusi. Lõpuks, kui testseanss on lõpule viidud, püüab süsteem luua koosluse ja protsessi, mis vastab valitud atribuudi väärtustele, ning esitab tõrketeate, kui midagi läheb valesti.

### <a name="the-configuration-page"></a>Konfiguratsiooni leht

Komponentide vahel liikumiseks klõpsake suvandit **Edasi** või klõpsake komponenti toote konfiguratsioonimudeli puus, et sellele fokuseerida.

## <a name="finalizing-a-model-for-configuration"></a>Mudeli lõpetamine konfiguratsiooniks
Kui toote konfiguratsioonimudel on valmis stsenaariumides tellimusel konfigureeritav kasutamiseks, tuleb luua versioon. Siiski on mitmeid võimalusi, mis võivad mudeldamiskogemust täiustada.

### <a name="user-interface"></a>Kasutajaliides

Konfiguratsiooni kasutajaliidest saab muuta, kasutades atribuudigruppe ühes või mitmes alamkomponendis. Selline rühmitamine tõstab esile seosed kindlate atribuutide vahel ja aitab konfiguratsiooni kasutajal tuvastada fookuses oleva toote valdkonda.

### <a name="templates"></a>Mallid

Konfigureerimisprotsessi kiirendamiseks saab luua ühe või mitu konfiguratsioonimalli. Teise võimalusena saab malle luua kindlate atribuudikombinatsioonide ülendamiseks, nt kui müügikampaania keskendub kindlale tootefunktsioonide komplektile.

### <a name="translations"></a>Tõlked

Kui toodet müüakse erinevas riigis/regioonis, saab luua tõlked kogu tekstile, mis ilmub konfiguratsiooni kasutajaliideses. Tekst hõlmab lisaks nime ja kirjelduse väljadele ka atribuudi teksti väärtusi.

### <a name="versions"></a>Versioonid

Viimane ja kõige olulisem etapp lõpetamisprotsessis on luua toote konfiguratsioonimudeli versioon. Versioon esindab seost tooteetaloni, mille saab konfiguratsioonile valida tellimuse või pakkumise real, ja toote konfiguratsioonimudeli vahel. Versioon tuleb kinnitada ja aktiveerida enne selle kasutamist konfiguratsiooniseansil.

## <a name="extending-a-product-configuration-model-through-the-api"></a>Toote konfiguratsioonimudeli laiendamine API kaudu
Juurutatud on sihtotstarbeline rakenduse programmiliides (API), nii et partnerid ja teised, kellel on arendaja litsents, saavad laiendada toote konfiguratsioonimudeli võimalusi. Peamine eesmärk on olnud luua mehhanism, mis võimaldab partnetitel ja klientidel, kes kasutavad olemasolevat tootekonstruktorit, kanda üle tootekonstruktori mudelitesse manustatud koodi API-sse. Sel moel saavad nad mudelid tootekonstruktorist toote konfiguratsiooni üle kanda. Kuid uued partnerid ja kliendid võidavad samuti API kasutamisest uute toote konfiguratsioonimudelite laiendamiseks.

### <a name="pcadaptor-class"></a>Klass PCAdaptor

API juurutatakse, kasutades klasside **PCAdaptor** komplekti, mis kasutab toote konfiguratsioonimudelite andmestruktuuri. Iga laiendatava mudeli jaoks tuleb luua klassi **PCAdaptor** eksemplar. Pärast konfigureerimisseansi lõpetamist otsib süsteem selle klassi eksemplari ja käivitab selle, kui see leitakse.  

Järgmine voodiagramm kirjeldab protsessi.  

[![Voodiagramm](./media/product_configuration_2.png)](./media/product_configuration_2.png)  

Toote konfiguratsiooni-API voodiagramm

## <a name="product-configuration"></a>Toote konfiguratsioon
Toote konfiguratsiooni saab läbi viia järgmistest kohtadest.

-   Müügitellimuse rida
-   Müügipakkumise rida
-   Ostutellimuse rida
-   Tootmistellimuse rida
-   Kaubavajaduse rida (projekt)

Konfiguratsiooni eesmärk on luua kliendi nõuetele vastav toote eristav variant. Igale uuele konfiguratsioonile luuakse kordumatu ID. See ID võimaldab lao kaudu jälgimist.

### <a name="multiple-sites-and-intercompany"></a>Mitu laoala ja kontsernisisesus

Kui konfiguratsioon tehakse laoalal või ettevõttes, mis ei ole laoala või ettevõte, kus toimub tootmine, luuakse kooslus ja protsess tarneettevõtte tarnija laoalale. Tootevariant antakse välja kõikides ettevõtetes, mis osalevad tarneahelas.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]