---
title: Sisestamine tuletatud raamatute kaudu
description: Selles artiklis kirjeldatakse tuletatud raamatute kasutamist.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6556965a1356522de5f4c17ddeab378a128fbe3f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833014"
---
# <a name="post-with-derived-books"></a>Sisestamine tuletatud raamatute kaudu

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse tuletatud raamatute kasutamist.

Kui sisestate tuletatud raamatuid sisaldava raamatu kandeid, sisestatakse tuletatud raamatu kanded töölehtedele, ostutellimustele või vabas vormis arvetele automaatselt. Kui aga valmistate põhivara töölehele sisestamiseks ette esmase raamatu kandeid, saate enne sisestamist vaadata ja muuta ka tuletatud kannete summasid.
-   Kindlaid kontosid, nagu käibemaksu- või kliendi- ja hankijakontod, värskendatakse esmase raamatu sisestamisel vaid üks kord. Tuletatud raamatu kanded sisestatakse neile kontodele, mis on lehel Põhivara sisestusreeglid tuletatud raamatu jaoks määratletud.
-   Tuletatud raamatute puhul on kande tüüp sageli Soetamine. Kasutage seda varianti, kui see raamat ja tuletatud raamat määratakse põhivarale alates selle soetusest.
-   Kande tüüp võib olla ka muu väärtusega. Näiteks kui esmasel raamatul ja tuletatud raamatul on samad müügi- ja likvideerimisintervallid, saab tuletatud raamatu seadistamisel kasutada kõiki põhivara kandetüüpe.

> [!WARNING]
> Tuletatud raamatusse sisestatava kulumi summa on sama, mis sisestati esmase raamatu puhul. Kui raamatute puhul kasutatakse erinevaid kulumiarvestuse meetodeid, ei tohi kulumikandeid tuletatud protsessi abil luua. |

## <a name="example"></a>Näide 
Järgmine teave kirjeldab, kuidas seadistada tuletatud raamatu funktsiooni abil soetamiskandeid.

1.  Looge raamatud lehel Raamatud.
    -   Raamatupidamise raamat: VM 1, praegune sisestuskiht
    -   Maksu raamat: VM 2, maksu sisestuskiht

2.  Klõpsake jaotises VM 1 vahekaarti Tuletatud raamatud. Valige väljal Raamat suvand VM 2 ja väljal Kande tüüp suvand Soetamine.

Seejärel saab raamatud kindlate põhivaradega siduda. 

Raamatuga VM 1 põhivara soetamise sisestamisel sisestatakse see mitte ainult raamatusse VM 1, vaid ka tuletatud raamatusse VM 2. Mõlema põhivara raamatu olekuks muutub Avatud.

> [!NOTE]                                                                                                         
> Kui te tuletatud raamatuid ei kasuta, tuleb teil soetamine sisestada nii raamatu VM 1 kui raamatu VM 2 kohta.

Lisateavet vt teemast [Tuletatud raamatud](derived-books.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]