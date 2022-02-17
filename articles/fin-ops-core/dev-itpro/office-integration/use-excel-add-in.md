---
title: Üksuse andmete vaatamine ja värskendamine Exceliga
description: See teema selgitab, kuidas avada üksuse andmeid Microsoft Excelis ning neid seejärel vaadata, värskendada ja redigeerida Microsoft Dynamicsi Excelile lisandmooduli abil.
author: jasongre
ms.date: 10/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1593206e8e22aed518ebca9bee0772c6620bec9
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068788"
---
# <a name="view-and-update-entity-data-with-excel"></a>Üksuse andmete vaatamine ja värskendamine Exceliga 

[!include [applies to](../includes/applies-to-commerce-finance-scm.md)]

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]


See teema selgitab, kuidas avada üksuse andmeid Microsoft Excelis ning neid seejärel vaadata, värskendada ja redigeerida Microsoft Dynamicsi Excelile lisandmooduli abil. Olemiandmete avamiseks saate alustada exceli või finance and Operationsi rakendustest.

Kui avate üksuse andmed Excelis, saate neid kiiresti ja hõlpsasti vaadata ja redigeerida, kasutades Exceli lisandmoodulit. See lisandmoodul nõuab rakendust Microsoft Excel 2016 või uuemat.

> [!NOTE]
> Kui teie Microsoft Azure Active Directory (Azure AD) rentnik konfigureeritakse kasutama teenust Active Directory Federation Services (AD FS), peate veenduma, et Office’i 2016. aasta mai värskendus oleks rakendatud, nii et Exceli lisandmoodul saab teid korrektselt sisse logida.

