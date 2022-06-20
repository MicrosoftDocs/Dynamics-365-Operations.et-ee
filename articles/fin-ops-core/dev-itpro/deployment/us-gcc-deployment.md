---
title: Dynamics 365 Finantsid, Tarneahela haldus ja Kaubandus USA valitsuse kogukonna pilves (GCC)
description: See artikkel annab teavet Microsoft Dynamics 365 USA valitsuse toodete kohta, mis on saadaval kvalifitseeritud valitsuse ja eraisikutele.
author: hasaid
ms.date: 11/12/2021
ms.topic: article
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2021-11-09
ms.openlocfilehash: 90e64fec512307af209ace128d5897475de7aee5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867269"
---
# <a name="dynamics-365-finance-supply-chain-management-and-commerce-in-us-government-community-cloud-gcc"></a>Dynamics 365 Finantsid, Tarneahela haldus ja Kaubandus USA valitsuse kogukonna pilves (GCC)

[!include [banner](../includes/banner.md)]



Valige Microsoft Dynamics 365 USA valitsuse tooted on saadaval kvalifitseeritud valitsuse ja eraisikutele. Need üksused on piiratud järgmiste tüüpide jaoks:

- USA föderaal-, osariigi-, kohaliku-, riigi- ja territoriaalvalitsuse üksused
- Privaatsed üksused, mis kasutavad Dynamics 365 USA valitsust, et pakkuda lahendusi valitsusüksustele või pilve kogukonna kvalifitseeritud liikmetele
- Eraisikud, kelle kliendiandmed kuuluvad valitsuse määrustele ja Dynamics 365 USA valitsus on sobiv teenus regulatiivsetele nõuetele vastamiseks

Lisateavet vt Dynamics [365 USA valitsusest](/power-platform/admin/microsoft-dynamics-365-government).

## <a name="onboarding"></a>Kasutuselevõtt

Rakendusprojekti algse sisseostmiseks elutsükli Microsoft Dynamics teenustes (LCS) [järgige rakendusprojekti juhiseid](../../../fin-ops-core/fin-ops/imp-lifecycle/onboard.md). Ärge siiski kasutage linki avalikule LCS-ile, mis on nendes juhistes antud. Kasutage selle asemel järgmist URL-i, et avada LCS USA valitsuse kogukonna pilve (GCC):<https://gov.lcs.microsoftdynamics.us>.

Kui algne sisseostmine on lõpule viidud, järgige projektis [olevaid juhiseid](../lifecycle-services/project-onboarding.md). Taas kord kasutage avaliku [LCS-i asemel GCC-d](https://gov.lcs.microsoftdynamics.us) LCS-i.

## <a name="environment-deployment"></a>Keskkonna juurutamine

Pärast projekti põhist lõpetamist saate üle vaadata finantside ja toimingute rakenduste klientide elutsükli teenustes (LCS) kirjeldatud LCS-i [lisavõimalused](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md). Seejärel minge edasi keskkonna juurutusse.

- Microsofti hallatud keskkondade juurutamiseks LCS-i [kaudu järgige finantside ja toimingute rakenduste klientide elutsükli teenuste (LCS) juhiseid](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md#new-deployment-experience).
- Pilve hostitud keskkondade kohta vt "Juurutamine [ja juurdepääs arenduskeskkonnad"](../../../fin-ops-core/dev-itpro/dev-tools/access-instances.md). Samuti peate oma konnektorite ressursihalduriga ühendamisprotsessi lõpule viima, [nagu on kirjeldatud Usa valitsuse elutsükli teenuste projektide azure'i ressursihaldurit läbiva ajastamise protsessis](arm-onbarding-us-goverment.md).

> [!NOTE]
> USA valitsuse LCS-projektide puhul toetatakse ainult Azure'i valitsusespetsiifilisi Azure'i kordustellimusi.

## <a name="features-that-arent-available"></a>Funktsioonid, mis pole saadaval

Mõned funktsioonid ei ole GCC-s juurutamiseks saadaval või ei ole need GCC-s kasutamiseks saadaval Dynamics 365-ga. Teenused pole Azure DevOps näiteks GCC-s saadaval. Siiski saab kasutada ettevõtte ettevõttes Azure DevOps kasutatavad Azure DevOps või avalikud teenused. Lisateavet funktsiooni saadavuse kohta vt Business [Applications US Government Feature Availability](https://aka.ms/BAPFunctionalParity).

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

### <a name="are-dynamics-365-finance-and-dynamics-365-supply-chain-management-supported-in-gcc-high"></a>Kas Dynamics 365 finance ja seda Dynamics 365 Supply Chain Management toetab GCC-High?

Ei. Dynamics 365 Finance ja seda Dynamics 365 Supply Chain Management toetab ainult GCC.

### <a name="can-i-use-public-azure-devops-with-finance-and-supply-chain-management-in-gcc"></a>Kas GCC-s Azure DevOps saab kasutada avalikku koos finants- ja tarneahelahaldusega?

Jah, kui teil Azure DevOps ei ole nõudeid lahendusele, mille on kinnitanud Föderaalrisk ja Autoriseerimise haldusprogramm (FEDRAMP). Teise võimalusena saate kasutada serverit Azure DevOps.

### <a name="can-i-deploy-a-cloud-hosted-environment-tier-1-development-environment-on-an-azure-commercial-subscription"></a>Kas ma soovin juurutada pilves majutatud keskkonna Tier-1 arenduskeskkonna Azure'i äri kordustellimuses?

Ei. GCC [puhul LCS-is](https://gov.lcs.microsoftdynamics.us) peate pilve majutatud keskkonna juurutamiseks kasutama Azure'i valitsuse kordustellimust.

### <a name="what-can-i-do-if-i-need-a-package-from-the-shared-asset-library-but-it-isnt-available-in-lcs-for-gcc"></a>Mida teha, kui vaja on ühiskasutusega varateegi paketti, kuid see pole GCC jaoks LCS-s saadaval?

Sama paketti saate alla laadida avalikuS LCS-i jagatud [varateegis](https://lcs.dynamics.com). Teise võimalusena võib teie partner aidata teil paketi alla laadida.

### <a name="is-the-code-upgrade-tool-available-in-gcc"></a>Kas kooditäienduse tööriist on GCC-s saadaval?

Ei, koodi uuendustööriist pole praegu GCC-s saadaval. Saate siiski luua potentsiaalse kliendi projekti avalikus [LCS-s](https://lcs.dynamics.com) ja kasutada koodi täiendamise tööriista. Võtke arvesse, et te ei saa potentsiaalse kliendi projektides keskkondi juurutada.

### <a name="can-my-partner-open-a-support-ticket-on-my-behalf"></a>Kas minu partner saab minu nimel tugipileti avada?

Jah. Kuid kui teie partner kasutab mitte-GCC identiteeti, suunatakse tugipilet avaliku tugiteenuste järjekorda. Soovitame kasutada LCS-i kliendi GCC-õigusõigusi, et avada tugipileteid.

## <a name="see-also"></a>Vt ka

- [Dynamics 365 USA valitsus](/power-platform/admin/microsoft-dynamics-365-government)
- [USA ärirakenduste valitsuse funktsiooni saadavus](https://aka.ms/BAPFunctionalParity).
- [Teenuse Lifecycle Services (LCS) kasutusjuhend](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [Pilvjuurutuse ülevaade](../../../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
