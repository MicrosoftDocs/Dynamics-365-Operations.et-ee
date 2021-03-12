---
title: Min-max täiendamisprotsessi seadistamine
description: Selles protseduuris kirjeldatakse, kuidas seadistada uut täiendamisprotsessi, mis kasutab minimaalse/maksimaalse täiendamise strateegiat.
author: perlynne
manager: tfehr
ms.date: 10/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, InventItemIdLookupSimple, WMSLocationIdLookup, WHSLocDirTable, InventLocationIdLookup, SysQueryForm, WHSWorkTemplateTable, WHSReplenishmentTemplates, UnitOfMeasureLookup, SysQueryTableLookUp, SysQueryFieldLookUp, SysRecurrence, WHSInventFixedLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e14614829f414bc9063b84ec848816e77dbd571a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976934"
---
# <a name="set-up-a-min-max-replenishment-process"></a>Min-max täiendamisprotsessi seadistamine

[!include [banner](../../includes/banner.md)]

Selles protseduuris kirjeldatakse, kuidas seadistada uut täiendamisprotsessi, mis kasutab minimaalse/maksimaalse täiendamise strateegiat. Kui varud jäävad allapoole minimaalset taset, luuakse töö asukoha täiendamiseks. Protseduur näitab ka seda, kuidas kasutada fikseeritud komplekteerimise asukohti, et lubada uuesti täiendamist isegi siis, kui varud jäävad allapoole minimaalset taset, ja, kuidas lubada täiendamisprotsessi regulaarset käitamist, kasutades pakett-tööd. Neid ülesandeid täidab üldjuhul laohaldur. Saate seda protseduuri käitada USMF-i demoandmete ettevõttes, kasutades allpool olevaid näidisväärtusi, või käitada seda oma andmetega. Kui kasutate oma andmeid, veenduge, et teil on ladu, mis on laohaldusprotsessideks lubatud.


## <a name="create-a-fixed-picking-location"></a>Fikseeritud komplekteerimise asukoha loomine
1. Avage **Navigeerimispaan > Moodulid > Laohaldus > Seadistus > Ladu > Fikseeritud asukohad**. See on valikuline ülesanne miinimumi-maksimumi täiendamiseks, kuid kui kasutate fikseeritud komplekteerimise asukohta, võimaldab see varude täiendamist, isegi kui see langeb allapoole minimaalset taset, kuna süsteem suudab määrata, milliseid kaupu on vaja täiendada, isegi, kui ühtki kaupa pole alles.
2. Klõpsake valikut **Uus**.
3. Sisestage või valige väärtus väljale **Kauba kood**. USMF-i kasutamisel saate valida kauba A0001.  
4. Sisestage või valige väärtus väljale **Sait**. Kui te kasutate USMF-i, saate valida saidi 2.  
5. Sisestage või valige väärtus väljale **Ladu**. Kui kasutate USMF-i, saate valida lao 24.  
6. Sisestage või valige väärtus väljal **Asukoht**. Kui kasutate USMF-i, saate teha valiku CP-003.  
7. Sulgege leht.

## <a name="create-a-replenishment-location-directive"></a>Täiendamise asukohakorralduse loomine
1. Avage **Laohaldus > Seadistus > Asukohakorraldused.** Asukohakorraldusi kasutatakse, et määrata, kus tuleb kaubad täiendamisprotsessiks komplekteerida.
2. Tehke väljal **Töötellimuse tüüp** valik Täiendamine.
3. Klõpsake **tegumiribal** valikut **Uus**.
4. Sisestage väärtus väljale **Nimi**.
5. Tehke väljal **Töö tüüp** valik Komplekteeri.
6. Sisestage või valige väärtus väljale **Sait**. Kui te kasutate USMF-i, saate valida saidi 2.  
7. Sisestage või valige väärtus väljale **Ladu**. Kui kasutate USMF-i, saate valida lao 24.  
8. Klõpsake valikut **Salvesta**.
9. Jaotises **Read** klõpsake valikut **Uus**.
10. Märkige loendis valitud rida.
11. Sisestage arv väljale **Kuni koguseni**. Näiteks saate määrata väärtuseks 9999.  
12. Valige märkeruut **Luba tükeldamine**. Kui valite selle suvandi, lubab töö loomise protsess töö rea koguste tükeldamist mitme asukoha vahel.  
13. Klõpsake valikut **Salvesta**.
14. Jaotises **Asukohakorralduse tegevused** klõpsake valikut **Uus**.
15. Märkige loendis valitud rida.
16. Sisestage väärtus väljale **Nimi**.
17. Klõpsake valikut **Salvesta**.
18. Klõpsake **Tegumiribal** käsku **Päringu redigeerimine**. Saate seda päringut redigeerida piirangute lisamiseks juhul, kui varusid saab valida täiendamisprotsessis. Näiteks võib juhtuda, et tuleb kasutada varusid ainult lao hulgialalt.
19. Klõpsake valikut **OK**.
20. Sulgege leht.

