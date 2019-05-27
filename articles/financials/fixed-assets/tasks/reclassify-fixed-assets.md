---
title: Põhivarade ümberklassifitseerimine
description: Põhivara ümberklassifitseerimiseks peate edastama selle uuele põhivaragrupile või määrama sellele samas grupis uue põhivara numbri.
author: saraschi2
manager: AnnBe
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df4a2fa3c1a38519da83391bcf1c4aa38b6504ff
ms.sourcegitcommit: 6890b5a372a18e11354003098a512685e339ddb0
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/14/2019
ms.locfileid: "1541193"
---
# <a name="reclassify-fixed-assets"></a>Põhivarade ümberklassifitseerimine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Põhivara ümberklassifitseerimiseks peate edastama selle uuele põhivaragrupile või määrama sellele samas grupis uue põhivara numbri. 

Kui põhivara ümber klassifitseerida:

• Uue põhivara jaoks on loodud kõik olemasoleva põhivararaamatud. Kogu algse põhivara jaoks häälestatud teave on kopeeritud uude põhivarasse. Raamatute algse põhivara olek on Suletud. 

• Uue põhivara uued raamatud sisaldavad ümberklassifitseerimise kuupäeva väljal **Soetamiskuupäev**. Kuupäev väljal **Amortiseerimise algus** on kopeeritud algsest vara puudutavast teabest. Kui kulumiarvestus on juba alanud, kuvab väli **Viimase kulumiarvestuse kuupäev** ümberklassifitseerimise kuupäeva. 

• Algse põhivara olemasolevad põhivarakanded on tühistatud ja uue põhivara jaoks uuesti loodud.

Põhivara ümberklassifitseerimiseks toimige järgmiselt.

1. Avage **Põhivarad > Perioodilised ülesanded > Ümberklassifitseerimine.**
2. Väljal **Põhivaragrupp** valige ümberklassifitseerimiseks grupp.
3. Väljal **Põhivara kood** valige ümberklassifitseerimiseks põhivara.
4. Valige väljal **Uus põhivaragrupp** see grupp, millele soovite põhivara üle kanda.
    * Kui uus põhivaragrupp on seotud numbriseeriaga, värskendatakse välja **Uue põhivara kood** numbriga uuest põhivaragrupi numbriseeriast. Vastasel juhul värskendatakse välja **Uue põhivara kood** numbriga numbriseeriast, mis häälestatakse lehel **Põhivara parameetrid**. Kui numbriseeriat ei häälestata leheküljel **Põhivara parameetrid**, sisestage number väljale **Uus põhivara kood**.  
5. Sisestage kuupäev väljale **Ümberklassifitseerimise kuupäev**.
6. Sisestage või valige väärtus väljal **Kande seeria**.
7. Klõpsake valikut **OK**.
