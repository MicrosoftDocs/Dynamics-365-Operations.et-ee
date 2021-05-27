---
title: Tagasimaksehalduse tehingu töövood
description: See teema kirjeldab, kuidas seadistada Tagasimaksehalduse tehingu töövoogu, et tehinguid kinnitada ja aktiveerida.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ee342de6d069131e230120c5d65aef58da8e632a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020382"
---
# <a name="rebate-management-deal-workflows"></a>Tagasimaksehalduse tehingu töövood

[!include [banner](../includes/banner.md)]

Tagasimaksete kinnitamiseks kasutab Tagasimaksehaldus sama töövoo platvorme kui teised Finance and Operations rakendused. Iga töövooga on seotud kaks tööprotsessi.

- Üks töövoo element aktiveerib tehingu, nii et kasutaja või töövoo protsess saab kanded kinnitada.
- Üks töövoo element kinnitab tehingu.

Enne tagasimakse tehingu kasutamist peab see olema aktiivne moodulis **Tagasimaksehaldus**. Tehingu aktiveerimiseks peate esmalt looma ja konfigureerima töövoo *Tagasimaksehalduse tehingu töövoog*.

Pärast töövoo aktiveerimist Tagasimakse halduse jaoks ei saa kasutajad tehinguid käsitsi kinnitada. Töövoogu peab alati kasutama.

## <a name="create-and-manage-rebate-management-deal-workflows"></a>Tagasimaksehalduse tehingu töövoogude loomine ja haldamine

Tagasimaksehalduse tehingu töövoogudega töötamiseks minge **Tagasimaksehaldus \> Seadistamine \> Tagasimaksehalduse töövood**. Seal saate vajadusel töövooge vaadata, luua ja uuendada. Korraga saab olla aktiivne ainult üks seda tüüpi töövoog. Lisateavet töövoogude kohta, kuidas töötada lehega **Tagasimaksehalduse töövood** ja kuidas töövooge luua, vaadake [Töövoo süsteemi ülevaadet](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) ja selle seotud teemasid.

## <a name="use-a-workflow-to-activate-a-deal"></a>Kasutage töövoogu tehingu aktiveerimiseks.

Tehingu aktiveerimiseks töövoo kaudu avage tehing (nt lehel **Kõik tagasimaksehalduse tehingud**). Seejärel valige toimingupaanil **Töövoog \> Edasta**. Kui uus tehing on töövoo kaudu töödeldud ja kinnitatud, on see aktiivne ja kasutamiseks valmis.

Pärast tehingu aktiveerimist ei saa te selle seadistust muuta. Kui peate aktiivset tehingut muutma, inaktiveerige see ja seejärel looge uus tehing. Kui uus tehing sarnaneb vana tehinguga, saate selle luua vana tehingut kopeerides.
