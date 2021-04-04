---
title: Hankijate vastuvõtmine
description: Selles teemas kirjeldatakse, kuidas uusi hankijaid vastu võtta. See kirjeldab mitmesuguste rollide puhul nõutavaid tegevusi selle protsessi käigus.
author: RichardLuan
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests, SysUserRequestListPage, VendRequestListPage, VendRequestCompanyProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 7cb6baefb9880ac0135405c4a3b2449814afd4a6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246617"
---
# <a name="onboard-vendors"></a>Hankijate vastuvõtmine

[!include [banner](../includes/banner.md)]

---

Uusi hankijaid saate rakenduses Microsoft Dynamics 365 Supply Chain Management vastu võtta ja neid hankijateks registreerida hankija esindajalt saadud teabe põhjal.

Protsess sisaldab järgmisi etappe, kus mitmesugused rollid süsteemis tegevusi teevad.

1. **OData andmehaldus** – üksuse importimine – esmane taotlus on potentsiaalse hankija registreerimistaotlus. Tavaliselt tuleb selline taotlus näiteks kliendi hostitud veebisaidilt, mis lubab anonüümset juurdepääsu. Hankijad saavad registreerida end, andes põhiteavet, nagu hankija nimi, põhjendus, organisatsiooni kood ja kontaktisiku nimi ning meiliaadress. Taotlused imporditakse andmehalduse kasutajaliidese kaudu.
2. **Potentsiaalse hankija registreerimistaotluse loendileht** – hankespetsialist otsustab potentsiaalse hankija registreerimistaotluses esitatud teabe põhjal, kas hankija tuleks organisatsiooni hankijate hulka arvata. Hankespetsialist saab sissetulevaid taotlusi vaadata loendilehel **Potentsiaalse hankija registreerimistaotlused**.
3. **Kasutajate ettevalmistuse töövoog** – kui hankespetsialist on sissetulevas taotluses oleva teabe kontrollinud ja otsustanud hankija vastu võtta, valmistab kasutajataotluse töövoog ette uue kasutaja ning saadab meiliga kutse kontaktisiku Microsoft Dynamics 365 autenditud kasutajana vastuvõtmiseks.
4. **Hankija registreerimisviisard** – hankija kontaktisik logib uue kasutajakontoga sisse. Ta viib hankija registreerimisviisardis teabe täitmise lõpule, andes sellist teavet nagu aadressid, äriteave, hankekategooriad, ja vastab küsimustikule.
5. **Kinnitamise töövoog** – luuakse registreerimisteavet sisaldav hankija taotlus. Hankija taotlus saadetakse töövoogu ja suunatakse ülevaatamiseks ning kinnitamiseks.
6. **Hankija koondandmete loomine ja kasutaja rolli muutmine** – hankija nõude kinnitamisel luuakse hankija kirje. Hankija kontaktisiku kasutajakontole antakse kas õigus hankija koostööks või see inaktiveeritakse.

Järgmises tabelis on toodud protsessiga seotud etapid ja rollid.

| Roll ja „protsess”       | OData andmehaldus – üksuse importimine | Potentsiaalse hankija registreerimistaotluse loendileht | Kasutajate ettevalmistuse töövoog | Hankija registreerimisviisard | Kinnitamise töövoog | Hankija koondandmete loomine ja kasutaja rolli muutmine |
|--------------------------|---|---|---|---|---|---|
| System                   | Uue hankija taotlus on imporditud. | | | | | Hankija nõude kinnitamisel luuakse hankija kirje. |
| Hankespetsialist | | Alustab vastuvõtuprotsessi. | | | Vaatab hankija taotluse üle ja aktseptib või lükkab selle tagasi. | |
| Administraator            | | | Looge kasutaja Supply Chain Managementis ja Microsoft Azures. | | | |
| Hankija kontaktisik    | | | Saadab kontaktisikule meili. | Registreerib hankija teabe. | | |

