---
title: Tegevuse salvestaja ning spikker Retail Modern POS-i (MPOS) ja pilvekassa jaoks
description: Selles teemas kirjeldatakse tegevuse salvestaja kasutamist Retail Modern POS-is (MPOS) ja pilvekassas.
author: mugunthanm
manager: AnnBe
ms.date: 06/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTerminalTable, SystemParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b0a5ca1e116e931ba992eab51a06dae9fdf92756
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006131"
---
# <a name="task-recorder-and-help-for-retail-modern-pos-mpos-and-cloud-pos"></a>Tegevuse salvestaja ning spikker Retail Modern POS-i (MPOS) ja pilvekassa jaoks

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse tegevuse salvestaja kasutamist Retail Modern POS-is (MPOS) ja pilvekassas.

## <a name="overview"></a>Ülevaade

Tegevuse salvestaja Retail Modern POSis või pilvekassas on uus lahendus, mille eesmärk on pöörata tähelepanu suurele tundlikkusele. Sellel on paindlik rakenduse programmeerimisliides (API) laiendatavuse ja sujuva integratsiooni tagamiseks äriprotsessi salvestiste tarbijatega. Peale selle on tõstetud esile tegevuse salvestaja integratsioon äriprotsesside modelleerija (BPM) tööriistaga teenuses Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)). Seetõttu saavad kasutajad luua oma rakenduste analüüsimiseks ja kujundamiseks salvestistest jätkuvalt rikkalikke äriprotsessi diagramme.

## <a name="architecture"></a>Arhitektuur

Tegevuse salvestaja suudab salvestada täpselt ja tõetruult kasutaja toiminguid kliendis. Iga juhtelement on seadistatud teavitama tegevuse salvestajat kasutaja toimingu täitmisest. Juhtelement teavitab tegevuse salvestajat, et toimus sündmus, ja edastab kogu asjassepuutuva teabe vastava kasutaja toimingu kohta reaalajas. Selle teabe põhjal suudab tegevuse salvestaja jäädvustada kasutaja toimingu tüübi (nt nupuvajutus, väärtuse sisestus või navigeerimine) ja mis tahes andmed, mis on kasutaja toiminguga seotud (nt sisestatud andmete väärtus ja tüüp, vormi kontekst või kirje kontekst). Tegevuse salvestaja lisab teabele piisavalt üksikasju, garanteerimaks, et salvestise taasesitamisel suudetakse teha salvestatud toiminguid täpselt samamoodi, nagu kasutaja neid tegi. (Taasesituse funktsioon ei ole veel Retail modern POS-is ega pilvekassas juurutatud.)

## <a name="basic-configuration"></a>Põhikonfiguratsioon

Tegevuse salvestamise lubamiseks kassas tehke järgmist.

1. Klõpsake valikuid **Jaemüük ja kaubandus** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Registrid**.
2. Klõpsake registrit, millel tegevuse salvestis aktiveerida.
3. Määrake vahekaardil **Registreeri** kiirkaardil **Üldine** valiku **Tegevuse salvestamise lubamine** väärtuseks **Jah**.
4. Klõpsake valikut **Salvesta**.
5. Avage **Jaemüük ja kaubandus** &gt; **Jaemüügi ja kaubanduse IT** &gt; **Jaotusgraafik**.
6. Valige töö **Registrid (1090)** ja klõpsake siis käsku **Käivita kohe**.

## <a name="create-a-recording"></a>Salvestise loomine

Tehke järgmist uue salvestise loomiseks tegevuse salvestaja abil.

