---
title: Toote valmisolek
description: See artikkel selgitab, kuidas te saate kasutada valmisoleku kontrolle, et veenduda, et toote nõutud koondandmed on enne kannetes kasutamist lõpetatud.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a8e76d5fc786b6f4cac7cd0430399ca3ad13a7bc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856218"
---
# <a name="product-readiness"></a>Toote valmisolek

[!include [banner](../includes/banner.md)]

Saate kasutada valmisoleku kontrolle, et tagada, et nõutavad põhiandmed täpsustatakse toote kohta enne selle kannetes kasutamist. Kui kasutatakse valmisoleku kontrolle, vastutab kasutaja või meeskond kindla eelmääratletud tootega seotud teabe kinnitamise eest.

Pärast kõigi nõutavate andmete sisestamist ja kontrollimist ning pärast kõigi valmisoleku kontrollide töötlemist saate insenertehnilise toote, variandi või versiooni jaoks märkeruudu **Aktiivne** märkida. Kui toote, versiooni või variandi jaoks pole üht või mitut tšekki töödeldud, siis kui proovite märkida märkeruutu **Aktiivne**, kuvatakse teile kiire hoiatus, et kõik kontrollid pole lõpule viidud.

Saate luua valmisoleku kontrolli uute tehniliste toodete, variantide ja versioonide jaoks. Valmisolekukontrolli saate rakendada ka standardsetele (mitte-tehnilistele) toodetele (vaata ka [Standardsete toodete valmisolekukontrollid](#standard-products)). 

Tehingutes saate kasutada standardtooteid, kuigi kõik valmisoleku kontrollid pole lõpule viidud. Kui peate blokeerima toote kasutamise tehingutes, kasutage selle töötsükli olekut. Saate määrata töötsükli oleku, mis blokeerib toote kasutamise tehingutes, ja seejärel, pärast kõigi valmisoleku kontrollide lõpetamist, saate määrata uue töötsükli oleku, mis võimaldab nõutavaid tehinguid.

## <a name="types-of-readiness-checks"></a>Valmisoleku kontrollide tüübid

Valmisoleku kontrolle on kolme tüüpi.

- **Süsteemi kontroll** – Süsteem kontrollib, kas on olemas kehtiv kirje. Näiteks võib kirje olla aktiivne materjalide spetsifikatsioon.
- **Manuaalne kontroll** – Kasutaja kontrollib, kas kirje on kehtiv. Näiteks võib valmisoleku kontroll nõuda vaikimisi tellimuse sätete kinnitamist. Mõnel juhul, näiteks kui toode on veel projekteerimises ja seetõttu ei paigutata seda lattu, ei nõuta vaikimisi tellimuse sätteid. Siiski võib olla vajalik, et mõne teise sama tüüpi toote puhul oleks vaikimisi tellimuse sätted nõutavad, sest toodet saab laos hoida. Kasutaja vastutab selle eest, kuidas õigesti otsustada, kas valmisoleku kontroll on nõutav.
- **Kontroll-loend** – Kasutaja vastab kontroll-loendi küsimustele ja süsteem määrab, kas vastused vastavad ootustele. Kontroll-loendis võib olla mis tahes teema. Näiteks saab seda kasutada, et teha kindlaks, kas turundusmaterjalid või toote dokumentatsioon on lõpule viidud.

<a name="checks-engineering"></a>

## <a name="how-readiness-checks-are-created-for-a-new-engineering-product-variant-or-version"></a>Kuidas valmisoleku kontroll luuakse uue toote, variandi või versiooni jaoks

Valmisoleku kontrolli poliitikaid saab rakendada väljastatud toote tasemel, väljastatud variandi tasemel ja tehnilise versiooni tasemel.

Kui loote uue *inseneritoote*, määrab süsteem, kas selle suhtes kehtib [valmisolekukontrolli poliitika](#assign-policy). Kui rakendatakse valmisolekukontrolli poliitikat, ilmnevad järgmised sündmused:

- Toote jaoks luuakse valmisoleku kontrollid vastavalt kehtivale poliitikale.
- Tehniline versioon on seatud passiivseks, et blokeerida toote kasutamine. Kõik toote tehnikaversioonid on seadistatud passiivseteks.

Kui uus *variant* on loodud tootele, rakendub valmisolekukontrolli poliitika. (Valmisoleku kontrolle saab rakendada väljastatud variandi tasemel ja tehnilise versiooni tasemel.) Kui valmisoleku kontroll on seadistatud, toimuvad järgmised sündmused:

- Toote jaoks luuakse valmisoleku kontrollid vastavalt kehtivale poliitikale.
- Tehniline versioon on seatud passiivseks, et blokeerida toote kasutamine.

Kui uus *variant* on loodud tootele, rakendab süsteem sellele kontrolliks valmisolekukontrolli poliitika. (Valmisoleku kontrolle saab rakendada väljastatud variandi tasemel). Kui valmisoleku kontroll on seadistatud, toimuvad järgmised sündmused:

- Toote jaoks luuakse valmisoleku kontrollid vastavalt kehtivale poliitikale.
- Tehniline versioon on seatud passiivseks, et blokeerida toote kasutamine.

> [!NOTE]
> Te saate rakendada ka valmisolekukontrollid standardsetele (mitteinsenerilistele) toodetele. Lisateavet vt jaotisest Standardtoodete [valmisolekukontrollid](#standard-products) (selles artiklis).

## <a name="view-readiness-checks"></a>Valmisoleku kontrollide kuvamine

### <a name="view-open-readiness-checks-for-a-product-or-product-version"></a>Toote või toote versiooni avatud valmisoleku kontrollide kuvamine

Toote avatud valmisoleku kontrollide otsimiseks avage leht **Väljastatud toodete üksikasjad**. Seejärel tehke tegumiriba vahekaardil **Toode** grupis **Valmisoleku kontrollid** valik **Valmisoleku kontrollid**.

Kui soovite leida toote versiooni jaoks avatud valmisoleku kontrolli, avage väljastatud tootele leht **Tehnilised versioonid** ja valige versioon. Seejärel tehke tegumiriba vahekaardil **Toode** grupis **Kontroll-loend** valik **Valmisoleku kontrollid**.

### <a name="view-open-readiness-checks-that-are-assigned-to-you"></a>Teile määratud avatud valmisoleku kontrollide kuvamine

Teile määratud avatud valmisoleku kontrollide vaatamiseks järgige ühte järgmistest sammudest.

- Mine **Tehniliste muutuste haldus \> Tavaline \> Toote valmisolek \> Minu avatud valmisoleku kontrollid**.
- Mine **Tooteinfo haldus \> Tööruumid \> Toote valmidus diskreetseks tootmiseks**.

Seadistus, mis määrab, kellele on määratud valmisoleku kontroll, tehakse tehniliste toodete kategooria jaoks. Valmisoleku kontrolli saab määrata isikule või meeskonnale. Kui valmisoleku kontroll on määratud meeskonnale, on meeskonnas üks isik, kes peab valmisoleku kontrolli töötlema.

## <a name="process-open-readiness-checks"></a>Avatud valmisoleku kontrollide töötlemine

### <a name="process-system-and-manual-readiness-checks"></a>Süsteemi ja manuaalsete valmisoleku kontrollide töötlemine

Kui olete avanud **Valmisoleku kontrollid** lehe, saate vaadata süsteemi ja manuaalse valmisoleku kontrollide teemat, valides tegevuspaanil **Seotud teabe vaatamine**. Seejärel saate valmisoleku kontrolli andmeid täiendada ja/või kontrollida. Avatud valmisoleku kontrolli **oleku** väärtus on *Ootel*. See olek näitab, et valmisoleku kontrolli peab veel töötlema. Valmisoleku kontrolli töötlemiseks järgige üht järgmist juhist.

- Tegevuse paanil valige **Kontrolli/Vii lõpule**, et vaadata üle ja viia lõpule valmisoleku kontroll. Kui olete lõpetanud, uuendatakse **Olek** välja *Läbitud*.
- Tegevuse paanil valige **Jäta vahele**, kui soovite vahele jätta valmisoleku kontrolli, mis pole kohustuslik. Näiteks seadistate valmisoleku kontrolli hinna arvutuste jaoks. Siiski otsustate selle kontrolli vahele jätta, kui toode on veel projekteerimise faasis. Sel juhul uuendatakse **Olek** välja väärtuseks *Vahele jäetud*.

Sõltuvalt valmisolekupoliitika konfiguratsioonist, kui valmisoleku kontrolli väli **Olek** on värskendatud olekusse *Läbitud*, valmisoleku kontrolli kinnitamiseks võib olla vajalik lisasamm. Sellisel juhul valige valmisoleku kontrolli lõpuleviimiseks **Kinnita**. See kinnitamise etapp on alati kohustuslik, kui valmisoleku kontroll jäetakse vahele.

Kui kõik avatud valmisoleku kontrollid uue toote, variandi või versiooni kohta on töödeldud ja kinnitatud vastavalt nõudmistele, muutub kaup automaatselt aktiivseks ja on seeläbi kasutamiseks valmis.

### <a name="process-checklist-readiness-checks"></a>Kontroll-loendi valmisoleku kontrollide töötlemine

Kontroll-loendi avamiseks avage **Valmisoleku kontrollid** leht ja seejärel valige tegevuspaanil **Käivita kontroll-loend**. Kui olete kontroll-loendi lõpetanud, kontrollib süsteem, kas valmisoleku kontroll on vastu võetud, võttes arvesse küsimustiku sätteid. Kui kontroll on vastu võetud, uuendatakse **Olek** väli olekusse *Läbitud*. Kui valmisoleku kontroll pole kohustuslik, saate selle vahele jätta. Sel juhul uuendatakse **Olek** välja väärtuseks *Vahele jäetud*.

Sõltuvalt valmisolekupoliitika konfiguratsioonist, kui valmisoleku kontrolli väli **Olek** on värskendatud olekusse *Läbitud*, valmisoleku kontrolli kinnitamiseks võib olla vajalik lisasamm. Sellisel juhul valige valmisoleku kontrolli lõpuleviimiseks **Kinnita**. See kinnitamise etapp on alati kohustuslik, kui valmisoleku kontroll jäetakse vahele.

Kui kõik avatud valmisoleku kontrollid uue toote, variandi või versiooni kohta on töödeldud ja kinnitatud vastavalt vajadusele, muutub kaup automaatselt aktiivseks ja on seeläbi kasutamiseks valmis.

## <a name="create-and-manage-product-readiness-policies"></a>Toote valmisoleku poliitikate loomine ja haldamine

Kasutage toote valmisoleku poliitikaid, et hallata tootele rakendatavat valmisoleku kontrolli. Iga valmisoleku poliitika sisaldab valmisoleku kontrolli kogumit. Kui valmisoleku poliitika on määratud tehniliste toodete kategooriale, on kõigil sellest tehniliste toodete kategooriast loodud toodetel valmisoleku kontroll, mis on määratud valmisoleku poliitikas.

Toote valmisoleku poliitikatega töötamiseks valige **Tehniliste muutuste haldus \> Häälestus \> Toote valmisoleku poliitikad**. Seejärel järgige üht neist sammudest.

- Uue poliitika loomiseks valige tegumiriba nupp **Uus** ja seejärel häälestage väljad, nagu on kirjeldatud järgmistes lõikudes.
- Olemasoleva poliitika redigeerimiseks valige see loendipaanil, valige tegumiribal nupp **Redigeeri** ja seejärel häälestage väljad nii, nagu on kirjeldatud järgmistes lõikudes.
- Olemasoleva poliitika kustutamiseks valige see loendipaanil, valige tegumiribal käsk **Redigeeri** ja seejärel veenduge, et **Üldine** FastTab-is on suvandi **Aktiivne** valikuks seatud *Ei*. Seejärel valige tegumiribal suvand **Kustuta**.

### <a name="header"></a>Päis

Häälestage järgmised väljad toote valmisoleku poliitika päises.

| Field | Kirjeldus |
|---|---|
| Nimi | Sisestage poliitika nimi. |
| Kirjeldus | Sisestage poliitika kirjeldus. |

### <a name="general-fasttab"></a>Kiirkaart Üldine

Seadista toote valmisoleku poliitika FastTab-is **Üldine** järgmised seaded.

| Field | Kirjeldus |
|---|---|
| Toote tüüp | Valige, kas poliitika rakendub *kauba* või *teenuse* tüübi toodetele. Pärast kirje salvestamist ei saa seda sätet muuta. |
| Aktiivne | Kasutage seda suvandit, et aidata säilitada valmisoleku poliitikaid. Seadistage see kõigi kasutatavate valmisoleku poliitikate puhul valikule *Jah*. Seadistage see valikule *Ei*, et tähistada valmisoleku poliitikat passiivsena, kui seda ei kasutata. Võtke arvesse, et te ei saa aktiveerida valmisoleku poliitikat, mis on määratud tehniliste toodete kategooriale, ja saate kustutada ainult passiivse väljastamise poliitika. |

### <a name="readiness-control-fasttab"></a>Valmisoleku kontrolli FastTab

Iga valmisoleku kontrolli tüübi kohta, mida soovite poliitikasse kaasata, lisage **Valmisoleku juhtimise** FastTab-i uus rida. Kasutage järgmisi nuppe tööriistaribal FastTab, et lisada ja eemaldada ridu, mida vajate:

- **Lisa kontroll** – Lisage poliitikale standardne valmisoleku kontroll. Selle nupu valimisel kuvatakse dialoogiaken **Lisa kontroll**. Seal saate teha valiku saadaolevate kontrollide loendist.
- **Lisa olemasolev küsimustik** – Lisage ruudustikku tühi rida. Seejärel saate määrata olemasoleva küsimustiku, seadistades väljad järgmises tabelis.
- **Kopeeri** – Lisage ruudustikku valitud rea koopia.
- **Kustuta** – Kustutage valitud rida ruudustikust.

Iga lisatava rea jaoks määrake järgmised väljad.

| Field | Kirjeldus |
| --- | --- |
| Protsessi ala | Valige ala, millega kontroll on seotud. |
| Tüüp | Valige, kas kontroll on süsteemi kontroll, käsitsi koostatud kontroll või kontroll-loend (küsimustik). |
| Nimi | Kui kontroll on kontroll-loend, sisestage nimi. Süsteemi ja manuaalsete kontrollide puhul seatakse see väli automaatselt. |
| Kirjeldus | Kui kontroll on kontroll-loend, sisestage kirjeldus. Süsteemi ja manuaalsete kontrollide puhul määratakse see väli automaatselt ja kirjeldus selgitab kontrolli fookust. |
| Kontrolli rakendamine | Valige, kas rida peaks looma valmisoleku kontrolli vastuseks uuele väljastatud tootele, väljastatud variandile või väljastatud versioonile. |
| Käivitage asukohas | Valige, kas rea loodud valmisoleku kontroll rakendub kõigile ettevõtetele või ühele ettevõttele. |
| Ettevõte | Kui seate **Käivita** välja väärtuseks *Üksik ettevõte*, valige ettevõte. |
| Omaniku tüüp | Valige, kas rea loodav valmisoleku kontroll tuleb määrata isikule või meeskonnale. |
| Omanik | Valige isik või meeskond, kellele rea loodav valmisoleku kontroll tuleb määrata. |
| Küsimustik | Valige küsimustik, mida tuleks kontroll-loendi puhul kasutada. Kontroll-loend on kohalik kontroll-loend ettevõttes, kus valmisoleku kontroll on teostatud. Süsteem peab saama hinnata, kas kontroll-loendile on õigesti vastatud. Seetõttu peab kontroll-loend olema seadistatud nii, et hinnang tehakse õigete vastuste põhjal. Lisateavet küsimustike loomise kohta vt teemast Küsimustike [kasutamine ja](/dynamicsax-2012/appuser-itpro/using-questionnaires) sellega seotud artiklid. |
| Automaatne kinnitamine | Valmisoleku kontrollimise kirjed sisaldavad märkeruutu **Kinnitatud**, mis näitab kinnituse olekut. Märkige **Automaatne kinnitamine** valikruut kontrollidele, mis tuleb kinnitada kohe pärast seda, kui määratud kasutaja on need täitnud. Tühjendage see märkeruut, et nõuda selgesõnalist kinnitust lisasammuna. |
| Kohustuslik | Märkige see ruut kontrollide jaoks, mida määratud kasutaja peab täitma. Kohustuslikke kontrolle ei saa vahele jätta. |

<a name="assign-policy"></a>

## <a name="assign-readiness-policies-to-standard-and-engineering-products"></a>Määrake valmisolekupoliitika standard- ja inseneritoodetele

Kui loote tehnika kategooria põhjal uue toote, loote nii *väljastatud toote* ja seotud *Seotud toote*. Viis, kuidas vabastatud *toote* valmisolekupoliitikad lahendatakse, sõltub sellest, kas toote valmisoleku kontrollide funktsioon on teie süsteemi jaoks sisse lülitatud ([vt](#standard-products) selle funktsiooni kohta üksikasjalikumat teavet selle funktsiooni kohta vt standardsete toodete valmisolekukontrollide jaotisest hilisemas jaotises ja selle kohta, kuidas see sisse või välja lülitada).

- Kui toote *valmisoleku kontrollide* funktsioon on süsteemist *välja* välja lülitatud, seatakse valmisoleku poliitika ja kuvatakse ainult [tehnika kategooria](engineering-versions-product-category.md) kirjetes. Et teada saada, millist poliitikat rakendatakse väljastatud tootele, kontrollib süsteem seotud **tehnikakategooria tootevalmiduse** poliitika välja. Saate muuta olemasoleva toote valmisoleku poliitikat, redigeerides seotud tehnika kategooriat (mitte jagatud toodet).
- Kui toote *valmisoleku kontrollide* funktsioon on *Sisse* lülitatud lisab see **Toote valmisoleku poliitika** välja **Toote** lehele (kus ühiskasutusega tooted on häälestatud) ja **Vabastatud** toote lehele (kus väärtus on kirjutuskaitstud ja võetakse seotudühiskasutusegalt). Süsteem leiab väljastatud toote valmisolekupoliitika, kontrollides seotud ühistoodet. Kui kasutate tehnika kategooriat uue tehnikatoote loomiseks, loob süsteem nii jagatud kui ka väljastatud toote ning kopeerib kõik toote **Valmisoleku poliitika** tehnika kategoorias uuele jagatud sättted tootele. Saate muuta olemasoleva toote valmisoleku poliitikat, redigeerides seotud tehnika kategooriat (mitte jagatud toodet).

Tootele tooteomaniku määramiseks tehke järgmist.

1. Avage **Tooteteabe haldus \> Tooted \> Tooted**.
1. Avage või looge toode, millele soovite määrata valmisolekupoliitika.
1. Seadke kiirkaardil **Üldine** toote valmisoleku poliitika väljale **Tootele rakenduv poliitika** väljal tootele rakenduv poliitika nimi.

Tootele tootekategooria määramiseks tehke järgmist.

1. Minge jaotisse **Tehnilise muudatuse haldamine \>Sammud \> Tehnilise toote kategooria üksikasjad**.
1. Avage või looge toode, millele soovite määrata tehnikakategooria poliitika.
1. Seadke kiirkaardil **toote valmisoleku poliitika** kiirkaardile väljale **Tootele rakenduv poliitika** tootele rakenduv tehnikakategooria.

<a name="standard-products"></a>

## <a name="readiness-checks-on-standard-products"></a>Standardtoodete valmisolekukontrollid

Saate lubada standardsete (mitteinseneriliste) toodete toote valmisolekukontrollid, lülitades funktsioonihalduses sisse *toote valmisoleku* Feature funktsiooni. See funktsioon teeb mõned väikesed muudatused valmisolekukontrolli süsteemis nii, et see toetab standardtooteid.

### <a name="enable-or-disable-readiness-checks-on-standard-products"></a>Standardsete toodete valmisolekukontrollide lubamine või keelamine

See funktsioon nõuab, et nii *tehnika muutmise haldamise* kui *ka toote valmiduskontrolli* funktsioonid lülitatakse teie süsteemi sisse. Üksikasju selle kohta, kuidas neid funktsioone sisse või välja lülitada, vt tehnika [muudatusehalduse ülevaadet](product-engineering-overview.md).

### <a name="create-readiness-policies-for-standard-products"></a>Standardsete toodete valmisolekupoliitika loomine

Te loote standardtoodetele valmisolekupoliitika samuti nagu tehnikatoodete puhul. Vt selle artikli varasemat teavet.

### <a name="assign-readiness-policies-to-standard-products"></a>Standardsete toodete valmisolekupoliitika loomine

Standardsele tootele valmisolekupoliitika määramiseks avage **seotud jagatud toode** ja seadke toote valmisoleku poliitika välirakendumise poliitika nimele. Lisateavet vt selle artikli jaotisest [Standarditoodetele valmisoleku poliitikate määramine standardsetele](#assign-policy) ja inseneritöö toodetele.

### <a name="view-and-process-readiness-checks-on-standard-products"></a>Standardtoodete valmisolekukontrollid

Kui see funktsioon on sisse lülitatud, vaatate ja töötlete standardtoodete valmisoleku kontrolle nagu tehnika toote puhul. Vt selle artikli varasemat teavet.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
