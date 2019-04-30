---
title: Töökuulutuste sisestamine Attractist välistele karjäärisaitidele
description: Selles teemas selgitatakse, kuidas kasutada rakendust Dynamics 365 for Talent - Attract töökuulutuste sisestamiseks välistele värbamissaitidele
author: pganapmsft
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: eca599ad189edae29ef2de496196b08799a5e745
ms.sourcegitcommit: 1653d1e28d02f8a9a4bea8df562ac98d7a350ed1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/15/2019
ms.locfileid: "993664"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a>Töökuulutuste sisestamine Attractist välistele karjäärisaitidele

[!include [banner](../includes/banner.md)]

Soovite, et teave teie vabadest ametikohtadest jõuaks võimalikult paljude kvalifitseeritud kandidaatideni. Värbamissaidid nagu Broadbean aitavad teil seda eesmärki saavutada. Microsoft Dynamics 365 Talent: Attract võimaldab teil töökuulutusi Broadbeani sisestada ja Microsoft teeb selles vallas pidevalt uusi pakkumisi.

## <a name="post-jobs-to-broadbean"></a>Töökuulutuste sisestamine Broadbeani

Enne töökuulutuste sisestamist Broadbeani peate konfigureerima Broadbeani integreerimise.

> [!NOTE]
> - Töökuulutuste sisestamiseks välistele veebisaitidele peab teil olema [tervikliku värbamise lisandmoodul](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).
> - See funktsioon on praegu eelvaateversioonis. Kui soovite seda proovida, peate [selle sisse lülitama Attracti administraatori sätetega](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).

### <a name="configure-broadbean-integration"></a>Broadbeani integreerimise konfigureerimine

1. Attracti administraatorina sisse logimine.
2. Valige lehe paremast ülanurgast nupp **Sätted** (hammasrattasümbol) ja seejärel valige **Administreerimiskeskus**.
3. Lülitage integratsioon sisse vahekaardi **Tööportaalide sätted** jaotises **Luba Broadbeani integreerimine**.
4. Looge Broadbeaniga ühendus ja sisestage oma andmed lahtritesse **Kasutajanimi, Kliendi ID, Krüptimise luba**.

> [!WARNING]
> Teie Broadbeani mandaadid on tundlikud ja konfidentsiaalsed. Seega talletage ja jagage neid vastutustundlikult. Mandaadid on nähtavad kõigile, kellel on Attractis administraatori roll.

> [!NOTE]
> Microsoft ja Attract ei ole nende väärtuste loomise ning haldamisega seotud. Mandaatide Attractis ajakohasena hoidmine ja nendega seotud võimalike probleemide lahendamine Broadbeanis on teie vastutus.

### <a name="post-a-job-to-broadbean"></a>Töökuulutuse sisestamine Broadbeani

Kui Broadbean on sisse lülitatud, saavad värbajad ja administraatorid sellesse töökuulutuse sisestada. Teil peab töökuulutuse jaoks olema kandideerimise URL.

1. Avage Attractis töökuulutus, mida soovite Broadbeani sisestada.
2. Valige jaotises **Sisestamised** Broadbeanile vastav nupp **Sisesta kohe**.
3. Järgige Broadbeani aknas juhiseid.

Attract jagab Broadbeaniga järgmist teavet.

- Taotluse ID
- Ametinimetus
- Töö kirjeldus
- Töö asukoht
- Kandideerimise URL
- Värbamisteave

Kui Broadbean on sisestamise edukalt lõpetanud, kuvatakse Attractis töökuulutuse jaotises **Sisestamised** Broadbeani olekut kui **Sisestatud**.

> [!NOTE]
> - Broadbeanis on nõutav väli **Tegevusvaldkond**. Praegu on selle välja vaikimisi säte **IT**. Broadbeani töökuulutuse sisestamise aknas saate väärtuse siiski muuta õigeks tegevusvaldkonnaks.
> - Broadbeanil läheb aega teie töökuulutuse sisestamiseks kõikidesse valitud tööportaalidesse. Seetõttu võib kuluda veidi aega enne kui Attract töökuulutuse olekut värskendab.

### <a name="view-a-broadbean-job-posting"></a>Broadbeani töökuulutuse sisestuse kuvamine

Pärast töökuulutuse Broadbeani sisestamist saate seda kuvada Attracti kaudu.

1. Avage Attractis töökuulutus, mida soovite Broadbeanis kuvada.
2. Valige jaotises **Sisestamised** Broadbeanile vastav kolmikpunkti nupp (**...**) ja seejärel valige **Kuva**.

Broadbeani töökuulutuse sisestus kuvatakse uues aknas.

### <a name="update-a-broadbean-job-posting"></a>Broadbeani töökuulutuse sisestuse värskendamine

Broadbeani töökuulutuse sisestust saate värskendada kahel viisil.

1. Avage Attractis töökuulutus, mida soovite Broadbeanis värskendada.
2. Valige jaotises **Sisestamised** Broadbeanile vastav nupp **Värskenda töökuulutust**.
3. Muutke töökuulutust Broadbeani aknas.

või

1. Avage Attractis töökuulutus, mida soovite Broadbeanis kuvada.
2. Valige jaotises **Sisestamised** Broadbeanile vastav kolmikpunkti nupp (**...**) ja seejärel valige **Kuva**.
3. Muutke Broadbeani aknas töökuulutuse üksikasju ja seejärel sisestage töökuulutus uuesti. Töökuulutuse üksikasjad Attractis ei muutu.

### <a name="remove-a-broadbean-job-posting"></a>Broadbeani töökuulutuse sisestuse eemaldamine

Töökuulutuse sisestusi saate Broadbeanist vajaduse korral eemaldada.

1. Avage Attractis töökuulutus, mida soovite eemaldada.
2. Valige jaotises **Sisestamised** Broadbeanile vastav kolmikpunkti nupp (**...**) ja seejärel valige **Eemalda töökuulutus**.

Kui Broadbean on töökuulutuse eemaldanud, on Attractis Broadbeani üksusel **Sisesta kohe** nupp. Selle nupu olemasolu näitab, et töökuulutus on eemaldatud ja seda on võimalik uuesti sisestada.

### <a name="troubleshoot-the-broadbean-integration"></a>Broadbeani integreerimise tõrkeotsing

Kui teil on Broadbeani töökuulutuse sisestamisega probleeme, proovige järgmist.

1. Kontrollige, kas Attracti sisestatud Broadbeani mandaadid on kehtivad ja õiged.
2. Kui mandaadid on kehtivad ja õiged, võtke ühendust [Broadbeani toega](https://www.broadbean.com/resources/support/).
3. Kui probleem ei lahene, võtke ühendust [Microsofti toega](./talent-support.md).
