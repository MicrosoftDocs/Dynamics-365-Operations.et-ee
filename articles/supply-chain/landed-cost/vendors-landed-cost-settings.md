---
title: Väljalaadimiskulu jaoks on lisatud hankija sätted
description: Selles teemas kirjeldatakse uusi välju, mis lisatakse olemasolevale hankijate lehele, kui lubate mooduli Väljalaadimiskulu. Nende väljade abil saate seadistada koos Väljalaadimiskulu funktsioonidega kasutatavad hankijaid.
author: sherry-zheng
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 8cc0622cd761a671ebb88addc36b777cfefb7dc7
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500906"
---
# <a name="vendor-settings-added-for-landed-cost"></a>Väljalaadimiskulu jaoks on lisatud hankija sätted

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

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
