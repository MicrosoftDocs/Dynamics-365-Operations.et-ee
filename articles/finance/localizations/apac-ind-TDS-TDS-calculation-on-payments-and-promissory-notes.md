---
title: TDS-i arvutamine maksetelt ja võlatähtedelt
description: See teema annab viiteteavet erinevate maksekannete kohta, mille alusel arvutatakse lähtekohas (TDS) kinni arvatud maks.
author: kailiang
ms.date: 02/12/2021
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
ms.openlocfilehash: 28afd04b1c341985f7ac15e05aba7a9039a59d869dd5bc60b4163d2ba1ae4ec0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750336"
---
# <a name="tds-calculation-on-payments-and-promissory-notes"></a>TDS-i arvutamine maksetelt ja võlatähtedelt

[!include [banner](../includes/banner.md)]

See teema annab viiteteavet erinevate maksekannete kohta, mille alusel arvutatakse lähtekohas (TDS) kinni arvatud maks.

| Seerianumber | Kande tüüp | Kandesumma | Lehe nimi ja valiku tee | Konto tüüp ja vastaskonto tüüp |
|---------------|------------------|--------------------|--------------------|--------------------------------------|
| 1             | Ettemaks/makse arve vastu (tasumisele kuuluv TDS) | Deebet või kreedit | <ul><li>Üldine tööleht (**Pearaamat \> Töölehekirjed \> Üldised töölehed**)</li><li>Arve tööleht (**Ostureskontro \> Arved \> Arve tööleht**)</li><li>Makse tööleht (**Ostureskontro \> Maksed \> Hankija maksete tööleht**)</li></ul> | Hanija (Dr.), Pank (Kr.) |
| 2             | Ettemaks/makse arve vastu (ost on tehtud kliendilt – TDS-i kohustus) | Deebet või kreedit | <ul><li>Üldine tööleht (**Pearaamat \> Töölehekirjed \> Üldised töölehed**)</li><li>Arve tööleht (**Ostureskontro \> Arved \> Arve tööleht**)</li><li>Makse tööleht (**Ostureskontro \> Maksed \> Hankija maksete tööleht**)</li></ul> | Klient (Dr.), Pank (Kr.) |
| 3             | Võlatähed | Debiteeri | Koosta võlatähe tööleht (**Ettemaksukonto \> Maksed \> Võlatähed \> Võlatähte koostamise tööleht**) | Hankija (Dr.), Pearaamat (Kr.) |
| 4             | Mitmesugused tulud (TDS-i saadaolev) | Deebet või kreedit | Üldine tööleht (**Pearaamat \> Töölehekirjed \> Üldised töölehed**) | Pank (Dr.), Pearaamat (Kr.) |
| 5             | Muud kulud (TDS-i kohustus) | Deebet või kreedit | Üldine tööleht (**Pearaamat \> Töölehekirjed \> Üldised töölehed**) | Pank (Dr.), Pearaamat (Kr.) |

Maksete ja võlatähtede TDS-i arvutamiseks järgige neid samme.

1. Looge töölehe lehtedel töölehe read. Valige konto tüüp ja vastaskonto tüüp.
2. Valige **Funktsioonid \> Tasakaalustus** et avada **Avatud kannete redigeerimise** leht. Seejärel valige konkreetne arve, mis tuleb tasakaalustada. Kui TDS on arve tasemel juba arvutatud, kuvatakse väljal **Summa** alussumma, mille alusel TDS arvutati. **Maksusumma** väli näitab TDS-i maksusummat, mis on kande jaoks arvutatud. Väljal **Summa** kuvatakse makse netosumma (st maksesumma pärast TDS-i mahaarvamist).

    > [!NOTE]
    > Arve vastu tehtud makse puhul kehtivad järgmised tingimused:
    >
    > - Kui maksesumma ja arve summa on samad, siis TDS-i ei arvutata, kui see on juba arve tasemel arvutatud.
    > - Kui arve summa pärast TDS-i summa mahaarvamist on suurem kui maksesumma, siis TDS-i ei arvutata.
    > - Kui arve summa pärast TDS-i summa mahaarvamist on väiksem kui maksesumma, arvutatakse TDS arvesummat ületavalt summalt.

