---
title: Pakkumiskutset kasutava taotluse loomine
description: Selles teemas selgitatakse, kuidas lisada hinda ja hankija teavet pakkumiskutselt ostutaotlusele.
author: GalynaFedorova
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 78092205c1a1d149b4dc202e085871d1fe46c4ad
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675117"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a>Pakkumiskutset kasutava taotluse loomine

[!include [banner](../../includes/banner.md)]

Selles teemas selgitatakse, kuidas lisada hinda ja hankija teavet pakkumiskutselt ostutaotlusele. Selles juhendis olevat näidet saab kasutada demoandmete ettevõttes USMF ja kõigi etappide läbimiseks peate olema administraatorina sisse loginud. Selle juhendi ülesandeid täidavad tavaliselt hankespetsialistid.


## <a name="create-a-requisition"></a>Taotluse loomine
1. Navigeerimispaanil avage **Moodulid > Hanked > Ostutaotlused > Minu ettevalmistatud ostutaotlused**.
2. Valige suvand **Uus**.
3. Sisestage väärtus väljale **Nimi**.
4. **Sisestage kuupäev väljale Nõutav kuupäev.**
5. Sisestage kuupäev väljale **Aruandluskuupäev.**
6. Valige nupp **OK**.
7. Väljale **Põhjus** sisestage või valige väärtus.
8. Valige **Lisa rida**.
9. Väljal **Hankekategooria** valige puust kategooria ja seejärel valige **OK**.
10. Sisestage väärtus väljale **Toote nimi**.
11. Sisestage arv väljale **Kogus**.
12. Sisestage või valige väärtus väljal **Ühik**.
13. Valige käsk **Salvesta**.
14. Rippdialoogi avamiseks klõpsake valikut **Uus**.
15. Valige käsk **Esita**.
16. Sulgege leht.
17. Valige käsk **Esita**.

## <a name="reassign-a-workflow-task"></a>Töövoo ülesande ümber määramine
Järgmine ülesanne on luua pakkumiskutse hankijatelt tootele pakkumiste saamiseks. USMF-i demoandmetes seadistatakse taotluse töövoog reegliga, nii et kui hankijat pole valitud või kui ühiku hind on real 0, määratakse ülesanne konkreetsele töötajale, kes koostab pakkumiskutse. Selle juhendiga jätkamiseks peate määrama selle ülesande ümber teisele kasutajale (endale). Seda saate teha ainult siis, kui olete administraatorina sisse loginud.  

1. Rippdialoogi avamiseks klõpsake valikut **Uus**.
2. Valige **Kuva ajalugu**.
3. Värskendage lehte.
4. Laiendage jaotist **Jälgimise üksikasjad**.
5. Valige puust rida, mille alguseks on „Rea töövoog aktiveeritud”.
6. Valige **Kuva töövoo üksikasjad**.
7. Laiendage jaotist **Tööüksused**.
8. Valige käsk **Määra ümber**.
9. Väljal **Kasutaja** valige **Administraator**.
10. Valige käsk **Määra ümber**.
11. Sulgege kaks lehte.

## <a name="create-an-rfq"></a>Pakkumiskutse loomine

1. Värskendage lehte.
2. Valige **Pakkumiskutse**.
3. Väljal **Ostev juriidiline isik** valige **USMF**. Peate valima sama juriidilise isiku, kes on taotluse real.  
4. Märkige loendis valitud rida. Kui ostutaotlusel oli mitu rida, valige kõik read, mida soovite pakkumiskutsesse lisada.  
5. Valige nupp **OK**.
6. Värskendage lehte.
7. Veenduge, et kiirinfo on avatud, seejärel laiendage jaotist **Seotud dokumendid**.
8. Valige link väljal **Pakkumiskutse**, et avada äsja loodud pakkumiskutse.
9. Valige **Päis**.
10. Valige **Lisa**.
11. Sisestage või valige väärtus väljale **Hankija konto**.
12. Valige **Lisa**.
13. Sisestage või valige väärtus väljale **Hankija konto**.
14. Valige **Saada**.
15. Valige nupp **OK**.
16. Valige **Sisesta vastus**.
17. Toimingupaanil valige käsk **Vasta**.
18. Valige **Kopeeri andmed vastuseväljadele**. Sellega kopeeritakse andmed nagu kogus ja kuupäevad pakkumiskutselt vastusele.  
19. Sisestage arv väljale **Ühiku hind**. See on hind, mille hankijalt saite. Teil võib olla vaja sisestada ka hankijalt saadud lisateavet.  
20. Valige **Aktsepteerimine**.
21. Valige nupp **OK**.

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a>Veenduge, et hankija ja hind oleksid taotlusele üle viidud
1. Sulgege leht.
2. Valige **Read**.
3. Valige **Seotud teave**.
4. Valige **Ostutaotlus**.
5. Valige rida, mis pakkumiskutsele üle viidi. Veenduge, et hind ja hankija oleksid taotlusele kopeeritud.  
6. Rippdialoogi avamiseks klõpsake valikut **Uus**.
7. Valige Lõpeta.
8. Valige leht.
9. Valige Lõpeta.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]