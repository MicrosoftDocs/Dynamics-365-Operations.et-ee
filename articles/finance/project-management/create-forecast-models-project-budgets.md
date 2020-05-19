---
title: Eelarvemudelite loomine projektieelarvete jaoks
description: Selles teemas kirjeldatakse, kuidas luua ülejäänud eelarvete kohta eelarvemudel.
author: RadhikaRS
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 07e540f23a668b40a54906a67d87552fe991825a
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321775"
---
# <a name="create-forecast-models-for-project-budgets"></a>Eelarvemudelite loomine projektieelarvete jaoks 

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas luua ülejäänud eelarvete kohta eelarvemudel. Projekt, millele rakendub eelarve juhtimine, kasutab kahte tüüpi eelarveid: algne ja ülejäänud. Projekti eelarve loomisel peate määrama algse ja ülejäänud eelarvemudelid, mis on loodud lehel **Eelarvemudelid** . Määratud mudelitel põhinevad projektieelarved luuakse projekti eelarve kooskõlastamisel.

> [!NOTE]
> Eelarvemudelil, mida kasutatakse eelarve juhtimiseks, ei saa olla alammudelit ja seda ei saa kasutada alammudelina.

1. Valige **Projektihaldus ja -arvestus** > **Seadistamine** > **Eelarved**  > **Eelarvemudelid**.
2. Uue eelarvemudeli loomiseks valige **Uus** ja sisestage seejärel uue mudeli ID-kood ja selle nimi. 
3. Seadke suvandi **Peatatud** väärtuseks **Jah**, et vältida eelarvemudeli eelarveridade muutusi. 
4. Kui eelarveread, millega mudel on seostatud, peaks moodustama pearaamatusse likviidsuse planeerimisi, seadke suvandi **Eelarvete kaasamine likviidsuse planeerimisse** väärtuseks **Jah**. 
5. Kui soovite kasutada arve kuupäevana projekti kuupäeva, siis seadke suvandi **Eelarve arve kuupäev** väärtuseks **Jah**. 
6. Väljal **Eelarve tüüp** valige üks järgmistest mudelitüüpidest.

   - **Algne eelarve**: kasutage algsete eelarvesummade jaoks, mis kooskõlastatakse esialgse eelarve loomisel ja kinnitamisel.
   - **Ülejäänud eelarve**: kasutage ülejäänud eelarvesummadega projekti eluea kestel. Selle eelarvemudeli saldosid vähendavad tegelikud kanded ja suurendavad või vähendavad eelarve revisjonid.
   - **Ülekantav**: kasutage projekti ülekantava eelarve summade puhul. Ülekandmine on valikuline protsess, mida saab käivitada üle kandma kasutamata eelarvesummasid ühest finantsaastast teise.

7. Seadke järgmised suvandid vastavalt vajadusele.

   - Kui soovite kasutada arve kuupäevana projekti kuupäeva, siis lubage **Eelarve arve kuupäev**.
   - Lubage poolelioleval tööl (WIP) põhineva eelarve jaoks **WIP-ga eelarve** ja seejärel valige WIP-i tüüp. 
   - Suvandi **Eelarve tüüp** vaikesätteks saate jätta **Puudub** või sisestada uue tüübi. Pärast kirje muutmist ei saa eelarve tüüpi muuta.     
    > [!NOTE]
    > Kui muudate eelarve tüübi vaikesätet, siis muutuvad kõik muud suvandid uuendustele suletuks ja te ei saa seda eelarvemudelit uuesti kasutada. 
   


 

