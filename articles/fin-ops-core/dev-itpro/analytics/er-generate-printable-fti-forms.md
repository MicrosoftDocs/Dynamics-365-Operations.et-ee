---
title: Prinditavate FTI-vormide loomine
description: Teemas selgitatakse, kuidas kasutada elektroonilise aruandluse (ER) raamistikku, et luua prinditavaid vabas vormis arvete (FTI) vorme Microsoft Office’i dokumentidena.
author: NickSelin
manager: AnnBe
ms.date: 07/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 168cef1b5f5d48cb739b08fa395c1bcd62089494
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686721"
---
# <a name="generate-printable-fti-forms"></a>Prinditavate FTI-vormide loomine

[!include[banner](../includes/banner.md)]

Elektroonilise aruandluse (ER) raamistik võimaldab teil luua prinditavaid vabas vormis arvete (FTI) vorme Microsoft Office’i dokumentidena. Teema annab teavet selle kohta, kuidas luua oma konfiguratsioone, ja üksikasjaliku ülevaate saadavaolevate konfiguratsioonimallide kohta.

## <a name="overview"></a>Ülevaade

Peale olemasoleva võimaluse luua teenusega Microsoft SQL Server Reporting Services (SSRS) prinditavaid FTI-vorme saate nüüd selleks kasutada ka elektroonilise aruandluse raamistikku. Saate hallata prinditavaid FTI-vorme Microsoft Office Excelis ja Wordis. Samuti saate konkreetsete nõuete täitmiseks muuta paigutust, andmevoogu ja vormingut ilma, et peaks tegema muudatusi koodis.

> [!NOTE]
> Kui soovite alustuseks näha ülevaadet olemasolevatest ER-i konfiguratsioonidest selle prinditavate FTI-vormide lahenduse näite jaoks, võite kohe liikuda selle teema jaotisesse **ER-i näidiskonfiguratsioonide allalaadimine, et luua prinditavaid FTI-vorme**.

## <a name="create-customized-configurations-for-fti-printable-forms"></a>Prinditavate FTI-vormide jaoks kohandatud konfiguratsioonide loomine
Prinditavate FTI-vormide kohandatud lahenduse osana peate looma ER-i konfiguratsioonide kogumi.

### <a name="configure-the-er-data-model"></a>Elektroonilise aruandluse andmemudeli konfigureerimine
Teie rakenduses peab olema ER-i andmemudeli konfiguratsioon, mis sisaldab andmemudelit, mis kirjeldab kliendi arveldamise ettevõttedomeeni. Selle andmemudeli nimi peab olema **CustomersInvoicing**. Teavet ER-i andmemudelite kujundamise kohta leiate teemast [Elektroonilise aruandluse domeenispetsiifilise andmemudeli kujundamine](tasks/er-design-domain-specific-data-model-2016-11.md).

### <a name="configure-the-er-model-mapping"></a>Elektroonilise aruandluse mudelivastenduse konfigureerimine
Teie rakenduses peab olema andmemudeli CustomersInvoicing jaoks ER-i mudelivastendus. Mudelivastendus võib olla kas ER-i andmemudeli konfiguratsioonis või ER-i mudelivastenduse konfiguratsioonis. Mudelivastenduse juurdeskriptori nimi peab aga olema **FreeTextInvoice**.

Vastendamine peab sisaldama järgmisi andmeallikaid.

- Andmeallika tüüp: **Tabeli kirjed**

    - Selle andmeallika nimi peab olema **CustInvoiceJour**.
    - See peab viitama rakendustabelile CustInvoiceJour.
    - Seda kasutatakse käitusajal, et edastada printimiseks valitud arvete loend rakendusest ER-i mudelivastendusele.

- Andmeallika tüüp: **Objekt**

    - Selle andmeallika nimi peab olema **PrintMgmtPrintSettingDetail**.
    - See peab viitama rakendusklassile **PrintMgmtPrintSettingDetail**.
    - Seda kasutatakse käitusajal, et edastada töötava ER-vormingu prindihalduse sätete üksikasjad rakendusest ER-i mudelivastendusele.

