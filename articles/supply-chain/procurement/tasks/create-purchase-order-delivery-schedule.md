--- 
title: Tarnegraafikuga ostutellimuse loomine
description: "See protseduur näitab, kuidas ostutellimuse jaoks tarnegraafikut luua."
author: FrankDahl
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchDeliverySchedule, PurchEditLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1e4a0204d74c8966cd90b52ae13c88e222ebc3ef
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-order-with-a-delivery-schedule"></a>Tarnegraafikuga ostutellimuse loomine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas ostutellimuse jaoks tarnegraafikut luua. Tarnegraafikut kasutatakse siis, kui tellimuse või töölehe koguse puhul on nõutav mitme saadetisega tarne. Selles juhendis toodud näidet saab kasutada demoandmete ettevõtte USMF puhul. Selle protseduuri viib tavaliselt läbi ostuagent.


## <a name="create-a-delivery-schedule"></a>Tarnegraafiku loomine
1. Avage Hanked > Ostutellimused > Kõik ostutellimused.
2. Klõpsake valikut Uus.
3. Sisestage väljale Hankija konto väärtus US-101.
4. Klõpsake nuppu OK.
5. Sisestage väljale Kauba kood väärtus M0001.
6. Sisestage väljale Kogus number 10.
7. Klõpsake suvandit Ostutellimuse rida.
8. Klõpsake valikut Tarnegraafik.
    * Lehel Tarnegraafik saate määrata, mitme saadetisega tellimuse rea lõplik kogus hankijalt tarnitakse.  
    * Vaikimisi kopeerib süsteem esimesele tarnegraafiku reale lõpliku koguse ja muud tarne üksikasjad algselt ostutellimuse realt. Selles näites loome kahe saadetisega graafiku, kus teise saadetise kuupäev on nädala võrra hilisem esimese saadetise omast.  
9. Määrake väljal Kogus koguseks 4.
10. Klõpsake valikut Uus.
11. Sisestage väljale Kogus järelejäänud koguseks 6.
    * Valige väljalt Tarnekuupäev kuupäev, mis on üks nädal pärast esimesel tarne real olevat kuupäeva.  
    * Väljade Kokku ja Järelejäänud abil saate jälgida lõplikku kogust, mis tarnegraafiku ridadele eraldati. Kui järelejäänud kogus on null, eraldati graafikusse algse rea täielik kogus.  
12. Laiendage jaotist Tasude teisendamine.
    * Siin olevad valikud võimaldavad teil juhtida, kuidas soovite tasusid tarnegraafiku ridade vahel jagada. Kui valite Kopeeri brutosummad, kopeeritakse igale tarnereale algsel tellimuse real olev tasu summa. Valik Eralda tarneridadele jagab algse rea tasu koguse järgi igale tarnereale.  
13. Ahendage jaotist Tasude teisendamine.
14. Klõpsake nuppu OK.
    * Tarnegraafik on nüüd tellimusele rakendatud.  
    * Algne tellimuse rida, mida nimetatakse nüüd äriandmete reaks, on teisendatud mitme tarnega tellimuse reaks. See on tähistatud eristatava ikooniga ja see toimib nagu tarneridade päis.  
15. Valige teine tellimuse rida, mis on kahest tarnereast esimene.
    * Kaks uut rida, mida nimetatakse tarneridadeks, moodustavad ühe tarnegraafiku. Tellimust töödeldakse nende ridade, mitte algse rea alusel. Dokumentide, nagu kinnitused, toote sissetuleku töölehed või arved, printimisel kuvatakse ainult tarneread.  

## <a name="change-the-delivery-schedule"></a>Tarnegraafiku muutmine
    * Saate tarneridadel koguseid muuta. Kui seda teete, uuendatakse tarneridade lõpliku koguse järgi automaatselt äriandmete rida.  
1. Määrake esimese tarnerea väljal Kogus koguseks 4 asemel 5.
2. Valige esimene tellimuse rida (äriandmete rida).
    * Äriandmete real olevaks koguseks on määratud 11.  

## <a name="process-product-receipt-using-delivery-schedules"></a>Toote sissetuleku töötlemine tarnegraafikuid kasutades
    * Ostutellimus tuleb enne toote sissetuleku töötlemist kinnitada. Selles näites kajastatakse sissetulek otse ostutellimusel. Sissetuleku oleks saanud registreerida ka siis, kui kaubad lattu saabusid.  
1. Klõpsake toimingupaanil valikut Ost.
2. Klõpsake käsku Kinnita.
3. Klõpsake toimingupaanil valikut Vastuvõtt.
4. Klõpsake valikut Toote sissetulek.
5. Sisestage suvaline väärtus väljale Toote sissetulek.
    * Seda välja kasutatakse viite sisestamiseks, mida kasutatakse toote sissetuleku töölehe kandena.  
    * Tehke väljal Kogus valik Tellitud kogus. See valik tähendab, et sissetulekut töödeldakse koguse puhul, millega tellimuse read loodi.  
    * Veenduge, et välja Toote sissetuleku printimine väärtuseks on määratud Ei. Selles näites ei ole printimine vajalik.  
6. Laiendage jaotist Read.
    * Pange tähele, kuidas toote sissetulek luuakse kahe tarnerea ja mitte algse tellimuse rea puhul. Kui sissetulek oleks laos registreeritud, oleks see registreeritud ka tarnegraafiku ridadel.  
7. Ahendage jaotist Read.
8. Klõpsake sissetuleku sisestamiseks nuppu OK.


