---
title: Väljalaadimiskulu jaoks on lisatud hankija sätted
description: Selles teemas kirjeldatakse uusi välju, mis lisatakse olemasolevale hankijate lehele, kui lubate mooduli Väljalaadimiskulu. Nende väljade abil saate seadistada koos Väljalaadimiskulu funktsioonidega kasutatavad hankijaid.
author: Weijiesa
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: b4e02397f7a4cdeaa21b451268b16e4fbe773612
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690522"
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
