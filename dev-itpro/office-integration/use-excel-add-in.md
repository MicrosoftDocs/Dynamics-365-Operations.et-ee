---
title: Kasutage Exceli lisandmoodul
description: "Selles artiklis käsitletakse avage olemi andmeid Microsoft Excelis, ja seejärel vaadata, värskendada ja andmeid redigeerida kasutades lisandmoodul Microsoft Dynamics Office Excel. Olemi andmete avamiseks alustamiseks kas Exceli või Microsoft Dynamics 365 toiminguteks."
author: ChrisGarty
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: af7e7288f741b3c519227e2778c4c4311c3a2012
ms.openlocfilehash: 8af663b47117759ed3b2e2ed8eee85ae4df100d1
ms.lasthandoff: 03/31/2017


---

# <a name="use-the-excel-add-in"></a>Kasutage Exceli lisandmoodul

Selles artiklis käsitletakse avage olemi andmeid Microsoft Excelis, ja seejärel vaadata, värskendada ja andmeid redigeerida kasutades lisandmoodul Microsoft Dynamics Office Excel. Olemi andmete avamiseks alustamiseks kas Exceli või Microsoft Dynamics 365 toiminguteks.

Microsoft Exceli avamisel olemi andmeid, saate kiiresti ja lihtsalt vaadata ja redigeerida andmeid Exceli lisandmoodul Microsoft Dynamics Office. Nõuab see lisandmoodul Microsoft Excel 2016. **Märkus:** kui Microsoft Azure Active Directory (Azure AD) Üürnik on konfigureeritud kasutama Active Directory Federation Services (AD FS), peate veenduma, et mai 2016 värskendus on rakendatud, et Exceli lisandmoodul võib õigesti teie sisselogimise.

## <a name="open-entity-data-in-excel-when-you-start-from-dynamics-365-for-operations"></a>Avatud üksuse andmed Exceli käivitamisel Dynamics 365 toiminguteks
1.  Klõpsake lehel Microsoft Dynamics 365 operatsioonide **avatud Microsoft Office'i**. Kui lehe root andmeallikas (tabel) on sama juur andmeallikas isikud, vaikimisi **Excelis avatud** Valikud luuakse lehe. **Excelis avatud** Valikud leiate sagedamini kasutatavad lehed, nagu **hankijate** ja **kõik kliendid**.
2.  Klõpsake selle **Excelis avada** valik ja avage töövihik, mis luuakse. See töövihik on siduv informatsioon ettevõte, oma keskkonda viit ja viit Exceli lisandmoodul.
3.  Klõpsake Excelis **redigeerimise lubamine** et Exceli lisandmoodulit käivitada. Exceli lisandmoodul jookseb Exceli akna paremal paanil.
4.  Kui teil on Exceli lisandmoodul esimest korda, klõpsake **usaldada selle Add-in**.
5.  Kui teil palutakse sisse logida, klõpsake **Logi sisse**, ja seejärel logige kasutades samu mandaate, mida kasutasite sisselogimiseks Dynamics 365 toiminguteks. Exceli lisandmoodul kasutab eelmise sisselogimise kontekstis Internet Explorerist ja automaatselt sisse, kui saab. Seetõttu kontrollida kasutajanime paremas nurgas Exceli lisandmoodul.

