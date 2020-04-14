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
ms.openlocfilehash: f641d75e06b11ca325d2624f836fc2a7c92d69e4
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138395"
---
# <a name="establish-customer-payment-terms"></a>Kliendi maksetingimuste määramine

[!include [banner](../../includes/banner.md)]

See protseduur määratleb skonto ja tähtaja seadistamise. See ülesande juhend kasutab demoettevõtet USMF.

1. Avage **Navigeerimispaan > Moodulid > Müügireskontro > Maksete seadistamine > Maksepäevad**. **Maksetingimuste** seadistust jagatakse **Müügireskontro** ja **Ostureskontroga**. Kui määratlete selle moodulis, on see saadaval ka teises moodulis. Selle ülesande juhendi puhul seadistan kõik maksetingimused suvandi **Müügireskontro** all.
2. Klõpsake valikut **Uus**. Looge maksepäev, kui teie maksetingimused nõuavad kindlat nädalapäeva (esmaspäev, teisipäev, jne) või kindlat kuupäeva (5., 10., jne). 
3. Sisestage ID väljale **Maksepäev**.
4. Sisestage maksepäeva kirjeldus väljale **Kirjeldus**.
5. Valige väljal **Nädal/kuu** Nädal või Kuu. Kui soovite sisestada nädalapäeva, nagu esmaspäev, valige nädal. Kui soovite sisestada kuupäeva, nagu 10., valige kuu. Selle näite puhul valige Kuu. 
6. Sisestage kuupäev väljale **Kuupäev**. Kuupäev tuleb sisestada numbriga, nagu 10, mitte järgarvuna 10. 
7. Klõpsake valikut **Salvesta**.
8. Sulgege leht.
9. Avage **Navigeerimispaan > Moodulid > Müügireskontro > Maksete seadistamine > Maksetingimused**.
10. Klõpsake valikut **Uus**. Maksetingimusi kasutatakse määratlemaks, kuidas tähtaegu arvutatakse. Skonto kuupäeva seadistus on määratletud eraldi lehel. 
11. Sisestage ID väljale **Maksetingimused**.
12. Väljale **Kirjeldus** sisestage kirjeldus.
13. Valige **Makseviis,** nt tasutakse kättesaamisel, neto, jooksev kuu jne. Makseviisi kasutatakse tähtaja arvutamise alguse määratlemiseks. Näiteks netot kasutatakse, kui tähtaeg on alati teatud arv kuid või päevi pärast arve kuupäeva. Suvandit Tasutakse kättesaamisel saab kasutada, kui makset nõutakse arve saamisel, nii et tähtaega ei arvutata. Valige selle ülesande juhendi puhul Käesolev kuu.  
14. Valige **Maksepäev**, kui arvutusse on kaasatud kindel nädalapäev või kuupäev. Olenevalt maksetingimustest võite koguse sisestada kuudes või päevades. Võite maksemeetodile lisamiseks kasutada ka valikut **Maksegraafik** või **Maksepäev**. Kui tähtaeg on alati järgmise kuu 10. kuupäev, valige **Maksepäevaks** 10. kuupäev. 
15. Klõpsake valikut **Salvesta**.
16. Sulgege leht.
17. Avage **Müügireskontro > Maksete seadistus > Skontod**.
18. Klõpsake valikut **Uus**. Seda lehte kasutatakse määratlemaks, kuidas skonto kuupäeva arvutatakse. 
19. Sisestage ID väljale **Skonto**.
20. Väljale **Kirjeldus** sisestage kirjeldus.
21. Kui saadaval on mitmetasandiline skonto, valige **Järgmine skonto kood**, mis on pärast seda uut skontot oluline.
22. Sisestage väljale **Päevad** skonto kuupäeva arvutamiseks kasutatav päevade arv. **Neto** põhimõtte valimisel lisatakse skonto kuupäeva arvutamiseks päevade arv arve kuupäevale.  
23. Sisestage väljale **Allahindlusprotsent** skonto protsent.
24. **Kliendi allahindluste põhikontol** sisestage põhikonto, kuhu sisestatakse skonto kliendiarvete jaoks.
25. Valige suvand väljalt **Allahindluse vastaskontod**. Kui valite suvandi Kontod arve real, sisestatakse skonto hankija arve ridadel sama vara/kulu põhikontole. Kui valite suvandi Kasuta hankija arvete puhul põhikontot, sisestatakse skonto põhikontole, mille määratlete suvandis Hankija arvete põhikonto. Selle näite puhul valige suvand Kasuta hankija arvete puhul põhikontot. 
26. **Hankija allahindluste põhikonto** väljal sisestage põhikonto, kuhu sisestatakse skonto hankija arvete jaoks.
27. Klõpsake valikut **Salvesta**.

