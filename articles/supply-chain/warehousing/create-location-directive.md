---
title: Asukohakorraldustega töötamine
description: See teema kirjeldab, kuidas töötada asukohakorraldustega. Asukohakorraldused on kasutaja määratud reeglid, mis aitavad tuvastada komplekteerimise ja ladustamise asukohti varude liigutamisel.
author: Mirzaab
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSLocDirHint, WHSLocDirTableUOM, WHSLocDirFailure
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-11-13
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 780902bf6abb0fe93ca9c57be6aa75ee5bc121b1779ea42effdaa0c7f08b5e1b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746839"
---
# <a name="work-with-location-directives"></a>Asukohakorraldustega töötamine

[!include [banner](../includes/banner.md)]

Asukoha korraldused on reeglid, mis aitavad tuvastada komplekteerimise ja mahapanemise asukohti varude liigutamisel. Näiteks määratleb asukohakorraldus müügitellimuse kandes koha, kus kaubad komplekteeritakse ja kuhu komplekteeritud kaubad maha pannakse. Asukohakorraldused koosnevad päisest ja seotud ridadest. Need luuakse kindlate *töökäsutüüpide* jaoks.

> [!NOTE]
> Selles teemas kirjeldatakse mooduli **Laohaldus** funktsioone. See ei kehti mooduli [Varude haldus](../inventory/inventory-home-page.md) funktsioonide korral.

Asukohakorraldusi saate kasutada järgmiste ülesannete täitmiseks.

- Sissetulevate kaupade ladustamine.
- Kaupade komplekteerimine ja etappide määramine väljaminevate kannete puhul.
- Toormaterjali komplekteerimine ja ladustamine tootmiseks.
- Asukohtade täiendamine.

## <a name="prerequisites"></a>Eeltingimused

Enne asukohakorralduse loomist peate järgima neid samme, et veenduda, et eeltingimused oleksid täidetud.

1. Veenduge, et nõutav litsentsivõti oleks sisse lülitatud. Avage **Süsteemhaldus \> Seadistus \> Litsentsi konfiguratsioon**, laiendage litsentsivõti **Kaubandus** ja seejärel valige konfiguratsioonivõti **Lao- ja transpordihaldus**. Võtke arvesse, et selle etapi jaoks on vajalik administraatori juurdepääs.
1. Avage **Laohaldus \> Seadistus \> Ladu \> Laod**.
1. Looge ladu.
1. Seadke kiirkaardil **Ladu** suvandi **Kasuta laohaldusprotsesse** väärtuseks *Jah*.
1. Looge asukohad, asukohatüübid, -profiilid ja -vormingud. Lisateavet lugege teemast [Asukohtade konfigureerimine WMS-loaga laos](./tasks/configure-locations-wms-enabled-warehouse.md).
1. Looge kohad, tsoonid ja tsoonigrupid. Lisateavet lugege teemadest [Lao seadistamine](../../commerce/channels-setup-warehouse.md) ja [Asukohtade konfigureerimine WMS-loaga laos](./tasks/configure-locations-wms-enabled-warehouse.md).

## <a name="work-order-types-for-location-directives"></a>Asukohakorralduste töökäsutüübid

Paljud asukohakorralduste jaoks määratud väljad on ühised kõigi töökäsutüüpide puhul. Kuid teised väljad on määratud kindlatele töökäsutüüpidele.

![Asukohakorralduste töökäsutüübid.](media/Location_Directives_Work_Order_Types.png "Asukohakorralduste töökäsutüübid")

> [!NOTE]
> Kahte töökäsutüüpi, *Tühistatud töö* ja *Tsükliline inventuur*, kasutab ainult süsteem. Asukohakorraldusi ei saa nende töökäsutüüpide jaoks luua.

Järgmistes jaotistes olevates tabelites on ühised ja töökäsutüübipõhised väljad, mis on saadaval asukohakorralduse seadistamisel.

### <a name="fields-that-are-common-to-all-work-order-types"></a>Kõigis töökäsutüüpides ühised väljad

Järgmises tabelis loetletakse väljad, mis on kõigi töökäsutüüpide korral ühised.

