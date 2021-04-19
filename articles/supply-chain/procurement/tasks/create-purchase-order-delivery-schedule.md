---
title: Tarnegraafikuga ostutellimuse loomine
description: Selles teemas näidatakse, kuidas luua ostutellimusele tarnegraafikut.
author: kamaybac
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchDeliverySchedule, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d788aaf3dc45542e20745cb295d77efdc277a4be
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812346"
---
# <a name="create-a-purchase-order-with-a-delivery-schedule"></a>Tarnegraafikuga ostutellimuse loomine

[!include [banner](../../includes/banner.md)]

Selles teemas näidatakse, kuidas luua ostutellimusele tarnegraafikut. Tarnegraafikut kasutatakse siis, kui tellimuse või töölehe koguse puhul on nõutav mitme saadetisega tarne. Selles juhendis toodud näidet saab kasutada demoandmete ettevõtte USMF puhul. Selle protseduuri viib tavaliselt läbi ostuagent.

## <a name="create-a-delivery-schedule"></a>Tarnegraafiku loomine
1. Avage navigeerimispaanil **Moodulid > Hange > Ostutellimused > Kõik ostutellimused**.
2. Valige toimingupaanil nupp **Uus**.
3. Väljale **Tarnija konto** sisestage `US-101`.
4. Valige nupp **OK**.
5. Väljale **Kauba kood** sisestage `M0001`.
6. Väljale **Kogus** sisestage `10`.
7. Valige **Ostutellimuse rida**.
8. Valige **Tarnegraafik**.
- Lehel **Tarnegraafik** saate määrata, mitme saadetisega tellimuse rea lõplik kogus hankijalt tarnitakse.  
- Vaikimisi kopeerib süsteem esimesele tarnegraafiku reale lõpliku koguse ja muud tarne üksikasjad algselt ostutellimuse realt. Selles näites loome kahe saadetisega graafiku, kus teise saadetise kuupäev on nädala võrra hilisem esimese saadetise omast.  
9. Väljal **Kogus** muutke koguse väärtuseks `4`.
10. Valige suvand **Uus**.
11. Väljale **Kogus** sisestage `6` järelejäänud koguseks.
- Valige väljalt Tarnekuupäev kuupäev, mis on üks nädal pärast esimesel tarnereal olevat kuupäeva.  
- Väljade **Kokku** ja **Järelejäänud** abil saate jälgida lõplikku kogust, mis tarnegraafiku ridadele eraldati. Kui järelejäänud kogus on null, eraldati graafikusse algse rea täielik kogus.  
12. Laiendage jaotist **Tasude teisendamine**.
- Siin olevad valikud võimaldavad teil juhtida, kuidas soovite tasusid tarnegraafiku ridade vahel jagada. Kui valite **Kopeeri brutosummad**, kopeeritakse igale tarnereale algsel tellimuse real olev tasu summa. Valik **Eralda tarneridadele** jagab algse rea tasu koguse järgi igale tarnereale.  
13. Ahendage jaotist **Tasude teisendamine**.
14. Valige nupp **OK**.
- Tarnegraafik on nüüd tellimusele rakendatud.  
- Algne tellimuse rida, mida nimetatakse nüüd äriandmete reaks, on teisendatud mitme tarnega tellimuse reaks. See on tähistatud eristatava ikooniga ja see toimib nagu tarneridade päis.  
15. Valige teine tellimuse rida, mis on kahest tarnereast esimene.
- Kaks uut rida, mida nimetatakse tarneridadeks, moodustavad ühe tarnegraafiku. Tellimust töödeldakse nende ridade, mitte algse rea alusel. Dokumentide, nagu kinnitused, toote sissetuleku töölehed või arved, printimisel kuvatakse ainult tarneread.  

## <a name="change-the-delivery-schedule"></a>Tarnegraafiku muutmine
Saate tarneridadel koguseid muuta. Kui seda teete, uuendatakse tarneridade lõpliku koguse järgi automaatselt äriandmete rida.  
1. Määrake esimese tarnerea väljal **Kogus** koguseks `4` asemel `5`.
2. Valige esimene tellimuse rida (äriandmete rida).  
- Äriandmete real olevaks koguseks on määratud 11.  

## <a name="process-product-receipt-using-delivery-schedules"></a>Toote sissetuleku töötlemine tarnegraafikuid kasutades
Ostutellimus tuleb enne toote sissetuleku töötlemist kinnitada. Selles näites kajastatakse sissetulek otse ostutellimusel. Sissetuleku oleks saanud registreerida ka siis, kui kaubad lattu saabusid.  
1. Valige toimingupaanil **Ostmine**.
2. Valige **Kinnita**.
3. Valige toimingupaanil **Vastuvõtmine**.
4. Valige **Toote sissetulek**. **Sisestage suvaline väärtus väljale Toote sissetulek.**
- Seda välja kasutatakse viite sisestamiseks, mida kasutatakse toote sissetuleku töölehe kandena.  
- Tehke väljal **Kogus** valik **Tellitud kogus**. See valik tähendab, et sissetulekut töödeldakse koguse puhul, millega tellimuse read loodi.  
- Veenduge, et välja **Toote sissetuleku printimine** väärtuseks on määratud **Ei**. Selles näites ei ole printimine vajalik.  
5. Laiendage jaotist **Read**.
- Pange tähele, kuidas toote sissetulek luuakse kahe tarnerea ja mitte algse tellimuse rea puhul. Kui sissetulek oleks laos registreeritud, oleks see registreeritud ka tarnegraafiku ridadel.  
6. **Ahendage jaotist Read.**
7. **Klõpsake sissetuleku sisestamiseks nuppu OK.**



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]