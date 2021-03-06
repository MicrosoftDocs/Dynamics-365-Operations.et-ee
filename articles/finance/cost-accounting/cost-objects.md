---
title: Kuluobjekti dimensioonid
description: Kulude analüüsimisel saate kasutada kuluelemendi dimensioone, et määrata, kuhu kulud voolavad. Saate kasutada kuluobjekti dimensioone, et määrata, kuhu peaksite kulud määrama. Teema sisaldab teavet kuluobjekti dimensioonide kohta.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimensionMember, CAMCostObject
audience: Application User
ms.reviewer: roschlom
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 20ae6295389fa3cbaa7c90844d2a90f1e38387c4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818773"
---
# <a name="cost-object-dimensions"></a>Kuluobjekti dimensioonid

[!include [banner](../includes/banner.md)]

Kulude analüüsimisel saate kasutada kuluelemendi dimensioone, et määrata, kuhu kulud voolavad. Saate kasutada kuluobjekti dimensioone, et määrata, kuhu peaksite kulud määrama. Teema sisaldab teavet kuluobjekti dimensioonide kohta.

Kuluobjekt saab olla mis tahes tüüpi objekt, mida soovite hinnata, millele soovite kulusid eraldada või otseselt mõõta. Tüüpilised kuluobjektid hõlmavad tooteid, projekte, ressursse, osakondi, kulukeskuseid ja geograafilisi regioone. Haldus kasutab kuluobjekte, et määrata kulude kogus, kuid samuti selleks, et juhtida tulususe analüüsi.

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a>Kuluobjekti dimensioonid ja kuluobjekti dimensiooni liikmed
Kuluobjekte nimetatakse *kuluobjekti dimensioonideks*. Pärast seda, kui olete otsustanud, millisele olemile kuluobjekti dimensioon peaks viitama, peate määrama individuaalsed dimensiooniväärtused või importima need teistest lähtesüsteemidest kuluarvestusse. Neid individuaalseid dimensiooniväärtuseid nimetatakse *kuluobjekti dimensiooni liikmeteks*. Näiteks soovite kasutada finantsdimensiooni, mida kulukeskuses nimetatakse kuluobjekti dimensiooniks. Nägemaks, kuidas kulud voolavad individuaalsetesse kulukeskustesse, peate importima kuluobjekti dimensiooni liikmed. Sellisel juhul on kuluobjekti dimensiooni liikmed tegelikud kulukeskused, nagu Müük, Tootmine, Administreerimine ja Geograafilised asukohad. Järgmine kuvatõmmis näitab näidet kulukeskustest kuluobjekti dimensioonina, kus selle tegelikud kulukeskused on kuluobjekti dimensiooni liikmed. 

[![Kuvatõmmis kulukeskusest kui kuluobjekti dimensioonist](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)

## <a name="import-cost-object-dimension-members-through-data-connectors"></a>Kuluobjekti dimensiooni liikmete importimine andmekonnektorite kaudu
Kuluobjekti dimensiooni liikmete lihtsamaks importimiseks saate kasutada andmekonnektoreid, et tuua väärtuseid üksustest, mida soovite kasutada kuluobjekti dimensioonidena. Saate kasutada eelnevalt ehitatud andmekonnektoreid või teie ehitatavaid kohandatud andmekonnektoreid.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]