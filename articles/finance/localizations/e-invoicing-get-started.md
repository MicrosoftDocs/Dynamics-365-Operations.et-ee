---
title: Elektroonilise arvelduse lisandmooduli kasutamise alustamine
description: Sellest teemast leiate teabe, mis aitab teil rakendustes Microsoft Dynamics 365 Finance ja Dynamics 365 Supply Chain Management elektroonilise arvelduse lisandmoodulit kasutama hakata.
author: gionoder
manager: AnnBe
ms.date: 02/03/2021
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
ms.openlocfilehash: 07954c5c96f390bc651794f8b6c61f2a1a17ab8b
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111216"
---
# <a name="get-started-with-the-electronic-invoicing-add-on"></a>Elektroonilise arvelduse lisandmooduli kasutamise alustamine

[!include [banner](../includes/banner.md)]

Sellest teemast leiate teabe, mis aitab teil elektroonilise arvelduse lisandmoodulit kasutama hakata.

Järgmises tabelis on toodud elektroonilise arvelduse funktsioonid ja äridokumendid, mille puhul neid saab rakendada.

| Funktsiooni nimi                         | Äridokument |
|--------------------------------------|-------------------|
| Austria elektroonilised arved (AT)    | <p>Müügiarve</p><p>Projektiarve</p> |
| Belgia elektrooniline arve (BE)      | <p>Müügiarve</p><p>Projektiarve</p> |
| Brasiilia NF-e (BR)                  | <p>Rahandusdokumentide 55. mudel</p><p>Paranduskiri</p> |
| Brasiilia NFS-e ABRASF Curitiba (BR) | Teenuse finantsdokument |
| Brasiilia NFS-e São Paulo (BR)       | Teenuse finantsdokument |
| Taani elektrooniline arve (DK)       | <p>Müügiarve</p><p>Projektiarve</p> |
| Egiptuse elektrooniline arve (EG)     | <p>Müügiarve</p><p>Projektiarve</p> |
| Eesti elektrooniline arve (EE)     | <p>Müügiarve</p><p>Projektiarve</p> |
| Soome elektrooniline arve (FI)       | <p>Müügiarve</p><p>Projektiarve</p> |
| Prantsusmaa elektrooniline arve (FR)       | <p>Müügiarve</p><p>Projektiarve</p> |
| Saksamaa elektrooniline arve (DE)       | <p>Müügiarve</p><p>Projektiarve</p> |
| FatturaPA (IT)                       | <p>Müügiarve</p><p>Projektiarve</p> |
| Mehhiko CFDI Interfactura (MX)       | <p>Müügiarve</p><p>Saateleht</p><p>Varude ülekanne</p><p>Maksetoetus</p> |
| Hollandi elektrooniline arve (NL)        | <p>Müügiarve</p><p>Projektiarve</p> |
| Norra elektrooniline arve (NO)    | <p>Müügiarve</p><p>Projektiarve</p> |
| Hispaania elektrooniline arve (ES)      | <p>Müügiarve</p><p>Projektiarve</p> |
| PEPPOL-i elektrooniline arve            | <p>Müügiarve</p><p>Projektiarve</p> |

## <a name="prerequisites"></a>Eeltingimused

Enne selles teemas kirjeldatud protseduuride lõpetamist peavad täidetud olema järgmised eeltingimused.

