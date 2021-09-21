---
title: Elektroonilise arveldusega alustamine
description: Sellest teemast leiate teabe, mis aitab teil Elektroonilise arveldusega alustada Microsoft Dynamics 365 Finance -is ja Dynamics 365 Supply Chain Management.
author: gionoder
ms.date: 08/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 3ba0b68ee61b130b8d0304d0bac6d1d720af8139
ms.sourcegitcommit: baf82100f0aa7d5f5f47c7f54bc155d8a07beab5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/31/2021
ms.locfileid: "7463830"
---
# <a name="get-started-with-electronic-invoicing"></a>Elektroonilise arveldusega alustamine

[!include [banner](../includes/banner.md)]

Sellest teemast leiate teabe, mis aitab teil alustada elektroonilise arveldusega. See teema juhib teid läbi Regulatory Configuration Services (RCS) ja Dynamics 365 Finance ning pakub samme, mida peate järgima, et esitada äridokumente ja ülevaateid töötlustulemustest.

## <a name="prerequisites"></a>Eeltingimused

Enne selles teemas kirjeldatud protseduuride lõpetamist peavad täidetud olema järgmised eeltingimused.

- Konfigureerige oma Microsoft Dynamics Lifecycle Services (LCS), regulatiivse konfiguratsiooni teenus (RCS) ja teie Microsoft Dynamics 365 Finance või Dynamics 365 Supply Chain Management keskkond. Lisateavet vt teemast [Elektroonilise arvelduse teenuse haldusega alustamine](e-invoicing-get-started-service-administration.md).
- Looge oma organisatsioonile konfiguratsioonipakkuja. Lisateavet vt teemast [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider"></a>Microsofti konfiguratsioonipakkujalt elektroonilise arvelduse funktsiooni importimine 

1. Logige oma teenuse Regulatory Configuration Service (RCS) kontole sisse.
2. Tööruumis **Globaliseerimisfunktsioonid** jaotises **Funktsioonid** valige paan **Elektrooniline arveldus** .
3. Valige **Impordi** ja seejärel **Sünkrooni**.
4. Filtreerige veerg **Konfiguratsioonipakkuja** terminiga **Microsoft**.
5. Valige tabelist elektroonilise arveldamise funktsiooni nimi ja seejärel valige käsk **Impordi**.

## <a name="create-an-electronic-invoicing-feature-under-your-organization-provider"></a>Organisatsiooni pakkuja all elektroonilise arvelduse funktsiooni loomine

1. RCS-i jaotises **Funktsioonid** tööruumis **Globaliseerimisfunktsioonid** valige paan **Elektrooniline arveldus**.
2. Valige **Lisa** > **Olemasoleva funktsiooni põhjal** ja sisestage väljale **Nimi** elektroonilise arvelduse funktsiooni nimi.
3. Sisestage väljale **Kirjeldus** funktsiooni kirjeldus.
4. Valige väljal **Põhifunktsioon** Microsofti konfiguratsioonipakkujalt imporditud elektroonilise arvelduse funktsioon.
5. Valige **Loo funktsioon**.

## <a name="country-specific-configuration-for-electronic-invoicing-feature"></a>Riigipõhine konfiguratsioon Elektroonilise arvelduse funktsioonile

Olenevalt riigist või regioonist võib elektroonilise arvelduse funktsioon vajada spetsiifilist konfiguratsiooni. 

Konkreetsete etappide kohta vt teavet teie riigi või regiooni jaoks saadaolevast dokumentatsioonist „Alustamine“.

## <a name="import-the-model-mapping-configurations-from-electronic-reporting"></a>Impordi mudelikaardistamise konfiguratsioon elektroonilisest aruandlusest

1. Valige RCS-is **Elektroonilise aruandluse** tööruum.
2. **Microsoft** konfiguratsiooni pakkujate loendist valige **Hoidlad**.
3. Valige **Globaalne** ja klõpsake tegevuspaanil, valige **Ava**.
4. Importige mudeli kaardistamise konfiguratsioonid vastavalt järgmisele tabelile funktsiooni nime järgi.

| Funktsiooni nimi                         | Mudelikaardistamise konfiguratsioon |
|--------------------------------------|-----------------------------|
| Austria elektroonilised arved (AT)    | <p>Kliendiarve kontekstimudel</p><p>Arve mudel</p> |
| Belgia elektrooniline arve (BE)      | <p>Kliendiarve kontekstimudel</p><p>Arve mudel</p> |
| Brasiilia NF-e (BR)                  | <p>Kliendiarve kontekstimudel</p><p>Finantsdokumendid</p><p>Vastusesõnumi mudel</p> |
| Brasiilia NFS-e ABRASF Curitiba (BR) | <p>Kliendiarve kontekstimudel</p><p>Finantsdokumendid</p><p>Vastusesõnumi mudel</p> |
| Taani elektrooniline arve (DK)       | <p>Kliendiarve kontekstimudel</p><p>Arve mudel</p> |
| Egiptuse elektrooniline arve (EG)     | <p>Kliendiarve kontekstimudel</p><p>Arve mudel</p><p>Vastusesõnumi mudel</p> |
| Eesti elektrooniline arve (EE)     | <p>Kliendiarve kontekstimudel</p><p>Arve mudel</p> |
| Soome elektrooniline arve (FI)       | <p>Kliendiarve kontekstimudel</p><p>Arve mudel</p> |
| Prantsusmaa elektrooniline arve (FR)       | <p>Kliendiarve kontekstimudel</p><p>Arve mudel</p> |
| Saksamaa elektrooniline arve (DE)       | <p>Kliendiarve kontekstimudel</p><p>Arve mudel</p> |
| FatturaPA (IT)                       | <p>Kliendiarve kontekstimudel</p><p>Arve mudel</p> |
| Mehhiko CFDI Interfactura (MX)       | <p>Kliendiarve kontekstimudel</p><p>Arve mudel</p><p>Vastusesõnumi mudel</p> |
| Hollandi elektrooniline arve (NL)        | <p>Kliendiarve kontekstimudel</p><p>Arve mudel</p> |
| Norra elektrooniline arve (NO)    | <p>Kliendiarve kontekstimudel</p><p>Arve mudel</p> |
| Hispaania elektrooniline arve (ES)      | <p>Kliendiarve kontekstimudel</p><p>Arve mudel</p> |
| PEPPOL-i elektrooniline arve            | <p>Kliendiarve kontekstimudel</p><p>Arve mudel</p> |


## <a name="configure-the-application-setup"></a>Rakenduse seadistuse konfigureerimine

1. Valige loodud elektroonilise arvelduse funktsioon.
2. Tehke vahekaardil **Seadistused** valik **Rakenduse seadistus**.
3. Valige väljal **Ühendatud rakendus** ühendus, mis on seotud teie finants või Supply Chain Management eksemplariga.
4. Valige jaotises **Elektroonilise dokumendi tüübid** käsk **Lisa**.
5. Vali ja sisesta **Tabeli nimi** väärtus vastavalt järgmisele tabelile.

    | Funktsiooni nimi                         | Äridokument | Tabeli nimi |
    |--------------------------------------|-------------------|------------|
    | Austria elektroonilised arved (AT)    | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarvete tööleht</p><p>Projektiarve</p> |
    | Belgia elektrooniline arve (BE)      | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarvete tööleht</p><p>Projektiarve</p> |
    | Brasiilia NF-e (BR)                  | <p>Fiskaaldokument</p><p>Paranduskiri</p> | Fiskaaldokument |
    | Brasiilia NFS-e ABRASF Curitiba (BR) | Teenuse finantsdokument | Fiskaaldokument |
    | Taani elektrooniline arve (DK)       | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarvete tööleht</p><p>Projektiarve</p> |
    | Egiptuse elektrooniline arve (EG)     | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarvete tööleht</p><p>Projektiarve</p> |
    | Eesti elektrooniline arve (EE)     | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarvete tööleht</p><p>Projektiarve</p> |
    | Soome elektrooniline arve (FI)       | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarvete tööleht</p><p>Projektiarve</p> |
    | Prantsusmaa elektrooniline arve (FR)       | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarvete tööleht</p><p>Projektiarve</p> |
    | Saksamaa elektrooniline arve (DE)       | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarvete tööleht</p><p>Projektiarve</p> |
    | FatturaPA (IT)                       | <p>Müügiarve</p><p>Projektiarve | <p>Kliendiarvete tööleht</p><p>Projektiarve</p> |
    | Mehhiko CFDI Interfactura (MX)       | <p>Müügiarve</p><p>Saateleht</p><p>Varude ülekanne</p><p>Maksetoetus</p> | Kliendiarvete tööleht |
    | Hollandi elektrooniline arve (NL)        | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarvete tööleht</p><p>Projektiarve</p> |
    | Norra elektrooniline arve (NO)    | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarvete tööleht</p><p>Projektiarve</p> |
    | Hispaania elektrooniline arve (ES)      | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarvete tööleht</p><p>Projektiarve</p> |
    | PEPPOL-i elektrooniline arve            | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarvete tööleht</p><p>Projektiarve</p> |

6. Iga tabeli nime jaoks, mille loote, valige ja sisestage kontekstiväärtus vastavalt järgnevale tabelile.

    | Funktsiooni nimi                         | Äridokument | Kontekst |
    |--------------------------------------|-------------------|---------|
    | Austria elektroonilised arved (AT)    | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarve kontekstimudel – kliendiarve kontekst</p><p>Kliendiarve kontekstimudel – projektiarve kontekst</p> |
    | Belgia elektrooniline arve (BE)      | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarve kontekstimudel – kliendiarve kontekst</p><p>Kliendiarve kontekstimudel – projektiarve kontekst</p> |
    | Brasiilia NF-e (BR)                  | <p>Fiskaaldokument</p><p>Paranduskiri</p> | <p>Kliendiarve kontekstimudel – finantsdokumendi kontekst</p><p>Kliendiarve kontekstimudel – FD paranduskirja kontekst</p> |
    | Brasiilia NFS-e ABRASF Curitiba (BR) | Teenuse finantsdokument| Kliendiarve kontekstimudel – finantsdokumendi kontekst |
    | Taani elektrooniline arve (DK)       | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarve kontekstimudel – kliendiarve kontekst</p><p>Kliendiarve kontekstimudel – projektiarve kontekst</p> |
    | Egiptuse elektrooniline arve (EG)     | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarve kontekstimudel – kliendiarve kontekst</p><p>Kliendiarve kontekstimudel – projektiarve kontekst</p> |
    | Eesti elektrooniline arve (EE)     | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarve kontekstimudel – kliendiarve kontekst</p><p>Kliendiarve kontekstimudel – projektiarve kontekst</p> |
    | Soome elektrooniline arve (FI)       | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarve kontekstimudel – kliendiarve kontekst</p><p>Kliendiarve kontekstimudel – projektiarve kontekst</p> |
    | Prantsusmaa elektrooniline arve (FR)       | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarve kontekstimudel – kliendiarve kontekst</p><p>Kliendiarve kontekstimudel – projektiarve kontekst</p> |
    | Saksamaa elektrooniline arve (DE)       | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarve kontekstimudel – kliendiarve kontekst</p><p>Kliendiarve kontekstimudel – projektiarve kontekst</p> |
    | FatturaPA (IT)                       | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarve kontekstimudel – kliendiarve kontekst</p><p>Kliendiarve kontekstimudel – projektiarve kontekst</p> |
    | Mehhiko CFDI Interfactura (MX)       | <p>Müügiarve</p><p>Saateleht</p><p>Varude ülekanne</p><p>Maksetoetus</p> | Kliendiarve kontekstimudel – kliendiarve kontekst |
    | Hollandi elektrooniline arve (NL)        | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarve kontekstimudel – kliendiarve kontekst</p><p>Kliendiarve kontekstimudel – projektiarve kontekst</p> |
    | Norra elektrooniline arve (NO)    | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarve kontekstimudel – kliendiarve kontekst</p><p>Kliendiarve kontekstimudel – projektiarve kontekst</p> |
    | Hispaania elektrooniline arve (ES)      | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarve kontekstimudel – kliendiarve kontekst</p><p>Kliendiarve kontekstimudel – projektiarve kontekst</p> |
    | PEPPOL-i elektrooniline arve            | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarve kontekstimudel – kliendiarve kontekst</p><p>Kliendiarve kontekstimudel – projektiarve kontekst</p> |

7. Iga tabeli nime ja konteksti jaoks valige ja sisestage äridokumendi kaardistav väärtus vastavalt järgmisele tabelile.

    | Funktsiooni nimi                         | Äridokument | Äridokumendi kaardistus |
    |--------------------------------------|-------------------|---------------------------|
    | Austria elektroonilised arved (AT)    | <p>Müügiarve</p><p>Projektiarve</p> | <p>Arvemudeli vastendus – kliendiarve</p><p>Arvemudeli vastendus – projektiarve</p> |
    | Belgia elektrooniline arve (BE)      | <p>Müügiarve</p><p>Projektiarve</p> | <p>Arvemudeli vastendus – kliendiarve</p><p>Arvemudeli vastendus – projektiarve</p> |
    | Brasiilia NF-e (BR)                  | <p>Fiskaaldokument</p><p>Paranduskiri</p> | <p>Finantsdokumendi vastendus – finantsdokumendi vastendus</p><p>Finantsdokumendi vastendus – paranduskirja vastendus</p> |
    | Brasiilia NFS-e ABRASF Curitiba (BR) | Teenuse finantsdokument | Finantsdokumendi vastendus – finantsdokumendi vastendus |
    | Taani elektrooniline arve (DK)       | <p>Müügiarve</p><p>Projektiarve</p> | <p>Arvemudeli vastendus – kliendiarve</p><p>Arvemudeli vastendus – projektiarve</p> |
    | Egiptuse elektrooniline arve (EG)     | <p>Müügiarve</p><p>Projektiarve</p> | <p>Arvemudeli vastendus – kliendiarve</p><p>Arvemudeli vastendus – projektiarve</p> |
    | Eesti elektrooniline arve (EE)     | <p>Müügiarve</p><p>Projektiarve</p> | <p>Arvemudeli vastendus – kliendiarve</p><p>Arvemudeli vastendus – projektiarve</p> |
    | Soome elektrooniline arve (FI)       | <p>Müügiarve</p><p>Projektiarve</p> | <p>Arvemudeli vastendus – kliendiarve</p><p>Arvemudeli vastendus – projektiarve</p> |
    | Prantsusmaa elektrooniline arve (FR)       | <p>Müügiarve</p><p>Projektiarve</p> | <p>Arvemudeli vastendus – kliendiarve</p><p>Arvemudeli vastendus – projektiarve</p> |
    | Saksamaa elektrooniline arve (DE)       | <p>Müügiarve</p><p>Projektiarve</p> | <p>Arvemudeli vastendus – kliendiarve</p><p>Arvemudeli vastendus – projektiarve</p> |
    | FatturaPA (IT)                       | <p>Müügiarve</p><p>Projektiarve</p> | <p>Arvemudeli vastendus – kliendiarve</p><p>Arvemudeli vastendus – projektiarve</p> |
    | Mehhiko CFDI Interfactura (MX)       | <p>Müügiarve</p><p>Saateleht</p><p>Varude ülekanne</p><p>Maksetoetus</p> | Arvemudeli vastendus – kliendiarve |
    | Hollandi elektrooniline arve (NL)        | <p>Müügiarve</p><p>Projektiarve</p> | <p>Arvemudeli vastendus – kliendiarve</p><p>Arvemudeli vastendus – projektiarve</p> |
    | Norra elektrooniline arve (NO)    | <p>Müügiarve</p><p>Projektiarve</p> | <p>Arvemudeli vastendus – kliendiarve</p><p>Arvemudeli vastendus – projektiarve</p> |
    | Hispaania elektrooniline arve (ES)      | <p>Müügiarve</p><p>Projektiarve</p> | <p>Arvemudeli vastendus – kliendiarve</p><p>Arvemudeli vastendus – projektiarve</p> |
    | PEPPOL-i elektrooniline arve            | <p>Müügiarve</p><p>Projektiarve</p> | <p>Arvemudeli vastendus – kliendiarve</p><p>Arvemudeli vastendus – projektiarve</p> |


## <a name="country-specific-configuration-of-application-setup"></a>Riigispetsiifiline rakenduse häälestuse konfiguratsioon

Olenevalt riigist või regioonist võib rakenduse häälestus nõuda spetsiifilist konfiguratsiooni. 

Konkreetsete etappide kohta vt teavet teie riigi või regiooni jaoks saadaolevast dokumentatsioonist „Alustamine“.

## <a name="deploy-the-electronic-invoicing-feature-to-service-environment"></a>Elektroonilise arveldamise funktsiooni juurutamine teenuse keskkonda

1. Valige vahekaardil **Versioonid** see elektroonilise arvelduse funktsiooni versioon, mida soovite juurutada.
2. Valige **Muuda olekut** \> **Lõpule viidud**.
3. Valige **Muuda olekut** \> **Avalda**.
4. Valige **Juuruta**.
5. Määrake **Juuruta ühendatud rakenduses** väärtuseks **Jah**.
6. Määrake suvandi **Juuruta teenusekeskkonnas** väärtuseks **Jah**.
7. Väljal **Teenusekeskkond** valige elektroonilise arvelduse teenusekeskkond, kus te soovite elektroonilise arvelduse funktsiooni juurutada.
8. Väljal **Alguskuupäev** valige kuupäev, millal peab elektroonilise arvelduse funktsioon elektroonilise arvelduses jõustuma.
9. Valige nupp **OK**.

## <a name="deploy-the-electronic-invoicing-feature-to-connected-application"></a>Elektroonilise arveldamise funktsiooni juurutamine Ühendatud rakendusse

1. Vahekaardil **Versioonid** valige see elektroonilise arvelduse funktsiooni versioon, mida soovite juurutada.
2. Valige **Juuruta**.
3. Määrake suvandi **Juuruta ühendatud rakenduses** väärtuseks **Jah**.
4. Väljal **Ühendatud rakendus** valige ühendus, mis on seotud teie finants või Supply Chain Management eksemplariga.
5. Määrake **Juuruta teenusekeskkonnas** väärtuseks **Ei**.
6. Valige nupp **OK**.

## <a name="turn-on-the-electronic-invoicing-feature-in-finance-or-supply-chain-management"></a>Teenuses Finance või Supply Chain Management elektroonilise arvelduse funktsiooni sisselülitamine

1. Logige teenusesse Finance või Supply Chain Management sisse ja veenduge, et oleksite õiges juriidilises isikus.
2. Avage **Organisatsiooni haldus** \> **Seadistus** \> **Elektroonilise dokumendi parameetrid**.
3. Vahekaardil **Funktsioonid** valige riigi-/regiooniomane funktsioon, et lülitada sisse Finance or Supply Chain Management jaoks. Järgmine tabel annab elektroonilise arveldamise funktsioonide loendi, mis on saadaval konkreetsete riikide/regioonide jaoks. 

    | Funktsiooni nimi                                          | Riik/regioon  |
    |-------------------------------------------------------|-----------------|
    | Austria elektroonilised arved (AT)                     | Austria         |
    | Belgia elektrooniline arve (BE)                       | Belgia         |
    | Mehhiko CFDI elektrooniline arve (MX)                  | Mehhiko          |
    | Taani elektrooniline arve (DK)                        | Taani         |
    | Hollandi elektrooniline arve (NL)                         | Holland |
    | Egiptuse elektrooniline arve (EG)                      | Egiptus           |
    | Eesti elektrooniline arve (EE)                      | Eesti         |
    | Soome elektrooniline arve (FI)                       | Soome         |
    | Prantsusmaa elektrooniline arve (FR)                        | Prantsusmaa          |
    | Saksamaa elektrooniline arve (DE)                        | Saksamaa         |
    | Itaalia elektrooniline arve (IT)                       | Itaalia           |
    | NF-e föderaalne – Brasiilia elektrooniline arve (BR)      | Brasiilia          |
    | NFS-e – Brasiilia teenuse (linna) elektrooniline arve   | Brasiilia          |
    | Norra elektrooniline arve (NO)                     | Norra          |
    | PEPPOL-i elektrooniline arve                             | Üldine          |
    | Hispaania elektrooniline arve (ES)                       | Hispaania           |

4. Valige käsk **Salvesta**.

## <a name="issue-electronic-invoices"></a>Elektrooniliste arvete väljastamine

1. Avage **Organisatsiooni haldus** \> **Perioodiline** \> **Elektroonilised dokumendid** \> **Edasta elektroonilised dokumendid**.
2. Valige kiirkaardil **Kaasatavad kirjed** suvand **Filter**.
3. Päringufiltrile tabeli nime lisamiseks valige käsk **Lisa**.
4. Valige arveid hõlmav tabel.

    > [!NOTE]
    > Tabeli nimi peab olema selle teema varasemas jaotises [Rakenduse seadistuse konfigureerimine](#configure-the-application-setup) olevas tabelis loetletud.

5. Valige tabelis välja nimi, mille puhul soovite päringu esitada.
6. Sisestage päringukriteeriumite jaoks tabeli nimi ja välja nimi.
7. Korrake 5. ja 6. etappi, et lisada päringule veel välju ja kriteeriume, seejärel valige **OK**.
8. Valige nupp **OK**.

## <a name="view-submission-logs"></a>Edastuslogide kuvamine

1. Avage **Organisatsiooni haldus** \> **Perioodiline** \> **Elektroonilised dokumendid** \> **Elektroonilise dokumendi edastuslogi**.
2. Valige väljal **Dokumendi tüüp** arveid hõlmav tabel.

    > [!NOTE]
    > Tabeli nimi peab olema selle teema varasemas jaotises [Rakenduse seadistuse konfigureerimine](#configure-the-application-setup) olevas tabelis loetletud.

3. Valige ruudustikust arve ja seejärel valige **Päringud** \> **Edastuse üksikasjad**.


## <a name="related-topics"></a>Seotud dokumendid

- [Elektroonilise arvelduse ülevaade](e-invoicing-service-overview.md)
- [Elektroonilise arvelduse lisandmooduli teenusehalduse kasutamise alustamine](e-invoicing-get-started-service-administration.md)
- [Alustage elektroonilise arveldusega Brasiilias](e-invoicing-bra-get-started.md)
- [Alustage elektroonilise arveldusega Mehhikos](e-invoicing-mex-get-started.md)
- [Elektroonilise arvelduse lisandmooduli kasutamise alustamine Itaalias](e-invoicing-ita-get-started.md)
- [Kliendi elektroonilised arved Egiptuses](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
