---
title: Varad ja töökäsud
description: Selles teemas kirjeldatakse varasid ja töökäskusid varahalduses.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5bd55988578be2b0287b399549f17642bfb1693b
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783204"
---
# <a name="assets-and-work-orders"></a>Varad ja töökäsud

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Selles teemas kirjeldatakse varasid ja töökäskusid varahalduses. Varad ja töökäsud on varahalduse kesksed osad. *Vara* on masin või masina osa, mis nõuab pidevat hooldust ja teenindust. Varasid saab luua hierarhilises struktuuris ja need võivad olla seotud funktsionaalsete asukohtadega. Hooldustöid saab kavandada varade kõikidel tasanditel.

Igale varale seadistatakse mitmesugused andmed, näiteks tooteteave ja vara täpsustus ning nõutavad hooldusplaanid. Järgmisel joonisel on ülevaade vara andmetest ja varade kuuluvusest töö tüüpides. Punast teksti kasutatakse näidete puhul, mis näitavad päritolu ja sõltuvused.

![Joonis 1](media/05-overview-image.png)

Igal töökäsul on töökäsu tüüp, ennetav hooldus, korrigeeriv hooldus või kontroll. Töökäsk sisaldab ühte või mitut töökäsu tööd. Iga töökäsu töö määratleb töö, mis tuleb sooritada vara ja seotud töö tüübiga. Seotud töö tüüpide hulgas on 10 000 km, 50 000 km, 1-aastane ülevaatus ja ohutusinspektsioon. Üks töökäsk võib olla seotud mitme varaga.

Järgmine illustratsioon näitab töökäsu põhiandmete ülevaadet.

![Joonis 2](media/06-overview-image.png)

Töökäsk võib olla seotud mõne muu töökäsuga ja töö tüübid võivad sisaldada töökäsu loomiseks järeltöid. Üldiselt ei ole töökäskude vahel sõltuvusi. Seetõttu saavad nad muuta oma töökäskude elutsükli olekut ja neid saab planeerida üksteisest sõltumatult.

Töökäskusid saab luua erinevatel viisidel, mis on seotud korrigeeriva, ennetava või reaktiivse hooldusega. Saate töökäske luua ka käsitsi. Järgmine illustratsioon näitab ülevaadet töökäskude automaatse või käsitsi loomise protsessist.

![Joonis 3](media/07-overview-image.png)

Töökäsu hooldustöö plaanimisel ja käitamisel tuleb täita mitu etappi. Järgmine illustratsioon näitab töötlemine ülevaadet.

![Joonis 4](media/08-overview-image.png)

> [!NOTE]
> Kui töötate rakenduses Microsoft Dynamics 365 for Finance and Operations ja moodulis **Varahaldus** valite uue kirje loomiseks **Uus**, valige **Redigeeri** olemasoleva kirje värskendamiseks ja valige **Salvesta** uute või redigeeritud andmete salvestamiseks.
