---
title: "Power BI sisu Tegelik võrreldes eelarvega"
description: "Selles teemas kirjeldatakse Power BI sisu Tegelik võrreldes eelarvega. See selgitab juurdepääsu sisus sisalduvatele aruannetele ning annab teavet andmemudeli ja olemite kohta, mida sisu loomiseks kasutati."
author: ryansandness
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: 2a0ad5af4e4d7da09690331dc9d1a51d2e97a664
ms.contentlocale: et-ee
ms.lasthandoff: 12/01/2017

---

# <a name="actual-vs-budget-power-bi-content"></a>Power BI sisu Tegelik võrreldes eelarvega

[!include[banner](../includes/banner.md)]


Selles teemas kirjeldatakse Microsoft Power BI sisu **Tegelik võrreldes eelarvega**. See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks. 

# <a name="overview"></a>Ülevaade

Power BI sisu **Tegelik võrreldes eelarvega** on koostatud inimestele, kes vastutavad oma organisatsioonist tegelike tulemuste jälgimise eest eelarvega võrreldes. Power BI sisu **Tegelik võrreldes eelarvega** toob nähtavale eelarvehälbed. Saate analüüsida jooksva aasta eelarvet kontokategooria, eelarvekoodi, põhikonto, põhikonto kirjelduste või rahandusperioodi järgi, et saada parem ülevaade hälvete põhjusest. 

# <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule
Aruanded Power BI sisust **Tegelik võrreldes eelarvega** kuvatakse tööruumides **Pearaamatu eelarved ja prognoosid** ja **CFO**.

# <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI sisu hulka kuuluvad aruanded
Järgmises tabelis on üksikasjad Power BI sisu **Tegelik võrreldes eelarvega** igal aruandelehel leiduvate mõõdikute kohta.

| Aruanne                      | Mõõdikud |
|-----------------------------|---------|
| Kulud – tegelik võrreldes eelarvega | <ul><li>Selle aasta kulud kokku</li><li>Selle aasta eelarvekulud kokku</li></ul> |
| Tulu – tegelik võrreldes eelarvega  | <ul><li>Selle aasta kogutulu</li><li>Selle aasta eelarvetulu kokku</li><ul> |
| Kulu                     | <ul><li>Selle aasta kulud kokku</li><li>Kulude eesmärk eelarve alusel </li><ul> |
| Tulu                     | <ul><li>Selle aasta kogutulu</li><li>Tulueesmärk eelarve alusel </li><ul> |
| Netotulu                  | <ul><li>Selle aasta netotulu</li><li>Netotulu eesmärk eelarve alusel </li><ul> |

## <a name="extending-the-power-bi-content"></a>Power BI sisu laiendamine
Kasutades teenuses Microsoft Dynamics Lifecycle Services (LCS) olevaid sisupakette, saate pakkuda suurepäraseid analüüsivõimalusi inimestele, kes rakendusse Microsoft Dynamics 365 sisse ei logi. Neid sisupakette saab muuta nii, et need sisaldaksid teisi aruandeid või visuaale, ja avaldada siis sisupaketid analüüsimiseks Power BI.com-i rentnikus. 

Power BI sisu **Tegelik võrreldes eelarvega** leiate LCS-i ühiste vahendite teegist. Lisateavet sisu allalaadimise ja selle rakendamise kohta organisatsioonis vt jaotisest [Power BI sisu Microsoftilt ja teie partneritelt LCS-is](power-bi-content-microsoft-partners.md). Demo vaatamiseks, mis näitab, kuidas Power BI sisu juurutada, vt [Power BI sisu Microsoftilt ja teie partneritelt teenuses Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

# <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused

| Üksus                    | Sisu |
|---------------------------|----------|
| Pearaamatu tegevused | Pearaamatu kandesummad |
| Eelarvetegevused         | Eelarveregistri kandesummad |
| Põhikontod             | Põhikontod, mille alusel aruandeid filtreerida |
| Rahanduskalendrid          | Rahanduskalendrid, mille alusel aruandeid filtreerida |
| Pearaamatud                   | Pearaamatud, mida saab kasutada praeguse pearaamatu aruande filtreerimiseks |
| Eelarvekoodid              | Eelarvekoodid, mille alusel aruandeid filtreerida |
| Juriidilised isikud            | Juriidilised isikud, mida saab kasutada praeguse juriidilise isiku aruande filtreerimiseks |

