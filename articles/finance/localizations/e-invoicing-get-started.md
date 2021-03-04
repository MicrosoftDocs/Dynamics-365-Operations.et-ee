---
title: Elektroonilise arvelduse lisandmooduli kasutamise alustamine
description: Sellest teemast leiate teabe, mis aitab teil rakendustes Microsoft Dynamics 365 Finance ja Dynamics 365 Supply Chain Management elektroonilise arvelduse lisandmoodulit kasutama hakata.
author: gionoder
manager: AnnBe
ms.date: 10/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 7b2a3aae43d42060c7fcd9e1ea3db814fc5d8f22
ms.sourcegitcommit: f860ac2b18f6bbbfc4a46b497baec2477105b116
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/19/2020
ms.locfileid: "4442548"
---
# <a name="get-started-with-the-electronic-invoicing-add-on"></a>Elektroonilise arvelduse lisandmooduli kasutamise alustamine

[!include [banner](../includes/banner.md)]

Sellest teemast leiate teabe, mis aitab teil elektroonilise arvelduse lisandmoodulit kasutama hakata. Esiteks antakse teile juhised konfigureerimise kohta lahendustes Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Services (RCS) ja Dynamics 365 Finance. Teiseks kirjeldatakse teenuse kaudu dokumentide edastamise protsessi rakenduses Dynamics 365 Finance või Dynamics 365 Supply Chain Management. Samuti saate teada, kuidas tõlgendada edastuslogisid.

## <a name="availability"></a>Kättesaadavus

Elektroonilise arvelduse lisandmoodul on alguses saadaval mitmes riigis. Lisandmoodul toetab elektrooniliste arvete loomist ja järgmiste äridokumentide esitamist.

| Riik/regioon  | Äridokument                          |
|-----------------|--------------------------------------------|
| Austria         | Müügi- ja projektiarved                 |
| Belgia         | Müügi- ja projektiarved                 |
| Brasiilia          | Elektroonilise finantsdokumendi mudel 55 (NF-e) |
| Taani         | Müügi- ja projektiarved                 |
| Eesti         | Müügi- ja projektiarved                 |
| Soome         | Müügi- ja projektiarved                 |
| Prantsusmaa          | Müügi- ja projektiarved                 |
| Saksamaa         | Müügi- ja projektiarved                 |
| Itaalia           | Müügi- ja projektiarved                 |
| Mehhiko          | CFDI arve                               |
| Holland     | Müügi- ja projektiarved                 |
| Norra          | Müügi- ja projektiarved                 |
| Hispaania           | Müügi- ja projektiarved                 |
| Euroopa          | PEPPOL-i müügi- ja projektiarved          |
    
## <a name="licensing"></a>Litsentsimine

Elektroonilise arvelduse lisandmoodulit saate kasutada oma praeguse litsentsiga. Teenuse kasutamiseks ei ole vaja lisalitsentse.

## <a name="prerequisites"></a>Eeltingimused

Enne selles teemas kirjeldatud sammude lõpetamist peavad täidetud olema järgmised eeltingimused.

