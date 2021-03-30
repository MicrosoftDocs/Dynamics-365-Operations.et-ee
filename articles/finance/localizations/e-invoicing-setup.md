---
title: Elektroonilise arvelduse lisandmooduli seadistamine
description: Selles teemas selgitatakse, kuidas seadistada rakendustes Microsoft Dynamics 365 Finance ja Dynamics 365 Supply Chain Management elektroonilise arvelduse lisandmoodulit.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 5821a512b2beaf7ba2b8015355f04562f7b3b38a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209942"
---
# <a name="set-up-the-electronic-invoicing-add-on"></a>Elektroonilise arvelduse lisandmooduli seadistamine

[!include [banner](../includes/banner.md)]


Elektroonilise arvelduse lisandmooduli funktsiooni seadistamine hõlmab vajaliku konfiguratsiooni loomist teenuste Regulatory Configuration Services (RCS) keskkonna kaudu ja konfiguratsiooni avaldamist elektroonilise arvelduse lisandmooduli serveris. Seadistus võimaldab teil luua konfigureeritavad reeglid, mis võimaldavad elektroonilise arvelduse lisandmoodulil kasutada internetis turvalist protokolli, et edastada ja vahetada veebiteenuste kaudu andmeid kolmandate isikutega.

Konfigureerimise aluseks on elektroonilise aruandluse (ER) vormingu konfiguratsioon kui vahend digitaalsete failide kaudu saadetud ja vastuvõetud sisu loomiseks. Samuti tugineb see suhtlustegevuste korraldamisele, et saata taotlusi ja võtta vastu vastuseid kolmandate isikute veebiteenustest ilma koodi kirjutamise vajaduseta.

## <a name="overview"></a>Ülevaade

„Elektroonilise arvelduse lisandmooduli funktsioon” on kindla ressursi üldnimi, mis on konfigureeritud ja avaldatud kasutama elektroonilise arvelduse lisandmooduli serverit. Funktsiooni seadistus hõlmab muu hulgas ER-i konfiguratsiooni vormingute kasutamist, et luua konfigureeritavaid ekspordi- ja impordifaile, ning tegevuste ja tegevusvoogude kasutamist, et luua konfigureeritavaid reegleid taotluste saatmiseks, vastuste importimiseks ning vastuste sisu sõelumiseks.

Järgmisel illustratsioonil on kujutatud elektroonilise arvelduse lisandmooduli funktsiooni põhikomponendid.

![Elektroonilise arvelduse lisandmooduli funktsiooni ülevaade](media/e-Invoicing-services-feature-setup-Overview-e-Invoicing-feature.png)

Kuna arvete vormingud ja tegevusvood erinevad üksteisest, võib funktsiooni seadistus olla erinev riigi, regiooni või ärivajaduste tõttu.

## <a name="set-up-the-electronic-invoicing-add-on-feature"></a>Elektroonilise arvelduse lisandmooduli funktsiooni seadistamine

Seadistusprotsess tuleb viia lõpule RCS-i keskkonnas. Järgige neid samme, et luua uus elektroonilise arvelduse lisandmooduli funktsioon.

1. Logige oma RCS-i keskkonda sisse.
2. Valige tööruumi **Globaliseerimisfunktsioonid** jaotisest **Funktsioonid** paan **Elektroonilise arvelduse lisandmoodul**.
3. Valige lehel **Elektroonilise arvelduse lisandmooduli funktsioonid** suvand **Impordi**, et importida globaalsest hoidlast ER-i andmemudeli konfiguratsioon.
4. Valige **Lisa**, et luua elektroonilise arvelduse lisandmooduli funktsioon. Saate luua funktsiooni otsast peale või tuletada selle olemasolevast elektroonilise arvelduse lisandmooduli funktsioonist.

    ![Elektroonilise arvelduse lisandmooduli funktsiooni lisamine](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature.png)

> [!NOTE]
> Kui loote uue elektroonilise arvelduse lisandmooduli funktsiooni, on sellel versiooninumber ning selle vaikeolekuks on seatud **Mustand**.

### <a name="configurations"></a>Konfiguratsioonid

