---
title: Varude märkimine planeerimise optimeerimisega
description: See teema annab teavet valikute kohta, mis on saadaval varude märkimiseks, kui kasutate planeerimise optimeerimist.
author: ChristianRytt
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: dc94ca8b15d626d8ff64f50718d7d2e3e0326144465f3d27787805220842849f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6711901"
---
# <a name="inventory-marking-with-planning-optimization"></a>Varude märkimine planeerimise optimeerimisega

[!include [banner](../../includes/banner.md)]

See teema annab teavet valikute kohta, mis on saadaval varude märkimiseks, kui kasutate planeerimise optimeerimist.

*Märkimist* kasutatakse pakkumise ja nõudluse linkimiseks. See meenutab *sidumist*, mis näitab, kuidas koondplaneerimise abil soovitakse nõudlusele vastata. Planeerimise vaatepunktist on peamiseks erinevuseks see, et märgistus on sidumisest püsivam.

Märgistus võeti kasutusele, et toetada spetsiaalseid kuluarvestuse stsenaariume FIFO-laomudeli (esimesena sisse, esimesena välja) ja LIFO-laomudeli (viimasena sisse, esimesena välja) korral. Kuid seda kasutatakse nüüd ka mõne mittekulupõhise stsenaariumi puhul. Pakkumise ja nõudluse vaheline märgistus on valikuline ja peaaegu püsiv. Kasutaja saab märgistuse eemaldada käsitsi või kasutades müügitellimusrea jaotamist, kus on valitud suvand **Eemalda märgistus**.

Sidumist juhitakse laovarude planeerimise ajal koondplaneerimise käigus, et siduda nõudlus vajaliku pakkumisega. Sidumist saab uuendada igaks planeerimiseks, et optimeerida pakkumist, mis on vajalik nõudluse katmiseks. Kui koondplaneerimisel värskendatakse sidumiseteavet, arvestatakse olemasoleva märgistusega.

Sidumist alustatakse vastava märgistuse, vabade reserveeringute ja tellimuse reserveeringute kaasamisega järgmises järjestuses.

1. Nõudluse ja tarnimise vaheline märgistus
1. Vabad reserveeringud
1. Tellimuse reserveeringud

Kui kinnitate plaanitud tellimust, pakutakse dialoogiboksis **Kinnitamine** välja **Märkimise värskendamine**, mida saate kasutada kinnitamise ajal loodud tellimuste märkimissuvandite määramiseks. Valige üks järgmistest väärtustest.

- **Ei** – varude märkimist ei rakendata.
- **Tavaline** – varude märkimine värskendatakse sidumise alusel. Vajaduse tellimus (nõudlus) märgitakse täitmise tellimusega (pakkumisega) võrreldes. Kui täitmise tellimusele jääb mõni kogus alles, siis seda ei märgita ja viideteteavet ei lisata. Näiteks kui müügitellimus (100 ea) on seotud ostutellimusega (150 ea), määratakse viiteteave ainult müügitellimusele.
- **Laiendatud** – märgitakse nii vajaduse (nõudluse) kui täitmise (pakkumise) tellimused, sõltumata sellest, kas täitmise tellimusele jääb teatud kaubakogus või mitte. Näiteks kui müügitellimus (100 ea) on seotud ostutellimusega (150 ea), määratakse viiteteave nii müügi- kui ka ostutellimusele.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]