## <a name="create-a-replenishment-work-template"></a>Täiendamise töömalli loomine
1. Avage **Laohaldus > Seadistus > Töö > Töömallid**. Töömalli kasutatakse selleks, et juhendada süsteemi, kuidas tuleb min/max-täiendustööd luua. Minimaalselt peab olema töömalli rida komplekteerimiseks ja paigutamiseks. Töömalli kohta öeldakse, et see on kehtetu, kuni kogu vajalik teave on sisestatud. 
2. Tehke väljal **Töötellimuse tüüp** valik Täiendamine.
3. Klõpsake **tegumiribal** valikut **Uus**.
4. Sisestage väärtus välja **Töömall**.
5. Klõpsake valikut **Salvesta**.
6. Klõpsake jaotises **Töömalli üksikasjad** valikut **Uus**.
7. Tehke väljal **Töö tüüp** valik Komplekteeri.
8. Väljal **Tööklassi ID** sisestage või valige väärtus. See peaks olema tööklass, mis on seotud varude täiendamisega. Kui kasutate USMF-i, tehke valik Täienda.  
9. Klõpsake jaotises **Töömalli üksikasjad** valikut **Uus**.
10. Märkige loendis valitud rida.
11. Valige väljal **Töö tüüp** suvand Pane.
12. Väljal **Tööklassi ID** sisestage või valige väärtus.
13. Klõpsake valikut **Salvesta**.
14. Sulgege leht.

## <a name="create-a-new-replenishment-template"></a>Uue täiendamismalli loomine
1. Avage **Laohaldus > Seadistus > Täiendamine > Täiendamise mallid**. Täiendamismalli kasutatakse selleks, et määratleda kaubad ja kogused ning täiendamise asukoht.
2. Klõpsake **tegumiribal** valikut **Uus**.
3. Tippige väärtus väljale **Täiendamismall**. Andke mallile nimi, mis näitab, et see on mõeldud min/max-täiendamiseks.  
4. Sisestage väärtus väljale **Kirjeldus**.
5. Valige märkeruut **Voo nõudel reserveerimata koguste kasutamise lubamine**. Kui valite selle suvandi, võimaldab see voo nõudluse täiendamisel tarbida koguseid, mis on seotud min/max-täiendamisega. Näiteks võib see olla kasulik, kui min/max-täiendustööd ei tehta kohe, et vältida soovimatute nõudluse täiendustööde loomist.
6. Klõpsake jaotises **Täiendamise malli üksikasjad** valikut **Uus**.
7. Sisestage arv väljale **Järjekorranumber**.
8. Sisestage väärtus väljale **Kirjeldus**.
9. Märkige loendis valitud rida.
10. Sisestage või valige väärtus väljal **Täiendamise ühik**. Valige näiteks tk. See säte on kohustuslik. See võimaldab teil määrata täiendamistööle erinevad mõõtühikud võrreldes ühikuga, mis on määratud selle malli minimaalse ja maksimaalse laoseisu tasemetele.
11. Sisestage või valige väärtus väljal **Töömall**. Valige töömall, mille lõite varem.  
12. Sisestage number väljale **Miinimumkogus**. Valige miinimumkogus, mis peaks täiendamise käivitama. Määrake väärtuseks näiteks 50. On võimalik jätta selleks väärtuseks null, kui täiendate fikseeritud asukohta ja kui suvand **Täienda varusid tühjades fikseeritud asukohtades** on seatud väärtusele Jah. Samuti soovitame valida suvandi **Täienda varusid ainult fikseeritud asukohtades** jõudluspõhjustel.
13. Sisestage number väljale **Maksimumkogus**. Valige väärtuseks näiteks 100.  
14. Sisestage või valige väärtus väljal **Ühik**. Määrake ühik minimaalsetele ja maksimaalsetele kogustele. Näiteks saate määrata selleks tk.  
15. Valige märkeruut **Täienda varusid tühjades fikseeritud asukohtades**. Valige see märkeruut, et täiendada fikseeritud asukohti, kui need on tühjad. Vastasel juhul täidetakse ainult asukohti, kus on laokogus olemas.
16. Valige märkeruut **Täienda varusid ainult fikseeritud asukohtades**.
17. Klõpsake suvandit **Vali tooted**. See on koht, kus määratleda, milliseid tooteid tuleb täiendada. Kui valitud on suvand Fikseeritud komplekteerimiskohad, peate määratlema ka selle päringu asukohad. Saadaval on nii variandipõhised kui ka tootepõhised päringud.
18. Valige suvand **Kaupade** rida.
19. Sisestage väärtus väljale **Kriteerium**. Valige kaubad, mida tuleks täiendada fikseeritud asukohtades. Tippige näiteks tüüp A*, et valida kõik kauba numbrid, mis algavad tähega A.
20. Klõpsake käsku **Lisa**. Lisage asukoha üksus (välja arvatud juhul, kui see on juba olemas), et piirata täiendustööd fikseeritud komplekteerimiskohtedega teatud laoalal.
21. Märkige loendis valitud rida.
22. Määrake välja **Tabel** olekuks Asukohad.
23. Tehke väljal **Väli** valik Asukoha profiili ID.
24. Sisestage või valige väärtus väljal **Kriteeriumid**.
25. Klõpsake valikut **OK**.
26. Sulgege leht.

## <a name="set-the-replenishment-process-to-run-as-a-batch-job"></a>Täiendamisprotsessi pakett-tööna käitamise seadistamine
1. Avage **Laohaldus > Täiendamine > Täiendamised**. Lehel Täiendused saate seadistada täiendamise käitamise pakett-tööna või nõuda, et see käivitataks käsitsi.
2. Klõpsake käsku **Filtreeri**.
3. Märkige loendis valitud rida.
4. Sisestage või valige väärtus väljal **Kriteeriumid**.
5. Klõpsake valikut **OK**.
6. Laiendage jaotist **Käivita taustal**.
7. Määrake suvandi **Pakktöötlus** väärtuseks Jah.
8. Klõpsake valikul **Korduvus**.
9. Valige suvand **Lõppkuupäev puudub**.
10. Määrake **kordumismuster**. Valige näiteks päevad.  
11. Klõpsake valikut **OK**.
12. Klõpsake valikut **OK**.

