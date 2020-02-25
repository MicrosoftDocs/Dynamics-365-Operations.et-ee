---
title: Sobivusreeglite ja -suvandite konfigureerimine
description: Määrake rakenduses Microsoft Dynamics 365 Human Resources soodustuste haldamises sobivusreeglid ja -suvandi.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 448156a2428e99d8b95de547cb6f1621d49b1c7b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008813"
---
# <a name="configure-eligibility-rules-and-options"></a>Sobivusreeglite ja -suvandite konfigureerimine

[!include [banner](includes/preview-feature.md)]

Kui olete rakenduses Microsoft Dynamics 365 Human Resources konfigureerinud soodustuste haldamise vajalikud parameetrid, saate luua sobivusreeglid, kogumid, perioodid ja programmid, mille soodustuse plaanidega seostate.

## <a name="create-an-eligibility-rule"></a>Sobivusreegli loomine

Sobivusreeglid määratlevad, millised töötajaid saavad igas soodustuse plaanis registreeruda. Pärast sobivusreeglite määratlemist määrate need soodustuse plaanidele. Seejärel saate töödelda registreerimise sobivust, et näha, millised töötajad on iga plaani jaoks sobilikud. 

Avatud registreerimise ajal saavad töötajad valida soodustuse plaanid. Kui nad muutuvad soodustuse plaani jaoks sobimatuks sobivusreeglite põhjal pärast seda, kui need on juba registreeritud, ei tühistata nende registreerimist automaatselt. Tavaliselt kui ilmneb elusündmus, mis mõjutab plaani sobivust, käivitatakse töövõtjale registreerimise periood, et valida plaanid, mille jaoks nad on sobivad. 

1. Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Sobivusreeglid ja -suvandid**.

2. Sobivusreegli loomiseks valige vahekaardil **Sobivusreeglid** suvand **Uus**. Sobivusreegliga seostatud plaanide vaatamiseks valige suvand **Lisatud plaanid**.

3. Määrake järgmiste väljade väärtused.

   | Väli | Kirjeldus |
   | --- | --- |
   | **Sobivusreegel** | Sobivusreegli kordumatu identifikaator. |
   | **Kirjeldus** | Sobivusreegli kirjeldus. |
   | **Kehtivuse alguskuupäev ja -aeg** | Sobivusreegli alguskuupäev. | 
   | **Kehtivuse lõppkuupäev ja -aeg** | Sobivusreegli lõpukuupäev. |
   | **Kasutaja töövõtja tüüp** | Määrab, kas kasutada soodustuse sobivusreeglis töövõtja töövõtja tüüpi. |
   | **Töötaja tüüp** | Töötaja tüüp, kui lüliti **Kasuta töövõtja tüüpi** on seatud väärtusele **Jah**. |
   | **Kasuta töövõtja olekut** | Määrab, kas kasutada soodustuse sobivusreeglis töövõtja tööhõiveolekut. |
   | **Olek** | Töövõtja olek, kui lüliti **Kasuta töövõtja olekut** on seatud väärtusele **Jah**. Kui lüliti **Kasuta töövõtja olekut** on seatud väärtusele **Ei**, siis seda välja ei kasutata. |
   | **Kasuta tööhõive kategooriat** | Määrab, kas kasutada osana soodustuse sobivusreeglist töövõtja väärtust **Tööhõive kategooria**. | 
   | **Tööhõive kategooria** | Töövõtja tööhõive kategooria, kui lüliti **Kasuta tööhõive kategooriat** on seatud väärtusele **Jah**. |
   | **Kasuta uue palkamise reeglit** | Määrab, kas kasutada uue töötaja uue palkamise perioodi väärtust soodustuste sobivusreegli osana. |
   | **Registreerimisperiood** | Ajaperiood, mil uue palkamise registreerimine on lubatud. Kui määrate parameetrites ka selle, on parameetrite seadistus kõrgema prioriteediga kui see. |

