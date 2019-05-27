---
title: Pakkumiskutse pakkumiste sisestamine ja võrdlemine ning lepingute määramine
description: See protseduur näitab, kuidas sisestada pakkumiskutsele (RFQ) vastuseid, pakkumisi hinnata ja võrrelda ning seejärel määrata leping ühele hankijatest.
author: mkirknel
manager: AnnBe
ms.date: 02/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchRFQCaseTable, PurchRFQReplyTable, PurchRFQCompare, PurchRFQEditLines, PurchRFQEditLinesParameters, PurchTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45ddab03810b331bcd8965f6a2ba699ffb138910
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1533348"
---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a>Pakkumiskutse pakkumiste sisestamine ja võrdlemine ning lepingute määramine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas sisestada pakkumiskutsele (RFQ) vastuseid, saabunud pakkumisi hinnata ja võrrelda ning seejärel määrata leping ühele pakkumise esitanud hankijatest. Saate seda protseduuri kasutada demoandmete ettevõttes **USMF**.

Enne protseduuri alustamist peab teil olema kahe reaga pakkumiskutse, mis on saadetud vähemalt kahele hankijale. Selle RFQ loomiseks viige lõpule protseduur [Pakkumiskutse loomine](create-request-quotation.md). Peate seadistama hindamiskriteeriumid enne, kui saate seda protseduuri lõpetada.

Pakkumise saate sisestada kas hankijana või hankespetsialistina. Lisateavet vaadake teemast [„Hankija koostöö seadistamine ja haldamine”](../set-up-maintain-vendor-collaboration.md).

## <a name="enter-a-reply-as-a-vendor"></a>Vastuse sisestamine hankijana

1. Armatuurlaual valige **Hankija pakkumine**.
2. Leidke loendist **Uued pakkumiskutsed** äsja saadetud pakkumiskutse. Valige vaatamiseks nõutud pakkumiskutse.
3. Valige **Pakkumiskutsete manused**, et vaadata lisatud manuseid.
4. Valige **Pakkumine**, et muuta väljad redigeeritavaks. Jälgige, et välja **Pakkumise edenemine** väärtuseks oleks määratud **Hankija värskendab**.
5. Sisestage päisesse ja ridadele väärtused pakkumise vastusest.
6. Kui pakkumisele tuleb lisada mis tahes manuseid, valige **Pakkumise manused.**
7. Valige kiirkaart **Pakkumisjuhiste üksused**, et vaadata, kas nõutakse mingisuguseid dokumente.
8. Valige kiirkaart **Parandused**, et vaadata, kas pakkumiskutset on muudetud.
9. Valige kiirkaart **Küsimustik**. Kõigile siin kuvatavatele küsimustikele tuleb vastata.
10. Valige kiirkaart **Rea üksikasjad**, et vaadata rea kohta laiendatud teavet.
11. Valige **Lähtestamine alates pakkumiskutsest** ainult siis, kui peate lähtestama väärtused, mis on sisestatud algse pakkumiskutse väärtusteks.
12. Saate pakkumise igal ajal salvestada ja seda hiljem uuesti töödelda tingimusel, et aegumiskuupäev ja-kellaaeg pole möödunud. Sel juhul leiate pakkumise loendist **Pooleliolevad pakkumised** tööruumis **Hankija pakkumine**.
13. Kui pakkumine on saatmiseks valmis, valige **Edasta**. Kui te ei soovi pakkumist teha, valige **Keeldu**.

    Esitatud pakkumised on saadavaloendis **Esitatud pakkumised** tööruumis **Hankija pakkumine**.

14. Pärast pakkumise esitamist saate selle mis tahes ajal tagasi kutsuda enne aegumiskuupäeva ja-kellaaega. Võtke arvesse, et pakkumise tagasikutsumisel ei käsitleta seda esitatuna.

    Kui hankeosakond võtab pakkumise vastu või lükkab tagasi , ilmub see kas loendis **Võidetud pakkumised** või **Kaotatud pakkumised** tööruumis **Hankija pakkumine**.

## <a name="enter-a-reply-from-a-vendor-as-a-procurement-professional"></a>Hankija vastuse sisestamine hankespetsialistina

1. Veenduge, et luba redigeerida hankija pakkumisi on seadistatud. Minge **Hanked \> Seadistus \> Hangete parameetrid**. Vahekaardil **Pakkumiskutse** seadke suvandi **Ostja saab redigeerida hankija pakkumist** väärtuseks **Jah**.
2. Avage **Hanked \> Pakkumiskutsed \> Kõik pakkumiskutsed**.
3. Valige pakkumiskutse, mille olek on **Saadetud**, ja klõpsake linki väljal **Pakkumiskutse juhtum**.
4. Valige **Halda vastuseid**. Ilmuval lehel näidatakse igale kutsutud hankijale tehtud pakkumiskutset.
5. Valige pakkumiskutse, millele pole vastatud. (Välja **Vastuse edenemine** väärtuseks peab olema määratud **Alustamata**.)
6. Valige **Redigeerimine \> Pakkumiskutse vastuse redigeerimine**.

    Kuvatakse leht **Pakkumiskutse vastus**. Hankespetsialistina saate nüüd sisestada vastuse hankija asemel. Jälgige, et välja **Pakkumise edenemine** väärtuseks oleks määratud **Ostja värskendab**.

