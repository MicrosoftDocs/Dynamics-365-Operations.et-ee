---
title: Mittevastavuste haldamine
description: Selles artiklis kirjeldatakse põhiseadistust, mis on mittevastavuste kasutamiseks nõutav. Täiendav seadistus on nõutav, kui soovite kasutada kvaliteettellimusi.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 28951
ms.assetid: a62d4ba8-eebc-4b14-b587-630be7298522
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f7bb4ffba4332314d1d7ab099232780584e75f9c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212867"
---
# <a name="nonconformance-management"></a>Mittevastavuste haldamine

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse põhiseadistust, mis on mittevastavuste kasutamiseks nõutav. Täiendav seadistus on nõutav, kui soovite kasutada kvaliteettellimusi.

Mittevastavuse haldamise võimaldamiseks tehke järgmist.

1.  Määratlege mittevastavustega seotud varude ja laohalduse parameetrid.
    -   Määrake suvandi **Kasuta kvaliteedijuhtimist** sätteks **Jah**.
    -   Sisestage väljale **Tunnimäär** tunnitasu kohalikus valuutas. Tunnimäära kasutatakse mittevastavusega seotud toimingute kulude arvutamiseks. Tunnimäär ja arvutatud kulud annavad viiteteavet mittevastavuse kohta. Need ei mõjuta teisi funktsioone.
    -   Kasutage prinditava dokumendi tüübi määratlemiseks vahekaarti **Kvaliteedijuhtimine** lehel **Aruande seadistus**. Saate printida mittevastavuse aruannet, mittevastavuse märgist või parandusaruannet. Saate määrata mitu kirjet erinevate dokumenditüüpide printimiseks aruandele või sise- või välismärkuste printimiseks. Kasulik võib olla kasutada lehte **Dokumendi tüüp**, et määrata mittevastavustele ja parandustele kordumatu dokumenditüüp. Näiteks soovite sisestada märkusi mittevastavuse kohta mittevastavuste kordumatu dokumenditüübi abil. Sellisel juhul tuvastage kordumatu dokumenditüüp aruandevalikutes.
    -   Lubage mittevastavuse ja paranduse viidete numbriseeriad.

2.  Lubage kasutajapoolne mittevastavuste kinnitamine. Kasutage välja **Nimi** lehel **Kasutajad** töötaja määramiseks igale kasutajale, kes peab mittevastavuse kinnitama. Süsteem kasutab mittevastavuse ajaloo jälgimiseks töötajaid, kes mittevastavuse olekut muudavad. Kasutajad ei saa mittevastavust kinnitada, kui neile pole töötaja ID-d määratud.
3.  Määratlege mittevastavustele määratavad probleemitüübid. Kasutage lehte **Probleemi tüübid** mitmesugustes mittevastavuse tüüpides ilmnevate kvaliteediprobleemide klassifikatsiooni määratlemiseks. Saate seadistada järgmisi mittevastavuse tüüpe: **Sisemine**, **Klient**, **Hankija**, **Teenuse päring**, **Tootmine** ja **Kaastoote tootmine**. Kasutage lehte **Mittevastavuse tüübid**, et lubada probleemi tüübi kasutamine ühes või enamas mittevastavuse tüübis. Näiteks veakoodiga seotud probleemitüüp võib rakenduda kõigile mittevastavuse tüüpidele, samas kui kliendikaebustega seotud probleemitüüp võib rakenduda ainult mittevastavuse tüüpidele **Klient** ja **Teenuse päring**.
4.  Määrake vahelao tsoonid vigase materjali kasutamise kohta juhiste pakkumiseks. Kasutage lehte **Vahelao tsoonid** tsoonide määratlemiseks, mida saab mittevastavusele määrata. Prinditud mittevastavuse silt kuvab määratud vahelao tsooni ja kasutamisteabe juhiste pakkumiseks vigaste materjalide käsitsemise kohta. Tsoonid võivad vastata lao asukohtadele või operatsiooniressurssidele.
5.  Määratlege parandustele määratavad diagnostika tüübid. Kasutage lehte **Diagnostika tüübid** diagnostiliste toimingute klassifikatsiooni määratlemiseks. Parandus määratleb, mis tüüpi diagnostilist tegevust tuleks kinnitatud mittevastavuse korral kasutada ja kes peaks seda tegema. Samuti määratleb see nõutava lõpetamise kuupäeva ja plaanitud lõpetamise kuupäeva.
6.  Määratlege mittevastavustele määratavad seotud toimingud. Kasutage lehte **Toimingud** töö klassifikatsiooni määratlemiseks, mida saab teha kinnitatud mittevastavuse puhul. Kui määrate mittevastavusele seotud toimingu, saate pakkuda üksikasjalikku teavet, nagu teavet toimingu tegemiseks nõutava seotud materjali, töötundide ja lisakulude kohta. Seda teavet kasutatakse toimingu eeldatava omahinna arvutamiseks. Üksikasjalikku teavet ja eeldatavat omahinda kasutatakse viitena. Kvaliteediga seotud toimingud erinevad toimingutest, mida saab määrata tootmisprotsessile.


<a name="additional-resources"></a>Lisaressursid
--------

[Vastavuse loomine ja töötlemine](tasks/create-process-non-conformance.md)

[Kvaliteedijuhtimise protsessid](quality-management-processes.md)

[Eeltingimuste seadistamine mittevastavuse halduseks](tasks/set-up-prerequisites-nonconformance-management.md)
