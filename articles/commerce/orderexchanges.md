---
title: Vahetuse konfigureerimine ja töötlemine tagastustellimusel
description: Selles teemas selgitatakse, kuidas konfigureerida vahetust tagastusel rakenduses Dynamics 365 Commerce.
author: josaw1
ms.date: 11/12/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 46d6e912aca64951da2865f5609a9dc22fbbcbe3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804597"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a>Vahetuse konfigureerimine ja töötlemine tagastustellimusel

[!include [banner](includes/banner.md)]

Rakenduse Dynamics 365 Commerce eelmistes versioonides töödeldi kliendi tellimuste tagastusi, kasutades tagastustellimuse dokumenti peakontoris. Kuid tagastustellimuse dokumenti saab kasutada vaid tagastatavate toodete töötlemiseks. Tagastatud tooted on tagastustellimuse ridadel tähistatud negatiivse kogusega. Müügid on aga tähistatud positiivse kogusega. Kuid tagastustellimuse dokument ei toeta positiivseid koguseid. Selle piirangu tõttu ei toetanud rakenduse varasemad versioonid stsenaariume, kus tootevahetusi tehakse tagastustellimuse dokumenti kasutades.

Kuid nüüd on lisatud funktsioon tagastustellimuste vahetuste stsenaariumide toetamiseks. Kaubandus kasutab nüüd seda tüüpi kannete töötlemiseks tagastustellimuse dokumendi asemel müügitellimuse dokumenti.

## <a name="configure-commerce-to-support-exchanges-on-return-orders"></a>Kaubanduse konfigureerimine vahetuste toetamiseks tagastustellimustel

Järgige neid etappe süsteemi konfigureerimiseks nii, et see toetaks vahetusi tagastustellimustel.

1. Valige suvandid **Jaemüük ja kaubandus \> Peakontori seadistamine \> Parameetrid \> Kaubanduse parameetrid**. Määrake kiirkaardil **Kliendi tellimused** suvand **Töötle tagastustellimusi müügitellimustena** valikule **Jah**.
2. Käivitage töö **Globaalse konfiguratsiooni jaotusgraafik** (**1110**).

## <a name="make-an-exchange"></a>Vahetuse tegemine

Kui süsteem on eelmises jaotises kirjeldatud viisil konfigureeritud, valib kassa (POS) kasutaja endiselt müügitellimuse või müügiarve tagastuse töötlemiseks, nagu rakenduse eelmistes versioonides. Kuid pärast tagastuskaupade lisamist korvi saab kasutaja lisada korvi uued müügiread.

Nende müügiridade jaoks peab kasutaja määrama kõik atribuudid, mis on vajalikud kliendi tellimuse rea töötlemiseks. Need atribuudid on muu hulgas tarneviis ja täitmisasukoht. Kandeks ootel makse on tagastustellimuse ridade ja müügitellimuse ridade netosumma. Kui makse kandeks makstakse, postitatakse tagastustellimus kaupluse halduses peakontori müügitellimuse dokumendina ja süsteem koostab kohe tagastusridade kohta arve.

Korvi eri summade paremaks nähtavuseks on korvi lisatud kolm uut summa välja. Nende väljade kättesaadavaks muutmiseks kassa kasutajaliideses (UI) saate kasutada ekraanikoostajat.

- **Rakendatud deposiit** – deposiidi summa, mis on kohaldatud kandele, kui kasutaja teeb kliendi tellimuse pealevõtmise. Kui deposiidi alistamine puudub ja konfigureeritud on 10-protsendine deposiit, on summa selles väljas 90 protsenti kliendi tellimuse kogusummast.
- **Realiseerimissumma** – kogusumma ridade kohta, kus tarneviis on seatud valikule **Tarne**, kui kliendi tellimus loodi või seda redigeeriti või kliendi tellimuse vahetuse ajal. Summa selles väljas sisaldab makse ja tasusid.
- **Tagastussumma** – kogusumma ridade kohta, kus on kliendi tellimuse vahetuse ajal negatiivne kogus. Summa selles väljas sisaldab makse ja tasusid.


[!INCLUDE[footer-include](../includes/footer-banner.md)]