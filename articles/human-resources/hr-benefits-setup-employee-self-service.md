---
title: Töötaja iseteeninduse konfigureerimine
description: Rakenduses Microsoft Dynamics 365 Human Resources saate konfigureerida töövõtja iseteeninduses ülemise taseme navigeerimispaane.
author: twheeloc
ms.date: 12/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d7ddb1f1ea74a16265dac701151b2c25a4f9d4dc
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687159"
---
# <a name="configure-employee-self-service"></a>Töövõtja iseteeninduse konfigureerimine


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Rakenduses Microsoft Dynamics 365 Human Resources saate konfigureerida **Töövõtja iseteeninduses** ülemise taseme navigeerimispaane. Soodustuse plaani paanid juhivad kasutajad soodustuse plaanide juurde, millele nad saavad registreeruda.

## <a name="set-up-a-benefit-plans-tile"></a>Soodustuse plaanide paani häälestamine

1. Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Töövõtja iseteeninduse parameetrid**.

2. Valige vahekaart **Soodustuse plaanide paani seadistamine** ja seejärel valige **Uus**.

3. Määrake järgmiste väljade väärtused.

   | Väli | Kirjeldus |
   | --- | --- |
   | **Plaani tüübi kood** | Plaani tüüp, mis kuvatakse, kui see paani on valitud valikus **Soodustused iseteenindus**. |
   | **Paani ID** | Paani kordumatu identifikaator. |
   | **Paani sildi tekst** | Paani jaoks kuvav tekst soodustuste **iseteeninduses**. |
   | **Kirjeldus** | Paani kirjeldus. |
   | **Paani taustapilt** | Paani jaoks kasutatava kujutise URL (valikuline). |
   | **Jälgi avatud registreerimist** | Valige see suvand, et jälgida selle plaanitüübi avatud registreerimise edenemist. Näiteks võib olla loodud plaane, kus **Plaani tüüp = Muu**. Need plaanid võivad olla valikulised plaanid, mille puhul te ei soovi jälgida registreerimise edenemist. Kui te seda plaanitüüpi ei vali, **ignoreeritakse seda tüüpi plaani registreerimiste edenemise või registreerimise lõpetamise jälgimisel vahekaardil Avatud** registreerimine. See säte rakendub plaani tüübile, mis valitakse kõigi perioodide ja juriidiliste isikute puhul. |

4. Valige käsk **Salvesta**.

## <a name="set-up-a-flex-credit-plan-tile"></a>Paindliku krediidiga plaani paani häälestamine

1. Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Töövõtja iseteeninduse parameetrid**.

2. Valige vahekaart **Paindliku krediidiga plaani paani seadistamine** ja seejärel valige **Uus**.

3. Määrake järgmiste väljade väärtused.

   | Väli | Kirjeldus |
   | --- | --- |
   | **Soodustuse krediidi ID** | Paindkrediidiprogrammi plaanid, mis kuvatakse, kui see paani valitakse valikus Soodustused **iseteenindus**. |
   | **Paani ID** | Paani kordumatu identifikaator. |
   | **Paani sildi tekst** | Paani jaoks kuvav tekst soodustuste **iseteeninduses**. |
   | **Kirjeldus** | Paani kirjeldus. |
   | **Paani taustapilt** | Paani jaoks kasutatava kujutise URL (valikuline). |
   | **Jälgi avatud registreerimist** | Valige see suvand, et jälgida selle plaanitüübi avatud registreerimise edenemist. Näiteks võib olla loodud plaane, kus **Plaani tüüp = Muu**. Need plaanid võivad olla valikulised plaanid, mille puhul te ei soovi jälgida registreerimise edenemist. Kui te seda plaanitüüpi ei vali, **ignoreeritakse seda tüüpi plaani registreerimiste edenemise või registreerimise lõpetamise jälgimisel vahekaardil Avatud** registreerimine. See säte rakendub plaani tüübile, mis valitakse kõigi perioodide ja juriidiliste isikute puhul. |

4. Valige käsk **Salvesta**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
