---
title: Soodustuste haldamise parameetrite konfigureerimine ettevõtte kohta
description: Konfigureerige soodustuste halduse parameetreid ettevõtte kohta rakenduses Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2943d0095e4c9421725b90e579b7cbb841038ab7
ms.sourcegitcommit: fd097f6f76f0d8428038fa3655b3188bf093b517
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692741"
---
# <a name="configure-benefits-management-parameters-per-company"></a>Soodustuste haldamise parameetrite konfigureerimine ettevõtte kohta

Iga soodustust pakkuva organisatsiooni jaoks peate konfigureerima soodustuste kinnitusmeilide sätted.

## <a name="configure-confirmation-email-settings"></a>Kinnitusmeilide sätete konfigureerimine

1. Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Human Resourcesi parameetrid**.

2. Määrake vahekaardil **Soodustuste haldus** järgmiste väljade väärtused. 

   | Field | Kirjeldus |
   | --- | --- |
   | **Saada kinnitusmeil** | Kui see funktsioon on sisse lülitatud, saadetakse töövõtjatele kinnitusmeili, kui nad registreerivad soodustuste registreerimise töövõtja iseteeninduse kaudu. |
   | **Kinnitusmeili mall** | Valige organisatsiooni meilisõnumi mall, mida kasutada registreerimise kinnituse saatmisel. Kui te malli ei vali, saadetakse järgmine üldine meilisõnum.<br><br>%EmployeeFirstName%,<br><br>Õnnitleme! Olete soodustuste registreerimise edukalt lõpule viinud.<br><br>Suur tänu!<br>Ettevõtte <Company/Org name> soodustused. |
   | **Vaikimisi meilisõnumi saatja aadress** | Meiliaadress, mida kasutada kinnitusmeili saatmisel. |

3. Valige käsk **Salvesta**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]