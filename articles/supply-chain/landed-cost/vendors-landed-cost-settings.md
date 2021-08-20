---
title: Väljalaadimiskulu jaoks on lisatud hankija sätted
description: Selles teemas kirjeldatakse uusi välju, mis lisatakse olemasolevale hankijate lehele, kui lubate mooduli Väljalaadimiskulu. Nende väljade abil saate seadistada koos Väljalaadimiskulu funktsioonidega kasutatavad hankijaid.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: b8f8e3969e7471f0ff694f2c7aa4464ee815082a5fae7ceff6010e915013988a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782559"
---
# <a name="vendor-settings-added-for-landed-cost"></a>Väljalaadimiskulu jaoks on lisatud hankija sätted

[!include [banner](../../includes/banner.md)]

Kui lubate mooduli **Väljalaadimiskulu**, lisatakse olemasolevale lehele **Hankijad** mitu uut välja. Nende väljade abil saate seadistada koos Väljalaadimiskulu funktsioonidega kasutatavad hankijaid.

Asjakohaste väljade määramiseks avage **Hanked \> Hankijiad \> Kõik hankijad**. Avage olemasolev hankija või looge uus hankija ja seejärel valige kiirkaart **Mitmesugused üksikasjad**. Kõik uued väljad, mille moodul **Väljalaadimiskulu** lisab, kuvatakse päise **Teekonnad** all. Järgmises tabelis kirjeldatakse neid välju.

| Field | Kirjeldus |
|---|---|
| Saatmise tüüp | <p>Valige hankija roll seoses väljalaadimiskuluga.</p><ul><li>**Pole** – hankijal pole väljalaadimiskuluga seotud kindlat rolli. See väärtus on vaikesäte, kuna tõenäoliselt enamikul hankijatel kindlat rolli pole.</li><li>**Saatmisettevõte** – hankija on saatmisettevõte. Selle saatmistüübiga hankijad on saadaval valimiseks lehe **Teekonnad** väljal **Saatmisettevõte**.</li><li>**Tollimaakler** – hankija on tollimaakler. Selle saatmistüübiga hankijad on saadaval valimiseks lehe **Fooliod** väljal **Tollimaakler**.</li><li>**Agent** – hankija on agent. Selle saatmistüübiga hankijad on saadaval valimiseks lehtede **Hankijad** ja **Ostutellimused** väljal **Agent**.</li></ul> |
| Kulutüübi grupp | Määrake hankija kulutüübi gruppi, et valida [automaatsed kulud](auto-cost-setup.md). |
| Lähtesadam | Valige teekonna päritolusadam. |
| Agent | Vaikeagent hankijalt ostude tegemisel. |
| Impordi kuluarvutuse hankija | <p>Saate määrata, kas hankija on väljalaadimiskulu hankija.</p><p>**Nõuanne.** Seda välja saate koos kirjetasandi turvalisusega kasutada selleks, et piirata teekonna loomisel kuvatavate ostutellimuste hulka.</p> |
| Saatmisettevõte | Saate valida vaikesaatmisettevõtte, mida kasutatakse hankija jaoks ostutellimuste loomisel. |
| Teenuste pakkuja | Saate määrata, kas hankija on teenusteosutaja. |
| Üle-/alataseme kõikumisvahemiku grupp | Saate valida hankija jaoks üle-/alataseme kõikumisvahemiku vaikegrupi. |
