---
title: Laotööde haldamise töökoormused pilv- ja perimeeterskaalaüksustele
description: See teema annab teavet funktsiooni kohta, mis võimaldab skaala ühikutel hallata valitud protsesse teie laohalduse töökoormusest.
author: perlynne
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, SysSecRolesEditUsers, SysWorkloadDuplicateRecord
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: ae8e9791b590a32581b66853f55ea11bc389bb19
ms.sourcegitcommit: 96515ddbe2f65905140b16088ba62e9b258863fa
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/04/2021
ms.locfileid: "7891747"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Laohaldustöökoormused pilv- ja perimeeterskaalaüksuste jaoks

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Töökoormust skaalaüksuses käitavate ladude puhul pole kõik laohaldusettevõtte funktsioonid täielikult toetatud. Kasutage kindlasti ainult neid protsesse, mida see teema konkreetselt toetab.

## <a name="warehouse-execution-on-scale-units"></a>Lao käivitamine skaala ühikutes

Warehouse management töökoormused võimaldavad pilve- ja servaskaala üksustel käitada laohalduse võimalustest valitud protsesse.

## <a name="prerequisites"></a>Eeltingimused

Teil peab olema Dynamics 365 Supply Chain Management keskus ja skaalaüksus, mis on rakendatud koos laohalduse töömahuga. Lisateavet arhitektuuri ja juurutamisprotsessi kohta vt [skaala ühikutest jaotatud hübriidtopoloogias](cloud-edge-landing-page.md).

## <a name="how-the-warehouse-execution-workload-works-on-scale-units"></a>Kuidas toimib laohalduse ellurakenduse töökoormus skaalaüksustes

Laohalduse töökoormuse protsesside puhul sünkroonitakse andmed keskuse ja skaala ühikute vahel.

Skaalaühik võib säilitada ainult oma omanduses olevad andmed. Andmete omandiõiguse mõiste skaalaühikutel aitab vältida mitme valdaja konflikti. Seetõttu on oluline, et te mõistate, millised protsessid kuuluvad keskusele ja mis kuuluvad skaala ühikutele.

Äriprotsessidest olenevalt võivad samad andmekirjed muuta keskuse ja kaalu üksuste omavahelist kuuluvust. Näide selle stsenaariumi kohta on toodud järgmises jaotises.

> [!IMPORTANT]
> Osa andmeid saab luua nii keskuses kui skaalaühikus. Näited hõlmavad **litsentsiplaate** ja **partiinumbreid**. Sihtotstarbelise konflikti käsitlemine on antud stsenaariumi korral, kus sama kordumatu kirje luuakse nii keskuses kui ka kaaluühikus sama sünkroonimistsükli jooksul. Kui see juhtub, nurjub järgmine sünkroonimine ja te peate minema **Süsteemihaldusse > Päringud > Töökoormuse päringud > Duplikaatkirjed**, kus saate andmeid vaadata ja ühendada.

## <a name="outbound-process-flow"></a>Väljamineva protsessi voog

Enne laohalduse töökoormuse juurutamist pilve või servaskaala ühikus veenduge, et teil on ettevõtte keskuses lubatud väljastamistellimuste funktsiooni lattu vabastamiseks *kaaluüksuse* tugi. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *kaaluühiku tugi lähetustellimuste lattu vabastamiseks*

Väljamineva andme omandiõiguse protsess sõltub sellest, kas kasutate koorma planeerimise protsessi. Kõigil juhtudel omab keskus *lähtedokumente* näiteks müügitellimusi ja seotud tellimuse kande andmeid, nagu ka üleviimistellimusi ja sellega seotud tellimuse kandeandmeid. Kuid kui kasutate koorma planeerimise protsessi, luuakse koormad keskusesse ja seetõttu on need algselt keskuse omad. Osana *lattu vabastamise* protsessist edastatakse koormuse andmete omand sihtotstarbelisesse skaalaüksuse juurutusse, millest saab *saadetise voo protsessi* omanik (nagu näiteks töö eraldamine, täiendustöö ja nõudlustöö loomine). Seega saavad laotöötajad töödelda ainult väljamineva müügi- ja üleviimistellimuse tööd, kasutades Warehouse Management mobiilirakendust, mis on ühendatud juurutuse abil, käitades konkreetse astala ühiku töökoormust.

