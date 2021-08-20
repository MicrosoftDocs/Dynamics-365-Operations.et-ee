---
title: Andmevaka lähtestamise KKK
description: Selles teemas antakse vastused mõnele korduma kippuvatele küsimustele andmevaka lähtestamise kohta.
author: jinniew
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e5a40342306eb9888b456a865ab2220dccfe65f8ccecc67bf8fc16f907e06977
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767751"
---
# <a name="data-mart-resets-faq"></a>Andmevaka lähtestamise KKK

Selles teemas antakse vastused mõnele korduma kippuvatele küsimustele andmevaka lähtestamise kohta. Andmevaka lähtestamine võib olla aeganõudev protsess ja olenevalt olukorrast ei pruugi see olla vajalik lahendus. Seetõttu sisaldab see teema teavet olukorrast, kus andmevaka lähtestamine võib aidata ning ka olukordi, kus ei saa.

## <a name="what-is-a-data-mart-reset"></a>Millal lähtestada andmevakka?

Andmevaka lähtestamine keelab integratsioonitoimingud, kustutab kõik andmevaka andmed ja lubab seejärel integreeruda uuesti.

Kindlustamaks, et vanu andmeid ei lisata, saab andmevakka lähtestada alles pärast olemasolevate ülesannete lõpuleviimist. Kui proovite lähtestada andmevakka enne kõigi ülesannete lõpetamist, võite saada sõnumi, näiteks: "Andmevaka lähtestamist ei saanud aktiivse ülesande tõttu töödelda. Proovige hiljem uuesti.”

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a>Millal tuleb andmevakk lähtestada?

Kui teie olukorras kehtib üks või mitu järgnevat lauset, võib teie organisatsioonile olla kasulik andmevaka lähtestamine.

- Rakenduse andmebaas taastati.
- Olete avanud tugipileti ja tugiinsener juhendas teid lähtestama andmevaka tõrkeotsingu sammu osana.
 
> [!NOTE]
> Andmebaasi lähtestamise protsessi mõjutab teie pearaamatu ja eelarvetehingute arv teie andmebaasis. Sõltuvalt teie süsteemis olevate tehingute arvust saab andmesidet lähtestada nii vähe kui 15 minutit või see võib võtta kuni neli tundi. Kui lähtestamine kestab aga üle nelja tunni, on soovitatav võtta ühendust tugiteenustega.
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a>Millal on sobilik andmevakka lähtestada?

Siin on mõned olukorrad, kus me ei soovita andmevakka lähtestada.

- Teil esineb andmete sünkroonimisega seotud jõudlusprobleeme.
- Teil on mõne järgmise põhjuse tõttu korduv lähtestamise muster.

    - **Puuduvad andmed** – kui märkate, et andmed puuduvad, avage koos Microsoftiga tugipilet, et vaadata üle teie aruande vorming ja võimalikud andmete sünkroonimise probleemid.
    - **Kinnise integratsiooni olek**
    - **Aegunud kirjed** – aegunud kirjed ei pruugi andmevaka lähtestamist alati õigustada. Kui teil on suur andmekomplekt, võtab lähtestamisprotsess aega, kuid tõenäoliselt ei vii see täiustamiseni.

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Kui lähtestan andmed marti, kas kaotan aruanded, mis ma juba kujundanud olen?

Ei. Teie aruandeid talletatakse SQL-tabelites, mida ei mõjuta andmevaka lähtestamine. Kui olete mures mõne loodud aruande kaotamise pärast, saate varundada kujundused, mida te ei soovi kaotada. Kujunduste varundamiseks avage aruandekujundaja ja minge **Ettevõtte \> Ettevõtted \> Koosteüksused \> Eksport**.
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a>Kas kõik kasutajad peavad süsteemist väljuma, enne kui ma andmevakka lähtestan?

Ei. Kasutajad saavad andmevaka lähtestamise ajal süsteemiga tööd jätkata. Kuid enne lähtestamise lõppu ei pääse kasutajad juurde aruannetele, mis on loodud Financial Reporter abil.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
