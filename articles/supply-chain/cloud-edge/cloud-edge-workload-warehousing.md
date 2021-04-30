---
title: Laotööde haldamise töökoormused pilv- ja perimeeterskaalaüksustele
description: See teema annab teavet funktsiooni kohta, mis võimaldab skaala ühikutel hallata valitud protsesse teie laohalduse töökoormusest.
author: perlynne
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, SysSecRolesEditUsers
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d6dffb1ea03b8d11519087163d2837d6cfe3df4e
ms.sourcegitcommit: 639175a39da38edd13e21eeb5a1a5ca62fa44d99
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/15/2021
ms.locfileid: "5899163"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Laohaldustöökoormused pilv- ja perimeeterskaalaüksuste jaoks

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> Töökoormust skaalaüksuses käitavate ladude puhul pole kõik laohaldusettevõtte funktsioonid täielikult toetatud. Kasutage kindlasti ainult neid protsesse, mida see teema konkreetselt toetab.

## <a name="warehouse-execution-on-scale-units"></a>Lao käivitamine skaala ühikutes

See funktsioon võimaldab skaala ühikutel hallata valitud protsesse laohalduse võimalustest.

Selles teemas on laohalduse täideviimistegevused laos, mis on määratletud skaalaüksusena, tuntud kui *Lao täideviimise süsteem* (*WES*).

## <a name="prerequisites"></a>Eeltingimused

Teil peab olema Dynamics 365 Supply Chain Management keskus ja skaalaüksus, mis on rakendatud koos laohalduse töömahuga. Rohkem teavet arhitektuuri ja juurutamisprotsessi kohta leiate teemast [Tarneahela haldamise töökoormuste vastupidavuse suurendamiseks kasutage skaalaühikuid](cloud-edge-landing-page.md).

## <a name="how-the-wes-workload-works-on-scale-units"></a>Kuidas toimub WES töökoormus skaalaüksustes

Laohalduse töökoormuse protsesside puhul sünkroonitakse andmed keskuse ja skaala ühikute vahel.

Skaalaühik võib säilitada ainult oma omanduses olevad andmed. Andmete omandiõiguse mõiste skaalaühikutel aitab vältida mitme valdaja konflikti. Seetõttu on oluline, et te mõistate, millised protsessid kuuluvad keskusele ja mis kuuluvad skaala ühikutele.

Skaala ühikutel on järgmised andmed:

- **Voo töötlemise andmed** – Valitud voo protsessi meetodeid käsitletakse osana skaala ühiku voo töötlemisest.
- **Töö töötlemise andmed** – toetatakse järgmist tüüpi töötellimuse töötlust:

  - **Lao liikumised** (käsitsi teisaldamine ja liikumine malli alusel)
  - **Ostutellimused** (laotellimuse kaudu tehtud ladustamistöö, kui ostutellimused pole koormatega seostatud)
  - **Müügitellimused** (lihtne komplekteerimis- ja laadimistöö)
  - **Üleviimistellimused** (ainult väljaminek lihtsa komplekteerimis- ja laadimistööga)

- **Lao tellimuse kviitungi andmed** – Neid andmeid kasutatakse ainult nende ostutellimuste puhul, mis on lattu käsitsi väljastatud.
- **Numbrimärgi andmed** – Numbrimärke saab luua keskuses ja skaala ühikus. Ette on nähtud spetsiaalne konfliktide käsitlemine. Pidage meeles, et need andmed ei ole lao-spetsiifilised.

## <a name="outbound-process-flow"></a>Väljamineva protsessi voog

Keskusel on järgmised andmed:

- Kõik alusdokumendid (nagu müügitellimused ja üleviimistellimused)
- Tellimuse eraldamine ja väljamineva koormuse töötlemine
- Lattu väljastamise, saadetise loomise, voo loomise ja voo lõpetamise protsessid

Skaala üksused omavad tegelikku voo töötlemist (nagu töö eraldamine, täiendamise töö ja nõude töö loomine) pärast vabastamist voogu. Seetõttu saavad lao töötajad töödelda väljaminevat tööd kasutades mobiilirakendust Warehouse Management, mis on ühendatud skaala ühikuga.