Exceli lisandmooduli kasutamise juhiste kohta lisateabe saamiseks vaadake lühivideot [Exceli malli loomine päise ja reamustrite jaoks](https://youtu.be/RTicLb-6dbI).

## <a name="open-entity-data-in-excel-when-you-start-from-a-finance-and-operations-app"></a>Olemiandmete avamine Excelis rakendusest Finance and Operations käivitamisel
1. Valige **rakenduse Finance and Operations lehel Ava rakenduses Microsoft Office**.

    Kui lehe juurandmete allikas (tabel) on sama kui mis tahes üksuste juurandmeallikas, luuakse lehe jaoks vaikesuvandid **Ava Excelis**. Suvandid **Ava Excelis** on leitavad sagedasti kasutatavatel lehtedel, nagu **Kõik hankijad** ja **Kõik kliendid**.
 
2. Valige käsk **Ava Excelis** ja avage loodav töövihik. Sellel töövihikul on üksuse jaoks sidumisteave, osuti teie keskkonnale ja osuti Exceli lisandmoodulile.
3. Valige Excelis käsk **Luba redigeerimine**, et lubada Exceli lisandmooduli käivitamine. Exceli lisandmoodul töötab Exceli akna paremal küljel olevas paanis.
4. Kui käivitate Exceli lisandmooduli esimest korda, valige käsk **Usalda seda lisandmoodulit**.
5. Kui teil palutakse sisse logida, valige **sisselogimine** ja seejärel logige sisse, kasutades samu mandaate, mida kasutasite rakendusse Finance and Operations sisselogimiseks. Exceli lisandmoodul kasutab varasemat brauseri sisselogimise konteksti ja logib teid võimaluse korral automaatselt sisse. (Lisateavet operatsioonisüsteemil põhineva brauseri kohta vt teemast [Office’i lisandmoodulite kasutatavad brauserid](/office/dev/add-ins/concepts/browsers-used-by-office-web-add-ins.) Veendumaks, et sisselogimine õnnestus, kontrollige kasutajanime Exceli lisandmooduli ülemises parempoolses nurgas. 

Exceli lisandmoodul loeb automaatselt valitud üksuse andmeid. Pange tähele, et töövihikus ei ole andmeid, kuni Exceli lisandmoodul loeb need sisse.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Üksuse andmete avamine Exceli kaudu käivitamisel
1. Valige Excelis vahekaardil **Lisa** grupis **Lisandmoodulid** suvand **Store**, et avada Office Store.
2. Office Store’is otsige märksõna **Dynamics** ja seejärel valige käsk **Lisa**, mis asub valiku **Microsoft Dynamics Office’i lisandmoodul** (Exceli lisandmoodul) kõrval.
3. Kui käivitate Exceli lisandmooduli esimest korda, valige käsk **Usalda seda lisandmoodulit**, et lubada Exceli lisandmooduli käivitamine. Exceli lisandmoodul töötab Exceli akna paremal küljel olevas paanis.
4. Valige suvand **Serveriteabe lisamine**, et avada paan **Suvandid**.
5. Kopeerige brauseris oma rakenduse Finance and Operations URL, kleepige see väljale **Serveri URL** ja kustutage seejärel kõik pärast hostinime. Tulemuseks saadav URL peaks sisaldama ainult hostinime.

    Näiteks kui URL on `https://xxx.dynamics.com/?cmp=usmf&amp;mi=CustTableListPage`, kustutage kõik peale `https://xxx.dynamics.com`.

6. Muudatuse kinnitamiseks valige **OK** ja seejärel **Jah**. Exceli lisandmoodul taaskäivitub ja laadib metaandmed.

    Nupp **Kujundus** on nüüd saadaval. Kui Exceli lisandmoodulil on link **Aplettide laadimine**, pole te tõenäoliselt õige kasutajana sisse logitud. Lisateabe saamiseks selle probleemi lahendamise kohta vaadake [Aplettide laadimine](../office-integration/office-integration-troubleshooting.md#issue-the-excel-add-in-loads-but-instead-of-showing-data-it-displays-load-applets-in-the-task-pane) veaotsingu kirjet.

7. Valige **Kujundus**. Exceli lisandmoodul toob üksuse metaandmed.
8. Valige käsk **Lisa tabel**. Ilmub olemite loend. Olemid on esitatud vormingus „Nimi – silt”.
9. Valige loendis üksus, nagu **Kliendid – kliendid**, ja seejärel valige suvand **Edasi**.
10. Välja lisamiseks loendist **Saadaolevad väljad** loendisse **Valitud väljad** valige väli ja seejärel nupp **Lisa**. Võite ka topeltklõpsata välja loendis **Saadolevad väljad**.
11. Pärast soovitud väljade loendisse **Valitud väljad** lisamist veenduge, et kursor oleks töölehel õiges kohas (nt lahter A1), ja seejärel valige nupp **Valmis**. Kujundajast väljumiseks valige nupp **Valmis**.
12. Andmekogumi sissetõmbamiseks valige käsk **Värskenda**.

## <a name="view-and-update-entity-data-in-excel"></a>Üksuse andmete vaatamine ja värskendamine Excelis
Pärast seda, kui Exceli lisandmoodul loeb üksuse andmed töövihikusse, saate värskendada andmeid igal ajal, valides Exceli lisandmoodulis nupu **Värskenda**.

## <a name="edit-entity-data-in-excel"></a>Üksuse andmete redigeerimine Excelis
Olemiandmeid saate vastavalt vajadusele muuta ja seejärel avaldada need tagasi finance and Operationsi rakendustesse, valides **Exceli lisandmoodulis avalda**. Kirje redigeerimiseks valige töölehel lahter ja muutke seejärel lahtri väärtust. Uue kirje lisamiseks järgige üht järgmist juhist.

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

## <a name="change-the-publish-batch-size"></a>Avaldamispartii suuruse muutmine
Kui kasutajad avaldavad andmekirjete muudatusi Exceli lisandmooduli abil, esitatakse värskendused pakettidena. Avaldamise vaikepartii suurus on 100 rida. Versioonis 10.0.17 ja hilisemates versioonides võimaldab funktsioon **Luba Exceli lisandmoodulis avaldamise partii suuruse konfigureerimine** teil paindlikult kontrollida avaldamise partii mahte.

Süsteemiadministraatorid saavad määrata kogu süsteemi hõlmava limiidi, määrates avaldamise partii suuruse töövihikute „Ava Excelis” jaoks, häälestades lehe **Office’i rakenduse parameetrid** jaotises **Rakenduse parameetrid** välja **Avalda partiilimiit**.

Avaldamispartii suurust saab üksiku töövihiku jaoks muuta ka Exceli lisandmooduli abil.

1. Avage töövihik Excelis.
2. Valige Exceli lisandmooduli ülemises parempoolses nurgas nupp **Suvand** (hammasratas).
3. Määrake väli **Avaldamispartii suurus** soovitud viisil. Teie määratud väärtus peab olema väiksem kui kogu süsteemi hõlmav avaldamispartii limiit.
4. Valige nupp **OK**.
5. Salvestage töövihik. Kui te ei salvesta töövihikut pärast lisandmooduli sätetes muudatuste tegemist, ei püsi need muudatused töövihiku uuesti avamisel.

Exceli töövihiku mallide autorid saavad kasutada sama protseduuri, et seada mallide jaoks avaldamise partii suurus enne, kui nad need süsteemi üles laadivad.

## <a name="copy-environment-data"></a>Kopeeri keskkonna andmed

Ühest keskkonnast töövihikusse toodud andmeid saab kopeerida muusse keskkonda. Siiski ei saa lihtsalt ühenduse URL-i muuta, kuna töövihiku andmete vahemälu käsitleb ka edaspidi andmeid olemasolevate andmetena. Selle asemel tuleb kasutada funktsiooni Keskkonna andmete kopeerimine, et kopeerida andmed uude keskkonda uute andmetena.

1. Valige nupp **Suvandid** (hammasrattasümbol) ja seejärel valige kiirkaardil **Andmekonnektor** suvand **Keskkonna andmete kopeerimine**. 
2. Sisestage uue keskkonna serveri URL. 
3. Tegevuse kinnitamiseks valige **OK** ja seejärel **Jah**. Exceli lisandmoodul taaskäivitub ja loob ühenduse uue keskkonnaga. Töövihiku olemasolevaid andmeid käsitletakse uute andmetena.

    Pärast Exceli lisandmooduli taaskäivitumist ilmub teateaken, mis annab teada, et töövihik on keskkonna kopeerimise režiimis.

4. Valige käsk **Avalda**, et kopeerida andmed uude keskkonda uute andmetena. Keskkonna kopeerimise operatsiooni tühistamiseks ja uues keskkonnas olemasolevate andmete ülevaatamiseks valige käsk **Värskenda**.

## <a name="troubleshooting"></a>Tõrkeotsing
On mõned probleemid, mida saab lahendada mõne lihtsa juhise kaudu.

- **Link „Aplettide laadimine" on näidatud** – Lisateabe saamiseks selle probleemi lahendamise kohta vaadake [Aplettide laadimine](../office-integration/office-integration-troubleshooting.md#issue-the-excel-add-in-loads-but-instead-of-showing-data-it-displays-load-applets-in-the-task-pane) veaotsingu kirjet. 
- **Kuvatakse teade „Keelatud”**: kui näete Exceli lisandmoodulis metaandmete laadimise ajal teadet „Keelatud”, siis ei ole kontol, mis on Exceli lisandmoodulisse sisse logitud, õigust kasutada sihtteenust, -eksemplari või -andmebaasi. Selle probleemi lahendamiseks veenduge, et Exceli paremas ülanurgas ilmub õige kasutaja. Kui ilmub vale kasutajanimi, valige see, logige välja ja logige tagasi sisse.
- **Excelis kuvatakse tühi veebileht**: kui sisselogimisprotsessi käigus avaneb tühi veebileht, nõuab konto AD FS-i, kuid lisandmoodulit sisaldav Exceli versioon pole sisselogimise dialoogiboksi laadimiseks piisavalt hiljutine. Selle probleemi lahendamiseks värskendage kasutatavat Exceli versiooni. Exceli versiooni värskendamiseks, kui olete viitkanalis asuvas ettevõttes, kasutage tööriista [Office’i juurutustööriist](/deployoffice/overview-office-deployment-tool), et [liikuda edasilükatud kanalist praegusesse kanalisse](/deployoffice/overview-update-channels).
- **Ajalõpu periood andmete muudatuste avaldamise ajal** – kui saate ajalõpu teate sel ajal, kui proovite üksuses andmemuudatusi avaldada, kaaluge mõjutatud töövihiku avaldamise partii suuruse vähendamist. Üksused, mis käivitavad kirjete muudatuste puhul suurema loogika hulga, nõuavad värskenduste saatmist väiksemates partiides, et vältida ajalõppe.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
