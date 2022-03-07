---
title: Fiskaalüksuse registreerimisteenuse integratsiooni näide Austria jaoks
description: See teema annab ülevaate Austria eelarveintegratsiooni näidisest Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: d720bffb98965bdc0276660d2a2e50d2bf155e74
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077161"
---
# <a name="fiscal-registration-service-integration-sample-for-austria"></a>Fiskaalüksuse registreerimisteenuse integratsiooni näide Austria jaoks

[!include[banner](../includes/banner.md)]

See teema annab ülevaate Austria eelarveintegratsiooni näidisest Microsoft Dynamics 365 Commerce.

Austria Dynamics 365 Retail kassaaparaatide kohalike maksunõuete täitmiseks hõlmab Austria funktsionaalsus müügikoha näidisi integreerimist välise maksuregistreerimisteenusega. Valim laiendab fiskaalintegratsiooni [funktsiooni](fiscal-integration-for-retail-channel.md). See põhineb EFSTA [EFR (Electronic Fiscal Register)](https://www.efsta.eu/at/fiskalloesungen/oesterreich) lahendusel [ja](https://www.efsta.eu/at/) võimaldab EFR-teenusega suhelda HTTPS-protokolli kaudu. EFR-teenust tuleks majutada kas jaemüügi riistvarajaamas või eraldi masinas, millega saab riistvarajaamast ühendada. Proov on esitatud lähtekoodi kujul ja see on osa jaemüügi tarkvaraarenduskomplektist (SDK).

Microsoft ei väljasta EFSTA-st riist-, tarkvara ega dokumente. EFR-lahenduse saamiseks ja selle käitamiseks võtke ühendust EFSTA-ga [...](https://www.efsta.eu/at/kontakt).

## <a name="scenarios"></a>Stsenaariumid

Austria maksuregistreerimisteenuse integratsioonivalim hõlmab järgmisi stsenaariume:

- Sularahakannete registreerimine maksuregistreerimisteenuses:

    - Saatke üksikasjalikud kandeandmed finantsregistreerimisteenusele. Need andmed sisaldavad müügirea teavet ning teavet allahindluste, maksete ja maksude kohta.
    - Jäädvustage vastus fiskaalregistreerimisteenusest. See vastus sisaldab digitaalallkirja ja linki registreeritud tehingule.
    - Registreerige maksud ja vastendage need maksuregistreerimisteenuse maksukoodidega.
    - Prindi kviitungile registreeritud kande QR-kood.

- Kinkekaardi toimingute ja kliendihoiuste registreerimine mitterahaliste tehingutena maksuregistreerimisteenuses:

    - Väljastage või lisage kinkekaardile raha.
    - Registreerige kliendikonto deposiit.
    - Registreerige klienditellimuse deposiit.

- Mittemüügitehingute ja sündmuste registreerimine mitterahaliste tehingutena maksuregistreerimisteenuses:

    - Avatud vahetus ja Vahetus
    - Stardisumma, Ujukkanne ja Maksevahendi eemaldamine
    - Hinnaerand
    - Maksu tühistamine
    - Kviitungi prinditud koopia
    - Ava sahtel
    - Prindi X-aruanne
    - Prindi Z-aruanne

- Päevalõpuväljavõtete (X/Z-aruannete) printimine, millel on Austria-spetsiifilised väljad:

    - Klientidele tarnitud toodete või teenuste koguarv
    - Müügi jaotus maksumäära järgi
    - Väljamaksete jaotus kassapidaja/kassapidaja poolt
    - Hinnasoodustused ja tagastused, mis vähendavad igapäevast müüki
    - Nullmüük (kingitused)

- Tõrkekäsitlus ( nt järgmised suvandid)

    - Kui eelarveregistreerimine on võimalik uuesti proovida nt kui fiskaalregistreerimisteenus pole saadaval, pole valmis või ei vasta.
    - Lükake finantsregistreerimine edasi.
    - Jätke finantsregistreerimine vahele või märkige kanne registreerituks ning lisage tõrke põhjuse ja lisateabe jäädvustamiseks infokoodid.
    - Kontrollige finantsregistreerimisteenuse kättesaadavust enne uue müügikande avamist või müügikande lõpuleviimist.

### <a name="gift-cards"></a>Kinkekaardid

Maksuregistreerimisteenuse integreerimise näidis rakendab järgmisi kinkekaartidega seotud reegleid.

- Välistage müügiread, mis on seotud *kinkekaardiGa* Väljastamine ja *Kinkekaardi* toimingutele lisamine sularahakandest. Selle asemel, et registreerida need read sularahatehingu osana, registreerige need eraldi mitterahalise tehinguna maksuregistreerimisteenuses.
- Ärge printige maksugrupi jaotust ja QR-koodi kviitungile, kui kviitung koosneb ainult kinkekaardi ridadest.
- Saate printida kandes väljastatud või uuesti tasutud kinkekaartide kogusumma eraldi kviitungil olevast sularahakande summast.
- Salvestage kanaliandmebaasi makseridade arvutatud korrigeerimised viitega vastavale finantskandele.
- Kinkekaardiga maksmist loetakse regulaarseks makseks.

### <a name="customer-deposits-and-customer-order-deposits"></a>Kliendihoiused ja klienditellimuse hoiused

Finantsregistreerimisteenuse integreerimise näidis rakendab järgmisi kliendihoiuste ja klienditellimuse hoiustega seotud reegleid.

- Registreeri mitterahaline kanne, kui kanne on kliendihoius.
- Registreeri mitterahaline kanne, kui kanne sisaldab ainult kliendi tellimuse tagatisraha või klienditellimuse deposiidi tagasimakset.
- Hübriidkliendi tellimuse loomisel lahutage klienditellimuse deposiidi summa makseridadelt.
- Salvestage kanaliandmebaasi makseridade arvutatud korrigeerimised viitega hübriidklienditellimuse finantskandele.

### <a name="limitations-of-the-sample"></a>Proovi piirangud

Maksuregistreerimisteenus toetab ainult stsenaariume, kus hinnas sisaldub käibemaks. Seetõttu **peab hinnas sisaldatav käibemaksusuvand** olema seatud **nii kaupluste kui ka klientide jaoks jah**.

## <a name="set-up-commerce-for-austria"></a>Austria kaubanduse häälestamine

Selles jaotises kirjeldatakse Austriale omast ja soovitatavat kaubandussätteid. Lisateavet häälestusteabe kohta leiate teemast [Commerce'i avaleht](../index.md).

Austria-põhiste funktsioonide kasutamiseks peate määrama järgmised sätted.

- Määrake **juriidilise isiku esmasel aadressil väli Riik/regioon** AUT **·** (Austria).
- Seadke **iga Austrias asuva kaupluse kassafunktsioonide profiilis ISO-koodi** väli **AT** (Austria).

Samuti peate määrama Austria jaoks järgmised sätted. Pange tähele, et pärast seadistuse lõpuleviimist peate käivitama asjakohased jaotustööd.

### <a name="set-up-vat-per-austrian-requirements"></a>Km häälestamine Austria nõuete kohta

Peate looma käibemaksukoodid, käibemaksugrupid ja kauba käibemaksugrupid. Samuti peate seadistama toodete ja teenuste käibemaksuteabe. Lisateavet käibemaksufunktsioonide seadistamise ja kasutamise kohta leiate teemast [Käibemaksu ülevaade](../../finance/general-ledger/indirect-taxes-overview.md).

Müügikviitungitel saate printida käibemaksukoodi lühendatud koodi (näiteks "A" või "B"). Selle funktsiooni kättesaadavaks tegemiseks seadke **välja** Prindi tähis **lehel Käibemaksukoodid**.

### <a name="set-up-stores"></a>Kaupluste häälestamine

Värskendage **lehel Kõik kauplused** poe üksikasju. Täpsemalt määrake järgmised parameetrid.

- Määrake väljal **Käibemaksugrupp** käibemaksugrupp, mida tuleks kasutada vaikekliendile müügiks.
- Määrake **suvandi Hinnad sisaldavad käibemaksu** valikuks **Jah**.
- Määrake **väli Nimi** ettevõtte nimeks. See muudatus aitab tagada, et ettevõtte nimi kuvatakse müügikviitungil. Teise võimalusena saate ettevõtte nime lisada müügikviitungi paigutusele vabas vormis tekstina.
- **Määrake välja Maksu ID-number (TIN)** ettevõtte ID-numbriks. See muudatus aitab tagada, et ettevõtte ID-number kuvatakse müügikviitungil. Teise võimalusena saate ettevõtte ID-numbri lisada müügikviitungi paigutusele vabas vormis tekstina.

### <a name="set-up-functionality-profiles"></a>Funktsiooniprofiilide häälestamine

Kassafunktsioonide profiilide häälestamine.

- Seadistage **kiirkaardil Tarne nummerdamine** kviitungi nummerdamine, luues või värskendades kirjeid müügi **-,** müügitellimuse **- ja** tagastustarne **kandetüüpide jaoks**.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Kohandatud väljade konfigureerimine nii, et neid saaks kasutada müügi sissetulekute vormingutes

Saate konfigureerida keeleteksti ja kohandatud väljad, mida kasutatakse kassa kviitungi vormingutes. Kviitungi häälestuse loonud kasutaja vaikeettevõte peaks olema sama juriidiline isik, kus keeleteksti häälestus luuakse. Teise võimalusena tuleks luua samad keeletekstid nii kasutaja vaikeettevõttes kui ka selle poe juriidilises isikus, kellele häälestus on loodud.

**Lisage lehel Keeletekst** kviitungipaigutuste kohandatud väljade siltide jaoks järgmised kirjed. Pange tähele, et **tabelis kuvatavad keele ID**, **teksti ID** ja **tekstiväärtused** on vaid näited. Saate neid muuta, et need vastaksid teie vajadustele. Kasutatavad teksti ID **väärtused peavad siiski** olema kordumatud ja need peavad olema võrdsed või suuremad kui 900001.

Lisage järgmised POS-sildid **POS** osa **Keeletekst** tabelist:

| Keele ID | Teksti ID | Tekst                      |
|-------------|---------|---------------------------|
| EN-US       | 900001  | QR-kood                   |
| EN-US       | 900002  | Pidev arv         |
| EN-US       | 900003  | Maksu jaemüügi prindikood     |
| EN-US       | 900004  | Kokku (müük)             |
| EN-US       | 900005  | Maks kokku (müük)         |
| EN-US       | 900006  | Kokku kaasa maksud (müük) |
| EN-US       | 900007  | Maksusumma (müük)        |
| EN-US       | 900008  | Maksu alus (müük)         |

**Lisage lehel Kohandatud väljad** kviitungipaigutuste kohandatud väljadele järgmised kirjed. Pange tähele, et **Tiitrite teksti ID** väärtused peavad vastama **Teksti ID** väärtused, mille määrasite **Keeletekst** leht:

| Nimi                 | Tüüp    | Pealdise teksti ID |
|----------------------|---------|-----------------|
| QRCODE               | Sissetulek | 900001          |
| PIDEV NUMBER     | Sissetulek | 900002          |
| RETAILPRINTCODE      | Sissetulek | 900003          |
| SALESTOTAL           | Sissetulek | 900004          |
| SALESTOTALTAX        | Sissetulek | 900005          |
| SALESTOTALINCLUDETAX | Sissetulek | 900006          |
| SALESTAXAMOUNT       | Sissetulek | 900007          |
| SALESTAXBASIS        | Sissetulek | 900008          |

> [!NOTE]
> On oluline määrata õiged kohandatud väljanimed, nagu on loetletud eelmises tabelis. Vale kohandatud välja nimi põhjustab kviitungitel puuduvaid andmeid.

### <a name="configure-receipt-formats"></a>Sissetulekuvormingute konfigureerimine

Iga nõutava kviitungivormingu puhul muutke väärtust **Prindi käitumine** väljale **Printige alati**.

Lisage kviitungivormingu kujundaja vastavatele kviitungi jaotistele järgmised kohandatud väljad. Pange tähele, et väljanimed vastavad eelmises jaotises määratletud keeletekstidele.

- **Päis:** Lisage järgmised väljad.

    - **Kaupluse nime** ja **maksuidentifikaatori** väljad, mida kasutatakse ettevõtte nime ja identifitseerimisnumbri printimiseks sissetulekutele. Teise võimalusena saate küljendusele lisada vabas vormis tekstina ettevõtte nime ja isikukoodi.
    - **Kaupluse aadress**, **kuupäev**, **kellaaeg 24H**, **Kviitungi number** ja **Registri numbri** väljad.
    - **Väljad Pidev arv**, et tuvastada finantsregistreerimisteenuse sularahakande number.

- **read:** Lisage järgmised väljad:

    - **Kauba nimi**.
    - **Kogus**.
    - **Koguhind koos maksuga**.
    - **Maksu jaemüügi prindikood**, mida kasutatakse kaubale rakenduvale käibemaksukoodile vastava lühendatud tähise printimiseks.

- **Jalus:** Lisage järgmised väljad:

    - Makseväljad, et prinditaks iga makseviisi maksesummad. Näiteks lisage **Pakkumise nimi** ja **Pakkumise summa** väljad paigutuse ühele reale.
    - **Müügi kogu** väljagrupp:

        - **Välja Kogusumma (müük),** mida kasutatakse kviitungi sularaha müügi kogusumma printimiseks. Summa ei sisalda makse. Ettemaksed ja kinkekaarditoimingud on välistatud.
        - **Väli Kaasa maks (müük),** mida kasutatakse sissetuleku kogu sularaha müügisumma printimiseks. Summa sisaldab makse. Ettemaksed ja kinkekaarditoimingud on välistatud.
        - **Välja Maks (müük)** kogusumma, mida kasutatakse kassa maksu kogusumma printimiseks sularaha müügiks. Ettemaksed ja kinkekaarditoimingud on välistatud.

    - **Maksuvähenduse** väljagrupp. Kõik selle väljarühma väljad tuleb trükkida ühele eraldi reale.

        - **Maksu ID** väli, mis on standardväli, mis võimaldab printida iga käibemaksukoodi kohta käibemaksu kokkuvõtte. Välja tuleb lisada uuele reale.
        - **Maksuprotsent** väli, mis on standardväli, mida kasutatakse müügimaksu koodi tegeliku maksumäära printimiseks.
        - **Maksubaas (müük)** välja, mida kasutatakse müügimaksu koodi jaoks kviitungi sularaha müügi kogusumma printimiseks. Ettemaksed ja kinkekaarditoimingud on välistatud.
        - **Maksusumma (müük)** väli, mida kasutatakse käibemaksukoodi sularahamüügi kviitungi maksusumma printimiseks.
        - **Maksu jaemüügi prindikood** välja, mida kasutatakse käibemaksukoodile vastava lühendatud koodi printimiseks.

    - **QR-koodi** väli, mida kasutatakse registreeritud sularahatehingule viite printimiseks QR-koodi kujul.

        > [!NOTE]
        > The **QR kood** väärtus saadakse fiskaalregistri vastusest. EFR tagastab vastuses QR-koodi ainult siis, kui väärtus on **Atribuudid** välja EFR konfiguratsioonis on kirjeldatud EFSTA dokumentatsioonis. QR-koodi vorming rakenduses **Atribuudid** EFR konfiguratsiooni väli peab olema seatud väärtusele **BMP**.

Kviitungivormingutega töötamise kohta lisateabe saamiseks vt [Kviitungivormingute seadistamine ja kujundamine](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-austria"></a>Austria fiskaalintegratsiooni häälestamine

Austria fiskaalregistreerimisteenuse integreerimise näidis põhineb fiskaalintegratsiooni [funktsioonil](fiscal-integration-for-retail-channel.md) ja on osa retail SDK-st. Näidis asub aadressil **src\\ Fiskaalintegratsioon\\ Efr** kaust [Dynamics 365 Commerce Lahendused](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidla (näiteks [väljalaskes olev näidis/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). [Näidis koosneb](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskaaldokumendi pakkujast, mis on Commerce'i käitusaja CRT () laiendus, ja fiskaalse konnektori, mis on Commerce'i riistvarajaama laiendus. Lisateavet jaemüügi SDK kasutamise kohta leiate teemast [Retail SDK arhitektuur](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [Sõltumatu pakendiga SDK](../dev-itpro/build-pipeline.md) ehitustorustiku seadistamine.

> [!WARNING]
> Uue sõltumatu pakendi- [ja laiendusmudeli](../dev-itpro/build-pipeline.md) piirangute tõttu ei saa seda praegu selle fiskaalse integratsiooni valimi jaoks kasutada. Peate kasutama Retail SDK eelmist versiooni arendaja virtuaalses masinas (VM) elutsükli teenustes Microsoft Dynamics (LCS). Lisateavet vt [teemast Deployment guidelines for fiscal integration sample for Austria (legacy)](emea-aut-fi-sample-sdk.md). Eelarveintegratsiooni näidiste uue sõltumatu pakendi- ja laiendusmudeli toetamine on kavandatud hilisematele versioonidele.

Viige fiskaalintegratsiooni seadistamise etapid lõpule, nagu on kirjeldatud jaotises [Seadistage kaubanduskanalite fiskaalintegratsioon](setting-up-fiscal-integration-for-retail-channel.md):

1. [Saate häälestada finantsregistreerimise protsessi](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Märkige üles ka fiskaalse registreerimise protsessi sätted [selle maksuregistriteenuse integratsiooninäidise spetsiifiline](#set-up-the-registration-process).
1. [Saate määrata tõrkekäsitluse sätted](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Lubage edasilükatud finantsregistreerimise käsitsi käivitamine](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Kanali komponentide](#configure-channel-components) konfigureerimine.

### <a name="set-up-the-registration-process"></a>Registreerimisprotsessi häälestamine

Registreerimisprotsessi lubamiseks järgige Commerce'i peakontori seadistamiseks neid juhiseid. Lisateavet vt teemast [Fiscal Integration for Commerce channels](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) häälestamine.

1. Laadige alla rahandusdokumendi pakkuja ja fiskaalse konnektori konfiguratsioonifailid.

    1. Avage lahenduste [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidla.
    1. Valige õige väljalaskeharu versioon vastavalt oma SDK/rakenduse versioonile (nt **[release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Avatud **src \> Fiskaalintegratsioon \> Efr**.
    1. Avage **konfiguratsioonid \> DocumentProviders** ja laadige alla finantsdokumendi pakkuja konfiguratsioonifailid: **DocumentProviderFiscalEFRSampleAustria.xml** ja **DocumentProviderNonFiscalEFRSampleAustria.xml** (nt [vabastamise failide asukoht/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders)).
    1. Laadige alla maksuühenduse konfiguratsioonifail aadressilt **Konfiguratsioonid \> Ühendused \> ConnectorEFRSample.xml** (näiteks, [vabastamise fail/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > Uue sõltumatu pakendi- [ja laiendusmudeli](../dev-itpro/build-pipeline.md) piirangute tõttu ei saa seda praegu selle fiskaalse integratsiooni valimi jaoks kasutada. Peate kasutama Retail SDK eelmist versiooni arendaja VM-is LCS-is. Selle fiskaalse integratsiooni näidise konfiguratsioonifailid asuvad LCS-i arendaja VM-i jaemüügi SDK järgmistes kaustades.
    >
    > - **Rahandusdokumendi pakkuja konfiguratsioonifailid:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration
    > - **Fiscal connectori konfiguratsioonifail:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EFRSample\\Configuration
    > 
    > Eelarveintegratsiooni näidiste uue sõltumatu pakendi- ja laiendusmudeli toetamine on kavandatud hilisematele versioonidele.

1. Valige suvandid **Jaemüük ja kaubandus \> Headquartersi häälestus \> Parameetrid \> Commerce’i ühiskasutuses parameetrid**. peal **Kindral** vahekaardil määrake **Luba maksuintegratsioon** võimalus **Jah**.
1. **Avage jae- ja kaubanduskanali \> häälestus \> Fiskaalseintegratsiooni \> fiskaaldokumentide pakkujad** ja laadige varem alla laaditud fiskaaldokumendi pakkuja konfiguratsioonifailid.
1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Fiskaalühendused** ja laadige varem alla laaditud fiskaalse konnektori konfiguratsioonifail.
1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Konnektori funktsionaalsed profiilid**. Looge kaks uut konnektori funktsionaalset profiili, üks iga varem laaditud rahandusdokumendi pakkuja kohta, ja valige varem laaditud fiskaalkonnektor. Värskendage andmete vastendamise [sätteid](#default-data-mapping) vastavalt vajadusele.
1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Konnektori tehnilised profiilid**. Looge uus konnektori tehniline profiil ja valige varem laaditud fiskaalkonnektor. Värskendage [konnektori sätteid](#fiscal-connector-settings) vastavalt vajadusele.
1. **Avage jaemüügi- ja kaubanduskanali \> häälestus \> Fiskaalintegratsioon \> Fiskaalkonnektorigrupid**. Looge kaks uut fiskaalse konnektori rühma, üks iga varem loodud konnektori funktsionaalse profiili kohta.
1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Fiskaalsed registreerimise protsessid**. Looge uus finantsregistreerimise protsess ja kaks finantsregistreerimise protsessietappi ning valige varem loodud fiskaalse konnektorigrupid.
1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Funktsiooniprofiilid**. Valige funktsiooniprofiil, mis on lingitud poega, kus registreerimisprotsess tuleks aktiveerida. peal **Maksustamise registreerimise protsess** FastTab, valige varem loodud maksuregistreerimisprotsess. Mitte fiscalsündmuste kassas **registreerimise lubamiseks seadke kiirkaardil Tegevused** kassas **valikuks** **Audit** valikule **Jah**.
1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Riistvaraprofiilid**. Valige riistvaraprofiil, mis on lingitud riistvarajaamaga, millega fiskaalprinter ühendatakse. Valige kiirkaardil **Fiskaalsed välisseadmed** varem loodud konnektori tehniline profiil.
1. Avage jaotusgraafik (**jae- ja kaubandus \> - ja kaubandus-kaubanduse IT-jaotuse \> ajakava**) ning valige tööd **1070** ja **1090**, et edastada andmeid kanali andmebaasi.

#### <a name="default-data-mapping"></a>Andmete vaikevastendus

Rahandusdokumendi pakkuja konfiguratsioonis, mis on esitatud fiskaalse integratsiooni valimi osana, kaasatakse järgmine andmete vaikevastendus.

- **Käibemaksu (KM) määrade kaardistamine** – käibemaksukoodide jaoks seadistatud maksuprotsentide väärtuste vastendamine väärtustega **TaxG** (maksugrupp) atribuut taotlustes, mis saadetakse maksuteenistusele. Siin on vaikevastendus.

    ```
    A: 20.00; B: 10.00; C: 13.00; D: 0.00; E: 19.00; F: 7.00
    ```

    Iga paari esimene komponent esindab käibemaksurühma, mida toetab EFR-i maksuregistreerimise teenus. Teine komponent tähistab vastavat KÄIBEMAKSUmäära. Lisateavet käibemaksukohustuslaste rühmade kohta, mida EFR Austria puhul toetab, leiate EFR-i [viitest](https://public.efsta.net/efr/).

#### <a name="fiscal-connector-settings"></a>Fiskaalse konnektori sätted

Fiskaalse konnektori konfiguratsiooni kuuluvad järgmised sätted, mis on esitatud fiskaalse integratsiooni valimi osana.

- **Lõpp-punkti aadress** – maksuregistreerimisteenuse URL.
- **Seadme ajalõng** – millisekundites olev aeg, mil fiskaalkonnektor ootab fiskaalregistreerimisteenuse vastust.
- **Näita maksuregistreerimise teatisi** – See lipp juhib, kas operaatorile tuleks näidata teatisi, mille maksuregistri teenus tagastab.

### <a name="configure-channel-components"></a>Kanali komponentide seadistamine

> [!WARNING]
> Uue sõltumatu pakendi- [ja laiendusmudeli](../dev-itpro/build-pipeline.md) piirangute tõttu ei saa seda praegu selle fiskaalse integratsiooni valimi jaoks kasutada. Peate kasutama Retail SDK eelmist versiooni arendaja VM-is LCS-is. Lisateavet vt [teemast Deployment guidelines for fiscal integration sample for Austria (legacy)](emea-aut-fi-sample-sdk.md).
>
> Eelarveintegratsiooni näidiste uue sõltumatu pakendi- ja laiendusmudeli toetamine on kavandatud hilisematele versioonidele.

#### <a name="set-up-the-development-environment"></a>Seadistage arenduskeskkond

Näidise testimiseks ja laiendamiseks arenduskeskkonna seadistamiseks toimige järgmiselt.

1. Kloonige või laadige alla [Dynamics 365 Commerce Lahendused](https://github.com/microsoft/Dynamics365Commerce.Solutions) hoidla. Valige õige väljalaske haru versioon vastavalt oma SDK/rakenduse versioonile. Lisateabe saamiseks vt [Laadige alla jaemüügi SDK näidised ja viitepaketid GitHubist ja NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Avage EFR-lahendus aadressil **Dynamics365Commerce.Solutions\\ Fiskaalintegratsioon\\ Efr\\ EFR.sln**, ja ehitada see.
1. Installige CRT laiendused:

    1. Otsige üles CRT laienduse paigaldaja:

        - **Kaubanduse mastaabiüksus:** Aastal **Efr\\ Skaalaühik\\ ScaleUnit.EFR.Installer\\ prügikast\\ Silumine\\ net461** kaust, otsige üles **ScaleUnit.EFR.Installer** paigaldaja.
        - **Kohalik CRT kaasaegses POS-is:** Aastal **Efr\\ Kaasaegne POS\\ ModernPOS.EFR.Installer\\ prügikast\\ Silumine\\ net461** kaust, otsige üles **ModernPOS.EFR.Installer** paigaldaja.

    1. Alustage CRT laienduse installija käsurealt:

        - **Kaubanduse mastaabiüksus:**

            ```Console
            ScaleUnit.EFR.Installer.exe install --verbosity 0
            ```

        - **Kohalik CRT kaasaegses POS-is:**

            ```Console
            ModernPOS.EFR.Installer.exe install --verbosity 0
            ```

1. Installige riistvarajaama laiendused:

    1. Aastal **Efr\\ Riistvarajaam\\ HardwareStation.EFR.Installer\\ prügikast\\ Silumine\\ net461** kaust, otsige üles **HardwareStation.EFR.Installer** paigaldaja.
    1. Käivitage laienduse paigaldaja käsurealt.

        ```Console
        HardwareStation.EFR.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Tootmiskeskkond

Järgige juhiseid [Seadistage fiskaalintegratsiooni näidise jaoks ehituskonveier](fiscal-integration-sample-build-pipeline.md) luua ja vabastada Cloud Scale Unit ja iseteenindusega juurutatavad paketid fiskaalintegratsiooni näidise jaoks. The **EFR build-pipeline.yml** malli YAML-faili leiate **Torujuhe\\ YAML_Files** kaust [Dynamics 365 Commerce Lahendused](https://github.com/microsoft/Dynamics365Commerce.Solutions) hoidla.

## <a name="design-of-extensions"></a>Laienduste kujundus

Austria fiskaalregistreerimisteenuse integreerimise näidis põhineb fiskaalintegratsiooni [funktsioonil](fiscal-integration-for-retail-channel.md) ja on osa retail SDK-st. Näidis asub aadressil **src\\ Fiskaalintegratsioon\\ Efr** kaust [Dynamics 365 Commerce Lahendused](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidla (näiteks [väljalaskes olev näidis/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Näidis [koosneb](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskaaldokumentide pakkuja, mis on laiendus CRT ja fiskaalne pistik, mis on Commerce Hardware Stationi laiendus. Lisateavet jaemüügi SDK kasutamise kohta leiate teemast [Retail SDK arhitektuur](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [Sõltumatu pakendiga SDK](../dev-itpro/build-pipeline.md) ehitustorustiku seadistamine.

> [!WARNING]
> Uue sõltumatu pakendi- [ja laiendusmudeli](../dev-itpro/build-pipeline.md) piirangute tõttu ei saa seda praegu selle fiskaalse integratsiooni valimi jaoks kasutada. Peate kasutama Retail SDK eelmist versiooni arendaja VM-is LCS-is. Lisateavet vt [teemast Deployment guidelines for fiscal integration sample for Austria (legacy)](emea-aut-fi-sample-sdk.md). Eelarveintegratsiooni näidiste uue sõltumatu pakendi- ja laiendusmudeli toetamine on kavandatud hilisematele versioonidele.

### <a name="commerce-runtime-extension-design"></a>Commerce'i käitusaja laienduse kujundus

Fiskaaldokumendi pakkuja laienduse eesmärk on luua teenusepõhiseid dokumente ja käsitleda fiskaalregistreerimisteenuse vastuseid.

#### <a name="request-handler"></a>Taotluse käitleja

Dokumendipakkujatele on kaks päringukäsitlejat.

- **DocumentProviderEFRFiscalAUT** – seda käitlejat kasutatakse finantsregistreerimisteenuse finantsdokumentide loomiseks.
- **DocumentProviderEFRNonFiscalAUT** – seda käitlejat kasutatakse fiskaalregistreerimisteenuse jaoks mitte fiscal-dokumentide loomiseks.

Need käitlejad on päritud **INamedRequestHandleri** liidesest. **Käitleja nime tagastamise eest vastutab meetod HandlerName**. Käitleja nimi peaks vastama Commerce'i peakontoris määratud konnektori dokumendipakkuja nimele.

Konnektor toetab järgmisi taotlusi.

- **GetFiscalDocumentDocumentProviderRequest** – see taotlus sisaldab teavet selle kohta, milline dokument tuleks luua. See tagastab teenusepõhise dokumendi, mis tuleks registreerida maksuregistreerimisteenuses.
- **GetNonFiscalDocumentDocumentProviderRequest** – see taotlus sisaldab teavet selle kohta, milline mitte-fiskaalne dokument tuleks luua. See tagastab teenusepõhise dokumendi, mis tuleks registreerida maksuregistreerimisteenuses.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – See päring tagastab tellitavate sündmuste loendi. Praegu toetatakse järgmisi sündmusi: müük, X-aruande printimine, Z-aruande printimine, kliendikonto hoiused, klienditellimuse hoiused, auditisündmused ja müügivälised tehingud.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – See päring tagastab maksuregistreerimisteenuse vastuse. See vastus järjestatakse stringi moodustamiseks, nii et see on salvestamiseks valmis.

#### <a name="configuration"></a>Konfiguratsioon

Rahandusdokumendi pakkuja konfiguratsioonifailid asuvad lahenduste hoidla kaustas **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders** [Dynamics 365 Commerce:](https://github.com/microsoft/Dynamics365Commerce.Solutions/)

- **DocumentProviderFiscalEFRSampleAustria** – rahandusdokumentide pakkuja konfiguratsioonifail.
- **DocumentProviderNonFiscalEFRSampleAustria** – mittemeedsedokumentide pakkuja konfiguratsioonifail.

Nende failide eesmärk on lubada finantsdokumendi pakkuja sätete konfigureerimist Commerce'i peakontorist. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetega.

### <a name="hardware-station-extension-design"></a>Riistvarajaama laienduse disain

Fiskaalühenduseks oleva laienduse eesmärk on suhelda maksuregistriteenusega. Riistvarajaama laiendus kasutab HTTP-protokolli dokumentide esitamiseks, mis CRT laiendus genereerib maksuregistriteenuse. Samuti käsitleb see maksuregistreerimisteenuselt saadud vastuseid.

#### <a name="request-handler"></a>Taotluse käitleja

The **EFRHandler** päringu töötleja on maksuregistreerimisteenuse taotluste käsitlemise sisenemispunkt.

Käitleja on päritud **INamedRequestHandler** liides. **Käitleja nime tagastamise eest vastutab meetod HandlerName**. Töötleja nimi peaks ühtima fiskaalse konnektori nimega, mis on määratud Commerce'i peakorteris.

Fiskaalkonnektor toetab järgmisi taotlusi.

- **SubmitDocumentFiscalDeviceRequest** – See päring saadab dokumendid maksuregistreerimisteenistusele ja saadab sealt vastuse.
- **IsReadyFiscalDeviceRequest** – Seda päringut kasutatakse maksuregistriteenuse tervisekontrolliks.
- **InitializeFiscalDeviceRequest** – Seda päringut kasutatakse maksuregistreerimisteenuse lähtestamiseks.

#### <a name="configuration"></a>Konfiguratsioon

Fiskaalse konnektori konfiguratsioonifail asub aadressil **src\\ Fiskaalintegratsioon\\ Efr\\ Konfiguratsioonid\\ Ühendused\\ ConnectorEFRSample.xml** aastal [Dynamics 365 Commerce Lahendused](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidla. Faili eesmärk on võimaldada fiskaalühenduse seadete konfigureerimist Commerce'i peakorteris. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetega.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
