---
title: Talenti laiendamine Power Appsi ja Power Automate’iga
description: Selles artiklis kirjeldatakse rakenduse Microsoft Dynamics 365 Human Resources laiendatavusstsenaariumeid, mis kasutavad Microsoft Power Appsi ja Microsoft Power Automate'i.
author: negudava
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5fe8ecd368bc63eed43c86053084ca67ef9beac6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859513"
---
# <a name="extend-with-power-apps-and-power-automate"></a>Laiendamine Power Appsi ja Power Automate’iga


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Selles artiklis kirjeldatakse rakenduse Microsoft Dynamics 365 Human Resources laiendatavusstsenaariumeid, mis kasutavad Microsoft Power Appsi ja Microsoft Power Automate'i. Saate rakenduse Power Apps keskkonda importida iga näitega seotud lahendusepaketi. Seejärel saate pakette kasutada juhisena või lähtekohana teie organisatsioonile sobivate stsenaariumide rakendamiseks.

> [!IMPORTANT]
> Kui soovite kasutada malle ja rakendusi, mida on kirjeldatud käesolevas artiklis "nagu on", kontrollige kindlasti, et need hõlmaks kõiki teie rakendusele omasi stsenaariume.

## <a name="prerequisites"></a>Eeltingimused

- Pakettide importimiseks peab kasutajatel olema **keskkonna looja** luba.
- Rakenduste eksportimiseks või importimiseks peab kasutajatel olema Power Appsi plaani 2 litsents või Power Appsi plaani 2 proovilitsents.

## <a name="integration-with-microsoft-365-power-automate"></a>Microsoft 365-ga integreerimine, Power Automate

Rakendust **Microsoft 365-ga integreerimine** saab kasutada sisse logitud kasutajate töörühma teabe ekstraktimiseks Microsoft 365-st. See viitab töötajatele rakenduses Human Resources, et hankida töövõtja tuvastustüüpe. Haldurid saavad kontrollida töötaja ID-tüüpide aegumiskuupäevi. Samuti võivad nad saata meeldetuletuse, kui töötaja ID-tüüp on aegumas. Selle meeldetuletuse saatmiseks Power Automate integreerub Power Appsiga. Kui meeldetuletus on saadetus, saadetakse Power Automate’ist tagasi Power Appsi kinnitus. Identifikatsiooni tüübid hõlmavad juhiluba, passi ja teisi aktsepteeritavaid ID vorme.

Saate seda rakendust laiendada teistele stsenaariumidele. Näiteks saate seda kasutada töörühma puhkuste teabe, kalendrisündmuste ja töörühmaga seotud sündmuste näitamiseks.

**Microsoft 365-ga integreerimise, Power Automate** rakenduse allalaadimiseks avage Microsofti allalaadimiskeskuses [Microsoft 365-ga integreerimine](https://go.microsoft.com/fwlink/?linkid=2081787).

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate – SQL-i ühendamine ja käivitamine

Mall **Power Automate – SQL-i ühendamine ja käivitamine** loob ühenduse Microsoft SQL Serveriga ja lubab käivitada SQL-i päringuid.

Kuigi see mall loeb ja värskendab SQL-tabeleid, saate seda laiendada ja kasutada seda muude stsenaariumite jaoks. Näiteks saate seda kasutada vahetabeli täitmiseks teenuses Dataverse kirjetega SQL-serverist ja vahetabeli aeg-ajalt sünkroonimiseks, kasutades SQL-serveri astmelist jaotust.

Täpsem päring on integreeritud Flowga, mis võimaldab andmete teisendamist ja astmelist jaotust.

Malli **Power Automate – SQL-i ühendamine ja käivitamine** allalaadimiseks avage Microsofti allalaadimiskeskuses [Power Automate – SQL-i ühendamine ja käivitamine](https://go.microsoft.com/fwlink/?linkid=2081789).

## <a name="additional-resources"></a>Lisaressursid

[Microsoft Power Platform](/power-platform/admin/admin-documentation)</br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
