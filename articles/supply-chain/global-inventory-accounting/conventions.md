---
title: Reeglid
description: See teema kirjeldab, kuidas seadistada reegleid, et määrata, kuidas kulusid peaks Global Inventory Accounting teenuses arvesse võtma.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 74d99d3eefdcaaa7f6551668990b702396b32ffc
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273144"
---
# <a name="conventions"></a>Reeglid

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Reeglid on konteiner poliitikate komplektile, mis mõjutavad süsteemi käitumist. Äritegevuse nõuetele toetudes peate määrama reeglid kasutades erinevate poliitikate kombinatsiooni, mis määravad, kuidas tuleb kulusid teenuses Global Inventory Accounting arvestada. Kõikide pearaamatute puhul rakendatud raamatupidamispoliitikate ühtsuse tagamiseks saate iga reegli seostada ühe või mitme pearaamatuga.

Oma reeglite seadistamiseks minge **Globaalne laoarvestus \> Seadistamine \> Reeglid**. Määrake igale reeglile järgmised väljad.

- **Nimi** – sisestage reegli nimi.
- **Kirjeldus** – sisestage reegli kirjeldus.
- **Kuluobjekti poliitika** – valige kuluobjekti poliitika. Need põhimõtted määratlevad granulaarsuse taseme, mida süsteem laoväärtuse arvutamisel ja säilitamiseks kohaldab. Saadaval on järgmised eelmääratud valikud:

    - Toode
    - Toode – Koht
    - Toode – Koht – Ladu

    Näiteks kui valite *Toode – Koht*, siis iga lao liikumise (sissevool või väljavool) jaoks arvutab ja haldab süsteem iga toote laokulu koha tasemel. Seetõttu ei mõjuta lao liikumised madalamatel tasemetel (nt laotasemel) laoväärtust. (Laotaseme ülekanne on näiteks kauba ülekanne ühel laokohal kahe lao vahel) Samamoodi ei saa te varude maksumust vaadata madalamal tasemel, näiteks laotasemel.

- **Sisendi mõõtmise aluspoliitika** – valige sisendi mõõtmise aluspoliitika. Need poliitikad määratlevad kulud, mis tuleks laokontole kanda ja kulud, mida tuleb nõuda. Kaubandusettevõtete jaoks on asjakohased järgmised valikud:

    - **Tavaline ajalooline** – kõikide kulukomponentide voog laokontole.
    - **Standartne** : standardsed kuluvood laokontodesse ning erinevus rakendatud kulu ja tegelike kulude vahel kantakse dispersioonikontodele. Kui soovite luua *standardse* sisendi mõõtmise aluspoliitikat, peate esmalt looma hinnakirja, kus poliitika saab otsida kauba standardset kulu.
    - **Hinnakirjad** – Global Inventory Accounting teenus toetab kauba hindade toomist mitmest juriidilisest isikust. Saate määratleda hinnakirja, mida sisendi mõõtmise aluspoliitika hakkab kasutama. Sel viisil saab süsteem teada, kust kauba hinda otsida. Hinnakirjade seadistamiseks toimige järgmiselt.

        1. Väljale **Nimi** sisestage nimi.
        1. Väljale **Kirjeldus** sisestage kirjeldus.
        1. Väljal **Kulu tüüp** valige kulu tüüp (*Standardne kulu* või *Planeeritud kulu*).
        1. Valige väljal **Hinna tüüp** hinnatüüp (*Kulu*, *Ost* või *Müügihind*).
        1. Kuluarvutue versiooni lisamine.
        1. Tegevuspaanil valige **Hind**, et kinnitada kauba hinnad hinnakirjas.

- **Kuluvoo eelduse poliitika** – valige kuluvoo eelduse poliitika. Need poliitikad määratlevad, kuidas eemaldatakse kulud varudest ja esitatakse müüdud kaupade maksumusena. Saadaval on järgmised eelmääratud valikud:

    - Keskmine
    - Konkreetne – partii

    > [!NOTE]
    > Global Inventory Accounting on tähtajatu laovarude süsteem. Süsteem jälgib laoväärtust kannete kaupa.

- **Kuluelemendi poliitika** – saate määrata kuluelemendi poliitikad ja siduda need selle väljaga. *Kuluelement* on sündmuse tarbitava ressursi kulu. Kuluelemente saate kasutada kulude jälgimiseks ja kategoriseerimiseks. Kuluelemendi poliitikate loomiseks sisestage teave järgmistesse kohtadesse:

    - **Nimi** väli
    - **Kirjelduse** väli
    - **Kuluelementide** loend
    - **Reeglite** ruudustik

    Kui te ei soovi laoväärtust veelgi täpsemaks muuta, peate looma kuluelemendi loendi, kus on üks kuluelement. Seejärel peate looma kuluelemendi poliitika, et vastendada kõik asjakohased mõõtmise tüübid (kulukomponendid) selle kuluelemendiga.
