---
title: Regulatory Configuration Service
description: See teema annab ülevaate Regulatory Configuration Service (RCS) võimalustest ja selgitab, kuidas teenusele juurde pääseda.
author: JaneA07
ms.date: 06/04/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 816b1bf9da9acdd5999320f39fb68fb6deda197c
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2022
ms.locfileid: "7983463"
---
# <a name="regulatory-configuration-service"></a>Regulatory Configuration Service

[!include [banner](../includes/banner.md)]

Regulatory Configuration Service (RCS) on autonoomne disainer ja elutsükli haldamise teenus koodita/vähese koodiga globaliseerumisfunktsioonide jaoks. RCS-i globaliseerumise sidusrühmad laiendavad ja kohandavad peamisi globaliseerumisvaldkondi nagu maksud, e-arved, regulatiivne aruandlus, pangandus ja äridokumendid, ilma et nad peaksid arendajaid kaasama. See koodita/vähese koodiga globaalne lähenemine muudab globaliseerumise lihtsamaks, kiiremaks ja kulutõhusamaks, et seda luua või laiendada.

RCS pakub järgmisi võimalusi.

- Kõigi elektroonilise aruandluse (ER) pakutavate funktsioonide tugi.
- Uute globaliseerumismikroteenuste konfigureerimise eeltingimus.
- Elektroonilise arvelduse tugi. Lisateavet leiate teemast [E-arveldus](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).
- Toetab maksuarvestust. Lisateavet vt jaotisest [Maksuteenus](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).
- Uute globaliseerumisfunktsioonide funktsioonide tugi, mis lihtsustab mitmekomponendiliste funktsioonide elutsükli haldamist ning pakub lisavõimalusi toimingute konfigureerimiseks ja funktsiooniparameetrite seadistamiseks. Lisateavet vt teemast [Regulatory Configuration Service – globaliseerumisteenuste lihtsustatud globaliseerumisfunktsioonide haldamine](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).
- Globaalses hoidlas kohandatud konfiguratsioonide tsentraliseeritud avaldamise, salvestamise ja ühiskasutuse tugi, et lihtsustada konfiguratsioonihaldust, ilma et oleks vaja kasutada Microsoft Dynamics Lifecycle Services (LCS) teenuseid.

## <a name="access-rcs"></a>RCS ligipääs

RCS-i saate registreeruda või sisse logida [Regulatory Configuration Service lehel](https://marketing.configure.global.dynamics.com/).

![RCS-i registreerimine ja sisselogimine.](media/202103_RCS%20Marketing%20page_updated_1.jpg)

Vaadake lehel **Regulatory Configuration Service** üle ja nõustuge teenuse kasutamise täiendavate tingimustega ning valige üks järgmistest nuppudest.

- **Registreeri**, kui olete teenuse esmakordne kasutaja ja kasutate ettevõtte meiliaadressi oma organisatsiooni teenusekeskkonna ettevalmistamiseks
- **Logi sisse**, kui olete varem teenuse kasutajaks registreerunud ja soovite pääseda ligi oma ettevõtte keskkonnale

> [!NOTE] 
> Pärast registreerumist on soovitatav lisada RCS-keskkonda täiendav SysAdmin`i kasutaja. See kasutaja on ette nähtud keskkonna kaasadministraatoriks. See aitab tagada stabiilsust juurdepääsuks RCS-keskkonnale, kuna rolliga SysAdmin hallatakse kasutajaid selle keskkonna puhul. Saate kasutajaid lisada kasutades **RCS tööruumi > Süsteemihaldus**.

## <a name="regional-availability"></a>Piirkondlik kättesaadavus

RCS on üldiselt saadaval järgmistes piirkondades:

- Ameerika Ühendriigid
- India
- Prantsusmaa
- Euroopa

Regioonide täieliku nimekirja saamiseks vt teemat [Dynamics 365 ja Power Platform: saadavus, andmete asukoht, keel ja lokaliseerimine](https://aka.ms/dynamics_365_international_availability_deck).

## <a name="rcs-default-company"></a>RCS väikeettevõte

RCS-is kasutatav kujundusaja funktsioon on ühiskasutuses kõigi ettevõtete vahel. Ettevõttepõhiseid funktsioone pole. Seetõttu soovitame teil kasutada ühte ettevõtet, **DAT**, koos teie RCS-keskkonnaga.

Mõne stsenaariumi puhul võite siiski soovida, et ER-vormingud kasutaks konkreetse juriidilise isikuga seotud parameetreid. Ainult sellistes stsenaariumides peaksite kasutama ettevõtte vaikelülitit. Näite vaatamiseks vt [ER-vormingute konfigureerimine juriidilise isiku kohta määratud parameetrite kasutamiseks](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).

## <a name="related-rcs-documentation"></a>Seotud RCS-dokumentatsioon

Seotud komponentide kohta lisateabe saamiseks vaadake järgmisi peatükke:

- **RCS:**

    - [ER-konfiguratsioonide loomine RCS-is ja üleslaadimine globaalsesse hoidlasse](rcs-global-repo-upload.md)

- **Globaalse hoidla:**

    - [ER-i konfiguratsiooni loomine ja üleslaadimine globaalsesse reposse](rcs-global-repo-upload.md)
    - [Ühiskasutuse konfiguratsioon globaalses hoidlas](rcs-global-repo-share-configuration.md)
    - [Täiustatud filtreerimine globaalses hoidlas](enhanced-filtering-global-repo.md)
    - [ER-i konfiguratsioonide allalaadimine globaalsest hoidlast](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [Konfiguratsioonide katkestamine globaalses hoidlas](discontinuing-configurations-rcs-global-repo.md)
    - [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) ladustamise amortiseerimine](rcs-lcs-repo-dep-faq.md)

- **Globaliseerimisfunktsioon:**

    - [Regulatory Configuration Service (RCS) – globaliseerumise funktsioon](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)


## <a name="troubleshooting-rcs-sign-up"></a>RCS logimise tõrkeotsing

Kui registreerite teenuse leheküljelt RCS-i, võib teil tekkida probleem, mis on seotud rakendusega Azure Active Directory (Azure AD). Tõrketeade näitab, et RCS-ile registreerimine on praegu välja lülitatud ja tuleb sisse lülitada, enne kui saate allkirjastamisprotsessi lõpule viia.

![RCS-i registreerumise tõrketeade.](media/01_RCSSignUpError.jpg)

Probleem ilmneb, kuna olete blokeerinud registreerumise sihttellimustele ja atribuut peab olema teie `AllowAdHocSubscriptions` rentnikus lubatud. 

- Kui teie IT-osakond haldab teie organisatsiooni Azure'i rentnikku, võtke probleemist aru anda selle osakonnaga ühendust.
- Kui vastutate Azure rentnike haldamise eest, saate probleemid lahendada, järgides [Mis on iseteeninduse registreerimine rakenduses Azure Active Directory](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).
