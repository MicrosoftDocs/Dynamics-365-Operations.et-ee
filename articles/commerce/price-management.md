---
title: Jaemüügi hinna haldamine
description: Selles teemas kirjeldatakse müügihindade loomise ja haldamise põhimõtteid rakenduses Dynamics 365 Commerce.
author: ShalabhjainMSFT
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2811e61045c0a830d1c814d760820a364893efcc
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352224"
---
# <a name="retail-sales-price-management"></a>Retaili müügihinna haldamine

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse müügihindade loomise ja rakendamise protsessi rakenduses Dynamics 365 Commerce. See keskendub protsessi põhimõtetele ja müügihindade mitmesuguste konfiguratsioonivalikute mõjudele.

## <a name="terminology"></a>Terminoloogia

Selles teemas on kasutatud järgmisi mõisteid.

| Mõiste | Definitsioon, kasutamine ja märkused |
|---|---|
| Hind | Ühe ühiku summa, mille eest toode müüb kassa (POS) kliendis või müügitellimuses. Selles teemas viitab mõiste *hind* alati müügihinnale, mitte laohinnale või omahinnale. |
| Baashind | Hind, mis on määratud väljastatud toote väljas **Hind**. |
| Kaubanduslepingu hind | Hind, mis määratakse tootele või variandile, kasutades tüübi **Hind (müük)** kaubanduslepingut. |
| Parim hind | Kui tootele saab rakendada rohkem kui ühe hinna või allahindluse, liidetakse väikseim hind ja/või suurim allahindluse hind, mis loob madalaima võimaliku netosumma, mille klient peab tasuma. Selles teemas viidatakse parima hinna mõistele alati sõnadega „parim hind”. See parim hind erineb allahindluse konkurentsirežiimi **parima hinna** loetelu väärtusest ja neid ei tohi omavahel segamini ajada. |

## <a name="price-groups"></a>Hinnagrupid

Hinnagrupid on rakenduses Commerce hinna ja allahindluste haldamise keskmes. Hinnagruppe kasutatakse hindade ja allahindluste määramiseks kaubanduse üksustele (nt kanalitele, kataloogidele, ühendustele ja püsikliendiprogrammidele). Kuna hinnagruppe kasutatakse igasuguse hinnakujunduse ja allahindluste jaoks, on väga oluline, et plaaniksite, kuidas neid enne alustamist kasutate.

Eraldi on hinnagrupp lihtsalt nimi, kirjeldus ja valikuliselt hinnakujunduse prioriteet. Hinnagruppide juures on peamine meeles pidada, et neid kasutatakse mitu-mitmele-seoste haldamiseks, mis on allahindlustel ja hindadel kaubanduse üksustes olemas.

Alloleval joonisel on näidatud, kuidas hinnagruppe kasutatakse. Pange tähele, et sellel joonisel on hinnagrupp täpselt hinnakujunduse ja allahindluse haldamise keskel. Kaubanduse üksused, mida kasutate eristavate hindade ja allahindluste haldamiseks, on vasakul, ning tegelik hind ja allahindluse kirjed on paremal.

![Hinnagrupid.](./media/PriceGroups.png "Hinnagrupid")

Hinnagruppe luues ei tohiks kasutada üht hinnagrupi mitut tüüpi kaubanduse üksuste jaoks. Muidu võib olla keeruline määrata, miks konkreetset hinda või allahindlust kandele rakendatakse.

Nagu punane katkendjoon joonisel näitab, toetab Commerce Microsoft Dynamics 365 otse kliendile määratud hinnagrupi põhifunktsioone. Kuid sellisel juhul saate ainult müügihinna kaubanduslepingud. Kui soovite rakendada kliendipõhiseid hindu, soovitame otse kliendile hinnagruppe mitte määrata. Selle asemel kasutage alluvusi. 

