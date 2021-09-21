---
title: Puhkuse ostmine ja müümine
description: See teema kirjeldab, kuidas esitada ostu- ja müügipuhkuste Dynamics 365 Human Resources taotlusi.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 716afdc4e52c3e4a0432b987cb82077012d4d0c2
ms.sourcegitcommit: a8ac6d9b63eb67d14dd17a086ef4f1eccd7f9fc1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/27/2021
ms.locfileid: "7431506"
---
# <a name="buy-and-sell-leave"></a>Puhkuse ostmine ja müümine

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources aitab edastada puhkuse ostmise ja müümise taotlusi teie ettevõttes häälestatud puhkuse ostmis- ja müümispoliitika alusel.  

## <a name="request-to-buy-leave"></a>Puhkuse ostmise taotlus

1. Tööruumis **Töövõtja iseteenindus** valige suvand **Puhkuse ostmise taotlemine** paanil **Vaba aja saldod**. 

2. Lisage **Puhkuse tüüp** ja sisestage **Summa**, mille eest soovite puhkust osta. 

3. Kui olete taotluse esitamiseks valmis, valige suvand **Esita**. 

Teie saldod kas värskendatakse automaatselt või need läbivad enne värskendamist kinnitustoimingu. See oleneb sellest, kuidas on ostupoliitika konfigureeritud.

## <a name="request-to-sell-leave"></a>Puhkuse müümise taotlus

1. Tööruumis **Töövõtja iseteenindus** valige suvand **Puhkuse müümise taotlemine** paanil **Vaba aja saldod**. 

2. Lisage **Puhkuse tüüp** ja sisestage **Summa**, mille eest soovite puhkust müüa. 

3. Kui olete taotluse esitamiseks valmis, valige suvand **Esita**.

Teie saldod kas värskendatakse automaatselt või need läbivad enne värskendamist kinnitustoimingu. See oleneb sellest, kuidas on ostupoliitika konfigureeritud.


## <a name="troubleshooting"></a>Tõrkeotsing 

Kui ostu või müügi puhkuse taotluse töövoog nurjub, saavad kasutajad, kellel on **EssLeaveBuySellRequestApprover** privileeg, vaadata üle kõikide puhkuse ostu- ja müügitaotluste teatelogi. Selleks minge **Puhkus ja puudumine > Link > Ostu- ja müügitaotluste päringud >Teatelogi** (vasakul üleval). **Teatelogi** näitab kasutajatele, kuidas kandeid töödeldakse ja seostatud töövoo ajalugu.


## <a name="see-also"></a>Vt ka

[Puhkuste ja puudumiste ülevaade](hr-leave-and-absence-overview.md)</br>
[Puhkuse ostu ja müügi poliitikate haldamine](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
