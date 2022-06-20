---
title: Puhkuse ostmine ja müümine
description: See artikkel kirjeldab, kuidas esitada ostu- ja müügipuhkuste taotlusi Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a6d38a69a73ce14f099beb6b6b560bf6c5686b0c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875709"
---
# <a name="buy-and-sell-leave"></a>Puhkuse ostmine ja müümine


>[!Important]
>Selles artiklis märgitud funktsioonid on klientide jaoks praegu saadaval eraldiseisev Dynamics 365 Human Resources. Osa või kõik funktsioonid on saadaval osana Finance'i taristu tulevasest väljalaskest pärast Finance'i versiooni 10.0.26.

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
