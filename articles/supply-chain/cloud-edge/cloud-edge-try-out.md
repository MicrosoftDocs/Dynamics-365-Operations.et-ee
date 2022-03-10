---
title: Proovi skaalaühikuid jaotatud topoloogias
description: See teema annab teavet, kuidas käivitada pilve- ja servaskaala ühikuid tootmis- ja laohalduse töökoormuste puhul.
author: perlynne
ms.date: 03/03/2022
ms.topic: article
ms.search.form: ScaleUnitWorkloadsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-03-03
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 04fd79f3c582ae9ac51882f73410477efaa35496
ms.sourcegitcommit: b52ff5dfd32580121f74a5f262e5c2495e39d578
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/03/2022
ms.locfileid: "8376255"
---
# <a name="try-out-scale-units-in-a-distributed-hybrid-topology"></a>Proovi skaalaühikuid jaotatud topoloogias

[!include [banner](../includes/banner.md)]

Jaotatud topoloogia proovimise protsess on lihtne. Esimese etapi jooksul peaksite kohandusi kinnitama, et tagada nende töö jaotatud topoloogias. Teil on kaks valikut.

## <a name="option-1-evaluate-customizations-in-development-environments"></a>Valik 1: hinnake kohandusi arenduskeskkonnas

Enne kui alustate oma sisendkausta keskkondades, soovitame teil uurida kaaluühikuid arenduse seadistuses, nagu ühe kasti keskkonnas (nimetatakse ka järgu 1 keskkonnas), et kontrollida protsesse, kohandusi ja lahendusi. Selles etapis rakendatakse andmed ja kohandused ühe lahendusega keskkondadele. Saate käitada üksikus keskkonnas, mis võib võtta rolli nii ettevõtte keskusel kui kaaluühikul. Teise võimalusena on teil kaks arenduskeskkonda, millest üks võtab keskuse rolli ja teine, mis võtab kaaluühiku rolli. See häälestus on parim viis probleemide tuvastamiseks ja lahendamiseks. Selle etapi [lõpuleviimiseks saab kasutada ka värskeimat](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxURUFWTjQzTzg0UUk5RkJHMDFEMVlSSDFEQy4u) varajast juurdepääsu (PEAP) koostet.

Keskkondade installimiseks [ja säilitamiseks peaksite kasutama ühe boksi arenduskeskkonna](https://github.com/microsoft/SCMScaleUnitDevTools) kaalu ühiku juurutamise tööriistu. Need tööriistad lasevad teil konfigureerida keskuse- ja kaaluühikud ühes või kahes ühe boksi keskkonnas. Tööriistad on saadaval nii binaarse väljaandena kui ka lähtekoodina GitHub-s. Projekti töös, mis sisaldab samm-sammulise [kasutusjuhendit](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide), mis kirjeldab tööriistade kasutamist. Kui juurutate [kohaliku äriandmete (LBD) abil kohandatud riistvarale servaskaala ühikud](cloud-edge-edge-scale-units-lbd.md), peate järgima teist protsessi.

## <a name="option-2-acquire-add-ins-and-deploy-in-your-sandbox-environments"></a>Valik 2: lisandmoodulite soemine ja juurutamine oma kausta keskkondades

Jaotatud topoloogia proovimiseks peab teil olema kaks ruutkeskkonda (kiht 2), millest ühel on teie andmed (ettevõttekeskus) ja teine, mis on kaaluühiku jaoks ja millel on "tühjad andmed".

Peate hankima lisandmoodulid vähemalt ühele pilve või servaskaala ühikule. Vastavaid projekti- ja keskkonnapesasid antakse [Microsoft Dynamics siis elutsükli teenustes](https://lcs.dynamics.com/)(LCS), [nii et kaaluühiku keskkondi saab juurutada kaaluühiku halduri portaali kasutades](https://aka.ms/SCMSUM).

Pöörduge Microsofti tugiteenuste poole, et taotleda selle kohta, et kausta keskkonnad on lubatud.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
