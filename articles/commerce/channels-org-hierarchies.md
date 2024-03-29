---
title: Organisatsiooni hierarhiate häälestus
description: See artikkel kirjeldab, kuidas seadistada organisatsiooni hierarhiaid Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 2555378c119e4c096c4bf0c0adc11e3a50cbfe38
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280443"
---
# <a name="set-up-organization-hierarchies"></a>Organisatsiooni hierarhiate häälestus

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas seadistada organisatsiooni hierarhiaid Microsoft Dynamics 365 Commerce.

Enne kanalite loomist peate veenduma, et teie organisatsiooni hierarhiad on seadistatud.

Saate kasutada organisatsiooni hierarhiaid oma äri vaatamiseks ja selle aruandluse tegemiseks erinevatest aspektidest. Näiteks saate seadistada ühe hierarhia maksu-, õigus- või seadusliku aruandluse jaoks. Seejärel saate seadistada teise hierarhia finantsteabe aruandluseks, mis ei ole õiguslikult vajalik, kuid mida kasutatakse sisemises aruandluses.

Enne organisatsiooni hierarhia loomist tuleb luua organisatsioonid. Lisateabe saamiseks vaadake jaotist [Juriidiliste isikute loomine](channels-legal-entities.md) või [Tootmisüksuste loomine](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).


Lisateavet vt järgmistest artiklitest.
- [Organisatsioonide ja organisatsioonihierarhiate ülevaade](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [Organisatsiooni hierarhia kavandamine](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [Organisatsioonihierarhia loomine](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a>Organisatsioonihierarhia loomine

Organisatsiooni hierarhia loomiseks toimige järgmiselt.

1. Avage navigeerimispaanilt **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Organisatsiooni hierarhiad**.
1. Valige toimingupaanil nupp **Uus**.
1. Sisestage väärtus väljale **Nimi**.
1. Jaotises **Eesmärk** valige **Määra eesmärk**.
1. Otsige loendist ja valige soovitud kirje. Valige organisatsiooni hierarhiale määratav eesmärk.
1. Jaotises **Määratud hierarhiad** valige **Lisa**.
1. Märkige loendis valitud rida. Otsige äsja loodud hierarhia üles.
1. Valige nupp **OK**.

Järgmine pilt näitab organisatsiooni hierarhia näidet, mis on loodud fiktiivsete "Adventure Works" kauplusteketi jaoks.

![Organisatsiooni hierarhia näide.](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a>Organisatsioonide lisamine hierarhiasse

Hierarhiale organisatsioonide lisamiseks toimige järgmiselt.

1. Otsige loendist ja valige soovitud kirje. Valige hierarhia.
1. Valige tegevuspaanil nupp **Kuva**.
1. Vajaduse korral lisage organisatsioone.
1. Organisatsiooni lisamiseks valige **Redigeerige** ja seejärel valige **Lisa**. Kui olete muudatuste tegemise lõpetanud, saate salvestada mustandi ja muudatused avaldada.

Järgmine pilt näitab hierarhia juurele lisatud juriidilist isikut nelja lisatud kulukeskusega kanalitele "Ostukeskus", "Outlet-pood", "Veeb" ja "Kõnekeskus". Seejärel saab igale lisada erinevaid jaemüügi-, kõnekeskuse- ja veebikanaleid.

![Hierarhia kujundaja näide.](media/hierarchy-designer.png)

## <a name="additional-resources"></a>Lisaressursid

[Organisatsioonide ja organisatsioonihierarhiate ülevaade](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Organisatsioonihierarhia kavandamine](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Juriidiliste isikute loomine](channels-legal-entities.md)

[Tootmisüksuste loomine](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[Kanalite ülevaade](channels-overview.md)

[Kanali seadistamise eeltingimused](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
