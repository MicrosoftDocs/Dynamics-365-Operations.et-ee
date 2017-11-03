---
title: Kuluobjekti dimensioonid
description: "Kulude analüüsimisel saate kasutada kuluelemendi dimensioone, et määrata, kuhu kulud voolavad. Saate kasutada kuluobjekti dimensioone, et määrata, kuhu peaksite kulud määrama. Teema sisaldab teavet kuluobjekti dimensioonide kohta."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimensionMember
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ed6aa29234f8e9dc8dbb4835ec260adc538989d3
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="cost-object-dimensions"></a>Kuluobjekti dimensioonid

[!include[banner](../includes/banner.md)]


Kulude analüüsimisel saate kasutada kuluelemendi dimensioone, et määrata, kuhu kulud voolavad. Saate kasutada kuluobjekti dimensioone, et määrata, kuhu peaksite kulud määrama. Teema sisaldab teavet kuluobjekti dimensioonide kohta.

Kuluobjekt saab olla mis tahes tüüpi objekt, mida soovite hinnata, millele soovite kulusid eraldada või otseselt mõõta. Tüüpilised kuluobjektid hõlmavad tooteid, projekte, ressursse, osakondi, kulukeskuseid ja geograafilisi regioone. Haldus kasutab kuluobjekte, et määrata kulude kogus, kuid samuti selleks, et juhtida tulususe analüüsi.

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a>Kuluobjekti dimensioonid ja kuluobjekti dimensiooni liikmed
Kuluobjekte nimetatakse *kuluobjekti dimensioonideks*. Pärast seda, kui olete otsustanud, millisele olemile kuluobjekti dimensioon peaks viitama, peate määrama individuaalsed dimensiooniväärtused või importima need teistest lähtesüsteemidest kuluarvestusse. Neid individuaalseid dimensiooniväärtuseid nimetatakse *kuluobjekti dimensiooni liikmeteks*. Näiteks soovite kasutada finantsdimensiooni, mida kulukeskuses nimetatakse kuluobjekti dimensiooniks. Nägemaks, kuidas kulud voolavad individuaalsetesse kulukeskustesse, peate importima kuluobjekti dimensiooni liikmed. Sellisel juhul on kuluobjekti dimensiooni liikmed tegelikud kulukeskused, nagu Müük, Tootmine, Administreerimine ja Geograafilised asukohad. Järgmine kuvatõmmis näitab näidet kulukeskustest kuluobjekti dimensioonina, kus selle tegelikud kulukeskused on kuluobjekti dimensiooni liikmed. 

[![kuluobjekti-dimensioonid](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)

## <a name="import-cost-object-dimension-members-through-data-connectors"></a>Kuluobjekti dimensiooni liikmete importimine andmekonnektorite kaudu
Kuluobjekti dimensiooni liikmete lihtsamaks importimiseks saate kasutada andmekonnektoreid, et tuua väärtuseid üksustest, mida soovite kasutada kuluobjekti dimensioonidena. Saate kasutada eelnevalt ehitatud andmekonnektoreid või teie ehitatavaid kohandatud andmekonnektoreid.




