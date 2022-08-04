---
title: Kliendi maksetingimuste määramine
description: See protseduur määratleb skonto ja tähtaja seadistamise.
author: aprilolson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PaymDay, PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6069d28d84ab1705fd62a33cea7e0b923f0e0705
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065704"
---
# <a name="establish-customer-payment-terms"></a>Kliendi maksetingimuste määramine

[!include [banner](../../includes/banner.md)]

See protseduur määratleb skonto ja tähtaja seadistamise. See ülesande juhend kasutab demoettevõtet USMF.

1. Avage **Navigeerimispaan > Moodulid > Müügireskontro > Maksete seadistamine > Maksepäevad**. **Maksetingimuste** seadistust jagatakse **Müügireskontro** ja **Ostureskontroga**. Kui määratlete selle moodulis, on see saadaval ka teises moodulis. Selle ülesande juhendi jaoks on seadistatud kõik müügireskontro **maksetingimused**.
2. Klõpsake valikut **Uus**. Looge maksepäev, kui teie maksetingimused nõuavad kindlat nädalapäeva (esmaspäev, teisipäev, jne) või kindlat kuupäeva (5., 10., jne). 
3. Sisestage ID väljale **Maksepäev**.
4. Sisestage maksepäeva kirjeldus väljale **Kirjeldus**.
5. Valige väljal **Nädal/kuu** Nädal või Kuu. Kui soovite sisestada nädalapäeva, nagu esmaspäev, valige nädal. Kui soovite sisestada kuupäeva, nagu 10., valige kuu. Selle näite puhul valige Kuu. 
6. Sisestage kuupäev väljale **Kuupäev**. Kuupäev tuleb sisestada numbriga, nagu 10, mitte järgarvuna 10. 
7. Klõpsake valikut **Salvesta**.
8. Sulgege leht.
9. Avage **Navigeerimispaan > Moodulid > Müügireskontro > Maksete seadistamine > Maksetingimused**.
10. Klõpsake valikut **Uus**. **Maksetingimusi** kasutatakse tähtaja arvutamise id määratlemaks. Skonto kuupäeva seadistus on määratletud eraldi lehel. 
11. Sisestage ID väljale **Maksetingimused**.
12. Väljale **Kirjeldus** sisestage kirjeldus.
13. Valige makseviis **,** nt **COD**, **Neto**, **Praegune** kuu jne. Maksemeetodi **abil** määratletakse tähtaja arvutamise algus. Näiteks netoarvet **kasutatakse** siis, kui tähtaeg on alati seatud kuude või päevade arv pärast arve kuupäeva. **Tasumist** saab kasutada juhul, kui arve maksmisel on nõutav makse, seega lõppkuupäeva ei arvutata. Ülesande **juhendi** jaoks praeguse kuu valimine.  
14. Valige **Maksepäev**, kui arvutusse on kaasatud kindel nädalapäev või kuupäev. Olenevalt maksetingimustest võite koguse sisestada kuudes või päevades. Või saate kasutada maksegraafikut või maksepäeva, et lisada see makseviisi **lõppu**.**·** **·** Kui tähtaeg on alati järgmise kuu 10. kuupäev, valige **Maksepäevaks** 10. kuupäev. Maksekalendri kasutamisel **saate määrata** tähtaja määratlemise, kui arvutatud kuupäev jääb mittetööpäevale. Algne tähtaeg arvutatakse kalendripäevade alusel. Kui arvutatud kuupäev jääb mittetööpäevale, saate arvutatud maksetähtaega korrigeerida kas järgmisele töökuupäevale või varasemale tööpäevale.
15. Klõpsake nuppu **Salvesta**.
16. Sulgege leht.
17. Avage **Müügireskontro > Maksete seadistus > Skontod**.
18. Klõpsake valikut **Uus**. Seda lehte kasutatakse määratlemaks, kuidas skonto kuupäeva arvutatakse. 
19. Sisestage ID väljale **Skonto**.
20. Väljale **Kirjeldus** sisestage kirjeldus.
21. Kui saadaval on mitmetasandiline skonto, valige **Järgmine skonto kood**, mis on pärast seda uut skontot oluline.
22. Sisestage väljale **Päevad** skonto kuupäeva arvutamiseks kasutatav päevade arv. **Neto** põhimõtte valimisel lisatakse skonto kuupäeva arvutamiseks päevade arv arve kuupäevale.  
23. Sisestage väljale **Allahindlusprotsent** skonto protsent.
24. **Kliendi allahindluste põhikontol** sisestage põhikonto, kuhu sisestatakse skonto kliendiarvete jaoks.
25. Valige suvand väljalt **Allahindluse vastaskontod**. Kui valite suvandi Kontod arve real, sisestatakse skonto hankija arve ridadel sama vara/kulu põhikontole. Kui valite **hankija arvete jaoks põhikonto**, sisestab skonto põhikonto põhikontole, **mille määratlete hankija arvete põhikontos**. Näiteks valige hankija arvete **jaoks põhikonto kasutamine**. 
26. **Hankija allahindluste põhikonto** väljal sisestage põhikonto, kuhu sisestatakse skonto hankija arvete jaoks.
27. Klõpsake valikut **Salvesta**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
