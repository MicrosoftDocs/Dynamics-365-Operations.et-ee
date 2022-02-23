---
title: Käibemaksu tasumise printimine koodide aruande järgi
description: Selles teemas antakse teavet seadistuste ja toimingute kohta, mis on nõutavad käibemaksu tasumise printimiseks koodide aruande järgi arvestus- või maksukoodi valuutas.
author: anasyash
manager: AnnBe
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 7033999f7258e9ddd1d01620f9ad416e94ef3111
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442376"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a>Käibemaksu tasumise printimine koodide aruande järgi 

[!include [banner](../includes/banner.md)]

Aruande **Käibemaksu tasumine koodide lõikes** printimiseks avage **Maks** \> **Päringud ja aruanded** \> **Käibemaksu aruanded** \> **Käibemaksu tasumine koodide lõikes**. Vaikimisi luuakse aruandesummad juriidilise isiku arvestusvaluutas kõigi aruandluse koodide kohta, mis on seadistatud lehel **Käibemaksuaruandluse koodid**.

Selle aruande saate luua ka nii, et see kuvaks käibemaksu maksesummad käibemaksukoodide valuutades kõigi aruandekoodide korral, mis on määratud käibemaksukoodidele lehel **Käibemaksukoodid**.

## <a name="turn-on-the-feature"></a>Funktsiooni sisselülitamine

Lülitage tööruumis **Funktsioonihaldus** sisse järgmine funktsioon: **Loo käibemaksumakse koodide aruande järgi käibemaksukoodi valuutas**.

## <a name="run-the-report"></a>Aruande käivitamine

1. Avage  **Maks** \> **Päringud ja aruanded** \> **Käibemaksu aruanded** \> **Käibemaksu tasumine koodide lõikes**.
2. Valige väljal **Aruandevaluuta** üks järgmistest väärtustest.

    - **Arvestusvaluuta** – saate printida aruandesummad arvestusvaluuta.
    - **Käibemaksukoodi valuuta** – saate printida aruandesummad käibemaksukoodide valuutades.

    ![Käibemaksu tasumine koodi dialoogiboksi järgi](media/Sales-tax-payment-by-code.png)

Järgnev illustratsioon näitab aruande loodud näidet. Aruanne näitab, et aruandluskoodil **101** on valuuta **EUR**, kui selle määratud aruandluskoodiga käibemaksukoodi jaoks on välja **Käibemaksu valuuta** väärtuseks määratud **EUR**.

![Näide käibemaksu tasumisest koodide aruande järgi](media/Sales-tax-payment-by-code-2.png)
