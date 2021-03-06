---
title: Laotöö tühistamine erandi käsitlemiseks
description: Selles teemas kirjeldatakse funktsiooni Töö tühistamine, mis võimaldab laoinspektoritel blokeeritud tööd käsitleda.
author: omulvad
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 552c83be411ed0be83b15d2541493ff0213fbe58
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831406"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a>Laotöö tühistamine erandi käsitlemiseks

[!include [banner](../includes/banner.md)]

Tarkvara Microsoft Dynamics 365 Supply Chain Management funktsioon Töö tühistamine võimaldab administraatorist kasutajal tühistada konkreetse laotöö, mis on küll praegu käimas, ent samas süsteemi poolt blokeeritud või seda ei saa erandlike asjaolude tõttu lõpule viia. See funktsioon on atraktiivne ja turvaline alternatiiv SQL-i parandusskriptidele, mis parandavad ebajärjekindlaid andmeid. Siiski, arvestades, et neid skripte taotletakse tavaliselt IT-spetsialistidelt, saavad funktsiooni Töö tühistamine kasutada ettevõttes administraatori õigustega kasutajad.

Funktsioonile Töö tühistamine juurdepääsemiseks avage **Laohaldus** \> **Perioodilised ülesanded** \> **Puhastamine \> Tühista töö**. Määrake dialoogiboksis **Töö tühistamine** tühistatava töö ID ja seejärel valige **OK**.

## <a name="warehouse-work-that-can-be-canceled"></a>Tühistatav laotöö

Lao komplekteerimistoimingute ajal võib töötajatel esineda olukordi, kus nad on kogused registreerinud kui ladustamiskohast kasutuskohta komplekteeritud kogused, kuid seejärel ei saa nad paigutustoimingut registreerida. Ebajärjekindlad laoandmed on sageli, kuid mitte alati, töö blokeerimise põhjus.

Erinevalt tavalisest tühistamis funktsioonist, millele pääseb juurde töö päise nupu **Tühista** abil, ei nõua funktsioon Töö tühistamine, et viimasele lõpetatud tööreale oleks määratud tüüp **paigutamine**. Teisisõnu võib funktsiooni Töö tühistamine tühistamisloogika käitada ka siis, kui tööreal oleva kauba kogus on kasutaja asukohas.

> [!NOTE]
> Töö jaoks, mis tuleb tööpõhjuste tõttu tühistada, peavad lao kasutajad jätkama töölehel asuva tavapärase tühistamisfunktsiooni kasutamist.

Funktsiooni Töö tühistamine abil saab tühistada ainult tööd, mille tüüp on **Müük**, **Edastuse väljaminek**, **Toormaterjalide komplekteerimine** või **Täiendamine**. Tühistamisloogikat ei käivitata külmutatud toormaterjalide komplekteerimise töö või töö puhul, mida saab tühistada tavapärase tühistamisfunktsiooni abil (vt eelmist märkust).

Töö blokeeringu tühistamiseks tühistab süsteem kõik allesjäänud tööread ja fikseerib laoandmed, mis on seotud kasutaja määratud töö ID-ga. Kõik tavapärased lao käitlustoimingud, mis hõlmavad mõjutatud kauba kogust, saavad seejärel jätkuda.

Et panna mõjutatud kaup kindlasse asukohta pärast töö tühistamist, peab kasutaja kasutama mobiilses seadmes varude liikumise või koguse korrigeerimise toimingut.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]