| Kiirkaart | Väli |
|---|---|
| Asukohakorraldus | Töö tüüp |
| Asukohakorraldus | Laoala |
| Asukohakorraldus | Ladu |
| Asukohakorraldus | Korralduse kood |
| Asukohakorraldus | Mitu SKU-d |
| Read | Järjekorranumber |
| Read | Alates kogusest |
| Read | Koguseni |
| Read | Ühik |
| Read | Koguse asukoha määramine |
| Read | Piira ühiku alusel |
| Read | Ümarda ühikuni |
| Read | Pakkimiskoguse leidmine |
| Read | Luba tükeldamine |
| Asukoha korralduse toimingud | Järjekorranumber |
| Asukoha korralduse toimingud | Nimi |
| Asukoha korralduse toimingud | Fikseeritud asukoha kasutamine |
| Asukoha korralduse toimingud | Luba negatiivne laovaru |
| Asukoha korralduse toimingud | Partii on lubatud |
| Asukoha korralduse toimingud | Strateegia |

### <a name="fields-that-are-specific-to-work-order-types"></a><a name="fields-specific-types"></a>Töökäsutüüpidele omased väljad

Järgmises tabelis loetletakse väljad, mis on eriomased kõigi töökäsutüüpide puhul.

| Kiirkaart | Väli | Töötellimuse tüüp |
|---|---|---|
| Asukohakorraldus | Asukoha määramise alus | Ostutellimused |
| Asukohakorraldus | Kohaldatav likvideerimiskood | Ostutellimused |
| Asukohakorraldus | Likvideerimiskood | Ostutellimused |
| Asukohakorraldus | Kohaldatav likvideerimiskood | Lõpetatud kaupade kõrvalepanek |
| Asukohakorraldus | Likvideerimiskood | Lõpetatud kaupade kõrvalepanek |
| Asukohakorraldus | Kohaldatav likvideerimiskood | Tagastustellimused |
| Asukohakorraldus | Likvideerimiskood | Tagastustellimused |
| Asukohakorraldus | Kohaldatav likvideerimiskood | Kanbani kõrvalepanek |
| Asukohakorraldus | Kohaldatav likvideerimiskood | Kanbani komplekteerimine |
| Read | Viivitamatu täiendamise mall | Müügitellimused |
| Read | Viivitamatu täiendamise mall | Toormaterjalide komplekteerimine |
| Read | Viivitamatu täiendamise mall | Edastuse väljaminek |
| Read | Viivitamatu täiendamise mall | Kanbani komplekteerimine |

## <a name="open-the-location-directives-page"></a>Lehe „Asukohakorraldused“ avamine

**Asukohakorralduste** lehe avamiseks minge **Laohaldus \> Seadistus \> Asukohakorraldused**.

Sealt saate vaadata, luua ja redigeerida oma asukohakorraldusi, kasutades toimingupaanil olevaid käske. Vaadake selle teema ülejäänud jaotisi, et saada teavet selle kohta, kuidas kasutada kõiki lehel saadaolevaid välju.

## <a name="action-pane"></a>Toimingupaan

Toimingupaan lehel **Asukohakorraldused** hõlmab nuppe, mida saate kasutada korralduste loomiseks, redigeerimiseks ja kustutamiseks (**Redigeeri**, **Uus** ja **Kustuta**). See sisaldab ka järgmisi nuppe, mis võimaldavad teil kohandada järjekorda, milles asukohakorraldus töödeldakse, ja konfigureerida päringut, mis määratleb asukohakorralduse rakendamise kriteeriumid.

- **Nihuta üles** – liigutage valitud asukohakorraldus järjestuses ülespoole. Näiteks saate liigutada selle järjestuses kohalt 4 kohale 3.
- **Nihuta alla** – liigutage valitud asukohakorraldus järjestuses allapoole. Näiteks saate liigutada selle järjestuses kohalt 4 kohale 5.
- **Redigeeri päringut** – avage dialoogiboks, kus saate määratleda tingimusi, mille alusel valitud asukohakorraldust tuleks töödelda. Näiteks võite soovida, et see rakenduks ainult kindlale laole.

## <a name="location-directives-header"></a>Asukohakorralduste päis

Asukohakorralduse päis sisaldab järgnevaid väljasid asukohakorralduse järjekorranumbri ja kirjeldava nime kohta.

