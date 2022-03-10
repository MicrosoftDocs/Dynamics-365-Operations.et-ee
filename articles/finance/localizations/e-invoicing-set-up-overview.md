---
title: Elektroonilise arveldamise seadistus
description: Selles teemas antakse ülevaade protsessist elektroonilise arvelduse seadistamiseks ja konfigureerimiseks.
author: dkalyuzh
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8138c63e9eff1d2ca934f9d4467e4e3b73dae941
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371870"
---
# <a name="electronic-invoicing-setup"></a>Elektroonilise arveldamise seadistus

[!include [banner](../includes/banner.md)]

Teema annab ülevaate protsessist elektroonilise arvelduse seadistamise ja konfigureerimise kohta. Seadistuse etapid tuleb lõpetada siin määratud järjestuses. Kui samm on kohustuslik, kuid te selle vahelejätte, ei tööta funktsioon õigesti ja mitme tõrke ilmneb järgmiste sammude ajal või funktsiooni kasutamisel. 

Enne alustamist veenduge, et kõik põhikomponendid on õigesti seadistatud, et olete registreeritud regulatiivsesse konfigureerimisteenusesse (RCS) ja teil on RCS-i eksemplar ning et elektroonilise arveldamise lisandmoodul on installitud teie Microsofti Dynamics 365 Finance Dynamics 365 Supply Chain Management või keskkonna jaoks. Lisateavet vt Jaotisest Elektroonilise [arveldamise allkiri ja installimine](e-invoicing-install-add-in-microservices-lcs.md).

Seejärel seadistage Azure'i ressursid, mida elektrooniline arveldamine nõuab oma töö jaoks. Lisateavet vt Azure'i [ressursside seadistamine elektrooniliseks arveldamiseks](e-invoicing-set-up-azure-resources.md).

Pärast põhikomponentide konfigureerimist töötage koos RCS-iga, et seadistada elektroonilise arveldamise põhikomponendid. Kõigepealt määrake säilitate teenuskeskkondade arvu. Sel viisil määrate loogilised andmed ja konfiguratsiooni sektsioonimise, et veenduda arendus- või katsekeskkonna ja tootmiskeskkondade piiris. Oma arendusprotsessi paindlikuks seadistamiseks võite vajada mitut eraldi arendus- ja katsekeskkonda. Lisaks teenusekeskkonna määratlemisele seadistage link oma ärirakendustele, nt finants- või tarneahela haldus, otse RCS-st, et seadistada parameetrid, mis on vajalikud elektroonilise arveldamise õigeks toiminguks. Lisateavet keskkonna kohta vt teenuse [keskkondadest](e-invoicing-service-environments.md).

Pärast kõige seadistamist saate luua oma globaliseerimisfunktsioonid, mis määratlevad erinevad stsenaariumid elektrooniliste dokumentide töötlemiseks ja andmete teisendamiseks, või importida dokumente globaalsest hoidlast. Lisateavet globaliseerimisfunktsiooniga töö kohta vt " [Globaliseerimisfunktsioonid"](e-invoicing-working-globalization-features.md).

Lisateavet konveierite töötlemistoimingute kohta, mis koosnevad protsessist, mille te globaliseerimisfunktsioonis koostate, vt **[COMPLETE!: Document processing actions]**.

Kui teie stsenaariumid vajavad integreerimist meiliga SharePoint või sissetulevate elektrooniliste dokumentide töötlemist, [vaadake](e-invoicing-process-incoming-electronic-documents.md) sissetulevate elektrooniliste dokumentide töötlemist, et saada teavet nende kanalite häälestamise ja kasutamise kohta.
