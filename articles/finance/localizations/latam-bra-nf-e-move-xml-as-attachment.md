---
title: NF-e XML-failide teisaldamine manustena
description: See teema selgitab, kuidas teisaldada NF-e XML-faile Microsoftist või andmebaasist Dynamics 365 Finance välja ja teha need Dynamics 365 Supply Chain Management manustena kättesaadavaks.
author: gionoder
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2022-01-27
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: c7b82d486cecf6b20f1283fa609c360b3003efca
ms.sourcegitcommit: ebf6546835e4d6a80aea1dfae81e119e294387f0
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/12/2021
ms.locfileid: "7799555"
---
# <a name="move-nf-e-xml-files-as-attachments"></a>NF-e XML-failide teisaldamine manustena

[!include [banner](../includes/banner.md)] 


Kui väljastatakse elektroonilisi finantsdokumente (NF-e), luuakse XML-failid ja salvestatakse Microsofti ja Dynamics 365 Finance Dynamics 365 Supply Chain Management andmebaasides. Brasiilia lokaliseerimisel saate kasutada NF-e XML-i teisaldamist manuse funktsioonina nende XML-failide tarbitava **·** andmebaasi ruumi vabastamiseks.

Konkreetse kuupäevavahemiku ja fiskaalettevõtte jaoks teisaldab funktsioon NF-e XML-failid finantside või tarneahela halduse andmebaasist bloobisalvestusse oma Azure'i kordustellimusest. See liikumine muudab failid kättesaadavaks ainult manustena. Kui XML-failid on edukalt bloobisalvestusse teisaldatud, kustutatakse originaalfailid finants- või tarneahela halduse andmebaasist. Seetõttu vabastatakse andmebaasi ruum, mida need failid kasutavad.

Järgige neid samme, et lubada **NF-e XML-i teisaldamine manuse** funktsioonina.

1. Finantside või tarneahela halduses avage **funktsioonihalduse** tööruum.
2. Vahekaardil **Kõik** otsige ja valige **NF-e XML-i teisaldamine manuse** funktsioonina.
3. Valige **Luba kohe**.

Järgige neid samme NF-e XML-failide teisaldamiseks manustena.

1. Minge **müügireskontro** \> **·** \> **finantsdokumentidesse Elektroonilised** \> **finantsdokumendid Teisalda NF-e XML** manustena.
2. Valige **väljadel** Alates ja Kuni **·** kuupäevani algus- ja lõppkuupäevad.
3. Valige **väärtus väljal** Fiskaalettevõtte ID.
4. Valige nupp **OK**.

> [!IMPORTANT]
> See protsess ei ole tühistatav. Pärast NF-e XML-failide teisaldamist saavad kasutajad neid vaadata ainult valides **Manused** finantsdokumendi **lehe** ülaosas.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
