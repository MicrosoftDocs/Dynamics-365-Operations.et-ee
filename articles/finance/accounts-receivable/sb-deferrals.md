---
title: Tulu ja kulu viitvõlad kordustellimuse arvelduses
description: See teema kirjeldab, kuidas seadistada tulu- ja kulu viitvõlgu kordustellimuse arvelduses.
author: JodiChristiansen
ms.date: 11/04/2021
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
ms.openlocfilehash: 9a12cf52d904db0396aa9914b8e324060289710f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690944"
---
# <a name="revenue-and-expense-deferrals-in-subscription-billing"></a>Tulu ja kulu viitvõlad kordustellimuse arvelduses

See teema kirjeldab, kuidas seadistada ja kasutada tulu- ja kulu viitvõlgu kordustellimuse arvelduses. Viitvõlgade graafikud põhinevad alati algdokumendil või arveldusgraafikul ja sõltuvad sellest. Kuna need luuakse vaikeväärtuste põhjal, ei saa neid eraldi sisestada ega luua.

Tulu- ja kulu viitvõlgade seadistamise ja kasutamise protsess toimub mitmel lehel:

- Lehel Tulu **ja kulu viitvõla parameetrid** saate määratleda ettevõtte eelistused.
- **Viitvõla vaikelehel** saate seadistada viitvõlagraafikutes kasutatavad vaikekontod ja mallid.
- Viitvõlamallidel **ja** sündmusepõhistel **viitvõlgade** mallidel saate määratleda viitvõlagraafikutes kasutatavad mallid.
- Lehel Kõik **viitvõlagraafikud saate** vaadata ja redigeerida viitvõlagraafikuid.

Tulu- ja kulu viitvõlgu saab kasutada koos korduva lepingu arveldusega.

## <a name="revenue-and-expense-deferral-parameters"></a>Tulude ja kulude edasilükkamise parameetrid

Leht **Tulu ja kulu viitvõla parameetrid** sisaldab järgmisi välju.

