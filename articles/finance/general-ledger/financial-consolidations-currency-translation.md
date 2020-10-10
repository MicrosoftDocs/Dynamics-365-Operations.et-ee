---
title: Finantskonsolideerimise ja valuuta teisenduse ülevaade
description: Selles teemas kirjeldatakse pearaamatu finantskonsolideerimisi ja valuuta teisendusi.
author: aprilolson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 2a6685a2dcf9d7bf7ac82c3dede9c3ece0c08698
ms.sourcegitcommit: 7537aa8ef619eea6c48467a3ca86e3372415f8a7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/18/2020
ms.locfileid: "3823451"
---
# <a name="financial-consolidations-and-currency-translation-overview"></a>Finantskonsolideerimiste ja valuutateisenduse ülevaade

[!include [banner](../includes/banner.md)]

Selles teemas tutvustatakse lähenemist, mida nii Microsoft Dynamics 365 Finance kui ka finantsaruandlus konsolideerimiste puhul kasutavad. Selles kirjeldatakse stsenaariume, mis hõlmavad mitme ettevõttega aruandlust, kogumit, eemaldamist ja vähemusosalust. Selgitatakse ka, kuidas tegeleda eriolukordade, nt stsenaariumitega, kus juriidilistel isikutel on erinevad rahandusperioodid või kontoplaanid.

See teema on kirjutatud kasutajatele ja funktsionaalsetele konsultantidele ning eeldab, et lugejatel on üldine arusaam Rahandusest ja finantsaruandlusest. Põhiseadistusest siin ei räägita.

> [!NOTE]
> Mõistet *juriidiline isik* kasutatakse rakenduses Rahandus ja mõistet *ettevõte* finantsaruandluses. Selles teemas on kasutatud mõlemat mõistet. Kuid selle teema huvides on nende tähendus sama.

## <a name="audience"></a>Sihtrühm
See teema on mõeldud finants- ja raamatupidamiskasutajatele ning rakenduse konsultantidele, kes tahavad kasutada rakendust Finance and Operations ning finantsaruandlust mitme ettevõtte ja mitme valuutaga andmete konsolideerimiseks.

## <a name="approach"></a>Lähenemine
Rahandus kasutab konsolideerimise töötlemiseks eraldi juriidilist isikut. See võimaldab üksiku juhtumi konsolideerimist, aga pakub võimalust kasutada andmeid teistest allikatest. Konsolideerimisprotsess tuleb käivitada iga kord, kui aluseks olevas juriidilises isikus tehakse muudatusi.

Finantsaruandlusega saab aruande loomise ajal konsolideerida mitut ettevõtet. Kuigi andmed salvestatakse andmevakka, need teisendatakse ja neid saab eksportida, on iga lähteettevõte andmete omanik ja valdaja. Aruande saab käivitada igal ajal, isegi näiteks iga minut. Sellel on palju lisaeeliseid, nt võimalus minna süvitsi kõikidesse ettevõtetesse ja dimensioonidesse.

Kasutajad saavad kasutada konsolideerimist võrguühendusega, finantsaruandlust või nende kombinatsiooni. Valik oleneb nende ettevõtte vajadustest ja audiitorite eelistustest.

## <a name="consolidations"></a>Konsolideerimised
Moodul **Konsolideerimised** hõlmab suvandeid mitme juriidilise isiku konsolideerimiseks konsolideerimisprotsessi käigus ja ettevõtte saldo importimiseks või eksportimiseks. Saate ka seadistada eemaldamisi ja sisestada eemaldamise töölehti.

## <a name="benefits-of-using-consolidate-online"></a>Võrguühendusega konsolideerimise eelised
Klientidel, kes kasutavad moodulit **Konsolideerimised**, on mitmesuguseid eeliseid:

