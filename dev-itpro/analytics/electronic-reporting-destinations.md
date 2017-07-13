---
title: Elektroonilise aruandluse sihtkohad
description: "Saate konfigureerida sihtkoha igale elektroonilise aruandluse (ER) vormingu konfiguratsioonile ja selle väljundi komponendile (kaust või fail). Kasutajad, kellele on antud sobilikud juurdepääsuõigused, võivad sihtkoha sätteid ka käitusajal muuta. Selles artiklis selgitatakse ER-i sihtkoha haldust, toetatud sihtkohtade tüüpe ja turbekaalutlusi."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: fb2aeee1f38823e7ea96071f773e8448d65ba8ff
ms.contentlocale: et-ee
ms.lasthandoff: 06/13/2017


---

# <a name="electronic-reporting-destinations"></a>Elektroonilise aruandluse sihtkohad

[!include[banner](../includes/banner.md)]


Saate konfigureerida sihtkoha igale elektroonilise aruandluse (ER) vormingu konfiguratsioonile ja selle väljundi komponendile (kaust või fail). Kasutajad, kellele on antud sobilikud juurdepääsuõigused, võivad sihtkoha sätteid ka käitusajal muuta. Selles artiklis selgitatakse ER-i sihtkoha haldust, toetatud sihtkohtade tüüpe ja turbekaalutlusi.

Elektroonilise aruandluse (ER) vormingu konfiguratsioonid sisaldavad tavaliselt vähemalt ühte väljundkomponenti: faili. Tavaliselt sisaldavad konfiguratsioonid mitut erinevat tüüpi faili väljundkomponenti (nt XML, TXT või XLSX), mis on rühmitatud ühte või mitmesse kausta. ER-i sihtkoha haldus võimaldab eelkonfigureerida, mis iga komponendi käitamisel toimub. Vaikimisi kuvatakse konfiguratsiooni käivitamisel dialoogiboks, mis võimaldab kasutajal faili salvestada või avada. Sama toimub ka siis, kui importida ER-i konfiguratsioon ja mitte konfigureerida sellele ühtegi konkreetset sihtkohta. Pärast peamisele väljundkomponendile sihtkoha loomist alistab see sihtkoht vaikekäitumise ja kaust või fail saadetakse sihtkoha sätete kohaselt.

## <a name="availability-and-general-prerequisites"></a>Kättesaadavus ja üldised eeltingimused
ER-i sihtkohtade funktsioon ei ole saadaval Microsoft Dynamics AX-i versioonis 7.0 (veebruar 2016). Seetõttu peate kõigi selles teemas kirjeldatud funktsioonide kasutamiseks installima Microsoft Dynamics 365 for Operationsi versiooni 1611 (2016. aasta novembrist). Teine võimalus on installida üks järgmistest eeltingimustest. Võtke siiski arvesse, et sellisel juhul on elektroonilise aruandluse sihtkohtade funktsionaalsus piiratud.