Konfiguratsioonid sisaldavad ER-i vormingu konfiguratsioone, mis on vajalikud teisendamiseks ja selliste failide loomiseks, mida vahetatakse kolmandate isikute veebiteenustega suheldes. Elektroonilise arvelduse lisandmooduli funktsioon võib sisaldada nii palju ER-i failivormingu konfiguratsioone, nagu on vaja, võttes arvesse veebiteenuse pakkujalt saadud integratsiooni tehnilist kirjeldust.

Järgige neid samme, et lisada ER-i vormingud elektroonilise arvelduse lisandmooduli funktsiooni.

1. Valige lehe **Elektroonilise arvelduse lisandmooduli funktsioonid** vahekaardil **Konfiguratsioonid** suvand **Lisa**, et lisada ER-i failivormingu konfiguratsioonid elektroonilise arvelduse lisandmooduli funktsiooni.

    ![Elektroonilise arvelduse lisandmooduli funktsiooni konfiguratsioonide lisamine](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature-Configurations.png)

    > [!NOTE]
    > Kui loote elektroonilise arvelduse lisandmooduli funktsiooni otsast peale, peate lisama käsitsi kõik ER-i failivormingu konfiguratsioonid. Kui tuletate elektroonilise arvelduse lisandmooduli funktsiooni olemasolevast funktsioonist, luuakse ER-i failivormingu konfiguratsioonid automaatselt, kuna need päritakse algsest elektroonilise arvelduse lisandmooduli funktsioonist.

2. Valige suvand **Redigeeri**, et avada leht **Vormingukujundaja**, kus saate redigeerida ER-i failivormingu konfiguratsiooni.

    ![Elektroonilise arvelduse lisandmooduli funktsiooni konfiguratsioonide redigeerimine](media/e-Invoicing-services-feature-setup-Select-Edit-e-Invoicing-feature-Configurations.png)

    > [!NOTE]
    > Vormingu redigeerimise ajal on konfiguratsiooni versiooni olekuks seatud **Mustand**.

3. Kasutage failivormingu konfiguratsiooni muutmiseks lehte **Vormingukujundaja**. Lisateavet leiate jaotisest [Elektrooniliste dokumentide konfiguratsioonide loomine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).

    ![Vormingukujundaja leht](media/e-Invoicing-services-feature-setup-ER-Format-designer.png)

### <a name="feature-setups"></a>Funktsiooniseadistused

Funktsiooniseadistused hõlmavad kolmanda isiku veebiteenusega suhtlemise ja turbereegleid. Elektroonilise arvelduse lisandmooduli funktsioonil võib olla nii palju funktsiooniseadistusi, kui on vaja, võttes arvesse ärireeglit, mida soovite täita.

Järgige neid samme, et lisada funktsiooniseadistused elektroonilise arvelduse lisandmooduli funktsiooni.

1. Valige lehe **Elektroonilise arvelduse lisandmooduli funktsioonid** vahekaardil **Seadistused** suvand **Lisa**, et lisada funktsiooniseadistused elektroonilise arvelduse lisandmooduli funktsiooni.

    ![Elektroonilise arvelduse lisandmooduli funktsiooni seadistuste lisamine](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature-Setups.png)

    > [!NOTE]
    > Kui loote elektroonilise arvelduse lisandmooduli funktsiooni otsast peale, peate lisama käsitsi kõik vajaminevad funktsiooniseadistused. Kui tuletate elektroonilise arvelduse lisandmooduli funktsiooni olemasolevast funktsioonist, luuakse kõik funktsiooniseadistused automaatselt, kuna need päritakse algsest elektroonilise arvelduse lisandmooduli funktsioonist.

2. Valige suvand **Redigeeri**, et redigeerida funktsiooni versiooni seadistust.

    ![Elektroonilise arvelduse lisandmooduli funktsiooni seadistuste redigeerimine](media/e-Invoicing-services-feature-setup-Select-Edit-e-Invoicing-feature-Setups.png)