Rakenduse ER-i raamistikuga integreerimise üksikasjad leiate rakenduse lähtekoodi klassis **ERPrintMgmtReportFormatSubscriber** (ER-i rakenduste komplekti integreerimismudel).

Lisateavet ER-i mudelivastenduste kujunduse kohta leiate teemast [Elektroonilise aruandluse mudelivastenduste määratlemine ja andmeallikate valimine](tasks/er-define-model-mapping-select-data-sources-2016-11.md).

### <a name="configure-the-er-format"></a>ER-i vormingu konfigureerimine
Teie rakenduse eksemplaris peab olema FTI-vormide loomiseks kasutatav ER-i vormingu konfiguratsioon. 

> [!NOTE]
> See vormingu konfiguratsioon tuleb luua andmemudeli CustomersInvoicing jaoks ja see vorming peab kasutama mudelivastendust, millel on juurdeskriptor **FreeTextInvoice**.

Teavet ER-vormingute konfigureerimise kohta leiate teemast [Elektrooniline aruandlus. Vormingu konfiguratsiooni loomine (november 2016)](tasks/er-format-configuration-2016-11.md). Teavet OpenXML-i vormingus aruannete loomiseks ER-vormingute kujundamise kohta leiate teemast [Elektrooniline aruandlus. OPENXML-vormingus aruannete loomiseks konfiguratsiooni koostamine (november 2016)](tasks/er-design-reports-openxml-2016-11.md).

## <a name="configure-print-management"></a>Prindihalduse konfigureerimine
ER-raamistiku kaudu FTI-vormingute loomiseks saate määrata ER-i vorminguid samamoodi, nagu määrate SSRS-aruandeid. Selleks, et seostada ER-i vorming kõikide müügireskontro FTI-dega, valige **Müügireskontro** \> **Seadistus** \> **Vormid** \> **Vormi seadistus** \> **Üldine** \> **Prindihaldus** \> **Vabas vormis arve** \> **Originaal**. ER-i vormingu seostamiseks kindla kliendi või arvega järgige järgmisi juhiseid.

1. Avage **Müügireskontro** \> **Arved** \> **Kõik vabas vormis arved**.
2. Valige FTI, millega ER-i vorming seostada, ja avage leht **Prindihalduse seadistus**.
3. Valige dokumendi tase, et määrata töötlemisele minevate arvete ulatus.
4. Valige määratletud dokumendi taseme jaoks ER-i vorming.

![Prindihalduse seadistus](media/FTIbyGER-PMSetting.png)

> [!NOTE]
> Valitud vormingu väljal **Aruande vormingu otsing** ilmuvad vaid ER-i vormingud, mis kasutavad andmemudeli **CustomersInvoicing** juurdeskriptorit **FreeTextInvoice**.

## <a name="generate-fti-forms"></a>FTI-vormide loomine
FTI-vorme luuakse ER-i raamistikus samamoodi, nagu luuakse SSRS-aruandeid.

FTI-vormide loomiseks saate valida arveid kas vahemiku järgi või valiku alusel. 

![Arvete valimine](media/FTIbyGER-InvoiceSelection.png)

![Arve eelvaade](media/FTIbyGER-InvoiceExcelPreview.png)

Kui kasutate ER-i vorminguid, et sellel teel FTI-vorme printida, siis kasutatakse ER-i failide vaikesihtkohti. Seda sihtkohta ei saa muuta. Lisateavet ER-vormingute sihtkohtade konfigureerimise kohta leiate teemast [Elektroonilise aruandluse (ER) sihtkohad](electronic-reporting-destinations.md).

FTI postitamisel saate ka luua FTI-vorme, kui lülitate sisse suvandi **Prindi arve** ja välja suvandi **Kasuta prindihalduse sihtkohti**.

