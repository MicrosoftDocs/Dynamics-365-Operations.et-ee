---
title: Töökäsu elutsükli olekud
description: See artikkel selgitab varahalduses töötellimuse töötsükli olekuid.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderLifecycleState, EntAssetWorkOrderLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9c6a7c204370542353e9b629b78091972f8ce9a1
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017083"
---
# <a name="work-order-lifecycle-states"></a>Töökäsu elutsükli olekud


[!include [banner](../../includes/banner.md)]

 

Töökäsu töötsüklis määratletakse olekud, mida töökäsk saab läbida. Näideteks **on** Loodud **,** Planeeritud **, Käimas** ja **Lõpetatud**. Töökäsu töötsükli olekuid saab töökäsul käsitsi uuendad või neid saab automaatselt uuendada (nt töökäsu planeerimisel).

Töökäsu töötsüklite olekud, mis on vajalikud teie tööolekute jaoks, tuleb siduda vastavate projektietappidega lehel **Projektijuhtimine ja raamatupidamise parameetrid** (**projektijuhtimine ja raamatupidamine** \> **Projektijuhtumise ja raamatupidamise parameetrid**). Esmalt seadistage projektietapid lehel Projektijuhtimine ja raamatupidamine. Seejärel seadistate töökäsu töötsükli olekud ja töökäsu töötsükli mudelid Varahalduses.

Järgmises tabelis on kirjeldatud valikud jaotistes **Töökäsk** ja **Graafik** kiirkaardil **Üldine** lehel **Töökäsu töötsükliolek** lehel (**Varahaldus** \> **Seadistus** \> **Töökäsud** \> **Töötsükli olekud**).

![Töökäsu töötsükli oleku leht.](media/09-setup-for-work-orders.png)

