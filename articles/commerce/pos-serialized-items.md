---
title: Seerianumbriga kaupadega töötamine kassas
description: Selles teemas on selgitatud, kuidas hallata seerianumbriga kaupu kassarakenduses.
author: boycezhu
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 5725943fd249e1b5d66b08b829c2eb58b6aad3ee24db9ca83bbde9be906bbf82
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737574"
---
# <a name="work-with-serialized-items-in-the-pos"></a>Seerianumbriga kaupadega töötamine kassas

[!include [banner](includes/banner.md)]

Paljud jaemüüjad müüvad kaupu, mis nõuavad seerianumbri kontrollimist. Selliseid tooteid nimetatakse *serialiseeritud kaupadeks*. Mõned jaemüüjad võivad kasutada seerianumbreid jälgimisotstarbel kaupluses või laos. Teised võivad rakendada seerianumbreid müügiprotsessi ajal teeninduse ja garantii otstarbel. Selles teemas on selgitatud, kuidas saate hallata seerianumbriga kaupu Microsoft Dynamics 365 Commerce kassarakenduses.

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

## <a name="sell-serialized-items-in-pos"></a>Järjestatud kaupade müümine kassas

Kuigi kassarakendus on alati järjestatud kaupade müümist toetanud, saavad organisatsioonid Commerce'i versioonis 10.0.17 lubada funktsionaalsuse, mis võimendab äriloogikat, mis käivitatakse järjestatud kaupade jälgimiseks konfigureeritud kaupade müümisel.

Kui funktsioon **Võimendatud seerianumbri kontrollimine kassa tellimuse hõivamisel ja tellimuse täitmisel** on lubatud, hinnatakse järjestatud kaupade kassas müümisel järgmisi toote konfiguratsioone.

- Toote **Seeriatüübi** seadistus (**aktiivne** või **aktiivne müügis**).
- Toote sätted **Määramata väljaminekud lubatud**.
- Toote ja/või müügilao sätted **Füüsiline negatiivne laovaru**.

### <a name="active-serial-configurations"></a>Aktiivsed seeria konfiguratsioonid

Kui kaupu müüakse kassas, mis on konfigureeritud **Aktiivse** seerianumbri jälgimisdimensiooniga, algatab kassa kinnitusloogika, mis takistab kasutajatel järjestatud kauba müügi sellise seerianumbriga, mida müügilao praegustes varudes ei leita. Selle kinnitusreegli jaoks on kaks erandit.

- Kui kaup on konfigureeritud ka nii, et **Määramata väljaminekud on lubatud**, saavad kasutajad seerianumbri sisestamise vahele jätta ja müüa kauba ilma seerianumbrit määramata.
- Kui kaup ja/või müügiladu on konfigureeritud nii, et **Füüsiline negatiivne laovaru** on lubatud, aktsepteerib ja müüb rakendus seerianumbri, mida ei saa kinnitada seda müünud lao varude hulgas. See konfiguratsioon võimaldab selle konkreetse kauba/seerianumbri laotehingu negatiivseks minemise ja seega lubab süsteem tundmatude seerianumbrite müügi.

> [!IMPORTANT]
> Tagamaks, et kassarakendus saab õigesti kontrollida, kas **Aktiivse** seeria tüübiga kaupadena müüdavad seerianumbrid on müügilao varudes olemas, nõutakse, et organisatsioonid käivitavad Commerce'i peakontoris töö **Toote saadavus jälgimise dimensioonidega** ja kaasneva **1130** toote saadavuse jaotuse töö Commerce'i peakontori kaudu regulaarselt. Kui müügilattu saabub uusi järjestatud kaubavarusid, peab varude etalon kassas müüdavate seerianumbritega varude saadavuse kontrollimiseks sageli kanalite andmebaasi kõige ajakohasemate varude saadavuse andmetega värskendama. Töö **Toote saadavus jälgimisdimensioonidega** teeb hetketõmmise kõigi ladude koondlaoseisust koos seerianumbritega. Jaotustöö **1130** teeb laoseisu hetketõmmise ja jagab seda kõigi konfigureeritud kanalite andmebaasidega.

### <a name="active-in-sales-process-serial-configurations"></a>Aktiivne müügiprotsessi seeria konfiguratsioonides

Kaubad, mis on konfigureeritud seeriadimensiooniga olekus **Müügiprotsessis aktiivne** ei läbi varude kinnitamise loogikat, sest see konfiguratsioon tähendab, et varude seerianumbrid ei ole lattu eelregistreeritud ja seerianumbrid hõivatakse alles müügi ajal.  