- **Seerianumber** – see väli viitab järjestusele, mille alusel püüab süsteem rakendada valitud töökäsutüübi igat asukohakorraldust. Väikeseid numbreid rakendatakse esimestena. Järjestust saate muuta kasutades toimingupaanil nuppe **Nihuta üles** ja **Nihuta alla**.
- **Nimi** – sisestage asukohakorraldust kirjeldav nimi. See nimi peaks aitama tuvastada korralduse üldist eesmärki. Näiteks sisestage *Müügitellimuse komplekteerimine laos 24*.

## <a name="location-directives-fasttab"></a>Asukohakorralduste kiirkaart

Kiirkaardi **Asukohakorraldused** väljad on omased töökäsutüübile, mis on valitud loendipaanil väljal **Töökäsutüüp** .

- **Töö tüüp** – valige tehtava töö tüüp. Saadaval väärtused sõltuvad laokandetüübist, mille valisite väljal **Töökäsutüüp** . Valige üks järgmistest väärtustest.

    - **Ladustamine** – asukohakorraldus proovib leida parimat asukohta, kuhu panna või kust leida varusid, mis tulevad süsteemi vastuvõtmisel, tootmisel või varude korrigeerimisel. Selle abil saab määratleda ka vaheasukohta ladustamist või viimase laadimisukse asukohta.
    - **Komplekteerimine** – asukohakorraldus püüab leida parimaid asukohti, kust varusid füüsiliselt reserveerida (st luuakse töö). Komplekteerimist saab lõpetada (see tähendab, et komplekteerimise töörea võib sulgeda) isegi siis, kui töö pole lõpule viidud. Kasutaja saab lõpetada füüsilise komplekteerimise. Süsteemis on see tegevus komplekteerimise etapp. Seejärel saab kasutaja töö mobiilsest seadmest tühistada ja hiljem lõpule viia. Lõpliku ladustamise lõpuleviimisel suletakse tööpäis siiski esimesena.

    > [!IMPORTANT]
    > Muud väärtused väljal **Töö tüüp** ei ole asukohakorralduste puhul asjakohased. Need kuvatakse ainult seetõttu, et välja ei filtreerita nii, et see ühtiks valitud töökäsutüübiga.

- **Tegevuskoht** on kohustuslik väli, kuna asukohakorraldus vajab kehtivat tegevuskohta ja ladu.
- **Ladu** – see väli on kohustuslik, kuna asukohakorraldus vajab kehtivat tegevuskohta ja ladu.
- **Korralduse kood** – valige korralduse kood töömalli või täiendamismalliga seostamiseks. Lehel **Korralduse kood** saate luua uusi koode, mida saab kasutada töömalli või täiendamismalli ühendamiseks asukohakorraldusega. Korralduse koode saab kasutada ka seose loomiseks mis tahes töömalli rea ja asukohakorralduse vahel (nagu laadimisuks või vaheasukoht).

    > [!TIP]
    > Kui korralduse kood on määratud, siis ei otsi süsteem töö loomisel asukohakorraldusi järjekorranumbri järgi. Selle asemel otsib see korralduse koodi järgi. Sel moel saate määrata täpsemalt asukohadirektiivi, mida kasutatakse töömallis kindla etapi jaoks, nt materjalide ettevalmistamise etapi jaoks.

