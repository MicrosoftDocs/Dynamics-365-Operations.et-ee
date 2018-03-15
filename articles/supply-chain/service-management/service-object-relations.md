---
title: Hooldusobjekti seosed
description: "Saate luua hooldusobjektide vahelisi seoseid, kas hooldusobjekti ja hooldusleppe või hooldustellimuse vahel."
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 221b9dae7e83e7f4a535ac60f2a2011533d7861c
ms.openlocfilehash: 0e54a0dc9b643077d45fe76e073772e81f99ea44
ms.contentlocale: et-ee
ms.lasthandoff: 02/21/2018

---

# <a name="service-object-relations"></a>Hooldusobjekti seosed 

[!include[banner](../includes/banner.md)]



Saate luua hooldusobjektide vahelisi seoseid, kas hooldusobjekti ja hooldusleppe või hooldustellimuse vahel. Seose loomisel lisate hooldusobjekti hooldusleppele või hooldustellimusele.

Kui seos on loodud, saate lisada hooldusobjekti mistahes hooldusleppe või hooldustellimuse reale.

## <a name="template-boms"></a>Mallkooslused

Saate täpsustada ka objektisuhte mallkooslust. Mallkooslus on teenust osutatavale objektile. Hooldusvisiidi ajal hooldusobjekti komponendi asendamise saate registreerida hoolduse mallkooslusele, kasutades selleks vormi Hooldusobjektid.

## <a name="example"></a>Näide

Te loote hooldusleppe kahe lifti hooldamiseks.
Hooldusleppe identifikaator on SAL-001.

Liftid on objektidena määratud vormis Hooldusobjektid kui EL-S/1000 ja EL-L/1000.

Teie lisate hooldusobjektid EL-S/1000 ja EL-L/1000 teenusleppele.

Registreerige hooldusobjektile koosluse muudatused, kuna te asendasite objekti komponendid, seega lisate hooldusobjekti seosele hoolduskoosluse, nagu kirjeldatud järgmises tabelis.

| Hooldusobjekt | Seos – hoolduslepe | Hoolduskooslus   |
|----------------|------------------------------|---------------|
| EL-S/1000      | ID SAL-001                   | BOM-EL-S/1000 |
| EL-L/1000      | ID SAL-001                   | BOM-EL-L/1000 |

Tänu sellele, et leppele rakenduvad hooldusobjekti seosed, saate nende objektidega luua hooldusleppe ridasid, nagu näidatud järgmises tabelis.

| Kande tüüp | Kategooria           | Hooldusobjekt |
|------------------|--------------------|----------------|
| Tund             | Kontroll         | EL-S/1000      |
| Tund             | Käigukasti puhastamine  | EL-S/1000      |
| Kaup             | Puhastusvahendid | EL-S/1000      |
| Tund             | Kontroll         | EL-L/1000      |
| Tund             | Käigukasti puhastamine   | EL-L/1000      |
| Kaup             | Puhastusvahendid | EL-L/1000      |

Hooldusvisiidi käigus peate asendama lifti EL-S/1000 käigukasti. Objekti komponendi välja vahetamisel pääsete hetke hooldusleppele seadistatud hooldusobjekti seost kasutades ligi koosluse koostajale.

Ligipääs koosluse koostajale hooldusobjekti seost kasutades

1. Hoolduslepped
2. Topeltklõpsake hoolduslepet või klõpsake valikut Hoolduslepe, et luua uus hoolduslepe.
3. Klõpsake vahekaarti Seadistus.
4. Teenusleppele mallkoosluse lisamiseks klõpsake valikut Hooldusobjektid.
5. Vormis Hooldusobjektid klõpsake valikut Kujundamine vormi Kujundamine avamiseks, et muuta mallkooslust.

## <a name="automatically-created-service-orders"></a>Automaatselt loodud hooldustellimused

Hooldusleppele automaatselt hooldustellimuste loomisel liiguvad ka lepete hooldusobjekti seosed loodud hooldustellimustesse.