Pidage meeles, et kui kliendile on seadistatud hinnagrupp, siis seotakse hinnagrupp selle kliendi jaoks loodud tellimuste müügitellimuse päisega. Kui kasutaja muudab tellimuse päises hinnagruppi, siis asendatakse vana hinnagrupp uue hinnagrupiga vaid käesoleva tellimuse jaoks. See tähendab, et vana hinnagrupp ei mõjuta näiteks käesolevat tellimust, kuid seda seostatakse sellegipoolest kliendi tulevaste tellimustega.

Järgmistes jaotistes on rohkem teavet kaubanduse üksuste kohta, mida saate hinnagruppide kasutamisel kasutada eraldi hindade määramiseks. Kõikide nende üksuste hindade ja allahindluste konfiguratsioon on kahesammuline protsess. Neid samme võib läbida mis tahes järjekorras. Kuid loogiline järjekord on kõigepealt määrata üksustele hinnagrupid, kuna see samm on tõenäoliselt ühekordne seadistamissamm, mida tehakse juurutamise ajal. Kui hinnad ja allahindlused on loodud, saate neile eraldi määrata hinnagrupid.

### <a name="channels"></a>Kanalid

Kaubanduse tööstuses on väga tavaline, et eri kanalites on eri hinnad. Kaks peamist tegurit, mis kanalipõhiseid hindu mõjutavad, on hinnad ja kohalikud turutingimused.

- **Kulud** – mida kaugemal on kanal toote lähtekohast, seda kallim on toote laos hoidmine. Näiteks värskel tootel on piiratud kõlblikkusaeg ja konkreetne tootmisplaan (nt kasvuaeg). Talvel maksab värske lehtsalat tõenäoliselt rohkem põhjapoolsetes kui lõunapoolsetes kohtades. Kui määrata hindu kanalitele suurel geograafilisel alal, tahate ilmselt määrata eri kanalitele erinevad hinnad.
- **Kohalikud turutingimused** – kauplus, millest üle tee on otsene konkurent, on palju hinnatundlikum kui kauplus, mille läheduses otseseid konkurente pole.

### <a name="affiliations"></a>Alluvused

Alluvuse üldine definitsioon on seos grupiga. Commerce’is on alluvused kliendigrupid. Alluvused on palju paindlikum vahend kliendi hinnakujunduseks ja allahindluste määramiseks kui Microsoft Dynamics 365 kliendigruppide ja allahindlusgruppide põhimõte. Esiteks saab alluvust kasutada nii hindade kui ka allahindluste jaoks, samas kui jaemüügiga mitteseotud hinnakujundusel on eraldi grupp iga allahindluse ja hinna tüübi jaoks. Teiseks võib klient kuuluda mitmesse alluvusse, aga vaid ühte iga tüübi jaemüügiga mitteseotud hinnakujundusgruppi. Viimasena, kuigi alluvusi saab seadistada nii, et need on kliendiga seotud, ei pea seda tegema. Konkreetseks otstarbeks mõeldud alluvust saab POS-is kasutada anonüümsete klientide jaoks. Anonüümse alluvuse allahindluse tüüpiline näide on allahindlus pensionäridele või õpilastele, mille korral klient saab allahindluse vaid grupi liikmekaarti näidates.

Kuigi alluvused on kõige sagedamini seotud allahindlustega, saab neid kasutada ka eristava hinnakujunduse määramiseks. Näiteks kui jaemüüja müüb töötajale, võib ta soovida müügihinda muuta, selle asemel et rakendada tavahinnale allahindlust. Näiteks võib ka jaemüüja, kes müüb nii tavaklientidele kui ka äriklientidele, pakkuda äriklientidele paremaid hindu, lähtudes ostu mahust. Alluvuste korral on võimalikud mõlemad variandid.

### <a name="loyalty-programs"></a>Püsikliendiprogrammid

