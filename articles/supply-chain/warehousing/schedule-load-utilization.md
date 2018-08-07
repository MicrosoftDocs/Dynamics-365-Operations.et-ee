---
title: Koormuse tulususe planeerimine
description: Selles teemas selgitatakse, kuidas seadistada ja planeerida lao koormust.
author: MarkusFogelberg
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSSpaceUtilSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d52ad452c615a61739582431fcd100a7efa3d93a
ms.openlocfilehash: 350666cee8f2643c53e9eed8ee73299bbea1e757
ms.contentlocale: et-ee
ms.lasthandoff: 04/26/2018

---

# <a name="schedule-load-utilization"></a>Koormuse tulususe planeerimine

[!include[banner](../includes/banner.md)]

Saate ajastada koormuse kasutamise valitud asukohatüüpide jaoks ning kavandada praegust ja tulevast koormuse kasutamist. Saate kavandada koormust ühe või mitme laoala, koormuse üksuste (tsoon või ladu) või tsooni ja lao kombinatsiooni jaoks.

## <a name="schedule-and-view-the-load-for-a-warehouse-or-site"></a>Lao või saidi koormuse ajastamine ja vaatamine

Koormuse ajastamiseks saitidele, ladudele või tsoonidele peate looma ruumikasutuse seadistuse ja seostama selle koondplaaniga.

Ruumikasutuse seadistamisel kasutage asukohatüüpe, nt **Hulgiasukoht** ja **Komplekteerimiskoht**, et määrata, kuidas tuleb ruumikasutust kavandada. Saate ka määrata ladustamise koormuse režiimi, näiteks **Tsoon**.

Tulevase ruumikasutuse kavandamise aluseks on teave, mis arvutatakse seotud koondplaanis. Koondplaanid prognoosivad ressursside kavandamist sissetulevate ja väljaminevate tellimuste jaoks tootmises ja operatsioonides. Saadaoleva ruumi prognoos põhineb ruumi kasutamise seadistuse ja valitud koondplaani suhtel.

Ruumikasutuse seadistuses valitud ladustamise koormuse režiimi kasutades saate määrata, kas koormus tuleb kavandada iga lao või tsooni jaoks või kas kavandamisel peab kaasama korraga nii ladude kui ka tsoonide teabe. Saate ka määrata, kas blokeeritud asukohad tuleks koormuse kasutamise arvutamisest välja jätta.

Saate kavandada ruumikasutuse, luues aruande **Lao koormuse kasutus**. Selle aruande loomisel saate määrata, kas koormuse kasutamine tuleb prognoosida iga saidi kohta, kõigi saitide kohta või valitud koormuse üksuse kohta, näiteks tsoon või ladu.

### <a name="create-a-space-utilization-setup-for-a-warehouse"></a>Ruumi kasutamise seadistuse loomine lao jaoks

1. Valige **Varude haldamine** \> **Seadistamine** \> **Lao jälgimine** \> **Ruumikasutus**.
2. Valige suvand **Uus**, et luua ruumikasutusele seadistus. Määrake uuele seadistusele ID ja nimi.
3. Väljas **Ladustamise koormuse režiim** valige, kas ruumikasutuse ülevaade peaks kuvama teavet lao, tsooni või mõlema järgi.
4. Määrake suvandi **Blokeeritud asukohtade välistamine** valikule **Jah**, et välistada blokeeritud lao asukohad vaba ruumi arvutusest. Saate blokeerida lao asukoha sissetulekute ja väljaminekute puhul, määrates asukoha blokeerimise põhjuse lehe **Lao asukohad** kiirkaardi **Muu** väljas **Saabumine blokeeritud** või **Väljastus blokeeritud**.
5. Valige kiirkaardil **Asukoha tüüp** asukohatüübid kaasamiseks ruumikasutuse arvutamisse. Peate prognoosimiseks valima vähemalt ühe asukohatüübi.

### <a name="associate-a-space-utilization-setup-with-a-master-plan"></a>Ruumi kasutamise seadistuse seostamine koondplaaniga

1. Valige **Varude haldamine** \> **Perioodilised ülesanded** \> **Koormuse tulususe planeerimine**.
2. Valige koondplaan väljalt **Koondplaan**.
3. Määrake väljal **Päevade arv** praeguse ja tulevase töökoormuse prognoosi kaasatavate päevade arv.
4. Valige väljal **Ruumikasutus** ruumikasutuse seadistus, mida kasutada praeguste ja tulevaste töökoormuste prognoosimisel.

### <a name="specify-the-load-utilization-projection-and-view-information"></a>Koormuse kasutamise prognoosimise määratlemine ja teabe kuvamine

1. Valige **Varude haldamine** \> **Päringud ja aruanded** \> **Füüsiliste varude aruanded** \> **Lao koormuse tulusus**.
2. Valige väljal **Kuvamisalus:** ruumikasutuse prognoosi tase.

    - **Tegevuskoht** – kavandab ruumikasutuse iga tegevuskoha kohta. See prognoos on kasulik, kui näiteks soovite vaadata saidi kõiki ladusid, et tasakaalustada ruumi kasutamist ladude vahel.
    - **Koormuse üksus** – kavandage ruumikasutus tsoonide või ladude jaoks. Vaba ruum kavandatakse seejärel lehe **Ruumikasutus** väljal **Ladustamise koormuse režiim** valitud väärtuse järgi, kui lõite ruumikasutuse seadistuse.

3. Järgige üht alltoodud etappidest, lähtudes väärtusest, mille valisite eelmises etapis.

    - Kui valisite väärtuse **Tegevuskoht** väljal **Kuvamisalus:**, on saadaval väli **Tegevuskoht**. Valige üks või mitu tegevuskohta prognoosi kaasamiseks.
    - Kui valisite väärtuse **Koormuse üksus** väljal **Kuvamisalus:**, on saadaval väli **Koormuse üksus**. Valige koormuse üksus.

4. Valige väljal **Koormuse tüüp** suvand **Maht** või **Kaal**, et määrata lao tootmisüksus, mille jaoks ruumi kavandatakse.
5. Väljal **Ruumikasutuse seadistamine** valige ruumikasutuse seadistus, mille alusel prognoos tuleb teha.

