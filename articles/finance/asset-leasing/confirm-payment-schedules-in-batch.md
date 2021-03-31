---
title: Vara rentimise maksegraafikute hulgikinnitamine
description: Selles teemas selgitatakse, kuidas mitu maksegraafikut hulgikinnitada.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0275fda306a58159a982b342622b9b6a18fa5b71
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225509"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a>Vara rentimise maksegraafikute hulgikinnitamine

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas mitu maksegraafikut hulgikinnitada. Maksegraafikud kinnitatakse kas rendikirje põhiselt või hulgikinnitamise protsessi kaudu. Töölehe kirje saab sisestada ainult kinnitatud maksegraafikuga rendikirjele. Maksegraafiku kinnitamine toimib rentimise finantsteabe lõpliku kinnitamisena. Kõik rendikirje finantsteabe tulevased muudatused (nt maksed ja rendiperiood), moodustavad rendi korrigeerimise ja tuleks sel viisil töödelda.

Mitme maksegraafiku kinnitamiseks toimige järgmiselt.

1. Avage suvand **Vara rentimine \> Perioodiline \> Kinnitamise partii**.
2. Valige lehel **Kinnitamise partii** suvand **Kinnitamise partii**.
3. Kuvatavas dialoogiaknas filtreerige raamatud, mille soovite kinnitada.

    - Kõigi kindlas rendirühmas olevate raamatute kinnitamiseks valige grupp väljal **Rendigrupp**.
    - Konkreetsete raamatute kinnitamiseks valige raamatud väljal **Raamatu ID**.
    - Kõigi raamatute kinnitamiseks lülitage sisse parameeter **Kõigi raamatute jaoks**.

Teave äsja kinnitatud raamatute kohta kuvatakse lehel **Kinnitatud raamatud**. Pärast maksegraafikute kinnitamist saab algse tuvastamise töölehtede kirjed sisestada vastavate rendikirjete suhtes.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]