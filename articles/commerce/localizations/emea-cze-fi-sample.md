---
title: Tšehhi Vabariigi maksuregistreerimisteenuse integratsiooni näidis
description: See teema annab ülevaate Tšehhi Vabariigi eelarveintegratsiooni valimist Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-4-1
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 990de96f57f4a22b4d58da5f970b1b96f5fc21f5
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077086"
---
# <a name="fiscal-registration-service-integration-sample-for-the-czech-republic"></a>Tšehhi Vabariigi maksuregistreerimisteenuse integratsiooni näidis

[!include[banner](../includes/banner.md)]

See teema annab ülevaate Tšehhi Vabariigi eelarveintegratsiooni valimist Microsoft Dynamics 365 Commerce.

Tšehhi Vabariigi Dynamics 365 Commerce kassaaparaatide kohalike maksunõuete täitmiseks hõlmab Tšehhi Vabariigi funktsionaalsus müügikoha näidisi integreerimist välise maksuregistreerimisteenusega. Valim laiendab fiskaalintegratsiooni [funktsiooni](fiscal-integration-for-retail-channel.md). See põhineb EFSTA [EFR (Electronic Fiscal Register)](https://efsta.org/sicherheitsloesungen/) lahendusel [ja](https://efsta.org/) võimaldab EFR-teenusega suhelda HTTPS-protokolli kaudu. EFR-teenus tagab müügi elektroonilise registreerimise (EET - Elektronická evidence tržeb), st müügiandmete veebipõhise edastamise maksuhaldurite maksupõhisele veebiteenusele.

EFR-teenust tuleks majutada kas Commerce Hardware jaamas või eraldi masinas, millega saab riistvarajaamast ühendada. Proov on esitatud lähtekoodi kujul ja see on osa jaemüügi tarkvaraarenduskomplektist (SDK).

Microsoft ei väljasta EFSTA-st riist-, tarkvara ega dokumente. EFR-lahenduse saamiseks ja selle käitamiseks võtke ühendust EFSTA-ga [...](https://efsta.org/kontakt/).

## <a name="scenarios"></a>Stsenaariumid

Tšehhi Vabariigi maksuregistreerimisteenuse integratsioonivalim hõlmab järgmisi stsenaariume.

- Sularahakannete registreerimine maksuregistreerimisteenuses.

    - Saatke üksikasjalikud kandeandmed finantsregistreerimisteenusele. Need andmed sisaldavad müügirea teavet ning teavet allahindluste, maksete ja maksude kohta. Maksuregistreerimisteenus saadab andmed edasi maksuhalduri veebiteenusele ja saab sellelt kinnituse, mis sisaldab tehingu finantskoodi.
    - Jäädvustage vastus fiskaalregistreerimisteenusest. See vastus hõlmab finantsandmeid, nagu finants-ID-kood ja tehingu turvakood jne.
    - Saate printida kviitungil registreeritud kande finantsandmed.

- Kinkekaardi toimingute ja kliendihoiuste registreerimine maksuregistreerimisteenuses.

    - Väljastage või lisage kinkekaardile raha.
    - Registreerige kliendikonto deposiit.
    - Looge klienditellimus ja registreerige tellimuse tagatisraha.
    - Redigeerige klienditellimust ja alistage tellimuse deposiit.
    - Tühistage kliendi tellimus ja tagastage tellimuse tagatisraha.

- Tõrkekäsitlus ( nt järgmised suvandid).

    - Kui eelarveregistreerimine on võimalik uuesti proovida nt kui fiskaalregistreerimisteenus pole saadaval, pole valmis või ei vasta.
    - Lükake finantsregistreerimine edasi.
    - Jätke finantsregistreerimine vahele või märkige kanne registreerituks ning lisage tõrke põhjuse ja lisateabe jäädvustamiseks infokoodid.
    - Kontrollige finantsregistreerimisteenuse kättesaadavust enne uue müügikande avamist või müügikande lõpuleviimist.

### <a name="gift-cards"></a>Kinkekaardid

Finantsregistreerimisteenuse integreerimise näidis rakendab järgmisi kinkekaartidega seotud reegleid.

- Müügiread, mis on seotud *kinkekaardiGa* Väljastamine või *Lisa kinkekaardi* toimingutesse müügikandes, märgitakse eriatribuudiga, kui kanne on registreeritud finantsregistreerimisteenuses.
- Kinkekaardiga makset loetakse regulaarseks makseks ja märgitakse spetsiaalse atribuudiga, kui tehing on registreeritud maksukohustuslasena registreerimise teenuses.

### <a name="customer-account-deposits-and-customer-order-deposits"></a>Kliendikonto hoiused ja klienditellimuse hoiused

Finantsregistreerimisteenuse integreerimise näidis rakendab järgmisi reegleid, mis on seotud kliendikonto hoiuste ja klienditellimuse hoiustega.

- Kliendikonto deposiidi või klienditellimuse deposiidiga seotud kanne registreeritakse finantsregistreerimisteenuses ühe reakandena ja on tähistatud eriatribuudiga. Sellel real on määratud hoiuse KM grupp.
- Kui luuakse hübriidne klienditellimus, st klienditellimus, mis sisaldab tooteid, mida klient saab kauplusest läbi viia, samuti tooted, mis võetakse peale või saadetakse hiljem, sisaldab maksuregistreerimisteenuses registreeritud kanne teostatud toodete ridu ning tellimuse deposiidi rida.
- Kliendikonto makset loetakse tavaliseks makseks ja see on märgitud spetsiaalse atribuudiga, kui tehing on registreeritud maksuregistreerimisteenuses.
- Klienditellimuse deposiidi summat, mis rakendub klienditellimuse *pealevõtmistoimingule*, loetakse tavaliseks makseks ja märgitakse eriatribuudiga, kui kanne on registreeritud finantsregistreerimisteenuses.

### <a name="offline-registration"></a>Ühenduseta registreerimine

Kui maksuregistreerimisteenus ei edasta tehinguandmeid maksuhalduri fiskaalsele veebiteenusele (näiteks reageerimisaja tõttu) ja ei saa veebiteenuselt kinnitust (st tehingu finants-ID-koodi), loob see tehingule kohaliku allkirja ja lisab selle ning vastusesse spetsiaalse veakoodi. Maksuregistreerimisteenus saadab kanded algses järjekorras uuesti taustal kohe, kui võrguühendus on taastatud.

### <a name="limitations-of-the-sample"></a>Proovi piirangud

Maksuregistreerimisteenus toetab ainult stsenaariume, kus hinnas sisaldub käibemaks. Seetõttu **peab hinnas sisaldatav käibemaksusuvand** olema seatud **nii kaupluste kui ka klientide jaoks jah**.

## <a name="set-up-commerce-for-the-czech-republic"></a>Tšehhi Vabariigi kaubanduse häälestamine

Selles jaotises kirjeldatakse Tšehhi Vabariigile omast ja soovitatavat kaubandusseadet. Lisateavet leiate teemast [Commerce'i avaleht](../index.md).

Tšehhi-põhise funktsiooni kasutamiseks peate määrama järgmised sätted.

- Määrake **juriidilise isiku esmasel aadressil väli Riik/regioon** aadressiks **CZE** (Tšehhi Vabariik).
- Seadke **iga Tšehhi Vabariigis asuva kaupluse kassafunktsioonide profiilis ISO-koodi** väli **CZ** (Tšehhi Vabariik).

Samuti peate Tšehhi Vabariigi jaoks määrama järgmised sätted. Pange tähele, et pärast seadistuse lõpuleviimist peate käivitama asjakohased jaotustööd.

### <a name="set-up-vat-per-czech-republic-requirements"></a>Käibemaksu häälestamine Tšehhi Vabariigi nõuete kohta


Peate looma käibemaksukoodid, käibemaksugrupid ja kauba käibemaksugrupid. Samuti peate seadistama toodete ja teenuste käibemaksuteabe. Lisateavet käibemaksufunktsioonide seadistamise ja kasutamise kohta leiate teemast [Käibemaksu ülevaade](../../finance/general-ledger/indirect-taxes-overview.md).

### <a name="set-up-stores"></a>Kaupluste häälestamine

Värskendage **lehel Kõik kauplused** poe üksikasju. Täpsemalt määrake järgmised parameetrid.

- Määrake väljal **Käibemaksugrupp** käibemaksugrupp, mida tuleks kasutada vaikekliendile müügiks.
- Määrake **suvandi Hinnad sisaldavad käibemaksu** valikuks **Jah**.
- Määrake **väli Nimi** ettevõtte nimeks. See muudatus aitab tagada, et ettevõtte nimi kuvatakse müügikviitungil. Teise võimalusena saate ettevõtte nime lisada müügikviitungi paigutusele vabas vormis tekstina.
- **Määrake välja Maksu ID-number (TIN)** ettevõtte ID-numbriks. See muudatus aitab tagada, et ettevõtte ID-number kuvatakse müügikviitungil. Teise võimalusena saate ettevõtte ID-numbri lisada müügikviitungi paigutusele vabas vormis tekstina.

### <a name="set-up-functionality-profiles"></a>Funktsiooniprofiilide häälestamine

Kassafunktsioonide profiilide häälestamine.

- Seadistage **kiirkaardil Tarne nummerdamine** kviitungi nummerdamine, luues või värskendades kirjeid müügi **-,** müügitellimuse **- ja** tagastustarne **kandetüüpide jaoks**.

### <a name="set-up-registration-numbers"></a>Registreerimisnumbrite häälestamine

1. Minge organisatsiooni **administreerimise \> globaalse aadressiraamatu \> registreerimistüüpide \> registritüüpide juurde**. Looge uus registreerimistüüp. **Määrake väli Riik/regioon** aadressile **CZE** (Tšehhi Vabariik) ja piirake seda organisatsiooniga.
2. Minge organisatsiooni **administreerimise \> globaalse aadressiraamatu \> registreerimistüüpide \> registrikategooriatesse**. Looge uus registreerimiskategooria. Valige eelmisest etapist registreerimistüüp ja seadke **kategooria Registreerimine ärieelduse ID-ks** **.**
3. Avage **Organisatsiooni haldamine \> Organisatsioonid \> Tootmisüksused**. Valige iga Tšehhi Vabariigis asuva kaupluse puhul kauplusega seotud üksus. Laiendage **kiirkaardil Aadress** ripploendit **Veel suvandeid** ja valige **Täpsem**. 
4. Avamisel **Aadresside haldamine** lehel peate määrama järgmise sätte.

    - peal **Aadress** FastTab määras **Riik/regioon** väljale **CZE**.
    - peal **Registreerimistunnus** FastTab loob uue kirje. Valige varem loodud registreerimistüüp ja määrake registreerimisnumber.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Kohandatud väljade konfigureerimine nii, et neid saaks kasutada müügi sissetulekute vormingutes

Saate konfigureerida keeleteksti ja kohandatud väljad, mida kasutatakse kassa kviitungi vormingutes. Kviitungi häälestuse loonud kasutaja vaikeettevõte peaks olema sama juriidiline isik, kus keeleteksti häälestus luuakse. Teise võimalusena tuleks luua samad keeletekstid nii kasutaja vaikeettevõttes kui ka selle poe juriidilises isikus, kellele häälestus on loodud.

**Lisage lehel Keeletekst** kviitungipaigutuste kohandatud väljade siltide jaoks järgmised kirjed. Pange tähele, et **tabelis kuvatavad keele ID**, **teksti ID** ja **tekstiväärtused** on vaid näited. Saate neid vastavalt oma vajadustele muuta. Kasutatavad teksti ID **väärtused peavad siiski** olema kordumatud ja need peavad olema võrdsed või suuremad kui 900001.

Lisage järgmised POS-sildid **POS** osa **Keeletekst** tabelist:

| Keele ID | Teksti ID | Tekst                   |
|-------------|---------|------------------------|
| EN-US       | 900001  | ID provozovny/pokladny |
| EN-US       | 900002  | BKP                    |
| EN-US       | 900003  | PKP                    |
| EN-US       | 900004  | FIK                    |
| EN-US       | 900005  | Teave                   |
| EN-US       | 900006  | Järjekorranumber        |

**Lisage lehel Kohandatud väljad** kviitungipaigutuste kohandatud väljadele järgmised kirjed. Pange tähele, et **Tiitrite teksti ID** väärtused peavad vastama **Teksti ID** väärtused, mille määrasite **Keeletekst** leht:

| Nimi                 | Tüüp    | Pealdise teksti ID |
|----------------------|---------|-----------------|
| TLT                  | Sissetulek | 900001          |
| SEC                  | Sissetulek | 900002          |
| ALL                 | Sissetulek | 900003          |
| FISKALNE               | Sissetulek | 900004          |
| INFO                 | Sissetulek | 900005          |
| PIDEV NUMBER     | Sissetulek | 900006          |

> [!NOTE]
> On oluline määrata õiged kohandatud väljanimed, nagu on loetletud eelmises tabelis. Vale kohandatud välja nimi põhjustab kviitungitel puuduvaid andmeid.

### <a name="configure-receipt-formats"></a>Sissetulekuvormingute konfigureerimine

Iga nõutava kviitungivormingu puhul muutke väärtust **Prindi käitumine** väljale **Printige alati**.

Lisage kviitungivormingu kujundaja vastavatele kviitungi jaotistele järgmised kohandatud väljad. Pange tähele, et väljanimed vastavad eelmises jaotises määratletud keeletekstidele.

- **Päis:** Lisage järgmised väljad.

    - **Kaupluse nimi** ja **Maksukohustuslasena registreerimise number** : neid välju kasutatakse kviitungitele ettevõtte nime ja isikukoodi printimiseks. Teise võimalusena saate küljendusele lisada vabas vormis tekstina ettevõtte nime ja isikukoodi.
    - **Kaupluse aadress**, **·**, **24h**, **number**, ja **Registri number**.
    - **Järjestuse number** : see väli identifitseerib sularahatehingu numbri maksuregistreerimise teenuses.

- **read:** Lisage järgmised väljad.

    - **Kauba nimetus**
    - **Kogus**
    - **Hind kokku koos käibemaksuga**

- **Jalus:** Lisage järgmised väljad.

    - Makseväljad, et prinditaks iga makseviisi maksesummad. Näiteks lisage **Pakkumise nimi** ja **Pakkumise summa** väljad paigutuse ühele reale.
    - **ID provozovny/pokladny** : sellel väljal trükitakse äriruumi ja kassaaparaadi tunnused.
    - **BKP** : sellel väljal prinditakse maksumaksja turvakood, mille on määranud maksuregistreerimisteenus.
    - **FIK** : sellel väljal prinditakse tehingu fiskaalne kood, mille maksuhalduri veebiteenus eduka veebipõhise registreerimise korral määrab.
    - **PKP** : sellel väljal prinditakse maksumaksja allkirjakood, mis võrguühenduseta registreerimise korral fiskaalse registreerimisteenuse poolt genereeritakse.
    - **Info** : sellel väljal prinditakse maksuregistriteenuse lisateave.

Kviitungivormingutega töötamise kohta lisateabe saamiseks vt [Kviitungivormingute seadistamine ja kujundamine](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-the-czech-republic"></a>Seadke sisse Tšehhi Vabariigi fiskaalintegratsioon

Tšehhi Vabariigi maksuregistriteenuse integreerimise näidis põhineb [fiskaalintegratsiooni funktsionaalsus](fiscal-integration-for-retail-channel.md) ja on osa jaemüügi SDK-st. Näidis asub aadressil **src\\ Fiskaalintegratsioon\\ Efr** kaust [Dynamics 365 Commerce Lahendused](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidla (näiteks [väljalaskes olev näidis/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). [Näidis koosneb](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskaaldokumendi pakkujast, mis on Commerce'i käitusaja CRT () laiendus, ja fiskaalse konnektori, mis on Commerce'i riistvarajaama laiendus. Lisateavet jaemüügi SDK kasutamise kohta leiate teemast [Retail SDK arhitektuur](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [Sõltumatu pakendiga SDK](../dev-itpro/build-pipeline.md) ehitustorustiku seadistamine.

> [!WARNING]
> Uue sõltumatu pakendi- [ja laiendusmudeli](../dev-itpro/build-pipeline.md) piirangute tõttu ei saa seda praegu selle fiskaalse integratsiooni valimi jaoks kasutada. Peate kasutama Retail SDK eelmist versiooni arendaja virtuaalses masinas (VM) elutsükli teenustes Microsoft Dynamics (LCS). Lisateabe saamiseks vt [Tšehhi Vabariigi eelarveintegratsiooni valimi kasutuselevõtu juhised (pärand)](emea-cze-fi-sample-sdk.md).
>
> Eelarveintegratsiooni näidiste uue sõltumatu pakendi- ja laiendusmudeli toetamine on kavandatud hilisematele versioonidele.

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
    1. Laadige alla maksudokumendi pakkuja konfiguratsioonifail aadressilt **Konfiguratsioonid \> Dokumendipakkujad \> DocumentProviderFiscalEFRSampleCzech.xml** (näiteks, [vabastamise fail/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleCzech.xml)).
    1. Laadige alla maksuühenduse konfiguratsioonifail aadressilt **Konfiguratsioonid \> Ühendused \> ConnectorEFRSample.xml** (näiteks, [vabastamise fail/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > Uue sõltumatu pakendi- [ja laiendusmudeli](../dev-itpro/build-pipeline.md) piirangute tõttu ei saa seda praegu selle fiskaalse integratsiooni valimi jaoks kasutada. Peate kasutama Retail SDK eelmist versiooni arendaja VM-is LCS-is. Selle fiskaalse integratsiooni näidise konfiguratsioonifailid asuvad LCS-i arendaja VM-i jaemüügi SDK järgmistes kaustades.
    >
    > - **Maksudokumendi pakkuja konfiguratsioonifail:** RetailSdk\\ Näidislaiendid\\ CommerceRuntime\\ Extensions.DocumentProvider.EFRSample\\ Seadistamine\\ DocumentProviderFiscalEFRSampleCzech.xml
    > - **Fiskaalse konnektori konfiguratsioonifail:** RetailSdk\\ Näidislaiendid\\ Riistvarajaam\\ Laiendus.EFRSnäidis\\ Seadistamine\\ ConnectorEFRSample.xml
    > 
    > Eelarveintegratsiooni näidiste uue sõltumatu pakendi- ja laiendusmudeli toetamine on kavandatud hilisematele versioonidele.

1. Valige suvandid **Jaemüük ja kaubandus \> Headquartersi häälestus \> Parameetrid \> Commerce’i ühiskasutuses parameetrid**. peal **Kindral** vahekaardil määrake **Luba maksuintegratsioon** võimalus **Jah**.
1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Maksudokumentide pakkujad** ja laadige varem alla laaditud maksudokumendi pakkuja konfiguratsioonifail.
1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Fiskaalühendused** ja laadige varem alla laaditud fiskaalse konnektori konfiguratsioonifail.
1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Konnektori funktsionaalsed profiilid**. Looge uus konnektori funktsionaalne profiil. Valige dokumendipakkuja ja varem laaditud konnektor. Värskendage andmete vastendamise [sätteid](#default-data-mapping) vastavalt vajadusele.
1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Konnektori tehnilised profiilid**. Looge uus konnektori tehniline profiil ja valige varem laaditud fiskaalkonnektor. Värskendage [konnektori sätteid](#fiscal-connector-settings) vastavalt vajadusele.
1. **Avage jaemüügi- ja kaubanduskanali \> häälestus \> Fiskaalintegratsioon \> Fiskaalkonnektorigrupid**. Looge varem loodud konnektori funktsionaalse profiili jaoks uus fiskaalse konnektori rühm.
1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Fiskaalsed registreerimise protsessid**. Looge uus maksuregistreerimisprotsess ja fiskaalse registreerimise protsessi etapp ning valige varem loodud maksuühenduse rühm.
1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Funktsiooniprofiilid**. Valige funktsiooniprofiil, mis on lingitud poega, kus registreerimisprotsess tuleks aktiveerida. peal **Maksustamise registreerimise protsess** FastTab, valige varem loodud maksuregistreerimisprotsess.
1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Riistvaraprofiilid**. Valige riistvaraprofiil, mis on lingitud riistvarajaamaga, millega fiskaalprinter ühendatakse. Valige kiirkaardil **Fiskaalsed välisseadmed** varem loodud konnektori tehniline profiil.
1. Avage jaotusgraafik (**jae- ja kaubandus \> - ja kaubandus-kaubanduse IT-jaotuse \> ajakava**) ning valige tööd **1070** ja **1090**, et edastada andmeid kanali andmebaasi.

#### <a name="default-data-mapping"></a>Andmete vaikevastendus

Rahandusdokumendi pakkuja konfiguratsioonis, mis on esitatud fiskaalse integratsiooni valimi osana, kaasatakse järgmine andmete vaikevastendus.

- **Käibemaksu (KM) määrade kaardistamine** – käibemaksukoodide jaoks seadistatud maksuprotsentide väärtuste vastendamine väärtustega **TaxG** (maksugrupp) atribuut taotlustes, mis saadetakse maksuteenistusele. Siin on vaikevastendus.

    ```
    A: 21.00; B: 15.00; C: 10.00; Z: 0.00
    ```

    Iga paari esimene komponent esindab käibemaksurühma, mida toetab EFR-i maksuregistreerimise teenus. Teine komponent tähistab vastavat KÄIBEMAKSUmäära. Lisateavet EFR-i Tšehhi Vabariigis toetatavate käibemaksugruppide kohta leiate aadressilt [EFR viide](https://public.efsta.net/efr/).

- **Vaikimisi käibemaksugrupi vastendus** – Kõik käibemaksusummad, mida ei saa ühega eelmääratud käibemaksugrupist vastendada, omistatakse vaikimisi (põhi)käibemaksurühmale. Siin on vaikevastendus.

    ```
    A
    ```

- **Sissemakse käibemaksugrupi kaardistamine** – Kliendi sissemakse summad ja kliendi tellimuse sissemakse summad seotakse sissemakse käibemaksu gruppi. Siin on vaikevastendus.

    ```
    Z
    ```

#### <a name="fiscal-connector-settings"></a>Fiskaalse konnektori sätted

Fiskaalse konnektori konfiguratsiooni kuuluvad järgmised sätted, mis on esitatud fiskaalse integratsiooni valimi osana.

- **Lõpp-punkti aadress** – maksuregistreerimisteenuse URL.
- **Aeg maha** – Aeg millisekundites, mille jooksul fiskaalne konnektor ootab maksuregistreerimisteenuse vastust.

### <a name="configure-channel-components"></a>Kanali komponentide seadistamine

> [!WARNING]
> Uue sõltumatu pakendi- [ja laiendusmudeli](../dev-itpro/build-pipeline.md) piirangute tõttu ei saa seda praegu selle fiskaalse integratsiooni valimi jaoks kasutada. Peate kasutama Retail SDK eelmist versiooni arendaja VM-is LCS-is. Lisateabe saamiseks vt [Tšehhi Vabariigi eelarveintegratsiooni valimi kasutuselevõtu juhised (pärand)](emea-cze-fi-sample-sdk.md).
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
    1. Käivitage laienduse installija käsurealt:

        ```Console
        HardwareStation.EFR.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Tootmiskeskkond

Järgige juhiseid [Seadistage fiskaalintegratsiooni näidise jaoks ehituskonveier](fiscal-integration-sample-build-pipeline.md) luua ja vabastada Cloud Scale Unit ja iseteenindusega juurutatavad paketid fiskaalintegratsiooni näidise jaoks. The **EFR build-pipeline.yml** malli YAML-faili leiate **Torujuhe\\ YAML_Files** kaust [Dynamics 365 Commerce Lahendused](https://github.com/microsoft/Dynamics365Commerce.Solutions) hoidla.

## <a name="design-of-extensions"></a>Laienduste kujundus

Tšehhi Vabariigi maksuregistriteenuse integreerimise näidis põhineb [fiskaalintegratsiooni funktsionaalsus](fiscal-integration-for-retail-channel.md) ja on osa jaemüügi SDK-st. Näidis asub aadressil **src\\ Fiskaalintegratsioon\\ Efr** kaust [Dynamics 365 Commerce Lahendused](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidla (näiteks [väljalaskes olev näidis/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Näidis [koosneb](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskaaldokumentide pakkuja, mis on laiendus CRT ja fiskaalne pistik, mis on Commerce Hardware Stationi laiendus. Lisateavet jaemüügi SDK kasutamise kohta leiate teemast [Retail SDK arhitektuur](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [Sõltumatu pakendiga SDK](../dev-itpro/build-pipeline.md) ehitustorustiku seadistamine.

> [!WARNING]
> Uue sõltumatu pakendi- [ja laiendusmudeli](../dev-itpro/build-pipeline.md) piirangute tõttu ei saa seda praegu selle fiskaalse integratsiooni valimi jaoks kasutada. Peate kasutama Retail SDK eelmist versiooni arendaja VM-is LCS-is. Lisateabe saamiseks vt [Tšehhi Vabariigi eelarveintegratsiooni valimi kasutuselevõtu juhised (pärand)](emea-cze-fi-sample-sdk.md). Eelarveintegratsiooni näidiste uue sõltumatu pakendi- ja laiendusmudeli toetamine on kavandatud hilisematele versioonidele.

### <a name="commerce-runtime-extension-design"></a>Commerce'i käitusaja laienduse kujundus

Fiskaaldokumendi pakkuja laienduse eesmärk on luua teenusepõhiseid dokumente ja käsitleda fiskaalregistreerimisteenuse vastuseid.

#### <a name="request-handler"></a>Taotluse käitleja

Üksik on olemas **DocumentProviderEFRFiscalCZE** Dokumendipakkuja päringu töötleja, mida kasutatakse fiskaaldokumentide genereerimiseks maksuregistreerimisteenuse jaoks.

See töötleja on päritud **INamedRequestHandler** liides. **Käitleja nime tagastamise eest vastutab meetod HandlerName**. Käitleja nimi peaks vastama Commerce'i peakontoris määratud konnektori dokumendipakkuja nimele.

Konnektor toetab järgmisi taotlusi.

- **GetFiscalDocumentDocumentProviderRequest** – see taotlus sisaldab teavet selle kohta, milline dokument tuleks luua. See tagastab teenusepõhise dokumendi, mis tuleks registreerida maksuregistreerimisteenuses.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – See päring tagastab tellitavate sündmuste loendi. Hetkel toetatakse järgmisi üritusi: müük, kliendikonto sissemaksed ja klientide tellimuste sissemaksed.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – See päring tagastab maksuregistreerimisteenuse vastuse. See vastus järjestatakse stringi moodustamiseks, nii et see on salvestamiseks valmis.

#### <a name="configuration"></a>Konfiguratsioon

Maksudokumendi pakkuja konfiguratsioonifail asub aadressil **src\\ Fiskaalintegratsioon\\ Efr\\ Konfiguratsioonid\\ Dokumendipakkujad\\ DocumentProviderFiscalEFRSampleCzech.xml** aastal [Dynamics 365 Commerce Lahendused](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidla. Faili eesmärk on võimaldada fiskaaldokumentide pakkuja seadeid konfigureerida Commerce'i peakorteris. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetega.

### <a name="hardware-station-extension-design"></a>Riistvarajaama laienduse disain

Fiskaalühenduseks oleva laienduse eesmärk on suhelda maksuregistriteenusega. Riistvarajaama laiendus kasutab HTTP-protokolli dokumentide esitamiseks, mis CRT laiendus genereerib maksuregistriteenuse. Samuti käsitleb see maksuregistreerimisteenuselt saadud vastuseid.

#### <a name="request-handler"></a>Taotluse käitleja

The **EFRHandler** päringu töötleja on maksuregistreerimisteenuse taotluste käsitlemise sisenemispunkt.

Käitleja on päritud **INamedRequestHandler** liides. **Käitleja nime tagastamise eest vastutab meetod HandlerName**. Töötleja nimi peaks ühtima fiskaalse konnektori nimega, mis on määratud Commerce'i peakorteris.

Konnektor toetab järgmisi taotlusi.

- **SubmitDocumentFiscalDeviceRequest** – See päring saadab dokumendid maksuregistreerimisteenistusele ja saadab sealt vastuse.
- **IsReadyFiscalDeviceRequest** – Seda päringut kasutatakse maksuregistriteenuse tervisekontrolliks.
- **InitializeFiscalDeviceRequest** – Seda päringut kasutatakse maksuregistreerimisteenuse lähtestamiseks.

#### <a name="configuration"></a>Konfiguratsioon

Fiskaalse konnektori konfiguratsioonifail asub aadressil **src\\ Fiskaalintegratsioon\\ Efr\\ Konfiguratsioonid\\ Ühendused\\ ConnectorEFRSample.xml** aastal [Dynamics 365 Commerce Lahendused](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidla. Faili eesmärk on võimaldada fiskaalühenduse seadete konfigureerimist Commerce'i peakorteris. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetega.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
