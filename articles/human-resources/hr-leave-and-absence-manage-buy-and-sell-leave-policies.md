---
title: Puhkuse ostmise ja müümise põhimõtete haldamine
description: Saate võimaldada töötajatel osta ja müüa puhkust rakenduses Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 491d1654bd219b487f95a1eb328e574114ec1f9f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051373"
---
# <a name="manage-buy-and-sell-leave-policies"></a>Puhkuse ostu ja müügi poliitikate haldamine

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Saate lubada töötajatel osta ja müüa puhkust, luues puhkuse ostmise ja müümise poliitika. Saate konfigureerida need poliitikad töövoogude kinnitamiseks kasutamiseks, maksimaalsete summade ja määrade ja ostmise ning müümise määrade määramiseks. 

## <a name="enable-employees-to-buy-and-sell-leave"></a>Töötajatele puhkuse ostu ja müügi lubamine

1. Valige lehel **Puhkuste ja puudumiste parameetrid** suvandite **Luba töötajatele puhkuse ostmine** ja **Luba töötajatele puhkuse müümine** väärtuseks **Jah**.

## <a name="create-a-buy-and-sell-leave-policy"></a>Puhkuse ostmise ja müümise poliitika loomine

1. Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**. 

2. Valige **Puhkuse ostmise ja müümise poliitika**.

3. Valige suvand **Uus**.

4. Sisestage jaotises **Puhkuse ostmise ja müümise poliitika** poliitika **Nimi** ja **Kirjeldus**. 

5. Valige **Poliitika tüüp**. 

   Saadaolevad poliitikatüübid on **Summa** ja **Tundi nädalas**. Valige suvand **Summa**, et sisestada töötajale müümiseks ja ostmiseks lubatud maksimumsummade **Fikseeritud summa**. Kui valite suvandi **Tundi nädalas**, siis kasutatakse poliitika maksimumsumma kindlaks määramiseks töötajale määratud tööaja kalendris määratletud tööaega. 

6. Valige poliitika **Alguskuupäev** ja **Lõppkuupäev**. Puhkuse ostmise või müümise taotlused on esitamiseks saadaval vaid antud ajavahemikus. 

7. Valige poliitika jaoks **Töövoo ID**. Kõik ostu- ja müügitaotlused kasutavad seda töövoogu ülevaatamiseks ja kinnitamiseks. 

8. Valige jaotises **Ostupoliitika** suvand **Täistööaja vaste**, et kasutada maksimumsumma proportsionaalsuse jaotamiseks töötaja ametikoha kohta määratletud täistööaja vastet. Kui poliitika tüüp on **Summa**, siis sisestage **Maksimaalne fikseeritud summa**. 

9. Töötajale puhkuse ostmiseks saadaolevate puhkuse tüüpide lisamiseks valige **Lisa**. Te saate lisada poliitikale mitu puhkuse tüüpi. 

10. Sisestage puhkuse tüübi jaoks **Töötatud kuud**, et lubada määratleda töötajale maksimaalne ostetav summa erinevate töötatud kuude alusel. 

11. Sisestage puhkuse tüübi **Maksimumsumma**. 

12. Sisestage **Määr**, mille alusel töötaja puhkust ostab. 

13. Soovi korral sisestage puhkuse ostmisel kasutatav **Tulukood**. 

14. Soovi korral saate valida, kas soovite kasutada puhkuse tüübi maksimumsumma kindlaks määramiseks täistööaja vastet. 

15. Müügipoliitika loomiseks järgige jaotise **Müügipoliitika** toiminguid 8 kuni 14. 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a>Puhkuse ostmise ja müümise poliitika lisamine puhkuste ja puudumiste plaanile

1. Valige lehel **Puhkus ja puudumine** puhkuste ja puudumiste plaan.

2. Valige jaotises **Reeglid** suvand **Puhkuse ostmise ja müümise poliitika**.

## <a name="see-also"></a>Vt ka

[Puhkuste ja puudumiste ülevaade](hr-leave-and-absence-overview.md)</br>
[Puhkuste ja puudumiste tüüpide konfigureerimine](hr-leave-and-absence-types.md)</br>
[Puhkuse ja puudumise plaanide juurdekasv](hr-leave-and-absence-accrue.md)</br>
[Puhkuse ostmine ja müümine](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]