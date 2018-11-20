---
title: "Jaemüügikanali fiskaalüksuse integreerimine"
description: "Selles teemas antakse ülevaade Retail POS-i fiskaalüksuse integreerimisest."
author: josaw
manager: annbe
ms.date: 11/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c852d095505abecbd44d29e9e7b53875e9069def
ms.contentlocale: et-ee
ms.lasthandoff: 11/01/2018

---
# <a name="fiscal-integration-for-retail-channel"></a>Jaemüügikanali fiskaalüksuse integreerimine

[!include [banner](../includes/banner.md)]

Selles teemas antakse ülevaade programmis Microsoft Dynamics 365 for Retail saadaolevast fiskaalse integreerimise funktsioonist. See fiskaalüksuse integreerimise funktsioon on raamistik, mis on loodud jaekaubanduse pettusi ennetavate kohalike maksuseaduste toetamiseks. Tavalised stsenaariumid, mis kuuluvad fiskaalüksuse integreerimise alla, on järgmised.

- Fiskaalkviitungi printimine ja selle kliendile andmine.
- Kassas teostatud müügi ja tagastustega seotud teabe edastamine maksuhalduri pakutavale välisele teenusele.
- Andmekaitse kasutamine maksuhalduri volitatud digitaalallkirjaga.

Selles teemas antakse juhised fiskaalüksuse integreerimise seadistamiseks, et kasutajad saaksid teha järgmist. 

- Fiskaalkonnektorite konfigureerimine, milleks on fiskaalsed seadmed või teenused, mida kasutatakse fiskaalüksuse registreerimise jaoks nagu salvestamine, digiallkirjastamine või finantsandmete turvaline esitamine.
- Dokumendipakkuja konfigureerimine, mis määratleb fiskaaldokumendi loomise väljundmeetodi ja algoritmi.
- Fiskaalüksuse registreerimisprotsessi konfigureerimine, mis määratleb etappide jada ja igal etapil kasutatava konnektorite grupi.
- Fiskaalüksuse registreerimisprotsessi määratlemine kassa funktsiooniprofiilidele.
- Konnektori tehniliste profiilide, kas riistvaraprofiilide (kohalike fiskaalkonntektorite) või kassa funktsiooniprofiilide (teiste fiskaalkonnektorite tüüpide jaoks) määratlemine.

## <a name="fiscal-integration-execution-flow"></a>Fiskaalüksuse integreerimise elluviimise voog
Järgmine stsenaarium näitab harilikku fiskaalüksuse integreerimise elluviimise voogu.

1. Fiskaalüksuse registreerimisprotsessi lähtestamine.
  
   Pärast mõne sellise toimingi tegemist, kus fiskaalüksuse registreerimine on nõutav (nt pärast jaemüügikande sõlmimist), seostatakse fiskaalüksuse registreerimisprotsess praeguse kassa funktsiooniprofiiliga.

1. Fiskaalkonnektori otsimine.
   
   Igale fiskaalüksuse registreerimisprotsessi etapile vastab süsteemis fiskaalkonnektorite loend. Nende konnektorite määratletud konnektori grupid hõlmavad funktsiooniprofiile ning mitme konnektori tehnilised profiilid on seotud praeguse riistvaraprofiiliga (ainult konnektoritüübi puhul, mis on **Kohalik**) või praeguse kassa funktsiooniprofiiliga (teiste konnektori tüüpide puhul).
   
1. Fiskaalüksuse integreerimise teostamine.

   Süsteem käivitab kõik vajalikud tegevused, mille määratleb leitud konnektoriga ühendatud kogum. See toimub vastavalt konnektori eelmise etapi funktsiooniprofiili ja tehnilise profiili seadetele.

## <a name="setup-needed-before-using-fiscal-integration"></a>Vajalikud seadistused enne fiskaalüksuse integreerimise kasutamist
Enne fiskaalüksuse integreerimise funktsiooni kasutamist tuleb määratleda järgmised seaded.

- Määratlege fiskaalüksuse funktsiooniprofiili numbri jaoks numbriseeria **Jaemüügi parameetrite** lehel.
  
- Määratlege numbriseeriad **Jaemüügi ühisparameetrite** lehel järgmistele viidetele:
  
  - Fiskaalüksuse tehnilise profiili number
  - Fiskaalkonnektori grupi number
  - Registreerimisprotsessi number

- Looge igale seadmele või teenusele, mida plaanite fiskaalüksuse integratsiooni eesmärgil kasutada **Fiskaalkonnektor**, minnes **Jaemüük > Kanali seadistus > Fiskaalüksuse integreerimine > Fiskaalkonnektorid**.

-  Looge kõigile fiskaalkonnektoritele **Fiskaaldokumendi pakkuja**, minnes **Jaemüük > Kanali seadistus > Fiskaalüksuse integreerimine > Fiskaaldokumendi pakkujad**. Andmetüüpide vastendamist peetakse fiskaaldokumendi pakkuja osaks. Samale konnektorile erinavte vastenduste loomiseks (nt riigipõhised määrused), tuleb luua erinevad fiskaaldokumendi pakkujad.

