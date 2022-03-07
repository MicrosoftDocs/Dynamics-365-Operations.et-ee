---
title: Imporditud ostutellimuste reanumbrid on valed
description: Kui ostutellimused imporditakse andmehalduse kaudu, ei järgita ostutellimuse reanumbrite puhul süsteemiparameetrites määratletud sammu
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: e1cf5cf1d04824213f495ac3ebf556796c96611a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476075"
---
# <a name="imported-purchase-orders-show-incorrect-line-numbers"></a>Imporditud ostutellimuste reanumbrid on valed

## <a name="symptoms"></a>Sümptomid

Vaikimisi ei kasutata andmeüksuse *Ostutellimuse read V2* kaudu imporditud ostutellimuse ridade jaoks automaatselt loodud reanumbrite puhul süsteemiparameetrites määratud süsteemi reanumbri sammu. Kui loote ostutellimuse käsitsi ja lisate ridu kasutajaliidese kaudu (UI), siis on reanumbrite samm õige. Kuid kui kasutate andmehaldusraamistikku (DMF), ei ole nende samm õige.

See probleem ilmneb seetõttu, et kui impordite ridu DMF-i kaudu ja reanumbrid ei ole imporditud üksuses juba määratud, kasutab süsteem nende määramiseks DMF-i meetodit. See meetod suurendab reanumbreid alati ühe võrra.

## <a name="workaround"></a>Vastukaal

Veenduge, et soovitud reanumbrid oleksid ostutellimuse ridade importimisel andmeüksuse reanumbrite väljades juba olemas. Sel juhul ei kirjuta DMF reanumbreid üle.
