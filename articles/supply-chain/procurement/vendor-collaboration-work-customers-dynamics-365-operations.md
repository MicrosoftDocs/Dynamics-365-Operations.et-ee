---
title: Hankija koostöö klientidega
description: See artikkel kirjeldab, kuidas saate hankija koostöö abil töötada ostuühikutega ja jälgida veose varusid.
author: GalynaFedorova
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, ConsignmentVendorPortalOnHand, PurchVendorPortalConfirmedOrders, PurchVendorPortalOriginalOrder, PurchVendorPortalResponsesHistoryList, PurchVendorPortalResponsesPart, VendVendorProfileCard, PurchVendorPortalAllResponse, PurchVendorPortalPendingResponsesPart, PurchVendorPortalResponses, PurchVendorPortalConfirmedOpenOrdersPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221234
ms.assetid: 6e69fb8b-6d3a-46ef-88cf-6d01212aa7c3
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4e5748f2368376ee03f280f1487d1de65250d3a4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859165"
---
# <a name="vendor-collaboration-with-customers"></a>Hankija koostöö klientidega

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas saate hankija koostöö abil Microsofti klientidega töötada Dynamics 365 Supply Chain Management. Hankijad saavad äriprotsesse lõpule viia järgmistes tööruumides.

- **Ostutellimuse kinnitus** – ostutellimuste (OT-de) jälgimine ja neile vastamine.
- **Hankija pakkumine** – pakkumiskutsete vaatamine ja neile reageerimine pakkumisi sisestades.
- **Hankija teave** – hankija koondandmete vaatamine ja värskendamine.
- **Arve koostamine** – töötamine arvetega. See artikkel ei hõlma arvelduse **tööruumi**. Lisateabe saamiseks selle tööruumi kohta vaadake teemat [„Hankija koostöö arve tööruum”](../../finance/accounts-payable/vendor-portal-invoicing-workspace.md).

Hankijad saavad jälgida ka teavet veose varude kohta.

## <a name="working-with-pos-in-the-purchase-order-confirmation-workspace"></a>Töö OT-dega tööruumis Ostutellimuse kinnitus

Tööruum **Ostutellimuse kinnitus** võimaldab teil vastata ülevaatamiseks saadetud ostutellimustele (OT-dele). See võimaldab teil vaadata ka teavet OT-de kohta, mis ootavad kliendipoolset tegevust, ja selliste OT-de kohta, mis on kinnitatud, kuid ikka avatud.

Tööruumis **Ostutellimuse kinnitus** on kolm loendit.

- **Ülevaatamist ootavad ostutellimused** – see loend näitab teile saadetud OT-sid, millele oodatakse teie vastust. Pärast vastamist kaob ostutellimus loendist. Kui klient saadab teile OT uue versiooni enne, kui olete eelmisele vastanud, näidatakse ainult värskeimat versiooni.
- **Kliendi tegevuse ootel** – selles loendis kuvatakse kõik OT-d, millele olete vastanud, kuid mida klient pole veel kinnitanud. OT aktseptimisel saate seda jälgida selles loendis, kuni OT olekuks muudetakse **Kinnitatud**. Kui lükkate OT tagasi või aktseptite selle muudatustega, saate seda jälgida siin, kuni klient saadab uue versiooni.
- **Ava kinnitatud ostutellimused** – selles loendis kuvatakse kõiki teie konto OT-sid, mille olek on **Kinnitatud**. Kui tooted ja teenused on ostutellimuse suhtes täielikult vastu võetud, kaob ostutellimus loendis.

OT-dega töötamiseks saate kasutada järgmisi lehti.

