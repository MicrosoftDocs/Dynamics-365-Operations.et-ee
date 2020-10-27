---
title: Seerianumbriga kaupadega töötamine kassas
description: Selles teemas on selgitatud, kuidas hallata seerianumbriga kaupu kassarakenduses.
author: boycezhu
manager: annbe
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 6ba01abc3d1a4496ec586a621aa03b4981f84d76
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978359"
---
# <a name="work-with-serialized-items-in-the-pos"></a>Seerianumbriga kaupadega töötamine kassas

[!include [banner](includes/banner.md)]

Paljud jaemüüjad müüvad kaupu, mis nõuavad seerianumbri kontrollimist. Selliseid tooteid nimetatakse *serialiseeritud kaupadeks*. Mõned jaemüüjad võivad kasutada seerianumbreid jälgimisotstarbel kaupluses või laos. Teised võivad rakendada seerianumbreid müügiprotsessi ajal teeninduse ja garantii otstarbel. Selles teemas on selgitatud, kuidas saate hallata seerianumbriga kaupu Microsoft Dynamics 365 Commerce'i kassarakenduses.

## <a name="serial-number-configurations"></a>Seerianumbrite konfiguratsioonid

Kaupa loetakse serialiseeritud kaubaks, kui sellele on määratud jälgimisdimensiooni grupp, millel on lubatud seerianumbrite säte. Valige Commerce'i peakorteris lehel **Jälgimisdimensiooni grupid** suvand **Aktiivne**, et lubada seerianumbrid laoprotsessi jaoks, või valige suvand **Aktiivne müügiprotsessis**, et lubada seerianumbrid müügiprotssi jaoks.

Lülitage kiirkaardil **Jälgimisdimensioonid** sisse parameeter **Määramata sissetulekud lubatud**, et seerianumber oleks lao sissetulekute protsessis valikuline sisend serialiseeritud kauba korral. Selle parameetri väljalülitamine muudab seerianumbri nõutavaks sisendiks. Samuti kontrollib parameeter **Määramata sissetulekud lubatud**, kas varude saatmisprotsessi ajal on seerianumber nõutav.

> [!NOTE]
> Kui seerianumbri serialiseeritud kaubale registreerimiseks või kinnitamiseks soovite kasutada kassatoimingut **Sissetulevad varud** ja **Väljaminevad varud**, siis peate konfigureerima antud kauba jälgimisdimensiooni sellesse gruppi määramiseks, milles on lubatud seerianumbrite suvand **Aktiivne**, kuid mitte suvand **Aktiivne müügiprotsessis**.

## <a name="serial-number-management-page"></a>Seerianumbri halduse leht

Kui kassatoimingute **Sissetulevad varud** ja **Väljaminevad varud** korral on valitud, vastu võetud või saadetav kaup serialiseeritud kaup, sisaldab paan **Üksikasjad** valikut **Seerianumbri haldamine**, mis suunab lehele **Seerianumbri haldus**, kus saate kauba seerianumbreid registreerida või valideerida. Teise võimalusena võite avada lehe **Seerianumbri haldamine**, valides tellimuse üksikasjade rakendusribal tegevuse **Seerianumber** või valides vastuvõtu- või saatmisprotsessi käigus ilmunud dialoogiaknas suvandi **Seerianumbri haldamine**. 

Lehel **Seerianumbri haldamine** on toodud kõik registreerimise või kinnituse ootel avatud seerianumbri read. Sellel lehel võib olla kaks vahekaarti: üks käesoleva kauba kohta ja teine kõigi loetelus sisalduvate serialiseeritud kaupade kohta.

Lehe **Seerianumbri haldus** väli **Olek** annab teavet iga seerianumbri praeguse etapi kohta.

- **Pole registreeritud** – seerianumbrit ei ole esitatud või eelregistreeritud seerianumbrit ei ole veel kinnitatud (vastuvõtuprotsessis).
- **Registreerimine** – seerianumber on registreeritud ja salvestatud poe kohaliku kanali andmebaasi või eelregistreeritud seerianumber on kinnitatud. Ainult olekuga **Registreerimine** seerianumbrid esitatakse pärast vastuvõtu või täitmise lõpetamist Commerce'i peakontorile.

## <a name="receive-serialized-items"></a>Serialiseeritud kaupade vastuvõtt

Kassatoiming **Sissetulevad varud** võimaldab kasutajatel teostada serialiseeritud kaupade osas järgmisi ülesandeid.

- Seerianumbrite registreerimine seerianumbriga kaupade põhjal, kui antud kaubad on poes vastu võetud ostutellimuse alusel.
- Eelregistreeritud seerianumbrite kinnitamine seerianumbriga kaupade põhjal, kui antud kaubad on poes vastu võetud ostutellimuse või üleviimistellimuse alusel.

### <a name="register-serial-numbers-against-serialized-items"></a>Seerianumbrite registreerimine seerianumbriga kaupade põhjal

Ostutellimuse korral on seerianumbriga kauba vastuvõtuprotsessi käigus avanenud dialoogiaknas valik **Seerianumbri haldamine**. Te võite valida selle suvandi, et avada leht **Seerianumbri haldamine** ja alustada seerianumbrite registreerimist. Samuti saate selle etapi vastuvõtuprotsessi käigus vahele jätta ja esitada sisendi hiljem, enne sissetuleku sisestamist.