-   Microsoft Dynamics AX-i versioon 7.0.1 (mai 2016)
-   ER-i sihtkoha halduse [rakenduse kiirparandus](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

Võite seadistada sihtkohad ainult imporditud ER-i konfiguratsioonidele ja vormingutele, mis on saadaval lehel **Elektroonilise aruandluse konfiguratsioonid**.

## <a name="overview"></a>Ülevaade
Elektroonilise aruandluse sihtkohahalduse funktsioon on saadaval jaotises **Organisatsiooni haldus** &gt; **Elektrooniline aruandlus**. Siin saab alistada konfiguratsiooni vaikekäitumise. Imporditud konfiguratsioone ei kuvata siin enne, kui klõpsate valikut **Uus** ja valite siis väljal **Viide** konfiguratsiooni, millele sihtkoha sätted luua.

[![Konfiguratsiooni valimine väljal Viide](./media/ger-destinations-2-1611-1024x574.jpg)](./media/ger-destinations-2-1611.jpg) 

Kui olete viite loonud, saate luua igale kaustale või failile failisihtkoha. 

[![Failisihtkoha loomine](./media/ger-destinations-1611-1024x586.jpg)](./media/ger-destinations-1611.jpg)

**Märkus.** Saate luua ühe faili sihtkoha igale sama vormingu väljundkomponendile (kaustale või failile), mis on valitud väljal **Faili nimi**. Seejärel saate lubada ja keelata failisihtkohti eraldi dialoogiboksis **Sihtkoha sätted**. Nuppu **Sätted** kasutatakse valitud faili sihtkohtade juhtimiseks. Dialoogiboksis **Sihtkoha sätted** saate iga sihtkohta eraldi juhtida, tehes sellele valiku **Lubatud**.

[![Dialoogiboks Sihtkoha sätted](./media/ger-destinations-settings-1611-1024x589.jpg)](./media/ger-destinations-settings-1611.jpg)

## <a name="destination-types"></a>Sihtkoha tüübid
Toetatakse mitmesugust tüüpi sihtkohti. Saate keelata või lubada kõik tüübid üheaegselt. Sel viisil võite mitte midagi teha või saata komponendi kõigisse konfigureeritud sihtkohtadesse. Järgmised jaotised kirjeldavad toetatud sihtkohti.

### <a name="email-destination"></a>Meili sihtkoht

Määrake valiku **Lubatud** väärtuseks **Jah** väljundfaili saatmiseks meiliga. Kui see valik on lubatud, saate määrata meili adressaadid ning redigeerida meilisõnumi teemat ja kehateksti. Saate seadistada meilide teema ja kehateksti jaoks püsiteksti või kasutada meilitekstide loomiseks elektroonilise aruandluse valemeid. Elektroonilise aruandluse meiliaadresside konfigureerimiseks on kaks võimalust. Konfiguratsiooni saab lõpule viia samamoodi, nagu prindihalduse funktsiooni puhul rakenduses Finance and Operations. Teine võimalus on lahendada meiliaadress otseviitega elektroonilisele aruandlusele valemi kaudu.

### <a name="email-address-types"></a>Meiliaadressi tüübid

Kui klõpsate valikut **Redigeeri** välja **Saaja** või **Koopia** puhul, kuvatakse dialoogiboks **Meili saaja**. Seejärel saate valida kasutatava meiliaadressi tüübi.

[![Dialoogiboks Meili saaja](./media/ger-destinations-email-1-1611-1024x588.jpg)](./media/ger-destinations-email-1-1611.jpg)

#### <a name="print-management"></a>Prindihaldus

Kui valite tüübi **Prindihalduse meil**, saate sisestada väljale **Saaja** fikseeritud meiliaadressid. Fikseerimata meiliaadresside kasutamiseks tuleb valida failisihtkohaks meiliallika tüüp. Toetatakse järgmisi väärtusi: **Klient**, **Hankija**, **Potentsiaalne klient**, **Kontakt**, **Konkurent**, **Töötaja**, **Kandidaat**, **Potentsiaalne hankija** ja **Keelatud hankija**. Pärast meiliallika tüübi valimist avage välja **Meiliallika konto** kõrval oleva nupu abil vorm **Valemi kujundaja**. Selle vormi abil saate lisada meilisihtkohale valemi, mis kujutab valitud osapoole kontot.

[![Prindihalduse meilitüübi konfigureerimine](./media/ger-destinations-email-2-1611-1024x588.jpg)](./media/ger-destinations-email-2-1611.jpg) 

Pange tähele, et valemid on ER-i konfiguratsiooni põhised. Sisestage väljale **Valem** dokumendipõhine viide kliendi või hankija osapoole tüübile. Tippimise asemel võite otsida üles andmeallika sõlme, mis tähistab kliendi või hankija kontot, ja klõpsata siis valemi värskendamiseks nuppu **Lisa andmeallikas**. Näiteks kui kasutate ISO 20022 kreeditülekande konfiguratsiooni, tähistab hankija kontot sõlm **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID**. Vastasel korral sisestage valemi salvestamiseks stringi väärtus, nagu **DE-001**.

[![Formula designer](./media/ger_formuladesignerfordestination-1024x541.jpg)](./media/ger_formuladesignerfordestination.jpg)

Klõpsake dialoogiboksis **Meili saaja** välja **Meiliallika konto** kõrval olevat prügikastiikooni, et selle meiliallika konto puhul valem jäädavalt kustutada. Teine võimalus on avada valemikujundaja, et muuta varem salvestatud valemit. Meiliaadresside määramiseks klõpsake nuppu **Redigeeri**, et avada dialoogiboks **Meiliaadresside määramine**.

[![Meiliaadresside määramine meilisihtkohale](./media/ger-destinations-email-3-1611-1024x587.jpg)](./media/ger-destinations-email-3-1611.jpg)

#### <a name="configuration-email"></a>Konfigureerimismeil

Kasutage seda meilitüüpi, kui kasutataval konfiguratsioonil on andmeallikates sõlm, mis kujutab meiliaadressi. Õigesti vormindatud meiliaadressi saamiseks saate kasutada valemikujundajas sisalduvaid andmeallikaid ja funktsioone.

[![Meiliaadressi andmeallika määramine meilisihtkohale](./media/ger-destinations-email-4-1611-1024x587.jpg)](./media/ger-destinations-email-4-1611.jpg) 

**Märkus.** Simple Mail Transfer Protocoli (SMTP) server peab olema konfigureeritud ja saadaval. Saate määrata oma SMTP-serveri Finance and Operationsi jaotises **Süsteemihaldus** &gt; **Seadistus** &gt; **Meil** &gt; **Meiliparameetrid**.

### <a name="archive-destination"></a>Arhiivi sihtkoht

Selle valiku abil saab saata väljundi Microsoft SharePointi kausta või Microsoft Azure’i salvestusruumi. Määrake valiku **Lubatud** väärtuseks **Jah** väljundi saatmiseks valitud dokumenditüübiga määratletud sihtkohta. Valida saab ainult neid dokumenditüüpe, millel grupiks on määratud **Fail**. Dokumenditüübid saate määratleda jaotises **Organisatsiooni haldus** &gt; **Dokumendihaldus** &gt; **Dokumenditüübid**. ER-i sihtkohtade konfiguratsioon on sama, mis dokumendihaldussüsteemi konfiguratsioon.

[![Leht Dokumenditüübid](./media/ger_documenttypefile-1024x542.jpg)](./media/ger_documenttypefile.jpg) 

Asukoht määrab, kuhu fail salvestatakse. Kui sihtkoht **Arhiiv** on lubatud, saab konfiguratsiooni käivitamise tulemused salvestada tööarhiivi. Tulemusi saate vaadata jaotises **Organisatsiooni haldus** &gt; **Elektrooniline aruandlus** &gt; **Elektroonilise aruandluse arhiivitud tööd**. **Märkus.** Tööarhiivi jaoks saate dokumenditüübi valida Finance and Operationsi jaotises **Organisatsiooni haldus** &gt; **Tööruumid** &gt; **Elektrooniline aruandlus** &gt; **Elektroonilise aruandluse parameetrid**.

#### <a name="sharepoint"></a>SharePoint

Faili saab salvestada selleks mõeldud SharePointi kausta. SharePointi vaikeserveri saate määratleda jaotises **Organisatsiooni haldus** &gt; **Dokumendihaldus** &gt; **Dokumendihalduse parameetrid** vahekaardil **SharePoint**. Pärast SharePointi kausta konfigureerimist saate valida selle kaustana, kuhu elektroonilise aruandluse väljund dokumenditüübi puhul salvestatakse. 

[![SharePointi kausta valimine](./media/ger_sharepointfolderselection-1024x543.jpg)](./media/ger_sharepointfolderselection.jpg) 

#### <a name="azure-storage"></a>Azure’i salvestusruum

Kui dokumenditüübi asukohaks on määratud **Arhiivikaust**, saab salvestada faili Azure’i salvestusruumi.

### <a name="file-destination"></a>Faili sihtkoht

Kui määrate valiku **Lubatud** väärtuseks **Jah**, kuvatakse konfigureerimise lõppemisel avamise või salvestamise dialoogiboks.

### <a name="screen-destination"></a>Sihtkoht Kuva

Kui määrate valiku **Lubatud** väärtuseks **Jah**, luuakse väljundi eelvaade. Saate mõnd failitüüpi, nagu XML, TXT või PDF, vaadata otse brauseriaknas. Muude failitüüpide, näiteks Microsoft Excel või Word, puhul kasutatakse Microsoft Office Online’i teenust.

### <a name="power-bi-destination"></a>Sihtkoht Power BI

Kui määrate valiku **Lubatud** väärtuseks **Jah**, saate oma elektroonilise aruandluse konfiguratsiooni abil korraldada andmete üleviimine teie Finance and Operationsi eksemplarist Microsoft Power BI teenustesse. Edastatud failid talletatakse Microsoft SharePoint Serveri eksemplari, mis on selleks otstarbeks konfigureeritud. Lisateavet vt teemast [Elektroonilise aruandluse konfiguratsiooni kasutamine Power BI-le andmete esitamiseks rakendusest Finance and Operations](general-electronic-reporting-report-configuration-get-data-powerbi.md). **Vihje.** Vaikekäitumise (st konfigureerimise dialoogiboksi) alistamiseks võite luua peamisele väljundkomponendile sihtkoha viite ja faili sihtkoha ning keelata siis kõik sihtkohad.

## <a name="security-considerations"></a>Turbemeetmed
ER-i sihtkohtade puhul kasutatakse kahesuguseid õigusi ja kohustusi. Üks neist juhib võimalust hallata üldisi juriidilisele isikule konfigureeritud sihtkohti (st juurdepääsu lehele **Elektroonilise aruandluse sihtkohad**). Teine juhib rakenduse kasutaja võimalust alistada käitusajal sihtkoha sätted, mille on konfigureerinud ER-i arendaja või ER-i funktsionaalne konsultant.

| Roll (AOT-nimi)                     | Rolli nimi                                  | Kohustus (AOT-nimi)                     | Kohustuse nimi                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Elektroonilise aruandluse arendaja             | ERFormatDestinationConfigure        | Elektroonilise aruandluse vormingu sihtkoha konfigureerimine                |
| ERFunctionalConsultant              | Elektroonilise aruandluse funktsionaalne konsultant | ERFormatDestinationConfigure        | Elektroonilise aruandluse vormingu sihtkoha konfigureerimine                |
| PaymAccountsPayablePaymentsClerk    | Ostureskontro maksuametnik            | ERFormatDestinationRuntimeConfigure | Elektroonilise aruandluse vormingu sihtkoha konfigureerimine käitusaja jooksul |
| PaymAccountsReceivablePaymentsClerk | Müügireskontro maksuametnik         | ERFormatDestinationRuntimeConfigure | Elektroonilise aruandluse vormingu sihtkoha konfigureerimine käitusaja jooksul |

**Märkus.** Kahte õigust kasutatakse eelnevates kohustustes. Nendel õigustel on samad nimed, mis vastavatel kohustustel: **ERFormatDestinationConfigure** ja **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused
### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Olen importinud elektroonilised konfiguratsioonid ja näen neid lehel Elektroonilise aruandluse konfiguratsioonid. Miks ma ei näe neid lehel Elektroonilise aruandluse sihtkohad?

Klõpsake kindlasti valikut **Uus** ja valige konfiguratsioon väljalt **Viide**. Lehel **Elektroonilise aruandluse sihtkohad** näete ainult neid konfiguratsioone, mille jaoks sihtkohad on konfigureeritud.

### <a name="is-there-any-way-to-define-which-azure-storage-account-and-azure-blob-storage-are-used"></a>Kas on võimalik kuidagi määratleda, millist Azure’i salvestusruumi kontot ja Azure’i bloobimälu kasutatakse?

Nr Kasutatakse Azure’i bloobimälu vaikeväärtust, mis on dokumendihalduse süsteemi puhul määratletud ja kasutusel.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Mis on failisihtkoha otstarve sihtkoha sätetes? Mida see seadistus teeb?

Sihtkohta **Fail** kasutatakse dialoogiboksi juhtimiseks. Kui lubate selle sihtkoha või kui konfiguratsioonile pole määratletud ühtki sihtkohta, näete pärast väljundfaili loomist salvestamise või avamise dialoogiboksi.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Kas oskate tuua näite valemi kohta, mis viitab hankija kontole, kuhu saan meili saata?

Valem on ER-i konfiguratsiooni põhine. Näiteks kui kasutate ISO 20022 kreeditülekande konfiguratsiooni, võite kasutada valemit **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** või **model.Payments.Creditor.Identification.SourceID** seotud hankija konto toomiseks.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-group-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Ühes minu vormingukonfiguratsioonidest on mitu faili, mis on rühmitatud ühte kausta (nt kaustas nimega Folder1 on failid File1, File2 ja File3). Kuidas saan seadistada sihtkohad nii, et faili Folder1.zip ei loodaks üldse, File1 saadetaks meiliga, File2 saadetaks SharePointi ja et saaksin faili File3 avada kohe pärast konfigureerimist?

Eeltingimus on, et teie vorming peab olema elektroonilise aruandluse konfiguratsioonides kättesaadav. Kui teil on oma vorming, avage leht **Elektroonilise aruandluse sihtkoht** ja looge sellele konfiguratsioonile uus viide. Seejärel peab teil olema neli faili sihtkohta, üks iga väljundkomponendi jaoks. Looge esimene faili sihtkoht, andke sellele nimi (nt **Kaust**) ja valige failinimi, mis tähistab teie konfiguratsioonis olevat kausta. Siis klõpsake valikut **Sätted** ja veenduge, et kõik sihtkohad oleksid keelatud. Selle faili sihtkoha jaoks ei looda kausta. Vaikimisi (hierarhiliste sõltuvuste tõttu failide ja põhikaustade vahel) käituvad failid samamoodi. Teisisõnu ei saadeta neid kuhugi. Selle vaikekäitumise alistamiseks tuleb luua veel kolm faili sihtkohta, üks iga faili jaoks. Igaühe sihtkoha sätetes tuleb lubada sihtkoht, kuhu fail tuleks saata.

# <a name="see-also"></a>Vt ka

[Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)




