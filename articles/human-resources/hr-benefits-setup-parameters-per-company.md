---
title: Soodustuste halduse parameetrite konfigureerimine ettevõtte alusel
description: See teema kirjeldab, kuidas konfigureerida soodustuste halduse parameetreid ettevõtte kohta rakenduses Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 8/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f6b3f068c9d3198afa8cd10aaa14bbc7ec9ef3c4
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065814"
---
# <a name="configure-benefits-management-parameters-per-company"></a>Soodustuste haldamise parameetrite konfigureerimine ettevõtte kohta


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Iga soodustust pakkuva organisatsiooni jaoks peate konfigureerima soodustuste kinnitusmeilide sätted.

## <a name="configure-confirmation-email-settings"></a>Kinnitusmeilide sätete konfigureerimine

1. Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Human Resourcesi parameetrid**.

2. Määrake vahekaardil **Soodustuste haldus** järgmiste väljade väärtused. 

   | Field | Kirjeldus |
   | --- | --- |
   | **Saada kinnitusmeil** | Kui see funktsioon on sisse lülitatud, saadetakse töövõtjatele kinnitusmeili, kui nad registreerivad soodustuste registreerimise **Töövõtja iseteeninduse** kaudu. |
   | **Kinnitusmeili mall** | Valige organisatsiooni meilisõnumi mall, mida kasutada registreerimise kinnituse saatmisel. Kui te malli ei vali, saadetakse järgmine üldine meilisõnum.<br><br>%EmployeeFirstName%,<br><br>Õnnitleme! Olete soodustuste registreerimise edukalt lõpule viinud.<br><br>Suur tänu!<br>Ettevõtte <Company/Org name> soodustused. |
   | **Vaikimisi meilisõnumi saatja aadress** | Meiliaadress, mida kasutada kinnitusmeili saatmisel. |

3. Valige käsk **Salvesta**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