Kohe, kui lõplik tööprotsess asetab varud lähetuse lõppsihtkohta (Baydoor), annab kaaluühik keskusele signaali lähtedokumendi laokannete uuendamiseks olekusse *Komplekteeritud*. Kuni see protsess käivitub ja saab sünkroonitud tagasi, reserveeritakse vaba kaubavaru kaaluühiku töökoormusel füüsiliselt lao tasemel ja te saate kohe töödelda väljamineva saadetise kinnituse ilma sünkroonimist lõpule viimata. Järgnevad koorma müügi saatelehe ja arve või üleviimistellimuse saadetised käsitsetakse keskuses.

See diagramm näitab väljaminevat voogu ja näitab, kus üksikud äriprotsessid toimuvad. (Valige selle laiendamiseks diagramm.)

[![Väljaminev protsessi voog.](media/wes_outbound_warehouse_processes-small.png "Väljaminev protsessi voog")](media/wes_outbound_warehouse_processes.png)

### <a name="outbound-processing-with-load-planning"></a>Väljaminevate koormate plaanimine

Kui kasutate koorma planeerimise protsessi, luuakse keskusesse koormad ja saadetised ning andmete omand kantakse kaaluüksustesse *lao vabastamise* protsessi osana, nagu näidatud järgmises joonisel.

![Väljaminevate koormate plaanimine.](./media/wes_outbound_processing_with_load_planning.png "Väljaminevate koormate plaanimine")

### <a name="outbound-processing-without-load-planning"></a>Väljaminev protsess ilma koormate plaanimiseta

Kui te ei kasuta koorma planeerimise protsessi, luuakse saadetised kaaluühikutes. Koormad luuakse ka skaalaüksustel laineprotsessi osana.

![Väljaminev protsess ilma koormate plaanimiseta.](./media/wes_outbound_processing_without_load_planning.png "Väljaminev protsess ilma koormate plaanimiseta")

## <a name="inbound-process-flow"></a>Sissetuleva protsessi voog

Keskusel on järgmised andmed:

- Kõik alusdokumendid nagu näiteks müügitellimused ja tootmistellimused
- Sissetuleva koormuse töötlus
- Kõik kulude ja finantsvärskendused

> [!NOTE]
> Sissetuleva ostutellimuse voog erineb kontseptuaalselt väljaminevast voost. Võite kasutada sama ladu kas skaleerimisüksuse või keskusega, sõltuvalt sellest, kas ostutellimus on lattu väljastatud või mitte. Peale seda, kui olete tellimuse lattu väljastanud, saate selle tellimusega töötada ainult siis, kui olete skaalaüksusesse sisse logitud.
>
> Kui kasutate protsessi *Lattu väljastamine*, luuakse [*laotellimused*](cloud-edge-warehouse-order.md) ja seotud vastuvõtva voo omand määratakse skaalaüksusele. Keskus ei saa sissetulevat vastuvõttu registreerida.

Protsessi *Lattu väljastamine* kasutamiseks peate keskusesse sisse logima. Ostutellimuste töötlemiseks minge selle käivitamiseks või ajastamiseks ühele järgmistest lehtedest:

- **Hanked > Ostutellimused > Kõik ostutellimused > Ladu > Tegevused > Lattu väljastamine**
- **Laohaldus > Lattu väljastamine > Müügitellimuste automaatne väljastamine**

Kui kasutate **ostutellimuste automaatset väljastamist**, siis saate päringu põhjal valida konkreetsed ostutellimuse read. Tavaline stsenaarium oleks häälestada korduv pakett-töö, millega väljastatakse kõik kinnitatud ostutellimuse read, mis saabuvad järgmisel päeval.

