---
title: Human Resources ei ilmu Microsoft Dynamics 365 rakenduste hulgas
description: Selles artiklis selgitatakse, mida teha, kui klient ei näe rakendust Microsoft Dynamics 365 Human Resources Microsoft Dynamics 365 rakenduste.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 658c6a4f17c022c3d0e3e49d16eb89624c4be27c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803965"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Human Resources ei ilmu Microsoft Dynamics 365 rakenduste hulgas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Väljastamine**

Klient ei näe rakendust Dynamics 365 Human Resources Microsoft Dynamics 365 rakenduste hulgas.

**Eraldusvõime**

Kasutajale peab Microsoft Power Appsis olema keskkonna jaoks lisatud roll Keskkonna looja.

1. Power Appsi plaani 2 litsentsi omav administraatorkasutaja peab avama lehe [Power Appsi Haldusportaal](https://preview.admin.powerapps.com/).

2. Valige **Keskkonnad** ja seejärel õige keskkond rakendusele Human Resources.

3. Tehke vahekaardi **Turve** vahekaardil **Keskkonnarollid** valik **Keskkonna looja**.

    ![Vahekaart Keskkonnarollid](media/environment-roles.png)

4. Lisage vahekaardil **Kasutajad** kasutaja või organisatsioon.

    ![Vahekaart Kasutajad](media/environment-maker.png)

5. Valige käsk **Salvesta**.

6. Kasutaja peab kohe sisse logima lehele [Microsoft Dynamics 365](https://home.dynamics.com/).

7. Valige kasutajarakenduste uuendamiseks **Sünkrooni**.

    ![Nupp Sünkrooni](media/get-more.png)

    Pärast sünkroonimise lõpuleviimist ilmub rakendus Human Resources avalehel.


[!INCLUDE[footer-include](../includes/footer-banner.md)]