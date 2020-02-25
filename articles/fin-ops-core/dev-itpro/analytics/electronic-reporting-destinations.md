---
title: Elektroonilise aruandluse (ER) sihtkohad
description: See teema annab teavet elektroonilise aruandluse (ER) sihtkohtade halduse, toetatud sihtkohtade tüüpide ja turvalisuse kaalutluste kohta.
author: nselin
manager: AnnBe
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 2e4c6951afbff367dc93072d20395c3a37fffbcb
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/07/2020
ms.locfileid: "3030769"
---
# <a name="electronic-reporting-er-destinations"></a>Elektroonilise aruandluse (ER) sihtkohad

[!include [banner](../includes/banner.md)]

Saate konfigureerida sihtkoha igale elektroonilise aruandluse (ER) vormingu konfiguratsioonile ja selle väljundi komponendile (kaust või fail). Kasutajad, kellel on sobilikud juurdepääsuõigused, võivad sihtkoha sätteid ka käitusajal muuta. Selles teemas selgitatakse ER-i sihtkoha haldust, toetatud sihtkohtade tüüpe ja turbekaalutlusi.

ER vormingu konfiguratsioonid sisaldavad tavaliselt vähemalt ühte väljundkomponenti: faili. Tavaliselt sisaldavad konfiguratsioonid mitut erinevat tüüpi faili väljundkomponenti (nt XML, TXT, XLSX, DOCX või PDF), mis on rühmitatud ühte või mitmesse kausta. ER-i sihtkoha haldus võimaldab eelkonfigureerida, mis iga komponendi käitamisel toimub. Vaikimisi kuvatakse konfiguratsiooni käivitamisel dialoogiboks, mis võimaldab teil faili salvestada või avada. Sama toimub ka siis, kui importida ER-i konfiguratsioon ja mitte konfigureerida sellele ühtegi konkreetset sihtkohta. Pärast peamisele väljundkomponendile sihtkoha loomist alistab see sihtkoht vaikekäitumise ja kaust või fail saadetakse sihtkoha sätete kohaselt.

## <a name="availability-and-general-prerequisites"></a>Kättesaadavus ja üldised eeltingimused

ER-i sihtkohtade funktsionaalsus ei ole saadaval Microsoft Dynamics AX-i versioonis 7.0 (veebruar 2016). Seetõttu peate installima Microsoft Dynamics 365 for Operationsi versiooni 1611 (november 2016) või uuema, et kasutada järgmisi sihtkoha tüüpe.

- [Meilisõnum](er-destination-type-email.md)
- [Arhiivi](er-destination-type-archive.md)
- [Fail](er-destination-type-file.md)
- [Ekraan](er-destination-type-screen.md)
- [Power BI](er-destination-type-powerbi.md)

Teine võimalus on installida üks järgmistest eeltingimustest. Võtke siiski arvesse, et sellisel juhul on elektroonilise aruandluse sihtkohtade funktsionaalsus piiratud.

