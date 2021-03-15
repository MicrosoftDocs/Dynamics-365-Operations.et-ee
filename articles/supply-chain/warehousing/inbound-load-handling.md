---
title: Ostutellimuste sissetulevate koormate laohaldus
description: Selles teemas kirjeldatakse ostutellimuste sissetulevate koormate laohaldusprotsessi.
author: omulvad
manager: tfehr
ms.date: 03/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadTable, WHSLoadPlanningListPage, WHSLoadPlanningWorkbench, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-21
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 991da4a1056bec933698d043fe45fe4e280f555a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004823"
---
# <a name="warehouse-handling-of-inbound-loads-for-purchase-orders"></a>Ostutellimuste sissetulevate koormate laohaldus

Selles teemas kirjeldatakse ostutellimuste sissetulevate koormate laohaldusprotsessi.

Iga sissetuleva koorma kohta peaks teie süsteem juba sisaldama seotud müügitellimust ja see võib sisaldada ka seotud koorma spetsifikatsioone ja/või transpordiplaani. Lisateavet sissetulevate koormate loomise ja haldamise kohta vt teemast [Äriprotsess: sissetulevate koormate transpordi planeerimine](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/business-process-planning-transportation-for-inbound-loads).

## <a name="overview-how-inbound-loads-are-created-registered-and-received"></a>Ülevaade: sissetulevate koormate loomine, registreerimine ja vastuvõtmine

Järgmisel joonisel on kujutatud tüüpilist kaubavoogu sissetulevate koormate käsitlemiseks, millel on ostutellimuse kogused, kui need saabuvad teie lattu.

![Sissetuleva koorma haldusprotsess](media/inbound-process.png "Sissetuleva koorma haldusprotsess")

1. **Hankija kinnitab ostutellimuse.**

    Protsess algab siis, kui ostutellimus sisestatakse süsteemi ja seejärel tarnitakse hankijale, kes tellimuse kinnitab. Ostutellimus peab olemas olema enne, kui saate luua sissetuleva koorma kirje. Sissetuleva koorma saate siiski luua ka siis, kui tellimust pole kinnitatud. Lisateavet leiate teemast [Ostutellimuste kinnitamine](../procurement/purchase-order-approval-confirmation.md).

1. **Sissetuleva koorma kirje luuakse koorma saabumise ja selle sisu plaanimiseks.**

    Sissetuleva koorma kirje tähistab ühe või mitme ostutellimuse hankija saadetist. Koorem peaks saabuma lattu ühe füüsilise transpordiüksusena (nt autokoorem). Sissetuleva koorma kirjet kasutatakse planeerimiseks ja see võimaldab logistikul jälgida koorma hankijalt saabumise teekonda. Seda kasutatakse ka tellimuserea koguste registreerimiseks ja töötlemise haldamiseks laotoimingute kaudu, nagu saabumisega seotud ja paigutustöö. Koormaid saab luua nii automaatselt kui ka käsitsi ja need võivad põhineda kas ostutellimusel või hankijalt saadud saadetise eelteatisel (ASN). Lisateavet vt teemast [Sissetuleva koorma loomine või muutmine](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/create-or-modify-an-inbound-load).

1. **Hankija kinnitab koorma lähetamise.**

    Kui hankija lähetab koorma, kinnitab vastuvõtvas laos asuv logistik koorma saadetise. Kui vastuvõttev ettevõte kasutab moodulit **Transpordihaldus**, käivitab sissetuleva saadetise kinnitamine muud koorma haldusprotsessid, mis on seotud sissetulevate koormatega. Lisateavet leiate jaotisest [Koorma tarnimiseks kinnitamine](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/confirm-a-load-for-shipping).