Töötaja saab töödelda vastuvõtuprotsessi kasutades mobiilirakendust Warehouse Management, mis on ühendatud skaalaühikule. Seejärel salvestatakse andmed skaalajaotisena ja esitatakse sissetuleva lao tellimuse suhtes. Järgnevate eeltöö loomist ja töötlemist käsitleb ka skaalajaotise üksus.

Kui te ei kasuta *väljalaset lattu* ja seetõttu ei kasuta *laotellimusi*, saab keskus töödelda lao sissetulekut ja töötöötlemist sõltumatult skaala ühikutest.

![Sissetuleva protsessi voog.](./media/wes-inbound-ga.png "Sissetuleva protsessi voog")

Kui töötaja teeb sissetuleva registreerimise, kasutades Warehouse Management mobiilirakenduse vastuvõtuprotsessi skaalaühiku suhtes, registreeritakse kviitung seotud laotellimuse kohta, mis salvestatakse skaalaühikule. Kaaluühiku töökoormus annab seejärel keskusele signaali seotud ostutellimuse rea kannete *registreerimiseks*. Niipea kui see on lõpetatud, saate käivitada keskuses ostutellimuse toote vastuvõtmise.

See diagramm näitab sissetulevat voogu ja näitab, kus üksikud äriprotsessid toimuvad. (Valige selle laiendamiseks diagramm.)

[![Väljamineva protsessi voog](media/wes_inbound_warehouse_processes-small.png "Väljamineva protsessi voog")](media/wes_inbound_warehouse_processes.png)

## <a name="supported-processes-and-roles"></a>Toetatud protsessid ja rollid

Mitte kõiki laohalduse protsesse ei toetata skaalaüksuse lao täitmise töömahus. Seetõttu soovitame määrata rollid, mis vastavad igale kasutajale saadaolevatele funktsioonidele.

Selle protsessi hõlbustamiseks on demoandmetesse **Süsteemi administreerimine \> Turvalisus \> Turvalisuse konfiguratsioon** kaasatud näiteroll nimega *Laohaldaja töömahus* . Selle rolli eesmärk on võimaldada laohaldajale juurdepääsu laohalduse elluviimise töökoormuse skaalaühikule. Roll annab juurdepääsu lehekülgedele, mis on asjakohased skaala üksuses majutatud töökoormuse kontekstis.

Kasutajate rollid skaalaühikul määratakse esialgse andmete sünkroniseerimise osana keskusest kuni skaalaühikuni.

Kasutajale määratud rollide muutmiseks avage **Süsteemihaldus \> Turvalisus \> Määra rollidele kasutajad**. Kasutajatele, kes toimivad laohaldajatena ainult skaala ühikutel, tuleb määrata ainult *Laohaldur töömahu* rolli. Selline lähenemine tagab, et nendel kasutajatel on juurdepääs ainult toetatud funktsioonidele. Eemaldage kõik teised neile kasutajatele määratud rollid.

Kasutajatele, kes toimivad laohaldajatena nii keskuses kui skaala üksustes peab olema määratud olemasolev *Laotöötajar* roll. Pange tähele, et see roll annab laotöötajatele juurdepääsu funktsioonidele (nt üleviimistellimuse vastuvõtmise töötlemine), mis kuvatakse kasutajaliideses (UI), kuid mida ei toetata praegu skaala ühikutes.

### <a name="supported-warehouse-execution-processes"></a>Toetatud lao käivitamisprotsessid

Järgmised laohalduse elluviimise protsessid saab lubada laohalduse elluviimise töökoormuse skaala ühikus:

- Valitud laineviisid müügi- ja ülekandetellimuste jaoks (valideerimine, koormuse loomine, jaotamine, nõudluse täiendamine, konteinerite paigutamine, töö loomine ja lainesiltide printimine)

