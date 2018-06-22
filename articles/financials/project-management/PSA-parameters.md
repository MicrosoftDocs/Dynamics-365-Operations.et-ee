---
title: Project Service Automationi integratsiooniparameetrid
description: "Saate konfigureerida andmete vaikesätted Project Service Automationi integreerimisel rakendusega Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 12/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 32f7f70c5b1071cef5a3360ccc09fa2d95fbf9a9
ms.contentlocale: et-ee
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation-integration-parameters"></a>Project Service Automationi integratsiooniparameetrid

Lehel **Project Service Automationi integratsiooniparameetrid** saate konfigureerida andmete vaikesätted Project Service Automationi integreerimisel Finance and Operationsiga. Projektide edukaks sünkroonimiseks Project Service Automationist Finance and Operationsisse tuleb teha järgmised seadistused.

> [!NOTE]
> Projektiülesannete integreerimine, kulukannete kategooriad, tunnihinnangud, kuluhinnangud ja funktsioonide lukustamine on saadaval rakenduse Dynamics 365 for Finance and Operations versioonis 8.0.




| **Vahekaart**                      | **Väli**                          | **Kirjeldus**                    |
|------------------------------|------------------------------------|--------------------------------|
| **Üldine**                  | **Vaikimisi projektitüüp**               | Valige suvandi **Projekti tüüp** vaikesäte, mida kasutatakse projektide sünkroonimisel Project Service Automationist, kui te pole määranud integratsioonimallis vaikeväärtust. Sünkroonimise ajal määratakse uutele projektidele selle väärtusega **projekti tüüp** ja seda võidakse värskendada projektilepingu ridade sünkroonimisel Project Service Automationist.               |
| **Üldine**                  | **Ajakategooria**                      | Valige suvandi **Ajakategooria** vaikesäte, mida kasutatakse tunnihinnangute sünkroonimisel Project Service Automationist. Sünkroonimise ajal määratakse uutele projekti tunnieelarvetele Finance and Operationsis selle väärtusega **kategooria** tunnihinnangute ja tunni tegelike näitajate sünkroonimisel Project Service Automationist.   |
| **Üldine**                  | **Tasukategooria**                       | Valige suvandi **Tasukategooria** vaikesäte, mida kasutatakse tasu tegelike näitajate sünkroonimisel Project Service Automationist. Sünkroonimise ajal määratakse uutele tasukannetele Finance and Operationsis selle väärtusega **kategooria** tasu tegelike näitajate sünkroonimisel Project Service Automationist.          |
| **Projektigrupi vaikeväärtused**   | **Projekti tüüp** | Klõpsake suvandit **Uus**, et lisada rida, kus saate valida projekti tüübi, millele määrata vaike-projektirühm. Konkreetse projekti tüübi saab valida konfiguratsioonis ainult ühe korra.              
|                              | **Projektigrupp**          | Valige määratud projektitüübi jaoks vaike-projektirühm. Kui uued projektid on Project Service Automationist sünkroonitud, määratakse suvandile **Projektirühm** vaikesäte projekti tüübi põhjal, kui te pole integratsioonimallis vaikeväärtust määranud.  |
| **Arvelduse tüübi vaikeväärtused**    | **Arvelduse tüüp** | Klõpsake suvandit **Uus**, et lisada rida, kus saate valida arveldustüübi, millele määrata vaike-reaatribuut. Konkreetse arveldustüübi saab valida konfiguratsioonis ainult ühe korra.          |
|                              | **Rea atribuut**| Valige määratud arveldustüübi jaoks vaike-reaatribuut. Kui uued tunnihinnangud, uued kuluhinnangud või uued tegelikud näitajad on Project Service Automationist sünkroonitud, määratakse suvandile **Rea atribuut** vaikesäte arveldustüübi põhjal.          |
| **Funktsioonide lukustamine**    |                   | Saate valida funktsioonide keelamise Finance and Operationsis projektide ja lepingute puhul, mis pärinevad Project Service Automationist. Näiteks saate välja lülitada lepingute ja projektide redigeerimise võimaluse, luua tööjaotuse struktuure ning sisestada ajatabeleid rakenduses Finance and Operations. Raamatupidamisega seotud väljad on endiselt lubatud, isegi kui need on parameetrisättega kättesaamatuks tehtud. Vaikimisi on kõik funktsioonid lubatud.           |