| Valiku nimi                   | Kirjeldus |
|-------------------------------|-------------|
| Aktiivne                        | Seadke see suvand valikule **Jah**, kui töökäsk peaks olema selles töötsükli olekus aktiivne. |
| Lisa rida                      | Seadke see suvand väärtusele **Jah**, kui töökäsu töid saab lisada tööolekule, mis on selles töötsükli olekus. |
| Kustutusklahv DELETE                        | Seadke see suvand valikule **Jah**, kui töökäsku saab selles töötsükli olekus kustutada. |
| Kas kustutada rida?                   | Seadke see suvand väärtusele **Jah**, kui töökäsu töid saab töökäsult kustutada, mis on selles töötsükli olekus. |
| Luba plaanimine              | Seadke see suvand valikule **Jah**, kui töökäsku saab selles töötsükli olekus graafikusse lisada. |
| Tegeliku alguse seadistamine              | Seadke see suvand väärtusele **Jah**, kui kasutajal palutakse valida töö tegelik alguskuupäeva ja-kellaaeg, kui see on selle töötsükliolekusse uuendatud. |
| Tegelik lõpu seadistamine                | Seadke see suvand väärtusele **Jah**, kui kasutajal palutakse valida töö tegelik lõpukuupäeva ja-kellaaeg, kui see on selle töötsükliolekusse uuendatud. |
| Sisesta töölehed                 | Seadke see suvand väärtusele **Jah**, kui töökäsu tööd tuleb automaatselt lisada, kui töökäsku uuendatakse selles töötsükliolekus. Kui töölehe sisestamisel ilmneb tõrge, kuvatakse teade ja töökäsu töötsükli oleku uuendamine on tühistatud. Töötellimuse **tööleheridade** \> **·** \> **vaatamiseks** valige varahalduse töötellimused Kõik töötellimused, **·** **aktiivsed** töötellimused või minu aktiivsed töötellimused, valige loendist töötellimus ja seejärel valige **Töölehed.** See automaatse töökäsu töölehe sisestamise seadistus kindlas töötsükli olekus on sama, mis siis, kui valite **Postita töölehed** lehel **Tööoleku töölehed**.<p>**Märge:** kui seate selle suvandi väärtuseks **Jah**, sisestatakse töölehed automaatselt, kui kinnitamise töövoogu pole seadistatud. Kui teie ettevõte kasutab töölehe kinnitamise seadistust, mis on konfigureeritud lehel **Töölehe kinnitamine** (**Projektijuhtimine ja raamatupidamise** \> **Seadistus** \> **Töölehed** \> **Töölehe kinnitamine**), peab haldur või ametnik kontrollima ja sisestama tarbimisjärgseid registreerimisi.</p> |
| Hoolduse kontrollnimekirja töötlemine | Seadke see suvand väärtusele **Jah**, kui kõik toodud hoolduse kontrollnimekirjad tuleb töödelda, kui töökäsku uuendatakse selles töötsükliolekus. Selle töötluse osana sisestatakse kõik hoolduse kontroll-loendis tehtud loenduri registreerimised ja hinnatakse kogu hoolduse kontroll-loendi tulemust. Hoolduse kontrollnimekirja ridu tulemustega **Keela** ja **Nurja** hinnatakse, kui kui vähemalt üks rida nurjub, märgitakse kogu hoolduse kontrollnimekiri väärtusele **Nurjunud**. |
| Valmis                         | Seadke see suvand väärtusele **Jah**, kui töökäsu töögraafiku olek kõigi töökäskude tööde jaoks, mis luuakse töökäsul, tuleks automaatselt uuendada olekuks **Valmis**, et see oleks töötsükli olekusse jõudmisel uuendatud. |
| Alusta                         | Seadke see suvand väärtusele **Jah**, kui töökäsu töögraafiku olek kõigi töökäskude tööde jaoks, mis luuakse töökäsul, tuleks automaatselt uuendada olekuks **Alustatud**, et see oleks töötsükli olekusse jõudmisel uuendatud. |
| Lõpp                           | Seadke see suvand väärtusele **Jah**, kui töökäsu töögraafiku olek kõigi töökäskude tööde jaoks, mis luuakse töökäsul, tuleks automaatselt uuendada olekuks **Lõppenud**, et see oleks töötsükli olekusse jõudmisel uuendatud. |
| Kustuta graafiku read         | Seadke see suvand väärtusele **Jah**, kui kõigi töökäskude tööde jaoks, mis on juba graafikusse lisatud, tuleks kustutada graafiku olek, et see oleks töötsükli olekusse jõudmisel uuendatud. Teisisõnu kustutatakse vara, sellega seotud hoolduse töötaja ja seotud tööriistade võimsuse reserveeringud. Näiteks seadistage see suvand väärtusele **Jah** tööoleku töötsükli olekus, mille nimi on **Hinnnanguline**. Seejärel, kui tööolek on tagasi selle töötsükli olekus, kuna on vaja ümberplaneerimist, saate selle töökäsu puhul selle kustutada. |

## <a name="set-up-project-stages-and-work-order-lifecycle-states"></a>Projektietappide ja töökäsu töötsükli olekute seadistamine

1. Klõpsake valikuid **Projektihaldus ja raamatupidamine** \> **Seadistus** \> **Projektihalduse ja raamatupidamise parameetrid**.
2. Märkige vahekaardil **Projektietapp** iga kasutatava etapi kohta ruut iga projekti tüübi kohta, mis on vajalik teie töökäskude jaoks. Projektitüübid määratlevad reeglid finantsülesannete kohta, mis on lubatud. Finantsülesannete näited on näiteks eelarve loomine, hinnangute loomine ja algsaldo loomine.

    > [!IMPORTANT]
    > Kui projektitüübi jaoks projektietappi ei valita, kuid projektietappi kasutatakse tööolek töötsükli olekus, ei värskendata tööolekute projekte sobival viisil.

3. Sulgege vorm **Projektijuhtimise ja raamatupidamise parameetrid**.
4. Valige **Varahaldus** \> **Seadistus** \> **Töökäsud** \> **Töötsükli olekud**.
5. Valige uue töökäsu töötsükli oleku loomiseks **Uus**.
6. Sisestage väljale **Elutsükli olek** elutsükli olek ID.
7. Väljale **Nimi** sisestage nimi.

    Kiirkaardi **Üksikasjad** väljal **Töötsükli mudelid** kuvatakse töökäsu töötsükli mudelite arvu, mida selles elutsükli olekus kasutatakse.