- Laorakenduse abil müügi- ja üleviimistellimuse laotöö töötlemine (sh täiendustöö)
- Vaba kaubavaru päring warehouse'i rakenduse abil
- Varude liikumiste loomine ja teostamine laorakenduse abil
- Tsüklilise inventuuri töö loomine ja töötlemine, kasutades laorakendust
- Kaubavaru kohanduste tegemine warehouse'i rakenduse abil
- Ostutellimiste registreerimine ja ladustamistööde tegemine laorakenduse abil

Skaalaühikule saab luua järgmisi töötüüpe ja tänu sellele saab neid laohalduse töökoormusese osana töödelda:

- **Laovaru liikumised** - käsitsi teisaldamine ja liikumine töö malli alusel.
- **Tsükliline inventuur** - sealhulgas kinnitamise/tagasilükkamise protsess inventuuritoimingute osana.
- **Ostutellimused** - laotellimuse kaudu tehtud ladustamistöö, kui ostutellimused pole koormatega seostatud.
- **Müügitellimused** - Lihtne komplekteerimis- ja laadimistöö.
- **Edastamise probleem** – lihtne komplekteerimine ja laadimine.
- **Täiendamine** - Ei hõlma tootmiseks kasutatavaid toormaterjale.
- **Lõpetatud kaupade ära panemine** – pärast lõpetatuna kinnitatud tootmisprotsessi.
- **Kaastoote ja kõrvaltoote ära panek** – pärast lõpetatuna kinnitatud tootmisprotsessi.

Skaalaüksustes ei toetata ühtegi teist tüüpi lähtedokumentide töötlemist ega laotööd. Näiteks laohalduse elluviimise töökoormus skaalaüksuses puhul ei saa te teha üleviimistellimuse vastuvõtmise protsessi töötlemist (üleviimise vastuvõtmine), selle asemel tuleb seda töödelda keskuse instantsis.

> [!NOTE]
> Toetuseta funktsioonide mobiilse seadme menüüelemente ega nuppe ei näidata _mobiilirakenduses Warehouse Management_, kui see on skaalaüksuse juurutusega ühendatud.
> 
> Kui käitate skaalaüksuses töömahu, ei saa te käitada mittetoetavaid protsesse kindla lao jaoks keskuses. Selles teemas hiljem toodud tabelid dokumenteerivad toetatud võimalusi.
>
> Valitud lao töötüüpe saab luua nii keskuses kui ka skaalaüksuses, kuid seda saab säilitada ainult omanikust keskus või skaalaüksus (andmed loonud juurutus).
>
> Isegi kui skaalaühik toetab kindlat protsessi, arvestage sellega, et kõiki vajalikke andmeid ei pruugita keskusest skaalaühikusse või skaalaühikust keskusesse sünkroonida, mis võib tuua kaasa ootamatu süsteemitöötluse. Selle stsenaariumi näidete hulgas on:
> 
> - Kui kasutate asukohakorralduse päringut, mis ühendab andmetabeli kirje, mis on olemas ainult keskuse juurutamisel.
> - Kui kasutate asukoha oleku ja/või asukoha mahulise koormuse funktsioone. Neid andmeid ei sünkroonita juurutuste vahel ja seega töötavad ainult asukoha vaba kaubavaru värskendamisel ühes juurutuses.

Järgmised laohalduse funktsioonid ei ole praegu skaalaühiku töökoormustes toetatud.

- Koormusele määratud ostutellimuse ridade sissetulev töötlemine.
- Projekti ostutellimuste sissetulev töötlemine.
- Maandumiskulude haldamine, reiside kasutamine ja transiitkauba jälgimine.
- Sissetuleva ja väljamineva töötlemise kaubad, millel on aktiivsed liikumise dimensioonid **Omanik** ja/või **Seerianumber**.
- Blokeeritud oleku väärtusega varude töötlemine.
- Varuda oleku muutmine mis tahes töö liikumisprotsessi ajal.
- Tellimusega seotud paindlikud laotaseme mõõtmete reserveeringud.
- Funktsiooni *Lao asukoha olek* kasutus (andmeid juurutuste vahel ei sünkroonita).
- Funktsiooni *Asukoha litsentsiplaadi paigutus* kasutamine.
- Suvandite *Tootefiltrid* ja *Tootefiltrite rühmad* kasutus, sh säte **Päevade arv partiide segamiseks**.
- Integratsioon kvaliteedijuhtimisega.
- Toodete tegeliku kaaluga töötlemine.
- Töötlemine üksustega, mis on lubatud ainult transpordihalduse (TMS) jaoks.
- Negatiivse vaba kaubainventuuriga töötlemine.
- Laotöö töötlemine saadetise märkustega.
- Laotöö töötlemine koos materjali töötlemisega/warehouse automation.
- Toote põhiandmete pildid (näiteks mobiilirakenduses Warehouse Management).
- Kontsernisisene tooteandmete ühiskasutus.

