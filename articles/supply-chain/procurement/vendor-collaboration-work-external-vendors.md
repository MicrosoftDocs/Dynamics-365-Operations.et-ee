---
title: "Hankija koostöö väliste hankijatega"
description: "Selles teemas selgitatakse, kuidas ostuagendid saavad teha koostööd väliste hankijatega, et vahetada teavet ostutellimuste ja veose varude kohta."
author: mkirknel
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchRFQCaseTableListPage, VendVendorPortalInvoicePart
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 24a17d3734e39815684098f694a77e96cdbc1cfe
ms.openlocfilehash: 2d879ee5a23e3263c9dce52f4732a2be74e60f8e
ms.contentlocale: et-ee
ms.lasthandoff: 03/07/2018

---

# <a name="vendor-collaboration-with-external-vendors"></a>Hankija koostöö väliste hankijatega

[!include[banner](../includes/banner.md)]

Moodul **Hankija koostöö** on suunatud hankijatele, kellel puudub elektrooniliste andmete vahetuse (EDI) integratsioon rakendusega Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition. See laseb hankijatel töötada ostutellimustega (OT-dega), arvetega, veose varude teabega ja pakkumiskutsetega, samuti võimaldab see neile juurdepääsu osale hankija koondandmetest. Selles teemas selgitatakse, kuidas saate teha koostööd väliste hankijatega, kes kasutavad hankija koostööliidest OT-de, pakkumiskutsete ja veose varudega töötamiseks. Selles selgitatakse ka, kuidas lubada konkreetset hankijat hankija koostöö kasutamiseks ja kuidas määratleda teavet, mida kõik hankijad näevad, kui nad vastavad OT-le.

Lisateavet selle kohta, mida välised hankijad saavad hankija koostöö liideses teha, leiate teemast [Hankija koostöö klientidega](vendor-collaboration-work-customers-dynamics-365-operations.md).

> [!NOTE]
> Selles teemas kirjeldatud teave hankija koostöö kohta kehtib ainult rakenduse Finance and Operations praeguse versiooni puhul. Microsoft Dynamics AX 7.0 (veebruar 2016) ja rakenduse Microsoft Dynamics AX versiooni 7.0.1 (mai 2016) puhul saate hankijatega koostööd teha, kasutades moodulit **Hankija portaal**. Mooduli **Hankija portaal** kohta teabe saamiseks vaadake teemat [„Hankijatega koostöö tegemine Hankija portaali kasutades”](collaborate-vendors-vendor-portal.md).

Lisateavet selle kohta, kuidas hankijad saavad kasutada hankija koostööd arveldamise protsessides, leiate teemast [Hankija koostöö arve tööruum](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md). Lisateavet selle kohta, kuidas ette valmistada uue hankija koostöö kasutajaid, leiate teemast [Hankija koostöö kasutajate haldamine](manage-vendor-collaboration-users.md).

## <a name="defining-the-information-that-is-shown-to-vendors-when-they-respond-to-pos"></a>Hankijatele kuvatava teabe määramine OT-dele vastamisel

Kui hankijad vastavad teie saadetud OT-le, näevad nad ühte kolmest sõnumiväljast, kus nad peavad kinnitama, et soovivad OT aktseptida, tagasi lükata või muudatustega aktseptida. Kuna teave, mis tuleb sellel hetkel hankijale kuvada, võib olla teie ettevõtte põhine, saate määrata igale kinnitusteatele oma sõnumi. Näiteks võib tekst teavitada hankijat järgmistest protsessi etappidest või tingimustest.

OT vastuses kuvatava teksti määramiseks toimige järgmiselt.

1. Valige vastuse tüüp lehel **Teave ostutellimustele vastavate hankijate jaoks** ja seejärel valige **Redigeeri**.
2. Sisestage väljale **Teabeteade** hankijatele sõnumiväljal kuvatav teave.

Kui peate lisama teateid rohkem kui ühes keeles, koostage eraldi teated ja määrake neist igaühele sobiv keelekood. Igale hankijale kuvatav teade on hankija kasutatavas keeles.

## <a name="setting-the-vendor-collaboration-options-for-a-specific-vendor"></a>Hankija koostöö valikute seadistamine konkreetsele hankijale

Rakenduses Finance and Operations saab kõigi hankijate jaoks koostöö üldsätted, nagu hankijale saadaolevad turberollid, konfigureerida administraator. Siiski on ka mõni säte, mis võib iga hankija konto puhul erinev olla. Peaksite need sätted konfigureerima.

