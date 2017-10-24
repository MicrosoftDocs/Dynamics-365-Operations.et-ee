---
title: Sisestamisdefinitsioonid
description: "Selles artiklis antakse teavet sisestamisdefinitsioonide ning nende määratlemise ja linkimise kohta. Toetatud sisestustüüpide ja dokumentide puhul saab sisestusreeglite asemel kasutada raamatupidamiskirjete põhikontode ja finantsdimensioonide klassifitseerimiseks sisestamisdefinitsioone."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9c49e4abe28078f62f46b4eea4e22a268339b569
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="posting-definitions"></a>Sisestamisdefinitsioonid

[!include[banner](../includes/banner.md)]


Selles artiklis antakse teavet sisestamisdefinitsioonide ning nende määratlemise ja linkimise kohta. Toetatud sisestustüüpide ja dokumentide puhul saab sisestusreeglite asemel kasutada raamatupidamiskirjete põhikontode ja finantsdimensioonide klassifitseerimiseks sisestamisdefinitsioone.

Toetatud sisestustüüpide ja dokumentide puhul saab sisestusreeglite asemel kasutada raamatupidamiskirjete põhikontode ja finantsdimensioonide klassifitseerimiseks sisestamisdefinitsioone. Toetatud dokumente ja sisestustüüpe saate vaadata lehel **Kande sisestamisdefinitsioonid**. 

Sisestamisdefinitsioonide kasutamise alustamiseks märkige valik**Kasuta sisestamisdefinitsioone** lehel **Pearaamatu parameetrid**. Isegi siis, kui kasutate sisestamisdefinitsioone, tuleb siiski määratleda algsete kirjete ning toetuseta sisestustüüpide ja dokumentide sisestusreeglid. 

Sisestamisdefinitsioone tuleb kasutada ostutellimuste pandiõiguse ja ostutaotluste eelpandiõiguse arvestuse lubamiseks.

## <a name="defining-posting-definitions"></a>Sisestamisdefinitsioonide määratlemine
Kasutage lehte**Sisestamisdefinitsioonid** vastendamise kriteeriumide määramiseks ja määratlege kirjed, mis tuleks luua, kui ilmneb vaste. Vastendamiskriteeriume hinnatakse algsete kannete puhul arvestuse jaotustena. 

Lehel **Sisestamisdefinitsioonid** saab määrata kirje ridadele ka prioriteedinumbreid, et juhtida ridade hindamise järjekorda. Vähima prioriteedinumbriga ridu hinnatakse esimesena. Näiteks hinnatakse kõigepealt kõiki ridu, mille prioriteet on 1, ja seejärel ridu, mille prioriteet on 2 jne. Vaste leidmisel eiratakse teisi vastavusseviimise kriteeriume. Lisaks loovad kirjeid ainult algsele kandele vastavad kriteeriumid grupis. 

Saate kinnitada oma sisestamisdefinitsioonid, kasutades viisardit **Sisestamisdefinitsiooni testimine**. Kui määratlete sisestamisdefinitsioonile algse kirje näidise, näete loodavaid kirjeid. 

Sisestamisdefinitsiooni versioone saab kasutada koos kehtivuskuupäevadega. Näiteks saate luua sisestamisdefinitsiooni tulevase versiooni teise pearaamatukontosse sisestamiseks uuel finantsaastal. 

Lehel **Kande sisestamisdefinitsioonid** saate määrata kandetüüpidele sisestamisdefinitsioonid.

## <a name="linking-posting-definitions"></a>Sisestamisdefinitsioonide sidumine
Sisestamisdefinitsioonide loomisel saate siduda ühe sisestamisdefinitsiooni teisega. Seotud definitsiooni kriteeriume arvestatakse siis lisaks praeguse sisestamisdefinitsiooni kriteeriumidele. See funktsioon aitab aega säästa, kuna pole vaja sisestada uuesti praeguse sisestamisdefinitsiooni kriteeriume kiirkaardile **Kirjed** lehel **Sisestamisdefinitsioonid**, kui sisestasite need read juba teisele definitsioonile. 

Lisage diagrammidele või tabelitele kõik lingid, mida võite kasutada. Praeguse sisestamisdefinitsiooniga vastuolude vältimiseks veenduge, et seotavate sisestamisdefinitsioonide read oleksid kordumatud. 

Sisestamisdefinitsioonide linkide loomisel kehtivad järgmised piirangud.

-   Antud sisestamisdefinitsioon võib olla lingitud teise sisestamisdefinitsiooniga või teisest sisestamisdefinitsioonist, kuid mitte mõlemat. Kuid sisestamisdefinitsioon võib olla lingitud mitme sisestamisdefinitsiooniga.
-   Saate seadistada linke ainult samas moodulis olevate sisestamisdefinitsioonide vahel.
-   Sisestamisdefinitsiooni saab määrata igale kandetüübile, kuid kandetüüp peab olema sisestamisdefinitsiooniga samas moodulis. Lehelt **Kande sisestamisdefinitsioonid** saate vaadata, millises moodulis kandetüüp on.


Lisateavet vaadake teemast [Sisestamisdefinitsioonide näited](example-posting-definitions.md). 



