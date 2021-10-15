---
title: Kontsernisiseste ostu- ja müügitellimuste loomine mitmes ettevõttes
description: See teema kirjeldab, kuidas luua kontsernisiseseid ostutellimusi või müügitellimusi mitmes ettevõttes
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 5d756a82abb7e7b19080128353d863f29837fc5b
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548212"
---
# <a name="creating-intercompany-purchase-and-sales-orders-in-several-companies"></a>Kontsernisiseste ostu- ja müügitellimuste loomine mitmes ettevõttes

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management ei piirdu ainult ühe tootmisettevõtte ja mitme müügiettevõtte käitlemisega. Kontserni seadistuses võivad kõik ettevõtted olla nii kaubandus- kui ka tootmisettevõtted.

Kui mitu ettevõtet tarnib sama kaupa, saate valida, kellelt kaupa osta ning uuendatud andmed töödeldakse isegi juhul, kui ühest müügitellimusest saab mitu ostutellimust.

Sarnaselt ühe kontsernisisese ostutellimuse automaatse loomisega võite oma ettevõttes luua algse müügitellimuse ja seejärel mitme kontsernisisese ostutellimuse loomisega täidab seda tellimust mitu kontsernisisest hankijaettevõtet. Microsoft Dynamics 365 Supply Chain Management loob hankijaettevõttes kontsernisisesed müügitellimused automaatselt.

Selleks tuleb kõik ettevõtted seadistada kaubandussuhetena. Hankijaettevõtted peavad olema Microsoft Dynamics 365 Supply Chain Managementis seadistatud kontsernisiseste hankijatena ja need peavad olema vastava kauba puhul esmased hankijad. Müügitellimuse puhul tuleb **Kontsernisiseste seadete** kiirkaardil **Päisevaates** valida väli **Automaatsed kontsernisisesed tellimused** ja **Otsetarne** väli. See on vaikesäte.

Looge müügiread tavapärasel viisil. Kui kirjest lahkute, kuvatakse teade, mis teavitab teid kontsernisiseste ostutellimuste ja kontsernisiseste müügitellimuste loomisest. Sõnum sisaldab ka uute tellimuste linke. Teie hankijaettevõtetes loodud kontsernisiseste müügitellimuste vaatamiseks avage algne müügitellimus ja valige vahekaardi **Üldine** jaotises **Seotud teave** suvand **Viited**.

Hankijate jaoks kontsernisiseseste ostutellimuste avamisel sisestab programm Microsoft Dynamics 365 Supply Chain Management iga hankija puhul automaatselt algse müügitellimuse numbri ja kontsernisisese ostutellimuse numbri.

Hankijate jaoks kontsernisiseseste müügitellimuste avamisel sisestab programm Microsoft Dynamics 365 Supply Chain Management iga hankija puhul automaatselt algse müügitellimuse numbri ja kontsernisisese müügitellimuse numbri.

> [!NOTE]
> Kui tellimusel olevad kaubad on olemas ühel kontsernisisesel hankijaettevõttel, kuid puuduvad teisel, siis Microsoft Dynamics 365 Supply Chain Management loob kaupu omava hankijaettevõtte jaoks kontsernisisesed tellimused ja katkestab tellimuste loomise teise ettevõtte jaoks. Sel juhul kuvatakse vastav teade.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
