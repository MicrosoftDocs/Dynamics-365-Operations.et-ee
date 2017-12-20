---
title: Exceli lisandmooduli kasutamine
description: "See teema selgitab, kuidas avada üksuse andmeid Microsoft Excelis, ja seejärel vaadata, värskendada ja redigeerida andmeid, kasutades Microsoft Dynamics Office’i Excelile mõeldud lisandmoodulit."
author: ChrisGarty
manager: AnnBe
ms.date: 11/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bf2607596993d01abaf5e8a66f14f8c091791d4a
ms.openlocfilehash: b4151ca929d0dbe073c1a8444cf63a90ac74e20c
ms.contentlocale: et-ee
ms.lasthandoff: 11/27/2017

---

# <a name="use-the-excel-add-in"></a>Exceli lisandmooduli kasutamine

[!include[banner](../includes/banner.md)]

See teema selgitab, kuidas avada üksuse andmeid Microsoft Excelis, ja seejärel vaadata, värskendada ja redigeerida andmeid, kasutades Microsoft Dynamics Office’i Excelile mõeldud lisandmoodulit. Üksuse andmete avamiseks saate käivitada Exceli või rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition kaudu.

Kui avate üksuse andmed Excelis, saate neid kiiresti ja hõlpsasti vaadata ja redigeerida, kasutades Exceli lisandmoodulit. See lisandmoodul nõuab rakendust Microsoft Excel 2016.

> [!NOTE]
> Kui teie Microsoft Azure Active Directory (Azure AD) rentnik konfigureeritakse kasutama teenust Active Directory Federation Services (AD FS), peate veenduma, et Office’i 2016. aasta mai värskendus on rakendatud nii, et Exceli lisandmoodul saab teid korrektselt sisse logida.

## <a name="open-entity-data-in-excel-when-you-start-from-finance-and-operations"></a>Avage üksuse andmed Excelis rakenduse Finance and Operations käivitamisel
1. Valige rakenduse Finance and Operations käsk **Ava Microsoft Office’is**.

    Kui lehe juurandmete allikas (tabel) on sama kui mis tahes üksuste juurandmeallikas, luuakse lehe jaoks vaikesuvandid **Ava Excelis**. Suvandid **Ava Excelis** on leitavad sagedasti kasutatavatel lehtedel, nagu **Kõik hankijad** ja **Kõik kliendid**.
 
2. Valige käsk **Ava Excelis** ja avage loodav töövihik. Sellel töövihikul on üksuse jaoks sidumisteave, osuti teie keskkonnale ja osuti Exceli lisandmoodulile.
3. Valige Excelis käsk **Luba redigeerimine**, et lubada Exceli lisandmooduli käivitamine. Exceli lisandmoodul töötab Exceli akna paremal küljel olevas paanis.
4. Kui käivitate Exceli lisandmooduli esimest korda, valige käsk **Usalda seda lisandmoodulit**.
5. Kui teil palutakse sisse logida, valige käsk **Logi sisse** ja seejärel logige sisse, kasutades samu mandaate, mida kasutasite rakendusse Finance and Operations sisselogimisel. Exceli lisandmoodul kasutab varasemat Internet Exploreri sisselogimise konteksti ja logib teid võimaluse korral automaatselt sisse. Seetõttu kinnitage kasutajanimi Exceli lisandmooduli paremal ülanurgas.

