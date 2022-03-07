---
title: Hankija arve kirjendamine arvete töölehele
description: Selles tegevuse juhises näitlikustatakse, kuidas salvestada hankija arveid, mis ei ole seostatud ostutellimustega.
author: abruer
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a60a5959046ca9e953bac80aaeb382d07a267643
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227132"
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