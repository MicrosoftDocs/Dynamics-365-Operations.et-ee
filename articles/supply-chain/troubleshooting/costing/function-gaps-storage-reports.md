---
title: Funktsionaalsed lüngad varude väärtuse/vananemise aruannete ja nende ladustamise versioonide vahel
description: Funktsionaalsed lüngad varude väärtuse/vananemise aruannete ja nende ladustamise versioonide vahel
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f74389648034bf036ce48ac84b3421a8a340f105
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686649"
---
# <a name="functional-gaps-between-inventory-valueaging-reports-and-their-storage-versions"></a>Funktsionaalsed lüngad varude väärtuse/vananemise aruannete ja nende ladustamise versioonide vahel

[Lao vananemise aruande ladustamise](/dynamics365/supply-chain/cost-management/inventory-aging-report-storage) ja [Varude väärtuse salvestamise aruande](/dynamics365/supply-chain/cost-management/inventory-value-report-storage) funktsioonid võimaldavad Supply Chain Managementil kuvada suuremahulisi laokandeid. Igal juhul salvestatakse aruande tulemused sirvimiseks ja eksportimiseks, erinevalt nende aruannete mitteladustatavatest versioonidest. Kuid mõned funktsioonid, mis on olemas nende aruannete mitteladustatavates versioonides, pole ladustamisversioonides olemas. Järgmised jaotised summeerivad erinevused ja annavad lahendused.

## <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>Ladustamise aruanded ei sisalda vahesummasid, isegi kui need on aruande kavandis lubatud.

Vahesummad võivad põhjustada probleeme, kui tulemus eksporditakse, eriti siis, kui kasutajad muudavad kirje järjestust.

Vahesummade kontrollimiseks saate tulemuse eksportida Microsoft Excel-isse. Teise võimalusena, kui soovite kontrollida vahekokkuvõtteid Supply Chain Managementi siseselt, kasutage [Funktsioonide haldust](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview), et lubada *Uue ruudustiku juhtelemendi* ja *Rühmitamise ruudustiku* funktsioonid, mis annavad palju paindlikuma viisi, et vaadata iga grupi jaoks veeru alusel vahekokkuvõtet. Lisateavet vt jaotisest [Ruudustiku võimalused](/dynamics365/fin-ops-core/fin-ops/get-started/grid-capabilities).

## <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>Varude väärtuse ladustamise aruanne ei toeta pearaamatu konto teavet.

Saate kasutada protsessi saldot, et saada lao kontode saldo ja võrrelda seda **Varude väärtuse ladustamise** aruandega.
