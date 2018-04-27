---
title: "Jaemüügi hinna haldamine"
description: "Selles teemas kirjeldatakse müügihindade loomise ja haldamise põhimõtteid lahenduses Microsoft Dynamics 365 for Retail."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 03/27/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: ShalabhjainMSFT
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a7e6babe1bfec60ece4f84a77bbd838faf7274e0
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="retail-sales-price-management"></a>Jaemüügi hinna haldamine

[!INCLUDE [banner](includes/banner.md)]

Selles teemas antakse teavet müügihindade loomise ja haldamise protsessi kohta lahenduses Microsoft Dynamics 365 for Retail. See keskendub protsessi põhimõtetele ja müügihindade mitmesuguste konfiguratsioonivalikute mõjudele.

## <a name="terminology"></a>Terminoloogia
Selles teemas on kasutatud järgmisi mõisteid.

| Mõiste | Definitsioon, kasutamine ja märkused |
|---|---|
| Hind | Ühe ühiku summa, mille eest toode müüb kassa (POS) kliendis või müügitellimuses. Selles teemas viitab mõiste *hind* alati müügihinnale, mitte laohinnale või omahinnale. |
| Baashind | Hind, mis on määratud väljastatud toote väljas **Hind**. |
| Kaubanduslepingu hind | Hind, mis määratakse tootele või variandile, kasutades tüübi **Hind (müük)** kaubanduslepingut. |
| Parim hind | Kui tootele saab rakendada rohkem kui ühe hinna või allahindluse, liidetakse väikseim hind ja/või suurim allahindluse hind, mis loob madalaima võimaliku netosumma, mille klient peab tasuma. Selles teemas viidatakse parima hinna mõistele alati sõnadega „parim hind”. See parim hind erineb allahindluse konkurentsirežiimi **parima hinna** loetelu väärtusest ja neid ei tohi omavahel segamini ajada. |

## <a name="price-groups"></a>Hinnagrupid
Hinnagrupid on Retailis hinna ja allahindluste haldamise keskmes. Hinnagruppe kasutatakse hindade ja allahindluste määramiseks jaemüügiüksustele (nt kanalitele, kataloogidele, ühendustele ja püsikliendiprogrammidele). Kuna hinnagruppe kasutatakse igasuguse hinnakujunduse ja allahindluste jaoks, on väga oluline, et plaaniksite, kuidas neid enne alustamist kasutate.

Eraldi on hinnagrupp lihtsalt nimi, kirjeldus ja valikuliselt hinnakujunduse prioriteet. Hinnagruppide juures on peamine meeles pidada, et neid kasutatakse mitu-mitmele-seoste haldamiseks, mis on allahindlustel ja hindadel jaemüügiüksustes.

Alloleval joonisel on näidatud, kuidas hinnagruppe kasutatakse. Pange tähele, et sellel joonisel on hinnagrupp täpselt hinnakujunduse ja allahindluse haldamise keskel. Jaemüügiüksused, mida kasutate eristavate hindade ja allahindluste haldamiseks, on vasakul, ning tegelik hind ja allahindluse kirjed on paremal.

![Hinnagrupid](./media/PriceGroups.png "Hinnagrupid")

Hinnagruppe luues ei tohiks kasutada üht hinnagrupi mitut tüüpi jaemüügiüksuste jaoks. Muidu võib olla keeruline määrata, miks konkreetset hinda või allahindlust kandele rakendatakse.

Nagu punane katkendjoon joonisel näitab, toetab Retail Microsoft Dynamics 365 otse kliendile määratud hinnagrupi põhifunktsiooni. Kuid sellisel juhul saate ainult müügihinna kaubanduslepingud. Kui soovite rakendada kliendipõhiseid hindu, soovitame otse kliendile hinnagruppe mitte määrata. Selle asemel kasutage alluvusi.