- Lubage hankija koostöö.
- Määrake, kas hankija peaks hinnateavet nägema.

### <a name="enabling-vendor-collaboration"></a>Hankija koostöö lubamine

Enne kui välise hankija jaoks saab kasutajakontod luua, peate konfigureerima hankija konto selliselt, et hankija saaks hankija koostööd kasutada. Seadistage väli **Koostöö aktiveerimine** lehe **Hankijad** vahekaardil **Üldine**. Valikud on järgmised:

- **Aktiivne (ostutellimus kinnitatakse automaatselt)** – OT-d kinnitatakse automaatselt, kui hankija aktseptib need ilma muudatusteta.
- **Aktiivne (ostutellimust ei kinnitata automaatselt)** – teie organisatsioon peab OT-d käsitsi kinnitama pärast seda, kui hankija on need aktseptinud.

### <a name="specifying-whether-the-vendor-should-see-price-information"></a>Hankijale hinnateabe kuvamise määramine

Hankija koostööliidesese kaudu OT-de hinnateabe jagamiseks peate hankija konto puhul vahekaardil **Ostutellimuse vaikeandmed** suvandi **Ostutellimuste hinnad/summa** väärtuseks määrama **Jah**. Hinnateave sisaldab ühikuhinda, allahindlusi ja tasusid.

## <a name="working-with-pos-when-vendor-collaboration-is-used"></a>OT-dega töötamine hankija koostööd kasutades

### <a name="sending-a-po-to-a-vendor"></a>OT saatmine hankijale

OT-d valmistatakse ette rakenduses Finance and Operations. Kui OT olek on **Kinnitatud**, saate selle hankijale saata, valides lehel **Ostutellimus** tegevuse **Kinnitamiseks saatmine**. Seejärel saab OT olekuks **Välisel ülevaatamisel**. Kui ostutellimus on saadetud, näeb hankija seda hankija koostöö liidese lehel **Ülevaatamist ootavad ostutellimused**. Seejärel võib hankija OT aktseptida, tagasi lükata või sellele muudatusi soovitada. Hankija saab lisada ka kommentaare teabe (nt ostutellimuse muudatuste) edastamiseks. Kui soovite juhtida hankija tähelepanu uuele OT-le, võite prindihalduse süsteemi kasutades OT meiliga saata.

### <a name="confirmation-and-acceptance-of-a-po-by-a-vendor"></a>OT kinnitamine ja vastuvõtmine hankijalt

Kui hankija on OT aktseptinud, saab OT kas automaatselt kinnitada või tuleb seda teha käsitsi. Seda olenevalt sellest kas väli **Koostöö aktiveerimine** on hankija puhul seatud olekusse **Aktiivne (ostutellimus kinnitatakse automaatselt)** või olekusse **Aktiivne (ostutellimust ei kinnitata automaatselt)**.

Järgmises tabelis näidatakse tavapärast teabevahetust, mis oleneb sellest, kuidas hankija vastab, kui saadate OT talle kinnitamiseks.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr>
<th>Hankija vastus</th>
<th>Tulemus</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td>Hankija <strong>aktseptib</strong> tellimuse ja rakendus Finance and Operations on konfigureeritud automaatselt hankija aktseptitud OT-d kinnitama.</td>
<td>Tellimuse olekuks määratakse <strong>Kinnitatud</strong>. Kui mingil põhjusel pole võimalik tellimust värskendada, salvestatakse hankija vastuseks ikkagi <strong>Aktsepteeritud</strong>, kuid OT olekuks jääb <strong>Välisel ülevaatamisel</strong>. 

OT, mis saadeti hankijale ja mille olek on <strong>Välisel ülevaatamisel</strong>, värskendatakse, lisades ridadele kinnitatud tarnekuupäevad. See värskendus algatab uue versiooni, mille olekuks määratakse automaatselt <strong>Kinnitatud</strong>. Kui OT kinnitatakse, ilmub see hankija koostööliidesesse.</td>
</tr>
<tr class="odd">
<td>Hankija <strong>aktseptib</strong> tellimuse, kuid rakendus Finance and Operations pole konfigureeritud automaatselt hankija aktseptitud OT-d kinnitama.</td>
<td>Hankija vastus salvestatakse kui <strong>Aktsepteeritud</strong>, kuid ostutellimuse olekuks jääb <strong>Välisel ülevaatamisel</strong>.