1. Käivitage Retail Modern POS või pilvekassa ja logige sisse.
2. Klõpsake lehel **Sätted** jaotises **Tegevuse salvestaja** valikut **Ava tegevuse salvestaja**. Kuvatakse paan **Tegevuse salvestaja**. Võite klõpsata nuppu **Sule** (**X**) ülemises paremas nurgas paani **Tegevuse salvestaja** sulgemiseks enne uue salvestuse alustamist. Paani taasavamiseks korrake toimingut 2.

    [![Tegevuse salvestaja paan](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)

3. Sisestage salvestise nimi ja kirjeldus, ning seejärel klõpsake nuppu **Käivita**. Salvestusseanss algab kohe, kui klõpsate nuppu **Käivita**.

    > [!NOTE]
    > Kui klõpsate nuppu **Sule** (**X**) ülemises paremas nurgas sel ajal, kui salvestamine käib, siis paan **Tegevuse salvestaja** suletakse, kuid salvestusseanssi ei lõpetata. Tegevuse salvestaja paani taasavamiseks klõpsake nuppu **Spikker** (küsimärk) ekraani ülaosas.
    >
    > [![Küsimärk](./media/help.jpg)](./media/help.jpg)

4. Pärast nupu **Käivita** klõpsamist läheb tegevuse salvestaja salvestusrežiimi. Paanil **Tegevuse salvestaja** on näha salvestusprotsessiga seotud andmed ja nupud.
5. Tehke uuesti toimingud, mida soovite Retail Modern POS-i või pilvekassa kasutajaliideses teha.
6. Salvestusseansi lõpetamiseks klõpsake nuppu **Peata**.

## <a name="download-options"></a>Allalaadimisvalikud

Pärast salvestusseansi lõpetamist kuvatakse mitu valikut, et saaksite oma salvestise alla laadida.

[![Allalaadimisvalikud](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)

### <a name="save-to-this-pc"></a>Salvesta sellesse arvutisse

Salvestuspaketti saab kasutada tegevuse juhise esitamiseks, salvestise säilitamiseks või salvestise märkuste redigeerimiseks. (See funktsioon ei ole veel Retail Modern POS-is ega pilvekassas juurutatud.)

### <a name="export-as-word-document"></a>Ekspordi Wordi dokumendina

Saate salvestada salvestise Microsoft Wordi dokumendina. Dokument sisaldab salvestatud toiminguid ja hõivatud kuvatõmmiseid.

### <a name="save-as-developer-recording"></a>Salvesta arendaja salvestisena

Töötlemata salvestusfail on kasulik arendaja stsenaariumide, nt testkoodi loomise jaoks. (See funktsioon ei ole veel juurutatud)

## <a name="recording-controls"></a>Salvestamise juhtelemendid

[![Salvestamise juhtelemendid](./media/controls.jpg)](./media/controls.jpg)

### <a name="stop"></a>Peata

Salvestusseansi lõpetamiseks klõpsake nuppu **Peata**. Arvestage, et pärast seansi lõpetamist ei saa seda uuesti käivitada. Seega veenduge enne lõpetamist, et salvestamine oleks lõpetatud.

### <a name="pause"></a>Paus

Salvestusseansi ajutiseks peatamiseks (pausi tegemiseks) ja toiminguga jätkamiseks klõpsake nuppu **Paus**. Toiminguid, mida teete pärast nupu **Paus** klõpsamist, ei salvestata.

### <a name="continue"></a>Jätka

Salvestamisseansi jätkamiseks pärast pausi klõpsake **Jätka**.

### <a name="capture-screenshots"></a>Tee kuvatõmmised

Tegevuse salvestaja suudab jäädvustada Retail Modern POS-i kasutajaliidese kuvatõmmiseid äriprotsessi salvestamise ajal. Kuvatõmmise jäädvustamise funktsiooni sisselülitamiseks määrake suvandi **Jäädvusta kuvatõmmis** väärtuseks **Jah** ja seejärel alustage jäädvustamist. Kui lõpetate salvestamise, klõpsake **Peata** ja laadige alla Wordi dokument. Dokumendis on sammud asjakohaste kuvatõmmistega.

> [!NOTE]
> Pilvekassas ei toetata kuvatõmmise jäädvustamise funktsiooni.

### <a name="start-task-and-end-task"></a>Tegevuse alustamine ja lõpetamine

Saate määrata rühmitatud toimingute kogumi alguse ja lõpu nuppudega **Alusta tegevust** ja **Lõpeta** **tegevus**. Klõpsake nuppu **Alusta tegevust** toimingu „Alusta tegevust” lisamiseks ja tehke siis toimingud, mis tuleks rühma lisada. Kui olete rühma toimingute tegemise lõpetanud, klõpsake valikut **Lõpeta toiming**. Toimingute abil saate oma protseduure korraldada. Toiminguid saab pesastada teistesse toimingutesse. Sel viisil saate korraldada paremini väga pikki ja keerukaid äriprotsesse.

## <a name="adding-annotations"></a>Märkuste lisamine

Märkus on lisatekst, mille saab toimingule salvestises lisada. Näiteks saab märkusi kasutada kasutajale täiendava konteksti või juhiste andmiseks. Märkusi saab lisada enne või pärast toimingut. Märkuse saab lisada mis tahes toimingule, klõpsates toimingust paremal asuvat nuppu **Redigeeri** (pliiatsi sümbol).

[![Toimingu redigeerimise nupp](./media/annotate.jpg)](./media/annotate.jpg)

### <a name="texts-and-notes"></a>Tekstid ja märkused

Väljade **Tekstid** ja **Märkused** abil saab lisada teksti, mis peaks olema tegevuse juhises toiminguga seotud.

[![Teksti ja märkuste väljad](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)

#### <a name="text"></a>Tekst

Väljale **Tekst** sisestatav tekst kuvatakse tegevuse juhises toimingu teksti *kohal*. See asukoht sobib teksti jaoks, mida kasutaja peaks enne toimingu tegemist lugema.

#### <a name="notes"></a>Märkmed

Väljale **Märkused** sisestatav tekst kuvatakse tegevuse juhises toimingu teksti *all*. Märkuse teksti lugemiseks peab kasutaja toimingu teksti hüpikaknas laiendama. See asukoht sobib soovi korral loetava materjali jaoks või muu teabe jaoks, millest kasutajale võib abi olla, kuid mis pole toimingu tegemise jaoks kasutajale tingimata vajalik.

## <a name="help-in-retail-modern-pos-and-cloud-pos"></a>Spikker Retail Modern POS-is ja pilvekassas

Oma kohandatud tegevuse salvestiste kuvamiseks Retail Modern POS-i ja pilvekassa spikripaanil, et neid saaks tekstina kuvada, peate salvestama tegevuse salvestised oma BPM-i teeki ja seejärel värskendama oma spikrisüsteemi parameetreid nii, et need osutaksid teie BPM-i teegile. Lisateavet leiate jaotisest [Spikrisüsteemi ühendamine](../fin-and-ops/get-started/help-connect.md). Retail Modern POS-i ja pilvekassa spikker otsib LCS-ist reaalajas. See otsib kõigist BPM-i teekidest, mis on Commerce’i spikrisüsteemi parameetrites valitud, ja kuvab asjakohased tulemused. **Spikri** menüü avamiseks klõpsake ekraani ülaosas **spikri** nuppu (küsimärk) ning sisestage siis otsinguväljale oma protsess nimi ja vajutage otsingunuppu.

[![Nupp Spikker](./media/help.jpg)](./media/help.jpg)

Kui klõpsate otsingutulemustes valikut Tegevuse juhis, saate vaadata toiminguid spikriteemana või eksportida toimingud Wordi dokumenti.

> [!NOTE]
> Retail Modern POS-i ja pilvekassa spikker ei kuva tegevusjuhiseid selle põhjal, millisel vormil olete või millist toimingut teete. Protsessi nimi tuleb sisestada otsinguväljale ja klõpsata siis nuppu **Otsing**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]