4. Jaotises **Lisakriteeriumid** valige järgmised suvandid ja lisage vastavalt vajadusele teave.

   | Suvand | Kirjeldus |
   | --- | --- |
   | **Kõlblik vanus** | Määrab sobivusreegli täitmiseks vajaliku vanusevahemiku või -vahemikud. |
   | **Sobilik osakond** | Määrab sobivusreegli täitmiseks vajaliku osakonna või osakonnad, kus töövõtja peab asuma. |
   | **Sobilik töölevõtu tüüp** | Määrab sobivusreegli täitmiseks vajaliku tööhõive tüübi või tüübid, mille alusel töövõtja peab olema kategoriseeritud. Näiteks täistööaeg või osaline tööaeg. |
   | **Sobilik töö** | Määratleb töö või tööd, mis vastavad sobivusreeglile. Tööd on seotud ametikohtadega ja ametikohad on täidetud töövõtjatega. |
   | **Sobilik tööfunktsioon** | Määratleb tööfunktsiooni või -funktsioonid, mis vastavad sobivusreeglile. Näiteks müügitöötajad või tehnikud. |
   | **Sobilik töötüüp** | Määratleb töö tüübi või tüübid, mis vastavad sobivusreeglile. Näiteks kontoritöötaja või juhtivtöötaja. |
   | **Kõlblik juriidiline isik** | Määrab juriidilise isiku või juriidilised isikud, mis kehtivad sobivusreeglile. Näiteks Contoso Entertainment System USA. |
   | **Sobiv hüvituspiirkond** | Määrab töövõtja asukoha, mis vastab sobivusreeglile. Näiteks Kesk-USA. |
   | **Sobilik ametikoht** | Määratleb ametikoha või ametikohad, mis vastavad sobivusreeglile. Näiteks personaliosakonna assistent või personaliosakonna juht. |
   | **Sobilik ametikoha tüüp** | Määratleb ametikoha tüübi või tüübid, mis vastavad sobivusreeglile. Näiteks täistööaeg. |
   | **Soodustuskõlblik olek** | Määratleb osariigid või provintsid, mis vastavad sobivusreeglile. Näiteks Põhja-Dakota (USA) või Briti Columbia (Kanada). |
   | **Sobilikud töölevõtu tingimused** | Määrab töölevõtutingimused, mis vastab sobivusreeglile. Näiteks üksikisiku või rühma leping. |
   | **Kõlblik ametiühing** | Määratleb ametiühingu liikmesused, mis vastavad sobivusreeglile. Näiteks Ameerika kahveltõstukite juhid. </br></br>Ametiühingu põhist sobivusreeglit kasutades peab töötaja ametiühingu kirjes olema lõpukuupäev täidetud. Te ei saa seda tühjaks jätta. |
   | **Sobilik sihtnumber** | Määratleb sihtnumbrid, mis vastavad sobivusreeglile. Näiteks 58104. |

5. Jaotises **Lisateave** saate kuvada järgmisi täiendavaid üksikasju.

   | Väli | Kirjeldus |
   | --- | --- |
   | **Sobilik kasutajaväli** | Määrab kliendi määratletud väljade põhjal täiendavad sobivusreeglid. |
   | **Sobivustüüp** | Määrab kriteeriumi kategooria, mille valisite jaotises **Lisakriteeriumid**. |
   | **Sobivusviide** | Määrab väärtused, mille valisite jaotises **Lisakriteeriumid**. |
   | **Kirjeldus** | Kirjeldus, mille valisite jaotises **Lisakriteeriumid**. |

6. Valige käsk **Salvesta**.

## <a name="configure-bundles"></a>Kogumite konfigureerimine

Kogumid on seotud soodustuste plaanide komplektid. Soodustuste kogumite abil saate rühmitada soodustuste plaane, mille töövõtja peab valima, et registreeruda teatud soodustuste plaanides, mis võivad sõltuda teistest soodustuse plaanide registreerumistest. Näited, millal võite tahta kasutada kogumit, on järgmised.

- Tervisekindlustuse kogum, mis sisaldab kõrge mahaarvamisega ravikindlustust koos seotud tervisesäästukontoga (HSA).

- Elukindlustuse plaan kohustusliku töövõtja elukindlustuse plaaniga, mis on komplekteeritud temast sõltuja eluplaaniga. See tagab, et töövõtja ei saa valida temast sõltuja elukindlustust ilma töövõtja kindlustuse jaoks registreerimiseta.

1. Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Sobivusreeglid ja -suvandid**.

2. Kogumi loomiseks valige vahekaardil **Kogumid** suvand **Uus**. Kogumiga seostatud plaanide vaatamiseks valige suvand **Lisatud plaanid**.

