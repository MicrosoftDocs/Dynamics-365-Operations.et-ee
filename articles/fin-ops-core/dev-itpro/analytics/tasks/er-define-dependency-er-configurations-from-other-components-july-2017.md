---
title: ER-i konfiguratsioonide sõltuvuse määramine teistest komponentidest
description: Selles teemas kirjeldatase, kuidas kujundada elektroonilise aruandluse (ER) konfiguratsiooni ja määrata selle sõltuvus teistest tarkvarakomponentidest.
author: NickSelin
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e4aef052a77428bb783a3a098754ca4dcc1b4296
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755102"
---
# <a name="define-the-dependency-of-er-configurations-on-other-components"></a>ER-i konfiguratsioonide sõltuvuse määramine teistest komponentidest

[!include [banner](../../includes/banner.md)]

Toimingute teostamiseks peate esmalt läbima tegevusjuhises toodud ja ER-i mudelihalduse vastendamise konfiguratsioonide etapid ning teil peab olema juurdepääs teenusele Microsoft Dynamics Lifecycle Services (LCS).

Järgmises protseduuris kirjeldatakse elektroonilise aruandluse (ER) konfiguratsiooni kavandamist ja selle teistest tarkvarakomponentidest sõltuvuse määramist tagamaks, et konfiguratsioon laaditaks õigesti alla rakenduse Finance and Operations, Enterprise Edition kindlale versioonile. Selles näites loote näidisettevõtte Litware, Inc jaoks vajalikud elektroonilise aruandluse konfiguratsioonid. 

Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll. Neid etappe võib teha igas ettevõttes, kuna ER-i konfiguratsioonid on kõigi ettevõtete vahel ühiskasutuses. 

1. Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.
    * Veenduge, et konfiguratsioonide puu sisaldab konfiguratsiooni „Näidisandmemudel" ja alamkaupu. Muul juhul toimige vastavalt tegevuse juhise „ER Mudelivastenduste konfiguratsioonide haldamine” juhistele ja käivitage see juhis uuesti.   

## <a name="define-the-dependency-of-er-configurations-from-other-components"></a>ERi konfiguratsioonide teistest komponentidest sõltuvuse määramine
1. Laiendage puul valikut „Sample data model".
2. Tehke puul valik "Näidisandmemudel\Näidisvastendus".
    * Valisime mudelivastenduse konfiguratsiooni „Näidisvastendus" mustandiversiooni. Nüüd määratleme selle sõltuvuse muudest tarkvarakomponentidest. Seda toimingut peetakse eeltingimuseks konfiguratsiooni versiooni allalaadimise kontrollimiseks ER-i hoidlast ja selle versiooni edasiseks kasutamiseks.   
3. Laiendage jaotist Eeltingimused.
    * Pange tähele, et „Juurutuste” eeltingimuste grupp on sellesse etappi lisatud automaatselt. See grupp sisaldab eeltingimuse komponenti, mis viitab andmemudeli konfiguratsioonile ning selle juurutuse lipp on sisse lülitatud. See lipp näitab, et „Näidisvastendamise” vastenduskonfiguratsiooni peetakse andmemudeli „Näidisandmemudel" juurutamiseks. See komponent sunnib elektroonilist aruandlust alla laadima vastenduse konfiguratsiooni „Näidisvastendus” elektroonilise aruandluse hoidlast, kui mudeli konfiguratsioon „Näidisandmemudel" on alla laaditud.   
4. Klõpsake nuppu Redigeeri.
    * Konfiguratsiooni praeguse versiooni ühekordne sõltuvust tarkvarakomponendist saab määratleda, kui kasutada komponendi tüübi definitsiooni ja kas komponendi versiooni või komponentide versioonide vahemikku.  
    * Soovitud sõltuvusi saab kokku grupeerida. Kui valida grupeerimistüüp „Kõik”, peetakse selle grupi sõltuvustingimust täidetuks, kui iga selle grupi ja alamgrupi sõltuvustingimus on täidetud. Kui valida grupeerimistüüp „Üks valitutest”, peetakse selle grupi sõltuvustingimus täidetuks, kui vähemalt üks selle grupi ja alamgrupi sõltuvustingimus on täidetud.   
