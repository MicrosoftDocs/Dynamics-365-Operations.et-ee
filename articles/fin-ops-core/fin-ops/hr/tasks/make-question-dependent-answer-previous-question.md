---
title: Eelmise küsimuse vastusest sõltuva küsimuse koostamine
description: Tingimuslike küsimuste abil saate määrata, milliseid järelküsimusi vastajale eelmise küsimuse vastuse põhjal esitatakse.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e49ee4dd1f2d4a5af3112d27eaf8d697904d2487
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177447"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a>Eelmise küsimuse vastusest sõltuva küsimuse koostamine

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