3. Kasutage lehte **Funktsiooni versiooni seadistus**, et konfigureerida tegevusi, rakendatavuse reegleid ja muutujaid.

    ![Tegevused, rakendatavuse reeglid ja muutujad](media/e-Invoicing-services-feature-setup-View-Actions-Applicability-Rules-Variables.png)

### <a name="actions"></a>Tegevused

Tegevused on eelmääratletud loend toimingutest, mis käivitatakse järjestikku. Loend kajastab nende sammude jaotust, mis on vajalikud elektroonilise arvelduse lisandmooduli funktsiooni täielikuks käivitamiseks. Tegevused võivad samas elektroonilise arvelduse lisandmooduli funktsioonis hõlmata suhtlust mõlemas suunas: sihtkoha taotluse saatmine ja vastuse vastuvõtmine ning selle sisu sõelumine.

Iga tegevus sisaldab eelmääratletud loendit parameetritest, mis on vajalikud tegevuse eesmärgi saavutamiseks. Valikuliselt võidakse pakkuda lisaparameetreid.

#### <a name="actions-fasttab"></a>Tegevuste kiirkaart

Tegevuste haldamiseks jälgige lehe **Funktsiooni versioonide seadistus** vahekaardi **Tegevused** kiirkaardil **Tegevused** üht või mõlemat järgmistest sammudest.

- Valige **Uus** või **Kustuta**, et lisada uusi tegevusi või kustutada olemasolevaid.
- Valige **Üles** või **Alla**, et teisaldada valitud tegevused ruudustikus üles või alla ning seetõttu muuta nende käitamise järjestust. Tegevused käitatakse ülevalt alla järjekorras, milles need ruudustikus kuvatakse.

![Tegevuste haldamine](media/e-Invoicing-services-feature-setup-Manage-Actions.png)

Järgmises tabelis kirjeldatakse kiirkaardil **Tegevused** olevaid välju.

| Väli        | Kirjeldus |
|--------------|-------------|
| Tegevus       | Eelmääratletud tegevusi on kaheksa.<ul><li><strong>Allkirjasta dokument</strong></li><li><strong>FileStoreActionName</strong></li><li><strong>Teisenda dokument</strong></li><li><strong>Töötle vastust</strong></li><li><strong>Kutsu REST-i veebiteenust</strong></li><li><strong>Kutsu Mehhiko PAC teenust</strong></li><li><strong>Kutsu Brasiilia SEFAZ teenust</strong></li><li><strong>Kutsu Itaalia SDI teenust</strong></li></ul> |
| Tegevuse nimi  | Tegevuse nimi ja selle käivitamise järjekord. |
| Kirjeldus  | Tegevuse kirjeldus. |
| Luba korduskatsed | Täidetud märkeruut näitab, et tegevust saab uuesti proovida, kui eelmine katse ei õnnestunud. |
| Korduskatse tegevus | Uuesti proovimise korral see tegevus, millest alates uuesti proovitakse. Korduskatse lõpeb praeguse tegevuse juures (kaasav korduskatse). Tegevuste puhul, millel on parameetrid **Minimaalne taganemine** ja **Maksimaalne taganemine**, tähistavad need korduskatsete minimaalset ja maksimaalset arvu. |

#### <a name="parameters-fasttab"></a>Parameetrite kiirkaart

Kiirkaart **Parameetrid** hõlmab selle tegevuse parameetreid, mis on valitud kiirkaardil **Tegevused**.

![Parameetrite kiirkaart](media/e-Invoicing-services-feature-setup-View-Actions-Parameters.png)

Järgmises tabelis kirjeldatakse kiirkaardil **Parameetrid** olevaid välju.

