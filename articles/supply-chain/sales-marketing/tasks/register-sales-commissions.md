---
title: Müügi komisjonitasude registreerimine
description: See artikkel selgitab, kuidas müügi komisjonitasu arvutatakse ja registreeritakse.
author: Henrikan
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher, CustClassificationGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b15ca78da14068fd2f3275e7aff04852625db7ee
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862507"
---
# <a name="register-sales-commissions"></a>Müügi komisjonitasude registreerimine

[!include [banner](../../includes/banner.md)]

See artikkel selgitab, kuidas müügi komisjonitasu arvutatakse ja registreeritakse. Saate seda protseduuri käitada demoettevõtte USMF-i andmetega või oma andmetega. Enne selle juhendi avamist käivitage juhend „Müügi komisjonitasu reeglite seadistamine” veendumaks, et teil on kõik vajalikud komisjonitasu arvutused seadistatud.

Märkige üles komisjonitasu töötlemiseks valitud kliendi ja kauba koodid ning kasutage neid, kui teil palutakse selles juhendis luua müügitellimus.


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a>Müügiisikule komisjonitasu kvalifitseeriva müügitellimuse arveldamine
1. Avage navigeerimispaanil **Moodulid > Müük ja turundus > Müügitellimused > Kõik müügitellimused**.
2. Valige suvand **Uus**.
3. Väljal **Kliendi konto** valige rippmenüüst soovitud kirje.
4. Valige nupp **OK**.
5. Toimingupaanil valige **Suvandid**.
6. Valige **Muuda vaadet**.
7. Valige **Päise vaade**.
8. Laiendage jaotist **Seadistus**.

    - Väärtus väljal **Müügigrupp** esindab rühma, millele on määratud üks või enam müügiesindajat. Grupis olevad inimesed on need, kes saavad tellimuse arveldamisel komisjonitasu eelmääratletud määrade ja jaotuse järgi.   
    - Väärtus kopeeritakse kliendikaardilt, kuid seda saab soovi korral muuta.  
    - Müügigrupp kopeeritakse ka müügitellimuse reale. Saate seda muuta, nii et see võib päise ja/või ridade vahel erineda.  
    - Väärtus väljal **Komisjonitasu grupp** esindab rühma, mille olete loonud ühe või enama kliendiga, eesmärgiga jälgida komisjonitasusid.   
    - Väärtus kopeeritakse kliendikaardilt, kuid seda saab soovi korral muuta.   

9. Toimingupaanil valige **Suvandid**.
10. Valige **Muuda vaadet**.
11. Valige **Reavaade**.
12. Välja **Kaubakood** rippmenüüst valige kaup, millele olete seadistanud komisjonitasud. 
13. Sisestage arv väljale **Kogus**. Märkige üles rea netosumma. See tähistab müügitulu, mis siintoodud näites on komisjonitasu arvutamise aluseks.  
14. Valige käsk **Salvesta**.
15. Toimingupaanil valige **Arve**.
16. Valige **Arve**.
17. Laiendage jaotist **Parameetrid**.
18. Valige väljal **Kogus** suvand **Kõik**.
19. Valige väärtus **Jah** väljal **Sisestamine**.
20. Valige **OK** seejärel valige järgmisel paanil **OK**. Kande sisestamiseks võib kuluda ligikaudu minut. Oodake, kuni töötlemine on lõpule viidud, ja ärge lehte sulgege.  

## <a name="review-the-registered-sales-commissions"></a>Registreeritud müügi komisjonitasude ülevaatamine
1. Toimingupaanil valige **Arve** seejärel valige uuesti **Arve**.
2. Toimingupaanil valige **Arve** seejärel valige **Komisjonitasude kanded**.

    - Vahekaardil **Ülevaade** kuvatakse read, mis esindavad müügiesindajatele makstavate komisjonitasude summasid, kes on seotud müügitellimusega, mille kohta on arve esitatud. Vaadakem üksikasjad üle.  
    - Kui kasutasite juhendit "Müügi komisjonitasude reeglite seadistamine", et seadistada rühm **Komisjonitasude müük**, on kaks müügiisikut, kes saavad müügi komisjonitasu ja komisjonitasu jagatakse nende vahel võrdselt.  
    - Selle näite puhul arvutatakse komisjonitasu kogusumma protsendina müügitulust (tellimuserea netosummast).  
3. Sulgege leht.
4. Valige **Kanne**. Saate üle vaadata komisjonitasu summade kandeid, mis on sisestatud eelmääratletud komisjonitasu kulukontodele ja komisjonitasu ostureskontrotele.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]