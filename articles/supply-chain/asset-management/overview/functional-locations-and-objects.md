---
title: Töö asukohad ja varad
description: See artikkel kirjeldab varahalduse funktsiooniasukohti ja varasid. Varahaldus on täpsem moodul varade ja hooldustööde haldamiseks rakenduses Dynamics 365 Supply Chain Management.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d8d155b8bbf981408f6f15e914fc3bb1da25c9c
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111072"
---
# <a name="functional-locations-and-assets"></a>Töö asukohad ja varad

[!include [banner](../../includes/banner.md)]

 

See artikkel kirjeldab varahalduse funktsiooniasukohti ja varasid. Varahaldus on täpsem moodul varade ja hooldustööde haldamiseks rakenduses Dynamics 365 Supply Chain Management.

## <a name="overview"></a>Ülevaade

Varahaldust integreeritakse sujuvalt mitme mooduliga muude finantside ja toimingute rakendustega. Järgmisel joonisel on kujutatud liidesed teiste moodulitega.

![Diagramm, mis näitab, kuidas varahaldus liidestub teiste moodulitega.](media/01-overview-image.png)

Varahaldus võimaldab teil tõhusalt hallata ja sooritada kõiki ülesandeid, mis on seotud teie ettevõtte mitut tüüpi seadmete haldamise ja hooldamisega. See varustus hõlmab masinaid, tootmisseadmeid ja sõidukeid. Varahaldus toetab lahendusi paljudes tööstusharudes.

Järgmisel joonisel on ülevaade varahalduse põhifunktsioonidest.

![Diagramm, mis näitab varahalduse põhifunktsioone.](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a>Töö asukohad ja varad

Funktsionaalseid asukohti kasutatakse varade haldamiseks asukohtades. See haldus hõlmab varade kulude jälgimist funktsionaalsetes asukohtades. Funktsionaalsed asukohad on struktureeritud hierarhiliselt ja asukohtadel võivad olla alamasukohad. Funktsionaalsete asukohtade struktuur on staatiline. Teisisõnu, asukohad ei saa muuta kohti. Varasid saab paigaldada funktsionaalsetele asukohtadele ja vajaduse korral saab neid hiljem installida ka muudesse funktsionaalsetele asukohtadesse.

Varakulud järgivad alati vara asukohta. Teisisõnu, kui installite vara uuele funktsionaalsele asukohale, kasutab vara automaatselt finantsdimensioone, mis on seotud uue funktsionaalse asukohaga. Seetõttu on vara kulud alati seotud funktsionaalse asukohaga, kuhu vara on praegu installitud. See finantsdimensioonide automaatne käsitlemine aitab tagada kulude täieliku jälgimise, kui teie ettevõte teeb projekti juhtimise ja aruandluse funktsionaalsetes asukohtades.

Funktsionaalsete asukohtade hierarhia ehitamine sõltub teie ettevõtte nõuetest sisemise varustuse hoidmise või kliendiseadmete teenindamise jaoks. Järgmisel joonisel on näide funktsionaalsetest asukohtadest, mis põhinevad geograafilistel asukohtadel.

![Diagramm, mis näitab töö asukohti geograafiliste asukohtade põhjal.](media/03-overview-image.png)

Järgmisel joonisel on näide funktsionaalsetest asukohtadest, mis põhinevad kliendid.

![Diagramm, mis näitab töö asukohti klientide põhjal.](media/04-overview-image.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
