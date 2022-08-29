---
title: Poe äri laiendusprobleemide tõrkeotsing
description: See artikkel selgitab, kuidas rakendus Store Commerce rakendus laiendiprobleemide Microsoft Dynamics 365 Commerce tõrkeotsingut teha.
author: josaw1
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 1a2d6a68b7556d8b4d05529efd90f9e66f0c5925
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269777"
---
# <a name="troubleshoot-store-commerce-extension-issues"></a>Poe äri laiendusprobleemide tõrkeotsing

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas rakendus Store Commerce rakendus laiendiprobleemide Microsoft Dynamics 365 Commerce tõrkeotsingut teha.

## <a name="extensions-packages-arent-loaded"></a>Laienduste pakette pole laaditud.

### <a name="extensions-packages-dont-appear-on-the-pos--settings-page"></a>Laienduste pakette ei kuvata kassa sätete \> lehel.

Äri käitusaja (CRT) päästikuid ei pruugi laiendipaketi kaasamiseks värskendada või need ei ole juurutatud. Lisateavet vt commerce runtime [(CRT) laiendatavus ja käivitajad](../dev-itpro/commerce-runtime-extensibility-trigger.md).

### <a name="extensions-packages-appear-on-the-pos--settings-page-but-the-manifest-isnt-loaded"></a>Laienduste paketid kuvatakse müügikoha \> sätete lehel, kuid manifesti pole laaditud.

Veenduge, et laienduste paketid on kaustas **C:\\ Program Files\\Microsoft Dynamics 365\\ 10.0\\ Store Commerce\\ Extensions** olemas. Kui paketid on olemas, peaks seal olema müügikoha **kaust**, mis sisaldab manifesti.

Kui müügikoha kausta **pole**, veenduge, et poe äriprojekt viitab õigesti kassa laiendusprojektile. Kontrollige projekti viiteteed ja veenduge, et see on olemas. 

Järgmises näite näites on installeri projektil probleemid viidatud laiendiprojektiga.

![Store Commerce Installeri projekti viide ei kehti.](media/ReferenceNotValid.png)

Kui laiendusprojekti viide on õigesti lisatud, ei kuvata installerprojektis hoiatusi ega sõltuvusprobleemi, nagu näha järgmises näite näites.

![Store Commerce Installeri projekti viide on kehtiv.](media/ReferenceValid.png)
