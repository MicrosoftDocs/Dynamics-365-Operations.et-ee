---
title: Küsimustike levitamine ajastamise abil
description: Küsimustiku planeerimine võimaldab plaanida ja jaotada küsimustikke mitmele vastajale.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 952048ce0a2ac94be70d7bde0dc52610f19151ed
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056296"
---
# <a name="distribute-questionnaires-using-scheduling"></a>Küsimustike levitamine ajastamise abil

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Küsimustiku planeerimine võimaldab plaanida ja jaotada küsimustikke mitmele vastajale. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.

## <a name="create-a-questionnaire-schedule"></a>Küsimustiku graafiku loomine

1. Tehke valik Küsimustik > Jaota > Küsimustiku graafikud.

2. Klõpsake valikut Uus.

3. Sisestage väärtus väljale Plaanimine.

4. Sisestage väljale Kirjeldus soovitud väärtus.
    * Määrake graafik olekusse Anonüümne, kui soovite vastused salvestada kujul, kus vastustega ei ole seotud nimesid.  
    * Anonüümsete tulemuste lubamine tuleb esmalt inimressursside parameetrites seadistada.  

5. Valige väljalt Tüüp plaanimise tüüp.  Selles näites kasutame tüüpi Rahulolu.

6. Otsige loendist ja valige soovitud kirje.

7. Klõpsake loendis valitud real olevat linki.

8. Sisestage kuupäev väljale Kuupäev.

9. Laiendage jaotist Töötaja iseteeninduse meil.

10. Sisestage väärtus väljale Teema.

    * Näide: küsimustik on saadaval  

11. Tippige väljale Tekst meilisõnumi sisu. Pange tähele, et süsteemis saab kasutada väärtuste asendamiseks muutujat.

    * Näide: Lugupeetud %P%! Töötajate tervise küsitluse täitmiseks palun logige sisse töötaja iseteenindusse.  Contoso  

12. Klõpsake nuppu Salvesta.

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a>Kasutage seadistuse üksikasju vastamiseks küsimustik(e) valimiseks ja päringuid vastajate valimiseks.

1. Klõpsake valikut Seadistuse üksikasjad.

2. Valige loendist päring, mille abil süsteemist küsimustikule vastajaid leida.

    * Näide: töötajad  

3. Klõpsake valikut Kuva või muuda päringut, et kindlaid inimesi valida, või kohandage päringut inimeste leidmiseks, kes vastavad teatud kriteeriumidele.

    * Pange tähele, et kõik vastajad peavad olema süsteemi kasutajad.  

4. Märkige loendis rida nimega Person

5. Sisestage või valige väärtus väljal Kriteeriumid.

    * Valige Julia Funderburk  

6. Valige loendist Julia Funderburk

7. Klõpsake nuppu OK.

8. Klõpsake vahekaarti Küsimustikud.

9. Laiendage puul valikut „sõlm küsimustiku tüübi Rahuoluküsitlus kohta”.

10. Märkige puul valik Töötajate tervise hindamine.

11. Klõpsake nuppu OK.

12. Klõpsake valikut Planeeritud vastamisseanss.

    * Pange tähele, et Planeeritud vastamisseansid on loodud iga valitud/päringuga leitud kasutaja jaoks.  

13. Sulgege leht.

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a>Küsimustiku graafiku käivitamine küsimustiku vastajatele kättesaadavaks muutmiseks.

1. Klõpsake suvandit Funktsioonid.

2. Klõpsake nuppu Käivita.

3. Klõpsake nuppu OK.

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a>Meili saatmine vastajate teavitamiseks saadaolevast küsimustikust.

1. Klõpsake suvandit Funktsioonid.

2. Klõpsake valikut Saada meil.

3. Klõpsake valikut Tühista.

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a>Kasutage Valikut Planeeritud vastamisseansid, et jälgida, kes peab küsimustiku täitma.

1. Klõpsake valikut Planeeritud vastamisseanss.

    * Kustutage kõik ülejäänud planeeritud vastamisseansid, kui olete valmis planeeritud seansi lõpetamiseks.  

2. Klõpsake  Kustuta.

3. Klõpsake nuppu Jah.

4. Sulgege leht.

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a>Lõpetage graafik, kui kõik vastajad on küsimustiku täitnud ja/või kõik järelejäänud plaanitud vastuseseansid on kustutatud.

1. Klõpsake suvandit Funktsioonid.
2. Klõpsake suvandit Lõpeta.
3. Klõpsake nuppu OK.



[!INCLUDE[footer-include](../includes/footer-banner.md)]