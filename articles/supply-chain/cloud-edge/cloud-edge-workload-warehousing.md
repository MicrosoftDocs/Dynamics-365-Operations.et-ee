---
title: Laotööde haldamise töökoormused pilv- ja perimeeterskaalaüksustele
description: See teema annab teavet funktsiooni kohta, mis võimaldab skaala ühikutel hallata valitud protsesse teie laohalduse töökoormusest.
author: perlynne
manager: tfeyr
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, SysSecRolesEditUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4ac76ad5cd88c35ac312b8e73d942a692f35c8aa
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516766"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Laotööde haldamise töökoormused pilv- ja perimeeterskaalaüksustele

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> Mitte kogu ettevõtte funktsionaalsus ei ole töökoormuse skaala ühikute kasutamisel avalikus eelvaates täielikult toetatud. Kasutage kindlasti ainult neid protsesse, mida see teema konkreetselt toetab.

## <a name="warehouse-execution-on-scale-units"></a>Lao käivitamine skaala ühikutes

See funktsioon võimaldab skaala ühikutel hallata valitud protsesse laohalduse võimalustest. Pilve skaala üksused käitavad oma töökoormust pilves, kasutades valitud regioonis spetsiaalset töötluse võimsust Microsoft Azure. Serva-skaala ühikute puhul saate käitada mõningaid töömahtusid eraldi ruumides, isegi kui skaala ühikud on pilvest ajutiselt lahti ühendatud.

Selles teemas on laohalduse täideviimistegevused laos, mis on määratletud skaalaüksusena, tuntud kui *Lao täideviimise süsteem* (*WES*).

## <a name="prerequisites"></a>Eeltingimused

Teil peab olema Dynamics 365 Supply Chain Management keskus ja skaalaüksus, mis on rakendatud koos laohalduse töömahuga. Rohkem teavet arhitektuuri ja juurutamisprotsessi kohta leiate teemast [Pilv- ja perimeeterskaalaüksused tootmis- ning laohaldustöökoormuste jaoks](cloud-edge-landing-page.md).

## <a name="how-the-wes-workload-works-on-scale-units"></a>Kuidas toimub WES töökoormus skaalaüksustes

Laohalduse töökoormuse protsesside puhul sünkroonitakse andmed keskuse ja skaala ühikute vahel.

Skaalaühik võib säilitada ainult oma omanduses olevad andmed. Andmete omandiõiguse mõiste skaalaühikutel aitab vältida mitme valdaja konflikti. Seetõttu on oluline, et te mõistate, millised protsessid kuuluvad keskusele ja mis kuuluvad skaala ühikutele.

Skaala ühikutel on järgmised andmed:

- **Voo töötlemise andmed** – Valitud voo protsessi meetodeid käsitletakse osana skaala ühiku voo töötlemisest.
- **Töö töötlemise andmed** – toetatakse järgmist tüüpi töötellimuse töötlust:

    - Lao liikumised (käsitsi teisaldamine ja liikumine malli alusel)
    - Ostutellimused (kõrvaltpaneku töö lao tellimuse kaudu)
    - Müügitellimused (lihtne komplekteerimis- ja laadimistöö)

- **Lao tellimuse kviitungi andmed** – Neid andmeid kasutatakse ainult nende ostutellimuste puhul, mis on lattu käsitsi väljastatud.
- **Numbrimärgi andmed** – Numbrimärke saab luua keskuses ja skaala ühikus. Ette on nähtud spetsiaalne konfliktide käsitlemine. Pidage meeles, et need andmed ei ole lao-spetsiifilised.

## <a name="outbound-process-flow"></a>Väljamineva protsessi voog

Keskusel on järgmised andmed:

- Kõik alusdokumendid (nagu müügitellimused ja üleviimistellimused)
- Tellimuse eraldamine ja väljamineva koormuse töötlemine
- Lattu väljastamine, saadetise loomine ja voo loomisprotsessid

Skaala üksused omavad tegelikku voo töötlemist (nagu töö eraldamine, täiendamise töö ja nõude töö loomine) pärast vabastamist voogu. Seetõttu saavad lao töötajad töödelda väljaminevat tööd kasutades laohalduse rakendust, mis on ühendatud skaala ühikuga.

![Voo töötlemise voog](./media/wes_wave_processing_flow.png "Voo töötlemise voog")

## <a name="inbound-process-flow"></a>Väljamineva protsessi voog

Keskusel on järgmised andmed:

- Kõik alusdokumendid (nagu müügitellimused ja üleviimistellimused)
- Sissetuleva koormuse töötlus

> [!NOTE]
> Sissetuleva ostutellimuse voog erineb kontseptuaalselt väljaminevast voost, kus skaala ühik, mis teeb töötlust, sõltub sellest, kas tellimus on lattu väljastatud.

