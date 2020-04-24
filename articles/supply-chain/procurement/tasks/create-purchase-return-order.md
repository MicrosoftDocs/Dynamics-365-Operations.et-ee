---
title: Ostu tagastustellimuse loomine
description: See protseduur näitab, kuidas koostada ostu tagastustellimust, kasutades kreeditarve toimingut hankija arve dokumendilt ridade kopeerimiseks uuele ostutellimusele.
author: mkirknel
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchCopying, InventMarking, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c83cafd3a8934c488bb7a9f315bd5cb154f88c09
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204819"
---
# <a name="create-a-purchase-return-order"></a>Ostu tagastustellimuse loomine

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas koostada ostu tagastustellimust, kasutades kreeditarve toimingut hankija arve dokumendilt ridade kopeerimiseks uuele ostutellimusele. Samuti näitab see, kuidas tellimust kinnitada ja töödelda kaupade saatmist tagasi hankijale. Selles protseduuris toodud näidet saab kasutada demoandmete ettevõtte USMF puhul. Seda ülesannet täidab üldjuhul ostuagent.

## <a name="create-a-new-purchase-return-order"></a>Uue ostu tagastustellimuse loomine
1. Minge **navigeerimispaanile > Moodulid > Hange ja hankimine > Ostutellimused > Kõik ostutellimused**. Esimene samm on koostada uus ostutellimus, mida kasutada ostu tagastustellimusena.  
2. Klõpsake valikut **Uus**.
3. Sisestage väljale **Hankija konto** väärtus „US-102”.
4. Klõpsake valikut **OK**.
5. Klõpsake **Tegevuspaanil** valikut **Ost**.
6. Klõpsake valikut **Kreeditarve**. See on leht, millel saate olemasolevalt hankija arvelt oma tagastustellimusele kopeerida. See on sama leht, mida kasutatakse teiste kopeerimistoimingute jaoks. Kuid kuna avasime selle toimingust Kreeditarve, on leht konfigureeritud toetama tagastustellimuse loomist, mis tasakaalustab hankija arved.  
7. Laiendage jaotist **Parameetrid**.
    - Valik **Muuda märki** on automaatselt märgitud ja seda ei saa muuta. See tagab märgi muutmise koguste puhul ja selle, et lisatavad read tasakaalustavad hankija arve.  
    - Valik **Kopeeri tasud** on automaatselt märgitud ja seda ei saa muuta. See tähendab, et hankija arvelt lisatakse tasud ostu tagastustellimusele algse tasu tasakaalustamiseks. Tellimuse päise ja ridade muudatusi on võimalik hiljem muuta.  
    - Valik **Kopeeri täpselt** on automaatselt märgitud ja seda ei saa muuta. See tagab kõigil hankija arve päise ja ridade väljadel olevatest väärtustest täpse koopia tegemise. See tähendab, et koostatakse ostu tagastustellimus väärtustega, mis vastavad kõigil hankija arve dokumendil kasutatavatele tingimustele. 
    - Valik **Kustuta osturead** kustutab enne uute ridade lisamist kõik ostutellimuse read, mis on juba ostutellimusel olemas. Selles näites pole me veel ostu tagastustellimusele ridu lisanud, seega poleks sellel mingit mõju. Kasutage seda valikut ettevaatlikult, kuna see kustutab kõik olemasolevad read hoiatamata.  
    * Valik **Kopeeri tellimuse päis** on automaatselt märgitud ja seda ei saa muuta. See tagab, et teave kopeeritakse hankija arvelt ja rakendatakse ostu tagastustellimuse päisele. See on kasulik, kuna aitab tagada, et ostu tagastustellimus tasakaalustab arve, kasutades sarnaseid tingimusi.  
8. Ahendage jaotist **Parameetrid**.
9. Laiendage jaotist **Arved**. Leht on avatud toimingust Kreeditarve, seega on ainus võimalik valik kopeerida andmed hankija arvetelt. Sellel vahekaardil on näidatud kõik hankija konto olemasolevad arved, mis on eelnevalt koostatud ostu tagastustellimusel nimetatud.   Arved tuvastatakse arve kande või ostutellimuse ID-de alusel.
10. Otsige üles hankija arve, mis on tähistatud numbriga AP-0006, ja tõstke see rida esile, klõpsates sellel real suvalist välja.
11. Valige rida, klõpsates rea märkeruutu. Pange tähele, et sellel hankija arvel olevad read valitakse automaatselt koos tellimusega. Sellel konkreetsel hankija arvel on 2 tellimuse rida. Selles näites tagastame osa kogusest teiselt realt.
12. Tõstke esile teine rida (see, millel on kaup M0006), klõpsates sellel real olevat suvalist välja.
13. Määrake väljal **Kogus** koguseks 10. See on kogus, mille hankijale tagastame. 
14. Tõstke esile esimene rida (see, millel on kaup M0005), klõpsates sellel real olevat suvalist välja.
15. Tühjendage selle rea märkeruut. Teie tellimusele kopeeritakse ainult teie valitud read.
16. Ahendage jaotist **Arved**.
17. Laiendage jaotist **Valitud read või päis kopeerimiseks**. Selles vaates kuvatakse kokkuvõte kõigist dokumentidest ja ridadest, mille olete oma tellimusele kopeerimiseks valinud.  
18. Ahendage jaotist **Valitud read või päis kopeerimiseks**.
19. Klõpsake valikut **OK**. Valitud rida on nüüd kopeeritud teie ostu tagastustellimusele. **Koguse** väljal on väärtus -10.   
20. Klõpsake jaotises **Ostutellimuse rida** valikut **Varud**.
21. Klõpsake valikut **Märkimine**. Loodud tellimuse rida on märgitud hankija arvel oleva laokande suhtes. See tagab, et hankijale tagastatavad varud on samad, mis neilt varem saadud varud. On olukordi, kus märgistamist ei toimu, näiteks kui varud on juba märgitud kui Tarbitud või kui toode on selline, mille puhul märgistust ei kasutata.  

22. Klõpsake valikut **OK**.

## <a name="confirm-and-record-the-shipment-of-goods"></a>Kaupade saatmise kinnitamine ja registreerimine
1. Avage **Toimingud > Kinnita**.
2. Klõpsake **Tegevuspaanil** valikut **Vastuvõtt**.
3. Klõpsake valikut **Toote sissetulek**.
    - Seda lehte kasutatakse toote sissetuleku registreerimiseks ostutellimuste puhul ja kaupade hankijale tagastamise töötlemiseks. Negatiivse kogusega tellimuseread tähendavad, et kaubad tuleb hankijale tagastada, ja dokumenti, mille saab sellelt lehelt luua, saab kasutada selleks saatelehena.   
    - Valige väljalt **Kogus** selle näite puhul Tellitud kogus. See tagab, et saadetist töödeldakse terve tellitud koguse ulatuses, millega tellimuse read loodi.   
4. Sisestage väärtus väljale **Toote sissetulek**. Seda välja kasutatakse viite sisestamiseks, mida kasutatakse toote sissetuleku töölehe kandena.  
5. Klõpsake valikut **OK**. Kaup on nüüd ostu tagastustellimusel saadetuks registreeritud ja loodud on toote sissetuleku tööleht. Saate kasutada toimingut Toote sissetulek ostutellimuse juurde loodud töölehtede ülevaatamiseks, et näha, mis millal vastu võeti või tagastati.  