| Väli | Kirjeldus |
|---|---| 
| **Vahekaart** Graafik | |
| Võrdub perioodiga | <p>Saate määrata, kas viitvõlagraafiku puhul kasutatakse perioodi summa arvutamisel päevade arvu:</p><ul><li>**Jah** – iga perioodi summa on sama, olenemata perioodi päevade arvust. Osalised perioodid (nt perioodid viitvõlagraafiku alguses või lõpus) jagatakse perioodide kaupa.</li><li>**Ei** – summa arvutatakse iga perioodi päevade arvu põhjal.</li></ul><p>Selle sätte saate alistada kande tasemel.</p> |
| Müügi allahindluse edasilükkamise valik | <p>Määrake, kas allahindluse ja müügitellimuse summade jaoks luuakse eraldi viitvõlagraafikud:</p><ul><li>**Eraldi allahindluse graafik** – allahindluse summa hoitakse eraldi tulusummast.<p>Sel juhul luuakse müügitellimuse loomisel ja seejärel sisestamisel kaks viitvõlagraafikut. Allahindluse ja tulu summad sisestatakse erinevatele viitvõlakontodele.</p></li><li>**Allahindluse ühendamine tuluga** – allahindluse summa kombineeritakse tulusummaga. Luuakse üks viitvõlagraafik ning allahindluse summa ja tulusumma sisestatakse samale viitvõla kontole.<p>Sel juhul luuakse müügitellimuse loomisel ja seejärel sisestamisel üks viitvõlagraafik. Nii allahindluse kui ka tulu summa sisestatakse samale viitvõlakontole.</p></li></ul><p>**Märkus:** allahindluste rakendamiseks kaupadele, mis kasutavad segmentimata tulu funktsiooni, valige **allahindluse jaoks eraldi graafik**. Seejärel saab allahindlusi rakendada kõigile kaupadele, sõltumata sellest, kas kasutatakse veamata tulu funktsiooni. Kui on **valitud suvand Ühenda allahindlus** tuluga, ei saa allahindlusi rakendada kaupadele, mis kasutavad segmentimata tulu funktsiooni.</p> |
| Ostmise allahindluse edasilükkamise valik | <p>Valige, kas allahindluse ja ostutellimuse summade jaoks luuakse eraldi viitvõlagraafikud:</p><ul><li>**Eraldi allahindluse graafik** – allahindluse summa hoitakse eraldi kulusummast.<p>Sel juhul luuakse ostutellimuse loomisel ja seejärel sisestamisel kaks viitvõlagraafikut. Allahindlused ja kulusummad sisestatakse erinevatele viitvõlakontodele.</p></li><li>**Allahindluse ühendamine tuluga** – allahindluse summa kombineeritakse kulusummaga. Luuakse üks viitvõlagraafik ja allahindluse summa ja kulusumma sisestatakse samale viitvõla kontole.<p>Sel juhul luuakse ostutellimuse loomisel ja seejärel sisestamisel üks viitvõlagraafik. Nii allahindluse summa kui ka kulusumma sisestatakse samale viitvõla kontole.</p></li></ul> |
| Eelnevate perioodide konsolideerimine | <p>Määrake, kas eelmiste perioodide viitvõlagraafiku read on konsolideeritud:</p><ul><li>**Jah** – kui viitvõla alguskuupäev on kande kuupäevale enne kandekuupäeva, ühendatakse kõik kandekuupäeva perioodi jooksul ülessaanud summad ühele viitvõlagraafiku reale.</li><li>**Ei** – kõigi perioodide summad hoitakse eraldi viitvõlagraafiku ridadel.<p>Kui viitvõla alguskuupäev on kande kuupäevaga samas perioodis või sellest hilisem periood, ei oma see valik mõju.</p></li></ul><p>Seda sätet saab kandetasemel uuendada.</p> |
| Vaikimisi edasilükkamise alguskuupäev | <p>Valige reegel, mida kasutatakse viitvõlagraafiku alguskuupäeva määratlemiseks:</p><ul><li>**Kande kuupäev** – kasutage kandekuupäeva alguskuupäevana.</li><li>**Jooksva kuu algus** – kasutage alguskuupäevana praeguse kuu esimest. Kui kandekuupäev on mis tahes kuu esimene, on alguskuupäev praeguse kuu esimene.</li><li>**Järgmise kuu algus** – kasutage alguskuupäevana järgmise kuu esimest. Kui kande kuupäev on esimene, kasutatakse kande kuupäeva. Muul juhul kasutatakse järgmise kuu esimest.</li><li>**Reegel 15** – kui kande kuupäev jääb 15. ja esimese vahele, kasutage alguskuupäevaks käesoleva kuu esimest. Kui kande kuupäev on kuueteistkümnes või hilisem, kasutage alguskuupäevana järgmise kuu esimest.</li></ul><p>Seda sätet saate uuendada kande tasemel.</p> |
| Lühiajalise edasilükkamise meetod | <p>Valige lühiajaline viitvõlameetod: **pole, jooksvad** **perioodid või** fikseeritud **aasta**.</p><p>|
| Edasilükkamise kirjendamise viis | <p>Valige viitvõlakannete loomiseks kasutatav meetod:</p><ul><li>**Bilanss** – kasutage viitvõlakannete loomiseks bilansi sisestusmeetodit.</li><li>**Tulu ja kulu** – kasutage viitvõlakannete loomiseks tulu ja kulu sisestusmeetodit. Kui kanded on sisestatud, saate arve kande üle vaadata, et vaadata lisakirjeid, mis tasakaalustavad algset tunnustus- ja tunnustusvastassummat.</li></ul> |
| Kreediti kasumi ja kahjumi tagasi võtmine | <p>**Märkus.** See väli on saadaval ainult siis, kui viitvõla **sisestusmeetodi** välja väärtuseks on **seatud Kasum ja kahjum**.</p><p>Määrake, kas kasumi ja kahjumi summad tühistatakse, kui tagasipööramine, lõpetamine või tagasimakse rakendatakse arveldusgraafikule või müügitellimusele:</p><ul><li>**Jah** – tühistage tulu ja kulu summad ja rakendage kreediti korrigeerimissumma viitvõlagraafikule.<p>Kui tagasipööramine toimub pool aega arveldusperioodi jooksul, on summad võrdelised.</p></li><li>**Ei** – kasumi ja kahjumi jaoks ei looda ühtki tagasipööratud kannet, kui tagasipööramist, lõpetamist või tagasimakset rakendatakse arveldusgraafikule või müügitellimusele.</li></ul> |
| **Vahekaart Tuvastamine** | |
| Üldiste töölehtede automaatne sisestamine | <p>Saate määrata, kas tulu ja kulu viitvõlgade abil loodud töölehe sisestused sisestatakse automaatselt:</p><ul><li>**Jah** – sisestage automaatselt töölehe kirjed, mis on loodud tulu ja kulu viitvõlgadega.<p>**Näpunäide**:**valides** Jah, saate aidata ennetada arvestuse vasturääkivuseid, mille põhjuseks on kannete käsitsi muutmine.</p></li><li>**Ei** : tulu ja kulu viitvõlgade loodud töölehe kirjeid ei sisestata automaatselt. Peate käsitsi sisestama mis tahes töölehed.</li></ul> |
| Kajastamise töölehe kokkuvõte | <p>Saate määrata, kas tunnustuskanded konsolideeritakse vaikimisi:</p><ul><li>**Jah** – saate luua ühe kande kõigi sama kuupäevaga tunnustusridade kohta. Kõik ühe ja sama kontoga kande read konsolideeritakse ühele reale.</li><li>**Ei** – saate luua iga tuvastamise rea kande;</li></ul><p>Seda sätet saate uuendada tuvastamise **töötlemise** lehel.</p> |
| Töölehe vaikenimi | Valige töölehe nimi töölehtedele, mis on loodud tulu- ja kulu viitvõlaprotsessidest, nagu tunnustuse töötlemine. |
| Kajastamise töölehe rea kirjeldus. | <p>Saate valida töölehe kanderea kirjelduses kuvatava kirjelduse:</p><ul><li>**Ajakava rea kuupäevad** – graafikurea kuupäevade näitamine töölehe rea kirjelduses.</li><li>**Algse kande üksikasjad** – näidake töölehe rea kirjelduses algset kandeteavet.<p>**Näide:** USMF-0001, CIV-00839, Software Revenue</p></li></ul> |
| **Vahekaart Numbriseeriad** | Kasutage seda vahekaarti, et seadistada liisingu numbriseeriate vaikeväärtused. Numbriseeria loomise viisardit kasutatakse numbriseeriate automaatseks loomiseks ja määramiseks. Te ei pea numbriseeriat muutma, välja arvatud juhul, kui soovite loodud numbriseeriatele käsitsi muudatusi teha. |
| Graafiku number | Viitvõlagraafikutes kasutatav seerianumber. |

