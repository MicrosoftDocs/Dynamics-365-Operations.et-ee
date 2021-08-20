---
title: Tagastuse hind ja tagastuspartii ID
description: Võib-olla soovite, et tagastatud toodete kulu oleks võrdne toodete kuluga ajal, kui tooted kliendile müüsite. Seda saate määrata valikuga **Tagastatud partii ID**.
author: ShylaThompson
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnInventTransIdLookup, ReturnItemNumLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d65d641cca1bf681dc84b8faaa9292b5a98a7221fd453351228a94671f75ad62
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776796"
---
# <a name="return-cost-price-and-return-lot-id"></a>Tagastuse hind ja tagastuspartii ID        

[!include [banner](../includes/banner.md)]



Varudesse tagastatavate toodete kulu arvutatakse, kasutades toodete praegust kulu. Kuid võib-olla soovite, et tagastatud toodete kulu oleks võrdne toodete kuluga ajal, kui tooted kliendile müüsite. Selleks võite kasutada välja **Tagastatud partii ID** kiirkaardil **Rea üksikasjad** vormis **Müügitellimus**.

Vaadake näiteks järgmist stsenaariumi. Saadate kliendile arve. Seejärel tagastab klient teile tarnitud tooted. Teie tagastate tooted lattu. Kliendile tagastatud toodete eest tagastatava makse korral arvutatakse toodete kulu, kasutades toodete praegust kulu. Kui kui kasutate välja **Tagastuse partii ID**, arvutatakse tagastatud toodete kulu, kasutades algsel müügil kliendile esitatud arvel olevat kulu.

Muu kui praeguse kulu kasutamiseks tagasimaksete tegemiseks kliendile toimige järgmiselt.

## <a name="method-1-manually-enter-the-return-cost-price"></a>Meetod 1: sisestage käsitsi tagastuse omahind

Kui lisate tagastustellimusse kauba, tagastatakse kaubad lattu vaikimisi praeguse omahinnaga. Muu tagastuse omahinna määramiseks tehke järgmist.

1.  Klõpsake valikuid **Müük ja turundus** \> **Üldine** \> **Tagastustellimused** \> **Kõik tagastustellimused**.

2.  Klõpsake **Toimingupaanil** grupis **Uus** valikut **Tagastustellimus**.

3.  Valige vormis **Tagastustellimuse loomine** kliendikonto ja seejärel klõpsake nuppu **OK**.

4.  Valige vormil **Tagastustellimus – RMA number: %1, %2** kaup ja sisestage väljale **Kogus** negatiivne kogus.

5.  Klõpsake kiirkaarti **Rea üksikasjad**.

6.  Vahekaardil **Üldine** sisestage väärtus välja **Tagastuse omahind**. Seda väärtust kasutatakse kaupade tagastamisel lattu. Kui te väärtust ei sisesta, kasutatakse kaupade tagastamisel lattu praegust omahinda.

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a>Meetod 2: looge automaatselt omahind kliendiarve rea põhjal

See on tagastusridade loomisel eelistatud meetod. Selleks et kasutada toodete kulu, mis kehtis toodete müümisel kliendile, looge tagastustellimus ja määrake tagastusele müügirida.

1.  Klõpsake valikuid **Müük ja turundus** \> **Üldine** \> **Tagastustellimused** \> **Kõik tagastustellimused**.

2.  Klõpsake **Toimingupaanil** grupis **Uus** valikut **Tagastustellimus**.

3.  Valige vormis **Tagastustellimuse loomine** kliendikonto ja seejärel klõpsake nuppu **OK**.

4.  Klõpsake vormil **Tagastustellimus – RMA number: %1, %2** **Toimingupaanil** suvandit **Otsi müügitellimust**.

5.  Valige vormis **Otsi müügitellimust** tagastatav arverida ja klõpsake nuppu **OK**.
    
    Kiirkaardil **Rea üksikasjad** vahekaardil **Üldine** väljas **Tagastuse partii ID** kuvatakse väärtus algselt müügirealt. Peale selle kuvab väli **Tagastuse omahind** omahinna algselt müügirealt.

