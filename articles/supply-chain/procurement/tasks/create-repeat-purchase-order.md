---
title: Korduva ostutellimuse loomine
description: See artikkel näitab, kuidas luua korduvat ostutellimust (PO), kopeerides ridu varasema ostutellimuse dokumendist uude ostutellimusesse või olemasolevasse ostutellimusse.
author: GalynaFedorova
ms.date: 09/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, PurchCopying
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 335461d60fa0bc92e9711806c6e42643a3f75d02
ms.sourcegitcommit: 073604c07116e0a87f78ab2c76cb89ae83ebba3c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/30/2022
ms.locfileid: "9608102"
---
# <a name="create-a-repeat-purchase-order"></a>Korduva ostutellimuse loomine

[!include [banner](../../includes/banner.md)]

See artikkel näitab, kuidas luua korduvat ostutellimust (PO), kopeerides ridu varasema ostutellimuse dokumendist uude ostutellimusesse või olemasolevasse ostutellimusse. Korduvate tellimuste koostamiseks on kaks meetodit. Saate kasutada dokumendi tasandil saadaolevaid toiminguid tegumiribalt või kasutada rea üksikasjade toiminguid. Dokumenditaseme tegevused on mõeldud uue ostutellimuse loomiseks, lisades teise tellimuse read ja päise teabe, samal ajal kui rea üksikasjade tegevus on peamiselt ridade lisamiseks olemasolevale tellimusele. Selles juhendis toodud näidet saab kasutada demoandmete ettevõtte USMF puhul. Seda ülesannet täidab üldjuhul ostuagent.

## <a name="create-a-new-repeat-purchase-order"></a>Uue korduva ostutellimuse loomine

1. Navigeerimispaanil minge moodulitesse **\> Hanked ja hanked \> Kõik \> ostutellimused**. Kõigepealt proovime võimalust kopeerida andmed uuele tellimusele.  
1. Valige suvand **Uus**.
1. Väljale **Tarnija konto** sisestage `US-101`.
1. Valige nupp **OK**.
1. Tegevuspaanil avage vahekaart Ostutellimus **ja valige grupist** **Kopeeri suvand** Kõigilt **.** Avaneb **dialoogiaken Kopeeri teistest** dokumentidest. Siit saate kopeerida olemasolevatelt tellimustelt oma tellimusse. Ridade kopeerimiseks on erinevaid võimalusi ja on erinevaid dokumente, millelt saate kopeerida. Vaatame kõigepealt ridade kopeerimise võimalusi.
1. Laiendage **kiirkaarti** Parameetrid.

    - Väli **Kogusetegur** on kasulik, kui soovite kasutada kogust, mis erineb kogusest, mis on tellimuses, millest te kopeerite. Näiteks kui soovite tellida kopeeritavate ridade kahekordse koguse, tuleks sisestada sellele väljale „2” ja seejärel lisab süsteem read, kus algne kogus on kahekordistatud.  
    - Väli **Muuda märki** toetab samuti tellitud koguse muutmist, muutes lisatud tellimuseridade koguse märki. Sellest võib olla abi, kui teil on vaja kanne tühistada, luues kande jaoks negatiivsed tellimuse read. See suvand on automaatselt valitud, kui leht avatakse toimingust **Loo kreediti märge**.  
    - Suvand **Kopeeri tasud** lubab teil kopeerida tasud oma uude tellimusse dokumendist, millest kopeerite tellimuseridu.  
    - Suvand **Arvuta hinnad uuesti** kasutab praeguseid hindu ja allahindlusi, mitte ei kopeeri neid dokumendist, millest muud teavet kopeerite.  
    - Valik **Kopeeri kopeerib** täpselt mitme välja väärtused tellimuse päises ja ridadel. Kui seda valikut ei valita, kasutatakse vaikeväärtusi paljude hankija ja toodetega seotud väljade puhul, näiteks uue tellimuse käsitsi loomisel. Näiteks kui seadistate väärtuseKs Kopeeri täpselt Jah ja kopeerite tellimuse, **·** *mis* alistab hankija vaikearvekonto, kopeeritakse see sama arvekonto teie uude tellimusse. Kui määrate **väärtuseks** Kopeeri *täpselt* Ei, kasutatakse selle asemel hankija vaikearvekontot teie uue tellimuse puhul. Järgmiste väljade väärtused kopeeritakse, kui kopeerimise väärtuseks **on** täpselt määratud *Jah*:
        - Keel
        - Maksetingimused
        - Makseviis
        - Makse täpsustus
        - Numbriseeria grupp
        - Sularahakonto
        - Allahindlusprotsent
        - Valuuta
        - Tarnetingimused
        - Tarneviis
        - Dimensioon
        - Käibemaksugrupp
        - Alista käibemaks
        - Hinnad sisaldavad käibemaksu
        - Transport
        - Sadam
        - Statistikatoimingud
        - Malli ID
        - Tarne nimi
        - Postiaadress
        - Viide
        - Viitetabeli kood
    - Suvand **Kustuta osturead** kustutab enne uute ridade lisamist kõik ostutellimuse read, mis on juba kopeeritavas ostutellimuses olemas. Kasutage seda valikut ettevaatlikult, kuna see kustutab kõik olemasolevad read hoiatamata.  
    - Kui kasutate suvandit **Kopeeri tellimuse päis**, ei pea te oma uue tellimuse jaoks käsitsi looma päise teavet. Selle valiku tulemuseks on, et hankijaga seotud väljadel kasutatakse vaikeväärtusi. Kui dokumendil, millest te kopeerite, on vaikesättest erinevad väärtused, mida soovite kopeerida, kasutage samuti suvandit **Kopeeri täpselt**.
    - On erinevaid dokumendiallikaid, millelt saate kopeerida, ja igaühel neist on sellel lehel eraldi jaotis. Näiteks jaotis **Ostutellimused** lubab teil kopeerida olemasolevatest ostutellimustest.  