Kui kasutate *väljalaskmine lattu* protsessi, luuakse laotellimused ja seotud vastuvõtva voo omand on määratud skaala ühikule. Keskus ei saa sissetulevat vastuvõttu registreerida.

Töötaja saab töödelda vastuvõtuprotsessi kasutades laorakendust, mis on ühendatud skaalaühikule. Seejärel salvestatakse andmed skaalajaotisena ja esitatakse sissetuleva lao tellimuse suhtes. Järgnevate eeltöö loomist ja töötlemist käsitleb ka skaalajaotise üksus.

Kui te ei kasuta *väljalaset lattu* ja seetõttu ei kasuta *laotellimusi*, saab keskus töödelda lao sissetulekut ja töötöötlemist sõltumatult skaala ühikutest.

![Sissetuleva protsessi voog](./media/wes_Inbound_flow.png "Sissetuleva protsessi voog")

## <a name="supported-processes-and-roles"></a>Toetatud protsessid ja rollid

Mitte kõiki laohalduse protsesse ei toetata skaala üksuses WES töömahus. Seetõttu soovitame määrata rollid, mis vastavad igale kasutajale saadaolevatele funktsioonidele.

Selle protsessi hõlbustamiseks on demoandmetesse **Süsteemi administreerimine \> Turvalisus \> Turvalisuse konfiguratsioon** kaasatud näiteroll nimega *Laohaldaja töömahus* . Selle rolli eesmärk on võimaldada laohaldajale juurdepääsu skaala ühikule WES. Roll annab juurdepääsu lehekülgedele, mis on asjakohased skaala üksuses majutatud töökoormuse kontekstis.

Kasutajate rollid skaalaühikul määratakse esialgse andmete sünkroniseerimise osana keskusest kuni skaalaühikuni.

Kasutajale määratud rollide muutmiseks minge **Süsteemi administreerimine \> Turvalisus \> Määra kasutajatele roll** skaala ühikul. Kasutajatele, kes toimivad laohaldajatena ainult skaala ühikutel, tuleb määrata ainult *Laohaldur töömahu* rolli. Selline lähenemine tagab, et nendel kasutajatel on juurdepääs ainult toetatud funktsioonidele. Eemaldage kõik teised neile kasutajatele määratud rollid.

Kasutajatele, kes toimivad laohaldajatena nii keskuses kui skaala üksustes peab olema määratud olemasolev *Laotöötajar* roll. Pange tähele, et see roll annab laotöötajatele juurdepääsu funktsioonidele (nt üleviimistellimuse töötlemine), mis kuvatakse kasutajaliideses (UI), kuid mida ei toetata praegu skaala ühikutes.

## <a name="supported-wes-processes"></a>Toetatud WES protsessid

Järgmised lao käivitamise protsessid saab lubada WES töökoormust skaala ühikus:

- Valitud voomeetodid müügitellimustele ja nõudluse täiendamise puhul
- Töökäskude käivitamine müügitellimustest ja nõudluse täiendamisest laorakendust kasutades
- Vaba kaubavaru päring warehouse'i rakenduse abil
- Varude liikumiste loomine ja teostamine laorakenduse abil
- Ostutellimiste registreerimine ja ladustamistööde tegemine laorakenduse abil

Järgmiseid töötellimmused on praegu toetatud WES töömahtudele skaalaüksuste kasutuselevõtmisel.

- Müügitellimused
- Täiendamine
- Lao liikumised
- Ostutellimused, mis on lingitud laotellimustega

Muude lähtedokumendi töötlemist ei toetata praegu skaala ühikutes. Näiteks ei saa skaala üksuse WES töökoormuse puhul teha järgmisi tegevusi:

- Üleviimistellimuse väljastamine.
- Töödeldakse väljamineva kauba komplekteerimise ja saatmise toiminguid.

> [!IMPORTANT]
> Kui kasutate skaala üksuses töömahtu, ei saa te käitada mittetoetavaid protsesse kindla lao jaoks keskuses.

Järgmised laohalduse funktsioonid ei ole praegu skaala üksustes toetatud.

- Sissetuleva ja väljamineva töötlemise kaubad, millel on aktiivsed liikumise dimensioonid (nt partii-või seerianumbri dimensioonid)
- Varude oleku muudatuste töötlemine
- Blokeeritud olekuga varude töötlemine
- Integratsioon kvaliteedijuhtimisega
- Integratsioon tootmisega
- Toodete tegeliku kaalu töötlemine
- Ületarne ja alatarne töötlemine
- Negatiivse vaba kaubainventuuri töötlemine

