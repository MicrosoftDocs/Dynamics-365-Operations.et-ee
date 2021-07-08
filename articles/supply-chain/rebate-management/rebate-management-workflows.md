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
ms.openlocfilehash: 8436842b4f07ba000649075198bdef43ad508f8f
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270953"
---
# <a name="rebate-management-deal-workflows"></a>Tagasimaksehalduse tehingu töövood

[!include [banner](../includes/banner.md)]

Tagasimaksete kinnitamiseks kasutab Tagasimaksehaldus sama töövoo platvorme kui teised Finance and Operations rakendused. Iga töövooga on seotud kaks tööprotsessi.

- Üks töövoo element kinnitab tehingu.
- Üks töövoo element aktiveerib tehingu, nii et kasutaja või töövoo protsess saab kanded kinnitada.

Enne tagasimakse tehingu kasutamist peab see olema aktiivne moodulis **Tagasimaksehaldus**. Tehingu aktiveerimiseks peate esmalt looma ja konfigureerima töövoo *Tagasimaksehalduse tehingu töövoog*.

Kasutajad ei saa tehinguid käsitsi kinnitada. Töövoogu peab alati kasutama.

## <a name="create-and-manage-rebate-management-deal-workflows"></a>Tagasimaksehalduse tehingu töövoogude loomine ja haldamine

Tagasimaksehalduse tehingu töövoogudega töötamiseks minge **Tagasimaksehaldus \> Seadistamine \> Tagasimaksehalduse töövood**. Seal saate vajadusel töövooge vaadata, luua ja uuendada. Korraga saab olla aktiivne ainult üks seda tüüpi töövoog. Lisateavet töövoogude kohta, kuidas töötada lehega **Tagasimaksehalduse töövood** ja kuidas töövooge luua, vaadake [Töövoo süsteemi ülevaadet](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) ja selle seotud teemasid.

## <a name="use-a-workflow-to-activate-a-deal"></a>Kasutage töövoogu tehingu aktiveerimiseks.

Tehingu aktiveerimiseks töövoo kaudu avage tehing (nt lehel **Kõik tagasimaksehalduse tehingud**). Seejärel valige toimingupaanil **Töövoog \> Edasta**. Kui uus tehing on töövoo kaudu töödeldud ja kinnitatud, on see aktiivne ja kasutamiseks valmis.

Pärast tehingu aktiveerimist ei saa te enamust selle seadistusest muuta. Kui peate aktiivset tehingut muutma, esmalt inaktiveerige see ja seejärel looge uus tehing. Kui uus tehing sarnaneb vana tehinguga, saate selle luua vana tehingut kopeerides.

Saate muuta tehingu järgmisi sätteid pärast selle aktiveerimist:

- Vastavusseviimine
- Kumulatiivne garantii
- Sisestusreeglid
- Garantii sisestusprofiil
- Dokumendi märkused
- Currency
- Alates kuupäevast
- Lõppkuupäev

Lisaks saab tagasimakse read eemaldada.
