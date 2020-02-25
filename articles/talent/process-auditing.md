---
title: Värbamisandmete muudatuste jälgimine
description: Protsessi auditeerimise funktsioon võimaldab teil jälgida, millal kandidaadid, vabad töökohad või tööavaldused muutuvad aruandluse või vastavuse põhjustel.
author: tracykeya
manager: AnnBe
ms.date: 04/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2019 update
ms.openlocfilehash: c009f82e69bff0e4ea540514de8f9e60eca1e466
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006347"
---
# <a name="track-changes-in-recruiting-data"></a>Värbamisandmete muudatuste jälgimine

[!include [banner](includes/banner.md)]

Saate jälgida kandidaatide, vabadele töökohtadele või tööavaldustele tehtud muudatusi, kasutades protsessi auditeerimist. See on kasulik aruandluse või vastavusega seotud põhjustel.

Saa vaadata jälgitud andmeid rakendusega Power BI, kasutades OData konnektorit. Lisateavet vt jaotisest [OData-kanalitega ühendamine Power BI Desktop](https://docs.microsoft.com/power-bi/desktop-connect-odata).

## <a name="track-changes"></a>Jälita muutusi
Muudatuste jälgimiseks värbamisandmetes toimige järgmiselt.

1. Valige [Power Appsis](https://web.powerapps.com) sobiv keskkond.

2. Valige **Sätted** (hammasratta ikoon), valige **Täpsemad kohandused**ja seejärel **Ressursid** jaotises **Arendaja ressursid**. 

3. Lehel **Arendaja ressursid** kopeerige väärtus väljale **Eksemplari veebi API väärtus**. Näiteks võib väärtus välja näha selline: https://yourorgname.api.crm.dynamics.com/api/data/v9.1/.

4. Seejärel saate pärida andmed ühelt järgmistest üksustest.
  - Vaba töökoha ajalugu (msdyn_jobopeninghistories)
  - Tööavalduse ajalugu (msdyn_jobapplicationhistories) 
  - Kandidaadi ajalugu (msdyn_candidatehistories)

## <a name="data-reported"></a>Esitatud andmed

Järgmised andmed on saadaval protsessi auditeerimisel.

| Esitatud andmed | Kirjeldus |
| --- | --- |
| Muudetud (msdyn_ChangedbyId) | Viide kasutajale |
| Koostamise aeg (createdon) |  UTC kuupäev ja kellaaeg, kui muutus juhtus |
| Muutuse tüüp (msdyn_changetype) | Milline muutus juhtus |
| Kandidaatide ühised väärtused, vabad töökohad, <br></br>ja tööavaldus | Loodud<br></br>Värskendatud |
| Tööavalduse ajalugu | Artefakt lisatud <br></br>Artefakt eemaldatud |
| Vaba töökoha ajalugu | TODO: sisestage lisatud <br></br>TODO: sisestus eemaldatud <br></br>TODO:värskendus sisestatud <br></br>Lisati osaleja lisatud <br></br>TODO: osaleja eemaldatud |
| Kandidaadi ajalugu | Artefakt lisatud <br></br>Artefakt eemaldatud <br></br>Töökogemus lisatud <br></br>Töökogemus eemaldatud <br></br>Haridus lisatud <br></br>Haridus eemaldatud <br></br>Oskus lisatud <br></br>Oskus eemaldatud <br></br>Silt lisatud <br></br>Silt eemaldatud <br></br>Suhtlusvõrk lisatud <br></br>Suhtlusvõrk eemaldatud <br></br>Isiklikud andmed lisatud <br></br>Isiklikud andmed uuendatud<br></br> |
| Muudetud väljad (msdyn_changedfields) | JSON-objekti kirje muutis välju, ei pruugi kõigi väljade väärtusi talletada.<br></br><br></br>Loodud ja Värskendatud muudatuste puhul loetletakse loodud või muudetud kirje väljad.<br></br><br></br>Lisatavate muudatuste tüüpide puhul loetletalse tütarkirje väljad.<br></br><br></br>**Näide:**<br></br><br></br>{<br></br>  "msdyn_applyurl": { "newValue": "" },<br></br>  "msdyn_description": { "valueOmitted": True } <br></br>} |
|Tööavalduse ajalugu | Tööavaldus (msdyn_JobapplicatonId)<br></br>Olek (msdyn_status) <br></br>Oleku põhjus (msdyn_statusreason) <br></br>Tagasilükkamise põhjus (msdyn_rejectionreason) |
| Vaba töökoha ajalugu | Vaba töökoht (msdyn_JobopeningId) <br></br>Olek (msdyn_jobopeningstatus) <br></br>Oleku põhjus (msdyn_jobopeningstatusreason) |
| Kandidaadi ajalugu | Kandidaat (msdyn_CandidateId) |
