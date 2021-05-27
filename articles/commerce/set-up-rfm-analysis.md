---
title: Hiljutisuse, sageduse ja valuuta (RFM-i) analüüsi seadistamine
description: Selles teemas selgitatakse, kuidas seadistada klientidele hiljutisuse, sageduse ja valuuta (RFM-i) analüüsi.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCRRFMDefinition
audience: Application User
ms.reviewer: josaw
ms.custom: 78943
ms.assetid: 8ff9aac3-5ada-4150-85fd-18901c926d53
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f1f91a67ebac212f72b5524723ec0b8b4e0e3e99
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6028271"
---
# <a name="set-up-recency-frequency-and-monetary-rfm-analysis"></a>Hiljutisuse, sageduse ja valuuta (RFM-i) analüüsi seadistamine

[!include [banner](includes/banner.md)]

Selles teemas selgitatakse, kuidas seadistada klientidele hiljutisuse, sageduse ja valuuta (RFM-i) analüüsi.

Hiljutisuse, sageduse ja rahasumma (RFM) analüüs on turunduse tööriist, mida teie organisatsioon saab kasutada kliendi ostudega loodud andmete hindamiseks. Pärast RFM-analüüsi seadistamist määratakse klientidele arvutatud RFM-i skoori, kui nad oste sooritavad. RFM-i skoor võib olla kolmekohaline hinne või koondnumber, sõltuvalt sellest, kuidas teie organisatsioon on RFM-analüüsi seadistanud. Kui teie organisatsioon kasutab skoori puhul kolmekohalist hinnet, siis selle põhimõte on järgmine.

- Esimene number on kliendi hiljutisuse määr, mis näitab, kui hiljuti klient teie organisatsioonist ostis.
- Teine number on kliendi sageduse hinne, mis näitab, kui tihti klient teie organisatsioonist ostab.
- Kolmas number on kliendi rahasumma hinne, mis näitab, kui palju klient teie organisatsioonist ostude tegemisel kulutab.

Näiteks on teie organisatsioon määranud hinded skaalal 1 kuni 5, kus 5 on kõrgeim hinne. Sel juhul ütleb kliendi hinne 535 teile kliendi kohta järgmist.

- **Hiljutisuse hinne 5** – klient ostis hiljuti.
- **Sageduse hinne 3** – klient ostab teie organisatsioonist tooteid keskmise sagedusega.
- **Rahasumma hinne 5** – klient kulutab ostes märkimisväärse rahasumma.

Kui teie organisatsioon kasutab skoori puhul koondnumbrit, pannake üksikud hinded kokku. Sama näite puhul on kliendi hinne 13 (5 + 3 + 5).

## <a name="set-up-rfm-analysis-for-the-customers-in-your-organization"></a>RFM-analüüsi seadistamine oma organisatsiooni klientide jaoks

1. Avage **Kõnekeskus** \> **Perioodiline** \> **RFM-analüüs**.
2. Valige lehel **RFM-analüüs** suvand **Uus**. Sisestage väljale **RFM-i definitsioon** RFM-i definitsiooni nimi. Näiteks võite anda definitsioonile nime RFM-A.
3. Sisestage selle RFM-i definitsiooni algus- ja lõppkuupäev.
4. Tehke kiirkaardil **Üldine** järgmist.

    - Kui RFM-i skoori iga osa peab sisaldama võrdset arvu kliente, märkige ruut **Ühtlane jaotus**.
    - Kolme tulemuse liitmiseks märkige ruut **Punktisummade lisamine**. Näiteks annab see kliendile RFM-i skoori 535 asemel skooriks 13.
    - Märkige ruut **Ajaloo salvestamine**, kui soovite, et süsteem salvestaks klientide statistilised andmed, et neid saaks RFM-i skoori arvutamiseks kasutada.

