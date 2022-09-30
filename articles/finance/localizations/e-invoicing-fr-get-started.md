---
title: Prantsusmaa jaoks elektroonilise arvelduse lisandmooduliga alustamine
description: See artikkel annab teavet, mis aitab teil alustada Prantsusmaa elektroonilise arvelduse lisandmooduliga.
author: dkalyuzh
ms.date: 07/07/2022
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2022-00-02
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: 3ac4af8c131e35d9a499d0d558c7cce1d4872b37
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573274"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-france"></a>Prantsusmaa jaoks elektroonilise arvelduse lisandmooduliga alustamine

[!include [banner](../includes/banner.md)]

See artikkel annab teavet, mis aitab teil Alustada Prantsusmaa elektroonilise arveldusega. See juhib teid läbi konfiguratsioonietappide, mis sõltuvad riigist regulatiivses konfiguratsiooniteenuses (RCS). Need sammud täiendavad samme, mida kirjeldatakse jaotises [Alustage elektroonilise arvelduse lisandmooduliga](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-french-chorus-pro-submission-fr-electronic-invoicing-feature"></a>Riigile omane konfiguratsioon Prantsuse Chorus Pro esitamise (FR) elektroonilise arveldamise funktsioonile

Mõned sammud on vajalikud Prantsuse **Chorus Pro esitamise (FR)** elektroonilise arveldamise funktsiooni konfigureerimiseks. Mõned konfiguratsiooni parameetrid avaldatakse vaikeväärtustega. Need väärtused tuleb läbi vaadata ja uuendada, et need paremini kajastaksid teie äritoiminguid.

### <a name="prerequisites"></a>Eeltingimused

Enne selle artikli protseduuride alustamist viige lõpule järgmised eeltingimused:

- Tutvuge elektroonilise arveldusega. Lisateavet vt elektroonilise arveldamise [ülevaatest](e-invoicing-service-overview.md).
- Registreerige RCS-ile ja seadistage elektrooniline arveldus. Lisateavet vt järgmistest artiklitest.

    - [Registreerige elektroonilise arve teenus ja installige see](e-invoicing-sign-up-install.md)
    - [Azure'i ressursside häälestamine elektroonilise arvelduse jaoks](e-invoicing-set-up-azure-resources.md)
    - [Lifecycle Servicesi mikroteenuste lisandmooduli installimine](e-invoicing-install-add-in-microservices-lcs.md)
    - [Aktiveerige ja seadistage integratsioon elektroonilise](e-invoicing-activate-setup-integration.md) arveldamisega – Microsoft Dynamics kasutage selle artikli teavet, et aktiveerida integratsioon oma 365 finantsi Dynamics 365 Supply Chain Management või rakenduse ja elektroonilise arveldamise teenuse vahel.
    - [NAF-koodid, siret-numbrid](emea-fra-naf-codes-siret-numbers.md)[ning NAF-koodide ja Siret-numbrite](tasks/fr-00003-naf-codes-siret-numbers.md) seadistamine – kasutage nende artiklite teavet, et seadistada oma juriidilistes isikutes NAF-koodid ja Siret-numbrid. 

- Teie organisatsioon peab olema registreeritud, et töötada Chorus Pro-ga. Microsoft pakub rakenduste programmeerimisliidese (API) kaudu integratsiooni Chorus proga OAuth2 režiimis. Üksikasjalikku teavet Chorus Pro registreerimise ja rakenduse aktiveerimise kohta vt ametlikust [dokumentatsioonist](https://communaute.chorus-pro.gouv.fr/documentation/help-for-api-developers-in-oauth2-mode/).

    Järgige neid samme, et registreerida koos Chorus Pro-ga.

    1. Registreerimise alustamiseks avage [PISTE](https://piste.gouv.fr/en/component/apiportal/registration) portaal. 
    2. Registreerige rakendus ja aktiveerige avatud autoriseerimise (OAuth) mandaadid.
    3. Kopeerige ja salvestage OAuthi mandaatide kliendi ID ja salavõti. Seda teavet saate kasutada hilisemate sammude abil.
    4. Minge registreerimiseks [Chorus Pro](https://portail.chorus-pro.gouv.fr/aife_csm/?id=aife_enrollment) portaali. 
    5. Looge API-juurdepääsuks tehniline konto. Lisateavet vt API toodangule [juurdepääsuks tehnilise konto loomine](https://communaute.chorus-pro.gouv.fr/documentation/creation-of-a-technical-account-for-an-api-access-in-production/).
    6. Kopeerige tehnilise konto kasutaja ID ja parool. Seda teavet saate kasutada hilisemate sammude abil.

## <a name="country-specific-configuration-of-the-application-setup-for-the-french-chorus-pro-submission-fr-electronic-invoicing-feature"></a>Prantsuse Chorus Pro esitamise (FR) elektroonilise arveldamise funktsiooni rakenduse häälestuse riigispetsiifiline konfiguratsioon

Mõned Prantsuse **Chorus Pro esitamise (FR) elektroonilise arveldamise funktsiooni** parameetrid avaldatakse vaikeväärtustega. Enne elektroonilise arveldusfunktsiooni juurutamist teenuse keskkonda vaadake üle ja uuendage vaikeväärtused vastavalt vajadusele, et need paremini kajastaksid teie äritoiminguid.

1. Azure’i võtme vaultis looge saladused ja vastav viide neile. Lisateabe saamiseks vt kliendi serte [ja saladusi](e-invoicing-customer-certificates-secrets.md).
2. Importige French **Chorus Pro esitamise (FR)** globaliseerimisfunktsiooni uusim versioon, nagu on kirjeldatud [jaotises Impordi funktsioonid globaalsest hoidlast](e-invoicing-import-feature-global-repository.md).
3. Looge imporditud globaliseerimisfunktsiooni koopia ja valige oma konfiguratsioonipakkuja. Lisateavet vt teemast Globaliseerimisfunktsiooni [loomine](e-invoicing-create-new-globalization-feature.md).
4. Vahekaardil **Versioon** kontrollige, et oleks valitud versioon **Mustand**.
5. Valige vahekaardi **Seadistused** ruudustikus UBL-i **müügiarve tuletatud funktsiooniseadistus**.
6. Valige **käsk Redigeeri** ja **seejärel** **·** **valige konveieri töötlemise jaotises suvand (Preview) French Chorus Pro** **integreerimine tegevuse nimega French Chorus Pro.**
7. **Valige jaotise Parameetrid** väljal Kliendi **ID** salanimi turvanimi, mille lõite kliendi ID jaoks võtmehoidlas.
8. Väljal Kliendi **saladusnimi valige** võtme vault kliendi saladuse jaoks loodud salanimi.
9. Väljal Tehniline **sisselogimise saladusnimi** valige saladusnimi, mille lõite tehnilise konto sisselogimiseks võtme vault.
10. Väljal Tehniline **parooli salanimi** valige saladusnimi, mille lõite tehnilise konto parooli jaoks võtme vault.
11. Konveieri **töötlemise** vahekaardi jaotises **Müügivõimaluste** **töötlemine valige suvand Integreeri koos French Chorus Pro’ga** tegevusnimega **French Chorus Pro taotluse olek**.
12. **Valige jaotise Parameetrid** väljal Kliendi **ID** salanimi turvanimi, mille lõite kliendi ID jaoks võtmehoidlas.
13. Väljal Kliendi **saladusnimi valige** võtme vault kliendi saladuse jaoks loodud salanimi.
14. Väljal Tehniline **sisselogimise saladusnimi** valige saladusnimi, mille lõite tehnilise konto sisselogimiseks võtme vault.
15. Väljal Tehniline **parooli salanimi** valige saladusnimi, mille lõite tehnilise konto parooli jaoks võtme vault.
16. Valige **Salvesta** ja sulgege seejärel leht.
17. Korrake UBL-projektiarve tuletatud funktsiooniseadistuse, **UBL-i** **müügi** kreeditarve tuletatud funktsiooniseadistuse ja UBL-projekti **kreeditarve tuletatud funktsiooniseadistuse puhul samme 6 kuni 16**.

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise arvelduse lisandmooduli ülevaade](e-invoicing-service-overview.md)
- [Elektroonilise arvelduse lisandmooduli teenusehalduse kasutamise alustamine](e-invoicing-get-started-service-administration.md)
- [Elektroonilise arvelduse lisandmooduli kasutamise alustamine](e-invoicing-get-started.md)