- Konfigureerige oma teenust Regulatory Configuration Service (RCS) ja Microsofti keskkonda Dynamics 365 Finance või Dynamics 365 Supply Chain Management nii, et saaksite elektroonilise arvelduse lisandmoodulisse edastada.
- Looge teenusekeskkond ja avaldage see elektroonilise arvelduse lisandmoodulis. Lisateavet vt teemast [Elektroonilise arvelduse lisandmooduli teenuse haldusega alustamine](e-invoicing-get-started-service-administration.md).
- Looge ühendatud rakendus. Lisateavet vt teemast [Elektroonilise arvelduse lisandmooduli teenuse haldusega alustamine](e-invoicing-get-started-service-administration.md).
- Looge oma organisatsioonile konfiguratsioonipakkuja. Lisateavet vt teemast [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider"></a>Microsofti konfiguratsioonipakkujalt elektroonilise arvelduse funktsiooni importimine 

1. Logige oma teenuse Regulatory Configuration Service (RCS) kontole sisse.
2. Valige tööruumi **Globaliseerimisfunktsioon** jaotises **Funktsioonid** paan **E-arveldus**.
3. Valige **Impordi** ja seejärel **Sünkrooni**.
4. Filtreerige veerg **Konfiguratsioonipakkuja** terminiga **Microsoft**.
5. Valige selle teema alguses olevast tabelist elektroonilise arvelduse funktsiooni nimi ja seejärel valige käsk **Impordi**.

## <a name="create-an-electronic-invoicing-feature-under-your-organization-provider"></a>Organisatsiooni pakkuja all elektroonilise arvelduse funktsiooni loomine

1. Valige RCS-is tööruumi **Globaliseerimisfunktsioon** jaotises **Funktsioonid** paan **E-arveldus**.
2. Valige **Lisa** > **Olemasoleva funktsiooni põhjal** ja sisestage väljale **Nimi** elektroonilise arvelduse funktsiooni nimi.
3. Sisestage väljale **Kirjeldus** funktsiooni kirjeldus.
4. Valige väljal **Põhifunktsioon** Microsofti konfiguratsioonipakkujalt imporditud elektroonilise arvelduse funktsioon.
5. Valige **Loo funktsioon**.

## <a name="configure-the-electronic-invoicing-feature"></a>Elektroonilise arvelduse funktsiooni konfigureerimine

Olenevalt riigist või regioonist võib elektroonilise arvelduse funktsioon vajada täiendavat konfiguratsiooni. Konkreetsete etappide kohta vt teavet teie riigi või regiooni jaoks saadaolevast dokumentatsioonist „Alustamine“.

## <a name="configure-the-application-setup"></a>Rakenduse seadistuse konfigureerimine

1. Valige loodud elektroonilise arvelduse funktsioon.
2. Kontrollige vahekaardil **Versioon**, et oleks valitud versioon **Mustand**.
3. Tehke vahekaardil **Seadistused** valik **Rakenduse seadistus**.

    > [!NOTE]
    > Kontrollige, kas teie organisatsioon on määratud **aktiivseks** konfiguratsioonipakkujaks. Lisateavet vt teemast [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

4. Valige **Funktsiooni seadistus** ja seejärel valige **Ühendatud rakendus**.
5. Valige jaotises **Elektroonilise dokumendi tüübid** käsk **Lisa**.
6. Valige ja sisestage iga äridokumendi jaoks, mida see funktsioon toetab, väärtus **Tabeli nimi** vastavalt järgmisele tabelile.

    | Funktsiooni nimi                         | Äridokument | Tabeli nimi |
    |--------------------------------------|-------------------|------------|
    | Austria elektroonilised arved (AT)    | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarvete tööleht</p><p>Projektiarve</p> |
    | Belgia elektrooniline arve (BE)      | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarvete tööleht</p><p>Projektiarve</p> |
    | Brasiilia NF-e (BR)                  | <p>Fiskaaldokument</p><p>Paranduskiri</p> | Fiskaaldokument |
    | Brasiilia NFS-e ABRASF Curitiba (BR) | Teenuse finantsdokument | Fiskaaldokument |
    | Brasiilia NFS-e São Paulo (BR)       | Teenuse finantsdokument | Fiskaaldokument |
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

7. Valige ja sisestage iga äridokumendi jaoks, mida see funktsioon toetab, väärtus **Kontekst** vastavalt järgmisele tabelile.

    | Funktsiooni nimi                         | Äridokument | Kontekst |
    |--------------------------------------|-------------------|---------|
    | Austria elektroonilised arved (AT)    | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarve kontekstimudel – kliendiarve kontekst</p><p>Kliendiarve kontekstimudel – projektiarve kontekst</p> |
    | Belgia elektrooniline arve (BE)      | <p>Müügiarve</p><p>Projektiarve</p> | <p>Kliendiarve kontekstimudel – kliendiarve kontekst</p><p>Kliendiarve kontekstimudel – projektiarve kontekst</p> |
    | Brasiilia NF-e (BR)                  | <p>Fiskaaldokument</p><p>Paranduskiri</p> | <p>Kliendiarve kontekstimudel – finantsdokumendi kontekst</p><p>Kliendiarve kontekstimudel – FD paranduskirja kontekst</p> |
    | Brasiilia NFS-e ABRASF Curitiba (BR) | Teenuse finantsdokument| Kliendiarve kontekstimudel – finantsdokumendi kontekst |
    | Brasiilia NFS-e São Paulo (BR)       | Teenuse finantsdokument| Kliendiarve kontekstimudel – finantsdokumendi kontekst |
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

8. Valige ja sisestage iga äridokumendi jaoks, mida see funktsioon toetab, väärtus **Äridokumentide vastendus** vastavalt järgmisele tabelile.

    | Funktsiooni nimi                         | Äridokument | Äridokumendi kaardistus |
    |--------------------------------------|-------------------|---------------------------|
    | Austria elektroonilised arved (AT)    | <p>Müügiarve</p><p>Projektiarve</p> | <p>Arvemudeli vastendus – kliendiarve</p><p>Arvemudeli vastendus – projektiarve</p> |
    | Belgia elektrooniline arve (BE)      | <p>Müügiarve</p><p>Projektiarve</p> | <p>Arvemudeli vastendus – kliendiarve</p><p>Arvemudeli vastendus – projektiarve</p> |
    | Brasiilia NF-e (BR)                  | <p>Fiskaaldokument</p><p>Paranduskiri</p> | <p>Finantsdokumendi vastendus – finantsdokumendi vastendus</p><p>Finantsdokumendi vastendus – paranduskirja vastendus</p> |
    | Brasiilia NFS-e ABRASF Curitiba (BR) | Teenuse finantsdokument | Finantsdokumendi vastendus – finantsdokumendi vastendus |
    | Brasiilia NFS-e São Paulo (BR)       | Teenuse finantsdokument | Finantsdokumendi vastendus – finantsdokumendi vastendus |
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

Olenevalt riigist või regioonist võib elektroonilise arvelduse funktsioon vajada täiendavat konfiguratsiooni. Konkreetsete etappide kohta vt teavet teie riigi või regiooni jaoks saadaolevast dokumentatsioonist „Alustamine“.

## <a name="deploy-the-electronic-invoicing-feature"></a>Elektroonilise arvelduse funktsiooni juurutamine

1. Valige vahekaardil **Versioonid** see elektroonilise arvelduse funktsiooni versioon, mida soovite juurutada.
2. Valige **Muuda olekut** \> **Lõpule viidud**.
3. Valige **Muuda olekut** \> **Avalda**.
4. Valige **Juuruta**.
5. Määrake suvandi **Juuruta ühendatud rakenduses** väärtuseks **Jah**.
6. Valige lehel **Ühendatud rakendus** ühendus, mis on seotud teie teenuse Finance või Supply Chain Management eksemplariga.
7. Määrake suvandi **Juuruta teenusekeskkonnas** väärtuseks **Jah**.
8. Valige väljal **Teenusekeskkond** elektroonilise arvelduse lisandmooduli teenusekeskkond, kus te soovite elektroonilise arvelduse funktsiooni juurutada.
9. Valige väljal **Alguskuupäev** kuupäev, millal peab elektroonilise arvelduse funktsioon elektroonilise arvelduse lisandmoodulis jõustuma.
10. Valige nupp **OK**.

## <a name="turn-on-the-electronic-invoicing-feature-in-finance-or-supply-chain-management"></a>Teenuses Finance või Supply Chain Management elektroonilise arvelduse funktsiooni sisselülitamine

1. Logige teenusesse Finance või Supply Chain Management sisse ja veenduge, et oleksite õiges juriidilises isikus.
2. Avage **Organisatsiooni haldus** \> **Seadistus** \> **Elektroonilise dokumendi parameetrid**.
3. Valige vahekaardil **Funktsioonid** funktsiooniviide või -viited, mis on toodud järgmises tabelis, et teenuses Finance või Supply Chain Management elektroonilise arvelduse funktsioon sisse lülitada.

    | Funktsiooni nimi                         | Riik/regioon  | Funktsiooni viide |
    |--------------------------------------|-----------------|-------------------|
    | Austria elektroonilised arved (AT)    | Austria         | EUR-00023 |
    | Belgia elektrooniline arve (BE)      | Belgia         | EUR-00023 |
    | Brasiilia NF-e (BR)                  | Brasiilia          | BR-00053 |
    | Brasiilia NFS-e ABRASF Curitiba (BR) | Brasiilia          | BR-00095 |
    | Brasiilia NFS-e São Paulo (BR)       | Brasiilia          | BR-00095 |
    | Taani elektrooniline arve (DK)       | Taani         | <p>EUR-00023</p><p>DK-00001</p> |
    | Hollandi elektrooniline arve (NL)        | Holland | EUR-00023 |
    | Egiptuse elektrooniline arve (EG)     | Egiptus           | EG-00008 |
    | Eesti elektrooniline arve (EE)     | Eesti         | EUR-00023 |
    | Soome elektrooniline arve (FI)      | Soome         | EUR-00023 |
     Prantsusmaa elektrooniline arve (FR)       | Prantsusmaa           | EUR-00023 |
    | Saksamaa elektrooniline arve (DE)       | Saksamaa         | EUR-00023 |
    | Mehhiko CFDI Interfactura (MX)       | Mehhiko          | <p>MX-00010</p><p>MX-00016</p> |
    | Norra elektrooniline arve (NO)    | Norra          | <p>EUR-00023</p><p>NO-00010</p> |
    | Hispaania elektrooniline arve (ES)      | Hispaania           | <p>EUR-00023</p><p>ES-00025</p> |
    | Itaalia elektrooniline arve (IT)      | Itaalia           | <p>EUR-00023</p><p>IT-00036</p> |
    | PEPPOL-i elektrooniline arve            | Euroopa          | EUR-00023 |

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

Olenevalt riigist või regioonist võib elektroonilise arvelduse funktsioon vajada täiendavat konfiguratsiooni. Konkreetsete etappide kohta vt teavet teie riigi või regiooni jaoks saadaolevast dokumentatsioonist „Alustamine“.

## <a name="related-topics"></a>Seotud dokumendid

- [Elektroonilise arvelduse lisandmooduli ülevaade](e-invoicing-service-overview.md)
- [Brasiilia elektroonilise arvelduse lisandmooduli kasutamise alustamine](e-invoicing-bra-get-started.md)
- [Mehhiko elektroonilise arvelduse lisandmooduli kasutamise alustamine](e-invoicing-mex-get-started.md)
- [Itaalia elektroonilise arvelduse lisandmooduli kasutamise alustamine](e-invoicing-ita-get-started.md)
- [Kliendi elektroonilised arved Egiptuses](emea-egy-e-invoices.md)
