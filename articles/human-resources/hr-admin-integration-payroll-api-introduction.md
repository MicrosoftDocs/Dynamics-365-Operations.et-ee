---
title: Palgaarvestuse integratsiooni API tutvustus
description: See artikkel kirjeldab Palga Dynamics 365 Human Resources integratsiooni API-d.
author: twheeloc
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 33c17dd25477b2c34470fe16ce2927c1781ae147
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846382"
---
# <a name="payroll-integration-api-introduction"></a>Palgaarvestuse integratsiooni API tutvustus


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See dokument kirjeldab Dynamics 365 Human Resources palgaarvestuse integratsiooni API-d. API võimaldab sujuvaid otsast otsani integratsioone personaliosakonna ja partnerite palgasüsteemide vahel. Integreeritud kogemus algab personaliosakonna töötaja profiili, palga ja mahaarvamise ning panuse teabega. Kui palkate töötaja ja sisestate nõutava profiili ning sisestate teabe personaliosakonna süsteemi, tõmbab palgasüsteem selle teabe palgaarvestuse töötlemisel. Võetakse ka kõiki töötajale tehtud uuendusi või palgateavet hilisemaks maksekäitumiseks.

[![Palgaarvestuse integratsiooni voog.](media/hr-admin-integration-payroll-api-introduction-flow.png)](media/hr-admin-integration-payroll-api-introduction-flow-2.png#lightbox)

Integratsiooni lubamiseks on personaliosakond sisaldanud järgmisi komponente.

- [Funktsioon töötaja staatuse muutmiseks kui "valmis makseks".](hr-compensation-payroll.md)
- Integratsiooni API, mis avab uued funktsioonid rakenduste integreerimiseks.

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

See API on ehitatud rakendusele Microsoft Dataverse (varem Common Data Service). Kogu RESTful interaktsioon selle API-ga toimub Microsoft Dataverse'i veebi API kaudu, mis kasutab OData. See API on Dataverse'i Web API alamkogum. Dataverse'i WEB API määratleb sellised omadused nagu autentimine, SLA-d, partii, samaaegsuse kontrolli ja tõrketöötluse.

Lisateavet Microsoft Dataverse'i Web API kohta leidke alpoolt.

- [Mis on Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)
- [Microsoft Dataverse'i Web API kasutamine](/powerapps/developer/data-platform/webapi/overview)
- [Microsoft Dataverse'i arendaja juhend](/powerapps/developer/data-platform)

See dokumentatsioon sisaldab üksikasju ja arendaja juhendeid Dataverse Web API kasutamiseks, sh järgmisi teemasid.

- [Autendi Microsoft Dataverse-ga üle veebi-API](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [Soorita toimingud veebi API abil](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [Kasutage veebi API-s Postmani](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [Kasuta muudatuste jälitamist andmete sünkroonimiseks välissüsteemidega](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>Virtuaalsed tabelid rakendusele Human Resources Dataverse'is

Palgaarvestuse integratsiooni API lõpp-punktid kasutavad rakenduse Microsoft Dataverse virtuaalse tabeli platvormi võimalusi. Vaikimisi ei juurutata virtuaalseid tabeleid ja nendega seotud API-lõpp-punkte Human Resources'i keskkondades, võimaldades organisatsioonidel määrata, millised OData lõpp-punktid keskkonnaga kokku puutuvad. API kasutamiseks peavad keskkonna jaoks olema loodud virtuaalsed tabelid rakenduse Human Resources olemite jaoks.

Lisateavet API jaoks virtuaaltabelite loomise kohta leiate jaotisest [Dataverse'i virtuaalsete tabelite konfigureerimine](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="data-model"></a>Andmemudel

Järgmine diagramm illustreerib seoseid API sees. Mitmetel tüüpidel on võõrvõtmeid rakenduse Human Resources teiste, olemasolevate olemite jaoks, mida siin ei ole kujutatud. See dokument annab teavet üksuste kohta, mis on integratsioonistsenaariumide palgaarvestusel spetsiifilised. Siiski on Dataverse'i Web APIs mitmeid teisi olemeid personaliosakonna jaoks, mis võivad samuti olla teie integratsioonile asjakohased. Mõnedele neile üksustele viidatakse võõrvõtme seostes või navigeerimisatribuutides.

[![Palgaarvestuse integratsiooni API andmemudel.](media/hr-admin-payroll-api-data-model.png)](media/hr-admin-payroll-api-data-model.png#lightbox)

## <a name="payroll-employee-and-related-entities"></a>Palgatöötaja ja seotud üksused

Üksused:

- [Palgaarvestuse töövõtja](hr-admin-integration-payroll-api-payroll-employee.md)
- [Palgaarvestuse töötaja aadress](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [Palgaarvestuse põhipalgaplaan](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md)
- [Palgaarvestuse hüvitise muutlik plaan](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md)
- [Palga positsiooni töö](hr-admin-integration-payroll-api-payroll-position-job.md)
- [Palga positsioon](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a>Vt ka

[Palgaarvestuse üksuste loomine ja ülevaatus](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[Human Resourcesi parameetrite konfigureerimine](hr-setup-parameters.md)<br>
[Human Resourcesi (personaliosakonna) ühiskasutuses parameetrite konfigureerimine](hr-setup-shared-parameters.md)<br>
[Mis on Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Microsoft Dataverse'i Web API kasutamine](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
