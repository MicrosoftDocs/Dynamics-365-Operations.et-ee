---
title: Konteinerite tegevuste üksused
description: See artikkel annab teavet konteineri tegevuste kohta, mida kasutatakse konteinerite saatmise edenemise jälgimiseks.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 6a518003f8624ef05ac86be1b963c3f916420278
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/15/2022
ms.locfileid: "9167569"
---
# <a name="container-activities-entity"></a>Konteinerite tegevuste üksused

[!include [banner](../includes/banner.md)]

Konteineritegevusi kasutatakse konteinerite saatmise edenemise jälgimiseks. Iga konteinerite loomise ajal valitud reisimallile määratud teele luuakse kirje. Kirjed luuakse ka siis, kui saadetise konteiner luuakse andmeüksuse kaudu.

Transiidis saadetise konteineri edenemise teave on sageli saadud väliselt allikalt. Konteineri tegevuste üksus võimaldab välist allikat, nt ekspediitaatorit, kirjet otse uuendada. Seetõttu pole andmete käsitsi uuendamine vajalik.

## <a name="container-activities-itmcontaineractivityentity"></a>Konteineri tegevused (ITMContainerActivityEntity)

Täiendavate tegevusekirjete loomiseks saate kasutada konteineri tegevuste üksust (`ITMContainerActivityEntity`). Teise võimalusena saab ekspediiter edastada uuendused kinnitatud tegeliku **lõppkuupäeva väärtuse** jaoks.

| Nimi | Vastendamine | Andmetüüp | Võti | Kohustuslik |
|---|---|---|---|---|
| Tegelik lõppkuupäev | ITMContainerActivityTable.ActualEndDate | Kuupäev ja kellaaeg | Nr | Nr |
| Tarneviis | ItMContainerActivityTable.DlvModeId | Nvarchar(10) | Nr | Nr |
| Eeldatav lõppkuupäev | ITMContainerActivityTable.EsimatedDate | Kuupäev ja kellaaeg | Nr | Nr |
| Rea number | ITMContainerActivityTable.LineNum | Numbriline(32, 16) | **Jah** | Nr |
| Märkmed | ITMContainerActivityTable.Notes | nvarchar(MAX) | Nr | Nr |
| Tegevus | ITMContainerActivityTable.ShipActivityId | Nvarchar(10) | Nr | **Jah** |
| Saatmiskonteiner | ITMContainerActivityTable.ShipContainerId | Nvarchar(20) | **Jah** | **Jah** |
| Reis | ITMContainerActivityTable.ShipId | Nvarchar(20) | **Jah** | **Jah** |
| Etapp | ITMContainerActivityTable.ShipLegId | Nvarchar(20) | Nr | **Jah** |
| Teenusepakkuja | ITMContainerActivityTable.ShipServiceProvider | Nvarchar(20) | Nr | Nr |
| Temperatuur | ITMContainerActivityTable.ShipTemperature | Numbriline(32, 6) | Nr | Nr |
| Laev | ITMContainerActivityTable.ShipVesselId | Nvarchar(20) | Nr | Nr |
| Alguskuupäev | ITMContainerActivityTable.StartDate | Kuupäev ja kellaaeg | Nr | Nr |

## <a name="tracking-control"></a>Jälgimiskontroll

Jälgimiskontrollikeskus võimaldab uuendada määratud lähtevälja, mis käivitatakse määratud sihtvälja uuendamisega. Kui lähtevälja ja sihtvälja väärtust värskendatakse konteineri tegevuste üksuse abil, kuvatakse sihtväljal üksuse väärtus. See käitumine on seotud jälgimiskontrolli kirjetega, mille täitmisaja **tüübi** väärtus *on Loo*.

Kulualade **puhul** *·* *·*, mille oleku uuendamise tüüp on Loo või Tühi (mis on kasutaja määratletud väärtus), uuendab süsteem reisi olekut või sihtvälja vastavalt jälgimiskontrolli konfiguratsioonile.

## <a name="calculated-fields"></a>Arvutatud väljad

Konteineri tegevuse kirje järgmiste väljade väärtused arvutatakse teiste väljade väärtuste alusel. Ehkki neid arvutatud välju ei kaasata andmeüksusesse, määratakse need siis, kui esitatakse arvutuste aluseks olevad väljad.

- **Eeldatavad** = **päevad Eeldatav lõppkuupäev** – **Alguskuupäev**
- **Tegelikud päevad** = **Tegelik lõppkuupäev** – **Alguskuupäev**