- **Andmete sügavus** – saate luua konsolideeritud aruandeid, mis koondavad tegelikud ja eelarve andmed nii konto tasemel kui ka dimensiooni tasemel.
- **Dünaamilised konsolideerimised** – konsolideerimisi saab töödelda mitu korda.
- **Auditi võimalused** – dimensioone ja kontosid säilitatakse analüüsimiseks ja auditeerimiseks ning saldod luuakse kuupäeva järgi.
- **Valuuta teisendamine** – saate seadistada konto vahemikud ja määrad teisendama lähteettevõtte arvestusvaluutast konsolideeritava ettevõtte arvestusvaluutasse.
- **Eemaldamiste töötlemine konsolideeritavas või eemaldamisettevõttes** – saate töödelda ja sisestada eemaldamisi konsolideerimise ajal ühe protsessina. Võimalik on ka käivitada soovitus eraldi.

## <a name="supported-consolidation-scenarios"></a>Toetatud konsolideerimisstsenaariumid
Siin on mõned konsolideerimisstsenaariumid, mida võrguühendusega konsolideerimine toetab:

- Ühetasemelised konsolideerimised juriidilistele isikutele
- Eemaldamisi sisaldavad konsolideerimised
- Vähemusosalus (selles stsenaariumis tuleb kasutada ettevõttes käsitsi arvutamist ja kannet)
- Mitu juriidiliste isikute kontoplaani
- Erinevad rahanduskalendrid mitme juriidilise isiku jaoks
- Konsolideerimised, mis hõlmavad mitut aruandlusvaluutat

## <a name="legal-entity-setup"></a>Juriidilise isiku seadistamine
Enne konsolideerimise töötlemist peate seadistama juriidilise isiku. Saate konsolideerimist käivitada nii palju kordi kui vaja ja kõik andmed teisendatakse lähteettevõte arvestusvaluutast valuutasse, mis on konsolideeritava ettevõtte jaoks määratud. Seetõttu, kui teil on järgmise organisatsiooni struktuuri jaoks vaja teisendada kõik Põhja-Ameerika ettevõtted esmalt USA dollaritele (USD) ja seejärel eurodele (EUR), emaettevõtte valuutale, peab teil olema vähemalt kaks konsolideeritavat ettevõtet.

![Organisatsiooni struktuur](./media/organizational-structure.png "Organisatsiooni struktuur")

Eelnevas ogranisatsioonilises struktuuris peab teil olema juriidiline isik Põhja-Ameerika konsolideerimise jaoks, kuna konsolideerimised konsolideerivad alati lähteettevõtte arvestusvaluutast konsolideeritava ettevõtte valuutasse. Kui näites on kõik ettevõtted kaasatud ühte konsolideerimisse, siis Mehhiko tütarettevõte teisendatakse Mehhiko peesodest (MXN) eurodeks, mitte peesodest USA dollariteks ja USA dollaritest eurodeks.

Kui loote juriidilise isiku, saate määrata, kas ettevõtet kasutatakse nii konsolideerimis- kui ka eemaldamisprotsessis või ainult ühes neist protsessidest. Järgmises näites kasutatakse ettevõtet mõlemas protsessis. Pange tähele, et igapäevaseid töölehti ei saa sisestada konsolideeritavasse ettevõttesse, aga saate need sisestada eemaldamisettevõttesse. Seetõttu võib olla kasulik eraldi eemaldamisettevõte.

![Juriidiline isik, mida kasutatakse nii konsolideerimiseks kui ka eemaldamiseks](./media/sep-elimination-company.png "Juriidiline isik, mida kasutatakse nii konsolideerimiseks kui ka eemaldamiseks")

## <a name="main-accounts-and-consolidation-account-groups"></a>Põhikontode ja konsolideerimiskontode grupid
Peate otsustama, kuidas soovite oma kontoplaane konsolideerida. Konsolideerimisprotsessi käigus on teil põhikontode konsolideerimiseks kolm võimalust.

Esimene võimalus on kasutada lähteettevõtete põhikontosid. Sellisel juhul konsolideeritakse iga konto kõikidelt ettevõtetelt. Näiteks kui sularaha on konto 100000 USMF-i ettevõttes ja konto 1100 DEMF-i ettevõttes, kaasab konsolideeritav ettevõte mõlemad kontod. Igal kontol on oma vastav saldo.

Teine võimalus on määrata vaikimisi konsolideerimiskonto lehel **Põhikontod**. Konto vastendatakse seejärel konsolideerimiskontoga. See suvand võib olla kasulik, kui teil on erisugused kontoplaanid või peate vastendama plaaniga, mille on määranud peakontor.

