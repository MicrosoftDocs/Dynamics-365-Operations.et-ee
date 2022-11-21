---
title: Ettemaksed Dynamics 365 Commerce
description: See artikkel annab ülevaate ettemaksukannete töötlemisest valuutas Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-06-28
ms.openlocfilehash: 8262470f83481ef8840857a52948c0833d8b278e
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780199"
---
# <a name="prepayments-in-dynamics-365-commerce"></a>Ettemaksed Dynamics 365 Commerce

[!include[banner](../includes/banner.md)]

See artikkel annab ülevaate ettemaksukannete töötlemisest valuutas Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce töötleb ettemaksukandeid järgmiste maksetüüpide puhul, mida kasutatakse müügireskontros või äris:

- **Kliendikonto deposiidimakse** – klient maksab kassas deposiidi. Commerce töötleb deposiidimakset ettemaksukandena. Kande sisestamisel luuakse ja sisestatakse maksetööleht **Commerce Headquartersi töölehe kande** lehele. Ettemaksu **töölehekande** märkeruut vahekaardil **Makse** valitakse automaatselt makse töölehele. Lisateavet, sh ettemakse- ja maksuteavet, mis on sihtpiirkonnale oluline, [vt globaliseerimisressursse – riigi-/regiooniomast spikrisisu](/dynamics365/fin-ops-core/dev-itpro/lcs-solutions/country-region?context=%2Fdynamics365%2Fcontext%2Ffinance#countryregion-specific-help-content).
- **Kliendi tellimus, kus on deposiit** – klient loob müügikohas klienditellimuse. Klient saab maksta tellimuse deposiidi, mis põhineb **rakenduse** Commerce headquarters klienditellimuste lehel (**Äriparameetrid \> Kliendi tellimused) konfigureeritud deposiidi vaikeprotsendil**. Commerce töötleb klienditellimuse deposiidimakseid ettemaksukandena. Kande sisestamisel luuakse ja sisestatakse maksetööleht töölehe kande **lehele**. Ettemaksu **töölehekande** märkeruut vahekaardil **Makse** valitakse automaatselt makse töölehele. Makse tasakaalustatakse ja kliendiarve väljastatakse tellimuse peale- või tarnimisel automaatselt.
- **Kõnekeskuse müügitellimus** – kõnekeskuse **·** **klienditeeninduse** esindaja loob kliendi eest müügitellimuse ja ettemakse atribuudi väärtuseks seatakse Makse hõivamise ajal Jah.

Commerce teeb ettemakse töötlemiseks järgmisi toiminguid:

- **Kliendikonto deposiidimakse** töötlemine – deposiidimakse, mille klient teeb, kantakse Ärisse üle andmesünkroonimisteenuse abil. Commerce loob makse jaoks jaemüügi maksekande. Kui sisestate jaemüügikande, sisestatakse sularahatööleht või kliendi maksetööleht. Commerce **headquartersi** Töölehekande lehe **Makse** **vahekaardil** Makse on maksetöölehe jaoks automaatselt valitud ettemaksu töölehe kande märkeruut. Ettemakseid ei saa töödelda, kui maksesumma on negatiivne.
- **Kliendi tellimuse või müügitellimuse, mil** on deposiit – klient maksab kliendi tellimuse eest nõutava deposiidi, kasutades Commerce Data Exchange selleks : Real-time Service. Commerce loob kliendi maksetöölehe või sularahatöölehe, sõltuvalt kliendi kasutatavast makseviisist. Töölehekande **lehe** Makse vahekaardil Makse **märkeruut** **valitakse** automaatselt töölehe jaoks Commerce headquartersis. Kui klient kasutab osamaksete tegemiseks mitut makseviisi, töötleb Commerce iga osamakse, mis põhineb kasutatud makseviisil.

Krediitkaartide ja digitaalsete deebetsummade puhul, mille krediitkaardi makseviisid on aluseks, saadab Commerce pärast edukat autoriseerimist "hõivamise" taotluse. (Fondid fikseeritakse enne müügitellimuse arveldamist.)

Kui tühistate kliendi tellimuse, makstakse ettemakse summa tagasi ja makse tagasimakse tööleht sisestatakse deposiidisummale. Tagasimakse summa arvutatakse ja sisestatakse makseviisi alusel, mille määrate tagasimakse sisestamisel. Commerce võib rakendada tühistamistasu, mis põhineb **Commerce headquartersi commerce’i parameetrite** lehel seadistatud protsendimääral.

Klienditellimuse tagastamisel luuakse tagastustellimus ja tagasimakse maksetööleht. Kui sisestate tagastustellimuse, loob Commerce kas kliendi maksetöölehe või sularahatöölehe, sõltuvalt maksemeetodist, mida klient algses kandes kasutab.