Järgmistes jaotistes on rohkem teavet jaemüügiüksuste kohta, mida saate hinnagruppide kasutamisel kasutada eraldi hindade määramiseks. Kõikide nende üksuste hindade ja allahindluste konfiguratsioon on kahesammuline protsess. Neid samme võib läbida mis tahes järjekorras. Kuid loogiline järjekord on kõigepealt määrata üksustele hinnagrupid, kuna see samm on tõenäoliselt ühekordne seadistamissamm, mida tehakse juurutamise ajal. Kui hinnad ja allahindlused on loodud, saate neile eraldi määrata hinnagrupid.

### <a name="channels"></a>Kanalid
Jaemüügitööstuses on väga tavaline, et eri kanalites on eri hinnad. Kaks peamist tegurit, mis kanalipõhiseid hindu mõjutavad, on hinnad ja kohalikud turutingimused.

- **Kulud** – mida kaugemal on kanal toote lähtekohast, seda kallim on toote laos hoidmine. Näiteks värskel tootel on piiratud kõlblikkusaeg ja konkreetne tootmisplaan (nt kasvuaeg). Talvel maksab värske lehtsalat tõenäoliselt rohkem põhjapoolsetes kui lõunapoolsetes kohtades. Kui määrata hindu kanalitele suurel geograafilisel alal, tahate ilmselt määrata eri kanalitele erinevad hinnad.
- **Kohalikud turutingimused** – kauplus, millest üle tee on otsene konkurent, on palju hinnatundlikum kui kauplus, mille läheduses otseseid konkurente pole.
 
### <a name="affiliations"></a>Alluvused
Alluvuse üldine definitsioon on seos grupiga. Retailis on alluvused kliendigrupid. Alluvused on palju paindlikum vahend kliendi hinnakujunduseks ja allahindluste määramiseks kui Microsoft Dynamics 365 kliendigruppide ja allahindlusgruppide põhimõiste. Esiteks saab alluvust kasutada nii hindade kui ka allahindluste jaoks, samas kui jaemüügiga mitteseotud hinnakujundusel on eraldi grupp iga allahindluse ja hinna tüübi jaoks. Teiseks võib klient kuuluda mitmesse alluvusse, aga vaid ühte iga tüübi jaemüügiga mitteseotud hinnakujundusgruppi. Viimasena, kuigi alluvusi saab seadistada nii, et need on kliendiga seotud, ei pea seda tegema. Konkreetseks otstarbeks mõeldud alluvust saab POS-is kasutada anonüümsete klientide jaoks. Anonüümse alluvuse allahindluse tüüpiline näide on allahindlus pensionäridele või õpilastele, mille korral klient saab allahindluse vaid grupi liikmekaarti näidates.

Kuigi alluvused on kõige sagedamini seotud allahindlustega, saab neid kasutada ka eristava hinnakujunduse määramiseks. Näiteks kui jaemüüja müüb töötajale, võib ta soovida müügihinda muuta, selle asemel et rakendada tavahinnale allahindlust. Näiteks võib ka jaemüüja, kes müüb nii tavaklientidele kui ka äriklientidele, pakkuda äriklientidele paremaid hindu, lähtudes ostu mahust. Alluvuste korral on võimalikud mõlemad variandid.

### <a name="loyalty-programs"></a>Püsikliendiprogrammid
Hindade ja allahindluste korral on püsikliendiprogrammid lihtsalt konkreetse nimega alluvus. Püsikliendiprogrammidele, nagu ka alluvusele, saab määrata nii hindu kui ka allahindlusi. Kuid see, kuidas klientidele määratakse püsikliendi hinnakujundus kande või tellimuse ajal, erineb sellest, kuidas tehakse alluvuse hinnakujundust. Kliendid saavad püsikliendihindu vaid siis, kui kandele lisatakse püsikliendikaart. Kui kandele lisatakse püsikliendikaart, lisatakse ka püsikliendiprogramm. Seejärel pakub püsikliendiprogramm erihindu ja allahindlusi.

Püsikliendiprogrammidel on mitu kihti ja allahindlused võivad eri kihtidel olla erinevad. Nii saavad jaemüüjad anda sagedastele klientidele suuremaid preemiaid, ilma et peaksid neid kliente käsitsi spetsiaalsesse gruppi panema.

