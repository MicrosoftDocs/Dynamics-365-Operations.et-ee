---
title: Tarbimistaotluse loomine
description: See teema kirjeldab küsimustiku koostamise protsessi.
author: mkirknel
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: acc2cdb9b74cccaefe565b0e2ae8ec4c5f2401c4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426126"
---
# <a name="create-a-requisition-for-consumption"></a>Tarbimistaotluse loomine

[!include [banner](../../includes/banner.md)]

See teema kirjeldab küsimustiku koostamise protsessi. See näitab erinevaid viise toodete otsimiseks hankekataloogist ja toodete lisamiseks, mis ei ole kataloogis. Enne selle protseduuri alustamist peab teil olema seadistatud ostupoliitika, mille ostutaotluse vaiketüübiks on Tarbimine. Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades. Protseduuri saab teha ainult kasutajaprofiiliga, mis on seadistatud töötaja profiilina. Seda ülesannet teeb tavaliselt töötaja. **Töötaja** turberoll võimaldab ülesandeid teha; või juhul, kui kasutate USMF-i, saate sisse logida nime **Alicia** alt.


## <a name="create-a-new-requisition"></a>Uue tellimuse loomine
1. Avage **Navigeerimispaan > Moodulid > Hanked > Ostutaotlused > Minu ette valmistatud ostutaotlused**.
2. Valige suvand **Uus**.
3. **Sisestage väljale Nimi tellimuse jaoks nimi.**
4. **Sisestage kuupäev väljale Nõutav kuupäev.** Vaikimisi kopeeritakse nõutav kuupäev ja aruandluskuupäev ostutellimuste ridadele. Neid saab muuta rea tasandil. Nõudekuupäev on nõutud kättetoimetamiskuupäev.  
5. Sisestage kuupäev väljale **Aruandluskuupäev.** Raamatupidamise kuupäeva kasutatakse raamatupidamiskirje salvestamiseks pearaamatusse ja kinnitamaks, kas eelarvevahendid on saadaval.  
6. Valige nupp **OK**.
7. Valige väljal **Põhjus** ripploendist suvand. Vaikimisi ilmub valitav äriline põhjendus ostutaotluse ridadel, kuid seda saab rea tasandil muuta.  
8. Valige põhjus.
9. Sisestage väljale **Üksikasjad** tellimuse põhjalikum kirjeldus.

## <a name="add-a-line-to-the-requisition"></a>Tellimusele rea lisamine
1. Valige **Lisa rida**. Ostutaotlusele ridade lisamiseks on kaks võimalust. Kui teate juba tootenumbrit või teate, et taotlete toodet, mis ei ole tootekataloogis, saate rea lisada otse suvandiga **Lisa rida**. Teine võimalus on kasutada suvandit **Lisa tooteid**, mille puhul saate kaupade tootekataloogist otsimiseks kasutada otsingut ja filtreerimist.    
2. Valige äsja loodud koondandmed.
    - Nõude esitaja on töötaja, kes esitas tellimuse.   
    - Vaikimisi on tellimuse koostaja töötaja, kes selle esitab. Teile peab olema antud õigus teise töötaja nimel tellimuserida ette valmistada. Kui teil on see õigus olemas, kuvatakse selles otsingus teised töötajad.  
3. Sisestage väärtus väljale **Kaubakood**. Teile valimiseks saada olevad kaubad on piiratud kategooria juurdepääsupoliitika ja ostva juriidilise isiku hankekataloogiga.   
4. Sisestage arv väljale **Kogus**.

## <a name="add-more-products-to-the-requisition"></a>Tellimusele lisatoodete lisamine
1. Valige **Lisa tooteid**. Selle suvandi puhul saate otsida tooteid tootekataloogist.    
2. Sisestage väljale **Leia hankekategooria sõlm** otsitava kategooria nime algus, seejärel klõpsake sisestusklahvi **Enter**. Sisestage näiteks `comput`.  
3. Kasutage otseteed **InvokeDefaultButton**.
4. Kasutage valitud kategooria toodete loendi filtreerimiseks suvandit **Filtreeri**.
5. Valige tootekaart, mille soovite tellimusele lisada.
6. Valige **Lisa ridadele**.
7. Sisestage arv väljale **Kogus**.
8. Sisestage väljale **Leia hankekategooria sõlm otsitava kategooria nime** algus, seejärel klõpsake sisestusklahvi **Enter**. Sisestage näiteks `High` (esiletõstjad).  
9. Kasutage otseteed **InvokeDefaultButton**.
10. Hankekataloogis puuduva toote lisamiseks klõpsake suvandit **Loendist puuduva toote lisamine ridadele**.
11. Sisestage väärtus väljale **Toote nimi**.
12. Sisestage väärtus väljale **Ühik**.
13. Valige nupp **OK**.
14. Sisestage väljale **Kauba kirjeldus** toote kirjeldus.
15. Sisestage arv väljale **Kogus**.
16. Sisestage arv väljale **Ühiku hind**. Kui teate kindla hankija hinda (kelle valite hankija konto väljal), saate sisestada selle hinna   
17. Klõpsake väljal **Hankija konto** otsingu avamiseks ripploendi nuppu. Sellel väljal saadaolevad hankijad olenevad ostupoliitikatest ja hankija olekust praeguses hankekategoorias. Hankija siin valimise asemel võite klõpsata ka nuppu **Soovita hankijat**.    
18. Valige loendist hankija, keda soovite kasutada.
19. Sisestage väärtus väljale **Väline kaubakood**. See on hankijale teada olev toote viitenumber. See võib olla näiteks toote kaubakood hankija enda kataloogis.  
20. Valige nupp **OK**.

## <a name="distribute-amounts"></a>Summade jaotamine
1. Valige **Finantsasjad**.
2. Kuva **jaotamissummad**. See protsess selgitab, kuidas jaotada esimese rea kulu kahe konto vahel. Seda saate teha ka hiljem, kui tellimus on läbivaatusel.  
3. Klõpsake uue jaotusrea lisamiseks suvandit **Tükelda**.
4. Valige väljal **Pearaamatukonto** esimene kulukeskus, mis peaks olema kulu osa.
5. Valige teine jaotusrida.
6. Määrake väljal Pearaamatukonto teine kulukeskus.
7. Jaota **võrdselt**
8. Sulgege leht.

## <a name="view-line-details"></a>Kuva rea üksikasjad
1. Lülitage jaotise **Rea üksikasjad** laiendamist.

## <a name="submit-the-requisition"></a>Tellimuse esitamine
1. Rippdialoogi avamiseks klõpsake valikut **Uus**.
2. Valige käsk **Esita**.
3. Sulgege leht.
4. Sisestage väljale **Kommentaar** märkus tellimuse kinnitajale.
5. Valige käsk **Esita**.
6. Sulgege leht.
7. Värskendage lehte.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]