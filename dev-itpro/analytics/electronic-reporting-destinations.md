---
title: Elektroonilise aruandluse sihtkohad
description: "Saate konfigureerida sihtkoha igale elektroonilise aruandluse (ER) vormingu konfiguratsioonile ja selle väljundi komponendile (kaust või fail). Kasutajad, kellele on antud sobilikud juurdepääsuõigused, võivad sihtkoha sätteid ka käitusajal muuta. Selles artiklis selgitatakse ER-i sihtkoha haldust, toetatud sihtkohtade tüüpe ja turbekaalutlusi."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: d38d05fe445bf0326d408038dff84ccf8c0ff64c
ms.lasthandoff: 03/31/2017


---

# <a name="electronic-reporting-destinations"></a>Elektroonilise aruandluse sihtkohad

Saate konfigureerida sihtkoha igale elektroonilise aruandluse (ER) vormingu konfiguratsioonile ja selle väljundi komponendile (kaust või fail). Kasutajad, kellele on antud sobilikud juurdepääsuõigused, võivad sihtkoha sätteid ka käitusajal muuta. Selles artiklis selgitatakse ER-i sihtkoha haldust, toetatud sihtkohtade tüüpe ja turbekaalutlusi.

Elektroonilise aruandluse (ER) vormingu konfiguratsioonid sisaldavad tavaliselt vähemalt ühte väljundkomponenti: faili. Tavaliselt sisaldavad konfiguratsioonid mitut erinevat tüüpi faili väljundkomponenti (nt XML, TXT või XLSX), mis on rühmitatud ühte või mitmesse kausta. ER-i sihtkoha haldus võimaldab eelkonfigureerida, mis iga komponendi käitamisel toimub. Vaikimisi konfiguratsioon käivitamisel kuvatakse dialoogiboks mis võimaldab kasutajal salvestada või avada faili. Sama toimub ka siis, kui importida ER-i konfiguratsioon ja mitte konfigureerida sellele ühtegi konkreetset sihtkohta. Pärast peamisele väljundkomponendile sihtkoha loomist alistab see sihtkoht vaikekäitumise ja kaust või fail saadetakse sihtkoha sätete kohaselt.

## <a name="availability-and-general-prerequisites"></a>Kättesaadavus ja üldised eeltingimused
ER sihtkohta funktsioonid pole saadaval Microsoft Dynamics 365 lubamise toimingute 7.0 (veebruar 2016). Seetõttu peate installima Microsoft Dynamics 365 operatsioonide (November 2016 release) kasutada kõiki funktsioone, mida on kirjeldatud selles teemas. Teise võimalusena saab paigaldada üks järgmised eeltingimused. Siiski tuleb nende asemel pakkuda piiratud ER sihtkoha kogemus.