3. Vahekaardil **Töölehe kanded** lehel **Üldine** vaadake või muutke hankijale või kliendile määratud TDS-i vaikegruppi **TDS grupp** väljal. Töölehe ridadel arvutatud TDS-i summa põhineb TDS-i grupi väljal loetletud TDS-i maksukoodide jaoks määratletud valemil.

    > [!NOTE]
    > TDS arvutatakse ainult siis, kui on märgitud **Arvuta kinnipeetav maks** valik **Jah** klientide jaoks **Kõik kliendid** lehel.

4. Vahekaardil **Maksuteave**, **Ettevõtte teave** jaotises **Nimi** väljal valige ettevõtte nimi, mis on seadistatud alternatiivse aadressi jaoks.

    Vaadake hankija või kliendi hinnalepete kategooria olemust **Kinnipeetava maksu** väljal, mis on **Hinna hindamise** väljagrupis. Väli **Maksukonto number (TAN)** näitab valitud ettevõtte maksukonto numbrit (TAN).

5. Valige **Kinnipeetav maks nupp \> menüüst Kinnipeetav maks** et avada **Ajutised kinnipeetava maksu kanded** leht. Selle lehekülje ülemisel osal on järgmised väljad:

    - **Kinnipeetava maksu summa kokku** - TDS-grupi kande jaoks arvutatud TDS-i kogusumma.
    - Väljal **Väärtus** - Kuvatakse kande TDS-i arvutamiseks kasutatav koguprotsent. Koguprotsent põhineb valemil, mis on määratud TDS-grupiga seotud TDS-i maksukoodide jaoks.
    - **Korrigeeritud kinnipeetava maksu summa kokku** - TDS-i grupi kõikide maksukoodide korrigeeritud TDS-i kogusumma.
    - **TDS** – valitud märkeruut näitab, et TDS-grupp on kandega seotud.

    Välja **Ülevaade**, **Üldine**, ja **Summa** vahekaardil kinnipeetava maksu kannete lehel kuvatakse TDS-summa ja korrigeeritud TDS-i summa TDS-i grupiga seotud TDS-i maksukoodi kohta.

6. Valige **Lävi** et avada leht **Lävi** kus saate üle vaadata läve piirmäära, mis on määratud konkreetse TDS-maksukoodiga seotud TDS-i maksukomponendile.
7. Valige **Valemikoostur** et avada **Valemikoosturi leht** kus saate üle vaadata TDS-i maksukoodi jaoks määratud valemi.
8. Sulgege **valemikoostur** ja **Ajutise kinnipeetava maksu kannete** lehed et naasta **Töölehe kande** lehele.
9. Kinnitage ja sisestage tööleht. Müügiarvetel arvutatud TDS-summa sisestatakse tasumisele kuuluvale kontole, mis on määratud igale TDS-i maksukoodile TDS-grupis. TDS-i maksukoodide ostureskontro või müügireskontrod määratletakse **Kinnipeetava maksu koodide** lehel.
10. Valige **Sisestatud kinnipeetav maks**, et avada **Kinnipeetava maksu kannete** leht. Väljal **Väärtus** kuvatakse kande TDS-i arvutamiseks kasutatav koguprotsent.

    Väljad **Ülevaade**, **, Üldine**, ja **Summa** vahekaardid kuvatakse TDS-i summad, mis arvutati kandega seotud TDS-grupi jaoks.

11. Vaadake TDS-i kalkulatsiooniteavet iga TDS-grupiga seotud TDS-i maksukoodi kohta.

## <a name="generate-payments"></a>Loo tasumised

Juurdepääsu piiramiseks tehke järgmist.

1. Järgige üht neist sammudest.

    - Avage **Ostureskontro \> Maksed \> Hankija maksete tööleht**.
    - Avage **Müügireskontro \> Maksed \> Kliendi makse tööleht**.
    - Mine **Ettemaksukonto \> Maksed \> Võlatähed \> Võlatähte koostamise tööleht**.
    - Avage jaotis **Müügireskontro \> Maksed \> Käskveksel \> Koosta käskveksli tööleht**.
    - Avage jaotis **Müügireskontro \> Maksed \> Käskveksel \> Koosta käskveksli tööleht uuesti**.

2. Valige **Read**.
3. Valige **Funktsioonid \> Loo maksed**.