![Põhikontode lehel määratud vaikimisi konsolideerimiskonto](./media/main-accounts.png "Põhikontode lehel määratud vaikimisi konsolideerimiskonto")

Kolmas võimalus on kasutada konsolideerimiskonto gruppe. Saate määrata nii palju konsolideerimiskonto gruppe kui vaja. Seejärel peate lehel **Täiendavad konsolideerimiskontod** vastendama põhikonto kontoplaanist kontoga, mida teil selle grupi jaoks vaja on.

![Vastendamine täiendavate konsolideerimiskontode lehel](./media/additional-consolidation-accounts.png "Vastendamine täiendavate konsolideerimiskontode lehel")

## <a name="consolidating-online"></a>Võrguühendusega konsolideerimine
Lisateavet konsolideerimise üksikasjade sisestamise kohta võrgus vt teemast [Finantskonsolideerimised võrgus](./consolidate-online.md).

## <a name="managing-consolidation-transactions"></a>Konsolideerimiskannete haldamine
Konsolideerimise tulemuste vaatamiseks on teil mitu võimalust.

- Looge konsolideeritava ettevõtte suhtes finantsaruanne.
- Vaadake üle konsolideeritava ettevõtte loendileht **Proovibilanss**.
- Vaadake konsolideerimiskannete loendis lehel **Konsolideerimised** saldosid, mis on loodud iga perioodi kohta igale lähteettevõttele kuupäeva järgi.

    ![Konsolideerimiskanded konsolideerimiste lehel](./media/managing-consolidation-transactions.png "Konsolideerimiskanded konsolideerimiste lehel")

Konsolideerimise uuesti käivitamiseks võite konsolideerimist lihtsalt töödelda. Võite ka esmalt valida suvandi **Kannete eemaldamine** lehelt **Konsolideerimised**.
Kui teie konsolideeritud konto saldod ei ole täpsed, saab saldosid korrigeerida lehe **Sulgemisperioodi korrigeerimised** abil.

## <a name="consolidate-with-import"></a>Konsolideeri impordiga
Impordiga konsolideerimise funktsioon töötab nagu võrguühendusega konsolideerimine. Kui valite juriidilised üksused, otsite välja lähtefaili, mis andmeid sisaldab.

## <a name="export-company-balances"></a>Ekspordi ettevõtte saldod
Ettevõtte saldode eksportimise funktsioon töötab samuti nagu võrguühendusega konsolideerimine. Kui valite juriidilised üksused, määrate väljundile failitee.

## <a name="elimination-rules"></a>Eemaldamisreeglid
Ettevõtete vaheliste kannete eemaldamiseks saate luua eemaldamisreegli. Teine võimalus on käsitsi eemaldada kanne ettevõttest, mis on määratud eemaldamisettevõtteks. Kui loote eemaldamisreegli, on teil eemaldamismeetodiks kaks võimalust: **Netomuutus** ja **Fikseeritud**.

### <a name="set-up-elimination-rules"></a>Eemaldamisreeglite seadistamine
Rahanduse eemaldamisreeglite seadistamisel saate luua finantsdimensiooni, mida kasutatakse spetsiaalselt eemaldamiseks. Enamik kliente annab sellele finantsdimensioonile nimeks **Kaubanduspartner** või muud sarnast. Kui te ei soovi finantsdimensiooni kasutada, siis veenduge, et teil oleks kindlasti olemas põhikontod, mida kasutatakse ainult ettevõtete vahelisteks kanneteks.

Eemaldamiste seadistuse leiate mooduli **Konsolideerimised** alal **Seadistus**. Kui olete reegli kohta kirjelduse sisestanud, peate valima ettevõtte, millesse eemaldamisreegel sisestatakse. Valitaval ettevõttel peab olema juriidilise isiku seadistuses valitud suvand **Kasuta finantsiliseks eemaldamisprotsessiks**.

Saate enda vajaduste järgi määrata kuupäeva, millal eemaldamisreegel toimima hakkab, ja kuupäeva, millal see aegub. Kui soovite, et eemaldamisreegel oleks eemaldamispakkumise protsessis saadaval, peate seadistama suvandi **Aktiivne** valikule **Jah**. Valige tüübi **Eemaldamine** töölehe nimi.

