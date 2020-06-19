---
title: Elusündmuste töötlemine
description: Töövõtja töötsükli ajal rakenduses Microsoft Dynamics 365 Human Resources võib igal töövõtjal esineda mitmesuguseid elusündmuste muudatusi.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 504408505168947ac725b5ee9764ecd994a64631
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429216"
---
# <a name="process-life-events"></a>Elusündmuste töötlemine

Töövõtja töötsükli ajal rakenduses Microsoft Dynamics 365 Human Resources võib igal töövõtjal esineda mitmesuguseid elusündmuste muudatusi. Näiteks abielu, tööhõive muutus või sõltuva isiku / kasusaaja muutus. Elusündmuste kasutamiseks peate lubama elusündmused soodustuste parameetrite vormil, häälestama elusündmuse tüübid ja seadistama plaani tüüpide jaoks elusündmuse valikud.

Enne kui saate elusündmusi töödelda, peate olema käitanud avatud registreerimist vähemalt üks kord värbamise ajavahemikus. Ameerika Ühendriikides on avatud registreerimine tavaliselt üks kord aastas. Väljaspool Ameerika Ühendriike võib avatud registreerimine toimuda värbamise ajal. Töötaja ei pea valima elusündmuste töötlemiseks soodustuse plaani, kuid nad peavad olema avatud registreerimise töötlemisse kaasatud. 

Kasutage elusündmuse töötlemist, kui teil on töötajad, kellel toimuvad elusündmused kuupäeval, mis on tulevikus. See sündmus töötleb kõiki elusündmusi, mida pole töödeldud (nt tulevased elusündmused või lisatud elusündmused, mis ei ole ühelegi töötajale spetsiifilised – üks näide on uus soodustus). Reaalajas elusündmused on peidetud.

Näiteks, kui täna on 1. veebruar ja 14. veebruaril töötaja Erki Sepal on plaanis muuta juriidilist isikut, kui käivitate elusündmuse töötluse 15. veebruaril, siis töötleb süsteem kõiki sündmusi kuni 15. veebruarini. 

1. Tööruumis **Soodustuste haldus** jaotises **Töötlemine** valige suvand **Elusündmuse töötlemine**.

2. Dialoogiaknas **Elusündmuse registreerimise protsessi käitamine** määrake järgmiste väljade väärtused.

   | Väli | Kirjeldus |
   | --- | --- |
   | **Registreerimisperiood** | Registreerimisperiood, mille jaoks elusündmusi töödelda. |
   | **Juriidiline isik** | Juriidiline isik, mille jaoks elusündmusi töödelda. |
   | **Elusündmuse kuupäev** | Süsteem töötleb kõiki sündmusi registreerimisperioodil, mis toimuvad kuni selle kuupäevani. |
   | **Töötaja** | Töötaja, kelle jaoks elusündmusi töödelda. Kui jätate selle välja tühjaks, töödeldakse elusündmusi kõigi töötajate puhul. |

3. Kui soovite protsessi käitada taustal, valige suvand **Käivita taustal** ja tehke järgmised ülesanded.

   1. Sisestage teavet protsessi kohta.

   2. Korduva töö seadistamiseks valige suvand **Kordumine**, sisestage kordumise teave ja valige **OK**.

   3. Töö teatise seadistamiseks valige suvand **teatised**, valige milliseid teatisi saada ja seejärel valige **OK**.

   4. Valige nupp **OK**. Protsess töötab teie määratud parameetritega.

4. Valige nupp **OK**.