Püsikliendiprogrammidel on peale hindade ja allahindluste lisafunktsioonid. Kuid hindade ja allahindluste osas on need sama kui alluvused.

### <a name="catalogs"></a>Kataloogid
Mõni jaemüüja kasutab füüsilisi või virtuaalseid katalooge toodete turustamiseks ja nende hinna kujundamiseks klientide koondgruppide jaoks. Osana ärimudelist turustada kataloogi kaudu saavad need jaemüüjad määrata kataloogides eristavaid hindu. Microsoft Dynamics 365 toetab seda võimalust, lastes teil määrata kataloogipõhiseid allahindlusi ja hindu, nagu saate määrata ka kanalipõhiseid või alluvusepõhiseid allahindlusi. Kataloogi redigeerides saate hinnagruppe seostada kataloogiga, nagu ka kanali, alluvuse või püsikliendiprogrammiga.

### <a name="best-practices-for-price-groups"></a>Hinnagruppide head tavad
Ärge kasutage hinnagruppi mitme jaemüügiüksuse tüübi jaoks. Selle asemel kasutage üht hinnagruppide kogumit kanalite, teist hinnagruppide kogumit alluvuste või püsikliendiprogrammide jaoks jne. Võite hinnagrupi nimes kasutada ees- või järelliidet, et visuaalselt rühmitada eri hinnagruppide tüüpe, mida kasutate.

Vältige hinnagruppide määramist otse kliendile. Selle asemel kasutage alluvust. Sedasi saate määrata kõik hindade ja allahindluste tüübid klientidele, mitte ainult müügihinna kaubanduslepingutele.

## <a name="pricing-priority"></a>Hinnakujunduse prioriteet
Eraldi on hinnakujunduse prioriteet lihtsalt number ja kirjeldus. Hinnakujunduse prioriteete saab rakendada hinnagruppidele või otse allahindlustele. Kui hinnakujunduse prioriteete kasutatakse, lasevad need jaemüüjal tühistada hea tava põhimõtet, juhtides järjekorda, milles hindu ja allahindlusi toodetele rakendatakse. Kõrgemat hinnakujunduse prioriteedi numbrit hinnatakse enne madalamat hinnakujunduse prioriteedi numbrit. Kui mis tahes prioriteedi numbris leidub hind või allahindlus, eiratakse kõiki hindu ja allahindlusi, mille prioriteedi number on madalam.

Hind ja allahindlus võivad pärineda erinevatest hinnakujunduse prioriteetidest, kuna hinnakujunduse prioriteedid rakenduvad hindadele ja allahindlustele sõltumatult.

Hindade hinnakujunduse prioriteedi kasutamiseks peate määrama hinnagrupile hinnakujunduse prioriteedi ja seejärel looma sellele hinnagrupile müügihinna kaubanduslepingu.

Hinnakujunduse prioriteedi funktsioon võeti kasutusele, et toetada stsenaariumi, kus jaemüüja soovib konkreetsele kaupluste kogumile rakendada kõrgemaid hindu. Näiteks on jaemüüja määranud piirkondlikud hinnad Ameerika Ühendriikide idarannikule, aga soovib kõrgemaid hindu mõnele tootele New York City kauplustes, kuna linnas maksab mõne toote müümine rohkem ja/või kohalikul turul kehtib kõrgem hind.

Nagu kirjeldasime selle teema jaotises „Parim hind”, valib jaemüügi hinnakujunduse mootor tavaliselt kahest hinnast madalama. Seetõttu ei saa jaemüüja enamasti kasutada kahest kõrgemat hinda kaupluses, millel on nii idaranniku kui ka New Yorgi hinnagrupid. Selle probleemi lahendamiseks enne hinnakujunduse prioriteedi funktsiooni kasutusele võtmist pidi jaemüüja määrama hinnad iga tootele kaks korda ja mitte määrama mõlemat hinnagruppi. Teine võimalus oli luua täiendavad hinnagrupid, et eraldada kõrgema hinnaga tooteid tavalise, madalama hinnaga toodetest.

