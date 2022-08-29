---
title: Käibemaksu tasumise printimine koodide aruande järgi
description: See artikkel annab teavet sätete ja tegevuste kohta, mis on vajalikud käibemaksu maksmise printimiseks koodiaruandena raamatupidamise või maksukoodi valuutas.
author: AdamTrukawka
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.search.form: ''
ms.openlocfilehash: ea11826d21b66e6283abf24b3f7b0945e6eb9192
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272364"
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