Hindade ja allahindluste korral on püsikliendiprogrammid lihtsalt konkreetse nimega alluvus. Püsikliendiprogrammidele, nagu ka alluvusele, saab määrata nii hindu kui ka allahindlusi. Kuid see, kuidas klientidele määratakse püsikliendi hinnakujundus kande või tellimuse ajal, erineb sellest, kuidas tehakse alluvuse hinnakujundust. Kliendid saavad püsikliendihindu vaid siis, kui kandele lisatakse püsikliendikaart. Kui kandele lisatakse püsikliendikaart, lisatakse ka püsikliendiprogramm. Seejärel pakub püsikliendiprogramm erihindu ja allahindlusi.

Püsikliendiprogrammidel on mitu kihti ja allahindlused võivad eri kihtidel olla erinevad. Nii saavad jaemüüjad anda sagedastele klientidele suuremaid preemiaid, ilma et peaksid neid kliente käsitsi spetsiaalsesse gruppi panema.

Püsikliendiprogrammidel on peale hindade ja allahindluste lisafunktsioonid. Kuid hindade ja allahindluste osas on need sama kui alluvused.

### <a name="catalogs"></a>Kataloogid

Mõni jaemüüja kasutab füüsilisi või virtuaalseid katalooge toodete turustamiseks ja nende hinna kujundamiseks klientide koondgruppide jaoks. Osana ärimudelist turustada kataloogi kaudu saavad need jaemüüjad määrata kataloogides eristavaid hindu. Microsoft Dynamics 365 toetab seda võimalust, lastes teil määrata kataloogipõhiseid allahindlusi ja hindu, nagu saate määrata ka kanalipõhiseid või alluvusepõhiseid allahindlusi. Kataloogi redigeerides saate hinnagruppe seostada kataloogiga, nagu ka kanali, alluvuse või püsikliendiprogrammiga.

### <a name="best-practices-for-price-groups"></a>Hinnagruppide head tavad

Ärge kasutage hinnagruppi mitme kaubanduse üksuse tüübi jaoks. Selle asemel kasutage üht hinnagruppide kogumit kanalite, teist hinnagruppide kogumit alluvuste või püsikliendiprogrammide jaoks jne. Võite hinnagrupi nimes kasutada ees- või järelliidet, et visuaalselt rühmitada eri hinnagruppide tüüpe, mida kasutate.

Vältige hinnagruppide määramist otse kliendile. Selle asemel kasutage alluvust. Sedasi saate määrata kõik hindade ja allahindluste tüübid klientidele, mitte ainult müügihinna kaubanduslepingutele.

## <a name="pricing-priority"></a>Hinnakujunduse prioriteet

Eraldi on hinnakujunduse prioriteet lihtsalt number ja kirjeldus. Hinnakujunduse prioriteete saab rakendada hinnagruppidele või otse allahindlustele. Kui hinnakujunduse prioriteete kasutatakse, lasevad need jaemüüjal tühistada hea tava põhimõtet, juhtides järjekorda, milles hindu ja allahindlusi toodetele rakendatakse. Kõrgemat hinnakujunduse prioriteedi numbrit hinnatakse enne madalamat hinnakujunduse prioriteedi numbrit. Kui mis tahes prioriteedi numbris leidub hind või allahindlus, eiratakse kõiki hindu ja allahindlusi, mille prioriteedi number on madalam.

Hind ja allahindlus võivad pärineda erinevatest hinnakujunduse prioriteetidest, kuna hinnakujunduse prioriteedid rakenduvad hindadele ja allahindlustele sõltumatult.

Hindade hinnakujunduse prioriteedi kasutamiseks peate määrama hinnagrupile hinnakujunduse prioriteedi ja seejärel looma sellele hinnagrupile müügihinna kaubanduslepingu.

Hinnakujunduse prioriteedi funktsioon võeti kasutusele, et toetada stsenaariumi, kus jaemüüja soovib konkreetsele kaupluste kogumile rakendada kõrgemaid hindu. Näiteks on jaemüüja määranud piirkondlikud hinnad Ameerika Ühendriikide idarannikule, aga soovib kõrgemaid hindu mõnele tootele New Yorgi kauplustes, kuna linnas maksab mõne toote müümine rohkem ja/või kohalikul turul kehtib kõrgem hind.

