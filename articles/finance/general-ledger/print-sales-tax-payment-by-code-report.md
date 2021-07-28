---
title: Käibemaksu tasumise printimine koodide aruande järgi
description: Selles teemas antakse teavet seadistuste ja toimingute kohta, mis on nõutavad käibemaksu tasumise printimiseks koodide aruande järgi arvestus- või maksukoodi valuutas.
author: anasyash
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: dad1cad6dcda1c7768f9be8bd7bd4426be7fbcbb
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358853"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a>Käibemaksu tasumise printimine koodide aruande järgi 

[!include [banner](../includes/banner.md)]

Aruande **Käibemaksu tasumine koodide lõikes** printimiseks avage **Maks** \> **Päringud ja aruanded** \> **Käibemaksu aruanded** \> **Käibemaksu tasumine koodide lõikes**. Vaikimisi luuakse aruandesummad juriidilise isiku arvestusvaluutas kõigi aruandluse koodide kohta, mis on seadistatud lehel **Käibemaksuaruandluse koodid**.

Selle aruande saate luua ka nii, et see kuvaks käibemaksu maksesummad käibemaksukoodide valuutades kõigi aruandekoodide korral, mis on määratud käibemaksukoodidele lehel **Käibemaksukoodid**.

## <a name="turn-on-the-feature"></a>Funktsiooni sisselülitamine

Lülitage tööruumis **Funktsioonihaldus** sisse järgmine funktsioon: **Loo käibemaksumakse koodide aruande järgi käibemaksukoodi valuutas**.

## <a name="run-the-report"></a>Aruande käivitamine

1. Avage **Maks** \> **Päringud ja aruanded** \> **Käibemaksu aruanded** \> **Käibemaksu tasumine koodide lõikes**.
2. Valige väljal **Aruandevaluuta** üks järgmistest väärtustest.

    - **Arvestusvaluuta** – saate printida aruandesummad arvestusvaluuta.
    - **Käibemaksukoodi valuuta** – saate printida aruandesummad käibemaksukoodide valuutades.

    ![Käibemaksu tasumine koodi dialoogiboksi järgi.](media/Sales-tax-payment-by-code.png)

Järgnev illustratsioon näitab aruande loodud näidet. Aruanne näitab, et aruandluskoodil **101** on valuuta **EUR**, kui selle määratud aruandluskoodiga käibemaksukoodi jaoks on välja **Käibemaksu valuuta** väärtuseks määratud **EUR**.

![Näide käibemaksu tasumisest koodide aruande järgi.](media/Sales-tax-payment-by-code-2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]