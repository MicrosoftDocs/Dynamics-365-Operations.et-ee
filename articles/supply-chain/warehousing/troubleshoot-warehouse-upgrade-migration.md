---
title: Täpsema laohalduse kasutuselevõtmine ja sellesse migreerumine
description: Selles teemas kirjeldatakse, kuidas lahendada täpsema laohalduse kasutuselevõtul ja sellesse migreerumisel tekkivaid probleeme.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d50c6d75ec7cc98109cf81c38ff42b4d2b105b0c
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645813"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a>Täpsema laohalduse kasutuselevõtmine ja sellesse migreerumine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas lahendada täpsema laohalduse kasutuselevõtul ja sellesse migreerumisel tekkivaid probleeme.

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a>Kuvatakse järgmine tõrketeade: "java.security.cert.certPathValidatorException: usaldusankru sertifitseerimise teed ei leitud."

### <a name="issue-description"></a>Probleemi kirjeldus

See tõrketeade kuvatakse laorakenduses, kuna iseseisvalt allkirjastatud sertifikaate ei usaldata Android 8+ asutusesiseses keskkonnas.

### <a name="issue-resolution"></a>Probleemi lahendamine

Kasutage välist (avaliku) sertifitseerimiskeskust (CA). Selle probleemi parandus on saadaval laorakenduse versioonis 1.9.0.0. Lisateavet selle probleemi ja lahendamise kohta vt teemast [Laorakenduse ühenduse probleemide tõrkeotsing](troubleshoot-warehouse-app-connection.md).

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a>Mis on kinnitatud protsess baaslaost täpsemale laole liikumiseks?

### <a name="issue-description"></a>Probleemi kirjeldus

Töötate praegu laos/laohalduses ja kasutate põhivoogude funktsiooni ning soovite migreeruda täpsemasse lattu mobiilsete seadmete, voogude ja töö kasutamiseks. Kuid teil esineb probleeme, kui proovite seda käiku teha. Näiteks ei saa te oma tooteid muuta nii, et need kasutaksid ladustamise dimensioone (sait, ladu ja asukoht), sest toodetel on nende vastu kanded. Seetõttu peate õppima kinnitatud protsessi baaslaost täpsemale laole liikumiseks.

### <a name="issue-resolution"></a>Probleemi lahendamine

Lisateavet protsessi kohta, kuidas liikuda baaslaost täpsemasse lattu, leiate järgmistest blogipostitustest ja dokumentatsioonist:

- [Võimalda olemasolevate kaupadele ja ladudele laohaldusprotsessid](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [Microsoft Dynamics AX WMS-i migratsioon uutele R3 lao ja transpordi funktsioonidele](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [WMSI/WMS2 kauba migreerimine](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [Laohalduse uuendamine rakendusest Microsoft Dynamics AX 2012 rakendusse Supply Chain Management](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/upgrade-migration-warehouse-management-processes)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]