Nagu kirjeldasime selle teema jaotises „Parim hind”, valib hinnakujunduse mootor tavaliselt kahest hinnast madalama. Seetõttu ei saa jaemüüja enamasti kasutada kahest kõrgemat hinda kaupluses, millel on nii idaranniku kui ka New Yorgi hinnagrupid. Selle probleemi lahendamiseks enne hinnakujunduse prioriteedi funktsiooni kasutusele võtmist pidi jaemüüja määrama hinnad iga tootele kaks korda ja mitte määrama mõlemat hinnagruppi. Teine võimalus oli luua täiendavad hinnagrupid, et eraldada kõrgema hinnaga tooteid tavalise, madalama hinnaga toodetest.

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

Baashind ja kaubanduslepingu hind on osa Dynamics 365 põhisisust ning need on saadaval ka siis, kui te Commerce’i ei kasuta. Hinna korrigeerimise funktsioon on saadaval ainult Commerce’is. Järgmises jaotises on rohkem teavet hindade määramise võimaluste kohta ja selles selgitatakse, kuidas need võimalused koos toimivad.

## <a name="setting-prices"></a>Hindade määramine

### <a name="base-price"></a>Baashind

Lihtsaim koht tootele hinna määramiseks on otse tootel. Otse tootel määratud väärtuse kohta öeldakse sageli toote baashind. Baashinna saate määrata väljas **Hind** vahekaardil **Müük** lehel **Väljastatud toote üksikasjad**. Sisestatud väärtus on esitatud ettevõtte valuutas. Vaikimisi on hind esitatud kogusega 1 mõõtühiku kohta (UoM), mis on määratud väljas **Ühik** vahelehel **Müük**. Tegelik hind toote ühiku kohta põhineb UoM-il, hinna kogusel ja valuutal.

Kui tootel on kõigi jaoks üks hind, pakub baashind kõige tõhusamat viisi selle toote hinna haldamiseks. Isegi kui kasutate hindade määramiseks kaubanduslepinguid, võite tootele määrata ka baashinna. Kui te siis ei kasuta kaubanduslepingut **Kõik**, on teil olemas varuhind, mida kasutatakse, kui kaubanduslepingut ei rakendu.

Kui kanali valuuta erineb ettevõtte valuutast, määratakse selle kanali baashind, kasutades tootele määratud hinnal valuutateisendust.

Kuigi hinnaühik ei ole tavastsenaarium, toetab hinnakujunduse mootor seda. Kui hinnaühik on määratud muule väärtusele kui **0** (null), on hind ühiku kohta võrdne võrrandiga hind ÷ hinnaühik. Näiteks kui kauba hind on 10 dollarit ja hinnaühik on 50, on koguse 1 hind 0,20 dollarit (= 10 ÷ 50).

### <a name="sales-price-trade-agreement"></a>Müügihinna kaubandusleping

Kaubanduslepingu töölehte kasutades saate luua igale tootele müügihinna kaubanduslepinguid. Rakenduses Microsoft Dynamics 365 on kolm müügihinna kaubanduslepingutele kolm kliendiulatust: **Tabel**, **Grupp** ja **Kõik**. Kliendiulatus määrab kliendid, kellele konkreetne müügihinna kaubandusleping kehtib.

Müügihinna kaubandusleping **Tabel** on ühele kliendile, kes on määratud otse kaubanduslepingus. See stsenaarium ei ole tavaline ettevõtte ja tarbija vaheline (B2C) stsenaarium. Samas kui see tekib, kasutab hinnakujunduse mootor kaubanduslepinguid **Tabel**, kui see määrab hinna.

Müügihinna kaubandusleping **Grupp** on tüüp, mida kasutatakse kõige sagedamini. Väljaspool Commerce’i on müügihinna kaubanduslepingud **Grupp** mõeldud lihtsatele kliendigruppidele. Kuid Commerce’is on kliendigrupi mõistet laiendatud, nii et see on üldisem hinnagrupp. Hinnagrupp võib olla seotud kanali, alluvuse, püsikliendi programmi või kataloogiga. Üksikasjalikku teavet hinnagruppide kohta leiate selle teema jaotisest „Hinnagrupid”.