Kui **Määramata väljaminekud lubatud** on **Müügiprotsessis aktviine** konfigureeritud kaupade jaoks konfigureeritud, saab samuti seerianumbri vahele jätta. Kui **Määramata väljaminekud lubatud** ei ole konfigureeritud, nõuab rakendus, et kasutaja sisestab seerianumbri, isegi kui seda saadaolevate varude suhtes ei kontrollita.

### <a name="apply-serial-numbers-during-creation-of-pos-transactions"></a>Kassatehingute loomise käigus seerianumbrite lisamine

Kassarakendus palub kasutajal järjestatud kauba müümisel kohe hõivata seerianumber, kuid rakendus võimaldab kasutajatel seerianumbri sisestamise teatud müügiprotsessi hetkeni vahele jätta. Kui kasutaja hakkab makset hõivama, jõustab rakendus seerianumbri kirje ja nõuab seerianumbri kirjet mis tahes kaupade puhul, mis ei ole konfigureeritud tulevaste saadetiste või pealekorjete kaudu täitmiseks. Kõik sularahas või järeletluemisega täitmistele konfigureeritud järjestatud kaubad nõuavad, et kasutaja hõivaks seerianumbri (või nõustuks selle tühjaks jätmisega, kui kauba konfiguratsioon seda võimaldab) enne müügi lõpetamist.

Tulevaseks pealekorjeks või tarneks müüdud järjestatud kaupade korral võivad kasutajad seerianumbri sisestamise esialgu vahele jätta ja klienditellimuse loomise siiski lõpule viia.   

> [!NOTE]
> Kassarakenduses järjestatud toodete müümisel või tellimuste täitmisel jõustatakse müügikandel järjestatud kauba koguseks "1". See on tingitud seerianumbri teabe jälgimisest müügireal. Kassas mitme järjestatud toote müümisel või tellimuse täitmisel peab iga rida olema konfigureeritud kogusele "1". 

### <a name="apply-serial-numbers-during-customer-order-fulfillment-or-pickup"></a>Seerianumbrite rakendamine klienditellimuse täitmisel või pealekorjel

Kui täidate järjestatud toodete klienditellimuse ridu kasutades kassa toimingut **Tellimuse täitmine**, jõustab kassa enne lõplikku täitmist seerianumbri hõivamise. Seega, kui algsel tellimuse hõivamisel seerianumbrit ei antud, tuleb see kassas komplekteerimis-, pakkimis- või lähetusprotsesside ajal hõivata. Kinnitamine toimub igas etapis ja kasutajalt küsitakse seerianumbrite andmeid ainult juhul, kui need puuduvad või enam ei kehti. Näiteks kui kasutaja jätab vahele korjamise või pakkimise etapid ja käivitab kohe saadetise ning rea seerianumbrit ei ole registreeritud, nõuab kassa seerianumbri sisestamist enne viimase arve etapi lõpetamist. Kassas tellimuse täitmistoimingute ajal seerianumbri hõivamise jõustamisel kehtivad endiselt kõik selles teemas mainitud reeglid. Järjestusega kaubad, mis on konfigureeritud **Aktiivsetena** läbivad seerianumbri laovarude kontrolli. Kaupu, mis on konfigureeritud **Müügiprotsessis aktiivsetena**, ei kontrollita. Kui **Füüsiline negatiivne laovaru** on **Aktiivsete** toodete jaoks lubatud, aktsepteeritakse mistahes seerianumbrit, olenemata laovarude saadavusest. Nii **Aktiivse** kui ka **Müügiprotsessis aktiivse** kauba korral, kui **Määramata väljaminekud lubatud** on konfigureeritud, saab kasutaja jätta seerianumbrid soovi korral korjamise, pakkimise ja saatmise etappides tühjaks.

Seerianumbrite kontrollid tehakse ka siis, kui kasutaja teeb kassas klienditellimustega pealekorjetoiminguid. Kassarakendus või luba järjestatud toote pealekorje enne, kui see läbib varem mainitud kontrollid. Kontrollid põhinevad alati toote jälgimise dimensioonil ja müügilao konfiguratsioonidel. 

## <a name="additional-resources"></a>Lisaressursid

[Sissetulev laooperatsioon kassas](./pos-inbound-inventory-operation.md)

[Väljaminev laooperatsioon kassas](./pos-outbound-inventory-operation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]