---
title: Fooliote haldamine
description: Selles teemas kirjeldatakse, kuidas töötada fooliotega. Foolio koosneb tavaliselt ühe hankija kaubast ühe üksuse või ettevõtte ja saadetise kohta. Kaubad foolios võivad olla ühes konteineris või need võivad olla jagatud mitme konteineri vahel.
author: sherry-zheng
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMFolioTable, ITMFolioTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: d414ed7ac55afbbc58b8f5542c713f56392f9bc7
ms.sourcegitcommit: 197e6ddee84522fd587c6e4ee4f9089101e301c2
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2022
ms.locfileid: "8570432"
---
# <a name="manage-folios"></a>Fooliote haldamine

[!include [banner](../../includes/banner.md)]

Foolio määratakse sageli kindlaks tollieeskirjadega. See võib koosneda ühe hankija kaubast ühe üksuse või ettevõtte ja saadetise kohta. Foolio kaupu hallatakse ühes konteineris.

Lehe **Kõik fooliod** avamiseks valige **Väljalaadimiskulu \> Fooliod \> Kõik fooliod**. Sellel lehel kuvatakse kõikide praeguste fooliote loend. Toimingupaani nuppude abil saate foolioid luua, kustutada ja nendega töötada. Valige loendist mõni foolio, et vaadata selle üksikasju lehel **Fooliod**.

## <a name="action-pane"></a>Toimingupaan

Lehe **Kõik fooliod** ja **Fooliod** toimingupaanil on nupud, mille abil saate valitud foolioga töötada. Iga nupp teeb ühe toimingu. Toimingupaanil on ka vahekaardid, millest omakorda igaühel on seotud nuppude komplekt. Välja arvatud juhul, kui on märgitud teisiti, on kõik järgmistes alamjaotistes kirjeldatud nupud ja vahekaardid saadaval nii loendivaates (st lehel **Kõik fooliod**) kui ka üksikasjalikus vaates (st lehel **Fooliod**).

### <a name="buttons-that-appear-directly-on-the-action-pane"></a>Otse toimingupaanil kuvatud nupud

Järgmises tabelis kirjeldatakse otse toimingupaanil saadaolevaid nuppe.

| Nupp | Kirjeldus |
|---|---|
| New | Looge foolio. |
| Kustutamine | Kustutage avatud või valitud foolio. |
| Reisikulud | Avage leht **Teekonna kulud**, kus saate kõigi teekonna kaupade fooliotaseme kulusid vaadata ja lisada. Kui fooliokulud lisatakse teekonnale käsitsi, lisatakse need kulude päringu lehele ja jaotatakse igale kaubale vastavalt lehel **Teekonnakulud** määratud meetodile. |

### <a name="buttons-on-the-manage-tab"></a>Nupud vahekaardil Halda

Järgmises tabelis kirjeldatakse toimingupaani vahekaardil **Halda** olevaid nuppe.

| Nupp | Kirjeldus |
|---|---|
| Kviitungite loendi sisestamine | Sisestage sissetulekute loend foolio kõigi ostutellimuse ridade jaoks. Kui kasutatakse mitut ettevõtet hõlmavaid saadetisi, avatakse iga ettevõtte jaoks uus sissetulekute loendi sisestamise dialoogiaken. |
| Toote sissetuleku sisestamine | Sisestage toote sissetulek foolio kõigi ostutellimuse ridade jaoks. Kui kasutatakse mitut ettevõtet hõlmavaid teekondi, avatakse iga ettevõtte jaoks uus toote sissetuleku sisestamise dialoogiaken. |
| Sisesta arve | Sisestage arve foolio kõigi ostutellimuse ridade jaoks. Kui kasutatakse mitut ettevõtet hõlmavaid teekondi, avatakse iga ettevõtte jaoks uus arve sisestamise dialoogiaken. |
| Lähetuse üleviimistellimus | Sisestage üleviimistellimus kõigile üleviimistellimuse ridadele, mis on seotud asjakohase saadetise praeguse foolioga. |
| Võta üleviimistellimus vastu | Sisestage üleviimistellimuse sissetulek kõigile üleviimistellimuse ridadele, mis on seotud asjakohase saadetise praeguse foolioga. |
| Võta transiidis olevad kaubad vastu | Võtke vastu kõik foolio transiidis olevad tellimuseread. |
| Dokumendid on vastu võetud | Värskendage suvandi **Dokumendid on vastu võetud** väärtuseks *Jah*. Selle nupu abil saate lukustada kauba ja/või osturea nii, et seda ei saa rohkem värskendada. |
| Otsi automaatseid kulusid | Otsige asjakohaseid teekonnakulusid. Kui need kulud on juba leitud või värskendatud, saate järgmise teate: „Leidub arveldamata kuluridasid. Kas soovite need üle kirjutada?“ Võtke arvesse, et teekonnakulusid, mis on fooliosse manustatud ja mis on arveldatud, ei kirjutata üle. |
| Loo saabumise tööleht | Looge täpsemaid laofunktsioone kasutades organisatsioonidele saabumiste töölehe. Soovi korral valige **Lähtesta kogus** (soovitatav), **Loo transiidis olevatest kaupadest** ja/või **Loo ostutellimustest**. Viimane suvand sõltub sellest, kas kasutatakse transiidis olevate kaupade töötlemist. |
| Kulude laekumine | Koguge kulusid seal, kus kulutüübil on deebeti jaoks määratud pearaamatukonto. Seda nuppu kasutatakse tavaliselt siis, kui varud on transiidis või kui kaubad on kätte saadud ja arveldatud. |