> [!NOTE]
> Kaubanduslepingu hinda kasutatakse alati enne baashinda.

### <a name="price-adjustment"></a>Hinna korrigeerimine

Nagu nimigi ütleb, kasutatakse hinna korrigeerimist selleks, et muuta hinda, mis oli määratud otse tootele või kaubanduslepingu kaudu. Hinna korrigeerimist saab kasutada ainult hinna langetamiseks, mitte selle tõstmiseks. Hinna korrigeerimine on soovitatav jaemüüjatele toodete hinnavähenduste loomiseks, jälgimiseks ja haldamiseks aja jooksul.

Hinna korrigeerimisi on kolme tüüpi: protsendi mahaarvutamine, summa mahaarvutamine ja hind. Hinna korrigeerimist protsendi või summa mahaarvutamisega rakendatakse alati müügitehingule. Kuid hinna järgi hinna korrigeerimist kasutatakse ainult siis, kui korrigeeritud hind on väiksem kui hind, mis määrati baashinda või kaubanduslepingu hinda kasutades. Seega, kui hinna korrigeerimises määratud hind on kõrgem kui korrigeerimata hind, siis hinna korrigeerimist ei kasutata.

## <a name="determining-price-for-a-product-in-a-transaction"></a>Hinna määramine tehingus olevale tootele

Tehingu hinna ja allahindluse arvutamisel kasutatakse kliendi jaoks parima hinna leidmise põhimõtet. Kui leitakse rohkem üks hind, kasutatakse selle põhimõtte järgi madalaimat hinda. Peale selle kasutatakse allahindluste kombinatsiooni, mis annab suurima allahindluse summa kogu tehingule. Mõnel juhul tuleb ühel tootel kasutada väiksemat allahindlust, et teistele tehingus olevatele toodetele saaks rakendada lisaallahindlusi.

Ainus erand kliendi jaoks parima hinna leidmise põhimõttele on soodsaimate allahindluste sobitamise võimalus. See suvand laseb kasutada kõige soodsamaid allahindlusi, mis toodete valimisel ja rühmitamisel on jaemüüjale kasuks. Seega, kui tehing sisaldab rohkem tooteid, kui on vaja soodsaima allahindluse kasutamiseks, valib hinnakujunduse mootor tooted, mis annavad kliendi jaoks väikseima võimaliku allahindluse summa.

Hinnakujunduse mootor annab iga toote kohta kolm hinda: baashind, kaubanduslepingu hind ja aktiivne hind.

Baashind on lihtsalt toote atribuut ja see on kõikjal kõigi jaoks sama.

Kui müügihinna kaubanduslepingul on suvandi **Otsi järgmine** väärtuseks **Jah**, kasutatakse kaubanduslepingu hinnana madalaimat hinda, mis vastavate müügihinna kaubanduslepingute kohta leitakse. Kaubanduslepinguid leiab, kasutades hinnagruppe või kontokoodi **KÕIK**. Teine võimalus on määrata kaubanduslepinguid otse kliendile. Kui suvandi **Otsi järgmine** väärtus on **Ei**, kasutatakse esimest leitud kaubanduslepingu hinda. Kui ühtegi müügihinna kaubanduslepingut ei leita, määratakse kaubanduslepingu hind võrdseks baashinnaga.

Aktiivne hind arvutatakse, võttes kaubanduslepingu hind ja rakendades suurimat hinna korrigeerimist, mis tootele kehtib. Kui ühtegi hinna korrigeerimist ei leita või arvutatud aktiivne hind on kõrgem kui kaubanduslepingu hind, määratakse aktiivne hind võrdseks kaubanduslepingu hinnaga. Pidage meeles, et toote hind ei saa tõsta, kasutades hinna korrigeerimist. Kehtiva hinna korrigeerimise leiate, kasutades kanalile, kataloogile, alluvusele või püsikliendiprogrammile määratud hinnagruppe.