Exceli lisandmoodul loeb automaatselt valitud olemi andmeid. Pange tähele, et andmed töövihiku kuni Exceli lisandmoodul loeb seda.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Avatud üksuse andmete Excelis Exceli käivitamisel
1.  Exceli kohta on **lisada** vahekaardil, on **lisandmoodulid** nuppu **poe** Office'i poe avamiseks.
2.  Office Store, otsige märksõna "Dynamics" ja klõpsake **lisa** kõrval on **Microsoft Dynamics Office Add-in** (Exceli lisandmoodul).
3.  Kui teil on Exceli lisandmoodul esimest korda, klõpsake **usaldada selle Add-in** et Exceli lisandmoodulit käivitada. Exceli lisandmoodul jookseb Exceli akna paremal paanil.
4.  Klõpsake **lisa info** avamiseks ning **Valikud** paani.
5.  Kopeerida oma eesmärgi Dynamics 365 toimingute astme brauseri URL, kleepige see on **serveri URL** välja ja seejärel kustutage kõik pärast hosti nimi (näiteks kustutada **/? VTMS = usmf & mi = CustTableListPage**). Tulemuseks URL peaks olema lihtsalt hosti nimi (näiteks **https://xxx.dynamics.com**).
6.  Klõpsake **OK**, ja seejärel klõpsake **Jah** muutuse kinnitamiseks. Exceli lisada taaskäivitub ja laadib metaandmed. Selle **projekti** nupp on nüüd saadaval. Kui Exceli lisandmoodul on saanud **laadida apletid** nupp, te ilmselt ei ole sisse loginud kasutaja õige. Lisateabe saamiseks vt "koormus apletid nuppu kuvatakse" selle teema jaotisest "Tõrkeotsing".
7.  Klõpsake **projekti**. Exceli lisandmoodul toob olemi metaandmeid.
8.  Klõpsake **lisa tabelis**. Kuvatakse loend üksustest. Üksused on loetletud "- nimesildi" formaadis.
9.  Valige üksus loendist, näiteks **klient - hotelli**, ja seejärel klõpsake **järgmise**.
10. Lisada väli selle **saadaolevad väljad** nimekirja on **valitud väljad**, klõpsake välja ja seejärel soovitud **lisa**. Teise võimalusena topeltklõpsake välja.
11. Kui olete lisanud soovitud väljad on **valitud väljad**, veenduge, et kursor asub õigesse kohta töölehel (nt lahter A1) ja seejärel soovitud **teha**. Klõpsake **teha** et väljumiseks.
12. Klõpsake **värskendada** andmete tõmmata.

## <a name="view-and-update-entity-data-in-excel"></a>Saate vaadata ja värskendada üksuse andmete kasutamine Excelis
Kui Exceli lisandmoodul loeb töövihikusse olemi andmeid, saate värskendada andmeid igal ajal klõpsates **värskendada** ja Exceli lisandmoodul.

## <a name="edit-entity-data-in-excel"></a>Üksuse andmete redigeerimine Excelis
Saate muuta olemi andmeid nõuavad ja avaldate selle siis klõpsake veel kord käsul **avalda** ja Exceli lisandmoodul. Kirje redigeerimiseks valige lahter töölehel ja seejärel muutke lahtri väärtuse. Uue kirje lisamiseks järgige neid samme:

-   Klõpsake töölehel, ja seejärel klõpsake **uus** ja Exceli lisandmoodul.
-   Klõpsake viimase töölehe rida ja vajutage tabeldusklahvi, kuni kursor selle rea viimases veerus kokku ja luuakse uus rida.
-   Klõpsake all töölehe rida ja sisestage andmed lahtrisse hakata. Kui te fookuse välja see lahter, tööleht laieneb, et kaasata uue rea.

Kirje kustutamiseks järgige neid samme:

-   Paremklõpsake rea number kõrval töölehe rida kustutada ja seejärel klõpsake **kustutada**.
-   Töölehe rea kustutamiseks paremklõpsake ja seejärel klõpsake **kustutada**&gt;**tabeli ridade**.

## <a name="add-or-remove-columns"></a>Lisa või eemalda veerge
Saate kohandada veerud, mis lisatakse automaatselt töölehe projekteerija.

1.  Andmete allika autori lisandmooduli Exceli käivitamiseks klõpsake selle **Valikud** nuppu (käik sümbol) ja seejärel klõpsake selle **disain lubade kasutada programmi** ruut.
2.  Klõpsake **projekti** ja Exceli lisandmoodul. Kõik andmeallikad on loetletud.
3.  Kõrval andmeallikas, klõpsake selle **muuta** nuppu (pliiats sümbol).
4.  Kohandada nimekirja ning **valitud väljad** nimekirja kui vaja:
    -   Lisada väli selle **saadaolevad väljad** nimekirja on **valitud väljad**, klõpsake välja ja seejärel soovitud **lisa**. Teise võimalusena topeltklõpsake välja.
    -   Väli, eemaldada selle **valitud väljad**, klõpsake välja ja seejärel soovitud **eemaldamine**. Teise võimalusena topeltklõpsake välja.
    -   Väljade järjestuse muutmiseks klõpsake välja selle **valitud väljad** ja seejärel soovitud **üles** või **ette**.

5.  Muudatused rakenduvad andmeallikas klõpsates **Update**. Klõpsake **teha** et väljumiseks. Kui lisasite (veerus), klõpsake **värskendada** tõmmata andmed uuendatud kogumik.

## <a name="httpspowerappsmicrosoftcomenustutorialsdataplatforminteractiveexceltroubleshootingtroubleshooting"></a>[](https://powerapps.microsoft.com/enus/tutorials/dataplatforminteractiveexcel/#troubleshooting)Troubleshooting
Seal on mõned probleemid, mida saab lahendada mõne lihtsa sammuga.

-   **Koormus apletid nuppu kuvatakse.** Kui Exceli lisandmoodul on saanud **laadida apletid** nuppu pärast sisselogimine, te ilmselt ei ole sisse loginud kasutaja õige. Selle probleemi lahendamiseks veenduge, et õige kasutajanime kuvatakse paremas nurgas Exceli lisandmoodul. Kui vale kasutajanime, klõpsake seda, logige välja ja seejärel logige uuesti sisse.
-   **Kuvatakse teade "Keelatud".** "Keelatud" sõnumi Exceli lisandmoodul metaandmete laadimine saamisel kontole, mis on sisse logitud, et Exceli lisandmoodul pole õigust kasutada suunatud teenuseid, näiteks või andmebaasi. Selle probleemi lahendamiseks veenduge, et õige kasutajanime kuvatakse paremas nurgas Exceli lisandmoodul. Kui vale kasutajanime, klõpsake seda, logige välja ja seejärel logige uuesti sisse.
-   **Tühi veebileht kuvatakse Exceli üle.** Kui tühi veebileht avaneb sisselogimise ajal, konto nõuab AD FS, kuid töötab lisandmooduli Exceli versiooni ei ole piisavalt tehtud, laadida sisselogimise dialoogiboksi. Probleemi lahendamiseks värskendage kasutate Exceli versiooni. Oled ettevõte, mis on edasilükkunud kanalil Exceli versiooni värskendamiseks kasutada ka [Office'i juurutamise tööriist](https://technet.microsoft.com/library/jj219422.aspx) et [praeguse kanali edasilükkunud kanal liikuda](https://technet.microsoft.com/library/mt455210.aspx).



