---
title: Hooldustöö tüübid, kategooriad, variandid, kaubandused ja kontroll-loendid
description: Selles teemas kirjeldatakse hooldustöö tüübi kategooriaid ja hooldustöö tüüpe, hooldustöö tüübi variante, hooldustööde vahetusi ja hoolduse kontrollnimekirju varahalduses
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetJobTypeDefaultForecast, EntAssetJobTrade, EntAssetJobTypeDefaultCopy, EntAssetChecklistVariableValueLookup, EntAssetChecklistTemplateCreate, EntAssetJobVariant, EntAssetJobTypeDefaultReference, EntAssetJobTypeDefaultChecklist, EntAssetJobTypeDefault, EntAssetJobType, EntAssetJobTypeDefaultChecklistCopy, EntAssetChecklistTemplate, EntAssetJobTypeDefaultDescription, EntAssetJobTypeLookup, EntAssetJobTypeDefaultToolCopy, EntAssetJobTypePreviewPart, EntAssetJobTypeDefaultTool, EntAssetJobTypeDefaultForecastCopy, EntAssetChecklistTemplateLookup, EntAssetJobGroup, EntAssetChecklistVariable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 252829ac2d070833023f1b49aef615cc376f37b6
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344636"
---
# <a name="maintenance-job-types-categories-variants-trades-and-checklists"></a>Hooldustöö tüübid, kategooriad, variandid, kaubandused ja kontroll-loendid

[!include [banner](../../includes/banner.md)]

Igale varale on lisatud vara tüüp. Varatüübid määratlevad hooldustööde tüübid (ja seetõttu ka hooldustööd), mida saab varadega teostada. Kui loote töökäsu, peate valima hooldustöö tüübi. Saate valida ainult need hooldustöö tüübid, mis on seotud vara jaoks kasutatava vara tüübi seadistamisega.

Varade graafilise ülevaate ja hooldustööde tüüpide ning nende seotuse kohta töökäskudega vt [Töö asukohad ja varad](../overview/functional-locations-and-objects.md).

Hooldustöö tüübi variante saab seadistada hooldustöö tüübi järgi. Hooldustöö tüübi variandid määratlevad töö tüübi variatsioonid, nt suurus (väike, keskmine või suur), perioodid (nädal, kaks nädalat, üks kuu või kolm kuud) ja konfiguratsioonid (madal standard, paindlik või suur jõudlus).

Hooldustöö vahetused pakuvad teavet vahetuste, nt mehaaniliste, elektriliste ja hüdrauliliste vahetuste kohta. Kompetentsinõudeid saab seadistada hooldustöö vahetuse järgi. Kõiki hooldustöö vahetusi saab kasutada kõikide hooldustöö tüüpide puhul. Hooldustöö tüübi valimine ja/või hooldustöö vahetus töökäsus on valikuline.

Iga hooldustöö tüübi jaoks saab luua hooldustöö tüübi seadistuse variatsioone. Näiteks kui teil on hooldustöö nimega **Teenindus**, saate luua hooldustöö tüübile järgmisi variatsioone: **Veoautod 30 000 km**, **Autod 30 000 km** ja **Kaubikud 30 000 km**.

Hooldustöö tüüpide kategooriaid kasutatakse hooldustööde rühmade kogumiseks ülevaate saamiseks. Hooldustöö tüüpide kategooriate näideteks võivad olla **Kalibreerimine**, **Kontroll**, **Remont** ja **Seadistamine**.

Hoolduse kontrollnimekirjade seadistamiseks kasutatakse hooldusnimekirjade malle ja hooldusnimekirjade muutujaid. Hoolduse kontrollnimekirjad on loodud hooldustööde tüüpide järgi ja neid kasutatakse töökäskude puhul.

Esmalt seadistage vajalikud hooldustööde tüübi kategooriad, hooldustöö tüübi variandid ja hooldustööde vahetused. Seejärel looge hooldustööde tüübid. Lõpuks looge lehel **Hooldustöö tüübi vaikeseaded** hooldustöö tüüpide kõik variatsioonid, mida teie seadme jaoks vaja on. Sellel lehel saate seadistada ka hooldustööde tüüpide kombinatsiooni prognoose, hoolduse kontrollnimekirju ja tööriistu.

