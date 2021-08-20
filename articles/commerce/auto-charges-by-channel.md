---
title: Automaatsete tasude lubamine ja konfigureerimine kanali kaupa
description: Selles teemas selgitatakse, kuidas lubada ja konfigureerida automaatseid tasusid kanali järgi Microsoft Microsoft Dynamics 365 Commerce'is.
author: gvrmohanreddy
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: d905819d1e0c8223c74509bfb357b3aaa51d20305a2857061eadb0b0ff8f6b9b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727626"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a>Automaatsete tasude lubamine ja konfigureerimine kanali kaupa

Selles teemas selgitatakse, kuidas lubada ja konfigureerida automaatseid tasusid kanali järgi Microsoft Dynamics 365 Commerce'is.

## <a name="overview"></a>Ülevaade

Teil võib ette tulla olukordi, kus peate rakendama ringlussevõtu tasusid või muid tasusid kindlale tootegrupile, mida müüakse kõikides või osades poodides kindlas osariigis (nt Californias). Commerce'i funktsioon **Luba automaatsete tasude filtreerimine kanali järgi** võimaldab teil määrata automaatseid tasusid kanali järgi (nt kindel füüsiliste poodide kanal). See funktsioon on saadaval rakenduses Dynamics 365 Commerce versioonis 10.0.10 ja uuemas.

Automaatsete tasude lubamiseks ja konfigureerimiseks kanali järgi peate lõpule viima järgmised toimingud.

- Lülitage sisse funktsioon **Luba automaatsete tasude filtreerimine kanali järgi**.
- Konfigureerige organisatsiooni hierarhia eesmärk.
- Määratlege automaatsed tasud kanali järgi.

> [!NOTE]
> Funktsioon **Luba automaatsete tasude filtreerimine kanali järgi** töötab ainult juhul, kui täpsemate automaatsete tasude funktsioon on samuti sisse lülitatud. Lisateabe saamiseks täpsemate automaatsete tasude funktsiooni sisselülitamise kohta leiate teemast [Omnikanali täpsemad automaatsed tasud](omni-auto-charges.md).

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a>Lülitage sisse funktsioon Luba automaatsete tasude filtreerimine kanali järgi

Commerce'is automaatsete tasude lubamiseks kanali järgi toimige järgnevalt.

1. Minge jaotisse **Süsteemi administraator \> Tööruumid \> Funktsioonihaldus**.
1. Vahekaardi **Pole lubatud** loendis **Funktsiooni nimi** otsige ja valige **Luba automaatsete tasude filtreerimine kanali järgi**.
1. Valige paremas alanurgas **Luba kohe**. Pärast funktsiooni sisselülitamist kuvatakse see vahekaardi loendis **Kõik**.
1. Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**.
1. Leidke ja valige vasakpoolsel paanil töö **1110** (**Globaalne konfiguratsioon**).
1. Konfiguratsioonimuudatuste lisamiseks valige tegevuse paanil käsk **Käivita kohe**.

> [!WARNING]
> Funktsiooni **Luba automaatsete tasude filtreerimine kanali järgi** väljalülitamisel, kui olete seda juba kasutanud, ei kuvata enam jaotises **Automaatsed tasud** välja **Jaemüügikanali seos** ja olemasolevad konfiguratsioonid lähevad kaotsi. Kui konfiguratsioonide **Jaemüügikanali seos** eemaldamine põhjustab automaatsete tasude reeglite dubleerimise, ei õnnestu funktsiooni välja lülitada. Enne funktsiooni väljalülitamist vaadake kindlasti üle kõik automaatsete tasude reeglid ja tehke vajalikud muudatused.

## <a name="configure-the-organization-hierarchy-purpose"></a>Organisatsiooni hierarhia eesmärgi konfigureerimine

Uus organisatsiooni hierarhia eesmärk nimega **Jaemüügi automaatsed tasud** on loodud automaatsete tasude hierarhia haldamiseks kanali järgi.

Commerce'is organisatsiooni hierarhia eesmärgi jaoks vaikehierarhia määramiseks toimige järgmiselt.
        
1. Minge jaotisse **Organisatsiooni haldus \> Organisatsioonid \> Organisatsiooni hierarhia eesmärgid**.
1. Valige vasakpoolsel paanil **Jaemüügi automaatsed tasud**.
1. Jaotises **Määratud hierarhiad** valige **Lisa**.
1. Dialoogiboksis **Organisatsiooni hierarhiad** valige organisatsiooni hierarhia (nt **Jaekauplused piirkonniti**) ja seejärel valige **OK**.
1. Jaotises **Määratud hierarhiad** valige **Määra vaikesätteks**.
1. Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**.
1. Leidke ja valige vasakpoolsel paanil töö **1040** (**Tooted**).
1. Valige tegevuste paanil käsk **Käivita kohe**.
1. Korrake kahte eelmist kahte toimingut tööde **1070** (**Kanali konfiguratsioon**) ja **1110** (**Globaalne konfiguratsioon**) käivitamiseks.

