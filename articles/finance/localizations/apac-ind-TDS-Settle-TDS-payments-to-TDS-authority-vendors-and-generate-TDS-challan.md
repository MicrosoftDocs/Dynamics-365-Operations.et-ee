---
title: TDS-i maksete tasakaalustamine TDS-i halduri hankijatele ja TDS-i challani loomine
description: See teema kirjeldab, kuidas tasakaalustada allika (TDS) maksetes maha arvatud maksu TDS-i halduri hankijatele.
author: kailiang
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 5b77985a75d2930267cf94d6f218d53b47e6e705
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023185"
---
# <a name="settle-tds-payments-to-tds-authority-vendors-and-generate-tds-challan"></a>TDS-i maksete tasakaalustamine TDS-i halduri hankijatele ja TDS-i challani loomine

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas tasakaalustada allika (TDS) maksetes maha arvatud maksu TDS-i halduri hankijatele.

1. Avage **Ostureskontro \> Maksed \> Hankija maksete tööleht**.

    [![Hankija maksetööleht](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)

2. Valige **Hankija makse tööleherea** lehel **Uus** et luua töölehel uus rida.
3. Valige **Konto** väljal TDS-i asutuse hankija, kellelt TDS-maksed tasakaalustada.
4. Valige **Tasakaalustuskanded** et avada **Tasakaalustuskanded** leht, kus saate vaadata TDS-i kandeid TDS-i autoriseeritud hankijate jaoks.

    Tasakaalustusperioodi tasakaalustatud TDS-kanded kuvatakse järgmisel viisil:

    - TDS-kanded, mille hinnangukategooria olemus on **Ettevõte** kuvatakse ühe kandereana.
    - TDS-kanded, mille hindamiskategooria olemus on **HUF**, **Firma**, **individduaal**, **AOP**, **BOI**, **Kohalik asutus**, või **Teised** kuvatakse ühe kandereana.
    - Väljal **Summa** kuvatakse TDS-i kogusumma, mis tuleb tasuda TDS-i asutuse hankijale.

5. Valige **Kinnipeetava maksu kanded**, et vaadata erinevaid TDS-i kandeid, mis kaasatakse tasakaalustuskirjesse. Saate vaadata kõigi sellel lehel oleva tasakaalustusperioodi tasakaalustusprotsessi kaasatud TDS-kannete tükeldamist.
6. Märkige **Ülevaade** vahekaardil märkeruut **Märk** TDS-kannete tasakaalustamiseks TDS-i asutuse hankijaga.

    Vahekaarddil **Ülevaade** kuvatakse iga avatud TDS-kande kohta järgmine teave:

    - **Kuupäev** – lisage kande kuupäev.
    - **Kviitung** – Kviitungi number.
    - **Allikas** – Moodul, kus TDS-kanne loodi.
    - **Hankija/klient** – hankija- või kliendikood, millest TDS maha arvatakse.
    - **Mahaarvatud isiku/osapoole nimi** – selle hankija või kliendi nimi, kellelt TDS maha arvatakse.
    - **Hindaja olemus** – selle hinnangukategooria olemus, kuhu mahaarvatav kuulub.
    - **Summa** - arvele sisestatud summa, mida TDS on arvutanud.
    - **Maksusumma** – TDS-i maksusumma, mis kande jaoks arvutatud.

    > [!NOTE]
    > Tühjendage **Märke** ruut kõikide TDS-kannete puhul, mida ei peaks TDS-i asutuse hankijaga tasakaalustama.

    Vahekaardil **Üldine** kuvatakse **PAN** väljal mahaarvatud kauba püsikonto number (PAN). Väljal **Kuupäev** kuvatakse TDS-i arvutuse kuupäev ja väljal **Väärtus** kuvatakse kogu protsent, mida kasutati TDS-i arvutamiseks.

7. Valige **Kanne** et vaaddata TDS-kande kandekirjeid.
8. Sulgege leht.
10. Valige **Kinnipeetava maksu komponendid** et avada **kinnipeetava maksu komponentide** leht, kus saate vaadataTDS-i, mis arvutati konkreetse TDS-i maksukoodi kohta.

    Vahekaardil **Ülevaade** näitab **maksukomponendi** väljal TDS-i maksukomponenti, mida kandes kasutati. Väljal **Summa** kuvatakse TDS-i summa, mis arvutati TDS-i maksukomponendi jaoks baasvaluutas. Väljal **Akumuleeritud summa** kuvatakse kõigi tasakaalustatud kannete TDS-i maksukomponendi jaoks arvutatud TDS-i kogusumma.

    Vahekaardil **Summa** jaotises **Vaikevaluuta** kuvatakse TDS-i maksukomponendi jaoks arvutatud TDS-summa vaikevaluutas. Jaotises **Paralleelvaluuta** kuvatakse summa paralleelvaluutas.

11. Sulgege **Kinnipeetava maksu komponentide** leht.
12. **Avatud kande redigeerimise** lehel **Summa** väljal pange tähele, et tasakaalustusperioodiks TDS-i asutuse hankijaga tasakaalustatav kogusumma uuendatakse.
13. Erinevate TDS-i tasakaalustusperioodide TDS-i tasakaalustuskannete tasakaalustamiseks TDS-i asutuse hankijaga märkige **Märgi** ruut kannete jaoks.
14. Sulgege **Avatud kannete redigeerimine** leht.

    > [!NOTE]
    > Kui kinnipeetava maksu kannete lehel on tasakaalustamiseks valitud vaid mõned kanded, uuendatakse valitud kannete TDS-i kogusumma **Kinnipeetava maksu kanded** **Redigeerimise** lehel **Aavatud kande redigeerimise** lehel. Parandussumma uuendatakse töölehe real ja avatud **Töölehe kande** lehel ja **Avatud kannete redigeerimine** leht on suletud.

    **Töölehe kande** lehel näitab **Deebet** väli TDS-i asutuse hankijale makstavat kogusummat.

15. Sisestage vastaskonto üksikasjad.

    > [!NOTE]
    > Kui TDS-kannetel on erinevad maksukonto numbrid (TAN-id), luuakse tööleheread TAN kohta **töölehe kande** lehel.

16. **Maksetasu** vahekaardil **Tasu ID** väljal valige tasu ID, mille tasu tüüp on **Intress** või **Teised** et nõuda maksetasu hilinenud maksete eest, mis on tehtud TDS-i asutuse hankijale.

    Vahekaardi **Maksuteave** jaotises **Ettevõtte teave** väljal kuvatakse **Nimi** väljal ettevõtte nimi. Jaotises **Kinnipeetav maks** kuvatakse väljal **Maksukonto number (TAN)** kandereaga seotud kinnipeetava maksu kood.

17. Kinnitage ja sisestage tööleht.
18. Valige **Kinnipeetav maks \> Challani teave** kande challani üksikasjade sisestamiseks.

    Väljal **Kviitung** kuvatakse TDS tehingukande kviitungi number.
    
19. Valige **TDS deponeeritud raamatukanne** märkeruut, kui TDS-i summa hoiustatakse raamatukirjet kasutades.
20. Sisestage **Challani numbri** väljale chalani number, mida kasutatakse makse maksmiseks TDS-i maksu hankijale.
21. Väljale **Kuupäev** sisestage kuupäev.
22. Valige väljal **Panga nimi** panga nimi, mille kohta tuleb TDS-i maksu hankijale makstav TDS-i summa deponeerida. See väli loetleb kõik pangakontod, mis seadistati TDS-i asutuse hankija jaoks väljal **Ostureskontro \> Kõik hankijad \> Seadista \> Pangakontod**.
23. Väljale **BSR-kood** sisestage panga basic Statistical Return (BSR) kood.
24. Sulgege leht.

### <a name="example"></a>Näide

Periood 04/01/2009 tasakaalustatakse **Rent** TDS-i komponendigrupi jaoks perioodilise TDS-i tasakaalustusprotsessi abil. TDS-i kogusumma 141 625.00 sisestatakse TDS-i tasakaalustusperioodi jooksul TDS-i hankija kontole. Seda summat saate vaadata **Kogusumma** väljal **Avatud kannete redigeerimise** TDS-i asutuse hankija lehel.

Kui valite **kinnipeetava maksu kanded** et vaadata erinevaid TDS-i kandeid, mis perioodi jooksul tasakaalustati, kuvatakse järgmine teave.

| TDS summa |
|------------|
| 16,995.00  |
| 22,660.00  |
| 28,325.00  |
| 16,995.00  |
| 28,325.00  |
| 16,995.00  |
| 11,330.00  |

Valige **Kinnipeetava maksu komponendid** et avada kinnipeetava maksu komponentide leht, kus saate vaadataTDS-i, mis arvutati konkreetse TDS-i maksukoodi kohta. Näiteks valite **Kinnipeetava maksu komponentide** TDS-i summa jaoks 16 995.00. Kuvatakse kande komponendi kohta arvutatud maksusumma.

| Maksukomponent | Summa    | Akumuleeritud summa |
|---------------|-----------|--------------------|
| TDS           | 1,5000.00 | 125,000.00         |
| Lisatasu     | 1,500.00  | 12,500.00          |
| PE-Cess       | 330.00    | 2,750.00           |
| SHE Cess      | 165.00    | 1,375.00           |

Kui valisite ainult TDS summa 16 995.00, 22 660.00, ja 2 8325.00 tasakaalustamiseks, kuvatakse **Kinnipeetava maksu kannete lehel** tasakaalustuse kogusumma **67 980.00** lehe **Parandus** väljal **Avatud kande redigeerimise**. Kui see kanne on tasakaalustamiseks märgitud ja **avatud kannete redigeerimise** leht on suletud, kuvatakse **67 980.00** väljal **Deebet** **Töölehe kande** lehel.

Nüüd saate sisestada töölehe ja luua TDS-challani.

### <a name="adjustment-of-advance-payments-that-are-made-to-tds-authority-vendors"></a>TDS-i asutusele hankijatele tehtud ettemaksete korrigeerimine

TDS-i asutuse hankijale tegelikuks makseks tehtud ettemakse korrigeerimiseks minge hankijatele **Ostureskonto \> Hankijad \> Kõik hankijad \> Kannete redigeerimine**. Kui tegelik makse, mis tehakse, ületab ettemaksu, luuakse kande jaoks kaks challani numbrit. Kuid TDS-päringus näidatakse ainult esimest chalani numbrit.
