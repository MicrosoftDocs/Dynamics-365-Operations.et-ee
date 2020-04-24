---
title: Soodustuste halduse parameetrite määramine
description: Konfigureerige soodustuste halduse parameetreid rakenduses Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9d6d463df08b9ae68047f09316f19e98740a8441
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229759"
---
# <a name="set-benefits-management-parameters"></a>Soodustuste halduse parameetrite määramine

Enne rakenduses Microsoft Dynamics 365 Human Resources puhkuseplaanid seadistamist peate konfigureerima soodustuste halduse parameetrid. Need parameetrid määravad vaikeväärtused, põhjuse koodid ja muud valikud.

## <a name="configure-general-parameters"></a>Üldiste parameetrite konfigureerimine

1. Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Parameetrid**.

2. Määrake vahekaardil **Üldine** järgmiste väljade väärtused.

   | Väli | Kirjeldus |
   | --- | --- |
   | **Riik/regioon** | Väli **Riik/regioon** määratleb sihtnumbrite/osariikide kuvamisjärjestuse. Valitud riik kuvatakse ripploendis esimesena. |
   | **Registreerimise põhjusekood** | Valige vaikimisi põhjuse kood, mida kasutada, kui töötaja plaanid avaliku registreerimise töötlemise käigus luuakse. |
   | **Tühistamise põhjusekood** | Töötaja soodustuse plaani tühistamisel kasutatav põhjuse kood. See kuvatakse tühistamise protsessi käigus dialoogiaknas. Kasutajad saavad vajadusel suvandit **Tühistamise põhjuse kood** muuta. |
   | **Põhjusekoodi taasavamine** | Töötaja soodustuse plaani taasavamisel kasutatav põhjuse kood. See kuvatakse tühistamise protsessi käigus dialoogiaknas. Kasutajad saavad vajadusel suvandit **Taasavamise põhjuse kood** muuta. | 
   | **Elusündmuse põhjusekood** | Põhjuse kood, mida kasutatakse elusündmuse toimumisel. |
   | **Määra muutuse põhjusekood** | Põhjuse kood, mida kasutada töötaja soodustuse plaani tühistamisel ja uuesti avamisel määra muutmise värskendamisprotsessi käigus. See näitab, milliseid kirjeid määra muutmise värskendusprotsessiga muudeti. |
   | **Uus palkamine sobilik** | Määrab, kas uued töötajad on sobivad. |
   | **Uue palkamise registreerimisperiood** | Ajaperiood, mil uue töötaja registreerimine on lubatud.</br></br>**Määrkus**: see säte alistab kõik uue töötaja registreerimisperioodid, mille plaani sobivusreeglis määrasite. | 
   | **Elusündmused on lubatud** | Lubab elusündmused. |
   | **Peida pärandsoodustuse vormid** | Võimaldab teil peita pärandsoodustuse vorme. |

3. Valige käsk **Salvesta**.

## <a name="configure-employee-self-service-parameters"></a>Töövõtja iseteeninduse parameetrite konfigureerimine

1. Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Parameetrid**.

2. Määrake vahekaardil **Töövõtja iseteenindus** järgmiste väljade väärtused.

   | Väli | Kirjeldus |
   | --- | --- |
   | **Soodustuse kinnitamine** | Soodustuste iseteenindusest väljaregistreerimisel kasutatav kinnitustekst. |
   | **Volitatud isikute automaatne valimine** | Määrab, kas valida sõltuvad ja kasusaajad vastavalt nende plaanisuvandite sobivusele automaatselt. |

3. Valige käsk **Salvesta**.
