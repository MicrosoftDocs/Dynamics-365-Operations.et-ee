---
title: Power BI sisu Tegelik võrreldes eelarvega
description: Selles teemas kirjeldatakse Power BI sisu Tegelik võrreldes eelarvega. See selgitab, kuidas aruannetele juurde pääseda, ja annab andmemudeli kohta teavet.
author: panolte
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 908b96af5b3d67f265953648edd6aa7ec31556a4
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093844"
---
# <a name="actual-vs-budget-power-bi-content"></a>Power BI sisu Tegelik võrreldes eelarvega

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse Microsoft Power BI sisu **Tegelik võrreldes eelarvega**. See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele, ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.

## <a name="overview"></a>Ülevaade

Power BI sisu **Tegelik võrreldes** eelarvega on koostatud inimestele, kes vastutavad oma organisatsioonist tegelike tulemuste jälgimise eest eelarvega võrreldes. Power BI sisu **Tegelik võrreldes eelarvega** toob nähtavale eelarvehälbed. Saate analüüsida jooksva aasta eelarvet kontokategooria, eelarvekoodi, põhikonto, põhikonto kirjelduste või rahandusperioodi järgi, et saada parem ülevaade hälvete põhjusest.

## <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule
Aruanded Power BI sisust **Tegelik võrreldes eelarvega** kuvatakse tööruumides **Pearaamatu eelarved** ja prognoosid ja **CFO**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI sisusse kuuluvad aruanded
Järgmises tabelis on üksikasjad Power BI sisu **Tegelik võrreldes eelarvega** igal aruandelehel leiduvate mõõdikute kohta.

| Aruanne                      | Mõõdikud                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| Kulud – tegelik võrreldes eelarvega | <ul><li>Selle aasta kulud kokku</li><li>Selle aasta eelarvekulud kokku</li></ul>  |
| Tulu – tegelik võrreldes eelarvega  | <ul><li>Selle aasta kogutulu</li><li>Selle aasta eelarvetulu kokku</li><ul>     |
| Kulu                     | <ul><li>Selle aasta kulud kokku</li><li>Kulude eesmärk eelarve alusel</li><ul> |
| Tulu                     | <ul><li>Selle aasta kogutulu</li><li>Tulueesmärk eelarve alusel</li><ul>   |
| Netotulu                  | <ul><li>Selle aasta netotulu</li><li>Netotulu eesmärk eelarve alusel</li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused

| Üksus                    | Sisu                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| Pearaamatu tegevused | Pearaamatu kandesummad                                       |
| Eelarvetegevused         | Eelarveregistri kandesummad                                      |
| Põhikontod             | Põhikontod, mille alusel aruandeid filtreerida                                               |
| Rahanduskalendrid          | Rahanduskalendrid, mille alusel aruandeid filtreerida                                            |
| Pearaamatud                   | Pearaamatud, mida saab kasutada praeguse pearaamatu aruande filtreerimiseks              |
| Eelarvekoodid              | Eelarvekoodid, mille alusel aruandeid filtreerida                                                |
| Juriidilised isikud            | Juriidilised isikud, mida saab kasutada praeguse juriidilise isiku aruande filtreerimiseks |