8. Valige kiirkaart **Üldine** jaotises **Töökäsk** ja seejärel valige funktsioonid, mis peaksid olema selle töötsükli oleku jaoks saadaval, seades vastavad valikud väärtusele **Jah**. Valikute kirjeldusi vt käesoleva artikli varasemast tabelist.
9. Jaotises **Projekt** valige väli **Etapp**, seejärel valige projektietapp, mis peaks olema selle töötsükli olekuga seotud.
10. Seadke jaotises **Projekt** valik **Sule tegevused** väärtuseks **Jah**, kui projekti tegevused, mis on seotud iga töökäsu tööga, tuleb automaatselt sulgeda, kui töö tellimus on selles töötsükli olekus.

    > [!NOTE]
    > Töötellimuse **tööga** \> **·** \> **seotud projektitegevuse numbri leidmiseks valige varahalduse töötellimused Kõik** töötellimused, **aktiivsed** töötellimused või minu **aktiivsed töötellimused.** Avage töökäsk ja valige töökäsu töö. Tegevuse number kuvatakse väljal **Aktiivsuse number** jaotises **Projekt** kaardil **Üldine** kiirkaardil **Rea üksikasjad**.

11. Seadke jaotises **Prognoos** valik **Kopeeri tundide prognoos**, **Kopeeri kauba prognoos** ja/või **Kopeeri kulude prognoos** väärtusele **Jah**, kui tööoleku projekti prognoosid kopeeritakse tööoleku töölehtedesse automaatselt, kui tööolek on selles töötsükli olekus.
12. Seadke jaotises **Graafik** üks valikutest väärtusele **Jah**, kui töökäsu tööde graafiku olekut tuleb uuendada, kui töökäsk on selles töötsükli olekus. Graafikuridade suvandite **Valmis**, **Algus**, **Lõpp** **ja** Kustuta kirjeldusi vt käesoleva artikli tabelist.

    > [!NOTE]
    > Töötellimuse töödega seotud graafiku ridade vaatamiseks **valige** \> **·** \> **Varahalduse** töötellimused Kõik töötellimused, **aktiivsed** töötellimused või minu **aktiivsed töötellimused.** Avage töökäsk, valige töökäsu töö kiirkaardilt **Töökäsu tööd** ja vaadake seotud teavet kiirkaardilt **Rea üksikasjad**. Vahekaardi **Graafik** väli **Olek** näitab töökäsu töö olekut. Välja **Olek** väärtuseks saab seada järgmised väärtused: **Plaanitud**, **Valmis**, **Alustatud**, **Peatatud** ja **Lõpetatud**.