1. Jaotises **Ostutellimused** valige read, mida soovite kopeerida oma lõikelauale. Võimalik on valida ka täiendavaid ostutellimuse ridu teistelt ostutellimustelt ja kopeerida ka neid teie tellimusele. Samuti on võimalik lisada ridu teistsugustelt ostudokumentidelt. Järgmised sammud annavad valikutest ülevaate.  
1. Laiendage jaotist **Kinnitus**. Siin saate valida ostutellimuse kinnitusi, millelt kopeerida. Ostutellimuse kinnitused tuvastatakse seotud ostutöölehe ID või ostutellimuse ID alusel.  
1. Laiendage jaotist **Toote sissetulekud**. Siin saate valida toote sissetuleku töölehti, millelt kopeerida. Toote sissetuleku töölehed tuvastatakse toote sissetuleku kande või ostutellimuse ID alusel.
1. Laiendage jaotist **Arved**. Siin saate valida hankija arveid, millelt kopeerida. Arved tuvastatakse arve kande või ostutellimuse ID alusel.
1. Laiendage jaotist **Valitud read või päis kopeerimiseks**. Selles vaates kuvatakse kokkuvõte kõigist dokumentidest ja ridadest, mis on teie tellimusele kopeerimiseks valitud.
1. Valige nupp **OK**. Valitud read on kopeeritud teie uude ostutellimusse.

## <a name="copy-lines-to-an-existing-purchase-order"></a>Ridade kopeerimine olemasolevale ostutellimusele  

Kogu tellimuse kopeerimise asemel luuakse sagedamini uus ostutellimus, täidetakse ostutellimuse päise andmed ja kopeeritakse siis eraldi read olemasolevatest tellimustest.  

1. Valige rida **Ostutellimus**.
1. Valige **Kõigilt**. Avanev leht on identne eelnevalt näidatud lehega, kuid kui see tellimuse ridade vaatest avatakse, märgitakse erinevad valikud. Vaatame parameetrid üle.
1. Laiendage jaotist **Parameetrid**.

    - Suvand **Kustuta osturead** pole valitud. See tähendab, et saate kopeerida uued read oma tellimusele, olemasolevaid ridu eemaldamata.
    - Suvand **Kopeeri tellimuse päis** ei ole samuti valitud, kuna lisame tellimusele ainult täiendavaid ridu.
    - Selles näites kopeerime read olemasolevalt ostutellimuselt.

1. Valige rida soovitud ostutellimuse jaoks. Pange tähele, et valitakse ka sellel ostutellimusel olev üks tellimuse rida.  
1. Valige nupp **OK**. Teie ostutellimusele on lisatud tellimuse rida.  

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]