1. **Koorem saabub lattu ja töötajad registreerivad kogused.**

    Kui autokoorem saabub vastuvõtvasse lattu, registreerivad laotöötajad koorma kogused. Kui kasutatakse moodulit **Laohaldus**, registreeritakse kogused mobiilsete seadmete abil. Lisateavet leiate jaotistest [Toote sissetulek ostutellimuste suhtes – registreerimine](../procurement/product-receipt-against-purchase-orders.md#registration) ja [Sissetuleva koorma kaubakoguste registreerimine](#register-item-quantities-arriving).

1. **Registreeritud koorma kogused sisestatakse ostutellimustele.**

    Kui koorma kogused on saabumisel registreeritud, peavad need kogused olema kantud ettevõtte lao pearaamatusse, et registreerida varude füüsiline kasv. Lisateavet vt [Toote sissetulek ostutellimuste suhtes – toote sissetulek](../procurement/product-receipt-against-purchase-orders.md#product-receipt) ja [Registreeritud toote koguste sisestamine ostutellimuste kohta](#post-registered-quantities).

## <a name="register-item-quantities-that-arrive-on-an-inbound-load"></a><a name="register-item-quantities-arriving"></a>Sissetuleva koorma kaubakoguste registreerimine

Microsoft Dynamics 365 Supply Chain Management toetab mitut toimingut tellitud toodete saabumise registreerimiseks. Seetõttu saate konfigureerida süsteemi, et see vastaks teie kindlatele ärivajadustele. Selles jaotises kirjeldatakse sissetulevate kaubakoguste registreerimist mobiilsete seadme abil, kui täpsem laohaldus on süsteemis sisse lülitatud. Siiski on olemas alternatiivne voog, mis põhineb mobiilse seadme kasutamise asemel kauba saabumistöölehe kasutamisel. Lisateavet selle voo kohta leiate teemast [Kaupade registreerimine täpsemaks ladustamiseks lubatud kauba puhul saabuva kauba töölehe abil](tasks/register-items-advanced-warehousing.md).

Kui sissetulev koorem saabub lattu, peavad laotöötajad registreerima saadetise kauba kogused. Tavaliselt kasutavad nad pihuskannereid. See töövoog on saadaval ainult juhul, kui süsteemis on olemas järgmised kaubad.

- **Sissetuleva koorma kirje, mis kirjeldab saadetise eeldatavaid kaubakoguseid**

    Tavaliselt kinnitab hankija sissetuleva koorma kirje enne saadetise saabumist lattu. Seetõttu on koorma olek _Saadetud_. Laotöötajad saavad registreerida ka kaupade kogused koormate kohta, mille olek on _Avatud_ või _Vastuvõetud_.

- **Mobiilse seadme menüü, mis on konfigureeritud toetama koorma vastuvõtmist**

    Mobiilsete seadmete jaoks mõeldud [laorakendus](install-configure-warehousing-app.md) toetab järgmisi töö loomise protsesse.

    - Vastuvõetav koormas olev kaup
    - Vastuvõetav ja kõrvaleseatav koormas olev kaup
    - Kombineeritud litsentsiplaadi vastuvõtt, mille korral on mobiilse seadme välja **Lähtedokumendi rea identifitseerimismeetod** menüükäsu väärtuseks seatud _Vastuvõetav koormas olev kaup_. Lisateavet vt teemast [Kombineeritud litsentsiplaadi vastuvõtt](mixed-license-plate-receiving.md).
    - Kombineeritud litsentsiplaadi vastuvõtt ja kõrvaleseadmine, mille korral on mobiilse seadme välja **Lähtedokumendi rea identifitseerimismeetod** menüükäsu väärtuseks seatud _Vastuvõetav koormas olev kaup_. Lisateavet vt teemast [Kombineeritud litsentsiplaadi vastuvõtt](mixed-license-plate-receiving.md).

    > [!NOTE]
    > Olenemata protsessist genereerib süsteem töö, et võtta vastu vastuvõtvas kohas registreeritud kogused ja panna need ära tavalisse ladustamiskohta. Kui kasutatakse protsessi _Vastuvõetav ja kõrvaleseatav koormas olev kaup_ või _Kombineeritud litsentsiplaadi vastuvõtt ja kõrvaleseadmine_, siis annab seade koorma koguse registreerinud töötajale ka korralduse teha paigutustööd registreerimistoimingu osana. Seevastu eeldatakse protsesside _Vastuvõetav koormas olev kaup_ ja _Kombineeritud litsentsiplaadi vastuvõtt_ korral, et paigutustööd tehakse registreerimisülesandest eraldi.

- **Töömall, mis määratleb sissetulevate koormate komplekteerimise ja paigutamise töö**

    See kaup on seotud eelmiste kaupadega. Töökäsu tüübi _Ostutellimus_ jaoks peab teil olema vähemalt üks töömall ja see peab sisaldama komplekteerimise ja paigutamise töö tüüpide kogumit.

Mobiilne seade juhendab lao vastuvõtuametnikku läbi koorma koguse registreerimise töövoo. See voog sisaldab iga koorma ID kohta vähemalt järgmisi etappe.

1. Sisestage koorma ID.
2. Sisestage saadud kauba kaubakood.
3. Sisestage saadud kaubakoodiga seotud kogus.
4. Sisestage kauba algse asukoha identifitseerimisnumber, kui süsteem pole seadistatud seda numbrit automaatselt looma.
5. Puudutage valikut **OK**.

Pärast seda, kui töötaja on need sammud lõpetanud, teeb süsteem vastavate üksuste kohta järgmised värskendused, tingimusel et ostutellimuse rea kogus saabus ühe koormana ja kõik koorma kogused on registreeritud.

| Üksus | Värskendused | Paberraha |
|---|---|---|
| Laadi | Koorma rea välja **Töö loodud kogus** värskendatakse registreeritud koguse näitamiseks. | Väärtuse **Koorma olek** olekuks jääb _Välja saadetud_ või _Avatud_, kui koorma kohta pole saadetise kinnitust esitatud. Kui vähemalt üks paigutustöö rida on käivitatud, muutub see olek olekuks _Pooleli_. |
| Ostutellimuse laokanne, mille jaoks seostuvad koorma kogused on registreeritud |<p>Värskendatakse järgmised väljad.</p><ul><li>Välja <b>Sissetulek</b> väärtuseks on seatud <i>Registreeritud.</i></li><li>Välja <b>Asukoht</b> värskendatakse vastuvõtudoki asukoha koodiga. (See kood on määratud iga lao väljal <b>Vaikimisi vastuvõtu asukoht</b>.)</li><li>Välja <b>Litsentsiplaat</b> värskendatakse identifitseerimisnumbriga, mis sisestati või loodi registreerimise käigus.</li><li>Välja <b>Koorma ID</b> värskendatakse selle koorma numbriga, millega kogus on registreeritud. (Vt märkust.)</li></ul> | Võimalus siduda ostutellimuse varude kanne ja koorma kohta registreeritud kogused võeti versioonis 10.0.9 kasutusele valikulise funktsioonina, mille nimi oli _Ostutellimuse varude kannete seostamine koormaga_. See funktsioon on eriti kasulik töövoogude jaoks, mille korral tarnitakse üks ostetud kaupade tellimus mitme koormana või kui koorem sisaldab mitme ostutellimuse koguseid. |
| Lao ladustamine | Töö luuakse töömalli alusel, et anda töötajale korraldus teisaldada registreeritud kogused vastuvõtvast asukohast tavalisse ladustamiskohta. | Asukoha valikut kontrollib asetamise koha direktiiv. Kui asukoha direktiiv on määratlemata, on töö asetamise koht tühi. |

Võtke arvesse, et lao töötajad saavad registreerida ühe või mitme seotud koormaga ostutellimuse sissetulekut, kasutamata protsessi _Vastuvõetav koormas olev kaup_. Saadaval on järgmised meetodid:

- **Mobiilses seadmes:** kasutage protsesse _Vastuvõttev ostutellimuse rida_ ja _Vastuvõttev ostutellimuse rida ja kõrvaleseadmine_. (Kui ostutellimuse rea koguse kohta on mitu koormat, ei saa töötaja kasutada protsessi _Vastuvõttev ostutellimuse rida_. Selle asemel juhendatakse töötajat kasutama seadme tegevust, mis on seotud protsessiga _Vastuvõetav koormas olev kaup_.)
- **Kliendis:** kasutage kauba saabumise töölehte.
- **Kliendis:** kasutage tegevust **Registreerimine**, millele pääseb juurde ostutellimuse realt.

> [!NOTE]
> Kui ostutellimuse sissetulek registreeritakse mõne eelneva meetodi abil, ei looda ostutellimuse kande ja koorma vahel seost isegi siis, kui funktsioon _Ostutellimuse varude kannete seostamine koormaga_ on sisse lülitatud. Üks seda reeglit puudutav erand on see, kui kasutate suvandit **Vastuvõttev ostutellimuse rida** ja ainult ühel koormal on tellimuse rea jaoks määratud muu olek kui _Vastu võetud_.

### <a name="handle-discrepancies-during-registration-of-inbound-load-quantities"></a>Lahknevuste käsitlemine sissetuleva koorma koguste registreerimisel

Laotöötajad saavad registreerida koorma koguse sissetuleku osaliselt. Iga osalise koorma koguse sissetulek loob seejärel eraldi kande, mille registreeritud koguse sissetuleku olek on _Registreeritud_ ja koorma ID viitab pärinevale ostutellimuse reale.

#### <a name="load-under-receiving"></a>Planeeritust väiksema koorma vastuvõtt

Kui koorma saabudes on kauba kogused väiksemad kui koorma kirjel märgitud kogused, saab lao vastuvõtupersonal töötada otse kliendis, et parandada see lahknevus, vähendades koorma real märgitud kogust, nii et see vastaks tegelikule saabunud ja registreeritud kogusele.

#### <a name="load-over-receiving"></a><a name="load-over-receiving"></a>Planeeritust suurema koorma vastuvõtt

Planeeritust suurema koorma vastuvõtt toimub siis, kui koorma saabudes ületavad kauba kogused koorma real märgitud eeldatava koguse. Saate kontrollida, kas ja millisel määral on planeeritust suurema koorma vastuvõtt koorma registreerimise ajal lubatud.

Kasutage vastavate mobiilsete seadmete menüükäskude välja **Koorma suurem sissetulek**, et kontrollida, mis juhtub, kui laotöötaja üritab registreerida ületarnet. See väli on saadaval mobiilse seadme menüükäskudele, mis kasutavad järgmist tüüpi töö loomise protsesse.

- Vastuvõetav koormas olev kaup
- Vastuvõetav ja kõrvaleseatav koormas olev kaup
- Kombineeritud litsentsiplaadi vastuvõtt (mille korral on välja **Lähtedokumendi rea identifitseerimismeetod** väärtuseks seatud _Vastuvõetav koormas olev kaup_)
- Kombineeritud litsentsiplaadi vastuvõtt ja kõrvaleseadmine (mille korral on välja **Lähtedokumendi rea identifitseerimismeetod** väärtuseks seatud _Vastuvõetav koormas olev kaup_)

Järgmises tabelis selgitatakse välja **Koorma suurem sissetulek** jaoks saadaolevaid suvandeid.

| Väärtus | Kirjeldus |
|---|---|
| Luba | Töötajad saavad registreerida koguste laekumise, mis ületavad valitud koorma ülejäänud registreerimata kogust, kuid ainult juhul, kui registreeritud üldkogus ei ületa koormaga seotud ostutellimuse rea kogust (pärast ületarne protsendi korrigeerimist). |
| Blokeeri | <p>Töötajad ei saa registreerida nende koguste sissetulekut, mis ületavad valitud koorma järelejäänud registreerimata kogust (pärast ületarne protsendi korrigeerimist). Töötaja, kes proovib sissetulekuid registreerida, võtab vastu vea ja ei saa jätkata enne, kui ta registreerib koguse, mis on järelejäänud registreerimata koorma kogusega võrdne või sellest väiksem.</p><p>Vaikimisi kopeeritakse koorma real olev ületarne protsendi väärtus seotud ostutellimuse realt. Kui välja <b>Koorma suurem sissetulek</b> väärtuseks on seatud <i>Blokeeri</i>, kasutab süsteem ületarne protsendi väärtust, et arvutada kogu kogus, mida saab koorma rea jaoks registreerida. Siiski saab seda väärtust üksikute koormate korral vastavalt vajadusele üle kirjutada. See käitumine muutub asjakohaseks vastuvõtuvoogude korral, kui osa tellimuse rea ületarne protsenti kajastavast üleliigsest kogusest või kogu üleliigne kogus jaotatakse ebaproportsionaalselt mitme koorma vahel. Siin on näidisstsenaarium.</p><ul><li>Ühe ostutellimuse rea jaoks on mitu koormat.</li><li>Ostutellimuse real on ületarne protsent, mis on suurem kui 0 (null).</li><li>Kogused on juba registreeritud ühe või mitme koorma kohta ületarne protsenti arvesse võtmata.</li><li>Ületarne kogus märgitakse viimasele koormale.</li></ul><p>Selle stsenaariumi korral saab mobiilset seadet kasutada viimase koorma üleliigse koguse registreerimiseks ainult juhul, kui laoinspektor suurendab vastava koorma rea ületarne protsendi vaikeväärtust väärtuseni, mis on piisavalt suur, et kogu ületarnet saaks viimasele koormale registreerida.</p> |
| Blokeeri ainult suletud koormate puhul | Töötajad võivad vastu võtta üleliigseid koorma rea koguseid avatud koormate jaoks, kuid mitte koormatele, mille olek on _Vastuvõetud_. |

> [!NOTE]
> Välja **Koorma suurem sissetulek** väärtus on _Luba_. Kui seda väärtust kasutatakse, ühtib käitumine standardse käitumisega, mis oli saadaval enne funktsiooni _Koorma rea koguse oodatust suurem sissetulek_ versioonis 10.0.11 kasutusele võtmist.

### <a name="put-away-the-registered-quantities"></a>Registreeritud koguste kõrvale panemine

Kui registreerimine on mobiilses seadmes lõpule viidud, värskendab tegevus _Koguse sissetuleku registreerimine_ varude ja laokirjeid näitamaks, et kogused on nüüd vastuvõtudoki asukohas ja reserveerimiseks saadaval. Kuid ettevõtte laotegevuste korral on tavaliselt nõutav, et kogused teisaldatakse vastuvõtudokilt tavalisse lattu, et hilisemaid komplekteerimisprotsesse saaks läbi viia. Paigutamise juhised jäädvustatakse paigutamistöös, mis luuakse automaatselt, kui sissetulev koorem on registreeritud tarnituna.

Kui laotöötaja on paigutamistöö lõpule viinud, salvestab ja jälitab süsteem tulemust, värskendades mitut üksust, nagu on kirjeldatud järgmises tabelis.

| Üksus | Värskendused | Paberraha |
|---|---|---|
| Laadi | <p>Värskendatakse järgmised väljad.</p><ul><li>Väärtus <b>Koorma olek</b> on muudetud väärtuseks <i>Pooleli</i>.</li><li>Väärtus <b>Töö olek</b> on muudetud väärtuseks <i>Töö on 100% valmis</i>.</li></ul> | Väärtus **Koorma olek** on muudetud väärtuseks _Pooleli_, kui töötaja alustab paigutamistoimingut vähemalt ühe paigutamistöö rea jaoks. |
| Nende tööde laokanded, mille jaoks seotud kogused on ladustatud | Väljad **Sissetulek** ja **Asukoht** ning muud asjakohased väljad värskendatakse, et kajastada liikumist vastuvõtvast asukohast salvestuskohta. | Ostutellimuse varude kande sätte **Sissetuleku olek** väärtuseks jääb _Registreeritud_. |
| Lao ladustamine | Väärtus **Töö olek** on muudetud väärtuseks _Suletud_. | |

## <a name="post-registered-product-quantities-against-purchase-orders"></a><a name="post-registered-quantities"></a>Registreeritud toote koguste sisestamine ostutellimuste kohta

Pärast seda, kui sissetulevad tootekogused on süsteemis registreeritud, muutuvad need reserveerimiseks kättesaadavaks seoses müügi ning muude väljamineku ja sissetuleku toimingutega. Kuid süsteem ei uuenda veel varude (vahepealseid) kontosid. Värskendamine saab toimuda ainult siis, kui operatsioonimeeskond sisestab registreeritud toote sissetulekud.

Selleks et avada leht, kus saab sisestada toote sissetuleku, saavad operatsioonimeeskonna liikmed järgida _ühte_ järgmistest juhistest.

- Avage asjakohane koorma kirje ja seejärel valige tegevus **Toote sissetulek**.
- Avage **Laohaldus \> Perioodilised ülesanded \> Toote sissetulekute värskendamine** ja seejärel määrake väljal **Koorma ID** sisestatav koorem.
- Avage asjakohane ostutellimus ja seejärel valige tegevus **Toote sissetulek**.
- Avage **Hanked \> Ostutellimused \> Toodete vastuvõtmine \> Toote sissetuleku töö sisestamine**.

Lehel **Koorem** (ja värskendustöö samaväärsel lehel **Toote sissetulekute värskendamine**) saadaolev toiming **Toote sissetulek** saab uuendada toote sissetulekute koguseid ainult ostutellimuse koguste korral, mille olek on _Registreeritud_. Tegevus **Toote sissetulek**, mis on saadaval lehel **Ostutellimus**, võib sisaldada koguseid töötlemise mõlemas olekus (_Tellitud_ ja _Registreeritud_). Samuti saab see kontrollida toote sissetuleku sisestamise ulatust lisaparameetrite (nt _Kohe tarnitav kogus_ ja _Registreeritud kogus ja teenused_) abil.

Sisestada võib ainult toote olekuga _Kinnitatud_ tellimused. Kinnitamata ostutellimuste korral kuvatakse tegevus **Toote sissetulek** mittesaadavana.

### <a name="post-registered-quantities-from-the-load-page"></a>Registreeritud koguste sisestaminee lehelt Koorem

Toote registreeritud koguste sisestamiseks lehelt **Koorem** peab olema täidetud järgmised eeltingimused.

- Koormal peab olema vähemalt üks koguse üksus, mille olek on _Registreeritud_.
- Koorma olek peab olema _Välja saadetud_.
- Koormaga seotud ostutellimuse olek peab olema _Kinnitatud_.

> [!NOTE]
> Kui koorma olekuks pole seatud _Välja saadetud_, kinnitab süsteem koorma automaatselt enne toote sissetuleku värskendamist. (Koorma olekuks seatakse _Välja saadetud_, kui kasutaja registreerib koorma sissetuleva saadetise.)

Valitud koormaga seotud toote saabumise registreerimiste sisestamiseks valib töötaja tegevuse **Toote sissetulek** lehel **Koorem**. Avatud lehel on järgmised põhiandmed.

- Vahekaardi **Sätted** jaotise **Parameetrid** väli **Kogus** kuvab _registreeritud koguse_. Muud valikud pole siin saadaval.
- Kiirkaardi **Ülevaade** ruudustikus on loetletud kõik ostutellimused, mis on kaasatud valitud koormasse.
- Kiirkaardi **Read** ruudustikus on loetletud kõik tellimuse read, millel on registreeritud kogus.

> [!NOTE]
> Vahekaardil **Rida** kuvatavate tellimuse ridade kogused arvutatakse erinevalt, olenevalt sellest, kas funktsioon _Mitme toote sissetuleku lubamine koorma kohta_ on saadaval ja teie Supply Chain Managementi versioonis sisse lülitatud.
>
> | Versioon | Kalkulatsioon |
> |---|---|
> | Versioonid enne versiooni 10.0.10 ja uuemad versioonid, mille korral pole funktsioon _Mitme toote sissetuleku lubamine koorma kohta_ sisse lülitatud | Rea kogus on _selle ostutellimuse rea_ kõigi registreeritud koguste kogusumma, olenemata sellest, kas korraga registreeriti mitu koormat koormast, mobiilsest seadmest või kliendist sõltumatult. |
> | Versioon 10.0.10 ja uuemad versioonid, mille korral on funktsioon _Mitme toote sissetuleku lubamine koorma kohta_ sisse lülitatud | Rea kogus on _koorma kirje_ kõigi registreeritud koguste kogusumma, millelt tegevus **Toote sissetuleku sisestamine** käivitati. |

Kui kasutaja teeb toote sissetuleku sisestamise kinnitamiseks valiku **OK**, teeb süsteem järgmised olulised värskendused vastavatel üksustel.

| Üksus | Värskendused |
|---|---|
| Selle ostutellimuse varude kanne, mille rea kogused on sisestamise ulatusse kaasatud | <p>Järgmised väljad on värskendatud (kuid arvestage, et on ka mitu muud värskendust).</p><ul><li>Välja <b>Sissetulek</b> väärtuseks on seatud <i>Vastuvõetud</i>.</li><li>Välja <b>Füüsiline kuupäev</b> värskendatakse sisestamise kuupäevaga.</li></ul> |
| Koorem, mille kohta kasutaja sisestas toote sissetuleku | Koormate värskendused sõltuvad kasutatavast versioonist ja välja **Mitme toote sissetuleku lubamine koorma kohta** sättest. Reegleid kirjeldatakse tabelis, mis kuvatakse selles jaotises hiljem. |

Väli **Mitme toote sissetuleku lubamine koorma kohta** võimaldab ettevõtetel valida sissetuleva koorma vastuvõtmise poliitika. Sõltuvalt oma toimingu voogudest saavad ettevõtted valida, kas lubavad toote sissetuleku mitut sisestamist või keelavad need sama koorma korral. Soovitame logistikul seada väljale **Mitme toote sissetuleku lubamine koorma kohta** ühe järgmistest väärtustest.

- **Ei** – valige see väärtus, kui vastuvõtuametnik registreerib alati kõik tellimuse kogused, mis saabuvad iga koormaga määratud ajavahemiku jooksul. Kui mis tahes koorma koguseid ei registreerita, eeldab süsteem, et need ei jõudnud kohale või ei olnud koormas ning seetõttu ei peeta neid koorma osaks. Koormaga seotud toote sissetuleku sisestamine kasutab sama eeldust. Lisaks toote kõigi registreeritud koguste sissetuleku värskendamisele (põhifunktsioon) märgib see koormaga seotud toimingud lõpetatuks ja koorma täiendavaks töötlemiseks suletuks. Sel juhul värskendatakse kõik koorma rea kogused automaatselt registreeritud kogustele, kõik ilma registreeritud koguseta koorma read kustutatakse ja koorma olekuks määratakse _Vastuvõetud_.
- **Jah** – valige see väärtus, kui vastuvõtuametnikud vajavad saabunud koorma kõigi koguste registreerimiseks rohkem aega, kuid vahepeal peate sisestama toote juba registreeritud kogused. Sel juhul soovib logistik hoida koorma avatuna ka pärast toote sissetuleku sisestamistöö käivitamist, nii et ülejäänud koorma koguseid saab pearaamatusse pidevalt sisestada ja värskendada.
- **Viip** – valige see väärtus, kui kasutate mitut erinevat koorma vastuvõtutegevust, ja valite sobiva tegevuse iga kord, kui toote sissetuleku sisestamine algab.

Järgmine tabel võtab kokku sätte **Mitme toote sissetuleku lubamine koorma kohta** mõju.

| Mitme toote sissetuleku lubamine koorma kohta | Koorma kogus | Koorma olek | Paberraha |
|---|---|---|---|
| Kui see väli ei ole saadaval (versioonist 10.0.10 vanemad versioonid) | <p>Koorma kogus seatakse nii, et see võrdub registreeritud kogusega.</p><p>Kui koorma kogus on uuendatud väärtusele 0 (null), mis tähendab, et registreeringut pole ja koorma rida kustutatakse.</p><p>Kui koorma kohta pole koorma ridu, siis koorem kustutatakse.</p> | _Vastuvõetud_ | Kui tellimuse rea registreeritud koguse kohta on mitu koormat, värskendatakse ainult selle koorma olek, mille kohta sissetulek sisestati, väärtusele _Vastuvõetud_. |
| Ei | <p>Koorma kogus on seatud nii, et see vastab registreeritud kogusele, mis on seotud koorma ID-ga.</p><p>Kui varude kande jaoks pole salvestatud koorma ID-d, ühtib käitumine versioonist 10.0.10 varasemate versioonide käitumisega.</p> | _Vastuvõetud_ | |
| Jah | Uuendusi pole | _Vastuvõetud_, kui registreeritud koorma lõplik kogus on võrdne koorma kogusega või sellest suurem | |
| Jah | Uuendusi pole | _Välja saadetud_ või _Pooleli_, kui registreeritud koorma lõplik kogus on koorma kogusest väiksem | |

Kui välja **Koorma olek** väärtuseks on seatud _Vastuvõetud_, ei saa selle koorma kohta enam toote sissetuleku sisestusi teha. Töötaja saab siiski registreerida järelejäänud tellimuse koguse vastuvõetud koorma järgi järgmistel tingimustel. (Lisateavet vaadake selle teema varasemast jaotisest [Planeeritust suurema koorma vastuvõtt](#load-over-receiving).)

- Supply Chain Managementi versioon on vanem kui versiooni 10.0.11.
- Funktsioon _Koorma oodatust suurem sissetulek_ on sisse lülitatud ja koorma üksuse vastuvõtutoimingu mobiilse seadme menüükäsu välja **Koorma rea koguse oodatust suurem sissetulek** väärtuseks on seatud _Luba_.

Selleks et sisestada toote registreeritud koorma täiendavaid koguseid selle koorma järgi, mille olek on _Vastuvõetud_, peab kasutaja käivitama sisestamistoimingu seostuvast ostutellimusest.

### <a name="post-registered-quantities-from-the-purchase-order-page"></a>Registreeritud koguste sisestaminee lehelt Ostutellimus

Toote registreeritud koguste sisestamiseks lehelt **Ostutellimus**, täidab kasutaja järgmised ülesanded enne tegevuse **Toote sissetulek** valimist.

- Seadke vahekaardi **Sätted** jaotise **Parameetrid** välja **Kogus** väärtuseks _Registreeritud kogus_.
- Sisestage väljale **Toote sissetulek** sisestamisse kaasatud ostutellimuste numbrid.

> [!NOTE]
> Sisestamise ulatusse kaasatud rea kogus on tellimuse rea kõigi registreeritud koguste kogusumma, olenemata sellest, kas korraga registreeriti mitu koormat koormast, mobiilsest seadmest või kliendist sõltumatult. Sama reegel kehtib siis, kui koormaga seotud toote sissetuleku sisestamistegevus käivitatakse koormast, kui see on tehtud seal, kus väli **Mitme toote sissetuleku lubamine koorma kohta** pole saadaval või pole lubatud.

Kui kasutaja teeb toote sissetuleku sisestamise kinnitamiseks valiku **OK**, teeb süsteem järgmised olulised värskendused vastavatel üksustel.

| Üksus | Värskendused |
|---|---|
| Selle ostutellimuse varude kanne, mille rea kogused on sisestamise ulatusse kaasatud | <p>Järgmised väljad on värskendatud (kuid arvestage, et on ka mitu muud värskendust).</p><ul><li>Välja <b>Sissetulek</b> väärtuseks on seatud <i>Vastuvõetud</i>.</li><li>Välja <b>Füüsiline kuupäev</b> värskendatakse toote sissetuleku sisestamistegevuse kuupäevaga.</li></ul> |
| Laadi | Koormate värskendused sõltuvad sellest, kas väli **Mitme toote sissetuleku lubamine koorma kohta** on saadaval ja lubatud. Reegleid kirjeldatakse järgmises tabelis. |

Järgmine tabel võtab kokku sätte **Mitme toote sissetuleku lubamine koorma kohta** mõju.

| Mitme toote sissetuleku lubamine koormuse kohta | Koorma kogus | Koorma olek | Paberraha |
|---|---|---|---|
| Kui see väli on keelatud või see pole saadaval (versioonist 10.0.10 varasemates versioonides) | Uuendusi pole | Pole värskendatud. (Oleku väärtuseks jääb _Avatud_, _Välja saadetud_ või _Pooleli_.) | Kuna toote sissetuleku sisestamine algatatakse ostutellimuselt, pole värskendamisloogikal teavet selle rakendusala registreeritud koguste ja koormate, mille järgi registreering salvestati, vahelise seose kohta. Seetõttu ei saa valida koormat oleku värskendamiseks. |
| Lubatud | Uuendusi pole | <p>Aset leiab üks järgmistest toimingutest.</p><ul><li>Olekuks seatakse <i>Vastuvõetud</i>, kui ostutellimuse varude kannete kogu saadud ja ostetud kogus on suurem kui nendega seotud koorma kogus või sellega võrdne.</li><li>Oleku väärtuseks jääb <i>Avatud</i>, <i>Välja saadetud</i> või <i>Pooleli</i>, kui eelmine tingimus pole koorma kõigi ridade korral täidetud.</li></ul> | |

### <a name="select-the-appropriate-product-receipt-posting-option-for-your-logistics-operations"></a>Valige oma logistikatoimingute jaoks sobiv toote sissetuleku sisestamise suvand

Nagu eelnevalt kirjeldatud, pakub süsteem kahte toote sissetuleku sisestamise valikut. Valikutele pääseb juurde järgmistest kohtadest.

- Lehelt **Koorem** või menüüst **Laohaldus \> Perioodilised ülesanded** värskendustööna
- Lehelt **Ostutellimus** või menüüst **Hanked \> Ostutellimused \> Toodete saamine** värskendustööna

Ettevõtetel, mis kasutavad koormaid oma sissetulevate tellimuste transpordi- ja laohalduse planeerimiseks ja haldamiseks, soovitatakse kasutada järgmisi funktsioone, mis on ette nähtud järgmiste koormatega töötamiseks.

- **Vastuvõetava koormas oleva kauba** tegevused oma lao mobiilsetes seadmetes, et registreerida toote koguse saabumine koorma järgi
- **Toote sissetuleku sisestamise** tegevused, mis käivitatakse koormalt, et uuendada lao pearaamat

> [!NOTE]
> Vastavate sissetulevate tööprotsesside toetamiseks saab kasutada muid koguse registreerimise ja toote sissetuleku sisestamise funktsioone. Kui kasutate neid vaheldumisi konkreetsete koormapõhiste funktsioonidega või nende asemel, võite seada ohtu koorma kirjete andmetäpsuse ja seega koormahalduse voogude sujuvuse.

## <a name="example-scenarios"></a>Näidisstsenaariumid

### <a name="prepare-your-system-to-run-the-sample-scenarios"></a>Valmistage süsteem ette, et kasutada näidisstsenaariume

Selles jaotises kirjeldatud näidisstsenaariumide kasutamiseks peate esmalt veenduma, et kõik vajalikud funktsioonid on teie süsteemis sisse lülitatud. Nõutavad demo andmed peavad samuti süsteemis saadaval olema.

#### <a name="turn-on-the-required-features"></a>Nõutavate funktsioonide sisselülitamine

Need stsenaariumid nõuavad funktsiooni _Mitme toote sissetuleku sisestamine ühe koorma kohta_ ja selle eeltingimuse funktsiooni. Administraatorid saavad need funktsioonid sisse lülitada, järgides järgmisi etappe.

1. Avage tööruum **Funktsioonihaldus**. (Täielikku teavet selle tööruumi leidmise ja kasutamise kohta vt teemast [Funktsioonihalduse ülevaade](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)

1. Lülitage sisse funktsioon _Ostutellimuse varude kannete seostamine koormaga_, mis on loetletud järgmiselt.

    - **Moodul:** _laohaldus_
    - **Funktsiooni nimi:** _ostutellimuse varude kannete seostamine koormaga_

1. Lülitage sisse funktsioon _Mitme toote sissetuleku sisestamine ühe koorma kohta_, mis on loetletud järgmisel viisil.

    - **Moodul:** _laohaldus_
    - **Funktsiooni nimi:** _Mitme toote sissetuleku sisestamine ühe koorma kohta_

#### <a name="enable-sample-data"></a>Luba näidisandmed

Nende stsenaariumide kasutamiseks määratud näidiskirjete ja -väärtuste abil peate kasutama süsteemi, kuhu on installitud standardsed demoandmed. Enne alustamist peate valima ka **USMF-i** juriidilise isiku.

#### <a name="add-a-menu-item-for-receiving-load-items-when-a-mobile-device-is-used"></a>Lisage menüükäsk koorma üksuste vastuvõtmiseks mobiilse seadme kasutamisel

Enne kui lao vastuvõtuametnikud saavad koormaga seotud sissetulevate varude registreerimiseks kasutada mobiilset seadet, peate selleks looma mobiilse seadme menüükäsu.

Selles jaotises loote mobiilse seadme menüükäsu ja lisate selle olemasolevasse menüüsse. Laotöötaja saab seejärel valida menüükäsu laorakenduses.

1. Avage **Laohaldus \> Seadistamine \> Mobiilne seade \> Mobiilse seadme menüükäsud** ja veenduge, et teie mobiilse seadme menüü sisaldab menüükäsku, millel on järgmised sätted.

    - **Režiim:** _töö_
    - **Töö loomise protsess:**_vastuvõetav koormas olev kaup_
    - **Loo litsentsiplaat:** _jah_

    Saate jätta kõik muud sätted nende vaikeväärtustele.

    ![Mobiilse seadme menüükäsu sätted](media/inbound-mobile-menu-items.png "Mobiilse seadme menüükäsu sätted")

    Lisateavet mobiilse seadme menüükäskude seadistamise kohta vt teemast [Mobiilsete seadmete seadistamine laotöö jaoks](configure-mobile-devices-warehouse.md).

2. Kui olete menüükäsu seadistamise lõpetanud, avage **Laohaldus \> Seadistamine \> Mobiilne seade \> Mobiilse seadme menüü** ja lisage see oma mobiilsete seadmete menüüstruktuuri.

### <a name="example-scenario-1-register-a-load-where-some-items-are-missing"></a>1. näidisstsenaarium: registreerige koorem, milles mõni üksus on puudu

See stsenaarium näitab, kuidas registreerida koguseid sissetuleva koorma jaoks, kui kõiki oodatud koguseid ei ole olemas. Seejärel kuvatakse, kuidas sisestada ostutellimusele toote sissetulekut.

#### <a name="create-a-load-to-plan-receipt-of-a-purchase-order"></a>Looge koorem ostutellimuse sissetuleku plaanimiseks

Selles protseduuri käigus loote ostutellimuse ja seotud koorma käsitsi. Seejärel värskendage koormat simuleerimaks, et see on saadetud hankijalt (see värskendab koorma olekut). Laoplaanijad saavad seejärel filtreerida koormaid **Koorma oleku** järgi, et leida eeldatavaid sissetulevaid koormaid.

1. Avage **Hanked \> Ostutellimused \> Kõik ostutellimused**.
1. Valige suvand **Uus**.
1. Seadistage dialoogiboksis **Loo ostutellimus** välja **Hankija konto** väärtuseks _1001_.
1. Tehke dialoogiboksi sulgemiseks valik **OK** ja looge ostutellimus.
1. Uus ostutellimus sisaldab juba rida jaotises **Ostutellimuse read**. Seadke selle rea jaoks järgmised väärtused.

    - **Kauba kood:** _A0001_
    - **Ladu:** _24_
    - **Kogus:** _10_

1. Tehke toimingupaani vahekaardil **Ostmine** valikud **Tegevused \> Kinnita**. Tellimuse olek on nüüd _Kinnitatud_.
1. Tehke toimingupaani vahekaardil **Ladu** valikud **Tegevused \> Koorma planeerimise töölaud**.
1. Tehke lehe **Koorma planeerimise töölaud** tegumiriba vahekaardil **Pakkumine ja nõudlus** valikud **Lisa \> Uude koormasse**.
1. Seadke dialoogiboksis **Koorma malli määramine** välja **Koorma malli ID** väärtuseks _20' konteiner_.
1. Tehke dialoogiboksi sulgemiseks valik **OK** ja liikuge tagasi töölauale.
1. Äsja loodud koorma avamiseks tehke jaotises **Koormad** valik **Koorma ID**.
1. Vaadake üle koorma päise ja rea üksikasjad ning võtke arvesse järgmisi punkte.

    - Kiirkaardil **Koorem** on välja **Koorma olek** väärtuseks seatud _Avatud_.
    - Jaotises **Koorma read** on üks rida, millel on välja **Kogus** väärtuseks seatud _10_ ja välja **Töö loodud kogus** väärtuseks on seatud _0_ (null).

    ![Koormuse üksikasjad](media/inbound-load-details.png "Koormuse üksikasjad")

1. Tehke tegumiriba vahekaardil **Läheta ja võta vastu** valikud **Kinnita \> Sissetulev saadetis**. Pange tähele, et sätte **Koorma olek** väärtus on muutunud väärtuseks _Välja saadetud_.
1. Tehke märge **Koorma ID** väärtuse kohta, et saaksite seda järgmises protseduuris kasutada.

#### <a name="register-receipt-of-the-quantities-that-arrived-on-the-load"></a>Saabunud koorma koguste sissetulekute registreerimine

Kui koorem saabub vastuvõtvasse lattu, registreerib vastuvõttev ametnik koorma kogused mobiilse seadme abil.

1. Lattu 24 sisselogimiseks kasutage oma mobiilset seadet. (Standardsete demoandmete korral logige sisse, kasutades kasutaja ID-na nr _24_ ja paroolina nr _1_.)
1. Valige selle stsenaariumi jaoks loodud menüükäsk _Vastuvõetav koormas olev kaup_.
1. Järgmiste väärtuste sisestamiseks järgige ekraanil kuvatavaid andmesisestuse juhiseid. (Tellimus võib varieeruda, sõltuvalt kasutatavast mobiilsest seadmest või emulaatorist.)

    - **Koorem** – sisestage eelmises protseduuris loodud koorma ID.
    - **Kaup** – sisestage väärtus _A0001_, mis on selle koorma korral oodatav kaup.
    - **Kogus** – sisestage koormal oleva tegeliku kogusena nr _9_. Võtke arvesse, et see kogus on eeldatavast kogusest väiksem.

1. Jätkake töövoo läbimist, jättes kõik muud väljad tühjaks või määrates nende vaikeväärtused, kuni seade teavitab teid töö lõpule viimisest.

Koorma vastuvõtmise ülesanne on nüüd lõpule viidud ja vastuvõtuametnik saab liikuda järgmise ülesande juurde. Kui lao vastuvõtupersonal vaatab koorma kirje üle, selgub, et vastuvõetud kogus oli oodatust väiksem. Seejärel sooritavad nad järgmise protseduuri veebikliendi abil.

1. Avage **Laohaldus \> Koormad \> Kõik koormad**.
1. Leidke loendist äsja vastu võetud koorem. (Võimalik, et peate märkima ruudu **Kuva suletud**, et kaasata sissetulevad koormad, mille koorma olek on _Välja saadetud_.) Seejärel valige koorma avamiseks veerus **Koorma ID** asuv link.
1. Pange tähele, et koorma kirje sätte **Koorma olek** väärtuseks jääb endiselt _Välja saadetud_, kuid koorma rea sätte **Töö loodud kogus** väärtus on muutunud väärtuseks _9_.
1. Avage **Hanked \> Ostutellimused \> Kõik ostutellimused**.
1. Leidke loendist äsja vastu võetud ost ja valige tellimuse avamiseks veerus **Ostutellimus** asuv link.
\
1. Tehke kiirkaardil **Ostutellimuse read** valikud **Varud \> Kuvamine \> Kanded**.
1. Vaadake üle kahe ostutellimuse kande üksikasjad. (Võimalik, et välja **Koorma ID** ruudustikus kuvamiseks peate isikupärastama lehe **Varude kanded**.) Peaksite nägema kahte kannet.

    - Kanne, mille sissetuleku olek on _Registreeritud_, tähistab registreerimiskogust _9_, mida käitati mobiilses seadmes kindla koorma järgi. **Koorma ID** on seotud kõnealuse kandega.
    - Kanne, mille sissetuleku olek on _Tellitud_, tähistab järelejäänud registreerimata tellimuse rea kogust _1_.

#### <a name="product-receiptpost-the-registered-load-quantities-against-purchase-orders"></a>Toote registreeritud koguste sisestamine ostutellimuste järgi

Selles toimingus sisestate toote varud, mille registreerisite koorma jaoks. Selle tulemusena lisatakse saadud varud ja sellega seotud kulud ettevõtte pearaamatusse.

1. Avage **Laohaldus \> Koormad \> Kõik koormad**.
1. Leidke loendist vastu võetud koorem. (Võimalik, et peate märkima ruudu **Kuva suletud**, et kaasata sissetulevad koormad, mille koorma olek on _Välja saadetud_.) Seejärel valige koorma avamiseks veerus **Koorma ID** asuv link.
1. Tehke tegumiriba vahekaardil **Läheta ja võta vastu** valikud **Võta vastu \> Toote sissetulek**. Kui teil palutakse tegevus kinnitada, klõpsake valikut **Jah**.
1. Kontrollige ruudustikku dialoogiboksi **Toote sissetuleku sisestamine** kiirkaardil **Read**. Peaksite nägema ostutellimuse rida, mille jaoks kogus on registreeritud valitud koorma järgi.

    > [!NOTE]
    > Versioonides, kus funktsioon _Mitme toote sissetuleku sisestamine ühe koorma kohta_ pole saadaval või pole lubatud, kuvatakse ruudustikus **Koorma read** vaikimisi kogusena lõplik kogus, mis on registreeritud kõigi ostutellimuse reaga seotud koormate kohta.

1. Kontrollige kiirkaardi **Ülevaade** ruudustikus välja **Toote sissetulek**. Pange tähele, et selleks tuleb seada number, mis sisaldab valitud koorma ID-d.
1. Toote sissetuleku sisestamiseks valige **OK** ja sulgege dialoogiboks **Toote sissetuleku sisestamine**.
1. Olete naasnud koorma üksikasjade vaatesse. Pidage meeles järgmiseid punkte.

    - Välja **Koorma olek** väärtuseks on nüüd seatud _Vastuvõetud_.
    - Koorma real on koorma välja **Kogus** väärtus muutunud väärtuseks _9_ varasema väärtuse _10_ asemel, et see vastaks registreeritud kogusele, kuid välja **Töö loodud kogus** väärtuseks jääb _9_.

Kui ostumeeskond ei eelda, et hankija tarnib järelejäänud tellimuse koguse 1, saab ta tellimuse sulgeda, värskendades rea tarnejäägi väärtusele _0_. Kui aga peagi selgub, et puuduv kaup saabus esimese koormaga, saavad laotöötajad teha ühe järgmistest toimingutest.

- Registreerige kogus sama koorma järgi. Sel juhul lähtestatakse väli **Koorma olek** väärtusele _Välja saadetud_ ja välja **Töö loodud kogus** väärtust värskendatakse väärtuseks _10_. See valik on saadaval ainult järgmistes olukordades.

    - Funktsioon _Koorma rea koguse oodatust suurem sissetulek_ ei ole saadaval või pole lubatud.
    - Funktsioon _Koorma oodatust suurem sissetulek_ on saadaval ja lubatud ning välja **Koorma rea koguse oodatust suurem sissetulek** väärtuseks on seatud _Luba_.

- Lisage kogus uuele või olemasolevale koormale ja töödelge seda tavalisel viisil.
- Registreerige ja/või võtke kogus vastu viisil, mis ei hõlma koorma käsitlemist.

### <a name="example-scenario-2-register-quantities-that-arrive-on-multiple-inbound-loads-where-some-items-are-missing"></a>2. näidisstsenaarium: registreerige kogused, mis saabuvad mitme sissetuleva koormaga, kust mõni kaup puudub

Selle stsenaariumi korral jagatakse ühe ostutellimuse reaga seotud sissetulev saadetis kaheks koormaks. Näiteks võib ostutellimuse rida jagada mitmeks koormaks, kuna koorma füüsiline kaal ja/või maht on piiratud.

See stsenaarium näitab ka, kuidas töödelda mitut toote sissetuleku sisestust sama koorma korral. Registreerite kogused, mis saabuvad mitme sissetuleva koormaga, kuid kogused ei vasta oodatud kogustele. Kulu värskendatakse toote sissetulekut sisestades sama koorma korral mitu korda.

#### <a name="set-up-load-receiving-policies"></a>Koorma vastuvõtmise poliitikate seadistamine

Selles protseduuris lubate mitu toote sissetuleku sisestust samast koorma korral.

1. Avage **Laohaldus \> Seadistus \> Laohalduse parameetrid**.
1. Seadke vahekaardil **Koormad** välja **Mitme toote sissetuleku lubamine koorma kohta** väärtuseks _Jah_.

#### <a name="create-two-loads-to-plan-receipt-of-a-purchase-order"></a>Looge kaks koormat ostutellimuse sissetuleku plaanimiseks

Selles protseduuri käigus loote ostutellimuse ja kaks koormat. Seejärel värskendage igat koormat käsitsi simuleerimaks, et see on saadetud hankijalt (see värskendab koorma olekut). Laoplaanijad saavad seejärel filtreerida koormaid **Koorma oleku** järgi, et leida eeldatavaid sissetulevaid koormaid.

Samuti saate teada, kuidas seada ostutellimuse rida nii, et saate vastu võtta koguse, mis on 20 protsenti suurem kui rea jaoks määratud kogus.

1. Avage **Hanked \> Ostutellimused \> Kõik ostutellimused**.
1. Valige suvand **Uus**.
1. Määrake kiirkaardil **Hankija** välja **Hankija konto** väärtuseks _1001_ ja seejärel valige **OK**.
1. Teie uus ostutellimus avatakse ja see sisaldab tühja rida ruudustikus **Ostutellimuse read**. Seadke selle tellimuse rea jaoks järgmised väärtused.

    - **Kauba kood:** _A0001_
    - **Ladu:** _24_
    - **Kogus:** _10_

1. Määrake kiirkaardi **Rea üksikasjad** vahekaardil **Tarne** välja **Ületarne** väärtuseks _20_.
1. Tehke toimingupaani vahekaardil **Ostmine** valikud **Tegevused \> Kinnita**. Tellimuse olek on nüüd _Kinnitatud_.
1. Tehke toimingupaani vahekaardil **Ladu** valikud **Tegevused \> Koorma planeerimise töölaud**.
1. Tehke lehe **Koorma planeerimise töölaud** tegumiriba vahekaardil **Pakkumine ja nõudlus** valikud **Lisa \> Uude koormasse**.
1. Seadke dialoogiboksis **Koorma malli määramine** välja **Koorma malli ID** väärtuseks _20' konteiner_. Muutke vahekaardil **Üksikasjad** välja **Kogus** väärtuseks  _5_ kuni _10_, et osaliselt lisada ostutellimuse rea kogus.
1. Valige **OK**, et rakendada oma sätted ja sulgeda dialoogiboks.
1. Teise koorma loomiseks korrake samme 8–10. Seekord peaks välja **Kogus** väärtus _5_ olema juba seatud.
1. Valige lehe **Koorma planeerimise töölaud** ruudustikus **Koormad** välja **Koorma ID** väärtus esimese loodud koorma jaoks. Kuvatakse leht **Koorma üksikasjad** ja valitud koorem. Tehke järgmist.

    1. Tehke tegumiriba vahekaardil **Läheta ja võta vastu** valikud **Kinnita \> Sissetulev saadetis**.
    1. Pange tähele, et sätte **Koorma olek** väärtus on muutunud väärtuseks _Välja saadetud_.
    1. Valige nupp Sule, et naasta lehele **Koorma planeerimise töölaud**.

1. Korrake eelmist sammu oma teise loodud koorma jaoks.
1. Märkige üles välja **Koorma ID** kaks väärtust, mis kuvatakse ruudustikus **Koormad**.

#### <a name="register-partial-receipt-of-the-quantities-that-arrived-on-the-first-load-and-post-the-registered-load-quantities"></a>Registreerige esimese koormaga saabunud koguste osaline sissetulek ja sisestage registreeritud koorma kogused

Kui koormad saabuvad vastuvõtvasse lattu, registreerib vastuvõttev ametnik koorma kogused mobiilse seadme abil. Koormaga seotud registreeritud varusid värskendatakse seejärel ettevõtte pearaamatus, sisestades ostutellimuse toote sissetuleku koorma järgi.

See protseduur näitab, kuidas vastuvõtuametnik registreerib koorma kogused mobiilses seadmes.

1. Lattu 24 sisselogimiseks kasutage oma mobiilset seadet. (Standardsete demoandmete korral logige sisse, kasutades kasutaja ID-na nr _24_ ja paroolina nr _1_.)
1. Valige selle stsenaariumi jaoks loodud menüükäsk _Vastuvõetav koormas olev kaup_.
1. Järgmiste väärtuste sisestamiseks järgige ekraanil kuvatavaid andmesisestuse juhiseid. (Tellimus võib varieeruda, sõltuvalt kasutatavast mobiilsest seadmest või emulaatorist.)

    - **Koorem** – sisestage eelmises protseduuris loodud esimese koorma ID.
    - **Kaup** – sisestage väärtus _A0001_, mis on selle koorma korral oodatav kaup.
    - **Kogus** – sisestage _3_. Võtke arvesse, et see kogus on eeldatavast kogusest väiksem. Selle stsenaariumi korral kujutage ette, et teil kui vastuvõtuametnikul ei ole aega registreerida kõiki koguseid selle koorma jaoks. Selle protseduuri käigus registreerite ülejäänud kogused hiljem, korrates seda juhist ja määrates välja **Kogus** väärtuseks _2_.

1. Jätkake töövoo läbimist, jättes kõik muud väljad tühjaks või määrates nende vaikeväärtused, kuni seade teavitab teid töö lõpule viimisest.
1. Tehke veebikliendis valikud **Laohaldus \> Koormad \> Kõik koormad**.
1. Leidke loendist äsja vastu võetud koorem ja valige koorma avamiseks väärtus **Koorma ID**. Pange tähele, et välja **Koorma olek** väärtuseks jääb endiselt _Välja saadetud_, kuid koorma rea sätte **Töö loodud kogus** väärtus on muutunud väärtuseks _3_.
1. Tehke tegumiriba vahekaardil **Läheta ja võta vastu** valikud **Võta vastu \> Toote sissetulek**. Kui teil palutakse tegevus kinnitada, klõpsake valikut **Jah**.
1. Vaadake dialoogiboksis **Toote sissetuleku sisestamine** kuvatavad väärtused üle, kuid ärge muutke neid ja valige seejärel **OK**.
1. Olete suunatud tagasi valitud koorma lehele **Koorma üksikasjad**. Pidage meeles järgmiseid punkte.

    - Välja **Koorma olek** väärtuseks jääb endiselt _Vastuvõetud_.
    - Koorma real jääb välja **Kogus** väärtuseks _5_, mis on algne koorma kogus, ja välja **Töö loodud kogus** väärtuseks jääb _3_.

1. Viige selle koorma järelejäänud koguse registreerimine lõpule, korrates seda protseduuri. Seadke 3. juhises välja **Kogus** väärtuseks _2_.

Esimese koorma vastuvõtmise ülesanne on nüüd lõpule viidud. Loodud on kaks toote sissetuleku töölehte, üks iga kahe teie käivitatud toote sissetuleku värskenduse kohta.

#### <a name="register-receipt-of-the-quantities-that-arrived-on-the-second-load-and-account-for-the-overdelivered-quantity"></a>Registreerige teise koormaga saabunud koguste sissetulek ja ületarne koguse konto

Selle stsenaariumi korral registreerib vastuvõtuametnik koguse, mis ületab koormas olevat kogust. Üleliigse koguse vastuvõtmine on lubatud, kuna süsteem on seadistatud lubama ületarnet.

1. Lattu 24 sisselogimiseks kasutage oma mobiilset seadet. (Standardsete demoandmete korral logige sisse, kasutades kasutaja ID-na nr _24_ ja paroolina nr _1_.)
1. Valige selle stsenaariumi jaoks loodud menüükäsk _Vastuvõetav koormas olev kaup_.
1. Järgmiste väärtuste sisestamiseks järgige ekraanil kuvatavaid andmesisestuse juhiseid. (Tellimus võib varieeruda, sõltuvalt kasutatavast mobiilsest seadmest või emulaatorist.)

    - **Koorem** – sisestage teise eelnevalt loodud koorma ID.
    - **Kaup** – sisestage väärtus _A0001_, mis on selle koorma korral oodatav kaup.
    - **Kogus** – sisestage väärtus _7_, mis on järelejäänud kogus, mille hankija saab tarnida osana kogu ostutellimuse kogusest 12 (milles 10 on algne tellimuse kogus ja 2 on 20 protsenti lubatud ületarne kogusest). Pidage meeles, et 5 tk on juba registreeritud esimese koorma järgi.

Teist koormat on nüüd värskendatud kogusele 7 ja toote sissetulekut võidakse värskendada selle koguse põhjal.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]