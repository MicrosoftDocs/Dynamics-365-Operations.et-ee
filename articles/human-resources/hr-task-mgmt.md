---
title: Ülesande haldus
description: See artikkel selgitab Microsoftis saadaolevaid ülesandehalduse funktsioone Dynamics 365 Human Resources.
author: twheeloc
ms.date: 12/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-29-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c567f6d74e6ff87a72ff3b8663ca3a291dff3abb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897860"
---
# <a name="task-management"></a>Ülesande haldus

[!INCLUDE [PEAP](../includes/peap-1.md)]

Ülesande haldus võimaldab teil luua tööülesanded, mis tuleb lõpetada töötajate palkamiseks (põhi põhitööks), töölepingu lõpetamiseks (väljaminev) ja töötajate üleviimine (üleviimine). Ülesandehaldus kasutab kontroll-loendite kontseptsiooni. Kontroll-loend on loend põhi-, ameti- või üleminekuülesannete kohta. Ülesandehaldus kasutab kontroll-loendeid ülesannete grupeerimiseks ja nende määramiseks üksikisikutele või gruppidele. Kontroll-loendi funktsioonid on sisse- ja väljalülitamine sarnased.

## <a name="checklist-overview"></a>Kontroll-loendi ülevaade

Kontroll-loend on ülesannete grupp. Kontroll-loendid annavad teile paindliku viisi ülesannete grupeerimiseks ning neid saab uuesti kasutada (nt lisatöötajate palkamisel). Saate luua nii palju kontroll-loendeid, kui vaja ja saate määrata samad ülesanded mitmele kontroll-loendile.

### <a name="examples"></a>Näited

Järgnevad näited näitavad, kuidas kontroll-loendeid saab kasutada sisseldmisprotsessis. Kuna aga kontroll-loendi funktsioonid on tahvlile, offboardingu ja üleminekud sarnased, rakendub teave ka offboarding- ja siirdeprotsessidele.

Osana vastuvõetavast protsessist saavad inimressursside spetsialistid luua ülesandeid, mis jälgivad sissetulevate ja hiljuti palgatud töötajate edenemist. Kuna sisseostmise protsess võib sõltuvalt töötaja positsioonist või geograafilisest asukohast erineda, saate erinevate palkamise situatsioonide jaoks luua mitu sisseseadmis kontroll-loendit.

**Näide 1**

Iga Ameerika Ühendriikidesse palgatud töötaja peab täitma selliseid ülesandeid nagu maksude kinnipidamisvormide täitmine. Kuid ülesanded, nagu ettevõttele auto määramine, võivad olla rakendatavad ainult tegevdirektori taseme personalile. Sel juhul saab luua kaks põhilist kontroll-loendit: **ainult USA-põhised** **töötajad ja juhatajad**. Seejärel valitakse USA kesktaseme juhi palkamisel **USA-s põhinevad töötajate kontroll-loend**. Kuid kui usa-s palgatakse tegevdirektor, valitakse mõlemad kontroll-loendid, et tagada kõikide nõutud põhiülesannete täitmist.

**Näide 2**

Ettevõttes on nii hooajalisi kui ka regulaarseid täiskohaga töötajaid. Kuigi teatud tööülesanded (nt uue töötaja saabumise aja kontrollimine) rakenduvad mõlemat tüüpi töötajatele, rakenduvad mõned lisaülesanded ainult regulaarsetele täiskohaga töötajatele. Sel juhul saate luua kaks kontroll-loendit. Mõlemad kontroll-loendid hõlmavad nii hooajalisi kui ka regulaarseid täistööajaga töötajate ülesandeid, kuid ainult üks kontroll-loend sisaldab seda, et regulaarsetele täiskohaga töötajatele omased ülesanded.

## <a name="task-management-workspace"></a>Ülesannete halduse tööruum

Ülesandehalduse **tööruum** loendab kõik ülesanded, mis on üksikisikutele määratud sisseastumisel, mahajuhtimisel ja üleminekuprotsessides. Protsessi ülesannete vaatamiseks valige vastav vahekaart ülemises vasakpoolses nurgas: **Sisse lülitatud**, **Välja lülitatud** või **Üleminekud**. Vaikimisi pääsevad ülesandehalduse tööruumile juurde ainult **personalispetsialistid**.

