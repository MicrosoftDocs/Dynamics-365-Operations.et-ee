---
title: Reeglid
description: See artikkel kirjeldab, kuidas seadistada conventions, et määrata, kuidas kulusid peaks globaalses varude raamatupidamises arvesse võtma.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0055757a0d012896232de58330ee142f702e4ed1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875390"
---
# <a name="conventions"></a>Reeglid

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

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
