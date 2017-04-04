---
title: "Hankija koostöö mobiilne tööruum Microsoft Dynamics 365 toimingute App"
description: "Hankija koostöö mobiilne tööruumiga, hankijad saate kursis mis saadetud neile heakskiidu ja uute ja värskendatud ostutellimuste ja kontaktide kohta teabe vaatamine."
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

# <a name="vendor-collaboration-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Hankija koostöö mobiilne tööruum Microsoft Dynamics 365 toimingute App

Hankija koostöö mobiilne tööruumiga, hankijad saate kursis mis saadetud neile heakskiidu ja uute ja värskendatud ostutellimuste ja kontaktide kohta teabe vaatamine.

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
<td>Lugeda Microsoft Dynamics 365 toimingute mobiilne platvorm</td>
<td><a href="/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform">Dynamics 365 toimingute mobiilne platvorm</a></td>
</tr>
<tr class="even">
<td>Dynamics 365 toiminguteks</td>
<td>Kindlasti kasutamisel keskkond, mis on Microsoft Dynamics 365 toiminguid versiooni 1611 ning Microsoft Dynamics toimingute platvormi update 3 (November 2016).</td>
</tr>
<tr class="odd">
<td><span style="color: #000000;">Mobiilne seade, mis on toimingute App installitud Dynamics 365</span></td>
<td><span style="color: #000000;">Lae toimingute rakenduse Dynamics 365 mobiilne app-store.</span></td>
</tr>
<tr class="even">
<td>Käigultparanduse KB 3215650</td>
<td>Installige käigultparandus et tööruumid, mis on toodud Dynamics 365 toiminguteks.</td>
</tr>
<tr class="odd">
<td><span style="color: #ff0000;"><span style="color: #000000;">Käigultparanduse KB 3216943</span> </span></td>
<td>Installige käigultparandus et hankija koostöö mobiilne tööruumi.</td>
</tr>
<tr class="even">
<td>Hankija kasutaja peab hankija koostöö liidesesse Dynamics 365 operatsioonide juurdepääsu ja tarnija koostöö Kasutaja seadistamine.</td>
<td>Järgige kirjeldatud järgmisi teemasid ja töötada hankija koostöö web interface.
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">Kasutada hankija koostöö välistarnijate töötamiseks</a></li>
<li><a href="manage-vendor-collaboration-users.md">Hankija koostöö kasutajate haldamine</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">Hankija koostöö seadistamine ja haldamine</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Hankija koostöö abil saate töötada klientidega Dynamics 365 toiminguteks</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="overview"></a>Ülevaade
Hankija koostöö mobiilne tööruumi hoiab kursis, et nad näevad ja ostutellimustel Dynamics 365 toimingute web klient vastata uutele hankijatele.  

**Märkus:** mobiilne tööruumi võib kasutada hankija koostöö web interface, kuid mitte täiendada.  

Hankija koostöö mobiilne tööruumiga, hankijad saate vaadata uute ostutellimuste, mis saadetakse kinnitamiseks. Kuvatakse ostutellimuste teabe, toodete, kogus ja nõutud kuupäevad. Hinnainfo on saadaval kõigi konfiguratsioonist.  

Kui kasutaja sisselogimise ajal kui müüja, näevad nad, mis ostutellimuste on vastatud või mis ostutellimuste ikka ootab kliendi tegevus. Hankija võib soovitas teisele tarnekuupäev, mis ei ole veel kokku lepitud kliendiga nii siis ootab kliendi tegevus. Müüja näitab ka nimekiri mis on kinnitatud, kuid veel tarnimata.  

Ostutellimuse vastamiseks on hankija koostöö web liides, mis on saadaval Dynamics 365 toimingute web klient kasutada. See on ka, kus hankija saavad rohkem teavet tellimuse, nagu dokumendi manuseid, tarneaadressi kohta rida ja kulud, mis on seotud hankija.  

Eriline roll hankija saab vaadata milline Kontakt isikud registreeritakse hankija konto. Sama turberolli hankija saab vaadata iga kasutaja taotluse esitamist staatuse.  

Uute kontaktide loomiseks ja uue kasutaja taotluste esitamine peab toimuma hankija koostöö liides, mis on esitatud tegevuse web kliendi Dynamics 365.  

Mobiilne tööruumi, saate oma poole:

-   Vaata uute ostutellimuste hankijale saadetavatele.
-   Vaadata ostutellimusi et müüja vastas ja ootab kliendi tegevus.
-   Vaata mis on kinnitatud riigi ja täielikult saamata.
-   Saate vaadata hankija konto on registreeritud kontaktisiku andmed (nõuab täiendavat turberolli).
-   Saate vaadata ja jälgida kasutaja (nõuab täiendavat turberolli) müüja poolt esitatud taotlus.

## <a name="get-started"></a>Alusta
Algas mobiilne seade:

1.  Mobiilirakenduse poes, alla laadida ja installida Microsoft Dynamics 365 toimingute app.
2.  Käivitada rakendus oma seadmes.
3.  Sisestage oma Dynamics 365 URL.
4.  Sisestage ettevõtte sisse logima. Sisestage **USMF**.
5.  Esimene kord, kui logite sisse, küsitakse kasutajanime ja parooli teie Microsofti Dynamics 365 operatsioonide tarbeks. 

