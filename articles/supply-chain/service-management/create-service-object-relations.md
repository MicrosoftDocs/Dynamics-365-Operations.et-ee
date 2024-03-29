---
title: teenusobjektide seoste loomine
description: See artikkel kirjeldab, kuidas luua teenuseobjekti seoseid teenuselepingu ja teenusetellimuse jaoks.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4d9424b5678a6f37d46203e5d4e359b020fda7a
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016966"
---
# <a name="create-service-object-relations"></a>teenusobjektide seoste loomine 

[!include [banner](../includes/banner.md)]


See artikkel kirjeldab, kuidas luua teenuseobjekti seoseid teenuselepingu ja teenusetellimuse jaoks. Teenuseobjekti seose loomisel seostate teenuseobjekti teenuseleppe või teenusetellimusega. Kui klient taotleb teenust kauba puhul, mis on teenuseobjekti, saate valida teenuseobjekti seoste loendist.

## <a name="create-a-service-object-relation-for-a-service-agreement"></a>Teenuseobjekti seose loomine teenuseleppe jaoks

Teenuseleppe jaoks teenuseobjekti seose loomiseks tehke järgmist.

1.  Klõpsake teenusehalduse **teenuseleppeid** \> **Teenuselepped.** \> **·**

2.  Valige loendis **Hoolduslepped** olemasolev hoolduslepe või klõpsake uue hooldusleppe loomiseks valikut **Uus**.

3.  Klõpsake vormi **Hoolduslepped** **toimingupaani** vahekaardi **Hoolduslepe** grupis **Seosed** valikut **Teenuse objektid**.

4.  Klõpsake vormil **Teenuse objektid** valikut **Uus** ja seejärel valige hooldusleppe jaoks hooldusobjekt.

5.  Hooldusleppele mallkoosluse (BOM) määramiseks klõpsake valikut **Funktsioonid** ja seejärel valige **Lisa mallkooslus**. Valige mall vormi **Lisa mallkooslus** väljal **Mallkooslus**. 

## <a name="create-a-service-object-relation-for-a-service-order"></a>Teenuseobjekti seose loomine teenusetellimuse jaoks

Teenusetellimuse jaoks teenuseobjekti seose loomiseks tehke järgmist.

1.  Klõpsake **teenusehalduse teenusetellimustel** \> **teenusetellimused.** \> **·**

2.  Valige loendis **Hooldustellimused** olemasolev hooldustellimus või looge uus.

3.  Klõpsake vormi **Hooldustellimused** **toimingupaani** vahekaardi **Hooldustellimus** grupis **Seosed** valikut **Teenuse objektid**.

4.  Klõpsake vormil **Teenuse objektid** valikut **Uus** ja seejärel valige hooldustellimuse jaoks hooldusobjekt.

5.  Hooldusleppele mallkoosluse määramiseks klõpsake valikut **Funktsioonid** ja seejärel valige **Lisa mallkooslus**. Valige mall vormi **Lisa mallkooslus** väljal **Mallkooslus**. 


## <a name="see-also"></a>Vt ka

[Teenuseobjektide ülevaade](service-objects.md)

[Hooldusobjekti seosed](service-object-relations.md)

[Mallkooslused](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]