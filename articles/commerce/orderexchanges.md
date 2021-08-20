---
title: Vahetuse konfigureerimine ja töötlemine tagastustellimusel
description: Selles teemas selgitatakse, kuidas konfigureerida vahetust tagastusel rakenduses Dynamics 365 Commerce.
author: josaw1
ms.date: 07/28/2021
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
ms.openlocfilehash: 488f6fb5af6451bc462566a9714054b49eb1a80b8264528778797f6a39647764
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758332"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a>Vahetuse konfigureerimine ja töötlemine tagastustellimusel

[!include [banner](includes/banner.md)]

Rakenduse Dynamics 365 Commerce eelmistes versioonides töödeldi kliendi tellimuste tagastusi, kasutades tagastustellimuse dokumenti peakontoris. Kuid tagastustellimuse dokumenti saab kasutada vaid tagastatavate toodete töötlemiseks. Tagastatud tooted on tagastustellimuse ridadel tähistatud negatiivse kogusega. Müügid on aga tähistatud positiivse kogusega. Kuid tagastustellimuse dokument ei toeta positiivseid koguseid. Selle piirangu tõttu ei toetanud rakenduse varasemad versioonid stsenaariume, kus tootevahetusi tehakse tagastustellimuse dokumenti kasutades.

Kuid nüüd on lisatud funktsioon tagastustellimuste vahetuste stsenaariumide toetamiseks. Commerce kasutab nüüd seda tüüpi kannete töötlemiseks tagastustellimuse dokumendi asemel müügitellimuse dokumenti.

## <a name="configure-commerce-to-support-exchanges-on-return-orders"></a>Commerce'i konfigureerimine vahetuste toetamiseks tagastustellimuste korral

> [!NOTE]
> Commerce'i versioonis 10.0.20 ja uuemates versioonides on saadaval uus funktsioon nimega „Ühtne tagastuste töötlemise kogemus kassas“. Selle funktsiooni lubamisel ei ole järgmised häälestustoimingud vajalikud. **Töötle tagastustellimusi müügitellimustena** muutub püsivalt konfigureeritud sätteks ja te ei saa seda muuta.

Järgige järgmisi juhiseid, et konfigureerida süsteem toetama tagastustellimuste vahetusi (kui funktsioon **Ühtne tagastuste töötlemise kogemus kassas** pole teil lubatud).

1. Valige suvandid **Retail ja Commerce \> Peakontori seadistamine \> Parameetrid \> Commerce'i parameetrid**. Määrake kiirkaardil **Kliendi tellimused** suvand **Töötle tagastustellimusi müügitellimustena** valikule **Jah**.
2. Käivitage töö **Globaalse konfiguratsiooni jaotusgraafik** (**1110**).

## <a name="make-an-exchange"></a>Vahetuse tegemine

Kui süsteem on eelmises jaotises kirjeldatud viisil konfigureeritud, valib kassa (POS) kasutaja endiselt müügitellimuse või müügiarve tagastuse töötlemiseks, nagu rakenduse eelmistes versioonides. Kuid pärast tagastuskaupade lisamist korvi saab kasutaja lisada korvi uued müügiread.

Nende müügiridade jaoks peab kasutaja määrama kõik atribuudid, mis on vajalikud kliendi tellimuse rea töötlemiseks. Need atribuudid on muu hulgas tarneviis ja täitmisasukoht. Kandeks ootel makse on tagastustellimuse ridade ja müügitellimuse ridade netosumma. Kui makse kandeks makstakse, postitatakse tagastustellimus kaupluse halduses peakontori müügitellimuse dokumendina ja süsteem koostab kohe tagastusridade kohta arve.

Korvi eri summade paremaks nähtavuseks on korvi lisatud kolm uut summa välja. Nende väljade kättesaadavaks muutmiseks kassa kasutajaliideses (UI) saate kasutada ekraanikoostajat.

- **Rakendatud deposiit** – deposiidi summa, mis on kohaldatud kandele, kui kasutaja teeb kliendi tellimuse pealevõtmise. Kui deposiidi alistamine puudub ja konfigureeritud on 10-protsendine deposiit, on summa selles väljas 90 protsenti kliendi tellimuse kogusummast.
- **Realiseerimissumma** – kogusumma ridade kohta, kus tarneviis on seatud valikule **Tarne**, kui kliendi tellimus loodi või seda redigeeriti või kliendi tellimuse vahetuse ajal. Summa selles väljas sisaldab makse ja tasusid.
- **Tagastussumma** – kogusumma ridade kohta, kus on kliendi tellimuse vahetuse ajal negatiivne kogus. Summa selles väljas sisaldab makse ja tasusid.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