- **Ülevaatamist ootavad ostutellimused** – see leht sisaldab sama teavet nagu loend **Ülevaatamist ootavad ostutellimused** tööruumis. Vt selle artikli varasemat kirjeldust.
- **Ostutellimuse hankija kinnitamise ajalugu** – see leht sisaldab kõiki OT-sid ja kõiki hankijale saadetud OT-de versioone. See sisaldab ka kõiki hankijalt saadud vastuseid.
- **Ava kinnitatud ostutellimused** – see leht sisaldab sama teavet nagu loend **Ava kinnitatud ostutellimus** tööruumis. Vt selle artikli varasemat kirjeldust.
- **Kõik kinnitatud ostutellimused** – see leht sisaldab kõiki kinnitatud OT-sid. Sellel lehel kuvatud OT-d hõlmavad ka saadud toodete või teenuste OT-sid. Saate kasutada seda loendit jälgimaks, milliste OT-de eest saate arveid saata.

### <a name="responding-to-pos"></a>OT-dele vastamine

Kliendi saadetud OT-d kuvatakse tööruumis **Ostutellimuse kinnitus** ja lehel **Ülevaatamist ootavad ostutellimused**. Pärast OT avamist saate selle aktseptida, tagasi lükata või aktseptida selle muudatustega. OT päises või üksikutel ridadel võib olla manuseid. Peale selle on teil võimalik lisada oma vastusele informatsiooni OT päisesse või üksikutele ridadele. Näiteks võite soovitada soovitada kauba asendamise ühele ridadest.

Saate eelvaadata ja printide ostutellimuse PDF-failina, kasutades suvandit **Kuva eelvaade / prindi**. Selliste dimensiooniveergude nagu **Tegevuskoht**, **Ladu**, **Värv**, **Suurus**, **Stiil** ja **Konfiguratsioon** peitmiseks või kuvamiseks saate kasutada ka tegevust **Dimensioonide kuvamine**. 

Kui kasutate suvandit **Aktsepteeri koos muudatustega**, saate üksikud read kinnitada või tagasi lükata. Samuti saate ridadele teha järgmised muudatused.

- Muutke kuupäevi või koguseid. Kinnitatud tarnekuupäeva värskendamiseks kõikidel ridadel kasutage OT päises olevat suvandit **Värskenda tarnekuupäeva**.
- Eri tarnekuupäevade ja -koguste jaoks saate ridu tükeldada.
- Asendage üksus. Sisestage jaotises **Rea üksikasjad** kauba kirjeldus ja kauba number väljale **Rea üksikasjad**.

Te ei saa muuta hinnateavet ega tasusid, kuid saate märkusi kasutades teha soovitusi nendele muudatuste tegemiseks.

Kui klient saadab teile OT uue versiooni, on sellel versiooni järelliide näitamaks, et see on varem saadetud OT muudetud versioon. Leht **Ostutellimuse hankija kinnitamise ajalugu** võimaldab teil jälgida iga tellimuse ajalugu.

## <a name="monitoring-consignment-inventory"></a>Veose varude jälgimine

Veose varude kasutamisel saate hankija koostööliidese kaudu vaadata teavet järgmistelt lehtedelt.

- **Ostutellimused, mis tarbivad veose varusid** – veose varude jaoks mõeldud OT-d luuakse siis, kui klient varude omandiõiguse üle võtab. Neid veose OT-d kuvatakse ainult sellel lehel. Neid ei leia lehelt **Kõik kinnitatud ostutellimused**.
- **Veose varudest saadud tooted** – sellel lehel on esitatud kõik kanded, kus toodete omandiõigus on ülekantud ettevõttele, mis tarbib varusid. Saate kasutada seda teavet, et kliendile arvet esitada.
- **Veose vaba kaubavaru** – see leht näitab vabu veose varusid, mille omanik on teie ettevõtte, kuid mis on klientide laos saadaval.

## <a name="working-with-rfqs-in-the-vendor-bidding-workspace"></a>Töö pakkumiskutsetega tööruumis Hankija pakkumine

Tööruum **Hankija pakkumine** võimaldab vaadata pakkumiskutseid, millele oodatakse teie ettevõte vastust. Samuti saate pakkumiskutsetele vastata.

Tööruumis kuvatakse ka kõik kaotatud või võidetud pakkumiskutsed. Kui süsteemi konfiguratsiooniks on avalik sektor, kuvatakse tööruumis ka avalikult kättesaadavad pakkumiskutsed.