> [!WARNING]
> Mõned laofunktsioonid ei ole saadaval ladude puhul, mis käitavad laohalduse töökoormusi skaalaüksuses, ning samuti ei toetata seda keskuse või skaalaüksuse töökoormusega.
> 
> Teisi võimalusi saab töödelda mõlemas, kuid nõuab teatud stsenaariumites hoolikat kasutamist, nt kui vaba kaubavaru värskendatakse asünkroonse andmevärskendusprotsessi tõttu samas laos nii keskuse kui ka skaalaüksuse puhul.
> 
> Kindlaid funktsioone (nagu näiteks *töö blokeerimine*), mida toetatakse nii keskuses kui ka skaalaüksuses, toetatakse ainult andmete omaniku jaoks.

### <a name="outbound-supported-only-for-sales-and-transfer-orders"></a>Väljaminev (toetatud ainult müügi- ja üleviimistellimuste puhul)

Järgmine tabel näitab, milliseid väljaminevaid funktsioone toetatakse ja kus neid toetatakse, kui laohalduse töömahtusid kasutatakse pilve ja perimeeterskaala üksustes.

| Töötle                                                      | Keskus | Lao täitmise töökoormus skaala ühikutes |
|--------------------------------------------------------------|-----|------------------------------|
| Lähtedokumendi töötlemine                                   | Jah | Ei |
| Laadimise ja transpordijuhtimise töötlemine                | Jah, kuid ainult koorma planeerimise protsessid. Transpordihalduse töötlemist ei toetata  | Ei |
| Lattu väljastamine                                         | Jah | Ei |
| Plaanitud ristlaadimine                                        | Ei  | Ei |
| Saadetise konsolideerimine                                       | Jah, koorma planeerimisel | Jah |
| Saatmisvoo töötlemine                                     | Ei  |Jah, välja arvatud **koorma ülesehitamine ja sortimine** |
| Voo saadetiste hooldamine                                  | Ei  | Jah|
| Laotöö töötlemine (sh litsentsiplaadi printimine)        | Ei  | Jah, kuid ainult ülalnimetatud toetatud võimaluste puhul |
| Kogumi komplekteerimine                                              | Ei  | Jah|
| Käsitsi pakkimise töötlemine, sh pakitud konteinerite komplekteerimise töö töötlemine | Ei <P>Teatud töötlust saab teha pärast algset komplekteerimisprotsessi, mida käsitseb skaalaüksus, kuid pole soovitatav järgmiste blokeeritud toimingute tõttu.</p>  | Ei |
| Eemalda konteiner grupist                                  | Ei  | Ei |
| Väljamineva sortimise töötlemine                                  | Ei  | Ei |
| Koormaga seotud dokumentide printimine                           | Jah | Jah|
| Konossemendi ja ASN-i loomine                            | Ei  | Jah|
| Saadetise kinnitus                                             | Ei  | Jah|
| Saadetise kinnitamine valikuga „Kinnita ja edasta”            | Ei  | Jah|
| Saatelehe ja arve töötlemine                        | Jah | Ei |
| Kiire komplekteerimine (müügi- ja üleviimistellimused)                    | Ei  | Jah, lähtedokumentide reserveeringuid eemaldamata|
| Ümberkomplekteerimine (müügi- ja üleviimistellimused)                     | Ei  | Jah|
| Tööasukohtade muutmine (müügi- ja üleviimistellimused)         | Ei  | Jah|
| Töö lõpetamine (müügi- ja üleviimistellimused)                    | Ei  | Jah|
| Tööaruande printimine                                            | Jah | Jah|
| Voo silt                                                   | Ei  | Jah|
| Töö tükeldamine                                                   | Ei  | Jah|
| Töö töötlemine – suunaja: transpordi laadimine            | Ei  | Ei |
| Vähenda komplekteeritavat kogust                                       | Ei  | Jah|
| Tühista töö                                                 | Ei  | Jah|
| Saadetise kinnitamise ümberpööramine                                | Ei  | Jah|

