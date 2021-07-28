---
title: Varad ja töökäsud
description: Selles teemas kirjeldatakse varasid ja töökäskusid varahalduses.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4be7d3b77f72a9d79047d31b46dcabcb2bf09d12
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6351557"
---
# <a name="assets-and-work-orders"></a>Varad ja töökäsud

[!include [banner](../../includes/banner.md)]

 

Selles teemas kirjeldatakse varasid ja töökäskusid varahalduses. Varad ja töökäsud on varahalduse kesksed osad. *Vara* on masin või masina osa, mis nõuab pidevat hooldust ja teenindust. Varasid saab luua hierarhilises struktuuris ja need võivad olla seotud funktsionaalsete asukohtadega. Hooldustöid saab kavandada varade kõikidel tasanditel.

Igale varale seadistatakse mitmesugused andmed, näiteks tooteteave ja vara täpsustus ning nõutavad hooldusplaanid. Järgmisel joonisel on ülevaade vara andmetest ja varade kuuluvusest töö tüüpides. Punast teksti kasutatakse näidete puhul, mis näitavad päritolu ja sõltuvused.

![Töö tüüpidega seotud vara andmeid kuvav diagramm.](media/05-overview-image.png)

Igal töökäsul on töökäsu tüüp, ennetav hooldus, korrigeeriv hooldus või kontroll. Töökäsk sisaldab ühte või mitut töökäsu tööd. Iga töökäsu töö määratleb töö, mis tuleb sooritada vara ja seotud töö tüübiga. Seotud töö tüüpide hulgas on 10 000 km, 50 000 km, 1-aastane ülevaatus ja ohutusinspektsioon. Üks töökäsk võib olla seotud mitme varaga.

Järgmine illustratsioon näitab töökäsu põhiandmete ülevaadet.

![Töökäsu põhiandmeid kuvav diagramm.](media/06-overview-image.png)

Töökäsk võib olla seotud mõne muu töökäsuga ja töö tüübid võivad sisaldada töökäsu loomiseks järeltöid. Üldiselt ei ole töökäskude vahel sõltuvusi. Seetõttu saavad nad muuta oma töökäskude elutsükli olekut ja neid saab planeerida üksteisest sõltumatult.

Töökäskusid saab luua erinevatel viisidel, mis on seotud korrigeeriva, ennetava või reaktiivse hooldusega. Saate töökäske luua ka käsitsi. Järgmine illustratsioon näitab ülevaadet töökäskude automaatse või käsitsi loomise protsessist.

![Töökäskude automaatset või käsitsi loomist kuvav diagramm.](media/07-overview-image.png)

Töökäsu hooldustöö plaanimisel ja käitamisel tuleb täita mitu etappi. Järgmine illustratsioon näitab töötlemine ülevaadet.

![Töökäsu töötlemise ülevaadet kuvav diagramm.](media/08-overview-image.png)

> [!NOTE]
> Kui töötate rakenduses Dynamics 365 Supply Chain Management ja moodulis **Varahaldus** valite uue kirje loomiseks **Uus**, valige **Redigeeri** olemasoleva kirje värskendamiseks ja valige **Salvesta** uute või redigeeritud andmete salvestamiseks.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]