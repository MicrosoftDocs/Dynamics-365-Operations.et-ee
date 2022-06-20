---
title: Arveldusgraafikute loomine
description: See artikkel selgitab, kuidas arveldusgraafikuid luua, kustutada ja redigeerida.
author: JodiChristiansen
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 1248799f92dc6cbce8528a53cc8a3012d2a67b3c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903388"
---
# <a name="create-billing-schedules"></a>Arveldusgraafikute loomine

[!include [banner](../includes/banner.md)]

Arveldusgraafiku **lehel** saate arveldusgraafikuid luua, kustutada või redigeerida. Saate ka vaadata arveldusgraafikute loendit. Kui loote arveldusgraafiku, määravad sellega seotud arveldusgrupi vaikeväärtused. Lisateave on häälestatud korduva lepingu **arveldusparameetrite lehel**.

## <a name="create-a-billing-schedule"></a>Arveldusgraafiku loomine

Arveldusgraafiku loomiseks järgige neid samme.

1. Valige arveldusgraafiku **lehel** Uus **·**.
2. **Dialoogiboksis Arveldusgraafiku** loomine väljal Arveldusgraafiku **grupp** valige arveldusgraafiku grupp.
3. **Valige kliendi** konto väljal Kliendi konto.
4. **Valige väljal Alguskuupäev** alguskuupäev ja sisestage seejärel **väljale** Perioodide arv perioodide arv. Välja **Lõppkuupäev** uuendatakse teie perioodide arvu põhjal. Kui värskendate arvelduse **lõppkuupäeva** välja, uuendatakse **perioodide** arv väärtusele **0** (null).
5. Valige nupp **OK**.
6. **Sisestage arveldusgraafiku** **kirjeldus** arveldusgraafiku **lehekülje** vahekaardi Üldine väljale Kirjeldus.
7. Valige vahe-eesmärgi **malli** väljal vahe-eesmärgi mall vahe-eesmärgi **arvelduse jaoks**.

Väljad, **nagu Arve** konto **ja Valuutakood**, uuendatakse klienditeabega.

Arveldussageduse **ja** **arveldusintervalli** väljad seatakse valitud arveldusgraafiku grupi põhjal automaatselt.

8. Eraldi arvete loomiseks määrake suvandi **Arve eraldi väärtuseks** **Jah**.
9. Arveldusgraafiku automaatseks uuendamiseks pärast **viimast arveldusperioodi määrake suvandi Värskenda** **automaatselt väärtuseks Jah** ja **seejärel määrake välja Uuendamis kohta lisamiseks read**.

Parameetrite **väljad** seadistatakse automaatselt, võttes aluseks korduva lepingu arveldusparameetrite **lehe** väärtused.

10. Arveldusgraafiku summa prorate selleks määrake suvandi **Osaliste perioodide periood väärtuseks** **Jah**.
11. Arveldusgraafiku üksikasjaridade joondamine kuu lõpuga **seadke suvandi Kuu järgi joondamine** suvandiks **Jah**.
12. Sisestage **lepingu alguskuupäev ja** **lepingu lõppkuupäev** väljadele lepingu algus- ja lõppkuupäev. Need kuupäevad on ainult teabeks.

Makse **väljal** kuvatakse kliendi makseteave kliendilt. Kui rea kaup on ootel või lõpetatud, ei saa makseteavet muuta.

> [!NOTE]
> Kui konsolideerite arveid kauba alusel, peavad maksetingimuste **,** **meetodi ja** arveldusgraafiku väljad **ühtima**. Vastasel juhul ei saa arveid konsolideerida.

