---
title: Pakkumiskutsete ülevaade
description: Selles teemas antakse ülevaade pakkumiskutsete kohta. Organisatsioonid väljastavad pakkumiskutse, kui saavad mitmelt hankijalt konkureerivaid pakkumisi kaupade või teenuste kohta, mida soovivad osta.
author: kamaybac
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage, BOMExpandPurchRFQ, PurchRFQReplyFollowupItem, PurchRFQCaseVend, PurchRFQReplyFollowup, PurchRFQCaseAmendmentInfo, PurchRFQReplyFollowupCase, PurchRFQReplyStatus, PurchRFQCaseReplyFields, PurchRFQAddQuestionnaire, PurchRFQAmendmentWizard, PurchRFQReplyTableStatus, PurchRFQReplyTableListPage, PurchRFQCancelWizard
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "2154"
- intro-internal
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fc7700c825feb9727b816d9a2776e37fdbd2ff8416ffb4530e5af8c35d61b070
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757682"
---
# <a name="requests-for-quotation-rfqs-overview"></a>Pakkumiskutsete ülevaade

[!include [banner](../includes/banner.md)]

Selles teemas antakse ülevaade pakkumiskutsete kohta. Organisatsioonid väljastavad pakkumiskutse, kui saavad mitmelt hankijalt konkureerivaid pakkumisi kaupade või teenuste kohta, mida soovivad osta. Pakkumiskutses saate hankijatelt küsida teie määratud kaubakoguse hindu ja tarneaegu.
Samuti saate hankijatelt küsida, kas on lisatasusid, nagu saatekulud, või allahindlusi suurte tellimuste või hankija arve ennetähtaegse maksmise korral.

Pakkumiskutse protsess koosneb järgmistest ülesannetest.

1. Pakkumiskutse loomine ja saatmine ühele või mitmele hankijale.
1. Pakkumiste vastuvõtmine ja registreerimine (RFQ vastused)
1. Aktsepteeritud pakkumiste ülekandmine ostutellimuseks, ostulepinguks või ostutaotluseks.

Järgmisel joonisel on näidatud ülevaade pakkumiskutse protsessist.

