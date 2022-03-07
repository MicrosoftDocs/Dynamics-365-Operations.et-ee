---
title: Likviidsuse planeerimine
description: See teema kirjeldab rahavoo prognoosimise võimekust.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ad568fcd126ad3dc9e5ff269cc3bc99b218e822a
ms.sourcegitcommit: 822aea26c5da259efe11ff3b3dc4cf1598425689
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386609"
---
# <a name="cash-flow-forecast"></a>Likviidsuse planeerimine

[!include [banner](../includes/banner.md)]

Rahavoog on igale ärile kriitilise tähtsusega. Isegi tulusatel ettevõtetel võib tekkida maksejõuetus, kui nad ei säilita vahetute vajaduste täitmiseks rahavoogu. Finantsülevaadete rahavoo prognoosimise võimalus võib aidata ettevõtetel tõhusalt jälgida ja hallata oma sularahasaldot. See funktsioon kasutab masinõppimist, et aidata ettevõtetel prognoosida rahavoogusid täpsemalt kui varem. Samuti võib see aidata juhtidel teha otsuseid, mis optimeerivad võimalusi oma praeguse sularahajäägi kontekstis. 

Enamiku ettevõtete puhul on rahavoo haldamine ja rahavoo prognoosimine tüütu, korduv ja käsitsi protsess. Enamik ettevõtteid tuginevad Microsoft Exceli lahendustele, mis võib olla erineva keerukuse astmega. Rahavoogude täpse prognoosimise väljakutsed hõlmavad järgmist.

- Andmed ei ole otsustajate jaoks kättesaadavad, kuna need on mitmes kohas hajutatud, sealhulgas järgnevates kohtades. 
  - Raamatupidamise või ettevõtte ressursside planeerimise süsteem
  - Finantsplaneerimise tarkvara
  - Excel
  - Täiendavad tarkvararakendused 
- Prognoosimine põhineb sisemistel teadmistel, mis paiknevad iga domeeni või osakonna nn hoidlates.
- Rahavoo prognoosimise täpsuse mõõtmine pärast finantside realiseerimist on ebakorrapärane ja keeruline.
    
## <a name="details-of-the-cash-flow-forecasts-capability"></a>Rahavoo prognoosimise võimaluse üksikasjad
Rahavoo prognoosimise funktsioon sisaldab järgmisi võimalusi. 

- Muudab rahavoo andmete integreerimise välistest süsteemidest rakendusse Dynamics 365 Finance lihtsaks. Rahavoo prognoosid võivad kasutada ka andmete importimise ja eksportimise raamistikku. Selle raamistiku abil on Exceli ODataga integreerimine lihtne. Samuti saate kombineerida mitmest allikast pärinevaid andmeid, et luua terviklik rahavoo lahendus. 

- Tutvustab nutikat sularahajääki. Sularahajääl luuakse kliendi maksekäitumise põhjal, et prognoosida aja, millal ettevõte võib oodata sularaha saabumist oma kontodele. Samuti analüüsitakse maksvate hankijate ajaloolisi mustreid, et ennustada tulevaste arvete ja tellimuste eest tasumist. 

- Tutvustab nutikat rahavoo prognoosimist pikaajaliseks prognoosimiseks, kasutades ajaseeriate prognoosimist läbi automaatset integreerimist AI Builderiga.

- Võimaldab salvestada kindla rahavoo positsiooni või prognoosid, neid redigeerida ning seejärel lihtsalt võrrelda ja mõõta prognoosi jõudlust võrreldes tegelike finantsnäitajatega.

- Võimaldab põhjuste ja tagajärgede analüüsi hetktõmmise võrdluse kaudu. Näiteks saate luua mitu hetktõmmist, mis esindavad teie rahavoogude optimistlikke, pessimistlikke ja kõige realistlikumaid vaateid ning võrrelda ja vaadata seejärel erinevusi.

- Pakub võimalust vaadata rahavoo prognoosi mitmes valuutas, erinevates juriidilistes olemites ning filtreerida ja vaadata rahavoogu konkreetsel pangakontol. 

- Võimaldab filtreerida ja vaadata finantsdimensiooniga seotud pangakontosid.

Rakenduse Dynamics 365 Finance rahavoo prognoosimise funktsioon võimaldab teie organisatsioonil muuta tüütu, keeruline ja korduv rahavoo prognoosimine lihtsaks automatiseeritud protsessiks. Rahavoo prognoosimise kõige tüütumate aspektide automatiseerimine võimaldab teil keskenduda kriitilise otsuse tegemisele, et saavutada soovitud äritulemusi.

## <a name="setting-up-dimensions-for-cash-flow-forecasting"></a>Rahavoo prognoosimise jaoks dimensioonide seadistamine
Lehe **Rahavoo prognoosimise seadistus** uus vahekaart võimaldab teil juhtida, milliseid finantsdimensioone tööruumis **Rahavoo prognoosimine** kasutada. See vahekaart ilmub ainult siis, kui rahavoo prognoosimise funktsioon on lubatud. 

Vahekaardil **Dimensioonid** tehke dimensioonide loendis filtreerimiseks valik ja kasutage nooleklahve, et liigutada need parempoolsesse veergu. Rahavoo prognoosimise andmete filtreerimiseks saab valida ainult kaks dimensiooni. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