![Voo töötlemise voog](./media/wes-wave-processing-ga.png "Voo töötlemise voog")

## <a name="inbound-process-flow"></a>Väljamineva protsessi voog

Keskusel on järgmised andmed:

- Kõik alusdokumendid (nagu müügitellimused ja üleviimistellimused)
- Sissetuleva koormuse töötlus
- Kõik kulude ja finantsvärskendused

> [!NOTE]
> Sissetuleva ostutellimuse voog erineb kontseptuaalselt väljaminevast voost. Võite kasutada sama ladu kas skaleerimisüksuse või keskusega, sõltuvalt sellest, kas ostutellimus on lattu väljastatud või mitte. Kui olete tellimuse lattu väljastanud, saate selle tellimusega töötada ainult siis, kui olete skaalaüksusesse sisse logitud.

Kui kasutate protsessi *Lattu väljastamine*, luuakse [*laotellimused*](cloud-edge-warehouse-order.md) ja seotud vastuvõtva voo omand määratakse skaalaüksusele. Keskus ei saa sissetulevat vastuvõttu registreerida.

Protsessi *Lattu väljastamine* kasutamiseks peate keskusesse sisse logima. Selle käivitamiseks või plaanimiseks avage üks järgmistest lehtedest:

- **Hanked > Ostutellimused > Kõik ostutellimused > Ladu > Tegevused > Lattu väljastamine**
- **Laohaldus > Lattu väljastamine > Müügitellimuste automaatne väljastamine**

Kui kasutate **ostutellimuste automaatset väljastamist**, siis saate päringu põhjal valida konkreetsed ostutellimuse read. Tavaline stsenaarium oleks häälestada korduv pakett-töö, millega väljastatakse kõik kinnitatud ostutellimuse read, mis saabuvad järgmisel päeval.

Töötaja saab töödelda vastuvõtuprotsessi kasutades mobiilirakendust Warehouse Management, mis on ühendatud skaalaühikule. Seejärel salvestatakse andmed skaalajaotisena ja esitatakse sissetuleva lao tellimuse suhtes. Järgnevate eeltöö loomist ja töötlemist käsitleb ka skaalajaotise üksus.

Kui te ei kasuta *väljalaset lattu* ja seetõttu ei kasuta *laotellimusi*, saab keskus töödelda lao sissetulekut ja töötöötlemist sõltumatult skaala ühikutest.

![Sissetuleva protsessi voog](./media/wes-inbound-ga.png "Sissetuleva protsessi voog")

## <a name="supported-processes-and-roles"></a>Toetatud protsessid ja rollid

Mitte kõiki laohalduse protsesse ei toetata skaala üksuses WES töömahus. Seetõttu soovitame määrata rollid, mis vastavad igale kasutajale saadaolevatele funktsioonidele.

Selle protsessi hõlbustamiseks on demoandmetesse **Süsteemi administreerimine \> Turvalisus \> Turvalisuse konfiguratsioon** kaasatud näiteroll nimega *Laohaldaja töömahus* . Selle rolli eesmärk on võimaldada laohaldajale juurdepääsu skaala ühikule WES. Roll annab juurdepääsu lehekülgedele, mis on asjakohased skaala üksuses majutatud töökoormuse kontekstis.

Kasutajate rollid skaalaühikul määratakse esialgse andmete sünkroniseerimise osana keskusest kuni skaalaühikuni.

Kasutajale määratud rollide muutmiseks avage **Süsteemihaldus \> Turvalisus \> Määra rollidele kasutajad**. Kasutajatele, kes toimivad laohaldajatena ainult skaala ühikutel, tuleb määrata ainult *Laohaldur töömahu* rolli. Selline lähenemine tagab, et nendel kasutajatel on juurdepääs ainult toetatud funktsioonidele. Eemaldage kõik teised neile kasutajatele määratud rollid.

Kasutajatele, kes toimivad laohaldajatena nii keskuses kui skaala üksustes peab olema määratud olemasolev *Laotöötajar* roll. Pange tähele, et see roll annab laotöötajatele juurdepääsu funktsioonidele (nt üleviimistellimuse vastuvõtmise töötlemine), mis kuvatakse kasutajaliideses (UI), kuid mida ei toetata praegu skaala ühikutes.

