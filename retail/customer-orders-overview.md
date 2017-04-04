---
title: "Kliendi tellimuste ülevaade"
description: "See teema pakub teavet klientide tellimused ja jaemüük kaasaegne POS (MPOS). Klienditellimuste on ka eritellimused. Teema sisaldab arutelu seotud parameetrid ja tehingu."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 2f466dfe53ccf0be15ed0793b4a6dd371bdacc0d
ms.lasthandoff: 03/31/2017


---

# <a name="customer-orders-overview"></a>Kliendi tellimuste ülevaade

See teema pakub teavet klientide tellimused ja jaemüük kaasaegne POS (MPOS). Klienditellimuste on ka eritellimused. Teema sisaldab arutelu seotud parameetrid ja tehingu.

Omni channel retail maailmas, paljud jaemüüjad pakkuda võimalust kliendi tellimuste või eritellimuste eri toote ja täitmise nõuetele. Siin on mõned tüüpilised stsenaariumid:

-   Klient soovib tooted tarnitakse eraldi kindlal kuupäeval.
-   Klient tahab valida tooteid poest või erinevat poodi või asukoha, kui klient ostab neid tooteid.
-   Klient soovib keegi teine valida tooteid, mida klient osta.

Jaemüüjad kasutada klienditellimuste vähendada käibe mis varude katkestused võib muidu põhjustada, kuna kauba saab kätte või eri aeg või koht kätte.

## <a name="set-up-customer-orders"></a>Saate seadistada klientide tellimused
Siin on mõned parameetrid saab määrata selle **hulgi parameetrid** määratleda, kuidas klientide tellimused täidetakse lehekülg:

-   **Vaikimisi tagatisraha protsent** – määrata summa, mida klient peab tasuma tagatisraha enne tellimuse saab kinnitada. Vaikimisi hoiuse summa arvutatakse protsendina tellimuste väärtusest. Sõltuvalt privileegid, pruugi poest saate alistada summa abil **hoiuste alistada**.
-   **Tühistamise tasu protsent** -tasu rakendatakse, kui kliendi tellimus tühistatakse, kui selle maksu suuruse.
-   **Tühistamise kulukoodi** -kui tasu rakendatakse kui kliendi tellimus on tühistatud, et tasu kajastub maksu koodi müügitellimuse Microsoft Dynamics AX-i. Kasutage seda parameetrit tühistamise lisakulude kood.
-   **Shipping kulukoodi** – jaemüüjatele saab tasuta shipping kauba kliendile tasuline. Selle saatmine maksu summa kajastub maksu koodi müügitellimuse Dynamics AX-i. Selle parameetri abil saate vastendada shipping kulukoodi saatmiskulud kliendi tellimusel.
-   **Tagastab laevaliini kulud** – saate määrata, kas veokulud, mis on seotud kliendi tellimuse eest.
-   **Maksimaalne summa ilma** -kui shipping tasu tagastatakse maksimaalse suuruse shipping tasu toetuste üle tagastuskorraldused. Kui nimetatud summa ületatakse, manager alistamine on vajalik jätkata toetuse. Järgmistel juhtudel mahutamiseks laevandus tagasi saada võivad ületada algselt makstud summa:
    -   Tasu rakendatakse tasandil müügitellimuse päise ja kui mõned kogus tootesari tagastatakse, suurimat toetust saatmiskulud, lubatud toodete ja koguse kindlaks sobib kõikide jaeklientidele.
    -   Veokulud tekivad iga juhu puhul saatmine. Kui klient tagastab toodete mitu korda ja vahendaja poliitikaga määratakse, et vahendaja kannab kulud tagasi shipping tasude, tagasi shipping eest tuleb rohkem kui tegelik laevaliini kulud.

## <a name="transaction-flow-for-customer-orders"></a>Tehingu voolu klientide tellimused
### <a name="create-a-customer-order-in-retail-modern-pos"></a>Jaemüügi kaasaegne POS kliendi loomine

1.  Lisage kandesse klient.
2.  Lisage tooted ostukorvi.
3.  Klõpsake **luua kliendi**, ja seejärel valige tellimuse tüüp. Tellimuse tüüp võib olla kas **kliendi tellimuse** või **tsitaat**.
4.  Klõpsake **valitud laeva** või **laeva kõik** laeva tooted aadressile kliendikonto, määrata nõutud lähetuskuupäev ja määrake laevaliini kulud.
5.  Klõpsake **kiirenemist valitud** või **Pick-up kõik** valida tooteid, mis on kiirenenud praeguse poest või teisest poest kindlal kuupäeval.
6.  Kogu hoiusumma, kui nõutakse ettemaksu.

### <a name="edit-an-existing-customer-order"></a>Muuta olemasoleva kliendi tellimuse

1.  Kodulehekülg, klõpsake **leida tellimuse**.
2.  Leidke ja valige muudetav tellimus. Klõpsake lehe allosas on **muuta**.

### <a name="pick-up-an-order"></a>Tõstma tellimuse

1.  Kodulehekülg, klõpsake **leida tellimuse**.
2.  Valige tellimus kiirenemist. Klõpsake lehe allosas **komplekteerimise ja pakkimisega**.
3.  Klõpsake **valida**.

### <a name="cancel-an-order"></a>Tellimusest loobuda

1.  Kodulehekülg, klõpsake **leida tellimuse**.
2.  Valige tellimus tühistada. Klõpsake lehe allosas **tühistada**.

#### <a name="create-a-return-order"></a>Tagastustellimuse loomine

1.  Kodulehekülg, klõpsake **leida tellimuse**.
2.  Valige tellimus, tagasi, valige arve tellimuse ja valige kauba tagasi tootesari.
3.  Klõpsake lehe allosas on **tagastuskorraldusel**.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Asünkroonne tehingu voolu klientide tellimused
Klienditellimuste loomist Müügikoht (POS) kliendi punktist režiimis sünkroonse või asünkroonse režiimi.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Lubade kasutada klienditellimuste asünkroonse režiimi luua programmi

1.  Dynamics AX-is klõpsake **hulgi- ja kaubanduse**&gt;**kanali seaded**&gt;**POS seadistus**&gt;**POS profiili**&gt;**funktsioonid profiilid**.
2.  Kohta ning **üldise** FastTab, seada selle **luua kliendi selleks asünkroonse režiimi** võimalus **Jah**.

Kui on **luua kliendi selleks asünkroonse režiimi** määrangu **Jah**, klientide tellimused luuakse alati asünkroonse režiimi, isegi kui jaemüük tehingu (RTS) on saadaval. Kui valid selle võimaluse, **nr**, klientide tellimused luuakse alati sünkroonne režiimis RTS abil. Klienditellimuste loomisel asünkroonse režiimi tõmbas ja tõmmake V/12(p) Jobs Dynamics AX-i lisada. Vastava müügitellimuste on loodud Dynamics AX-i kui **sünkroonida tellimuste** käivitatakse kas käsitsi või partii töötlemiseks.

<a name="see-also"></a>Vt ka
--------

[Hübriid klienditellimuste](hybrid-customer-orders.md)