5. Klõpsake valikut Uus.
6. Valige toote eeltingimuse komponent.
7. Valige Microsoft Dynamics 365 for Operations (1611).
8. Sisestage versiooniväljale väärtus „[7.1.1541.3036,8)”.
    * [7.1.1541.3036,8)  
    * Sisestatud sõltuvusi hinnatakse, kui see konfiguratsioon on ER-i hoidlast alla laaditud. See konfiguratsiooni versioon laaditakse ER-i hoidlast alla, kui konfiguratsiooni „Näidisandmemudel” 1. versioon on juba olemas või eelnevalt alla laaditud. Kui see on eelnevalt alla laaditud, tuleb see lõpule viia rakenduse Finance and Operations versioonis 7.1.1541.3036 või uuemas, kuid see ei tohi ületada põhiversiooni 8.   
9. Klõpsake nuppu Salvesta.
10. Sulgege leht.
11. Klõpsake valikut Muuda olekut.
12. Klõpsake valikut Valmis.
13. Klõpsake nuppu OK.
14. Tehke puul valik „Näidisandmemudel\Näidisvastendamine (alternatiivne)".
15. Klõpsake nuppu Redigeeri.
16. Klõpsake valikut Uus.
17. Valige toote eeltingimuse komponent.
18. Valige Microsoft Dynamics AX 7.0 RTW.
19. Sisestage versiooniväljale väärtus „[7.0.1265.3015,7.1)”.
    * [7.0.1265.3015,7.1)  
    * Sõltuvusi hinnatakse, kui see konfiguratsioon on ER-i hoidlast alla laaditud. See konfiguratsiooni versioon laaditakse ER-i hoidlast alla, kui konfiguratsiooni „Näidisandmemudel” 1. versioon on juba olemas või eelnevalt alla laaditud. Kui see on eelnevalt alla laaditud, tuleb see lõpule viia rakenduses Microsoft Dynamics 365 for Finance and Operations Enterprise Editionis, mis peab olema 7.0.1265.3015 või uuem versioon, kuid mis ei tohi ületada lühiversiooni 1.   
20. Klõpsake nuppu Salvesta.
21. Sulgege leht.
22. Klõpsake valikut Muuda olekut.
23. Klõpsake valikut Valmis.
24. Klõpsake nuppu OK.

## <a name="configure-the-er-repository"></a>ER-i hoidla konfigureerimine
1. Sulgege leht.
2. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
    * Avage ER-i hoidlate loend praeguse ER-i pakkuja, ettevõtte Litware, Inc. jaoks.  
3. Märkige loendis valitud rida.
4. Klõpsake valikut Hoidlad.
5. Klõpsake suvandit Näita filtreid.
6. Sisestage filtrioperaatori „contains” abil filtriväärtus „LCS" väljale „Type name”.
    * LCS-i hoidla on praeguse ER-i pakkuja jaoks juba registreeritud ja te võite selle alamülesande järgmised toimingud vahele jätta. Kui LCS-hoidla pole veel registreeritud, täitke ka ülejäänud juhised.   
7. Klõpsake valikut Lisa rippdialoogi avamiseks.
8. Sisestage väljale Konfiguratsioonihoidla tüüp valik LCS.
9. Klõpsake käsku Loo hoidla.
10. Valige või sisestage väärtus väljal Projekt.
    * Valige välja „Projekt” otsingust soovitud LCS-projekt.  
11. Klõpsake nuppu OK.
12. Sulgege leht.

## <a name="upload-configurations-to-lcs"></a>Konfiguratsioonide üleslaadimine LCS-i
1. Klõpsake valikut Aruandluse konfiguratsioonid.
2. Tehke puul valik „Sample data model".
3. Valige selle konfiguratsiooni lõpuleviidud versioon.
4. Klõpsake valikut Muuda olekut.
5. Klõpsake nuppu Jaga.
6. Klõpsake nuppu OK.
    * Selle mudelikonfiguratsiooni 1. versioon on LCS-i üles laaditud eelnevalt konfigureeritud ER-i hoidla LCS-projekti jaoks.   
