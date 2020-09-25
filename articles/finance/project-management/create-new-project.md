---
title: Loo uus projekt
description: See teema sisaldab teavet uue projekti loomise kohta.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8c52b8c1c86ea2f6e03cf439ba5930f1006ab4f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760523"
---
# <a name="create-a-new-project"></a>Loo uus projekt

[!include [banner](../includes/banner.md)]

Uue projekti loomiseks läbige järgmised etapid.

1. Tehke lehel **Projektihaldus** valik **Uus projekt** ja sisestage järgmised väärtused.

    - **Projekti tüüp:** aeg ja materjal
    - **Projekti nimi:** XYZ täiendusfaas 2
    - **Projektigrupp:** TM\_WIP
    - **Projektilepingu ID:** 00000002

2. Valige **Loo projekt**.

## <a name="assign-a-resource-to-a-project"></a>Ressursi määramine projektile

1. Valige lehel **Töötajad** loendist **Töötajad** selle töötaja kirje, kelle jaoks eelnevalt kompetentsid seadistasite, ja avage töötaja kirje.
2. Tehke tegumiriba vahekaardil **Projekt** grupis **Seadistus** valik **Projektide määramine**.
3. Filtreerige lehe **Ressursi kinnitamise projekti määrangud** vahekaardi **Projektid** väljal **Lisa projekt valitud projektidele** projekti **XYZ täiendusfaas 2**.
4. Valige paanilt **Järelejäänud projektid** projekt ja valige siis noolenupp selle lisamiseks paanile **Valitud projektid**.

Vajaduse korral saate ka ressursile kategooriaid määrata. Kategooria tüüp on **Kulu** või **Tulu**. Kategooria tüübi määrab teie organisatsioon. Kui ressursile pole määratud ühtegi kategooriat, otsib Finance üles kulu ja tulu tunnihindade vaikekategooria.

## <a name="set-up-project-resource-and-role-characteristics"></a>Projekti ressursi ja rolli omaduste seadistamine

Projektijuht saab kasutada projekti ressursieralduse funktsiooni projekti jaoks vajalike rollide loomiseks. Rolle saab kasutada juhul, kui kinnitatud ressursid on ressursside reserveerimise ajal veel teadmata. Rolle saab reserveerida ajutiselt plaanitud ressurssidena, et saaksite projekti plaanimise etappe jätkata.

[![Rolli näide](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Stsenaarium:** Contoso palgati täitma aja ja materjali projekti, millel on kinnitatud projekti põhikiri. Noorem-projektijuht täidab veel projekti ulatust. Ressursihaldur tuvastab praegu konkreetseid ressursse, mis uue projektiga töötamiseks reserveeritakse. Projekti kriitilise iseloomu tõttu soovis projekti sponsor ühena rollidest vanem-projektijuhti. Ressursihaldur peab uue ressursi hankima ja määratlema rolli süsteemis, juhul kui noorem-projektijuht vajab projekti plaanimise käigus teavet ressursi kohta.

Järgmised juhised näitavad, kuidas ressursihaldur saab vanem-projektijuhi rolli seadistada ja seostada sellega ressursi omadused. Hiljem saab rolli kasutada vajalikele ressursi kompetentsidele vastavate olemasolevate ressursside otsimiseks.

1. Tehke lehel **Rollide seadistus** valik **Uus** ja sisestage järgmised väärtused.

    - **Rolli ID:** vanem-projektijuht
    - **Kirjeldus:** vanem-projektijuht

2. Valige **Loo**.
3. Valige roll **Vanem-projektijuht** ja siis valige **Omaduste konfigureerimine**.
4. Valige väljalt **Omaduse tüüp** väärtus **Oskus**.
5. Sisestage väljale **Olemasolev omadus** oskus, mida otsida.
6. Valige väljalt **Omaduse tüüp** väärtus **Tunnistus**.
7. Sisestage väljale **Olemasolev omadus** tunnistuse tüüp, mida otsida.

## <a name="assign-a-project-resource-to-a-project"></a>Projekti ressursi määramine projektile

1. Valige lehelt **Kõik projektid** projekt **XYZ täiendusfaas 2**.
2. Tehke vahekaardil **Projektimeeskond ja plaanimine** valik **Lisa**.
3. Valige väljalt **Roll** väärtus **Meeskonnaliige**.
4. Valige **Kalendrist reserveerimine**.
5. Tehke lehel **Ressursi saadavus** valik **Kuva sätted**.
6. Sisestage lehele **Kuvasätete kohandamine** järgmised väärtused.

    - **Kuupäevavahemiku kuva jaoks vormindamine:** päev
    - **Kuva saadavuse kirjeldused:** jah
    - **Kuva järelejääv võimsus:** jah

7. Valige ressursiloendist ressurss.
8. Valige **Fikseeritud reserveerimine** ja **Kogujõudlus**.

## <a name="assign-a-resource-to-a-default-role"></a>Vaikerollile ressursi määramine

Projekti- või ressursihaldurite abistamiseks võite minna veel rohkem süvitsi ressurssides, mida projektile reserveerida saab. Saate seostada vaikerolli olemasoleva ressursiga või äsja omandatud ressursiga. Näiteks kui Daniel palgati, olid tal kogemuse ja oskused ärianalüütiku rolli täitmiseks. Ressursihaldur määras selle rolli Danieli vaikerolliks. Seetõttu lisas ressursihaldur Danieli projektidega töötavate analüütikute kausta.

Ressursi reserveerimise ajal saavad projektijuhid filtreerida rolli ressursse, mis on projektidega töötamiseks saadaval. Nad saavad kasutada neid andmeid ühe kriteeriumina, kui nad teevad ressursside täitmisel mitmel kriteeriumil põhinevaid analüüse. Samuti saavad nad lisada filtrile muid ressursiomadusi, et otsida antud projekti jaoks konkreetsete oskuste, hariduse ja kogemustega ressursse.

**Stsenaarium:** kinnitatud projekt on alanud ja vanem-projektijuhi roll reserveeriti plaanitud ressursina projekti plaanimisetapi käigus. Ressursihaldur on nüüd hankinud ressursi vanem-projektijuhi rolli täitmiseks.

1. Valige lehelt **Ressursside loend** väärtus **Daniel Goldschmidt**.
2. Tehke lehel **Ressursi roll** valik **Uus** ja sisestage järgmised väärtused.

    - **Jõustub:** sisestage jooksev kuupäev.
    - **Aegumine:** sisestage **Mitte kunagi**.
    - **Roll:** sisestage **Vanem-projektijuht**.

3. Valige **Salvesta** ja sulgege seejärel leht.
4. Lisage vahekaardile **Kompetentsid** oskus **ProjectMgmt** ja tunnistus **PMP**.
