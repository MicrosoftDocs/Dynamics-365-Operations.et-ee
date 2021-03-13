---
title: Tellimuse tagasikutsumise toiming kassas
description: Selles teemas selgitatakse funktsioonivõimalusi, mis on saadaval kassas täiustatud tellimuse tagasikutsumise lehtedel.
author: hhainesms
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 21e8045d754006345f5ad68e1e67579386c6df4a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010070"
---
# <a name="recall-order-operation-in-pos"></a>Tellimuse tagasikutsumise toiming kassas

[!include [banner](includes/banner.md)]

**Tellimuse tagasikutsumise** toiming rakenduse Commerce kassas (POS) pakub värskendatud tellimuste otsimise ja filtreerimise funktsioone ning tellimusespetsiifilist teavet. See funktsioon on saadaval rakenduse Commerce versioonis 10.0.15 ja uuemates.

Selle funktsiooni lubamiseks lülitage sisse funktsioon **Täiustatud tellimuse tagasikutsumise toiming kassas**, mis asub rakenduse Commerce peakontoris tööruumis **Funktsioonihaldus**. Pärast funktsiooni lubamist kaaluge kassas oma [kuvapaigutuste](pos-screen-layouts.md) värskendamist, et kasutada ära mõningaid muudetud võimalusi.

Toimingu **Tellimuse tagasikutsumine** nupp võimaldab organisatsioonidel teha toimingut eelnevalt määratletud kuva kaudu.

![Nupuruudustiku konfiguratsioon](media/recallorderbuttongrid.png)

Kuvasuvandid on järgmised.
- **Puudub** – see suvand käivitab toimingu ilma kindla kuvata. Kui kasutaja avab toimingu selle konfiguratsiooniga, palutakse neil tellimusi otsida ja leida või valida eelnevalt määratud tellimuse filtri seast.
- **Täidetavad tellimused** – kui kasutaja käivitab toimingu, käivitub päring automaatselt, et otsida üles ja kuvada loend tellimustest, mille kauplus peab täitma. Need tellimused on konfigureeritud kaupluses pealevõtmiseks või kauplusest lähetamiseks ning nende tellimuste ridu pole veel peale võetud ega pakitud.
- **Pealevõetavad tellimused** – kui kasutaja käivitab toimingu, käivitub päring automaatselt, et otsida üles ja kuvada loend tellimustest, mis on konfigureeritud kaupluses pealevõtmiseks kasutaja praeguses kaupluses.
- **Lähetatavad tellimused** – kui kasutaja käivitab toimingu, käivitub päring automaatselt, et otsida üles ja kuvada loend tellimustest, mis on konfigureeritud lähetamiseks kasutaja praegusest kauplusest.

Kui kassas käivitatakse toiming **Tellimuse tagasikutsumine** ja kuva väärtuseks on konfigureeritud **Puudub**, saab kasutaja tellimusi otsida ja leida ühel järgmistest viisidest.
- Skannige tellimuse vöötkoodid. See otsib vasteid tellimuse numbri, kanali viite ja sissetuleku ID väljadelt.
- Valige rakenduseribalt ikoon **Otsi tellimusi** või **Otsi ja filtreeri**, et kasutada kriteeriumidele vastavate tellimuste leidmiseks filtreerimist.
- Valige eelmääratletud filtri kaudu rippmenüüst **Kuva tellimused** (täidetavad tellimused, pealevõetavad tellimused või lähetatavad tellimused).

![RecallOrderMainMenu](media/recallordermain.png)

Pärast otsingukriteeriumide rakendamist kuvatakse rakenduses ühtivate müügitellimuste loend.

![RecallOrderDetail](media/orderrecalldetail.png)

Kasutaja saab valida loendist tellimuse, et vaadata täiendavaid üksikasju. Ekraani paremas servas oleval teabepaanil kuvatakse valitud tellimuse üksikasjad, sh tellimuse rea üksikasjad, tarne üksikasjad ja täitmise üksikasjad.

Rakendusepaanilt saab kasutaja valida toimingu. Sõltuvalt tellimuse olekust ei pruugi kindlad toimingud lubatud olla.

- **Tagasta** – käivitab valitud klienditellimusega seotud ühe või mitme arve tagastamise.

- **Tühista** – tühistab valitud müügitellimuse täielikult.

- **Täida** – viib kasutaja tellimuse täitmise lehele, mis on valitud tellimuse jaoks eelfiltreeritud. Kuvatakse ainult tellimuse read, mida saab valitud tellimuse puhul kasutaja kaupluses täita.

- **Redigeeri** – lubab kasutajatel valitud klienditellimust muuta.

- **Pealevõtmine** – käivitab pealevõtmise voo, mis võimaldab kasutajal valida peale võtavad tooted ning loob pealevõtmise müügitehingu.
