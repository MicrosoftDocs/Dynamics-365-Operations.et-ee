---
title: Kliendiserdid ja -saladused
description: See artikkel selgitab, kuidas seadistada kliendi serte ja saladusi elektroonilises arveldamises.
author: gionoder
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 3943e7cb43cc6bf93995f0b3957766227cc3ec99
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279836"
---
# <a name="customer-certificates-and-secrets"></a>Kliendiserdid ja -saladused

[!include [banner](../includes/banner.md)]

Kui teil on juba Microsoft Azure regulatiivses konfiguratsiooniteenuses (RCS) võtme hoidla viide, saate luua viiteid võtme vaultsertifikaatidele ja saladustele. Kui teil ei ole veel võtme hoidla viidet, [vaadake](e-invoicing-service-environments.md) selle loomise kohta teenuse keskkondi.

## <a name="create-certificates-and-secrets"></a>Sertide ja saladuste loomine

Sertide ja saladuste loomiseks ja häälestamiseks järgige neid samme.

1. Logige oma RCS-i kontole sisse.
2. Tööruumis **Globaliseerimisfunktsioonid** jaotises **Keskkond** valige paan **Elektrooniline arveldus**.
3. **Valige tegevuspaanil** Keskkonna häälestuslehelt **teenusekeskkonnad**.
4. Teenuse keskkondade **lehel**, valige tegevuspaanil võtme **hoidla parameetrid**.
5. **Lehel Võtme hoidla parameetrid** valige võtme vaultviide ja seejärel **valige jaotises Sertifikaadid** suvand **Lisa**.
6. Sisestage **väljale** Nimi võtme vaultsertifikaadi või saladuse nimi. Lisateavet vt Azure’i [ladustamiskonto loomine Azure’i portaalis](e-invoicing-create-azure-storage-account-azure-portal.md).
7. Väljale **Kirjeldus** sisestage kirjeldus.
8. **Väljal Tüüp** valige **sert**, kui viitate võtmehoidlas talletatavale serdile. Valige **suvand** Saladus, kui viitate võtme varas talletatavale saladusle.
9. Valige käsk **Salvesta**.

> [!NOTE]
> Mõnes stsenaariumis peate kasutama tunnistusi, mille .cer failinime laiend on. Võti Vault ei toeta aga seda tüüpi sertide importimist ja salvestamist võtme vaultsertifikaatidena. Sellistes stsenaariumides peaksite salvestama Cer-faili Base-64-kodeeritud X.509 (. CER) string. Seejärel salvestage võtme Vault saladuses string **, mis ilmub failis BEGIN-serdi** **rea ja END-tunnistuse** rea vahele. Teenuse keskkonnas peaksite siiski looma viite võtme hoidlakirjele ja seadistama **välja Tüüp väärtuseks** **Sert**.

## <a name="create-a-chain-of-certificates"></a>Sertide ahela loomine

Kui teie riigi-/regiooniomased arved nõuavad sertifikaatide ahelat, et rakendada digitaalallkirju või luua väliste veebiteenustega turvaline (Secure Sockets Layer \[SSL\]) ühendus, looge sertide kett järgmises järjekorras:

1. Juursertifikaadid
2. Vahesertifikaadid
3. Lõppkasutaja sertifikaadid

Juursertifikaadi asutused on usaldusväärsed sertide allikad. Vahe-CA-tunnistused on vahesillad, mis seovad lõppkasutaja tunnistused juur-CA-sertidega.

Sertifikaatide ahela loomiseks ja häälestamiseks järgige neid samme.

1. Tegevuspaanil **oleva võtme** hoidla parameetrite lehel valige **sertide ahel**.
2. Serdiahela loomiseks valige **Uus**.
3. **Sisestage** sertifikaatide ahela nimi väljale Nimi.
4. Väljale **Kirjeldus** sisestage kirjeldus.
5. Valige jaotises **Serdid** käsk **Lisa**, et ahelale sert lisada.
6. Kasutage nuppu **Üles** või **Alla**, et ahelas serdi asukohta muuta. Säilitage CA juursertifikaat loendi ülaosas ja lõppkasutaja sert allosas.
7. Valige käsk **Salvesta**.

Saate luua RCS-i nii palju võtme vaultviiteid, kui soovite. Pidage meeles, et ühise salvestuse ühiskasutuses juurdepääsu allkirja (SAS) loa saladust kasutatakse antud teenusekeskkonna seostamiseks võtme hoidla viitega. Saate viidata võtme vaultsertifikaatidele ja saladustele, mis on talletatud võtmehoidlas, mis sisaldab ka salvestus-SAS-i loa saladust, mida kasutate teenusekeskkonna häälestamisel.