### <a name="inbound"></a>Sissetulev

Järgnev tabel näitab, milliseid sissetulevaid funktsioone toetatakse ja kus neid toetatakse, kui laohalduse töömahtusid kasutatakse pilve ja perimeeterskaala üksustes.

| Töötle                                                          | Keskus | Lao täitmise töökoormus skaala ühikutes<BR>*(Valikuga „Jah” märgitud üksused rakenduvad ainult laotellimustele)* |
|------------------------------------------------------------------|-----|----------------------------------------------------------------------------------|
| Lähte&nbsp;dokumendi&nbsp;töötlemine                             | Jah | Ei |
| Laadimise ja transpordijuhtimise töötlemine                    | Jah | Ei |
| Maandumiskulu ja transiitkauba vastuvõtmine                       | Jah | Ei |
| Sissetuleva saadetise kinnitus                                    | Jah | Ei |
| Ostutellimuse vabastamine lattu (lao tellimuse töötlemine) | Jah | Ei |
| Laotellimuse ridade tühistamine<p>Pange tähele, et seda toetatakse ainult siis, kui reaga pole toimingu tühistamise taotluse töötlemise ajal *toimunud ühtegi* registreerimist.</p> | Jah | Ei |
| Vastuvõttev ostutellimuse üksus ja kõrvaleseadmine                       | <p>Jah,&nbsp;kui &nbsp;sinna&nbsp;lao tellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | <p>Jah, kui ostutellimus pole <i>koormuse</i> osa</p> |
| Vastuvõttev ostutellimuse rida ja kõrvaleseadmine                       | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | <p>Jah, kui ostutellimus pole <i>koormuse</i> osa</p></p> |
| Tagastustellimuse vastuvõtt ja kõrvaleseadmine                              | Jah | Ei |
| Kombineeritud litsentsiplaadi vastuvõtt ja kõrvaleseadmine                       | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | Jah |
| Vastuvõetav koormas olev kaup                                              | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | Ei |
| Litsentsiplaadi vastuvõtt ja kõrvaleseadmine                             | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | Ei |
| Vastuvõttev edastustellimuse üksus ja kõrvaleseadmine                       | Jah | Ei |
| Vastuvõetava ja kõrvaleseatava tellimuserea ülekanne                       | Jah | Ei |
| Töö tühistamine (sissetulev)                                            | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | <p>Jah, kuid ainult siis, kui valik <b>Tühista registreerimine töö tühistamisel</b> (lehel <b>Laohalduse parameetrid</b>) on tühistatud</p> |
| Ostutellimuse toote tšeki töötlemine                        | Jah | Ei |
| Ostutellimuse vastuvõtmine alatarnega                      | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | Jah, kuid ainult keskusest tühistamistaotluse tegemisega |
| Ostutellimuse vastuvõtmine ületarnega                       | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | Jah  |
| Vastuvõtmine koos töö *Ristlaadimine* loomisega                 | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | Ei |
| Vastuvõtmine koos töö *Kvaliteettellimus* loomisega                  | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | Ei |
| Vastuvõtmine koos töö *Kauba kvaliteedivalim* loomisega          | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | Ei |
| Vastuvõtmine koos töö *Kvaliteet kvaliteedikontrollis* loomisega       | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | Ei |
| Vastuvõtmine koos kvaliteettellimuse loomisega                            | <p>Jah, kui laotellimust pole</p><p>Ei, kui on olemas lao tellimus</p> | Ei |
| Töö töötlemine – suunaja: *Kogumi kõrvalepanek*                 | Jah | Ei |
| Töö töötlemine koos *kiire komplekteerimisega*                               | Jah | Jah |
| Litsentsiplaadi laadimine                                           | Jah | Jah |

