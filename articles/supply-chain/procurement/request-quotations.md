---
title: Pakkumiskutsed
description: "Selles teemas antakse ülevaade pakkumiskutsete kohta. Organisatsioonid väljastavad pakkumiskutse, kui saavad mitmelt hankijalt konkureerivaid pakkumisi kaupade või teenuste kohta, mida soovivad osta."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 2154
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: b86363004b8702d1a654f2a1da49bba82fc8ff2a
ms.contentlocale: et-ee
ms.lasthandoff: 03/26/2018

---

# <a name="requests-for-quotation-rfqs"></a>Pakkumiskutsed

[!include[banner](../includes/banner.md)]

Selles teemas antakse ülevaade pakkumiskutsete kohta. Organisatsioonid väljastavad pakkumiskutse, kui saavad mitmelt hankijalt konkureerivaid pakkumisi kaupade või teenuste kohta, mida soovivad osta. Pakkumiskutses saate hankijatelt küsida teie määratud kaubakoguse hindu ja tarneaegu. Samuti saate hankijatelt küsida, kas on lisatasusid, nagu saatekulud, või allahindlusi suurte tellimuste või hankija arve ennetähtaegse maksmise korral.

Pakkumiskutse protsess koosneb järgmistest ülesannetest.

1. Pakkumiskutse loomine ja saatmine ühele või mitmele hankijale.
2. Pakkumiskutse vastuste (pakkumiste) vastuvõtmine ja registreerimine.
3. Aktsepteeritud pakkumiste ülekandmine ostutellimuseks, ostulepinguks või ostutaotluseks.

Järgmisel joonisel on näidatud ülevaade pakkumiskutse protsessist.