## <a name="category-price-rules"></a>Kategooria hinnareeglid

Commerce’i kategooria hinnareeglite funktsioon on lihtne moodus uute kaubanduslepingute loomiseks kõikidele kategoorias olevatele toodetele. Selle funktsiooniga saate automaatselt leida kategoorias olevate toodete jaoks olemasolevaid kaubanduslepinguid ja neid kehtetuks muuta.

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
- Commerce’i toimingute variandipõhised hinnad kõige konkreetsematest kõige vähem konkreetsemateni. Kui tootedimensioon ei mõjuta hinda, ei pea te sellele kaubanduslepinguid määrama. Näiteks toode on saadaval kolmes värvis ja neljas suuruses, aga hind erineb vaid suuruse põhjal. Kui määrate igale variandile kaubanduslepingu, loote 12 kirjet. Selle asemel saate määrata kaubanduslepingu ainult igale suurusele ja jätta värvi dimensiooni tühjaks. Sel juhul loote ainult neli kirjet.

    Kui iga dimensiooni väärtus ei loo eri hinda, saate tooteetalonile määrata ühe kaubanduslepingu ja jätta kõik tootedimensioonid tühjaks. Seejärel määrake eraldi kaubandusleping ainult iga dimensiooni väärtusele, mis loob erineva hinna. Näiteks kui XXL-suuruse hind on kõrgem, aga kõikide teiste suuruste hind on sama, on vaja vaid kaht kaubanduslepingut: üks tooteetalonile ja üks XXL-suurusele.

## <a name="prices-that-include-tax-vs-prices-that-exclude-tax"></a>Maksu sisaldavad ja maksu mitte sisaldavad hinnad

Kui määrate Dynamics 365-s müügihinnad, siis te ei määra, kas määratav hinnaväärtus sisaldab maksu või mitte. Väärtus väljal lihtsalt hind. Samas kanalite säte **Hind sisaldab käibemaksu** laseb konfigureerida kanaleid nii, et need kas lisavad hinnale maksu või mitte. See säte on määratud kanalis ja seda saab muuta isegi ühes ettevõttes.

Kui töötate nii hõlmavate kui ka välistavate maksutüüpidega, on väga oluline määrata hinnad õigesti, kuna kogusumma, mille klient maksab, muutub, kui kanali sätet **Hind sisaldab käibemaksu** muudetakse.

## <a name="differences-between-retail-pricing-and-non-retail-pricing"></a>Erinevused jaemüügi hinnakujunduse ja jaemüügiga mitteseotud hinnakujunduse vahel

Hindade arvutamiseks kõikides kanalites (kõnekeskus, kauplus ja e-poed) kasutatakse üht hinnakujunduse mootorit. See aitab lubada ühtlustatud kaubanduse stsenaariume.

Hinnakujundus on loodud toimima jaemüügiüksustega, mitte jaemüügiga mitteseotud üksustega. Eeskätt on see loodud määrama hindu kaupluse, mitte lao järgi.

Hinnakujunduse mootor **ei toeta** järgmisi hinnakujunduse funktsioone.

