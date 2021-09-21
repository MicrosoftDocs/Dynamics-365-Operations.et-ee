---
title: Koosluse ja protsessikoodide aktiivset versiooni ei saa sisestada
description: Teil ei paluta sisestada koosluse ja protsessi numbreid, kui valitud toote jaoks on vaikimisi sait ja ladu määratud.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 241618d70f01c85df946a48493f5d84e0964218e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476073"
---
# <a name="cant-insert-bill-of-material-and-route-when-creating-a-new-production-order"></a>Uue tootmistellimuse loomisel ei saa sisestada materjali arvet ja marsruuti

## <a name="symptoms"></a>Sümptomid

Kui loote uue tootmistellimuse, seadistatakse pärast kaubakoodi sisestamist **Saidi** ja **Lao** väljad automaatselt vaikimisi saidi ja lao jaoks, mis on määratud lõpetatud tooteüksusele **Vaikimisi tellimuse sätete** lehel. Lisaks sisestatakse automaatselt aktiivne koosluse number ja protsessi kood, nii et te ei saa järgmist teadet, mis teid nende väärtuste kohta küsib:

> Kas sisestada koosluse ja protsessi jaoks aktiivne versioon?

## <a name="resolution"></a>Lahendus

Teil ei paluta sisestada koosluse ja protsessi numbreid, kui valite toote, mille sait ja ladu on **Vaikimisi tellimuse sätete** lehel määratud. Teilt küsitakse ainult juhul, kui need väärtused pole valitud toote puhul määratletud.
