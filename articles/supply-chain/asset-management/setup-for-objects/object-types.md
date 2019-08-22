---
title: Vara tüübid
description: Selles teemas selgitatakse vara tüüpide loomist rakenduses Asset Management. Samuti kirjeldatakse varatüüpidega seotud elemente.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 288dac77f9d999012ec930ef2bca5c0921c2955f
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783214"
---
# <a name="asset-types"></a>Vara tüübid

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

See teema selgitab, kuidas varatüüpe luua. Samuti kirjeldatakse varatüüpidega seotud elemente. Varatüüpe kasutatakse varade üldiste kategooriatena. Näited on CNC-seadmed, mõõteseadmed ja veokimootorid. Varatüüpe kasutatakse vara jaoks valitud töötüüpide (hooldustööde), vara töötsükli olekute, varade, varade atribuutide, seisundi hindamise mallide ja varamudelite haldamiseks. Vara loomisel tuleb määrata vara tüüp.

Iga varatüübi puhul saab luua varade tüübi seadistuse variatsioone. Näiteks kui teil on varatüüp, mille nimi **Veokid**, saate luua erinevate varatootjate ja varamudelite puhul selle varatüübi variatsioone. Igale varatüübi seadistusele saate lisada nõutavaid varuosi ja hoolduskavu.

Esmalt seadistage nõutavad varatüübid. Järgmisena saate luua varamudelid, mis peaksid olema seotud varatüüpidega. Lõpuks saate lehel **Varatüübi vaikesätted** luua kõik teie seadme jaoks vajalikud varatüüpide variandid.

## <a name="create-an-asset-type"></a>Varatüübi loomine

1. Valige **Varade haldus** \> **Seadistus** \> **Varatüübid** \> **Varatüübid**.
2. Varatüübi loomiseks valige **Uus**.
3. Sisestage väljale **Varatüüp** varatüübi ID.
4. Väljale **Nimi** sisestage nimi.
5. Valige väljal **Vara töötsükli olek** vara elutsükli mudel. Lisateavet vara töötsükli olekute ja vara töötsükli mudelite kohta lugege teemast [Vara töötsükli olekud](object-stages.md).
6. Määrake suvandi **Kokku** väärtuseks **Jah**, kui selle varatüübiga varade jaoks tuleb arvutada juhtimismõõdiku (KPI) väärtused.
7. Valige käsk **Salvesta**.
8. Valige kiirkaardil **Töötüübid** töötüübid, mis tuleks siduda varatüübiga.

    - Töötüübi valimiseks valige see väljal **Järelejäänud töötüübid** ja seejärel valige paremnoole nupp ![Paremnoole nupp](media/29-setup-for-objects.png), et teisaldada see jaotisse  **Valitud töötüübid**.
    - Kõigi saadaolevate töötüüpide valimiseks valige nupp ![Edasta kõik](media/30-setup-for-objects.png). Kõik töö tüübid kantakse väljalt **Järelejäänud töötüübid** üle väljale **Valitud töötüübid**.
    - Töötüübi valiku tühistamiseks valige see väljal **Valitud töötüübid** ja seejärel valige vasaknoole nupp ![Vasaknoole nupp](media/31-setup-for-objects.png) selle teisaldamiseks väljale **Järelejäänud töötüübid**.

9. Saate valida ka varamõõdikud, mis peaksid olema seotud varatüüpidega. Kiirkaardil **Varamõõdikud** tehke oma valikud, kasutades meetodeid, mida on kirjeldatud töötüüpide juhises 8. Lisateavet varamõõdikute seadistamise kohta lugege teemast [Varahoolduse mõõtmine](counters.md)
10. Saate valida ka atribuutide tüübid, mis peaksid olema seotud varatüüpidega. Kiirkaardil **Atribuutide tüübid** tehke oma valikud, kasutades meetodeid, mida on kirjeldatud töötüüpide juhises 8. Seejärel valige atribuuditüüpide eelistatud jada loomiseks atribuuditüüp väljal **Valitud atribuuditüübid** ja kasutage selle teisaldamiseks üles-ja allanoolenuppe. Atribuuditüüpide jada näidatakse varadele, mis kasutavad seda varatüüpi. Lisateavet vara atribuutide kohta lugege teemast [Hooldusatribuutide tüübid](../setup-for-functional-locations/specification-types.md).

    > [!NOTE]
    > Uute atribuuditüüpide lisamisel kiirkaardil **Atribuuditüübid** värskendatakse olemasolevat vara automaatselt selle teabega.

11. Saate valida ka seisundi hindamise mallid, mis peaksid olema seotud varatüüpidega. Kiirkaardil **Seisundi hindamine** tehke oma valikud, kasutades meetodeid, mida on kirjeldatud töötüüpide juhises 8. Lisateabe saamiseks seisundi hindamise mallide ja registreerimiste kohta lugege teemat [Seisundi hindamine](../setup-for-objects/condition-assessment.md).
12. Kiirkaardil **Varamudel** kuvatakse kõik varatootjate ja-mudelite kombinatsioonid, mis on seadistatud valitud varatüübis. Et näha tootja järgi jagatud kombinatsioone, tehke lehe **Varamudel** avamiseks valik **Varamudel**.

    Lehel **Varamudel** saate lisada seose varamudel–varatüüp. Lisaks saate lehel **Varadetüübid** lisada vara tootja–varamudeli seosed otse varatüübile. Lõpuks saate lehel **Varamudel** (**Varahaldus** \> **Seadistus** \> **Varad** \> **Varamudel**) luua uued seosed vara tootja–varamudel–varatüüp. Seetõttu on olemas kolm viisi, kuidas seadistada ja muuta seoseid vara tootja–varamudel–varatüüp. Kõik saadaolevad kombinatsioonid kuvatakse erinevast perspektiivist ja seadistusega töötamise ajal saate valida eelistatud sisenemiskoha.

