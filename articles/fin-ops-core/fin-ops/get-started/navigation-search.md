---
title: Navigeerimisotsing
description: See artikkel selgitab, kuidas kasutada lehtedel navigeerimiseks otsingufunktsioone.
author: jasongre
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.openlocfilehash: 4c362e4cd83f926e7e21d775abd24ae6ddfcbbed
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292333"
---
# <a name="navigation-search"></a>Navigeerimisotsing

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

See artikkel selgitab, kuidas kasutada lehtedel navigeerimiseks otsingufunktsioone.

Rakendus sisaldab mitut ala ja lehte, mis aitavad teil mitmesuguseid toiminguid teha. Ülesannete täitmiseks vajalike lehtede kiireks leidmiseks saate kasutada navigeerimise otsingufunktsiooni.

Selle funktsiooni kasutamiseks klõpsake ikooni **Otsing**, et kuvada väli **Otsing**. Seejärel saate tippida väljale sõna või väljendi. Süsteem otsib kohe rakendusest lehti, mis vastavad teie sisestatud sõnale. Näiteks võite tippida sõna „hankijaarve” ja süsteem kuvab sellele sisestusele vastavad tulemused.

> [!NOTE]
> Väli **Otsing** aitab lehti leida ja nende juurde liikuda. See ei aita leida konkreetseid andmeid ega toiminguid.

![otsingukast.](media/navigation-search.png "Otsingukast")

## <a name="quickly-navigate-to-a-particular-page"></a>Kiiresti liikumine kindlale lehele

Navigeerimise otsingufunktsioon on ka suurepärane viis kiiresti kindlale lehele liikumiseks. Näiteks kui olete ostureskontro ametnik, kes kasutab sageli lehte **Maksetööleht**, võite sisestada **otsinguväljale** sõna „maksetööleht”. Kuna sisestus vastab täpselt lehe pealkirjale, on leht otsingutulemuste alguses ja pääsete sellele kiiresti juurde.

Otsingutulemuste loend kuvab lehe pealkirja ja navigeerimistee. See näitab lehe asukohta rakenduses. Samuti aitab see eristada tulemustes mitut sarnast lehte.

Lehe otsimisel võrreldakse sisestust lehe pealkirja ja selle navigeerimisteega. Näiteks, kui sisestate väljale **Otsing** sõna „saadaolev”, näete nende lehtede tulemusi, mis on teile kättesaadavad ostureskontro alal – isegi, kui lehtede pealkirjades pole sõna „saadaolev”.

## <a name="quickly-navigate-to-a-page-based-on-the-technical-form-name"></a>Lehele kiiresti liikumine tehnilise vormi nime alusel

Navigeerimisotsingu funktsioon sisaldab ka eeliskasutajate palju nõutud funktsiooni: võimalust minna kiiresti lehele tehnilise vormi nime alusel. Paljud kasutajad on süsteemiga nii tuttavad, et nad teavad täpseid vormide nimesid, millega nad töötavad. Kui olete ka selline kasutaja, võite sisestada sõna **vorm:** ja selle järele vormi nime, mida otsite. Näiteks kui sisestate **vorm: vendinvoice**, kuvatakse otsingutulemustes kõik lehed, kus vormi nimi algab sõnaga **vendinvoice**.

## <a name="administration-and-security"></a>Administreerimine ja turve

Administreerimise ja turbe vaatepunktist hõlmab navigeerimisotsingu funktsioon ainult kaht tüüpi tulemusi:

- lehti, mis on praeguses konfiguratsioonis lubatud (konfiguratsioonivõtmete kaudu);
- lehti, millele kasutajal on oma rolli põhjal juurdepääs.

Otsingutulemuste loend on piiratud 10 üksusega. Kui te ei leia tulemustest seda, mida otsite, võiksite proovida sisestust täpsustada või muuta.

## <a name="development"></a>Arendus

Arenduse vaatepunktist on navigeerimise otsingufunktsiooni väga lihtne kasutada, kuna menüüelementide juurutamise ja nende kuvamise vahel otsingutulemustes puudub praktiliselt igasugune viivitus. Kui menüüelemendid on seotud navigeerimispaani või armatuurlauaga, muutuvad need automaatselt otsitavaks.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