13. Valige jaotises **Hooldusnõuded** väljal **Töötsükli olek** hooldusenõude töötsükli olek, kuhu seotud hooldustööd tuleb uuendada. See uuendus toimub automaatselt. Seda saab teha ainult juhul, kui hooldusenõude töötsükli olek on valitud hooldusnõude töötsükli mudelis, mida kasutatakse hooldusnõude puhul.
14. Seadke jaotises **Vara** suvandi **Uuenda vara kooslus** väärtuseks **Jah**, kui kõik töökäsul kasutatavad kaubad tuleks töökäsu uuendamisel automaatselt uuendada lehel **Vara kooslus**, kui töökäsk uuendatakse sellesse töötsükli olekusse. See säte võib olla asjakohane, kui näiteks töökäsu töötsükli olek määratleb töökäsu lõpetatuks või lõpetatud.
15. Seadistage jaotises **Töökäsu kaust** suvand **Kustuta kausta viide** väärtuseks **Jah**, kui selles töötsüklis olevate töökäskude olek tuleks automaatselt töökäskude kaustadest kustutada.
16. Valige kiirkaardil **Kinnita** kinnitamistüübid, mis tuleks selles töötsükli olekus aktiveerida, seades vastavad valikud väärtusele **Jah**. Seejärel valige iga valitud kinnitustüübi väljas **Tüüp** see sõnumitüüp, mis tuleks kuvada, kui kinnituse tüübiga seotud kohustuslikud väljad ei ole kinnitatud. Kui valite **Viga**, tühistatakse töökäsu töötsükli oleku uuendamine seniks, kuni seotud kohustuslikud väljad on töökäsus uuendatud.

    - Valikud **Hoolduse seisak**, **Hoolduse kontrollnimekiri**, **Tõrkesümptom**, **Tõrke põhjus** ja **Vigane valik** on seotud valikutega jaotises **Kohustuslik** lehel **Töökäsu tüübid** (**Varahaldus** \> **Seadistus** \> **Töökäsud** \> **Töökäsutüübid**). Nende kinnituste aktiveerimiseks peavad seotud valikud olema seadistatud töökäsu tüübile **Jah**.
    - Kui suvand **Hoolduse kontrollnimekiri** on seadistatud väärtuseks **Jah** töötsükli olekus, millesse töökäsk on uuendatud, tehakse kontroll, kas hoolduse kontrollnimekirja read, mis on märgistatud kui **Kohustuslik** on seadistatud kui **Kontrollitud** või **Pole rakendatav**. Kui ükski neist seadistustest ei ole kohustuslikel ridadel tehtud, kuvatakse töökäsu uuendamisel selle töötsükli olekusse teave, tõrge või hoiatusteade.
    - Kui suvand **Kooskõlastatud kulu** on seatud väärtusele **Jah**, et töötsükli olekus on töökäsku uuendatud, arvutatakse kooskõlastatud kulude kogusumma (st kulude kogusumma, mille juriidiline isik on kohustunud maksma) iga töökäsu töö jaoks. Kuvatakse teade, kui kooskõlastatud kulu summa on suurem kui 0 (null). Saate valida kulukohustuse tüübid, mis on toodud kiirkaardi **Kulukohustused** kaardil **Kulukontroll** lehel **Projektijuhtimise ja raamatupudamise parameetrid** (**Projektijuhtimine ja raamatupidamine** \> **Seadistus** \> **Projektijuhtimise ja raamatupidamise parameetrid**).
    - Kui suvandi **Hoolduse seisakud** väärtuseks on **Jah** töötsükli olekus, millesse töötkäsk on uuendatud, tehakse hoolduse seisakute kinnitamine töökäsuga seotud vara puhul. Kui hoolduse seisakute registreerimine on tehtud, kuid pole **Lõpetatud** registreerimist, kuvatakse teade, kui töökäsku värskendatakse selle elutsükli olekusse.
    - Kui standardse projekti seadistamine ei sisalda kõiki teie varahalduse seadistuse jaoks nõutud etappe, saate seadistada kasutaja määratletud projektietapid vahekaardil **Projektietapp** lehel **Projektijuhtimise ja raamatupidamise parameetrid**. Järgmisel illustratsioonil kuvatakse vahekaart **Projektietapp** lehel **Projektijuhtimise ja raamatupidamise parameetrid**.

    ![Leht projektietappide häälestamiseks eri projektitüüpide puhul.](media/10-setup-for-work-orders.png)

