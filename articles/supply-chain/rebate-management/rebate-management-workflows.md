---
title: Tagasimakse halduse tehingute töövood
description: See artikkel selgitab, kuidas seadistada Tagasimaksehalduse hinnaalanduste töövoogu, et tehinguid kinnitada ja aktiveerida.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2b1611ff7877efc4a2f98b8f84a1ef91971902ab
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869513"
---
# <a name="rebate-management-deal-workflows"></a>Tagasimaksehalduse tehingu töövood

[!include [banner](../includes/banner.md)]

Tagasimaksetehingute kinnitamiseks kasutab Tagasimaksehaldus sama töövoo platvorme kui teised finantside ja toimingute rakendused. Iga töövooga on seotud kaks tööprotsessi.

- Üks töövoo element kinnitab tehingu.
- Üks töövoo element aktiveerib tehingu, nii et kasutaja või töövoo protsess saab kanded kinnitada.

Enne tagasimakse tehingu kasutamist peab see olema aktiivne moodulis **Tagasimaksehaldus**. Tehingu aktiveerimiseks peate esmalt looma ja konfigureerima töövoo *Tagasimaksehalduse tehingu töövoog*.

Kasutajad ei saa tehinguid käsitsi kinnitada. Töövoogu peab alati kasutama.

## <a name="create-and-manage-rebate-management-deal-workflows"></a>Tagasimaksehalduse tehingu töövoogude loomine ja haldamine

Tagasimaksehalduse tehingu töövoogudega töötamiseks minge **Tagasimaksehaldus \> Seadistamine \> Tagasimaksehalduse töövood**. Seal saate vajadusel töövooge vaadata, luua ja uuendada. Korraga saab olla aktiivne ainult üks seda tüüpi töövoog. Lisateavet töövoogude kohta, **kuidas töötada tagasimaksehalduse töövoogude** lehega ja kuidas töövooge luua, [vt](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) Töövoo süsteemi ülevaadet ja selle seotud artikleid.

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