Pärast teie rakenduses, kuvatakse tööruume pole. Saate vaadata oma mobiilirakendus tööruumid, peab esmalt avaldama soovitud tööruumid toimingute rakenduse Dynamics 365. Peate süsteemi haldamise luba avaldada tööruumi.

1.  Käivitage Dynamics 365 toiminguteks.
2.  Mine **süsteemi halduse**&gt;**install**&gt;**süsteemi parameetrid**.
3.  Valige **Halda mobiilirakendus**.
4.  Valige tööruum **hankija koostöö** avaldada mobiilsel platvormil.
5.  Valige **avaldada tööruumi**.
6.  Värskendage seadme avaldatud tööruumid.
7.  Valige selle **hankija koostöö** tööruumi. Siis järgmisel leheküljel.

[![hankija-koostöö-mobiilirakenduse](./media/vendor-collaboration-mobile-app.png)](./media/vendor-collaboration-mobile-app.png)

## <a name="contacts"></a>Kontaktid
Selle **kontaktid** lehel saab näha seadistatud hankija konto kontakte. See näitab kontaktisiku nimi ja esmane e-posti kasutajad alias, kui see on saadaval. See näitab ka, kas kontaktisiku kasutaja konto on aktiivne. Valides kontakti, vt nt millised juriidilised isikud on kontakti, kontaktandmete ja kontaktandmeid nagu telefoninumber ja erinevate e-posti aadress.

## <a name="user-requests"></a>Kasutaja nõuded
Selle **kasutaja taotlused** lehekülg võimaldab vaadata kõiki kasutaja soovib, et on esitanud hankija koostöö veebiliidese kaudu ja jälgida. Kui valite kasutaja taotlusel, saate näha, mida nõuti, lisada või inaktiveerida kasutaja, turvalisuse muutmine, ja vaata mis turberollid paluti kasutaja.

## <a name="purchase-orders-ready-for-review"></a>Ostutellimuste läbivaatuseks valmis
Selle **ostutellimuste valmis keskmiseks** lehel saate vaadata tellimusega kõik ostu kliendi poolt saadetud ja pole vastatud. Saate vaadata valitud tellimuse, nt millised tooted on küsitud ja millal pakkuda teavet. Hinnainfo on ainult juhul, kui see on seadistatud hankija.  

Näete, kas siis on märkmete või manuseid. Manuste avamiseks peate kasutama hankija koostöö web klient. Valige **ostutellimuse reale** üksikasjad kõikide ridade kuvamiseks. Pange tähele, et iga rea indikaator näitab märgib või manuseid või lisandub kohaletoimetamise aadressi, mis erineb mida kuvatakse päises.  

Ostutellimuse vastamiseks kasutage hankija koostöö web klient.

## <a name="awaiting-customer-action"></a>Kliendi tegevuse ootel
Selle **ootab kliendi tegevuse** lehekülg võimaldab teil leida ostutellimuste, teie või keegi teie ettevõttes, kes pääseb ka hankija koostöö reageerinud. Ostutellimusi on selles loendis nähtavad ainult siis, kui klient peab tee üht järgnevast ostutellimuse.

-   Kui ostutellimuse lükati klient oleks kas tuleb ajakohastada saadetud tellimuse ja saatke uuesti, või tellimus tühistada ja uuesti saata. Siis kohe uuesti see kaob ning **ootab kliendi tegevuse** lehel.
-   Kui siis kiideti muudatustega, peaksid kliendi algne uuendada ja uuesti läbivaatamiseks või uuendada vastavalt muudatustele ja kinnitage see kohe. Mõlemal juhul kaob siis ka **ootab kliendi tegevuse** lehel.
-   Kui siis nõustuti ning kuvatakse on **ootab kliendi tegevuse** leht, sellepärast siis ei automaatselt kinnitati kiidab lõppedes. Hankija esindaja järjekorra muutmiseks kinnitatud ootama. Tavaliselt käsitletaks kokkuleppel kliendi ja hankija ostutellimuse, kui tarnija nõustub tellimuse. Asute siis kinnitatud riiki oleks formaalsus.

Valige ostutellimus, täiendavad üksikasjad kuvatakse vastuse kohta käivat. Saate vaadata tellimuserea üksikasjade ja vastus igal real. Rea olek näitab, mis järgmistest vastustest on esitatud.

-   Aktsepteeritud
-   Tagasi lükatud
-   Aktsepteeritud koos muudatustega
-   Asendada/asendaja
-   Ajakava/ajakava rida jagatud

Pange tähele, et tähis näitab **toimetamine**= jah/ei, mida kasutatakse näitamaks, et ridu ei saadeta. Võimalik, et rida ei nõustunud või asendada kui algse rea ei tohiks üle või ajakava mitmeks reaks tükeldatud rida ja algse rea ei tohiks taotletud tellimuse kohale toimetada.  

Tellimuse rea vastus muutused kuvatakse välja arvatud üles laaditud märkmed ja manuseid, mida näete hankija koostöö liidese abil.

## <a name="open-confirmed-orders"></a>Avatud kinnitatud tellimused
Ostutellimuse kinnitab klient, mis tähendab, et ostutellimuse vahetatakse kinnitatud riigile, see ilmub avatud tellimuse. See jääb loendis enne, kui see on registreeritud, kui kliendi poolt.


