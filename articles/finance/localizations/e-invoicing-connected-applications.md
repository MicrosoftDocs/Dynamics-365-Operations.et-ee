---
title: Ühendatud rakendused
description: See artikkel selgitab, kuidas seadistada ühendatud rakendusi elektroonilises arveldamises.
author: dkalyuzh
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7a0a9c19009c49b80ca8c182c31592c1a713a2aa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906283"
---
# <a name="connected-applications"></a>Ühendatud rakendused

[!include [banner](../includes/banner.md)]

Ühendatud rakendused on Microsoft Dynamics 365 Finantside Dynamics 365 Supply Chain Management eksemplarid ja te võite soovida ühendust võtta läbi regulatiivse konfiguratsiooniteenuse (RCS). Ühendatud rakenduste kaudu saate konfigureerida osa oma finantside või tarneahelate halduse globaliseerimisfunktsioonist, et teha elektroonilise arvelduse stsenaariumi töö.

Kui juurutate oma globaliseerimisfunktsiooni, saab teie finantside või tarneahela halduse rakendusele rakendatava seadistusteabe avaldada otse RCS-ist vastavasse ühendatud rakendusse.

Finantside või tarneahela haldamise parameetrite saadavus RCS-is on kasulik, kui teil on erinevad rakenduskeskkonnad, nt kasutaja aktsepteerimise testimine (UAT) ja tootmiskeskkonnad, ning kui soovite seadistust säilitada järjepidevana, juurutades samad parameetrid erinevatesse keskkondades.

## <a name="create-a-connected-application"></a>Ühendatud rakenduse loomine

1. Logige oma RCS-i kontole sisse.
2. Tööruumis **Globaliseerimisfunktsioonid** jaotises **Keskkond** valige paan **Elektrooniline arveldus**.
3. **Valige tegevuspaanil** Keskkonna häälestuslehe kaudu ühendatud **rakendused**.
4. Valige ühendatud rakenduse loomiseks **Uus**.
5. Sisestage väljale **Nimi** ühendatava rakenduse nimi.
6. Väljal Tüüp **valige** Dynamics **365 Finantsid**.
7. **Sisestage** väljale Rakendus ühenduse loomiseks keskkonna URL.
8. Sisestage **rentniku** väljale keskkonna rentnik.
9. Valige käsk **Salvesta**.
10. Keskkonnaga lodud ühenduse testimiseks valige toimingupaanil käsk **Kontrolli ühendust**. Seejärel sulgege leht.

## <a name="link-connected-applications-to-environments"></a>Ühendatud rakenduste keskkondadega linkimine

1. Keskkonna seadistuse **lehel** valige uus **,** et määrata ühendatud rakendus keskkonda.
2. Valige väljal **Ühendatud rakendus** ühendatud rakendus.
3. Valige väljal **Teenusekeskkond** teenusekeskkond.
4. Valige **Salvesta** ja sulgege seejärel leht.