7. Laiendage puul valikut „Sample data model".
8. Tehke puul valik "Näidisandmemudel\Näidisvastendus".
9. Valige selle konfiguratsiooni lõpuleviidud versioon.
10. Klõpsake valikut Muuda olekut.
11. Klõpsake nuppu Jaga.
12. Klõpsake nuppu OK.
    * Selle mudelivastenduskonfiguratsiooni 1.1. versioon on LCS-i üles laaditud eelnevalt konfigureeritud ER-i hoidla LCS-projekti jaoks.   
13. Tehke puul valik „Näidisandmemudel\Näidisvastendamine (alternatiivne)".
14. Valige selle konfiguratsiooni lõpuleviidud versioon.
15. Klõpsake valikut Muuda olekut.
16. Klõpsake nuppu Jaga.
17. Klõpsake nuppu OK.
    * Selle mudelivastenduskonfiguratsiooni 1.1. versioon on LCS-i üles laaditud eelnevalt konfigureeritud ER-i hoidla LCS-projekti jaoks.   

## <a name="evaluate-er-configuration-dependencies"></a>ER-i konfiguratsioonide sõltuvuste hindamine
Kustutame süsteemist loodud konfiguratsioonid ja laadime need uuesti alla LCS-i hoidlast.  
1. Tehke puul valik "Näidisandmemudel\Näidisvastendus".
2. Klõpsake Kustuta.
3. Klõpsake nuppu Jah.
4. Tehke puul valik „Näidisandmemudel\Näidisvastendamine (alternatiivne)".
5. Klõpsake Kustuta.
6. Klõpsake nuppu Jah.
7. Tehke puul valik „Näidisandmemudel\Näidisformaat".
8. Klõpsake Kustuta.
9. Klõpsake nuppu Jah.
10. Tehke puul valik „Sample data model".
11. Klõpsake Kustuta.
12. Klõpsake nuppu Jah.
13. Sulgege leht.
    * Avage ER-i hoidlate loend praeguse ER-i pakkuja, ettevõtte Litware, Inc. jaoks.  
14. Klõpsake valikut Hoidlad.
15. Klõpsake suvandit Näita filtreid.
16. Sisestage filtrioperaatori „contains” abil filtriväärtus „LCS" väljale „Type name”.
17. Klõpsake valikut Ava.
18. Tehke puul valik „Sample data model".
    * Pange tähele, et saate vaadata hinnangut selle kohta, kas praeguse hoidla ER-konfiguratsiooni versiooni eeltingimused on täidetud. Hinnangu vaatamiseks klõpsake valikut Kontrolli eeltingimusi.   
19. Klõpsake valikut Kontrolli eeltingimusi.
20. Klõpsake Import.
21. Klõpsake nuppu Jah.
22. Sulgege leht.
23. Sulgege leht.
24. Sulgege leht.
25. Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.
26. Laiendage puul valikut „Sample data model".
    * Pange tähele, et mudeli „Näidisvastendamine" vastenduskonfiguratsioon on alla laaditud koos valitud andmemudeli konfiguratsiooniga. Kaks faili laaditi koos alla, kuna „Näidisvastendus" on määratletud valitud andmemudeli juurutamisena ja kuna see kehtib rakenduse kohta. Konfiguratsiooni „Näidisvastendus (alternatiivne)” pole alla laaditud, kuna nõutava avalduse versiooni tingimust pole täidetud.   
    * Kui logite sisse Finance and Operationsi, registreerige sama pakkuja, avage sama LCS-projekt ja laadige alla sama andmemudeli konfiguratsioon. Konfiguratsioon „Näidisvastendus (alternatiivne)” laaditakse alla, aga konfiguratsioon „Näidisvastendus” jäetakse vahele.  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]