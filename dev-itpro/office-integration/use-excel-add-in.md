---
title: Exceli lisandmooduli kasutamine
description: "See teema selgitab, kuidas avada üksuse andmeid Microsoft Excelis, ja seejärel vaadata, värskendada ja redigeerida andmeid, kasutades Microsoft Dynamics Office’i Excelile mõeldud lisandmoodulit."
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 06fc9f8dda83fddea9ae331bb82c8874b15d76b9
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---

# <a name="use-the-excel-add-in"></a>Exceli lisandmooduli kasutamine

[!include[banner](../includes/banner.md)]


See teema selgitab, kuidas avada üksuse andmeid Microsoft Excelis, ja seejärel vaadata, värskendada ja redigeerida andmeid, kasutades Microsoft Dynamics Office’i Excelile mõeldud lisandmoodulit. Üksuse andmete avamiseks saate käivitada Exceli või rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition kaudu.

Üksuse andmete avamisel Microsoft Excelis saate kiiresti ja hõlpsasti vaadata ja redigeerida andmeid, kasutades Microsoft Dynamics Office’i Exceli jaoks mõeldud lisandmoodulit. See lisandmoodul nõuab rakendust Microsoft Excel 2016. **Märkus.** Kui teie Microsoft Azure Active Directory (Azure AD) rentnik konfigureeritakse kasutama teenust Active Directory Federation Services (AD FS), peate veenduma, et 2016. aasta mai värskendus on rakendatud nii, et Exceli lisandmoodul saab teid korrektselt sisse logida.

## <a name="open-entity-data-in-excel-when-you-start-from-dynamics-365-for-finance-and-operations"></a>Avage üksuse andmed Excelis rakenduse Dynamics 365 for Finance and Operations käivitamisel
1.  Rakenduse Microsoft Dynamics 365 for Finance and Operations lehel klõpsake nuppu **Ava Microsoft Office’is**. Kui lehe juurandmete allikas (tabel) on sama kui mis tahes üksuste juurandmeallikas, luuakse lehe jaoks vaikesuvandid **Ava Excelis**. Suvandid **Ava Excelis** on leitavad sagedasti kasutatavatel lehtedel, nagu **Kõik hankijad** ja **Kõik kliendid**.
2.  Klõpsake suvandit **Ava Excelis** ja avage loodav töövihik. Sellel töövihikul on üksuse jaoks sidumisteave, osuti teie keskkonnale ja osuti Exceli lisandmoodulile.
3.  Excelis klõpsake nuppu **Redigeerimise lubamine**, et lubada Exceli lisandmooduli käivitamine. Exceli lisandmoodul töötab Exceli akna paremal küljel olevas paanis.
4.  Kui käivitate Exceli lisandmooduli esimest korda, klõpsake nuppu **Usalda seda lisandmoodulit**.
5.  Kui teil palutakse sisse logida, klõpsake nuppu **Logi sisse** ja seejärel logige sisse, kasutades samu mandaate, mida kasutasite rakendusse Dynamics 365 for Finance and Operations sisselogimisel. Exceli lisandmoodul kasutab varasemat Internet Exploreri sisselogimise konteksti ja logib teid võimaluse korral automaatselt sisse. Seetõttu kinnitage kasutajanimi Exceli lisandmooduli paremal ülanurgas.