OT, mis saadeti hankijale ja mille olek on <strong>Välisel ülevaatamisel</strong>, värskendatakse, lisades ridadele kinnitatud tarnekuupäevad. See värskendus algatab uue versiooni, mille olekuks määratakse automaatselt <strong>Välisel ülevaatamisel</strong>. Seejärel saate OT käsitsi kinnitada.</td>
</tr>
<tr class="even">
<td>Hankija <strong>lükkab</strong> tellimuse tagasi.</td>
<td>Hankija vastus salvestatakse kui <strong>Tagasi lükatud</strong> ja ostutellimus jääb olekusse <strong>Välisel ülevaatamisel</strong>. Tagasilükkamine saadakse koos hankija märkusega.</td>
</tr>
<tr class="odd">
<td>Hankija <strong>aktseptib</strong> tellimuse <strong>muudatustega</strong>. Muudatusi soovitatakse reatasemel. Hankija võib üksikuid ridu aktseptida või tagasi lükata. Järgnevalt on toodud näiteid muudatustest, mida hankija võib soovida teha.
<ul>
<li>Muutke kuupäevi või koguseid.</li>
<li>Eri tarnekuupäevade ja -koguste jaoks saate ridu tükeldada.</li>
<li>Asendage üksus.</li>
</ul>
Hankija ei saa muuta hinnateavet ja kulusid. Siiski saab hankija neid muudatusi märkusi kasutades soovitada.</td>
<td>Hankija vastus salvestatakse kui <strong>Aktsepteeritud koos muudatustega</strong> ja ostutellimuse olekuks jääb <strong>Välisel ülevaatamisel</strong>. Olekud näitavad, millist tüüpi muudatusi hankija on soovitanud. Muudatuste automaatse tarbimise kohta leiate teavet allpool olevast jaotisest „Ostutellimuse uuendamine, kui hankija soovitab muudatusi”. </td>
</tr>
</tbody>
</table>

Jälgimaks, millistele OT-dele hankija on vastanud, saate kasutada tööruumi **Ostutellimuse ettevalmistus**. See tööruum sisaldab kahte loendit, milles on OT-d olekuga **Välisel ülevaatamisel**.

- Välisel ülevaatamisel nõuab tegevust
- Välisel ülevaatusel hankija vastuse ootel

### <a name="changing-a-po"></a>Ostutellimuse muutmine

Juba vastatud OT muutmiseks peate hankijale saatma OT uue versiooni. Uuel OT-l on versiooni järelliide näitamaks, et see on varem saadetud OT muudetud versioon. Leht **Ostutellimuse hankija kinnitamise ajalugu** võimaldab teil ja teie hankijatel jälgida iga tellimuse ajalugu. Ostutellimuse varem kinnitatud versioon jääb uue ostutellimuse kinnitamiseni kinnitatud ostutellimuste nimekirja.

### <a name="canceling-a-po"></a>Ostutellimuse tühistamine

Ostutellimuse tühistamisel muudetakse olekuks uuesti **Aktsepteeritud**. Peate ostutellimuse hankijale tagasi saatma, et ta saaks tühistamise kinnitada või tagasi lükata. Pärast tühistamise kinnitamist kuvatakse ostutellimus hankija kinnitatud ostutellimuste loendis olekuga **Tühistatud**.

### <a name="adding-attachments-to-a-po"></a>Ostutellimusele manuste lisamine

Ostutellimusele saate lisada manuseid, nagu failid, pildid ja märkused, kasutades dokumendihalduse süsteemi. Manused tüübiga **Väline** on hankijale nähtavad, kui ostutellimuse saadate.

## <a name="updating-a-po-when-a-vendor-suggests-changes"></a>Ostutellimuse uuendamine, kui hankija soovitab muudatusi

Kui hankija on OT-le vastanud ja soovitanud muudatusi, on järgmine etapp vastuse töötlemine.

OT-sid, mille hankija on muudatustega aktseptinud, näete loendis **Välisel ülevaatamisel nõuab tegevust** tööruumis **Ostutellimuse ettevalmistamine**. Sellest loendist saate liikuda ka hankija vastuse juurde.

Hankija saab vastuse päises muuta järgmisi andmeid.
 
- Hankija dokumendiviide
- Tarneviis
- Tarnetingimus
- Kinnitatud tarnekuupäev

Hankija saab lisada ka märkuse või manuse.

Ridadel saab hankija muuta kogust ja tarnekuupäevi, lisada märkusi ja manuseid, lükata rea tagasi, asendada rea mõne teise kaubaga, mis on sisestatud tekstina, ja tükeldada rea mitmeks tarneks. Rea olek oleneb sellest, milliseid muudatusi hankija on soovitanud.
    
