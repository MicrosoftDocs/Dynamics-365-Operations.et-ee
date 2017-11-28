---
title: "Hankija koostöö väliste hankijatega"
description: "See teema kirjeldab, kuidas ostuagendid saavad teha koostööd väliste hankijatega, et vahetada teavet ostutellimuste ja veose varude kohta."
author: mkirknel
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
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
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: abff906bcdf31c91ce696afbcd651a1d7a87ea8a
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="vendor-collaboration-with-external-vendors"></a>Hankija koostöö väliste hankijatega

[!include[banner](../includes/banner.md)]


See teema kirjeldab, kuidas ostuagendid saavad teha koostööd väliste hankijatega, et vahetada teavet ostutellimuste ja veose varude kohta.

Moodul **Hankija koostöö** on suunatud hankijatele, kellel puudub elektroonilise andmete vahetuse (EDI) integratsioon rakendusega Microsoft Dynamics 365 for Finance and Operations. See võimaldab hankijatel töötada ostutellimuse, arve ja veose varude teabega. See teema kirjeldab, kuidas saate teha koostööd väliste hankijatega, kes kasutavad hankija koostöö liidest ostutellimuste ja veoste varudega töötamiseks. See kirjeldab ka, kuidas lubada konkreetset hankijat hankija koostöö kasutamiseks ja kuidas määratleda teavet, mida kõik hankijad näevad, kui nad vastavad ostutellimusele. Lisateavet selle kohta, mida välised hankijad saavad hankija koostöö liideses teha, leiate teemast [Hankija koostöö klientidega](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Teemas kirjeldatud teave hankija koostöö kohta kehtib ainult Dynamics 365 for Finance and Operationsi praeguse versiooni puhul. Microsoft Dynamics AX-i 2016. aasta veebruari ja 2016. aasta mai versioonis kasutate hankijatega koostöö tegemiseks hankijaportaali moodulit. Hankijaportaali mooduli kohta teabe saamiseks vt [Hankijatega koostöö tegemine hankijaportaali abil](collaborate-vendors-vendor-portal.md).

Lisateavet selle kohta, kuidas hankijad saavad kasutada hankija koostööd arveldamise protsessides, leiate teemast [Hankija koostöö arve tööruum](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md). Lisateavet selle kohta, kuidas ette valmistada uue hankija koostöö kasutajaid, leiate teemast [Hankija koostöö kasutajate haldamine](manage-vendor-collaboration-users.md).

Lisateavet selle kohta, kuidas hankijad saavad kasutada hankija koostööd arveldamise protsessides, leiate teemast [Hankija koostöö arve tööruum](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md). 

Lisateavet selle kohta, kuidas ette valmistada uue hankija koostöö kasutajaid, leiate teemast [Hankija koostöö kasutajate haldamine](manage-vendor-collaboration-users.md).

## <a name="define-the-information-that-is-shown-to-vendors-when-they-respond-to-pos"></a>Hankijatele näidatud teabe määratlemine, kui nad vastavad ostutellimustele
Kui hankijad vastavad ostutellimusele, mille neile saadate, näevad nad sõnumiboksi, kus nad peavad kinnitama, et soovivad ostutellimuse muudatustega aktsepteerida või tagasi lükata. Kuna teave, mis tuleb sellel hetkel hankijale kuvada, võib olla teie ettevõtte põhine, saate määrata teksti, mis kuvatakse igal kolmest kinnitusteatest. Näiteks võib tekst teavitada hankijat järgmistest protsessi etappidest või tingimustest.  

Ostutellimuse vastuses näidatava teksti määratlemiseks:

1.  Avage leht **Teave ostutellimustele vastavate hankijate jaoks**.
2.  Valige üks vastuse tüüpidest.
3.  Klõpsake valikut **Redigeeri**.
4.  Sisestage teave, mida soovite, et hankijad näeksid boksis **Teabeteade**.

Kui peate lisama teateid rohkem kui ühes keeles, koostage eraldi teated ja määrake neist igaühele sobivad keelekoodid. Hankijale kuvatav teade on hankija kasutatavas keeles.

## <a name="set-the-vendor-collaboration-options-for-a-specific-vendor"></a>Hankija koostöö valikute seadistamine konkreetsele hankijale
Rakenduses Finance and Operations konfigureerib administraator üldised hankija koostöö sätted. Näiteks määrab administraator, millised turberollid on saadaval kõikidele hankijatele, kellega koostööd teete. On ka mõned sätted, mis võivad olla iga hankija konto puhul erinevad, ja need tuleb määrata järgmiselt.
-   Lubage hankija koostöö.
-   Otsustage, kas soovite, et hankija näeks hinna teavet.

### <a name="enable-vendor-collaboration"></a>Hankija koostöö lubamine

Enne kui välise hankija jaoks saab kasutajakontosid luua, peate konfigureerima hankijakonto, et lubada neil hankija koostööd kasutada. Selleks määrake väli **Koostöö aktiveerimine** aktiivseks vahekaardil **Üldine** lehel **Hankijad**. On kaks valikut, mida saate teha:

-   **Aktiivne (ostutellimus kinnitatakse automaatselt)**– ostutellimused kinnitatakse automaatselt, kui hankija aktsepteerib need ilma muudatusteta.
-   **Aktiivne (ostutellimust ei kinnitata automaatselt)**– teie organisatsioon peab ostutellimused käsitsi kinnitama pärast seda, kui hankija on neid aktsepteerinud.

### <a name="decide-whether-you-want-the-vendor-to-see-price-information"></a>Otsustage, kas soovite, et hankija näeks hinna teavet.

Kui soovite jagada hinnateavet, nagu ühikuhind, allahindlused ja tasud, koostööliidese kaudu, peate määrama suvandi **Ostutellimuste hinnad/summa** hankija kontol sättele **Jah**. See suvand on saadaval vahekaardil **Ostutellimuse vaikeandmed**.

## <a name="work-with-pos-when-using-vendor-collaboration"></a>Hankija koostööd kasutades ostutellimustega töötamine
### <a name="sending-a-po-to-the-vendor"></a>Ostutellimuse hankijale saatmine

Ostutellimused valmistatakse ette rakenduses Finance and Operations. Kui ostutellimusel on olek **Aktsepteeritud**, saadate selle hankijale, kasutades tegevust **Kinnitamiseks saatmine** lehel **Ostutellimus**. Ostutellimuse olekuks saab **Välisel ülevaatamisel**. Kui ostutellimus on saadetud, näeb hankija seda hankija koostöö liidese lehel **Ülevaatamist ootavad ostutellimused**. Seejärel võib hankija tellimuse vastu võtta, tagasi lükata või sellele muudatusi soovitada. Hankija saab lisada ka kommentaare teabe (nt ostutellimuse muudatuste) edastamiseks. Kui soovite juhtida hankija tähelepanu uuele ostutellimusele, võite ostutellimuse saatmiseks meiliga kasutada prindihalduse süsteemi.

### <a name="confirmation-and-acceptance-of-the-po-by-the-vendor"></a>Ostutellimuse kinnitamine ja vastuvõtmine hankijalt

Kui hankija on ostutellimuse aktsepteerinud, saab ostutellimuse automaatselt kinnitada või see tuleb vajadusel käsitsi kinnitada. See sõltub sellest, kas väli **Hankija aktiveerimine** on hankija puhul seatud olekusse **Aktiivne (ostutellimus kinnitatakse automaatselt)** või olekusse **Aktiivne (ostutellimust ei kinnitata automaatselt)**.  

Järgmises tabelis näidatakse tavapärast teabevahetust, mis oleneb sellest, kuidas hankija vastab, kui saadate talle kinnitamiseks ostutellimuse.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Hankija vastus</strong></td>
<td><strong>Tulemus</strong></td>
</tr>
<tr class="even">
<td>Hankija <strong>aktsepteerib</strong> tellimuse. Finance and Operations on konfigureeritud hankija aktsepteerimise korral automaatselt ostutellimusi kinnitama.</td>

<td>Tellimuse olekuks määratakse <strong>Kinnitatud</strong>. Kui miski takistab tellimuse värskendamist, salvestatakse hankija vastuseks ikkagi <strong>Aktsepteeritud</strong>, kuid ostutellimuse olekuks jääb <strong>Välisel ülevaatamisel</strong>. 

Ostutellimust, mis saadeti hankijale ja mille olek on **Välisel ülevaatamisel**, uuendatakse, lisades ridadele kinnitatud tarnekuupäevad. Uuendus algatab uue versiooni, mille olekuks määratakse automaatselt **Kinnitatud**. Kui ostutellimus kinnitatakse, ilmub see hankija koostöö liidesesse.</td>
</tr>
<tr class="odd">
<td>Hankija <strong>aktsepteerib</strong> tellimuse. Finance and Operations ei ole konfigureeritud hankija aktsepteerimise korral automaatselt ostutellimusi kinnitama.</td>
<td>Hankija vastus salvestatakse kui <strong>Aktsepteeritud</strong>, kuid ostutellimuse olekuks jääb <strong>Välisel ülevaatamisel</strong>.

Ostutellimust, mis saadeti hankijale ja mille olek on **Välisel ülevaatamisel**, uuendatakse, lisades ridadele kinnitatud tarnekuupäevad. Uuendus algatab uue versiooni, mille olekuks määratakse **Välisel ülevaatamisel**. Seejärel saate ostutellimuse käsitsi kinnitada.</td>

</tr>
<tr class="even">
<td>Hankija <strong>lükkab</strong> tellimuse tagasi.</td>
<td>Hankija vastus salvestatakse kui <strong>Tagasi lükatud</strong> ja ostutellimus jääb olekusse <strong>Välisel ülevaatamisel</strong>. Tagasilükkamine saadakse koos hankija märkusega.</td>
</tr>
<tr class="odd">
<td>Hankija <strong>kinnitab tellimuse muudatustega</strong>. Muudatusi soovitatakse reatasemel. Üksikuid ridu on võimalik aktsepteerida või tagasi lükata. Muud võimalikud muudatused hõlmavad:
<ul>
<li>Kuupäevad või koguste muutmine.</li>
<li>Ridade tükeldamine erinevate tarnekuupäevade ja -koguste jaoks.</li>
<li>Kauba asendamine.</li>
</ul>
Hankija ei saa hinnateavet ja kulusid muuta. Nendele muudatuste tegemise soovitusi saab teha märkuseid kasutades.</td>
<td>Hankija vastus salvestatakse kui <strong>Aktsepteeritud koos muudatustega</strong> ja ostutellimuse olekuks jääb <strong>Välisel ülevaatamisel</strong>. Olekud näitavad, millist tüüpi muudatusi hankija on soovitanud. Teavet muudatuste automaatse tarbimise kohta leiate järgmisest jaotisest, mis käsitleb seda, kuidas uuendada ostutellimust, kui hankija soovitab muudatusi. </td>
</tr>
</tbody>
</table>

Saate kasutada tööruumi **Ostutellimuse** **ettevalmistus**, et jälgida, millistele ostutellimustele on hankija vastanud. See tööruum sisaldab kaht loendit, mis sisaldab olekuga **Välisel ülevaatamisel** ostutellimusi.

-   Välisel ülevaatamisel nõuab tegevust.
-   Välisel ülevaatusel hankija vastuse ootel.

### <a name="changing-a-po"></a>Ostutellimuse muutmine

Juba vastatud ostutellimuse muutmiseks peate hankijale saatma ostutellimuse uue versiooni. Uuel ostutellimusel on versiooni järelliide näitamaks, et see on varasemalt kommunikeeritud ostutellimuse modifitseeritud versioon. Leht **Ostutellimuse hankija kinnitamise ajalugu** võimaldab teil ja teie hankijatel jälgida iga tellimuse ajalugu. Ostutellimuse varem kinnitatud versioon jääb uue ostutellimuse kinnitamiseni kinnitatud ostutellimuste nimekirja.

### <a name="cancelling-a-po"></a>Ostutellimuse tühistamine

Ostutellimuse tühistamisel muudetakse olekuks uuesti **Aktsepteeritud**. Peate ostutellimuse hankijale tagasi saatma, et ta saaks tühistamise kinnitada või tagasi lükata. Pärast tühistamise kinnitamist ilmub ostutellimus kinnitatud ostutellimuste hankija loendis kui **Tühistatud**.

### <a name="adding-attachments-to-a-po"></a>Ostutellimusele manuste lisamine

Ostutellimusele saate lisada manuseid, nagu failid, pildid ja märkused, kasutades dokumendihalduse süsteemi. Manused tüübiga **Väline** on hankijale nähtavad, kui ostutellimuse saadate.

## <a name="update-the-po-when-a-vendor-suggests-changes"></a>Ostutellimuse uuendamine, kui hankija soovitab muudatusi
Kui hankija on ostutellimusele vastanud ja soovitanud muudatusi, on järgmine etapp vastuse töötlemine.
**Ostutellimuse ettevalmistamise tööruumi** loendis Välisel ülevaatamisel nõuab tegevust saate märkida ostutellimuse, millele hankija vastas, muudatustega aktsepteeritud tellimuseks. Loendis Välisel ülevaatamisel nõuab tegevust saate liikuda ka hankija vastuse juurde. Vastuse päises saab hankija muuta järgmisi andmeid.
 
-   Hankija dokumendiviide
-   Tarneviis
-   Tarnetingimus
-   Kinnitatud tarnekuupäev

Hankija saab lisada ka märkuse või manuse

Ridadel saab hankija muuta kogust ja tarnekuupäevi, lisada märkusi ja manuseid, lükata rea tagasi, asendada rea mõne teise kaubaga, mis on sisestatud tekstina, ja jagada rea mitmeks tarneks. Olenevalt sellest, milliseid muudatusi hankija soovitab, on rea olekud erinevad.
    
-   **Aktsepteeritud koos muudatustega**
-   **Tagasi lükatud**
-   **Asendatud** – sel juhul lisatakse rida, mille olek on **Asendamine**.
-   **Kinnitatud** Tükeldamine graafikusse Sel juhul lisatakse read, mille olek on **Graafiku read**.

Kui real pole muudatusi, on rea olek **Aktsepteeritud**.

Vastusel näete varem nimetatud reaolekuid, mis näitavad hankija tehtud muudatuste tüüpi. Lisaks kuvatakse kõik muudetud väljad paksus kirjas, et saaksite muudatused tuvastada.

Saate ostutellimust uuendada, klõpsates vastusel või ühel real korraga tegevust **Töötle ostutellimuse uuendust**. Päises ja ridadel olev tähis **Kas ostutellimuse uuendus on töödeldud?** võimaldab näha, kas süsteem on päist või ridu töödelnud, et uuendada ostutellimust mis tahes võimalike vastusest pärinevate muudatustega. Protsessi **Töötle ostutellimuse uuendust** saab käivitada päise või rea kohta ainult ühe korra.

Kõiki soovituslikke muudatusi ei saa ostutellimusel muuta. Ostutellimusel saab automaatselt teha ainult päise uuendusi ning kuupäevade ja koguste uuendusi ridadel. Teiste muudatuste puhul tuleb ostutellimust käsitsi uuendada. Praegusel juhul näitab tähis **Kas ostutellimuse uuendus on töödeldud?** olekut **Käsitsi uuendamine**. Näide muudatuse kohta, mida tuleb teha käsitsi, on see, kui hankija soovitab tükeldada rea graafikuks.

Real, mille olek on **Aktsepteeritud**, on kinnitatud tarnekuupäev, mis uuendatakse ostutellimusel, kui käivitate käsu **Töötle ostutellimuse uuendust**. Märkusi ja manuseid ei edastata automaatselt praegusse ostutellimusse. Pange tähele, et kui uuendate praegust ostutellimust toiminguga **Töötle ostutellimuse uuendust**, ei hinnata kaubandusleppeid ostutellimuse ridadel ümber.


## <a name="po-statuses-and-versions"></a>Ostutellimuse olekud ja versioonid
See jaotis kirjeldab erinevaid olekuid, mis ostutellimusel võivad kinnitamiseni olla. Samuti kirjeldab see, mis hetkel uued ostutellimuse versioonid hankijale kättesaadavaks tehakse. Käitumine erineb, olenevalt sellest, kas kasutate ostutellimuste puhul muudatuste haldamist. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Versioonid ja olekud, kui te ei kasuta muudatusehaldust

Järgmises tabelis on näide oleku ja versiooni muudatuste kohta, mida ostutellimuses teha saab.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tegevus**                                                               | **Olek ja versioon**                                                                                                                                       |
| Ostutellimuse algne versioon luuakse rakenduses Finance and Operations. | Olek on **Kinnitatud**.                                                                                                                                  |
| Ostutellimus saadetakse hankijale.                                            | Versioon registreeritakse hankija koostöö liideses ja olekuks muudetakse **Välisel ülevaatamisel**.                                          |
| Hankija saadab vastuse **Aktsepteeritud koos muudatustega**                  | Olek on ikka **Välisel ülevaatamisel**.                                                                                                                  |
| Teete mõningaid hankija soovitud muudatusi.                  | Olekuks saab **Kinnitatud**.                                                                                                                        |
| Saadate ostutellimuse uue versiooni hankijale.                        | Uus versioon registreeritakse hankija koostöö liideses ja olekuks muudetakse **Välisel ülevaatamisel**.                                      |
| Hankija aktsepteerib ostutellimuse uue versiooni.                            | Olek on endiselt **Välisel ülevaatamisel**, välja arvatud juhul, kui hankija konto konfigureeritakse ostutellimust automaatselt olekusse **Kinnitatud** määrama, kui nad selle aktsepteerivad. |


Hankijad ei pea ostutellimust kinnitama, kasutades hankija koostöö liidest. Nad võivad saata ka meilisõnumi või teatama ostutellimuse vastuvõtmisest muude kanalite kaudu. Seejärel saate tellimuse kinnitada käsitsi rakenduses Finance and Operations. Sellisel juhul saate hoiatuse, et tellimus on kinnitatud, kuigi hankijalt puudub vastus. Seejärel kuvatakse ostutellimus kinnitusajaloos avatud kinnitatud tellimusena, millel puuduvad vastused. Hankijal ei ole enam võimalust ostutellimust kinnitada või tagasi lükata.  


>[!NOTE]
>Ostutellimuse versioon, mis on saadaval teistele protsessidele rakenduses Dynamics 365 for Finance and Operations, on alati värskeim versioon isegi juhul, kui seda versiooni pole veel registreeritud hankija koostöö liideses.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Versioonid ja olekud, kui kasutate muudatusehaldust

Kui muudatusehaldus on ostutellimuste jaoks lubatud, läbib ostutellimus kinnitamise töövoo, et saavutada olek **Kinnitatud**. See protsess ei ole hankijale nähtav.  

Järgmises tabelis on näide oleku ja versiooni muudatustest, mida ostutellimusse teha võidakse, kui muudatuste haldamine on sisse lülitatud. Versioon registreeritakse ostutellimuse kinnitamisel, mitte siis, kui ostutellimus saadetakse hankijale või kinnitatakse.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tegevus**                                                               | **Olek ja versioon**                                                                                                                                       |
| Ostutellimuse algne versioon luuakse rakenduses Finance and Operations.      | Olek on **Mustand**.  |
| Ostutellimus esitatakse kinnitusprotsessile. (Kinnitusprotsess on sisemine protsess, millesse hankija ei ole kaasatud.)                                                           | Olek muudetakse olekust **Mustand** olekusse **Ülevaatamisel** ja omakorda olekusse **Kinnitus**, kui ostutellimust ei lükata kinnitamisprotsessi käigus tagasi. Kinnitatud ostutellimus registreeritakse versioonina.           | 
| Ostutellimus saadetakse hankijale.                                                            | Versioon registreeritakse hankija koostöö liideses ja olekuks muudetakse **Välisel ülevaatamisel**.      |
| Teete muudatusi, mida hankija soovib, kas käsitsi või kasutades vastusel olevat tegevust ostutellimuse uuendamiseks.                                                            | Olekuks määratakse uuesti **Mustand**.     |
|Ostutellimus esitatakse uuesti kinnitusprotsessile.                                                |  Olek **Mustand** muutub olekuks **Ülevaatamisel** ja siis olekuks **Kinnitamine**, kui ostutellimust ei lükata kinnitamisprotsessi käigus tagasi. Teise võimalusena saab süsteemi konfigureerida nii, et konkreetse välja muudatused ei nõua uuesti kinnitamist. Sellisel juhul määratakse olekuks kõigepealt **Mustand** ja seejärel automaatselt **Kinnitatud**. Kinnitatud ostutellimus registreeritakse uue versioonina.                                         |
|Saadate ostutellimuse uue versiooni hankijale.                                                |  Uus versioon registreeritakse hankija koostöö liideses ja olekuks muudetakse **Välisel ülevaatamisel**.                                         |
|Hankija kinnitab ostutellimuse uue versiooni.                                                |  Olekuks määratakse **Kinnitatud**, kas automaatselt või siis, kui saate hankijalt vastuse ja kinnitate siis ostutellimuse. |

## <a name="share-information-about-consignment-inventory"></a>Teabe jagamine veose varude kohta
Kui kasutate veose varusid, saavad hankijad kasutada hankija koostöö liidest, et kuvada teavet järgmistel lehtedel:

-   **Ostutellimused, mis tarbivad veose varusid** – ostutellimused veose varude jaoks luuakse siis, kui varude omandiõigus muutub hankijalt teie ettevõttele. Toote sissetulek sisestatakse samal ajal. Need veose ostutellimused kuvatakse ainult lehel **Ostutellimused, mis tarbivad veose varusid**. Neid ei kaasata lehele **Kõik kinnitatud ostutellimused** moodulis **Hankija koostöö**.
-   **Veose varudest saadud tooted** – see leht loetleb kõik kanded, kus toodete omandiõigus on hankijalt teie ettevõttele üle viidud. Hankijad saavad kasutada seda teavet, et kliendile arvet esitada.
-   **Veose vaba kaubavaru** – see leht näitab hankijale kuuluvat vabu veose varusid, mis on teie lattu vastu võetud.





