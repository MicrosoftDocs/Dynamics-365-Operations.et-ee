---
title: Hooldusobjekti seosed
description: Saate luua hooldusobjektide vahelisi seoseid, kas hooldusobjekti ja hooldusleppe või hooldustellimuse vahel.
author: sorenva
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 831db29589826904666049edbc8be0c38e1d02a5
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676631"
---
# <a name="service-object-relations"></a>Hooldusobjekti seosed 

[!include [banner](../includes/banner.md)]

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

Teenusvisiidi käigus peate asendama lifti EL-S/1000 käigukasti. Objekti komponendi välja vahetamisel pääsete hetke hooldusleppele seadistatud hooldusobjekti seost kasutades ligi koosluse koostajale.

Ligipääs koosluse koostajale hooldusobjekti seost kasutades

1. Hoolduslepped
2. Topeltklõpsake hoolduslepet või klõpsake valikut Hoolduslepe, et luua uus hoolduslepe.
3. Klõpsake vahekaarti Seadistus.
4. Teenusleppele mallkoosluse lisamiseks klõpsake valikut Hooldusobjektid.
5. Vormis Hooldusobjektid klõpsake valikut Kujundamine vormi Kujundamine avamiseks, et muuta mallkooslust.

## <a name="automatically-created-service-orders"></a>Automaatselt loodud hooldustellimused

Hooldusleppele automaatselt hooldustellimuste loomisel liiguvad ka lepete hooldusobjekti seosed loodud hooldustellimustesse.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]