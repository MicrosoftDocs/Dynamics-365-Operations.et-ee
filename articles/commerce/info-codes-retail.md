---
title: Teabekoodid ja teabekoodide grupid
description: See artikkel annab ülevaate teabekoodidest, teabekoodide gruppidest ja nende kasutamisest.
author: mugunthanm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailInfocodeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 22761
ms.assetid: 99877dba-a6e3-4d88-ba0a-ee5913aea17e
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 046204d36e2fc7a69129aaf7fe027b2abc7e8dd9
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411664"
---
# <a name="info-codes-and-info-code-groups"></a>Teabekoodid ja teabekoodide grupid

[!include [banner](includes/banner.md)]

See artikkel annab ülevaate teabekoodidest, teabekoodide gruppidest ja nende kasutamisest.

Teabekoodid võimaldavad teil hõivata andmeid kassaregistris. Saate teabekoodidega esitada kassapidajale viipasid teabe sisestamiseks mitmesuguste kassatoimingute, näiteks kaupade müümise ja tagastamise või klientide valimise ajal. Kassapidajad saavad valida sisendi loendist või sisestada selle koodi, numbri, kuupäeva või tekstina. Saate määrata teabekoodid poe eelmääratletud toimingutele, jaekaupadele, makseviisidele, klientidele või kindlatele kassategevustele. Teabekoodidega saate teha järgmist.

- Hõivake kande ajal lisateavet, nagu lennu number või tagastamise põhjus.
- Esitage kassapidajale viipasid, mis võimaldavad valida kindlate toodete hindade loendist.
- Linkige alamkood teabekoodiga, et esitada kassapidajale viip sisendiks kindla tegevuse ajal. Näiteks kui klient tagastab toote, võite paluda kassapidajal küsida, miks toode tagastatakse. Seejärel saate alamkoodidega lasta kuvada loendi põhjustest, mille vahel kassapidaja valida saab.
- Müüge toodet regulaarse hinnaga, allahindlusega või tasuta tootena.
- Esitage müügioperatsioonita kassasahtli avanud kassapidajale viip, mis võimaldab väärtuse sisestada või alamkoodide loendist valida.

## <a name="info-codes-group"></a>Teabekoodide grupp

Rakenduses Commerce saate luua teabekoodide gruppe. Teabekoodide grupid lisavad paindlikkust, võimaldades teil määratleda vähem teabekoode ja kasutada neid mitmekülgsemalt. Teabekoodide gruppe saate kasutada järgmiselt.

- Määratlege vähem teabekoode ja kasutage neid hõlpsasti uuesti. Teabekoodigruppides olevatel teabekoodidel ei ole eelmääratletud sõltuvusi teiste teabekoodidega. Võite lisada sama teabekoodi mitmesse teabekoodigruppi ja seejärel esitada prioriteetide abil samu teabekoode järjekorras, mis on mis tahes olukorras loogiline.
- Saate linkida teabekoodid muude teabekoodide või teabekoodigruppidega, et koguda teavet toote või kande kohta, ilma et peaksite määratlema iga stsenaariumi puhul eraldi teabekoodi või lingitud teabekoodi.

## <a name="info-code-examples"></a>Teabekoodide näited

**Näide 1: teabekoodide korduvkasutamine**

Saate teabekoodid linkida, mis tähendab, et ühe teabekoodi käivitamise järel käivitub kohe muu teabekood. Näiteks kui müüte teatud tooteid, saate lasta kassapidajal küsida, kas klient soovib osta patareisid ja tootegarantii. Muude toodete puhul saate lasta kassapidajal küsida, kas klient soovib osta ka patareisid, ja märkida üles kliendi sihtnumbri. Kui loote stsenaariumite jaoks lingitud teabekoodid, tuleb teil häälestada teabekoodi kõik variatsioonid, et kassapidajal palutaks küsida õiget teavet. Kui kasutate teabekoodigruppe, saate häälestada üldised teabekoodid, näiteks patareide pakkumine, ja seejärel kasutada teabekoode mitmes teabekoodigrupis. Teabekoodigruppides saate ka prioriteetide alusel määrata viipade kuvamise järjekorra.

**Näide 2: teabekoodide linkimine teabekoodigruppidega**

Kui müüte teatud tooteid, näiteks mobiilseid seadmeid, siis küsite klientidelt alati kindlaid andmeid, nagu telefoninumber, mobiilseadme ID (MEID) ja seerianumber. Samas soovite koguda tahvelarvutite müümisel muid andmeid kui mobiiltelefonide puhul. Saate seadistada teabekoodigrupi, mis sisaldab telefoninumbri, MEID ja seerianumbrite viipasid, ning seejärel linkida teabekoodigrupi individuaalse teabekoodiga. Tootepõhise teabekoodi käivitamise järel võib käivituda teabekoodigrupp, mis võimaldab teil koguda üldandmeid, ilma et peaksite määratlema iga seadme jaoks mitut lingitud teabekoodide kogumit.


[!INCLUDE[footer-include](../includes/footer-banner.md)]