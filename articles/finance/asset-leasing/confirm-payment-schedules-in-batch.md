---
title: Vara rentimise maksegraafikute hulgikinnitamine
description: See artikkel selgitab, kuidas kinnitada partiis mitut maksegraafikut.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePaymConfirmationDetails
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: bd75e22f6407d6bc25a78c1dfeacf70022238e94
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895047"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a>Vara rentimise maksegraafikute hulgikinnitamine

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas kinnitada partiis mitut maksegraafikut. Maksegraafikud kinnitatakse kas rendikirje põhiselt või hulgikinnitamise protsessi kaudu. Töölehe kirje saab sisestada ainult kinnitatud maksegraafikuga rendikirjele. Maksegraafiku kinnitamine toimib rentimise finantsteabe lõpliku kinnitamisena. Kõik rendikirje finantsteabe tulevased muudatused (nt maksed ja rendiperiood), moodustavad rendi korrigeerimise ja tuleks sel viisil töödelda.

Mitme maksegraafiku kinnitamiseks toimige järgmiselt.

1. Avage suvand **Vara rentimine \> Perioodiline \> Kinnitamise partii**.
2. Valige lehel **Kinnitamise partii** suvand **Kinnitamise partii**.
3. Kuvatavas dialoogiaknas filtreerige raamatud, mille soovite kinnitada.

    - Kõigi kindlas rendirühmas olevate raamatute kinnitamiseks valige grupp väljal **Rendigrupp**.
    - Konkreetsete raamatute kinnitamiseks valige raamatud väljal **Raamatu ID**.
    - Kõigi raamatute kinnitamiseks lülitage sisse parameeter **Kõigi raamatute jaoks**.

Teave äsja kinnitatud raamatute kohta kuvatakse lehel **Kinnitatud raamatud**. Pärast maksegraafikute kinnitamist saab algse tuvastamise töölehtede kirjed sisestada vastavate rendikirjete suhtes.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
