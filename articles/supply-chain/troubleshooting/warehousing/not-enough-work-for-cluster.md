---
title: Pärast profiili konfigureerimist klastri jaoks ei leitud piisavalt tööd
description: Kui konfigureerite kogumiprofiili, võidakse kuvada tõrketeade, mis ütleb, et ei leidu piisavalt tööd. Redigeerige profiil ja seadke aktiveeri ametikohtade väärtuseks Ei.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 139fd72e571c8ef83af2fd0e497cf334b6ef0ea4
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476086"
---
# <a name="not-enough-work-found-for-cluster-when-using-system-directed-cluster-picking"></a>Kogumi jaoks ei leidu piisavalt tööd, kui kasutatakse süsteemi suunatud kogumi komplekteerimist

## <a name="symptoms"></a>Sümptomid

Kui kasutate *Süsteemi suunatud kogumi komplekteerimise* protsessi, kui konfigureerite kogumi profiili, kus näiteks 10 positsiooni saab komplekteerida, toimib protsess plaanipäraselt, kui on piisavalt tööd, et komplekteerida 10 positsiooni. Kuid kui valida, on ainult kaheksa ametikohta, kuvatakse järgmine tõrketeade:

> Kogumi jaoks ei leitud piisavalt tööd.

## <a name="resolution"></a>Lahendus

Probleemi lahendamiseks redigeerige kogumi profiili ja seadke suvandi **Aktiveeri positsioone** väärtuseks *Ei*.
