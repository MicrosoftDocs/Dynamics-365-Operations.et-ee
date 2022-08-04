---
title: Koormate ja saadetiste planeerimine koorma planeerimise töölaua abil
description: See artikkel näitab, kuidas kasutada koorma planeerimise töölauda müügitellimuse koorma loomiseks.
author: Mirzaab
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e53b7667dd4589a7c6c14b8aaf8ba51017eee0d
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068326"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>Koormate ja saadetiste planeerimine koorma planeerimise töölaua abil

[!include [banner](../../includes/banner.md)]

See artikkel näitab, kuidas kasutada koorma planeerimise töölauda müügitellimuse koorma loomiseks. Eeltingimusena loome esmalt müügitellimuse. See protseduur on osa transpordikoordinaatori igapäevatööst. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="create-a-sales-order"></a>Loo müügitellimus
1. Avage **Navigeerimispaan > Moodulid > Müügireskontro > Tellimused > Kõik müügitellimused**.
2. Valige suvand **Uus**.
3. Valige otsingu avamiseks väljal **Kliendi konto** ripploendi nupp.
4. Valige konto **US-004**.
5. Valige nupp **OK**.
6. Valige otsingu avamiseks väljal **Kaubakood** ripploendi nupp.
7. Valige üksus **A0001**. **A0001** on transpordihaldusele lubatud.  
8. Valige väljal **Koht** ripploendi nupp, et avada otsing, ja seejärel valige üksus.
9. Sisestage arv väljale **Kogus**.
10. Selle näite korral sisestage väljale **Ladu** tekst „24“. See ladu on lubatud transpordihalduse ja laohaldusprotsesside jaoks (WMS).  
11. Valige käsk **Salvesta**.
12. Sulgege leht.

## <a name="create-a-new-load"></a>Uue koorma loomine
1. Avage **Navigeerimispaan > Moodulid > Transpordihaldus > planeerimine > Koormuse planeerimise töölaud**.
2. Valige vahekaart **Müügiread**. Nüüd saate luua koormuse äsja loodud müügitellimuse jaoks. Koormaid saab luua ostutellimuste, üleviimistellimuste ja müügitellimuste pakkumise ja nõudluse põhjal.  
3. Valige toimingupaanil **Pakkumine ja nõudlus**.
4. Valige **Uuele koormusele**.
5. Valige väljal **Koormuse malli ID** otsingu avamiseks ripploendi nupp. Koorma mall määratleb kogu koorma maksimaalse kaalu ja mahu mõõtmed. Näiteks võib koorma mall tähistada konteineri või veoauto suurust. Valige kaup.
6. Valige nupp **OK**.

## <a name="rate-and-route-the-load"></a>Koorma hindamine ja marsruudi määramine
1. Valige **Hindamine ja marsruutimine**.
2. Valige **Hinda marsruudi töölauda**.
3. Valige **Hinda poodi**.
4. Otsige loendist ja valige soovitud kirje.
5. Valige **Määra**.
6. Sulgege leht.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]