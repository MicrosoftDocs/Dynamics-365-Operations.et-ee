---
title: Rakenduse Store Commerce häälestus- ja installiprobleemide tõrkeotsing
description: See artikkel selgitab, kuidas rakenduse Store Commerce häälestus- ja installiprobleemide Microsoft Dynamics 365 Commerce tõrkeotsingut teha.
author: josaw1
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: e3d115e84af1aaf5266eff6588ca6996a333e51a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286326"
---
# <a name="troubleshoot-store-commerce-setup-and-installation-issues"></a>Rakenduse Store Commerce häälestus- ja installiprobleemide tõrkeotsing

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas rakenduse Store Commerce häälestus- ja installiprobleemide Microsoft Dynamics 365 Commerce tõrkeotsingut teha.

## <a name="i-cant-activate-the-app-and-i-receive-a-connectivity-error-message"></a>Ma ei saa rakendust aktiveerida ja kuvatakse ühenduvuse tõrketeade.

Pärast kehtiva müügi pilveteenuse (CPOS) URL-i sisestamist võite saada ühenduvuse tõrketeate, mis sarnaneb järgmise näitega:

> Ilmnes ühenduvuse tõrge ja teie seade ei saa CPOS-ga ühendust luua. Tipitud CPOS-i URL-il võivad olla mõned probleemid.

Sellisel juhul vaadake üle kirjavigade URL või määratlege, kas CPOS-i ei saani, kuna see on võrguühenduseta.

Lisaks veenduge, et pilve kaaluühiku (CSU) versioon on 10.0.25 (9.35.\*.\*) või uuem. Rakenduse Store Commerce kasutamiseks on nõutav CPOS-versioon 10.0.25 või uuem.

## <a name="i-cant-install-the-app-because-modern-pos-is-already-installed"></a>Rakendust ei saa installida, kuna Modern POS on juba installitud

Installimise ajal võidakse kuvada tõrketeade, nt järgmises näites:

> Selle toote (Modern POS) versioon (9.\*.\*.\*) on pärandinstalli kaudu eelnevalt installitud.

Tõrke lahendamiseks peate desinstallima moderni müügipunkti (MPOS) rakenduse kõigi arvutis kasutajate jaoks ja seejärel uuesti proovima. Saate kinnitada, kas MPOS on kõigi kasutajate jaoks eemaldatud, käivitades järgmise PowerShelli käsu.

```PowerShell
Get-AppxPackage | Where-Object {$_.PackageFullName -like "Microsoft.Dynamics.*.Pos"} | Remove-AppxPackage -Allusers
```

## <a name="i-cant-activate-the-app-because-of-an-invalid-url-or-an-error-state"></a>Rakendust ei saa aktiveerida kehtetu URL-i või tõrke oleku tõttu.

Kui sisestatud CPOS-i URL ei kehti ja te soovite seda muuta või kui Rakenduse Store Commerce aktiveerimise ajal on tõrkeolekus, saate rakenduse lähtestades protsessi taaskäivitada. Rakendus Store Commerce salvestab ainult kehtiva CPOS-i URL-i.

Rakenduse Store Commerce lähtestamiseks järgige neid samme.

1. Windowsi menüüs **Start valige** ja hoidke all (või paremklõpsake) rakendust ja valige seejärel suvand **Veel rakenduse \> sätteid**.
2. Kerige rakenduse sätete lehe all, kuni leiate nupu **Lähtesta**.
3. Valige **Lähtesta**. Seejärel, kui teid küsitakse, kinnitage, et soovite rakenduse lähtestada.
