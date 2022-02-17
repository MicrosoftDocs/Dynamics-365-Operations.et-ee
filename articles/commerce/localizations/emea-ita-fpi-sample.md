---
title: Fiskaalprinteri integratsiooni näide Itaalia jaoks
description: Selles teemas antakse ülevaade Itaalia eelarveintegratsiooni proovist Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2018-11-1
ms.openlocfilehash: 02226fd9f2c92db2518ca48baefb680a3d2f0ac1
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076899"
---
# <a name="fiscal-printer-integration-sample-for-italy"></a>Fiskaalprinteri integratsiooni näide Itaalia jaoks

[!include[banner](../includes/banner.md)]

Selles teemas antakse ülevaade Itaalia eelarveintegratsiooni proovist Microsoft Dynamics 365 Commerce.

Itaalia kaubandusfunktsioon sisaldab müügikoha näidisintegratsiooni fiskaalprinteriga. Näidis laiendab fiskaalseintegratsiooni [funktsiooni](fiscal-integration-for-retail-channel.md) nii, et see töötab [Epsoni Epsoni Epson FP-90III seeria](https://www.epson.it/products/sd/pos-printer/epson-fp-90iii-series) printeritega ja võimaldab suhelda veebiserveri režiimis fiskaalprinteriga EpsonFPMate veebiteenuse kaudu, kasutades Fiscal ePOS-Print API-d. Valim toetab ainult registripidaja Telematico (RT) režiimi. Proov on esitatud lähtekoodi kujul ja see on osa jaemüügi tarkvaraarenduskomplektist (SDK).

Microsoft ei väljasta Epsonilt riist-, tarkvara ega dokumente. Lisateavet fiskaalprinteri hankimise ja käitamise kohta võtke ühendust [Epson Italia S.p.A.-ga](https://www.epson.it).

## <a name="scenarios"></a>Stsenaariumid

Itaalia fiskaalprinterite integratsioonivalim hõlmab järgmisi stsenaariume.

- Müügistsenaariumid:

    - Saate printida kassa- ja müügi- ja tagastustarne.
    - Jäädvustage fiskaalprinteri vastus ja salvestage see kanali andmebaasi.
    - Maksud:

        - Vastendage fiskaalprinteri maksukoodidega (osakondadega).
        - Saate vastendusega maksuandmed finantsprinterisse üle kanda.
        - Saate printida maksud finants sissetulekule.

    - Maksed:

        - Vastendage fiskaalprinteri makseviisidega.
        - Saate printida maksed finantskviitungile.
        - Saate printida muudatuste teabe.

    - Saate printida rea hinnaalandid.
    - Kinkekaardid:

        - Välista väljastatud/laetud kinkekaardi rida müügi finantskviitungilt.
        - Prindi makse, mis kasutab kinkekaarti tavalise makseviisina.

    - Saate printida klienditellimuse toimingute finantstarned.

        - Klienditellimuse deposiidi jaoks pole finantskviitungit prinditud.
        - Saate printida hübriidklienditellimuse tarneridade finantstarne.
        - Saate printida klienditellimuse pealevõtmistoimingu finantstšeki.
        - Saate printida tagastustellimuse finantstarne.

    - Saate printida finantskviitungil kviitungi numbri vöötkoodi.
    - [Saate printida finantskviitungile müügikande jaoks määratud klienditeabe](emea-ita-customer-information.md). Selle teabe näiteks on kliendi loteriikood. 

- Päevalõpuaruanded (X- ja eelarve Z-eelarvearuanded).
- Tõrkekäsitlus ( nt järgmised suvandid)

    - Kui fiskaalprinter pole ühendatud, pole valmis või ei reageeri, printer on paberist väljas või on paberimoosi.
    - Lükake finantsregistreerimine edasi.
    - Jätke finantsregistreerimine vahele või märkige kanne registreerituks ning lisage tõrke põhjuse ja lisateabe jäädvustamiseks infokoodid.
    - Kontrollige fiskaalprinteri saadavust enne uue müügikande avamist või müügikande lõpuleviimist.

### <a name="gift-cards"></a>Kinkekaardid

Fiskaalprinteri integratsiooni näidis rakendab järgmisi kinkekaartidega seotud reegleid.

- Välista finantskviitungilt müügiread, mis on seotud *kinkekaardiGa* Väljasta ja *Lisa kinkekaardi* toimingutesse.
- Ärge printige finantskviitungit, kui see koosneb ainult kinkekaardi ridadest.
- Lahutage finantskviitungi makseridadelt kandes väljastatud või laetud kinkekaartide kogusumma.
- Salvestage kanaliandmebaasi makseridade arvutatud korrigeerimised viitega vastavale finantskandele.
- Kinkekaardiga maksmist loetakse regulaarseks makseks.

### <a name="customer-deposits-and-customer-order-deposits"></a>Kliendihoiused ja klienditellimuse hoiused

Fiskaalprinteri integratsiooninäidis rakendab järgmisi reegleid, mis on seotud kliendihoiuste ja klienditellimuse hoiustega.

- Ärge printige finantskviitungit, kui kanne on kliendihoius.
- Ärge printige finantskviitungit, kui kanne sisaldab ainult klienditellimuse deposiiti või klienditellimuse deposiidi tagasimakset.
- Saate printida klienditellimuse pealevõtmistoimingu finantstarnele varem tasutud deposiidi summa.
- Hübriidkliendi tellimuse loomisel lahutage klienditellimuse deposiidi summa makseridadelt.
- Salvestage kanaliandmebaasi makseridade arvutatud korrigeerimised viitega hübriidklienditellimuse finantskandele.

### <a name="limitations-of-the-sample"></a>Proovi piirangud

- Fiskaalprinter toetab ainult stsenaariume, kus hinnas sisaldub käibemaks. Seetõttu **peab hinnas sisaldatav käibemaksusuvand** olema seatud **nii kaupluste kui ka klientide jaoks jah**.
- Igapäevased aruanded (fiskaalne X ja fiskaalne Z) prinditakse fiskaalprinteri püsivarasse manustatud vormingu abil.
- Fiskaalprinter ei toeta segakandeid. Suvand **Keela müügi ja tagastuste segamine ühes kviitungis** peaks olema seatud väärtusele **Jah** kassa funktsioonide profiilides.
- Näidis toetab integreerimist ainult fiskaalprinteriga, mis töötab registripidaja Telematico (RT)) režiimis.

## <a name="set-up-fiscal-integration-for-italy"></a>Itaalia fiskaalintegratsiooni häälestamine

Itaalia fiskaalprinterite integreerimise näidis põhineb fiskaalintegratsiooni [funktsioonil](fiscal-integration-for-retail-channel.md) ja on osa retail SDK-st. Proov asub lahenduste hoidla kaustas **src\\FiscalIntegration\\EpsonFP90IIISample** [Dynamics 365 Commerce (näiteks](https://github.com/microsoft/Dynamics365Commerce.Solutions/) proov  [väljalaskes/9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/EpsonFP90IIISample) [Näidis koosneb](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskaaldokumendi pakkujast, mis on Commerce'i käitusaja CRT () laiendus, ja fiskaalse konnektori, mis on Commerce'i riistvarajaama laiendus. Lisateavet jaemüügi SDK kasutamise kohta leiate teemast [Retail SDK arhitektuur](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [Sõltumatu pakendiga SDK](../dev-itpro/build-pipeline.md) ehitustorustiku seadistamine.

> [!WARNING]
> Uue sõltumatu pakendi- [ja laiendusmudeli](../dev-itpro/build-pipeline.md) piirangute tõttu ei saa seda praegu selle fiskaalse integratsiooni valimi jaoks kasutada. Peate kasutama Retail SDK eelmist versiooni arendaja virtuaalses masinas (VM) elutsükli teenustes Microsoft Dynamics (LCS). Lisateavet vt [teemast Juurutusjuhised fiskaalprinteri integratsiooni näidise jaoks Itaalias (pärand)](emea-ita-fpi-sample-sdk.md).
>
> Eelarveintegratsiooni näidiste uue sõltumatu pakendi- ja laiendusmudeli toetamine on kavandatud hilisematele versioonidele.

Täitke fiskaalintegratsiooni häälestusetapid, nagu on kirjeldatud jaotises [Commerce'i kanalite](setting-up-fiscal-integration-for-retail-channel.md) fiskaalintegratsiooni häälestamine.

1. [Saate häälestada finantsregistreerimise protsessi](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Samuti märkige ära finantsregistreerimise protsessi sätted, mis on selle fiskaalprinteri integratsioonivalimi jaoks [spetsiifilised](#set-up-the-registration-process).
1. [Saate seadistada allahindluste finantstekste](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).
1. [Saate määrata tõrkekäsitluse sätted](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Saate kassast häälestada X/Z-fiskaalaruandeid](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [Lubage edasilükatud finantsregistreerimise käsitsi käivitamine](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Saate seadistada klienditeabe haldamise funktsioonid kassas](emea-ita-customer-information.md#setup).
1. [Kanali komponentide](#configure-channel-components) konfigureerimine.

### <a name="set-up-the-registration-process"></a>Registreerimisprotsessi häälestamine

Registreerimisprotsessi lubamiseks järgige Commerce'i peakontori seadistamiseks neid juhiseid. Lisateavet vt teemast [Fiscal Integration for Commerce channels](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) häälestamine.

1. Laadige alla rahandusdokumendi pakkuja ja fiskaalse konnektori konfiguratsioonifailid.

    1. Avage lahenduste [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidla.
    1. Valige õige väljalaskeharu versioon vastavalt oma SDK/rakenduse versioonile (nt **[release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Avage **src \> FiscalIntegration \> EpsonFP90IIISample**.
    1. Laadige alla rahandusdokumendi pakkuja konfiguratsioonifail aadressil CommerceRuntime DocumentProvider.EpsonFP90IIISample Configuration DocumentProviderEpsonFP90IIISample.xml **(nt \> väljalaskefail/9.33 \>).\>**[...](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/EpsonFP90IIISample/CommerceRuntime/DocumentProvider.EpsonFP90IIISample/Configuration/DocumentProviderEpsonFP90IIISample.xml)
    1. Laadige alla fiskaalse konnektori konfiguratsioonifail aadressil HardwareStation EpsonFP90IIIFiscalDeviceSample **Configuration \> ConnectorEpsonFP90IIISample.xml \> (näiteks \> väljalaskefail/9.33**.[...](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/EpsonFP90IIISample/HardwareStation/EpsonFP90IIIFiscalDeviceSample/Configuration/ConnectorEpsonFP90IIISample.xml)

    > [!WARNING]
    > Uue sõltumatu pakendi- [ja laiendusmudeli](../dev-itpro/build-pipeline.md) piirangute tõttu ei saa seda praegu selle fiskaalse integratsiooni valimi jaoks kasutada. Peate kasutama Retail SDK eelmist versiooni arendaja VM-is LCS-is. Selle fiskaalse integratsiooni näidise konfiguratsioonifailid asuvad LCS-i arendaja VM-i jaemüügi SDK järgmistes kaustades.
    >
    > - **Fiskaaldokumendi pakkuja konfiguratsioonifail:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extension.DocumentProvider.EpsonFP90IIISample\\Configuration\\DocumentProviderEpsonFP90IIISample.xml
    > - **Fiscal connectori konfiguratsioonifail:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EpsonFP90IIIFiscalDeviceSample\\Configuration\\ConnectorEpsonFP90IIISample.xml
    > 
    > Eelarveintegratsiooni näidiste uue sõltumatu pakendi- ja laiendusmudeli toetamine on kavandatud hilisematele versioonidele.

1. Valige suvandid **Jaemüük ja kaubandus \> Headquartersi häälestus \> Parameetrid \> Commerce’i ühiskasutuses parameetrid**. peal **Kindral** vahekaardil määrake **Luba maksuintegratsioon** võimalus **Jah**.
1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Maksudokumentide pakkujad** ja laadige varem alla laaditud maksudokumendi pakkuja konfiguratsioonifail.
1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Fiskaalühendused** ja laadige varem alla laaditud fiskaalse konnektori konfiguratsioonifail.
1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Konnektori funktsionaalsed profiilid**. Looge uus konnektori funktsionaalne profiil. Valige dokumendipakkuja ja varem laaditud konnektor. Värskendage andmete vastendamise [sätteid](#default-data-mapping) vastavalt vajadusele.
1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Konnektori tehnilised profiilid**. Looge uus konnektori tehniline profiil ja valige varem laaditud fiskaalkonnektor. Värskendage [konnektori sätteid](#fiscal-connector-settings) vastavalt vajadusele.
6. **Avage jaemüügi- ja kaubanduskanali \> häälestus \> Fiskaalintegratsioon \> Fiskaalkonnektorigrupid**. Looge varem loodud konnektori funktsionaalse profiili jaoks uus fiskaalse konnektori rühm.
7. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Fiskaalsed registreerimise protsessid**. Looge uus maksuregistreerimisprotsess ja fiskaalse registreerimise protsessi etapp ning valige varem loodud maksuühenduse rühm.
8. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Funktsiooniprofiilid**. Valige funktsiooniprofiil, mis on lingitud poega, kus registreerimisprotsess tuleks aktiveerida. peal **Maksustamise registreerimise protsess** FastTab, valige varem loodud maksuregistreerimisprotsess.
9. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Riistvaraprofiilid**. Valige riistvaraprofiil, mis on lingitud riistvarajaamaga, millega fiskaalprinter ühendatakse. Valige kiirkaardil **Fiskaalsed välisseadmed** varem loodud konnektori tehniline profiil.
10. Avage jaotusgraafik (**jae- ja kaubandus \> - ja kaubandus-kaubanduse IT-jaotuse \> ajakava**) ning valige tööd **1070** ja **1090**, et edastada andmeid kanali andmebaasi.

#### <a name="default-data-mapping"></a>Andmete vaikevastendus

Rahandusdokumendi pakkuja konfiguratsioonis, mis on esitatud fiskaalse integratsiooni valimi osana, kaasatakse järgmine andmete vaikevastendus.

- **Maksevahendi tüübi vastendamine** – kaupluse jaoks konfigureeritud makseviiside vastendamine maksetüüpidega, mida fiskaalprinter toetab. Järgmises näites kuvatakse vaikevastendus.

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

    Siin on selgitus selle vastenduse atribuutide kohta:

    - **StorePaymentMethod** on makseviis, mis on kaupluse jaoks seadistatud jaotises **Retail and Commerce \> Channel setup \> Makseviisid \> Makseviisid**.
    - **PrinterPaymentType** ja **PrinterPaymentIndex** on vastav maksetüüp ja indeks, mis on määratletud Epsoni fiskaalprinteri dokumentatsioonis.
    - **DepositPaymentMethodi** kasutatakse printeri maksetüübi ja klienditellimuse pealevõtmissumma selle osa indeksi määramiseks, mis arveldatakse klienditellimuse deposiidiga.

    Järgmises tabelis on näidatud, kuidas makseviiside näidisvastastus vastab tavalistes demoandmetes konfigureeritud poe makseviisidele.

    | Makseviis | Makseviisi nimi |
    |----------------|---------------------|
    | 1              | Sularaha                |
    | 3              | Kaart                |
    | 4              | Kliendi konto    |
    | 6              | Valuuta            |
    | 8              | Kinkekaart           |

    Näidisvastendust tuleb muuta vastavalt rakenduses konfigureeritud makseviisile.

- **Kviitungi numbri vöötkoodi tüüp** – Vöötkoodi tüüp, mida kasutatakse maksukviitungil kviitungi numbri kuvamiseks. Vaikimisi vastendamine on **KOOD 128**.
- **Prindi eelarveandmed kviitungi päisesse** – Kui see parameeter on sisse lülitatud, prinditakse poe teave maksukviitungile. See teave sisaldab poe nime, aadressi ja maksukohustuslasena registreerimisnumbrit ning kassapidaja nime.
- **Fiskaalprinteri osakonna kaardistamine** – Fiskaalprinteri osakondade kaardistamine käibemaksumäärade, käibemaksuvabade olemuste ja tootetüüpidega. Järgmises näites kuvatakse vaikevastendus.

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

    Siin on selgitus selle vastenduse atribuutide kohta:

    - **VATRe** on toetatud käibemaksumäär, mis on konfigureeritud müügimaksukoodina. Vastenduse väärtusel on kaks kohta pärast koma, kuid kümnendkoha eraldajat pole. Näiteks, **2200** moodustab 22 protsenti ja **1000** moodustab 10 protsenti.
    - **VATExeptNature** on kohaldatav ainult juhtudel, kui käibemaksumäär on 0 (null), sh juhtudel, kui maksu ei ole. Praegu **VATExeptNature** on toetatud ainult kinkekaartide puhul ja vastenduses olev väärtus peaks vastama väärtusele **VATExemptNatureFor GiftCard** atribuut XML-konfiguratsioonifailis.
    - **Toote tüüp** on toote tüüp. Väärtus **0** esindab kaupu ja väärtust **1** esindab teenuseid.
    - **Osakonnanumber** on osakonna number, mis on printeris konfigureeritud ja mis vastab kolmele eelmisele atribuudile.

    Peate muutma näidisvastastust vastavalt teie rakenduses konfigureeritud käibemaksumääradele ja vastavatele osakondadele, mis on konfigureeritud teie fiskaalprinteris.

- **Kinkekaardi puhul käibemaksuvaba loodus** – Käibemaksuvaba olemus, mida tuleks kohaldada kinkekaardi väljastamisel või uuesti täitmisel. Väärtus peaks vastama mõnele kirjele fiskaalprinteri osakonna kaardistuses. Vaikimisi vastendamine on **NS**.
- **Lubage tasuta üksused** – Kui see parameeter on sisse lülitatud, kuvatakse spetsiaalne *omaggio* allahindluse korrigeerimise tüüp kaupade jaoks, millel on 100-protsendiline allahindlus, on lubatud.
- **Tagastamise päritolu infokood** – teabekood, mida kasutatakse tagastustehingu päritolu jäädvustamiseks, kui algset müügikviitungit ei esitata. Seda parameetrit kasutatakse koos **Algse müügikuupäeva infokood** ja **Tagastamise päritolu kaardistamine** parameetrid, et luua maksukviitungil õige teade tagastustehingu päritolu kohta, kui algset müügitehingut pole. 

    See teabekood peaks olema konfigureeritud nii, et kasutaja saaks valida või sisestada teie kauplustes ühe võimaliku tagastamise lähtekoha. Näiteks saab selle konfigureerida alamkoodide loendina (nt **Tagasi saidilt** või **Kioskist tagasitulek**). The **Tagastamise päritolu kaardistamine** parameetrit kasutatakse seejärel teabekoodi väärtuse tõlkimiseks fiskaalprinteri käsuks.

    Teabekood, mille jaoks on valitud **Tagastamise päritolu infokood** tuleks konfigureerida kohustusliku teabekoodina, mis käivitatakse üks kord müügitehingu kohta. See tuleks määrata kui **Toote tagastamine** teabekood POS-funktsiooni profiilis, et see käivitataks, kui **Toote tagastamine** operatsioon käivitatakse.

    Selle vastenduse jaoks pole vaikeväärtust määratud. Peate valima teabekoodi, mis on teie rakenduses konfigureeritud.

- **Algse müügikuupäeva infokood** – Teabekood, mida kasutatakse tagastustehingu algse müügikuupäeva jäädvustamiseks, kui algset müügikviitungit ei esitata. Seda parameetrit kasutatakse koos **Tagastamise päritolu infokood** ja **Tagastamise päritolu kaardistamine** parameetrid, et luua maksukviitungil õige teade tagastustehingu päritolu kohta, kui algset müügitehingut pole.

    Infokood tuleks konfigureerida nii, et **Sisestuse tüüp** väli on seatud **Kuupäev**. See peaks olema konfigureeritud kohustusliku teabekoodina, mis käivitatakse üks kord müügitehingu kohta. See tuleks määrata ka kui **Lingitud teabekood** jaoks valitud teabekoodi jaoks **Tagastamise päritolu infokood** parameetrit, nii et kaks teabekoodi käivitatakse üksteise järel.

    Selle vastenduse jaoks pole vaikeväärtust määratud. Peate valima teabekoodi, mis on teie rakenduses konfigureeritud.

- **Tagastamise päritolu kaardistamine** – Tagastamise päritolu kaardistamine, mida kasutatakse tagastustehingu päritolu printimiseks, kui originaalmüügikviitungit ei esitata. Seda parameetrit kasutatakse koos **Tagastamise päritolu infokood** ja **Algse müügikuupäeva infokood** parameetrid, et luua maksukviitungil õige teade tagastustehingu päritolu kohta, kui algset müügitehingut pole. Järgmises näites kuvatakse vaikevastendus.

    ```JSON
    {"ReturnOrigins": [
        {"ReturnOrigin":"1", "PrinterReturnOrigin":"POS"},
        {"ReturnOrigin":"2", "PrinterReturnOrigin":"ND"}
        ],
        "PrinterReturnOriginWithoutFiscalData":"POS"}
    ```

    Siin on selgitus selle vastenduse atribuutide kohta:

    - **ReturnOrigin** on teie kauplustes üks võimalikest tagastamisallikatest. Väärtus peaks vastama väärtusele **Tagastamise päritolu infokood** parameeter.
    - **PrinterReturnOrigin** on üks tagastusallikatest, mille fiskaalprinter aktsepteerib (**POS**, **·**, või **ND**).
    - **PrinterReturnOriginWithoutFiscalData** on tagastamise lähtekoht, mille maksuprinter aktsepteerib ja mis vastab tagastustehingule, mis on lingitud algse müügitehinguga, millel pole lingitud fiskaalandmeid, kuna seda ei registreeritud fiskaalprinteri kaudu. Sel juhul tuvastatakse algne müügikuupäev algse müügitehingu kuupäevana.

Järgmised vaikeandmete vastendused on vananenud ja neid säilitatakse ainult tagasiühilduvuse huvides:

- Käibemaksu (KM) koodide kaardistamine
- Deposiitmakse tüüp

#### <a name="fiscal-connector-settings"></a>Fiskaalse konnektori sätted

Fiskaalse konnektori konfiguratsiooni kuuluvad järgmised sätted, mis on esitatud fiskaalse integratsiooni valimi osana.

- **Lõpp-punkti aadress** – printeri URL.
- **Kuupäeva ja kellaaja sünkroonimine** – Väärtus, mis määrab, kas printeri kuupäev ja kellaaeg tuleb ühendatud riistvarajaamaga sünkroonida.

### <a name="configure-channel-components"></a>Kanali komponentide seadistamine

> [!WARNING]
> Uue sõltumatu pakendi- [ja laiendusmudeli](../dev-itpro/build-pipeline.md) piirangute tõttu ei saa seda praegu selle fiskaalse integratsiooni valimi jaoks kasutada. Peate kasutama Retail SDK eelmist versiooni arendaja VM-is LCS-is. Lisateavet vt [teemast Juurutusjuhised fiskaalprinteri integratsiooni näidise jaoks Itaalias (pärand)](emea-ita-fpi-sample-sdk.md).
>
> Eelarveintegratsiooni näidiste uue sõltumatu pakendi- ja laiendusmudeli toetamine on kavandatud hilisematele versioonidele.

#### <a name="set-up-the-development-environment"></a>Seadistage arenduskeskkond

Näidise testimiseks ja laiendamiseks arenduskeskkonna seadistamiseks toimige järgmiselt.

1. Kloonige või laadige alla [Dynamics 365 Commerce Lahendused](https://github.com/microsoft/Dynamics365Commerce.Solutions) hoidla. Valige õige väljalaske haru versioon vastavalt oma SDK/rakenduse versioonile. Lisateabe saamiseks vt [Laadige alla jaemüügi SDK näidised ja viitepaketid GitHubist ja NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Avage fiskaalprinteri integreerimislahendus aadressil **Dynamics365Commerce.Solutions\\ Fiskaalintegratsioon\\ EpsonFP90III Näidis\\ EpsonFP90IIISample.sln** ja ehitage see üles.
1. Installige CRT laiendused:

    1. Otsige üles CRT laienduse paigaldaja:

        - **Kaubanduse mastaabiüksus:** Aastal **EpsonFP90III Näidis\\ Skaalaühik\\ ScaleUnit.EpsonFP90III.Installer\\ prügikast\\ Silumine\\ net461** kaust, otsige üles **ScaleUnit.EpsonFP90III.Installer** paigaldaja.
        - **Kohalik CRT kaasaegses POS-is:** Aastal **EpsonFP90III Näidis\\ Kaasaegne POS\\ Kaasaegne POS.EpsonFP90III. Installer\\ prügikast\\ Silumine\\ net461** kaust, otsige üles **Kaasaegne POS.EpsonFP90III. Installer** paigaldaja.

    1. Alustage CRT laienduse installija käsurealt:

        - **Kaubanduse mastaabiüksus:**

            ```Console
            ScaleUnit.EpsonFP90III.Installer.exe install --verbosity 0
            ```

        - **Kohalik CRT kaasaegses POS-is:**

            ```Console
            ModernPOS.EpsonFP90III.Installer.exe install --verbosity 0
            ```

1. Installige riistvarajaama laiendused:

    1. Aastal **EpsonFP90III Näidis\\ Riistvarajaam\\ HardwareStation.EpsonFP90III. Installer\\ prügikast\\ Silumine\\ net461** kaust, otsige üles **HardwareStation.EpsonFP90III. Installer** paigaldaja.
    1. Käivitage laienduse installija käsurealt:

        ```Console
        HardwareStation.EpsonFP90III.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Tootmiskeskkond

Järgige juhiseid [Seadistage fiskaalintegratsiooni näidise jaoks ehituskonveier](fiscal-integration-sample-build-pipeline.md) luua ja vabastada Cloud Scale Unit ja iseteenindusega juurutatavad paketid fiskaalintegratsiooni näidise jaoks. The **EpsonFP90III build-pipeline.yml** malli YAML-faili leiate **Torujuhe\\ YAML_Files** kaust [Dynamics 365 Commerce Lahendused](https://github.com/microsoft/Dynamics365Commerce.Solutions) hoidla.

## <a name="design-of-extensions"></a>Laienduste kujundus

Itaalia fiskaalprinterite integreerimise näidis põhineb fiskaalintegratsiooni [funktsioonil](fiscal-integration-for-retail-channel.md) ja on osa retail SDK-st. Proov asub lahenduste hoidla kaustas **src\\FiscalIntegration\\EpsonFP90IIISample** [Dynamics 365 Commerce (näiteks](https://github.com/microsoft/Dynamics365Commerce.Solutions/) proov väljalaskes/9.33 [).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/EpsonFP90IIISample) Näidis [koosneb](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskaaldokumentide pakkuja, mis on laiendus CRT ja fiskaalne pistik, mis on Commerce Hardware Stationi laiendus. Lisateavet jaemüügi SDK kasutamise kohta leiate teemast [Retail SDK arhitektuur](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [Sõltumatu pakendiga SDK](../dev-itpro/build-pipeline.md) ehitustorustiku seadistamine.

> [!WARNING]
> Uue sõltumatu pakendi- [ja laiendusmudeli](../dev-itpro/build-pipeline.md) piirangute tõttu ei saa seda praegu selle fiskaalse integratsiooni valimi jaoks kasutada. Peate kasutama Retail SDK eelmist versiooni arendaja VM-is LCS-is. Lisateavet vt [teemast Juurutusjuhised fiskaalprinteri integratsiooni näidise jaoks Itaalias (pärand)](emea-ita-fpi-sample-sdk.md). Eelarveintegratsiooni näidiste uue sõltumatu pakendi- ja laiendusmudeli toetamine on kavandatud hilisematele versioonidele.

### <a name="commerce-runtime-extension-design"></a>Commerce'i käitusaja laienduse kujundus

Maksudokumentide pakkuja laienduse eesmärk on luua printeripõhiseid dokumente ja käsitleda fiskaalprinteri vastuseid.

#### <a name="request-handler"></a>Taotluse käitleja

**Päringukäsitleja DocumentProviderEpsonFP90IIII** on finantsprinterist dokumentide loomise taotluse sisenemispunkt.

Käitleja on päritud **INamedRequestHandler** liides. **Käitleja nime tagastamise eest vastutab meetod HandlerName**. Käitleja nimi peaks vastama Commerce'i peakontoris määratud konnektori dokumendipakkuja nimele.

Konnektor toetab järgmisi taotlusi.

- **GetFiscalDocumentDocumentProviderRequest** – see taotlus sisaldab teavet selle kohta, milline dokument tuleks luua. See tagastab printerispetsiifilise dokumendi, mis tuleks fiskaalprinteris registreerida.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – See päring tagastab tellitavate sündmuste loendi. Praegu toetatakse järgmisi sündmusi: müük, X-aruande printimine ja Z-aruande printimine.

#### <a name="configuration"></a>Konfiguratsioon

Maksudokumendi pakkuja konfiguratsioonifail asub aadressil **src\\ Fiskaalintegratsioon\\ EpsonFP90III Näidis\\ CommerceRuntime\\ DocumentProvider.EpsonFP90IIISample\\ Seadistamine\\ DocumentProviderEpsonFP90IIISample.xml** aastal [Dynamics 365 Commerce Lahendused](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidla. Faili eesmärk on lubada dokumendipakkuja sätete konfigureerimine Commerce'i peakontorist. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetega.

### <a name="hardware-station-extension-design"></a>Riistvarajaama laienduse disain

Fiskaalpistikuks oleva laienduse eesmärk on suhelda fiskaalprinteriga. See laiendus kasutab HTTP-protokolli, et esitada dokumente, mille CRT laiendus fiskaalprinterile genereerib. Samuti tegeleb see fiskaalprinterilt saadud vastustega.

#### <a name="request-handler"></a>Taotluse käitleja

The **EpsonFP90III Näidis** päringu töötleja on maksuvälisseadme päringu käsitlemise sisenemispunkt.

Käitleja on päritud **INamedRequestHandler** liides. **Käitleja nime tagastamise eest vastutab meetod HandlerName**. Töötleja nimi peaks ühtima fiskaalse konnektori nimega, mis on määratud Commerce'i peakorteris.

Konnektor toetab järgmisi taotlusi.

- **SubmitDocumentFiscalDeviceRequest** – See päring saadab dokumendid printeritele ja tagastab fiskaalprinterilt vastuse.
- **IsReadyFiscalDeviceRequest** – Seda päringut kasutatakse seadme tervisekontrolliks.
- **InitializeFiscalDeviceRequest** – Seda päringut kasutatakse printeri lähtestamiseks.

#### <a name="configuration"></a>Konfiguratsioon

Fiskaalse konnektori konfiguratsioonifail asub aadressil **src\\ Fiskaalintegratsioon\\ EpsonFP90III Näidis\\ Riistvarajaam\\ EpsonFP90IIIFiscalDeviceSample\\ Seadistamine\\ ConnectorEpsonFP90IIISample.xml** aastal [Dynamics 365 Commerce Lahendused](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidla. Faili eesmärk on lubada konnektori sätete konfigureerimine Commerce'i peakontorist. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetega.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