- **Mitu SKU-d** – seadke selle suvandi väärtuseks *Jah*, et kasutada asukohas mitut varude arvestusühikut (SKU). Näiteks peab laadimisukse asukoha puhul olema lubatud mitu SKU-d. Mitme SKU lubamisel määratakse ladustamise asukoht töös ootuspäraselt. Kuid ladustamise asukoht saab käsitleda ainult mitme kaubaga ladustamist (kui töö hõlmab erinevaid SKU-sid, mis tuleb komplekteerida ja ladustada). See ei saa hakkama ühe SKU ladustamisega. Kui seate selle suvandi väärtuseks *Ei*, määratakse ladustamise asukoht ainult juhul, kui ladustamine hõlmab vaid üht tüüpi SKU-d.

    > [!IMPORTANT]
    > Selleks, et ladustada nii mitmeid kaupu kui ka üht SKU-d, peate määrama kaks rida, millel on sama struktuur ja seadistus, kuid peate seadma ühe rea korral suvandi **Mitu SKU-d** väärtuseks *Jah* ja teise rea korral *Ei*. Ladustamistoimingute jaoks peavad teil olema identsed asukohakorraldused, isegi kui te ei pea eristama töö ID-s üht ja mitut SKU-d. Kui te ei seadista mõlemat asukohakorraldust, siis on rakendatud asukohakorralduse loodud äriprotsesside asukohad ootamatud. Peate kasutama sarnast seadistust asukohakorralduste jaoks, mille **Töö tüüp** on *Komplekteerimine* , kui teil on vaja töödelda tellimusi, mis sisaldavad mitut SKU-d.

    Kasutage suvandit **Mitu SKU-d** tööridade puhul, mis hõlmavad rohkem kui üht kaubakoodi. (Kaubakood võib jääda töö üksikasjades tühjaks ja see kuvatakse mobiilirakenduse Warehouse Management töötluslehtedel kui **Mitu**.)

    Tüüpilises näitestsenaariumis on töömall seadistatud nii, et sellel on mitu komplekteerimise/ladustamise paari. Sellisel juhul võite soovida otsida kindlat vaheasukohta, et kasutada ridu, mille **Töö tüüp** on *Ladustamine*.

    > [!NOTE]
    > Kui suvandi **Mitu SKU-d** väärtuseks on seatud *Jah*, ei saa te valida tegevuspaanil suvandit **Redigeeri päringut**, kuna päring ei saa mitme kauba korral teha hindamist kaubatasemel. Tagamaks, et soovitud asukohakorraldus on valitud, kasutage välja **Korralduse kood** , et juhtida asukohakorralduse valikut, mis on seotud selliste ladustamisridadega, kus see korralduse kood on töömallis määratud.

    Kui te ei tööta alati ühe kauba või segatud kaupadega, on oluline määratleda kaks asukohakorraldust töötüübi *Ladustamine* jaoks: üks, milles suvandi **Mitu SKU-d** väärtuseks on seatud *Jah*, ja üks, milles see on seatud väärtusele *Ei*.

