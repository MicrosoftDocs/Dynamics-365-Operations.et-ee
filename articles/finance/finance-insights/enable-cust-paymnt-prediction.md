---
title: Kliendimaksete prognoosimise lubamine
description: Selles teemas selgitatakse, kuidas lülitada sisse ja konfigureerida finantsülevaadetes kliendimakse prognooside funktsioon.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: b83d1230c94462ca722ad7ceb7b2185afd636aae
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109600"
---
# <a name="enable-customer-payment-predictions"></a>Kliendimaksete prognoosimise lubamine

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas lülitada sisse ja konfigureerida finantsülevaadetes kliendimakse prognooside funktsioon. Lülitate funktsiooni sisse funktsioonihalduse tööruumis **ja** sisestate konfiguratsioonisätted finantsülevaate **konfiguratsioonilehele**. See teema sisaldab ka teavet, mis võib aidata teil funktsiooni tõhusalt kasutada.

> [!NOTE]
> Enne järgmiste etappide täitmist täitke kindlasti eeltingimuse etapid jaotises [Finantsülevaadete konfigureerimine](configure-for-fin-insites.md).

1. Lülitage kliendi makseprognooside funktsioon sisse:

    1. Avage tööruum **Funktsioonihaldus**.
    2. Valige **Otsi värskendusi**.
    3. Otsige vahekaardil **Kõik** kliendi **makseprognoose**. Kui te seda funktsiooni ei leia, otsige (eelvaade **) kliendi makseprognoose**. 
    4. Lülitage funktsioon sisse.

    Kliendi makseennustused on nüüd sisse lülitatud ja konfigureerimiseks valmis.

2. Kliendimaksete ülevaadete funktsiooni konfigureerimine.

    1. Mine kreediti **ja kollektsioonide häälestuse \>\> finantsülevaadete kliendi \> makseprognooside kohta**
    2. Finantsülevaate **konfiguratsioonilehel kliendi** **makse prognooside vahekaardil valige prognoosimudelis** kasutatavate andmeväljade kuvamine **prognoosimudeli** **andmeväljade avamiseks prognoosimudeli lehe** jaoks. Siin saate vaadata väljade vaikeloendit, mida kasutatakse kliendimaksete prognooside jaoks tehisintellekti (AI) prognoosimismudeli loomiseks.

        Ennustuse **·** **·** **·** **mudeli loomiseks väljade vaikeloendi kasutamiseks sulgege prognoosimudeli lehe andmeväljad ja seadke seejärel finantsülevaadete konfiguratsioonilehel suvandi Luba funktsioon väärtuseks Jah.**
        
   > [!NOTE]
   > Kliendi **makseprognooside funktsiooni puhul** on eelmises kuues kuni üheksas kuus vaja üle 100 kande. Kanded võivad sisaldada vabas vormis arveid, müügitellimusi ja kliendimakseid. Need andmed peavad olema laotud üle **on-time**, **Late ja** **Very late** sätted.    
     

    3. Määrake väga hilise kande periood, et määratleda, mida tähendab teie ettevõtte jaoks prognoosisalv **Väga hilja**.

        Iga avatud arve puhul ennustab süsteem makse tõenäosuse kolme salve seast: **õigel ajal**, **hilja** ja **väga hilja**.

        - **Õigel ajal** – see salv hõlmab makseid, mida prognoositakse, et makstakse kande tähtajal või enne seda.
        - **Hilja** – see salv hõlmab makseid, mille maksmine prognoositakse pärast kande tähtaega, kuid enne kande perioodi „väga hilja” algamist.
        - **Väga hilja** – see salv hõlmab makseid, mille maksmine prognoositakse pärast kande perioodi „väga hilja” algamist.

        > [!NOTE]
        > Kui muudate kande perioodi „väga hilja” ja valite suvandi **Hilise lävendi muutmine** pärast seda, kui tehisintellekti prognoosimise mudel on kliendimaksete jaoks on loodud, olemasolev prognoosimise mudel kustutatakse ja luuakse uus mudel. Uus prognoosimise mudel teisaldab kanded perioodile „väga hilja”, mis põhineb selle määratlemiseks sisestatud sätetel.

    4. Kui olete tehingu perioodi „väga hilja” määratlenud, valige prognoosimise mudeli loomiseks suvand **Prognoosimise mudeli loomine**. Finantside **vihjete** konfiguratsioonilehe **ennustuse** mudeli jaotis näitab ennustuse mudeli olekut.

        > [!NOTE]
        > Prognoosimise mudeli loomise ajal saate igal ajal protsessi taaskäivitamiseks valida suvandi **Lähtesta mudeli loomine**.

    Funktsioon on nüüd konfigureeritud ja kasutamiseks valmis.

Kui funktsioon on sisse lülitatud ja konfigureeritud ning ennustuse mudel on loodud ja töötab, **·** **näitab** finantsülevaate parameetrite lehe ennustuse mudeli jaotis mudeli täpsust.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
