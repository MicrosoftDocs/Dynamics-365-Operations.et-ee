---
title: Hankija arve kirjendamine arvete töölehele
description: Selles tegevuse juhises näitlikustatakse, kuidas salvestada hankija arveid, mis ei ole seostatud ostutellimustega.
author: abruer
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27d0e81ca37c9a59adc3acce3610fd17fd954a8b
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716637"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Hankija arve kirjendamine arvete töölehele

[!include [banner](../../includes/banner.md)]

Selles tegevuse juhises näitlikustatakse, kuidas salvestada hankija arveid, mis ei ole seostatud ostutellimustega. Selle arve tüübi näited sisaldavad varude või teenuste kulusid.  Salvestamisel kasutatakse demoettevõtte USMF-i.

1. Avage **Navigeerimispaan > Moodulid > Ostureskontro > Tööruumid > Müüja arve kanne**.
2. Klõpsake **tegumiribal** valikut **Uus**.
3. Klõpsake valikut **Uus**.
4. Sisestage töölehe nimi väljale **Nimi** või klõpsake otsingu avamiseks ripploendi nuppu.
5. Sisestage väärtus väljale **Kirjeldus**.
6. Klõpsake **Toimingupaanil** valikut **Read**. Sisestage sisestuskuupäev, mis ühtlasi värskendab pearaamatut, väljale **Kuupäev**.  
7. Täpsustage **Hankija kontot** väljal **Konto**.
8. Sisestage arve number väljale **Arve**.
9. Sisestage väärtus väljale **Kirjeldus**.
10. Sisestage number väljale **Kreedit**.
11. Sisestage kontonumber väljale **Vastaskonto** või klõpsake otsingu avamiseks ripploendi nuppu
    * **Käibemaksugrupp** pärineb vaikimisi hankija kontolt.  
    * **Kauba käibemaksugrupp** pärineb vaikimisi väljal **Vastaskonto** määratud põhikontolt.  
    * **Tähtaeg** arvutatakse maksetingimuste alusel.  
    * **Sularaha allahindlus** vaikimisi kehtib müüjakontolt.
12. Kui olete hankija arve töölehe töövoo lubanud, klõpsake valikul **Töövoog > Esita**.
    * Kui teie esildis on kinnitatud, edastatakse kuupäev järgmise avatud perioodi esimesele päevale, kui kande sisestuskuupäev jääb perioodi, mis on ootel või pearaamatu sisestusteks suletud.
12. Klõpsake käsku **Sisesta**.
13. Sulgege leht.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
