---
title: Kvaliteettellimuste seadistamine
description: See protseduur näitab teile, kuidas lubada kvaliteedijuhtimise protsess, kui sissetulevaid varusid tuleb kontrollida kohe pärast saabumise registreerimist.
author: perlynne
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, InventTestTable, DefaultDashboard, InventTestVariable, InventTestVariableOutcome, InventItemSampling, InventTestQualityGroup, InventTestItemQualityGroupAdd, SysQueryForm, InventTestItemQualityGroup, InventTestGroup, InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 875d79e33fbd1d3d811d93dea98fa9d490716744
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011468"
---
# <a name="set-up-quality-orders"></a>Kvaliteettellimuste seadistamine

[!include [banner](../../includes/banner.md)]

See protseduur näitab teile, kuidas lubada kvaliteedijuhtimise protsess, kui sissetulevaid varusid tuleb kontrollida kohe pärast saabumise registreerimist. Protseduuri täidab üldjuhul kvaliteedijuht. Protsess hõlmab kvaliteedigrupi loomist näidise võtmiseks kasutatavate kaupade määratlemiseks ja katsegrupi loomist kvaliteedigrupi kaupade puhul tehtavate katsete grupeerimiseks. Saate seda juhendit käitada demoettevõtte USMF andmetega.


## <a name="enable-quality-management"></a>Kvaliteedijuhtimise lubamine
1. Avage **Navigeerimispaan > Moodulid > Varud > Häälestus > Varude ja laohalduse parameetrid**.
2. Klõpsake vahekaardil **Kvaliteedijuhtimine**.
3. Seadistage suvand **Kasuta kvaliteedihaldust** olekusse „Jah“.
4. Klõpsake **Aruande seadistus**. USMF-is on kvaliteedijuhtimise aruande seadistus juba määratletud. Kui seda pole tehtud, tuleks lisada siia uued read erinevate aruandetüüpide jaoks ja valida iga aruande jaoks kasutatav dokumenditüüp.  
5. Sulgege leht.
6. Sulgege leht.

## <a name="create-a-test"></a>Katse loomine
1. Avage **Varud > Häälestus > Kvaliteedijuhtimine > Katsed**.
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Test**.
4. Sisestage väärtus väljale **Kirjeldus**.
5. Valige suvand väljal **Tüüp**. Selles näites valime valiku Suvand, mis võimaldab määrata katsetulemused eelmääratletud väärtuste alusel.  
6. Klõpsake valikut **Salvesta**.
7. Sulgege leht.

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a>Katse muutujate loomine katsetulemuste salvestamise viisi määratlemiseks
1. Avage **Varud > Häälestus > Kvaliteedijuhtimine > Katse muutujad**.
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Muutuv**.
4. Sisestage väärtus väljale **Kirjeldus**.
5. Klõpsake valikut **Salvesta**.
6. Klõpsake **Tulemused**.
7. Klõpsake valikut **Uus**.
8. Sisestage väärtus väljale **Tulemus**.
9. Sisestage väärtus väljale **Kirjeldus**.
10. Valige väljal **Tulemuse olek** „Läbitud“.
11. Klõpsake valikut **Salvesta**.
12. Klõpsake valikut **Uus**.
13. Sisestage väärtus väljale **Tulemus**.
14. Sisestage väärtus väljale **Kirjeldus**.
15. Klõpsake valikut **Salvesta**.
16. Sulgege leht.
17. Sulgege leht.

## <a name="set-up-item-sampling"></a>Kauba valimi seadistamine
1. Avage **Varud > Häälestus > Kvaliteedijuhtimine > Üksuse diskreetimine**.
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Üksuse diskreetimine**.
4. Sisestage väärtus väljale **Kirjeldus**.
5. Sisestage arv väljale **Väärtus**. See väärtus on seotud kõrvalväljal valitud koguse spetsifikatsiooniga.  
6. Laiendage või ahendage jaotist **Protsess**.
7. Valige või tühjendage märkeruut **Täielik blokeerimine**. Selle suvandi valimisel blokeeritakse katse nurjumisel kogu saatepartii või tellimuse rea kogus. Selle mittevalimisel blokeeritakse ainult kvaliteettellimuse kaubad.  
8. Klõpsake valikut **Salvesta**.
9. Sulgege leht.

> [!NOTE]
> Funktsioon *Kvaliteedijuhtimine laoprotsesside jaoks* pakub täiendavaid kauba valimi määramise võimalusi. See lisab *kauba valimi ulatuse* ning võimaluse määrata koguse spetsifikatsiooniks kogu litsentsiplaat. Kui olete selle funktsiooni lubanud, leiate üksikasjad jaotisest [Kvaliteedijuhtimine laoprotsesside jaoks](../quality-management-for-warehouses-processes.md).