![Eemaldamisreegli põhiatribuudid](./media/ledger-elimination-rule-journal.png "Eemaldamisreegli põhiatribuudid")

Kui olete põhiatribuudid määratlenud, valige suvand **Read**, et määratleda tegelikud töötlusreeglid. Eemaldamiseks on kaks võimalust: võite eemaldada netomuutuse summa või määrata fikseeritud summa.

Valige lähtekontod. Saate kasutada metamärgina tärni (\*). Näiteks väärtuse **1\*** korral valitakse eralduse andmeallikana kõik kontod, mis algavad numbriga **1**.

Kui olete lähtekontod valinud, kasutage välja **Konto täpsustus**, et määrata konto, mida kasutatakse sihtettevõttest. Valige suvand **Allikas**, et kasutada sama põhikontot, mis on määratletud lähtekontol. Kui valite suvandi **Kasutaja määratletud**, peate määrama sihtkonto.

![Pearaamatu eemaldamisreegli rea leht](./media/ledger-elimination-rule-line.png "Pearaamatu eemaldamisreegli rea leht")

Väli **Dimensioonide täpsustus** töötab nagu väli **Konto täpsustus**. Valige suvand **Allikas**, et kasutada sihtettevõttes ja lähteettevõttes samu dimensioone. Kui valite suvandi **Kasutaja määratletud**, peate määrama sihtettevõttes dimensioonid, valides suvandi **Sihtdimensioonid**. Seejärel valige lähtedimensioonid ja finantsdimensioonid ning väärtused, mida kasutatakse eemaldamisallikana.

### <a name="process-elimination-transactions"></a>Eemaldamiskannete töötlemine
Eemaldamiskannete töötlemiseks on kaks võimalust. Kannet saab töödelda võrguühendusega konsolideerimise ajal või luues eemaldamise tööraamatu ja käitades eemaldamissoovituse protsessi. Selles jaotises keskendutakse teisele võimalusele.

Valige eemaldamisettevõttena määratletud ettevõttes moodulis **Konsolideerimine** suvand **Eemaldamise tööleht**. Pärast töölehe nime valimist valige suvand **Read**. Soovituse käivitamiseks valige **Soovitused** \> **Eemaldamissoovitus**.

Valige ettevõte, mis on konsolideeritud andmete allikas, ja seejärel valige töötlemiseks reegel. Sisestage algus- ja lõppkuupäevad, et määrata kuupäevavahemik, kust otsitakse eemaldamissummasid. Väli **Pearaamatu sisestamise kuupäev** määrab kuupäeva, mida kasutatakse töölehe pearaamatusse sisestamiseks. Pärast nupu **OK** valimist saate summad üle vaadata ja töölehe sisestada.

> [!NOTE]
> Eemaldamistööleht kuvab kontoväärtuste summad algsete kannete valuutas, mitte arvestusvaluutas. Kui vaatate üle summad eemaldamistöölehel, võib see käitumine tunduda segadust tekitav.

Lisateavet eemaldamiste kohta ja näiteid vt teemast [Eemaldamisreeglid](./elimination-rules.md).

## <a name="currency-revaluation-in-a-consolidation-company"></a>Valuuta ümberarvutamine konsolideeritavas ettevõttes
Kui konsolideerite andmeid ühelt arveldusvaluutalt teisele, peate siiski käivitama valuuta ümberarvestamise, kui vahetuskursid muutuvad, et teie konto saldo arvestataks õigesti ümber. Kasutage algsel andmete konsolideerimisel vahekaarti **Valuuta teisendamine**, et valida algsed vahetuskursid, mida kasutama peaks, ümberarvestamiseks konsolideerimisprotsessi käigus. Pärast uue vahetuskursi sisestamist (näiteks järgmisel kuul) peate konto saldo ümber arvutama. Realiseerimata kasumeid või kahjumeid värskendatakse uue vahetuskursi ja kuupäeva järgi.