Kuid hinnakujunduse prioriteedi funktsioon laseb jaemüüjal luua kaupluse hindade hinnakujunduse prioriteedi, mis on kõrgem kui piirkondlike hindade hinnakujunduse prioriteet. Teine võimalus on luua hinnakujunduse prioriteet ainult kaupluse hindadele ja jätta piirkondlikud hinnad vaikimisi hinnakujunduse prioriteedi väärtusele, mis on 0 (null). Mõlemad seadistused aitavad tagada selle, et kaupluse hindu kasutatakse alati enne piirkondlikke hindu.

### <a name="pricing-priority-example"></a>Hinnakujunduse prioriteedi näide
Vaatame näidet, kus kaupluse hinnad tühistavad muud hinnad.

Riiklik jaemüüja määrab enamiku hindu piirkonna järgi ja tal on neli piirkonda: kirre, kagu, kesk-lääs ja lääs. Jaemüüja on tuvastanud mitu suure kuluga turgu, mis võivad toetada kõrgemaid hindu. Need turud on New York Citys, Chicagos ja San Francisco Bay piirkonnas.

Selles näites vaatame lähemalt kirde piirkonda. Kauplus 1 asub Bostonis ja kauplus 2 Manhattanil. Boston kaupluse jaoks on kanaliga seostatud kaks hinnagruppi: kirre ja kauplus 1. Manhattani kaupluse jaoks on kanaliga seostatud kolm hinnagruppi: kirre, NYC ja kauplus 2.

Jaemüüja seadistab kaks hinnakujunduse prioriteeti: suurel kulul on prioriteedi number 5 ja kaupluse hindadel on prioriteedi number 10. (Pidage meeles, et vaikimisi on hinnakujunduse prioriteet 0 \[null\] ja hinda või allahindlust, millel on kõrgem prioriteedi number, kasutatakse enne hinda või allahindlust, millel on madalam prioriteedi number.) Kirde hinnagrupi hinnakujunduse prioriteet jäetakse vaikeväärtusele **0** (null). NYC hinnagrupi jaoks määratakse hinnakujunduse prioriteet väärtusele **5**, kuna New York City on suure kuluga turg. Kaupluse 1 ja kaupluse 2 hinnagruppide hinnakujunduse prioriteediks määratakse **10**.

Kaks toodet, mida jaemüüja müüb, on toode 1, kaubamärgita T-särk, ja toode 2, konkreetse tootemargi teksapüksid.

| Toode | Kirde hind | NYC hind | Kaupluse hind |
|---|---|---|---|
| T-särk | 15 dollarit | Pole seatud | Pole seatud |
| Teksapüksid | 50 dollarit | 70 dollarit | Pole seatud |

T-särki müüakse sama hinnaga (15 dollarit) nii Bostoni kui ka Manhattani kauplustes, kuna kirde hinnagrupis on määratud ainult üks hind, mis on seostatud mõlema kanaliga. Teksapükse müüakse 50 dollari eest Bostoni kaupluses, kuna see on ainus hind, mis on selle kaupluses saadaval. Kuid Manhattani kaupluses on saadaval kaks hinda: 50 ja 70 dollarit. Kuna hinnakujunduse prioriteet 5 NYC hinnagrupile on kõrgem kui hinnakujunduse prioriteet 0 (null) kirde hinnagrupile, määratakse POS-i süsteemis hinnaks 70 dollarit.

> [!NOTE]
> Iga hinnakujunduse prioriteedi jaoks on vaja täielikult läbida jaemüügi hinnakujunduse mootori loogika. Seetõttu peaksite kasutama hinnakujunduse prioriteete mõõdukalt, et aidata säilitada hinna ja allahindluse arvutuse jõudlust.

## <a name="types-of-prices"></a>Hinnatüübid
Microsoft Dynamics 365-s saate määrate toote hinna kolmes kohas:

- otse tootele (baashind)
- müügihinna kaubanduslepingus
- hinna korrigeerimises

Baashind ja kaubanduslepingu hind on osa Microsoft Dynamics 365 põhisisust ning need on saadaval ka siis, kui te Retaili ei kasuta. Hinna korrigeerimise funktsioon on saadaval ainult Retailis. Järgmises jaotises on rohkem teavet hindade määramise võimaluste kohta ja selles selgitatakse, kuidas need võimalused koos toimivad.