### <a name="buttons-on-the-general-tab"></a>Nupud vahekaardil Üldine

Järgmises tabelis kirjeldatakse toimingupaani vahekaardil **Üldine** olevaid nuppe.

| Nupp | Kirjeldus |
|---|---|
| Saabunud kaupade loend | Sisestage sissetulekute loend foolio kõigi ostutellimuse ridade jaoks. Kui kasutatakse mitut ettevõtet hõlmavaid teekondi, avatakse iga ettevõtte jaoks uus sissetulekute loendi sisestamise dialoogiaken. |
| Toote sissetulek | Vaadake toote sissetulekukirjet, kui seda kasutatakse. |
| Kauba saabumine | Vaadake kauba saabumise töölehte, kui seda kasutatakse. |
| Kulude päring | Avage kulude päringu leht, et vaadata kõiki teekonna kulusid, kaasa arvatud saatmiskonteinerit, fooliot ja ostutellimust. Lehe täpset vaadet saate kohandada toiminguga Kuva. Kulude päringu lehel saate vaadata mis tahes alasid ning kauba ja kulutüübi koodi. Nende üksuste eemaldamise korral saate lehte kohandada, rühmitades kulud kokku. See võimalus võib olla kasulik, kui kasutate suurusi ja värve. Saate muuta lehel kuvatud dimensioone. Lehel **Kulud** kuvatakse ainult kulutüübi koodid, mille korral on vahekaardi **Sisestamine** kirjeks **Dr** seatud *Kaup*. |

## <a name="header-view"></a>Päisevaade

Vaate **Päis** avamiseks avage foolio ja seejärel valige foolio päises ülal paremal vahekaart **Päis**.

### <a name="settings-on-the-general-fasttab"></a>Kiirkaardi Üldine sätted