13. Vahekaardil Aadress **saate** vaadata üle ja värskendada välju **Tarneaadress ja** **Maksja** aadress.
14. **Vahekaardil Kontaktteave** saate seostada lõppkasutaja konto arveldusgraafikuga.
15. Kontaktiteabe **väljadele** saate sisestada kontakti, meiliaadressi ja interneti-aadressi.
16. Partneri komisjonitasu teabe jälgimiseks seadistage partneri **konto ja** partneri komisjonitasu **määra väljad**. Need väljad on ainult teabeks.
17. **Vahekaardil Kokku** saate vaadata erinevaid arveldusgraafiku jaoks arvutatud kogusummasid.
18. Vahekaardil Ootel **saate** vaadata auditi teavet selle kohta, millal arveldusgraafik ootele pannakse, kui ootel oli eemaldatud.
19. Vahekaardil Lõpetamine **saate** vaadata lõpetamise ajalugu, mis arveldusgraafikule rakendati või sellest eemaldati.
20. Valige käsk **Salvesta**.
21. Valige arveldusgraafiku **ridade** kiirkaardil suvand **Lisa rida**.
22. **Valige kaubakood** väljal Kaubakood. Kui lisakaubaks on tulu tükeldatud emaüksus, uuendatakse read automaatselt tütarüksustega. Tulu tükeldades saate redigeerida ainult emaüksust. Seejärel uuendatakse kõik tütarüksused vastavalt.
23. **Valige väljal Kauba** tüüp kauba tüüp.
24. Uuendage algus- ja lõppkuupäevi.
25. Enne arvete loomist saate arveldussagedust muuta, uuendades arveldussageduse **välja**. Pärast arveldusgraafiku esimese arve loomist ei saa arveldussagedust muuta.
26. **Valige kaubale** mõõtühik väljal Ühik.
27. **Väljal Hinnakujundusmeetod** valige kaubale hinnakujundusmeetod.

Väli **Ühiku hind** seatakse automaatselt laost. Kuid te saate seda uuendada, kui muudate hinnakujundusmeetodiks **Lame**.

## <a name="remove-a-line-item"></a>Rea kauba eemaldamine

Kauba eemaldamiseks arveldusgraafikust järgige neid samme.

1. **Valige redigeeritav** arveldusgraafiku **number arveldusgraafiku** leheküljelt väljal Graafiku number.
2. Valige arveldusgraafiku **ridade** kiirkaardil kustutamisrida ja seejärel valige käsk **Eemalda**.
3. Valige käsk **Salvesta**.

Ülejäänud selles artiklis kirjeldatakse tegevusi ja üksikasju, mis on saadaval arveldusgraafiku **ridade kiirkaardi** ridadel.

## <a name="billing-schedule-line-actions"></a>Arveldusgraafiku rea tegevused

Arveldusgraafiku ridade kiirkaardi **nupud** lasevad teil rakendada tegevusi üksikutele ridadele.

