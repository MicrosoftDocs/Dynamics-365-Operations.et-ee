---
title: Täpsema panga vastavusseviimise importimise häälestus elektroonilise aruandluse abil
description: See artikkel selgitab, kuidas kasutada elektroonilist aruandlust täpsema panga vastavusseviimise impordiprotsessi häälestamiseks.
author: panolte
ms.date: 03/30/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 2ac8811a5c10490d90f782472d3c198474c7edc0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889116"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>Täpsema panga vastavusseviimise importimise häälestus elektroonilise aruandluse abil

[!include [banner](../includes/banner.md)]

Täpsem panga vastavusseviimise funktsioon võimaldab teil importida elektroonilisi pangaväljavõtteid ja viia need automaatselt vastavusse pangakannetega Microsoft Dynamics 365 finantsis. Selles artiklis selgitatakse, kuidas seadistada pangaväljavõtete impordifunktsiooni. Pangaväljavõtte importimise seadistus erineb, olenevalt teie elektroonilise pangaväljavõtte vormingust. Microsoft Dynamics 365 Finantsid toetavad kolme pangaväljavõtte vormingut: ISO20022, MT940 ja BAI2. 

## <a name="set-up-the-electronic-reporting-configuration"></a>Elektroonilise aruandluse konfiguratsiooni seadistamine

1. Minge tööruumide **elektroonilise aruandluse \> juurde**.
2. Microsofti konfiguratsioonipakkuja paanil **valige** hoidlad **·**.
3. Valige **Globaalne** ja seejärel valige **Ava**.
4. Kui tuleb luua ühendus hoidlaga, valige dialoogiaknast sinine link.
5. Konfiguratsiooniloendist otsige pangaväljavõtte **mudeli bai2 \> pangaväljavõtte mudelit**.
6. **Valige BAI2-vorming**.
7. Valige kiirkaardil **Versioonid** uusim versioon ja seejärel käsk **Impordi**.

## <a name="set-up-the-bank-statement-format"></a>Pangaväljavõtte vormingu häälestamine

1. Minge kassa- **ja pangahalduse häälestuse täpsema \>\> panga vastavusseviimise häälestuse pangaväljavõtte \> vormingule**.
2. Valige suvand **Uus**.
3. Seadke väljavõtte **vorming ja** nimeväljad **·**.
4. Märkige ruut **Üldine elektrooniline impordivorming**.
5. Seadke impordivormingu **konfiguratsiooni** väli **BAI2-vormingule**.

## <a name="set-up-the-bank-account"></a>Pangakonto seadistamine

1. Minge jaotisse **Sularaha- ja pangahaldus \> Pangakontod \> Pangakontod**.
2. Avage pangakonto.
3. Seadke vastavusseviimise **kiirkaardil** panga vastavusseviimise **täpsemaks suvandiks** **Jah**.
4. Seadke väljavõtte **vormingu väli** varem loodud **BAI2-vormingule**.

## <a name="import-the-bank-statement"></a>Pangaväljavõtte importimine

1. Avage sularaha- **ja pangahalduse pangaväljavõtte \> vastavusseviimise pangaväljavõtted \>**.
2. Valige pangaväljavõtete **lehe** ülaosas suvand **Impordi väljavõte**.
3. **Seadke väljavõttes** pangakontole väli Pangakonto.
4. Seadke väljavõtte **vormingu väli** varem loodud **BAI2-vormingule**.
5. Valige **sirvimine** ja valige **BAI-fail**.
6. Valige nupp **Laadi üles**.
7. Valitud **faili importimiseks valige OK**.


## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Näited pangaväljavõtte vormingutest ja tehnilistest paigutustest
Allpool on näited täiustatud panga vastavusseviimise impordifaili tehniliste paigutuste määratlustest ja kolmest seotud pangaväljavõtte näidisfailist: [Impodifaili näited](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Tehnilise paigutuse määratlus                             | Pangaväljavõtte näidisfail          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)     |
| DynamicsAXISO20022Layout | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)     |