- Hinna määramine tegevuskoha või tegevuskoha ja laoala dimensioone kasutades pole toetatud. Kui täpsustate kaubandusleppes ainult tegevuskoha dimensioonid, siis hinnakujunduse mootor ignoreerib tegevuskohta ja rakendab kaubandusleppe kõigile saitidele. Kui määrate nii tegevuskoha kui ka lao, siis on käitumine määratlemata/testimata, kuna eeldatakse, et jaemüüjad kasutavad poe hinnagruppe, kontrollida iga kaupluse/lao hindu.
- Atribuudipõhist hinnakujundust ei toetata.
- Hankija allahindluse läbimist ei toetata.
- Tavapärane Supply Chain Managementi hinnastamismootor toetab hindade arvutamist praeguse kuupäeva kõrval „Soovitud lähetuskuupäeva“ ja „Soovitud sissetulekukuupäeva“ alusel. Samas ei toeta jaemüügi hinnakujundus hetkel neid väärtusi. Põhjuseks on tõsiasi, et B2C stsenaariumite puhul ei eelda kliendid, et soovitud sissetulekukuupäev mõjutab kauba hinda. Mõnel juhul rakendavad jaemüüjad nii B2B kui ka B2C toiminguid. B2B toimingute puhul on tavaline, et hinnad muutuvad sõltuvalt sissetulekukuupäevadest. Need jaemüüjad saavad kasutada B2B äritegevuses Supply Chain Managementi hinnakujundust ja B2C äritegevuses jaemüügi hinnakujundust. Jaemüügi hinnakujundus hakkab tööle vaid siis, kui rakenduse kasutaja lisatakse kõnekeskuse kasutajaks, nii et jaemüüjad saavad määrata teatud kasutajad, kes töötavad Supply Chain Managementi hinnakujundusega, ning mõned kasutajad, kes töötavad jaemüügi hinnakujundusega, st need kasutajad tuleks lisadada kõnekeskuse kasutajatena. Lisaks peab olema sisse lülitatud atribuut **Tänase kuupäeva kasutamine hindade arvutamisel** jaotises **Kaubanduse parameetrid > hinnakujundus ja allahindlused > Mitmesugune**. Sel moel saavad nad Supply Chain Managementi hinnakujundamisel jätkata ostureskontro parameetri väärtuse kasutamist soovitud lähetuskuupäeva või soovitud sissetulekukuupäeva jaoks, kuid jaemüügi hinnakujunduses rakendatakse hindade arvutamisel jätkuvalt tänast kuupäeva.

Peale selle toetab järgmisi hinnakujunduse funktsioone **ainult** hinnakujunduse mootor.

- Hind põhineb tootedimensioonil kõige konkreetsemast variandi hinnast kõige vähem konkreetse variandi hinnani tooteetaloni hinnani. Hinda, mis on määratud kaht tootedimensiooni kasutades (nt värv ja suurus), kasutatakse enne hinda, mis on määratud ainult üht tootedimensiooni kasutades (nt suurus).
- Hinnakujunduse ja allahindluste juhtimiseks saab kasutada sama hinnagruppi.

## <a name="pricing-api-enhancements"></a>Hinnakujunduse API-täiustused

Hind on üks kõige tähtsamaid tegureid, mis juhivad klientide ostuotsuseid, ja paljud kliendid võrdlevad enne ostu sooritamist hindu eri veebisaitidel. Selleks, et tagada konkurentsivõimeliste hindade pakkumine, jälgivad jaemüüjad hoolikalt oma konkurente ning korraldavad sageli kampaaniaid. Aitamaks jaemüüjatel kliente ligi meelitada, on seega väga oluline, et toote otsingu lehel, sirvimise funktsiooni puhul ning toote üksikasjade lehel kuvataks kõige täpsemaid hindu.

Rakenduse Commerce tulevases väljalaskes esitab rakenduse programmeerimisliides (API) **GetActivePrices** hindu, mis kaasavad lihtsaid allahindlusi (näiteks ühe rea allahindlused, mis ei sõltu muudest ostukorvis olevatest kaupadest). Sellisel moel on kuvatud hinnad sarnasemad tegeliku summaga, mida kliendid kaupade eest maksavad. See API kaasab kõiki lihtsate allahindluste tüüpe: alluvus-, püsikliendi-, kataloogi- ja kanalipõhised allahindlused. Peale selle esitab see API rakendatud allahindluste nimed ja kehtivusteabe, nii et jaemüüjad saavad pakkuda üksiksasjalikumat hinnakirjeldust ning rõhutada kiireloomulisust, kui allahindluse kehtivus peagi aegub.


[!INCLUDE[footer-include](../includes/footer-banner.md)]