---
title: Kõigi ettevõtete soodustuste haldamise ja töövõtjate iseteeninduse parameetrite määramine
description: Soodustuste haldamise ja töövõtja iseteeninduse parameetrite konfigureerimine rakenduses Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e1bae79e47c3fa695ac239320eeee17b1a480f18
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337288"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a>Kõigi ettevõtete soodustuste haldamise ja töövõtjate iseteeninduse parameetrite määramine



Enne rakenduses Microsoft Dynamics 365 Human Resources soodustusplaanide häälestamist peate konfigureerima soodustuste halduse parameetrid. Need parameetrid määravad vaikeväärtused, põhjuse koodid ja muud valikud. 

## <a name="configure-general-parameters"></a>Üldiste parameetrite konfigureerimine

1. Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Human Resourcesi ühiskasutusega parameetrid**.

2. Määrake vahekaardil **Soodustuste haldus** järgmiste väljade väärtused.

   | Field | Kirjeldus |
   | --- | --- |
   | **Riik/regioon** | Väli **Riik/regioon** määratleb sihtnumbrite/osariikide kuvamisjärjestuse. Valitud riik kuvatakse ripploendis esimesena. |
   | **Registreerimise põhjusekood** | Valige vaikimisi põhjuse kood, mida kasutada, kui töötaja plaanid avaliku registreerimise töötlemise käigus luuakse. |
   | **Tühistamise põhjusekood** | Töötaja soodustuse plaani tühistamisel kasutatav põhjuse kood. See kuvatakse tühistamise protsessi käigus dialoogiaknas. Kasutajad saavad vajadusel suvandit **Tühistamise põhjuse kood** muuta. |
   | **Põhjusekoodi taasavamine** | Töötaja soodustuse plaani taasavamisel kasutatav põhjuse kood. See kuvatakse tühistamise protsessi käigus dialoogiaknas. Kasutajad saavad vajadusel suvandit **Taasavamise põhjuse kood** muuta. | 
   | **Elusündmuse põhjusekood** | Põhjuse kood, mida kasutatakse elusündmuse toimumisel. |
   | **Määra muutuse põhjusekood** | Põhjuse kood, mida kasutada töötaja soodustuse plaani tühistamisel ja uuesti avamisel määra muutmise värskendamisprotsessi käigus. See näitab, milliseid kirjeid määra muutmise värskendusprotsessiga muudeti. |
   | **Soodustuste aastane palk** | Lubab teil määrata summa **Soodustuste aastane palgasumma** töövõtja jaoks. Human Resources kasutab summat **Soodustuse aastane palgasumma** kindlustussummade määramiseks aastase põhipalga summa asemel. |
   | **Uus palkamine sobilik** | Määrab, kas uued töötajad on sobivad. |
   | **Uue palkamise registreerimisperiood** | Ajaperiood, mil uue töötaja registreerimine on lubatud.</br></br>**Määrkus**: see säte alistab kõik uue töötaja registreerimisperioodid, mille plaani sobivusreeglis määrasite. |
   | **Maksete vaikesagedus** | Vaikimisi kasutatav maksesagedus uute töötajate lisamisel. |
   | **Elusündmused on lubatud** | Lubab elusündmused. |
   | **Peida pärandsoodustuse vormid** | Võimaldab teil peita pärandsoodustuse vorme. |
   | **Soodustuse kinnitamine** | Soodustuste iseteenindusest väljaregistreerimisel kasutatav kinnitustekst. |
   | **Volitatud isikute automaatne valimine** | Määrab, kas valida sõltuvad ja kasusaajad vastavalt nende plaanisuvandite sobivusele automaatselt. |

3. Valige käsk **Salvesta**.

## <a name="configure-employee-self-service-parameters"></a>Töövõtja iseteeninduse parameetrite konfigureerimine

1. Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Human Resourcesi parameetrid**.

2. Määrake vahekaardil **Soodustuste haldus** järgmiste väljade väärtused.

   | Field | Kirjeldus |
   | --- | --- |
   | **Soodustuse kinnitamine** | Soodustuste iseteenindusest väljaregistreerimisel kasutatav kinnitustekst. |
   | **Volitatud isikute automaatne valimine** | Määrab, kas valida sõltuvad ja kasusaajad vastavalt nende plaanisuvandite sobivusele automaatselt. |

3. Valige käsk **Salvesta**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
