---
title: Sünkrooniseeri kontsernisisese kliendi teave
description: See artikkel selgitab kontsernisiseste tellimuste klienditeabe sünkroonimist
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: a3a67c9bcf93f88375d2d4d78d87175200626d50
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897512"
---
# <a name="synchronize-intercompany-customer-information"></a>Sünkrooniseeri kontsernisisese kliendi teave

[!include [banner](../../includes/banner.md)]

Kui on märgitud väli **Kliendi teave**, siis sünkroonitakse kliendi teave müügitellimuse loomisel või kliendi-, hankijaviite ning kliendi tellimusnumbri muutmisel.

Nende sünkroonimisväljade väärtust saate alati muuta. Selle parameetri valimisega saate siiski määratleda ainult selle, kas see väärtus kopeeritakse muudele kontsernisisestele tellimustele. Kui on märgitud kontsernisisese müügitellimuse väli **Kliendi teave**, sünkroonitakse kontsernisisese müügitellimuse muudatus kontsernisisese ostutellimusega. Kui märkisite ka kontsernisisesel ostutellimusel välja **Kliendi teave**, sünkroonitakse see algse müügitellimusega.

> [!NOTE]
> Kui nii kontsernisisese müügi- kui ka ostutellimuse puhul on märgitud väli **Kliendi teave**, siis ühe ettevõtte ühe töötaja tehtud muudatused allutatakse samal tellimusel teise töötaja teises ettevõttes tehtud muudatustele.

Parim tava on lubada kontsernisisesel ostutellimusel väli **Kliendi teave**. See lubab sünkroonimise algse müügitellimuse ja kontsernisisese ostutellimuse vahel ning kontsernisiseselt ostutellimuselt kontsernisisesele müügitellimusele.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