### <a name="viewing-rfqs"></a>Pakkumiskutsete vaatamine

Alljärgnevale teabele juurdepääsemiseks avage tööruum **Hankija pakkumine**.

- Nägemaks pakkumiskutseid, millele oodatakse teie ettevõttelt vastust, valige **Uue pakkumise kutsed**. Siin saate pakkumiskutseid vaadata ja pakkumisprotsessi käivitada. Saate vaadata ka parandatud pakkumiskutseid, millele tuleb esitada uus pakkumine.
- Vaatamaks pakkumiskutseid, mille klient on teile tagasi saatnud, et saaksite pakkumisele täiendavat teavet lisada või pakkumist värskendada, valige **Tagastatud pakkumised**.
- Vaatamaks kõiki pakkumiskutseid, mille kallal teie või teie ettevõtte kontaktisik on töötanud, kuid mida pole veel esitatud, valige **Pooleliolevad pakkumised**.
- Vaatamaks pakkumisi, kus klient on vähemalt ühe rea teie pakkumises heaks kiitnud, valige **Võidetud pakkumised**.
- Vaatamaks pakkumisi, mille kõik read on tagasi lükatud, valige **Kaotatud pakkumised**.
- Nägemaks kõiki hankija pakkumiskutseid ja mis tahes esitatud pakkumisi, valige link **Pakkumiskutsed**. Lehel **Pakkumiskutsed** reastatakse kõik hankijaga seotud pakkumiskutsed. Saate otsida oleku järgi.
- Nägemaks loendit kõigist pakkumiskutsetest, mille puhul hankija kontaktisik on keeldunud pakkumise tegemisest, valige link **Tagasilükatud pakkumised**.

### <a name="working-with-rfqs-that-are-publicly-available"></a>Avalikult kättesaadavate pakkumiskutsetega töötamine

Avalikus sektoris töötavad inimesed näevad avatud ja aegunud pakkumiskutseid, mis on avalikult kättesaadavad.

- Avalikult kättesaadavaks tehtud avatud pakkumiskutsete vaatamiseks valige link **Avatud avaldatud pakkumiskutsed**. Avatud pakkumiskutse on praegu veel aegumata pakkumiskutse. Aegumiskuupäeva ja -kellaaja leiate pakkumiskutse päisest.

    Kui teid on kutsutud pakkumist esitama, leiate sama pakkumiskutse lehelt **Uue pakkumise kutsed**. Mõnikord võib ette tulla, et teile pole avatud pakkumiskutset saadetud, kuid soovite siiski pakkumise esitada. Sel juhul võib olla võimalik iseennast kutsuda, eeldusel et klient on selle pakkumiskutse puhul lubanud ise end kutsuda. 

    Uute **pakkumiste kutsete leht** võib pakkuda filtrit, mis võimaldab teil vaadata avatud pakkumiskutseid ja tuvastada ridu, mis sisaldavad teie kinnitatud hankekategooriatele vastanud ridu. Filtri kättesaadavaks miseks peate lülitama sisse funktsiooni *Luba hankijatel pakkumiskutseid otsida hankekategooria* funktsiooni alusel. Administraatorid saavad kasutada funktsioonihalduse **tööruumi**, et kontrollida selle funktsiooni olekut ja lülitada see sisse, kui seda on vaja. Seega on funktsioon loetletud järgmisel viisil.

    - **Moodul: Ostureskontro** *·*
    - **Funktsiooni nimi:** *lubage hankijatel pakkumiskutseid hankekategooria alusel otsida.* <!-- KFM: I don't see this here, is this right? -->

    Lingi Avatud avaldatud **pakkumiskutsed** *juurdepääsu parandamiseks saate lülitada sisse lingi Kuva "Avatud avaldatud pakkumiskutsed" paanifunktsioonina.* See funktsioon teisendab lingi paanile ja teisaldab selle väljapaistvasse asukohta, et oleks lihtne leida. Administraatorid saavad kasutada funktsioonihalduse **tööruumi**, et kontrollida selle funktsiooni olekut ja lülitada see sisse, kui seda on vaja. (Tarneahela halduse versiooni 10.0.21 puhul lülitatakse funktsioon vaikimisi sisse.) Seal on see funktsioon loetletud järgmisel viisil:

    - **Moodul:** *hanked*
    - **Funktsiooni nimi:** *kuva link "Avatud avaldatud pakkumiskutsed" paanina*