### <a name="warehouse-operations-and-exception-handing"></a>Lao toimingud ja erandi üleandmine

Järgnev tabel näitab, milliseid lao toiminguid ja erandi üleandmise funktsioone toetatakse ja kus neid toetatakse, kui laohalduse töömahtusid kasutatakse pilve ja perimeeterskaala üksustes.

| Töötle                                            | Keskus | Lao täitmise töökoormus skaala ühikutes |
|----------------------------------------------------|-----|------------------------------|
| Numbrimärgi päring                              | Jah | Jah                          |
| Kauba päring                                       | Jah | Jah                          |
| Asukoha päring                                   | Jah | Jah                          |
| Vaheta ladu                                   | Jah | Jah                          |
| Liikumine                                           | Jah | Jah                          |
| Teisaldus malli alusel                               | Jah | Jah                          |
| Edastus laos                                 | Jah | Ei                           |
| Üleviimistellimuse loomine laorakenduses           | Jah | Ei                           |
| Korrigeerimine (sisse/välja)                                | Jah | Jah, kuid mitte kohandamisstsenaariumi korral, kus varude reserveerimine tuleb eemaldada, kasutades inventari korrigeerimistüüpide sätet **Varude eemaldamine**</p>                           |
| Varude oleku muutmine                            | Jah | Ei                           |
| Tsüklilise inventuuri ja inventuuri lahknevuse töötlemine | Jah | Jah                           |
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

Järgmine tabel võtab kokku, milliseid laohalduse tootmistsenaariume praegu skaalaühiku töökoormuse korral toetatakse.

| Töötle | Keskus | Lao täitmise töökoormus skaala ühikutes |
|---------|-----|------------------------------|
| Teata lõpetamisest ja kaupade kõrvale panemisest | Jah | Jah |
| Kaastoodete ja kõrvalsaaduste kõrvalepanek | Jah | Jah |
| Käivita tootmistellimus | Jah | Jah |
| <p>Kõik muud laohalduse protsessid, mis on seotud tootmisega, kaasa arvatud:</p><li>Lattu väljastamine</li><li>Tootmisvoo töötlemine</li><li>Toormaterjalide komplekteerimine</li><li>Kanbani kõrvalepanek</li><li>Kanbani komplekteerimine</li><li>Tootmise praak</li><li>Tootmise viimane kaubaalus</li><li>Materjali tarbimise registreerimine</li><li>Tühi kanban</li></ul> | Jah | Ei |
| Toormaterjali täiendamine | Ei | Ei |

## <a name="maintaining-scale-units-for-warehouse-execution"></a>Skaalaühikute säilitamine lao täitmiseks

Mitu partii-tööd töötavad nii keskuses kui ka skaalaüksustes.

Keskuse juurutamisel saate pakett-töid käsitsi hallata. Saate järgmisi pakett-töösid hallata suvandis **Laohaldus \> Perioodilised ülesanded \> Tagatoa töökoormuse haldamine**:

- Skaalaüksus keskusesse sõnumiprotsessor
- Lähtetellimuse sissetulekute registreerimine
- Lõpeta laotellimused

Skaalaüksustes saate töökoormuse korral hallata järgmisi pakett-töösid suvandis **Laohaldus \> Perioodilised ülesanded \> Töökoormuse haldamine**.

- Vootabeli kirjete töötlemine
- Lao keskusest skaalaüksusesse sõnumiprotsessor
- Laotellimuse ridade töötlemise koguse värskendustaotlused

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
