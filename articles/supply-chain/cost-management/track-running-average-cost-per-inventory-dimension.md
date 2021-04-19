---
title: Jooksvate keskmiste kulude jälgimine varude dimensiooni alusel
description: Igale laokaubale on lisatud varude dimensioonigrupp. Seetõttu arvutatakse kauba jooksev keskmine omahind finantsiliselt jälgitavate varude dimensioonide valiku põhjal.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8da13a01b28ca09ce9c29ecd3a9342dfb9eaa4bd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834309"
---
# <a name="track-running-average-cost-per-inventory-dimension"></a>Jooksvate keskmiste kulude jälgimine varude dimensiooni alusel

[!include [banner](../includes/banner.md)]

Igale laokaubale on lisatud varude dimensioonigrupp. Seetõttu arvutatakse kauba jooksev keskmine omahind finantsiliselt jälgitavate varude dimensioonide valiku põhjal.

Varude dimensioone on kolm tüüpi: toote-, laoala ja jälgimisdimensioon. Tootedimensioonid hõlmavad konfiguratsiooni, suurust ja värvi. Tootedimensioone jälgitakse alati finantsiliselt. Laoala ja jälgimisdimensioonid hõlmavad tegevuskohta, ladu, asukohta, varude olekut, litsentsiplaati, partii numbrit ja seerianumbrit. Saate määrata, milliseid laoala ja jälgimisdimensioone finantsiliselt jälgitakse. 

**1. näide** 

Kui kaubaga seotud laoala dimensioonigruppi jälgitakse finantsiliselt lao järgi, arvutatakse jooksev keskmine omahind iga lao kohta. Arveldatud on järgmised ostutellimused:

-   Ostutellimus kogusele 2 omahinnaga 10,00 USA dollarit on arveldatud laole GW.
-   Ostutellimus kogusele 3 omahinnaga 12,00 USA dollarit on arveldatud laole GW.
-   Ostutellimus kogusele 5 omahinnaga 15,00 USA dollarit on arveldatud laole MW.

Jooksev keskmine omahind lao GW puhul on 11,20 USA dollarit ja jooksev keskmine omahind lao MW puhul on 15,00 USA dollarit. Müügitellimuse arve sisestatakse laole GW. Varude väärtus ja tuletusreegel (enne lao sulgemise käitamist ja ilma märgistuseta) on 11,20 USA dollarit. Teine müügitellimus sisestatakse laole MW. Varude väärtus ja tuletusreegel (enne lao sulgemise käitamist ja ilma märgistuseta) on 15,00 USA dollarit. 

**2. näide.** Kui kaubaga seotud laoala dimensioonigruppi jälgitakse finantsiliselt lao järgi ja jälgimisdimensioonigruppi jälgitakse finantsiliselt partiinumbri järgi, arvutatakse jooksev keskmine omahind iga partii kohta. 

**Märkus.** Soovitame alati vaadata kõigi jälgitavate finantsdimensioonide omahinda. Arveldatud on järgmised ostutellimused:

-   Ostutellimus kogusele 2 omahinnaga 10,00 USA dollarit on arveldatud laole GW ja partiile AAA.
-   Ostutellimus kogusele 3 omahinnaga 12,00 USA dollarit on arveldatud laole GW ja partiile AAA.
-   Ostutellimus kogusele 2 omahinnaga 15,00 USA dollarit on arveldatud laole GW ja partiile BBB.

Jooksev keskmine omahind lao GW ja partii AAA puhul on 11,20 USA dollarit ning jooksev keskmine omahind lao MW ja partii BBB puhul on 15,00 USA dollarit.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]