- Juurdepääs LCS-i kontole.
- LCS-i juurutusprojekt, mis sisaldab rakenduse Finance või Supply Chain Management versiooni 10.0.13 või uuemat versiooni.
- Juurdepääs RCS-i kontole.
- Lülitage mooduli **Funktsioonihaldus** kaudu oma RCS-i konto jaoks sisse globaliseerimisfunktsioon. Lisateavet leiate jaotisest [Regulatory Configuration Services (RCS) – globaliseerimisfunktsioonid](rcs-globalization-feature.md)
- Looge Azure'is võtmehoidla ressurss ja salvestusruumi konto. Lisateavet leiate jaotisest [Azure'i salvestusruumi konto ja võtmehoidla loomine](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="overview"></a>Ülevaade

Järgmisel illustratsioonil on näha viis põhisammu, mille te selle teema käigus läbite.

![Selle teema viie sammu ülevaade](media/e-invoicing-services-get-started-overview-5-steps.png)

1. **Azure'i ressursside seadistus:** konfigureerige Azure'i salvestusruum ja digitaalsete sertide üleslaadimine Azure'i võtmehoidlas.
2. **LCS-i seadistus:** installige lisandmoodul mikroteenuste jaoks.
3. **RCS-i seadistus:** seadistage keskkond, kasutajate juurdepääs ja e-arvete funktsioonid.
4. **Kliendi seadistus:** seadistage ühendus kliendi ja elektroonilise arvelduse lisandmooduli vahel ning lülitage välja vanad elektrooniliste dokumentide edastamise ja vastuste vastuvõtmise funktsioonid.
5. **Arvete esitamine:** esitage elektroonilise arvelduse lisandmooduli kaudu elektroonilisi dokumente ja võtke vastu vastuseid.

> [!NOTE]
> Mõned selle teema konfiguratsioonisammud on tavalised ja riigi-/regioonipõhised. Riigi-/regioonipõhiseid samme ja seadistustoiminguid kirjeldatakse riigi-/regioonipõhistes teemades.

## <a name="lcs-setup"></a>LCS häälestus

1. Logige oma LCS-i kontole sisse.
2. Valige paan **Funktsiooni eelversiooni haldus** ning valige väljagrupist **Avaliku eelversiooni funktsioonid** suvand **BusinessDocumentSubmission**.
3. Märkige väli **Funktsiooni eelversioon on lubatud**.
4. Valige LCS-i juurutusprojekt. Enne projekti valimist peab see olema konfigureeritud ja töötama.
5. Valige kiirkaardil **Keskkonna lisandmoodulid** suvand **Installi uus lisandmoodul**.
6. Valige **Äridokumendi esitamine**.
7. Sisestage dialoogiboksis **Lisandmooduli seadistus** väljale **AAD rakenduse ID** tekst **091c98b0-a1c9-4b02-b62c-7753395ccabe**. See väärtus ei muutu.
8. Sisestage väljale **AAD rentniku ID** oma Azure'i tellimuse konto ID.

    ![Lisandmooduli seadistuse dialoogiboks LCS-is](media/e-invoicing-services-get-started-lcs-addin-setup.png)

9. Tingimustega nõustumiseks valige märkeruut.
10. Valige **Installi**.

## <a name="rcs-setup"></a>RCS-i seadistus

RCS-i seadistuse käigus teete järgmist.

1. Seadistage RCS-is võtmehoidla.
2. Seadistage RCS-i integratsioon elektroonilise arvelduse lisandmooduli serveriga.
3. Looge oma organisatsiooni jaoks elektroonilise arvelduse lisandmooduli keskkond.

### <a name="set-up-the-key-vault-in-rcs"></a>RCS-is võtmehoidla seadistamine

1. Logige oma RCS-i kontole sisse.
2. Valige tööruumis **Globaliseerimisfunktsioonid** jaotises **Keskkonnad** paan **E-arveldus**.
3. Valige **Teenusekeskkonnad**.

    ![Teenusekeskkondade valimine](media/e-invoicing-services-get-started-select-service-environments.png)

> [!NOTE]
> Suvand **Ühendatud rakendused** võimaldab pääseda RCS-i kaudu juurde rakenduses Finance või Supply Chain Management olevale elektroonilise arvelduse lisandmooduli automaatsele konfiguratsioonile. Kuid praegu seda funktsiooni alles arendatakse.

4. Valige toimingupaanil **Võtmehoidla parameetrid**.

    ![Võtmehoidla parameetri valimine](media/e-invoicing-services-get-started-select-key-vault-parameters.png)

5. Võtmehoidla lisamiseks valige toimingupaanilt suvand **Uus**.
6. Sisestage väljale **Võtmehoidla URI** Azure'is konfigureeritud võtmehoidla ressursi atribuudi **DNS-i nimi** väärtus. Lisateavet väärtuse **DNS-i nimi** leidmise kohta leiate jaotisest [Azure'i salvestusruumi konto ja võtmehoidla loomine](e-invoicing-create-azure-storage-account-key-vault.md).

    ![Võtmehoidla URI väli](media/e-invoicing-services-get-started-enter-key-vault-uri.png)