## <a name="deferral-templates"></a>Edasilükkamise mallid

Viitvõla **mallide lehel** saate määratleda viitvõlagraafikutes kasutatavad lineaalsed mallid.

Siin on mõned malli kasutamisest:

* Viitvõla pikkus arvutatakse automaatselt.
* Lubate viitvõlagraafikuid, mille perioodid, kus tuvastamine vahele jäetakse.
* Viitvõlgade automatiseerimiseks saate määrata malli tootele, tootegrupile, tootekategooriale, klientidele või kliendigrupile. Malli määramine toimub viitvõla **vaikelehe** kaudu.

Mallide jaoks on saadaval mitu perioodisagedust: igapäevased, igakuised või rahandusperioodid.

Malliread koosnevad tüübist (**Tuvastatud** või **Vahele** jäetud) ja perioodi pikkusest. Vahelejäetud ridade viitvõlagraafiku ridadel on summa 0 (null). Selline käitumine võib olla kasulik, kui te ei soovi tulu kõigil perioodidel ära tunda.

### <a name="create-a-deferral-template"></a>Viitvõlamalli loomine

Viitvõla malli loomiseks järgige neid samme.

1. Valige leheküljel **Viitvõlamallid** väärtus **Uus**.
2. **Sisestage** nimi väljale Mall.
3. Väljale **Kirjeldus** sisestage kirjeldus.
4. Valige väljal **Perioodi** sagedus perioodi sagedus.
5. Rea **lisamiseks** ridade loendi ülaosasse valige lisamisrida **või** valige loendi allserva rea lisamiseks suvand Lisa.
6. **Valige väljal** Tüüp perioodi tüüp.
7. **Määrake väljal** Perioodi pikkus perioodi pikkus.
8. Korrake samme 5 kuni 7 iga täiendava rea puhul, mida vajate.
9. Valige käsk **Salvesta**.

## <a name="deferral-defaults"></a>Edasilükkamise vaikesätted

Kasutage viitvõla **vaikelehte**, et seadistada kaupade viitvõla vaikekontod ja määrata viitvõlgatavatele kaupadele vaikemallid. Samuti saate seadistada viitvõlakontod kulude jaoks ja määrata viitvõlgade kuludele malle.

**Viitvõlg kauba järgi**

