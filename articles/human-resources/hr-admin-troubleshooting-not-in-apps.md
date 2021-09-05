---
title: Human Resources ei ilmu Microsoft Dynamics 365 rakenduste hulgas
description: See teema selgitab, mida teha, kui rakendust Microsoft Dynamics 365 Human Resources ei ole Microsoft Dynamics 365 rakenduste hulgas.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dfed82463eece882bed66c7b2dac1dd30e04720e
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413397"
---
# <a name="human-resources-app-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Rakendust Human Resources ei kuvata Microsoft Dynamics 365 rakenduste hulgas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Probleem**

Klient ei näe rakendust Dynamics 365 Human Resources Microsoft Dynamics 365 rakenduste hulgas.

**Eraldusvõime**

Kasutajale peab Microsoft Power Appsis olema keskkonna jaoks lisatud roll Keskkonna looja.

1. Power Appsi plaani 2 litsentsi omav administraatorkasutaja peab avama lehe [Power Appsi Haldusportaal](https://preview.admin.powerapps.com/).

2. Valige **Keskkonnad** ja seejärel õige keskkond rakendusele Human Resources.

3. Tehke vahekaardi **Turve** vahekaardil **Keskkonnarollid** valik **Keskkonna looja**.

    ![Keskkonnarollide vahekaart.](media/environment-roles.png)

4. Lisage vahekaardil **Kasutajad** kasutaja või organisatsioon.

    ![Kasutajate vahekaart.](media/environment-maker.png)

5. Valige käsk **Salvesta**.

6. Kasutaja peab kohe sisse logima lehele [Microsoft Dynamics 365](https://home.dynamics.com/).

7. Valige kasutajarakenduste uuendamiseks **Sünkrooni**.

    ![Sünkroniseerimise nupp.](media/get-more.png)

    Pärast sünkroonimise lõpuleviimist ilmub rakendus Human Resources avalehel.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