## <a name="supported-wes-processes"></a>Toetatud WES protsessid

Järgmised lao käivitamise protsessid saab lubada WES töökoormust skaala ühikus:

- Valitud müügi- ja üleviimistellimuste voomeetodid (eraldamine, nõudluse täiendamine, konteinerisse määramine, töö loomine ja voo sildi printimine)
- Mobiilirakenduse Warehouse Management abil müügi- ja üleviimistellimuse laotöö töötlemine (sh täiendustöö)
- Vaba kaubavaru päring mobiilirakenduse Warehouse Management abil
- Varude liikumiste loomine ja teostamine mobiilirakenduse Warehouse Management abil
- Ostutellimiste registreerimine ja ladustamistööde tegemine mobiilirakenduse Warehouse Management abil

Järgmiseid töötellimmused on praegu toetatud WES töömahtudele skaalaüksuste kasutuselevõtmisel.

- Müügitellimused
- Edastuse väljaminek
- Täiendamine
- Lao liikumised
- Ostutellimused (laotellimustega lingitud)

Skaalaüksustes ei toetata ühtegi teist tüüpi lähtedokumentide töötlemist ega laotööd. Näiteks skaalaüksuse WES-i töökoormuse puhul ei saa te teha üleviimistellimuse vastuvõtmise töötlemist (üleviimistarne) ega töödelda tsüklilise inventuuri tööd.

> [!NOTE]
> Toetuseta funktsioonide mobiilse seadme menüüelemente ega nuppe ei näidata _mobiilirakenduses Warehouse Management_, kui see on skaalaüksuse juurutusega ühendatud.

> [!WARNING]
> Kui käitate skaalaüksuses töömahu, ei saa te käitada mittetoetavaid protsesse kindla lao jaoks keskuses. Selles teemas hiljem toodud tabelid dokumenteerivad toetatud võimalusi.
>
> Valitud lao töötüüpe saab luua nii keskuses kui ka skaalaüksuses, kuid seda saab säilitada ainult omanikust keskus või skaalaüksus (andmed loonud juurutus).
>
> Isegi kui skaalaühik toetab kindlat protsessi, arvestage sellega, et kõiki vajalikke andmeid ei pruugita keskusest skaalaühikusse või skaalaühikust keskusesse sünkroonida, mis võib tuua kaasa ootamatu süsteemitöötluse. Näited on järgmised.
> 
> - Kui kasutate asukohakorralduse päringut, mis ühendab andmetabeli kirje, mis on olemas ainult keskuse juurutamisel.
> - Kui kasutate asukoha oleku ja/või asukoha mahulise koormuse funktsioone. Neid andmeid ei sünkroonita juurutuste vahel ja seega töötavad ainult asukoha vaba kaubavaru värskendamisel ühes juurutuses.

Järgmised laohalduse funktsioonid ei ole praegu skaalaühiku töökoormustes toetatud.

- Koormusele määratud ostutellimuse ridade sissetulev töötlemine
- Projekti ostutellimuste sissetulev töötlemine
- Sissetuleva ja väljamineva töötlemise kaubad, millel on aktiivsed liikumise dimensioonid **Omanik** ja/või **Seerianumber**
- Blokeeritud olekuga varude töötlemine
- Varuda oleku muutmine mis tahes töö liikumisprotsessi ajal
- Tellimusega kooskõlastatud paindliku dimensiooni reserveerimised
- Funktsiooni *Lao asukoha olek* kasutus (andmeid juurutuste vahel ei sünkroonita)
- Funktsiooni *Asukoha litsentsiplaadi paigutus* kasutamine
- Suvandite *Tootefiltrid* ja *Tootefiltrite rühmad* kasutus, sh säte **Päevade arv partiide segamiseks**
- Integratsioon kvaliteedijuhtimisega
- Toodete tegeliku kaaluga töötlemine
- Töötlemine üksustega, mis on lubatud ainult transpordihalduse (TMS) jaoks
- Negatiivse vaba kaubainventuuriga töötlemine
- Laotöö töötlemine kohandatud töötüüpidega
- Laotöö töötlemine saadetise märkustega
- Laotöö töötlemine tsüklilise inventuuri läve käivitamisega
- Laotöö töötlemine koos materjali töötlemisega / lao automatiseerimisega
- Toote põhiandmete pildi kasutamine (näiteks mobiilirakenduses Warehouse Management)