-   Microsoft Dynamics 365 toimingute rakenduse versioon 7.0.1 (mai 2016)
-   ER-i sihtkoha halduse [rakenduse kiirparandus](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

Võite seadistada sihtkohad ainult imporditud ER-i konfiguratsioonidele ja vormingutele, mis on saadaval lehel **Elektroonilise aruandluse konfiguratsioonid**.

## <a name="overview"></a>Ülevaade
ER sihtkoha juhtimine funktsioonid on saadaval **organisatsiooni haldamine**&gt;**elektrooniline**. Siin saab alistada konfiguratsiooni vaikekäitumise. Imporditud konfiguratsioone ei kuvata siin enne, kui klõpsate valikut **Uus** ja valite siis väljal **Viide** konfiguratsiooni, millele sihtkoha sätted luua.

[![Valige konfiguratsioon väljal viide](./media/ger-destinations-2-1611-1024x574.jpg)](./media/ger-destinations-2-1611.jpg) 

Pärast viite loomist saate luua faili sihtkohta iga kausta või faili. 

[![Luua faili sihtkohta](./media/ger-destinations-1611-1024x586.jpg)](./media/ger-destinations-1611.jpg)

**Märkus.** Saate luua ühe faili sihtkoha igale sama vormingu väljundkomponendile (kaustale või failile), mis on valitud väljal **Faili nimi**. Saab siis lubada ja keelata üksikute sihtkohta faili sihtkohta ning **sihtkoha seaded** dialoogiboksis. Nuppu **Sätted** kasutatakse valitud faili sihtkohtade juhtimiseks. Dialoogiboksis **Sihtkoha sätted** saate iga sihtkohta eraldi juhtida, tehes sellele valiku **Lubatud**.

[![Sihtkoha sätete dialoogiboksi](./media/ger-destinations-settings-1611-1024x589.jpg)](./media/ger-destinations-settings-1611.jpg)

## <a name="destination-types"></a>Sihtkoha tüübid
Toetatakse mitmesugust tüüpi sihtkohti. Saate keelata või lubada kõik tüübid üheaegselt. Sel viisil võite mitte midagi teha või saata komponendi kõigisse konfigureeritud sihtkohtadesse. Järgmised jaotised kirjeldavad toetatud sihtkohti.

### <a name="email-destination"></a>Meili sihtkoht

Määrake valiku **Lubatud **väärtuseks **Jah** väljundfaili saatmiseks meiliga. Pärast seda, kui see on lubatud, saate määrata adressaadile e-posti ja redigeerige sõnumi teemat ja keha e-kirja. Seadistage pidev tekstid, e-kirja teemat ja keha või ER valemeid saate kasutada dünaamiliselt luua e-posti tekstid. Saate konfigureerida e-posti aadressid ER kahel viisil. Konfiguratsiooni saab valmis Dynamics 365 operatsioonide Print halduse funktsioon lõpetab see samamoodi. Teise võimalusena saate e-posti aadressi lahendamiseks kasutada ER konfiguratsiooni kaudu valemi otseviitega.

### <a name="email-address-types"></a>E-posti aadressi tüübid

Kui klõpsate **muuta** jaoks on **et** või **koopia** välja, on **e-** dialoogiboks. Seejärel saate meiliaadressi kasutada tüüpi.

[![Dialoogiboksis e-posti](./media/ger-destinations-email-1-1611-1024x588.jpg)](./media/ger-destinations-email-1-1611.jpg)

#### <a name="print-management"></a>Prindihaldus

Kui valite selle **prindihalduse e-posti** liik, saate sisestada fikseeritud meiliaadressid on **et** välja. E-posti aadressid, mis ei ole määratud kasutamiseks valige e-posti allika liik faili sihtkohta. Toetatakse järgmisi väärtusi: **kliendi**, **hankija**, **väljavaade**, **kontakt**, **konkurent**, **töötaja**, **taotleja**, **tulevane müük**, ja **pole lubatud hankija**. Valige e-posti allika liik, kasutada nupu kõrval on **e-posti konto allikas** välja avamiseks on ** valemi disainer ** vormi. Selle vormi abil saate lisada valemi, mis tähistab valitud tootja konto e-posti sihtkohta.

[![Konfigureerida prindihalduse meilisõnumi tüüp](./media/ger-destinations-email-2-1611-1024x588.jpg)](./media/ger-destinations-email-2-1611.jpg) 

Pange tähele, et valemid on ER-i konfiguratsiooni põhised. Sisestage väljale **Valem** dokumendipõhine viide kliendi või hankija osapoole tüübile. Tippimise asemel võite otsida üles andmeallika sõlme, mis tähistab kliendi või hankija kontot, ja klõpsata siis valemi värskendamiseks nuppu **Lisa andmeallikas**. Näiteks kui kasutate ISO 20022 kreeditülekande konfiguratsiooni, tähistab hankija kontot sõlm **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID**. Vastasel korral sisestage valemi salvestamiseks stringi väärtus, nagu **DE-001**.

[![Formula designer](./media/ger_formuladesignerfordestination-1024x541.jpg)](./media/ger_formuladesignerfordestination.jpg)

Linnas on **e-** dialoogiboksis klõpsake nuppu prügikasti kõrval on **e-posti konto allikas** välja valem allikas konto jäädavalt kustutada. Teise võimalusena avamist valem valem, mis oli varem salvestatud muuta. E-posti aadresside määramiseks klõpsake **muuta** avamiseks ning **määramine e-posti aadressid** dialoogiboksis.

[![E-posti aadressid, e-posti sihtkoha määramine](./media/ger-destinations-email-3-1611-1024x587.jpg)](./media/ger-destinations-email-3-1611.jpg)

#### <a name="configuration-email"></a>Konfigureerimismeil

Kasutada sellist e-posti, kui konfiguratsiooni, mida kasutada on andmeallikate sõlme, mis moodustab e-posti aadress. Saate andmeallikate ja ülesanded valemi kujundaja õigesti vormindatud e-posti aadressi.

[![E-posti aadressi andmete allikas e-posti sihtkoha määramine](./media/ger-destinations-email-4-1611-1024x587.jpg)](./media/ger-destinations-email-4-1611.jpg) 

**Märkus.** Simple Mail Transfer Protocoli (SMTP) server peab olema konfigureeritud ja saadaval. Võite määrata oma SMTP-serveri Dynamics 365 korral sel **süsteemi halduse**&gt;**install**&gt;**e-posti**&gt;**e-posti parameetrid**.

### <a name="archive-destination"></a>Arhiivi sihtkoht

Selle valiku abil saab saata väljundi Microsoft SharePointi kausta või Microsoft Azure’i salvestusruumi. Määrake valiku **Lubatud** väärtuseks **Jah **väljundi saatmiseks valitud dokumenditüübiga määratletud sihtkohta. Valida saab ainult neid dokumenditüüpe, millel grupiks on määratud **Fail**. Saate määratleda dokumendi tüübiga kokku **organisatsiooni haldamine**&gt;**Dokumendihaldus**&gt;**dokumendi liiki**. ER-i sihtkohtade konfiguratsioon on sama, mis dokumendihaldussüsteemi konfiguratsioon.

[![Dokumendi liigid lehele](./media/ger_documenttypefile-1024x542.jpg)](./media/ger_documenttypefile.jpg) 

Asukoht määrab, kuhu fail salvestatakse. Pärast selle **Arhiiv** alal on lubatud, konfiguratsiooni täitmise tulemused salvestatakse töö Arhiiv. Tulemused kuvatakse **organisatsiooni haldamine**&gt;**elektrooniline**&gt;**elektrooniline arhiveeritud Tööpakkumised**. **Märkus:** valige dokumenditüübi töö Arhiiv Dynamics 365 korral kell **organisatsiooni haldamine**&gt;**tööruumide**&gt;**elektrooniline**&gt;**elektroonilise aruandluse parameetrid**.

#### <a name="sharepoint"></a>SharePoint

Faili saab salvestada selleks mõeldud SharePointi kausta. Saate määratleda vaikimisi SharePointi serverisse **organisatsiooni haldamine**&gt;**Dokumendihaldus**&gt;**dokumendihalduse parameetrite**, on **SharePointi** vahekaart. Pärast SharePointi kausta konfigureerimist valige see kaust, kuhu salvestatakse väljund ER dokumenditüübi. 

[![Valige SharePointi kaust](./media/ger_sharepointfolderselection-1024x543.jpg)](./media/ger_sharepointfolderselection.jpg) 

#### <a name="azure-storage"></a>Azure’i salvestusruum

Kui dokumenditüübi asukohaks on määratud **Arhiivikaust**, saab salvestada faili Azure’i salvestusruumi.

### <a name="file-destination"></a>Faili sihtkoht

Kui seate **lubatud** et **Jah**an open või save dialoogiboks kuvatakse, kui konfiguratsioon on töö lõpetanud.

### <a name="screen-destination"></a>Ekraani sihtkoha

Kui seate **lubatud** et **Jah**, eelvaade väljund luuakse. Mõned failitüübid, nagu XML, TXT või PDF, saate vaadata otse brauseriaknas. Muid failitüüpe, selline Microsoft Excelis või Wordis, kasutatakse Office Online'i teenuseid.

### <a name="power-bi-destination"></a>Power BI sihtkoha

Seada **lubatud** et **Jah** ER konfiguratsiooni abil saate korraldada oma eksemplari Dynamics 365 andmete edastamise toimingute Microsoft Power BI teenused. Edastatud failid on salvestatud Microsoft SharePoint Serveri eksemplari, mis peab olema selleks konfigureeritud. Lisateabe saamiseks vaadake [pakub Power BI andmetega Dynamics 365 meetmeteks elektroonilise aruandluse konfiguratsiooni abil](general-electronic-reporting-report-configuration-get-data-powerbi.md). **Vihje.** Vaikekäitumise (st konfigureerimise dialoogiboksi) alistamiseks võite luua peamisele väljundkomponendile sihtkoha viite ja faili sihtkoha ning keelata siis kõik sihtkohad.

## <a name="security-considerations"></a>Turbemeetmed
ER-i sihtkohtade puhul kasutatakse kahesuguseid õigusi ja kohustusi. Üks tüüp reguleerida säilitada üldine sihtkohtadesse, juriidilise isiku jaoks konfigureeritud (st kontrollib juurdepääsu ning **elektroonilise aruandluse sihtkohta** leht). Teine juhib rakenduse kasutaja võimalust alistada käitusajal sihtkoha sätted, mille on konfigureerinud ER-i arendaja või ER-i funktsionaalne konsultant.

| Roll (AOT-nimi)                     | Rolli nimi                                  | Kohustus (AOT-nimi)                     | Kohustuse nimi                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Elektroonilise aruandluse arendaja             | ERFormatDestinationConfigure        | Elektroonilise aruandluse vormingu sihtkoha konfigureerimine                |
| ERFunctionalConsultant              | Elektroonilise aruandluse funktsionaalne konsultant | ERFormatDestinationConfigure        | Elektroonilise aruandluse vormingu sihtkoha konfigureerimine                |
| PaymAccountsPayablePaymentsClerk    | Ostureskontro maksuametnik            | ERFormatDestinationRuntimeConfigure | Elektroonilise aruandluse vormingu sihtkoha konfigureerimine käitusaja jooksul |
| PaymAccountsReceivablePaymentsClerk | Müügireskontro maksuametnik         | ERFormatDestinationRuntimeConfigure | Elektroonilise aruandluse vormingu sihtkoha konfigureerimine käitusaja jooksul |

**Märkus.** Kahte õigust kasutatakse eelnevates kohustustes. Nendel õigustel on samad nimed, mis vastavatel kohustustel: **ERFormatDestinationConfigure** ja **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused
### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Olen importinud elektroonilised konfiguratsioonid ja näen neid lehel Elektroonilise aruandluse konfiguratsioonid. Aga miks ma ei näe neid elektroonilise aruandluse sihtkohta lehel?

Veenduge, et klõpsate **uus** ja valige konfiguratsioon ja selle **viide** välja. Lehel **Elektroonilise aruandluse sihtkohad** näete ainult neid konfiguratsioone, mille jaoks sihtkohad on konfigureeritud.

### <a name="is-there-any-way-to-define-which-azure-storage-account-and-azure-blob-storage-are-used"></a>Kas kuidagi määratleda, milliseid Azure Storage konto ja Azure bloobimälu kasutada?

Nr Kasutatakse vaikimisi Azure Kämp ladustamise, mis on määratletud ja kasutatakse dokumendihaldussüsteemi.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Mis on faili sihtkoha sihtkoht seaded? Mida see seadistus teeb?

Sihtkohta **Fail** kasutatakse dialoogiboksi juhtimiseks. Kui lubate tagasi või kui konfiguratsiooni jaoks määratletud sihtkohta, vt avatud või salvestada dialoogiboksi väljund faili on loodud.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Kas oskate tuua näite valemi kohta, mis viitab hankija kontole, kuhu saan meili saata?

Valem on ER-i konfiguratsiooni põhine. Näiteks kui kasutate ISO 20022 kreeditülekande konfiguratsiooni, võite kasutada valemit **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** või **model.Payments.Creditor.Identification.SourceID** seotud hankija konto toomiseks.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-group-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Ühes minu vormingukonfiguratsioonidest on mitu faili, mis on rühmitatud ühte kausta (nt kaustas nimega Folder1 on failid File1, File2 ja File3). Kuidas saan seadistada sihtkohad nii, et faili Folder1.zip ei loodaks üldse, File1 saadetaks meiliga, File2 saadetaks SharePointi ja et saaksin faili File3 avada kohe pärast konfigureerimist?

Eeltingimus on, et tuleb oma formaadis ER versiooni. Kui teil on oma vorming, avage leht **Elektroonilise aruandluse sihtkoht** ja looge sellele konfiguratsioonile uus viide. Seejärel peab teil olema neli faili sihtkohta, üks iga väljundkomponendi jaoks. Looge esimene faili sihtkoht, andke sellele nimi (nt **Kaust**) ja valige failinimi, mis tähistab teie konfiguratsioonis olevat kausta. Siis klõpsake valikut **Sätted** ja veenduge, et kõik sihtkohad oleksid keelatud. Selle faili sihtkoha jaoks ei looda kausta. Vaikimisi (hierarhiliste sõltuvuste tõttu failide ja põhikaustade vahel) käituvad failid samamoodi. Teisisõnu ei saadeta neid kuhugi. Selle vaikekäitumise alistamiseks tuleb luua veel kolm faili sihtkohta, üks iga faili jaoks. Igaühe sihtkoha sätetes tuleb lubada sihtkoht, kuhu fail tuleks saata.

# <a name="see-also"></a>Vt ka

[Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)