| Väli       | Kirjeldus |
|-------------|-------------|
| Nimi        | Eelmääratletud loend parameetritest. Lisateavet leiate jaotisest [Parameetrite loend tegevuse järgi](#list-of-parameters-by-action). |
| Kirjeldus | Parameetri kirjeldus. |
| Väärtus       | Parameetri väärtus. |

#### <a name="list-of-parameters-by-action"></a>Parameetrite loend tegevuse järgi

Saadaolevad parameetrid erinevad sõltuvalt tegevusest, mis on valitud kiirkaardil **Tegevused**.

###### <a name="action-sign-document"></a>Tegevus: allkirjasta dokument

| Parameeter                             | Kirjeldus |
|---------------------------------------|-------------|
| Sisendfail                            | XML-dokumendist sisendfail, mis tuleb allkirjastada digitaalallkirja abil. |
| Serdi nimi                      | Talletatud serdi nimi. |
| Allkirja tüüp                        | Kasutatava allkirja tüüp. |
| Allkirjameetodi nimi                 | Allkirjameetodi nimi, mida kasutatakse digitaalallkirja loomiseks. |
| Referaatmeetodi nimi                    | Referaatmeetod, mida kasutatakse digitaalallkirjas referaatstringi loomiseks. |
| Kanoniseerimismeetodi nimi          | Kanoniseerimismeetod, mida kasutatakse allkirjaräsi arvutamiseks. |
| Viiteatribuudi nimi              | Atribuudi nimi, mis näitab, kus kohas tuleb viite ID allkirjaelemendile lisada. |
| Allkirjastatava elemendi nimi               | Dokumendis oleva XML-elemendi nimi, mis tuleb allkirjastada digitaalallkirja abil. Kui elementi pole määratud, allkirjastatakse dokumendi juur. |
| Sisestatavat allkirja sisaldava elemendi nimi   | XML-elemendi nimi, kuhu tuleb sisestada loodud digitaalallkiri. Kui elementi pole määratud, sisestatakse allkiri dokumendi juurde. |
| XLST-fail koos referaatteisendusega       | Laiendatava vormingukeele teisenduse (XSLT) fail, mis sisaldab referaatvastenduse reegleid, et luua digitaalallkirja jaoks referaatstring. |
| Tee referaatstringi lisamiseks          | Vormingus **\<elementName\>.\<Attribute.Path\>** tee, mis näitab asukohta, kuhu loodud referaatstring tuleb sisestada. |
| Serdinumbri asukoht           | Elemendi ja atribuudi nimi, kuhu tuleb sisestada serdinumber. |
| Serdiandmete asukoht          | Elemendi ja atribuudi nimi, kuhu tuleb sisestada serdiandmed (Base64). |
| Serdinumber on ASCII-vormingus | Väärtus, mis määrab, kas serdinumber on kodeeritud ASCII-vormingus. |

###### <a name="action-filestoreactionname"></a>Tegevus: FileStoreActionName

| Parameeter  | Kirjeldus |
|------------|-------------|
| Sisendfail | Talletatav sisendfail. |

###### <a name="action-transform-document"></a>Tegevus: teisenda dokument

| Parameeter                       | Kirjeldus |
|---------------------------------|-------------|
| Sisendfail                      | Lähtefail, mis sisaldab andmeid, mida tuleb tegevuse korral rakendada. |
| Suund                       | Väärtus, mis näitab, kas tuleb kasutada impordi- või ekspordivormingut. |
| Konfiguratsiooni ID                | Vorming, mis tuleb käivitada. |
| Konfiguratsiooni versioon           | Kui konfiguratsiooni versiooni pole määratud, kasutatakse kõige uuemat versiooni. |
| Konfiguratsiooni integratsioonipunkt | Lähtefail, mis sisaldab andmeid aruandluse käitusaja jaoks. |

###### <a name="action-process-response"></a>Tegevus: töötle vastust

| Parameeter                    | Kirjeldus |
|------------------------------|-------------|
| Sisendfail                   | Analüüsitav vastus. |
| Aruandluse konfiguratsiooni loend | Konfiguratsioonide loend, mida kasutatakse vastuste sõelumiseks. |

###### <a name="action-call-rest-web-service"></a>Tegevus: kutsu REST-i veebiteenust

| Parameeter                   | Kirjeldus |
|-----------------------------|-------------|
| Veebiteenuse URL             | URL, kuhu päringuid saata. |
| Veebipäringu ajalõpp         | Maksimaalne veebiteenuse vastuse ootamise aeg (millisekundites). |
| Päringu toimingu tüüp      | HTTP-päringu toimingu tüüp (nt **GET**, **POST** või **DELETE**). |
| Serdinimed           | Serdinimed. |
| Vastuse keha kodeering      | HTTP-vastuse keha eeldatav kodeering, et seda saaks õigesti dekodeerida. |
| HTTP-päringu sisu tüüp   | HTTP-päringu sisu tüübi päise sisend. |
| HTTP-päringu sisu keha   | HTTP-päringu keha. (Keha võib olla tühi.) |
| HTTP parameetri päringuväärtused | Parameetri päringuväärtused, mida kasutatakse URL-i täitmiseks muutuvate parameetritega. |
| Päringu marsruut               | HTTP-päringu marsruut. Muutuvaid parameetreid saab esitada nii: **\{paramName\}**. Siin on näide: **"api/{id}/submit"**. |
| Marsruudi parameetriloend        | Marsruudi parameetrid võtme ja väärtuste paaridena, mida kasutatakse muutujate lisamiseks marsruuti. |
| Kohandatud HTTP-päised         | Päringusse sisestamiseks mõeldud kohandatud HTTP-päised. |
| HTTP-päringu küpsised        | Loend küpsistest, mis on esitatud võtme ja väärtuse paaridena, mis tuleb sisestada HTTP küpsiste päise päringusse. |
| Turbeprotokoll           | Turbeprotokoll, mida tuleb kasutada HTTP-päringute puhul serveriga suhtlemiseks. (Vaikimisi kasutatakse transpordikihi turbeprotokolli \[TLS\] versiooni 1.2.) |

###### <a name="action-call-mexican-pac-service"></a>Tegevus: kutsu Mehhiko PAC teenust

| Parameeter                | Kirjeldus |
|--------------------------|-------------|
| Sisendfail               | Fail, mis sisaldab XML-andmeid, mis saadetakse veebiteenusele meetodi sisendparameetrina. |
| URL-aadress              | Veebiteenuse aadress (lõpp-punkt). |
| Veebimeetodi (tegevuse) nimi | Veebimeetodi (tegevuse) nimi, mis tuleb käivitada. |
| Serdid             | Serdiahel, mida veebiteenus vajab kliendi autentimiseks. Kliendi sert peaks olema ahelas viimane sert. Juur- ja vaheserdid peaksid olema esimesed. |
| Veebipäringu ajalõpp      | Maksimaalne veebiteenuse vastuse ootamise aeg (millisekundites). |
| Korduskatsete intervall           | Veebiteenuse kutsumise ja sellelt vastuse saamise katsete vaheline intervall. Kui intervalli pole määratud, ei proovita pärast esimest nurjunud kutset uuesti. |
| Uuesti proovimiste arv              | Veebiteenuse kutsumise ja sellelt vastuse saamise korduskatsete maksimaalne arv. |
| Korduskatsete kestus               | Maksimaalne aeg (millisekundites), mille jooksul korduskutsed võivad kesta. |
| Minimaalne taganemine         | Minimaalne taganemise määr korduskatsete intervallide eksponentsiaalseks arvutamiseks. |
| Maksimaalne taganemine         | Maksimaalne taganemise määr korduskatsete intervallide eksponentsiaalseks arvutamiseks. |
| Turbeprotokoll        | Turbeprotokoll, mida tuleb kasutada HTTP-päringute puhul serveriga suhtlemiseks. (Vaikimisi kasutatakse protokolli TLS 1.2.) |

###### <a name="action-call-brazilian-sefaz-service"></a>Tegevus: kutsu Brasiilia SEFAZ teenust

| Parameeter                | Kirjeldus |
|--------------------------|-------------|
| Sisendfail               | Fail, mis sisaldab XML-andmeid, mis saadetakse veebiteenusele meetodi sisendparameetrina. |
| URL-aadress              | Veebiteenuse aadress (lõpp-punkt). |
| Veebimeetodi (tegevuse) nimi | Veebimeetodi (tegevuse) nimi, mis tuleb käivitada. |
| Serdid             | Serdiahel, mida veebiteenus vajab kliendi autentimiseks. Kliendi sert peaks olema ahelas viimane sert. Juur- ja vaheserdid peaksid olema esimesed. |
| Veebipäringu ajalõpp      | Maksimaalne veebiteenuse vastuse ootamise aeg (millisekundites). |
| Korduskatsete intervall           | Veebiteenuse kutsumise ja sellelt vastuse saamise katsete vaheline intervall. Kui intervalli pole määratud, ei proovita pärast esimest nurjunud kutset uuesti. |
| Uuesti proovimiste arv              | Veebiteenuse kutsumise ja sellelt vastuse saamise korduskatsete maksimaalne arv. |
| Korduskatsete kestus               | Maksimaalne aeg (millisekundites), mille jooksul korduskutsed võivad kesta. |
| Minimaalne taganemine         | Minimaalne taganemise määr korduskatsete intervallide eksponentsiaalseks arvutamiseks. |
| Maksimaalne taganemine         | Maksimaalne taganemise määr korduskatsete intervallide eksponentsiaalseks arvutamiseks. |
| Turbeprotokoll        | Turbeprotokoll, mida tuleb kasutada HTTP-päringute puhul serveriga suhtlemiseks. (Vaikimisi kasutatakse protokolli TLS 1.2.) |

###### <a name="action-call-italian-sdi-service"></a>Tegevus: kutsu Itaalia SDI teenust

| Parameeter                | Kirjeldus |
|--------------------------|-------------|
| Sisendfail               | Fail, mis sisaldab XML-andmeid, mis saadetakse veebiteenusele meetodi sisendparameetrina. |
| URL-aadress              | Veebiteenuse aadress (lõpp-punkt). |
| Veebimeetodi (tegevuse) nimi | Veebimeetodi (tegevuse) nimi, mis tuleb käivitada. |
| Serdid             | Serdiahel, mida veebiteenus vajab kliendi autentimiseks. Kliendi sert peaks olema ahelas viimane sert. Juur- ja vaheserdid peaksid olema esimesed. |
| Veebipäringu ajalõpp      | Maksimaalne veebiteenuse vastuse ootamise aeg (millisekundites). |
| Korduskatsete intervall           | Veebiteenuse kutsumise ja sellelt vastuse saamise katsete vaheline intervall. Kui intervalli pole määratud, ei proovita pärast esimest nurjunud kutset uuesti. |
| Uuesti proovimiste arv              | Veebiteenuse kutsumise ja sellelt vastuse saamise korduskatsete maksimaalne arv. |
| Korduskatsete kestus               | Maksimaalne aeg (millisekundites), mille jooksul korduskutsed võivad kesta. |
| Minimaalne taganemine         | Minimaalne taganemise määr korduskatsete intervallide eksponentsiaalseks arvutamiseks. |
| Maksimaalne taganemine         | Maksimaalne taganemise määr korduskatsete intervallide eksponentsiaalseks arvutamiseks. |
| Turbeprotokoll        | Turbeprotokoll, mida tuleb kasutada HTTP-päringute puhul serveriga suhtlemiseks. (Vaikimisi kasutatakse protokolli TLS 1.2.) |

### <a name="applicability-rules"></a>Rakendatavuse reeglid

Rakendatavuse reeglid võimaldavad teil luua loogilisi reegleid, mis määravad funktsiooniseadistuse kasutuse konteksti. Seega valitakse edastatud dokumendi töötlemiseks kasutatav elektroonilise arvelduse lisandmooduli funktsioon töötlemisele saadetud äridokumendis sisalduva konteksti ja rakendatavuse reegli kriteeriumide ühtimise põhjal.

#### <a name="set-up-applicability-rules"></a>Rakendatavuse reeglite seadistamine

1. Valige lehel **Funktsiooni versiooni seadistus** vahekaardil **Rakendatavuse reeglid** suvand **Uus**, et lisada rakendatavuse reegel.

    ![Rakendatavuse reeglite haldamine](media/e-Invoicing-services-feature-setup-Manage-Actions-Applicability-rules.png)

2. Valige ruudustikus klauslid, mis tuleks rühmitada.
3. Valige **Rühmita klausel**.

    ![Klauslite rühmitamine](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-Group-clause.png)

    Pärast klauslite rühmitamist lisatakse ruudustikku uus veerg. See veerg määrab rühmitatud klauslite jaoks loogilise tehtemärgi.

    ![Loogiline tehtemärk rühmitatud klauslite jaoks](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-Group-criterias.png)

Klauslite rühmituse tühistamiseks valige rühmitatud klauslid ja seejärel suvand **Tühista klausli rühmitus**.

![Klauslite rühmituse tühistamine](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-UnGroup-criterias.png)

> [!NOTE]
> Klausli rühmituse tühistamise korral alustage alati kõige sisemisest rühmitustasemest.

Järgmises tabelis kirjeldatakse vahekaardil **Rakendatavuse reeglid** olevaid välju.

| Väli         | Kirjeldus |
|---------------|-------------|
| Ja/või        | Loogiline tehtemärk. |
| Väli         | Väli, mida kasutatakse reegli koostamiseks. |
| Tehtemärgi tüüp | Tehtemärgi tüüp.<ul><li>Võrdne</li><li>Pole võrdne</li><li>Suurem kui/väiksem kui</li><li>Suurem kui või võrdne / väiksem kui või võrdne</li><li>Sisaldab</li><li>Algab viisil</li></ul> |
| Väärtus         | Reegli kriteerium. |

### <a name="variables"></a>Muutujad

Saate luua muutujaid ja seejärel kasutada neid konkreetse tegevuse parameetri sisendväärtusena. Samuti saate neid kasutada elektroonilise arvelduse lisandmooduli teenuste ja kliendi vahel teabe vahetamiseks, mis juhtub edastusvoo osana konkreetse tegevuse käivitamise tõttu.

#### <a name="set-up-variables"></a>Muutujate seadistamine

- Valige lehe **Funktsiooni versiooni seadistus** vahekaardil **Muutujad** suvand **Uus** või **Kustuta**, et muutujaid hallata.

    ![Muutujate haldamine](media/e-Invoicing-services-feature-setup-Manage-Variables.png)

Järgmises tabelis kirjeldatakse vahekaardil **Muutujad** olevaid välju.

| Väli       | Kirjeldus |
|-------------|-------------|
| Nimi        | Muutuja nimi. |
| Kirjeldus | Muutuja lühikirjeldus. |
| Tüüp        | Muutuja tüüp.<ul><li><strong>Konstant</strong> – muutuja sisu ei muutu.</li><li><strong>Kliendist</strong> – muutuja sisu hangitakse edastusprotsessi käivitamise käigus rakenduse Microsoft Dynamics 365 kliendist.</li><li><strong>Klienti</strong> – rakenduse Microsoft Dynamics 365 klient paneb muutuja sisu edastusprotsessi käivitamise käigus importimiseks valmis.</li></ul> |
| Andmetüüp   | Muutuja andmetüüp.<ul><li>Kahendmuutuja</li><li>Kuupäev</li><li>Arv</li><li>UUID</li><li>String</li><li>Fail</li></ul> |
| Väärtus       | Muutuja väärtus või selle väärtust määrava tegevuse nimi. |

### <a name="validate-the-feature-setup"></a>Funktsiooniseadistuse kontrollimine

- Valige lehe **Funktsiooni versiooni seadistus** toimingupaanilt suvand **Kontrolli**, et kontrollida funktsiooni versiooni seadistust.

   ![Nupu „Kontrolli” valimine](media/e-Invoicing-services-feature-setup-Select-Validate-Button.png)

Kontrollimise käigus kontrollitakse kogu konfiguratsiooni terviklikkust. Näiteks kui tegevuse puhul on mõni konkreetne parameeter kohustuslik, kuid selle väärtus on tühi, tuvastatakse see vastuolu kontrollimise käigus ja teile näidatakse tõrget.

## <a name="environments"></a>Keskkonnad

Elektroonilise arvelduse lisandmooduli keskkond tuleb seostada elektroonilise arvelduse lisandmooduli funktsiooniga ja selle jaoks lubada. Elektroonilise arvelduse lisandmooduli keskkonnad tuleb luua ja avaldada varem, kasutades organisatsiooni RCS-i kontol olevat globaliseerimisfunktsioonide konfiguratsiooni.

Elektroonilise arvelduse lisandmooduli keskkonna lubamiseks elektroonilise arvelduse lisandmooduli funktsiooni jaoks toimige järgmiselt.

1. Valige lehe **Elektroonilise arvelduse lisandmooduli funktsioonid** vahekaardil **Keskkonnad** suvand **Luba**, et lisada elektroonilise arvelduse lisandmooduli keskkond.
2. Sisestage väljale **Kehtiv alates** kuupäev, mil uus keskkond kehtima hakkab.

![Elektroonilise arvelduse lisandmooduli keskkonna lubamine](media/e-Invoicing-services-feature-setup-Select-Enable-e-Invoicing-feature-Environment.png)

## <a name="organizations"></a>Organisatsioonid

Elektroonilise arvelduse lisandmooduli funktsiooni saab jagada mitme organisatsiooniga.

- Valige lehe **Elektroonilise arvelduse lisandmooduli funktsioonid** vahekaardil **Organisatsioonid** suvand **Jaga**, et lisada organisatsioon, millega soovite jagada elektroonilise arvelduse lisandmooduli funktsiooni.

Kui soovite lõpetada elektroonilise arvelduse lisandmooduli funktsiooni jagamise organisatsiooniga, valige **Tühista jagamine**.

## <a name="versions"></a>Versioonid

Versioonid aitavad kontrollida elektroonilise arvelduse lisandmooduli funktsiooni töötsüklit, hallates selle olekut. Saate luua olemasoleva elektroonilise arvelduse lisandmooduli funktsiooni uue versiooni või seada funktsiooni oleku väärtuseks **Lõpetatud** ja seejärel **Avalda**, kui elektroonilise arvelduse lisandmooduli funktsiooni konfigureerimine on täielikult lõpetatud.

### <a name="create-a-new-version-of-an-existing-electronic-invoicing-add-on-feature"></a>Olemasoleva elektroonilise arvelduse lisandmooduli funktsiooni uue versiooni loomine

1. Valige lehel **Elektroonilise arvelduse lisandmooduli funktsioonid** vasakpoolsest ruudustikust elektroonilise arvelduse lisandmooduli funktsioon.
2. Valige vahekaardil **Versioonid** suvand **Uus**, et lisada elektroonilise arvelduse lisandmooduli funktsiooni uus versioon.

### <a name="change-the-status-of-the-electronic-invoicing-add-on-feature"></a>Elektroonilise arvelduse lisandmooduli funktsiooni oleku muutmine

Järgige neid samme, et hallata elektroonilise arvelduse lisandmooduli funktsiooni töötsüklit.

1. Valige lehel **Elektroonilise arvelduse lisandmooduli funktsioonid** vasakpoolsest ruudustikust elektroonilise arvelduse lisandmooduli funktsioon.
2. Valige vahekaardil **Versioonid** suvand **Muuda olekut** ja seejärel muutke olek väärtuselt **Mustand** väärtuseks **Lõpetatud**.
3. Teil palutakse kinnitada, et soovite lõpetada elektroonilise arvelduse lisandmooduli funktsiooni ja kõik selle komponendid. Tegevuse kinnitamiseks valige **Jah** või selle tühistamiseks **Ei**.

    > [!NOTE]
    > Kui valite valiku **Jah**, muudetakse konfiguratsiooni versioonide (mis on elektroonilise arvelduse lisamooduli funktsiooni komponendid) olek automaatselt väärtuselt **Mustand** väärtuseks **Lõpetatud**.

4. Valige suvand **Muuda olekut** ja seejärel muutke olek väärtuselt **Lõpetatud** väärtuseks **Avalda**.
5. Teil palutakse kinnitada, et soovite avaldada elektroonilise arvelduse lisandmooduli funktsiooni ja kõik selle komponendid globaalses hoidlas. Tegevuse kinnitamiseks valige **Jah** või selle tühistamiseks **Ei**.

    > [!NOTE]
    > Kui valite **Jah**, muudetakse konfiguratsiooni versioonide olek automaatselt olekust **Lõpetatud** olekuks **Jagatud**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]