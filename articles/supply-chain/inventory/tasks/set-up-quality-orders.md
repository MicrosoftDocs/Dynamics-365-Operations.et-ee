---
title: Kvaliteettellimuste seadistamine
description: "See protseduur näitab teile, kuidas lubada kvaliteedijuhtimise protsess, kui sissetulevaid varusid tuleb kontrollida kohe pärast saabumise registreerimist."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 0bd8bc73a3cbb42cb7e6d42a07d58c0b02673ba1
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-quality-orders"></a>Kvaliteettellimuste seadistamine

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab teile, kuidas lubada kvaliteedijuhtimise protsess, kui sissetulevaid varusid tuleb kontrollida kohe pärast saabumise registreerimist. Protseduuri täidab üldjuhul kvaliteedijuht. Protsess hõlmab kvaliteedigrupi loomist näidise võtmiseks kasutatavate kaupade määratlemiseks ja katsegrupi loomist kvaliteedigrupi kaupade puhul tehtavate katsete grupeerimiseks. Saate seda juhendit käitada demoettevõtte USMF andmetega.


## <a name="enable-quality-management"></a>Kvaliteedijuhtimise lubamine
1. Avage Varude haldus > Seadistus > Varude ja lao halduse parameetrid.
2. Klõpsake vahekaarti Kvaliteedijuhtimine.
3. Määrake suvandi Kasuta kvaliteedijuhtimist sätteks Jah.
4. Klõpsake suvandit Aruande seadistus.
    * USMF-is on kvaliteedijuhtimise aruande seadistus juba määratletud. Kui seda pole tehtud, tuleks lisada siia uued read erinevate aruandetüüpide jaoks ja valida iga aruande jaoks kasutatav dokumenditüüp.  
5. Sulgege leht.
6. Sulgege leht.

## <a name="create-a-test"></a>Katse loomine
1. Avage Varude haldus > Seadistus > Kvaliteedijuhtimine > Katsed.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Katse.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Valige väljalt Tüüp valik Suvand.
    * Selles näites valime valiku Suvand, mis võimaldab määrata katsetulemused eelmääratletud väärtuste alusel.  
6. Klõpsake nuppu Salvesta.
7. Sulgege leht.

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a>Katse muutujate loomine katsetulemuste salvestamise viisi määratlemiseks
1. Avage Varude haldus > Seadistus > Kvaliteedijuhtimine > Katse muutujad.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Muutuja.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Klõpsake nuppu Salvesta.
6. Klõpsake suvandit Tulemused.
7. Klõpsake valikut Uus.
8. Sisestage väärtus väljale Tulemus.
9. Sisestage väljale Kirjeldus soovitud väärtus.
10. Valige väljalt Tulemuse olek suvand Läbinud.
11. Klõpsake nuppu Salvesta.
12. Klõpsake valikut Uus.
13. Sisestage väärtus väljale Tulemus.
14. Sisestage väljale Kirjeldus soovitud väärtus.
15. Klõpsake nuppu Salvesta.
16. Sulgege leht.
17. Sulgege leht.

## <a name="set-up-item-sampling"></a>Kauba valimi seadistamine
1. Avage Varude haldus > Seadistus > Kvaliteedijuhtimine > Kaubanäidised.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Kauba valim.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Sisestage number väljale Väärtus.
    * See väärtus on seotud kõrvalväljal valitud koguse spetsifikatsiooniga.  
6. Laiendage või ahendage jaotist Protsess.
7. Märkige või tühjendage ruut Täielik blokeerimine.
    * Selle suvandi valimisel blokeeritakse katse nurjumisel kogu saatepartii või tellimuse rea kogus. Selle mittevalimisel blokeeritakse ainult kvaliteettellimuse kaubad.  
8. Klõpsake nuppu Salvesta.
9. Sulgege leht.