Järgmises tabelis kirjeldatakse foolio vaate **Päis** kiirkaardil **Üldine** saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Foolio | Foolio nimi. See nimi luuakse automaatselt foolio loomisel.|
| Reis | Foolioga seotud teekond. |
| Tollimaakler | Valige foolio tollimaakler. Tollimaaklerid määratakse hankija jaoks. Need võimaldavad tekkinud kulud automaatselt kindlaks määrata. |
| Maja lennu veokiri / veokiri | Määrake foolio kohta kehtiv edasisaatja lennu saateleht või veokiri. |
| Ettevõte | Foolioga seotud juriidiline isik (ettevõte). |
| Lasti kontrollnumber | Seda välja kasutavad mõne riigi või regiooni tolliosakonnad. |
| Mõõtmine | See väli võimaldab mõõdu määrata moodulis **Väljalaadimiskulu**. Mõõtmisi kasutavad tihti organisatsioonid, kes ei tea kaupade individuaalset mahtu või kaalu, kuid vajavad täpsemat jaotust, kui võimaldavad summa või koguse suvandid. Ekspediitor esitab kaalu või kuupmõõdu ja teie saate selle seada kas kauba või ostutellimuse tasemele. Selle saab parameetri valimisel automaatselt värskendada või käsitsi sisestada. |
| Mõõtühik | Määratud mõõtmise kohta kehtiv ühik. |
| Pakkide arv | Pakkide arv foolios. Selle välja saab parameetrivalikust olenevalt värskendada automaatselt. |
| Hankija konto | Valige foolioga seotud hankija. Sellel väljal on ainult informatiivne eesmärk. See ei mõjuta funktsioone. |
| Nimi | Valitud hankijakonto nimi. |
| Märkused | Sisestage foolioga seotud igasugune lisateave. |
| Kauba kirjeldus | Valige kaupade kirjeldus, mis aitab tuvastada fooliot. Lisateabe saamiseks lugege teemat [Kaupade kirjeldus](shipping-information-setup.md#description-of-goods). |
| Hindamise kuupäev | See väli on seotud kohustuse sisestamise lehega. Moodul **Väljalaadimiskulu** kasutab siin seatud kuupäeva tollivahetuskurssi. Vaikeväärtus on kohustuse sisestamise lehel märgitud kuupäev. |
| Tolli ID | Sisestage tolli ID. Selle ID saate riikide või regioonide tolliosakondadest. |
| Tollimaksu kood | Sisestage foolioga seostatav tariifikood. Tavaliselt nõuab (ja määrab) seda koodi riik või regioon, kuhu kauba lähetate. |

### <a name="settings-on-the-delivery-fasttab"></a>Kiirkaardi Tarne sätted

Järgmises tabelis kirjeldatakse foolio vaate **Päis** kiirkaardil **Tarne** saadaolevaid sätteid.

| Field | Kirjeldus |
|---|---|
| Foolio kuupäev | Valige foolioga seostatav kuupäev. Vaikeväärtus on teekonna loomiskuupäev. |
| Arvatav saabumisaeg sadamas | Sihtkohta („sihtkoha“ sadamasse) prognoositud saabumisaja (ETA) kuupäev. |
| Eeldatav tarnekuupäev | Tavaliselt kuupäev, mil kaubad peaksid lattu saabuma. Seda välja ei kasutata eeldatava tarnekuupäeva arvutamise korral. (Selle asemel kasutatakse jälgimiskontrolli eeldatavat tarnekuupäeva.) Selleks, et seada see väli nii, et väärtus vastaks jälgimiskontrolli eeldatavale tarnekuupäevale, kasutage jaotist [Jälgimise juhtimiskeskus](delivery-information-setup.md#tracking-control-center). |
| Algdokumendid on vastu võetud | Algdokumentide vastuvõtmise kuupäev. |
| Maakleri soovitus | Maakleri teavitamise kuupäev. |
| Algne veokiri on saadetud | Algse veokirja saatmise kuupäev. |
| Kaubad on vabastatud | Kaupade väljastamise kuupäev. |
| Kliendiga kohtumine | Kliendikohtumise kuupäev. |
| Lattu tarnitud | Kuupäev, mil kaubad lattu tarniti. |
| Kinnitamise kuupäev | Kinnitamise kuupäev. |
| Tarnejuhised | Tarnejuhiste vastuvõtmise kuupäev. |
| Lähtesadam | Sadam, millest teekond väljub. |
| Sihtsadam | Sadam, kuhu teekond saabub. Saatmiskonteineril võib olla erinev sadam, sest laev võib peatuda mitmes sadamas. |

### <a name="settings-on-the-export-fasttab"></a>Kiirkaardi Eksportimine sätted

Järgmises tabelis kirjeldatakse foolio vaate **Päis** kiirkaardil **Eksportimine** saadaolevaid sätteid.

| Field | Kirjeldus |
|---|---|
| Eksportija | Eksportija saab salvestada fooliosse. Rahvusvahelises kaubanduses võite saata ostutellimuse ühele ettevõttele, kuid võtta kaubad vastu teisest ettevõttest. Tolliasutused nõuavad jälgimist ja dokumenteerimist. Eksportija nime ja aadressi saab salvestada siin. |
| Nimi | Valitud eksportija nimi. |

## <a name="lines-view"></a>Ridade vaade

Vaate **Read** avamiseks avage foolio ja seejärel valige foolio päises ülal paremal vahekaart **Read**.

### <a name="information-on-the-folio-fasttab"></a>Teave kiirkaardil Foolio

Vaate **Read** kiirkaardil **Foolio** on kuvatud teave foolio kohta. Suurem osa sellest teabest on kuvatud ka vaates **Päis**, nagu on kirjeldatud selles teemas eespool.

### <a name="information-and-buttons-on-the-lines-fasttab"></a>Teave ja nupud kiirkaardil Read

Vaate **Read** kiirkaardil **Read** on kuvatud üksikasjad iga täieliku või osalise ostutellimuse rea kohta, mis on kaasatud praegusesse fooliosse.

Järgmises tabelis kirjeldatakse vaate **Read** kiirkaardil **Read** saadaolevaid nuppe.

| Nupp | Kirjeldus |
|---|---|
| Eemaldamine | Eemaldage valitud ostutellimuse rida teekonnast. |
| Varud \> Kanded | Vaadake valitud ostutellimuse rea laokandeid. Pange tähele, et kui kasutate transiidis kaupade funktsiooni, kuvatakse ka algne tellimus ja transiidis olevate kaupade tellimused. |
| Varud \> Kuva dimensioonid | Avage dialoogiboks, kus saate valida varude dimensioonid, mis kuvatakse teie vaadatavate kannete kohta. |
| Värskendamine | Värskendage teavet, mis on seotud valitud ostutellimuserea reasumma, kaalu või mahuga. |

### <a name="information-on-the-lines-details-fasttab"></a>Teave kiirkaardil Ridade üksikasjad

Vaate **Read** kiirkaart **Ridade üksikasjad** kuvab üksikasjad kiirkaardil **Read** parasjagu valitud ostutellimuse rea kohta.