5. Tehke kiirkaardil **Hiljutisus** järgmist.

    - Sisestage väljale **Jaotused** jaotuste või gruppide arv, mida klientide hiljutisuse skoori arvutamisel kasutada. Näiteks kui teil on 100 klienti, tähendab jaotus 5, et iga skoori kohta on 20 klienti. 20 kliendi puhul, kes on kõige viimasena ostnud, on hiljutisuse skoor 5. Järgmise 20 kliendi hiljutisuse skoor on 4 jne. Kui teil on 50 klienti, on 10 kliendi hiljutisuse skoor 5, 10 kliendi hiljutisuse skoor 4 jne.
    - Valige väljal **Prioriteet**, kui suur kaal on kliendi RFM-i skoori arvutamisel hiljutisuse parameetril võrreldes teiste parameetritega. Näiteks võite hiljutisuse skoori väärtuse rahalise skoori omast suuremaks määrata.
    - Sisestage väljale **Kordaja** väärtus, millega hiljutisuse skoori korrutada. Kui te väärtust ei sisesta, siis skoori ei korrutata.
    - Valige väljal **Periood** ajavahemik, mille alusel hiljutisuse skoori arvutada. Nt nädala või kuu kaupa.

6. Tehke kiirkaardil **Sagedus** järgmist.

    - Sisestage väljale **Jaotused** jaotuste või gruppide arv, mida klientide sageduse skoori arvutamisel kasutada.
    - Valige väljal **Prioriteet**, kui suur kaal on kliendi RFM-i skoori arvutamisel sageduse parameetril võrreldes teiste parameetritega.
    - Sisestage väljale **Kordaja** väärtus, millega sageduse skoori korrutada. Kui te väärtust ei sisesta, siis skoori ei korrutata.

7. Tehke kiirkaardil **Valuuta** järgmist.

    - Sisestage väljale **Jaotused** jaotuste või gruppide arv, mida klientide rahalise skoori arvutamisel kasutada.
    - Valige väljal **Prioriteet**, kui suur kaal on kliendi RFM-i skoori arvutamisel rahalisel parameetril võrreldes teiste parameetritega.
    - Sisestage väljale **Kordaja** väärtus, millega rahalist skoori korrutada. Kui te väärtust ei sisesta, siis skoori ei korrutata.
    - Valige väljal **Bruto/neto**, kas kliendi rahalist skoori tuleks arvutada arvete bruto- või netosumma alusel.
    - Kui kliendi tagastuste summad tuleks kliendi arvete kogusummadest lahutada, märkige ruut **Tagastuste lahutamine**.

## <a name="view-a-customers-rfm-score"></a>Kliendi RFM-i skoori vaatamine

Kasutage seda protseduuri kliendi RFM-i skoori vaatamiseks.

1. Avage **Kõnekeskus** \> **Töölehed** \> **Klienditeenindus**.
2. Valige lehe **Klienditeenindus** paani **Klienditeenindus** otsinguväljadelt otsitava märksõna tüüp ja sisestage otsingutekst.
3. Valige **Otsi**.
4. Valige lehel **Kliendi otsing** soovitud kliendi kirje ja seejärel klõpsake valikut **Vali klient**.

RFM-i skoor kuvatakse grupis **Tellimuste ajalugu** lehe **Klienditeenindus** parempoolses osas.

## <a name="view-or-clear-the-history-of-an-rfm-analysis-record"></a>RFM-i analüüsi kirje vaatamine või kustutamine

Kasutage seda protseduuri RFM-i analüüsi kirje vaatamiseks või kustutamiseks.

1. Avage **Kõnekeskus** \> **Perioodiline** \> **RFM-analüüs**.
2. Valige lehel **RFM-analüüs** kirje, mida soovite vaadata.
3. Kirje ajaloo vaatamiseks klõpsake kiirkaarti **Ajalugu**.
4. Kirje ajaloo kustutamiseks klõpsake käsku **Kustuta ajalugu**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]