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
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 83718856a864123d7941b21c078bcdb96a62cca8
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067575"
---
# <a name="configure-employee-self-service"></a>Töövõtja iseteeninduse konfigureerimine


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Rakenduses Microsoft Dynamics 365 Human Resources saate konfigureerida **Töövõtja iseteeninduses** ülemise taseme navigeerimispaane. Soodustuse plaani paanid juhivad kasutajad soodustuse plaanide juurde, millele nad saavad registreeruda.

## <a name="set-up-a-benefit-plans-tile"></a>Soodustuse plaanide paani häälestamine

1. Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Töövõtja iseteeninduse parameetrid**.

2. Valige vahekaart **Soodustuse plaanide paani seadistamine** ja seejärel valige **Uus**.

3. Määrake järgmiste väljade väärtused.

   | Field | Kirjeldus |
   | --- | --- |
   | **Plaani tüübi kood** | Plaani tüüp, mis kuvatakse, kui see paan on valitud **Soodustuste iseteeninduses**. |
   | **Paani ID** | Paani kordumatu identifikaator. |
   | **Paani sildi tekst** | Tekst, mis kuvatakse paani jaoks Soodustuste **iseteeninduses**. |
   | **Kirjeldus** | Paani kirjeldus. |
   | **Paani taustapilt** | Paani jaoks kasutatava kujutise URL (valikuline). |
   | **Avatud registreerimise jälgimine** | Valige see suvand selle plaanitüübi avatud registreerimise edenemise jälgimiseks. Näiteks võib teil olla loodud plaanid, kus **plaani tüüp = Muu**. Need plaanid võivad olla valikulised plaanid, mille puhul te ei soovi jälgida registreerimise edenemist. Kui te seda plaanitüüpi ei vali, ignoreeritakse seda tüüpi plaani registreerimise edenemise või registreerimise lõpetamise jälgimisel vahekaardil **Ava registreerimine** . See säte rakendub plaani tüübile, mis on valitud kõigi perioodide ja juriidiliste isikute jaoks. |

4. Valige käsk **Salvesta**.

## <a name="set-up-a-flex-credit-plan-tile"></a>Paindliku krediidiga plaani paani häälestamine

1. Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Töövõtja iseteeninduse parameetrid**.

2. Valige vahekaart **Paindliku krediidiga plaani paani seadistamine** ja seejärel valige **Uus**.

3. Määrake järgmiste väljade väärtused.

   | Field | Kirjeldus |
   | --- | --- |
   | **Soodustuse krediidi ID** | Paindkrediidiprogrammi plaanid, mis kuvatakse, kui see paan on valitud **soodustuste iseteeninduses**. |
   | **Paani ID** | Paani kordumatu identifikaator. |
   | **Paani sildi tekst** | Tekst, mis kuvatakse paani jaoks Soodustuste **iseteeninduses**. |
   | **Kirjeldus** | Paani kirjeldus. |
   | **Paani taustapilt** | Paani jaoks kasutatava kujutise URL (valikuline). |
   | **Avatud registreerimise jälgimine** | Valige see suvand selle plaanitüübi avatud registreerimise edenemise jälgimiseks. Näiteks võib teil olla loodud plaanid, kus **plaani tüüp = Muu**. Need plaanid võivad olla valikulised plaanid, mille puhul te ei soovi jälgida registreerimise edenemist. Kui te seda plaanitüüpi ei vali, ignoreeritakse seda tüüpi plaani registreerimise edenemise või registreerimise lõpetamise jälgimisel vahekaardil **Ava registreerimine** . See säte rakendub plaani tüübile, mis on valitud kõigi perioodide ja juriidiliste isikute jaoks. |

4. Valige käsk **Salvesta**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