Lisateavet valuuta ümberarvutamise kohta konsolideeritavas ettevõttes vt teemast [Valuuta ümberarvutamine konsolideeritavas ettevõttes](currency-revaluation-consolidation-company.md).

Lisateavet valuuta ümberarvestamise toimimise kohta moodulis **Pearaamat** vt teemast [Pearaamatu välisvaluuta ümberarvutamine](./foreign-currency-revaluation-general-ledger.md).

### <a name="additional-information"></a>Lisateave
- Kõik sisestamiskihid konsolideeritakse konsolideerimise töötlemisel.
- Eemaldamise töölehti saab sisestada ainult praegusesse kihti.
- Konsolideeritakse ainult tootmissaldosid. Seetõttu peate algsaldode nägemiseks siiski konsolideeritavas ettevõttes käivitama rahandusaasta sulgemise.
- Saate sisestada igapäevaseid töölehti eemaldamisettevõttesse, aga mitte konsolideeritavasse ettevõttesse.
- Konsolideeritava ettevõtte saldosid saab korrigeerida ainult lehe **Sulgemisperioodi korrigeerimised** abil. 

## <a name="benefits-of-using-financial-reporting-for-financial-consolidations-and-currency-translation-or-to-complement-consolidate-online-for-consolidated-reporting"></a>Finantskonsolideerimisteks ja valuuta teisendamiseks või konsolideeritud aruandluse jaoks võrguühendusega konsolideerimise täiendamiseks finantsaruandluse kasutamise eelised
Klientidel, kes kasutavad finantsaruandlust finantskonsolideerimisteks ja valuuta teisendamiseks või konsolideeritud aruandluse jaoks võrguühendusega konsolideerimise täiendamiseks, on mitmesuguseid eeliseid.

- **Andmete sügavus** – saate luua konsolideeritud aruandeid, mis koondavad tegelikud ja eelarve andmed nii konto tasemel kui ka dimensiooni tasemel. Rakenduses Rahandus hõlmab see teave andmeid nii eelarve juhtimisest kui ka eelarve plaanimisest.
- **Dünaamilised konsolideerimised** – konsolideerimisi saab teha igal ajal ja organisatsiooni hierarhia igal tasemel.
- **Auditi täielikud võimalused** – kõiki dimensioone, kontosid ja kannete üksikasju säilitatakse analüüsimiseks ja auditeerimiseks. Peale selle pakub finantsaruandlus täielikku tagasiminemise võimalust algsele kandele kõigis konsolideeritavates juriidilistes isikutes.
- **Sujuv valuuta teisendamine** – pärast minimaalset seadistamist rakenduses Rahandus saate teisendada mis tahes finantsaruandluse aruandeid ükskõik millisesse seadistatud aruandlusvaluutasse. Peale selle saate seadistada piiramatu arvu aruandlusvaluutasid.
- **Eemaldamiste sisestamine allikas** – saate luua ja printida eemaldamisaruannet, et kontrollida eemaldamiskandeid. Seejärel saate sisestada mis tahes uue eemaldamise standardse ettevõtete vahelise kandena. Võite ka kasutada eemaldamise juriidilist isikut mis tahes kande jaoks, mida te oma juriidilisse isikusse ei soovi.

## <a name="supported-consolidation-scenarios"></a>Toetatud konsolideerimisstsenaariumid
Siin on mõned konsolideerimisstsenaariumid, mida finantsaruandlus toetab:

- Ühe- ja mitmetasemelised konsolideerimised juriidilistele isikutele
- Konsolideerimised, mis kasutavad juriidilistest isikutest loodud organisatsiooni struktuure
- Eemaldamisi sisaldavad konsolideerimised
- Vähemusosalus
- Mitu juriidiliste isikute kontoplaani
- Erinevad rahanduskalendrid mitme juriidilise isiku jaoks
- Konsolideerimised, mis hõlmavad mitut aruandlusvaluutat
- Äriüksuse konsolideerimised

## <a name="generating-consolidated-financial-statements"></a>Konsolideeritud finantsaruannete loomine
Lisateavet stsenaariumide kohta, kus võite luua konsolideeritud finantsaruandeid, vt teemast [Konsolideeritud finantsaruannete loomine](./generating-consolidated-financial-statements.md).
