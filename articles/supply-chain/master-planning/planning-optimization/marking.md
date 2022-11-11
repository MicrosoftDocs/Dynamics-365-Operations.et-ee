---
title: Varude märkimine
description: See artikkel annab teavet valikute kohta, mis on saadaval lao märkimiseks kinnitatud tellimustes.
author: t-benebo
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
ms.author: benebotg
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: c86db6a670d7d0f7bfe74b7466b9bce766e4a08d
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740572"
---
# <a name="inventory-marking"></a>Varude märkimine

[!include [banner](../../includes/banner.md)]

See artikkel annab teavet valikute kohta, mis on saadaval lao märkimiseks kinnitatud tellimustes.

*Märkimist* kasutatakse pakkumise ja nõudluse linkimiseks. See meenutab *sidumist*, mis näitab, kuidas koondplaneerimise abil soovitakse nõudlusele vastata. Planeerimise vaatepunktist on peamiseks erinevuseks see, et märgistus on sidumisest püsivam.

Märgistus võeti kasutusele, et toetada spetsiaalseid kuluarvestuse stsenaariume FIFO-laomudeli (esimesena sisse, esimesena välja) ja LIFO-laomudeli (viimasena sisse, esimesena välja) korral. Kuid seda kasutatakse nüüd ka mõne mittekulupõhise stsenaariumi puhul. Pakkumise ja nõudluse vaheline märgistus on valikuline ja peaaegu püsiv. Kasutaja saab märgistuse eemaldada käsitsi või kasutades müügitellimusrea jaotamist, kus on valitud suvand **Eemalda märgistus**.

Sidumist juhitakse laovarude planeerimise ajal koondplaneerimise käigus, et siduda nõudlus vajaliku pakkumisega. Sidumist saab uuendada igaks planeerimiseks, et optimeerida pakkumist, mis on vajalik nõudluse katmiseks. Kui koondplaneerimisel värskendatakse sidumiseteavet, arvestatakse olemasoleva märgistusega.

Sidumist alustatakse vastava märgistuse, vabade reserveeringute ja tellimuse reserveeringute kaasamisega järgmises järjestuses.

1. Nõudluse ja tarnimise vaheline märgistus
1. Vabad reserveeringud
1. Tellimuse reserveeringud

Kui kinnitate plaanitud tellimust, pakutakse dialoogiboksis **Kinnitamine** välja **Märkimise värskendamine**, mida saate kasutada kinnitamise ajal loodud tellimuste märkimissuvandite määramiseks. Valige üks järgmistest väärtustest.

- *Ei* – varude märkimist ei rakendata.
- *Tavaline* – varude märkimine värskendatakse sidumise alusel. Vajaduse tellimus (nõudlus) märgitakse täitmise tellimusega (pakkumisega) võrreldes. Kui täitmise tellimusele jääb mõni kogus alles, siis seda ei märgita ja viideteteavet ei lisata. Näiteks kui müügitellimus (100 ea) on seotud ostutellimusega (150 ea), määratakse viiteteave ainult müügitellimusele.
- *Laiendatud* – märgitakse nii vajaduse (nõudluse) kui täitmise (pakkumise) tellimused, sõltumata sellest, kas täitmise tellimusele jääb teatud kaubakogus või mitte. Näiteks kui müügitellimus (100 ea) on seotud ostutellimusega (150 ea), määratakse viiteteave nii müügi- kui ka ostutellimusele.
- *Ühetasemeline* – kasutatakse ühetaseme märkimist. Ühetasemeline märgistus märgib ainult põhikaupa, mitte selle koosluse komponente. Seetõttu saate pärast kinnitamist säilitada tootmistellimuste komponentide määramise paindlikuna. Ühetasemeline märkimine võimaldab süsteemil optimeerida viimase minuti nõudluse muudatusi. Standardses *ühetaseme* märkimises märgitakse vajaduse tellimused nende täitmistellimustele vastamiseks, kuid täitmistellimusi ei märgita, kui nende kogus on järelejääv.
- *Ühetasemeline laiendatud* – kasutatakse ühetaseme märkimist. Laiendatud *ühetasemeline* märgistus näitab vajadusetellimusi nende täitmistellimustega seoses ja täitmistellimused märgitakse alati, olenemata sellest, kas mingi kogus jääb alles.

Süsteemi jaoks vaikemärkimissuvandi seadmine minge koondplaneerimise **seadistuse \>\> koondplaneerimise parameetritesse**. Seejärel seadke vahekaardil **Standardne uuendamine** välja Uuenda märkimine **väärtuseks** eelistatud suvand.

> [!NOTE]
> Ühetasemeline *standard* ja *ühe taseme laiendatud* valikud on saadaval *ainult* siis, kui vastavalt tellimusele tarnimise automatiseerimise funktsioon on teie süsteemis lubatud. Lisateavet selle funktsiooni ja selle lubamise kohta vt tellimusele [tarnimise automatiseerimise kohta](../make-to-order-supply-automation.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
