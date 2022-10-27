---
title: Kursuste ülevaade
description: See artikkel selgitab, kuidas inimressursside administraatorid ja juhatajad saavad kasutada kursuste funktsioone töötajatele saadaval kursuste kohta teabe säilitamiseks.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable, HcmLearningWorkspace
audience: Application User
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a1fd00fb9feea9ab426f67095770389696452215
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/25/2022
ms.locfileid: "9716282"
---
# <a name="courses-overview"></a>Kursuste ülevaade

Microsoft Dynamics 365 Human Resources pakub lahendust teie organisatsiooni õppevajadustele. See lahendus pakub kahte õppekursuse teed: *virtuaalne* ja *juhendaja juhitud*.

*Virtuaalne* õpe on võrguressursside kaudu täiendatud õppekogemus. Juhendaja *koolitusel hõlbustab* juhendaja töötajate või õppurite grupi koolitusseanssi.

Meie õppemoodulis saavad inimressursside asjatundjad, administraatorid, koolitusjuhid ja haldurid luua ja määrata töötajatele nii kursuseteed kui ka kursused.

> [!NOTE]
> Virtuaalkursuste kasutamiseks peate funktsioonihalduses lubama **kursuse täiustuste** funktsiooni.

## <a name="set-up-virtual-courses"></a>Saate häälestada virtuaalkursusi.

Virtuaalkursuste konfigureerimiseks peate funktsioonihalduses lubama **kursuse täiustuste** funktsiooni. Minge kursusele **Uus \> ja** seadke suvandi Virtuaalne **väärtuseks** **Jah**. Kui see funktsioon on lubatud, on kursuse link vajalik. Kursuse **oleku** välja väärtuseks seatakse **Avatud**. Valik **Luba töötajal end registreerida** seatakse väärtusele **Jah**, kuid selle saab seada valikule **Ei**.

**Pärast kursuste täiustuste** funktsiooni lubamist funktsioonihalduses ilmnevad järgmised muudatused:

- Kursuse määrangu jaoks tuleb määrata tähtaeg.
- Kursuse link on nõutav.
- **Töötaja iseteenindus** näitab töötaja ülevaadet **kursustel**. Kasutaja saab vaadata tähtaja ületanud, varsti või määratud kursusi.
- Töötajad saavad lõpetada virtuaalseid kursusi ja neile end ise testida.

## <a name="set-up-instructor-led-courses"></a>Saate häälestada juhendaja juhitud kursusi.

Juhendajaga seotud kursusi ei pea enne kasutamist konfigureerima.

Järgmine teave on valikuline ja selle saab määrata kursustele. Kui see teave sisestatakse kursuste kohta, tuleb see seadistada enne kursusekirjete loomist:

- Kursuse tüüp
- Klassiruumide grupid
- Kursustegrupid
- Kursuste toimumiskohad
- Klassiruumid
- Juhendajad
- Kursuste tüübid

Kursusetüüpide abil *saate* kursusi liigitada nende struktuuri või sisu järgi. Kursuse tüüpe saate luua leheküljel **Kursuse tüübid** .

Minimaalne ja maksimaalne kursusele registreerida võiv osalejate arv määratakse **** kursuste lehe kiirkaardil **** Üldine.

### <a name="course-setup-type"></a>Kursuse seadistuse tüüp 

*Seadistustüübid* määratlevad kursuse struktuuri. Kursustel on kolm seadistustüüpi.

| Seadistamise tüüp | Kirjeldus |
|------|--------|
| Standardne | Seda tüüpi kursustel ei ole päevakorda. Uue kursuse loomisel on see seadistuse vaiketüüp. |
| Päevakord | Mitme päeva jooksul toimunud kursuse iga päeva üksikasjade plaanimiseks valige see seadistustüüp. |
| Päevakord + seanss | <p>Valige see seadistustüüp keerukamate kursuste jaoks. Näiteks saate jagada kursuse päevakorra teedele ja *seanssidele* *·*:</p><ul><li>*Teed* on kursuse konkreetsed teemaalad.</li><li>*Seansid* jagavad teid ja aitavad määratleda kindlaid teele olulisi protsesse või võtteid.</li></ul> |

### <a name="course-tasks"></a>Kursuse ülesanded

Iga kursuse puhul viige lõpule järgmised ülesanded:

- Osalejate registreerimine.
- Registreerimise lõpptähtaja määramine.
- Osalejate vähima ja suurima arvu määratlemine.
- Kursuse asukoha ja klassiruumi määramine.
- Kursusel osalejatele hotellide soovitamine.
- Looge kursuse kirjeldus, mida saab sisestada töötaja iseteenindusse ****.

> [!NOTE]
> Kursuse saate kustutada ainult siis, kui keegi pole sellele registreerunud.

### <a name="course-statuses"></a>Kursuse olekud

Järgmine tabel loetleb kursuse olekud ja tegevused, mis iga kursuse puhul on lõpetatud.

| Olek | Toimingud |
|------|--------|
| Loodud | <ul><li>Kursuseteabe sisestamine ja redigeerimine.</li><li>Muutke kursuse olekuks Avatud ****, et töötajad saaksid kursusele registreeruda.</li></ul> | 
| Ava | <ul><li>Kursusele osalejate registreerimine.</li><li>Kursuselt osalejate eemaldamine.</li><li>Kursusel osalejate kinnitamine.</li><li>Muutke osalejate, kelle olek on **** Kinnitatud, **** kursuse olekuks Suletud või **Tühistatud**.</li></ul>|
| Suletud | Saate kursuse uuesti avada. |
| Tühistatud | Saate kursuse uuesti avada. |

### <a name="course-participants"></a>Kursusel osalejad

*Kursusel osalejad* on töötajad, kes osalevad koolituskursusel või sündmusel. Osalejaid saate registreerida ainult avatud kursustele.

### <a name="workflow"></a>Töövoog

Töötajatel, kes registreeruvad kursusele Töötaja **iseteeninduslehe** kaudu, saab nende registreerimine suunatakse kinnitamiseks töövoo kaudu. Töövoo saate määrata kursusele kursuste **** lehe üldisel **kiirkaardil** .
