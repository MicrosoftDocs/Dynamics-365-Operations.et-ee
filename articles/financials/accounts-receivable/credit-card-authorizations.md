---
title: "Krediitkaardi seadistamine, autoriseerimine ja hõivamine"
description: "See artikkel annab ülevaate krediitkaardi autoriseerimisest Microsoft Dynamics 365 for Finance and Operationsis. See sisaldab teavet makseteenuse seadistamise, krediitkaardi lisamise kohta müügitellimusele ja loa tühistamise kohta."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, Retail
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 4a6354563fdebff901498f1cd6caed3aedae668b
ms.contentlocale: et-ee
ms.lasthandoff: 03/26/2018

---

# <a name="credit-card-setup-authorization-and-capture"></a>Krediitkaardi seadistamine, autoriseerimine ja hõivamine

[!INCLUDE [banner](../includes/banner.md)]

[!INCLUDE [retail name](../includes/retail-name.md)]

See artikkel annab ülevaate krediitkaardi autoriseerimisest Microsoft Dynamics 365 for Finance and Operationsis. See sisaldab teavet makseteenuse seadistamise, krediitkaardi lisamise kohta müügitellimusele ja loa tühistamise kohta.

<a name="setting-up-the-credit-card-payment-service"></a>Krediitkaardi makseteenuse seadistamine
------------------------------------------

Krediitkaartide kasutamiseks tuleb makseteenus lehel Makseteenused seadistada ja aktiveerida. Makseteenus toimib sillana teie juriidilise isiku ja kliendi krediitkaarditasusid töötleva panga vahel. Peaksite töötama väljal Makse ülekandmine loetletud krediitkaardi pakkujaga ja seadistama selle pakkujaga konto. Seejärel tuleks seadistada teised suvandid lehel Makseteenused, seadistada krediitkaardi tüübid American Expressi, Discoveri, MasterCardi ja Discoveri jaoks leheküljel Krediitkaardi tüübid ning aktiveerida pakkuja vaikepakkujana. Seadistuse lõpetamiseks peaksite järgima neid samme.
-   Määrake lehel Müügireskontro parameetrid krediitkaardi kasutamise parameetrid.
-   Seadistage lehel Maksetingimused krediitkaartide maksetingimused. Väljal Makse tüüp valige Krediitkaart.
-   Sisestage lehele Kliendi krediitkaardid klientide jaoks krediitkaardi teave.

## <a name="adding-a-new-credit-card"></a>Uue krediitkaardi lisamine
Uusi krediitkaardi kirjeid saate luua lehel Kliendid, kasutades välju Klient, Hääletamine, Krediitkaart. Krediitkaardi kirjeid saate luua ka müügitellimusi lehel Müügitellimus sisestades, kasutades välju Haldamine, Klient, Krediitkaart, Registreerimine.
Müügitellimusele krediitkaardi lisamine
-------------------------------------

Krediitkaardi lisamiseks müügitellimusele valige krediitkaart krediitkaardi otsingust lehe Müügitellimus vahekaardil Hinnad ja allahindlused. Autoriseerimisprotsessi käivitamiseks avage tegevuspaani vahekaart Haldamine, kus valige Krediitkaart ja Autoriseerimine.
Krediitkaardi autoriseerimine
-------------------------

Kui krediitkaardi autoriseerimisel kontrollitakse kaardi numbrit ja kaardiomaniku nime ning olemasolev kreeditsaldo kinnitatakse. Alternatiivina võib kontrollida kaardi kontrollnumbrit ja kaardiomaniku aadressi. Seejärel vähendatakse kliendi olemasolevat kreeditsaldot arve summa võrra. Makseteenus annab teada, kas krediitkaart on kinnitatud või tagasi lükatud. Kui müügitellimus on arveldatud, võetakse krediitkaardilt tasu (hõivatakse) arve summa väärtuses.

### <a name="card-verification-value"></a>Kaardi tõendamise väärtus

Saate nõuda kaardi kontrollnumbrit, millele mõnikord on viidatud ka kui kaardi turvakoodile. American Expressi puhul on see neljakohaline. Discoveri, MasterCardi ja Visa puhul on see kolmekohaline.

### <a name="address-verification"></a>Aadressi tõendamine

Aadressi tõendamise teave saadetakse alati maksepakkujale. Saate määrata kande aktseptimiseks nõutava teabe hulga. Kindlasti kontrollige oma pakkujalt, kas ta aktseptib seda teavet. Siin on aadressi tõendamise võimalused.
-   **Luba kanne alati** – kanne aktseptitakse aadressi tõendamise tulemustest olenemata.
-   **Kontoomanik** – kandel olevat kaardiomaniku nime võrreldakse krediitkaardi ettevõtte teabega.
-   **Arveldusaadress** – kaardiomaniku nime ja arveldusaadressi kandel võrreldakse krediitkaardi ettevõtte teabega.
-   **Arve sihtnumber** – kaardiomaniku nime, arveldusaadressi ja arve sihtnumbrit kandel võrreldakse krediitkaardi ettevõtte teabega.

## <a name="data-support"></a>Andmete tugi
Igale toetatud krediitkaardile saate määrata andmete toe taseme. Tase kontrollib kande kohta makseteenusele ülekantava teabe hulka. Kindlasti kontrollige oma pakkujalt, kas ta saab seda teavet anda. Siin on andmete toe taseme võimalused.
-   **1. tase** – üle kantakse kande kuupäev, summa ja kirjeldus.
-   **2. tase** – üle kantakse 1. taseme teave ja lisaks tarne- ja kaupmehe aadressid ning maksuteave.
-   **3. tase** – üle kantakse 2. taseme ja lisaks tellimuse rea teave.

## <a name="partial-payments"></a>Osalised maksed
Kui lähetate tellimuse osaliselt, hõivatakse osaline summa ja kogu tellimuse summale tehtud autoriseerimine suletakse. Seejärel tehakse järelejäänud lähetamata tellimuse summale uus autoriseerimine.

## <a name="voiding-an-authorization"></a>Autoriseerimise tühistamine 
Krediitkaardi autoriseerimise tühistamiseks saate muuta makseviisi teise meetodi vastu, millel ei ole tüüpi Krediitkaart.