> [!WARNING]
> Mõned laofunktsioonid ei ole saadaval ladude puhul, mis käitavad laohalduse töökoormusi skaalaüksuses, ning samuti ei toetata seda keskuse või skaalaüksuse töökoormusega.
> 
> Teisi võimalusi saab töödelda mõlemas, kuid nõuab teatud stsenaariumites hoolikat kasutamist, nt kui vaba kaubavaru värskendatakse asünkroonse andmevärskendusprotsessi tõttu samas laos nii keskuse kui ka skaalaüksuse puhul.
> 
> Kindlaid funktsioone (nt *töö blokeerimine*), mida toetatakse nii keskuses kui ka skaalaüksuses, toetatakse ainult andmete omaniku jaoks.

### <a name="outbound-supported-only-for-sales-and-transfer-orders"></a>Väljaminev (toetatud ainult müügi- ja üleviimistellimuste puhul)

Järgmine tabel näitab, milliseid väljaminevaid funktsioone toetatakse ja kus neid toetatakse, kui laohalduse töömahtusid kasutatakse pilve ja perimeeterskaala üksustes.

| Töötle                                                      | Keskus | WES-i töökoormus skaalaüksusel |
|--------------------------------------------------------------|-----|------------------------------|
| Lähtedokumendi töötlemine                                   | Jah | Ei |
| Laadimise ja transpordijuhtimise töötlemine                | Jah | Ei |
| Lattu väljastamine                                         | Jah | Ei |
| Plaanitud ristlaadimine                                        | Ei  | Ei |
| Saadetise konsolideerimine                                       | Jah | Ei |
| Saatmisvoo töötlemine                                     | Jah, kuid ainult voo lähtestamist ja lõpetamist käsitletakse keskuses. See tähendab, et väljamineva ülekande ja müügitellimuse töötlemist saab käsitseda ainult skaalaühikuga.|<p>Ei, lähtestamist ja lõpetamist käsitsetakse keskusega ning suvandit **Koorma koostamine ja sorteerimine** ei toetata<p><b>NB:</b> juurdepääs keskusele on vajalik, et lõpetada voo staatus osana voo töötlusest.</p> |
| Voo saadetiste hooldamine                                  | Jah | Ei |
| Laotöö töötlemine (sh litsentsiplaadi printimine)        | Ei  | <p>Jah, kuid ainult ülalnimetatud toetatud võimaluste puhul. |
| Kogumi komplekteerimine                                              | Ei  | Jah|
| Käsitsi pakkimise töötlemine, sh pakitud konteinerite komplekteerimise töö töötlemine                                           | Ei <P>Teatud töötlust saab teha pärast algset komplekteerimisprotsessi, mida käsitseb skaalaüksus, kuid pole soovitatav järgmiste blokeeritud toimingute tõttu.</p>  | Ei  |
| Eemalda konteiner grupist                        | Ei  | Ei                           |
| Väljamineva sortimise töötlemine                                  | Ei  | Ei |
| Koormaga seotud dokumentide printimine                           | Jah | Ei |
| Konossemendi ja ASN-i loomine                            | Jah | Ei |
| Saadetise kinnitus                    | Jah  | Ei |
| Saadetise kinnitamine valikuga „Kinnita ja edasta”                    | Ei  | Ei |
| Saatelehe ja arve töötlemine                | Jah | Ei |
| Kiire komplekteerimine (müügi- ja üleviimistellimused)                    | Ei  | Ei |
| Ümberkomplekteerimine (müügi- ja üleviimistellimused)                     | Ei  | Ei |
| Tööasukohtade muutmine (müügi- ja üleviimistellimused)         | Ei  | Jah|
| Töö lõpetamine (müügi- ja üleviimistellimused)                    | Ei  | Jah|
| Tööaruande printimine                                            | Jah | Ei |
| Voo silt                                                   | Ei  | Jah|
| Töö tükeldamine                                                   | Ei  | Jah|
| Töö töötlemine – suunaja: transpordi laadimine            | Ei  | Ei |
| Vähenda komplekteeritavat kogust                                       | Ei  | Ei |
| Tühista töö                                                 | Ei  | Ei |
| Saadetise kinnitamise ümberpööramine                                | Jah | Ei |