3. Määrake järgmiste väljade väärtused.

   | Väli | Kirjeldus |
   | --- | --- |
   | **Kogum** | Kogumi kordumatu identifikaator. |
   | **Kirjeldus** | Kogumi kirjeldus. |
   | **Põhiveokiri** | Näitab, kas üks kogumi plaanidest peab olema märgitud põhiplaanina. Põhiplaan tuleb valida avatud registreerimisel kogumi osana, enne kui soodustuste haldur saab töövõtja soodustuste valikud kinnitada. |
   | **Kehtivuse alguskuupäev ja -aeg** | Kogumi aktiivseks muutumise kuupäev ja kellaaeg. |
   | **Kehtiv kuni** | Kogumi aegumise kuupäev. Vaikimisi on see 12/31/2154, mis tähistab, et mitte kunagi. |

4. Valige käsk **Salvesta**.

## <a name="configure-periods"></a>Perioodide konfigureerimine

Perioodid määratlevad, millal soodustused on jõus ja millal on töötajatel lubatud registreeruda. Saate luua nii palju perioode kui soovite, et säilitada soodustuste avatud registreerimine ja soodustuse katvuse perioodid. Soodustuse plaani aastad võivad, kuid ei pruugi järgida kalendriaastat. 

1. Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Sobivusreeglid ja -suvandid**.

2. Perioodi loomiseks valige vahekaardil **Perioodid** suvand **Uus**. Protsessi käivitamiseks, mis lisab kõik kehtivad aktiivsed soodustuse plaanid soodustuse perioodile, valige suvand **Lisa plaanid**. Kogumiga seostatud plaanide vaatamiseks valige suvand **Lisatud plaanid**. 

3. Määrake järgmiste väljade väärtused.

   | Väli | Kirjeldus |
   | --- | --- |
   | **Periood** | Perioodi kordumatu identifikaator. |
   | **Kehtivuse alguskuupäev ja -aeg** | Alguskuupäev ja -kellaaeg, mil soodustuste periood on aktiivne. |
   | **Kehtivuse lõppkuupäev ja -aeg** | Kuupäev ja kellaaeg, mil soodustuste periood muutub passiivseks. |
   | **Registreerimise algus** | Avatud registreerimise alguskuupäev. Avatud registreerimine on siis, kui töövõtja iseteeninduse soodustuste seas teha soodustuse valikuid. |
   | **Registreerimise lõpp** | Avatud registreerimise lõpukuupäev. |
   | **Avamine** | Näitab, kas periood on süsteemi kuupäeva põhjal avatud ning kehtiv algus- ja lõpukuupäevadel ja kellaaegadel. | 
   | **Eelmine periood** | Määrab soodustuste perioodi, mis eelneb valitud soodustuste perioodile. Seda teavet kasutatakse soodustuse sobivuse registreerimisel, et määrata plaanid, katvuse valikud ja volitatud isikud eelmisest aastast. |
 
4. Valige käsk **Salvesta**.

## <a name="use-a-flex-credit-program"></a>Paindliku krediidiga programmi kasutamine

Saate kasutada paindliku krediidiga programme, et registreerida töötajad eelmääratud hulgale paindlikule krediidile. Töötajad saavad valida, kuidas oma paindlikku krediiti jaotada. Näiteks kui töötaja on kaetud oma abikaasa ravikindlustusplaaniga, võivad nad soovida kasutada krediiti, mida nad oleks muidu kasutanud tervisekindlustuse jaoks, teisteks soodustusteks.

1. Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Sobivusreeglid ja -suvandid**.

2. Valige vahekaardil **Perioodid** suvand **Paindliku krediidiga programmid**.

