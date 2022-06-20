---
title: Väljalaadimiskulu jaoks on lisatud hankija sätted
description: See artikkel kirjeldab uusi välju, mis lisatakse olemasolevale hankijate lehele, kui lubate väljaminev kulumoodul. Nende väljade abil saate seadistada koos Väljalaadimiskulu funktsioonidega kasutatavad hankijaid.
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
ms.openlocfilehash: 84d1dee0815b036a3d411eabff49d8a08249bed3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882572"
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