Exceli lisandmoodul loeb automaatselt valitud üksuse andmeid. Pange tähele, et töövihikus ei ole andmeid, kuni Exceli lisandmoodul loeb need sisse.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Üksuse andmete avamine Exceli kaudu käivitamisel
1. Valige Excelis vahekaardil **Lisa** grupis **Lisandmoodulid** suvand **Store**, et avada Office Store.
2. Office Store’is otsige märksõna **Dynamics** ja seejärel valige käsk **Lisa**, mis asub valiku **Microsoft Dynamicsi Office’i lisandmoodul** (Exceli lisandmoodul) kõrval.
3. Kui käivitate Exceli lisandmooduli esimest korda, valige käsk **Usalda seda lisandmoodulit**, et lubada Exceli lisandmooduli käivitamine. Exceli lisandmoodul töötab Exceli akna paremal küljel olevas paanis.
4. Valige suvand **Serveriteabe lisamine**, et avada paan **Suvandid**.
5. Kopeerige brauseris URL rakenduse Finance and Operations sihteksemplari URL, kleepige see väljale **Serveri URL** ja seejärel kustutage kõik, mis järgneb hostinimele. Tulemuseks saadav URL peaks sisaldama ainult hostinime.

    Näiteks kui URL on `https://xxx.dynamics.com/?cmp=usmf&amp;mi=CustTableListPage`, kustutage kõik peale `https://xxx.dynamics.com`.

