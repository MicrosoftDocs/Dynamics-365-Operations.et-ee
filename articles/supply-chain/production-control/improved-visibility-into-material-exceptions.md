---
title: Materjalierandite nähtavus
description: See teema kirjeldab, kuidas saate parandada tootmistellimuste ja partiitellimuste puhul toormaterjalide erandite nähtavust.
author: johanhoffmann
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgShopSupervisorWorkspace, WHSProdWaveTableListPage, WHSProdWaveTableManageBOMPool
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: d3ea260535e76d7ac3d73d4bca930b7b4b2d22b2b2c076d4d1346785eaed85b8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726797"
---
# <a name="visibility-into-material-exceptions"></a>Materjalierandite nähtavus

[!include [banner](../includes/banner.md)]

Tööruumis **Tootmisosakonna haldus** pakuvad kolm paani teile tootmistellimuste ja partiitellimuste toormaterjalide eranditele paremat nähtavust.

- Tähelepanu vajavad väljastamata koosluseread
- Tähelepanu vajavad töötlemata vood
- Tähelepanu vajav avatud laotöö

Kõigi kolme paani puhul võrreldakse koosluseridade ja valemiridade toormaterjali kuupäeva tööruumi kuupäeva ning filtritega **Tootmisüksus**, **Ressursigrupp** ja **Ressurss**, mis on määratud menüüs **Minu tööruumi konfigureerimine**. Vaikimisi on tööruumi kuupäevaks seatud praegune kuupäev, kuid saate seda reguleerida.

Väljastamata koosluse- või valemirida nõuab tähelepanu, kui rea toormaterjali kuupäev on sama või varasem kui tööruumi kuupäev ja kui see vastab tööruumi filtritega määratletud kriteeriumidele.

Järgmisel joonisel kujutab sinine riba ressursile planeeritud tootmistööd. Töö alguseks on planeeritud 1. mai 2017 (2017/05/01). See kuupäev on toormaterjali kuupäev. Teisisõnu peavad koosluse- ja valemiridadel olevale tööle määratud materjalid olema selleks kuupäevaks valmis. Teine kuupäev joonisel, 6 mai 2017 (2017/05/06), tähistab tööruumi kuupäeva. Selles näites on toormaterjali kuupäev varasem kui tööruumi kuupäev. Seega on toormaterjali tarbimise planeeritud alguskuupäev möödas ning koosluse- ja valemiread vastavad tähelepanu nõudmise kriteeriumidele.

![Tootmistöö näide, kus toormaterjali kuupäev on varasem kui tööruumi kuupäev.](./media/improved-visibility.png)

## <a name="unreleased-material-lines-needing-attention"></a>Tähelepanu vajavad väljastamata koosluseread

Koosluse- või valemirea lattu väljastamiseks on kolm võimalust.

- Tootmistellimuse või partiitellimuse väljastamise osana
- Käsitsi väljastamisena
- Pakett-töö kaudu automaatselt

Lisateavet vt teemast [Koosluse- ja valemiridade lattu väljastamine](releasing-bom-and-formula-lines-to-warehouse.md). 

Kui koosluse- või valemirida pole väljastatud või on ainult osaliselt väljastatud ja tööruumi kuupäeva ning filtreerimiskriteeriumid on täidetud, kaasatakse rida paanil **Tähelepanu vajavad väljastamata materjali read** kuvatava arvu arvutusse.

Paani valimisel avaneb leht **Lattu väljastamine**. Sellel lehel kuvatakse väljastamata koosluse- ja valemiridade arv, mis on näidatud numbriga paanil. Väljastamata read kuvatakse ülemises ruudustikus. Selles ruudustikus kuvatakse rea jaoks algselt hinnatud kogus, juba väljastatud kogus ja veel väljastamist vajav järelejäänud kogus. Saate lisada ridu ülemisest ruudustikust alumisse ruudustikku. Seejärel saate valitud read alumisest ruudustikust lattu väljastada. Alumises ruudustikus saate korrigeerida ka väljastatavat kogust, nii et väljastatakse ainult osaline kogus.

## <a name="unprocessed-waves-needing-attention"></a>Tähelepanu vajavad töötlemata vood

Koosluse- või valemirea väljastamisel lisatakse see kas uute tootmisvoogu või olemasolevasse avatud voogu olenevalt tootmisvoo malli konfiguratsioonist. Voomalli konfiguratsiooni kaudu saate voo seadistada ka nii, et seda töödeldakse koosluse- või valemirea väljastamisel automaatselt. Kui voog on töödeldud, luuakse laotöö toormaterjali komplekteerimiseks. Kui voomall on konfigureeritud nii, et voogusid väljastamise ajal ei töödelda, jääb voog töötlemata olekusse. Paanil **Tähelepanu vajavad töötlemata vood** kuvatakse koosluse- ja valemiridade arv, mis on väljastatud lattu töötlemata voogudes ja mille toormaterjali kuupäev on varasem või sama kui tööruumi kuupäev. Ridu peab tarbima ka toiminguressurss, kes rakendab tööruumile filtri.

Paani valimisel avaneb leht **Kõik tootmisvood**. See leht on filtreeritud avatud voogude arvu järgi, mis sisaldavad vooridu paani kriteeriumidele vastavatelt väljastatud koosluse- ja valemiridadelt.

### <a name="manually-maintain-production-waves"></a>Tootmisvoogude käsitsi hooldamine

**Kõik tootmisvood** lehel saate kasutada tegevuspaani vahekaardi **Voog** nuppe, et voogu käsitsi **töödelda** ja **välja anda**. Saate kasutada ka valikut **Säilita tootmised**, et vaadata ja säilitada **tootmise kooslusekausta** andmeid, mida kasutatakse voo protsessi töötlemiseks.

## <a name="open-warehouse-work-needing-attention"></a>Tähelepanu vajav avatud laotöö

Paanil **Tähelepanu vajav avatud laotöö** kuvatakse koosluse- ja valemiridade arv, mis on väljastatud lattu töötlemata voogudes, mis sisaldavad töötlemata tööd ja mille toormaterjali kuupäev on varasem või sama kui tööruumi kuupäev. Ridu peab tarbima ka toiminguressurss, kes rakendab tööruumile filtri.

Paani valimisel avaneb leht **Kõik tööd**. See leht on filtreeritud avatud tööpäiste arvu järgi, mis sisaldavad tööridu paani kriteeriumidele vastavatelt väljastatud koosluse- ja valemiridadelt. Lehel **Kõik tööd** saate tööd käsitsi töödelda.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]