- **Aktsepteeritud koos muudatustega**
- **Tagasilükatud**
- **Asendatud** – sel juhul lisatakse rida, mille olek on **Asendamine**.
- **Kinnitatud**
- **Tükeldamine graafikusse** – sel juhul lisatakse read, mille olek on **Graafiku read**.

Kui real pole muudatusi, on rea olek **Aktsepteeritud**.

Vastusel näete reaolekuid, mis näitavad hankija tehtud muudatuste tüüpe. Lisaks kuvatakse kõik muudetud väljad paksus kirjas, et saaksite muudatused tuvastada.

Saate OT-d värskendada, valides vastusel või ühel real korraga tegevuse **Töötle ostutellimuse värskendust**. Päises ja ridadel olev väli **Kas ostutellimuse värskendus on töödeldud?** võimaldab tuvastada, kas süsteem on päist või ridu töödelnud, et värskendada OT-d mis tahes võimalike vastusest pärinevate muudatustega. Tegevuse **Töötle ostutellimuse värskendust** saab käivitada päise või rea kohta ainult ühe korra.

Kõiki soovituslikke muudatusi ei saa ostutellimusel muuta. OT-l saab automaatselt teha ainult päise värskendusi ning kuupäevade ja koguste värskendusi ridadel. Teiste muudatuste puhul tuleb ostutellimust käsitsi uuendada. Sel juhul on välja **Kas ostutellimuse värskendus on töödeldud?** väärtus **Käsitsi värskendamine**. Näiteks kui hankija soovib, et rida tükeldataks graafikuks, tuleb see muudatus teha käsitsi.

Iga olekuga **Aktsepteeritud** rea tarnekuupäev on kinnitatud. Kui käitate tegevuse **Töötle ostutellimuse värskendust**, värskendatakse OT-l seda kuupäeva. Märkusi ja manuseid ei edastata automaatselt praegusse OT-sse. Peale selle ei hinnata ümber kaubandusleppeid OT ridadel, kui värskendate praegust OT-d toiminguga **Töötle ostutellimuse värskendust**.

## <a name="po-statuses-and-versions"></a>Ostutellimuse olekud ja versioonid

See jaotis kirjeldab erinevaid olekuid, mis OT-l võivad kuni kinnitamiseni olla. Samuti kirjeldab see, millal uued OT versioonid hankijale kättesaadavaks tehakse. Käitumine erineb, olenevalt sellest, kas kasutate ostutellimuste puhul muudatuste haldamist. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Versioonid ja olekud, kui te ei kasuta muudatusehaldust

Järgmises tabelis on näide oleku ja versiooni muudatuste kohta, mida ostutellimuses teha saab.

| Tegevus | Olek ja versioon |
|--------|--------------------|
| Ostutellimuse algne versioon luuakse rakenduses Finance and Operations. | Olek on **Kinnitatud**. |
| Ostutellimus saadetakse hankijale. | Versioon registreeritakse hankija koostöö liideses ja olekuks muudetakse **Välisel ülevaatamisel**. |
| Hankija saadab vastuse **Aktsepteeritud koos muudatustega** | Olek on ikka **Välisel ülevaatamisel**. |
| Teete mõningaid hankija soovitud muudatusi. | Olekuks saab **Kinnitatud**. |
| Saadate ostutellimuse uue versiooni hankijale. | Uus versioon registreeritakse hankija koostöö liideses ja olekuks muudetakse **Välisel ülevaatamisel**. |
| Hankija aktsepteerib ostutellimuse uue versiooni. | Olek on endiselt **Välisel ülevaatamisel**, välja arvatud juhul, kui hankija konto konfigureeritakse OT-sid automaatselt olekusse **Kinnitatud** määrama, kui hankija need aktseptib. |

Hankijad ei pea OT-d hankija koostööliidese kaudu kinnitama. Nad võivad saata ka meili või teatada ostutellimuse vastuvõtmisest muude kanalite kaudu. Seejärel saate tellimuse käsitsi rakenduses Finance and Operations kinnitada. Sellisel juhul saate hoiatuse, et tellimus on kinnitatud, kuigi hankijalt puudub vastus. Seejärel kuvatakse ostutellimus kinnitusajaloos avatud kinnitatud tellimusena, millel puuduvad vastused. Nüüd pole hankijal enam võimalik ostutellimust kinnitada ega tagasi lükata.