> [!NOTE]
> Hooldustöö tüüp võib olla seotud ainult ühe hooldustöö tüübi kategooriaga.

## <a name="create-a-maintenance-job-type-category"></a>Looge hooldustöö tüübi kategooria

1. Valige **Varahaldus** \> **Seadistus** \> **Tööd** \> **Hooldustöö tüübi kategooriad**.
2. Valige suvand **Uus**.
3. Sisestage väljale **Hooldustöö tüübi kategooria** hooldustöö tüübi kategooria ID.
4. Väljale **Nimi** sisestage nimi.

    Pärast hooldustöö tüüpide kategooriate seostamist hooldustöö tüüpidega näitab väli **Töö tüübid** selle hooldustöö tüübi kategooriaga seotud hooldustöö tüüpide arvu.

![Hooldustöö tüübi kategooriate leht.](media/01-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-type-variant"></a>Looge hooldustöö tüübi variant

1. Valige **Varahaldus** \> **Seadistus** \> **Tööd** \> **Hooldustöö tüübi variandid**.
2. Valige suvand **Uus**.
3. Sisestage väljale **Hooldustöö tüübi variant** hooldustöö tüübi variandi ID.
4. Väljale **Kirjeldus** sisestage kirjeldus.
5. Vahekaardil **Hooldustööde tüübid** valige hooldustöö tüübi lisamiseks **Lisa**.
6. Väljal **Hooldustöö tüüp** valige hooldustöö tüüp.
7. Hooldustöö tüübi variandile hooldustöö tüüpide lisamiseks korrake punkte 5–6.

    Vahekaardil **Üksikasjad** näitab väli **Töö tüübid** hooldustöö tüüpide arvu, mis on lisatud sellele hooldustöö tüübi variandile.

![Hooldustöö tüübi variantide leht.](media/02-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-trade"></a>Looge hooldustöö tüübi vahetus

1. Valige **Varahaldus** \> **Seadistus** \> **Tööd** \> **Hooldustöö tüübi vahetus**.
2. Valige suvand **Uus**.
3. Sisestage väljale **Vahetus** hooldustöö tüübi vahetuse ID.
4. Väljale **Kirjeldus** sisestage kirjeldus.
5. Vahekaardil **Oskused** valige hooldustöö vahetusega seotud uue oskuse lisamiseks **Lisa**.
6. Väljal **Oskus** valige oskus.
7. Väljal **Tase** valige oskuse tase.
8. Kui soovite hooldustöö vahetusse lisada rohkem oskusi, korrake juhiseid 5–7.

    Vahekaardil **Üksikasjad** näitab väli **Oskused** oskuste arvu, mis on lisatud sellele hooldustöö vahetusele.

9. Vahekaardil **Serdid** valige hooldustöö vahetusega seotud serdi lisamiseks **Lisa**.
10. Väljal **Serdi tüüp** valige sert.
11. Kui soovite hooldustöö vahtusse lisada rohkem serte, korrake juhiseid 9–10.

    Vahekaardil **Üksikasjad** näitab väli **Serdid** sertide arvu, mis on lisatud sellele hooldustöö vahetusele.

![Hooldustöö tüübi vahetuse leht.](media/03-setup-for-work-orders.png)

## <a name="create-a-maintenance-checklist-variable"></a>Looge hoolduse kontrollnimekirja muutuja

Kui loote hooldustööde vaiketüübis hoolduse kontrollnimekirja read, peate valima hoolduse kontrollnimekirja tüübi. **Muutuja** on üks hoolduse kontrollnimekirja tüüp. Seda kasutatakse hoolduse kontrollnimekirja rea vahemiku võimaliku tulemuse määratlemiseks, mis on seotud töökäsu reaga. Muutuja võimaldab teil luua eelnevalt määratletud tulemuste kogumi ilma täpset mõõtmist tegemata.

**Näide 1:** Saate muuta õlitaset, määrates kolm väärtust: **Tase liiga kõrge**, **Tase liiga madal** ja **Tase sobiv**. Saate iga väärtuse jaoks määrata, kas tase on **Läbitud**, **Mitteläbitud** või **Puudub**.

**Näide 2:** Kulumise hindamiseks saate teha seadme visuaalse kontrolli.

1. Valige **Varahaldus** \> **Seadistus** \> **Hoolduse kontrollnimekirjad** \> **Hoolduse kontrollnimekirja muutujad**.
2. Valige suvand **Uus**.
3. Väljale **Muutuja** sisestage hoolduse kontrollnimekirja muutuja ID.
4. Väljale **Nimi** sisestage nimi.
5. Vahekaardil **Üldine** valige **Lisa**, et lisada muutujale rida.

    Järjekorranumber sisestatakse automaatselt väljale **Reanumber**. Kui olete kõik read lisanud, saate vastavalt vajadusele muuta ridade numbreid. Kui valite rea ja vajutate siis **nooleklahvi alla**, sisestatakse järjekorranumber järgmisele reale automaatselt.

6. Väljale **Väärtus** sisestage uus väärtuse kirjeldus.
7. Väljal **Tulemus** valige rea tulemus.

![Hoolduse kontrollnimekirja muutujate leht.](media/04-setup-for-work-orders.png)

## <a name="create-a-maintenance-checklist-template"></a>Looge hoolduse kontrollnimekirja mall

Hoolduse kontrollnimekirja malle saab kasutada tavalise tööülesandekogumina, mida töötaja peab töökäsu korrektseks täitmiseks täitma. Mallidele viidatakse hooldustööde vaiketüübi hoolduse kontrollnimekirjade ridadel. Mallidele saab viidata mitme hooldustöö tüübi vaikeridade kaudu. Seetõttu saate hõlpsalt uuesti kasutada tavalise hoolduse kontrollnimekirja ülesannete komplekti. Hoolduse kontrollnimekirja mallide näideteks on üldised ohutusjuhised ning loetelu elementidest ja tingimustest, mida tuleb kontrollida konkreetse pumba või samalaadsete konveierilindi mudelite korral.

1. Valige **Varahaldus** \> **Seadistus** \> **Hoolduse kontrollnimekirjad** \> **Hoolduse kontrollnimekirjade mallid**.
2. Valige suvand **Uus**.

    Malli ID sisestatakse automaatselt väljale **Hoolduse kontrollnimekirja mall**.

3. Sisestage väljale **Nimi** hoolduse kontrollnimekirja malli nimi.
4. Vahekaardil **Hoolduse kontrollnimekirja read** valige malli rea lisamiseks **Lisa**.

    Järjekorranumber sisestatakse automaatselt väljale **Reanumber**. Kui olete kõik read lisanud, saate vastavalt vajadusele muuta ridade numbreid. Kui valite rea ja vajutate siis **nooleklahvi alla**, sisestatakse järjekorranumber järgmisele reale automaatselt.

5. Väljal **Tüüp** valige hoolduse kontrollnimekirja rea tüüp. Iga hoolduse kontrollnimekirja tüübi korral kuvatakse vahekaardil **Rea üksikasjad** seotud välju. Saadaval on järgmised väärtused:

    - **Tekst** – real on tekst, mis kirjeldab, mida teha. Kasutage seda hoolduse kontrollnimekirja tüüpi, kui soovite, et töötaja midagi kontrolliks või üle vaataks, kuid te ei oota konkreetset (mõõdetavat) tulemust. Pärast selle tüübi valimist sisestage väljale **Nimi** nimi või pealkiri. Väljale **Juhised** sisestage kirjeldus, mida tuleb teha. Kui see samm on hoolduse kontrollnimekirja jaoks kohustuslik, määrake suvandi **Kohustuslik** väärtuseks **Jah**.
    - **Päis** – rida kasutatakse pealkirjana selle all asuvate hoolduse kontrollnimekirjade ridade rühmitamiseks. See tüüp on kasulik, kui teil on mitu hoolduse kontrollnimekirja rida, mida saab jagada konkreetseteks tööaladeks. Päised annavad ülevaate töötajale, kes täidab hoolduse kontrollnimekirja, millel on palju hoolduse kontrollnimekirja ridu. Pärast selle tüübi valimist sisestage väljale **Nimi** kirjeldav nimi.
    - **Mall** – rida kasutatakse olemasolevale mallile viitamiseks. Pärast selle tüübi valimist sisestage väljale **Nimi** malli nimi. Väljal **Mall** valige mall.
    - **Muutuja** – rida kasutatakse vahemiku võimaliku tulemuse määratlemiseks. Hoolduse kontrollnimekirja muutujate seadistamise kohta lisateabe saamiseks lugege jaotist[Hoolduse kontrollnimekirja muutuja loomine](#create-a-maintenance-checklist-variable). Pärast selle tüübi valimist sisestage väljale **Nimi** muutuja kirjeldav nimi. Väljal **Muutuja** valige muutuja. Väljale **Juhised** sisestage kirjeldus, mida tuleb teha. Kui see samm on hoolduse kontrollnimekirja jaoks kohustuslik, määrake suvandi **Kohustuslik** väärtuseks **Jah**.
    - **Mõõtmine** – rida kasutatakse konkreetse mõõtmise registreerimiseks. Saate seadistada mõõtmise, mis peaks olema seotud eelnevalt määratletud loenduriga. Pärast selle tüübi valimist sisestage väljale **Nimi** malli nimi. Kui see samm on hoolduse kontrollnimekirja jaoks kohustuslik, määrake suvandi **Kohustuslik** väärtuseks **Jah**. Kui soovite mõõtejoont kasutada loendurina, valige loendur väljal **Loendur**. Seotud väli **Ühik** värskendatakse seejärel automaatselt. Kui olete valinud loenduri, valige värskendusmeetod väljal **Väärtus**. Väljadel **Min. väärtus** ja **Maks. väärtus** sisestage lubatud väärtusvahemik. Väljale **Juhised** sisestage kirjeldus, mida tuleb teha.

        > [!NOTE]
        > Kõiki **Mõõtmed** tüüpi ridu, millel pole loenduri seadistust, käsitletakse iseseiva mõõtmise registreerimisena, millele varahalduses automaatne järelkontroll puudub. Samuti, kui töökäsuga seotud varal pole valitud loenduritüüp, käsitletakse hoolduse kontrollnimekirja ülesannet iseseisva mõõtmisena. Loenduri väärtust saab mitu korda muuta. Seda ei postitata enne kui [töökäsu töötsükli oleks](work-order-lifecycle-states.md) on muudetud olekuks kus, suvandi **Protsessi hoolduse kontrollnimekiri** seadeks on määratud **Jah**.

    Vahekaardil **Üksikasjad** väljal **Kontrollid** kuvatakse teie malli kontrollnimekirja ridade arv. See arv sisaldab olemasolevas mallis sisalduvaid ridu, millele olete oma mallis viidanud.

![Hoolduse kontrollnimekirja mallide leht.](media/05-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-type"></a>Looge hooldustöö tüüp

1. Valige **Varahaldus** \> **Seadistus** \> **Tööd** \> **Hooldustöö tüübid**.
2. Valige suvand **Uus**.
3. Sisestage väljale **Hooldustöö tüüp** hooldustöö tüübi ID.
4. Väljale **Nimi** sisestage nimi.

    Vahekaardil **Üksikasjad** kuvatakse hooldustöö tüübi variantide, oskuste, sertide, järgnevate tööde ja vara tüüpide ülevaade Väljal **Ridade seadistamine** kuvatakse selle hooldustöö tüübi jaoks seadistatud hooldustöö tüübi vaikeridade arv. Väljal **Varad** kuvatakse aktiivsete varade arvu, mis seda hooldustöö tüüpi kasutavad.

5. Vahekaardil **Üldine** väljal **Hooldustöö tüübi kategooria** valige hooldustöö tüübi kategooria.
6. Seadke suvandi **Hoolduskatkestuse tegevused** väärtuseks **Jah**, kui hooldustöö tüüp nõuab enne töö alustamist seadme hoolduspeatust.
7. Vahekaardil **Kirjeldus** sisestage hooldustöö tüübi kirjeldus.
8. Vahekaardil **Hooldustöö tüübi variandid** saate lisada hooldustöö tüübile variante.
9. Vahekaartidel **Vajalikud oskused** ja **Vajalikud serdid** saate lisada hooldustöö tüübile oskusi ja serdinõudeid.
10. Kui järgmiseks tuleb läbi viia konkreetne hooldustöö tüüp, lisage see vahekaardile **Järgnevad tööd**. Samuti saate seadistada hooldustöö tüübi variandi ja vahetuse, mis on seotud hooldustöö tüübiga. Kui järgnev töö peaks algama kindel arv päevi enne või pärast seda, kui seda hooldustöö tüüpi kasutav töö on alustatud, sisestage väljale **Viivitus päevade järgi** päevade arv. Positiivsed numbrid tähistavad päevi pärast seotud töö algust ja negatiivsed numbrid tähistavad päevi enne seotud töö kavandatud algust. Näiteks kui sisestate **5**, algab järgnev töö viis päeva pärast hooldustöö tüübiga seotud töö algust. Kui sisestate **-3**, algab järgnev töö kolm päeva enne hooldustöö tüübiga seotud töö kavandatud algust.

    > [!NOTE]
    > Kui lisate rohkem kui ühe hooldustöö tüübi rea, näitab ridade järjestus nende täitmise järjekorda. Järjestus algab loendi ülaosast.

11. Vahekaardil **Vara tüübid** saate hooldustöö tüübile lisada vara tüüpe.

![Hooldustöö tüüpide leht.](media/06-setup-for-work-orders.png)

## <a name="create-maintenance-job-type-default-lines-and-related-forecasts-maintenance-checklists-tools-description-and-attachments"></a>Looge hooldustöö tüübi vaikeread ja nendega seotud prognoosid, hoolduse kontrollnimekirjad, tööriistad, kirjeldus ja manused

1. Valige **Varahaldus** \> **Seadistus** \> **Tööd** \> **Hooldustöö tüübi vaikeväärtused**.

    või

    Valige **Varahaldus** \> **Seadistus** \> **Tööd** \> **Hooldustöö tüübid**, valige hooldustöö tüüp ja seejärel valige **Hooldustöö tüübi vaikeväärtused**.

2. Valige suvand **Uus**.
3. Väljadel **Töö asukoht**, **Vara tüüp**, **Tootja**, **Mudel** ja **Vara** valige sobivad väärtused, sõltuvalt sellest, kui konkreetne hooldustöö tüüp peaks olema.
4. Valige väljal **Hooldustöö tüüp** hooldustöö tüüp, kui seda ei valitud automaatselt.
5. Väljadel **Hooldustöö tüübi variant** ja **Vahetus** valige hooldustöö tüübi variant ja hooldustöö vahetus vastavalt vajadusele.
6. Valige **Prognoos**.
7. Lehel **Hooldustöö tüübi vaikesätete prognoos** saate prognoosida tunde, üksusi ja kulusid. Vastavatel vahekaartidel valige **Lisa** ja tehke valikud, et luua hooldustöö tüübi jaoks vajalikud prognoosid.
8. Vahekaardil **Üksuse prognoos** saate valida varude mõõtmed, mida tuleks kuvada üksuse real. Valige **Varud** \> **Mõõtmed**, valige kuvatavad mõõtmed, seadke suvandi **Seadistuse salvestamine** väärtuseks **Jah** ja seejärel valige **OK**.
9. Vahekaardil **Üksuse prognoos** valige **Üksus kus kasutatakse**, et näha ülevaadet selle kohta, kus valitud real üksust varahalduses kasutatakse seoses varade, hooldustöö tüübi vaikesätte, varuosade ja töökorraldustega. 

    Vahekaardil **Hooldusprognooside kogusummad** kuvatakse prognooside kogusumma ülevaade. See ülevaade sisaldab loodud tundide koguarvu ja prognoosiridu.

    > [!NOTE]
    > Prognoosi seadistuse kopeerimiseks teiselt hooldustöö tüübilt valige **Kopeeri prognoos** ja seejärel valige hooldustöö tüüp, millest seadistus kopeerida.

11. Oma muudatuste salvestamiseks valige **Salvesta**.
12. Sulgege leht **Hooldustöö tüübi vaikesätete prognoos**, et naasta lehele **Hooldustöö tüübi vaikesätted** page.
13. Valige **Hoolduse kontrollnimekiri**.
14. Lehel **Hooldustöö tüübi vaikesätete kontrollnimekiri** saate lisada hoolduse kontrollnimekirja read valitud hooldustöö tüübi vaikesätetele. Vahekaardil **Hoolduse kontrollnimekirja read** valige **Uus**, et lisada hoolduse kontrollnimekirja rida.

    Reanumbrid sisestatakse väljale **Reanumber** automaatselt, et näidata hooldusnimekirja ridade järjestust. Ridade numbreid saate vastavalt vajadusele muuta. Pärast esimese hoolduse kontrollnimekirja rea loomist valige see rida ja vajutage rea alla lisamiseks klahvi **Allanool**. Teise võimalusena võite valida hoolduse kontrollnimekirja rea ja seejärel valida **Uus**. Sel juhul lisatakse valitud hoolduse kontrollnimekirja rea kohale uus rida.

15. Valige väljal **Tüüp** rea tüüp ja lisage seejärel hoolduse kontrollnimekirja tüübiga seotud teave. Saadaolevate tüüpide ja nendega seotud väljade kirjelduse leiate jaotisest [Hoolduse kontrollnimekirja malli loomine](#create-a-maintenance-checklist-template).

    > [!NOTE]
    > Hoolduse kontrollnimekirja seadistuse kopeerimiseks teiselt hooldustöö tüübilt valige **Kopeeri hoolduse kontrollnimekiri** ja seejärel valige hooldustöö tüüp, millest seadistus kopeerida.
    >
    > Malli saate hõlpsalt luua olemasoleva hoolduse kontrollnimekirja põhjal. Seejärel saate malli uuesti kasutada mitmel hoolduse kontrollnimekirjal. Uus mall on aktiivse hoolduse kontrollnimekirja täpne koopia. Valige **Loo mall** ja seejärel sisestage malli nimi. Olemasoleva hooldusnimekirja asendamiseks ühe reaga, mis viitab uuele mallile, seadke suvandi **Asendamine** väärtuseks **Jah**. Malli sisu saate vaadata üksikasjade lehel **Hooldusnimekirjade mallid**.

16. Oma muudatuste salvestamiseks valige **Salvesta**.
17. Naaske lehele **Hooldustöö tüübi vaikesätted**.
18. Valige **Tööriistad**.
19. Lehele **Hooldustöö tüübi vaikesätete tööriistad** saate lisada tööriistad (ressursid), mida tuleks hooldustöö tüübi jaoks kasutada. Valige **Uus** ja seejärel valige tööriist väljal **Ressurss**.

    > [!NOTE]
    > Tööriista seadistuse kopeerimiseks teiselt hooldustöö tüübilt valige **Kopeeri tööriist** ja seejärel valige hooldustöö tüüp, millest seadistus kopeerida.

20. Oma muudatuste salvestamiseks valige **Salvesta**.
21. Naaske lehele **Hooldustöö tüübi vaikesätted**.
22. Valige **Töö kirjeldus**.
23. Valige lehel **Töö kirjeldus** käsk **Redigeerimine** ja lisage seejärel soovitud kirjeldus, mis on seotud valitud hooldustöö tüübi vaikeseadega.
24. Kirjelduse salvestamiseks valige **Salvesta**.

    Kui lisate siia töökirjelduse, tühistab see kirjelduse, mis on hooldustöö tüübi jaoks lehel **Hooldustöö tüübid** seadistatud. Kui te siia töökirjeldust ei lisa, kasutatakse hooldustöö tüübi jaoks seadistatud kirjeldust. Kirjeldused kantakse automaatselt üle töökorraldustesse, mis kasutavad hooldustöö tüübi või hooldustöö tüübi vaikesätet.

25. Naaske lehele **Hooldustöö tüübi vaikesätted**.
26. Manuste seadistamiseks valitud hooldustöö tüübi vaikereal valige **Manusta dokumendid**. Manused, mis on seadistatud hooldustöö tüübi vaikereale, lisatakse automaatselt töökorralduse ridadele, mis kasutavad seda hooldustöö tüübi vaikerida.
27. Valige **Uus** ja valige siis dokumenditüüp.
28. Laadige dokument või fail üles.
29. Seadistage väljad lehel **Manused**. Manuse seadistus kasutab standardseid dokumendi seadistamise funktsioone.
30. Manuse salvestamiseks valige **Salvesta**.

    > [!NOTE]
    > Hooldustöö tüübi vaikerea manuseid prinditakse koos töökäskude aruandega ainult siis, kui manuste dokumenditüübid on valitud vahekaardil **Dokumenditüübid** lehel **Varahalduse parameetrid** (**Varahaldus** \> **Seadistamine** \> **Varahaldusparameetrid**). Manuste näideteks on juhised, mis selgitavad, kuidas täita konkreetset tööd või eelmääratud hoolduse kontrollnimekirja (kui te ei kasuta hooldustööde kontrollnimekirja funktsioone hooldustöö tüübi vaikeridade korral).

    Lehel **Hooldustöö tüübi vaikesätted** kuvatakse igal real prognoositud tundide arv ja üksuste, kulude, hoolduse kontrollnimekirjade ja tööriistade jaoks loodud ridade arv. Väljal **Varad** kuvatakse hooldustöö tüübi vaikereaga seotud aktiivsete varade arv.

31. Hooldustöö tüübi vaikesätte kopeerimiseks teise hooldustöö tüübi vaikesätteks valige hooldustöö tüübi vaikerida, millesse teine seadistus kopeerida, valige **Seadistuse kopeerimine** ja seejärel valige hooldustöö tüübi vaikesäte kopeerimiseks.
32. Selliste varade, hooldusplaanide või hoolduskordade nimekirja kuvamiseks, kus praegu kasutatakse hooldustöö tüübi vaikerida, valige rida ja seejärel **Kasutaja**.

![Hooldustöö tüübi vaikesuvandite leht.](media/07-setup-for-work-orders.png)

Kui süsteem valib saadaoleva hooldustöö tüübi vaikesätte, mida tuleks kasutada töökäskude real, põhineb valik vara ja sellega seotud vara tüübi seadistusel. Varahaldus läbib kõik hooldustöö tüübi vaikekirjed, mis on seotud vara tüübiga seotud hooldustöö tüübiga, et kontrollida võimalikku vastet. Varahaldus kontrollib alati kõige spetsiifilisemat kombinatsiooni esimesena. Teisisõnu, kõige spetsiifilisema kombinatsiooni leidmiseks kontrollib varahaldus kõigepealt võimalikku vastet väljale **Vahetus**. Kui vastet ei leita, otsib see vastet väljale **Hooldustöö tüübi variant**. Kui vastet ei leita, kontrollib see vastet väljadele **Hooldustöö tüüp** jne (**Vahetus**, siis **Hooldustöö tüübi variant**, siis **Hooldustöö tüüp**, siis **Vara**, siis **Mudel**, siis **Tootja** ja siis **Vara tüüp**). Kui vastet ei leita, kasutatakse vaikekirjet, kus on valitud ainult hooldustöö tüüp.

Projekti tegevuse ID seotakse automaatselt iga teie loodud hooldustöö tüübi vaikereaga. Projekti tegevus luuakse prognoosiprojektil, mis valitakse väljal **Hoolduse prognoosi projekt** vahekaardil **Varad** lehel **Varahalduse parameetrid**. Projekti tegevuse eesmärk on hallata töökäskudega seotud töötundide, üksuste ja kulude prognoose. Hooldustöö tüübi prognoosid kantakse automaatselt töökäsu reale ja need kopeeritakse prognoosiprojektist töökäsu projektile, mis luuakse töökäsu reale. Projekti tegevuse eesmärk on hallata töökäskudega seotud töötundide, üksuste ja kulude prognoose.

Hooldustöö tüübi vaikeviidete värskendamiseks korrapäraste intervallidega saate seadistada pakett-töö või saate seda tööd käsitsi käivitada. Pakett-töö loomiseks või käsitsi värskenduse käivitamiseks valige **Varahaldus** \> **Perioodiline** \> **Ennetav hooldus** \> **Hooldustöö tüübi vaikeviidete värskendamine**.

## <a name="overview-of-maintenance-job-types-that-are-related-to-assets"></a>Ülevaade varadega seotud hooldustöödest

Pärast vajalike hooldustöötüüpide vaikekombinatsioonide loomist saate lehel **Kõik varad** ülevaate konkreetse varaga seotud praeguse hooldustöö tüübi vaikeseadistusest. Ülevaade näitab kõikide hooldustöö tüüpide vaikekombinatsioone, mida saab vara jaoks valitud vara tüübil kasutada. Need kombinatsioonid hõlmavad kombinatsioone, millel on erinevad hooldustöö tüüpide variandid ja hooldustööde vahetused.

1. Valige **Varahaldus** \> **Ühine** \> **Varad** \> **Kõik varad** või **Aktiivsed varad**.
2. Valige loendist vara, et näha ülevaadet hooldustööde tüüpide kombinatsioonidest.
3. Toimingupaani vahekaardil **Üldine** rühmas **Seotud teave** valige **Hooldustööde tüübid**.

    Lehe **Vara hooldustööde tüübid** vasakul paanil kuvatakse loend kõigist valitud varaga seotud hooldustööde tüüpide kombinatsioonidest.

4. Valige hooldustööde tüüpide kombinatsioon, et näha hoolduse kontrollnimekirjade, prognooside ja tööriistadega seotud seadistusi. Jaotis **Üksikasjad** vahekaardil **Hooldustööde tüüpide vaikesätted** kuvatakse seotud hoolduse kontrollnimekirjad, prognoositud tunnid, üksused jne, mis on seotud valitud hooldustööde tüüpide kombinatsiooniga.
5. Valitud hooldustööde tüübi üksikasjade nägemiseks valige **Hooldustööde tüübid**.

![Vara hooldustöö tüüpide leht.](media/08-setup-for-work-orders.png)

## <a name="automatic-update-of-maintenance-job-type-forecasts"></a>Hooldustööde tüübi prognooside automaatne värskendamine

Varahalduses saate automaatselt värskendada hooldustöö tüübi prognoosides tehtud muudatusi tunni-, üksuse- ja muude kulude osas, mida on ajakohastatud teistes moodulites. Sel viisil saate aidata tagada, et teie hooldustööde tüübi prognoosides kasutatakse alati uusimaid kulusid.

1. Valige **Varahaldus** \> **Perioodiline** \> **Prognoos** \> **Hooldustöö tüübi prognoosi värskendamine**.
2. Dialoogiboksis **Hooldustöö tüübi prognoosi värskendamine** vahekaardil **Kaasatavad kirjed** saate vastavalt vajadusele lisada konkreetsete hooldustööde tüüpide valikuid. Valige **Filter** ja siis valige valikute tegemiseks **Vali**.
3. Vahekaardil **Taustal käitamine** saate vastavalt vajadusele seadistada automaatse värskenduse pakett-tööna.
4. Valige **OK**, et alustada prognoosi värskendamist.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]