Kiiret demonstratsiooni uute hankijate vastuvõtmise protsessist saate vaadata järgmisest lühikesest YouTube’i videost: [Uue hankija vastuvõtmine rakenduses Finance and Operations](https://www.youtube.com/watch?v=0KUc3AGaTKk).

## <a name="importing-the-prospective-vendor-registration-request"></a>Potentsiaalse hankija registreerimistaotluste importimine

Potentsiaalse hankija registreerimistaotlus on rakenduse Supply Chain Management üksus. Saate seadistada süsteemi selle üksuse kaudu andmeid importima. 

Alljärgnevas tabelis on toodud teave, mida see üksus sisaldab ja mida saab importida.

| Väli                        | Kirjeldus |
|------------------------------|-------------|
| Hankija nimi                  | Tarnija nimi. |
| Põhjendus       | Hankija taotluse esitamise põhjendus või põhjendused. |
| Organisatsiooni kood          | Registreerimisnumber, mis on ametlikult tunnustatud. |
| Tegevusala             | Tegevusharu, kus hankija tegutseb. |
| Kontaktisiku eesnimi  | Selle isiku eesnimi, keda kutsutakse hankija teavet registreerima. |
| Kontaktisiku teine eesnimi | Selle isiku teine eesnimi, keda kutsutakse hankija teavet registreerima. |
| Kontaktisiku perekonnanimi   | Selle isiku perekonnanimi, keda kutsutakse hankija teavet registreerima. |
| Kontaktisiku meiliaadress       | Meiliaadress, mida kasutatakse rakenduses Supply Chain Management uue kasutaja loomiseks ja mis registreeritakse rentniku Azure Active Directory (Azure AD) kontol. |
| Edastamiskuupäev               | Kuupäev, mil taotlus välises süsteemis loodi. |
| Juriidiline isik                 | Juriidiline isik, mille hankijaks hankija soovib saada. See väärtus peab olema rakenduses Supply Chain Management registreeritud juriidilise isiku kood. Kui importimisprotsessi kaudu ei saada ühtki väärtust, rakendatakse mõnda väärtust hanke parameetritest. |
| Hankija tüüp                  | Hankija võib olla kas organisatsioon või isik. Hankija lõpliku loomise määrab hankija tüüp. |

Potentsiaalse hankija registreerimistaotluse importimise järel kuvatakse see loendilehel **Potentsiaalse hankija registreerimistaotlus**. Sellel loendilehel saab hankespetsialist kasutajale kutse saata. Kasutaja ettevalmistustaotlus saadetakse töövoogu.

## <a name="submitting-a-prospective-vendor-user-request"></a>Potentsiaalse hankija-kasutaja taotluse esitamine

Potentsiaalse hankija-kasutaja taotluse eesmärk on valmistada ette kasutaja esialgse taotluse esitanud isikule, et ta saaks rakendusse Supply Chain Management sisse logida, kasutades potentsiaalse hankija registreerimistaotlusel esitatud meilikontot.

Potentsiaalse hankija-kasutaja taotlust töödeldakse kasutajataotluse töövoos. See töövoog suhtleb Azure AD B2B koostöö kaudu. See loob rakenduses Supply Chain Management asjakohaste turvesätetega kasutaja.

Uutel seadistatud kasutajatel on järgmised turberollid.

- Süsteemiväline kasutaja
- Potentsiaalne hankija (väline)

Uus kasutaja saab kasutajataotluse töövoos loodud meili. See meil kutsub kasutajat süsteemi sisse logima.

Teavet meili konfigureerimise ja töövoo kohta üldiselt vaadake kasutajataotluse töövoo kirjeldusest teemas [„Hankija koostöö seadistamine ja haldamine”](set-up-maintain-vendor-collaboration.md).

## <a name="vendor-registration"></a>Hankija registreerimine

Kui potentsiaalne hankija logib sisse rakendusse Supply Chain Management, näeb ta esimese lehena hankija registreerimisviisardit, kus ta saab hankija kohta teabe sisestada.

Viisard kajastab hankija taotluse konfiguratsiooni. Viisardis küsitav teave, samuti milline osa sellest on kohustuslik sisestada, oleneb sellest, millises riigis või regioonis hankija tegutseb.

Lisateavet hankija taotluse seadistamise kohta vaadake teemast [„Hankija koostöö seadistamine ja haldamine”](set-up-maintain-vendor-collaboration.md). Alljärgnev tabel annab ülevaate viisardi lehekülgedest ja nende eesmärkidest.

| Leht                       | Kirjeldus |
|----------------------------|-------------|
| Riik/regioon             | Ülejäänud viisardi lehtedele rakendatav konfiguratsioon oleneb hankija riigist või regioonist. See määrab ka otsingu **Maksuriik** väärtused. |
| Nõuded ja tingimused       | See leht võib olenevalt hankija taotluse konfiguratsioonist saadaval olla. Kui see on saadaval, peab kasutaja jätkamiseks nõustuma nõuete ja tingimustega. |
| Hankija teave         | See leht sisaldab hankija nime, mis sisestatakse automaatselt algsest potentsiaalse hankija registreerimistaotlusest. See sisaldab ka organisatsiooni koodi, hankija telefoninumbrit, faksinumbrit ja meiliaadressi ning hankija eri aadresse. |
| Kontaktisiku teave | See leht sisaldab kontaktisiku nime, mis sisestatakse automaatselt algsest potentsiaalse hankija registreerimistaotlusest. See sisaldab ka kontaktisiku telefoninumbrit ja meiliaadressi ning kontaktisiku eri aadresse. |
| Ettevõtte teave       | See leht sisaldab maksu registreerimisnumbreid (eri riikides või regioonides) ja töötajate arvu. See näitab ka, kas ettevõte on vähemusomanduses. |
| Hankekategooriad     | See leht sisaldab hankekategooriad, millele hankija taotleb kinnitust. Kasutaja saab valida kategooriad hanke kategooriahierarhiast. Hierarhia tasemete arvu saate konfigureerida, avades **Hangete parameetrid** &gt; **Hankija koostöö** ja sealt **Hanked** &gt; **Seadistamine**. |
| Küsimustikud             | Viisard võib hõlmata ka hankijale mõeldud küsimustike kogumit. Viisardis olevad küsimustikud võivad olla konfigureeritud kas hankija taotluses või hankekategooria kohta. Kui küsimustikud konfigureeritakse hankekategooria kohta, olenevad viisardis kuvatavad küsimustikud sellest, millistes hankekategooriates hankija heakskiitu taotleb. Küsimustiku saate vastavale kategooriale lisada lehel **Hankekategooriad**, samuti saate seal määrata tegevuse tüübiks **Hankija vastuvõtt**. |

Hankija taotlus luuakse pärast seda, kui potentsiaalne hankija-kasutaja on läbinud hankija registreerimisviisardi.

## <a name="manually-or-automatically-submit-a-vendor-request"></a>Hankija taotluse saatmine käsitsi või automaatselt

Hankija taotluse saab luua mustandina ja käsitsi töövoogu saata. Teise võimalusena saab hankija taotluse automaatselt töövoogu saata, kui hankija registreerimisviisard on läbitud. Taotluse saab käsitsi esitada näiteks siis, kui hankespetsialist tahab hinnata, kas taotlus peaks enne töövoogu saatmist läbima kinnitusprotsessi.

- Hankija taotluse automaatseks töövoogu saatmiseks pärast hankija registreerimisviisardi läbimist, avage **Hangete parameetrid** &gt; **Hankija koostöö** ja valige **Potentsiaalse hankija registreeringu automaatne saatmine töövoogu**.

## <a name="vendor-requests"></a>Hankija nõuded

Hankija taotlused on saadaval lehel **Hankija koostöö kasutajataotlused**.

Hankija taotlus sisaldab potentsiaalse hankija-kasutaja hankija registreerimisviisardis sisestatud teavet.

Taotlus annab võimaluse vaadata üle hankija teave ja otsustada, kas registreerida hankija.

Hankija taotlus tuleks saata töövoogu ja suunata asjakohastele ülevaatajatele ja kinnitajatele. Põhiteavet töövoogude seadistamise kohta hangetes vaadake teemast [„Hangete töövood”](procurement-sourcing-workflows.md).

Alljärgnevas tabelis on toodud hankija taotluste võimalikud olekud.

| Olek                     | Kirjeldus |
|----------------------------|-------------|
| Mustand                      | Hankija taotlus pole veel esitatud. |
| Taotlus on esitatud.          | Hankija taotlus on esitatud ja töövoo esimest etappi töödeldakse. |
| Ülevaatuse ootel             | Kui töövooülesandel on mitu ülevaatajat, saab ülevaataja aktseptida hankija taotluse ülevaatamisülesande ja seejärel ülevaatamise lõpule viia. Kui on ainult üks ülevaataja, saab ta ülevaatamise lõpetada, valides töövootegevuse **Lõpetatud**. Ta ei pea tööüksust esmalt aktseptima. |
| Taotlus on kinnitamise ootel.   | Hankija taotlus on suunatud asjaosalistele kinnitamiseks ja on võimalus, et küsitakse täiendavat teavet. Lisateabe taotlus suunab tööüksuse tagasi esitajale. Ka selle olekuga hankija taotlust saab ka kinnitada või tagasi lükata. |
| Taotluse muutmistaotlus | Kinnitaja on taotlenud lisateavet ja hankija taotlus on suunatud tagasi isikule, kes hankija taotluse esitas. Esitaja saab lisada nõutud teabe ja siis hankija taotluse uuesti esitada. Kui hankija taotlus esitatakse uuesti, muudetakse olek tagasi olekuks **Taotlus on kinnitamise ootel**. |
| Taotlus on kinnitatud           | See on lõppolek. |
| Taotlus on tagasi lükatud.           | See on lõppolek. |

## <a name="approving-a-vendor-request"></a>Hankija taotluse kinnitamine

Hankija taotluse kinnitamisel luuakse hankija konto ja nii esialgse potentsiaalse hankija registreerimistaotluse kui ka hankija taotluse olekuks saab **Kinnitatud**.

Enne kui saate hankija taotluse kinnitada, peate määrama hankijagrupi, avades lehe **Uus hankija** kiirkaardi **Üldine** ja valides **Hankijagrupp**.

Kui hankija esindajal peaks potentsiaalse hankija-kasutajana olema hankija koostöö kasutajana juurdepääs rakendusele Supply Chain Management, siis määrake hankija koostöö juurdepääsu loaks **Jah**. Potentsiaalse hankija registreerimisel kasutatud kasutajakonto inaktiveerimiseks määrake see luba väärtusele **Ei**.

Kui hankija koostöö juurdepääsuloaks on määratud **Jah**, siis esitatakse hankija taotluse kinnitamisel taotlus kasutaja rolli muutmiseks **välistes rollides** määratud **hankija** tüübiks. Kui selle loa väärtuseks on seatud **Ei**, esitatakse hankija taotluse kinnitamisel taotlus kasutaja inaktiveerimiseks. Sel juhul peab olema seadistatud kasutaja taotluse inaktiveerimise töövoog.

Selleks et hankija taotluse kinnitamisel hankija konto loodaks, peab hankija taotlustest hankijate loomise järjekorranumber olema seatud väärtusele **Automaatne**.

Hankija koostöö kasutaja juurdepääsulubadest ülevaate saamiseks vaadake teemat [„Hankija koostöö seadistamine ja haldamine”](set-up-maintain-vendor-collaboration.md).

## <a name="rejecting-a-vendor-request"></a>Hankija taotluse tagasilükkamine

Hankija taotluse tagasilükkamisel peate valima hankija taotluse tagasilükkamise põhjuse.

Hankija taotluse tagasilükkamisel esitatakse taotlus kasutaja inaktiveerimiseks. Sel juhul peab olema seadistatud kasutaja taotluse inaktiveerimise töövoog. Lisateavet vaadake teemast [„Hankija koostöö seadistamine ja haldamine”](set-up-maintain-vendor-collaboration.md).

Hankija taotluse tagasilükkamisel kuvatakse nii esialgse potentsiaalse hankija registreerimistaotluse kui ka hankija taotluse juures olek **Tagasi lükatud**.

## <a name="deleting-a-prospective-vendor-registration-request-in-various-statuses"></a>Eri olekutes potentsiaalse hankija registreerimistaotluse kustutamine

Potentsiaalse hankija registreerimistaotluse eri olekud annavad ülevaate taotluse edenemisest.

Loodud kirjete ahela saate korrastada ja eemaldada ning kasutajakonto inaktiveerida, kasutades potentsiaalse hankija registreerimistaotluse juures tegevust **Kustuta**. Tegevuse **Kustuta** tulemus oleneb potentsiaalse hankija registreerimistaotluse olekust, nagu on näidatud alljärgnevas tabelis.


|          Olek          |                                                                                     Oleku kirjeldus                                                                                      |                                                                                                                                                            Kustutamistegevuse tulemus                                                                                                                                                             |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|           Uus            |                                                                         Taotlusega pole tehtud ühtki tegevust.                                                                          |                                                                                                                                              Potentsiaalse hankija registreerimistaotlus kustutatakse.                                                                                                                                               |
|      Nõutud kasutaja      | Kui valite <strong>Kutsu kasutajat</strong>, saab selle olekuks <strong>Nõutud kasutaja</strong> ja luuakse potentsiaalse kasutaja taotlus, mis saadetakse töövoogu. |                                                                                                          Selle olekuga potentsiaalse hankija registreerimistaotlust ei saa kustutada, sest kasutajataotluse töövoog pole veel lõppenud.                                                                                                          |
|       Kutsutud kasutaja       |                                                               Kasutajataotluse töövoog kinnitatakse ja luuakse kasutaja.                                                               |                                                                                                                      Luuakse kasutaja inaktiveerimistaotlus ja potentsiaalse hankija registreerimistaotlus kustutakse.                                                                                                                      |
| Registreerimine on pooleli |                                                         Uus kasutaja on sisse loginud ja käivitanud hankija registreerimisviisardi.                                                          |                                                                                     Luuakse kasutaja inaktiveerimistaotlus ning kustutatakse potentsiaalse hankija registreerimistaotlus ja hankija registreerimisviisardis sisestatud andmed.                                                                                      |
|  Hankija nõue on loodud  |                                                                     Hankija registreerimisviisard on läbitud.                                                                      | Luuakse kasutaja inaktiveerimistaotlus ning kustutatakse potentsiaalse hankija registreerimistaotlus, hankija registreerimisviisardis sisestatud andmed ja hankija taotlus.<blockquote>[!NOTE]<br>Tegevust <strong>Kustuta</strong> ei saa kasutada, kui hankija taotlus on töövoos ülevaatamisel.</blockquote> |
|         Kinnitatud         |                                                                               Hankija taotlus on kinnitatud.                                                                               |                                                                                                   Potentsiaalse hankija registreerimistaotlus, hankija registreerimisviisardis sisestatud andmed ja hankija taotlus kustutatakse.                                                                                                    |
|         Tagasi lükatud         |                                                                               Hankija taotlus on tagasi lükatud.                                                                               |                                                                                                   Potentsiaalse hankija registreerimistaotlus, hankija registreerimisviisardis sisestatud andmed ja hankija taotlus kustutatakse.                                                                                                    |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]