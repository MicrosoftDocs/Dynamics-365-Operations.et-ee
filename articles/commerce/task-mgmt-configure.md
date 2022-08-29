---
title: Ülesandehalduse konfigureerimine
description: See artikkel kirjeldab, kuidas konfigureerida toiminguhalduse funktsioone moodulis Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.search.industry: ''
ms.openlocfilehash: ff97abab330174b41af76d22c202e8338d6d37fd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282757"
---
# <a name="configure-task-management"></a>Ülesandehalduse konfigureerimine

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas konfigureerida toiminguhalduse funktsioone moodulis Microsoft Dynamics 365 Commerce.

Enne kui rakenduse Dynamics 365 Commerce juhatajad ja töötajad saavad Commerce’is ülesande haldamise funktsioone kasutada, tuleb ülesannete haldus konfigureerida. Konfiguratsiooni etapid hõlmavad juhatajatele ja töötajatele lubade andmist, kassa klientidele lubade andmist, kassa teavituste seadistamist ja kassarakenduse avalehel paani **Ülesanded** konfigureerimist.

## <a name="configure-permissions-for-store-managers"></a>Poe juhatajate lubade konfigureerimine

Konkreetse poe iga töötaja saab vaadata kõiki sellele poele määratud ülesandeid. Samuti saavad nad värskendada neile määratud ülesannete olekut. Samas peab isikutel, nagu poe juhatajad, olema ülesande halduri load, et hallata poele määratud ülesandeid ja luua ühekordseid ülesandeid.

Poe juhatajate ülesannete halduse lubade konfigureerimiseks tehke järgmist.

1. Avage **Jaemüük ja kaubandus \> Töötajad \> Loagrupid**.
1. Valige konkreetne loagrupp (nt **Juhataja**) ja seejärel valige suvand **Redigeeri**.
1. Kiirkaardil **Load** määrake suvand **Luba ülesannete haldus** valikule **Jah**.
1. Kiirkaardil **Teatised** lisage toiming **Ülesannete haldus** ja sisestage väärtus väljale **Kuvamisjärjestus**. Näiteks sisestage **2**, kui toimingul **Tellimuse täitmise** on juba suvandi **Kuvamisjärjestus** jaoks väärtus **1**.
    
> [!NOTE]
> Kui mitte-juhist isikul peab omama kassa ülesannete halduse õiguseid, saate isikule anda load. Teise võimalusena saate luua uue õiguste grupi mitte-juhtidele ja seada suvand **Luba ülesannete haldamine** väärtusele **Jah**.

Järgmisel joonisel on näidatud, kuidas konfigureerida poe juhatajate ülesannete halduse lubasid.

![Poe juhatajate ülesannete halduse lubade konfigureerimine.](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a>Töötajate lubade konfigureerimine

Töötajatel peavad olema õigused ülesannete loendite loomiseks, määramise kriteeriumide haldamiseks ja ülesannete loendi kordumise konfigureerimiseks. Nende lubade konfigureerimiseks määrate töötajad rollile **Jaemüügi ülesannete haldur**.

Töötaja lubade konfigureerimiseks tehke järgmist.

1. Avage **Jaemüük ja kaubandus \> Töötajad \> Kasutajad**.
1. Valige töötaja.
1. Kiirkaardil **Kasutaja rollid** valige suvand **Määra rollid**.
1. Dialoogiboksis **Määra kasutajale rollid** valige roll **Jaemüügi ülesannete haldur** ja seejärel valige **OK**.

## <a name="distribute-permissions-to-pos-clients"></a>Kassa klientidele lubade jaotamine

Enne kui töötajad saavad kassa kliente kasutada, peavad load olema nende klientide vahel jaotatud ja sünkroonitud.

Kassa klientidele lubade jaotamiseks tehke järgmist.

1. Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**.
1. Valige jaotusgraafik **1060** (**Personal**) ja seejärel valige käsk **Käita kohe**.
1. Valige jaotusgraafik **1070** (**Kanali konfiguratsioon**) ja seejärel valige käsk **Käita kohe**.

## <a name="configure-pos-notifications-for-tasks"></a>Ülesannete jaoks kassa teatiste konfigureerimine

Ülesannete haldus peab olema konfigureeritud nii, et teatised oleksid kassarakenduses saadaval.

Ülesannete jaoks kassa teatiste konfigureerimiseks tehke järgmist.

1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassa \> Kassatoimingud**.
1. Leidke toiming **1400** (**Ülesannete haldus**) ja valige selle joaks märkeruut **Luba teatised**.

Järgmisel joonisel on kujutatud toiming **Ülesannete haldus** lehel **Kassa toimingud**.

![Ülesannete halduse toiming kassa toimingute lehel.](media/HQ-POS-Tasks-Notifications.png)

Lisateavet kassa teatiste konfigureerimise kohta vt teemast [Kassa tellimuse teatiste kuvamine](notifications-pos.md).

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a>Paani Ülesanded konfigureerimine kassarakenduse avalehel

Enne kassarakenduse avalehel paani **Ülesanded** konfigureerimist, vt teemast [Kassa ekraanipaigutused](pos-screen-layouts.md) teavet selle kohta, kuidas konfigureerida ja lisada kassa ekraanipaigutusse uusi nuppe.

Kassarakenduse avalehel paani **Ülesanded** konfigureerimiseks tehke järgmist.

1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassa \> Ekraanipaigutused**.
1. Valige ekraanipaigutus, valige paigutuse suurus ja valige nupupaneel.
1. Kiirkaardil **Nupupaneelid** valige suvand **Kujundaja**, et redigeerida valitud nupupaneeli.
1. Lisage paan **Ülesanded** avalehe vastavale jaotisele.

Järgmisel joonisel on näidatud paani **Ülesanded** näide kassa avalehel.

![Ülesannete paan kassa avalehel.](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a>Lisaressursid

[Ülesandehalduse ülevaade](task-mgmt-overview.md)

[Tööülesannete loendite loomine ja ülesannete lisamine](task-mgmt-create-lists.md)

[Ülesandeloendite määramine poodidele või töötajatele](task-mgmt-assign-lists.md)

[Ülesannete haldus kassas](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