Kannete puhul, kus on kaup (nt müügitellimused), saate määrata kontod ja mallid kindlatele kaupadele ja klientidele. Neid sätteid kasutatakse vaikeväärtustena, kui kanne on edasi lükatud. Kande edasilükkamise vaikimisi tegemiseks tuleb kaubad seadistada **lehel Viitmakstavad** kaubad.

**Viitvõlg konto järgi**

Kannete puhul, kus kaubad ei ole (nt üldised töölehed), saate määrata viitvõlakontod. Kui neid kontosid kasutatakse kandereal, märgitakse kanne automaatselt edasilükkumiseks. Kandereale määratakse vastav mall ja tunnustuskonto.

**Kõik kandetüübid (nt müügitellimuste, ostu ja pearaamatu vahekaartide puhul)**

Leheküljel olevad kontod on põhikontod, mis ei oma finantsdimensioone. Tunnustuskonto finantsdimensioonid on pärit kliendilt või kaubalt, mis põhinevad teie organisatsioonil.

Igal mallireal peab olema kas line põhinev mall või sündmusepõhine mall. Sellel ei saa olla mõlemat.

### <a name="for-sales-orders"></a>Müügitellimustele

Müügitellimuste viitvõla vaikeväärtuste määramiseks järgige neid samme.

1. **Valige vahekaardil Müügitellimus** viitvõla tüüp.
2. Rea lisamiseks valige **Lisa**.
3. **Valige kaubakood** väljal Kaubakood. Kaubakood määrab, kuidas viitvõla vaikeväärtusi rakendatakse.
4. Saate määrata kaubakoodi rakendusmeetodeid:

    * Kui välja **Kaubakood** väärtuseks on seatud **Tabel** või **Grupp**, valige kauba seos **väljal Kauba** seos.
    * Kui välja **Kaubakood** väärtuseks on seatud **Kategooria**, valige kategooriaseoses **kategooria seos**.
    * Kui välja **Kaubakood** väärtuseks on seatud **Kõik**, rakenduvad vaikeväärtused kõigile rakendatavatele kirjetele.

5. Saate määrata, kuidas kontokoodi rakendatakse:

    * Kui kontokoodi **välja** väärtuseks on seatud **Tabel** või **Grupp**, valige kontoseose väli **Kontoseose** väljal.
    * Kui kontokoodi **välja** väärtuseks on seatud **Kõik**, rakendub konto kõigile kirjetele.

6. **Valige väljal Põhikonto** viitvõla põhikonto.
7. Kui viitvõla **sisestamismeetodi välja** **väärtuseks on seatud Tulu** ja kulu, **·** **valige algne tulukonto väljal Algse tulu konto ja tulu vastaskonto väljal Tulu** vastaskonto.
8. Kui lühiajalise **viitvõla** **·** **meetodi** välja väärtuseks on seatud Perioodide või fikseeritud aasta, **valige lühiajalise viitvõla konto väljal Lühiajaline viitvõlakonto.**
9. Malli jaoks saate valida rea **lisamiseks** suvandi Lisa.
10. **Valige kaubakood** väljal Kaubakood.
11. Saate määrata kaubakoodi rakendusmeetodeid:

    * Kui välja **Kaubakood** väärtuseks on seatud **Tabel** või **Grupp**, valige kauba seos **väljal Kauba** seos.
    * Kui välja **Kaubakood** väärtuseks on seatud **Kategooria**, valige kategooriaseose **väli Kategooriaseose** väljal.
    * Kui välja **Kaubakood** väärtuseks on seatud **Kõik**, rakenduvad vaikeväärtused kõigile rakendatavatele kirjetele.

12. Saate määrata, kuidas kontokoodi rakendatakse:

    * Kui kontokoodi **välja** väärtuseks on seatud **Tabel** või **Grupp**, valige kontoseose väli **Kontoseose** väljal.
    * Kui kontokoodi **väli** on seatud väärtusele **Kõik**, rakendub konto kõigile rakenduvad kirjetele.
    * Valige line line põhinev mall väljal **Line põhinev mall** või sündmusepõhine mall väljalt **Sündmusepõhine mall**.

13. Valige käsk **Salvesta**.

### <a name="for-purchase-orders"></a>Ostutellimustele

Ostutellimuste viitvõla vaikeväärtuste määramiseks järgige neid samme.

