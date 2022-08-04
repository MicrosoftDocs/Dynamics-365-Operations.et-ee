---
title: Andmevaka lähtestamise KKK
description: See artikkel annab vastused korduma kippuvatele küsimustele data marti lähtestamise kohta.
author: jinniew
ms.date: 03/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.search.form: ''
ms.openlocfilehash: 6cb418c331f0ad260f0c370b87404028e5a953f1
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/28/2022
ms.locfileid: "9205822"
---
# <a name="data-mart-resets-faq"></a>Andmevaka lähtestamise KKK

See artikkel annab vastused korduma kippuvatele küsimustele data marti lähtestamise kohta. Andmevaka lähtestamine võib olla aeganõudev protsess ja olenevalt olukorrast ei pruugi see olla vajalik lahendus. Seetõttu sisaldab see artikkel teavet olukorra kohta, kus data marti lähtestamine võib aidata ning ka olukordi, kus see ei suuda aidata.

## <a name="what-is-a-data-mart-reset"></a>Millal lähtestada andmevakka?

Andmevaka lähtestamine keelab integratsioonitoimingud, kustutab kõik andmevaka andmed ja lubab seejärel integreeruda uuesti.

Kindlustamaks, et vanu andmeid ei lisata, saab andmevakka lähtestada alles pärast olemasolevate ülesannete lõpuleviimist. Kui proovite lähtestada andmevakka enne kõigi ülesannete lõpetamist, võite saada sõnumi, näiteks: "Andmevaka lähtestamist ei saanud aktiivse ülesande tõttu töödelda. Proovige hiljem uuesti.”

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a>Millal tuleb andmevakk lähtestada?

Kui teie olukorras kehtib üks või mitu järgnevat lauset, võib teie organisatsioonile olla kasulik andmevaka lähtestamine.

- **Rakenduse andmebaas taastati**
- **Avasite tugipileti** – tugiinsener juhendas teid lähtestama data marti tõrkeotsingu etapi osana.
- **Suur protsent aegunud kirjeid –** aegunud kirjed ise ei pruugi andmete lähtestamist õigustada. Aegunud andmete kõrged protsendid võivad kogu aruande genereerimist ja integratsiooni jõudlust alandada ning hõivata andmebaasi ruumi lisakasutust. Kui data marti andmetes on rohkem kui 80% aegunud andmeid, on soovitatav viia andmete lähtestamine lõpule.
 
> [!NOTE]
> Andmebaasi lähtestamise protsessi mõjutab teie pearaamatu ja eelarvetehingute arv teie andmebaasis. Sõltuvalt teie süsteemis olevate tehingute arvust saab andmesidet lähtestada nii vähe kui 15 minutit või see võib võtta kuni neli tundi. Kui lähtestamine kestab aga üle nelja tunni, on soovitatav võtta ühendust tugiteenustega.
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a>Millal on sobilik andmevakka lähtestada?

Siin on mõned olukorrad, kus me ei soovita andmevakka lähtestada.

- Teil esineb andmete integreerimise jõudlusprobleeme.
- Teie finants aru reporteri integreerimine pole lubatud. 

    - See tähendab, et pearaamatu andmeid ei sünkroonita enam teie finantsaruandluse andmekooslusega. Võimalik, et teie finants aru anda teie finantsaruannete jaoks ei pruugi teie finants aru anda ajaja numbreid. See juhtub tavaliselt siis, kui te pole finantsreporterit kaua kasutada.
    - Teil palutakse integratsioon lubada, lähtestades data marti. Jätkamiseks valige **Jah**. Võite valida ka andmete marti hilisema lähtestamise. Kui integratsioon on lubatud, sünkroonitakse teie pearaamatu andmed uuesti Finantsaruandes. 
- Teil on mõne järgmise põhjuse tõttu korduv lähtestamise muster.

    - **Aruandes puuduvad või ootamatud andmed** – kui teate, et andmed puuduvad, avage tugipilet Microsoftiga, et vaadata üle oma aruande vorming ja võimalikud andmete sünkroonimise probleemid.
    - **Kinnise integratsiooni** olek – kui märkate, et integratsiooni olek on käivitatud, võib selle põhjuseks olla suur kannete hulk süsteemis. See olek lahendab enda. Kui aga teate, et intregratsiooni olek on kleebitud rohkem kui neljaks tunniks, avage Microsofti tugipilet. 
   
## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Kui lähtestan andmed marti, kas kaotan aruanded, mis ma juba kujundanud olen?

Ei. Teie aruandeid talletatakse SQL-tabelites, mida ei mõjuta andmevaka lähtestamine. Kui olete mures mõne loodud aruande kaotamise pärast, saate varundada kujundused, mida te ei soovi kaotada. Kujunduste varundamiseks avage aruandekujundaja ja minge **Ettevõtte \> Ettevõtted \> Koosteüksused \> Eksport**.
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a>Kas kõik kasutajad peavad süsteemist väljuma, enne kui ma andmevakka lähtestan?

Ei. Kasutajad saavad andmevaka lähtestamise ajal süsteemiga tööd jätkata. Kuid enne lähtestamise lõppu ei pääse kasutajad juurde aruannetele, mis on loodud Financial Reporter abil.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
