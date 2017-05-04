---
title: "Hankija koostöö mobiilne tööruum rakendusele Microsoft Dynamics 365 for Operations"
description: "Hankija koostöö mobiilse tööruumiga saavad teie hankijad püsida ajakohasena neile kinnitamiseks saadetud ostutellimuste osas ja vaadata teavet uute ja värskendatud ostutellimuste ja kontaktide kohta."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 36 - 37
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267074
ms.assetid: fe8e912d-8446-4584-8a24-d8892e9028cd
ms.search.region: global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 9f441508b745d22218316128572c9ec6aeb7207b
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-collaboration-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Hankija koostöö mobiilne tööruum rakendusele Microsoft Dynamics 365 for Operations

Hankija koostöö mobiilse tööruumiga saavad teie hankijad püsida ajakohasena neile kinnitamiseks saadetud ostutellimuste osas ja vaadata teavet uute ja värskendatud ostutellimuste ja kontaktide kohta.

<a name="prerequisites"></a>Eeltingimused
-------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Eeltingimus</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Lugege teavet Microsoft Dynamics 365 for Operationsi mobiiliplatvormi kohta</td>
<td><a href="/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform">Dynamics 365 for Operationsi mobiilne platvorm</a></td>
</tr>
<tr class="even">
<td>Dynamics 365 for Operations</td>
<td>Veenduge, et kasutaksite keskkonda, millesse on installitud Microsoft Dynamics 365 for Operationsi versioon 1611 ja Microsoft Dynamics for Operationsi platvormivärskendus 3 (november 2016).</td>
</tr>
<tr class="odd">
<td><span style="color: #000000;">Mobiilne seade, kuhu on installitud rakendus Dynamics 365 for Operations</span></td>
<td><span style="color: #000000;">Laadige mobiilirakenduste poest alla rakendus Dynamics 365 for Operations.</span></td>
</tr>
<tr class="even">
<td>Kiirparandus KB 3215650</td>
<td>Installige kiirparandus, et lubada rakenduses Dynamics 365 for Operations sisestatud tööruumid.</td>
</tr>
<tr class="odd">
<td><span style="color: #ff0000;"><span style="color: #000000;">Kiirparandus KB 3216943</span> </span></td>
<td>Installige kiirparandus, et lubada hankija koostöö mobiilne tööruum.</td>
</tr>
<tr class="even">
<td>Hankija-kasutajal peab olema juurdepääs hankija koostöö veebiliidesele rakenduses Dynamics 365 for Operations ja seadistada hankija koostöö kasutaja.</td>
<td>Järgige järgmistes teemades kirjeldatud juhiseid, et seadistada ja töötada hankija koostöö veebiliidesega.
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">Hankija koostöö kasutamine väliste hankijatega töötamiseks</a></li>
<li><a href="manage-vendor-collaboration-users.md">Hankija koostöö kasutajate haldamine</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">Hankija koostöö seadistamine ja haldamine</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Hankija koostöö kasutamine klientidega töötamiseks rakenduses Dynamics 365 for Operations</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="overview"></a>Ülevaade
Hankija koostöö mobiilne tööruum teavitab hankijaid uutest ostutellimustest, et nad saaks näha ja vastata ostutellimustele rakenduse Dynamics 365 for Operations veebikliendis.  

**Märkus.** Mobiilset tööruumi tuleb kasutada hankija koostöö veebiliidese lisana, kuid mitte asendusena.  

Hankija koostöö mobiilse tööruumiga saavad teie hankijad vaadata uusi kinnitamiseks saadetud ostutellimusi. See kuvab ostutellimuse teabe, nagu tooted, kogus ja nõutavad tarnekuupäevad. Hinnateave on saadaval sõltuvalt iga hankija jaoks tehtud konfiguratsioonist.  

Kui kasutaja logib hankijana sisse, siis nad näevad, millistele ostutellimustele on vastatud või millised ostutellimused ootavad endiselt kliendi tegevust. Hankija võis pakkuda teist tarnekuupäeva, mille osas pole kliendiga kokku lepitud, seega ootab ostutellimus kliendi tegevust. Hankija näeb ka loendit ostutellimustest, mis on kinnitatud, kuid pole veel kohale toimetatud.  

