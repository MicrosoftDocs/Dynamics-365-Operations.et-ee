---
title: Põhivarade ümberklassifitseerimine
description: Põhivara ümberklassifitseerimiseks peate edastama selle uuele põhivaragrupile või määrama sellele samas grupis uue põhivara numbri.
author: saraschi2
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8935213c4629de408a48df5e54a2122324e1b3e7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823928"
---
# <a name="reclassify-fixed-assets"></a>Põhivarade ümberklassifitseerimine

[!include [banner](../../includes/banner.md)]

Põhivara ümberklassifitseerimiseks peate edastama selle uuele põhivaragrupile või määrama sellele samas grupis uue põhivara numbri. 

Kui põhivara ümber klassifitseerida:

* Uue põhivara jaoks on loodud kõik olemasoleva põhivararaamatud. Kogu algse põhivara jaoks häälestatud teave on kopeeritud uude põhivarasse. Raamatute algse põhivara olek on Suletud. 

* Uue põhivara uued raamatud sisaldavad ümberklassifitseerimise kuupäeva väljal **Soetamiskuupäev**. Kuupäev väljal **Amortiseerimise algus** on kopeeritud algsest vara puudutavast teabest. Kui kulumiarvestus on juba alanud, kuvab väli **Viimase kulumiarvestuse kuupäev** ümberklassifitseerimise kuupäeva. 

* Algse põhivara olemasolevad põhivarakanded on tühistatud ja uue põhivara jaoks uuesti loodud.

Põhivara ümberklassifitseerimiseks toimige järgmiselt.

1. Avage **Põhivarad > Perioodilised ülesanded > Ümberklassifitseerimine.**
2. Väljal **Põhivaragrupp** valige ümberklassifitseerimiseks grupp.
3. Väljal **Põhivara kood** valige ümberklassifitseerimiseks põhivara.
4. Valige väljal **Uus põhivaragrupp** see grupp, millele soovite põhivara üle kanda.
    * Kui uus põhivaragrupp on seotud numbriseeriaga, värskendatakse välja **Uue põhivara kood** numbriga uuest põhivaragrupi numbriseeriast. Vastasel juhul värskendatakse välja **Uue põhivara kood** numbriga numbriseeriast, mis häälestatakse lehel **Põhivara parameetrid**. Kui numbriseeriat ei häälestata leheküljel **Põhivara parameetrid**, sisestage number väljale **Uus põhivara kood**.  
5. Sisestage kuupäev väljale **Ümberklassifitseerimise kuupäev**.
6. Sisestage või valige väärtus väljal **Kande seeria**.
7. Klõpsake valikut **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]