| Nupp | Kirjeldus |
|--------|-------------|
| Lisa rida | Lisage arveldusgraafikule rida. |
| Kaupade loendist lisamine | Lisage arveldusgraafikusse mitu üksust, valides need loendist. |
| Eemaldage | <p>Eemaldage valitud rida arveldusgraafikust.</p><p>Kaupade puhul, mis on tulude tükeldamise osa, saate eemaldada ainult emakauba. Kõik seostatud tütarüksused eemaldatakse seejärel automaatselt.</p> |
| Vaadake arveldusandmeid | Vaadake arvelduse üksikasju. |
| Lõpeta | <p>Lõpetage valitud read. See nupp on saadaval ainult siis, kui valitud ridade olek on **Aktiivne**.</p><p>Kaupade puhul, mis on tulude tükeldamise osa, saate lõpetada ainult peamise kauba.</p> |
| Lõpetamise eemaldamine | <p>Saate valitud ridadelt lepingu lõpetamise eemaldada. See nupp on saadaval ainult siis, kui valitud ridade olek on **Lõpetatud**.</p><p>Kaupade puhul, mis on tulude tükeldamise osa, saate lõpetamise eemaldada ainult põhikaubalt.</p> |
| Koha kinnipidamine | <p>Valige valitud rea ootele panemiseks soovitud üksikasjad.</p><p>Kaupade puhul, mis on tulude tükeldamise osa, saate panna ootele ainult emakauba.</p> |
| Ooteloleku eemaldamine | <p>Eemaldage ootel olemine valitud realt.</p><p>Kaupade puhul, mis on tulude tükeldamise osa, saate ooteloleva ainult peakaubalt eemaldada.</p> |
| Eskaleerimine ja allahindlus | See nupp ei ole saadaval kaupade puhul, mis on tulude tükeldamise osa, v.a emaüksused, kus tulu tükeldamine kasutab **eraldamise meetodit** Nullsumma. |
| Edasilükkamised | <p>Saate sisestada valitud rea viitvõlavalikud.</p><p>Tulu tükeldamisel ei ole see nupp saadaval emaüksuste puhul.</p> |
| Vahe-etapi eraldamine | <p>Vaadake üle ja uuendage valitud rea vahe-eesmärgi eraldusteavet.</p><p>See nupp on saadaval ainult siis, kui arveldusgraafiku rea kaup on vahe-eesmärgi kaup.</p> |
| Tugi ja uuendamine | <p>Vaadake üle ja uuendage valitud rea toe- ja uuendamisteavet.</p><p>See nupp on saadaval ainult siis, kui arveldusgraafiku rea kaup on toe või uuendamisüksus.</p> |
| Dimensioonide kuvamine | Näidake või peitke dimensiooniveerud, mis kuvatakse arveldusgraafiku **ridade ruudustikus**. |
| Arvutage ühiku hind | <p>Arvutage kauba ühiku hind nii, et klient saaks maksta lepingu summa osamaksetena (nt iga päev, kuu, kvartal, poolaasta või iga-aastane). Saate valida lepingu hinna ja hinnasageduse.</p><p>Saate vaadata muudatuste kontrolljälge: vana lepingu hind ja sagedus, uus lepingu hind ja sagedus, muudatuse teinud kasutaja ning muudatuse kuupäev ja kellaaeg.</p> |
| Joondamise kuupäev | <p>Määrake kaupade uuendamise joonduse kuupäev.</p><p>Kui valite kaubagrupi väljal **Kaubagrupp**, kasutavad kõik kaubad arveldusgraafikus kaubagrupi esimese kauba joonduskuupäeva. Kui väli **Kaubagrupp** on tühi, saate kõigi kaupade jaoks määrata joonduse kuupäeva.</p><p>See nupp on saadaval ainult siis, kui arveldussageduse **välja** väärtuseks on seatud Iga-aastane **·**.</p> |
| Arveldamata tulu | <p>Seadke kaup kasutama kuluga stamata tulu funktsiooni. Seejärel saate määrata kaubale segmentimata tulu ja skonto kontod.</p><p>See nupp on saadaval ainult nende kaupade puhul, mille puhul **on välja Kauba** tüüp väärtuseks seatud **Standardne**. See ei ole saadaval olemasolevate arveldusgraafikute ega arveldusgraafiku ridade jaoks, kus arve on juba loodud.</p> |
| Tulujaotuse alamversiooni lisamine | <p>Valige tütarkaup müügitellimusele lisamiseks.</p><p>See nupp on saadaval ainult tulu tükeldatud emaüksuste puhul.</p> |
| Täpsema hinnakujunduse valikud | Redigeerige kauba hinnavalikuid. |

## <a name="billing-schedule-line-details"></a>Arveldusgraafiku rea üksikasjad

Kui valite rea arveldusgraafiku **ridade kiirkaardil**, saate vaadata selle rea üksikasju. Need üksikasjad on jagatud erinevate vahekaartide vahel.

### <a name="general-tab"></a>Vahekaart Üldine

Järgmine teave on saadaval vahekaardil **Üldine**.

| Väli või sektsioon | Kirjeldus |
|------------------|-------------|
| Kasutus | <p>Sellest jaotisest leiate teavet kaupade kasutamise kohta. See sisaldab järgmisi välju:</p><ul><li>**Kasutus** IDENTIFIKAATOR – arvesti või kasutuskauba identifikaator.</li><li>**Lugemissuvand** – kasutuslugemise suvand: **lugemine** või **tarbimine**.</li><li>**Eeldatav** tarbimine : määrake kasutuskauba hinnanguline tarbimine, mille perioodidel pole arvet loodud. Arvelduse **üksikasjade lehel** saate vaadata üle hinnangulise tarbimise arvelduse üksikasjaread.</li></ul> |
| Välised viited\* | See jaotis sisaldab välis **- ja** reanumbrite **välju**, kus saate määrata välisviite teabe. |
| Vahe-eesmärk | <p>Sellest jaotisest leiate vahe-eesmärkide kaupade teavet. See sisaldab kauba **lõpetamiskuupäeva** näitav välja Hinnanguline valmimiskuupäev.</li></ul> |
| Tekst | Rea kommentaar. Tekst tõlgitakse kliendi või juriidilise isiku vaikekeeleks. |
| Kaubagrupp | Rea kauba kaubagrupp. |
| Joondamise kuupäev | Arveldusgraafiku joondamise kuupäev. |

\* Kui konsolideerite arved kauba alusel lehel Loo **arve**, peavad välisviite **väljad** ühtima. Kui isegi üks märk erineb, ei konsolideerita kaupu arvel. Kummalgi väljal ei kontrollita **välisviite** **sektsiooni ning välja Rea number** väärtus peab olema positiivne täisarv.

