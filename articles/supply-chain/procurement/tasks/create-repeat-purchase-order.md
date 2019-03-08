---
title: Korduva ostutellimuse loomine
description: See protseduur näitab, kuidas koostada korduvat ostutellimust, kopeerides read varasemast ostutellimuse dokumendist uuele või olemasolevale ostutellimusele.
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchCopying
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 74dcee8a614363cf1f1ebc71e3e39a14c59bb774
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "345877"
---
# <a name="create-a-repeat-purchase-order"></a>Korduva ostutellimuse loomine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas koostada korduvat ostutellimust, kopeerides read varasemast ostutellimuse dokumendist uuele või olemasolevale ostutellimusele. Korduvate tellimuste koostamiseks on kaks meetodit. Saate kasutada dokumendi tasandil saadaolevaid toiminguid tegumiribalt või kasutada rea üksikasjade toiminguid. Dokumendi tasandi toimingud on peamiselt mõeldud uue ostutellimuse loomiseks, lisades ridu ja päise andmeid teisest tellimusest, samas kui rea üksikasjade toiming on peamiselt mõeldud olemasolevale tellimusele ridade lisamiseks. Selles juhendis toodud näidet saab kasutada demoandmete ettevõtte USMF puhul. Seda ülesannet täidab üldjuhul ostuagent.


## <a name="create-a-new-repeat-purchase-order"></a>Uue korduva ostutellimuse loomine
1. Avage Hanked > Ostutellimused > Kõik ostutellimused.
    * Kõigepealt proovime võimalust kopeerida andmed uuele tellimusele.  
2. Klõpsake valikut Uus.
3. Sisestage väljale Hankija konto väärtus US-101.
4. Klõpsake nuppu OK.
5. Klõpsake tegumiribal valikut Ostutellimus.
6. Klõpsake valikut Kõikidelt.
    * See on leht, millelt saate olemasolevate tellimuste andmeid oma tellimusele kopeerida. Ridade kopeerimiseks on erinevaid võimalusi ja on erinevaid dokumente, millelt saate kopeerida. Vaatame kõigepealt ridade kopeerimise võimalusi.   
7. Laiendage jaotis Parameetrid.
    * Väli Kogusetegur on abiks, kui teil on vaja kasutada kogust, mis erineb tellimuse omast, millelt kopeerite. Näiteks kui soovite tellida kopeeritavate ridade kahekordse koguse, tuleks sisestada sellele väljale 2 ja seejärel lisab süsteem read, kus algne kogus on kahekordistatud.  
    * Väli Muuda märki toetab samuti tellitud koguse muutmist, muutes lisatavate tellimuseridade märki. Sellest võib olla abi, kui teil on vaja kanne tühistada, luues kande jaoks negatiivsed tellimuse read. See valik tehakse automaatselt lehe avamisel toimingust Loo kreeditarve.  
    * Valik Kopeeri tasud võimaldab kopeerida tasud uuele tellimusele dokumendist, millest tellimuse read kopeerite.  
    * Valik Arvuta hinnad ümber kasutab kehtivaid hindu ja allahindlusi, mitte ei kopeeri neid dokumendist, kust muid andmeid kopeerite.  
    * Valik Kopeeri täpselt loob tellimuse dokumendi päise ja ridade kõigil väljadel olevate väärtuste täpse koopia. Kui seda pole valitud, kasutatakse paljudel hankijat ja tooteid puudutavatel väljadel vaikeväärtusi, täpselt nii, nagu uue tellimuse käsitsi koostamisel. Näiteks kui tellimus, millelt kopeerite, oleks tühistanud hankija vaike-arvekonto, kopeeritaks seesama arvekonto teie tellimusele. Kui te ei teeks valikut Kopeeri täpselt, kasutataks selle asemel teie tellimusel hankija vaike-arvekontot.  
    * Valik Kustuta osturead kustutab enne uute ridade rakendamist kõik ostutellimuse read, mis on juba kopeeritaval ostutellimusel olemas. Kasutage seda valikut ettevaatlikult, kuna see kustutab kõik olemasolevad read hoiatamata.  
    * Kui kasutate valikut Kopeeri tellimuse päis, ei ole vaja uuel tellimusel päise teavet käsitsi luua. Pange tähele, et selle valiku tulemusena kasutatakse hankijaga seotud väljadel vaikeväärtusi. Kui dokumendil, millelt kopeerite, on mitte-vaikeväärtusi, mida soovite kopeerida, kasutage samuti valikut Kopeeri täpselt.  
