---
title: Käibemaksu tasumise printimine koodide aruande järgi
description: See artikkel annab teavet sätete ja tegevuste kohta, mis on vajalikud käibemaksu maksmise printimiseks koodiaruandena raamatupidamise või maksukoodi valuutas.
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
ms.openlocfilehash: 9c6b51da41f2aaa3206f8ad97a364a9cd5ca6d49
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856650"
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