### <a name="inbound"></a>Sissetulev

Järgnev tabel näitab, milliseid sissetulevaid funktsioone toetatakse ja kus neid toetatakse, kui laohalduse töömahtusid kasutatakse pilve ja perimeeterskaala üksustes.

| Töötle                                                          | Keskus | WES-i töökoormus skaalaüksusel<BR>*(Valikuga „Jah” märgitud üksused rakenduvad ainult laotellimustele)*</p> |
|------------------------------------------------------------------|-----|----------------------------------------------------------------------------------|
| Lähte&nbsp;dokumendi&nbsp;töötlemine                                       | Jah | Ei |
| Laadimise ja transpordijuhtimise töötlemine                    | Jah | Ei |
| Sissetuleva saadetise kinnitus                                            | Jah | Ei |
| Ostutellimuse vabastamine lattu (lao tellimuse töötlemine) | Jah | Ei |
| Laotellimuse ridade tühistamine<p>Pange tähele, et seda toetatakse ainult siis, kui rea suhtes pole registreerimist toimunud</p>          | Jah | Ei |
| Vastuvõttev ostutellimuse üksus ja kõrvaleseadmine                       | <p>Jah,&nbsp;kui &nbsp;sinna&nbsp;lao tellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | <p>Jah, kui ostutellimus pole <i>koormuse</i> osa</p> |
| Vastuvõttev ostutellimuse rida ja kõrvaleseadmine                        | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | <p>Jah, kui ostutellimus pole <i>koormuse</i> osa</p></p> |
| Tagastustellimuse vastuvõtt ja kõrvaleseadmine                               | Jah | Ei |
| Kombineeritud litsentsiplaadi vastuvõtt ja kõrvaleseadmine                        | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | Ei |
| Vastuvõetav koormas olev kaup                                             | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | Ei |
| Litsentsiplaadi vastuvõtt ja kõrvaleseadmine                              | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | Ei |
| Vastuvõttev edastustellimuse üksus ja kõrvaleseadmine                        | Jah | Ei |
| Vastuvõetava ja kõrvaleseatava tellimuserea ülekanne                        | Jah | Ei |
| Töö tühistamine (sissetulev)                                              | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | <p>Jah, kuid ainult siis, kui valik <b>Tühista registreerimine töö tühistamisel</b> (lehel <b>Laohalduse parameetrid</b>) on tühistatud</p> |
| Ostutellimuse toote tšeki töötlemine                          | Jah | Ei |
| Ostutellimuse vastuvõtmine alatarnega                        | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | Jah, kuid ainult keskusest tühistamistaotluse tegemisega |
| Ostutellimuse vastuvõtmine ületarnega                        | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | Jah  |
| Vastuvõtmine koos töö *Ristlaadimine* loomisega                   | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | Ei |
| Vastuvõtmine koos töö *Kvaliteettellimus* loomisega                  | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | Ei |
| Vastuvõtmine koos töö *Kauba kvaliteedivalim* loomisega          | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | Ei |
| Vastuvõtmine koos töö *Kvaliteet kvaliteedikontrollis* loomisega       | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | Ei |
| Vastuvõtmine koos kvaliteettellimuse loomisega                            | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | Ei |
| Töö töötlemine – suunaja: *Kogumi kõrvalepanek*                             | Jah | Ei |
| Töö töötlemine koos *kiire komplekteerimisega*                                           | Jah | Ei |
| Litsentsiplaadi laadimine                                           | Jah | Ei |

### <a name="warehouse-operations-and-exception-handing"></a>Lao toimingud ja erandi üleandmine

Järgnev tabel näitab, milliseid lao toiminguid ja erandi üleandmise funktsioone toetatakse ja kus neid toetatakse, kui laohalduse töömahtusid kasutatakse pilve ja perimeeterskaala üksustes.

