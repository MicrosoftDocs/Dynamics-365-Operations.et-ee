---
title: Piiramatu võimsusega plaanimine
description: Sellest teemast leiate teavet Planning Optimization piiramatu võimsuse plaanimise kohta. See kirjeldab ka funktsiooni praeguseid piiranguid.
author: crytt
ms.date: 6/9/2021
ms.topic: article
ms.search.form: RouteInventProd
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fc40dc2bcf1969e4c566b624a9425638e69ab2a17892f035aeabb74068aadd14
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718968"
---
# <a name="scheduling-with-infinite-capacity"></a>Piiramatu võimsusega plaanimine

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

*Piiramatu võimsuse plaanimine Planning Optimization`is* funktsioon tutvustab marsruuditeabel põhinevat planeerimist. See võimaldab teil planeerida töid protsessi erinevate seadistuste põhjal. Planning Optimization planeerimine hõlmab sageli kasutatavaid protsessisätteid, sh protsessi operatsiooni järjestust või protsessi operatsiooni ressursside nõudeid.

## <a name="turn-on-the-infinite-capacity-scheduling-feature"></a>Lülitage sisse piiramatu võimsuse planeerimise funktsioon

Kui teie süsteemis ei ole veel selles teemas kirjeldatud funktsioone, avage [Funktsioonihaldus](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruum ja lülitage funktsioon *Plaanitud optimeerimine plaanitud tootetellimustele* sisse.

## <a name="added-functionality"></a>Lisatud funktsionaalsus

*Piiramatu võimsuse plaanimine Planning Optimization`is* funktsioon võimaldab marsruuditeabel põhinevat planeerimist. Seetõttu saab tootmisprotsesside plaanimiseks kasutada protsessi seadistust. Kuigi sellel funktsioonil on mõned piirangud, mis integreeritud koondplaneerimisel ei ole, toetab see tootmisstsenaariumide puhul kõige tavalisemaid funktsioone.

See funktsioon arvestab nii *lihtsaid teid* kui ka *protsessivõrke*. Kasutades protsessi operatsiooni välja **Edasi** saate seadistada keerukaid protsesse, mille alguspunktid on erinevad ja mitu paralleelsel käitatud operatsiooni. Süsteem kaalub planeerimisel seda tüüpi keerukaid protsessistruktuure.

Lisaks toetab see funktsioon *paralleeltoiminguid* protsessides. Kasutades protsessioperatsioonide prioriteediväljal *Esmased* ja *Teisesed* valikuid **Prioriteet** väljal, saate määratleda protsessi struktuuri, kus üks protsessi operatsioon on esmane operatsioon ja teine teisene. Sel juhul süsteem kaalub planeerimisel seda tüüpi keerukaid protsessistruktuure.

Planeerimisprotsessi ajal võtab süsteem arvesse ka operatsioonile määratud *ressursinõudeid*. Süsteem kasutab ressursinõudeid, et määrata, millised ressursid on toimingu sooritamiseks vajalikud. Praegu toetab *piiramatu võimsuse planeerimise Planning Optimization* funktsioon järgmist tüüpi ressursinõudeid:

- Ressursi tüüp
- Ressurss
- Ressursigrupp
- Võimalus

> [!NOTE]
> Inimressurssidega seotud nõudeid (nt oskused või tunnistuse nõuded) ei toetata veel.

See funktsioon toetab ka **seadistusaja** ja **käitusaja** töö atribuute. Kui seadistate need atribuudid protsessi operatsioonis, loob planeerimisprotsess sobivad seadistus- ja protsessitööd.

Kokkuvõttena toetab Planning Optimization planeerimine kõige sagedamini kasutatavaid stsenaariume. Saate luua protsessi, lisada esmaseid ja teisesi operatsioone, määratleda järgmiseid operatsioone, lisada ressursinõudeid ning lisada seadistusaja ja käitusaja. Süsteem võtab seda teavet planeerimisel arvesse.

## <a name="limitations"></a>Kitsendused

Kui kasutate plaanimiseks Planning Optimization`i, rakenduvad järgmised piirangud:

- See funktsioon toetab ainult tööde planeerimist. Operatsioonide planeerimisega seotud sätteid ei loeta planeerimisel, olenemata koondplaanide planeerimisviisist.
- See funktsioon toetab ainult piiramatut võimsust.
- Funktsioon ei toeta ressursi koormuse funktsioone.
- See funktsioon ei arvesta protsessi praaki.
- Funktsioon toetab *kestust* ainult esmase ressursi valikuna.

Pidage meeles, et *Piiramatu võimsuse plaanimine Planning Optimization* funktsioonis parandatakse pidevalt. Microsoft ootab tulevaste väljalasete täiendavate plaanimissätete toetamist.