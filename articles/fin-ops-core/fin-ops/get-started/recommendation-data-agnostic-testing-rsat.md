---
title: Andmete agnostiline testimine, kasutadesRegression Suite Automation Tool
description: See artikkel käsitleb soovitusi andmeagnostiliseks testimiseks Regression Suite Automation Tool.
author: FrankDahl
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2019-09-11
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.custom: 21761
ms.openlocfilehash: f4322cb76d1d83c02ec9d4dcb997a1cd4730d090
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269587"
---
# <a name="data-agnostic-testing-using-the-regression-suite-automation-tool"></a>Andmete agnostiline testimine, kasutadesRegression Suite Automation Tool

[!include [banner](../includes/banner.md)]

Kui ERP-rakenduse funktsionaalne valideerimine ei saa olla täielikult agnostiline, on katsetamiseks mitu faasi ja lähenemist. Need testimise etapid hõlmavad järgmist:  

- SysTest raamistik
- ATL raamistik
- Regression Suite Automation Tool (RSAT)

[![Testi klassifikatsiooni püramiid.](./media/rsat-data-agnostic-testing-01.PNG)](./media/rsat-data-agnostic-testing-01.PNG)

## <a name="overview"></a>Ülevaade
-   **SysTest raamistik** – SysTest raamistik on usaldusväärseks ühiku testimiseks. Kuna ühiku testid testivad üldiselt meetodit või funktsiooni, peaksid need alati olema andmeagnostilised ja sõltuvad ainult sisendi andmetest, mis esitatakse katse osana.
-   **ATL raamistik** – Microsoftil on ATL raamistik, mis on SysTest raamistikus abstraktsioon ja muudab funktsionaalse testi kirjutamise palju lihtsamaks ja usaldusväärsemaks. Seda raamistikku tuleks kasutada komponentide testide või lihtsate integratsiooni katsete kirjutamiseks.
-   **RSAT** – RSAT kasutatakse integratsiooni testide ja äritsükli testide jaoks. Äritsükli testid, mida kutsutakse ka regressiooni kinnitamise testideks, sõltuvad olemasolevatest andmetest. Kuid need testid võivad muutuda andmete agnostiliseks, kui kaalute täiendavaid tegureid. 

    - o Kui ühiku testid ja komponentide testid on madalad ja võivad täielikult olla andmed agnostilised (ei sõltu olemasolevast andmekogumist), on äritsükli või regressiooni kinnitamise testid sõltuvad mõnedest olemasolevatest andmetest. Need andmed sisaldavad häälestust, konfiguratsioonisätteid (parameetreid) ja koondandmete (klient, hankijad, kaubad jne), kuid mitte kunagi kande andmeid. Veenduge, et testi ajal, kui mõnda neist muudetakse, taastatakse need lõpliku testi osana tagasi.
    - Valige kindla kirje valimise asemel koondandmete aluseks olevad andmed. Näiteks kui soovite valida oma dimensiooniväärtuste ja varude saadavuse põhjal kauba, filtreerida nende väärtustega toodete loendit, valida esimese kauba ja kopeerida tulevaste katsete jaoks kasutatav number. Kui see on lihtne koondandmete rida, nt klient, hankija või kaup, saab seda luua automatiseerimise osana ja kasutada tulevastes testides keti kaudu. 
    - o Sisestage kordumatud ID-d (nt arve numbrid) numbriseeria kaudu või kasutades Microsoft Excel funktsioone, nt =TEXT(NOW(),"yyyymmddhhmm"). See funktsioon annab iga minut kordumatu numbri, mis võimaldab teil jälgida, millal tegevus toimus. Seda saab kasutada muutujate jaoks, nagu toote sissetuleku numbrid ja hankija arve numbrid. Need testid jätkavad tööd sama andmebaasiga uuesti ja uuesti, nõudmata taastamist.
    - Määrake alati keskkonna **Redigeerimise režiim**, et **lugeda** või **redigeerida** esimese testi juhtumina, kuna vaikimisi on suvand **Automaatne**.**Automaatne** suvandid kasutavad alati eelmist sätet ja võivad põhjustada ebausaldusväärseid teste. 
 
    [![Suvandite leht, jõudluse vahekaart.](./media/rsat-data-agnostic-testing-02.PNG)](./media/rsat-data-agnostic-testing-02.PNG)
 
    - Kinnitage ainult pärast kindla kande filtreerimist üldise kinnitamise asemel. Näiteks kirjete arvu puhul filtreerige kande number või kande kuupäev nii, et kontroll välistab kõik muud kanded. 
    - Kui kontrollite kliendi saldot või eelarvet, salvestage esmalt väärtus ja lisage seejärel oma tehinguväärtus, et kontrollida oodatavat tulemust, kindla eeldatava väärtuse kinnitamise asemel. 
 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