## <a name="create-a-quality-group"></a>Kvaliteedigrupi loomine
1. Avage Varude haldus > Seadistus > Kvaliteedijuhtimine > Kvaliteedigrupid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Kvaliteedigrupp.
    * Kasutage kirjeldavat nime, mis aitab teil tuvastada, millist tüüpi kaupu grupp sisaldab (valimi kriteeriumid).  
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Klõpsake nuppu Salvesta.
6. Klõpsake käsku Lisa kaupu.
7. Kaubakoodi rea valimine
    * Selles näites käivitatakse filtrimine kaubakoodi põhjal.  
8. Sisestage väärtus väljale Kriteeriumid.
    * Näiteks sisestage T* kaubakoodide filtrimiseks, mis algavad T-ga.  
9. Klõpsake nuppu OK.
10. Klõpsake nuppu OK.
11. Klõpsake suvandit Kauba kvaliteedigrupid.
12. Sulgege leht.
13. Sulgege leht.

## <a name="create-a-test-group"></a>Katsegrupi loomine
1. Avage Varude haldus > Seadistus > Kvaliteedijuhtimine > Katsegrupid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Katsegrupp.
    * Andke katsegrupile nimi, mis aitab teil meeles pidada, milliseid katseid tehakse ja millise kvaliteedigrupiga peaks need seostatud olema. Näiteks kui seda kasutatakse kvaliteedigrupiga, mis valib T-ga algavaid kaupu, võite selle nimeks panna T-kauba katsed.  
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Valige väljalt Kauba näidised varem loodud kauba näidiste rida.
6. Otsige loendist ja valige soovitud kirje.
7. Klõpsake vahekaarti Lisa.
8. Sisestage number väljale Seerianumber.
9. Valige väljalt Katse varem loodud katse.
10. Otsige loendist ja valige soovitud kirje.
11. Klõpsake vahekaarti Katsetamine.
12. Valige väljalt Muutuja varem loodud katse muutuja.
13. Otsige loendist ja valige soovitud kirje.
14. Klõpsake väljal Vaiketulemus otsingu avamiseks ripploendi nuppu.
15. Klõpsake loendis valitud real olevat linki.
16. Klõpsake nuppu Salvesta.
17. Sulgege leht.

## <a name="define-when-quality-orders-will-be-created"></a>Kvaliteettellimuste loomise aja määratlemine
1. Avage Varude haldus > Seadistus > Kvaliteedijuhtimine > Kvaliteediseosed.
2. Klõpsake valikut Uus.
3. Valige suvand väljalt Viite tüüp.
4. Valige väljalt Kaubakood suvand Grupp.
    * Selles näites valime suvandi Grupp ja kasutame varem loodud kvaliteedigruppi. Võite selle seada ka valikule Tabel, et määrata kaupu käsitsi, või valida suvandi Kõik kõikide kaupade lisamiseks kvaliteettellimusse.  
5. Valige väljalt Kaup varem loodud kvaliteedigrupp.
    * Väljal Kaup saadaolevad suvandid olenevad sellest, mille määrate väljal Kauba kood.  
6. Otsige loendist ja valige soovitud kirje.
7. Laiendage või ahendage jaotist Protsess.
8. Valige suvand väljalt Sündmuse tüüp.
    * See on katse käivitav sündmus. Siin saadaolevad suvandid olenevad protsessist, mille valisite väljal Viite tüüp.  
9. Valige suvand väljalt Käivitamine.
10. Laiendage või ahendage jaotist Kvaliteettellimuse protsess.
11. Klõpsake väljal Sündmuse blokeerimine otsingu avamiseks ripploendi nuppu.
    * Sellel väljal kuvatakse protsesside loend, mida on võimalik blokeerida, kui kvaliteettellimus on veel avatud. Suvandid olenevad sellest, mille valisite väljal Sündmuse tüüp.  
12. Klõpsake loendis valitud real olevat linki.
    * See oleneb eelmistest valitud väärtustest. Valige, kui blokeerida tuleb järgmised protsessid, kui lähtedokumendi reaga on seotud avatud kvaliteettellimused.  
13. Laiendage või ahendage jaotist Tehnilised andmed.
14. Valige väljalt Katsegrupp varem loodud katsegrupp.
15. Otsige loendist ja valige soovitud kirje.
16. Klõpsake nuppu Salvesta.
17. Sulgege leht.