- Avalikult kättesaadavaks tehtud suletud pakkumiskutsete vaatamiseks valige link **Suletud avaldatud pakkumiskutsed**. Suletud pakkumiskutse on aegunud pakkumiskutse. Aegumiskuupäeva ja -kellaaja leiate pakkumiskutse päisest.

    Suletud pakkumiskutse näitab kõiki hankija pakkumisi kuni rea tasemeni. Teave pakkumiste valituks osutumise või tagasilükkamise kohta kajastub suletud pakkumiskutses. Kättesaadavad on ka kõik pakkumisele lisatud manused.

> [!NOTE]
> See funktsioon on saadaval ainult siis, kui avaliku sektori konfiguratsioon on sisse lülitatud.

### <a name="bidding"></a>Pakkumine

- Pakkumiskutsele vastamiseks valige suvand **Pakkumine**.

    Kui pakkumiskutse päistes ja ridades on pakkumiseväljade muutmine lubatud, saate oma pakkumise sisestada ruudustikku. Peate ka arvestama mis tahes täiendava teabega pakkumise kohta, mis tuleks lisada rea üksikasjadesse.

    Pakkumise loomisel ilmub see jaotisesse **Pooleliolevad pakkumised**.

    Pakkumist saate enne aegumiskuupäeva igal ajal salvestada. Seejärel võite hiljem naasta, et pakkumine lõpetada ja esitada. Pakkumise esitamise järel saate seda kuni aegumiskuupäevani tagasi kutsuda ja värskendada.

- Pakkumisse sisestatud andmete lähtestamiseks ja algse pakkumiskutse ennistamiseks valige **Pakkumiskutsest lähtestamine**. Saate lähtestada kas päise või rea.
- Ruudustikus alternatiividega töötamiseks valige **Lisa alternatiiv** või **Eemalda alternatiiv**.

    Mõne pakkumiskutse puhul on lubatud alternatiivsed pakkumised. Alternatiivseid pakkumisi saate määrata ainult **kategooria** tüüpi ridadele, kuna kindlaid kaupu ei saa alternatiividena lisada. 

- Avamaks mis tahes manust, mille klient on pakkumiskutsele lisanud, valige **Pakkumiskutse manus** või **Pakkumiskutse ridade manus**. Manuste üles laadimiseks koos pakkumisega valige **Pakkumise manused** või **Pakkumise rea manused**.

    Võib juhtuda, et peate enne pakkumise esitamist küsimustikule vastama.

- Kui te ei soovi pakkumist esitada, valige **Keeldu**. Kui olete valinud **Keeldu**, ei saa seda tegevust tagasi kutsuda ega pakkumist sisestada.

Kui pakkumiskutset on parandatud, peate sisestama uue pakkumise. Paranduste kohta leiate teavet pakkumiskutse lehe vahekaardilt **Parandused**. Parandatud pakkumiskutseid kuvatakse lehel **Uue pakkumise kutsed**.

## <a name="accessing-vendor-master-data-in-the-vendor-information-workspace"></a>Juurdepääs hankija koondandmetele tööruumis Hankija teave

Hankijana on teil juurdepääs osale teabest, mida klient säilitab hankija koondkirjes. Seetõttu saate teavet ajakohasena hoida. Teabe värskendamiseks peab teil olema hankija administraatori (väline) roll.

Juurdepääsetav teave on järgmine: hankija nimi; aadress; kontaktandmed; kontaktisikud ja nende kontaktteave; ID-numbrid; maksu registreerimisnumbrid; hankekategooriad, mille klient on hankija puhul kinnitanud, ja sertide teave.

## <a name="additional-resources"></a>Lisaressursid

[Hankija koostöö kasutajate haldamine](manage-vendor-collaboration-users.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
