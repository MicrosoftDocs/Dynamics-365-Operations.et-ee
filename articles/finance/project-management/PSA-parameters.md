---
title: Project Service Automationi integratsiooniparameetrid
description: Selles teemas selgitatakse, kuidas konfigureerida vaikeandmete sisestamise viisi, kui integreerite Microsoft Dynamics 365 for Project Service Automationi Microsoft Dynamics 365 Financeiga.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: f7cef5384812e0dcb7d5e084ddd7668a7687a259
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174828"
---
# <a name="project-service-automation-integration-parameters"></a>Project Service Automationi integreerimisparameetrid

[!include[banner](../includes/banner.md)]

Lehel **Project Service Automationi integratsiooniparameetrid** saate konfigureerida vaikeandmete sisestamise viisi, kui integreerite Dynamics 365 Project Service Automationi Dynamics 365 Financeiga. Projektide edukaks sünkroonimiseks Project Service Automationist Finance’i peate seadistama järgmised väljad.

> [!NOTE]
> - Versioonis 8.0 on saadaval projektiülesannete integreerimine, kulukannete kategooriad, tunnihinnangud, kuluhinnangud ja funktsioonide lukustamine.
> - Tegelike näitajate integratsioon on saadaval versioonis 8.0.1 või uuemas.


| Tabeldusklahv TAB                    | Väli                | Kirjeldus |
|------------------------|----------------------|-------------|
| Üldine                | Vaikimisi projektitüüp | Saate valida vaike-projektitüübi. Kui projektid sünkroonitakse Project Service Automationist, kasutatakse seda väärtust, kui te pole määranud integratsioonimallis vaikeväärtust. Sünkroonimise ajal määratakse uute projektide väljale **Projektitüüp** see väärtus. Kuid väärtust võidakse värskendada, kui projekti lepinguread sünkroonitakse Project Service Automationist. |
|                        | Ajakategooria        | Saate valida vaike-ajakategooria. Seda väärtust kasutatakse eeldatava tundide arvu sünkroonimisel Project Service Automationist. Kui eeldatavad tunnid ja tunni tegelikud näitajad sünkroonitakse Project Service Automationist, määratakse uue projekti tunnieelarvete väljale **Kategooria** Finance’is see väärtus. |
|                        | Tasukategooria         | Saate valida vaike-tasukategooria. Seda väärtust kasutatakse tasu tegelike näidajate sünkroonimisel Project Service Automationist. Tasu tegelike näitajate sünkroonimisel Project Service Automationist määratakse uute tasukannete väljale **Kategooria** Finance’is see väärtus. |
| Projektigrupi vaikeväärtused | Projekti tüüp         | Klõpsake nuppu **Uus**, et lisada rida, kus saate valida projekti tüübi, mille jaoks määrata vaike-projektirühm. Konkreetse projekti tüübi saab valida konfiguratsioonis ainult ühe korra. |
|                        | Projektigrupp        | Valige valitud projektitüübi jaoks vaike-projektirühm. Kui uued projektid on Project Service Automationist sünkroonitud, määratakse väljale **Projektirühm** projektitüübi vaikesäte, kui te pole integratsioonimallis vaikeväärtust määranud. |
| Arvelduse tüübi vaikeväärtused  | Arvelduse tüüp         | Klõpsake suvandit **Uus**, et lisada rida, kus saate valida arveldustüübi, mille jaoks määrata vaike-reaatribuut. Konkreetse arveldustüübi saab valida konfiguratsioonis ainult ühe korra. |
|                        | Rea atribuut        | Valige valitud arveldustüübi jaoks vaike-reaatribuut. Kui uued tunnihinnangud, uued kuluhinnangud või uued tegelikud näitajad on Project Service Automationist sünkroonitud, määratakse väljale **Rea atribuut** arveldustüübi vaikeväärtus. |
| Funktsioonide lukustamine  | Pole kohaldatav       | Saate valida funktsioonide keelamise Finance’is projektide ja lepingute puhul, mis pärinevad Project Service Automationist. Näiteks saate välja lülitada lepingute ja projektide redigeerimise võimaluse, luua tööjaotuse struktuure ning sisestada ajatabeleid rakenduses Finance. Raamatupidamisega seotud väljad on endiselt lubatud, isegi kui need on parameetrisättega kättesaamatuks tehtud. Vaikimisi on kõik funktsioonid lubatud. |
