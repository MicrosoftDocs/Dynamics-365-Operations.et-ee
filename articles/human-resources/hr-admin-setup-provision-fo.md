---
title: Inimressursside ettevalmistamine finantside ja toimingute infrastruktuuris
description: See artikkel selgitab Microsoftile uue tootmiskeskkonna ettevalmistamise Dynamics 365 Human Resources protsessi finantside ja toimingute infrastruktuuris.
author: twheeloc
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 15060d8bdd598476081c22d7280319da3db0cb31
ms.sourcegitcommit: 1401d66b6b64c590ca1f8f339d622e922920cf15
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/20/2022
ms.locfileid: "9178406"
---
# <a name="provision-human-resources-in-the-finance-and-operations-infrastructure"></a>Inimressursside ettevalmistamine finantside ja toimingute infrastruktuuris

_**Rakendub:** inimressursid finantside ja toimingute rakenduse infrastruktuuris_ 

> [!NOTE]
> Alates 2022. juulist ei saa uusi inimressursid keskkondi eraldi inimressursside infrastruktuuris Microsoft Dynamics ette luua ja uusi elutsükli teenuste (LCS) projekte ei saa selles luua. Kliendid saavad inimressursside keskkondi kasutusele võtta finantside ja toimingute infrastruktuuris.

See artikkel selgitab Microsoftile uue tootmiskeskkonna ettevalmistamise Dynamics 365 Human Resources protsessi finantside ja toimingute infrastruktuuris.

## <a name="prerequisites"></a>Eeltingimused

Enne uue keskkonna kasutamist peavad olema täidetud järgmised eeltingimused:

- Olete ostnud Inimressursse pilvelahenduste pakkuja (CSP) või ettevõtte arhitektuuri (EA) lepingu kaudu. Kui teil on olemasolev Dynamics 365 litsents, mis sisaldab juba Inimressursside teenuse plaani ja te ei saa selle artikli samme lõpetada, pöörduge tugiteenuste osutaja poole.
- Globaalne administraator on sisse loginud elutsükli [Microsoft Dynamics teenustesse (LCS)](https://lcs.dynamics.com) ja loonud uue finants- ja operatsiooniprojekti.

## <a name="provision-a-human-resources-trial-environment"></a>Human Resources proovikeskkonna ettevalmistamine

> [!NOTE]
> Alates 2022. aasta aprillist ei ole Inimressursside proovikeskkonnad saadaval eraldi rakenduses. Potentsiaalsed kliendid, kes on huvitatud inimressursside võimaluste hindamisest finantside ja operatsioonide rakendustes, saavad koos demoandmetega kasutada tasuta 30-päevast proovimist. Dynamics 365 Finance hõlmab inimressursside võimalusi, mis tuuakse finantside infrastruktuuri autonoomse rakenduse ühendamise kaudu. Lisateavet vt jaotisest [Inimressursside pakkumiste ühendamine toob klientide võimalused kokku](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers). Lisateavet Dynamics 365 Finance katsete kohta vt samm-sammult [juhendist](../fin-ops-core/fin-ops/get-started/before-you-buy.md).

## <a name="plan-human-resources-environments"></a>Human Resourcesi keskkondade plaanimine

Enne oma esimese Human Resourcesi keskkonna loomist peaksite hoolikalt planeerima keskkonna vajadused oma projekti jaoks. Inimressursside baas kordustellimus hõlmab kahte keskkonda: tootmiskeskkonda ja vaikestandardse kinnitamiskatset (Box) keskkonda. Sõltuvalt teie projekti keerukusest on teil võimalik projektitegevuste toetamiseks osta täiendavaid keskkondi.

Siin on mõned kaalutlused täiendavatele valikulistele keskkondadele:

- **Andmete** migratsioon – andmete siirdamise tegevused võimaldavad teie sisendkausta keskkonda kasutada eesmärkide katsetamiseks kogu projekti vältel. Kui teil on lisakeskkond, saavad andmete siirde tegevused jätkata samas ajal, kui testitakse ja konfigureeritakse tegevusi üheaegselt teises keskkonnas.
- **Integratsioon** : konfigureerige ja katsetage integratsiooni, mis võib hõlmata algintegratsiooni või kohandatud integratsiooni, nt palgaarvestuse, kandidaadi jälgimissüsteemide või soodustussüsteemide ja pakkujate integratsioone.
- **Koolitus** – teil võib olla vaja eraldi keskkonda, mis on konfigureeritud koolitusandmete komplektiga, nii et saate oma töötajaid õpetama uut süsteemi kasutama. 
- **Mitmefaasiline projekt** – võib olla vajalik täiendav keskkond konfiguratsiooni, andmete migratsiooni, testimise või muude projektifaasi tegevuste toetamiseks, mis on planeeritud pärast projekti esmast läbimist.
- **Arendus** – finantside ja toimingute infrastruktuuris saate nüüd lahendust laiendada ja oma kohandusi laiendada. Iga arendaja peab kasutama oma arenduskeskkonda. Lisateavet vt jaotisest Arenduskeskkonna [juurutamine ja juurdepääs](/fin-ops-core/dev-itpro/dev-tools/access-instances).
- **GOLD** – uute juurutamise puhul on levinud tava kasutada eraldi kuldkeskkonda, mida hoitakse konfiguratsiooni ja andmete migratsiooni jaoks pristiinis. Seda keskkonda saab kasutada kogu rakenduskeskkonnas, et värskendada teisi keskkondi. Seda kasutatakse uue tootmiskeskkonna loomiseks, kus on põhikonfiguratsioon ja andmete migratsioon. Te ei saa juurutada tootmiskeskkonda finantside ja toimingute infrastruktuuris enne, kui olete läbinud käivitamisvalmiduse protsessi. Lisateavet vt "Reaalajas [ettevalmistamine"](/fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live).