- **Kohaldatav likvideerimiskood** – Määrake, kas asukohakorralduse likvideerimiskood peab ühtima kauba vastuvõtmisel rakendatava likvideerimiskoodiga või tohib asukohakorralduse valida mis tahes likvideerimiskoodi põhjal. Kui valite suvandi *Täpne vaste* ning väli **Likvideerimiskood** on tühi, kasutatakse selle asukohakorralduse jaoks ainult tühje likvideerimiskoode.

    > [!NOTE]
    > See väli on saadaval ainult valitud töökäsutüüpide puhul, kus täiendamine on lubatud. Täieliku loendi leiate selle teema varasemast jaotisest [Töökäsutüüpidele omased väljad](#fields-specific-types).

- **Leidmisalus** – täpsustage, kas ladustamise kogus peaks olema terve litsentsiplaadi kogus või peaks see olema kaup kauba põhjal. Kasutage seda välja, et tagada, et kogu litsentsiplaadi sisu ladustatakse ühte asukohta ja et süsteem ei soovitaks jagada sisu mitmesse asukohta vastuvõtmisprotsesside **ASN** (litsentsiplaadi vastuvõtmine), **Kombineeritud litsentsiplaat** ja **Kogum** korral. (Vastuvõtmisprotsessi **Kogum** korral on vaja, et funktsioon *Kogumi ladustamise funktsioon* oleks sisse lülitatud.) Asukohakorralduse päringu, ridade ja tegevuste käitumine sõltub valitud väärtusest. Kiirkaarti **Read** kasutatakse ainult siis, kui **Leidmisalus** on seatud väärtusele *Kaup*.

    > [!NOTE]
    > See väli on saadaval ainult valitud töökäsutüüpide puhul, kus täiendamine on lubatud. Täieliku loendi leiate jaotisest [Töökäsutüüpidele omased väljad](#fields-specific-types).

- **Likvideerimiskood** – seda välja kasutatakse asukohakorralduste puhul, mille töökäsutüüp on *Ostutellimus*, *Lõpetatud kaupade ladustamine* või *Tagastustellimused* ning töö tüüp *Ladustamine*. Kasutage seda, et voog kasutaks kindlat asukohakorraldust sõltuvalt likvideerimiskoodist, mille töötaja on mobiilirakenduses Warehouse Management valinud. Näiteks saate suunata tagastatud kauba tagasi kontrolliasukohta enne, kui need lattu tagastatakse. Likvideerimiskoodi saab seostada varude olekuga. Sel viisil saab seda kasutada varude oleku muutmiseks vastuvõtmisprotsessi osana. Näiteks on teil likvideerimiskood, *QA*, mis määrab varude olekuks *QA*. Seejärel saate luua eraldi asukohakorralduse, et teisaldada need varud karantiiniasukohta.

    > [!NOTE]
    > See väli on saadaval ainult valitud töökäsutüüpide puhul, kus täiendamine on lubatud. Täieliku loendi leiate jaotisest [Töökäsutüüpidele omased väljad](#fields-specific-types).

## <a name="lines-fasttab"></a>Ridade kiirkaart

Kasutage kiirkaarti **Read**, et luua tingimused seotud tegevuste rakendamiseks, mis on määratud kiirkaardil **Asukohakorralduste tegevused**. Iga rea kohta saate määrata minimaalse ja maksimaalse koguse, mille puhul peaks korraldus rakenduma. Samuti saate määrata, et neid tegevusi rakendataks konkreetse laoühiku puhul.

- **Järjekorranumber** – sisestage järjekord, mille alusel tuleks iga asukohakorralduse rida valitud töötüübis töödelda. Järjestust saate muuta vastavalt vajadusele kasutades tegevuspaanil nuppe **Nihuta üles** ja **Nihuta alla**.
- **Alates kogusest** – määrake koguste ulatuse algus, mille korral rida rakendub. Määrake kogus mõõtühikus, mis on valitud väljal **Ühik**.
- **Kuni koguseni** – määrake koguste ulatuse lõpp, mille korral rida rakendub. Määrake kogus mõõtühikus, mis on valitud väljal **Ühik**.
- **Mõõtühik** – valige kaupade jaoks mõõtühik. Saate määrata minimaalse ja maksimaalse koguse, millele korraldus vastama peab, ja saate määrata, et korraldus on kindlale laoühikule. Välja **Mõõtühik** kasutatakse *ainult* koguse hindamiseks. Et teha kindlaks, kas asukohakorralduse rida üldse rakendub, kasutab süsteem kogust mõõtühikus, mis on sellel real määratud. Iga kord kui see jõuab asukohakorralduse reale, üritab süsteem teisendada nõudluse mõõtühiku mõõtühikuks, mis on real määratud. Kui mõõtühikut ei saa teisendada, liigub süsteem edasi järgmisele reale.
- **Leia kogus** – seda välja kasutatakse ainult kaupade ladustamiseks lattu või nende asukoha määramiseks laos. (Seetõttu rakendub see ainult siis, kui välja **Töö tüüp** väärtuseks on seatud *Ladustamine*). Valige üks järgmistest väärtustest, et määrata kogus, mida kasutatakse, et hinnata, kas kogus jääb vahemikku **Alates kogusest** **Kuni koguseni**.

    - **Litsentsiplaadi kogus** – kasutage saadud litsentsiplaadi kogust.
    - **Ühikuteks jagatav kogus** – kasutage kande ajal kasutatavat kogust. Näiteks saate laos koguse 1000 ja tükeldate selle 10 litsentsiplaadiks, millest igaühe kogus on 100. Sel juhul saate kasutada kogust 1000 kaupa, mitte litsentsiplaadi kogust 100.
    - **Järelejääv kogus** – kasutage kogust, mis tuleb töödeldava ostutellimuse rea puhul veel vastu võtta.
    - **Eeldatav kogus** – kasutage ostutellimuse rea kogu kogust, sõltumata sellest, mis on juba vastu võetud.

- **Piira mõõtühiku alusel** – see märkeruut võimaldab teil asukohakorralduse rida kasutada konkreetse mõõtühiku või mitme mõõtühiku jaoks. Valige see, et piirata mõõtühikuid, mida peetakse asukohakorralduste ridade puhul sobivateks valikukriteeriumideks. See funktsioon töötab ainult asukohakorralduse puhul, kus välja **Töö tüüp** väärtuseks on seatud *Komplekteerimine*.

    Näiteks kui te reserveerite koguseid, tahate ainult kindlatest asukohtadest kaubaaluseid reserveerida. Sel juhul piiravad read seda kaubaaluste järjestust nii, et iga kaubaalusest väiksem kogus jääb asukohakorraldusest välja.

    Pange tähele, et märkeruut **Piira mõõtühiku alusel** ei reguleeri mõõtühikut või mõõtühikuid, mida on tööridadel rakendatud. Ühikupiirang rakendub ainult ühikutele, mis on saadaval ühiku seeriagrupi kaudu. Näiteks on kaup seotud ühiku seeriagrupiga, mis sisaldab nii *kaubaaluste* kui ka *tk* ühikut. Määratletud on mõõtühik, kus 1 kaubaalus = 100 tk, ning asukohakorraldus kasutab funktsiooni **Piira mõõtühiku alusel** ainult kaubaaluste puhul. Lisaks on määratletud töömall, mis seab tööpäise loomisele 50 tk suuruse piirangu. Sel juhul luuakse 50 tk suuruseid tööridasid. Piiramiseks mõõtühiku määramiseks toimige järgmiselt.

    1. Valige tööriistariba kiirkaardil **Read** suvand **Piira mõõtühiku alusel** . (See nupp muutub kättesaadavaks ainult pärast seda, kui valite real märkeruudu **Piira mõõtühiku alusel** ja seejärel **Salvesta**.)
    1. Valige lehel **Mõõtühikute alusel piiramine** väljal **Mõõtühik** see mõõtühik, mille alusel soovite komplekteerimise ja ladustamise protsesse piirata.

- **Ümarda kuni mõõtühikuni** – see väli toimib koos märkeruuduga **Piira mõõtühiku alusel**. Kui näiteks **Piira mõõtühiku alusel** ja **Ümarda mõõtühikuni** on asukohakorralduse real valitud, siis tuleb töö, mille lõi korraldus toormaterjali komplekteerimiseks, ümardada materjali käsitlemisühiku (määratletud lehel **Piira mõõtühiku alusel**) arvu 1 kordseni.

    > [!NOTE]
    > Seadistus **Ümarda mõõtühikuni** toimib ainult töökäsutüübi *Toormaterjali komplekteerimine* puhul ja ainult asukohakorralduste puhul, mille välja **Töö tüüp** väärtuseks on seatud *Komplekteerimine*.

- **Leia pakkimise kogus** – Kui määrate pakkimise koguse müügitellimusel, üleviimistellimusel või tootmistellimusel, laseb see märkeruut teil süsteemi piirata nii, et see saaks valida ainult need asukohad, millel on vähemalt see pakkimise kogus.

    > [!NOTE]
    > Seefunktsioon toimib ainult *Komplekteerimise* tüübi asukohakorraldustega.

- **Luba Tükeldamine** – Määra kas asukohakorraldusel on lubatud vastuvõetav kogus või mitmes laoasukohas reserveeritav kogus tükeldada või kas töö loomiseks tuleb kogu kogus leida ühest asukohast või reserveerida ühest asukohast.
- **Kohene täiendamismall** – Kasuta seda välja täiendamismalliga ühendamiseks, nii et täiendamine algab kohe kui kaupu ei eraldata. Kui jätate selle välja tühjaks, ei käivitu kauba täiendamine enne, kui kõik asukohakorralduse read on töödeldud.

    > [!NOTE]
    > See väli on saadaval ainult valitud töökäsutüüpide puhul, kus täiendamine on lubatud. Täieliku loendi leiate jaotisest [Töökäsutüüpidele omased väljad](#fields-specific-types).

## <a name="location-directive-actions-fasttab"></a>Asukohakorralduste tegevus KiirKaardil

Saate määratleda igale reale mitu asukoha korralduse tegevust. Järjekorranumbrit kasutatakse selleks, et määrata tegevuste järjekord. Sellel tasemel saate seadistada päringu määratlemaks, kuidas leida laos parim asukoht. Saate kasutada ka eelmääratletud **Strateegia** väärtuseid, et leida optimaalne asukoht.

- **Järjekorranumber** – sellel väljal kuvatakse järjestus, mille alusel tegevusi valitud töötüübi puhul töödeldakse. Järjestust saate muuta, kasutades tööriistaribal nuppe **Nihuta üles** ja **Nihuta alla**.
- **Nimi** – Sisestage asukohakorralduse tegevuse nimi. Olge täpsed, nii et sooritatav tegevus on nimevaba.
- **Fikseeritud asukoha kasutus** – Määrake, milliseid asukohti asukoha direktiiv peaks arvestama. Valige üks järgmistest väärtustest.

    - **Fikseeritud ja fikseerimata asukohad** – asukohakorraldus kaalub kõiki asukohti.
    - **Ainult toote fikseeritud asukohad** – asukohakorraldus kaalub ainult toodete fikseeritud asukohti.
    - **Ainult tootevariandi fikseeritud asukohad** – asukohakorraldus kaalub ainult tootevariantide fikseeritud asukohti.

- **Luba negatiivset varu** – Märkige see märkeruut, et lubada negatiivset varu asukohakorralduse määratud laoasukohas.
- **Partii on Lubatud** – Märkige see märkeruut, et kasutada partiistrateegiaid partiiloaga kaupade jaoks. On oluline, et märgite selle märkeruudu protsesside jaoks, mis kasutavad asukoha direktiive, et leida asukohti jälgitava partiinumbriga kauba komplekteerimiseks. Sel viisil kaasatakse nende asukohtade otsing, mille kabad on jälgitava partiinumbriga. Kui see märkeruut on märgitud ja välja **Strateegia** väärtuseks on seatud *Puudub*, liigub süsteem edasi järgmisele tegevusreale.
- **Strateegia** – Iga asukohakorralduse reaga seotud toimingute hõlpsamaks ja kiiremaks määratlemiseks, märgi üks järgnevatest eelnevalt määratud strateegiatest.

    - **Puudub** – ühtegi strateegiat ei kasutata.
    - **Vii pakkimiskogusega vastavusse** – see strateegia kontrollib, kas komplekteerimisasukohas on määratud pakkimiskogus olemas. See strateegia kehtib ainult siis, kui välja **Töö tüüp** väärtuseks on seatud *Komplekteerimine*.
    - **Konsolideeri** – see strateegia konsolideerib kaubad kindlas asukohas, kui sarnased kaubad on juba saadaval. See strateegia kehtib ainult siis, kui välja **Töö tüüp** väärtuseks on seatud *Ladustamine*. Tüüpilise ladustamisseadistuse puhul püüab süsteem konsolideerida esimesel tegevusereal ja üritab seejärel teisel tegevusreal ladustada ilma konsolideerimata. Kaupade konsolideerimine muudab hilisema komplekteerimise tõhusamaks.
    - **FEFO partii reserveering** – see strateegia kasutab esimesena-aegunud-esimesena-välja (FEFO) partii reserveeringuid. Kasutage seda siis, kui varud leitakse partii aegumiskuupäeva abil ja eraldatakse partii reserveerimiseks. Seda strateegiat saate kasutada ainult partiiloaga kaupade puhul. See kehtib ainult siis, kui välja **Töö tüüp** väärtuseks on seatud *Komplekteerimine*.
    - **Ümarda täieliku LP-ni ja FEFO partii** – see strateegia ühendab endas strateegiad *FEFO partii reserveering* ja *Ümarda täieliku LP-ni*. See kehtib ainult partiiloaga kaupade ning asukohakorralduste puhul, mille töötüüp on *Komplekteerimine*. Rida peab olema partiiloaga, et kasutada strateegiat *FEFO partii reserveering*, ning strateegiat *Ümarda täieliku LP-ni* saab kasutada ainult täiendamiseks. Kui see strateegia konfigureeritakse koos asukoha ladustamispiiranguga, võib see valitud ladustamistöö asukoha üle koormata ja põhjustada ladustamispiirangute eiramist.
    - **Täieliku LP-ni ümardamine** – seda strateegiat kasutatakse varude koguse ümardamiseks, et see vastaks litsentsiplaadi kogusele, mis on määratud komplekteeritavatele kaupadele. Saate seda strateegiat kasutada ainult täiendamise asukohakorralduste jaoks, mille tüüp on *Komplekteerimine*. Kui see strateegia konfigureeritakse koos asukoha ladustamispiiranguga, võib see valitud ladustamistöö asukoha üle koormata ja põhjustada ladustamispiirangute eiramist.
    - **Litsentsiplaadi põhjal juhitav** – kasutage seda strateegiat, kui väljastate tellimuse komplekteerimise ja ladustamise töö loomiseks lattu. Seda saate teha mitme litsentsiplaadi korral. See strateegia üritab reserveerida ja luua komplekteerimistööd nende asukohtade põhjal, milles asuvad üleviimistellimuse ridadega seotud nõutud litsentsiplaadid. Kui neid tegevusi ei saa lõpule viia, kuid soovite siiski komplekteerimistööd luua, peaksite valima asukohakorralduse tegevuste jaoks teise strateegia. Sõltuvalt teie äriprotsessi nõuetest võite soovida otsida ka varusid teisest lao piirkonnast.
    - **Tühi asukoht ilma sissetuleva tööta** – kasutage seda strateegiat tühjade asukohtade leidmiseks. Asukoht loetakse tühjaks, kui sel ei ole füüsilisi varusid ja eeldatavat sissetulevat tööd. Saate seda strateegiat kasutada ainult asukohakorralduste jaoks, mille töötüüp on *Paigutamine*.
    - **Asukoha aegumise FIFO** – kasutage esimesena-sisse-esimesena-välja-strateegiat (FIFO), et lähetada nii partiijälgimisega kui ka partiijälgimiseta kaupu kuupäeva alusel, mil varud lattu jõudsid. See võimalus võib olla eriti kasulik partiijälgimiseta varude puhul, mille korral ei saa sortimiseks kasutada aegumiskuupäeva. FIFO-strateegia leiab üles asukoha, mis sisaldab vanimat aegumiskuupäeva ja planeerib komplekteerimise selle aegumiskuupäev põhjal.
    - **Asukoha aegumise LIFO** – kasutage viimasena-sisse-viimasena-välja-strateegiat (LIFO), et lähetada nii partiijälgimisega kui ka partiijälgimiseta kaupu kuupäeva alusel, mil varud lattu jõudsid. See võimalus võib olla eriti kasulik partiijälgimiseta varude puhul, mille korral ei saa sortimiseks kasutada aegumiskuupäeva. LIFO-strateegia leiab üles asukoha, mis sisaldab uusimat aegumiskuupäeva ja planeerib komplekteerimise selle aegumiskuupäev põhjal.

## <a name="example-using-location-directives"></a>Näide: asukohakorralduste kasutamine

Selle näite puhul kaaluge ostutellimuse protsessi, kus asukohakorraldus peab leidma laos äsja vastuvõtudokis registreeritud laokaupade jaoks vaba ruumi. Esiteks peate leidma vaba ruumi laos, konsolideerides olemasoleva vaba kaubavaruga. Kui konsolideerimine ei ole võimalik, peate leidma tühja asukoha.

Selle stsenaariumi puhul peate määratlema kaks asukohakorralduse toimingut. Esimene tegevus järjekorras peab kasutama strateegiat *Konsolideeri* ja teine strateegiat *Tühi asukoht sissetuleva tööta*. Kui te ei määratle kolmandat toimingut ületäitmisstsenaariumi käsitlemiseks, on võimalikud kaks tulemust, kui laos ei ole enam ruumi: töö saab luua isegi siis, kui asukohti ei määratleta, või töö loomise protsess võib nurjuda. Tulemuse määrab lehe **Asukohakorralduse tõrked** seadistus, kus saate otsustada, kas valida suvand **Peata töö asukohakorralduse tõrke korral** iga töökäsutüübi korral.

## <a name="next-step"></a>Järgmine samm

Pärast asukohakorralduste loomist saate töö loomiseks seostada iga korraldusekoodi töömalli koodiga. Lisateavet vaadake teemast [Laotöö juhtimine töömallide ja asukohadirektiividega](./control-warehouse-location-directives.md).

## <a name="additional-resources"></a>Lisaressursid

- Video: [laohalduse konfiguratsiooni üksikasjalik juhis](https://community.dynamics.com/365/b/techtalks/posts/warehouse-management-configuration-deep-dive-october-14-2020)
- Spikriteema: [laotöö juhtimine töömallide ja asukohakorraldustega](control-warehouse-location-directives.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]