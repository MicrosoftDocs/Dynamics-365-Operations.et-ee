---
title: Funktsionaalsed asukohad ja varad
description: Selles teemas kirjeldatakse funktsionaalseid asukohti ja varasid varahalduses. Varahaldus on täpsem moodul varade ja hooldustööde haldamiseks rakenduses Dynamics 365 Supply Chain Management.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5271b673d758608cae8e43d72b7e75b259d5f142
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024610"
---
# <a name="functional-locations-and-assets"></a>Funktsionaalsed asukohad ja varad

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Selles teemas kirjeldatakse funktsionaalseid asukohti ja varasid varahalduses. Varahaldus on täpsem moodul varade ja hooldustööde haldamiseks rakenduses Dynamics 365 Supply Chain Management.

## <a name="overview"></a>Ülevaade

Varahaldus on integreeritud sujuvalt mitme mooduliga rakenduses Finance and Operations. Järgmisel joonisel on kujutatud liidesed teiste moodulitega.

![Joonis 1](media/01-overview-image.png)

Varahaldus võimaldab teil tõhusalt hallata ja sooritada kõiki ülesandeid, mis on seotud teie ettevõtte mitut tüüpi seadmete haldamise ja hooldamisega. See varustus hõlmab masinaid, tootmisseadmeid ja sõidukeid. Varahaldus toetab lahendusi paljudes tööstusharudes.

Järgmisel joonisel on ülevaade varahalduse põhifunktsioonidest.

![Joonis 2](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a>Funktsionaalsed asukohad ja varad

Funktsionaalseid asukohti kasutatakse varade haldamiseks asukohtades. See haldus hõlmab varade kulude jälgimist funktsionaalsetes asukohtades. Funktsionaalsed asukohad on struktureeritud hierarhiliselt ja asukohtadel võivad olla alamasukohad. Funktsionaalsete asukohtade struktuur on staatiline. Teisisõnu, asukohad ei saa muuta kohti. Varasid saab paigaldada funktsionaalsetele asukohtadele ja vajaduse korral saab neid hiljem installida ka muudesse funktsionaalsetele asukohtadesse.

Varakulud järgivad alati vara asukohta. Teisisõnu, kui installite vara uuele funktsionaalsele asukohale, kasutab vara automaatselt finantsdimensioone, mis on seotud uue funktsionaalse asukohaga. Seetõttu on vara kulud alati seotud funktsionaalse asukohaga, kuhu vara on praegu installitud. See finantsdimensioonide automaatne käsitlemine aitab tagada kulude täieliku jälgimise, kui teie ettevõte teeb projekti juhtimise ja aruandluse funktsionaalsetes asukohtades.

Funktsionaalsete asukohtade hierarhia ehitamine sõltub teie ettevõtte nõuetest sisemise varustuse hoidmise või kliendiseadmete teenindamise jaoks. Järgmisel joonisel on näide funktsionaalsetest asukohtadest, mis põhinevad geograafilistel asukohtadel.

![Joonis 3](media/03-overview-image.png)

Järgmisel joonisel on näide funktsionaalsetest asukohtadest, mis põhinevad kliendid.

![Joonis 4](media/04-overview-image.png)
