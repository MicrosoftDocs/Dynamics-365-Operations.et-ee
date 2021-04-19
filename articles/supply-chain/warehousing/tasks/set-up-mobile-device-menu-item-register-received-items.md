---
title: Mobiilse seadme menüükäsu seadistamine saabunud kaupade registreerimiseks
description: See teema keskendub mobiilse seadme menüü-üksuse seadistamisele.
author: ShylaThompson
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFMenu, WHSRFDefaultData
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dfe068bd964f31b77e30b34ef20c2b0f70ed6238
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830782"
---
# <a name="set-up-a-mobile-device-menu-item-to-register-received-items"></a>Mobiilse seadme menüükäsu seadistamine saabunud kaupade registreerimiseks

[!include [banner](../../includes/banner.md)]

See teema keskendub mobiilse seadme menüü-üksuse seadistamisele. Seda menüü-üksust kasutatakse ostutellimuste kaudu tellitud kaupade vastuvõtu registreerimiseks. 

Saate seda juhendit kasutada demoettevõtte USMF andmetega. See protseduur on mõeldud laohaldurile.


## <a name="create-a-mobile-device-menu-item"></a>Mobiilse seadme menüü-üksuse loomine
1. Avage Navigeerimispaneel > **Moodulid > Laohaldus > Seadistus > Mobiilne seade > Mobiilse seadme menüü-üksused.**
2. Valige suvand **Uus**.
3. Sisestage väärtus väljale **Menüü-üksuse nimi**. See on selle mobiilse seadme menüü-üksuse ainuidentifikaator. Näiteks võite sisestada `My PO registration`.  
4. Sisestage väärtus väljale **Pealkiri**. See on pealkiri, mis kuvatakse kasutajale mobiilses seadmes. Näiteks võite sisestada `PO registration`.  
5. Valige väljal **Režiim** suvand **Töö**. Ostutellimuse rea jaoks vastu võetud vaba kaubavaru koguste registreerimine loob töö kaupade teisaldamiseks vastuvõtualast varudesse. Tööd ei looda enne, kui kaubad on registreeritud. Seetõttu jätke suvandi **Kasuta** olemasolevat tööd sätteks **Ei**.
6. Valige jaotise **Üldine** väljal **Töö loomise protsess**, **Ostutellimuse objekt saab**.
    - Ostutellimuse rida peab olema üheselt identifitseeritud, enne kui vaba kaubavaru saab laos registreerida. Selles stsenaariumis registreerib mobiilne seade ostutellimuse numbri ja kaubakoodi ning see võimaldab süsteemil tuvastada ostutellimuse rea. Luuakse paigutamistöö ja selle saab võtta teine töötaja. Teie valitud töö loomise meetod määrab, millised väljad muutuvad **Üldist** FastTabis kättesaadavaks.  
    - Kui valite suvandi **Kasuta vaikemisi andmeid**, on nupp **Vaikeandmed** sisse lülitatud. siin saate valida väljad nende andmete kuvamiseks, mida töötajal enamasti igapäevases töös vaja läheb, nii et need väärtused kuvatakse mobiilses seadmes.  
    - Parameeter **Numbrimärkide rühmitus** töötab koos ühikute seeriagrupiga, mis on määratud vastuvõetavale üksusele. Saate määrata, kas vähema või rohkema kui ühe kaubaaluse sissetulekud rühmitatakse ühele litsentsiplaadile või luuakse iga ühiku kohta eraldi litsentsiplaat.  
    - Kui valite valiku **Genereeri numbrimärk**, genereerib see numbrijadade valiku põhjal kordumatu numbrimärgi numbri.  
    - Saate valida malli, mida kasutatakse töö loomisel. Näiteks kui registreerite ostutellimuse jaoks kauba, luuakse töömalli alusel paigutamistöö. Kui te siin töömalli ei vali, määrab süsteem malli mallidega seostatud päringukriteeriumite alusel.  
    - Kui mobiilses seadmes kuvatakse likvideerimiskoodid, saavad töötajad hinnata kaupade olekut või kvaliteeti ja valida sobiva koodi. Likvideerimiskoodi reeglid määratlevad, kas kaup on saadaval teiste laoprotsesside jaoks. Reeglid määratlevad ka selle, millist asukohakorraldust loodud töö jaoks kasutatakse.   
    - Kui valite valiku **Partii dispositsiooni koodid**, saavad töötajad hinnata partii olekut või kvaliteeti ja valida sobiva dispositsiooni koodi. Partii likvideerimiskoodile määratud reeglid määratlevad, kas partii on saadaval teiste laoprotsesside jaoks.  
    - Kui valite suvandi **Prindi sildid**, prinditakse numbrimärgi sildid objektide vastuvõtmisel automaatselt.  
7. Valige käsk **Salvesta**.
8. Sulgege leht.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Menüü-üksuse lisamine mobiilse seadme menüüsse
1. Avage Navigeerimispaneel > **Moodulid > Laohaldus > Seadistus > Mobiilne seade > Mobiilse seadme menüü-üksused.**
2. Kasutage **Kiirfiltrit**, et filtreerida väljal **Nimi** väärtusega '`inbound`.
3. Valige suvand **Redigeeri**.
4. Valige puul Saadaolevad menüüd ja üksused varem loodud menüü-üksus.
5. Klõpsake paremale suunatud noolt.
6. Valige käsk **Salvesta**.
7. Sulgege leht.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]