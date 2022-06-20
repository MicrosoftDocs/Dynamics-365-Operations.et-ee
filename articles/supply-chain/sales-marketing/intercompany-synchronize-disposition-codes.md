---
title: Likvideerimiskoodide sünkroniseerimine
description: See artikkel selgitab kontsernisisese äri likvideerimiskoodide sünkroonimist
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: d347181dd6ba12de0e114d74d43cd46230ba4fb7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905656"
---
# <a name="synchronize-intercompany-disposition-codes"></a>Likvideerimiskoodide kontsernisisene sünkroniseerimine

[!include [banner](../../includes/banner.md)]

Kontsernisiseste tagastuste toetamiseks on rakendusel Microsoft Dynamics 365 Supply Chain Management funktsioon väliselt määratud likvideerimiskoodide vastendamiseks vastavate siseste likvideerimiskoodidega. Kontserniahela häälestamisel peavad likvideerimistegevused olema kahes teineteisega vastendatud ettevõttes samad. Kui need erinevad, ei õnnestu sünkroniseerimisprotsess.

## <a name="about-disposition-codes-for-three-legged-direct-returns"></a>Teave kolmeharuliste otsetoodangu paigutuskoodide kohta

Likvideerimiskoodid sünkroniseeritakse kontsernisisese müügitellimuse rida algse müügitellimuse reaga. Sünkroniseerimisel on algse müügitellimuse reale vaid üks vahetu mõju. See on nii, et rea lisakulud kustutatakse ettevõttes A seadistatud likvideerimiskoodi ja lisakulude alusel. Ettevõte A on tagastustellimust loov ettevõte.

Komeharulises otsetarne ahela kontsernisisese müügitellimuse real toetatakse kõiki likvideerimistegevusi. Kui toode tagastatakse kliendile, peate te kinnitama, et tagastustellimusel olev tarneaadress vastab esialgses tellimuses määratud kliendi tarneaadressile.

> [!NOTE]
> Ostutellimuste jaoks ei ole likvideerimiskoode. Seepärast tuleb likvideerimiskoodide kontsernisisese müügitellimuse sünkroonimine algse tagastustellimusega teha müügitellimuselt müügitellimusele.

## <a name="replacing-returned-items"></a>Tagastatud kaupade asendamine

Kui tagastatud kaup asendatakse ja ettevõttes B on juba loodud asendustellimus, ei saa valida likvideerimiskoodi ja ettevõttes A ei looda lisaasendustellimust.

## <a name="rules-for-intercompany-direct-deliveries"></a>Kontsernisiseste otsetarnete reeglid

Järgmised üldreeglid kehtivad algsetele tagastustellimustele kontsernisisese otsetarne stsenaariumi korral:

- Kui aluseks olev likvideerimistegevus algsel müügitellimuse real on Krediit ja Jäägid, Krediit või Kliendile tagastamine, rakendatakse Krediidilepingu toimingut. Tagasta kliendile-tegevuskood seadistab olemasoleval real ja kontsernisisese müügitellimuse uuesti sünkroonitud real netosummaks 0 (null). Praagiridu ei sünkroniseerita kunagi. Kui kontsernisisesele müügitellimusele lisatakse rida, ei sünkroniseerita seda kunagi positiivse kogusega müügitellimusega ega praagi likvideerimistegevusega (nt Kreedit ja Praak või Asenda ja Praak).
- Aluseks olevat likvideerimistegevust Kreedit ja Asenda või Praak ja Asenda ei alluta. Seda käsitletakse kui Krediidi ja Asendamise või Praak ja Asendamise likvideerimistegevust. See reegel kehtib ka juhul, kui ettevõttes A ei ole praagirida loodud ja ettevõttes B (tagastatud kauba vastu loonud ettevõte) ei ole loodud ühtegi asendustellimust. Asendustellimus luuakse ettevõttes A ainult siis, kui värskendatakse saatelehte.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
