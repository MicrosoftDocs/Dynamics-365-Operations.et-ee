---
title: Täpsema laohalduse kasutuselevõtmine ja sellesse migreerumine
description: Selles teemas kirjeldatakse, kuidas lahendada täpsema laohalduse kasutuselevõtul ja sellesse migreerumisel tekkivaid probleeme.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: c07c5894f340fde2834e95d53fa390ec5789feeca9b3902e56c333da0d143f5b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747789"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a>Täpsema laohalduse kasutuselevõtmine ja sellesse migreerumine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas lahendada täpsema laohalduse kasutuselevõtul ja sellesse migreerumisel tekkivaid probleeme.

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a>Kuvatakse järgmine tõrketeade: "java.security.cert.certPathValidatorException: usaldusankru sertifitseerimise teed ei leitud."

### <a name="issue-description"></a>Probleemi kirjeldus

See tõrketeade kuvatakse mobiilirakenduses Warehouse Management, kuna iseseisvalt allkirjastatud sertifikaate ei usaldata Android 8+ asutusesiseses keskkonnas.

### <a name="issue-resolution"></a>Probleemi lahendamine

Kasutage välist (avaliku) sertifitseerimiskeskust (CA). Selle probleemi parandus on saadaval laorakenduse versioonis 1.9.0.0. Lisateavet selle probleemi ja lahendamise kohta vt teemast [Lao mobiilirakenduse Warehouse Management ühenduse probleemide tõrkeotsing](troubleshoot-warehouse-app-connection.md).

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a>Mis on kinnitatud protsess baaslaost täpsemale laole liikumiseks?

### <a name="issue-description"></a>Probleemi kirjeldus

Töötate praegu laos/laohalduses ja kasutate põhivoogude funktsiooni ning soovite migreeruda täpsemasse lattu mobiilsete seadmete, voogude ja töö kasutamiseks. Kuid teil esineb probleeme, kui proovite seda käiku teha. Näiteks ei saa te oma tooteid muuta nii, et need kasutaksid ladustamise dimensioone (sait, ladu ja asukoht), sest toodetel on nende vastu kanded. Seetõttu peate õppima kinnitatud protsessi baaslaost täpsemale laole liikumiseks.

### <a name="issue-resolution"></a>Probleemi lahendamine

Lisateavet protsessi kohta, kuidas liikuda baaslaost täpsemasse lattu, leiate järgmistest blogipostitustest ja dokumentatsioonist:

- [Võimalda olemasolevate kaupadele ja ladudele laohaldusprotsessid](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [Microsoft Dynamics AX WMS-i migratsioon uutele R3 lao ja transpordi funktsioonidele](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [WMSI/WMS2 kauba migreerimine](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [Laohalduse uuendamine rakendusest Microsoft Dynamics AX 2012 rakendusse Supply Chain Management](./upgrade-migration-warehouse-management-processes.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]