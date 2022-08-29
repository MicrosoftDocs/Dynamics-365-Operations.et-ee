---
title: Elektroonilise aruandluse kaudu elektrooniliste dokumentide loomine ja rakenduse andmete värskendamine
description: Saate kujundada elektroonilise aruandluse (ER) vorminguid, mida saab rakenduses väljaminevate elektrooniliste dokumentide loomiseks kasutada.
author: kfend
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
ms.openlocfilehash: 1be618d16be2ce9e50c2a43864040dfd23a8ff69
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269657"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a>Elektrooniliste dokumentide loomine ja rakenduse andmete värskendamine ER-i abil

[!include [banner](../includes/banner.md)]

Saate kujundada elektroonilise aruandluse (ER) vorminguid, mida saab rakenduses väljaminevate elektrooniliste dokumentide loomiseks kasutada. Saate kujundada ka ER-vorminguid, mis sõeluvad sissetulevaid elektroonilisi dokumente ja kasutavad nende dokumentide sisu rakenduse andmete uuendamiseks.

Selle funktsiooniga saab ühte ER-i vormingut kasutada väljaminevate elektrooniliste dokumentide loomiseks ja seejärel rakenduse andmete uuendamiseks. Seda funktsiooni saab kasutada järgmistes stsenaariumides.

- Rakenduse andmete korduva kasutamise vältimiseks järjestikustes protsessides võite märkida rakenduse andmed kohe pärast nende kasutamist elektrooniliste dokumentide loomiseks. Näiteks saate märkida maksekanded juba töödelduks kohe pärast seda, kui need on koostatud makseteatesse lisatud.
- ER-i loogika abil loodud elektrooniliste dokumentide töötlemise üksikasjade salvestamiseks. Näiteks kordumatu makseteate ID, mis luuakse ER-i avaldise abil. Avaldis põhineb ER-i vormi käitamisel dokumentide loomiseks ER-i dialoogiboksi sisestatud andmetel.

Lisateabe saamiseks selle funktsiooni kohta esitage tegevusjuhiste kogum Elektrooniline aruandlus. Dokumentide loomine rakenduse andmete uuendamisega (osa äriprotsessist 7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)), mis selgitab Intrastati aruandluse ja arhiivimise üksikasju. Teatud etappide läbimiseks nendes tegevusjuhistes on vajalikud järgmised failid. Laadige need failid alla ja salvestage kohalikku arvutisse.

- [Elektroonilise aruandluse andmemudeli konfiguratsioon: Intrastat (mudel)](https://download.microsoft.com/download/9/c/e/9ceeacbe-c13e-422e-96f2-594c4a6b45b7/Intrastatmodel.xml)
- [Elektroonilise aruandluse mudeli vastendamise konfiguratsioon: Intrastat (vastendamine)](https://download.microsoft.com/download/2/1/d/21ddaaeb-64c5-4408-a35f-1ccb922d40a4/Intrastatmapping.xml)
- [Elektroonilise aruandluse vormingu konfiguratsioon: Intrastat (vorming)](https://download.microsoft.com/download/8/b/b/8bbb8891-e88d-4739-b92a-2d1d2fffcb79/Intrastatformat.xml)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