Ostutellimusele vastamiseks peab hankija kasutama hankija koostöö veebiliidest, mis on saadaval veebikliendis Dynamics 365 for Operations. See on ka koht, kus hankija saab tellimuse kohta rohkem teavet, nagu dokumendimanused, tarneaadress rea kohta ja hankijaga seotud kulud.  

Spetsiaalse turberolliga saab hankija vaadata, millised kontaktisikud on hankijakonto jaoks registreeritud. Sama turberolliga saab hankija vaadata mis tahes edastatud kasutajataotluse olekut.  

Uute kontaktide loomine ja uute kasutajataotluste edastamist tuleb teha hankija koostööliideses, mis on saadaval rakenduse Dynamics 365 for Operations veebikliendist.  

Mobiilse tööruumiga saab teie hankija teha järgmist.

-   Vaadata hankijale saadetud uusi ostutellimusi.
-   Vaadata ostutellimusi, millele hankija on vastanud ja mis ootavad kliendipoolset tegevust.
-   Vaadata ostutellimusi, mis on kinnitatud olekus ja mis pole veel täielikult vastu võetud.
-   Vaadata hankijakonto jaoks registreeritud kontaktisiku teavet (nõuab täiendavat turberolli).
-   Vaadata teavet ja järgida hankija kasutajataotluse olekut (nõuab täiendavat turberolli).

## <a name="get-started"></a>Alusta
Mobiilsel seadmel alustamiseks tehke järgmist.

1.  Laadige mobiilirakenduste poest alla rakendus Microsoft Dynamics 365 for Operations ja installige see.
2.  Käivitage rakendus oma seadmes.
3.  Sisestage Dynamics 365 URL.
4.  Sisestage ettevõte, millesse soovite sisse logida. Näiteks sisestage **USMF**.
5.  Esmakordsel sisselogimisel palutakse teil sisestada oma Microsoft Dynamics 365 for Operationsi konto kasutajanimi ja parool. 

Pärast rakendusse sisselogimist pole ükski tööruum nähtav. Tööruumide vaatamiseks mobiilirakenduses peate soovitud tööruumid esmalt avaldama rakenduses Microsoft Dynamics 365 for Operations. Tööruumi avaldamiseks vajate süsteemiadministraatori õigust.

1.  Käivitage Dynamics 365 for Operations.
2.  Minge jaotisse **Süsteemihaldus** &gt; **Seadistus** &gt; **Süsteemi parameetrid**.
3.  Valige suvand **Mobiilirakenduse haldamine**.
4.  Mobiilse platvormi avaldamiseks valige tööruum **Hankija koostöö**.
5.  Valige suvand **Avalda tööruum**.
6.  Värskendage seadet, et näha avaldatud tööruume.
7.  Valige tööruum **Hankija koostöö**. Näete järgmist lehte.

[![vendor-collaboration-mobile-app](./media/vendor-collaboration-mobile-app.png)](./media/vendor-collaboration-mobile-app.png)

## <a name="contacts"></a>Kontaktid
Leht **Kontaktid** võimaldab teil näha kõiki kontakte, mis on hankija konto jaoks seadistatud. See näitab kontaktisiku nime, peamist meiliaadressi ja kasutajate aliast, kui see on saadaval. See näitab ka, kas kontaktisiku kasutajakonto on aktiivne. Kontakti valimisel näete kontakti üksikasju, nt seda, milliste juriidiliste isikute kontakt isik on, ja kontaktteavet, nagu telefoninumber või teine meiliaadress.

## <a name="user-requests"></a>Kasutaja nõuded
Leht **Kasutaja nõuded** võimaldab teil näha kasutajataotlusi, mis on edastatud hankija koostöö veebiliidese kaudu ja mis järgivad olekut. Kasutajataotluse valimisel saate näha, mida taotleti, lisada või inaktiveerida kasutajat, muuta turvet ja näha, milliseid turberolle kasutajale taotleti.

