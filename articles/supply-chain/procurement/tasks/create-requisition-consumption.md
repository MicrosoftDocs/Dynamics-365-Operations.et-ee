--- 
title: Tarbimistaotluse loomine
description: See protseduur selgitab ostutaotluse loomise protsessi.
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 55ef4b1757a6f3c28c8575412d66488fda8608a5
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---
# <a name="create-a-requisition-for-consumption"></a>Tarbimistaotluse loomine

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur selgitab ostutaotluse loomise protsessi. See näitab erinevaid viise toodete otsimiseks hankekataloogist ja toodete lisamiseks, mis ei ole kataloogis. Enne selle protseduuri alustamist peab teil olema seadistatud ostupoliitika, mille ostutaotluse vaiketüübiks on Tarbimine. Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades. Protseduuri saab teha ainult kasutajaprofiiliga, mis on seadistatud töötaja profiilina.  Seda ülesannet teeb tavaliselt töötaja. Töötaja turberoll võimaldab ülesandeid teha; või juhul, kui kasutate USMF-i, saate sisse logida nime Alicia alt.


## <a name="create-a-new-requisition"></a>Uue tellimuse loomine
1. Tehke valik Hanked > Ostutaotlused > Minu ettevalmistatud ostutaotlused.
2. Klõpsake valikut Uus.
3. Sisestage väljale Nimi tellimuse jaoks nimi.
4. Sisestage kuupäev väljale Nõutav kuupäev.
    * Vaikimisi kopeeritakse nõutav kuupäev ja aruandluskuupäev ostutellimuste ridadele. Neid saab muuta rea tasandil. Nõudekuupäev on nõutud kättetoimetamiskuupäev.  
5. Sisestage kuupäev väljale Aruandluskuupäev.
    * Raamatupidamise kuupäeva kasutatakse raamatupidamiskirje salvestamiseks pearaamatusse ja kinnitamaks, kas eelarvevahendid on saadaval.  
6. Klõpsake nuppu OK.
7. Klõpsake väljal Põhjus otsingu avamiseks ripploendi nuppu.
    * Vaikimisi ilmub valitav äriline põhjendus ostutaotluse ridadel, kuid seda saab rea tasandil muuta.    
8. Otsige loendist ja valige soovitud kirje.
9. Valige põhjus.
10. Sisestage väljale Üksikasjad tellimuse põhjalikum kirjeldus.

## <a name="add-a-line-to-the-requisition"></a>Tellimusele rea lisamine
1. Klõpsake käsku Lisa rida.
    * Ostutaotlusele ridade lisamiseks on kaks võimalust. Kui teate juba tootenumbrit või teate, et taotlete toodet, mis ei ole tootekataloogis, saate rea lisada otse suvandiga „Lisa rida”. Teine võimalus on kasutada suvandit „Lisa tooteid”, mille puhul saate kaupade tootekataloogist otsimiseks kasutada otsingut ja filtreerimist.    
2. Klõpsake äsja loodud rida.
    * Nõude esitaja on töötaja, kes esitas tellimuse.   
    * Vaikimisi on tellimuse koostaja töötaja, kes selle esitab. Teile peab olema antud õigus teise töötaja nimel tellimuserida ette valmistada. Kui teil on see õigus olemas, kuvatakse selles otsingus teised töötajad.  
3. Sisestage väärtus väljale Kaubakood.
    * Teile valimiseks saada olevad kaubad on piiratud kategooria juurdepääsupoliitika ja ostva juriidilise isiku hankekataloogiga.   
4. Sisestage arv väljale Kogus.

## <a name="add-more-products-to-the-requisition"></a>Tellimusele lisatoodete lisamine
1. Klõpsake suvandit Lisa tooteid.
    * Selle suvandi puhul saate otsida tooteid tootekataloogist.    
2. Sisestage väljale Leia hankekategooria sõlm otsitava kategooria nime algus, seejärel klõpsake sisestusklahvi Enter.
    * Sisestage näiteks „arvut”.  
3. Kasutage otseteed InvokeDefaultButton.
4. Kasutage valitud kategooria toodete loendi filtreerimiseks suvandit Filtreeri.
5. Valige tootekaart, mille soovite tellimusele lisada.
6. Klõpsake suvandit Lisam ridadele.
7. Sisestage arv väljale Kogus.
8. Sisestage väljale Leia hankekategooria sõlm otsitava kategooria nime algus, seejärel klõpsake sisestusklahvi Enter.
    * Sisestage näiteks „Esilet” (esiletõstupliiatsid).  
9. Kasutage otseteed InvokeDefaultButton.
10. Hankekataloogis puuduva toote lisamiseks klõpsake suvandit Loendist puuduva toote lisamine ridadele.
11. Sisestage väärtus väljale Toote nimi.
12. Sisestage väärtus väljale Ühik.
13. Klõpsake nuppu OK.
14. Sisestage väljale Kauba kirjeldus toote kirjeldus.
15. Sisestage arv väljale Kogus.
16. Sisestage arv väljale Ühiku hind.
    * Kui teate kindla hankija hinda (kelle valite hankija konto väljal), saate sisestada selle hinna   
17. Klõpsake väljal Hankija konto otsingu avamiseks ripploendi nuppu.
    * Sellel väljal saadaolevad hankijad olenevad ostupoliitikatest ja hankija olekust praeguses hankekategoorias. Hankija siin valimise asemel võite klõpsata ka nuppu Soovita hankijat.    
18. Valige loendist hankija, keda soovite kasutada.
19. Sisestage väärtus väljale Väline kaubakood.
    * See on hankijale teada olev toote viitenumber. See võib olla näiteks toote kaubakood hankija enda kataloogis.  
20. Klõpsake nuppu OK.

## <a name="distribute-amounts"></a>Summade jaotamine
1. Klõpsake suvandit Finantsid.
2. Klõpsake suvandit Summade jaotamine.
    * See protsess selgitab, kuidas jaotada esimese rea kulu kahe konto vahel. Seda saate teha ka hiljem, kui tellimus on läbivaatusel.  
3. Klõpsake uue jaotusrea lisamiseks suvandit Tükelda.
4. Valige väljal Pearaamatukonto esimene kulukeskus, mis peaks olema kulu osa.
5. Valige teine jaotusrida.
6. Määrake väljal Pearaamatukonto teine kulukeskus.
7. Klõpsake suvandit Jaota võrdselt.
8. Sulgege leht.

## <a name="view-line-details"></a>Kuva rea üksikasjad
1. Lülitage jaotise Rea üksikasjad laiendamist.

## <a name="submit-the-requisition"></a>Tellimuse esitamine
1. Klõpsake suvandit Töövoog rippdialoogi avamiseks.
2. Klõpsake Edasta.
3. Sulgege leht.
4. Sisestage väljale Kommentaar märkus tellimuse kinnitajale.
5. Klõpsake Edasta.
6. Sulgege leht.
7. Värskendage lehte.