| Töötle                                            | Keskus | WES-i töökoormus skaalaüksusel |
|----------------------------------------------------|-----|------------------------------|
| Numbrimärgi päring                              | Jah | Jah                          |
| Kauba päring                                       | Jah | Jah                          |
| Asukoha päring                                   | Jah | Jah                          |
| Vaheta ladu                                   | Jah | Jah                          |
| Liikumine                                           | Jah | Jah                          |
| Teisaldus malli alusel                               | Jah | Jah                          |
| Edastus laos                                 | Jah | Ei                           |
| Üleviimistellimuse loomine mobiilirakenduses Warehouse Management           | Jah | Ei                           |
| Korrigeerimine (sisse/välja)                                | Jah | Ei                           |
| Varude oleku muutmine                            | Jah | Ei                           |
| Tsüklilise inventuuri ja inventuuri lahknevuse töötlemine | Jah | Ei                           |
| Prindi silt uuesti (Litsentsiplaadi printimise)             | Jah | Jah                          |
| Litsentsiplaadi koostamine                                | Jah | Ei                           |
| Litsentsiplaadi vahe                                | Jah | Ei                           |
| Paki pesastatud litsentsiplaatidesse                                | Jah | Ei                           |
| Juhi sisseregistreerimine                                    | Jah | Ei                           |
| Juhi väljaregistreerimine                                   | Jah | Ei                           |
| Partii likvideerimiskoodi muutmine                      | Jah | Jah                          |
| Kuva avatud tööloend                             | Jah | Jah                          |
| Konsolideeri identifitseerimismärgised                         | Jah | Ei                           |
| Min/max ja tsooni läve varude täiendamise töötlemine| Jah <p>Soovitatav on sama asukohta päringute osana mitte kaasata</p>| Jah                          |
| Laoruumi täiendamise töötlemine                  | Jah  | Jah<p>Pange tähele, et seadistus tuleb teha skaalaüksuses</p>                           |
| Blokeeri ja deblokeeri töö                             | Jah | Jah                          |
| Muuda kasutajat                                        | Jah | Jah                          |
| Töö töökausta muutmine                           | Jah | Jah                          |
| Tühista töö                                        | Jah | Jah                          |


### <a name="production"></a>Tootmine

Laohalduse tootmisstsenaariumeid praegu skaalaüksuse töökoormustes ei toetata, nagu järgmises tabelis on näidatud.

| Töötle | Keskus | WES-i töökoormus skaalaüksusel |
|---------|-----|------------------------------|
| <p>Kõik laohalduse protsessid, mis on seotud tootmisega. Järgmisena on toodud mõned näited.</p><li>Lattu väljastamine</li><li>Tootmisvoo töötlemine</li><li>Toormaterjalide komplekteerimine</li><li>RAF-i ja lõpetatud kaupade kõrvalepanek</li><li>Kaastoodete ja kõrvalsaaduste kõrvalepanek</li><li>Kanbani kõrvalepanek</li><li>Kanbani komplekteerimine</li><li>Käivita tootmistellimus</li><li>Tootmise praak</li><li>Tootmise viimane kaubaalus</li><li>Materjali tarbimise registreerimine</li><li>Tühi kanban</li></ul> | Jah | Ei |

## <a name="maintaining-scale-units-for-wes"></a>WES-i jaoks skaalaüksuste haldamine

Mitu partii-tööd töötavad nii keskuses kui ka skaalaüksustes.

Keskuse juurutamisel saate pakett-töid käsitsi hallata. Saate järgmisi pakett-töösid hallata suvandis **Laohaldus \> Perioodilised ülesanded \> Tagatoa töökoormuse haldamine**:

- Tööoleku värskendussündmuste töötlemine
- Skaalaüksus keskusesse sõnumiprotsessor
- Lähtetellimuse sissetulekute registreerimine
- Lõpeta laotellimused
- Laotellimuse ridade töötlemise koguse värskenduse vastused

Skaalaüksustes saate töökoormuse korral hallata järgmisi pakett-töösid suvandis **Laohaldus \> Perioodilised ülesanded \> Töökoormuse haldamine**.

- Vootabeli kirjete töötlemine
- Lao keskusest skaalaüksusesse sõnumiprotsessor
- Laotellimuse ridade töötlemise koguse värskendustaotlused

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