[![RFQ-protsess.](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)

Saate luua pakkumiskutse juhtumi plaanitud tellimustelt, ostutaotluselt või käsitsi sisestades. Pakkumiskutse juhtum on alusdokument, mida kasutate igale hankijale pakkumiskutse väljastamiseks.

Kui olete pakkumiskutse ette valmistanud ja hankijad lisanud, valige pakkumiskutses **Saada** (**Saada ja avalda** avaliku sektori korral). Iga hankija kohta, kellele pakkumiskutse saadate, luuakse pakkumiskutse tööleht. Saate konfigureerida saatmistegevuse prindisuvandeid kas printima iga hankija kohta aruande arhiivi või saatma aruande iga hankija meiliaadressile. Peale selle saate iga hankija pakkumiskutse töölehe abil luua aruande, mille saate hankijale saata kohe või hiljem uuesti. Samuti saate konfigureerida saatmistegevuse nii, et see loob vastuselehe, mille hankija saab täita.

Selles teemas käsitletakse pakkumiskutsete käsitlemise protsessi, kui hankija koostööd ei kasutata. Kui teie süsteem on seadistatud hankija koostöö kasutamiseks, saavad hankijad sisestada pakkumised otse rakenduses Supply Chain Management. Lisateavet vt teemast [Hankija koostöö klientidega](/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-work-customers-dynamics-365-operations) ja [Hankija koostöö väliste hankijatega](vendor-collaboration-work-external-vendors.md).

Kui peate pakkumiskutset pärast selle saatmist täiendama, saate pakkumiskutse hankijatele uuesti saata, kasutades kaht täiendamistegevust: loomine ja lõpetamine.

Pakkumiste vastuvõtmisel meili teel saate neid pakkumisi käsitleda lehel **Pakkumiskutsed**.

Kui nõutav on hankija vastuse teine iteratsioon, valige lehel **Pakkumiskutse** käsk **Tagasta**. Tagastustegevus loob uue töölehe ja aruande, mis prinditakse, arhiivitakse ja saadetakse teie prindisätete järgi.

Kui olete lisanud pakkumiskutse juhtumile hindamiskriteeriumid, on pakkumiskutsel hindamispaneel, kuhu saate punktisummad sisestada. Punktide kogusumma kuvatakse pakkumiskutsel, kui võrdlete vastuseid lehel **Vastuste võrdlemine**. Lehel **Võrdle vastuseid** saate ka võrrelda vastuse andmeid, nagu rea hind, tarnekuupäev ja koguhind.

Pärast seda, kui valite pakkumise või ridade arvu pakkumises, saate aktsepteerida mõned või kõik read ja ülejäänud tagasi lükata. Luuakse aktsepteerimise ja tagasilükkamise töölehed ning vastavad aruanded, mis prinditakse, arhiivitakse ja saadetakse teie prindisätete järgi. Kui aktsepteerite mõne pakkumise või pakkumise konkreetsed read, luuakse kas ostuleping või ostutellimus või värskendatakse ostutaotlust olenevalt pakkumiskutse ostutüübist. Saate luua kaubandusleppe, mida saate hiljem kasutada mis tahes vastuste puhul olenemata sellest, kas olete need aktsepteerinud või tagasi lükanud.

Pakkumiskutsel on kaks olekut: madalaim ja kõrgeim, saate olekut vaadata suvandi **Kõik pakkumiskutsed** loendilehel. Madalaim olek on pakkumiskutse juhtumil ükskõik millise rea kõige vähemarenenum etapp ja kõrgeim olek on pakkumiskutse juhtumil ükskõik millise rea kõige arenenum etapp. Oletame näiteks, et kolme reaga pakkumiskutse juhtum saadetakse kahele hankijale, nii et olemas on kaks kolme reaga pakkumiskutset. Kõik read on olekuga **Saadetud**. Nüüd sisestatakse ühest hankijast pakkumine ja pakkumiskutse rea olekuks määratakse **Vastu võetud**. See tähendab, et pakkumiskutse juhtumi kolmest reast on ühe pakkumiskutse korral kõik neist **Saadetud** ja teise pakkumiskutse korral **Vastu võetud**. Madalaim olek on sellisel juhul **Saadetud** ja kõrgeim olek **Vastu võetud.**

Neid olekuid kirjeldatakse üksikasjalikumalt selles teemas allpool.

## <a name="setting-up-rfq-functionality"></a>Pakkumiskutse funktsiooni seadistamine

Enne pakkumiskutse juhtumi loomist peate seadistama pakkumiskutse teabe lehel **Hankeparameetrid**. Pakkumiskutse juhtumi loomisel saate määrata vaikeväärtused, mis kopeeritakse pakkumiskutsele. Saate määrata järgmised vaikeväärtused.

- Uus pakkumiskutsete ostutellimuse tüüp: **Ostutellimuse** või **Ostuleping**
- Aegumiskuupäev ja kellaaja nihe pakkumiskutse juhtumi loomise päevast.
- Kutse tüüp, mis võib vaikimisi pakkumiskutse juhtumile määrata kindla hindamismeetodi.
- Tarneteave ja maksetingimused.

Saate need väärtused kindla pakkumiskutse juhtumi puhul tühistada.

Peate seadistama ka parandusprotsessi. Selle konfiguratsiooni osana saate väljalukustuse sisse lülitada. Kui väljalukustus on sisse lülitatud, peab hankespetsialist, kes soovib pakkumiskutset parandada, pakkumiskutse juhtumis vahekaardil **Pakkumine** jaotises **Parandus** esmalt valima käsu **Loo**. Seejärel, pärast pakkumiskutse juhtumi värskendamist lisaga peab hankespetsialist protsessi lõpule viima, valides suvandi **Vii lõpule**. Tegevus Lõpuleviimine loob meili, mis teavitab hankijaid täiendatud pakkumiskutsest.

Hankijatele saadetava meiliteatise jaoks saate malli valida lehel **Hankeparameetrid**. Malli loomisel valikus **Meilimallid** võib see sisaldada järgmisi asendussõnesid.

- %Pakkumiskutse juhtum%
- %Pakkumise tagastamise põhjus%
- %Paranduse põhjus%
- %Paranduse ettevalmistaja%
- %Company%
- %Pakkumiskutse juhtumi nimi%
- %Aegumiskuupäev%
- %Date%

Sõned %Pakkumise tagastuse põhjus% ja %Paranduse põhjus% asendatakse tekstiga, mille hankespetsialist saab sisestada paranduse tegemisel viisardis **Parandus**. Sõnede %Paranduse ettevalmistaja% ja %Company% väärtused võetakse automaatselt pakkumiskutselt. Sõne %Date% asendatakse praeguse kuupäevaga.

Kui soovite tühistada pakkumiskutse pärast selle saatmist, saate seda teha pakkumiskutse juhtumis. Tühistamiseks tuleb kasutada meilimalli, et saata tühistamisteatis hankija kontaktisikutele. Mall tuleb valida lehel **Hankeparameetrid**. Malli loomisel võib see sisaldada järgmisi asendussõnesid.

- %Tühistamise põhjus%
- %Pakkumiskutse juhtum%
- %Pakkumiskutse tühistaja%
- %Company%
- %Pakkumiskutse juhtumi nimi%
- %Date%

Sõne %Tühistamise põhjus% asendatakse tekstiga, mille hankespetsialist saab sisestada viisardis **Tühistamine**. Sõne %Date% asendatakse praeguse kuupäevaga.

Kui soovite kasutada pakkumises põhjusekoode, et näidata pakkumise tagasilükkamise või aktsepteerimise põhjust, peate seadistama põhjusekoodid lehel **Hankija põhjused**.

Mooduli Hanked lehel **Vormiseadistus** saate konfigureerida prinditud või salvestatud pakkumiskutse dokumentide välimust.

> [!NOTE]
> Avaliku sektori konfiguratsiooni puhul peate juba saadetud pakkumiskutse muutmiseks kasutama täiendamisprotsessi. Kui pakkumiskutse on saadetud, on väljad lukustatud.
Seetõttu peate pakkumiskutse muutmiseks valima käsu **Loo**, et alustada täiendamisprotsessi, nagu on ülalpool kirjeldatud. Lukustuskäitumist juhitakse suvandiga **Lukusta saadetud pakkumiskutsed** lehel **Hankeparameetrid**. Vaikimisi on selle parameetri säte **Jah** ja avaliku sektori konfiguratsiooni puhul ei saa vaikesätet muuta. Kuigi täiendamisprotsessi saab mitteavaliku sektori konfiguratsioonis käsitsi käsitleda, tuleb seda kasutada avaliku sektori konfiguratsiooni puhul.

Kui loote ostutellimuse tüüpi pakkumiskutse juhtumi ja lisate pakkumiskutsele laokauba, luuakse ka laokanne, mille sissetuleku olek on **Saadud pakkumine**. Koondplaani abil varude arvutamisel arvestatakse vaid selle olekuga pakkumiskutse juhtumi ridu. Kui soovite, et koondplaan sisaldaks pakkumiskutse juhtumi ridu eeldatava sissetulekuna, peate konfigureerima selle käitumise koondplaneerimise seadistamisel.

Ostujuht või -agent saab luua kutsetüüpe oma organisatsiooni hankenõuete täitmiseks. Iga kutsetüübi saab seostada hindamismeetodiga. Hindamismeetodid koosnevad kriteeriumitest, mida saab kasutada pakkumiste hindamisel. Peate seadistama kutsetüübid, hindamismeetodid ja hindamiskriteeriumid lehtedel **Kutsetüüp** ja **Hindamismeetod**.

## <a name="choose-default-fields-to-include-in-vendor-rfq-reply-forms"></a><a name="default-reply-fields"></a>Vaikeväljade valimine hankija pakkumiskutse vastusevormidesse kaasamiseks

Saate määratleda kindlat tüüpi teabe, mida soovite saada hankijatelt, kui nad vastavad pakkumiskutsetele. Väljad, mis märgitakse vaikeväljadeks, lisatakse hankija koostöö jaoks mõeldud veebivormile. Nende sätete määramiseks tehke järgmist.

1. Kui te pole seda juba teinud, kasutage lehte [Funktsioonihaldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), et lubada funktsioon *Pakkumiskutse väljade valimine hankija pakkumiskutse vastusevormidesse kaasamiseks*.
1. Minge **Hanked > Seadistus > Hangete parameetrid**.
1. Avage vahekaart **Pakkumiskutse**.
1. Valige vastuseväljade link **Vaikepakkumiskutsed** pealkirja **Vaikeväärtuste seadistamine pakkumiskutsete jaoks** alt.
1. Avaneb dialoogiboks **Pakkumiskutse vastuse vaikeväljad**.
1. Jaotis **Hankija pakkumiskutse vastusevormidesse kaasatud pakkumiskutse väljad** sisaldab liugurit iga välja jaoks, mis on saadaval pakkumiskutse vastusevormides kasutamiseks. Väljad, mille väärtuseks on selles jaotises seatud *Jah*, lisatakse (koos oma väärtustega) pakkumiskutse vastusevormidesse. Seadke liuguri väärtuseks *Ei* iga välja jaoks, mille puhul soovite, et hankijad ei näeks selle andmeid pakkumiste läbivaatamisel. See võimaldab teil sisestada pakkumiskutse sisestamise ajal ettevõttesisesteks eesmärkideks hinnangulisi või oodatud väärtuseid, ilma et hankija sisestatud andmeid näeks.

Vajadusel saate need sätted üksikute pakkumiskutsete puhul alistada.

## <a name="creating-and-sending-an-rfq"></a>Pakkumiskutse loomine ja saatmine

Looge pakkumiskutse juhtum, valige hankijad, kellelt soovite pakkumiskutse juhtumi kohta pakkumisi saada, ja saatke seejärel pakkumiskutse hankijatele. Prindisätete abil saate pakkumiskutse aruande ja vastuselehe aruanded suunata soovitud sihtkohta.

Saate käsitsi luua pakkumiskutse juhtumi kas ostutellimuse tüübile **Ostutellimus** või **Ostuleping**.

Kui pakkumiskutse juhtumi tüüp on **Ostutellimus**, ilmneb järgmine käitumine, mis hälbib muud tüüpi pakkumiskutse juhtumitest:

- Pakkumiskutse juhtumi ridade loomisel luuakse laokanded, mille sissetuleku olek on **Pakkumise sissetulek**.
- Pakkumise aktsepteerimisel luuakse ostutellimus.

Kui pakkumiskutse tüüp on **Ostuleping**, ilmneb järgmine käitumine, mis hälbib muudest pakkumiskutse juhtumitest:

- Pakkumiskutse juhtumit kasutatakse hankijalt pikema aja vältel kindlas koguses või väärtuses toote ostmiseks. Peate valima ostulepingule kehtiva kuupäevavahemiku ja ostulepingut haldava isiku nime.
- Pakkumise aktsepteerimisel luuakse ostuleping.

Kui pakkumiskutse juhtum luuakse ostutellimuselt, määratakse automaatselt tüüp **Ostutaotluse**. Pakkumiskutse juhtumit, mille tüüp on **Ostutaotlus**, ei saa käsitsi luua.

Saate luua on pakkumiskutse juhtumi ostutaotluselt ainult siis, kui ostutaotluse olek on **Ülevaatusel** ja teile on määratud järgmine töövooülesanne. Ostutaotluse ridu värskendatakse automaatselt, kui aktsepteerite hankijalt saadud pakkumiste (pakkumiskutse vastuste) ridu. Te ei saa ostutaotlust lõpule viia, tagasi lükata, kinnitada ega sellega muid toiminguid teha, kuni tellimuserida on värskendatud kinnitatud pakkumiskutse reaga või pakkumiskutse juhtum on tühistatud.

Pakkumiskutse juhtumi loomisel saate valida kutsetüübi. Kutsetüüp määrab hindamiskriteeriumite komplekti, mida kasutatakse pakkumiskutse vastuste hindamiseks pakkumiskutse juhtumi suhtes.

Saate lisada pakkumiskutse juhtumile küsimustiku. Seejärel kuvatakse küsimustik pärast pakkumiskutse saatmist kõigil pakkumiskutse vastustel. Küsimustiku täitmine on kohustuslik ülesanne, enne kui pakkumise saab esitada.

Ehkki vaikeväärtused on olemas, saate vajadusel muuta iga pakkumiskutse juhtumi puhul **hankija pakkumiskutse vastusevormidesse kaasatud pakkumiskutse väljade** sätteid. Selleks looge või avage pakkumiskutse juhtum. Seejärel avage toimingupaanil vahekaart **Pakkumine** ja valige jaotises **Vastused** suvand **Sea pakkumiskutse vastuse vaikeväärtused**. Avaneb dialoogiboks **Pakkumiskutse vastuse vaikeväljad**, mis toimib sama moodi nagu hankija pakkumiskutse vastusevormidele vaikeväärtuste seadmine, kuigi siin tehtud muudatused mõjutavad ainult praegust pakkumiskutse juhtumit. Lisateavet selle funktsiooni lubamise ja selle töötamise kohta leiate teemast [Vaikeväljade valimine hankija pakkumiskutse vastusevormidesse kaasamiseks](#default-reply-fields).

Hankijate lisamiseks pakkumiskutse juhtumile on kolm võimalust.

- Hankijate lisamine ükshaaval.
- Kindlatele kriteeriumitele vastavate hankijate otsimine.
- Kõigi hankijate automaatne lisamine, kes on pakkumiskutse juhtumi ridadel kasutatud hankekategooriate puhul kinnitatud.

Kui pakkumiskutse on valmis, valige käsk **Saada**. Saatmistegevus loob töölehed ja aruanded, mis prinditakse, arhiivitakse ja saadetakse teie prindisätete järgi.

Kui valisite pakkumiskutse saatmisel hankijale lehel **Pakkumiskutse saatmine** suvandite **Kasuta hindade ümberarvutamiseks hankijat** ja **Kasuta hankijakohast kaubateavet** sätteks **Jah**, sisestatakse osa hankijakohast teavet automaatselt selle hankija pakkumiskutsesse.

## <a name="amending-an-rfq-case"></a>Pakkumiskutse juhtumi parandamine

Mõnikord peate pakkumiskutse juhtumit pärast selle saatmist muutma. Pakkumiskutse juhtumi muutmine võib olla vajalik näiteks siis, kui tarnekuupäevad on muutunud või kui soovite täiendavaid tooteid või teistsuguseid tootekoguseid. Saate konfigureerida parandusprotsessi nii, et see oleks rohkem või vähem piirav.

Kui konfigureerite täiendamisprotsessi nii, et see oleks rohkem piirav, siis enne, kui saate juba saadetud pakkumiskutse välju muuta, peate valima pakkumiskutse juhtumis käsu **Loo**, et käivitada täiendamine. Kui olete muudatuste tegemise lõpule viinud, peate valima käsu **Vii lõpule**. Seejärel juhendatakse teid läbi teabe lisamise protsessi, et saata hankijatele paranduse kohta meilisõnum. Värskendatud pakkumiskutse aruanne, mis sisaldab täienduse märkust, lisatakse meilile automaatselt.

Kui konfigureerite täiendamisprotsessi nii, et see oleks vähem piirav, ei pea te enne saadetud pakkumiskutse juhtumi väljade muutmist käsku **Loo** valima. Siiski peate täiendamismärkuse käsitsi pakkumiskutsele lisama ja juhtumi uuesti saatma. Võtke arvesse, et seda lähenemisviisi saab kasutada ainult siis, kui ühtki vastust (pakkumist) pole redigeeritud. Kui olete vastuse sisestanud ja selle olek on **Vastu võetud**, pole nupp **Saada** saadaval. Sel juhul peate valima käsu **Loo** ja seejärel **VII lõpule** ning tegutsema rohkem piiravas protsessis. Seejärel saadetakse vastus pakkumiskutse juhtumi muudatuste kajastamiseks.

Kui hankijad kasutavad pakkumiste sisestamiseks hankija koostöö liidest, peate hankijaid pakkumiskutse juhtumi muudatustest teavitama alati täiendamisprotsessi kaudu. See protsess aitab vältida olukorda, kus hankijad teevad aegunud pakkumiskutsele pakkumise, kui nende pakkumine on veel pooleli. Lisateavet hankija koostöö kohta vt teemast [Hankija koostöö väliste hankijatega](/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-work-external-vendors).

Kui soovite kutsuda pakkumist tegema täiendavaid hankijaid ja pakkumiskutse juhtumit pole muudetud, saate kasutada nuppu **Saada**. Lisatud hankijad kuvatakse lehel **Saatmine** ja neile saadetakse meilikutse.

## <a name="receiving-and-registering-rfq-replies"></a>Pakkumiskutse vastuste vastuvõtmine ja registreerimine

Pakkumiskutse saatmisel luuakse automaatselt vastuseleht. Pakkumiste saamisel pakkumiskutses peate need sisestama lehe **Pakkumiskutse** kaudu, klõpsates tegevusel **Redigeeri pakkumiskutse vastust**. See võimaldab teil sisestada pakkumise teabe spetsiaalsel pakkumise vormil. Alguses on suvandi **Vastuse edenemine** olekuks **Alustamata**. Kui klõpsate valikul **Redigeeri pakkumiskutse vastust**, on edenemise olekuks **Ostja värskendab** kuni pakkumise esitamiseni. Klõpsake **Edasta**, kui olete pakkumise teabe sisestanud. Vastuse edenemisolekuks muutub **Ostja edastatud.** Sarnaselt, kui hankija koostöö on lubatud, värskendatakse suvandit **Vastuse edenemine**, kui hankija käsitleb pakkumist. Olek muutub väärtuselt **Hankija värskendab** väärtusele **Hankija edastatud**. Kui pakkumine on esitatud, luuakse tööleht olekuga **Vastu võetud**. Vastus (pakkumine) peab olema esitatud, et see registreeritaks vastuvõetuks ja alles seejärel saab seda edasi töödelda kinnitatuna või tagasi lükatuna.

Kui soovite pakkumist värskendada, peata läbima sama protsessi, mis on esitatud ülal, ja esitama selle uuesti.

Pange tähele, et vormil **Pakkumiskutse** tohib muuta ainult teavet, mis on seotud pakkumise töötlemise, mitte pakkumise sisestamisega. Pakkumise sisestamiseks või muutmiseks klõpsake valikut **Redigeeri pakkumiskutse vastust.**

Pakkumise teabe sisestamisel, kui pakkumiskutse juhtum võimaldab kasutada alternatiivseid ridu, saate lisada alternatiivseid ridu ridade jaoks, millel on määratletud ainult hankekategooria, mitte kataloogi kaup. Alternatiivsete ridade lisamiseks klõpsake **Lisa alternatiiv**.

Kui olete sisestanud vastuse, kuid nõuate hankijalt uut pakkumist, saate pakkumiskutse tagastada. Luuakse uus tööleht ja aruanne, mille saab saata hankijale.

Kõigi pakkumiskutsete ülevaadet ja nende olekuid **Saadetud, Vastu võetud, Kinnitatud, Tagasi lükatud, Tühistatud, Keeldutud** saate vaadata lehel **Pakkumiskutse järeltoimingud**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Pakkumiste aktsepteerimine ja tagasilükkamine ning aktsepteeritud pakkumiste ülekandmine allavoolu dokumentidele

Pärast parima pakkumise tuvastamist, nt parima koondhinnaga pakkumine, aktsepteerite pakkumise. Saate pakkumises mõne rea aktsepteerida ja ülejäänud tagasi lükata.
Samuti saate aktsepteerida ridu teistelt hankijatelt. Võtke arvesse, et mõne rea aktsepteerimisel palutakse teil kõik teised read tagasi lükata. Seega kui soovite teised read aktsepteerida, peate viiba kuvamisel valima käsu **Tühista**. Pakkumiskutse vastuse olek iga hankija puhul, kelle pakkumised või read aktsepteerite, värskendatakse sättele **Aktsepteeritud**.

Kui soovite ostutellimuse või ostulepingu ettevalmistamisel lisada pakkumiskutsesse täiendava rea, saate seda teha, klõpsates lehe **Pakkumiskutse** ruudustikus valikul **Lisa rida**. Saate lehel **Pakkumiskutse** vaadata ja redigeerida ainult seda rida. Selle vastuvõtmisel on see nähtav pakkumise lehel.

Pakkumise või selle ühe või mitme rea aktsepteerimisel luuakse automaatselt ostutellimus või ostuleping. Seejärel saate kõigi teiste hankijate pakkumised tagasi lükata.

Saate vastusele lisada põhjusekoodi, millega selgitada pakkumise aktsepteerimist või tagasilükkamist.

Kui aktsepteerite pakkumise tüübiga **Ostutaotlus**, värskendatakse ostutaotluse ridu järgmise teabega, mis kajastab aktsepteeritud pakkumise teavet:

- Ühiku hind
- Allahindlusprotsent
- Allahindluse summa
- Ostukulud
- Reatasud
- Tarnija
- Väline number
- Väline kirjeldus

Järgmises tabelis kuvatakse pakkumiskutse oleku muudatused, kui hankija pakkumisi aktsepteerite või tagasi lükkate.

## <a name="statuses--highest-and-lowest"></a>Olekud – kõrgeim ja madalaim

Pakkumiskutse juhtumi vahekaardil Hankija saate vaadata ridu teatud hankija kõrgeima ja madalaima olekuga. Kui hankija on lisatud ja ridu pole veel saadetud, <strong>luuakse</strong> nii madalaim kui ka kõrgeim olek. Kui pakkumiskutse saadetakse hankijale kõigi ridadega, siis on kahe rea olek <strong>Saadetud</strong>. Kui mõned read hankijalt pärit pakkumises aktsepteeritakse ja teised lükatakse tagasi, saavad tagasi lükatud read madalaima oleku, milleks on <strong>Tagasi lükatud</strong> ja aktsepteeritud read saavad kõrgeima oleku, milleks on <strong>Kinnitatud</strong>.

Pakkumiskutse juhtumi ridadel näete kõrgeimat ja madalaimat olekut rea kohta kõigi hankijate lõikes. Kui saatsite rea kõigile hankijatele pakkumiskutse juhtumis ja keegi pole veel vastanud, on nii madalaima kui ka kõrgeima oleku väärtuseks **Saadetud.** Kui vähemalt üks hankija vastab, muutub kõrgeima oleku väärtuseks **Vastu võetud**. Kui lisate juhtumisse uue hankija, muutub madalaima oleku väärtuseks **Loodud**

Kõrgeim ja madalaim olek pakkumiskutse juhtumis on \<vahekaardil Hankija ja vahekaardil Read olevate olekute kogum.

Olekud on järjestatud järgmisel viisil madalaimast kõrgeimani: Loodud, Saadetud, Vastu võetud, Tagasi lükatud, Kinnitatud, Keeldutud, Tühistatud.

Järgmises tabelis kuvatakse pakkumiskutse juhtumi oleku muudatused, kui loote pakkumiskutse juhtumi koos ridadega ja saadate selle hankijatele.

| **Tegevus**                                | **Madalaim pakkumiskutse juhtumi olek** | **Kõrgeim pakkumiskutse juhtumi olek** | **Madalaim pakkumiskutse rea olek** | **Kõrgeim pakkumiskutse rea olek** |
|-------------------------------------------|----------------------------|-----------------------------|---------------------------------|----------------------------------|
| Looge pakkumiskutse juhtumi päis ja rida.      | Loodud                    | Loodud                     | Loodud                         | Loodud                          |
| Saatke pakkumiskutsed kõigile hankijatele pakkumiskutse juhtumis. | Saadetud                       | Saadetud                        | Saadetud                            | Saadetud                             |
| Lisage teine hankija.                       | Loodud                    | Saadetud                        | Loodud                         | Saadetud                             |
| Saatke pakkumiskutse teisele hankijale.        | Saadetud                       | Saadetud                        | Saadetud                            | Saadetud                             |

Kõik read pakkumiskutses, mis on seotud pakkumiskutse juhtumiga, on olekus **Saadetud**.

Järgmises tabelis on toodud pakkumiskutse oleku muudatused, kui saate pakkumisi ja registreerite teabe pakkumiskutse vastuselehel.

| **Tegevus**                                               | **Madalaim olek kõigi pakkumiskutsete kõigi ridade lõikes** | **Kõrgeim olek kõigi pakkumiskutsete kõigi ridade lõikes** | **Madalaim pakkumiskutse juhtumi päise olek** | **Kõrgeim pakkumiskutse juhtumi päise olek** | **Madalaim pakkumiskutse rea olek** | **Kõrgeim pakkumiskutse rea olek** |
|----------------------------------------------------------|------------------------------------------------|-------------------------------------------------|-----------------------------------|------------------------------------|---------------------------------|----------------------------------|
| Registreerige ühe hankija pakkumine pakkumiskutses ja salvestage see.        | Saadetud                                           | Vastu võetud                                        | Saadetud                              | Vastu võetud                           | Saadetud                            | Vastu võetud                         |
| Registreerige teise hankija pakkumine pakkumiskutses ja salvestage see. | Vastu võetud                                       | Vastu võetud                                        | Vastu võetud                          | Vastu võetud                           | Vastu võetud                        | Vastu võetud                         |


All toodud näites näete kõrgeimat ja madalaimat olekut pakkumiskutse juhtumis, kus üks pakkumine on vastu võetud ja ülejäänud pakkumised on kinnitatud. Kui vastu võetud pakkumine lükatakse tagasi, muutub pakkumisekutse juhtumi päises ja real madalaima oleku väärtuseks Vastu võetud asemel Tagasi lükatud.


|            <strong>Tegevus</strong>             | <strong>Madalaim olek kõigi pakkumiskutsete kõigi ridade lõikes</strong> | <strong>Kõrgeim olek kõigi pakkumiskutsete kõigi ridade lõikes</strong> | <strong>Madalaim pakkumiskutse juhtumi päise olek</strong> | <strong>Kõrgeim pakkumiskutse juhtumi päise olek</strong> | <strong>Madalaim pakkumiskutse rea olek</strong> | <strong>Kõrgeim pakkumiskutse rea olek</strong> |
|------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------|-------------------------------------------------|----------------------------------------------|-----------------------------------------------|
| Aktsepteerige üks pakkumistest. (või vähemalt üks rida) |                          Vastu võetud                           |                           Aktsepteeritud                           |                    Vastu võetud                    |                    Aktsepteeritud                     |                   Vastu võetud                   |                   Aktsepteeritud                    |
|           Lükake kõik teised pakkumised tagasi.           |                          Tagasi lükatud                           |                           Aktsepteeritud                           |                    Tagasi lükatud                    |                    Aktsepteeritud                     |                   Tagasi lükatud                   |                   Aktsepteeritud                    |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]