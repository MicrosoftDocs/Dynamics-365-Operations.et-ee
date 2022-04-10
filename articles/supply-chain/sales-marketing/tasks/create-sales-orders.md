---
title: luua müügitellimusi;
description: Selles protseduuris näitlikustatakse, kuidas luua müügitellimust.
author: Henrikan
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, InventDimParmFixed, InventProductDimensionLookup, SalesTotals
audience: Application User, SalesTableDelete, SalesTableListPagePreviewPage, SalesUpdateRemain
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5746fa0ab9fd7ef3e288adc88a755324309a27c0
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566307"
---
# <a name="create-sales-orders"></a>luua müügitellimusi;

[!include [banner](../../includes/banner.md)]

Selles protseduuris näitlikustatakse, kuidas luua müügitellimust. Saate selleks protseduuriks kasutada demoettevõtte USMF-i andmeid. Müügitellimusi loob tavaliselt müügitellimuse töötleja. 

## <a name="enter-sales-order-header-details"></a>Müügitellimuse päise üksikasjade sisestamine
1. Avage **Navigeerimispaan > Moodulid > Müük ja turundus > Müügitellimused > Kõik müügitellimused**.
2. Valige suvand **Uus**.
3. Valige otsingu avamiseks väljal **Kliendi konto** ripploendi nupp.
4. Leidke loendist ja valige soovitud kliendikirje.
    - Selle näite puhul valige kliendikood US-004.  
5. Valige nupp **OK**.

## <a name="enter-sales-order-line-details"></a>Müügitellimuse rea üksikasjade sisestamine
    
Organisatsiooni müüdavate toodete variante saate eristada dimensioonide, nagu konfiguratsioon, värv, suurus ja stiil, kaupa. Tooted võivad olla seadistatud ka kasutama laoala dimensioone, nagu koht, ladu ja kaubaalus, või jälgimisdimensioone, nagu partii- ja seerianumbrid. Kui need dimensioonid on määratud, tuleks neile tellimuse real väärtused valida. Tellimuse sisestamise efektiivsuse parandamiseks võite lisada vastavad dimensiooniväljad tellimuse ruudustikule.
    
1. Valige jaotises **Müügitellimuse read** suvand **Müügitellimuse rida**.
2. Valige **Dimensioonid**.
    
    Selle näite puhul valige dimensioonid Värv, Koht ja Ladu. Siin valitud dimensioonid kuvatakse müügitellimuse ruudustikus. Kui soovitite, et teie valikud oleksid püsivad, seadke valiku **Salvesta seadistus** suvand olekusse Jah.
    
3. Valige nupp **OK**.
4. Valige otsingu avamiseks väljal **Kaubakood** ripploendi nupp.
5. Selle näite puhul valige kaubakood T0004.
    - Kui kaup on müügikategooria osa, ilmub kauba nimi automaatselt väljale Müügikategooria.  
    - Kui tootedimensiooni väljadel on juba väärtus, on see väärtus kopeeritud toote kirjest, kus see on määratletud kui toote vaikedimensioon. Vaikeväärtust saate alati muuta.   
6. Valige otsingu avamiseks väljal **Värv** ripploendi nupp.
7. Otsige loendist ja valige soovitud kirje.
8. Sisestage arv väljale **Kogus**.
    - Kui kaupa müüakse ostetavast, toodetavast või ladustatavast kaubast erineva ühikuga ning müügi mõõtühik on seatud toote kirjes, näidatakse seda väärtust väljal **Ühik**. Väärtust saab alati muuta.   
    - Kui väli **Koht** sisaldab juba väärtust, kopeeriti see tellimuse päisest või tootega seostatud tellimuse sätetest . Väärtust saab alati muuta. Kui väli on tühi, valige väärtus.   
    - Kui väli **Ühiku hind** sisaldab juba väärtust, kopeeriti see kehtivast kaubandusleppest või toote kirjest. (Ühiku hind võib tuleneda ka müügilepingust, kuid müügilepingu põhjal müügitellimuse loomise protsess erineb siin näidatust.) Kui väli on tühi, sisestage väärtus.   
    - Väli **Allahindlus** sisaldab allahindluse summat tooteühiku kohta. Rea allahindluse kogusumma arvutamiseks korrutatakse allahindluse väärtus rea kogusega. Kui väli **Allahindlus** sisaldab juba väärtust, kopeeriti see kehtivast kaubandusleppest. Kui väli on tühi, ent soovite kliendile rea allahindlust anda, sisestage väärtus.  
    - Väli **Allahindluse protsent** sisaldab protsentväärtust, mille alusel rea brutosummat vähendatakse.  Kui väli **Allahindluse protsent** sisaldab juba väärtust, kopeeriti see kehtivast kaubandusleppest. Kui väli on tühi, ent soovite kliendile rea allahindlust anda, sisestage väärtus. 
    - Väljal **Netosumma** on väärtus, mis arvutatakse rea koguse ja allahindlusest lähtuvalt korrigeeritud ühikuhinna põhjal.  Saate arvutatud väärtuse tühistada ja muuga asendada.  

## <a name="review-the-order-totals"></a>Müügitellimuse kogusummade ülevaatamine
1. Klõpsake **Toimingupaanil** valikut **Müügitellimus**.
2. Valige **summad**.
    
    Leheküljel **Kogusummad** kuvatakse kogu tellimuse üksikasjad. See sisaldab vahesummat, mis on kõigi lõplike rea allahindluste võrra korrigeeritud rea netosummade summa, ning arve kogusummat, mis on lõpliku tellimuse taseme allahindluse, tasude, käibemaksu, kliendi krediidilimiidi jms alusel korrigeeritud vahesumma. Arve summa on summa, mis kuvatakse kliendi arvedokumendil.  
    
3. Valige nupp **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]