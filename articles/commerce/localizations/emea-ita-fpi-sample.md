---
title: Fiskaalprinteri integratsiooni näide Itaalia jaoks
description: Selles teemas antakse ülevaade Fiskaalintegratsiooni näidistest Itaalia jaoks teemas Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2018-11-1
ms.openlocfilehash: 592cecff5b6179e7afd1bacb25beda277dfb8fa3
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944630"
---
# <a name="fiscal-printer-integration-sample-for-italy"></a>Fiskaalprinteri integratsiooni näide Itaalia jaoks

[!include[banner](../includes/banner.md)]

Selles teemas antakse ülevaade Fiskaalintegratsiooni näidistest Itaalia jaoks teemas Microsoft Dynamics 365 Commerce.

Itaalia ärifunktsioon hõlmab kassa (POS) näidisintegratsiooni fiskaalprinteriga. Näidis laiendab fiskaalintegratsiooni funktsiooni nii, et see töötab Epson FP-90III seeriaprinteritega Epsonist ja võimaldab finantsprinteriga suhtlemist veebiserveri režiimis EpsonFPMate veebiteenuse kaudu, kasutades [...](fiscal-integration-for-retail-channel.md)[fiskaal](https://www.epson.it/products/sd/pos-printer/epson-fp-90iii-series)-ePOS-print API-t. Näidis toetab ainult Registratore Telemaregistri (RT) režiimi. Näidis esitatakse lähtekoodina ja on osa jaemüügi tarkvara arenduskomplektist (SDK).

Microsoft ei vabasta Epsoni riistvara, tarkvara ega dokumentatsiooni. Fiskaalprinteri saamiseks ja selle käsitsemiseks võtke ühendust [Epson Epso S.p.A-ga](https://www.epson.it).

## <a name="scenarios"></a>Stsenaariumid

Järgmisi stsenaariume hõlmab Fiskaalprinteri integratsiooni näidis Itaalia jaoks:

- Müügistsenaariumid:

    - Printige fiskaalsissetulek sularaha ja edasimüügi ning tagastuste jaoks.
    - Fikseerige fiskaalprinteri vastus ja salvestage see kanali andmebaasi.
    - Maksud:

        - Vastendage fiskaalprinteri maksukoodidega (osakonnad).
        - Vastendatud maksuandmete ülekandmine fiskaalprinterisse.
        - Prinditakse fiskaalsissetuleku maksud.

    - Maksed:

        - Vastendage fiskaalprinteri makseviisid.
        - Prindib maksed fiskaalsissetulekutele.
        - Prindib muudatuse teabe.

    - Saate printida rea allahindlused.
    - Kinkekaardid:

        - Välistage müügi fiskaalsissetulekult väljastatud/uuesti küsitud kinkekaardi rida.
        - Printige makse, mis kasutab tavalise makseviisina kinkekaarti.

    - Prindib klienditellimuse toimingute fiskaalsissetulekud:

        - Klienditellimuse deposiidi jaoks ei prindita fiskaalsissetulekit.
        - Printige klienditellimuse tarneridade fiskaalsissetulek.
        - Printige klienditellimuse vastuvõtmise toimingu fiskaalsissetulek.
        - Printige tagastustellimuse fiskaalsissetulek.

    - Prinditakse fiskaalsissetuleku kviitungi numbri vöötkood.
    - [Printige](emea-ita-customer-information.md) fiskaalsissetuleku müügikande jaoks määratud klienditeave. Selle teabe näiteks on kliendi kood. 

- Päeva lõpetamise laused (fiskaal X- ja fiskaal-Z-aruanded).
- Tõrkekäsitlus, nt järgmised valikud:

    - Kui on võimalik, et fiskaalprinterit saab uuesti registreerida, nt kui fiskaalprinter ei ole ühendatud, ei ole valmis või ei vasta sellele, on printerist paber väljas või on olemas paberi jada.
    - Finantsregistreerimise edasilükkamine.
    - Jätte fiskaalregistreerimise vahele või märgite kande registreeritud koodina ja kaasate teabekoodid, et hõivata tõrke põhjus ja lisateave.
    - Kontrollige fiskaalprinteri saadavust enne uue müügikande avamist või müügikande sulgemist.

### <a name="gift-cards"></a>Kinkekaardid

Fiskaalprinteri integreerimise näidis juurutab järgmised kinkekaartidega seotud reeglid:

- Välistage fiskaalsissetuleku kinkekaardi toimingutesse *väljastamise* *kinkekaardiga* seotud müügiread.
- Kui see koosneb ainult kinkekaardi ridadest, siis ärge printige fiskaalkviitungit.
- Lahutage fiskaalsissetuleku makseridadelt kandes väljastatud või uuesti sisse küsitavate kinkekaartide kogusumma.
- Salvestage makseridade arvutatud korrigeerimised kanali andmebaasis viitega vastavale fiskaalkandele.
- Kinkekaardiga maksmine on tavamakse.

### <a name="customer-deposits-and-customer-order-deposits"></a>Kliendi deposiitid ja kliendi tellimuse deposiidid

Fiskaalprinteri integratsiooni näidis juurutab järgmised kliendi deposiitide ja klienditellimuse deposiittega seotud reeglid:

- Ärge printige fiskaalsissetulekit, kui kanne on kliendi deposiit.
- Ärge printige fiskaalsissetulekit, kui kanne sisaldab ainult klienditellimuse deposiiti või klienditellimuse deposiidi tagasimakset.
- Prindib kliendi tellimuse vastuvõtmise toimingu jaoks eelnevalt makstud deposiidi summa fiskaalsissetulekil.
- Klienditellimuse deposiidisumma arvatakse hankija tellimuse loomisel maha makseridadelt.
- Salvestage makseridade arvutatud korrigeerimised kanali andmebaasis viitega klienditellimuse fiskaalkandele.

### <a name="limitations-of-the-sample"></a>Näidiste piirangud

- Fiskaalprinter toetab ainult stsenaariume, kus hind sisaldab käibemaksu. Seetõttu peab nii kaupluste kui ka klientide puhul valik Hind **sisaldama** käibemaksu **väärtuseks** olema seatud Jah.
- Päevaaruanded (fiskaal X ja fiskaal Z) prinditakse fiskaalprinteri sse manustatud vormingu abil.
- Fiskaalprinter ei toeta segatud kandeid. Valik **Keela müügi ja tagastuste segamine ühes kviitungis tuleks kassa funktsiooniprofiilides seada** **väärtusele** Jah.
- Näidis toetab integreerimist ainult fiskaalprinteriga, mis töötab Registratore Telemagrammis (RT)) režiimis.

## <a name="set-up-fiscal-integration-for-italy"></a>Saate häälestada Itaalia rahandusintegratsiooni.

Itaalia fiskaalprinteri integratsiooni näidis põhineb [fiskaalintegratsiooni funktsioonil ja](fiscal-integration-for-retail-channel.md) on osa Retail SDK-st. Näidis asub lahenduste hoidla **kaustas \\\\ FiscalIntegration EpsonFP90IIISample (näiteks näidis**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/)[väljalaskes/9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/EpsonFP90IIISample) Näidis [koosneb fiskaaldokumendi pakkujast, mis on Commerce Runtime'i () laiendus, ja fiskaalühendusest, mis](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices)CRT on Commerce Hardware Stationi laiendus. Lisateavet Retail SDK kasutamise kohta vt [Retail SDK arhitektuurist](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [iseseisva pakendamise SDK koostamisvõimaluste häälestamisest](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Uue sõltumatu pakendi- ja laiendusmudeli piirangute tõttu ei saa seda praegu selle [fiskaalintegratsiooni](../dev-itpro/build-pipeline.md) näidise jaoks kasutada. Retail SDK eelmist versiooni peate kasutama arendaja virtuaalmasinas (VM) Microsoft Dynamics elutsükli teenustes (LCS). Lisateavet vt Itaalia [(pärand) fiskaalprinteri integratsiooni näidise juurutuse](emea-ita-fpi-sample-sdk.md) juhised.
>
> Uutesse versioonidesse planeeritakse fiskaalintegratsiooni valimite uue sõltumatu pakendi- ja laiendusmudeli tugi.

Viige finantsintegratsiooni seadistuse etapid lõpule, nagu [on kirjeldatud Ärikanalite fiskaalintegratsiooni seadistamises](setting-up-fiscal-integration-for-retail-channel.md).

1. [Seadistage fiskaalregistreerimise protsess](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Lisaks tehke märkus fiskaalregistreerimise protsessi sätete kohta, mis on sellele [fiskaalprinteri integreerimisnäidsele spetsiifilised](#set-up-the-registration-process).
1. [Saate seadistada allahindluste](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts) finantstekste.
1. [Tõrke käsitlemise sätete](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings) seadistamine.
1. [Seadistage kassast finants-X/Z-aruanded.](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos)
1. [Luba edasilükatud fiskaalregistreerimise käsitsi](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration) käivitamine.
1. [Seadistage klienditeabe haldamise funktsioon](emea-ita-customer-information.md#setup) kassas.
1. [Kanali komponentide](#configure-channel-components) konfigureerimine.

### <a name="set-up-the-registration-process"></a>Registreerimisprotsessi häälestamine

Registreerimisprotsessi lubamiseks järgige neid samme Commerce headquartersi häälestamiseks. Lisateavet vt Commerce'i [kanalite fiskaalintegratsiooni](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) häälestamine.

1. Laadige alla finantsdokumendi pakkuja ja fiskaalkonnektori konfiguratsioonifailid:

    1. Lahenduste [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidla avamine.
    1. Valige õige väljalaske haruversioon vastavalt oma SDK-le/rakenduse versioonile (nt **[vabastamine/9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**
    1. Saate **avada src \>\> FiscalIntegrationi EpsonFP90IIISample.**
    1. Laadige alla finantsdokumendi pakkuja **konfiguratsioonifail commerceRuntime \> DocumentProvider.EpsonFP90IIISample \> Configuration \> DocumentProviderEpsonFP90IIISample.xml** (nt [väljalaske/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/EpsonFP90IIISample/CommerceRuntime/DocumentProvider.EpsonFP90IIISample/Configuration/DocumentProviderEpsonFP90IIISample.xml) fail).
    1. Laadige fiskaalkonnektori konfiguratsioonifail alla **failis HardwareStation \> EpsonFP90IIIFiscalDeviceSample \> Configuration \> ConnectorEpsonFP90IIISample.xml (nt väljalaske**[9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/EpsonFP90IIISample/HardwareStation/EpsonFP90IIIFiscalDeviceSample/Configuration/ConnectorEpsonFP90IIISample.xml) fail).

    > [!WARNING]
    > Uue sõltumatu pakendi- ja laiendusmudeli piirangute tõttu ei saa seda praegu selle [fiskaalintegratsiooni](../dev-itpro/build-pipeline.md) näidise jaoks kasutada. Retail SDK eelmist versiooni peate kasutama LCS-i arendaja VM-s. Selle fiskaalintegratsiooni näidiskonfiguratsiooni failid asuvad Retail SDK arendaja VM LCS-i kaustades:
    >
    > - **Fiskaaldokumendi pakkuja konfiguratsioonifail:** RetailSdk \\ SampleExtensions \\ CommerceRuntime \\ Extension.DocumentProvider.EpsonFP90IIISample \\ konfiguratsiooni \\ DocumentProviderEpsonFP90IIISample.xml
    > - **Fiskaalkonnektori konfiguratsioonifail:** RetailSdk \\ SampleExtensions \\ HardwareStation \\ Extension.EpsonFP90IIIFiscalDeviceSample \\ Configuration \\ ConnectorEpsonFP90IIISample.xml
    > 
    > Uutesse versioonidesse planeeritakse fiskaalintegratsiooni valimite uue sõltumatu pakendi- ja laiendusmudeli tugi.

1. Valige suvandid **Jaemüük ja kaubandus \> Headquartersi häälestus \> Parameetrid \> Commerce’i ühiskasutuses parameetrid**. Seadke **vahekaardil** Üldine suvand Luba **fiskaalintegratsioon** väärtusele **Jah**.
1. Minge jaemüügi **ja ärikanali häälestuse \>\> fiskaalintegratsiooni finantsdokumendi pakkujate juurde ja laadige varem alla \>** laaditud finantsdokumendi pakkuja konfiguratsioonifail.
1. Minge **jaemüügi- ja ärikanali \>\>\> häälestuse fiskaalintegratsiooni fiskaalkonnektori ja laadige varem alla** laaditud fiskaalkonnektori konfiguratsioonifail.
1. Minge jaemüügi ja **ärikanali \> häälestuse \> fiskaalintegratsiooni \> konnektori** funktsiooniprofiilidesse. Looge uus konnektori funktsiooniprofiil. Valige dokumendipakkuja ja ühendus, mille varem laadisite. Värskendage [andmevastendussätted](#default-data-mapping) vastavalt vajadusele.
1. Minge jaemüügi ja **ärikanali \> häälestuse \> finantsintegratsiooni \> konnektori tehnilistesse** profiilidesse. Looge uus konnektori tehniline profiil ja valige varem laaditud fiskaalühendus. Uuendage [konnektori](#fiscal-connector-settings) sätteid vastavalt vajadusele.
6. Minge jaemüügi ja **ärikanali \> häälestuse \> fiskaalintegratsiooni \> fiskaalühenduse gruppidesse**. Looge varem loodud konnektori funktsiooniprofiilile uus fiskaalühenduse grupp.
7. Minge jaemüügi **ja ärikanali häälestuse \> fiskaalintegratsiooni \>\> fiskaalregistreerimisprotsessidesse.** Looge uus fiskaalregistreerimise protsess ja fiskaalregistreerimise protsessi samm ning valige varem loodud fiskaalühenduse grupp.
8. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Funktsiooniprofiilid**. Valige funktsiooniprofiil, mis on lingitud kauplusega, kus registreerimisprotsess tuleks aktiveerida. Valige **finants registreerimisprotsessi** kiirkaardil varem loodud fiskaalregistreerimise protsess.
9. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Riistvaraprofiilid**. Valige riistvaraprofiil, mis on lingitud riistvarajaamaga, millega fiskaalprinter on ühendatud. Valige **kiirkaardil Fiscal** peripherals varem loodud konnektori tehniline profiil.
10. Avage jaotusgraafik (Retail ja Commerce Retail ja Commerce IT Distribution schedule) ning valige tööd **\>\>** **1070 ja** **1090 andmete** edastamiseks kanali andmebaasi.

#### <a name="default-data-mapping"></a>Vaikeandmete vastendamine

Järgmine vaikeandmete vastendamine on kaasatud fiskaaldokumendi pakkuja konfiguratsiooni, mis antakse fiskaalintegratsiooni näidisosana:

- **Maksevahendi tüübi** vastendamine : kaupluse jaoks konfigureeritud makseviiside vastendamine fiskaalprinteri toetud maksetüüpidega. Järgmine näide näitab vaikevastendust.

    ```JSON
    {"PaymentMethods": [
        {"StorePaymentMethod":"1", "PrinterPaymentType":"0", "PrinterPaymentIndex":"00"},
        {"StorePaymentMethod":"3", "PrinterPaymentType":"2", "PrinterPaymentIndex":"00"},
        {"StorePaymentMethod":"4", "PrinterPaymentType":"2", "PrinterPaymentIndex":"01"},
        {"StorePaymentMethod":"6", "PrinterPaymentType":"0", "PrinterPaymentIndex":"01"},
        {"StorePaymentMethod":"8", "PrinterPaymentType":"6", "PrinterPaymentIndex":"01"}
        ],
        "DepositPaymentMethod": {"PrinterPaymentType":"2", "PrinterPaymentIndex":"00"}}
    ```

    Siin on atribuutide selgitus selles vastendamises:

    - **StorePaymentMethod on makseviis, mis on häälestatud kauplusele** **Kaupluses ja Ärikanali \>\> häälestuses \>** Makseviisid.
    - **PrinterPaymentType ja PrinterPaymentIndex on vastav maksetüüp ja indeks, mis on määratletud** **Epsoni** fiskaalprinteri dokumentatsioonis.
    - **DepositPaymentMethodit kasutatakse printeri maksetüübi ja indeksi määramiseks kliendi tellimuse pealevõtja summa osa jaoks, mis tasakaalustatakse kliendi tellimuse** deposiidiga.

    Järgmises tabelis on näidatud, kuidas makseviiside näidisvastendus vastab standardsete demoandmete jaoks konfigureeritud makseviiside talletamiseks.

    | Makseviis | Makseviisi nimi |
    |----------------|---------------------|
    | 1              | Sularaha                |
    | 3              | Kaart                |
    | 4              | Kliendi konto    |
    | 6              | Valuuta            |
    | 8              | Kinkekaart           |

    Peate muutma näidisvastendust vastavalt maksemeetoditele, mis on teie rakenduses konfigureeritud.

- **Kviitungi numbri vöötkoodi tüüp – vöötkoodi tüüp, mida kasutatakse** fiskaalsissetuleku sissetuleku numbri näitamiseks. Vaikimisi vastendamine on **CODE128**.
- **Prindi finantsandmed kviitungi** päisesse – kui see parameeter on sisse lülitatud, prinditakse fiskaalsissetuleku teave. See teave sisaldab kaupluse nime, aadressi, maksu ID-koodi ja kassapidaja nime.
- **Fiskaalprinteri osakonna vastendamine – fiskaalprinteri osakondade vastendamine** käibemaksumääradega, KM-määradega, KM-määradega ja tootetüüpidega. Järgmine näide näitab vaikevastendust.

    ```JSON
    {"Departments": [
        {"VATRate":"2200", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"01"},
        {"VATRate":"2200", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"02"},
        {"VATRate":"1000", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"03"},
        {"VATRate":"1000", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"04"},
        {"VATRate":"0500", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"05"},
        {"VATRate":"0500", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"06"},
        {"VATRate":"0400", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"07"},
        {"VATRate":"0400", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"08"},
        {"VATRate":"0000", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"09"},
        {"VATRate":"0000", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"10"},
        {"VATRate":"0000", "VATExemptNature":"NS", "ProductType":"0", "DepartmentNumber":"99"}]}
    ```

    Siin on atribuutide selgitus selles vastendamises:

    - **VATRate** on toetatud KM-määr, mis on konfigureeritud käibemaksukoodina. Vastendamise väärtusel on kaks komakohta, kuid kümnendkohaeraldaja puudub. Näiteks **2200** esindab 22 protsenti ja **1000** esindab 10 protsenti.
    - **VATExemptNature kehtib ainult juhul, kui KM-määr on 0 (null), kaasa arvatud juhul,** kui maksu pole. Praegu toetatakse VATExemptNature ainult kinkekaartide puhul ja vastendamise väärtus peab vastama XML-i konfiguratsioonifaili **atribuudi** **VATExemptNatureForGiftCard** väärtusele.
    - **ProductType** on toote tüüp. Väärtus **0 esindab** kaupu ja väärtus **1 esindab** teenuseid.
    - **DepartmentNumber on printeris konfigureeritud ja eelmisele** kolmele atribuudile vastava osakonna kood.

    Peate muutma näidisvastendust vastavalt KM-määradele, mis on konfigureeritud teie rakenduses ja vastavatele osakondadele, mis on konfigureeritud teie fiskaalprinteris.

- **Kinkekaardi km-vabastuse olemus – KÄIBEMAKSUvabastuse olemus, mida tuleks rakendada kinkekaardi** väljaregistreerimisel või uuestitäitmisel. Väärtus peab vastama fiskaalprinteri osakonna vastendamise kirjele. Vaikimisi vastendamine on **NS**.
- **Luba tasuta kaubad – kui see parameeter on sisse lülitatud, siis on lubatud** *100*-protsendise allahindlusega kaupade eriallahindluse tüüp.
- **Teabekood tagastuse päritolu kohta – teabekood, mida kasutatakse tagastuskande** päritolu hõivamiseks, kui algset müügikviitungit ei ole antud. Seda parameetrit kasutatakse koos algse müügikuupäeva teabekoodiga ja tagastuse päritolu vastendamisparameetriga, et luua fiskaalsissetuleku õige sõnum tagastatud kande päritolu kohta, kui algset müügikannet **pole** **olemas**. 

    See teabekood peab olema konfigureeritud nii, et kasutaja saab kauplustes valida või sisestada ühe võimaliku tagastuste päritolu. Näiteks saab seda konfigureerida alamkoodide loendina (nt Return from site või **Return** from **kiosk).** Seejärel **kasutatakse** tagastuse päritolu vastendamise parameetrit, et tõlkida teabekoodi väärtus fiskaalprinteri käsule.

    Teabekood, mis on valitud tagastuse päritolu teabekoodile, peab olema konfigureeritud kohustusliku teabekoodina, mis vallandatakse üks kord **müügikande** kohta. See tuleks kassa funktsiooniprofiilis määrata tagastustoote teabekoodina, nii et see käivitatakse tagastatud **toote** toimingu **käivitamisel**.

    Selle vastendamise jaoks pole vaikeväärtust määratud. Peate valima oma rakenduses konfigureeritud teabekoodi.

- **Algse müügikuupäeva teabekood – teabekood, mida kasutatakse algse müügikuupäeva hõivamiseks tagastuskande** puhul, kui algset müügi sissetulekut ei ole antud. Seda parameetrit kasutatakse koos tagastuse päritolu teabekoodi ja tagastuse päritolu vastendamise parameetritega, et luua fiskaalsissetulekis õige sõnum tagastatud kande päritolu kohta, kui algset müügikannet **pole** **olemas**.

    Teabekood peab olema konfigureeritud nii, et **sisendi tüübi** välja väärtuseks oleks **seatud** Kuupäev. See peab olema konfigureeritud kohustusliku teabekoodina, mis vallandatakse üks kord müügikande kohta. Samuti peaks see olema määratud lingitud teabekoodina teabekoodile, mis valitakse teabekoodile tagastuse päritolu parameetri jaoks, nii et need kaks **teabekoodi** **vallandatakse** ükshaaval.

    Selle vastendamise jaoks pole vaikeväärtust määratud. Peate valima oma rakenduses konfigureeritud teabekoodi.

- **Tagastuse päritolu vastendamine – tagastuse päritolu vastendamine, mida kasutatakse tagastuskande** päritolu printimiseks, kui algset müügikviitungit ei ole antud. Seda parameetrit kasutatakse koos tagastuse päritolu teabekoodi ja algsete müügikuupäeva parameetrite teabekoodiga, et luua **fiskaalsissetuleku õige teade tagastatud kande päritolu kohta, kui algset müügikannet pole** **olemas**. Järgmine näide näitab vaikevastendust.

    ```JSON
    {"ReturnOrigins": [
        {"ReturnOrigin":"1", "PrinterReturnOrigin":"POS"},
        {"ReturnOrigin":"2", "PrinterReturnOrigin":"ND"}
        ],
        "PrinterReturnOriginWithoutFiscalData":"POS"}
    ```

    Siin on atribuutide selgitus selles vastendamises:

    - **ReturnOrigin** on üks võimalik tagastuste päritolu kauplustes. Väärtus peab vastama tagastuse päritolu **parameetri teabekoodi** väärtusele.
    - **PrinterReturnOrigin on üks tagastuse päritoludest,** mida fiskaalprinter **aktsepteerib** **(POS,** TAGASTUS, **ND**).
    - **PrinterReturnOriginWithoutFiscalData on tagastuse päritolu, millega fiskaalprinter aktsepteerib ja mis vastab algsele müügikandele, mis ei ole lingitud fiskaalandmetega, sest seda ei registreeritud fiskaalprinteri** kaudu. Sellisel juhul tuvastatakse algne müügikuupäev algse müügikande kuupäevana.

Järgmised vaikimisi andmevastendused on aegunud ja neid säilitatakse ainult tagasiühilduvuse jaoks:

- Käibemaksukoodide vastendamine
- Deposiitmakse tüüp

#### <a name="fiscal-connector-settings"></a>Fiskaalühenduse sätted

Järgmised sätted on kaasatud fiskaalkonnektori konfiguratsiooni, mis on antud fiskaalintegratsiooni näidisosana:

- **Lõpp**-punkti aadress – printeri URL.
- **Kuupäeva ja kellaaja sünkroonimine – väärtus, mis määrab, kas printeri kuupäev ja kellaaeg tuleb** sünkroonida ühendatud riistvarajaamaga.

### <a name="configure-channel-components"></a>Kanali komponentide konfigureerimine

> [!WARNING]
> Uue sõltumatu pakendi- ja laiendusmudeli piirangute tõttu ei saa seda praegu selle [fiskaalintegratsiooni](../dev-itpro/build-pipeline.md) näidise jaoks kasutada. Retail SDK eelmist versiooni peate kasutama LCS-i arendaja VM-s. Lisateavet vt Itaalia [(pärand) fiskaalprinteri integratsiooni näidise juurutuse](emea-ita-fpi-sample-sdk.md) juhised.
>
> Uutesse versioonidesse planeeritakse fiskaalintegratsiooni valimite uue sõltumatu pakendi- ja laiendusmudeli tugi.

#### <a name="set-up-the-development-environment"></a>Saate häälestada arenduskeskkonda.

Arenduskeskkonna katsetada ja näidist laiendada, järgige neid samme.

1. Rakenduste hoidla [Dynamics 365 Commerce leidmine](https://github.com/microsoft/Dynamics365Commerce.Solutions) või allalaadimine. Valige õige väljalaske haruversioon vastavalt oma SDK-le/rakenduse versioonile. Lisateavet vt jaotisest Jaemüügi SDK näidised ja viitepakendid alla laadida [GitHub-st ja NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Avage rahandusprinteri integreerimislahendus **Dynamics365Commerce.Solutions \\ FiscalIntegration \\ EpsonFP90IIISample \\ EpsonFP90IIISample.sln** ja koostage see.
1. Installi CRT laiendid:

    1. Leidke laiendi CRT installer:

        - **Commerce Scale Unit:** **kaustas EpsonFP90IIISample \\\\ ScaleUnit ScaleUnit.EpsonFP90III.Installer \\ bin \\ Debug \\ net461** leidke **ScaleUnit.EpsonFP90III.Installer.**
        - **Modern CRT POS-i kohalik:** **kaustas EpsonFP90IIISample \\\\ ModernPOS.EpsonFP90III.Installer \\ bin \\ Debug \\ net461** leidke **ModernPOS.EpsonFP90III.Installer.**

    1. Käivitage CRT laiendiinstall käsurealt:

        - **Commerce Scalei üksus:**

            ```Console
            ScaleUnit.EpsonFP90III.Installer.exe install --verbosity 0
            ```

        - **Kohalik CRT Modern POS-s:**

            ```Console
            ModernPOS.EpsonFP90III.Installer.exe install --verbosity 0
            ```

1. Riistvarajaama laienduste installimine:

    1. **Kaustas EpsonFP90IIISample \\\\ HardwareStation HardwareStation.EpsonFP90III.Installer \\ bin \\ Debug \\ net461 leidke** **HardwareStation.EpsonFP90III.Installer.**
    1. Käivitage laiendiinstall käsurealt:

        ```Console
        HardwareStation.EpsonFP90III.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Tootmiskeskkond

Järgige fiskaalintegratsiooni näidise jaoks koostevõimaluste häälestamise etappe, et luua ja vabastada pilveskaala üksus ja iseteeninduse juurutatavad paketid [fiskaalintegratsiooni](fiscal-integration-sample-build-pipeline.md) näidiskomplekti jaoks. **EpsonFP90III build-pipeline.yml malli JAML faili saab leida** **lahenduste \\ hoidla YAML_Files**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions) müügivõimalustest.

## <a name="design-of-extensions"></a>Laienduste kujundus

Itaalia fiskaalprinteri integratsiooni näidis põhineb [fiskaalintegratsiooni funktsioonil ja](fiscal-integration-for-retail-channel.md) on osa Retail SDK-st. Näidis asub lahenduste hoidla **kaustas \\\\ FiscalIntegration EpsonFP90IIISample (näiteks näidis**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/)[väljalaskes/9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/EpsonFP90IIISample) Näidis [koosneb](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) fiskaaldokumendi pakkujast, mis on CRT laiendiks, ja fiskaalühendusest, mis on Commerce Hardware Stationi laiendus. Lisateavet Retail SDK kasutamise kohta vt [Retail SDK arhitektuurist](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [iseseisva pakendamise SDK koostamisvõimaluste häälestamisest](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Uue sõltumatu pakendi- ja laiendusmudeli piirangute tõttu ei saa seda praegu selle [fiskaalintegratsiooni](../dev-itpro/build-pipeline.md) näidise jaoks kasutada. Retail SDK eelmist versiooni peate kasutama LCS-i arendaja VM-s. Lisateavet vt Itaalia [(pärand) fiskaalprinteri integratsiooni näidise juurutuse](emea-ita-fpi-sample-sdk.md) juhised. Uutesse versioonidesse planeeritakse fiskaalintegratsiooni valimite uue sõltumatu pakendi- ja laiendusmudeli tugi.

### <a name="commerce-runtime-extension-design"></a>Äri käitusaja laiendi kujundus

Fiskaaldokumendi pakkujaks olemise laiend on luua printeripõhiseid dokumente ja käsitleda fiskaalprinteri vastuseid.

#### <a name="request-handler"></a>Nõudeohjur

**DocumentProviderEpsonFP90III taotluseohjur on fiskaalprinterist** dokumentide loomise nõude sisenemispunkt.

Ohjur pärineb **INamedRequestHandler** liideselt. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab vastama Commerce Headquartersis määratud konnektori dokumendi pakkuja nimele.

Konnektor toetab järgmisi taotlusi:

- **GetFiscalDocumentDocumentProviderRequest** – see taotlus sisaldab teavet selle kohta, milline dokument tuleks luua. See tagastab printeripõhise dokumendi, mis tuleb registreerida fiskaalprinteris.
- **GetSupportedRegistrableEventsDocumentProviderRequest – see taotlus tagastab** tellitavate sündmuste loendi. Praegu toetatakse järgmisi sündmusi: müük, X-aruande printimine ja Z-aruande printimine.

#### <a name="configuration"></a>Konfiguratsioon

Fiskaaldokumendi pakkuja konfiguratsioonifail asub **\\ src FiscalIntegration \\ EpsonFP90IIISample \\ CommerceRuntime \\ DocumentProvider.EpsonFP90IIISample \\ Configuration \\ DocumentProviderEpsonFP90IIISample.xml lahenduste**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidlas. Faili eesmärk on lubada dokumendipakkuja sätted rakendusest Commerce headquarters konfigureerimist. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele.

### <a name="hardware-station-extension-design"></a>Riistvarajaama laienduse kujundus

Fiskaalühenduseks olemise laiendi eesmärgiks on side fiskaalprinteriga. See laiend kasutab HTTP-protokolli, et esitada dokumente, CRT mida laiend fiskaalprinterile loob. Samuti käsitletakse fiskaalprinterilt saadud vastuseid.

#### <a name="request-handler"></a>Nõudeohjur

**EpsonFP90IIISample'i taotluseohjur on fiskaalseadme** käsitsemise nõude sisenemispunkt.

Ohjur pärineb **INamedRequestHandler** liideselt. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab ühtima Commerce Headquartersis määratud fiskaalühenduse nimega.

Konnektor toetab järgmisi taotlusi:

- **SubmitDocumentFiscalDeviceRequest – see taotlus saadab dokumendid printerisse ja** tagastab vastuse fiskaalprinterist.
- **IsReadyFiscalDeviceRequest** – seda taotlust kasutatakse seadme seisundikontrolliks.
- **InitializeFiscalDeviceRequest** – seda taotlust kasutatakse printeri lähtestamiseks.

#### <a name="configuration"></a>Konfiguratsioon

Fiskaalkonnektori konfiguratsioonifail asub **\\ src FiscalIntegration \\ EpsonFP90IIISample \\ HardwareStation \\ EpsonFP90IIIFiscalDeviceSample \\ Configuration \\ ConnectorEpsonFP90IIISample.xml lahenduste**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidlas. Faili eesmärk on lubada ühenduse sätete konfigureerimine rakendusest Commerce headquarters. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
