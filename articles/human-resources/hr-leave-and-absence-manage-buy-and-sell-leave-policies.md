---
title: Puhkuse ostmise ja müümise põhimõtete haldamine
description: Saate võimaldada töötajatel osta ja müüa puhkust rakenduses Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9db86f2a482e7a1c1eee854958cb3f097d6baf61
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888813"
---
# <a name="manage-buy-and-sell-leave-policies"></a>Puhkuse ostu ja müügi poliitikate haldamine

>[!Important]
>Selles artiklis märgitud funktsioonid on klientide jaoks praegu saadaval eraldiseisev Dynamics 365 Human Resources. Osa või kõik funktsioonid on saadaval osana Finance'i taristu tulevasest väljalaskest pärast Finance'i versiooni 10.0.26.


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