7. Valige kiirkaardil **Serdid** suvand **Lisa**, et sisestada kõik digitaalsete sertide nimed ja võtmehoidla saladused, mis on vajalikud usaldusväärsete ühenduste loomiseks. Veerus **Tüüp** saate määrata, kas see on sert või saladus. Mõlemad väärtuste komplektid on konfigureeritud Azure'is võtmehoidla ressursis.

    ![Sertide lisamine](media/e-invoicing-services-get-started-add-digital-certificates.png)

8. Kui teie riigi-/regioonipõhise arve puhul on digitaalallkirja rakendamiseks vaja serdiahelat, valige toimingupaanilt **Serdiahel** ja sisestage ahela moodustavate sertide või võtmehoidla saladuste järjekord.

### <a name="set-up-the-rcs-integration-with-the-electronic-invoicing-add-on-server"></a>RCS-i integratsiooni seadistamine elektroonilise arvelduse lisandmooduli serveriga

1. Valige tööruumi **Globaliseerimisfunktsioonid** jaotisest **Seotud sätted** link **Elektroonilise aruandluse parameetrid**.
2. Valige **Klõpsake siin, et luua ühendus teenusega Lifecycle Service**. Kui te ei soovi LCS-iga ühendust luua, valige **Tühista**.
3. Sisestage vahekaardil **E-arvelduse teenused** väljale **Teenuse lõpp-punkti URI** väärtus olemasolevate geograafiliste piirkondade järgi: `https://businessdocumentsubmission.us.operations365.dynamics.com/` või `https://businessdocumentsubmission.eu.operations365.dynamics.com/`.
4. Veenduge, et välja **Rakenduse ID** väärtus oleks ID **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. See väärtus ei muutu.
5. Sisestage väljale **LCS-i keskkonna ID** oma LCS-i tellimuse konto ID.

![Elektroonilise arvelduse lisandmooduli parameetrite sisestamine](media/e-invoicing-services-get-started-enter-e-invoicing-parameters.png)

### <a name="add-an-electronic-invoicing-add-on-environment"></a>Elektroonilise arvelduse lisandmooduli keskkonna lisamine

Saate luua elektroonilise arvelduse lisandmooduli jaoks eri keskkondi, näiteks arendus-, testimis- või töökeskkondi.

1. Valige tööruumis **Globaliseerimisfunktsioonid** jaotises **Keskkonnad** paan **E-arveldus**.
2. Valige keskkonna loomiseks **Uus**.
3. Sisestage väljale **Salvestusruumi SAS-tõendi konto** võtmehoidla saladuse nimi, mille te RCS-is võtmehoidlas konfigureerisite.

    ![Salvestusruumi SAS-tõendi konto väli](media/e-invoicing-services-get-started-enter-sas-token-secret.png)

4. Valige kiirkaardil **Kasutajad** suvand **Uus**, et anda kasutajatele juurdepääs sellele keskkonnale.

    ![Teenuse kasutajate lisamine](media/e-invoicing-services-get-started-enter-service-users.png)

5. Valige toimingupaanil **Avalda**, et avaldada keskkond elektroonilise arvelduse lisandmooduli serveris.

    ![Nupp „Avalda”](media/e-invoicing-services-get-started-publish-service-environment.png)

### <a name="e-invoicing-feature-setup"></a>E-arvelduse funktsiooni seadistus

„E-arvelduse funktsioon” on kindla ressursi üldnimi, mis on konfigureeritud ja avaldatud kasutama elektroonilise arvelduse lisandmooduli serverit. E-arvelduse funktsiooni seadistus hõlmab muu hulgas elektroonilise aruandluse (ER) konfiguratsiooni vormingute kasutamist, et luua konfigureeritavaid ekspordi- ja impordifaile, ning tegevuste ja tegevusvoogude kasutamist, et luua konfigureeritavaid reegleid taotluste saatmiseks, vastuste importimiseks ning vastuste sisu sõelumiseks.

Arvevormingute ja tegevusvoogude erinevuste tõttu on e-arvelduse funktsiooni seadistus riigi-/regioonipõhine.

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a>Elektroonilise arvelduse lisandmooduli integratsiooni seadistamine rakenduses Finance või Supply Chain Management 

Selle seadistuse käigus täidate järgmised ülesanded.