## <a name="create-a-quality-group"></a>Kvaliteedigrupi loomine
1. Avage **Varud > Häälestus > Kvaliteedijuhtimine > Kvaliteedirühmad**.
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Kvaliteedirühm**. Kasutage kirjeldavat nime, mis aitab teil tuvastada, millist tüüpi kaupu grupp sisaldab (valimi kriteeriumid).  
4. Sisestage väärtus väljale **Kirjeldus**.
5. Klõpsake valikut **Salvesta**.
6. Klõpsake **Üksuste lisamine**.
7. Valige rida **Kaubakood**. Selles näites käivitatakse filtrimine kaubakoodi põhjal.  
8. Sisestage väärtus väljale **Kriteerium**. Näiteks sisestage T* kaubakoodide filtrimiseks, mis algavad T-ga.  
9. Klõpsake valikut **OK**.
10. Klõpsake valikut **OK**.
11. Klõpsake nuppu **Kauba kvaliteedigrupid**.
12. Sulgege leht.
13. Sulgege leht.

## <a name="create-a-test-group"></a>Katsegrupi loomine
1. Avage **Varud > Häälestus > Kvaliteedijuhtimine > Testrühmad**.
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Testrühm**. Andke **Testrühmale** nimi, mis aitab teil meeles pidada, milliseid katseid teostatakse ja millise kvaliteedigrupiga see peaks seotud olema. Näiteks kui seda kasutatakse kvaliteedigrupiga, mis valib T-ga algavaid kaupu, võite selle nimeks panna T-kauba katsed.  
4. Sisestage väärtus väljale **Kirjeldus**.
5. Valige väljal **Üksuse diskreetimine** üksuse diskreetimise rida, mille enne lõite.
6. Otsige loendist ja valige soovitud kirje.
7. Klõpsake käsku **Lisa**.
8. Sisestage arv väljale **Järjekorranumber**.
9. Valige väljal **Katse** see katse, mille enne lõite.
10. Otsige loendist ja valige soovitud kirje.
11. Klõpsake vahekaarti **Katsetamine**.
12. Valige väljal **Muutuja** see katse muutuja, mille enne lõite.
13. Otsige loendist ja valige soovitud kirje.
14. Klõpsake väljal **Vaiketulemus** otsingu avamiseks ripploendi nuppu.
15. Klõpsake loendis valitud real olevat linki.
16. Klõpsake valikut **Salvesta**.
17. Sulgege leht.

## <a name="define-when-quality-orders-will-be-created"></a>Kvaliteettellimuste loomise aja määratlemine
1. Avage **Varud > Häälestus > Kvaliteedijuhtimine > Kvaliteedi seosed**.
2. Klõpsake valikut **Uus**.
3. Valige suvand väljal **Viite tüüp**.
4. Valige väljal **Kaubakood** „Rühm“. Selles näites valime suvandi Grupp ja kasutame varem loodud kvaliteedigruppi. Võite selle seada ka valikule Tabel, et määrata kaupu käsitsi, või valida suvandi Kõik kõikide kaupade lisamiseks kvaliteettellimusse.  
5. Valige väljal **Üksus** see kvaliteedi rühm, mille enne lõite. Väljal Kaup saadaolevad suvandid olenevad sellest, mille määrate väljal Kauba kood.  
6. Otsige loendist ja valige soovitud kirje.
7. Laiendage või ahendage jaotist Protsess.
8. Valige suvand väljal **Sündmuse tüüp**. See on katse käivitav sündmus. Siin saadaolevad suvandid olenevad protsessist, mille valisite väljal Viite tüüp.  
9. Valige suvand väljal **Täitmine**.
10. Laiendage või ahendage jaotist **Kvaliteettellimuse protsess**.
11. Klõpsake väljal **Sündmuste blokeerimine** otsingu avamiseks ripploendi nuppu. Sellel väljal kuvatakse protsesside loend, mida on võimalik blokeerida, kui kvaliteettellimus on veel avatud. Suvandid olenevad sellest, mille valisite väljal Sündmuse tüüp.  
12. Klõpsake loendis valitud real olevat linki. See oleneb eelmistest valitud väärtustest. Valige, kui blokeerida tuleb järgmised protsessid, kui lähtedokumendi reaga on seotud avatud kvaliteettellimused.  
13. Laiendage või ahendage jaotist **Spetsifikatsioonid**.
14. Valige väljal **Testgrupp** see testgrupp, mille enne lõite.
15. Otsige loendist ja valige soovitud kirje.
16. Klõpsake valikut **Salvesta**.
17. Sulgege leht.

> [!NOTE]
> Funktsioon *Kvaliteedijuhtimine laoprotsesside jaoks* pakub kvaliteediseoste seadistamiseks lisavõimalusi. Sellega lisatakse uus tingimus (**Kohaldatav lao tüüp**) ja uus säte (**Kvaliteeditöötluse poliitika**). Kui olete selle funktsiooni lubanud, leiate üksikasjad jaotisest [Kvaliteedijuhtimine laoprotsesside jaoks](../quality-management-for-warehouses-processes.md).