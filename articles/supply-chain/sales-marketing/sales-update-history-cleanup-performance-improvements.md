---
title: Müügiajaloo puhastamise jõudluse täiustused
description: Selles teemas kirjeldatakse müügiajaloo jõudluse parenduste funktsiooni ja selle lubamist.
author: myvakalo
ms.date: 10/05/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d4eeee3c1228b278fea07464f35946c295c5aea8
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/25/2021
ms.locfileid: "7679051"
---
# <a name="saleshistorycleanupperformanceimprovements"></a>Müügiajaloo puhastamise jõudluse täiustused

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)] <!-- GA with 10.0.24 -->

**Müügi värskenduste ajaloo puhastamise** perioodiline töö võib võtta kaua aega, kui seda käitatakse harva suure müügiuuendustega keskkondades. Sellises olukorras võib funktsioon *Müügiajaloo puhastamisjõudluse parendamine* vähendada käituskestust ja parandada usaldusväärsust.

See funktsioon parandab olemasolevat puhastustööd järgmistel viisidel:

- See tükeldab puhastuse partiideks (partii suurust saate kohandamiste kaudu muuta).
- See töötab maksimaalselt 2 tundi (kohandamiste kaudu saate kestust muuta).
- Võimaluse korral võimendatakse andmebaasi võimalusi lukustamise minimeerimiseks ja kannete tabelite ühendamise vältimiseks puhastamise ajal.

Pärast funktsiooni lubamist käitatakse partiitöö **Müügi värskendamise ajaloo puhastamine** (**Müük ja turundus \> Perioodi ülesanded \> Puhastamine \> Müügi värskendamiste ajaloo puhastamine**) nii, nagu seda enne, kuid parema jõudluse ja maksimaalselt 2 tunni jooksul. See tähendab, et teatud andmete säilitamiseks teatud ajavahemiku jooksul võib vaja minna mitut käivitamist.

## <a name="turn-on-the-saleshistorycleanupperformanceimprovements-feature"></a>Lülitage müügiajaloo puhastulemuste täiustamise funktsioon sisse

Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *Müük ja turundus*
- **Funktsiooni nimi:** *Müügiajaloo puhastamise jõudluse täiustused*