> [!NOTE]
> Ostutellimuse versioon, mis on saadaval teistele protsessidele rakenduses Finance and Operations, on alati värskeim versioon isegi juhul, kui seda versiooni pole veel registreeritud hankija koostööliideses.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Versioonid ja olekud, kui kasutate muudatusehaldust

Kui muudatusehaldus on ostutellimuste jaoks lubatud, läbivad ostutellimused kinnitamise töövoo, et saavutada olek **Kinnitatud**. See protsess ei ole hankijale nähtav.

Järgmises tabelis on näide oleku ja versiooni muudatustest, mida ostutellimusse teha võidakse, kui muudatuste haldamine on sisse lülitatud. Versioon registreeritakse OT kinnitamisel, mitte siis, kui OT saadetakse hankijale või kinnitatakse.

| Tegevus | Olek ja versioon |
|--------|--------------------|
| Ostutellimuse algne versioon luuakse rakenduses Finance and Operations. | Olek on **Mustand**. |
| Ostutellimus esitatakse kinnitusprotsessile. (Kinnitusprotsess on sisemine protsess, millesse hankija pole kaasatud.) | Olek **Mustand** muutub olekuks **Ülevaatamisel** ja siis olekuks **Kinnitamine**, kui ostutellimust kinnitamisprotsessi ajal tagasi ei lükata. Kinnitatud ostutellimus registreeritakse versioonina. | 
| Ostutellimus saadetakse hankijale. | Versioon registreeritakse hankija koostöö liideses ja olekuks muudetakse **Välisel ülevaatamisel**. |
| Vastuseks teete OT värskendamiseks muudatusi, mida hankija soovis, kas käsitsi või kasutades tegevust **Töötle ostutellimuse värskendust**. | Olekuks määratakse uuesti **Mustand**. |
| Ostutellimus esitatakse uuesti kinnitusprotsessile. | Olek **Mustand** muutub olekuks **Ülevaatamisel** ja siis olekuks **Kinnitamine**, kui ostutellimust kinnitamisprotsessi ajal tagasi ei lükata. Teise võimalusena saab süsteemi konfigureerida nii, et konkreetsete välja muudatuste jaoks ei ole vaja uuesti kinnitamist. Sellisel juhul määratakse olekuks kõigepealt **Mustand** ja seejärel automaatselt **Kinnitatud**. Kinnitatud ostutellimus registreeritakse uue versioonina. |
| Saadate ostutellimuse uue versiooni hankijale. | Uus versioon registreeritakse hankija koostöö liideses ja olekuks muudetakse **Välisel ülevaatamisel**. |
| Hankija kinnitab ostutellimuse uue versiooni. | Olekuks määratakse **Kinnitatud**, kas automaatselt või siis, kui saate hankijalt vastuse ja kinnitate siis ostutellimuse. |

## <a name="sharing-information-about-consignment-inventory"></a>Veose varude kohta teabe jagamine

Kui kasutate veose varusid, saavad hankijad kasutada hankija koostööliidest, et kuvada teavet järgmistel lehtedel.

- **Ostutellimused, mis tarbivad veose varusid** – OT-d veose varude jaoks luuakse siis, kui varude omandiõigus läheb hankijalt teie ettevõttele. Toote sissetulek sisestatakse samal ajal. Need veose OT-d kuvatakse ainult lehel **Ostutellimused, mis tarbivad veose varusid**. Neid ei kaasata lehele **Kõik kinnitatud ostutellimused** moodulis **Hankija koostöö**.
- **Veose varudest saadud tooted** – see leht loetleb kõik kanded, kus toodete omandiõigus on hankijalt teie ettevõttele üle viidud. Hankijad saavad kasutada seda teavet, et kliendile arvet esitada.
- **Veose vaba kaubavaru** – see leht näitab hankijale kuuluvaid vabu veose varusid, mis on teie lattu vastu võetud.

## <a name="working-with-rfqs-when-you-use-vendor-collaboration"></a>Pakkumiskutsetega töötamine hankija koostööd kasutades

See jaotis kirjeldab klientide ja hankijate omavahelist suhtlust pakkumiskutse protsessi käigus. See selgitab ka, kuidas hankijatele teavet edastatakse. Pakkumiskutse protsessi toest põhiülevaate saamiseks vaadake jaotist [„Pakkumiskutsed (RFQ-d)”](request-quotations.md).