> [!NOTE]
> Kui kasutate ER-i vorminguid, et sellel teel FTI-vorme printida, siis kasutatakse ER-i failide vaikesihtkohti. Kui sihtkoht on juba konfigureeritud, saate muuta vaikesihtkoha käitusajal. Sihtkoha muutmiseks peab teil olema järgmine turbeprivileeg.
>
> - **Nimi:** ERFormatDestinationRuntimeMaintain
> - **Silt:** elektroonilise aruandluse vormingu sihtkoha haldamine käitusaja jooksul

![Elektroonilise aruandluse sihtkoht](media/FTIbyGER-ERFileDestinationSetting.png)

![Elektroonilise aruandluse vormingu sihtkoht](media/FTIbyGER-ERFileDestinationUsage.png)

ER-i raamistik toetab praegu loodud dokumentide jaoks järgmisi sihtkohti.

- **Allalaaditud fail** – loodud vorme pakutakse allalaadimistena, mida saate brauseri kaudu salvestada.
- **Ekraan** – kasutatakse rakendust Microsoft 365 Excel, et kuvada loodud FTI-vormide eelvaated Exceli vormingus.
- **SharePointi kaust** – loodud vorme hoiustatakse dokumendihalduse raamistiku sätete põhjal.
- **Rakenduse arhiiv**– loodud vorme hoiustatakse Microsoft Azure’i salvestusruumis käivituslogi kirjete manustena.
- **Meil** – loodud vormid saadetakse meilimanustena.

> [!NOTE]
> Te ei saa loodud FTI-vorme otse printimisele saata, sest otseprintimine kasutab Dynamicsi printeri marsruudivaliku agenti, mis ei ole praegu toetatud.

## <a name="download-sample-er-configurations-to-generate-printable-fti-forms"></a>ER-i näidiskonfiguratsioonide allalaadimine, et luua prinditavaid FTI-vorme
Saate alla laadida ER-i näidiskonfiguratsioone, et kasutada neid oma FTI-lahenduses mallina. Konfiguratsioone talletatakse Microsoft Dynamics teenuse Lifecycle Services (LCS) ühiste vahendite teegis. Konfiguratsioonid sisaldavad järgmist.

- Konfiguratsioon **Kliendiarvete mudel** sisaldab vajalikku andmemudelit ja mudelivastendust.
- Konfiguratsioon **Kliendi FTI-aruanne (GER)** sisaldab näidisvormingut.

> [!NOTE]
> Need konfiguratsioonid on loodud näidisteks, et selgitada võimalikke stsenaariumeid. Nende konfiguratsioonide tulevik sõltub selle hinnangu tulemustest ja saadud tagasisidest.

### <a name="features-that-are-implemented-in-the-sample-er-format"></a>ER-i näidisvormingus rakendatud funktsioonid
ER-i näidisvormingu konfiguratsioonis kasutatakse FTI-vormide loomisel mallina Exceli faili.

![Vormingu koostaja](media/FTIbyGER-ERFormat.png)

Praegu toetab see ER-i näidisvorming FTI-vormide loomiseks järgmisi funktsioone.