1. **Valige vahekaardil Ostmine** viitvõla tüüp.
2. Rea lisamiseks valige **Lisa**.
3. **Valige kaubakood** väljal Kaubakood.
4. Saate määrata kaubakoodi rakendusmeetodeid:

    * Kui välja **Kaubakood** väärtuseks on seatud **Tabel** või **Grupp**, valige kauba seos **väljal Kauba** seos.
    * Kui välja **Kaubakood** väärtuseks on seatud **Kategooria**, valige kategooriaseose **väli Kategooriaseose** väljal.
    * Kui välja **Kaubakood** väärtuseks on seatud **Kõik**, rakenduvad vaikeväärtused kõigile rakendatavatele kirjetele.

5. Saate määrata, kuidas kontokoodi rakendatakse:

    * Kui kontokoodi **välja** väärtuseks on seatud **Tabel** või **Grupp**, valige kontoseose väli **Kontoseose** väljal.
    * Kui kontokoodi **väli** on seatud väärtusele **Kõik**, rakendub konto kõigile rakenduvad kirjetele.

6. **Valige väljal Põhikonto** viitvõla põhikonto.
7. Kui viitvõla **sisestamismeetodi välja** **väärtuseks on seatud Tulu** ja kulu, **·** **valige algne tulukonto väljal Algse tulu konto ja tulu vastaskonto väljal Tulu** vastaskonto.
8. Kui lühiajalise **viitvõla** **·** **meetodi** välja väärtuseks on seatud Perioodide või fikseeritud aasta, **valige lühiajalise viitvõla konto väljal Lühiajaline viitvõlakonto.**
9. Malli puhul valige rea **lisamiseks** suvand Lisa. 
10. **Valige kaubakood** väljal Kaubakood.
11. Saate määrata kaubakoodi rakendusmeetodeid:

    * Kui välja **Kaubakood** väärtuseks on seatud **Tabel** või **Grupp**, valige kauba seos **väljal Kauba** seos.
    * Kui välja **Kaubakood** väärtuseks on seatud **Kategooria**, valige kategooriaseose **väli Kategooriaseose** väljal.
    * Kui välja **Kaubakood** väärtuseks on seatud **Kõik**, rakenduvad vaikeväärtused kõigile rakendatavatele kirjetele.

12. Saate määrata, kuidas kontokoodi rakendatakse:

    * Kui välja **Konto kood** väärtuseks on seatud **Tabel** või **Grupp**, valige konto seos konto **suhtest**.
    * Kui kontokoodi **väli** on seatud väärtusele **Kõik**, rakendub konto kõigile rakenduvad kirjetele.
    * Valige line line põhinev mall väljal **Line põhinev mall** või sündmusepõhine mall väljalt **Sündmusepõhine mall**.

13. Valige käsk **Salvesta**.

### <a name="for-general-journals"></a>Üldistele töölehtedele

Üldiste töölehe sisestuste viitvõla vaikeväärtuste määramiseks järgige neid samme.

1. Valige vahekaart **Peatööleht**.
2. Viitvõla jaoks valige lisa **,** et rida lisada.
3. Kui lühiajalise **viitvõla** **·** **meetodi** välja väärtuseks on seatud Perioodide või fikseeritud aasta, **valige lühiajalise viitvõla konto väljal Lühiajaline viitvõlakonto.**
4. **Valige väljal Viitvõlakonto** viitvõlakonto.
5. Valige tuvastamise **konto** väljal Tunnustuskonto.
6. Kui viitvõla **sisestamismeetodi välja** **väärtuseks on seatud Tulu** ja kulu, **·** **valige algne tulukonto väljal Algse tulu konto ja tulu vastaskonto väljal Tulu** vastaskonto.
7. Valige line line põhinev mall väljal **Line põhinev mall** või sündmusepõhine mall väljalt **Sündmusepõhine mall**.
8. Valige käsk **Salvesta**.

### <a name="for-free-text-invoices"></a>Vabas vormis arvete jaoks

Vabas vormis arvete viitvõla vaikeväärtuste määramiseks järgige neid samme.

1. Valige vahekaart **Vabas vormis** arve.
2. Viitvõla jaoks valige lisa **,** et rida lisada.
3. Saate määrata, kuidas kontokoodi rakendatakse:

    * Kui kontokoodi **välja** väärtuseks on seatud **Tabel** või **Grupp**, valige kontoseose väli **Kontoseose** väljal.
    * Kui kontokoodi **välja** väärtuseks on seatud **Kõik**, rakendub kontokood kõigile rakendatavatele kirjetele.