7. Pakkumise andmete sisestamine. Kui olete lõpetanud, valige **Edastmine**.

## <a name="score-the-bids"></a>Pakkumiste hindamine

1. Lehel **Kõik pakkumiskutsed** valige pakkumiskutse juhtum, mille kohta soovite hindamisvastuseid saada.
2. Valige **Halda vastuseid**.
3. Valige vastuse skoor.
4. Valige **Päis**, et saaksite vaadata pakkumise hindamist.
5. Sisestage kiirkaardil **Pakkumise hindamine** väljale **Skoor** number ühe hindamiskriteeriumi kohta.

    Kui liigute hiirega üle hindamiskriteeriumi, näitab kohtspikker vahemiku, millesse skoor peab jääma. Selles demos saate sisestada mis tahes skoorikriteeriumidele arvu vahemikus 1 ja 5.

6. Korrake etappi 5 teise skoorikriteeriumiga.
7. Kui pakkumiskutse juhtumil on küsimustik, mis saadeti hankijatele, saate sisestada hankijate vastused kiirkaardil **Küsimustikud**.
8. Sulgege leht.
9. Korrake etappe 1 kuni 8 kõigi teiste pakkumiste puhul.

## <a name="compare-the-replies"></a>Vastuste võrdlemine

1. Toimingupaani vahekaardil **Üldine** valige suvand **Vastuste võrdlemine**.
2. Väljale **Reiting** sisestage number.

    See leht näitab pakkumisi koos päise ja ridade teabega ning ka punktide kogusummat päise tasemel. Saate ridu võrrelda, sortides ruudustikku nii, et võrreldavad read on üksteise kõrval. See teema sisaldab lisaks järgmist teavet.

    - **Kogus** – hankija pakutud kogus. See kogus ei pruugi võrduda kogusega, mis määratud pakkumiskutses.
    - **Netosumma** – hankija pakutud hind real olevatele kaupadele, miinus mis tahes allahindlused.
    - **Hälve** – päevade arv, mille võrra pakkumise päise või rea tarnekuupäev pakkumiskutses päises või real taotletud tarnekuupäevast erineb. Saate sisestada taseme iga pakkumise puhul.

3. Valige päise rida teisele pakkumisele, mida soovite järjestada.
4. Väljale **Reiting** sisestage number.
5. Valige käsk **Salvesta**.

## <a name="reject-a-bid"></a>Pakkumise tagasilükkamine

1. Valige päise rida pakkumisele, mille soovite tagasi lükata.

    Ühe pakkumise puhul saate korraga aktsepteerida, tagasi lükata või tagastada ainult ühe pakkumise või rea.

2. Valige märkeruut **Märgi.**

    Kui valite pakkumise päises märkeruudu **Märgi**, märgitakse ka kõik read. Ainult mõnede pakkumise ridade tagasilükkamiseks või aktsepteerimiseks saate märkida ainult need read. Lisaks saate kinnitada mõne pakkumiskutse rea puhul ühe hankija pakkumise ja siis märata teised pakkumiskutse read teisele hankijale. Kuid peate tegema ühe pakkumise korraga.

    Kui on olemas alternatiivsed read, saate aktsepteerida esialgse pakkumise rea või selle alternatiivi, kuid mitte mõlemaid.

3. Valige **Keeldu**.
4. Valige **Parameetrid**ja seejärel sisestage või valige väljale **Tagasilükkamise põhjus** pakkumise tagasilükkamise põhjus.

    Põhjus salvestatakse vastuses.

5. Valige nupp **OK**.
6. Valige nupp **OK**.

## <a name="accept-a-bid"></a>Pakkumise aktsepteerimine

1. Valige pakkumine, mille soovite aktsepteerida, ja seejärel valige link väljal **Pakkumiskutse**.

    Kui olete lehel **Pakkumiskutse vastuste võrdlemine** siis keskendub süsteem esiletõstetud pakkumisele aktsepteerimistoimingu käigus. Saate aktsepteerida ridu ainult ühest pakkumisest korraga.

2. Toimingupaanil valige käsk **Vasta**.
3. Valige **Aktsepteerimine**.

    Kui märkisite ainult kindlad read, kaasatakse aktsepteerimistoimingusse ainult need read. Kui soovite aktsepteerida kõiki pakkumise ridu, siis ei pea te ridu märkima.

4. Valige **Parameetrid**ja seejärel sisestage või valige väljale **Aktsepteerimise põhjus** pakkumise aktsepteerimise põhjus.

    Põhjus salvestatakse pakkumises.

5. Valige nupp **OK**.
6. Valige nupp **OK**.

    Kui valite nupu **OK**, luuakse ostutellimus pakkumiskutse kinnitusse lisatud ridade alusel. Kui on teisi pakkumisi, mida ei ole töödeldud (aktsepteeritud, tagasi lükatud või tagastatud), siis palub süsteem teil need pakkumised tagasi lükata.

## <a name="view-the-purchase-order-that-is-generated"></a>Loodud ostutellimuse vaatamine

- Toimingupaani vahekaardil **Üldine** valige suvand **Ostutellimus**.

    Ilmuval lehel saate vaadata ostutellimust, mis loodi pakkumise aktsepteerimisel.