- Rakenduse Microsoft Dynamics AX versioon 7.0.1 (mai 2016)
- [Elektroonilise aruandluse sihtkoha halduse rakenduse kiirparandus](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

Olemas on ka sihtkoha tüüp [Printimine](er-destination-type-print.md). Selle kasutamiseks peate installima Microsoft Dynamics 365 Finance'i versiooni 10.0.9 (aprill 2020).

## <a name="overview"></a>Ülevaade

Võite seadistada sihtkohad ainult imporditud ER-i konfiguratsioonidele, mis on [imporditud](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) praegusesse Finance'i eksemplari ja vormingutele, mis on saadaval lehel **Elektroonilise aruandluse konfiguratsioonid**. ER sihtkohahalduse funktsionaalsus on saadaval jaotises **Organisatsiooni haldus** \> **Elektrooniline aruandlus** \> **Elektroonilise aruandluse sihtkoht**. Lehel **Elektroonilise aruandluse sihtkoht** saate konfiguratsiooni vaikekäitumise tühistada. Imporditud konfiguratsioone ei kuvata siin lehel enne, kui valite **Uus** ja seejärel valite väljal **Viide** konfiguratsiooni, millele sihtkoha sätted luua.

[![Konfiguratsiooni valimine väljal Viide](./media/ER_Destinations-SelectFormat.png)](./media/ER_Destinations-SelectFormat.png)

Pärast viite loomist saate luua faili sihtkoha iga viidatud ER vormingu **Kausta** või **Faili** väljundi komponendi jaoks.

[![Failisihtkoha loomine](./media/ER_Destinations-ConfigureElementDestination.png)](./media/ER_Destinations-ConfigureElementDestination.png)

Seejärel saate faili sihtkoha jaoks üksikuid sihtkohti dialoogiboksis **Sihtkoha sätted** kas lubada või keelata. Nuppu **Sätted** kasutatakse valitud faili sihtkohtade juhtimiseks. Dialoogiboksis **Sihtkoha sätted** saate iga sihtkohta eraldi juhtida, tehes sellele valiku **Lubatud**.

Finance'i versioonides **enne versiooni 10.0.9** saate luua **ühe faili sihtkoha** igale sama vormingu väljundi komponendile, nagu näiteks kaust või fail, mis on valitud väljal **Faili nimi**. Kuid **versioonis 10.0.9 ja uuemas** saate luua **mitu faili sihtkohta** igale samas vormingus väljundi komponendile.

Näiteks saate kasutada seda võimalust failide sihtkohtade konfigureerimiseks sellise faili komponendi jaoks, mida kasutatakse väljamineva dokumendi loomiseks Exceli vormingus. Ühte sihtkohta ([arhiivi](er-destination-type-archive.md)) saab konfigureerida salvestama algse Exceli faili ER-tööde arhiivi ja teise sihtkohta ([meili](er-destination-type-email.md)) saab konfigureerida samaaegselt [teisendama](#OutputConversionToPDF) Exceli faili PDF-vormingusse ja saatma PDF-faili e-postiga.

[![Ühele vormingu elemendile mitme sihtkoha konfigureerimine](./media/ER_Destinations-SampleDestinations.png)](./media/ER_Destinations-SampleDestinations.png)

## <a name="destination-types"></a>Sihtkoha tüübid

Järgmised sihtkohad on praegu ER-vormingute puhul toetatud. Saate keelata või lubada kõik tüübid üheaegselt. Sel viisil võite mitte midagi teha või saata komponendi kõigisse konfigureeritud sihtkohtadesse.

- [Meilisõnum](er-destination-type-email.md)
- [Arhiivi](er-destination-type-archive.md)
- [Fail](er-destination-type-file.md)
- [Ekraan](er-destination-type-screen.md)
- [Power BI](er-destination-type-powerbi.md)
- [Print](er-destination-type-print.md)

## <a name="applicability"></a>Kohaldatavus

Võite seadistada sihtkohad ainult imporditud ER-i konfiguratsioonidele ja vormingutele, mis on saadaval lehel **Elektroonilise aruandluse konfiguratsioonid**.

> [!NOTE]
> Konfigureeritud sihtkohad on ettevõttepõhised. Kui plaanite kasutada praeguse Finance'i eksemplari erinevates ettevõtetes ER-vormingut, tuleb teil iga ettevõtte jaoks konfigureerida sihtkohad selle ER-vormingu jaoks.

Kui konfigureerite valitud vormingu jaoks faili sihtkohti, konfigureerite need kogu vormingu jaoks.

[![Konfiguratsiooni link](./media/ER_Destinations-ConfigurationLink.png)](./media/ER_Destinations-ConfigurationLink.png)

Samal ajal võib teil olla praegusesse Finance'i eksemplari imporditud vormingust mitu [versiooni](general-electronic-reporting.md#component-versioning). Saate neid vaadata valides linki **Konfiguratsioon**, mida näete, kui valite välja **Viide**.

[![Konfiguratsiooni versioonid](./media/ER_Destinations-ConfigurationVersions.png)](./media/ER_Destinations-ConfigurationVersions.png)

Vaikimisi rakendatakse konfigureeritud sihtkoti ainult juhul, kui käivitate ER vormingu versiooni, mille olek on kas **Lõpetatud** või **Ühiskasutuses**. Kuid vahel peate kasutama konfigureeritud sihtkohti, kui käivitatakse ER-vormingu mustandversioon. Näiteks muudate oma vormingu mustandversiooni ja soovite kasutada konfigureeritud sihtkohti, et katsetada, kuidas loodud väljund tarnitakse. Järgige neid samme, et rakendada ER-vormingule sihtkohti mustandversiooni käivitamisel.

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Valige lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** valik **Kasutaja parameetrid**.
3. Seadistage suvand **Kasuta mustandi oleku korral sihtkohti** väärtusele **Jah**.

[![Suvand Kasuta mustandi oleku korral sihtkohti](./media/ER_Destinations-UserSetting1.png)](./media/ER_Destinations-UserSetting1.png)

ER-vormingu mustandversiooni kasutamiseks peate ER-vormingu vastavalt märgistama.

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Valige lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** valik **Kasutaja parameetrid**.
3. Seadistage suvand **Käivita säte** väärtusele **Jah**.

[![Sätte käivitamise suvand](./media/ER_Destinations-UserSetting2.png)](./media/ER_Destinations-UserSetting2.png)

Pärast selle seadistuse lõpuleviimist muutub suvand **Käivita mustand** muudetavate ER-vormingute juures kättesaadavaks. Seadistage see suvand väärtusele **Jah**, et hakata kasutama vormingu käivitamisel vormingu mustandversiooni.

[![Mustandi käivitamise suvand](./media/ER_Destinations-FormatSetting.png)](./media/ER_Destinations-FormatSetting.png)

## <a name="DestinationFailure"></a>Sihtkoha tõrke käsitlemine

Tavaliselt käivitatakse ER-vorming kindla äriprotsessi piires. Kuid väljamineva dokumendi tarnet, mis luuakse ER-vormingu käitamisel, tuleb mõnikord lugeda selle äriprotsessi osaks. Sellisel juhul, kui konfigureeritud sihtkohta loodud väljamineva dokumendi kättetoimetamine ebaõnnestub, tuleb äriprotsessi käivitamine tühistada. Sobiva ER sihtkoha konfigureerimiseks valige suvand **Lõpeta nurjumisel töötlemine**.

Näiteks konfigureerite hankija makse töötlemise nii, et **ISO20022 krediidiülekande** ER-vorming käivitatakse maksefaili ja lisadokumentide (nt kaaskiri ja kontroll-aruanne) loomiseks. Kui makse tuleks lugeda edukalt töödelduks ainult siis, kui kaaskiri on edukalt e-posti teel kohale toimetatud, peate valima märkeruudu **Lõpeta tõrke korral töötlemine** komponendile **Kaaskiri** sobivas faili sihtkohas, nii nagu näidatud järgmisel joonisel. Sellisel juhul muudetakse töötlemiseks valitud makse olekut väärtuselt **Puudub** väärtusele **Saadetud** ainult siis, kui loodav kaaskiri on Finance'i eksemplaris konfigureeritud meiliteenuse pakkuja poolt kättetoimetamiseks vastu võetud.

[![Faili sihtkoha nurjumise protsessi töötlemise konfigureerimine](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)

Kui tühjendate märkeruudu **Lõpeta tõrke korral töötlemine** sihtkohas komponendi **Kaaskiri** jaoks, peetakse makset edukalt töödelduks isegi siis, kui kaaskiri ei ole edukalt meili teel kohale toimetatud. Makse olek muudetakse olekust **Puudub** olekusse **Saadetud** isegi siis, kui kaaskirja ei saa saata näiteks seetõttu, et saaja meiliaadress puudub või on vale.

## <a name="OutputConversionToPDF"></a>Väljundi teisendamine PDF-iks

Saate kasutada PDF-vormingu valikut väljundi teisendamiseks Microsoft Office'i vormingust (Excel/Word) PDF-vormingusse.

### <a name="make-pdf-conversion-available"></a>PDF-i teisendamise kättesaadavaks tegemine

PDF-i teisenduse võimaluse kättesaadavaks tegemiseks praeguses Finance'i eksemplaris avage tööruum **Funktsioonide haldus** ja lülitage sisse funktsioon **Elektroonilise aruandluse väljaminevate dokumentide teisendamine Microsoft Office'i vormingutest PDF-i**.

[![Väljamineva dokumendi PDF-i teisenduse sisselülitamine funktsioonide halduses](./media/ER_Destinations-EnablePdfConversionFeature.png)](./media/ER_Destinations-EnablePdfConversionFeature.png)

### <a name="applicability"></a>Kohaldatavus

PDF-i teisenduse valikut saab sisse lülitada ainult faili komponentide puhul, mida kasutatakse väljundi loomiseks Microsoft Office Exceli või Wordi vormingus (**Exceli fail**). Kui see võimalus on sisse lülitatud, teisendatakse Office'i vormingus loodud väljund automaatselt PDF-vormingusse.

### <a name="limitations"></a>Kitsendused

> [!NOTE]
> See funktsioon on eelvaate funktsioon ja seda kasutatakse tingimustes, mida on kirjeldatud teemas [Microsoft Dynamics 365 eelvaadete kasutamise täiendavad tingimused](https://go.microsoft.com/fwlink/?linkid=2105274).

> [!NOTE]
> PDF-i teisenduse valik on saadaval ainult pilvejuurutustes.
>
> Toodetud PDF-fail on piiratud maksimaalselt 300 leheküljega.
>
> Praegu toetatakse Exceli väljundist loodud PDF-dokumendi juures ainult horisontaalpaigutust.
>
> Väljundi teisendamisel kasutatakse ainult tavalisi Windowsi operatsioonisüsteemi süsteemifonte, mis ei sisalda manustatud fonte.

### <a name="use-the-pdf-conversion-option"></a>PDF-teisenduse suvandi kasutamine

Faili sihtkoha jaoks PDF-teisenduse sisselülitamiseks valige märkeruut **Teisenda PDF-iks**.

[![Faili sihtkoha jaoks PDF-teisenduse sisselülitamine](./media/ER_Destinations-TurnOnPDFConversion.png)](./media/ER_Destinations-TurnOnPDFConversion.png)

## <a name="security-considerations"></a>Turbemeetmed

ER-i sihtkohtade puhul kasutatakse kahesuguseid õigusi ja kohustusi. Üks neist juhib kasutaja üldist võimalust hallata juriidilisele isikule konfigureeritud sihtkohti (st juurdepääsu lehele **Elektroonilise aruandluse sihtkohad**). Teine juhib rakenduse kasutaja võimalust alistada käitusajal sihtkoha sätted, mille on konfigureerinud ER-i arendaja või ER-i funktsionaalne konsultant.

| Roll (AOT-nimi)                     | Rolli nimi                                  | Kohustus (AOT-nimi)                     | Kohustuse nimi                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Elektroonilise aruandluse arendaja             | ERFormatDestinationConfigure        | Elektroonilise aruandluse vormingu sihtkoha konfigureerimine                |
| ERFunctionalConsultant              | Elektroonilise aruandluse funktsionaalne konsultant | ERFormatDestinationConfigure        | Elektroonilise aruandluse vormingu sihtkoha konfigureerimine                |
| PaymAccountsPayablePaymentsClerk    | Ostureskontro maksuametnik            | ERFormatDestinationRuntimeConfigure | Elektroonilise aruandluse vormingu sihtkoha konfigureerimine käitusaja jooksul |
| PaymAccountsReceivablePaymentsClerk | Müügireskontro maksuametnik         | ERFormatDestinationRuntimeConfigure | Elektroonilise aruandluse vormingu sihtkoha konfigureerimine käitusaja jooksul |

> [!NOTE]
> Kahte õigust kasutatakse eelnevates kohustustes. Nendel õigustel on samad nimed, mis vastavatel kohustustel: **ERFormatDestinationConfigure** ja **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Olen importinud elektroonilised konfiguratsioonid ja näen neid lehel Elektroonilise aruandluse konfiguratsioonid. Miks ma ei näe neid lehel Elektroonilise aruandluse sihtkohad?

Valige kindlasti **Uus** ja seejärel valige konfiguratsioon väljalt **Viide**. Lehel **Elektroonilise aruandluse sihtkohad** näete ainult neid konfiguratsioone, mille jaoks sihtkohad on konfigureeritud.

### <a name="is-there-any-way-to-define-which-microsoft-azure-storage-account-and-azure-blob-storage-are-used"></a>Kas on võimalik kuidagi määratleda, millist Microsoft Azure'i salvestusruumi kontot ja Azure’i bloobimälu kasutatakse?

Nr Kasutatakse Microsoft Azurei bloobimälu vaikeväärtust, mis on dokumendihalduse süsteemi puhul määratletud ja kasutusel.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Mis on failisihtkoha otstarve sihtkoha sätetes? Mida see seadistus teeb?

Sihtkohta **Fail** kasutatakse dialoogiboksi juhtimiseks. Kui lubate selle sihtkoha või kui konfiguratsioonile pole määratletud ühtki sihtkohta, näete pärast väljundfaili loomist salvestamise või avamise dialoogiboksi.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Kas oskate tuua näite valemi kohta, mis viitab hankija kontole, kuhu saan meili saata?

Valem on ER-i konfiguratsiooni põhine. Näiteks kui kasutate ISO 20022 kreeditülekande konfiguratsiooni, võite kasutada valemit **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** või **model.Payments.Creditor.Identification.SourceID** seotud hankija konto toomiseks.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-grouped-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Ühes minu vormingukonfiguratsioonidest on mitu faili, mis on grupeeritud ühte kausta (nt kaustas nimega Folder1 on failid File1, File2 ja File3). Kuidas saan seadistada sihtkohad nii, et faili Folder1.zip ei loodaks üldse, File1 saadetaks meiliga, File2 saadetaks SharePointi ja saaksin faili File3 avada kohe pärast konfigureerimist?

Teie vorming peab kõigepealt olema ER-i konfiguratsioonide hulgas kättesaadav. Kui see eeltingimus on täidetud, avage leht **Elektroonilise aruandluse sihtkoht** ja looge sellele konfiguratsioonile uus viide. Seejärel peab teil olema neli faili sihtkohta, üks iga väljundkomponendi jaoks. Looge esimene faili sihtkoht, andke sellele nimi (nt **Kaust**) ja valige failinimi, mis tähistab teie konfiguratsioonis olevat kausta. Siis klõpsake valikut **Sätted** ja veenduge, et kõik sihtkohad oleksid keelatud. Selle faili sihtkoha jaoks ei looda kausta. Vaikimisi (hierarhiliste sõltuvuste tõttu failide ja põhikaustade vahel) käituvad failid samamoodi. Teisisõnu ei saadeta neid kuhugi. Selle vaikekäitumise alistamiseks tuleb luua veel kolm faili sihtkohta, üks iga faili jaoks. Igaühe sihtkoha sätetes tuleb lubada sihtkoht, kuhu fail tuleks saata.

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)
