---
title: Loo veokiri
description: See teema kirjeldab, kuidas luua veokirja, kui kasutate laohalduse protsesse.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8d5caed5553ad1c7aec5db83591024129aab1264
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "352593"
---
# <a name="create-a-bill-of-lading"></a>Loo veokiri

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas luua veokirja, kui kasutate laohalduse protsesse.  

Veokiri on juriidiline dokument kaupu tarniva ettevõtte ja vedaja vahel. Dokument on tarnitavate kaupadega kaasas ja see on saadetise kviitungiks, kui kaubad tarnitakse sihtkohta. Kui kasutate laohaldust, on veokirja loomiseks kaks viisi.

  -   Looge aruanne käsitsi, kasutades lehte **Veokiri**.
  -   Looge aruanne valikust **Koorma planeerimise töölaud**.

Kui loote veokirja valikust **Koorma planeerimise töölaud**, siis peab koorma olek olema **Välja saadetud** Kui koormas on rohkem kui üks saadetis, luuakse veokiri iga saadetise jaoks. Pärast veokirja loomist saate seda muuta lehel **Veokiri**.

## <a name="master-bill-of-lading"></a>Põhiveokiri
Kui koormas on rohkem kui üks saadetis, saate luua koondveokirja. Sellel on sama paigutus ja teave kui veokirjal, kuid sisaldab kokkuvõtlikku sisu kõikide saadetiste kohta. Kui valiku **Loo põhiveokiri, kui koormas on rohkem kui üks saadetis** sätteks on **Jah** lehel **Transpordihalduse parameetrid**, luuakse koondveokiri automaatselt, kui loote veokirja valikust **Koorma planeerimise töölaud** ja on rohkem kui üks saadetis. Saate ka loendi veokirjadest, klõpsates valikuid **Seotud teave** &gt; **Veokiri**. Kui loote veokirju käsitsi, saate koondveokirja luua lehel **Veokiri**.