## <a name="setting-prices"></a>Hindade määramine
### <a name="base-price"></a>Baashind
Lihtsaim koht tootele hinna määramiseks on otse tootel. Otse tootel määratud väärtuse kohta öeldakse sageli toote baashind. Baashinna saate määrata väljas **Hind** vahekaardil **Müük** lehel **Väljastatud toote üksikasjad**. Sisestatud väärtus on esitatud ettevõtte valuutas. Vaikimisi on hind esitatud kogusega 1 mõõtühiku kohta (UoM), mis on määratud väljas **Ühik** vahelehel **Müük**. Tegelik hind toote ühiku kohta põhineb UoM-il, hinna kogusel ja valuutal.

Kui tootel on kõigi jaoks üks hind, pakub baashind kõige tõhusamat viisi selle toote hinna haldamiseks. Isegi kui kasutate hindade määramiseks kaubanduslepinguid, võite tootele määrata ka baashinna. Kui te siis ei kasuta kaubanduslepingut **Kõik**, on teil olemas varuhind, mida kasutatakse, kui kaubanduslepingut ei rakendu.

Kui jaemüügikanali valuuta erineb ettevõtte valuutast, määratakse selle jaemüügikanali baashind, kasutades tootele määratud hinnal valuutateisendust.

Kuigi hinnaühik ei ole jaemüügis tavaline, toetab jaemüügi hinnakujunduse mootor seda. Kui hinnaühik on määratud muule väärtusele kui **0** (null), on hind ühiku kohta võrdne võrrandiga hind ÷ hinnaühik. Näiteks kui kauba hind on 10 dollarit ja hinnaühik on 50, on koguse 1 hind 0,20 dollarit (= 10 ÷ 50).

### <a name="sales-price-trade-agreement"></a>Müügihinna kaubandusleping
Kaubanduslepingu töölehte kasutades saate luua igale tootele müügihinna kaubanduslepinguid. Rakenduses Microsoft Dynamics 365 on kolm müügihinna kaubanduslepingutele kolm kliendiulatust: **Tabel**, **Grupp** ja **Kõik**. Kliendiulatus määrab kliendid, kellele konkreetne müügihinna kaubandusleping kehtib.

Müügihinna kaubandusleping **Tabel** on ühele kliendile, kes on määratud otse kaubanduslepingus. See stsenaarium ei ole tavaline jaemüügi ettevõtte ja tarbija vaheline (B2C) stsenaarium. Kuid kui see tekib, kasutab jaemüügi hinnakujunduse mootor kaubanduslepinguid **Tabel**, kui see määrab hinna. 

Müügihinna kaubandusleping **Grupp** on tüüp, mida kasutatakse jaemüügi funktsiooniga kõige sagedamini. Väljaspool Retaili on müügihinna kaubanduslepingud **Grupp** mõeldud lihtsatele kliendigruppidele. Kuid Retailis on kliendigrupi mõistet laiendatud, nii et see on üldisem jaemüügi hinnagrupp. Hinnagrupp võib olla seotud jaemüügikanali, alluvuse, püsikliendiprogrammi või kataloogiga. Üksikasjalikku teavet hinnagruppide kohta leiate selle teema jaotisest „Hinnagrupid”.

> [!NOTE]
> Kaubanduslepingu hinda kasutatakse alati enne baashinda.

### <a name="price-adjustment"></a>Hinna korrigeerimine
Nagu nimigi ütleb, kasutatakse hinna korrigeerimist selleks, et muuta hinda, mis oli määratud otse tootele või kaubanduslepingu kaudu. Hinna korrigeerimist saab kasutada ainult hinna langetamiseks, mitte selle tõstmiseks. Hinna korrigeerimine on soovitatav jaemüüjatele toodete hinnavähenduste loomiseks, jälgimiseks ja haldamiseks aja jooksul. 

