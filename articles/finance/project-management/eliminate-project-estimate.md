---
title: Projektihinnangu eemaldamine
description: See teema annab teavet projektihinnangu eemaldamise kohta pärast selle lõpule viimist.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: eb323bdeb2a4701cdc9383b8da29e05a4cab107c
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410210"
---
# <a name="eliminate-a-project-estimate"></a>Projektihinnangu eemaldamine

[!include [banner](../includes/banner.md)]

Projektihinnangud võimaldavad kuvada projekti jaoks hinnanguliselt vaja mineva ja plaanitud töö finantsandmeid. Projektihinnangutega töötamiseks tuleb projekt siduda hinnanguprojektiga. Hinnanguprojekt põhineb alati mõnel olemasoleval projektil, kuid ühele hinnanguprojektile võib viidata mitu projekti. Hinnanguprojektidele saab lisada ainult fikseeritud hinnaga ja investeerimisprojekte ning need projektid peavad kuuluma hinnanguprojektiga samasse projektigruppi.

Hinnanguprojekti eemaldamiseks peab see olema lõpule viidud. Järgmistes etappides on kirjeldatud, kuidas hinnangut eemaldada.

1. Avage **Projektihaldus ja raamatupidamine** > **Kõik projektid** ning avage projekt. 
2. Valige vahekaardil **Haldamine** suvand **Hinnangud** ning valige lehel **Hinnangud** suvand **Eemaldamine**.
3. Seadke lehel **Hinnangu eemaldamine**, mis asub vahekaardil **Üldine**, järgmised väärtused.

   - **Perioodi kood**: valige perioodi kood vajalike hinnanguprojektide valimiseks. 
   - **Hinnangu kuupäev:** valige eemaldamiseks sobiv hinnangu kuupäev.
   - **Eemalda WIP-hoiatustega**: lubage see suvand teatise saamiseks, kui poolelioleva (WIP) üksusega seotud hinnang eemaldatakse. Kui see suvand ei ole lubatud, ei saa eemaldamine mittehinnatud kannete olemasolu korral jätkuda. 
   > [!NOTE]
   > See suvand on saadaval vaid siis, kui eemaldamistoimingut rakendatakse hinnanguprojekti puhul. See ei ole saadaval, kui kasutate perioodilisi sisestusi. See säte toimib sätetega, mis asuvad lehe **Projekti parameetrid** vahekaardil **Hinnang** väljagrupis **Luba eemaldamine mittehinnatud kannete olemasolu korral**.
   - **Märgi etapp lõpetatuks**: lubage see suvand, et seada hinnanguprojekti etapp pärast eemaldamise käitamist olekusse **Lõpetatud**.
   - **Prindi hinnanguloend**: valige hinnanguloendi printimisel kaasatav teave.
   - **Kuva teabelogi**: lubage see suvand teabelogi kuvamiseks.
   - **Sisestuskuupäev**: valige hinnangu pearaamatusse sisestamise kuupäev

4.  Valige nupp **OK**.
5. Kui eemaldamisprotsess on lõpetatud, kuvatakse eemaldatud hinnanguprojekt negatiivse väärtusega. 

Kui te ei plaaninud hinnangut eemaldada, saate valida eemaldatud hinnangu ja klõpsata suvandit **Tühista eemaldamine**.   
