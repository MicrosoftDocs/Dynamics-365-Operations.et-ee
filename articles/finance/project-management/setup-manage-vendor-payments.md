---
title: Maksmisel tasutavate hankija maksete seadistamine ja kasutamine
description: See teema selgitab, kuidas luua maksmisel tasumise (PWP) tingimusi, nii et saate väljastada osalisi hankija makseid kliendi maksete alusel.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 390cec62d2790ed10892669e283f2283c6b8e686
ms.sourcegitcommit: 399f128d90b71bd836a1c8c0c8c257b7f9eeb39a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/23/2020
ms.locfileid: "3284109"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Maksmisel tasutavate hankija maksete seadistamine ja kasutamine

[!include [banner](../includes/banner.md)]

Kui kinnitate hankija alltöövõtjana, võib olla vaja hankija makset kinni pidada, kuni klient teile projekti eest maksab. Sellise olukorra jaoks saata seadistada maksmisel tasumise (PWP) tingimused hankija ostutellimuse (PO) seadistamisel.

Näiteks kui klient maksab teatud projekti arve summa, saate hankija arvel oleva summa osaliselt või täielikult maksmiseks vabastada. Seadistage lihtsalt PWP tingimused nii, et hankijale makstakse pärast seda, kui olete saanud kliendilt konkreetse protsendi seotud maksest. Kui saate kliendilt osalise makse, võite mõned seotud hankija arved käsitsi maksmiseks vabastada.

Järgmises näites kirjeldatakse protsessi, kui kasutatakse PWP tingimusi.

## <a name="example"></a>Näide

Teie organisatsioon nõustub müüma kliendile 100 arvutit, kuhu on installitud tarkvara, hinnaga 150,00 USA dollarit (USD) arvuti kohta. Seejärel palkate hankija, kes pakub teile arvuteid, kuhu on installitud tarkvara. Lepingu järgi peab klient enne teie organisatsioonile tasumist arvutite kvaliteedi kinnitama. Teie organisatsioonis on tava maksta hankijatele alles siis, kui klient on teile tasunud. Seega saate seadistada projekti nii, et selle maksmisel tasumise protsent on 100 protsenti.

Hankija saadab teile 100 arvutit, kuhu on installitud tarkvara, koos arvega, mille summa on 10 000,00 USD. Kuna teie projekti jaoks on seadistatud PWP tingimused, ei maksa te hankijale arvutite vastuvõtmisel. Selle asemel saadate arvutid kliendile koos arvega, mille summa on 15 000,00. Klient kontrollib arvutid üle ja kinnitab kogu projekti arve summa.

Kui olete kliendilt täieliku makse saanud, maksate hankijale hankija arve kogusummas 10 000,00.

## <a name="set-up-pwp-terms-for-a-project"></a>Projekti jaoks PWP tingimuste seadistamine

Kui seadistate projektile PWP tingimused, peate määrama protsendina minimaalse summa, mille klient peab teile projekti eest maksma enne seda, kui te hankijale tasute. Projekti kliendiarvete puhul arvutatakse automaatselt lävisumma. PWP tingimuste läviprotsentide seadistamiseks tehke järgmist.

1. Avage **Projektihaldus ja raamatupidamine** \> **Projektid** \> **Kõik projektid**.
2. Leidke ja avage projekt, millele soovite PWP tingimused seadistada.
3. Klõpsake kiirkaardil **Hankija lepingud** valikut **Lisa rida**.
3. Tehke väljal **Konto kood** üks järgmistest valikutest.

    - **Tabel** – PWP tingimused kehtivad ühele hankijale.
    - **Grupp** – PWP tingimused kehtivad kõikidele hankijagrupi hankijatele.
    - **Kõik** – PWP tingimused kehtivad kõigile hankijatele.

4. Kui valisite eelmises etapis valiku **Tabel** või **Grupp**, valige väljal **Hankija / Hankijagrupp** hankija või hankijagrupp, kelle puhul PWP tingimused rakenduvad. Kui valisite eelmises etapis **Kõik**, ei saa välja **Hankija / Hankijagrupp** redigeerida.
5. Kui projektis on seadistatud ka hankija kinnipidamise tingimused, valige väljal **Hankija kinnipidamise tingimused** reegli ID kinnipidamistingimustele.
6. Väljale **PWP läviväärtuse protsent** sisestage projekti läviväärtuse protsent. Projektile sisestatav protsent määrab miinimumsumma, mille klient peab teile tasuma enne, kui te maksate hankijale.

## <a name="create-a-po-that-has-pwp-terms"></a>PWP tingimustega ostutellimuse loomine

Kui sisestate hankijale arve ja hankijale kehtivad PWP tingimused, kuvatakse need tingimused ostutellimuse ridadel. PWP tingimustega ostutellimuse loomiseks toimige järgmiselt.

1. Avage **Hanked** \> **Ostutellimused** \> **Kõik ostutellimused**.
2. Valige toimingupaanil nupp **Uus**. Seejärel sisestage dialoogiboksis **Loo ostutellimus** vajalik teave ja valige **OK**.

    Teise võimalusena avage olemasolev ostutellimus lehel **Kõik ostutellimused**.

4. Vaadake lehe **Ostutellimus** kiirkaardil **Ostutellimuse read** läbi hankija ostutellimuse rea üksikasjad. Suvand **Maksmisel tasumine** valitakse automaatselt ja välja **PWP läviväärtuse protsent** väärtus kopeeritakse automaatselt vormi **PWP läviväärtuse protsent** lehel **Projektid**.
6. Kui te ei soovi rakendada ostutellimuse real hankijale PWP tingimusi, tühjendage valik **Maksmisel tasumine**. Sel juhul lähtestatakse ostutellimuse rea **PWP läviväärtuse protsent** väärtusele 0 (null).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Kliendi makseteabe uuendamine ja hankijale maksmine

Kui hankija lõpetab projektis töö ja saadab teile arve, peate te projekti oleku ja kliendiarved üle vaatama, et teha kindlaks, kas projektis täideti maksmisel tasumise tingimused. Kui hankija maksmisel tasumise tingimused olid täidetud, saab määrata tasumiseks hankija arve read, mille read põhinevad projekti kliendimaksetel. Kui otsustate hankijale maksta isegi juhul, kui PWP tingimused ei ole täidetud, saate PWP tingimusi lehel **Maksmisel tasutavad hankija arved** muuta.

1. Avage **Projektihaldus ja raamatupidamine** \> **Päringud ja aruanded** \> **Säilitamise päringud** \> **Maksmisel tasutavad hankija arved**.
2. Sisestage lehel **Maksmisel tasutavad hankija arved** otsinguväljale otsingusõnad, et leida hankija arve, mida soovite üle vaadata, ja seejärel valige **Otsi**.
3. Valige kiirkaardil **Hankija arve read** need read, mida soovite muuta.
4. Kui **Maksmisel tasumise** tingimused on arve real täidetud, valige **Väljasta hankija makse**. Valik **Maksmisel tasumine** tühjendatakse ja välja **Maksmiseks valmis** väärtus muudetakse väärtuseks **Jah**.