> [!NOTE]
> Kui töötsükli olek, mille värskendate töökäsuks on passiivne, kustutatakse töökäskudega seotud töölehed, kuid see pole veel sisestatud. Selline käitumine aitab tagada kasutamata teabe automaatse puhastamise. (Töötsükli olek on passiivne, kui selle suvand **Aktiivne** on seatud väärtusele **Ei** kiirkaardil **Üldine** lehel **Töökäsu töötsükli olek**.)
>
> Kui töötsükli olek on käsitsi seadustatud passiivseks, siis **ei** kustutata automaatselt töökäskudega seotud töölehti, kuid neid pole veel sisestatud. (Töötellimuse käsitsi inaktiveerimiseks valige **Varahalduse** \> **töötellimused** \> **kõik töötellimused** või aktiivsed **töötellimused.** Avage töökäsk ja aktiveerige vaade **Päis**. Valige kiirkaardil **Üldine** käsk **Redigeeri** ja määrake suvandi **Aktiivne** väärtuseks **Ei**.

## <a name="relations-among-work-order-lifecycle-models-work-order-types-and-work-order-lifecycle-states"></a>Seosed töökäsu elutsükli olekute, töökäsu elutsükli mudelite ja töökäsu tüüpide vahel

Töötsükli mudelid viitavad töövoogudele ja töötsükli olekud on töötsükli mudelis valitud järjekorras. Töötsükli mudelid seadistatakse töökäsu tüüpide puhul. Töökäsutüübid määravad töövoogude ja tööprotsesside suuruse või ulatuse. Näiteks **Hooldus**, mis on standardne töökäsutüüp, võib olla seotud töökäsu töötsükli mudeliga, millel on palju töötsükliolekuid. Seevastu võib teil olla töökäsu tüübiks **Korrigeeriv**, mida kasutatakse töökäskude puhul, mida pole plaanitud, või töökäskude puhul, mille töö on lõpetatud enne, kui töö on tehtud kiireloomulise olukorra tõttu. See töökäsutüüp võib olla seotud töökäsu töötsükli mudeliga, millel on ainult mõned töötsükliolekud.

Tüüpide kasutamise põhjus on, et kui tüüp on määratletud näiteks töökäsul või varal, määratletakse automaatselt sellega seotud tööprotsessid (töötsükliolekud). Lisateavet töökäsutüüpide seadistamise kohta vt [Töökäsutüübid](../setup-for-work-orders/work-order-types.md).

> [!NOTE]
> Töötsükliolekud, töötsükli mudelik ja tüübid rakenduvad funktsionaalsetele asukohtadele, varadele ja hooldusnõuetele lisaks töökäskudele.

Järgmine illustratsioon näitab seost töökäskude tüüpide, töötsükli mudelite ja töötsükliolekute vahel.

![Töökäsu tüübi lehe ja töökäsu töötsükli mudelite lehe võrdlus.](media/11-setup-for-work-orders.png)

## <a name="work-order-lifecycle-models"></a>Töökäsu töötsükli mudelid

Pärast seda, kui olete loonud oma töökäskude jaoks nõutavad tääkäsu töötsükliolekud, saab neid jagada töökäsu töötsükli mudeliteks. Peate looma vähemalt ühe standardse töötsükli mudeli.

1. Valige **Varahaldus** \> **Seadistus** \> **Töökäsud** \> **Töötsükli mudelid**.
2. Valige uue töökäsu töötsükli mudeli loomiseks **Uus**.
3. Sisestage väljale **Elutsükli mudel** elutsükli mudeli ID.
4. Väljale **Nimi** sisestage nimi.

    Kiirkaardil **Üksikasjad** kuvab **Elutsükli olekud** selles elutsükli mudelis valitud elutsükli olekute arvu. Väljal **Töökäsu tüübid** kuvatakse töökäsu tüüpide arv, mis kasutavad seda töötsüklimudelit.

5. Kiirkaardil **Elutsükli olekud** valige need elutsükli olekud, mis tuleks elutsükli mudelisse kaasata.

    - Elutsükli oleku lisamiseks elutsükli mudelisse, valige see jaotises **Järelejäänud elutsükli olekud** ja seejärel valige paremnool ![paremnool.](media/12-setup-for-work-orders.png) et teisaldada see valitud jaotisesse **Elutsükli valitud olekud**.
    - Et lisada kõik saadaolevad elutsükli olekud elutsükli mudelisse valige **Vali kõik saadaolevad etapid** nupp ![Vali kõik saadaolevad etapid.](media/13-setup-for-work-orders.png). Kõik elutsükli olekud teisaldatakse jaotisesse **Valitud elutsükli olekud**.
    - Elutsükli oleku lisamiseks elutsükli mudelisse, valige see jaotises **Järelejäänud elutsükli olekud** ja seejärel valige paremnool ![paremnool.](media/14-setup-for-work-orders.png) et teisaldada see valitud jaotisesse **Elutsükli järelejäänud olekud**.

6. Valige **Töötsükli oleku värskendused**, et määratleda, millised töötsükli olekud saavad valitud töötsükli olekut järgida.
7. Valige kiirkaardi **Uuendused** väljal **Plaanitud olek** töötsükli olek, mis tuleks alati valida töökäsule, mille jaoks olete lõpetanud töökäsu planeerimise, sõltumata töökäsu eelnevast töötsükli olekust.
8. Valige väljal **Plaanimata töötsükli olek** töötsükli olek, mis tuleks töökäsule alati valida, kui töökäsu graafik on kustutatud.
9. Salvestage töökäsu töötsükli mudel.

![Töökäsu töötsükli mudelite leht.](media/15-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]