8. Ahendage jaotist Parameetrid.
    * On erinevaid dokumendiallikaid, millelt saate kopeerida, ja igaühel neist on sellel lehel eraldi jaotis. Näiteks jaotises Ostutellimused saab kopeerida olemasolevatelt ostutellimustelt.  
9. Klõpsake ostutellimuse rida, mille ID on 00015. 
10. Valige rida, klõpsates märkeruutu.
11. Tühjendage rea märkeruut, et seda teie tellimusele ei kopeeritaks.
    * Nüüd on valitud 4 rida teie ostutellimusele kopeerimiseks. Võimalik on valida ka täiendavaid ostutellimuse ridu teistelt ostutellimustelt ja kopeerida ka neid teie tellimusele. Samuti on võimalik lisada ridu teistsugustelt ostudokumentidelt. Järgmised sammud annavad valikutest ülevaate.  
12. Ahendage jaotist Ostutellimused.
13. Laiendage jaotist Kinnitamine.
    * Siin saate valida ostutellimuse kinnitusi, millelt kopeerida. Ostutellimuse kinnitused tuvastatakse seotud ostutöölehe ID või ostutellimuse ID alusel.  
14. Ahendage jaotist Kinnitamine.
15. Laiendage jaotist Toote sissetulekud.
    * Siin saate valida toote sissetuleku töölehti, millelt kopeerida. Toote sissetuleku töölehed tuvastatakse toote sissetuleku kande või ostutellimuse ID alusel.   
16. Ahendage jaotist Toote sissetulekud.
17. Laiendage jaotist Arved.
    * Siin saate valida hankija arveid, millelt kopeerida. Arved tuvastatakse arve kande või ostutellimuse ID alusel.   
18. Ahendage jaotist Arved.
19. Laiendage jaotist Valitud read või päis kopeerimiseks.
    * Selles vaates kuvatakse kokkuvõte kõigist dokumentidest ja ridadest, mis on teie tellimusele kopeerimiseks valitud.   
20. Ahendage jaotist Valitud read või päis kopeerimiseks.
21. Klõpsake nuppu OK.
    * Valitud 4 rida on kopeeritud teie uuele ostutellimusele.   

## <a name="copy-lines-to-an-existing-purchase-order"></a>Ridade kopeerimine olemasolevale ostutellimusele
    * Kogu tellimuse kopeerimise asemel luuakse sagedamini uus ostutellimus, täidetakse ostutellimuse päise andmed ja kopeeritakse siis eraldi read olemasolevatest tellimustest.  
1. Klõpsake suvandit Ostutellimuse rida.
2. Klõpsake valikut Kõikidelt.
    * Avanev leht on identne eelnevalt näidatud lehega, kuid kui see tellimuse ridade vaatest avatakse, märgitakse erinevad valikud. Vaatame parameetrid üle.   
3. Laiendage jaotis Parameetrid.
    * Valik Kustuta osturead pole märgitud. See tähendab, et saate kopeerida uued read oma tellimusele, olemasolevaid ridu eemaldamata.   
    * Valikut Kopeeri tellimuse päis pole samuti märgitud, kuna lisame tellimusele ainult ridu.   
4. Ahendage jaotist Parameetrid.
    * Selles näites kopeerime read olemasolevalt ostutellimuselt.   
5. Klõpsake ostutellimuse rida, mille ID on 00034. 
6. Valige rida, klõpsates märkeruutu.
    * Pange tähele, et valitakse ka sellel ostutellimusel olev üks tellimuse rida.  
7. Klõpsake nuppu OK.
    * Teie ostutellimusele on lisatud tellimuse rida.  

