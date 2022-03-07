---
title: Te ei leia varude töölehel ripploendi välja „Töövoog”
description: Te ei leia töölehelt ripploendi välja "Töövoog" või ei ole seotud töövoo toimingud saadaval
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8b2772a75c2388f4d78a459f9dfb72ad7c1be4ab
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476102"
---
# <a name="you-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a>Te ei leia varude töölehel ripploendi välja „Töövoog”

## <a name="symptoms"></a>Sümptomid

Te ei leia töölehelt ripploendi välja **Töövoog** või ei ole seotud töövoo toimingud saadaval.

See probleem võib esineda kolmel põhjusel, nagu kirjeldatud järgmistes alamjaotistes.

## <a name="resolution-1"></a>Lahendus 1

Kui see probleem tekib kõigil kasutajatel, võib selle põhjuseks olla, et kinnitamise töövoog pole töölehe nimele määratud. Probleemi lahendamiseks tehke järgmist.

1. Avage **Varude haldus &gt; Seadistus &gt; Töölehtede nimed &gt; Varud**.
1. Valige sellel paanil töölehe nimi, et avada selle sätted.
1. Määrake kiirkaardi **Üldine** suvandi **Kinnituse töövoog** väärtuseks *Jah*. Kui teil palutakse muudatus kinnitada, klõpsake valikut **Jah**.
1. Väljal **Töövoog** valige töövoog, mida soovite valitud töölehe nime jaoks kasutada.

## <a name="resolution-2"></a>Lahendus 2

Kui teie töövoog kasutab kohandatud koodi, võivad ilmneda probleemid pärast süsteemi täiendamist. Näiteks võidakse töölehe töövoos nupp **Esita** muutuda halliks, nii et te ei saa seda esitamise kinnitamiseks valida.

Kui nupp **Esita** on hall, on võimalik, et teie töövoog on kohandatud, mis tähendab, et töövoo meetodit `canSubmitToWorkflow()` atribuudis `FormDataUtil` laiendati. Selle probleemi lahendamiseks muutke viisi, kuidas te atribuudi `canSubmitToWorkflow()` meetodit laiendate, et kasutada järgmises näites.

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

## <a name="resolution-3"></a>Lahendus 3

Kui probleem esineb vaid teatud kindlatel kasutajatel, ei pruugi nendel kasutajatel olla turvaõigusi, mis on vajalikud varude töölehtedel töövoo toimingute käivitamiseks. Veenduge, et igal mõjutatud kasutajal oleks turvalisuse privileeg *Varude töölehe töövoo haldamine*. Vaikimisi määratakse see privileeg kohustusele, mis on sama nimega, ja see kohustus rakendatakse rollidele *Laotöötaja* ja *Lao juhataja*.
