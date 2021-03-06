---
title: Kassa (POS) täiustused seerianumbritega toodete jaoks
description: Selles teemas käsitletakse täiustusi, mis on tehtud seerianumbriga toodetes, et säästaksite aega ja saaksite olla produktiivsemad.
author: ShalabhjainMSFT
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-08-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: fbd1d9c71ece77cbf4c6ecb741eb6d5e3e3455d9
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6028151"
---
# <a name="point-of-sale-pos-improvements-for-serialized-products"></a>Kassa (POS) täiustused seerianumbritega toodete jaoks

[!include [banner](includes/banner.md)]

## <a name="overview"></a>Ülevaade

Commerce Headquartersi sätete põhjal saab tooted liigitada seerianumbriga või seerianumbrita toodeteks. Kui tooted on seerianumbriga, saab igale kaubale määrata kordumatu numbri, mis aitab jälgida garantiisid, leida kaupu ja kinnitada omandiõigust. Kuigi meie kaasaegse/pilvekassa puhul oli olemas võimalus seerianumbriga toodetele seerianumbreid anda, on lisatud mõningaid täiustusi, et aidata kassapidajatel aega säästa ja produktiivsem olla.

## <a name="pos-improvements"></a>Kassa täiustused

- **Seerianumbreid pole vaja enne maksmist** – varem pidi kassapidaja, kes lisas kandesse seerianumbriga toote, sisestama seerianumbri. See nõue oli kliendisuhtluses probleem, kui kassapidajatel ja müüjatel tekkis võimalus tooteid üles müüa. Maksmise etapini oli sageli vaja tooteid ostukorvis muuta. Seetõttu küsis süsteem kassapidajalt iga kord uue toote lisamisel seerianumbrit. Nüüd on seerianumbri dialoogiboksis nupp **Lisa hiljem**. Seega saavad müüjad lisada kauba kandesse, kuid sisestada seerianumbri hiljem. Müüjad saavad seerianumbriga kaupu ostukorvis kiiresti lisada ja asendada ning sisestada seerianumbri vahetult enne maksmist. Kui mõne seerianumbriga toote puhul seerianumbrit ei sisestata, saab kassapidaja, kes püüab kannet lõpule viia, tõrketeate. See teade ütleb, et kassapidaja peab sisestama enne jätkamist puuduvad seerianumbrid.

    Iga seerianumbriga toote puhul, mille seerianumber on vahele jäetud, kuvatakse kande rea all kommentaar. See kommentaar ütleb, et kaubale pole seerianumbrit sisestatud. Seetõttu leiab kassapidaja kiiresti puuduva seerianumbriga kaubad.

    Uus toiming **Seerianumbri lisamine** lisab samuti seerianumbri kaupadele, millel see puudub. Kui seerianumber sisestatakse, ei saa seda redigeerida. Kassapidaja peab rea tühistama ja toote uuesti lisama.
    
- **Klienditellimuste esitamiseks pole seerianumbrid nõutavad** – klienditellimusi saab esitada ühest poest ja täita teisest. Kassapidaja, kes esitab klienditellimuse, ei pea seerianumbrit sisestama. Seerianumber sisestatakse komplekteerimise või pealevõtmise etapis. Kuid seerianumber tuleb sisestada kõigile reaüksustele, millele on valitud tarne tüüp **Sularahatarne**. Vastasel juhul ei saa kannet lõpule viia.
- **Seerianumbriga tooteid ei liideta kande ekraanil** – säte **Liida tooted** lehe **Funktsiooniprofiil** väljal **Terminal** võimaldab liita kande ekraanil samad seerianumbrita tooted. Samade toodete liitmisel on neid kande ruudustikus lihtsam näha. Kuid kuna seerianumbrid on üldiselt kordumatud ja müüjad ei pea sisestama seerianumbreid enne maksmist, ei kohaldu säte **Liida tooted** seerianumbriga toodetele. Seetõttu ei liideta seerianumbriga tooteid kande ekraanil, kui on valitud säte **Liida tooted**.
- **Võimalus otsida töölehti seerianumbri järgi** – nüüdsest saab töölehtede otsimiseks täiendavalt kasutada seerianumbreid. Selleks avage toiming „Töölehed” ja vajutage rakenduseribal nuppu „Täpsem otsing”. Seerianumbreid saate otsida, kui rakendate filtri, kasutades nuppu „Lisa filter”.


[!INCLUDE[footer-include](../includes/footer-banner.md)]