### <a name="address-tab"></a>Vahekaart Aadress

Järgmine teave on saadaval vahekaardil **Aadress**.

| Väli | Kirjeldus |
|-------|-------------|
| Tarneaadress | <p>Valige reaüksuse tarneaadress. Vaikimisi on tarneaadress esmane tarneaadress aadressi **kiirkaardilt**.</p><p>Aadressi muutmisel saate valida järgmiste aadressivalikute vahel:</p><ul><li>**Aadressid** – valige praeguse kliendi aadress.</li><li>**Kasutusel**: valige aadress, mida praegu praeguse kliendi jaoks kasutatakse.</li><li>**Muu aadress** – valige aadress iga kliendikirje jaoks.</li></ul><p>Kaupade puhul, mis kasutavad tulu tükeldamist, saab redigeerida ainult emakauba aadressi. Tütarüksuste aadress vastab emaüksuse aadressile ja seda ei saa eraldi redigeerida.</p> |
| Maksja aadress | <p>Valige reaüksusele maksja aadress. Vaikimisi on tarneaadress esmane tarneaadress aadressi **kiirkaardilt**. Aadressi saate olemasolevate aadresside eesmärgi alusel vastavalt vajadusele muuta.</p><ul><li>Kui ühelgi aadressil puudub **arve eesmärk**, on vaikimisi maksja aadress kliendi esmane aadress, sõltumata eesmärgist.</li><li>Kui ühel või rohkemal aadressil on arve **eesmärk**, on vaikimisi maksja aadress aadress, mis viimati sisestati.</li><li>Kui ühel või **rohkemal** aadressil on arve eesmärk ja üks arve aadressidest on seadistatud esmaseks aadressiks, on maksja vaikeaadress **aadress**, mis on arve eesmärk ja seadistatud esmaseks aadressiks.</li><li>Kaupade puhul, mis kasutavad tulu tükeldamist, saab redigeerida ainult emakauba aadressi. Tütarüksuste aadress vastab emaüksuse aadressile ja seda ei saa eraldi redigeerida.</li></ul> |

### <a name="product-tab"></a>Vahekaart Toode

Järgmine teave on saadaval vahekaardil **Toode**.

| Väli või sektsioon | Kirjeldus |
|------------------|-------------|
| Laodimensioonid | <p>Sellest jaotisest leiate kauba ladustamisteabe. See sisaldab seerianumbri **välja**, mis näitab kauba seerianumbrit.</p><p>See seerianumber kopeeritakse algsest müügitellimusest toe- ja uuendamisprotsessi ajal. Kaupade puhul, mis kasutavad tulu tükeldamist, kopeeritakse emakauba seerianumber kõigile tütarüksustele. Seerianumber kopeeritakse, kui korduva lepingu **arveldusparameetrite** **lehel** on **suvand Kopeeri seerianumber seatud väärtusele** Jah.</li></ul> |
| Tootedimensioonid | Kauba toote üksikasjad ja väärtused uuendatakse automaatselt, **võttes** aluseks arveldusgraafiku rea jaoks valitud variandinumbri väärtuse. |

### <a name="account-tab"></a>Vahekaart Konto

Järgmine teave on saadaval vahekaardil **Konto**.

| Väli | Kirjeldus |
|-------|-------------|
| Põhikonto | Müügireal loodud põhikonto. Vaikeväärtus tuleb müügitellimuselt. Välja võib tühjaks jätta. |
| Kauba finantsdimensioonid | <p>Vaikimisi finantsdimensiooni väärtused, mis põhinevad kliendi ja kauba kirjel.</p><p>Kaupade puhul, mis kasutavad tulu tükeldamist, kasutavad tütarüksused kliendi ja kauba kirjete finantsdimensiooni väärtusi, nagu varem kirjeldatud. Kui peate alamüksuste finantsdimensiooni väärtuseid uuendama, saate andmeüksuse importida.</p> |

### <a name="renewals-tab"></a>Vahekaart Uuendused

Järgmine teave on saadaval vahekaardil **Uuendamised**.

| Väli | Kirjeldus |
|-------|-------------|
| Uuenda automaatselt | <p>Väärtus, mis näitab, kas arveldusgraafiku rida värskendatakse automaatselt järgmisele arveldusperioodile:</p><ul><li>**Jah** – arve loomisel uuendatakse arveldusgraafiku rida järgmise arveldusperioodi jaoks automaatselt.</li><li>**Ei** – arveldusgraafiku rida ei värskendata automaatselt. Peate arveldusgraafikut käsitsi uuendama.</li></ul> |
| Lisatavad read uuenduse kohta | Ridade arv, mida lisada arveldusgraafiku uuendamisele. |

