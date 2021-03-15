---
title: Pearaamatute konfigureerimine
description: See teema annab teavet selle kohta, kuidas konfigureerida iga juriidilise isiku jaoks pearaamatuid. See hõlmab teavet valuutade, majandusaasta kalender, kontoplaani ja konto struktuuride valimise kohta, mida tuleks kasutada iga juriidilise isiku puhul.
author: kweekley
manager: ''
ms.date: 09/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Ledger
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-09
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 5a7fcda435fd957edbbe09d796685c0c742dc6a8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975812"
---
# <a name="configure-ledgers"></a>Pearaamatute konfigureerimine

[!include [banner](../includes/banner.md)]

See teema annab teavet selle kohta, kuidas konfigureerida iga juriidilise isiku jaoks pearaamatuid. See hõlmab teavet valuutade, majandusaasta kalender, kontoplaani ja konto struktuuride valimise kohta, mida tuleks kasutada iga juriidilise isiku puhul.

## <a name="selecting-the-chart-of-accounts"></a>Kontoplaani valimine

Iga rakenduse Microsoft Dynamics 365 Finance juriidilise isiku pearaamatu üksikasjad tuleb konfigureerida. Leht **Pearaamat** võimaldab teil valida kontoplaani ja konto struktuurid, mida kasutatakse valitud juriidilise isiku puhul. Saate oma kontoplaani ja konto struktuure jagada, konfigureerides iga juriidilise isiku lehe **Pearaamat**, et kasutada sama kontoplaani ja konto struktuure. Samuti saate jagada osa iga juriidilise isiku konfiguratsioonist ja omada iga juriidilise isiku jaoks kindlaid konfiguratsioone.

Kui teie juriidilistel isikutel peavad olema erinevad kontoplaanid või erinevad konto struktuurid, võib olla kasu juriidilise isiku alistamise funktsioonist. Mitme juriidilise isiku jaoks sama kontoplaani ja kontode struktuuri kasutamine ning seejärel mis tahes erandite haldamine läbi juriidilise isiku alistamiste võimaldab aja jooksul haldamist lihtsustada.

Juriidilise isiku kontoplaani konfigureerimiseks avage **Pearaamat \> Pearaamatu seadistus \> Pearaamat**. Valige lehel **Pearaamat** suvand **Kontoplaan** ja valige seejärel loendist kasutamiseks kontoplaan. Pange tähele, et kontoplaani ei saa muuta pärast juriidilises isikus väärtuse valimist ja kannete sisestamist.

Lisateavet kontoplaani ja põhikontode kavandamise ning konfigureerimise kohta vt teemast [Kontoplaani kavandamine](plan-chart-of-accounts.md).

## <a name="selecting-account-structures"></a>Kontostruktuuri valimine

Iga rakenduse Dynamics 365 Finance juriidilise isiku saab konfigureerida kasutama ühte või mitut konto struktuuri. Iga konto struktuur määratleb finantsdimensioonid ning põhikontode ja finantsdimensioonide kombinatsioonid, mis on kannete sisestamisel lubatud. Sama konto struktuure saate kasutada rohkem kui ühes juriidilises isikus.

Pidage meeles, et kui teil on mitu konto struktuuri, saate valida ainult konto struktuurid, millel ei ole põhikontode ja finantsdimensioonide kattuvaid kombinatsioone. Näiteks on üks teie konto struktuuridest konfigureeritud lisama põhikontodele vahemikus 1000 ja 1999 äriüksuse. Teises konto struktuuris olete lisanud 1-ga algavatele põhikontodele osakonna finantsdimensiooni. Sellisel juhul saab samale juriidilisele isikule lisada ainult ühe konto struktuuri.

Pearaamatu konto struktuuride konfigureerimiseks valige lehe **Pearaamat** kiirkaardil **Konto struktuurid** suvand **Lisa**, valige loendist konto struktuur ja valige seejärel suvand **Vali**. Konto struktuuride lisamiseks ja salvestamiseks võib kuluda mõni minut. Pange tähele, et teie valitud konto struktuurid peavad olema aktiivsed. Vastasel juhul ei kehti konto struktuuride üksikasjad juriidilistele isikutele, millega need on seotud.

Konto struktuuri eemaldamiseks valige lehe **Pearaamatu** kiirkaardil **Konto struktuurid** suvand **Eemalda**. Pange tähele, et kui eemaldate pearaamatust konto struktuuri, ei eemaldata selle konto struktuuri konfiguratsiooni abil sisestatud kandeid.

Lisateavet oma kontostruktuuride häälestamise kohta leiate jaotisest [Kontostruktuuride konfigureerimine](configure-account-structures.md).

## <a name="configuring-calendars-for-the-ledger"></a>Pearaamatu kalendrite konfigureerimine

Pearaamatu teine komponent on majandusaasta kalender. Majandusaasta kalender peab olema valitud iga juriidilise isiku jaoks. Sama finantsaasta kalendrit saate kasutada rohkem kui ühes juriidilises isikus. Kui valite pearaamatu jaoks majandusaasta kalendri, tehakse koopia. Seda koopiat nimetatakse pearaamatu kalendriks. Pearaamatu kalendri abil saate valida perioodide ja iga perioodi moodulite oleku.

