---
title: Pakkumiskutset kasutava taotluse loomine
description: See juhend näitab, kuidas lisada ostutaotlusele pakkumiskutse protsessist hinda ja hankija teavet.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a9418b526f992008086f10ce78e95cb682bc164
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547395"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a>Pakkumiskutset kasutava taotluse loomine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See juhend näitab, kuidas lisada ostutaotlusele pakkumiskutse protsessist hinda ja hankija teavet. Selles juhendis olevat näidet saab kasutada demoandmete ettevõttes USMF ja kõigi etappide läbimiseks peate olema administraatorina sisse loginud. Selle juhendi ülesandeid täidavad tavaliselt hankespetsialistid.


## <a name="create-a-requisition"></a>Taotluse loomine
1. Tehke valik Hanked > Ostutaotlused > Minu ettevalmistatud ostutaotlused.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Nimi.
4. Sisestage kuupäev väljale Nõutav kuupäev.
5. Sisestage kuupäev väljale Aruandluskuupäev.
6. Klõpsake nuppu OK.
7. Valige või sisestage väärtus väljal Põhjus.
8. Klõpsake käsku Lisa rida.
9. Valige väljalt Hankekategooria puult kategooria ja klõpsake siis nuppu OK.
10. Sisestage väärtus väljale Toote nimi.
11. Sisestage arv väljale Kogus.
12. Sisestage või valige väärtus väljal Ühik.
13. Klõpsake nuppu Salvesta.
14. Klõpsake suvandit Töövoog rippdialoogi avamiseks.
15. Klõpsake Edasta.
16. Sulgege leht.
17. Klõpsake Edasta.

## <a name="reassign-a-workflow-task"></a>Töövoo ülesande ümber määramine
    * Järgmine ülesanne on luua pakkumiskutse hankijatelt tootele pakkumiste saamiseks. USMF-i demoandmetes seadistatakse taotluse töövoog reegliga, nii et kui hankijat pole valitud või kui ühiku hind on real 0, määratakse ülesanne konkreetsele töötajale, kes koostab pakkumiskutse. Selle juhendiga jätkamiseks peate määrama selle ülesande ümber teisele kasutajale (endale). Seda saate teha ainult siis, kui olete administraatorina sisse loginud.  
1. Klõpsake suvandit Töövoog rippdialoogi avamiseks.
2. Klõpsake valikut Kuva ajalugu.
3. Värskendage lehte.
4. Laiendage jaotist Jälgimise üksikasjad.
5. Valige puult rida, mis algab sõnadega Rea töövoog aktiveeritud kuupäeval.
6. Klõpsake valikut Kuva töövoo üksikasjad.
7. Laiendage jaotist Tööüksused.
8. Klõpsake käsku Määra uuesti.
9. Tehke väljal Kasutaja valik Administraator.
10. Klõpsake käsku Määra uuesti.
11. Sulgege leht.
12. Sulgege leht.

## <a name="create-an-rfq"></a>Pakkumiskutse loomine
1. Värskendage lehte.
2. Klõpsake valikut Pakkumiskutse vastus.
3. Tehke väljal Ostev juriidiline isik valik USMF.
    * Peate valima sama juriidilise isiku, kes on taotluse real.  
4. Märkige loendis valitud rida.
    * Kui ostutaotlusel oli mitu rida, valige kõik read, mida soovite pakkumiskutsesse lisada.  
5. Klõpsake nuppu OK.
6. Värskendage lehte.
7. Avage kiirinfo ja laiendage siis jaotist Seotud dokumendid.
    * Teil võib kiirinfo juba lahti olla. Otsige noolega ikooni nuppudest Read/päis paremal. Kui nool osutab paremale, on kiirinfo juba avatud. Kui nool osutab vasakule, klõpsake seda kiirinfo avamiseks.  
8. Klõpsake linki väljal Pakkumiskutse äsja loodud pakkumiskutse avamiseks.
9. Klõpsake päist.
10. Klõpsake vahekaarti Lisa.
11. Sisestage väärtus väljale Hankija konto või valige see.
12. Klõpsake vahekaarti Lisa.
13. Sisestage väärtus väljale Hankija konto või valige see.
14. Klõpsake käsku Saada.
15. Klõpsake nuppu OK.
16. Klõpsake nuppu Sisesta vastus.
17. Klõpsake toimingupaanil käsku Vasta.
18. Klõpsake käsku Kopeeri andmed vastuseväljadele.
    * Sellega kopeeritakse andmed nagu kogus ja kuupäevad pakkumiskutselt vastusele.  
19. Sisestage arv väljale Ühiku hind.
    * See on hind, mille hankijalt saite. Teil võib olla vaja sisestada ka hankijalt saadud lisateavet.  
20. Klõpsake suvandit Nõustu.
21. Klõpsake nuppu OK.

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a>Veenduge, et hankija ja hind oleksid taotlusele üle viidud
1. Sulgege leht.
2. Klõpsake valikut Read.
3. Klõpsake valikut Seostuv teave.
4. Klõpsake valikut Ostutaotlus.
5. Valige rida, mis pakkumiskutsele üle viidi.
    * Veenduge, et hind ja hankija oleksid taotlusele kopeeritud.  
6. Klõpsake suvandit Töövoog rippdialoogi avamiseks.
7. Klõpsake valikut Valmis.
8. Sulgege leht.
9. Klõpsake valikut Valmis.

