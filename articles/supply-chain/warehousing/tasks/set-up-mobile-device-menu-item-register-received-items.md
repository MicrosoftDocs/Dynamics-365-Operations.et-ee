--- 
title: "Mobiilse seadme menüükäsu seadistamine saabunud kaupade registreerimiseks"
description: "See ülesanne keskendub mobiilse seadme menüü-üksuse seadistamisele."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem, WHSRFMenu
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 7b5d757361c1163bbd0300abd3da4e0a2dd6b0e0
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-mobile-device-menu-item-to-register-received-items"></a>Mobiilse seadme menüükäsu seadistamine saabunud kaupade registreerimiseks

[!include [task guide banner](../../includes/task-guide-banner.md)]

See ülesanne keskendub mobiilse seadme menüü-üksuse seadistamisele. Seda menüü-üksust kasutatakse ostutellimuste kaudu tellitud kaupade vastuvõtu registreerimiseks. 

Saate seda juhendit kasutada demoettevõtte USMF andmetega. See protseduur on mõeldud laohaldurile.


## <a name="create-a-mobile-device-menu-item"></a>Mobiilse seadme menüü-üksuse loomine
1. Avage Laohaldus > Seadistus > Mobiilne seade > Mobiilse seadme menüü-üksused.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Menüü-üksuse nimi.
    * See on selle mobiilse seadme menüü-üksuse ainuidentifikaator. Näiteks võite sisestada teksti „Minu ostutellimuse registreerimine”.  
4. Sisestage väärtus väljale Pealkiri.
    * See on pealkiri, mis kuvatakse kasutajale mobiilses seadmes. Näiteks võite sisestada teksti „Ostutellimuse registreerimine”.  
5. Valige väljal Režiim suvand Töö.
    * Ostutellimuse rea jaoks vastu võetud vaba kaubavaru koguste registreerimine loob töö kaupade teisaldamiseks vastuvõtualast varudesse. Tööd ei looda enne, kui kaubad on registreeritud.  Seetõttu jätke suvandi Kasuta olemasolevat tööd sätteks Ei.  
6. Laiendage või ahendage jaotist Üldine.
7. Valige väljal Töö loomise protsess suvand Ostutellimuse kauba vastuvõtmine.
    * Ostutellimuse rida peab olema üheselt identifitseeritud, enne kui vaba kaubavaru saab laos registreerida. Selles stsenaariumis registreerib mobiilne seade ostutellimuse numbri ja kaubakoodi ning see võimaldab süsteemil tuvastada ostutellimuse rea. Luuakse paigutamistöö ja selle saab võtta teine töötaja.    Teie valitud töö loomismeetod määratleb, millised väljad on kiirkaardil Üldine saadaval.  
    * Kui valite suvandi Kasuta vaikeandmeid, lubatakse nupp Vaikeandmed. siin saate valida väljad nende andmete kuvamiseks, mida töötajal enamasti igapäevases töös vaja läheb, nii et need väärtused kuvatakse mobiilses seadmes.  
    * Litsentsiplaadi grupeerimise parameeter toimib koos vastuvõetavale kaubale määratud ühiku seeriagrupiga. Saate määrata, kas vähema või rohkema kui ühe kaubaaluse sissetulekud rühmitatakse ühele litsentsiplaadile või luuakse iga ühiku kohta eraldi litsentsiplaat.  
    * Kui valite suvandi Loo litsentsiplaat, luuakse numbriseeria valiku põhjal kordumatu identifitseerimisnumber.   
    * Saate valida malli, mida kasutatakse töö loomisel. Näiteks kui registreerite ostutellimuse jaoks kauba, luuakse töömalli alusel paigutamistöö. Kui te siin töömalli ei vali, määrab süsteem malli mallidega seostatud päringukriteeriumite alusel.  
    * Kui mobiilses seadmes kuvatakse likvideerimiskoodid, saavad töötajad hinnata kaupade olekut või kvaliteeti ja valida sobiva koodi. Likvideerimiskoodi reeglid määratlevad, kas kaup on saadaval teiste laoprotsesside jaoks. Reeglid määratlevad ka selle, millist asukohakorraldust loodud töö jaoks kasutatakse.   
    * Kui valite suvandi Partii likvideerimiskoodid, saavad töötajad hinnata partii olekut või kvaliteeti ja valida sobiva likvideerimiskoodi.  Partii likvideerimiskoodile määratud reeglid määratlevad, kas partii on saadaval teiste laoprotsesside jaoks.  
    * Kui valite suvandi Prindi sildid, prinditakse kaupade vastuvõtmisel automaatselt litsentsiplaat.  
8. Klõpsake nuppu Salvesta.
9. Sulgege leht.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Menüü-üksuse lisamine mobiilse seadme menüüsse
1. Avage Laohaldus > Seadistus > Mobiilne seade > Mobiilse seadme menüü.
2. Kasutage kiirfiltrit, et filtreerida välja Nimi väärtuse Sissetulev järgi.
3. Klõpsake nuppu Redigeeri.
4. Valige puul suvand „Valige saadaoleva menüü ja kaupade puul varem loodud menüü-üksus.”.
    * Valige varem loodud menüü-üksus.  
5. Klõpsake paremale suunatud noolt.
6. Klõpsake nuppu Salvesta.
7. Sulgege leht.