<!--NOTE: Need to come back and verify Tier-1 can be used and if a customer cannot purchase tier 3-5 need specific documentation about this.-->

> [!IMPORTANT]
> Keskkonda arvesse võtmaks soovitame järgmist lähenemist:
>
> - Kasutage vaikestandardi kinnitamiskatset (varasemaltUdud) keskkonda või muud keskkonda, et teha mkausta üleminekut enne oma otseülekannet.
> - Säilitage üksikasjalik ülemineku kontroll-loend, mis hõlmab kõiki andmepakette, mis on vajalikud lõplike andmete siirdamiseks tootmiskeskkonda ülemineku ajal. See soovitus on eriti oluline juhul, kui teil ei ole konfiguratsioonide salvestamiseks eraldi kuldkeskkonda.
> - Saate kogu projekti jooksul kasutada standardset kinnitamiskatset (varasemaltUdud) keskkonda või teist kiht-2 või kõrgemat keskkonda testkeskkonnana. Kui vajate täiendavaid keskkondi, saab teie organisatsioon neid osta lisakuluga.

## <a name="create-an-lcs-project"></a>LCS-i projekti loomine

Selleks, et kasutada oma rakenduse Human Resources keskkondade haldamiseks LCS-i, peate esmalt looma LCS-i projekti. Inimressursside keskkonna migreerimisel finantside ja toimingute infrastruktuuri peate looma uue LCS-projekti finantside ja toimingute rakenduste jaoks. Lisateavet vt jaotisest [Inimressursside keskkonna migereerumine](hr-admin-migrate-overview). Kui teil on juba LCS-projekt muude finantside ja toimingute rakenduste jaoks, saate inimressursside funktsioonid funktsioonihalduse tööruumis **lubada**. Lisateavet vt [Funktsioonihalduse ülevaatest](/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Kui uus klient registreerub inimressursside kasutajaks, hõlmab kordustellimus rakendusprojekti tööruumi. Kui klient on teenuse aktiveerinud, peab rentniku administraator rentnikukontoga <https://lcs.dynamics.com> sisse logima. Projekti tööruum luuakse organisatsiooni jaoks automaatselt. Lisateavet vt finantside ja [toimingute rakenduste klientide elutsükli](/fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs) teenustest (LCS).

> [!NOTE]
> Eduka ressursi ressursimääramise tagamiseks peab konto, mida kasutate Inimressursside keskkonna ressursina kasutamiseks, olema määratud kas süsteemiadministraatori rollile või süsteemi kohandaja rollile keskkonnas, **·** **·** Power Apps mis on seostatud Inimressursside keskkonnaga. Lisateavet selle kohta, kuidas määrata kasutajatele turberollid, Microsoft Power Platform vaadake jaotisest [Kasutaja turbe konfigureerimine ressurssidele](/power-platform/admin/database-security).

Enne keskkonna juurutamist peate LCS-i projektile vastama. Lisateavet vt "Projektiletamine ["](/fin-ops-core/dev-itpro/lifecycle-services/project-onboarding). Lisateavet LCS-i kasutamise kohta vt elutsükli [teenuste (LCS) kasutusjuhendist](/fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide).