## <a name="purchase-orders-ready-for-review"></a>Ülevaatamiseks valmis ostutellimused
Leht **Ülevaatamiseks valmis ostutellimused** võimaldab näha kõiki kliendi saadetud ja vastamata ostutellimusi. Saate vaadata tellimuse kohta valitud teavet, näiteks seda, milliseid tooteid on taotletud ja millal kohale toimetada. Hinnateave on saadaval ainult siis, kui see on hankija jaoks konfigureeritud.  

Saate näha, kas ostutellimusel on märkusi või manuseid. Manuste avamiseks peate kasutama veebikliendis hankija koostööd. Valige **Ostutellimuse rida**, et näha kõiki ridu koos üksikasjadega. Pange iga rea puhul tähele, et kuvatakse indikaator, mis näitab, kas on märkusi või manuseid või kas on olemas tarneaadress, mis erineb päises näidatud aadressist.  

Ostutellimusele vastamiseks peate kasutama hankija koostöö veebiklienti.

## <a name="awaiting-customer-action"></a>Kliendi tegevuse ootel
Leht **Kliendi tegevuse ootel** võimaldab teil leida ostutellimusi, millele teie või keegi teie ettevõttes, kellel on juurdepääs hankija koostööle, on vastanud. Ostutellimused on selles loendis nähtavad ainult siis, kui klient peab tegema ostutellimusel ühe järgmistest tegevustest.

-   Kui ostutellimus lükati tagasi, peab klient värskendama saadetud tellimust ja saatma uuesti või tühistama tellimuse ja uuesti saatma. Kui ostutellimus saadetakse uuesti, kaob see lehelt **Kliendi tegevuse ootel**.
-   Kui ostutellimus kinnitati muudatustega, peab klient värskendama originaaltellimust ja saatma ülevaatamiseks uuesti või värskendama seda vastavalt muudatustele ja kinnitama selle koheselt. Mõlemal juhul kaob ostutellimus lehelt **Kliendi tegevuse ootel**.
-   Kui ostutellimus kinnitati ja see ilmub lehel **Kliendi tegevuse ootel**, on see sellepärast, et ostutellimust ei kinnitatud kinnitamisel automaatselt. See ootab ostuagenti, et ta muudaks tellimuse olekuks Kinnitatud. Tavaliselt loetakse ostutellimus lepinguks kliendi ja hankija vahel kohe, kui hankija tellimuse kinnitab. Ostutellimuse teisaldamiseks olekusse Kinnitatud on formaalsus.

Ostutellimuse valimisega ilmuvad vastuse kohta täiendavad üksikasjad. Saate näha rea üksikasju ja vastust iga rea kohta. Rea olek näitab, milline järgmistest vastustest on antud.

-   Aktsepteeritud
-   Tagasi lükatud
-   Aktsepteeritud koos muudatustega
-   Asendatud/asendaja
-   Tükeldamine graafikusse / graafiku rida

Pange tähele, et indikaator näitab **Tarnimisel**=jah/ei, mida kasutatakse näitamiseks, et ridu ei edastata. See võib olla selle tõttu, et rida lükati tagasi või asendati seal, kus originaalridade edastamist ei oodatud, või mitmeks graafiku reaks tükeldatud rea ja originaalrea edastamist ei oodata nii, nagu vastuvõetud tellimuses on soovitud.  

Kuvatakse mis tahes tellimusereale tehtud muudatused, välja arvatud üles laaditud märkused ja manused, mida saate näha, kasutades hankija koostöö veebiliidest.

## <a name="open-confirmed-orders"></a>Kinnitatud tellimuste avamine
Kui klient kinnitab ostutellimuse, mis tähendab, et ostutellimus muudetakse olekusse Kinnitatud, ilmub see avatud kinnitatud olekusse. See püsib loendis, kuni see registreeritakse kliendilt vastuvõetuks.


