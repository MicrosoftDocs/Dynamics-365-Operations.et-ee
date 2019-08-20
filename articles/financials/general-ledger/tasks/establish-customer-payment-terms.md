---
title: Kliendi maksetingimuste määramine
description: See protseduur määratleb skonto ja tähtaja seadistamise.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymDay, PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cddccbeb60e3eb9e498affcaa547fddb145a2bb2
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846412"
---
# <a name="establish-customer-payment-terms"></a>Kliendi maksetingimuste määramine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur määratleb skonto ja tähtaja seadistamise. See ülesande juhend kasutab demoettevõtet USMF.

1. Avage Müügireskontro > Maksete seadistus > Maksepäevad.
    * Maksetingimuste seadistust jagatakse Müügireskontro ja Ostureskontroga. Kui määratlete selle moodulis, on see saadaval ka teises moodulis. Selle ülesande juhendi puhul seadistan kõik maksetingimused suvandi Müügireskontro all.  
2. Klõpsake valikut Uus.
    * Looge maksepäev, kui teie maksetingimused nõuavad kindlat nädalapäeva (esmaspäev, teisipäev, jne) või kindlat kuupäeva (5., 10., jne).  
3. Sisestage maksepäeva ID maksepäeva väljale Maksepäev.
4. Sisestage maksepäeva kirjeldus väljale Kirjeldus.
5. Valige väljal Nädal/kuu Nädal või Kuu.
    * Kui soovite sisestada nädalapäeva, nagu esmaspäev, valige nädal. Kui soovite sisestada kuupäeva, nagu 10., valige kuu. Selle näite puhul valige Kuu.  
6. Sisestage kuupäev väljale Kuupäev.
    * Kuupäev tuleb sisestada numbriga, nagu 10, mitte järgarvuna 10.  
7. Klõpsake nuppu Salvesta.
8. Sulgege leht.
9. Avage Müügireskontro > Maksete seadistus > Maksetingimused.
10. Klõpsake valikut Uus.
    * Maksetingimusi kasutatakse määratlemaks, kuidas tähtaegu arvutatakse. Skonto kuupäeva seadistus on määratletud eraldi lehel.  
11. Sisestage väljal Maksetingimused ID väljale Maksetingimused.
12. Sisestage kirjeldus väljale Kirjeldus.
13. Valige makseviis, nagu Tasutakse kättesaamisel, Neto, Praegune kuu jne.
    * Maksetingimusi kasutatakse määratlemaks, kuidas tähtaja algust arvutatakse.  Näiteks netot kasutatakse, kui tähtaeg on alati teatud arv kuid või päevi pärast arve kuupäeva. Suvandit Tasutakse kättesaamisel saab kasutada, kui makset nõutakse arve saamisel, nii et tähtaega ei arvutata. Valige selle ülesande juhendi puhul Käesolev kuu.  
14. Valige maksepäev, kui arvutusse on kaasatud kindel nädalapäev või kuupäev.
    * Olenevalt maksetingimustest võite koguse sisestada kuudes või päevades. Võite maksemeetodile lisamiseks kasutada ka valikut Maksegraafik või Maksepäev. Kui tähtaeg on alati järgmise kuu 10. kuupäev, valige Maksepäevaks 10. kuupäev.  
15. Klõpsake nuppu Salvesta.
16. Sulgege leht.
17. Avage Müügireskontro > Maksete seadistus > Skontod.
18. Klõpsake valikut Uus.
    * Seda lehte kasutatakse määratlemaks, kuidas skonto kuupäeva arvutatakse.  
19. Sisestage väljal Skonto ID väljale Skonto.
20. Sisestage kirjeldus väljale Kirjeldus.
21. Kui saadaval on mitmetasandiline skonto, valige Järgmine skonto kood, mis on pärast seda uut skontot oluline.
22. Sisestage skonto kuupäeva arvutamiseks kasutatav päevade arv.
    * Neto põhimõtte valimisel lisatakse skonto kuupäeva arvutamiseks päevade arv arve kuupäevale.  
23. Sisestage skonto protsent.
24. Sisestage põhikonto, millele sisestatakse skonto kliendiarvete puhul.
25. Valige suvand väljalt Allahindluse vastaskontod.
    * Kui valite suvandi Kontod arve real, sisestatakse skonto hankija arve ridadel sama vara/kulu põhikontole. Kui valite suvandi Kasuta hankija arvete puhul põhikontot, sisestatakse skonto põhikontole, mille määratlete suvandis Hankija arvete põhikonto. Selle näite puhul valige suvand Kasuta hankija arvete puhul põhikontot.  
26. Sisestage põhikonto, millele sisestatakse skonto hankija arvete puhul.
27. Klõpsake nuppu Salvesta.

