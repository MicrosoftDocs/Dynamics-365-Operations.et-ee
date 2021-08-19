---
title: Korduva ostutellimuse loomine
description: Selles teemas näidatakse, kuidas luua korduvat ostutellimust, kopeerides read varasemast ostutellimust dokumendist uude ostutellimusse või olemasolevasse ostutellimusse.
author: kamaybac
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, PurchCopying
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b75d8414e40d65267494eb495bf99daa62b3e2d5850db27ecae99f30d543c870
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719595"
---
# <a name="create-a-repeat-purchase-order"></a>Korduva ostutellimuse loomine

[!include [banner](../../includes/banner.md)]

Selles teemas näidatakse, kuidas luua korduvat ostutellimust, kopeerides read varasemast ostutellimust dokumendist uude ostutellimusse või olemasolevasse ostutellimusse. Korduvate tellimuste koostamiseks on kaks meetodit. Saate kasutada dokumendi tasandil saadaolevaid toiminguid tegumiribalt või kasutada rea üksikasjade toiminguid. Dokumendi tasandi toimingud on peamiselt mõeldud uue ostutellimuse loomiseks, lisades ridu ja päise andmeid teisest tellimusest, samas kui rea üksikasjade toiming on peamiselt mõeldud olemasolevale tellimusele ridade lisamiseks. Selles juhendis toodud näidet saab kasutada demoandmete ettevõtte USMF puhul. Seda ülesannet täidab üldjuhul ostuagent.


## <a name="create-a-new-repeat-purchase-order"></a>Uue korduva ostutellimuse loomine
1. Avage navigeerimispaanil **Moodulid > Hange > Ostutellimused > Kõik ostutellimused**. Kõigepealt proovime võimalust kopeerida andmed uuele tellimusele.  
2. Valige suvand **Uus**.
3. Väljale **Tarnija konto** sisestage `US-101`.
4. Valige nupp **OK**.
5. Toimingupaanil valige **Ostutellimus**.
6. Valige **Kõigilt**. See on leht, millelt saate olemasolevate tellimuste andmeid oma tellimusele kopeerida. Ridade kopeerimiseks on erinevaid võimalusi ja on erinevaid dokumente, millelt saate kopeerida. Vaatame kõigepealt ridade kopeerimise võimalusi. 
7. Laiendage jaotist **Parameetrid**.

    - Väli **Kogusetegur** on kasulik, kui soovite kasutada kogust, mis erineb kogusest, mis on tellimuses, millest te kopeerite. Näiteks kui soovite tellida kopeeritavate ridade kahekordse koguse, tuleks sisestada sellele väljale „2” ja seejärel lisab süsteem read, kus algne kogus on kahekordistatud.  
    - Väli **Muuda märki** toetab samuti tellitud koguse muutmist, muutes lisatud tellimuseridade koguse märki. Sellest võib olla abi, kui teil on vaja kanne tühistada, luues kande jaoks negatiivsed tellimuse read. See suvand on automaatselt valitud, kui leht avatakse toimingust **Loo kreediti märge**.  
    - Suvand **Kopeeri tasud** lubab teil kopeerida tasud oma uude tellimusse dokumendist, millest kopeerite tellimuseridu.  
    - Suvand **Arvuta hinnad uuesti** kasutab praeguseid hindu ja allahindlusi, mitte ei kopeeri neid dokumendist, millest muud teavet kopeerite.  
    - Suvand **Kopeeri täpselt** loob täpse koopia kõigi väljade väärtustest tellimuse dokumendi päisest ja ridadelt. Kui seda pole valitud, kasutatakse paljudel hankijat ja tooteid puudutavatel väljadel vaikeväärtusi, täpselt nii, nagu uue tellimuse käsitsi koostamisel. Näiteks kui tellimus, millelt kopeerite, oleks tühistanud hankija vaike-arvekonto, kopeeritaks seesama arvekonto teie tellimusele. Kui te ei valinud suvandit **Kopeeri täpselt**, kasutatakse selle asemel vaike-arvekontot, mida hankija teie tellimuses kasutaks.  
    - Suvand **Kustuta osturead** kustutab enne uute ridade lisamist kõik ostutellimuse read, mis on juba kopeeritavas ostutellimuses olemas. Kasutage seda valikut ettevaatlikult, kuna see kustutab kõik olemasolevad read hoiatamata.  
    - Kui kasutate suvandit **Kopeeri tellimuse päis**, ei pea te oma uue tellimuse jaoks käsitsi looma päise teavet. Pange tähele, et selle valiku tulemusena kasutatakse hankijaga seotud väljadel vaikeväärtusi. Kui dokumendil, millest te kopeerite, on vaikesättest erinevad väärtused, mida soovite kopeerida, kasutage samuti suvandit **Kopeeri täpselt**.   
    - On erinevaid dokumendiallikaid, millelt saate kopeerida, ja igaühel neist on sellel lehel eraldi jaotis. Näiteks jaotis **Ostutellimused** lubab teil kopeerida olemasolevatest ostutellimustest.  

8. Jaotises **Ostutellimused** valige read, mida soovite kopeerida oma lõikelauale. Võimalik on valida ka täiendavaid ostutellimuse ridu teistelt ostutellimustelt ja kopeerida ka neid teie tellimusele. Samuti on võimalik lisada ridu teistsugustelt ostudokumentidelt. Järgmised sammud annavad valikutest ülevaate.  
9. Laiendage jaotist **Kinnitus**. Siin saate valida ostutellimuse kinnitusi, millelt kopeerida. Ostutellimuse kinnitused tuvastatakse seotud ostutöölehe ID või ostutellimuse ID alusel.  
10. Laiendage jaotist **Toote sissetulekud**. Siin saate valida toote sissetuleku töölehti, millelt kopeerida. Toote sissetuleku töölehed tuvastatakse toote sissetuleku kande või ostutellimuse ID alusel.   
11. Laiendage jaotist **Arved**. Siin saate valida hankija arveid, millelt kopeerida. Arved tuvastatakse arve kande või ostutellimuse ID alusel.   
12. Laiendage jaotist **Valitud read või päis kopeerimiseks**. Selles vaates kuvatakse kokkuvõte kõigist dokumentidest ja ridadest, mis on teie tellimusele kopeerimiseks valitud.   
13. Valige nupp **OK**. Valitud read on kopeeritud teie uude ostutellimusse.   

## <a name="copy-lines-to-an-existing-purchase-order"></a>Ridade kopeerimine olemasolevale ostutellimusele  

Kogu tellimuse kopeerimise asemel luuakse sagedamini uus ostutellimus, täidetakse ostutellimuse päise andmed ja kopeeritakse siis eraldi read olemasolevatest tellimustest.  

1. Valige rida **Ostutellimus**.
2. Valige **Kõigilt**. Avanev leht on identne eelnevalt näidatud lehega, kuid kui see tellimuse ridade vaatest avatakse, märgitakse erinevad valikud. Vaatame parameetrid üle.   
3. Laiendage jaotist **Parameetrid**.

    - Suvand **Kustuta osturead** ei ole valitud. See tähendab, et saate kopeerida uued read oma tellimusele, olemasolevaid ridu eemaldamata.   
    - Suvand **Kopeeri tellimuse päis** ei ole samuti valitud, kuna lisame tellimusele ainult täiendavaid ridu.   
    - Selles näites kopeerime read olemasolevalt ostutellimuselt.   

4. Valige rida soovitud ostutellimuse jaoks. Pange tähele, et valitakse ka sellel ostutellimusel olev üks tellimuse rida.  
5. Valige nupp **OK**. Teie ostutellimusele on lisatud tellimuse rida.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]