---
title: Makseviisid kõnekeskustes
description: Selles teemas kirjeldatakse erinevaid makseviise, mida saate Dynamics 365 Commercei kõnekeskuses kasutada.
author: josaw1
manager: AnnBe
ms.date: 03/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCRSalesTableOrderHistory, MCRCCAuthManagement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 92163
ms.assetid: 8e738907-870b-466c-ab0c-07f4a4aa47f3
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e7636f5c664634c680edf2ff9d8bae5ebb9035af
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411689"
---
# <a name="payment-methods-in-call-centers"></a>Makseviisid kõnekeskustes

[!include [banner](includes/banner.md)]

Rakenduses Dynamics 365 Commerce sisaldab kõnekeskuse kanali konfiguratsioon sätet nimega **Tellimuse lõpetamise lubamine**. See säte aitab tagada, et kõik tellimused, mille kanali kasutajad loovad, väljastatakse tellimuse töötlemisse ainult juhul, kui neil on ettemakstud või eelautoriseerida makse, mis on kinnitatud piirides. Kui säte **Tellimuse lõpetamise lubamine** on sisse lülitatud, saavad kõnekeskuse kasutajad sisestada klientide müügitellimuste makseid, kasutades kõnekeskuse makse töötlemise funktsioone. Kui säte on välja lülitatud, ei saa kõnekeskuse kasutajad kõnekeskuse makse töötlemise funktsioone kasutada, kuid nad saavad siiski müügitellimustele ettemakseid rakendada, kasutades standardset müügireskontro funktsiooni.

Kanali konfiguratsiooni osana saab ettevõte määratleda makseviisid, mis on kõnekeskuse kanalil lubatud. Kõnekeskuse kanal kasutab samu makseviise, mis on määratletud poe kanalite jaoks.

Kõnekeskuse kanali maksemeetodite konfigureerimiseks avage **Jaemüük ja kaubandus** \> **Kanalid** \> **Kõnekeskused** \> **Kõik kõnekeskused** ja seejärel valige menüüs **Seadista** suvand **Makseviisid**.

Makseviisi loomisel saate määrata viis makseviisi funktsiooni.

| Funktsioon            | Kirjeldus |
|---------------------|-------------|
| Tavaline              | Kasutage oma makseviisis funktsiooni **Tavaline**, kui määratlete makseviise, nagu sularaha või kanded. Kõnekeskuses seda tüüpi makseviiside rakendamisel müügitellimusele määratakse lipu **Ettemaks** vaikeolekuks **Jah**. See postitab tellimuse esitamisel kohe ettemaksekande kliendikontole. Kasutajad võivad soovi korral lipu **Ettemaks** olekuks määrata **Ei**, et maksekannet ei loodaks enne arve sisestamist. Ettemaksekanne sisestatakse kliendikannete ajalukku, kus see tasakaalustatakse süstemaatiliselt müügitellimuse arvega. |
| Kontrolli               | Kasutage funktsiooni **Kontrolli**, kui määratlete makseviisina pangatšeki. Kui müügitellimusele rakendatakse see maksetüüp, peab kasutaja maksuavalduse töötlemise osana sisestama kliendi tšekinumbri. Tšekimakseid käsitletakse nende rakendamisel alati ettemaksetena ja maksekanded luuakse kohe tellimuse esitamisel. Need ettemaksekanded tasakaalustatakse süstemaatiliselt tellimuse jaoks loodud arvetega. |
| Kaardid               | Kaardimakse tüübid esindavad mis tahes maksetüüpi, mille jaoks tuleb sisestada kaardi number, mis on määratletud kliendi maksekaardil. Näiteks on krediitkaardid ja kinkekaardid. Seda tüüpi maksete konfigureerimisel peate kasutama menüüd **Kaardi häälestus**, et määratleda selle makseviisiga seostatud kaardi ID-d. Tellimuse sisestamise ajal saavad kasutajad määrata, kas kaardimakse on ettemakse, kasutades suvandit **Ettemaks**, mis kuvatakse maksekande lehel. Kui ettevõtte ei nõua ettemakseid, on krediitkaardimakse tavapärane voog kaheastmelise protsess, kus tellimuse sisestamise ajal saadakse luba ning seejärel tasakaalustatakse arveldamisel makse ja võetakse see kliendi kaardilt. Kinkekaardimaksete korral on ettemakse soovitatav, sest kinkekaardi saldot tuleks vähendada kohe, et klient ei saaks sama väärtust rakendada mujal. |
| Klient            | Makseviisi funktsioon **Klient** tähendab, et makse rakendatakse kliendi krediidilimiidile või pannakse ettemaksele. Rakenduses Commerce saab klient määrata krediidilimiidi, mille saab kinnitada tellimuse sisestamise ajal. Maksed, mis tehakse makseviisiga, mis on seotud funktsiooniga **Klient**, loovad kliendikonto suhtes kohustuse. Seejärel kuvatakse müügitellimuse arveldamisel deebetsaldo. Sellistel juhtudel saadavad kliendid tavaliselt makse esitatud tingimuste kohaselt. Teise võimalusena saab tähtajani jõudnud saldo tasakaalustamiseks rakendada eelmise avatud kreeditkande kliendi kontol. Pange tähele, et isegi juhul, kui määrate selle makseviisi, ei kuvata seda kõnekeskuse tellimuse kirjes maksevalikute all, kui te pole kliendi, kellega töötate, kirjel märkinud lippu **Ettemaksu lubamine**. Selle lipu leiate kliendikirje vahekaardil **Makse vaikeandmed**. |
| Väljamakse-/vahetusraha | Funktsiooni **Väljamakse-/vahetusraha** kõnekeskus ei kasuta. See on rakendatav ainult siis, kui määratlete makseviisid, mida kassarakendus kasutab kaupluse kanalil. |

Makseviiside määratlemisel tuleb need siduda pearaamatu või pangakontoga. Kui jätate selle etapi vahele, kuvatakse kasutajatel makseviisi salvestamisel tõrked.

## <a name="refund-payment-methods"></a>Tagasimakse viisid

Tagasimakse töötlemise stsenaariumides kasutab kõnekeskus osasid makseviise, mis on määratletud valikus Müügireskontro. Nende makseviiside konfigureerimiseks avage **Jaemüük ja kaubandus** \> **Kanali häälestus** \> **Kõnekeskuse seadistamine** \> **Kõnekeskuse tagasimakseviisid**. Kliendi tagasimakse kontrollide töötlemiseks peate selle konfiguratsiooni lõpule viima. Näiteks, kui klient tasus algselt tellimuse eest sularahas või tšekiga, võib kasutaja soovida saata kliendile tagasimakse tšeki valiku Müügireskontro kaudu. Sel juhul tuleb sularaha ja tšekiga makseviisid kõnekeskuses vastendada õige makseviisiga valikus Müügireskontro, et tagada, et tagasimakse töödeldakse õigesti.

Lisaks, kui kasutaja töötleb tagastustellimust kõnekeskuse kasutajana rakenduses Commerce, kuid ta ei saa tagastust siduda algse müügiga, tuleb kõnekeskuse parameetrites määratleda makseviis **Tagastus**. Avage **Jaemüük ja kaubandus** \> **Kanali häälestus** \> **Kõnekeskuse seadistamine** \> **Kõnekeskuse parameetrid** ja seejärel vahekaardil **RMA/Tagastus** väljal **Makseviis** veenduge, et makseviis oleks määratletud. See makseviisi on makseviis, mida kasutatakse tagastuste tegemiseks. Tavaliselt on see määratletud tšeki meetodi või kliendikonto meetodina.