Valitud juriidilise isiku kalendri avamiseks ja uuendamiseks valige lehe **Pearaamat** tegevuspaanil suvand **Pearaamatu kalender**.

Kalendri valimiseks valige **Majandusaasta kalendrid** ja valige seejärel loendist Kalender. Kui muudate majandusaasta kalendrit pärast kannete juriidilisse isikusse sisestamist, peate valima suvandi **Pearaamatu perioodide ümberarvutamine**. Seejärel saate kuvatavas dialoogis uuendada pearaamatu saldosid kalendri perioodide jaoks. Soovitame käivitada protsessi **Pearaamatu perioodide ümberarvutamine** režiimis **Partii** ja käivitada selle siis, kui teie süsteemis esinevad mitte-kriitilised protsessid. Sõltuvalt kannete arvust ja finantsdimensiooni kombinatsioonidest võib selle protsessi peale kuluda aega.

Kui juriidilise isiku jaoks ei ole valitud ühtegi majandusaasta kalendrit, kuvatakse tõrketeade, kui püüate sisestada tehingut selles juriidilises isikus.

Lisateavet leiate jaotisest [Rahanduskalendrid, rahandusaastad ja -perioodid](../budgeting/fiscal-calendars-fiscal-years-periods.md).

## <a name="using-a-balancing-financial-dimension"></a>Tasakaalustava finantsdimensiooni kasutamine

Pärast kontoplaani valimist ja ühe või mitme konto struktuuri lisamist saate valikuliselt valida ühe finantsdimensiooni, mida kasutada tasakaalustava finantsdimensioonina. Teie valitud dimensioon peab olemas olema kõigis konto struktuurides. Samuti peab see olema tasakaalustatud kõigis raamatupidamise kannetes. Teisisõnu peavad deebetid ja kreeditid olema põhikonto ja tasakaalustava finantsdimensiooni puhul võrdsed. Süsteem loob kannete tasakaalustamiseks automaatselt kanded, võttes aluseks põhikontod, mis on määratud väljadel **Üksustevaheline kreedit** ja **Üksustevaheline deebet** lehel **Automaatsete kannete kontod**.

Lisateavet kirjete tasakaalustamise kohta vt teemast [Tasakaalustatud töölehed sisekäibe jaoks](example-balanced-journals-interunit-accounting.md).

## <a name="configuring-currencies-for-the-ledger"></a>Pearaamatu valuutade konfigureerimine

Lehte **Pearaamat** kasutatakse ka nende valuutade juhtimiseks ja määratlemiseks, mida kasutatakse kannete sisestamisel pearaamatusse. Peate määrama raamatupidamise valuuta, mis on kõikides kannetes pearaamatu veerus **Raamatupidamise valuuta** kasutatav valuuta. Lisaks saate veerus **Raamatupidamise valuuta** valida valikuliselt teise valuuta. Kui valite aruandlusvaluuta, kirjendatakse kõik kanded pearaamatu kannete jaoks veerus **Aruandlusvaluuta** selles valuutas.

Kui kanded sisestatakse muus valuutas, teisendab süsteem kande summa automaatselt kannete valuutast raamatupidamise valuutasse ja kande aruandluse valuutasse. Valige lehe **Pearaamat** väljal **Raamatupidamise valuuta vahetuskursi tüüp** vahetuskursi jaoks konfigureeritud vahetuskursi tüüp, mida tuleks kasutada väärtuste teisendamiseks tehingu valuutast kande raamatupidamise valuutasse. Kui valisite aruandevaluuta, peate määrama ka välja **Aruandevaluuta vahetuskursi tüüp**, et näidata vahetuskurssi, mida tuleks kasutada väärtuste teisendamiseks tehingute valuutast kande aruandlusvaluutasse.

Kui kasutate eelarvestamise funktsiooni, saate määrata ka välja **Eelarve vahetuskursi tüüp**, et näidata vahetuskurssi, mida tuleks kasutada eelarvekannete teisendamiseks ühest valuutast teise.

Kui kasutate kahte valuutat või kui kasutate ühte valuutat, kuid kanded sisestatakse muus valuutas, tuleb teil konfigureerida kiirkaart **Valuuta ümberhindamise kontor** lehel **Pearaamat**. Sellel kiirkaardil saate määratleda vaikimisi realiseeritud ja realiseerimata kasumi ja kahjumi kontod, mida kasutatakse vaikimisi kannete sisestamisel, kui lehel **Valuuta ümberarvestuse kontod** ei ole kontot määratud. (Lehte **Valuuta ümberhindamise kontod** kasutatakse erinevate kontode konfigureerimiseks realiseeritud ja realiseerimata kasumi ja kahjumi jaoks iga valuuta puhul.)

Realiseeritud kasumid ja kahjumid on lõpetatud kannetest saadud kasumid ja kahjumid. Need kirjendatakse kasumi- ja kahjumiaruannetes. Realiseerimata kasumid ja kahjumid on teoks saanud kasumid ja kahjumid, kuid kanne pole lõpetatud. Teisisõnu olete näiteks sisestanud arve, kuid arvet pole veel tasutud. Realiseerimata kasumid ja kahjumid kirjendatakse bilansis.

Lisateavet kahe valuuta kasutamise kohta vt teemast [Topeltvaluuta](dual-currency.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]