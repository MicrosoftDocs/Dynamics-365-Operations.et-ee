---
title: Dynamics 365 Finance ja Dynamics 365 Supply Chain Management USA valitsuse kogukonna pilves (GCC)
description: See teema annab teavet 365 USA valitsuse toote kohta Microsoft Dynamics, mis on kättesaadavad kvalifitseeritud valitsus- ja eraõiguslikele üksustele.
author: hasaid
ms.date: 11/12/2021
ms.topic: article
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2021-11-09
ms.openlocfilehash: 0c8b88e5d190f6dc9beb9342909d1e489d4af10b
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062282"
---
# <a name="dynamics-365-finance-and-dynamics-365-supply-chain-management-in-us-government-community-cloud-gcc"></a>Dynamics 365 Finance ja Dynamics 365 Supply Chain Management USA valitsuse kogukonna pilves (GCC)

[!include [banner](../includes/banner.md)]



Valige Microsoft Dynamics 365 Ameerika Ühendriikide (USA) valitsuse toodet, mis on saadaval kvalifitseeritud valitsus- ja eraõiguslikele üksustele. Need üksused on piiratud järgmiste tüüpidega:

- USA föderaal-, osariigi-, kohalikud, hõimu- ja territoriaalsed valitsusüksused
- Eraolemid, mis kasutavad Dynamics 365 USA valitsust, et pakkuda lahendusi valitsusasutustele või pilvekogukonna kvalifitseeritud liikmetele
- Eraõiguslikud üksused, kellel on kliendiandmed, mille suhtes kehtivad valitsuse määrused, ja Dynamics 365 USA valitsus on sobiv teenus regulatiivsete nõuete täitmiseks

Lisateavet vt teemast [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government).

## <a name="onboarding"></a>Kasutuselevõtt

Lifecycle Servicesi (LCS) rakendusprojekti Microsoft Dynamics esialgse kasutuselevõtu lõpuleviimiseks järgige rakendusprojekti Onboard [juhiseid](../../../fin-ops-core/fin-ops/imp-lifecycle/onboard.md). Kuid ärge kasutage linki avalikule LCS-ile, mis on esitatud nendes juhistes. Selle asemel kasutage USA valitsuse kogukonna pilve (GCC) LCS-i avamiseks järgmist URL-i:<https://gov.lcs.microsoftdynamics.us>.

Kui esialgne sisseminek on lõpule viidud, järgige Projecti kasutuselevõtu [juhiseid](../lifecycle-services/project-onboarding.md). Jällegi kasutage [avaliku LCS-i asemel GCC-d](https://gov.lcs.microsoftdynamics.us).

## <a name="environment-deployment"></a>Keskkonna juurutamine

Pärast projekti kasutuselevõtu lõpetamist saate vaadata LCS-i lisavõimalusi, mida on kirjeldatud finance and Operationsi rakenduste klientide [elutsükli teenustes](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md)(LCS). Seejärel liikuge edasi keskkonna juurutamise juurde.

- Microsofti hallatavate keskkondade juurutamiseks LCS-i kaudu järgige finance and Operationsi rakenduste klientide [lifecycle services (LCS) juhiseid](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md#new-deployment-experience).
- Pilve majutatud keskkondade kohta leiate teemast [Arenduskeskkondade](../../../fin-ops-core/dev-itpro/dev-tools/access-instances.md) juurutamine ja sellele juurdepääs. Samuti peate oma konnektorite jaoks lõpule viima ressursihalduri sisseelamisprotsessi, nagu on kirjeldatud jaotises [Azure Resource Manageri sisseelamisprotsessi lõpuleviimine USA valitsuse elutsükli teenuste projektide](arm-onbarding-us-goverment.md) jaoks.

> [!NOTE]
> US Government LCS-projektide puhul toetatakse ainult Azure Governmenti-spetsiifilisi Azure'i tellimusi.

## <a name="features-that-arent-available"></a>Funktsioonid, mis pole saadaval

Mõned funktsioonid pole GCC-s juurutamiseks saadaval või neid pole GCC-s dynamics 365-ga kasutamiseks saadaval. Näiteks Azure DevOps pole teenused GCC-s saadaval. Siiski saab kasutada kohapealseid Azure DevOps või avalikke Azure DevOps teenuseid. Lisateavet funktsioonide saadavuse kohta leiate teemast [Ärirakendused USA valitsuse funktsiooni saadavus](https://aka.ms/BAPFunctionalParity).

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

### <a name="are-dynamics-365-finance-and-dynamics-365-supply-chain-management-supported-in-gcc-high"></a>Kas Dynamics 365 Finance ja Dynamics 365 Supply Chain Management toetatakse GCC-High's?

Ei. Dynamics 365 Finance ja Dynamics 365 Supply Chain Management neid toetatakse ainult GCC-s.

### <a name="can-i-use-public-azure-devops-with-finance-and-supply-chain-management-in-gcc"></a>Kas GCC-s saab kasutada finants- ja tarneahela juhtimisega avalikkust Azure DevOps?

Jah, võite kasutada avalikke Azure DevOps teenuseid, kui teil ei ole nõudeid lahendusele, mis on sertifitseeritud föderaalse riski- ja loahaldusprogrammi (FEDRAMP) poolt. Teise võimalusena võite kasutada Azure DevOps serverit.

### <a name="can-i-deploy-a-cloud-hosted-environment-tier-1-development-environment-on-an-azure-commercial-subscription"></a>Kas Azure'i kommertstellimusel saab juurutada pilvepõhise keskkonna Tier-1 arenduskeskkonna?

Ei. GCC [LCS](https://gov.lcs.microsoftdynamics.us)-is peate pilve majutatud keskkonna juurutamiseks kasutama Azure Governmenti tellimust.

### <a name="what-can-i-do-if-i-need-a-package-from-the-shared-asset-library-but-it-isnt-available-in-lcs-for-gcc"></a>Mida teha, kui mul on vaja ühisvarateegi paketti, kuid see pole GCC jaoks LCS-is saadaval?

Sama paketi saate alla laadida jagatud varateegist [avalikus LCS-is](https://lcs.dynamics.com). Teise võimalusena aitab teie partner teil paketti alla laadida.

### <a name="is-the-code-upgrade-tool-available-in-gcc"></a>Kas koodi uuendamise tööriist on GCC-s saadaval?

Ei, koodi täiendamise tööriist pole praegu GCC-s saadaval. Siiski saate luua potentsiaalse kliendi projekti avalikus LCS-is [ja](https://lcs.dynamics.com) kasutada koodi täiendamise tööriista. Pange tähele, et te ei saa potentsiaalse kliendi projektides keskkondi juurutada.

### <a name="can-my-partner-open-a-support-ticket-on-my-behalf"></a>Kas mu partner võib minu nimel tugipileti avada?

Jah. Kui aga teie partner kasutab mitte-GCC identiteeti, suunatakse tugipilet avaliku toetuse järjekorda. Soovitame kasutada kliendi GCC õigust LCS-is tugipiletite avamiseks.

## <a name="see-also"></a>Vt ka

- [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government)
- [Ärirakendused USA valitsuse funktsioon kättesaadavus](https://aka.ms/BAPFunctionalParity).
- [Teenuse Lifecycle Services (LCS) kasutusjuhend](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [Pilvjuurutuse ülevaade](../../../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