### <a name="outbound-supported-only-for-sales-orders-and-demand-replenishment"></a>Väljaminev (toetatud ainult müügitellimuste ja nõudluse täiendamise puhul)

Järgmine tabel näitab, milliseid väljaminevaid funktsioone toetatakse ja kus neid toetatakse, kui laohalduse töömahtusid kasutatakse pilve ja perimeeterskaala üksustes.

> [!WARNING]
> Kuna ainult müügitellimuse töötlemist toetatakse, ei saa väljaminevat laohalduse töötlemist kasutada üleviimistellimuste puhul.
>
> Mõned laofunktsioonid ei ole saadaval ladudes, kus laohalduse töökoormust käitatakse skaalaüksustes.

| Töötle                                                      | Keskus | WES-i töökoormus skaalaüksusel |
|--------------------------------------------------------------|-----|------------------------------|
| Lähtedokumendi töötlemine                                   | Jah | Ei |
| Laadimise ja transpordijuhtimise töötlemine                | Jah | Ei |
| Lattu väljastamine                                         | Jah | Ei |
| Saadetise konsolideerimine                                       | Ei  | Ei |
| Ristlaadimine (komplekteerimistöö)                                 | Ei  | Ei |
| Saatmisvoo töötlemine                                     | Ei, kuid voo oleku lõpetamist käsitletakse keskuses |<p>Jah, kuid järgmised võimalused ei ole toetatud.</p><ul><li>Paralleelse töö loomine</li><li>Koorma koostamine ja sorteerimine</li><li>Konteinerisse määramine</li><li>Voosildi printimine</li></li></ul><p><b>NB:</b> juurdepääs keskusele on vajalik, et lõpetada voo staatus osana voo töötlusest.</p> |
| Laotöö töötlemine (sh litsentsiplaadi printimine)     | Ei  | <p>Jah, kuid ainult järgmiste võimaluste puhul:</p><ul><li>Komplekteerimine (aktiivse jälgimise dimensioonide kasutamata)</li><li>Komplekteerimine (aktiivse jälgimise dimensioonide kasutamata)</li></ul> |
| Kogumi komplekteerimine                                              | Ei  | Ei |
| Pakkimise töötlemine                                           | Ei  | Ei |
| Väljamineva sortimise töötlemine                                  | Ei  | Ei |
| Koormaga seotud dokumentide printimine                           | Jah | Ei |
| Konossemendi ja ASN-i loomine                            | Jah | Ei |
| Saadetise kinnitus ja saatelehe töötlemine                | Jah | Ei |
| Lühike komplekteerimine (müügitellimused)                                 | Ei  | Ei |
| Töö tühistamine                                            | Ei  | Ei |
| Tööasukohtade muutmine (müügitellimused)                      | Ei  | Ei |
| Lõpeta töö (müügitellimused)                                 | Ei  | Ei |
| Blokeeri ja deblokeeri töö                                       | Ei  | Ei |
| Muuda kasutajat                                                  | Ei  | Ei |
| Tööaruande printimine                                            | Ei  | Ei |
| Voo silt                                                   | Ei  | Ei |
| Tühista töö                                                 | Ei  | Ei |

### <a name="inbound"></a>Sissetulev

Järgnev tabel näitab, milliseid sissetulevaid funktsioone toetatakse ja kus neid toetatakse, kui laohalduse töömahtusid kasutatakse pilve ja perimeeterskaala üksustes.

| Töötle                                                          | Keskus | WES-i töökoormus skaalaüksusel |
|------------------------------------------------------------------|-----|------------------------------|
| Lähte&nbsp;dokumendi&nbsp;töötlemine                                       | Jah | Ei |
| Laadimise ja transpordijuhtimise töötlemine                    | Jah | Ei |
| Saadetise kinnitus                                            | Jah | Ei |
| Ostutellimuse vabastamine lattu (lao tellimuse töötlemine) | Jah | Ei |
| Vastuvõttev ostutellimuse üksus ja kõrvaleseadmine                        | <p>Jah,&nbsp;kui &nbsp;sinna&nbsp;lao tellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | <p>Jah, kui on olemas lao tellimus, ja kui ostutellimus pole osa <i>koormast</i>. Siiski tuleb kasutada kaht mobiilse seadme menüükäsku, ühte vastuvõtmiseks (<i>Ostutellimuse kauba vastuvõtmine</i>) ja teist, koos <b>Kasuta olemasolevat tööd</b> võimalusega eeltöö töötlemiseks.</p><p>Ei, kui ei ole laotellimust.</p> |
| Vastuvõttev ostutellimuse rida ja kõrvaleseadmine                        | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | Ei |
| Tagastustellimuse vastuvõtt ja kõrvaleseadmine                               | Jah | Ei |
| Kombineeritud litsentsiplaadi vastuvõtt ja kõrvaleseadmine                        | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | Ei |
| Vastuvõetav koormas olev kaup                                              | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | Ei |
| Litsentsiplaadi vastuvõtt ja kõrvaleseadmine                              | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | Ei |
| Vastuvõttev edastustellimuse üksus ja kõrvaleseadmine                        | Jah | Ei |
| Vastuvõetava ja kõrvaleseatava tellimuserea ülekanne                        | Jah | Ei |
| Töö tühistamine                                                | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | <p>Jah, kuid <b>registreerimise tühistamist töö tühistamisel</b> valikul ( <b>laohalduse parameetrite</b> lehel) ei toetata.</p> |
| Ostutellimuse toote tšeki töötlemine                        | Jah | Ei |
| Ristlaadimise töö loomine vastuvõtmise osana                 | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | Ei |