[![RFQ-protsess](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)

Saate luua pakkumiskutse plaanitud tellimustelt, ostutaotluselt või käsitsi sisestades. Teie loodud pakkumiskutset nimetatakse pakkumiskutse juhtumiks. Pakkumiskutse juhtum on alusdokument, mida kasutate igale hankijale pakkumiskutse väljastamiseks.

Kui olete pakkumiskutse ette valmistanud ja hankijad lisanud, valige pakkumiskutse juhtumis käsk **Saada**. Iga hankija kohta, kellele pakkumiskutse saadate, luuakse pakkumiskutse tööleht. Saate konfigureerida saatmistegevuse prindihaldussätteid kas printima iga hankija kohta aruande arhiivi või saatma aruande iga hankija meiliaadressile. Peale selle saate iga hankija pakkumiskutse töölehe abil luua aruande, mille saate hankijale saata kohe või hiljem uuesti. Samuti saate konfigureerida saatmistegevuse nii, et see loob vastuselehe, mille hankija saab täita.

Selles teemas käsitletakse pakkumiskutsete käsitlemise protsessi, kui hankija koostööd ei kasutata. Kui teie süsteem on seadistatud hankija koostöö kasutamiseks, saavad hankijad sisestada pakkumised otse rakendusse Microsoft Dynamics 365 for Finance and Operations. Lisateavet vaadake teemast [Hankija koostöö klientidega](vendor-collaboration-work-customers-dynamics-365-operations.md).
 
Kui peate pakkumiskutset pärast selle saatmist täiendama, saate valmis pakkumiskutse hankijatele uuesti saata, kasutades kaht täiendamistegevust: loomine ja lõpetamine.

Pakkumiste vastuvõtmisel meili teel peate sisestama need lehel **Pakkumiskutse vastused**. Kui valite suvandi **Kopeeri andmed vastuseväljadele**, kopeeritakse vastuseväljadele pakkumiskutse juhtumi andmed, nagu kogus ja kuupäevad. Saate neid andmeid muuta, et kajastada hankija pakkumist.

Kui hankija puhul on nõutav vastuse teine iteratsioon, valige lehel **Pakkumiskutse vastus** käsk **Tagasta**. Tagastustegevus loob uue töölehe ja aruande, mis prinditakse, arhiivitakse ja saadetakse teie prindihaldussätete järgi.

Kui olete lisanud pakkumiskutse juhtumile hindamiskriteeriumid, on pakkumiskutse vastusel hindamispaneel, kuhu saate punktisummad sisestada. Punktide kogusumma kuvatakse, kui võrdlete vastuseid lehel **Vastuste võrdlemine**. Sellel lehel saate ka võrrelda vastuse andmeid, nagu rea hind, tarnekuupäev ja koguhind.

Kui olete mõne pakkumise või osalise pakkumise välja valinud, saate selle aktsepteerida ja ülejäänud tagasi lükata. Luuakse aktsepteerimise ja tagasilükkamise töölehed ning vastavad aruanded, mis prinditakse, arhiivitakse ja saadetakse teie prindihaldussätete järgi. Kui aktsepteerite mõne pakkumise või pakkumise konkreetsed read, luuakse kas ostuleping või ostutellimus või värskendatakse ostutaotlust olenevalt pakkumiskutse ostutüübist. Saate luua kaubandusleppe, mida saate hiljem kasutada mis tahes vastuste puhul olenemata sellest, kas olete need aktsepteerinud või tagasi lükanud.

Pakkumiskutse olek kuvatakse pakkumiskutse päises ja see oleneb pakkumiskutse ridade olekust. Olek näitab, kui palju olete pakkumiskutset töödelnud. Igal pakkumiskutsel on kaks oleku väärtust: madalaim ja kõrgeim. Madalaim olek on pakkumiskutse ükskõik millise rea kõige vähemarenenum etapp ja kõrgeim olek on pakkumiskutse ükskõik millise rea kõige arenenum etapp. Näiteks kui pakkumiskutse kõige vähemarenenum etapp on loodud rea kohta, siis on pakkumiskutse madalaim olek **Loodud**. Kui pakkumiskutse kõige arenenum etapp on hankijatele saadetud rea kohta, siis on pakkumiskutse kõrgeim olek **Saadetud**. Pakkumiskutse töötlemisel värskendatakse olekuid automaatselt.

Saate pakkumiskutse päise madalaimaid ja kõrgeimaid olekuid vaadata lehel **Kõik pakkumiskutsed**. Saate pakkumiskutse rea madalaimaid ja kõrgeimaid olekuid vaadata lehe **Pakkumiskutsed** vahekaardil **Read**.

Pakkumiskutsete töötlemise olekute järjestus on järgmine.

1. **Loodud**
2. **Saadetud**
3. **Saadud**
4. **Aktsepteeritud**, **Tühistatud** või **Tagasi lükatud**

Neid olekuid kirjeldatakse üksikasjalikumalt selles teemas allpool.

## <a name="setting-up-rfq-functionality"></a>Pakkumiskutse funktsiooni seadistamine

Enne pakkumiskutse juhtumi loomist peate seadistama pakkumiskutse teabe lehel **Hankeparameetrid**. Pakkumiskutse juhtumi loomisel saate määrata vaikeväärtused, mis kopeeritakse pakkumiskutsele. Saate määrata järgmised vaikeväärtused.

- Uus pakkumiskutsete ostutellimuse tüüp: **Ostutellimuse** või **Ostuleping**
- Aegumiskuupäev ja -kellaaeg
- Tarneteave ja maksetingimused
- Väljad, mis peavad olema pakkumiskutse vastuses

Saate need väärtused kindla pakkumiskutse juhtumi puhul tühistada.

Peate seadistama ka parandusprotsessi. Selle konfiguratsiooni osana saate väljalukustuse sisse lülitada. Kui väljalukustus on sisse lülitatud, peab hankespetsialist, kes soovib pakkumiskutset parandada, valima esmalt vahekaardi **Pakkumine** jaotises **Parandus** käsu **Loo**. Pärast pakkumiskutse värskendamist lisaga peab hankespetsialist protsessi lõpule viima, valides käsu **Vii lõpule**. Tegevus Lõpuleviimine loob meili, mis teavitab hankijaid täiendatud pakkumiskutsest.

Hankijatele saadetava meiliteatise jaoks saate malli valida lehel **Hankeparameetrid**. Malli loomisel võib see sisaldada järgmisi asendussõnesid.

- %Pakkumiskutse juhtum%
- %Pakkumise tagastamise põhjus%
- %Paranduse põhjus%
- %Paranduse ettevalmistaja%
- %Ettevõte%
- %Pakkumiskutse juhtumi nimi%
- %ExpiryDateTime%
- %Kuupäev%

Sõned %Pakkumise tagastuse põhjus% ja %Paranduse põhjus% asendatakse tekstiga, mille hankespetsialist saab sisestada paranduse tegemisel viisardis **Parandus**. Sõned %Paranduse ettevalmistaja% ja %Ettevõte% võetakse automaatselt pakkumiskutselt. Sõne %Kuupäev% asendatakse praeguse kuupäevaga.

Meilimall on vajalik ka siis, kui tühistate pakkumiskutse pärast selle saatmist. Seda meilimalli kasutatakse tühistamisteatise saatmiseks hankija kontaktisikutele. Mall tuleb valida lehel **Hankeparameetrid**. Malli loomisel võib see sisaldada järgmisi asendussõnesid.

- %Tühistamise põhjus%
- %Pakkumiskutse juhtum% 
- %Pakkumiskutse tühistaja%
- %Ettevõte%
- %Pakkumiskutse juhtumi nimi%
- %Kuupäev%

Sõne %Tühistamise põhjus% asendatakse tekstiga, mille hankespetsialist saab sisestada viisardis **Tühistamine**. Sõne %Kuupäev% asendatakse praeguse kuupäevaga.

Kui soovite kasutada pakkumiskutse vastusel põhjusekoode, et näidata pakkumise tagasilükkamise või aktsepteerimise põhjust, peate seadistama põhjusekoodid lehel **Hankija põhjused**.

Mooduli Hanked lehel **Vormiseadistus** saate konfigureerida prinditud või salvestatud pakkumiskutse dokumentide välimust.

> [!NOTE]
> Avaliku sektori konfiguratsiooni puhul peate juba saadetud pakkumiskutse muutmiseks kasutama täiendamisprotsessi. Kui pakkumiskutse on saadetud, on väljad lukustatud. Seetõttu peate pakkumiskutse muutmiseks valima käsu **Loo**, et alustada täiendamisprotsessi, nagu on ülalpool kirjeldatud. Lukustuskäitumist juhitakse suvandiga **Lukusta saadetud pakkumiskutsed** lehel **Hankeparameetrid**. Vaikimisi on selle parameetri säte **Jah** ja avaliku sektori konfiguratsiooni puhul ei saa vaikesätet muuta. Kuigi täiendamisprotsessi saab mitteavaliku sektori konfiguratsioonis käsitsi käsitleda, tuleb seda kasutada avaliku sektori konfiguratsiooni puhul.

Kui loote pakkumiskutse ostutellimuse jaoks ja lisate pakkumiskutsele laokauba, luuakse ka laokanne, mille sissetuleku olek on **Saadud pakkumine**. Koondplaani abil varude arvutamisel arvestatakse vaid selle olekuga pakkumiskutse ridu. Kui soovite, et koondplaan sisaldaks pakkumiskutse ridu eeldatava sissetulekuna, peate konfigureerima selle käitumise koondplaneerimise seadistamisel.

Ostujuht või -agent saab luua kutsetüüpe oma organisatsiooni hankenõuete täitmiseks. Iga kutsetüübi saab seostada hindamismeetodiga. Hindamismeetodid koosnevad kriteeriumitest, mida saab kasutada pakkumiste hindamisel. Peate seadistama kutsetüübid, hindamismeetodid ja hindamiskriteeriumid lehtedel **Kutsetüüp** ja **Hindamismeetod**.

## <a name="creating-and-sending-an-rfq"></a>Pakkumiskutse loomine ja saatmine

Looge pakkumiskutse, valige hankijad, kellelt soovite pakkumiskutse kohta pakkumisi saada, ja saatke seejärel pakkumiskutse hankijatele. Prindihalduse abil saate pakkumiskutse aruande ja vastuselehe aruanded suunata soovitud sihtkohta.

Saate luua pakkumiskutse kas ostutellimuse tüübile **Ostutellimus** või **Ostuleping**.

Kui pakkumiskutse tüüp on **Ostutellimus**, juhtub järgmine.

- Pakkumiskutse ridade loomisel luuakse laokanded, mille sissetuleku olek on **Pakkumise sissetulek**.
- Pakkumise aktsepteerimisel luuakse ostutellimus.

Kui pakkumiskutse tüüp on **Ostuleping**, juhtub järgmine.

- Pakkumiskutset kasutatakse hankijalt pikema aja vältel kindlas koguses või väärtuses toote ostmiseks. Peate valima ostulepingule kehtiva kuupäevavahemiku ja ostulepingut haldava isiku nime.
- Pakkumise aktsepteerimisel luuakse ostuleping.

Kui pakkumiskutse luuakse ostutellimuselt, määratakse automaatselt tüüp **Ostutaotluse**. Pakkumiskutset, mille tüüp on **Ostutaotlus**, ei saa käsitsi luua.

Saate luua on pakkumiskutse ostutaotluselt ainult siis, kui ostutaotluse olek on **Ülevaatusel** ja teile on määratud järgmine töövooülesanne. Ostutaotluse ridu värskendatakse automaatselt, kui aktsepteerite hankijalt saadud pakkumiskutse vastuste (pakkumiste) ridu. Te ei saa ostutaotlust lõpule viia, tagasi lükata, kinnitada ega sellega muid toiminguid teha, kuni pakkumiskutse on pooleli.

Pakkumiskutse loomisel saate valida kutsetüübi. Kutsetüüp määrab hindamiskriteeriumite komplekti, mida kasutatakse pakkumiskutse vastuste hindamiseks.

Saate lisada pakkumiskutse juhtumile küsimustiku. Seejärel kuvatakse küsimustik pärast pakkumiskutse saatmist kõigil vastustel.

Hankijate lisamiseks pakkumiskutse juhtumile on kolm võimalust.

- Hankijate lisamine ükshaaval.
- Kindlatele kriteeriumitele vastavate hankijate otsimine.
- Kõigi hankijate automaatne lisamine, kes on pakkumiskutse ridadel kasutatud hankekategooriate puhul kinnitatud.

Kui pakkumiskutse on valmis, valige käsk **Saada**. Saatmistegevus loob töölehed ja aruanded, mis prinditakse, arhiivitakse ja saadetakse teie prindihaldussätete järgi.

Kui valisite pakkumiskutse saatmisel hankijatele lehel **Pakkumiskutse saatmine** suvandite **Kasuta hindade ümberarvutamiseks hankijat** ja **Kasuta hankijakohast kaubateavet** sätteks **Jah**, sisestatakse osa hankijakohast teavet automaatselt. Saate seda teavet muuta lehel **Pakkumiskutse vastus**.

Järgmises tabelis kuvatakse pakkumiskutse oleku muudatused, kui loote pakkumiskutse ja saadate selle hankijatele.

| Tegevus                             | Madalaim pakkumiskutse päise olek | Kõrgeim pakkumiskutse päise olek                        | Madalaim pakkumiskutse rea olek | Kõrgeim pakkumiskutse rea olek |
|------------------------------------|--------------------------|--------------------------------------------------|------------------------|-------------------------|
| Looge pakkumiskutse päis ja rida.    | Loodud                  | Loodud                                          | Loodud                | Loodud |
| Saatke pakkumiskutse kindlale hankijale. | Saadetud                     | Saadetud                                             | Saadetud                   | Saadetud |
| Lisage teine hankija.                | Loodud                  | Saadetud (pakkumiskutse on saadetud ainult ühele hankijale.) | Loodud                | Saadetud |
| Saatke pakkumiskutse teisele hankijale. | Saadetud                     | Saadetud                                             | Saadetud                   | Saadetud |

> [!NOTE]
> Saate igal ajal pakkumiskutsele täiendavaid hankijaid lisada ning madalaimaid ja kõrgeimaid olekuid värskendatakse kajastamaks uusi hankijaid. Näiteks kui saite pakkumisi kõikidelt hankijatelt ja nõustusite vähemalt ühe pakkumise reaga, siis on pakkumiskutse päise madalaim olek **Tagasi lükatud** ja kõrgeim olek **Aktsepteeritud**. Kui lisate uue hankija, on ükskõik millise rea madalaim olek nüüd **Loodud**. Seega saab pakkumiskutse päise madalaimaks olekuks **Loodud**, kuid kõrgeimaks olekuks jääb **Aktsepteeritud**.

## <a name="amending-an-rfq"></a>Pakkumiskutse parandamine

Mõnikord peate pakkumiskutset pärast selle saatmist muutma. Pakkumiskutse muutmine võib olla vajalik näiteks siis, kui tarnekuupäevad on muutunud või kui soovite täiendavaid tooteid või teistsuguseid tootekoguseid. Saate konfigureerida parandusprotsessi nii, et see oleks rohkem või vähem piirav.

Kui konfigureerite täiendamisprotsessi nii, et see oleks rohkem piirav, siis enne, kui saate juba saadetud pakkumiskutse välju muuta, peate valima pakkumiskutse juhtumis käsu **Loo**, et käivitada täiendamine. Kui olete muudatuste tegemise lõpule viinud, peate valima käsu **Vii lõpule**. Seejärel juhendatakse teid läbi teabe lisamise protsessi, et saata hankijatele paranduse kohta meilisõnum. Värskendatud pakkumiskutse aruanne, mis sisaldab täienduse märkust, lisatakse meilile automaatselt.

Kui konfigureerite täiendamisprotsessi nii, et see oleks vähem piirav, ei pea te enne saadetud pakkumiskutse juhtumi väljade muutmist käsku **Loo** valima. Siiski peate täiendamismärkuse käsitsi pakkumiskutsele lisama ja juhtumi uuesti saatma. Võtke arvesse, et seda lähenemisviisi saab kasutada ainult siis, kui ühtki vastust (pakkumist) pole redigeeritud. Kui olete vastuse sisestanud ja selle olek on **Vastu võetud**, pole nupp **Saada** saadaval. Sel juhul peate valima käsu **Loo** ja seejärel **VII lõpule** ning tegutsema rohkem piiravas protsessis. Seejärel saadetakse vastus pakkumiskutse juhtumi muudatuste kajastamiseks. 

Kui hankijad kasutavad pakkumiste sisestamiseks hankija koostöö liidest, peate hankijaid pakkumiskutse juhtumi muudatustest teavitama alati täiendamisprotsessi kaudu. See nõue aitab vältida olukorda, kus hankijad teevad aegunud pakkumiskutsele pakkumise, kui nende pakkumine on veel pooleli. Lisateavet hankija koostöö kohta vt teemast [Hankija koostöö väliste hankijatega](vendor-collaboration-work-external-vendors.md). 

Kui soovite kutsuda pakkumist tegema täiendavaid hankijaid ja pakkumiskutse juhtumit pole muudetud, saate kasutada nuppu **Saada**. Lisatud hankijad kuvatakse lehel **Saatmine** ja neile saadetakse meilikutse.

## <a name="receiving-and-registering-rfq-replies"></a>Pakkumiskutse vastuste vastuvõtmine ja registreerimine

Pakkumiskutse saatmisel luuakse automaatselt vastuseleht. Pärast pakkumiskutsele vastuste (pakkumiste) saamist peate sisestama iga hankija teabe hankijakohase pakkumiskutse vastuselehele. Kui olete lisanud hindamiskriteeriumid, saate vastuseid hinnata. Seejärel saate hankijate pakkumisi võrrelda ja hinnata oma hindamiskriteeriumite järgi, nagu parim koguhind või parim lõplik tarneaeg.

Kui pakkumiskutse juhtumile on lisatud küsimustik, peate küsimuste vastused vastuselehele käsitsi sisestama.

Saate sisestada ka alternatiivseid ridu, kui pakkumiskutse juhtum lubab nende kasutamist. Valige kiirkaardil **Ostupakkumise read** käsk **Lisa rida**. Seejärel sisestage toote teave, nagu kaubakood või hankekategooria, kogus, hind ja allahindlus.

Kui olete sisestanud vastuse, kuid nõuate hankijalt uut pakkumist, saate pakkumiskutse uuesti saata. Luuakse uus tööleht ja aruanne, mida saate kasutada hankijalt muudatuste taotlemiseks.

Kõigi pakkumiskutsete ülevaadet ja nende vastuste olekuid saate vaadata lehel **Pakkumiskutse järeltoimingud**.

Järgmises tabelis on toodud pakkumiskutse oleku muudatused, kui saate pakkumisi ja registreerite teabe pakkumiskutse vastuselehel.

| Tegevus                                         | Madalaim pakkumise olek | Kõrgeim pakkumise olek | Madalaim pakkumiskutse päise olek | Kõrgeim pakkumiskutse päise olek | Madalaim pakkumiskutse rea olek | Kõrgeim pakkumiskutse rea olek |
|------------------------------------------------|-------------------|--------------------|--------------------------|---------------------------|------------------------|-------------------------|
| Registreerige ühe hankija pakkumine ja salvestage see.        | Saadetud              | Vastu võetud           | Saadetud                     | Vastu võetud                  | Saadetud                   | Vastu võetud |
| Registreerige teise hankija pakkumine ja salvestage see. | Vastu võetud          | Vastu võetud           | Vastu võetud                 | Vastu võetud                  | Vastu võetud               | Saadud |

> [!NOTE]
> Kui tagastate pakkumise hankijale edasiste läbirääkimiste eesmärgil, jäävad madalaimaks ja kõrgeimaks olekuks **Vastu võetud**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Pakkumiste aktsepteerimine ja tagasilükkamine ning aktsepteeritud pakkumiste ülekandmine allavoolu dokumentidele

Pärast parima pakkumise tuvastamist, nt parima koondhinnaga pakkumine, aktsepteerite pakkumise. Saate pakkumises mõne rea aktsepteerida ja ülejäänud tagasi lükata. Samuti saate aktsepteerida ridu teistelt hankijatelt. Võtke arvesse, et mõne rea aktsepteerimisel palutakse teil kõik teised read tagasi lükata. Seega kui soovite teised read aktsepteerida, peate viiba kuvamisel valima käsu **Tühista**. Pakkumiskutse vastuse olek iga hankija puhul, kelle pakkumised või read aktsepteerite, värskendatakse sättele **Aktsepteeritud**. 

Pakkumise või selle konkreetsete ridade aktsepteerimisel luuakse automaatselt ostutellimus või ostuleping. Seejärel saate kõigi teiste hankijate pakkumised tagasi lükata.

Saate vastusele lisada põhjusekoodi, millega selgitada pakkumise aktsepteerimist või tagasilükkamist.

Kui aktsepteerite pakkumiskutse vastuse, mille tüüp on **Ostutaotlus**, värskendavad pakkumiskutse vastuse read ostutaotluse ridu järgmise teabega.

- Ühiku hind
- Allahindlusprotsent
- Allahindluse summa
- Ostukulud
- Reatasud
- Tarnija
- Väline number
- Väline kirjeldus

Järgmises tabelis kuvatakse pakkumiskutse oleku muudatused, kui hankija pakkumisi aktsepteerite või tagasi lükkate.

| Tegevus                      | Madalaim pakkumise olek | Kõrgeim pakkumise olek | Madalaim pakkumiskutse päise olek | Kõrgeim pakkumiskutse päise olek | Madalaim pakkumiskutse rea olek | Kõrgeim pakkumiskutse rea olek |
|-------------------------    |-------------------|--------------------|--------------------------|---------------------------|------------------------|-------------------------|
| Aktsepteerige üks pakkumistest.     | Vastu võetud          | Aktsepteeritud           | Vastu võetud                 | Aktsepteeritud                  | Vastu võetud               | Aktsepteeritud |
| Lükake kõik teised pakkumised tagasi.  | Tagasi lükatud          | Aktsepteeritud           | Tagasi lükatud                 | Aktsepteeritud                  | Tagasi lükatud               | Aktsepteeritud |