Vahekaart **Sissetulev vahekaart** sisaldab peatselt **algloendit**, mis **näitab** hiljuti palgatud töötajaid ja sissetulevate töötajate loendit. Mõlemas loendis saate valida ainult ühe töötaja. Kui valite töötaja, näidatakse kõiki selle töötajaga seotud ülesandeid lehekülje paremal küljel. Vahekaart **Sissetulev sisaldab** ka kõigi ülesannete **loendit**, mis näitab kõiki sissetulevate või hiljuti palgatud töötajate ülesandeid. Lõpuks sisaldab see tähtaja ületanud ülesannete loendit ja praegusele kasutajale määratud ülesannete loendit.

Vahekaart **Offboarding** sisaldab ettevõttest lahkunud töötajate loendit ja ettevõttest juba väljunud töötajate loendit. Mõlemas loendis saate valida ainult ühe töötaja. Kui valite töötaja, kuvatakse kõik ülesanded, mis on seotud selle töötaja ametist väljas olemisega. Vahekaart **Offboarding** sisaldab ka kõigi ülesannete **loendit, mis** näitab kõiki ülesandeid kõigi lahkumis- või lahkumistöötajate jaoks. Lõpuks sisaldab see tähtaja ületanud ülesannete loendit ja praegusele kasutajale määratud ülesannete loendit.

Vahekaart **Siirded** sisaldab kõigi ülesannete **loendit**, mis näitab kõiki ülesandeid kõigi töötajate jaoks, kes ametikohti muudavad või kes on hiljuti vahetanud ametikohti. Samuti on olemas tähtaja ületanud ülesannete loend ja praegusele kasutajale määratud ülesannete loend.

Kõigil kolmel vahekaardil saavad personali abistajad ja haldurid sooritada järgmisi toiminguid:
- Kontroll-loendi töötajale rakendamine
- Ülesande oleku värskendamine
- Ülesande uuestimääramine
- Ülesande tähtaja värskendamine

> [!NOTE]
> Vaikimisi näitab vahekaart **Sisseostja** töötajaid, kes on palgatud viimase 7 päeva jooksul. Selle sätte muutmiseks **sisestage** **·** **ajaraami lehekülje Inimressursside parameetrid vahekaardi Üldine väljale Hiljutised** palkamised. Loendis Hiljutised **palkamised** kuvatud teavet saab kuvada kindla päevade, kuude või aastate arvu kohta. Näiteks viimase 14 **päeva jooksul palgatud töötajate loendi vaatamiseks seadke välja Periood** **väärtuseks 14** **ja** välja Ühik väärtuseks Päevad.**·**
> **Inimressursside parameetrite lehel** saate uuendada ka lahkumis- ja väljumistöötajate loendite kuupäevavahemikku, mis kuvatakse **vahekaardil Mahapaigutus**. Need sätted kehtivad ka personalihalduse **tööruumi** kohta.

## <a name="setting-up-tasks"></a>Ülesannete seadistamine

Saate ülesandeid luua ükshaaval ja seejärel taaskasutada neid mitmes kontroll-loendis. Ülesande loomiseks tehke lehel Põhiseadistus vahekaardil Ülesanded valik **Uus**.**·** **·**

Võite ülesandeid lisada ka otse kontroll-loendisse. Ülesande lisamiseks kontroll-loendile, **·** **on sisseostmise seadistuse lehel vahekaardil Kontroll-loend** looge uus kontroll-loend, et ülesanne lisada või lisage ülesanne olemasolevasse kontroll-loendisse.

> [!NOTE]
> Kui lisate ülesande otse kontroll-loendisse, ei saa te seda teistes kontroll-loendites taaskasutada.

Järgmises tabelis kirjeldatakse välju, mis on saadaval, kui loote ülesande mõlema meetodiga.