3. Valige rakendamiseks paindliku krediidiga programm. Väljad sisaldavad järgmist teavet.

   | Väli | Kirjeldus |
   | --- | --- |
   | Soodustuse krediidi ID | Paindliku krediidiga programmi kordumatu identifikaator. |
   | Kirjeldus | Paindliku krediidiga programm kirjeldus. | 
   | Kehtivuse alguskuupäev | Paindliku krediidiga programmi aktiivseks muutumise kuupäev. |
   | Kuupäevani | Paindliku krediidiga programmi lõpukuupäev. Saate jätta vaikeväärtuse (12/31/2154), mis näitab, et paindliku krediidiga programmil ei ole plaanitud aegumist. |
   | Krediidi koguväärtus | Krediidi hulk, mida iga töövõtja saab nende soodustuste jaoks kasutada. |
   | Proportsionaalse jaotumise reegel | Reeglit kasutatakse paindliku krediidi proportsionaalseks jaotamiseks, kui töövõtja palgatakse paindliku krediidi perioodi keskel. </br></br><ul><li>**Pole** – töövõtja ei saa paindlikku krediiti, kui ta on palgatud pärast paindliku krediidiga programmi perioodi algust.</li><li>**Täiskrediit** – töötaja saab paindliku krediidi koguhulga, olenemata nende palkamise ajast.</li><li>**Jaota proportsionaalselt** – töövõtja saab proportsionaalselt jaotatud hulga paindlikku krediiti, olenevalt nende tööhõive alguskuupäevast.</li></ul> |
   | Paindliku krediidi proportsionaalse jaotamise valem | Reeglit kasutatakse paindliku krediidi proportsionaalseks jaotamiseks töövõtjatele, kes palgatakse paindliku krediidi programmi soodustuste perioodi keskel. Proportsionaalne jaotamine põhineb tööhõive alguskuupäeval. Seda välja kasutatakse ainult siis kui valite suvandi **Jaota proportsionaalselt** väljal **Proportsionaalselt jaotamise reegel**. </br></br><ul><li>**Igapäevane** – jaotab töövõtja saadava paindliku krediidi hulga proportsionaalselt päevade tasemel. Paindliku krediidi koguhulk jagatakse perioodi päevade arvuga. Näiteks kui teie soodustuste periood on 400 päeva, jaotab süsteem paindliku krediidi koguhulga 400-ga, et arvutada paindliku krediidi hulga, mida töötaja päevas saab.</li><li>**Jooksev kuu** – jaotab töövõtja saadava paindliku krediidi hulga proportsionaalselt kuu tasemel, ümardatuna praeguse kuuni. Paindliku krediidi koguhulk jagatakse perioodi kuude arvuga. Näiteks kui teie soodustuste periood on 15 kuud, jaotab süsteem paindliku krediidi koguhulga 15-ga, et arvutada paindliku krediidi hulga, mida töötaja kuus saab.</li><li>**Järgmine kuu** – jaotab töövõtja saadava paindliku krediidi hulga proportsionaalselt kuu tasemel, ümardatuna järgmise kuuni. Paindliku krediidi koguhulk jagatakse perioodi kuude arvuga. Näiteks kui teie soodustuste periood on 15 kuud, jaotab süsteem paindliku krediidi koguhulga 15-ga, et arvutada paindliku krediidi hulga, mida töötaja kuus saab.</li></ul> |
   
   Veenduge, et iga soodustuse plaan oleks igal soodustuse perioodil registreeritud ainult ühes paindliku krediidiga programmis. Vastasel juhul süsteem ei tea, millist paindliku krediidiga programmi kasutada, et paindlikku krediiti anda, ja teil tekib probleeme. 

## <a name="configure-programs"></a>Programmide konfigureerimine

Programmid on soodustuste plaanide komplektid, mis jagavad ühiseid sobivusreegleid. Saate määratleda sobivusreeglid iga üksiku plaani asemel kogu programmile. Näiteks Contoso Kanada FTE programm või Contoso Euroopa juhtimistaseme programm. 

1. Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Sobivusreeglid ja -suvandid**.

2. Programmi loomiseks valige vahekaardil **Programmid** suvand **Uus**. Erandite tegemiseks töötajatele, kes sobivusreegli nõuetele ei vasta, valige suvand **Sobivusreegli tühistamine**. Programmiga seostatud plaanide vaatamiseks valige suvand **Lisatud plaanid**.

3. Määrake järgmiste väljade väärtused.

   | Väli | Kirjeldus |
   | --- | --- |
   | **Programm** | Programmi kordumatu identifikaator. |
   | **Kirjeldus** | Programmi kirjeldus. | 
   | **Kehtivuse alguskuupäev ja -aeg** | Programmi aktiivseks muutumise kuupäev ja kellaaeg. |
   | **Kehtivuse lõppkuupäev ja -aeg** | Programmi aegumise kuupäev ja kellaaeg. Vaikimisi on see 12/31/2154, mis tähistab, et mitte kunagi. |
   | **Kehtivusperioodi ooteaeg** | Aeg, kaua töövõtja peab ootama, enne kui soodustusprogrammi katvus algab. |
   | **Mahaarvamise ooteaeg** | Aeg, kaua töövõtja ootab, enne kui soodusprogrammi mahaarvamised algavad. |
   | **Sobivusreeglid** | Valige soodustusprogrammidele kehtivad sobivusreeglid. Sobivusreeglid määratlete selle lehe vahekaardil **Sobivusreeglid**. |
   
4. Valige käsk **Salvesta**.