1. Funktsiooni eelväljaande avamine
2. Elektroonilise arvelduse lisandmooduli integratsioonifunktsiooni sisselülitamine, et lubada integratsioon rakendusega Finance.
3. Elektroonilise arvelduse lisandmooduli lõpp-punkti URL-i seadistamine.
4. ER-i konfiguratsioonide importimine, mis on seotud riigi-/regioonipõhise e-arvelduse funktsiooniga.
5. Asjakohase riigi-/regioonipõhise e-arvelduse funktsiooni sisselülitamine.
6. ER-i konfiguratsioonide importimine ja vastusetüüpide seadistamine, mis on vajalikud teie riigi-/regioonipõhise arvedokumendi värskendamiseks edastusprotsessi tulemusena.

### <a name="open-flighted-feature"></a>Funktsiooni eelväljaande avamine
Elektroonilise arve integratsioonifunktsiooni saab lubada eelväljaannete kaudu. Eelväljaanded võimaldavad funktsiooni vaikimisi sisse või välja lülitada. Järgmiseid samme järgides lubatakse mitte-töökeskkonnas eelväljaanne. 

1. Käivitage järgmine SQL-i käsk.

    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)
    
2. Pärast ülaltoodud muudatuse tegemist tehke toiming IISReset kõigi AOS-ide puhul

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a>Elektroonilise arvelduse lisandmooduli integratsioonifunktsiooni sisselülitamine

1. Logige sisse rakendusse Finance või Supply Chain Management.
2. Otsige tööruumis **Funktsioonihaldus** üles uus funktsioon **Konfigureeritav elektroonilise arvelduse lisandmooduli integratsioon**. Kui funktsioon pole ikka funktsioonihalduse lehel nähtav, käivitage funktsioon **Otsi värskendusi**
3. Valige funktsioon ja seejärel valige **Luba kohe**.

### <a name="set-up-the-service-endpoint-url"></a>Teenuse lõpp-punkti URL-i seadistamine

1. Avage **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameetrid**.
2. Sisestage vahekaardil **Edastusteenus** väljale **Teenuse lõpp-punkti URL** tekst `https://businessdocumentsubmission.us.operations365.dynamics.com/`.
3. Sisestage väljale **Keskkond** RCS-i seadistuse käigus loodud elektroonilise arvelduse lisandmooduli keskkonna nimi.

![Teenuse parameetrite sisestamine](media/e-invoicing-services-get-started-enter-service-endpoint.png)

### <a name="import-the-er-configurations"></a>ER-i konfiguratsioonide importimine

Et lubada äriandmete kogumine ja saatmine elektroonilise arvelduse lisandmoodulile, peate importima ER-i andmemudeli ja ER-i andmemudeli konfiguratsiooni, mis on seotud riigi-/regioonipõhise e-arvelduse funktsiooniga, mida soovite kasutada.

