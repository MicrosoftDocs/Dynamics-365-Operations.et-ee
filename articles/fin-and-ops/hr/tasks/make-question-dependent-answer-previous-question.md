--- 
title: "Eelmise küsimuse vastusest sõltuvate küsimuste koostamine"
description: "Tingimuslike küsimuste abil saate määrata, milliseid järelküsimusi vastajale eelmise küsimuse vastuse põhjal esitatakse."
author: ShylaThompson
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 3e0a6d63a266bf49764c8cdcfd407ff0733ea27c
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---
# <a name="make-questions-dependent-on-the-answer-of-the-previous-question"></a>Eelmise küsimuse vastusest sõltuvate küsimuste koostamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tingimuslike küsimuste abil saate määrata, milliseid järelküsimusi vastajale eelmise küsimuse vastuse põhjal esitatakse. Näiteks kui küsite Kas eelistate kohvi või teed?, saab loogilise järelküsimuse määrata olenevalt sellest, kas vastaja valib vastuseks kohvi või tee. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="find-the-existing-questionnaire"></a>Olemasoleva küsimustiku leidmine
1. Avage Küsimustik > Kujundus > Küsimustikud.
2. Valige loendist küsimustik WorkFH.

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a>Kõikide küsimuste ja alamküsimuste lisamine küsimustikku
1. Klõpsake suvandit Küsimused.
2. Klõpsake valikut Uus.
3. Valige küsimus number 00016 väljalt Küsimus.
4. Otsige loendist ja valige soovitud kirje.
5. Klõpsake loendis valitud real olevat linki.
6. Klõpsake nuppu Salvesta.
7. Sulgege leht.

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a>Küsimustiku järjestuse määramine tingimuslikuks ja küsimuse muutmine asjakohasest küsimusest sõltuvaks
1. Klõpsake nuppu Redigeeri.
2. Laiendage jaotist Seadistus.
3. Valige väljalt Küsimuste järjekord suvand Tingimuslik.
4. Klõpsake suvandit Tinglik küsimus.
5. Valige puult suvand Küsimused\selgitage, miks vastasite eelmisele küsimusele selliselt?.
6. Valige küsimus 00009 väljalt Esmane küsimus.
7. Klõpsake loendis valitud real olevat linki.
8. Sisestage väljale Vastus see vastuse suvandi vastuse seeria ID, millest soovite küsimuse sõltuvaks teha. Näiteks sisestage esimese vastuse suvandi puhul 1.
9. Klõpsake nuppu Salvesta.
10. Valige puul suvand Küsimused\mulle makstakse tehtava töö eest õiglast tasu.
    * Pange tähele, et küsimuse puud värskendatakse sõltuvuse näitamiseks.  