### <a name="alternates-attachments-amendments-and-returns"></a>Alternatiivid, manused, parandused ja tagastused

- **Alternatiivid** – kui kataloogiväliste kaubaridade puhul on lubatud alternatiivid, siis näete seda pakkumiskutse päises. Kui alternatiivid on lubatud, saavad hankijad igale taotletud reale alternatiivseid ridu lisada.
- **Manused** – manuseid saab lisada nii pakkumiskutse päise kui ka rea tasemel. Manuseid saab liigitada kas sisemisteks või välisteks. Sisemisi manuseid saab vaadata ainult kliendi poolel, samas kui hankijad saavad väliseid manuseid vaadata alles pärast saatmist.

    Samuti saavad hankijad oma pakkumise vastusele manuseid lisada. Kliendi poolel saab neid manuseid vaadata pärast seda, kui hankija on pakkumise vastuse esitanud. Hankijate lisatud manused liigitatakse alati välisteks. Hankija pakkumisega esitatud manuste vaatamiseks valige **Pakkumise manused** või **Pakkumise rea manused**.
    
    Pakkumiskutsega koos saadetud manuste vaatamiseks kasutage vastuses olevat dokumentide töötlemise kirjaklambri sümbolit.

- **Parandused** – kui parandus on lõpule viidud, eemaldatakse olemasolevad pakkumise vastused, nii et need saaks asendada värskendatud väärtustega. Varasema pakkumise vastuses olevat teavet rea hinna ja koguse kohta saab vaadata pakkumiskutse juhtumi töölehtedelt.

    Paranduse töötlemise jõustamiseks määrake lehe **Hangete parameetrid** kiirkaardi **Pakkumiskutsed** suvandi **Lukusta saadetavad pakkumiskutsed** väärtuseks **Jah**. (Avaliku sektori puhul on see suvand seatud ja nõutav.)

- **Tagastused** – kui hankija on edastanud pakkumise, kuid pakkumiskutse juhtumi puhul on nõutud rohkem või muudetud teavet, saab klient pakkumise hankijale tagasi saata. Varem edastatud pakkumise andmed säilitatakse ja hankija saab nõutud muudatused teha ilma pakkumise protsessi uuesti alustamata.

## <a name="public-sector-extensions"></a>Avaliku sektori laiendused

Avaliku sektori laiendatud funktsioonid võimaldavad pakkumiskutse juhtumi hankijatele saata ja avaldada. Pakkumiskutse avaldamisel saavad kõik, kes teabenõude esitavad, tööd vaadata, mis on kooskõlas enamike avalikku sektorit puudutavate määrustega. Kõik saadaolevad tööd kuvatakse loendilehel **Avaldatud pakkumiskutsete avamine** ja tühistatud, ootel või lõppenud pakkumiskutseid saab vaadata loendilehel **Suletud avaldatud pakkumiskutsed**. Neid dokumente saab vaadata ka väljaspool rakendust Finance and Operations järgmiste andmeüksuste integreerimise kaudu.

- Avaldatud pakkumiskutsed
- Avaldatud pakkumiskutsete rida
- Avaldatud pakkumiskutsete päise manused

Need üksused lasevad inimestel, kes pole rakenduse Finance and Operations lepingulised kasutajad, kuid kellel on anonüümne juurdepääs välisele saidile, vaadata saadaolevaid ja suletud töid. Lisaks annab suvandi **Saada ja avalda** laiendatud funktsionaalsus kasutajale, kes seadistab pakkumiskutse protsessi parameetrid, võimaluse määrata meilimall. Kui hankespetsialist loob nüüd pakkumiskutse juhtumi, peab ta pakkumiskutse juhtumi puhul nõutava teabe saatmiseks hankijatele valima meilimalli. 

Kasutaja, kes pakkumiskutse protsessi parameetreid määrab, saab luua mitu meilimalli. Need meilimallid võivad sisaldada nii staatilist teksti kui ka järgmisi asendussõnesid. Meili loomisel asendatakse sõned konteksti puudutavate väärtustega.

- %RFQCase%
- %RFQCaseName%
- %bidType%
- %inviteOnly%
- %expiryDateTime%
- %requester%
- %requestingDepartment%
- %accountnum%
- %todaysdate%
- %createddate%

Kui parandus on vajalik ja saadetakse pärast pakkumiskutse saatmist, saadetakse pakkumiskutse kõigile kutsutud hankijatele uuesti. Samuti uuendatakse avaldatud dokumenti lehel **Avaldatud pakkumiskutsete avamine**.