Exceli lisandmoodul loeb automaatselt valitud üksuse andmeid. Pange tähele, et töövihikus ei ole andmeid, kuni Exceli lisandmoodul loeb need sisse.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Üksuse andmete avamine Exceli kaudu käivitamisel
1.  Klõpsake Excelis vahekaardil **Lisa** grupis **Lisandmoodulid** nuppu **Ladu**, et avada Office Store.
2.  Office Store’is otsige märksõna „Dynamics” ja klõpsake nuppu **Lisa**, mis asub valiku **Microsoft Dynamicsi Office’i lisandmoodul** (Exceli lisandmoodul) kõrval.
3.  Kui käivitate Exceli lisandmooduli esimest korda, klõpsake nuppu **Usalda seda lisandmoodulit**, et lubada Exceli lisandmooduli käivitamine. Exceli lisandmoodul töötab Exceli akna paremal küljel olevas paanis.
4.  Klõpsake nuppu **Serveriteabe lisamine**, et avada paan **Suvandid**.
5.  Kopeerige brauseri URL rakenduse Dynamics 365 for Finance and Operations sihteksemplari, kleepige see väljale **Serveri URL** ja seejärel kustutage kõik hostinime järelt. Tulemuseks saadav URL peaks sisaldama ainult hostinime.
Näiteks kui URL on https://xxx.dynamics.com/?cmp=usmf&amp;mi=CustTableListPage, kustutage kõik peale **https://xxx.dynamics.com**.
6.  Klõpsake **OK** ja seejärel klõpsake muudatuse kinnitamiseks nuppu **Jah**. Exceli lisandmoodul taaskäivitab ja laadib metaandmed. Nupp **Kujundus** on nüüd saadaval. Kui Exceli lisandmoodulil on nupp **Aplettide laadimine**, pole te tõenäoliselt õige kasutajana sisse logitud. Lisateabe saamiseks vaadake selle teema jaotises „Tõrkeotsing” olevat nuppu „Kuvatakse nupp Aplettide laadimine”.
7.  Klõpsake valikut **Kujundus**. Exceli lisandmoodul toob üksuse metaandmed.
8.  Klõpsake nuppu **Lisa tabel**. Ilmub olemite loend. Olemid on esitatud vormingus „Nimi – silt”.
9.  Valige loendis üksus, nagu **Kliendid – kliendid** ja klõpsake seejärel nuppu **Edasi**.
10. Välja lisamiseks loendist **Saadaolevad väljad** loendisse **Valitud väljad** klõpsake välja ja seejärel nuppu **Lisa**. Teise võimalusena topeltklõpsake välja.
11. Pärast soovitud väljade loendisse **Valitud väljad** lisamist veenduge, et kursor oleks töölehel õiges kohas (nt lahter A1), ja klõpsake seejärel nuppu **Valmis**. Kujundajast väljumiseks klõpsake seejärel nuppu **Valmis**.
12. Andmekogumi sissetõmbamiseks klõpsake nuppu **Värskenda**.

## <a name="view-and-update-entity-data-in-excel"></a>Üksuse andmete vaatamine ja värskendamine Excelis
Pärast seda, kui Exceli lisandmoodul loeb üksuse andmed töövihikusse, saate värskendada andmeid igal ajal, klõpsates Exceli lisandmoodulis nuppu **Värskenda**.

## <a name="edit-entity-data-in-excel"></a>Üksuse andmete redigeerimine Excelis
Saate muuta üksuse andmeid vastavalt vajadusele ja avaldada selle seejärel tagasi, klõpsates Exceli lisandmoodulis nuppu **Avalda**. Kirje redigeerimiseks valige töölehel lahter ja muutke seejärel lahtri väärtust. Uue kirje lisamiseks järgige üht järgmist juhist.

-   Klõpsake andmeallikate tabelis mis tahes kohas ja seejärel klõpsake Exceli lisandmoodulis nuppu **Uus**.
-   Klõpsake andmeallikate tabeli viimases reas ja seejärel vajutage tabulaatoriklahvi, kuni kursor liigub selle rea viimasest veerust välja ja luuakse uus rida.
-   Klõpsake vahetult andmeallikate tabeli all olevat rida ja alustage lahtrisse andmete sisestamist. Kui liigutate fookuse sellest lahtrist välja, laieneb tabel uue rea kaasamiseks.
-   Päisekirjete väljaseoste puhul klõpsake üht välja ja seejärel klõpsake Exceli tabelis nuppu **Uus**..

Pange tähele, et uue kirje saab luua ainult siis, kui kõik põhi- ja kohustuslikud väljad on töölehel seotud või kui filtritingimusi kasutades on vaikeväärtused sisestatud.
Kirje kustutamiseks järgige üht nendest juhistest.

