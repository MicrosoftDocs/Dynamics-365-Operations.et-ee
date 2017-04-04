---
title: "Hankija koostöö väliste hankijatega"
description: "See teema kirjeldab, kuidas ostuagendid saavad teha koostööd väliste hankijatega, et vahetada teavet ostutellimuste ja veose varude kohta."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: d585ae0716a4bd9c3531e8639cd7c6b3cab780ac
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-collaboration-with-external-vendors"></a>Hankija koostöö väliste hankijatega

See teema kirjeldab, kuidas ostuagendid saavad teha koostööd väliste hankijatega, et vahetada teavet ostutellimuste ja veose varude kohta.

Moodul **Hankija koostöö** on suunatud hankijatele, kellel puudub elektroonilise andmete vahetuse (EDI) integratsioon rakendusega Microsoft Dynamics 365 for Operations. See võimaldab hankijatel töötada ostutellimuse, arve ja veose varude teabega. See teema kirjeldab, kuidas saate teha koostööd väliste hankijatega, kes kasutavad hankija koostöö liidest ostutellimuste ja veoste varudega töötamiseks. See kirjeldab ka, kuidas lubada konkreetset hankijat hankija koostöö kasutamiseks ja kuidas määratleda teavet, mida kõik hankijad näevad, kui nad vastavad ostutellimusele. Lisateavet selle kohta, mida välised hankijad saavad hankija koostöö liideses teha, leiate teemast [Hankija koostöö klientidega](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Lisateavet selle kohta, kuidas hankijad saavad kasutada hankija koostööd arveldamise protsessides, leiate teemast [Hankija koostöö arve tööruum](/dynamics365/operations/financials/accounts-payable/vendor-portal-invoicing-workspace). Lisateavet selle kohta, kuidas ette valmistada uue hankija koostöö kasutajaid, leiate teemast [Hankija koostöö kasutajate haldamine](manage-vendor-collaboration-users.md).

## <a name="define-the-information-shown-to-vendors-when-they-respond-to-pos"></a>Hankijatele näidatud teabe määratlemine, kui nad vastavad ostutellimustele
Kui hankijad vastavad ostutellimusele, mille neile saadate, näevad nad dialoogiboksi, kus nad peavad kinnitama, et soovivad ostutellimuse muudatustega aktsepteerida või tagasi lükata. Teave, mis tuleb kuvada hankijale sellel hetkel, võib olla teie ettevõtte spetsiifiline, seega saate määrata teksti, mida näidatakse igal kolmest kinnitusteatest. Näiteks võib tekst teavitada hankijat järgmiste protsessi etappide või tingimuste kohta.  

Ostutellimuse vastuses näidatava teksti määratlemiseks:

1.  Avage leht **Teave ostutellimustele vastavate hankijate jaoks**.
2.  Valige üks vastuse tüüpidest.
3.  Klõpsake valikut **Redigeeri**.
4.  Sisestage teave, mida soovite, et hankijad näeksid boksis **Teabeteade**.

Kui peate lisama teateid rohkem kui ühes keeles, looge sobivate keelekoodidega eraldi teated. Hankijale näidatakse teadet keeles, mida nad kasutavad.

## <a name="set-the-vendor-collaboration-options-for-a-specific-vendor"></a>Hankija koostöö valikute seadistamine konkreetsele hankijale
Rakenduses Dynamics 365 for Operations konfigureerib administraator üldised hankija koostöö sätted. Näiteks määravad nad, millised turberollid on saadaval kõikidele hankijatele, kellega koostööd teete. On ka mõned sätted, mis võivad erineda iga hankija konto puhul ja te peaks määrama need.

-   Lubage hankija koostöö.
-   Otsustage, kas soovite, et hankija näeks hinna teavet.

### <a name="enable-vendor-collaboration"></a>Hankija koostöö lubamine

Enne kui välise hankija jaoks saab kasutajakontosid luua, peate konfigureerima hankijakonto, et lubada neil hankija koostööd kasutada. Selleks määrake väli **Koostöö aktiveerimine** aktiivseks vahekaardil **Üldine** lehel **Hankijad**. On kaks valikut, mida saate teha:

-   **Aktiivne (ostutellimus kinnitatakse automaatselt) **– ostutellimused kinnitatakse automaatselt, kui hankija aktsepteerib need ilma muudatusteta.
-   **Aktiivne (ostutellimust ei kinnitata automaatselt) **– teie organisatsioon peab ostutellimused käsitsi kinnitama pärast seda, kui hankija on neid aktsepteerinud.

### <a name="decide-whether-you-want-the-vendor-to-see-price-information"></a>Otsustage, kas soovite, et hankija näeks hinna teavet.

Kui soovite jagada hinnateavet, nagu ühikuhind, allahindlused ja tasud, koostööliidese kaudu, peate määrama suvandi **Ostutellimuste hinnad/summa** hankija kontol sättele **Jah**. See suvand on saadaval vahekaardil **Ostutellimuse vaikeandmed**.

## <a name="work-with-pos-when-using-vendor-collaboration"></a>Hankija koostööd kasutades ostutellimustega töötamine
### <a name="sending-a-po-to-the-vendor"></a>Ostutellimuse hankijale saatmine

Ostutellimused valmistatakse ette rakenduses Dynamics 365 for Operations. Kui Tootjaorganisatsioon on olek **kinnitatud**, saatmist kasutades hankijale on ** kinnitust saada ** tegevus on **Ostutellimus** lehel. Ostutellimuse olekuks saab **Välisel ülevaatamisel**. Pärast ostutellimuse saatmist saab hankija seda näha hankija koostöö liidese lehel **Ülevaatamist ootavad ostutellimused**, kus nad saavad tellimuse muudatusi aktsepteerida, tagasi lükata või soovitada. Hankija saab lisada ka kommentaare teabe (nt ostutellimuse muudatuste) edastamiseks. Kui soovite juhtida hankija tähelepanu uuele ostutellimusele, võite ostutellimuse saatmiseks meiliga kasutada prindihalduse süsteemi.

### <a name="confirmation-and-acceptance-of-the-po-by-the-vendor"></a>Ostutellimuse kinnitamine ja vastuvõtmine hankijalt

Kui hankija on ostutellimuse aktsepteerinud, saab ostutellimuse automaatselt kinnitada või see tuleb vajadusel käsitsi kinnitada. See sellest, kas selle ** hankija aktiveerimise ** väärtuseks on **aktiivne (PO on kinnitatud auto)** hankija või - **aktiivne (PO ei ole auto kinnitusega)**.  

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
<td>Hankija <strong>aktsepteerib</strong> tellimuse. Dynamics 365 for Operations on konfigureeritud hankija aktsepteerimise korral automaatselt ostutellimusi kinnitama.</td>
<td>Tellimuse olekuks määratakse <strong>Kinnitatud</strong>. Kui miski takistab tellimuse värskendamist, salvestatakse hankija vastuseks ikkagi <strong>Aktsepteeritud</strong>, kuid ostutellimuse olekuks jääb <strong>Välisel ülevaatamisel</strong>.</td>
</tr>
<tr class="odd">
<td>Hankija <strong>aktsepteerib</strong> tellimuse. Dynamics 365 for Operations ei ole konfigureeritud hankija aktsepteerimise korral ostutellimust automaatselt kinnitama.</td>
<td>Hankija vastus salvestatakse kui <strong>Aktsepteeritud</strong>, kuid ostutellimuse olekuks jääb <strong>Välisel ülevaatamisel</strong>.</td>
</tr>
<tr class="even">
<td>Hankija <strong>lükkab</strong> tellimuse tagasi.</td>
<td>Hankija vastus salvestatakse kui <strong>Tagasi lükatud</strong> ja ostutellimus jääb olekusse <strong>Välisel ülevaatamisel</strong>. Tagasilükkamine saadakse koos hankija märkusega.</td>
</tr>
<tr class="odd">
<td>Hankija <strong>korralduse muudatustega nõustub</strong>. Muutus on soovitatud kui tasemel. Üksikuid ridu on võimalik aktsepteerida või tagasi lükata. Muud võimalikud muudatused hõlmavad:
<ul>
<li>Kuupäevad või koguste muutmine.</li>
<li>Ridade tükeldamine erinevate tarnekuupäevade ja -koguste jaoks.</li>
<li>Kauba asendamine.</li>
</ul>
Hankija ei saa hinnateavet ja kulusid muuta. Nendele muudatuste tegemise soovitusi saab teha märkuseid kasutades.</td>
<td>Müüja vastus, tähistatakse <strong>on siis muutused</strong>, <strong></strong>ja staatus PO <strong>välise keskmiseks</strong>.</td>
</tr>
</tbody>
</table>

Kasutage selle **Ostutellimus****ettevalmistus** tööruumi jälgida mis POs müüja vastas. See tööruum sisaldab kaks loendid, mis sisaldavad ostutellimuste oleku **välise keskmiseks**:

-   Välisel ülevaatamisel nõuab tegevust.
-   Välisel ülevaatusel hankija vastuse ootel.

### <a name="changing-a-po"></a>Ostutellimuse muutmine

Kui peate muutma ostutellimust, millele on juba vastatud, peate hankijale saatma ostutellimuse uue versiooni. Uuel ostutellimusel on versiooni järelliide näitamaks, et see on varasemalt kommunikeeritud ostutellimuse modifitseeritud versioon. Leht **Ostutellimuse hankija kinnitamise ajalugu** võimaldab teil ja teie hankijatel jälgida iga tellimuse ajalugu. Ostutellimuse varem kinnitatud versioon jääb uue ostutellimuse kinnitamiseni kinnitatud ostutellimuste nimekirja.

### <a name="cancelling-a-po"></a>Ostutellimuse tühistamine

Ostutellimuse tühistamisel muudetakse olekuks uuesti **Aktsepteeritud**. Peate ostutellimuse hankija portaali kaudu hankijale tagasi saatma, et hankija saaks tühistamise kinnitada või tagasi lükata. Pärast tühistamise kinnitamist ilmub ostutellimus kinnitatud ostutellimuste hankija loendis kui **Tühistatud**.

### <a name="adding-attachments-to-a-po"></a>Ostutellimusele manuste lisamine

Ostutellimusele saate lisada manuseid, nagu failid, pildid ja märkused, kasutades dokumendihalduse süsteemi. Tüübi **Väline**piiranguga lisatud manused on hankijale nähtavad, kui neile ostutellimuse saadate.

## <a name="purchase-order-statuses-and-versions"></a>Ostutellimuse olekud ja versioonid
See jaotis kirjeldab erinevaid olekuid, mis võib ostutellimusel olla kuni selle kinnitamiseni, ja millisel hetkel tehakse ostutellimuse uued versioonid hankijale kättesaadavaks. Esineb erinevusi, sõltuvalt sellest, kas kasutate muudatuste haldamise ostutellimuste puhul. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Versioonid ja olekud, kui te ei kasuta muudatusehaldust

Järgmises tabelis on näide oleku ja versiooni muudatuste kohta, mida ostutellimuses teha saab.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tegevus**                                                               | **Olek ja versioon**                                                                                                                                       |
| Ostutellimuse algne versioon luuakse rakenduses Dynamics 365 for Operations. | Olek on **Kinnitatud**.                                                                                                                                  |
| Ostutellimus saadetakse hankijale.                                            | Versioon registreeritakse hankija koostöö liideses ja olekuks muudetakse **Välisel ülevaatamisel**.                                          |
| Hankija saadab vastuse **Aktsepteeritud koos muudatustega**                  | Olek on ikka **Välisel ülevaatamisel**.                                                                                                                  |
| Teete mõningaid hankija soovitud muudatusi.                  | Olekuks saab **Kinnitatud**.                                                                                                                        |
| Saadate ostutellimuse uue versiooni hankijale.                        | Uus versioon registreeritakse hankija koostöö liideses ja olekuks muudetakse **Välisel ülevaatamisel**.                                      |
| Hankija aktsepteerib ostutellimuse uue versiooni.                            | Olek on endiselt **Välisel ülevaatamisel **, välja arvatud juhul, kui hankija konto konfigureeritakse ostutellimust automaatselt olekusse **Kinnitatud** määrama, kui nad selle aktsepteerivad. |

Hankijad ei pea ostutellimust kinnitama, kasutades hankija koostöö liidest. Nad võivad saata ka meilisõnumi või teatama ostutellimuse vastuvõtmisest muude kanalite kaudu. Seejärel saate tellimuse kinnitada käsitsi rakenduses Dynamics 365 for Operations. Kui teete seda, saate hoiatuse, et tellimus kinnitatakse vaatamata sellele, et hankijalt ei ole mingit vastust. Seejärel kuvatakse ostutellimus kinnitusajaloos avatud kinnitatud tellimusena, millel puuduvad vastused. Hankijal ei ole enam võimalust ostutellimust kinnitada või tagasi lükata.  

**Märkus.** Ostutellimuse versioon, mis on saadaval teistele protsessidele rakenduses Dynamics 365 for Operations, on alati värskeim versioon isegi juhul, kui seda versiooni pole veel registreertud hankija koostöö liideses.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Versioonid ja olekud, kui kasutate muudatusehaldust

Kui muudatusehaldus on ostutellimuste jaoks lubatud, läbib ostutellimus kinnitamise töövoo, et saavutada olek **Kinnitatud**. See protsess ei ole hankijale nähtav.  

Järgmises tabelis on näide oleku ja versiooni muudatustest, mida ostutellimusse teha võidakse, kui muudatuste haldamine on sisse lülitatud. Versioon registreeritakse ostutellimuse kinnitamisel, mitte siis, kui ostutellimus saadetakse hankijale või kinnitatakse.

|                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tegevus**                                                                                                    | **Olek ja versioon**                                                                                                                                                                                                                                                                                                                                                                      |
| Ostutellimuse algne versioon luuakse rakenduses Dynamics 365 for Operations.                                      | Olek on **Mustand**.                                                                                                                                                                                                                                                                                                                                                                    |
| Ostutellimus esitatakse kinnitusprotsessile. (See on sisemine protsess, millesse hankija ei ole kaasatud.) | Olek muudetakse olekust **Mustand** olekusse **Ülevaatamisel** ja omakorda olekusse **Kinnitus**, kui ostutellimust ei lükata kinnitamisprotsessi käigus tagasi. Kinnitatud ostutellimus registreeritakse versioonina.                                                                                                                                                                                                                     |
| Ostutellimus saadetakse hankijale.                                                                                  | Versioon registreeritakse hankija koostöö liideses ja olekuks muudetakse **Välisel ülevaatamisel**.                                                                                                                                                                                                                                                                       |
| Teete mõningaid hankija soovitud muudatusi.                                                       | Olekuks määratakse uuesti **Mustand**.                                                                                                                                                                                                                                                                                                                                                    |
| Ostutellimus esitatakse uuesti kinnitusprotsessile.                                                            | Olek **Mustand** muutub olekuks**Ülevaatamisel** ja siis olekuks **Kinnitamine**, kui ostutellimust ei lükata kinnitamisprotsessi käigus tagasi. Teise võimalusena saab süsteemi konfigureerida nii, et konkreetse välja muudatused ei nõua uuesti kinnitamist. Sellisel juhul määratakse olekuks kõigepealt **Mustand** ja seejärel automaatselt **Kinnitatud**. Kinnitatud ostutellimus registreeritakse uue versioonina. |
| Saadate ostutellimuse uue versiooni hankijale.                                                             | Uus versioon registreeritakse hankija koostöö liideses ja olekuks muudetakse **Välisel ülevaatamisel**.                                                                                                                                                                                                                                                                   |
| Hankija kinnitab ostutellimuse uue versiooni.                                                                | Olekuks määratakse **Kinnitatud**, kas automaatselt või siis, kui saate hankijalt vastuse ja kinnitate siis ostutellimuse.                                                                                                                                                                                                                                                     |

## <a name="share-information-about-consignment-inventory"></a>Teabe jagamine veose varude kohta
Kui kasutate veose varusid, saavad hankijad kasutada hankija koostöö liidest, et kuvada teavet järgmistel lehtedel:

-   **Ostutellimused, mis tarbivad veose varusid** – ostutellimused veose varude jaoks luuakse siis, kui varude omandiõigus muutub hankijalt teie ettevõttele. Toote sissetulek sisestatakse samal ajal. Need veose ostutellimused kuvatakse ainult lehel **Ostutellimused, mis tarbivad veose varusid**. Neid ei kaasata lehele **Kõik kinnitatud ostutellimused** moodulis **Hankija koostöö**.
-   **Veose varudest saadud tooted** – see leht loetleb kõik kanded, kus toodete omandiõigus on hankijalt teie ettevõttele üle viidud. Hankijad saavad kasutada seda teavet, et kliendile arvet esitada.
-   **Veose vaba kaubavaru** – see leht näitab hankijale kuuluvat vabu veose varusid, mis on teie lattu vastu võetud.



