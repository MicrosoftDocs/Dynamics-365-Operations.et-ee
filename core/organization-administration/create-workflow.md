---
title: "Töövoo loomine"
description: "See teema selgitab, kuidas töövoogu luua."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Core
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 1255cf90498f1968568dd2fa5a1377d989f40182
ms.lasthandoff: 03/31/2017


---

# <a name="create-a-workflow"></a>Töövoo loomine

[!include[banner](../includes/banner.md)]


See teema selgitab, kuidas töövoogu luua.

<a name="open-the-workflow-editor"></a>Avage töövoo redaktor
------------------------

Microsoft Dynamics 365 for Operationsi moodul, milles töötate, määrab töövootüübid, mida saate luua. Läbige need etapid töövoo tüübi valimiseks, et luua ja avada töövoo redaktor.

1.  Avage moodul, mille jaoks soovite luua uue töövoo. Näiteks ostutaotluste jaoks töövoo loomiseks klõpsake valikut **Hanked**.
2.  Klõpsake valikuid **Seadistus** &gt; **Mooduli \[mooduli nimi\] töövood**.
3.  Ilmuva loendilehe tegumiribal klõpsake valikut **Uus**.
4.  Lehel **Töövoo loomine** valige loomiseks töövoo tüüp ja klõpsake seejärel valikut **Töövoo loomine**. Ilmub töövooredaktor. Nüüd saate kasutada töövoo kujundamiseks järgmiseid protseduure.

## <a name="drag-workflow-elements-onto-the-canvas"></a>Lohistage töövoo elemendid lõuend
Töövooredaktori ala **Töövoo elemendid** sisaldab elemente, mida saate oma töövoole lisada. Töövoole elementide lisamiseks lohistage need lõuendile.

## <a name="connect-the-elements"></a>Ühendage elemendid
Ühe töövoo elemendi teisega ühendamiseks hoidke kursorit elemendi kohal, kuni ühenduspunktid kuvatakse. Klõpsake ühenduspunkti ja lohistage see teisele elemendile. Ühendage kindlasti kõik elemendid.

## <a name="configure-the-properties-of-the-workflow"></a>Konfigureerige töövoo atribuudid
Järgige neid juhiseid töövoo atribuutide konfigureerimiseks.

1.  Klõpsake lõuend veendumaks, et töövoo element pole valitud.
2.  Klõpsake valikut **Atribuudid**, et avada töövoo leht **Atribuudid**.
3.  Järgige teemas [Töövoo atribuutide konfigureerimine](configure-workflow-properties.md) kirjeldatud protseduure.

## <a name="configure-the-elements-of-the-workflow"></a>Töövoo elementide konfigureerimine
Konfigureerige iga elemendi läbite lõuendile. Iga töövooelemendi konfigureerimise kohta lisateabe saamiseks vaadake järgmisi teemasid.

-   [Käsitsi ülesande konfigureerimine](configure-manual-task-workflow.md)
-   [Automatiseeritud ülesande konfigureerimine](configure-automated-task-workflow.md)
-   [Kinnitusprotsessi konfigureerimine](configure-approval-process-workflow.md)
-   [Kinnitussammude konfigureerimine](configure-approval-step-workflow.md)
-   [Käsitsi otsuse konfigureerimine](configure-manual-decision-workflow.md)
-   [Tingimusliku otsuse konfigureerimine](configure-conditional-decision-workflow.md)
-   [Paralleeltegevuse konfigureerimine](configure-parallel-activity-workflow.md)
-   [Paralleelharu konfigureerimine](configure-parallel-branch-workflow.md)
-   [Reakauba töövoo konfigureerimine](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a>Lahenda tõrkeid ja hoiatusi
Töövooredaktori allservas olev paan **Tõrked ja hoiatused** näitab töövoo jaoks loodud teateid. Selle elemendi leidmiseks, kus tõrge või hoiatus ilmnes, topeltklõpsake tõrget või hoiatusteadet. Enne töövoo aktiivseks tegemist peate lahendama kõik tõrked ja hoiatused.

## <a name="save-and-activate-the-workflow"></a>Salvestage ja aktiveerige töövoog
Kui olete valmis töövoo salvestama ja aktiveerima, järgige neid juhiseid.

1.  Klõpsake valikut**Salvesta ja sule**, et sulgeda töövooredaktor ja avada leht **Salvesta töövoog**.
2.  Sisestage kommentaarid töövoole tehtud muudatuste kohta ja klõpsake seejärel **OK**.
3.  Kui kõik tõrked ja hoiatused on lahendatud, ilmub leht **Aktiveeri töövoog**. Tehke üks järgmistest valikutest:
    -   Töövoo selle versiooni aktiveerimiseks klõpsake valikut **Aktiveeri uus versioon**. Kui töövoog on aktiivne, saavad kasutajad esitada töötlemiseks dokumente.
    -   Kui te ei soovi seda versiooni aktiveerida, klõpsake valikut **Ära aktiveeri uut versiooni**. Saate töövoo hiljem aktiveerida.