![Jaemüügi automaatsete tasude organisatsiooni hierarhia eesmärgi konfigureerimine.](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a>Automaatsete tasude määratlemine kanali järgi

Pärast funktsiooni **Luba automaatsete tasude filtreerimine kanali järgi** sisselülitamist ja organisatsiooni hierarhia eesmärgi **Jaemüügi automaatsed tasud** konfigureerimist saab automaatseid kulusid kanali järgi määratleda kas tellimuse päise või tellimuserea tasemel.

Commerce'is automaatsete tasude määratlemiseks kanali järgi toimige järgnevalt.

1. Minge jaotisse **Müügireskontro \> Kulude seadistus \> Automaatsed kulud**.
1. Valige vasakpoolse paani väljlal **Tase** kas **Päis** või **Rida**, sõltuvalt teie ettevõtte vajadusest.
1. Valige väljal **Jaemüügikanali kood** sobiv kanali kood (nt **Tabel** või **Grupp**). Kui kasutate vaikesätet **Kõik**, rakendatakse tasude reeglid kõigile kanalitele.

    - Kui teete valiku **Grupp**, veenduge, et jaemüügikanali tasude grupp luuakse jaotises **Jaemüük ja kaubandus \> Kanali häälestus \> Tasud \> Jaemüügikanali tasude grupid**.
    - Kui teete valiku **Tabel**, saate valida kindla kanali (nt **San Francisco**) väljal **Jaemüügikanali seos**.

1. Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**.
1. Leidke ja valige vasakpoolsel paanil töö **1040** (**Tooted**).
1. Valige tegevuste paanil käsk **Käivita kohe**.
1. Korrake kahte eelmist kahte toimingut tööde **1070** (**Kanali konfiguratsioon**) ja **1110** (**Globaalne konfiguratsioon**) käivitamiseks.
    
![Kanali järgi määratletud automaatsed tasud.](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a>Näidisstsenaarium

Järgmises näites kirjeldatakse toote konfigureerimiseks vajalikke etappe nii, et ringlussevõtu tasusid võetakse toote müümisel San Francisco füüsilise kaupluse kanali kaudu. Selles näites kirjeldatakse ka automaatsete tasude kuvamist Commerce'i kassarakenduses.

Organisatsioon määratleb tasude koodi nimega **RINGLUSSEVÕTT**, nagu järgmisel joonisel on näidatud.

![Tasude kood RINGLUSSEVÕTT.](media/Auto-charges-charge-code.png)

Automaatne tasu luuakse reatasemel. Sellel on järgmine konfiguratsioon.

- Välja **Konto kood** väärtuseks on seatud **Kõik**.
- Välja **Kaubakood** väärtuseks on seatud **Tabel**.
- Välja **Kauba seos** väärtuseks on seatud toote ID **91001**.
- Välja **Tarneviisi kood** väärtuseks on seatud **Kõik**.
- Välja **Jaemüügikanali kood** väärtuseks on seatud **Tabel**.
- Välja **Jaemüügikanali seos** väärtuseks on seatud kauplus **San Francisco**.

Automaatsete tasude rida on loodud. Sellel on järgmine konfiguratsioon.

- Välja **Valuuta** väärtuseks on seatud **USD**.
- Välja **Tasude kood** väärtuseks on seatud **RINGLUSSEVÕTT**.
- Välja **Kategooria** väärtuseks on seatud **Fikseeritud**.
- Välja **Tasud** väärtuseks on seatud **6,25 $**.

![Reataseme automaatsete tasude ja automaatsete tasude rea konfigureerimine.](media/Auto-charges-recyclingfee-line-fee.png)

Kassarakenduses on loodud müügitellimus kaupluse kanalis **San Francisco**. Real **Kulud** kuvatakse ringlussevõtu tasu **6,25 $**.

Valides kassarakenduses **Kande suvandid \> Tasud \> Tasude haldamine** saate vaadata tasude koodi ja ringlussevõtu tasu kirjeldust.

![Ringlussevõtu tasu kassarakenduses.](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a>Lisaressursid

[Omnikanali täpsemad automaatsed kulud](omni-auto-charges.md)

[Päisekulude proportsionaalselt jaotamine vastavatele müügiridadele](pro-rate-charges-matching-lines.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]