Lisaks on vahekaardil Uuendamised saadaval järgmised **nupud**.

| Nupp | Kirjeldus |
|--------|-------------|
| Arveldamata tulu töölehe sisestuse audit | Vaadake kõiki muudatusi kaupade puhul, mis kasutavad kulumata tulu funktsiooni. |
| Uuendamise tingimuse lisamine | Lisage kaubale uuendamistermin. Uue uuendamistermini alguskuupäev on järgmine kuupäev pärast eelmise perioodi lõppkuupäeva. Väljad **Uuendamise lõppkuupäev**, **Viitvõla alguskuupäev**, **Viitvõla lõppkuupäev**, **Kauba** **kogus** ja Ühiku hind saab värskendada. |
| Uuendamise tähtaja muutmine | <p>Uuendamistermini muutmine. Esialgseks termin võib muuta viitvõla algus- ja lõppkuupäevi enne algse töölehe sisestuse loomist. Järgmiste tingimuste puhul ei saa alguskuupäeva muuta. See on alati järgmine kuupäev pärast eelmise tähtaja lõppu.</p><p>Kui uuendamistermin on olemas pärast muutmist, ei saa selle kuupäeva muuta. Sel juhul saab uuendada **ainult** uuendatava **kauba** välju Kogus ja Ühiku hind.</p><p>Näiteks on olemas kolm terminit. <ul><li>Esimest terminit ei saa muuta, kuna see on juba alanud.</li><li>Teise termini puhul saab muuta ainult kogust ja ühikuhinda.</li><li>Kolmanda termini puhul saab muuta kõiki väärtusi, v.a alguskuupäev. Lisaks võimaldab mallist **plaanimine** luua viitvõlagraafiku, mis põhineb tasumata tulu kauba mallil. Kui see suvand on seatud väärtusele **Jah**, **valige** malliväljal viitvõla mall ja muutke vajaduse järgi viitvõla algus- ja lõppkuupäevi. Järgnevad uuendamistingimused kasutavad sama viitvõlamalli. Kuid viitvõla malli saab muuta.</p></li></ul> |

### <a name="termination-tab"></a>Vahekaart Lõpetamine

Järgnev teave on saadaval vahekaardil **Lõpetamine**.

| Väli | Kirjeldus |
|-------|-------------|
| Lõpetamiskuupäev | Kuupäev, millal arveldusgraafiku rida lõpetatakse. Vaikeväärtus põhineb päise väljal **Lõpetamiskuupäev**. Väärtust saate vajaduse korral muuta. |
| Lõpetamise tüüp | Lõpetamise tüüp. Vaikeväärtus kuvatakse päise väljalt **Lepingu** lõpetamise tüüp. |

### <a name="hold-tab"></a>Vahekaart Ootel

Kui kasutatakse tulu- ja kulu viitvõlgu, **kuvatakse** vahekaardil Ootel viitvõla kuupäev.

### <a name="escalation-and-discount-tab"></a>Vahekaart Laiendus ja allahindlus

Järgmine teave on saadaval vahekaardil Laiendus **ja allahindlus**.

| Väli | Kirjeldus |
|-------|-------------|
| Laiendus | <p>Valige, kas eskalatsioonid on arveldusgraafiku rea puhul lubatud. Mis tahes päise eskalatsioonirida rakendatakse arveldusgraafiku rea loomisel.</p><ul><li>**Jah** – eskalatsioone saab reale rakendada. Kui see suvand on **valitud, saate seadistada laiendused arveldusgraafiku ridade jaoks laienduse ja allahindluse** lehel.</li><li>**Ei** – laiendusi ei saa reale rakendada.</li></ul><p>Vaikesäte põhineb valitud arveldusgraafiku **grupil**.</p> |

### <a name="price-changes-tab"></a>Vahekaart Hinnamuutused

Ridade puhul, mis muudetakse standardsest **hinnast** **lamehinnaks**, sisaldab **vahekaardi Hinnamuutus ruudustik** järgmisi veerge:

- Muuda kuupäeva
- Kasutaja muudetud
- Tavahind
- Kindla hinnaga
- Hinna uuendamine