Hinna korrigeerimisi on kolme tüüpi: protsendi mahaarvutamine, summa mahaarvutamine ja hind. Hinna korrigeerimist protsendi või summa mahaarvutamisega rakendatakse alati müügitehingule. Kuid hinna järgi hinna korrigeerimist kasutatakse ainult siis, kui korrigeeritud hind on väiksem kui hind, mis määrati baashinda või kaubanduslepingu hinda kasutades. Seega, kui hinna korrigeerimises määratud hind on kõrgem kui korrigeerimata hind, siis hinna korrigeerimist ei kasutata.

## <a name="determining-price-for-a-product-in-a-transaction"></a>Hinna määramine tehingus olevale tootele

Tehingu hinna ja allahindluse arvutamisel kasutatakse kliendi jaoks parima hinna leidmise põhimõtet. Kui leitakse rohkem üks hind, kasutatakse selle põhimõtte järgi madalaimat hinda. Peale selle kasutatakse allahindluste kombinatsiooni, mis annab suurima allahindluse summa kogu tehingule. Mõnel juhul tuleb ühel tootel kasutada väiksemat allahindlust, et teistele tehingus olevatele toodetele saaks rakendada lisaallahindlusi.

Ainus erand kliendi jaoks parima hinna leidmise põhimõttele on soodsaimate allahindluste sobitamise võimalus. See suvand laseb kasutada kõige soodsamaid allahindlusi, mis toodete valimisel ja rühmitamisel on jaemüüjale kasuks. Seega, kui tehing sisaldab rohkem tooteid, kui on vaja soodsaima allahindluse kasutamiseks, valib jaemüügi hinnakujunduse mootor tooted, mis annavad kliendi jaoks väikseima võimaliku allahindluse summa.

Jaemüügi hinnakujunduse mootor annab iga toote kohta kolm hinda: baashind, kaubanduslepingu hind ja aktiivne hind.

Baashind on lihtsalt toote atribuut ja see on kõikjal kõigi jaoks sama. 

Kui müügihinna kaubanduslepingul on suvandi **Otsi järgmine** väärtuseks **Jah**, kasutatakse kaubanduslepingu hinnana madalaimat hinda, mis vastavate müügihinna kaubanduslepingute kohta leitakse. Kaubanduslepinguid leiab, kasutades hinnagruppe või kontokoodi **KÕIK**. Teine võimalus on määrata kaubanduslepinguid otse kliendile. Kui suvandi **Otsi järgmine** väärtus on **Ei**, kasutatakse esimest leitud kaubanduslepingu hinda. Kui ühtegi müügihinna kaubanduslepingut ei leita, määratakse kaubanduslepingu hind võrdseks baashinnaga.

Aktiivne hind arvutatakse, võttes kaubanduslepingu hind ja rakendades suurimat hinna korrigeerimist, mis tootele kehtib. Kui ühtegi hinna korrigeerimist ei leita või arvutatud aktiivne hind on kõrgem kui kaubanduslepingu hind, määratakse aktiivne hind võrdseks kaubanduslepingu hinnaga. Pidage meeles, et toote hind ei saa tõsta, kasutades hinna korrigeerimist. Kehtiva hinna korrigeerimise leiate, kasutades kanalile, kataloogile, alluvusele või püsikliendiprogrammile määratud hinnagruppe.

## <a name="category-price-rules"></a>Kategooria hinnareeglid
Kategooria hinnareeglite funktsioon Retailis on lihtne moodus uute kaubanduslepingute loomiseks kõikidele kategoorias olevatele toodetele. Selle funktsiooniga saate automaatselt leida kategoorias olevate toodete jaoks olemasolevaid kaubanduslepinguid ja neid kehtetuks muuta.

Kui valite olemasoleva kaubanduslepingu kehtetuks muutmise valiku, loob süsteem uue kaubanduslepingu töölehe kategoorias olevatele toodetele, millel on aktiivne kaubandusleping. Kuid tööleht tuleb käsitsi sisestada. Peale selle võivad kategooria hinnareeglid leida olemasolevaid kaubanduslepinguid vaid siis, kui kasutate sama hinnareeglit (ehk loote uue hinnareegli, mis kasutab kategooriat, mis oli enne). Kui te ei kasuta sama hinnareeglit, siis olemasolevaid kaubanduslepinguid kehtetuks ei muudeta.

