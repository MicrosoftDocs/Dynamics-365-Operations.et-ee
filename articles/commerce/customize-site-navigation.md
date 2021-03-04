---
title: Saidil navigeerimise kohandamine
description: Selles teemas kirjeldatakse, kuidas luua kohandatud veebipõhist navigeerimishierarhiat, et korrastada tooted rakenduse Microsoft Dynamics 365 Commerce saidil sirvimiseks.
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c2b6a7a3b35873e80be391c627d0397fd6398a99
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411659"
---
# <a name="customize-site-navigation"></a>Saidil navigeerimise kohandamine


[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas luua kohandatud veebipõhist navigeerimishierarhiat, et korrastada tooted rakenduse Microsoft Dynamics 365 Commerce saidil sirvimiseks.

## <a name="overview"></a>Ülevaade

Veebipoe fassaadid võimaldavad tavaliselt klientidel tooteid avastada ja sirvida, navigeerides tootekategooriate kaudu. Seda võimalust pakuvad tavaliselt lehe ülaosas olevad vahekaardid või vasakul olev navigeerimisriba. Rakenduses Dynamics 365 Commerce saate luua ja hallata kategooria navigeerimise hierarhilist struktuuri ja erinevates kategooriates sisalduvaid tooteid.

## <a name="create-a-channel-navigation-hierarchy"></a>Kanali navigeerimishierarhia loomine

Kanali navigeerimishierarhia loomiseks toimige järgmiselt.

1. Avage **Jaemüük ja kaubandus \> Tooted ja kategooriad \> Kategooria- ja tootehaldus**.
1. Valige suvand **Kategooria hierarhiad** ja valige seejärel **Uus**.
1. Andke hierarhiale nimi.

    > [!NOTE]
    > Kõige ülemine loodav kategooria on juurekategooria sõlm. Teie saidil seda ei kuvata. Kategooriahierarhia loomiseks, kus teie saidil kuvatakse üks ülemise taseme sõlm, looge ja nimetage kategooria juurekategooria alamana.

1. Valige suvand **Uus kategooria sõlm** ja andke kategooriale nimi.
1. Jätkake vastavalt vajadusele õe- ja alamkategooriate loomist.

Nüüd saate määrata tooted igale kategooriale, mille ülemise taseme kategooria alla lõite.

## <a name="customize-the-order-of-categories"></a>Kategooriate järjestuse kohandamine

Vaikimisi ilmuvad määratletud kategooriad teie saidi tähestikulises järjestuses. Samas saate kategooriate kuvamise järjestust ka kohandada.

## <a name="assign-a-category-hierarchy-type"></a>Kategooriahierarhia tüübi määramine

1. Avage **Jaemüük ja kaubandus \> Tooted ja kategooriad \> Kategooria- ja tootehaldus**.
1. Valige suvand **Kategooriahierarhiad**.
1. Valige tegumiriba vahekaardil **Kategooriahierarhia** grupis **Häälesta** suvand **Hierarhiatüübi seostamine**.
1. Valige suvand **Uus**.
1. Valige väljal **Kategooria hierarhia tüüp** suvand **Kanali navigeerimishierarhia**.
1. Valige väljal **Kategooriahierarhia** varem loodud kanali navigeerimishierarhia.

## <a name="publish-new-or-updated-navigation-hierarchies"></a>Uute või värskendatud navigeerimishierarhiate avaldamine

Oma navigeerimishierarhia veebipoe fassaadis kättesaadavaks tegemiseks toimige järgmiselt.

1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kanali kategooriad ja toote atribuudid**.
1. Valige vasakpoolsel puul oma veebipood.
1. Valige suvand **Kanalivärskenduste avaldamine**.
1. Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**.
1. Otsige ja valige loendist **Töö 1040**.
1. Valige käsk **Käita kohe**.
1. Korrake samme 5 ja 6 tööde 1070 ja 1150 jaoks.

## <a name="show-categories-on-your-site"></a>Kategooriate kuvamine saidil

Kategooriahierarhia kuvamiseks veebipoe fassaadil peate lisama mallis või fragmendis sobivasse asukohta navigeerimismenüü mooduli. Seejärel kuvab navigeerimismenüü moodul teie navigeerimishierarhia, kui olete oma navigeerimishierarhia avaldanud kanalis, millega teie sait on seotud.

> [!NOTE]
> Mooduliteegis sisalduv navigeerimismenüü moodul võimaldab kasutajatel navigeerida ainult kategooriatesse, millel puuduvad alamkategooriad. Kui teie kliendid peaksid saama navigeerida kategooriatesse, millel on alamkategooriad, peate navigeerimispaani moodulit kohandama.

## <a name="add-custom-navigation-options"></a>Kohandatud navigeerimissuvandite lisamine

Navigeerimismenüüs saate lisada navigeerimissuvandeid, mis ei kuulu teie toote kategooriahierarhiasse. Näiteks saate toote kategooria loendi lõpus saate lisada üksuse **Võtke meiega ühendust**, mis osutab saidi jaoks loodud kontaktide lehele.

Navigeerimismenüüsse kohandatud navigeerimisesuvandite lisamiseks toimige järgmiselt.

1. Valige mallis või fragmendis, mida soovite kohandada, navigeerimismenüü moodul.
1. Valige atribuudipaanil vahekaardil **Andmed** suvand **Lisa üksus**, et luua uus sisuhaldussüsteemi (CMS) navigeerimisüksus.
1. Sisestage lingi tekst ja URL.
1. Rohkemate kohandatud navigeerimissuvandite lisamiseks korrake samme 2 ja 3.
1. Kui olete lõpetanud, valige malli või fragmendi salvestamiseks **Salvesta** ja seejärel selle registreerimiseks **Lõpeta redigeerimine**.

## <a name="additional-resources"></a>Lisaressursid

[Mallide ja paigutuste ülevaade](templates-layouts-overview.md)

[Mallidega töötamine](work-with-templates.md)

[Eelmääratud paigutustega töötamine](work-with-layouts.md)

[Fragmentidega töötamine](work-with-fragments.md)

[Moodulitega töötamine](work-with-modules.md)

[Lehe URL-i loomine](create-page-url.md)

[Avaldamisrühmadega töötamine](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]