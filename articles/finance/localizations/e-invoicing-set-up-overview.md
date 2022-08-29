---
title: Elektroonilise arveldamise seadistus
description: See artikkel annab ülevaate protsessist elektroonilise arvelduse seadistamiseks ja konfigureerimiseks.
author: gionoder
ms.date: 02/28/2022
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
ms.openlocfilehash: de94843c1e98a8788375bd41def587a64baea07d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272175"
---
# <a name="electronic-invoicing-setup"></a>Elektroonilise arveldamise seadistus

[!include [banner](../includes/banner.md)]

Artikkel annab ülevaate protsessist elektroonilise arvelduse seadistamise ja konfigureerimise kohta. Seadistuse etapid tuleb lõpetada siin määratud järjestuses. Kui samm on kohustuslik, kuid te selle vahelejätte, ei tööta funktsioon õigesti ja mitme tõrke ilmneb järgmiste sammude ajal või funktsiooni kasutamisel. 

Enne alustamist veenduge, et kõik põhikomponendid on õigesti seadistatud, et olete registreeritud regulatiivsesse konfigureerimisteenusesse (RCS) ja teil on RCS-i Microsoft Dynamics eksemplar ning et elektroonilise arveldamise lisandmoodul on installitud teie 365 Dynamics 365 Supply Chain Management Finantsi või keskkonna jaoks. Lisateavet vt Jaotisest Elektroonilise [arveldamise allkiri ja installimine](e-invoicing-install-add-in-microservices-lcs.md).

Seejärel seadistage Azure’i ressursid, mida elektrooniline arveldamine nõuab oma töö jaoks. Lisateavet vt Azure’i [ressursside seadistamine elektrooniliseks arveldamiseks](e-invoicing-set-up-azure-resources.md).

Pärast põhikomponentide konfigureerimist töötage koos RCS-iga, et seadistada elektroonilise arveldamise põhikomponendid. Kõigepealt määrake säilitate teenuskeskkondade arvu. Sel viisil määrate loogilised andmed ja konfiguratsiooni sektsioonimise, et veenduda arendus- või katsekeskkonna ja tootmiskeskkondade piiris. Oma arendusprotsessi paindlikuks seadistamiseks võite vajada mitut eraldi arendus- ja katsekeskkonda. Lisaks teenusekeskkonna määratlemisele seadistage link oma ärirakendustele, nt finants- või tarneahela haldus, otse RCS-st, et seadistada parameetrid, mis on vajalikud elektroonilise arveldamise õigeks toiminguks. Lisateavet keskkonna kohta vt teenuse [keskkondadest](e-invoicing-service-environments.md).

Pärast kõige seadistamist saate luua oma globaliseerimisfunktsioonid, mis määratlevad erinevad stsenaariumid elektrooniliste dokumentide töötlemiseks ja andmete teisendamiseks, või importida dokumente globaalsest hoidlast. Lisateavet globaliseerimisfunktsiooniga töö kohta vt " [Globaliseerimisfunktsioonid"](e-invoicing-working-globalization-features.md).

Kui teie stsenaariumid vajavad integreerimist meiliga SharePoint või sissetulevate elektrooniliste dokumentide töötlemist, [vaadake](e-invoicing-process-incoming-electronic-documents.md) sissetulevate elektrooniliste dokumentide töötlemist, et saada teavet nende kanalite häälestamise ja kasutamise kohta.