| Väli           | Kirjeldus |
|-----------------|-------------|
| Ülesanne            | Sisestage ülesande nimi. |
| Kirjeldus     | Sisestage ülesande kirjeldus. |
| Valikuline        | Määrake, kas ülesanne on valikuline ja ainult teabeline. |
| Ülesande link       | Sisestage välise veebilehe VÕI kindla lehe URL rakenduses, kus kasutaja peaks ülesande lõpule viima. Lisateavet vt ülesande linkide [jaotisest](#task-links). |
| Määramise tüüp | Ülesandeid saab määrata kindlale töötajale, ametikohale või positsioonide grupile, mõjutatud töötaja juhatajale (st töötajale, kes on osa põhitööst, ametialalt või siirde protsessist) või mõjutatud töötajale. Valige määramise tüüp. Lisateavet vt jaotisest [Määrangutüübid](#assignment-types). |
| Määratud kasutajale     | Valige konkreetne töötaja, ametikoht või positsioonide grupp, mille jaoks ülesanne määrata. |
| Kontaktisik  | Saate määrata isiku, kellega tuleks ühendust võtta, kui ülesande kohta on küsimusi. |
| Tähtaja vastaskonto | Määrake päevade arv enne või pärast ülesande täitmiseks lubatud põhist, lõpetamist või siirde kuupäeva. Lisateavet vt jaotisest Ülesande [tähtajad ja Tähtaja vastaskonto](#task-due-dates-and-the-due-date-offset-field) väli. |
| Juhised    | Sisestage juhised ülesande lõpetamiseks. Lisateavet vt jaotisest [Juhised](#instructions). |

### <a name="task-links"></a>Ülesande lingid

Ülesande link annab lingi välisele veebilehele või Dynamics 365 rakenduse leheküljele. Saate määrata ülesande lingi, kui ülesandega seotud isik peaks ülesande lõpetamiseks minge konkreetsele veebilehele või kindlale lehele Dynamics 365 rakenduses. Ülesande lingi loomisel saate valida ühe järgmistest suvanditest:

- **Menüükäsk** – selle suvandi valimisel kuvatakse Dynamics 365 rakenduse kõigi lehtede loend. Valige loendist lehekülg.
- **URL** : selle suvandi valimisel sisestage selle veebilehe URL, kuhu soovite ülesandele määratud isiku üle viia. Määratud lehekülg võib olla leht, mis ei ole Dynamics 365 rakenduse osa.
- **Töötaja üksikasjad** – selle suvandi valimisel valige üks järgmistest suvanditest:

    - **Töötaja iseteenindustegevused** – see valik kuvab loendi lehtedest, mis on saadaval Töötaja **iseteeninduses**. Kasutage seda juhul, kui töötajale määratud ülesanne peab olema täidetud Töötaja **iseteeninduses**. Näiteks kui soovite, et töötaja sisestaks oma isikliku kontaktteabe, valige **Töötaja iseteenindustegevused** ja seejärel isiklikud **&gt; andmed**.
    - **Töötaja haldustegevused** – see suvand kuvab loendi lehtedest, mis on seotud töötaja kirjega, kuid mis pole töötaja jaoks saadaval. Näiteks kui soovite, et ülesande omanik sisestaks teabe, mis on omane põhitöölisele, nt kompensatsiooni teave, **valige** Töötaja haldustegevused ja seejärel valige **Tasu&gt; põhitasu**.

### <a name="assignment-types"></a>Määrangutüübid

Kui töötaja on palgatud, lõpetatud või üle kantud, saab valida ühe või mitu kontroll-loendit. Kui kontroll-loend on valitud ja palkamise, lõpetamise või üleviimise protsess on lõpetatud, luuakse toimingud ja määratakse edenemise jälgimiseks kasutajatele.

Ülesande loomisel määratakse see kindlale kasutajale. Kasutaja, kellele ülesanne määratakse, sõltub ülesande jaoks valitud määramise tüübist. Väljal Määrangu tüüp on saadaval **järgmised** väärtused:

- **Töötaja** : määrake ülesanne kindlale töötajale. Pärast selle väärtuse valimist valige töötaja väljal **Määratud**.
- **Ametikoht** – määrake ülesanne kindlale ametikohale. Pärast selle väärtuse valimist valige positsioon **väljal Määratud**.

    Näiteks IT-insener vastutab alati sülearvuti ettevalmistamise eest uuele töötajale. Sel juhul, kui loote sülearvuti konfiguratsiooni ülesande, valige **määramise** tüübiks positsioon ja seejärel valige **ametikohaks IT-insener**. Seejärel, kui töötaja palgatakse ja kontroll-loend on määratud, määratakse sülearvuti konfiguratsiooni ülesanne sellele, milline töötaja on IT-insener positsioonil palkamise toimingu sisestamise ajal.

- **Grupp** – ülesande määramine positsioonide grupile (määrangugrupp). Pärast selle väärtuse valimist valige grupp **väljal Määratud**. Lisateavet vt jaotisest Määramisgruppide [seadistamine (Valikuline](#setting-up-assignment-groups-optional)).
- **Juhataja** : määrake ülesanne palgata, lõpetatud või ülekantud töötaja juhile.

    > [!IMPORTANT]
    > Kui kontroll-loendit ei rakendata, ei saa juhatajat määratleda, kui palgatud, lõpetatud või üle kantud töötajale pole praegu ametikohta määratud. Sel juhul määratakse ülesanne kontroll-loendi omanikule. Lisateavet vt jaotisest [Kontroll-loendite seadistamine](#setting-up-checklists).

- **Töötaja** – määrake töötaja, kes palgatakse, lõpetatakse või üle viiakse.

### <a name="task-due-dates-and-the-due-date-offset-field"></a>Ülesande tähtajad ja tähtaja vastaskonto väli

Ülesande tähtajad põhinevad töösuhte alguskuupäeval, lõpetamise kuupäeval või siirde kuupäeval. Mõned ülesanded peavad olema lõpetatud enne töötaja alguskuupäeva, samas kui teisi ülesandeid saab pärast lõpule viia. Ülesande määratlemisel seadistate **tähtaja** vastasvälja, et määrata alguskuupäeva, lõpetamise kuupäeva või siirde kuupäevaga seotud tähtaeg. Näiteks IT-insener peab uuele töötajale kaks päeva enne selle töötaja alguskuupäeva sülearvuti ette valmistama. Sellisel juhul, kui loote sülearvuti konfiguratsiooni ülesande, seadistage **tähtaja tasakaalustuse välja** väärtusele **-2**. Kui töötaja alguskuupäev on 5. mai, on ülesande tähtaeg 3. mai.

> [!NOTE]
> Tähtaegu saab pärast ülesande loomist korrigeerida.

Tähtajad arvutatakse kontroll-loendiga seotud kalendri alusel. Lisateavet vt jaotisest [Kontroll-loendite seadistamine](#setting-up-checklists).

### <a name="instructions"></a>Juhised

Kompleksülesanded võivad nõuda mitut sammu või võib isikul, kes ülesannet täidab, anda täiendavat teavet. **Väljale Juhised** saate sisestada juhised või lisateabe ülesandega seotud isiku abi saamiseks.

## <a name="setting-up-checklists"></a>Kontroll-loendite seadistamine

Kontroll-loend on ülesannete grupp. Saate luua nii palju kontroll-loendeid, kui vaja ja saate määrata samad ülesanded mitmele kontroll-loendile. Kontroll-loendi loomisel määrate omaniku ja kalendri.

Kui ülesande **määrangu** tüübi **väli** on seatud väärtusele Positsioon, **·** **Juhataja või Grupp**, kuid määramise tüübist ei saa konkreetset töötajat tuletada, määratakse ülesanne kontroll-loendi omanikule. Siin on mõned näited olukorrast, kus ülesanded määratakse kontroll-loendi omanikule:

- Palgaastatele või tööltaanud töötajale pole ühtegi positsiooni määratud. Kuna töötajale ei ole määratud ametikohta, ei saa tema juhatajat määrata.
- Välja **Määrangu** tüüp väärtuseks on **seatud** Positsioon, kuid töötajat pole ülesande loomise ajal ametikohale määratud. Näiteks määratakse sülearvuti seadistuse **ülesanne** positsiooninumbrile 000876 (**Tehnilise toe spetsialist**). Töötaja palkamise ajal pole ühtegi töötajat määratud ametikohale 000876. Seepärast luuakse kontroll-loendi omaniku jaoks ülesanne.
- Välja **Määrangu** tüüp väärtuseks on **seatud** Grupp, kuid töötajat pole ülesande loomise ajal grupi positsioonidele määratud.

Kontroll-loendi jaoks määratud kalendrit kasutatakse selle kontroll-loendiga seotud ülesannete tähtaja arvutamiseks. Töö- ja mitte tööpäevad määratletakse kalendri seadistuses. Tööpäevad kaasatakse ülesannete tähtaja arvutamisel ja mitte-tööpäevad jäetakse välja. Mittetööpäevad hõlmavad nädalavahetusi ja puhkusi. 

Pärast kalendri seadistamist on see seotud kontroll-loendi malliga. Sel viisil arvutatakse kontroll-loendi iga ülesande tähtaeg samal viisil. Saate seadistada mitmeid kalendreid, kuid iga kontroll-loendiga saab seostada ainult ühe kalendri.

## <a name="setting-up-assignment-groups-optional"></a>Määramisgruppide seadistamine (valikuline)

Mõnikord vastutab ülesande eest üksikisikute grupp. Näiteks grupp IT-töötajaid võib olla vastutav sülearvutite ettevalmistamise eest uuteks töötajateks.

Määrangugrupi häälestamiseks järgige neid samme.

1. Grupi määrangulehel **valige** uus **·**.
1. Sisestage grupi nimi (**nt IT-sülearvuti**) ja kirjeldus.
1. Valige käsk **Salvesta**.
1. Valige kiirkaardil **Liikmed** suvand **Lisa**.
1. Väljal Positsioonid **valige** kõik ametikohad, mis ülesande eest vastutavad.

Kui määrangugrupp on loodud, on see saadaval valiku jaoks ülesande loomisel. Konkreetse grupi valimiseks ülesandele peate valima suvandi Grupp **tüübist** **Määramine**. Loodud grupp on seejärel saadaval valiku jaoks väljal **Määratud**.

> [!IMPORTANT]
> Kui ülesanne on määratud grupile, märgitakse ülesanne **lõpetatuks**, kui üks gruppi täidab selle. Ülesanded luuakse palkamise, lõpetamise või ülemineku ajal. Need luuakse kasutajatele, kes on määratud gruppi kaasatud positsioonidele.

## <a name="setting-up-task-groups-optional"></a>Ülesandegruppide seadistamine (valikuline)

Põhi-, offboarding või siirde protsess võib sisaldada palju ülesandeid. Kõigi nõutud ülesannete kontroll-loendile määramise hõlbustamiseks saate luua valikulisi ülesandegruppe seotud ülesannete kategoriseerimiseks. Näiteks inimressursside, IT ja palgaosakonnad peavad uue töötaja palkamiseks täitma kõik konkreetsed ülesanded. Seetõttu loote järgmised ülesandegrupid: **HR**, **IT** ja **Palk**. Seejärel saate ülesande loomisel seostada sellega ühe neist ülesandegruppidest.

Kui soovite lisada ülesande kontroll-loendisse, saate filtreerida ülesannete loendit ülesandegrupi järgi, millele on määratud soovitud ülesanne. Näiteks kontroll-loendi malli loomisel saate loendit filtreerida nii, et kuvatakse ainult IT-ülesandegrupile **määratud IT-toimingud**. Seega saate tagada, et valitakse ainult asjakohased IT-toimingud.

## <a name="using-checklists"></a>Kontroll-loendite kasutamine

Kui töötaja on palgatud, lõpetatud või üle kantud, saab valida ühe või mitu kontroll-loendit. Ülesande tähtajad ja töötaja määramised luuakse pärast palkamise, lõpetamise või ülemineku protsessi lõpetamist. Näiteks kui valite nupu Palka **või** **Palka ja lisa** üksikasjad, luuakse tööülesanded üksikisikutele, võttes aluseks määramise tüübi.

Igale ülesandele määratakse tähtaeg, lisades või lahutades töötaja alguskuupäevast tähtaja tasakaalustuse. Lisateavet vt jaotisest Ülesande [tähtajad ja Tähtaja vastaskonto](#task-due-dates-and-the-due-date-offset-field) väli.

Personalitoimingute kasutamisel luuakse ülesanded nupu **Lõpeta** valimisel või tegevuse heakskiidul.

Ülesandehalduse **tööruumis** saate rakendada töötajale kontroll-loendi, valides töötaja lihtsal loendilehel või üksikasjade lehel ja valides seejärel rakenda **kontroll-loendi**. Välja Sihtkuupäev **kasutatakse** ülesannete tähtaja arvutamiseks. Tavaliselt peab sihtkuupäev vastama töötaja palkamise, lõpetamise või siirde kuupäevale.

Kontroll-loendit saate rakendada ka töötajale, avades lehekülje **Töötaja** ja valides **menüüst Kontroll-loendid**.

## <a name="completing-tasks"></a>Ülesannete lõpuleviimine

**Töötaja iseteeninduse** lehel saab töötaja vaadata kõiki talle määratud ülesandeid. Kuvatakse iga määratud ülesande, **ülesande**, **kirjelduse** **·**, juhiste **ja kontaktisiku** väärtused. Lisaks saab töötaja iga ülesande jaoks avada seotud välist veebilehte või seotud lehte Dynamics 365 rakenduses.

Ülesandeid saab kuvada ka vaike-armatuurlaudal. Vaike-armatuurlauda ülesannete kuvamiseks:
1. Avage kasutajavalikud **– eelistused – ülesandehaldus** 
2. Valige suvand Kuva **ülesanded vaikimisi armatuurlauda** valikule **Sees**.  

>[!Note] 
>Kasutaja **valikutes** kuvamiseks peab ülesandehalduse **funktsioon** olema funktsioonihalduses **sisse lülitatud**.

Toimingud saab märkida kui **Pooleli**, Tühistatud **või** Lõpule **viidud**. Kui ülesanne määrati grupile, märgitakse **see** lõpetatuks, kui üks gruppi täidab selle.

Ülesandeid saab ka uuesti määrata.
