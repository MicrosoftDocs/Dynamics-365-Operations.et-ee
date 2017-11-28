--- 
title: "Põhivara kulumi arvutamine juriidiliste isikute lõikes"
description: "See protseduur näitab, kuidas seadistada ja käivitada mitme juriidilise isiku kulumiprotsessi."
author: saraschi2
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d804480167414cd038f8229db312dc9c52d131f8
ms.openlocfilehash: 4c45da124136b7fecb916d2ff9098c8ffeff6cb1
ms.contentlocale: et-ee
ms.lasthandoff: 11/02/2017

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a>Põhivara kulumi arvutamine juriidiliste isikute lõikes

[!include[task guide banner](../../includes/task-guide-banner.md)]

Mitme juriidilise isiku põhivara kulumit saab käitada ühe etapina. See protseduur näitab, kuidas seadistada ja käitada protsessi mitme juriidilise isiku jaoks. Selleks kasutatakse raamatupidaja rolli.  

Salvestamisel kasutatakse demoettevõtte USMF-i.


Toimingud (16) Alamtoiming: seadistage kontsernisiseste kulumikäituste töölehed. 

1. Esmalt peate seadistama töölehed, mida kasutatakse iga juriidilise isiku kontsernisiseses kulumikäituses. Avage Põhivarad > Seadistus > Põhivarade parameetrid. 
2. Laiendage jaotist Põhivara ettepanekud. 
3. Looge töölehe nimega kirje, mida kasutatakse juriidilises isikus iga sisestamiskihi jaoks. Kui raamatuid ei sisestata pearaamatusse, tuleb valida sisestamiskiht Puudub ja sellega seotud tööleht. Klõpsake vahekaarti Lisa. 
4. Valige või sisestage väärtus väljal Sisestamiskiht. 
5. Valige või sisestage väärtus väljal Töölehe nimi. 
6. Korrake töölehe seadistust iga juriidilise isiku lehel Põhivara parameetrid. 

Alamülesanne: kulumi arvutamine

1. Lehel Kulumiettepaneku loomine saate käivitada kulumikäituse mitmes juriidilises isikus. Avage Põhivarad > Töölehe kirjed > Kulumisoovituse koostamine. 
2. Valige või sisestage väärtus väljal Sisestamiskiht. 
3. Töölehe nimi põhineb põhivara parameetrites määratud vaikesättel. Seda saab praeguse juriidilise isiku jaoks siin muuta. 
4. Sisestage kuupäev väljale Lõpukuupäev. 
5. Valige kulumikäitusesse kaasatavad juriidilised isikud. Loendis kuvatakse ainult juriidilised isikud, kelle töölehed on põhivara parameetrite lehel põhivara ettepanekute jaoks häälestatud. 
6. Kui suvand Sisesta töölehed on lubatud, sisestatakse kulumitöölehed loomisel automaatselt. Kui suvand ei ole valitud, siis loodud töölehti ei sisestata, et saaksite üksikasjad enne sisestamist üle vaadata. Valige väljal Sisesta töölehed väärtus Jah. 
7. Filtreerimisväljad hõlmavad kõiki selle kulumikäituse jaoks valitud juriidiliste isikute põhivarasid, gruppe ja raamatuid. 
8. Suvand Pakktöötlus on vaikimisi lubatud. Kui suvand on lubatud, toimub kulumitöölehe loomine ja sisestamine taustal. 
9. Klõpsake suvandit Loo tööleht. 
10. Peate vaatama vastavates juriidilistes isikutes loodud kulumitöölehti. Avage Põhivarad > Töölehe sisestused > Põhivarade tööleht.

