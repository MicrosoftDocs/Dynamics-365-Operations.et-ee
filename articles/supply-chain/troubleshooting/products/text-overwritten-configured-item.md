---
title: Tekst kirjutatakse üle, kui kaup konfigureeritakse müügitellimuse real
description: Kui toode konfigureeritakse müügitellimuse real, kirjutatakse muudetud tekst üle standardtekstiga. Muutke teksti pärast rea konfigureerimist, mitte enne.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 20239b9b0eecb355274e909a8b8b39450e468c7e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476074"
---
# <a name="item-text-is-overwritten-when-a-product-is-configured-on-a-sales-order-line"></a>Kauba tekst kirjutatakse üle, kui toode konfigureeritakse müügitellimuse real

## <a name="symptoms"></a>Sümptomid

See probleem ilmneb, kui loote müügitellimuse rea seadistatavale kaubale ja seejärel muudate kauba teksti. Kui konfigureerite kauba ja seejärel valite **OK**, kirjutatakse tekst üle standardse tekstiga.

## <a name="resolution"></a>Lahendus

Selline käitumine on oodatud. Tekstiväli sisaldab variandi nime, mis on täidetud ainult pärast rea konfigureerimist. Seetõttu peate muutma teksti pärast rea konfigureerimist, mitte varem.
