---
title: Puhkuse ostmise ja müümise põhimõtete haldamine
description: Saate võimaldada töötajatel osta ja müüa puhkust rakenduses Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 859445f2b6e980b5960e512e69129f6a8fc6df2b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429009"
---
# <a name="manage-buy-and-sell-leave-policies"></a>Puhkuse ostmise ja müümise põhimõtete haldamine

[!include [banner](includes/preview-feature.md)]

Saate lubada töötajatel osta puhkust, luues puhkuse ostmise poliitika.  

## <a name="enable-employees-to-buy-and-sell-leave"></a>Töötajatele puhkuse ostu ja müügi lubamine

1. Valige lehel **Puhkuste ja puudumiste parameetrid** suvandi **Luba töötajatele puhkuse ostmine** väärtuseks **Jah**. 

## <a name="create-a-buy-leave-policy"></a>Puhkuse ostmise poliitika loomine

1. Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**. 

2. Valige **Puhkuse ostmise ja müümise poliitika**.

3. Valige suvand **Uus**.

4. Sisestage jaotises **Puhkuse ostmise ja müümise poliitika** poliitika **Nimi** ja **Kirjeldus**. 

5. Valige **Poliitika tüüp**. 

   Saadaolevad poliitikatüübid on **Summa** ja **Tundi nädalas**. Valige suvand **Summa**, et sisestada töötajale müümiseks ja ostmiseks lubatud maksimumsummade **Fikseeritud summa**. Kui valite suvandi **Tundi nädalas**, siis kasutatakse poliitika maksimumsumma kindlaks määramiseks töötajale määratud tööaja kalendris määratletud tööaega. 

6. Valige poliitika **Alguskuupäev** ja **Lõppkuupäev**. Puhkuse ostmise või müümise taotlused on esitamiseks saadaval vaid antud ajavahemikus. 

7. Valige jaotises **Ostupoliitika** suvand **Täistööaja vaste**, et kasutada maksimumsumma proportsionaalsuse jaotamiseks töötaja ametikoha kohta määratletud täistööaja vastet. Kui poliitika tüüp on **Summa**, siis sisestage **Maksimaalne fikseeritud summa**. 

8. Töötajale puhkuse ostmiseks saadaolevate puhkuse tüüpide lisamiseks valige **Lisa**. Te saate lisada poliitikale mitu puhkuse tüüpi. 

9. Sisestage puhkuse tüübi jaoks **Töötatud kuud**, et lubada määratleda töötajale maksimaalne ostetav summa erinevate töötatud kuude alusel. 

10. Sisestage puhkuse tüübi **Maksimumsumma**. 

11. Sisestage **Määr**, mille alusel töötaja puhkust ostab. 

12. Soovi korral sisestage puhkuse ostmisel kasutatav **Tulukood**. 

13. Soovi korral saate valida, kas soovite kasutada puhkuse tüübi maksimumsumma kindlaks määramiseks täistööaja vastet. 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a>Puhkuse ostmise ja müümise poliitika lisamine puhkuste ja puudumiste plaanile

1. Valige lehel **Puhkus ja puudumine** puhkuste ja puudumiste plaan.

2. Valige jaotises **Reeglid** suvand **Puhkuse ostmise ja müümise poliitika**.

## <a name="see-also"></a>Vt ka

[Puhkuste ja puudumiste ülevaade](hr-leave-and-absence-overview.md)</br>
[Puhkuste ja puudumiste tüüpide konfigureerimine](hr-leave-and-absence-types.md)</br>
[Puhkuse ja puudumise plaanide juurdekasv](hr-leave-and-absence-accrue.md)</br>
[Puhkuse ostmine ja müümine](hr-employee-self-service-buy-sell-leave.md)

