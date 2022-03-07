---
title: Ülesandeloendite määramine poodidele või töötajatele
description: Selles teemas kirjeldatakse, kuidas määrata rakenduses Microsoft Dynamics 365 Commerce poodidele või töötajatele ülesandeloendeid.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: ee924f5bf95d47814e7ca09b392a3d10b5e9b9dc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006256"
---
# <a name="assign-task-lists-to-stores-or-employees"></a>Ülesandeloendite määramine poodidele või töötajatele

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas määrata rakenduses Microsoft Dynamics 365 Commerce poodidele või töötajatele ülesandeloendeid.

## <a name="overview"></a>Ülevaade

Rakenduse Dynamics 365 Commerce ülesannete haldus võimaldab teil määrata ülesandeloendeid erinevatele poodidele või töötajatele või poodide ja töötajate kombinatsioonile. Näiteks võib 20 poe piirkondlik juht soovida määrata kõigile 20 poele ülesandeloendi **Pühadeaja ettevalmistus**.

## <a name="start-the-task-list-assignment-process"></a>Ülesandeloendi määramise protsessi käivitamine

Ülesandeloendi määramise protsessi alustamiseks toimige järgmiselt.

1. Avage **Jaemüük ja kaubandus \> Ülesannete haldus \> Ülesannete halduse administreerimine**.
1. Valige määramiseks ülesandeloend.
1. Valige suvand **Alusta protsessi**.
1. Dialoogiboksis **Käivita protsess** vahekaardil **Üldine** väljal **Protsessi nimi** sisestage nimi (näiteks **Ida piirkonna poed**).
1. Täpsustage kuupäev väljal **Sihtkuupäev**.
1. Ülesandeloendi poodidele määramiseks kasutage vahekaardil **Poed** filtrit **Organisatsiooni hierarhia**, et otsida ja valida poed.

    Ülesandeloendi töötajatele määramiseks otsige ja valige töötajad vahekaardil **Töötajad**.

1. Protsessi alustamiseks valige **OK**. Ülesandeloend määratakse valitud poodidele või töötajatele.

Järgmisel joonisel on toodud näide, kuidas dialoogiboksis **Alusta protsessi** otsida ja valida poode.

![Poodide otsimine ja valimine dialoogiboksis Alusta protsessi](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a>Korduva ülesandeloendi määramine

Jaemüüjal on mõnikord korduvad ülesanded, nagu „Neljapäevane sulgemise kontroll-loend” või „Kuu esimese päeva kontroll-loend”. Seetõttu võivad nad soovida määrata korduva ülesandeloendi.

1. Avage **Jaemüük ja kaubandus \> Ülesannete haldus \> Ülesannete halduse administreerimine**.
1. Valige määramiseks ülesandeloend.
1. Valige suvand **Alusta protsessi**.
1. Dialoogiboksis **Alusta protsessi** vahekaardil **Üldine** väljal **Protsessi nimi** sisestage nimi.
1. Määrake suvand **Kordumine** valikule **Jah**.
1. Sisestage päevade arv väljale **Korduvuse sihtkuupäeva nihe päevades**. Näiteks kui sisestate **4**, on sihtkuupäevaks kordumise kuupäev pluss neli päeva.
1. Vahekaardil **Käivita taustal** valige suvand **Kordumine**.
1. Sisestage dialoogiboksis **Korduse määratlemine** sageduse kriteeriumid ja seejärel valige **OK**.

Järgmisel joonisel on toodud näidis, kuidas sisestada dialoogiboksi **Korduse määratlemine** sageduse kriteeriume.

![Sageduse kriteeriumite sisestamine dialoogiboksis Korduse määratlemine](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a>Ülesandeloendi oleku jälgimine

Kui olete piirkondlik juht või poe juhataja, võite tahta jälgida ülesandeloendite olekut, mis on mitmele poele või töötajale määratud. Seejärel saate teha järeltegevusi poodide või töötajatega, kes neile määratud ülesandeid õigeaegselt ei täitnud. Commerce’i kontor võimaldab teil vaadata ülesandeloendite olekut, ülesandeid uuesti märata või muuta ülesande olekut.

Kõikide ülesannete ülesandeloendi oleku jälgimiseks toimige järgnevalt.

1. Avage **Jaemüük ja kaubandus \> Ülesannete haldus \> Ülesannete halduse protsess**.
1. Erinevatele poodidele määratud kõikide ülesandeloendite oleku vaatamiseks valige vahekaart **Kõik ülesandeloendid**.

Kõikide teile määratud ülesannete ülesandeloendi oleku jälgimiseks toimige järgnevalt.

1. Avage **Jaemüük ja kaubandus \> Ülesannete haldus \> Ülesannete halduse protsess**.
1. Valige vahekaart **Minu ülesanded** või **Kõik ülesanded**, et vaadata või värskendada teile määratud ülesannete olekut.

## <a name="additional-resources"></a>Lisaressursid

[Ülesannete halduse ülevaade](task-mgmt-overview.md)

[Ülesannete halduse konfigureerimine](task-mgmt-configure.md)

[Ülesandeloendite loomine ja ülesannete lisamine](task-mgmt-create-lists.md)

[Ülesannete haldus kassas](task-mgmt-POS.md)
