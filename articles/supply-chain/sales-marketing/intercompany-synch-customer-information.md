---
title: Sünkrooniseeri kontsernisisese kliendi teave
description: See teema kirjeldab kontsernisiseste tellimuste klienditeabe sünkroniseerimist
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c82216c8391f6c447bec74f25cd16b9db18d468d
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548221"
---
# <a name="synchronize-intercompany-customer-information"></a>Sünkrooniseeri kontsernisisese kliendi teave

[!include [banner](../../includes/banner.md)]

Kui on märgitud väli **Kliendi teave**, siis sünkroonitakse kliendi teave müügitellimuse loomisel või kliendi-, hankijaviite ning kliendi tellimusnumbri muutmisel.

Nende sünkroonimisväljade väärtust saate alati muuta. Selle parameetri valimisega saate siiski määratleda ainult selle, kas see väärtus kopeeritakse muudele kontsernisisestele tellimustele. Kui on märgitud kontsernisisese müügitellimuse väli **Kliendi teave**, sünkroonitakse kontsernisisese müügitellimuse muudatus kontsernisisese ostutellimusega. Kui märkisite ka kontsernisisesel ostutellimusel välja **Kliendi teave**, sünkroonitakse see algse müügitellimusega.

> [!NOTE]
> Kui nii kontsernisisese müügi- kui ka ostutellimuse puhul on märgitud väli **Kliendi teave**, siis ühe ettevõtte ühe töötaja tehtud muudatused allutatakse samal tellimusel teise töötaja teises ettevõttes tehtud muudatustele.

Parim tava on lubada kontsernisisesel ostutellimusel väli **Kliendi teave**. See lubab sünkroonimise algse müügitellimuse ja kontsernisisese ostutellimuse vahel ning kontsernisiseselt ostutellimuselt kontsernisisesele müügitellimusele.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