1. Valige tööruumi **Elektrooniline aruandlus** jaotisest **Konfiguratsioonipakkujad** paan **Microsoft**. Veenduge, et konfiguratsioonipakkuja olekuks oleks seatud **Aktiivne**. Lisateavet pakkuja **aktiivseks** märkimise kohta leiate teemast [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. Valige **Hoidlad**.
4. Valige **Globaalne ressurss** ja seejärel **Ava**.
5. Valige dialoogiboksis **Teenustega Lifecycle Services ühenduse loomine** suvand **Klõpsake siin, et luua ühendus teenusega Lifecycle Service**.
6. Sõltuvalt riigist või regioonist, kus soovite e-arvelduse funktsiooni kasutada, peate importima asjakohase andmemudeli, andmemudeli vastenduse ja vormingud. Lisateavet ER-i konfiguratsioonide kohta, mille peaksite importima, leiate riigi-/regioonipõhisest teemast „Elektroonilise arvelduse lisandmooduli kasutamise alustamine”.
7. Importige **Kliendi arve kontekstimudel**. See mudel sisaldab lisaparameetreid, mis kirjeldavad muu hulgas rakenduses Finance olevat keskkonda, mida kasutatakse elektroonilise arvelduse lisandmooduli jaoks äriandmete edastamise ajal.

### <a name="turn-on-countryregion-specific-e-invoicing-features"></a><a name="region-specific"></a>Riigi-/regioonipõhiste e-arvelduse funktsioonide sisselülitamine

Riigi-/regioonipõhiste e-arvelduse funktsioonide sisselülitamiseks, et need töötaksid koos elektroonilise arvelduse lisandmooduliga, peate funktsiooni sisse lülitama igas juriidilises isikus, kus soovite seda kasutada. Hiljem ei saa vana elektroonilise arvelduse integratsiooni enam kasutada ja integratsioon uue elektroonilise arvelduse lisandmooduliga on sisse lülitatud.

1. Avage **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameetrid**.
2. Valige vahekaardil **Funktsioonid** teie riigi-/regioonipõhise e-arvelduse funktsiooniga seotud reas märkeruut, mis asub veerus **Lubatud**. Lisateavet funktsioonide kohta, mille peaksite sisse lülitama, leiate riigi-/regioonipõhisest teemast „Elektroonilise arvelduse lisandmooduli kasutamise alustamine”.

![E-arvelduse funktsiooni sisselülitamine](media/e-invoicing-services-get-started-enable-invoicing-feature.png)

> [!NOTE]
> Kui teil on mitu juriidilist isikut, mis on konfigureeritud eri riikide või regioonide jaoks, saate iga juriidilise isiku puhul sisse lülitada riigi-/regioonipõhise e-arvelduse funktsiooni.

### <a name="import-er-configurations-and-set-up-the-response-types-to-update-your-countryregion-specific-invoice-document"></a>ER-i konfiguratsioonide importimine ja vastusetüüpide seadistamine riigi-/regioonipõhise arvedokumendi värskendamiseks

Kui edastatud arvedokumenti on vaja pärast riiklikele autentimisteenustele edastamise vastust värskendada, peate importima spetsiaalse ER-i andmemudeli ja konfiguratsioonid, et lubada arvedokumendi või muu lisavälja värskendamine.

1. Valige tööruumi **Elektrooniline aruandlus** jaotisest **Konfiguratsioonipakkujad** paan **Microsoft**.
2. Valige **Osad**.
3. Valige **Globaalne ressurss** ja seejärel **Ava**.
4. Importige **Vastuseteate mudel**, **Vastuseteate impordivorming**, **Vastuseteate mudeli vastendus sihtkohaga** ja **Failisisu impordivorming**.
5. Avage **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameetrid**.
6. Valige vahekaardil **Elektrooniline dokument** suvand **Lisa**, et sisestada teie riigi-/regioonipõhise arvedokumendiga seotud tabeli nimi. Lisateavet tabelinimede kohta, mille peaksite valima, leiate riigi-/regioonipõhisest teemast „Elektroonilise arvelduse lisandmooduli kasutamise alustamine”.
7. Valige **Vastuse tüübid**, et konfigureerida vastuse tüübid. Lisateavet tabelinimede kohta, mille peaksite valima, leiate riigi-/regioonipõhisest teemast „Elektroonilise arvelduse lisandmooduli kasutamise alustamine”.

![Vastusetüüpide seadistamine](media/e-invoicing-services-get-started-set-up-response-types.png)

## <a name="e-invoicing-feature-names-by-country"></a>E-arvelduse funktsiooni nimed riigi põhjal 
Järgmises tabelis on kirjeldatud muid e-arvelduse funktsioone, mida on võimalik elektrooniliste arvete loomiseks elektroonilise aruandluse globaalsest hoidlast alla laadida.
RCS-is saate alla laadida selles tabelis loetletud e-arvelduse funktsioonid, ER-i konfiguratsioonid ja saadaolevad e-arvelduse funktsiooni seadistused.
Rakenduses Finance saate lubada seotud funktsiooniviiteid lehel **Elektroonilise dokumendi parameetrid**, et väljastada nende riikide jaoks elektroonilisi arveid. Lisateavet leiate selle teema varasemast jaotisest [Riigi-/regioonipõhiste e-arvelduse funktsioonide sisselülitamine](#region-specific).

| Funktsiooni nimi                      | Kirjeldus                                 | Elektroonilise aruandluse konfiguratsioonid                                                                                                  | Seadistused                                                                                                                                                         | Riik/regioon  | Funktsiooni viide      |
|-----------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------|------------------------|
| Austria elektroonilised arved (AT) | Müügi- ja projektiarved Austria jaoks      | - OIOUBL-i müügiarve <br>- OIOUBL-i projektiarve <br>- OIOUBL-i müügi kreeditarve <br>- OIOUBL-i projekti kreeditarve | - Müügiarve loomine (AT) <br>- Projektiarve loomine (AT) <br>- Müügi kreeditarve loomine (AT) <br>- Projekti kreeditarve loomine (AT)         | Austria         | EUR-00023              |
| Belgia elektrooniline arve (BE)   | Müügi- ja projektiarved Belgia jaoks      | - UBL-i müügiarve BE <br>- UBL-i projektiarve BE <br>- UBL-i projekti kreeditarve BE <br>- UBL-i müügi kreeditarve BE | - Müügiarve loomine (BE)<br>- Projektiarve loomine (BE) <br>- Müügi kreeditarve loomine (BE) <br>- Projekti kreeditarve loomine (BE)         | Belgia         | EUR-00023              |
| Taani elektrooniline arve (DK)    | Müügi- ja projektiarved Taani jaoks      | - OIOUBL-i müügiarve <br>- OIOUBL-i projektiarve <br>- OIOUBL-i müügi kreeditarve <br>- OIOUBL-i projekti kreeditarve | - Müügiarve loomine (DK) <br>- Projektiarve loomine (DK) <br>- Müügi kreeditarve loomine (DK)<br>- Projekti kreeditarve loomine (DK)         | Taani         | EUR-00023<br> DK-00001 |
| Hollandi elektrooniline arve (NL)     | Müügi- ja projektiarved Hollandi jaoks  | - UBL-i müügiarve NL <br>- UBL-i projektiarve NL <br>- UBL-i müügi kreeditarve NL <br>- UBL-i projekti kreeditarve NL | - Müügiarve loomine (NL) <br> - Projektiarve loomine (NL) <br> - Müügi kreeditarve loomine (NL) <br>- Projekti kreeditarve loomine (NL)          | Holland | EUR-00023              |
| Eesti elektrooniline arve (EE)  | Müügi- ja projektiarved Eesti jaoks      | - Müügiarve (EE) <br> - Projektiarve (EE)                                                                     | - Müügiarve loomine (EE) <br>- Projektiarve loomine (EE)                                                                                           | Eesti         | EUR-00023              |
| Soome elektrooniline arve (FI)   | Müügi- ja projektiarved Soome jaoks      | - Müügiarve (FI) <br>- Projektiarve loomine (FI)                                                          | - Müügiarve loomine (FI) <br>- Projektiarve loomine (FI)                                                                                           | Soome         | EUR-00023              |
| Prantsusmaa elektrooniline arve (FR)    | Müügi- ja projektiarved Prantsusmaa jaoks    | - UBL-i müügiarve FR <br> - UBL-i projektiarve FR <br> - UBL-i müügi kreeditarve FR <br>- UBL-i projekti kreeditarve FR | - Müügiarve loomine (FR) <br> - Projektiarve loomine (FR) <br>- Müügi kreeditarve loomine (FR) <br>- Projekti kreeditarve loomine (FR)         | Prantsusmaa          | EUR-00023              |
| Saksamaa elektrooniline arve (DE)    | Müügi- ja projektiarved Saksamaa jaoks      |- Müügiarve (DE) <br> - Projektiarve <DE>                                                                     | - Müügiarve loomine (DE) <br>- Projektiarve loomine (DE)                                                                                           | Saksamaa         | EUR-00023              |
| Norra elektrooniline arve (NO) | Müügi- ja projektiarved Norra jaoks       | - OIOUBL-i müügiarve <br>- OIOUBL-i projektiarve <br>- OIOUBL-i müügi kreeditarve <br>- OIOUBL-i projekti kreeditarve | - Müügiarve loomine (NO) <br>- Projektiarve loomine (NO) <br>- Müügi kreeditarve loomine (NO) <br>- Projekti kreeditarve loomine (NO)          | Norra          | EUR-00023<br> NO-00010 |
| Hispaania elektrooniline arve (ES)   | Müügi- ja projektiarved Hispaania jaoks        | - Müügiarve (ES) <br>- Projektiarve (ES)                                                                     | - Müügiarve loomine (ES) <br>- Projektiarve loomine (ES)                                                                                           | Hispaania           | EUR-00023 <br>ES-00025 |
| Itaalia elektrooniline arve (IT)   | Müügi- ja projektiarved Itaalia jaoks        | - (Eelversioon) Müügiarve (IT) <br> - Projektiarve (IT)                                                           | - Müügiarve <br> - Projektiarve                                                                                                                           | Itaalia           | EUR-00023 <br>IT-00036 |
| PEPPOL-i elektrooniline arve         | PEPPOL-i müügi- ja projektiarve loomine | - PEPPOL-i müügiarve <br>- PEPPOL-i projektiarve <br>- PEPPOL-i müügi kreeditarve <br> - PEPPOL-i projekti kreeditarve | - PEPPOL-i müügiarve loomine <br>- PEPPOL-i projektiarve loomine <br>- PEPPOL-i müügi kreeditarve loomine <br>- PEPPOL-i projekti kreeditarve loomine |                 | EUR-00023              |


## <a name="electronic-invoice-processing-in-finance-and-supply-chain-management"></a>Elektroonilise arve töötlemine rakendustes Finance ja Supply Chain Management

Töötlemise käigus teete järgmist.

1. Äridokumendi (arve) esitamine elektroonilise arvelduse lisandmooduli kaudu.
2. Edastuse käivituslogide kuvamine.

### <a name="submit-business-documents"></a>Äridokumentide edastamine

Tavapärase edastusprotsessi käigus on kliendi ja elektroonilise arvelduse lisandmooduli vaheline suhtlus kahesuunaline. Elektrooniliste dokumentide edastamise ajal on eesmärk täita kaks põhiülesannet.

1. Kõikide elektrooniliste dokumentide saatmine, mis on Finance'is edastamise ootel, millel on edastamiseks õige olek ning mis vastavad valikukriteeriumidele.
2. Elektroonilise arvelduse lisandmooduli tagastatud varem edastatud elektrooniliste dokumentide vastuse importimine rakendusse Finance. Pärast importimist vastused sõelutakse ja äridokumentide olekut värskendatakse vastavalt.

Äridokumente saate edastada kas käsitsi või oma graafikunõuete alusel.

1. Avage **Organisatsiooni haldus \> Perioodiline \> Elektroonilised dokumendid \> Edasta elektroonilised dokumendid**.
2. Mis tahes dokumendi esimese edastamise korral seadke suvandi **Dokumentide taasedastamine** väärtuseks alati **Ei**. Kui peate dokumendi teenuse kaudu uuesti edastama, seadke selle suvandi väärtuseks **Jah**.
3. Valige kiirkaardil **Kaasatavad kirjed** suvand **Filter**, et avada dialoogiboks **Päring**, kus saate luua päringu edastatavate dokumentide valimiseks.

![Elektrooniliste dokumentide edastamise dialoogiboks](media/e-invoicing-services-get-started-submission-form.png)

### <a name="filter-query"></a>Filtri päring

1. Sisestage dialoogiboksis **Päring** vahekaardil **Vahemik** filtrikriteeriumid, kasutades välju **Tabel**, **Tuletatud tabel**, **Väli** ja **Kriteeriumid**.
2. Valige **Lisa**, et lisada nii palju lisakriteeriume, kui teil on äridokumentide valimiseks vaja.

    ![Edastamise filtreerimiskriteeriumide seadistamine](media/e-invoicing-services-get-started-set-up-submission-filter-criteria.png)

3. Valige dialoogiboksi **Päring** sulgemiseks **OK**.
4. Valige **OK**, et edastada valitud äridokumendid elektroonilise arvelduse lisandmoodulile.

    > [!NOTE]
    > Esimesel dokumendi edastamise katsel teenuse kaudu palutakse teil kinnitada ühendus elektroonilise arvelduse lisandmooduliga. Valige **Elektroonilise dokumendi edastusteenusega ühendumiseks klõpsake siin**.
    >
    > ![Elektroonilise dokumendi edastusteenusega ühendumise teateaken](media/e-invoicing-services-get-started-dialog-form-connect-e-Invoicing-services.png)
    >
    > Kui ühendumine õnnestus, saate kinnitusteate.
    >
    > ![Elektroonilise arvelduse lisandmooduliga ühendumise kinnitus](media/e-invoicing-services-get-started-confirmation-connection-e-invoicing-services.png)

5. Sulgege dialoogiboks.

> [!NOTE]
> Pärast iga edastust kuvatakse tegevuskeskuses edastatud dokumentide arv.
>
> ![Tegevuskeskuse teated](media/e-invoicing-services-get-started-view-action-center-messages.png)

### <a name="submission-by-batch"></a>Edastamine partii alusel

Dokumentide käsitsi edastamise asemel saate edastusprotsessi automatiseerida ja taustal käivitada, võttes arvesse pakktöötluse konfigureeritud sagedust.

1. Valige dialoogiboksis **Elektrooniliste dokumentide edastamine** kiirkaardil **Käivita taustal** suvandi **Pakktöötlus** väärtuseks **Jah**.
2. Konfigureerige vahekaardil **Kordumine** pakktöötluse sagedus.

![Partii alusel edastamise seadistamine](media/e-invoicing-services-get-started-set-up-submission-batch.png)

### <a name="view-all-submission-logs"></a>Kõigi edastuslogide kuvamine

1. Avage **Organisatsiooni haldus \> Perioodiline \> Elektroonilised dokumendid \> Elektroonilise dokumendi edastuslogi**.
2. Valige väljal **Dokumendi tüüp** see dokumendi tüüp, mille järgi filtreerida.

    ![Dokumendi tüübi valimine, mille alusel kuvada edastuslogid](media/e-invoicing-services-get-started-select-document-type-for-viewing-submission-log.png)

    > [!IMPORTANT]
    > Veerus **Edastuse olek** toodud väärtus tähistab olekut, mis on seotud edastusprotsessi enda lõpetamisega. See näitab, kas RCS-is konfigureeritud tegevusvoog käitati lõpuni hoolimata sellest, kas elektrooniline dokument kinnitati või lükati tagasi. Veerus **Edastuse olek** olev väärtus ei tähista edastatud dokumendi olekut. Edastatud dokumendi olekut (st seda, kas dokument kinnitati või lükati tagasi) saate vaadata kiirkaardilt **Töötlemise tegevuslogi** edastuslogi üksikasjadest, nagu järgmisena kirjeldatakse.

3. Valige toimingupaanilt **Päringud \> Edastuse üksikasjad**.
4. Vaadake edastuslogi üksikasju.

    ![Edastuslogi üksikasjad](media/e-invoicing-services-get-started-view-submission-log-form.png)

Edastuslogis kuvatavad tulemused sõltuvad sellest, kuidas e-arvelduse funktsioon RCS-is seadistati. Kuid hoolimata seadistusest on edastuslogil alati kolm kiirkaarti.

- **Töötlemistegevused** – sellel kiirkaardil näidatakse RCS-is seadistatud funktsiooni versioonis konfigureeritud tegevuste käivituslogi. Veerus **Olek** on näha, kas tegevuse käivitamine õnnestus.
- **Tegevusfailid** – sellel kiirkaadil on vahefailid, mis loodi tegevuste käivitamise ajal. Saate valida **Kuva**, et fail alla laadida ja selle sisu vaadata.
- **Töötlemise tegevuslogi** – sellel kiirkaardil on kuvatud elektroonilise arvelduse lisandmooduli ja sihtveebiteenuse vahelise suhtluse tulemused. See näitab ka, mis veebiteenuse töötlemise käigus tagastati.

## <a name="related-topics"></a>Seotud teemad

- [Elektroonilise arvelduse lisandmooduli ülevaade](e-invoicing-service-overview.md)
- [Brasiilia elektroonilise arvelduse lisandmooduli kasutamise alustamine](e-invoicing-bra-get-started.md)
- [Mehhiko elektroonilise arvelduse lisandmooduli kasutamise alustamine](e-invoicing-mex-get-started.md)
- [Itaalia elektroonilise arvelduse lisandmooduli kasutamise alustamine](e-invoicing-ita-get-started.md)
- [Elektroonilise arvelduse lisandmooduli seadistamine](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]