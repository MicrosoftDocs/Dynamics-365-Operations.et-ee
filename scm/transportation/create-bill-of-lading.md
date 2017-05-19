---
title: Loo veokiri
description: See teema kirjeldab, kuidas luua veokirja, kui kasutate laohalduse protsesse.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 2a0ce07dab60b8ad660008cd77fbeadbf652224e
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="create-a-bill-of-lading"></a>Loo veokiri

[!include[banner](../includes/banner.md)]


See teema kirjeldab, kuidas luua veokirja, kui kasutate laohalduse protsesse.  

Veokiri on juriidiline dokument kaupu tarniva ettevõtte ja vedaja vahel. Dokument on tarnitavate kaupadega kaasas ja see on saadetise kviitungiks, kui kaubad tarnitakse sihtkohta. Kui kasutate laohaldust, on veokirja loomiseks kaks viisi.

  -   Looge aruanne käsitsi, kasutades lehte **Veokiri**.
  -   Looge aruanne valikust **Koorma planeerimise töölaud**.

Kui loote veokirja valikust **Koorma planeerimise töölaud**, siis peab koorma olek olema **Välja saadetud** Kui koormas on rohkem kui üks saadetis, luuakse veokiri iga saadetise jaoks. Pärast veokirja loomist saate seda muuta lehel **Veokiri**.

## <a name="master-bill-of-lading"></a>Põhiveokiri
Kui koormas on rohkem kui üks saadetis, saate luua koondveokirja. Sellel on sama paigutus ja teave kui veokirjal, kuid sisaldab kokkuvõtlikku sisu kõikide saadetiste kohta. Kui valiku **Loo põhiveokiri, kui koormas on rohkem kui üks saadetis** sätteks on **Jah** lehel **Transpordihalduse parameetrid**, luuakse koondveokiri automaatselt, kui loote veokirja valikust **Koorma planeerimise töölaud** ja on rohkem kui üks saadetis. Saate ka loendi veokirjadest, klõpsates valikuid **Seotud teave** &gt; **Veokiri**. Kui loote veokirju käsitsi, saate koondveokirja luua lehel **Veokiri**.