## <a name="cost-calculation-example"></a>Kulu kalkulatsiooni näide

Kui kasutate välja **Tagastuse partii ID** tagastustellimuse real tagastuse omahinna määramiseks, kasutatakse kulu tagastustellimuse real. Kui kasutate lao sulgemise või ümberarvutuse funktsiooni, kohandatakse kulu algsel müügireal. Kulu tagastustellimuse real kohandatakse automaatselt, et see kajastaks sama kulu tüki kohta.

1.  Looge ja väljastage toode nimega Test. Sisestage vormi **Väljastatud toote üksikasjad** järgmine teave.
    
    1.  Kiirkaardil **Kulude haldamine** väljas **Kaubagrupp** valige grupp **Osad**.
    
    2.  Kiirkaardi **Üldine** väljal **Kauba mudeligrupp** valige suvand **DEF**.
    
    3.  Kiirkaardil **Ost** välja **Hind** sisestage kauba omahinnaks 10.00.
    
    4.  Klõpsake **toimingupaanil** valikut **Dimensioonigrupid**. Valige väljas **Laoala dimensiooni grupp** suvand **Ainult tegevuskoht ja ladu**. Valige väljas **Jälgimisdimensiooni grupp** suvand **Aktiivne jälgimisdimensioon puudub**.

2.  Looge 10 katsekaubale ostutellimus hinnaga 6.00 tüki kohta ja sisestage arve ostutellimuse jaoks.
    
    Looge 10 katsekaubale teine ostutellimus hinnaga 8.00 tüki kohta ja sisestage arve ostutellimuse jaoks.

3.  Sisestage arve müügitellimusele, et müüa viis katsekaupa.
    
    Sel juhul määratakse müügitellimusele reale kulu väärtus 35.00 (5 tükki \* keskmine kulu 7.00 tüki kohta).

4.  Looge kliendile tagastustellimus. Valige vormis **Otsi müügitellimust** arverida ja klõpsake nuppu **OK**.

5.  Kontrollige vormis **Tagastustellimus – RMA number: %1, %2**, kas tagastustellimus on loodud katsekauba tagastamiseks. Tagastustellimuse koguseks on määratud –5.00.
    
    Väljas **Tagastuse partii ID** kuvatakse partii ID. See partii ID võetakse kliendile müüdud kauba algsest müügitellimusest. Väli **Tagastuse omahind** kuvab omahinna algselt müügirealt.

6.  Registreerige tagastatud kauba sissetulek.

7.  Sisestage tagastatud kaupadele saateleht.

8.  Sisestage tagastustellimusele arve. Valige loendilehelt **Kõik müügitellimused** müügitellimus, mille puhul tellimuse tüüp on **Tagastatud tellimus**.

9.  Avage vorm **Laokanded**. Kontrollige, kas tagastusel on arvutatud kulu 7.00 tüki kohta, kasutades väärtust väljas **Tagastuse omahind**, väljas **Omahind** on kogukulu 35.00. Vormi **Laokanded** saate avada vormilt **Tagastustellimus – RMA number: %1, %2**. Klõpsake ruudustikul **Read** valikuid **Varud** \> **Kanded**.

10. Kasutage varude ja laohalduses vormi **Sulgemine ja korrigeerimine**, et käivitada protseduur **3. Sulgemine**.
    
    See toiming kohandab algse müügirea kulu, mis arvutati väärtuselt –35.00 (5 tükki \* 7.00) väärtusele –30.00 (5 tükki \* 6.00). See on seepärast, et laomudeligrupp kasutab elavjärjekorra mudelit (FIFO) ja 6.00 tüki kohta FIFO kulu esimesest ostutellimusest. Peale selle kohandab toiming tagastusmüügi rea kulu, et see ühtiks kuluga tüki kohta algsel müügireal. Seega kohandatakse tagastusrea kulu väärtuselt 35.00 väärtusele 30.00.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]