> [!NOTE]
> - Kui valite varatüübis varamõõdikud, uuendatakse valikud automaatselt lehel **Varamõõdikud** (**Varahaldus** \> **Sedistus** \> **Varad** \> **Varatüübid** \> **Varamõõdikud**).
> - Kiirkaardil **Üldine** oleva jaotise **Üksikasjad** väljadel kuvatakse valitud varatüübile seadistatud töötüüpide, varamõõdikute ja atribuutide arv jne.

Tavaliselt on käsitsi loodud töökäsud seotud korrigeeriva hooldusega, samas kui automaatselt loodud töökäsud on seotud ennetava hooldusega. Töökäskude käsitsi loomisel saab kasutada ainult töötüüpe, mis on valitud lehe **Varatüübid** kiirkaardil **Töötüübid**. Siiski saavad automaatselt loodud töökäsud kasutada kõiki lehel **Töötüübid** (**Varahaldus** \> **Seadistus** \> **Tööd** \> **Töötüübis**) loodud töötüüpe.

## <a name="create-asset-type-setup-lines"></a>Varatüübi seadistusridade loomine

1. Valige **Varahaldus** \> **Seadisus** \> **Varad** \> **Varatüübid** \> **Varatüübi seadistamine**. Teise võimalusena saate valida **Varahaldus** \> **Seadistus** \> **Varad** \> **Varatüübid** \> **Varatüübis**, siis varatüübi ja seejärel teha valiku **Varatüübi seadistamine**.
2. Lehe **Varatüübi seadistamine** esmakordsel kasutusel võib kasulik olla nupp **Loo kombinatsioonid**. Selle nupu abil saate kiiresti luua kõik varamudeli kombinatsioonid varatüübile. Valige **Loo kombinatsioonid**, valige varatüüp, millele kombinatsioone luua ja seejärel valige **OK.**

    > [!NOTE]
    > Kui te ei kasuta kõiki automaatselt loodud varatüübi seadistuskombinatsioone, saate seadistuse kustutada, valides selle ja klõpsates seejärel käsku **Kustuta**.

3. Varatüübi seadistuse loomiseks valige **Uus**.
4. Olenevalt sellest, kui konkreetne peab varatüübi seadistus olema, tehke valikud väljadel **Varatüüp**, **Tootja** ja **Mudel**.
5. Kui varatüübiga on seotud garantiileping, valige leping väljadel **Hankija garantii** ja **Kliendi garantii**. 
6. Kiirkaardil **Varuosad** valige **Lisa**, et lisada varuosi valitud varatüübi seadistusele.
7. Varuosa kinnitamiseks valige varuosa rida ja seejärel valige **Kinnita.** Kinnitamiseks saate valida mitu rida.
8. Et näha, kas varuosa kasutatakse mujal moodulis Asset Management (nt seoses varade ja töökäskudega), valige varuosa rida ja seejärel tehke lehe **Kauba kasutuskoht** avamiseks valik **Kauba kasutuskoht**. Loendi kõigi aktiivsete varuosade nägemiseks märkige ruut **Aktiivne**. Ainult kinnitatud varuosade nägemiseks märkige ruut **Kinnitatud**.
9. Kiirkaardil **Hoolduskavad** valige **Lisa**, et lisada hoolduskavasid valitud varatüübi seadistusele.
10. Varatüübi seadistuse kopeerimiseks mõnele muule seadistusele võite kasutada funktsiooni Kopeeri. Valige varatüübi seadistus, kuhu soovite seadistuse kopeerida, valige **Kopeeri seadistus** varatüübi seadistus, millest soovite seadistuse kopeerida. Erinevate suvandite sätted määratlevad, kui palju teavet kaasatakse. Kui olete lõpetanud, klõpsake seadistuse kopeerimiseks nuppu **OK**.

> [!NOTE]
> Kui teil on palju varuosa ja hoolduskava ridu, mida korduskasutate, võimaldab funktsioon Kopeeri teil kiiresti ja hõlpsalt seadistada andmeid mitme varatüübi seadistuskombinatsioonide kohta.

## <a name="spare-parts-on-the-asset-type-setup"></a>Vara tüübi seadistuses olevad varuosad

Nagu kirjeldati jaotises „Varatüübi seadistusridade loomine", seadistatakse varuosad varamudelitele lehel **Varatüübi seadistamine**. Seega, kui avate lehe **Varatüübi seadistamine**, kuvatakse ainult varuosad, mis on seotud varatüübi, vara tootja ja varamudeli valitud kombinatsiooniga. Kõigi varuosakirjete kuvamiseks avage leht **Varuosad** (**Varahaldus** \> **Päringud** \> **Varuosad**).

Lehel **Varuosad** saate luua ka uusi varuosi varatüübi, vara tootja ja varamudeli olemasolevate kombinatsioonide jaoks. Saate otsustada, kas soovite luua varuosa kirjeid lehel **Varatüübi seadistamine** või lehel **Varuosad**. Leht **Varatüübi seadistamine** annab ülevaate andmetest, mis on seotud varatüübi, vara tootja ja varamudeli valitud kombinatsiooniga, samas kui leht **Varuosad** annab annab täieliku ülevaate kõigist varatüübi seadistamise ridadest. Kui leht **Varuosad** sisaldab palju kirjeid, võib leht **Varatüübi seadistamine** anda parema ülevaate.

Et näha, kas valitud real olevat varuosa kasutatakse mujal moodulis Asset Management (nt seoses varade ja töökäskudega), tehke lehe **Kauba kasutuskoht** avamiseks valik **Kauba kasutuskoht**. 