Hindu saab suurendada või vähendada, kasutades kategooria hinnareeglite välju **Hinnareegel** ja **Hinna alus**.

- Valige väljal **Hinnareegel**, millist hinnamuutuse tüüpi kasutada.

    - **Hinnalisand** – müügihinna arvutamiseks kasutatav baashinna protsent. Näiteks on tootel, mis maksab 10,00 eurot ja mis müüakse hinnaga 15,00 eurot, hinnalisand 50 protsenti.
    - **Marginaal** – kasumisumma arvutamiseks kasutatav müügihinna protsent. Näiteks on tootel, mis maksab 10,00 eurot ja mis müüakse hinnaga 15,00 eurot, hinnalisand 33,3 protsenti.
    - **Fikseeritud summa** – müügihinna arvutamiseks kasutatav baashinnale lisatav summa. Näiteks on tootel, mis maksab 10,00 eurot ja mis müüakse hinnaga 15,00 eurot, fikseeritud summa 5,00 protsenti.

- Valige väljal **Baashind** muudetava hinna tüüp.

    - **Põhikulu** – summa, mille jaemüüja maksis tarnijale.
    - **Baashind** – müügihind enne kaubanduslepete ja hinna korrigeerimise rakendamist.
    - **Praegune hind** – müügihind pärast kaubanduslepete ja hinna korrigeerimise rakendamist.

Eri tootekategooriatest pärit eri toodete hindade lihtsaks värskendamiseks võite kasutada täiendavaid tootekategooriaid koos kategooria hinnareeglitega.

## <a name="best-practices"></a>Head tavad
Microsoft SQL Server Expressi kasutatakse kanali andmebaasides sageli hinna tõttu (tasuta). Pidage meeles, et SQL Server Expressi riistvara ja andmemaht on piiratud. Kui te õigesti ei plaani, võib SQL Server Expressi andmemaht kiiresti täis saada. See kehtib lisaks hinnakujundusele ka teistele toote valdkondadele. Siin on paar head tava, mis aitavad andmemahtu vähendada.

- Kui kasutate kaubanduslepinguid ja hinnad muutuvad, peaksite vana kaubanduslepingu kehtetuks muutma, määrates sellele lõppkuupäeva. Aja jooksul aitab see lähenemine vähendada kaubanduslepingute arvu, mida kanali andmebaasides hoitakse. See aitab ka vähendada andmete mahtu, millega hinnaarvutuse algoritm peab tegelema.
- Kui hinnad tootevariantidel erinevad, kaaluge toote baashinna kasutamist kõige tavalisema variandi hinnana. Seejärel kasutage kaubanduslepinguid ainult nendel variandi hindadel, mis on erandlikud. See lähenemine aitab vähendada kaubanduslepingute kirjete arvu. Kuna andmete importimine Microsoft Dynamics 365 on nii lihtne, võib teil tekkida kiusatus importida kaubandusleping iga toote variandi kohta. Kuid see võib tekitada palju kaubanduslepinguid, millel on sama väärtus. Seega võib see mõttetult andmemahtu suurendada.
- Jaemüügiprotsesside variandipõhised hinnad kõige konkreetsematest kõige vähem konkreetsemateni. Kui tootedimensioon ei mõjuta hinda, ei pea te sellele kaubanduslepinguid määrama. Näiteks toode on saadaval kolmes värvis ja neljas suuruses, aga hind erineb vaid suuruse põhjal. Kui määrate igale variandile kaubanduslepingu, loote 12 kirjet. Selle asemel saate määrata kaubanduslepingu ainult igale suurusele ja jätta värvi dimensiooni tühjaks. Sel juhul loote ainult neli kirjet.

    Kui iga dimensiooni väärtus ei loo eri hinda, saate tooteetalonile määrata ühe kaubanduslepingu ja jätta kõik tootedimensioonid tühjaks. Seejärel määrake eraldi kaubandusleping ainult iga dimensiooni väärtusele, mis loob erineva hinna. Näiteks kui XXL-suuruse hind on kõrgem, aga kõikide teiste suuruste hind on sama, on vaja vaid kaht kaubanduslepingut: üks tooteetalonile ja üks XXL-suurusele.