-   Paremklõpsake kustutatava töölehe rea kõrval olevat rea numbrit ja klõpsake seejärel nuppu **Kustuta**.
-   Paremklõpsake kustutatava töölehe rea kõrval olevat rea numbrit ja klõpsake seejärel nuppu **Kustuta** &gt; **Tabeliread**.
Kui andmeallikad on lisatud seotuna, avaldatakse päis enne ridu. Kui teiste andmeallikate vahel esineb sõltuvusi, võite muuta avaldamise vaikejärjekorda. Avaldamisjärjekorra muutmiseks klõpsake Exceli lisandmoodulis nuppu **Suvandid** (hammasrattaikoon). Seejärel klõpsake kiirkaardil **Andmekonnektor** valikut **Avaldamisjärjekorra konfigureerimine**.

## <a name="add-or-remove-columns"></a>Lisa või eemalda veerge
Saate kasutada kujundajat, et reguleerida veerge, mis lisatakse automaatselt töölehele.

1.  Käivitage Exceli lisandmooduli andmeallika kujundaja, klõpsates nuppu **Suvandid** (hammasratta sümbol) ja märkides seejärel ruudu **Luba kujundamine**.
2.  Klõpsake Exceli lisandmoodulis nuppu **Kujundus**. Kõik andmeallikad on nimetatud.
3.  Andmeallika kõrval klõpsake nuppu **Redigeeri** (pliiatsi sümbol).
4.  Reguleerige loendis **Valitud väljad** olevat loendit vastavalt vajadusele.
    -   Välja lisamiseks loendist **Saadaolevad väljad** loendisse **Valitud väljad** klõpsake välja ja seejärel nuppu **Lisa**. Teise võimalusena topeltklõpsake välja.
    -   Välja loendist **Valitud väljad** eemaldamiseks klõpsake välja ja seejärel klõpsake nuppu **Eemalda**. Teise võimalusena topeltklõpsake välja.
    -   Väljade järjestuse muutmiseks klõpsake loendis **Valitud väljad** soovitud välja ja seejärel klõpsake nuppu **Üles** või **Alla**.

5. Andmeallikale tehtud muudatuste rakendamiseks klõpsake nuppu **Värskenda**. Kujundajast väljumiseks klõpsake seejärel nuppu **Valmis**. 
6. Kui lisasite välja (veerg), klõpsake nuppu **Värskenda**, et tõmmata sisse värskendatud andmekogum.

## <a name="troubleshooting"></a>Tõrkeotsing
On mõned probleemid, mida saab lahendada mõne lihtsa juhise kaudu.

-   **Kuvatakse nupp Aplettide laadimine.** Kui Exceli lisandmoodulil on pärast sisselogimist nupp **Aplettide laadimine**, pole te tõenäoliselt õige kasutajana sisse logitud. Selle probleemi lahendamiseks veenduge, et Exceli paremas ülanurgas ilmub õige kasutaja. Kui ilmub vale kasutajanimi, klõpsake seda, logige välja ja logige tagasi sisse.
-   **Saate sõnumi „Keelatud”.** Kui saate ajal, mil Exceli lisandmoodul laadib metaandmeid, sõnumi „Keelatud”, siis ei ole kontol, mis on Exceli lisandmoodulisse sisse logitud, õigust kasutada sihtteenust, -eksemplari või -andmebaasi. Selle probleemi lahendamiseks veenduge, et Exceli paremas ülanurgas ilmub õige kasutaja. Kui ilmub vale kasutajanimi, klõpsake seda, logige välja ja logige tagasi sisse.
-   **Exceli kohal kuvatakse tühi veebileht.** Kui tühi veebileht avaneb sisselogimisprotsessi käigus, nõuab konto AD FS-i, kuid lisandmoodulit sisaldav Exceli versioon pole sisselogimise dialoogiboksi laadimiseks piisavalt hiljutine. Selle probleemi lahendamiseks värskendage kasutatavat Exceli versiooni. Exceli versiooni värskendamiseks, kui olete viitkanalis asuvas ettevõttes, kasutage tööriista [Office’i juurutustööriist](https://technet.microsoft.com/library/jj219422.aspx), et [liikuda edasilükatud kanalist praegusesse kanalisse](https://technet.microsoft.com/library/mt455210.aspx).