## <a name="deploy-human-resources-environments"></a>Inimressursside keskkonna juurutamine

Finantside ja toimingute rakenduste, sealhulgas inimressursside juurutamine pilves nõuab, et mõistate keskkonda ja kordustellimust, kuhu te juurutate, kes saab teha, milliseid ülesandeid teha ja milliseid andmeid ja kohandusi hallata. Uute keskkondade juurutamisel on soovitatav kasutada nimelise kasutaja asemel teenusekontot. Lisateavet keskkonna juurutamise kohta finantside ja toimingute infrastruktuuris vt pilve juurutuse [ülevaadet](/fin-ops-core/dev-itpro/deployment/cloud-deployment-overview).

Inimressursid tootmiskeskkonna juurutamiseks finantside ja toimingute infrastruktuuris peate lõpule viia reaalajas valmisoleku protsessi. Lisateavet vt "Reaalajas [ettevalmistamine"](/fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live). See protsess hõlmab LCS-i kordustellimuse hindajat. Lisateabe saamiseks vt kordustellimuse [hindajat](/fin-ops-core/dev-itpro/lifecycle-services/subscription-estimator).

## <a name="integrate-microsoft-power-platform-with-human-resources"></a>Inimressurssidega Microsoft Power Platform integreerimine

Microsoft Power Platform Rakendus <a0/& pakub halduskeskuse kaudu Dynamics 365 rakenduste jaoks Power Platform võimaluste komplekti. Inimressursside andmete kasutamist saab integreerida ja laiendada Microsoft Power Platform. Lisateavet inimressursside integreerimise kohta vt integreerimisest Microsoft Power Platform Finantside [Microsoft Power Platform ja toimingute rakendustega](/fin-ops-core/dev-itpro/power-platform/overview).

## <a name="supported-geographies"></a>Toetatud geograafilised graafikud

Lisateavet inimressursside jaoks toetatud keelte ja geograafiliste keelte kohta [vt teemast Globaalne kujunduse abil: lisateave riikide ja toetatud keelte kohta](https://dynamics.microsoft.com/availability-reports/).

## <a name="grant-access-to-the-environment"></a>Keskkonnale juurdepääsu andmine

Vaikimisi on keskkonnale juurdepääs ainult selle loonud üldadministraatoril. Te peate rakenduse teistele kasutajatele konkreetselt juurdepääsu andma. Te peate rakenduse Human Resources keskkonnas kasutajad lisama ja neile sobivad rollid määrama. Lisateabe saamiseks vaadake teemasid [Uute kasutajate loomine](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) ja [Kasutajate määramine turberollidesse](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles).

## <a name="additional-resources"></a>Lisaressursid
Lisateavet projektide kasutamise ja haldamise kohta LCS-is finantside ja operatsioonide rakenduse infrastruktuuris leiate järgmistest ressurssidest:

- [Teenuse Lifecycle Services ressursid](/fin-ops-core/dev-itpro/lifecycle-services/lcs.md)
- [Teenuse Lifecycle Services (LCS) kasutusjuhend](/fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [Iseteeninduse juurutamise ülevaade](../fin-ops-core/dev-itpro/deployment/infrastructure-stack.md)
- [Andmebaasi tegemistoimingute avaleht](../fin-ops-core/dev-itpro/database/dbmovement-operations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