4. **Valige väljal Viitvõlakonto** viitvõlakonto.
5. Kui lühiajalise **viitvõla** **·** **meetodi** välja väärtuseks on seatud Perioodide või fikseeritud aasta, **valige lühiajalise viitvõla konto väljal Lühiajaline viitvõlakonto.**
6. Valige tuvastamise **konto** väljal Tunnustuskonto.
7. Kui viitvõla **sisestamismeetodi välja** **väärtuseks on seatud Tulu** ja kulu, **·** **valige algne tulukonto väljal Algse tulu konto ja tulu vastaskonto väljal Tulu** vastaskonto.
8. Valige line line põhinev mall väljal **Line põhinev mall** või sündmusepõhine mall väljalt **Sündmusepõhine mall**.
9. Valige käsk **Salvesta**.

### <a name="for-invoice-journals"></a>Arvetöölehtedele

Arve töölehe sisestuste viitvõla vaikeväärtuste määramiseks järgige neid samme.

1. Valige arve **töölehe** vahekaart.
2. Viitvõla jaoks valige lisa **,** et rida lisada.
3. Saate määrata, kuidas kontokoodi rakendatakse:

    * Kui kontokoodi **välja** väärtuseks on seatud **Tabel** või **Grupp**, valige kontoseose väli **Kontoseose** väljal.
    * Kui kontokoodi **välja** väärtuseks on seatud **Kõik**, rakendub kontokood kõigile rakendatavatele kirjetele.

4. **Valige väljal Viitvõlakonto** viitvõlakonto.
5. Kui lühiajalise **viitvõla** **·** **meetodi** välja väärtuseks on seatud Perioodide või fikseeritud aasta, **valige lühiajalise viitvõla konto väljal Lühiajaline viitvõlakonto.**
6. Valige tuvastamise **konto** väljal Tunnustuskonto.
7. Kui viitvõla **sisestamismeetodi välja** **väärtuseks on seatud Tulu** ja kulu, **·** **valige algne tulukonto väljal Algse tulu konto ja tulu vastaskonto väljal Tulu** vastaskonto.
8. Valige line line põhinev mall väljal **Line põhinev mall** või sündmusepõhine mall väljalt **Sündmusepõhine mall**.
9. Valige käsk **Salvesta**.

### <a name="items-that-are-deferred-by-default"></a>Vaikimisi edasi lükatud kaubad

Vaikelehel **Edasi lükatud kaubad abil** saate määratleda, millised kaubad vaikimisi edasi lükatakse. Saate seadistada kannete tüübid, mille jaoks kaubad edasi lükatakse. Saate määrata, kas üks kaup lükatakse edasi või kogu kaubagrupp või kategooria.

Kui seadistate kaubad edasilükkumiseks, valige vaikekontod ja mallid **viitvõla vaikelehel**. Kui kontosid ja malle ei ole valitud, ei lükata edasi nende kaupade sisestamise kanderidu.

Kaupade puhul, mis on edasi lükatud müügi- või ostukategooria alusel, millega need on seotud, põhinevad viitvõla sätted kategoorial. Kui aga kategooriat pole kategooriaseose **väljal** valitud, kasutatakse astmes kõrgema kategooria viitvõlasätteid. Näiteks saate lisada kodu video **müügikategooria**, kuid mitte televisiooni **müügikategooria**. Kui lisate kategooriaga **Televisioon** seostatud viitvõlakauba, **kasutatakse kauba jaoks kodu video** viitvõlasätteid.

### <a name="set-up-deferred-items"></a>Saate häälestada edasilükatud kaupu.

Vaikimisi edasilükatud kaupade seadistamiseks järgige neid samme.

1. Valige vaikelehel **Kaubad edasi** lükatud vahekaart, mida soovite: **müügitellimus või** **ost**.
2. Rea lisamiseks valige **Lisa**.
3. **Valige kaubakood** väljal Kaubakood.
4. Saate määrata kaubakoodi rakendusmeetodeid:

    * Kui välja **Kaubakood** väärtuseks on seatud **Grupp** või **Tabel**, valige kauba seos **väljal Kauba** seos.
    * Kui välja **Kaubakood** väärtuseks on seatud **Kategooria**, valige kategooriaseose **väli Kategooriaseose** väljal.

