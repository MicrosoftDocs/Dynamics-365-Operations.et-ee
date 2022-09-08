---
title: Laotöö tühistamine erandi käitlemiseks
description: See artikkel kirjeldab töö tühistamise funktsiooni, mis võimaldab lao ülevaatajatel käsitseda blokeeritud tööd.
author: Mirzaab
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b1e2036e4e7a8a47d6df029f285df7aca0fa74e6
ms.sourcegitcommit: 0220be95c007c77ba3b73fed8ac68a3d72dc2884
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404422"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a>Laotöö tühistamine erandi käitlemiseks

[!include [banner](../includes/banner.md)]

Microsofti tühistatud töö Dynamics 365 Supply Chain Management funktsionaalsus võimaldab administraatorkasutajal tühistada kindlat laotööd, mis on praegu pooleli, kuid mis on süsteemi poolt blokeeritud või mida ei saa erandlike tingimuste tõttu lõpule viia. See funktsioon on atraktiivne ja turvaline alternatiiv SQL-i parandusskriptidele, mis parandavad ebajärjekindlaid andmeid. Samas kui neid skripte taotletakse tavaliselt IT-spetsialistidelt, saavad tühistamistöö funktsioone kasutada selle ettevõtte kasutajad, kellel on administraatori õigused.

Laohalduse perioodiliste ülesannete tühistamise töö **funktsioonile** \> **pääsete juurde.** \> **Tühista töö \> puhastamine.** Määrake dialoogiboksis **Töö tühistamine** tühistatava töö ID ja seejärel valige **OK**.

## <a name="warehouse-work-that-can-be-canceled"></a>Tühistatav laotöö

Lao komplekteerimistoimingute ajal võib töötajatel esineda olukordi, kus nad on kogused registreerinud kui ladustamiskohast kasutuskohta komplekteeritud kogused, kuid seejärel ei saa nad paigutustoimingut registreerida. Ebajärjekindlad laoandmed on sageli, kuid mitte alati, töö blokeerimise põhjus.

Erinevalt regulaarsest **tühistamisfunktsioonist**, mida saab kasutada töö päise nupu Tühista abil, **ei nõua töö tühistamise funktsioon, et viimane lõpetatud töö rida oleks panemise tüüpi töörida**. Teisisõnu võib töö tühistamise funktsiooni tühistamisloogikat käivitada ka siis, kui töö rea kaubakogus on kasutaja asukohas.

> [!NOTE]
> Töö puhul, mis tuleb töö tõttu tühistada, peavad lao kasutajad jätkama regulaarsete tühistamisfunktsioonide kasutamist töö lehel.

Tühista tööfunktsiooniga **saab** **tühistada ainult** töö, **mille** tüüp on Müük, Ülekanne, **Toormaterjali** komplekteerimine või Varude ülekandmine. Külmutatud toormaterjali komplekteerimistöö või töö puhul, mida saab tühistada regulaarset tühistamisfunktsiooni kasutades, ei käivitata tühistamisloogikat (vt eelmist märkust).

Töö blokeeringu tühistamiseks tühistab süsteem kõik allesjäänud tööread ja fikseerib laoandmed, mis on seotud kasutaja määratud töö ID-ga. Kõik tavapärased lao käitlustoimingud, mis hõlmavad mõjutatud kauba kogust, saavad seejärel jätkuda.

Et panna mõjutatud kaup kindlasse asukohta pärast töö tühistamist, peab kasutaja kasutama mobiilses seadmes varude liikumise või koguse korrigeerimise toimingut.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]