Vaikesättena kuvatakse käesoleva kauba vahekaart. Kõikide seerianumbriridade seerianumbri väärtus on tühi ja olek on **Pole registreeritud**. Seerianumbrite järjest sisestamiseks võite skannida seerianumbrite vöötkoodid või valida rakenduspaanil **Seerianumber**. Sisestatud seerianumbrid kuvatakse loetelus ja nende oleku väärtuseks saab **Registreerimine**. Suurim võimalik registreeritavate seerianumbrite arv on võrdne vastuvõetava kogusega. Kui teete vea, siis võite sisestatud seerianumbrite muutmiseks valida paanil **Üksikasjad** suvandi **Redigeerimine** või **Eemaldamine**.

Samuti võite registreerida seerianumbreid lehe **Seerianumbri haldamine** vahekaardil **Kõik seerianumbriga kaubad**. Valige loetelust kaup, mille suhtes soovite seerianumbreid registreerida.

### <a name="validate-serial-numbers-on-serialized-items"></a>Seerianumbriga kaupade seerianumbrite kinnitamine

Üleviimistellimuse puhul tuleb seerianumbriga kaupade seerianumbrid eelnevalt tarneprotsessi käigus väljamineku poole poolt registreerida. Ostutellimuse puhul võib tarnija esitada seerianumbri teabe saadetise eelteatise kaudu ning te saate eelnevalt registreerida tarnimisele kuuluvate kaupade numbrid. Mõlemal juhul on seerianumbrid enne vastuvõttu teada. Seetõttu peate vastuvõtu poolel vaid kinnitama, et saite kätte kauba, mille pidite kätte saama.

Seerianumbrite kinnitamiseks võite avada vastuvõtuprotsessi ajal või mis tahes muul ajal enne vastuvõtu sisestamist lehe **Seerianumbri haldus**. Sellel lehel on kõigi eelregistreeritud seerianumbriga kaupade seerianumbrid automaatselt määratud esialgsesse olekusse **Pole registreeritud**. Seerianumbrite kinnitamiseks saate need skannida või sisestada. Kui seerianumber on sisestatud, siis rakendus kontrollib, kas see vastab eelregistreeritud seerianumbrile. Kui need ühtivad, muudetakse nende olekuks **Registreerimine**. Vastasel juhul kuvatakse tõrketeade. Teise võimalusena saate seerianumbri otse valida ja seejärel teha paanil **Üksikasjad** valiku **Kinnita seerianumber**, et see seerianumber kiiresti kinnitatuks märkida. Suurim võimalik kinnitatavate seerianumbrite arv on võrdne vastuvõetava kogusega.

Samuti võite kinnitada seerianumbreid lehe **Seerianumbri haldamine** vahekaardil **Kõik seerianumbriga kaubad**. Valige loetelust kaup, mille suhtes soovite seerianumbreid kinnitada.

## <a name="ship-serialized-items"></a>Serialiseeritud kaupade saatmine

Kassatoimingu **Väljaminevad varud** abil saate registreerida seerianumbreid serialiseeritud kaupade alusel, kui saadate need üleviimistellimusena praegusest kauplusest välja.

### <a name="register-serial-numbers-against-serialized-items"></a>Seerianumbrite registreerimine seerianumbriga kaupade põhjal

Üleviimistellimuse korral on seerianumbriga kauba saatmisprotsessi käigus avanenud dialoogiaknas valik **Seerianumbri haldamine**. Te võite valida selle suvandi, et avada leht **Seerianumbri haldamine** ja alustada seerianumbrite registreerimist. Samuti saate selle etapi saatmisprotsessi käigus vahele jätta ja esitada sisendi hiljem, enne saadetise sisestamist.

Vaikesättena kuvatakse käesoleva kauba vahekaart. Kõikide seerianumbriridade seerianumbri väärtus on tühi ja olek on **Pole registreeritud**. Seerianumbrite järjest sisestamiseks võite skannida seerianumbrite vöötkoodid või valida rakenduspaanil **Seerianumber**. Sisestatud seerianumbrid kuvatakse loetelus ja nende oleku väärtuseks saab **Registreerimine**. Suurim võimalik registreeritavate seerianumbrite arv on võrdne saadetava kogusega. Kui teete vea, siis võite sisestatud seerianumbrite muutmiseks valida paanil **Üksikasjad** suvandi **Redigeerimine** või **Eemaldamine**.

Samuti võite registreerida seerianumbreid lehe **Seerianumbri haldamine** vahekaardil **Kõik seerianumbriga kaubad**. Valige loetelust kaup, mille suhtes soovite seerianumbreid registreerida.

Soovi korral saate seerianumbri registreerimise ajal lubada seerianumbri saadavuse kinnitamise väljamineva üleviimistellimuse korral. Kui selle kinnitamise korral püüate tarnida seerianumbrit, mis pole lähetava kaupluse laos saadaval, kuvatakse tõrketeade ja peate sisestama mõne muu numbri.

Sellise valideerimise lubamiseks tuleb teil eeltingimusena ajastada järgmised tööd korduvalt töötama.

- **Jaemüük ja kaubandus** > **Jaemüügi ja kaubanduse IT** > **Tooted ja varud** > **Jälgimisdimensioonidega toote saadavus**
- **Jaemüük ja kaubandus** > **Jaotusgraafikud** > **1130** (**Toote saadavus**)

## <a name="additional-resources"></a>Lisaressursid

[Sissetulev laooperatsioon kassas](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)

[Väljaminev laooperatsioon kassas](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)