- FTI-vormid luuakse nii sisestatud kui ka sisetamata originaalarvete jaoks. Korrigeeritud arveid ja kreeditarveid ei toetata.
- FTI-vormid luuakse arve keeles. Loodud vormide väärtuste ja kuupäevade vorming on kasutaja kliendi lokaadi sätete põhjal määratud.
- Loodud arved näitavad andmete mittesaadavuse teatisi, kui arvetes pole töödeldud ridasid.
- Loodud arvete päised põhinevad paberiformaadil, mis on lehel **Müügireskontro parameetrid** FTI-vormi jaoks valitud. Ettevõtte andmeid näidatakse loodud arve vormi päises vaid siis, kui paberiformaadi valik on tühi.
- Loodud arve vormid näitavad ettevõtte ja kliendi maksuvabastuskoode, kui FTI-vormi jaoks on lehel **Müügireskontro parameetrid** tehtud asjakohane valik.
- Loodud arve ridade ja arve kogusumma jaotised näitavad arve valuutaandmete vaikevarianti arve registreerimisvaluutas.
- Loodud arve kogusummade jaotis võib näidata valuutaandmeid eurodes ja arve registreerimisvaluutas, kui suvand **Eurot tähistavas valuutas summa printimine** on lehel **Müügireskontro parameetrid** lubatud.
- Loodud arve vormid näitavad iga protsessi saadavaolevaid arve märkuseid, nagu on määratud lehe **Müügireskontro parameetrid** sätetes. Märkused on olemas nii kogu arve kui ka iga arverea jaoks.
- Loodud arve vormidel on märkused kliendi FTI-vormi ja töötlemise arve keele jaoks, kui see on nii konfigureeritud ER-i vormi märkuse loendis.
- Olenevalt prindihalduse sätetest on loodud arvetel kohandatud tekstiga jalus, kui see on konfigureeritud arve keele, ER-i vormingu ja FTI-dokumendi ulatuse jaoks.
- Loodud arve vormide kogusummade jaotis hõlmab kõik saadavaloleva skonto teave.
- Loodud arve vormide maksegraafiku jaotis hõlmab kõik saadavalolevad maksegraafikud.
- Loodud arve vormide hinnalisandi jaotis hõlmab kõik saadavalolevad tasude kanded.
- Loodud arve vormid sisaldavad käibemaksu üksikasju, nagu on määratletud lehe **Müügireskontro parameetrid** sättes **Käibemaksu täpsustus**. Selles jaotises võidakse näidata maksu üksikasju kas ainult arve registreerimisvaluutas või arve registreerimisvaluutas ja ettevõtte arvestusvaluutas samal ajal.
- Loodud arve vormid näitavad otsekorralduse teatise üksikasju. Näiteks näitavad need, millal valiti arve jaoks kohustusliku otsekorralduse loa ID-ga makseviis, millal registreeriti töödeldav arve valuutas euro ja millal määratleti arve jaoks otsekorralduse loa ID.
- Loodud arved näitavad kõiki ettemakse üksikasju, mis on sisestatud arvete jaoks saadaval.
- Loodud arve vorme saab saata arve kliendile meilimanusena. Kasutatava ER-i vormingu jaoks tuleks konfigureerida asjakohane ER-i faili sihtkoht.

### <a name="countryregion-specific-features"></a>Riigi/regioonikohased funktsioonid 
ER-i näidisvormingusse on kaasatud järgmised riigi-/regioonipõhised funktsioonid, et näidata, kuidas konkreetseid nõudeid saab ER-i konfiguratsioonides käsitleda.

#### <a name="norway"></a>Norra
Loodud arve päisesse lisatakse ettevõtte registri tingimus siis, kui arve töödeldakse juriidilisele isikule, mis on järgmiselt konfigureeritud.

- Kasutatakse Norra riigi/regiooni konteksti.
- Müügidokumentidel on aktiivne parameeter **Prindi Foretaksregisteret**.

#### <a name="spain"></a>Hispaania
Loodud arve päisesse lisatakse tingimus **Sularahaarvestuse meetodi erirežiim** siis, kui arve töödeldakse juriidilisele isikule, mis on järgmiselt konfigureeritud.

- Kasutatakse Hispaania riigi/regiooni konteksti.
- Sularahaarvestuse meetodi erirežiim on arve töötlemise kuupäeval lubatud.

Kui saadaval on skonto üksikasjad, näiteks skonto summa ja arverea netosumma, siis näidatakse neid loodud arve kogusumma jaotises siis, kui arve töödeldakse juriidilisele isikule, mis on järgmiselt konfigureeritud.

