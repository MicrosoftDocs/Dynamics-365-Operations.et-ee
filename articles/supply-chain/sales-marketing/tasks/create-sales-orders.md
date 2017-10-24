--- 
title: "luua müügitellimusi;"
description: "Selles protseduuris näitlikustatakse, kuidas luua müügitellimust."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 4ccd2c4ace41f07dce14498031e3cc29ecb61b1c
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="create-sales-orders"></a>luua müügitellimusi;

[!include[task guide banner](../../includes/task-guide-banner.md)]

Selles protseduuris näitlikustatakse, kuidas luua müügitellimust. Saate selleks protseduuriks kasutada demoettevõtte USMF-i andmeid. Müügitellimusi loob tavaliselt müügitellimuse töötleja. 




## <a name="enter-sales-order-header-details"></a>Müügitellimuse päise üksikasjade sisestamine
1. Avage Müük ja turundus > Müügitellimused > Kõik müügitellimused.
2. Klõpsake valikut Uus.
3. Klõpsake väljal Kliendi konto otsingu avamiseks ripploendi nuppu.
4. Leidke loendist ja valige soovitud kliendikirje.
    * Selle näite puhul valige kliendikood US-004.  
5. Klõpsake loendis valitud real olevat linki.
6. Klõpsake nuppu OK.

## <a name="enter-sales-order-line-details"></a>Müügitellimuse rea üksikasjade sisestamine
    * Organisatsiooni müüdavate toodete variante saate eristada dimensioonide, nagu konfiguratsioon, värv, suurus ja stiil, kaupa. Tooted võivad olla seadistatud kasutama ladustamisdimensioone, nagu koht, ladu ja kaubaalus, või jälgimisdimensioone, nagu partii- ja seerianumbrid. Kui need dimensioonid on määratud, tuleks neile tellimuse real väärtused valida. Tellimuse sisestamise efektiivsuse parandamiseks võite lisada vastavad dimensiooniväljad tellimuse ruudustikule.  
1. Klõpsake valikut Müügitellimuse rida.
2. Klõpsake valikut Dimensioonid.
    * Selle näite puhul valige dimensioonid Värv, Koht ja Ladu. Siin valitud dimensioonid kuvatakse müügitellimuse ruudustikus. Kui soovitite, et teie valikud oleksid püsivad, seadke valiku Salvesta seadistus suvand olekusse Jah.   
3. Klõpsake nuppu OK.
4. Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.
5. Selle näite puhul valige kaubakood T0004.
6. Klõpsake loendis valitud real olevat linki.
    * Kui kaup on müügikategooria osa, ilmub kauba nimi automaatselt väljale Müügikategooria.  
    * Kui tootedimensiooni väljadel on juba väärtus, on see väärtus kopeeritud toote kirjest, kus see on määratletud kui toote vaikedimensioon. Vaikeväärtust saate alati muuta.   
7. Klõpsake väljal Värv otsingu avamiseks ripploendi nuppu.
8. Otsige loendist ja valige soovitud kirje.
9. Klõpsake loendis valitud real olevat linki.
10. Sisestage arv väljale Kogus.
    * Kui kaupa müüakse ostetavast, toodetavast või ladustatavast kaubast erineva ühikuga ning müügi mõõtühik on seatud toote kirjes, näidatakse seda väärtust väljal Ühik. Väärtust saab alati muuta.   
    * Kui väli Koht sisaldab juba väärtust, kopeeriti see tellimuse päisest või tootega seostatud tellimuse sätetest . Väärtust saab alati muuta. Kui väli on tühi, valige väärtus.   
    * Kui väli Ühiku hind sisaldab juba väärtust, kopeeriti see kehtivast kaubandusleppest või toote kirjest. (Ühiku hind võib tuleneda ka müügilepingust, kuid müügilepingu põhjal müügitellimuse loomise protsess erineb siin näidatust.) Kui väli on tühi, sisestage väärtus.   
    * Väli Allahindlus sisaldab allahindluse summat tooteühiku kohta. Rea allahindluse kogusumma arvutamiseks korrutatakse allahindluse väärtus rea kogusega.    Kui väli Allahindlus sisaldab juba väärtust, kopeeriti see kehtivast kaubandusleppest. Kui väli on tühi, ent soovite kliendile rea allahindlust anda, sisestage väärtus.  
    * Väli Allahindluse protsent sisaldab protsentväärtust, mille alusel rea brutosummat vähendatakse.  Kui väli Allahindluse protsent sisaldab juba väärtust, kopeeriti see kehtivast kaubandusleppest. Kui väli on tühi, ent soovite kliendile rea allahindlust anda, sisestage väärtus.  
    * Väljal Netosumma on väärtus, mis arvutatakse rea koguse ja allahindlusest lähtuvalt korrigeeritud ühikuhinna põhjal.  Saate arvutatud väärtuse tühistada ja muuga asendada.  

## <a name="review-the-order-totals"></a>Müügitellimuse kogusummade ülevaatamine
1. Klõpsake toimingupaanil valikut Müügitellimus.
2. Klõpsake valikut Kogusummad.
    * Leheküljel Kogusummad kuvatakse kogu tellimuse üksikasjad. See sisaldab vahesummat, mis on kõigi lõplike rea allahindluste võrra korrigeeritud rea netosummade summa, ning arve kogusummat, mis on lõpliku tellimuse taseme allahindluse, tasude, käibemaksu, kliendi krediidilimiidi jms alusel korrigeeritud vahesumma.  Arve summa on summa, mis kuvatakse kliendi arvedokumendil.  
3. Klõpsake nuppu OK.