### <a name="warehouse-operations-and-exception-handing"></a>Lao toimingud ja erandi üleandmine

Järgnev tabel näitab, milliseid lao toiminguid ja erandi üleandmise funktsioone toetatakse ja kus neid toetatakse, kui laohalduse töömahtusid kasutatakse pilve ja perimeeterskaala üksustes.

| Töötle                                            | Keskus | WES-i töökoormus skaalaüksusel |
|----------------------------------------------------|-----|------------------------------|
| Numbrimärgi päring                              | Jah | Jah                          |
| Kauba päring                                       | Jah | Jah                          |
| Asukoha päring                                   | Jah | Jah                          |
| Vaheta ladu                                   | Jah | Jah                          |
| Liikumine                                           | Ei  | Jah                          |
| Teisaldus malli alusel                               | Ei  | Jah                          |
| Korrigeerimine (sisse/välja)                                | Jah | Ei                           |
| Tsüklilise inventuuri ja inventuuri lahknevuse töötlemine | Jah | Ei                           |
| Prindi silt uuesti (Litsentsiplaadi printimise)             | Jah | Ei                           |
| Litsentsiplaadi koostamine                                | Jah | Ei                           |
| Litsentsiplaadi vahe                                | Jah | Ei                           |
| Juhi sisseregistreerimine                                    | Jah | Ei                           |
| Juhi väljaregistreerimine                                   | Jah | Ei                           |
| Partii likvideerimiskoodi muutmine                      | Jah | Ei                           |
| Kuva avatud tööloend                             | Jah | Ei                           |
| Konsolideeri identifitseerimismärgised                         | Ei  | Ei                           |
| Eemalda konteiner grupist                        | Ei  | Ei                           |
| Tühista töö                                        | Ei  | Ei                           |
| Min-max täiendamise töötlus                   | Ei  | Ei                           |
| Laoruumi täiendamise töötlemine                  | Ei  | Ei                           |

### <a name="production"></a>Tootmine

Laohalduse integratsiooni tootmisstsenaariumitele ei toetata praegu, nagu näidatud järgmises tabelis.

| Töötle | Keskus | WES-i töökoormus skaalaüksusel |
|---------|-----|------------------------------|
| <p>Kõik laohalduse protsessid, mis on seotud tootmisega. Järgmisena on toodud mõned näited.</p><li>Lattu väljastamine</li><li>Tootmisvoo töötlemine</li><li>Toormaterjalide komplekteerimine</li><li>Lõpetatud kaupade kõrvalepanek</li><li>Kaastoodete ja kõrvalsaaduste kõrvalepanek</li><li>Kanbani kõrvalepanek</li><li>Kanbani komplekteerimine</li><li>Käivita tootmistellimus</li><li>Tootmise praak</li><li>Tootmise viimane kaubaalus</li><li>Materjali tarbimise registreerimine</li><li>Tühi kanban</li></ul> | Ei | Ei |

## <a name="maintaining-scale-units-for-wes"></a>WES-i jaoks skaalaüksuste haldamine

Mitu partii-tööd töötavad nii keskuses kui ka skaalaüksustes.

Keskuse juurutamisel saate pakett-töid käsitsi hallata. Jaotises **Laohaldus \> Perioodilised ülesanded \> Tagatoa töökoormuse haldamine**:

- Tööoleku värskendussündmuste töötlemine
- Töötle voo käitamise juhtimise edastussündmust
- Lähtetellimuse sissetulekute registreerimine

Skaalaüksustes saate töökoormuse korral hallata järgmist kahte pakett-tööd jaotises **Laohaldus \> Perioodilised ülesannded \> Töökoormuse haldamine**.

- Vootabeli kirjete töötlemine
- Töötle voo käitamise juhtimise edastussündmust


[!INCLUDE[footer-include](../../includes/footer-banner.md)]