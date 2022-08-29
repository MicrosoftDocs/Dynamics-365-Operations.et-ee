---
title: Elektrooniline arveldus Egiptuse kohta
description: See artikkel annab teavet, mis aitab teil alustada Egiptuse elektroonilise arveldusega Microsoft Dynamics 365 Finants ja Dynamics 365 Supply Chain Management.
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: e603bcad4d6dc46bd2594cfdcdf8871eb1f49019
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269497"
---
# <a name="electronic-invoicing-for-egypt"></a>Elektrooniline arveldus Egiptuse kohta

[!include [banner](../includes/banner.md)]

See artikkel annab teavet, mis aitab teil egiptuse elektroonilise arveldusega alustada. See juhib teid läbi konfiguratsioonietappide, mis sõltuvad riigist regulatiivses konfiguratsiooniteenuses (RCS). Need sammud täiendavad sammud, mida kirjeldatakse elektroonilise [arvelduse häälestamisel](e-invoicing-set-up-overview.md).

## <a name="prerequisites"></a>Eeltingimused

Enne selle artikli protseduuride alustamist viige lõpule järgmised eeltingimused:

- Tutvuge elektroonilise arveldamisega, nagu seda kirjeldatakse elektroonilise [arveldamise ülevaates](e-invoicing-service-overview.md).
- Registreerige RCS-ile ja seadistage elektrooniline arveldus. Lisateavet vt järgmistest teemadest:

    - [Registreerige elektroonilise arve teenus ja installige see](e-invoicing-sign-up-install.md)
    - [Azure'i ressursside häälestamine elektroonilise arvelduse jaoks](e-invoicing-set-up-azure-resources.md)
    - [Lifecycle Servicesi mikroteenuste lisandmooduli installimine](e-invoicing-install-add-in-microservices-lcs.md)
    
- Aktiveerige integratsioon oma Microsoft Dynamics 365 Finantsi Dynamics 365 Supply Chain Management või rakenduse ja Elektroonilise arveldamise teenuse [vahel, nagu kirjeldatud jaotises Aktiveeri ja seadista elektroonilise arveldamise integreerimine](e-invoicing-activate-setup-integration.md).
- Looge digitaalserdi saladus azure Key Vault-s ja seadistage see nii, nagu on kirjeldatud kliendi [sertides ja saladustes](e-invoicing-customer-certificates-secrets.md). Testimiseks annab Egiptuse maksuamet kindlad testi digitaalsed sertifikaadid, mida tuleb kasutada ainult testimise ja lahenduse valideerimise faasides. Lisateabe saamiseks minge Egiptuse maksuameti [veebisaidile, kasutades Linki, mis on esitatud Egiptuse e-arve SDK-s](https://sdk.invoicing.eta.gov.eg/faq/).

## <a name="country-specific-configuration-for-the-egyptian-electronic-invoice-eg-feature"></a>Egiptuse elektroonilise arve (SOOVI) funktsiooni riigispetsiifiline konfiguratsioon

Mõned parameetreid Egiptuse elektroonilise arve **(KREEDITARVE)** elektroonilise arveldamise funktsioonist avaldatakse vaikeväärtustega. Enne elektroonilise arveldamise funktsiooni juurutamist teenuse keskkonda vaadake üle vaikeväärtused ja uuendage neid vastavalt vajadusele, et need paremini kajastaksid teie äritoimingut.

1. Importige Egiptuse elektroonilise arve **(UUENDUS) globaliseerimisfunktsiooni** uusim versioon, nagu on kirjeldatud [jaotises Impordi funktsioonid globaalsest hoidlast](e-invoicing-import-feature-global-repository.md).
2. Looge imporditud globaliseerimisfunktsiooni koopia ja valige selle jaoks oma konfiguratsioonipakkuja, nagu kirjeldatud jaotises [Globaliseerimisfunktsiooni loomine](e-invoicing-create-new-globalization-feature.md).
3. Vahekaardil **Versioon** kontrollige, et oleks valitud versioon **Mustand**.
4. Valige vahekaardi **Seadistused** ruudustikus müügiarve **tuletatud funktsiooniseadistus**.
5. Valige suvand **Redigeeri**.
6. Konveieri **töötlemise** vahekaardil jaotises Müügivõimaluste **töötlemine** valige Egiptuse **maksuameti jaoks suvand Allkirjasta jasoni dokument**.
7. **Valige jaotises Parameetrid** väärtus **Serdi nimi** ja seejärel valige loodud digitaalsertifikaadi nimi.
8. Jaotises Müügivõimaluste **töötlemine** valige integreerimine **Egiptuse ETA teenusega**. Korrake seda sammu toimingu kahe esinemiskorra puhul.
9. Valige jaotises **Parameetrid veebiteenuse** **URL** ja sisselogimise **teenuse URL**. Seejärel vaadake üle URL-i parameetrid. Testimise ja tootmise URL-i loomiseks minge [Egiptuse maksuameti veebisaidile, kasutades linki, mis on esitatud Egiptuse e-arve SDK-s](https://sdk.invoicing.eta.gov.eg/faq/).
10. Valige **Salvesta** ja sulgege leht.
11. Korrake projektiarve tuletatud funktsiooniseadistuse jaoks **samme 4 kuni** 10.

## <a name="country-specific-configuration-for-the-egyptian-electronic-invoice-eg-application-setup"></a>Egiptuse elektroonilise arve (ELECTRONIC Invoice) rakenduse häälestuse riigispetsiifiline konfiguratsioon

On parameetreid, mis tuleb seadistada teie finantside või tarneahela halduskeskkonnas. Selle seadistuse saate lõpule viia kahel kohas:

- Otse oma finantside või tarneahela halduskeskkonnas, Lisateavet vt elektroonilise arveldamise [parameetrite seadistamisest](e-invoicing-set-up-parameters.md).
- RCS-s. Elektroonilise arveldamise funktsiooni häälestuse ulatuses saate määrata kõik parameetrid ja seejärel juurutada need elektroonilise arveldamise funktsiooni juurutamisel otse oma finantside või tarneahela halduskeskkonnas.

Mõlema valiku parameetrid on samad. Kui seadistate elektroonilise arveldamise teenuse esimese funktsiooni, on soovitatav järgida neid samme RCS-i parameetrite seadistamiseks ja seejärel juurutada need ühendatud rakendusse.

> [!NOTE]
> Mõned elektroonilise arveldamise funktsiooniversioonid võivad sisaldada eelmääratletud rakendusespetsiifilisi parameetreid finants- või tarneahela halduse jaoks. Sel juhul peaksite kontrollima, et andmed on õiged. Vastasel juhul seadistage parameetrid käsitsi.

1. Otsige üles egiptuse elektroonilise arve **(NT) loodud** globaliseerimisfunktsiooni koopia.
2. Vahekaardil **Versioon** kontrollige, et oleks valitud versioon **Mustand**.
3. Tehke vahekaardil **Seadistused** valik **Rakenduse seadistus**.
4. **Väljal Ühendatud rakendused** valige rakendus, kus soovite parameetreid juurutada.
5. **Elektrooniliste dokumenditüüpide lehel** valige kirje **loomiseks** käsk Lisa.
6. Lisage väljale **Tabeli nimi custInvoiceJour** **.**
7. Lisage kontekstiväljale **viide** kliendiarve konteksti vastendamise **nimele**. Konfiguratsioon on kliendiarve **kontekstimudel**.
8. Lisage elektroonilise **dokumendi vastendamise** väljale viide kliendiarve vastendamise **nimele**. Konfiguratsioon on Arve **mudeli vastendamine**.
9. Valige käsk **Salvesta**.
10. Valige **leheküljel Vastuse** tüübid suvand **Lisa**.
11. Väljal **Vastuse tüüp** sisestage **Vastus**.
12. Väljale Kirjeldus **sisestage** Protsessi **vastus**.
13. Valige väljal **Edastuse olek** suvand **Ootel**.
14. Valige väljal **Mudeli vastendamine** suvand Vastusesõnumi **importimine**. Konfiguratsiooniks on **Egiptuse vastuseteate import (VASTAVALT).**
15. Valige käsk **Salvesta**.
16. Valige **Lisa**.
17. Väljale Vastuse **tüüp** sisestage **ResponseData**.
18. Väljale Kirjeldus **sisestage** protsessi **vastuse andmed**.
19. Valige väljal **Edastuse olek** suvand **Ootel**.
20. Valige andmeüksuse **nime väljal** **SalesInvoiceHeaderV2Entity**.
21. Valige väljal **Mudeli vastendamine** suvand **Vastuseandmete import**. Konfiguratsioon on Egiptuse **vastuse andmeimpordivorming (SAMA).**
22. Valige **Salvesta** ja sulgege leht.
23. Sulgege leht.

Funktsiooni juurutamiseks teeninduskeskkonda ja [rakenduse häälestuse juurutamiseks finantside või tarneahelate halduse ühendatud rakendusse vt Vii lõpule, avalda ja juuruta globaliseerimisfunktsioon](e-invoicing-complete-publish-deploy-globalization-feature.md)

## <a name="privacy-notice"></a>Privaatsusavaldus

Egiptuse elektroonilise **arve (THE) funktsiooni** lubamine võib nõuda piiratud andmete saatmist. Need andmed hõlmavad organisatsiooni maksuregistreerimise ID-d. Andmed edastatakse kolmanda isiku asutused, mille maksuamet on volitanud saatma sellele maksuametile elektroonilisi arveid eelmääratletud vormingus, mis on vajalik integratsiooniks valitsuse veebiteenusega. Administraator saab funktsiooni lubada ja keelata, kui läheb organisatsiooni haldamise **seadistuse** \> **·** \> **elektroonilise dokumendi parameetritesse.** Valige **Funktsioonid** vahekaart, valige read, mis sisaldavad **Egiptuse elektroonilise arve (EG)** lisandmoodul ning seejärel tehke sobiv valik. Välissüsteemidest sellesse Dynamics 365 võrguteenusse imporditud andmed allutavad meie [privaatsusavaldusele](https://go.microsoft.com/fwlink/?LinkId=512132). Lisateavet vt riigispetsiifilise funktsioonidokumentatsiooni jaotisest "Privaatsusteatis".

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise arvelduse ülevaade](e-invoicing-service-overview.md)
- [Elektroonilise arvelduse lisandmooduli teenusehalduse kasutamise alustamine](e-invoicing-get-started-service-administration.md)
- [Elektroonilise arveldusega alustamine](e-invoicing-get-started.md)
- [Kliendi elektroonilised arved Egiptuses](emea-egy-e-invoices.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
