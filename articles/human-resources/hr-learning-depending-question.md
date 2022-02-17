---
title: Eelmise küsimuse vastusest sõltuva küsimuse koostamine
description: Tingimuslike küsimuste abil saate määrata, milliseid järelküsimusi vastajale eelmise küsimuse vastuse põhjal esitatakse.
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f28f75a902121f23c92a919b539517dbdb191447
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066721"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a>Eelmise küsimuse vastusest sõltuva küsimuse koostamine


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Tingimuslike küsimuste abil saate määrata, milliseid järelküsimusi vastajale eelmise küsimuse vastuse põhjal esitatakse. Näiteks kui küsite Kas eelistate kohvi või teed?, saab loogilise järelküsimuse määrata olenevalt sellest, kas vastaja valib vastuseks kohvi või tee. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="find-the-existing-questionnaire"></a>Olemasoleva küsimustiku leidmine
1. Minema **Küsimustik** > **Disain** > **Küsimustikud**.
2. Valige loendist küsimustik WorkFH.

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a>Kõikide küsimuste ja alamküsimuste lisamine küsimustikku
1. Klõpsake **Küsimused**.
2. Klõpsake valikut **Uus**.
3. Aastal **küsimus** väljal valige küsimuse number 00016.
4. Otsige loendist ja valige soovitud kirje.
5. Klõpsake loendis valitud real olevat linki.
6. Klõpsake nuppu **Salvesta**.
7. Sulgege leht.

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a>Küsimustiku järjestuse määramine tingimuslikuks ja küsimuse muutmine asjakohasest küsimusest sõltuvaks
1. Klõpsake valikut **Redigeeri**.
2. Laiendage jaotist **Seadistus**.
3. Aastal **Küsimuste järjekord** valige "Tingimuslik".
4. Klõpsake **Tingimuslik** küsimus.
5. Valige puult suvand Küsimused\selgitage, miks vastasite eelmisele küsimusele selliselt?.
6. Aastal **Esmane küsimus** väljal valige küsimus 00009.
7. Klõpsake loendis valitud real olevat linki.
8. Aastal **Vastus** väljale sisestage selle vastusevariandi ID, millest soovite küsimuse sõltuvaks muuta. Näiteks sisestage esimese vastuse suvandi puhul 1.
9. Klõpsake nuppu **Salvesta**.
10. Valige puul suvand Küsimused\mulle makstakse tehtava töö eest õiglast tasu.
    * Pange tähele, et küsimuse puud värskendatakse sõltuvuse näitamiseks.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