6. Muudatuse kinnitamiseks valige **OK** ja seejärel **Jah**. Exceli lisandmoodul taaskäivitub ja laadib metaandmed.

    Nupp **Kujundus** on nüüd saadaval. Kui Exceli lisandmoodulil on nupp **Aplettide laadimine**, pole te tõenäoliselt õige kasutajana sisse logitud. Lisateabe saamiseks vaadake selle teema jaotises [Tõrkeotsing](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in#troubleshooting) olevat nuppu „Kuvatakse nupp Aplettide laadimine”.

7. Valige **Kujundus**. Exceli lisandmoodul toob üksuse metaandmed.
8. Valige käsk **Lisa tabel**. Ilmub olemite loend. Olemid on esitatud vormingus „Nimi – silt”.
9. Valige loendis üksus, nagu **Kliendid – kliendid**, ja seejärel valige suvand **Edasi**.
10. Välja lisamiseks loendist **Saadaolevad väljad** loendisse **Valitud väljad** valige väli ja seejärel nupp **Lisa**. Võite ka topeltklõpsata välja loendis **Saadolevad väljad**.
11. Pärast soovitud väljade loendisse **Valitud väljad** lisamist veenduge, et kursor oleks töölehel õiges kohas (nt lahter A1), ja seejärel valige nupp **Valmis**. Kujundajast väljumiseks valige nupp **Valmis**.
12. Andmekogumi sissetõmbamiseks valige käsk **Värskenda**.

## <a name="view-and-update-entity-data-in-excel"></a>Üksuse andmete vaatamine ja värskendamine Excelis
Pärast seda, kui Exceli lisandmoodul loeb üksuse andmed töövihikusse, saate värskendada andmeid igal ajal, valides Exceli lisandmoodulis nupu **Värskenda**.

## <a name="edit-entity-data-in-excel"></a>Üksuse andmete redigeerimine Excelis
Saate muuta üksuse andmeid vastavalt vajadusele ja avaldada selle seejärel tagasi, valides Exceli lisandmoodulis nupu **Avalda**. Kirje redigeerimiseks valige töölehel lahter ja muutke seejärel lahtri väärtust. Uue kirje lisamiseks järgige üht järgmist juhist.

- Klõpsake andmeallikate tabelis mis tahes kohas ja seejärel valige Exceli lisandmoodulis nupp **Uus**.
- Klõpsake andmeallikate tabeli viimases reas ja seejärel vajutage tabulaatoriklahvi, kuni kursor liigub selle rea viimasest veerust välja ja luuakse uus rida.
- Klõpsake vahetult andmeallikate tabeli all olevas reas ja alustage lahtrisse andmete sisestamist. Kui liigutate fookuse sellest lahtrist välja, laieneb tabel uue rea kaasamiseks.
- Päisekirjete väljaseoste puhul valige üks väli ja seejärel valige Exceli lisandmoodulis nupp **Uus**.

Pange tähele, et uue kirje saab luua ainult siis, kui kõik põhi- ja kohustuslikud väljad on töölehel seotud või kui filtritingimusi kasutades on vaikeväärtused sisestatud.

Kirje kustutamiseks järgige üht nendest juhistest.

- Paremklõpsake kustutatava töölehe rea kõrval olevat rea numbrit ja seejärel valige käsk **Kustuta**.
- Paremklõpsake kustutatava töölehe rea kõrval olevas reas ja seejärel valige **Kustuta** &gt; **Tabeli read**.

Kui andmeallikad on lisatud seotud andmeallikatena, avaldatakse päis enne ridu. Kui teiste andmeallikate vahel esineb sõltuvusi, võite muuta avaldamise vaikejärjekorda. Avaldamise järjekorra muutmiseks valige Exceli lisandmoodulis nupp **Suvandid** (hammasrattasümbol) ja seejärel valige kiirkaardil **Andmekonnektor** käsk **Konfigureeri avaldamisjärjekorda**.

## <a name="add-or-remove-columns"></a>Lisa või eemalda veerge
Saate kasutada kujundajat, et reguleerida veerge, mis lisatakse automaatselt töölehele.

> [!NOTE]
> Kui nuppu **Kujundus** ei kuvata Exceli lisandmoodulis nupu **Filter** all, peate lubama andmeallika kujundaja. Valige nupp **Suvandid** (hammasrattasümbol) ja seejärel märkige ruut **Luba kujundus**.

1. Valige Exceli lisandmoodulis suvand **Kujundus**. Kõik andmeallikad on nimetatud.
2. Valige andmeallika kõrval käsk **Redigeeri** (pliiatsisümbol).
3. Reguleerige väljade loendit vastavalt vajadusele loendis **Valitud väljad**.

    - Välja lisamiseks loendist **Saadaolevad väljad** loendisse **Valitud väljad** valige väli ja seejärel nupp **Lisa**. Võite ka topeltklõpsata välja loendis **Saadolevad väljad**.
    - Välja loendist **Valitud väljad** eemaldamiseks valige väli ja seejärel käsk **Eemalda**. Teise võimalusena topeltklõpsake välja.
    - Väljade järjestuse muutmiseks valige väli loendis **Valitud väljad** ja seejärel klõpsake nuppu **Üles** või **Alla**.

4. Andmeallikale tehtud muudatuste rakendamiseks valige käsk **Värskenda**. Kujundajast väljumiseks valige nupp **Valmis**.
5. Kui lisasite välja (veerg), valige käsk **Värskenda**, et tõmmata sisse värskendatud andmekogum.

## <a name="troubleshooting"></a>Tõrkeotsing
On mõned probleemid, mida saab lahendada mõne lihtsa juhise kaudu.

- **Kuvatakse nupp Aplettide laadimine**: kui Exceli lisandmoodulil on pärast sisselogimist nupp **Aplettide laadimine**, pole te tõenäoliselt õige kasutajana sisse logitud. Selle probleemi lahendamiseks veenduge, et Exceli paremas ülanurgas ilmub õige kasutaja. Kui ilmub vale kasutajanimi, valige see, logige välja ja logige tagasi sisse.
- **Kuvatakse teade „Keelatud”**: kui näete Exceli lisandmoodulis metaandmete laadimise ajal teadet „Keelatud”, siis ei ole kontol, mis on Exceli lisandmoodulisse sisse logitud, õigust kasutada sihtteenust, -eksemplari või -andmebaasi. Selle probleemi lahendamiseks veenduge, et Exceli paremas ülanurgas ilmub õige kasutaja. Kui ilmub vale kasutajanimi, valige see, logige välja ja logige tagasi sisse.
- **Excelis kuvatakse tühi veebileht**: kui sisselogimisprotsessi käigus avaneb tühi veebileht, nõuab konto AD FS-i, kuid lisandmoodulit sisaldav Exceli versioon pole sisselogimise dialoogiboksi laadimiseks piisavalt hiljutine. Selle probleemi lahendamiseks värskendage kasutatavat Exceli versiooni. Exceli versiooni värskendamiseks, kui olete viitkanalis asuvas ettevõttes, kasutage tööriista [Office’i juurutustööriist](https://technet.microsoft.com/library/jj219422.aspx), et [liikuda edasilükatud kanalist praegusesse kanalisse](https://technet.microsoft.com/library/mt455210.aspx).