## <a name="prices-that-include-tax-vs-prices-that-exclude-tax"></a>Maksu sisaldavad ja maksu mitte sisaldavad hinnad
Kui määrate Microsoft Dynamics 365-s müügihinnad, siis te ei määra, kas määratav hinnaväärtus sisaldab maksu või mitte. Väärtus väljal lihtsalt hind. Kuid jaemüügikanalite säte **Hind sisaldab käibemaksu** laseb konfigureerida jaemüügikanaleid nii, et need kas lisavad hinnale maksu või mitte. See säte on määratud kanalis ja seda saab muuta isegi ühes ettevõttes.

Kui töötate nii hõlmavate kui ka välistavate maksutüüpidega, on väga oluline määrata hinnad õigesti, kuna kogusumma, mille klient maksab, muutub, kui kanali sätet **Hind sisaldab käibemaksu** muudetakse.

### <a name="effect-of-the-price-includes-sales-tax-setting-on-financial-postings"></a>Sätte Hind sisaldab käibemaksu mõju finantsilistele sisestustele
Kõiki tulu ja allahindluse kontode kohta pearaamatusse sisestatavad summasid mõjutab säte **Hind sisaldab käibemaksu**. Järgmises näites on näha, kuidas mõjutab see säte finantsilisi sisestusi.

Näites räägitakse vaid müügi postitustest, kuna säte **Hind sisaldab käibemaksu** ei mõjuta kaubavaru kulu sisestusi.

#### <a name="example"></a>Näide
Selles näiteks konfigureeritakse allahindluse summad nii, et need sisestatakse tulust eraldi.

Müüte 100-dollarilist toodet, mille maksumäär on 10 protsenti, ja rakendate allahindlust 5 protsenti. Kasutati järgmisi USRT demoandmete kontosid.

- **Tulu:** 401100
- **Allahindlus:** 403200
- **Maks:** 202100

**1. juhtum: ei sisalda maksu (ehk käibemaks)**

- **Tulu:** 100 dollarit
- **Allahindlus:** 5 dollarit
- **Maks:** 9,5 dollarit (= 10 protsenti 95 dollarist)

**2. juhtum: sisaldab maksu (käibemaks \[KM\])**

- **Tulu:** 90 dollarit
- **Allahindlus:** 4,5 dollarit (= 5 protsenti 90 dollarist)
- **Maks:** 10 dollarit

## <a name="differences-between-retail-pricing-and-non-retail-pricing"></a>Erinevused jaemüügi hinnakujunduse ja jaemüügiga mitteseotud hinnakujunduse vahel
Jaemüügihindade arvutamiseks kõikides kanalites (kõnekeskus, kauplus ja e-poed) kasutatakse üht hinnakujunduse mootorit. See aitab lubada ühtlustatud kaubanduse stsenaariume. 

Jaemüügi hinnakujundus on loodud toimima jaemüügiüksustega, mitte jaemüügiga mitteseotud üksustega. Eeskätt on see loodud määrama hindu kaupluse, mitte lao järgi.

Jaemüügi hinnakujunduse mootor ei toeta järgmisi hinnakujunduse funktsioone.

- Hinna määramine tegevuskoha ja laoala dimensioone kasutades
- Atribuudipõhine hinnakujundus
- Hankija allahindluse läbimine

Peale selle toetab järgmisi hinnakujunduse funktsioone **ainult** jaemüügi hinnakujunduse mootor.

- Hind põhineb tootedimensioonil kõige konkreetsemast variandi hinnast kõige vähem konkreetse variandi hinnani tooteetaloni hinnani. Hinda, mis on määratud kaht tootedimensiooni kasutades (nt värv ja suurus), kasutatakse enne hinda, mis on määratud ainult üht tootedimensiooni kasutades (nt suurus).
- Hinnakujunduse ja allahindluste juhtimiseks saab kasutada sama hinnagruppi.