- Looge igale fiskaaldokumendi pakkujale **Konnektori funktsiooniprofiil**, minnes **Jaemüük > Kanali seadistus > Fiskaalüksuse integreerimine > Konnektori funktsiooniprofiilid**.
  - Valige konnektori nimi.
  - Valige dokumendipakkuja.
  - Määratlege KM-määra sätted vahekaardil **Teenuse seadistus**.
  - Määratlege KM-koodide vastendamine ja maksevahendi tüübi vastendamine **Andmete vastendamise** vahekaardil.

  #### <a name="examples"></a>Näited 

  |  | Vorming | Näide | 
  |--------|--------|--------|
  | KM-määrade seadistamine | väärtus: KM-määr | 1 : 2000, 2 : 1800 |
  | KM-koodide vastendamine | KM-kood: väärtus | KM20 : 1, KM18 : 2 |
  | Maksevahendi tüüpide vastendamine | Maksevahendi tüüp: väärtus | Sularaha: 1 kaart: 2 |

- Looge **Fiskaalkonnektorite grupid**, minnes **Jaemüük > Kanali seadistus > Fiskaalüksuse integreerimine > Fiskaalkonnektori grupp**. Konnektori grupp on selliste funktsiooniprofiilide alamkogu, mis on seotud fiskaalkonnektoritega, mis teostvad samu funktsioone ja mida kasutatakse fiskaalüksuse registreerimise protsessi samal etapil.

   - Konnektori grupile funktsiooniprofiilide lisamine. Klõpsake **Lisa** lehel **Funktsiooniprofiilid** ja valige profiili number.
   - Kui soovite peatada funktsiooniprofiili kasutamise, määratlege **Keela** olekuks **Jah**. 
   
     See muudatus mõjutab ainult praegust konnektori gruppi. Saate jätkata sama funktsiooniprofiili kasutamist teistes konnektori gruppides.

     >[!NOTE]
     > Konnektori grupis saab igal fiskaalkonnektoril olla ainult üks funktsiooniprofiil.

- Looge igale fiskaalkonnektorile **Konnektori tehniline profiil**, minnes **Jaemüük > Kanali seadistus > Fiskaalüksuse integreerimine > Konnektori tehnilised profiilid**.
  - Valige konnektori nimi.
  - Valige konnektori tüüp. 
      - **Kohalik** – määratlege see tüüp füüsilistele seadmetele või kohalikku arvutisse installitud rakendustele.
      - **Sisemine** – määratlege see tüüp fiskaalsetele seadmetele ja teenustele, mis on ühendatud jaemüügiserveriga.
      - **Väline** – väliste finantsteenuste jaoks nagu maksuhalduri pakutav veebiportaal.
    
  - Määratlege sätted **Ühenduse** vahekaardil.

      
 >[!NOTE]
 > Nii tehnilistele kui funktsiooniprofiilidele laaditakse varem laaditud värskendatud konfiguratsiooni versioon. Teid teavitatakse, kui sobiv konnektor või dokumendipakkuja on juba kasutuses. Vaikimisi talletatakse kõik tehnilistes ja funktsiooniprofiilides käsitsi tehtud muudatused. Nende profiilide asendamiseks konfiguratsiooni vaikeparameetritega klõpsake **Konnektori funktsiooniprofiilide** lehel ja **Konnektori tehniliste profiilide** lehel nuppu **Värskenda**.
 
- Looge igale fiskaalüksuse integreerimise kordumatule protsessile **Fiskaalüksuse registreerimisprotsess**, minnes **Jaemüük > Kanali seadistus > Fiskaalüksuse integreerimine > Fiskaalüksuse integreerimisprotsess**. Registreerimisprotsess määratletakse registreerimisetappide järjestuse ja igal etapil kasutatava konnektori grupi järgi. 
  
  - Registreerimisetappide protsessi lisamine.
      - Klõpsake vahekaarti **Lisa**.
      - Valige konnektori tüüp.
      
      >[!NOTE]
      > See väli määratleb, kust süsteem konnektorile tehnilist profiili otsib, kas riistvaraprofiilidest **Kohaliku** konnektori tüübi jaoks või kassa funktsiooniprofiilidest teiste fiskaalkonnektori tüüpide jaoks.
      
   - Konnektori grupi valimine.
   
     >[!NOTE]
     > Klõpsake **Kontrolli**, et kontrollida registreerimisprotsessi struktuuri tervislikkust. Kontrollimine on soovitatav järgmistel juhtudel.
       >- Uue registreerimisprotsessi suhtes pärast seda, kui kõik seadistamised (sh kassa funktsiooniprofiilide ja riistvaraprofiilide sidumine) on lõpule viidud.
       >- Pärast olemasoleva registreerimisprotsessi värskendamist.

-  Fsikaalüksuse registreerimisprotsessi sidumiseks kassa funktsiooniprofiilidega minge **Jaemüük > Kanali seadistus > Kassa seadistus > Kassa profiilid > Funktsiooniprofiilid**.
   - Klõpsake **Redigeeri** ja valige **Protsessi number** vahekaardil **Fiskaalüksuse registreerimisprotsess**.
- Konnektori tehniliste profiilide sidumiseks riistvaraprofiilidega minge **Jaemüük > Kanali seadistus > Kassa seadistus > Kassa profiilid > Riistvaraprofiilid**.
   - Klõpsake **Redigeeri**, seejärel klõpsake **Fiskaalüksuse tehnilise profiili** vahekaardil **Uus**.
   - Valige **Profiili numbri** väljal konnektori tehniline profiil.
   
     >[!NOTE]
     > Riistvaraprofiilile saab lisada mitu tehnilist profiili. Kuid seda ei toetata, kui riistvaraprofiilil on mis tahes konnektori grupiga rohkem kui üks lõikumine. Valede seadistuste vältimiseks on soovitatav pärast kõigi riistvaraprofiilide värskendamist registreerimisprotsessi kontrollida.