5. Korrake samme 2 kuni 4 iga täiendava rea puhul, mida vajate.
6. Valige käsk **Salvesta**.

## <a name="deferred-charges"></a>Viitkulud

Kasutage viitvõla **kulude lehte**, et määrata, millised tasud vaikimisi edasi lükatakse.

> [!NOTE]
> * Praegu on viitvõlgnevad tasud saadaval ainult müügitellimuste jaoks.
> * Tasusid saab edasi lükata ainult rea tasemel. Kulu edasilükkamine müügitellimuse päise tasemel saate seadistada viitkaubana müügitellimuse eraldi real.
> * Vabas vormis arve tasu edasilükkamimiseks peate sisestama tasu eraldi edasilükatud arvereana.
> * See funktsioon pole tugikulude ja tulu tükeldamise funktsiooni jaoks saadaval.

### <a name="set-up-deferred-charges"></a>Saate häälestada viitkulusid.

Edasilükatud tasude häälestamiseks järgige neid samme.

1. **Viitvõla kulude lehel** valige rea **lisamiseks** suvand Lisa.
2. **Valige väljal Tasukood** kulukood.
3. **Valige väljal Tasuseost** kulu seos.
4. Korrake samme 1 kuni 3 iga täiendava rea puhul, mida vajate.
5. Valige käsk **Salvesta**.

## <a name="event-based-deferral-templates"></a>Sündmusepõhised edasilükkamise mallid

Kasutage sündmusepõhist **viitvõlamallide** **lehte, et määrata sündmusepõhised viitvõlamallid, mida saate kasutada viitvõlakannetes ja määrata viitvõla vaikelehel**.

### <a name="create-an-event-based-template"></a>Loo sündmusepõhine mall

Sündmusepõhise viitvõla malli loomiseks järgige neid samme.

1. Sündmusepõhiste **viitvõla mallide lehel** valige **Uus**.
2. **Sisestage** malli kordumatu nimi väljale Mall.
3. Väljale **Kirjeldus** sisestage kirjeldus.
4. Valige väljal **Eraldamise** tüüp eraldamise tüüp:

    * **Muutuv** summa : eraldage konkreetne summa igale sisestatud reale.
    * **Võrdne summa** – eraldage sama summa igale sisestatud reale. 
    * **Protsent** – eraldage summa, mis põhineb iga rea puhul sisestatud protsendiväärtusel.
    * **Valmimisprotsent** – eraldage kumulatiivne lõpetamisväärtus igale sisestatud reale.
    * **Muutuv** kogus – eraldage konkreetne kogus igale sisestatud reale.

5. Kui soovite **, et iga sündmuse rida** **jagatakse** arvekande ühikute arvuga ühtlaselt, määrake suvandi Loo eraldi sündmused ühiku kohta väärtuseks Jah. Kui te ei **soovi** sündmuse ridu tükeldada, määrake selle väärtuseks Ei.
6. Valige aegumiskonto **väljal** Aegumiskonto.
7. Rea **lisamiseks** ridade loendi ülaosasse valige lisamisrida **või** valige loendi allserva rea lisamiseks suvand Lisa.
8. **Sisestage** väljale Kirjeldus sündmuse kirjeldus.
9. Kui välja **Eraldamise tüüp** väärtuseks on seatud **Protsent**, määrake väljal **Eraldamisprotsent eraldise** protsent. Protsent peab olema vahemikus 0 (null) kuni 100. Kui jätate välja **Eraldamisprotsent** tühjaks, peetakse protsenti 0-ks. Kõigi protsentide summa kuvatakse lehe allosas **väljal** Koguprotsent ja peab olema võrdne 100-ga.
10. Määrake väljal **Kuud kuni** aegumiskuupäevani sündmuse kehtivuse kuude arv. Kande viitvõla aegumiskuupäev sisestatakse selle väärtuse alusel automaatselt.
11. Märkige ruut **Tuvasta sisestatud** ajal, et tulu kande sisestamisel automaatselt ära tunda. Kui jätate selle ruudu tühjaks, tuleb tulu käsitsi tuvastada.
12. Valige tunnustuskonto **väljal** sündmuse tunnustuskonto, kui sündmus kasutab kogu viitvõlagraafikust erinevat kontot. Seda välja kasutatakse koos märkeruuduga **Tuvasta sisestamisel**.
13. Korrake samme 7 kuni 12 iga täiendava rea puhul, mida vajate.
14. Valige käsk **Salvesta**.
