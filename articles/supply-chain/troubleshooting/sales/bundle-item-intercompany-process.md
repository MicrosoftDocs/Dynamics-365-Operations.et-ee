---
title: Kogumiüksust ei toetata ettevõtetevahelises protsessis
description: Kogumi kaup ei ole ostuks saadaval. Müügitellimus ostab ainult kogumi kauba komponente, mitte kogumisse seotud kaupa ennast.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 21adc7d071837b762157364f6f8ed370c69c7fd3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476122"
---
# <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>Kontsernisiseses protsessis ei toetata kogumiüksust

## <a name="symptoms"></a>Sümptomid

Kogumiüksus pole ostutellimuse jaoks saadaval, sest kogumiüksuse müügitellimuse ridu uurides võib märgata, et kogus on *0* (null) ja olek on *Tühistatud*.

## <a name="resolution"></a>Lahendus

Selline käitumine on nii kavandatud. Müügitellimus ostab ainult kogumiüksuse komponente. See ei osta kogumiüksust ennast. Kui peate kogumi ostma, kaaluge, kas peate selle märkima kogumiüksusena, kuna see funktsioon on mõeldud tulu tuvastamise stsenaariumide jaoks. Lisateavet kogumiüksuste kohta leiate teemast [Kogumid](/dynamics365/finance/accounts-receivable/revenue-recognition-setup).