- Kasutatakse Hispaania riigi/regiooni konteksti.
- Arve suvandis on valik **Arvele rakendatakse skontot** sisse lülitatud (**Üldised pearaamatu parameetrid** \> **Käibemaksu jaotis**).

#### <a name="italy"></a>Itaalia
Kaupade allahindluse märge on kaasatud loodud arve arveridadele siis, kui arve töödeldakse juriidilisele isikule, mis on konfigureeritud Itaalia riigi/piirkonna kontekstiga.

#### <a name="finland"></a>Soome
Peale loodud arve vormi saab luua maksekorraldusi järgmiselt.

- Juriidilise isiku jaoks, mis kasutab Soome riigi/regiooni konteksti ja millel on vähemalt üks pangakonto, mis on märgitud **Ülekandekontoks** ja kaasatud **Panga vöötkoodi**. 
- Arve jaoks, mis on **Soome** seostatud maksemanuse jaoks vajalikuks märgitud.

![Ülekandeleht](media/FTIbyGER-GiroSlip.PNG)

> [!NOTE]
> ER-i näidisvorming on konfigureeritud valikuliselt eraldi töölehel maksekorraldusi looma.

> [!NOTE]
> Esmalt peate installima fondi, mida kasutatakse vöötkoodi loomiseks kohalikul masinal, kus vaadatakse Exceli vormingus loodud arve vormi eelvaadet.

### <a name="use-the-sample-er-format-to-configure-email-destinations"></a>ER-i näidisvormingu kasutamine meilisihtkohtade konfigureerimiseks
Kasutage ER-i näidisvormingu järgmisi elemente, et konfigureerida meilisihtkohti.

- Kliendi kontakti meiliaadressile saab juurdepääsu järgmise ER-i avaldisega: **model.InvoiceBase.Contact.ElectronicMail**.
- Meili teema tekstile saab juurdepääsu järgmise ER-i avaldisega: **Emailing.TxtToUse.Subject**.
- Meili kehatekstile saab juurdepääsu järgmise ER-i avaldisega: **Emailing.TxtToUse.Body**.

![Sihtkoha sätted](media/FTIbyGER-ERFileDestinationSettingEmail.png)

Meili teema ja keha vaiketekst on ER-i näidisvormingus määratletud. Keelevalik sõltub vormingu siltidest. Meilide jaoks kasutatakse vaiketeksti, kui lisatud on kohandatud organisatsiooni meilimall, millel on eelmääratletud ID **ERFTITMP**.

> [!NOTE]
> Meilimalli ID **ERFTITMP** on ER-i näidisvormingus määratletud. Seda saab vajaduse korral muuta uues näidisvormingu põhjal loodud ER-i vormingus.

Kui eelmääratletud ID-ga **ERFTITMP** organisatsiooni meilimall on lisatud juriidilisele isikule, mille arvet te töötlete, siis kasutatakse meili loomiseks meilimalli teema ja kehateksti. 

![Organisatsiooni meilimallid](media/FTIbyGER-EmailTemplate.png)

![Meilimalli üleslaadimine](media/FTIbyGER-EmailTemplateBody.png)

Elektroonilise aruandluse näidisvormingu ER-avaldis **Emailing.TxtToUse.Subject** on konfigureeritud asendama kõik kohatäite %1 esinemised töödeldava arve ID-ga.

ER-i näidisvormingu ER-avaldis **Emailing.TxtToUse.Body** on konfigureeritud kohatäiteid järgmiste andmetega asendama.

- „%1” asendatakse kliendi kontaktisiku nimega.
- „%2” asendatakse ettevõtte nimega.
- „%3” asendatakse kliendi nimega.
- „%4” asendatakse ettevõtte kontaktisiku nimega.
- „%5” asendatakse ettevõtte kontaktisiku ametinimetusega.
- „%6” asendatakse ettevõtte kontaktisiku meiliaadressiga.

![Meilisõnum](media/FTIbyGER-Email.PNG)

## <a name="additional-resources"></a>Lisaressursid
[Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]