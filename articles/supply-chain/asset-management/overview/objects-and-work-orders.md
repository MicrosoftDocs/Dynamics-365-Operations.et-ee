---
title: Varad ja töökäsud
description: Selles teemas kirjeldatakse varasid ja töökäskusid varahalduses.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c2500a695fcffe0d60ac13b1b74cda4322b0e14
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426300"
---
# <a name="assets-and-work-orders"></a>Varad ja töökäsud

[!include [banner](../../includes/banner.md)]

 

Selles teemas kirjeldatakse varasid ja töökäskusid varahalduses. Varad ja töökäsud on varahalduse kesksed osad. *Vara* on masin või masina osa, mis nõuab pidevat hooldust ja teenindust. Varasid saab luua hierarhilises struktuuris ja need võivad olla seotud funktsionaalsete asukohtadega. Hooldustöid saab kavandada varade kõikidel tasanditel.

Igale varale seadistatakse mitmesugused andmed, näiteks tooteteave ja vara täpsustus ning nõutavad hooldusplaanid. Järgmisel joonisel on ülevaade vara andmetest ja varade kuuluvusest töö tüüpides. Punast teksti kasutatakse näidete puhul, mis näitavad päritolu ja sõltuvused.

![Töö tüüpidega seotud vara andmeid kuvav diagramm](media/05-overview-image.png)

Igal töökäsul on töökäsu tüüp, ennetav hooldus, korrigeeriv hooldus või kontroll. Töökäsk sisaldab ühte või mitut töökäsu tööd. Iga töökäsu töö määratleb töö, mis tuleb sooritada vara ja seotud töö tüübiga. Seotud töö tüüpide hulgas on 10 000 km, 50 000 km, 1-aastane ülevaatus ja ohutusinspektsioon. Üks töökäsk võib olla seotud mitme varaga.

Järgmine illustratsioon näitab töökäsu põhiandmete ülevaadet.

![Töökäsu põhiandmeid kuvav diagramm](media/06-overview-image.png)

Töökäsk võib olla seotud mõne muu töökäsuga ja töö tüübid võivad sisaldada töökäsu loomiseks järeltöid. Üldiselt ei ole töökäskude vahel sõltuvusi. Seetõttu saavad nad muuta oma töökäskude elutsükli olekut ja neid saab planeerida üksteisest sõltumatult.

Töökäskusid saab luua erinevatel viisidel, mis on seotud korrigeeriva, ennetava või reaktiivse hooldusega. Saate töökäske luua ka käsitsi. Järgmine illustratsioon näitab ülevaadet töökäskude automaatse või käsitsi loomise protsessist.

![Töökäskude automaatset või käsitsi loomist kuvav diagramm](media/07-overview-image.png)

Töökäsu hooldustöö plaanimisel ja käitamisel tuleb täita mitu etappi. Järgmine illustratsioon näitab töötlemine ülevaadet.

![Töökäsu töötlemise ülevaadet kuvav diagramm](media/08-overview-image.png)

> [!NOTE]
> Kui töötate rakenduses Dynamics 365 Supply Chain Management ja moodulis **Varahaldus** valite uue kirje loomiseks **Uus**, valige **Redigeeri** olemasoleva kirje värskendamiseks ja valige **Salvesta** uute või redigeeritud andmete salvestamiseks.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]