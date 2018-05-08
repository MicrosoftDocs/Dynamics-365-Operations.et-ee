---
title: PowerAppsi manustamine
description: "Selles teemas kirjeldatakse, kuidas manustada PowerAppsi Finance and Operationsi klienti, et tõsta toote funktsionaalsust."
author: jasongre
manager: AnnBe
ms.date: 04/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 07224faabcf2b183d4c8da0ba4588c33ec140d03
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="embed-powerapps"></a>PowerAppsi manustamine

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/pre-release.md)]

Microsoft Dynamics 365 for Finance and Operationsi platvormivärskendus 14 toetab integratsiooni Microsoft PowerAppsiga, mis on mõeldud arendajatele ja mittetehnilistele kasutajatele kohandatud ärirakenduste ehitamiseks mobiilsideseadmete, tahvelarvutite ja veebi jaoks ilma koodi kirjutamata. Teie, teie organisatsiooni või laiema ettevõtete „ökosüsteemi” arendatud PowerAppsi saab lisada rakenduse Finance and Operations klienti, et võimendada toote funktsionaalsust. Näiteks võib luua PowerAppi, mis täiendab Finance and Operationsi teisest süsteemist toodud teabega. 

Lisateavet PowerAppsi manustamise kohta vaadake lühikesest videost [Kuidas manustada PowerAppsi Dynamics 365 for Finance and Operationsisse?](https://www.youtube.com/watch?v=x3qyA1bH-NY).

> [!Video https://www.youtube.com/embed/x3qyA1bH-NY]

## <a name="adding-an-embedded-powerapp-to-a-page"></a>Manustatud PowerAppi lisamine lehele
### <a name="overview"></a>Ülevaade
Enne PowerAppi Finance and Operationsi klienti manustamist peate esmalt leidma või looma soovitud visuaalide ja/või funktsionaalsusega PowerAppi. Siin ei kirjeldata PowerAppi üksikasjalikku loomisprotsessi. Kui olete alles uus PowerAppsi kasutaja, siis teema [PowerAppsi sissejuhatus](https://docs.microsoft.com/en-us/powerapps/getting-started) on heaks algukspunktiks.

Kui olete valmis konkreetset PowerAppi manustama, on teil valida kahe võimaluse vahel, kuidas PowerAppi lehel avada, olenevalt sellest, milline viis teile paremini sobib. Esimene võimalus on kasutada standardselt toimingupaanile lisatud nuppu PowerApps. Sedasi lisatud PowerApps kuvatakse menüünupu PowerApps menüü üksusena. Valimisel avab iga menüü üksus külgpaani, mis sisaldab manustatud PowerAppi. Teise võimalusena saate PowerAppi kuvada otse lehel uue vahekaardina, kiirkaardina, labana või uue jaotisena tööruumis. 

Manustatud PowerAppi konfigureerimisel rakenduses Finance and Operations saate valida ühe välja, mida PowerAppi sisendina saata. See võimaldab PowerAppil reageerida praegu rakenduses Finance and Operations vaadatavate andmete põhjal.  

### <a name="details"></a>Üksikasjad
Järgmised juhised näitavad, kuidas manustada PowerAppi Finance and Operationsi veebiklienti.  

1. Minge lehele, kuhu soovite PowerAppi manustada. See on sama leht, mis sisaldab mis tahes andmeid, mis tuleb PowerAppi sisendina edastada.  
2. Paani **Lisa PowerApp** avamiseks tehke järgmist.
   - Klõpsake valikut **Suvandid** ja seejärel valige **Vormi isikupärastamine**. Valige menüüst **Lisa** suvand **PowerApp**. Lõpuks valige piirkond, kuhu soovite PowerAppi lisada. Kui soovite PowerAppi menüünupu PowerApps alt manustada, valige toimingupaan. Kui soovite PowerAppi otse lehele manustada, valige asjakohane vahekaart, kiirkaart, laba või jaotis (kui kasutate tööruumi).   
   - Kui PowerAppi avamiseks kasutatakse menüünuppu PowerApps, võite teise võimalusena klõpsata standardse toimingupaani menüünuppu **PowerApps** ja valida seejärel **Lisa PowerApp**.  
3. Manustatud PowerAppi konfigureerimiseks tehke järgmist.
   - Väljal **Nimi** on näidatud tekst, mis kuvatakse manustatud PowerAppi sisaldava nupu või vahekaardi jaoks. Sageli korratakse sellel väljal PowerAppi nime.  
   - **Rakenduse ID** on manustatava PowerAppi GUID. Selle väärtuse toomiseks leidke PowerApp aadressilt [web.powerapps.com](https://web.powerapps.com) ja seejärel väli **Rakenduse ID** jaotisest **Üksikasjad**.  
   - Välja **PowerAppi sisendandmed** jaoks võite valida ka välja, mis sisaldab andmeid, mida soovite PowerAppi sisendina edastada. Üksikasju, kuidas PowerApp rakendusest Finance and Operations saadetud andmetele juurde pääseb, saate vaadata selle jaotise allpool olevast teemast pealkirjaga [Rakenduse Finance and Operations andmeid kasutava PowerAppi loomine](#building-a-powerapp-that-leverages-data-sent-from-finance-and-operations).  
   - Valige **Rakenduse suurus**, mis on kooskõlas manustatava PowerAppi tüübiga. Valige **Peenike** mobiilsetele seadmetele loodud PowerAppsi jaoks ja **Lai** tahvelarvutitele loodud PowerAppsi jaoks. See tagab, et manustatud PowerAppi jaoks eraldatakse piisavalt ruumi.
   - Kiirkaardil **Juriidilised isikud** saate määrata, milliste juriidiliste isikute jaoks see PowerApp saadaval on. Vaikimisi kuvatakse PowerApp kõigis juriidilistes isikutes.  
4. Kui olete veendunud, et PowerAppi konfiguratsioon on õige, klõpsake PowerAppi lehele manustamiseks suvandit **Lisa**. Manustatud PowerAppi nägemiseks palutakse teil brauserit värskendada. 

## <a name="sharing-an-embedded-powerapp"></a>Manustatud PowerAppi ühiskasutusse andmine
Kui olete PowerAppi lehele manustanud ja veendunud, et see töötab korrektselt mis tahes lehelt edastatud andmete konteksti puhul, võite seda manustatud PowerAppi teistele süsteemis olevatele kasutajatele ühiskasutusse anda. Seda saab toote isikupärastamisvõimalusi kasutades teha kahel viisil.

- Soovitatav on seda teha süsteemi administraatori kaudu, kes saab isikupärastamise avaldada kõigile kasutajatele või kasutajate alamkogumile. 

- Teise võimalusena saate lehe isikupärastamised eksportida, saata need ühele või mitmele kasutajale ja igaüks neist saab muudatused importida. Isikupärastamise tööriistariba suvand Halda võimaldab teil isikupärastamisi eksportida ja importida.

Toote isikupärastamise võimaluste ja nende kasutamise kohta vaadake lisateavet teemast [Kasutuskogemuse isikupärastamine](personalize-user-experience.md).

## <a name="building-a-powerapp-that-leverages-data-sent-from-finance-and-operations"></a>Rakenduse Finance and Operations andmeid kasutava PowerAppi loomine
Rakendusse Finance and Operations manustamiseks loodava PowerAppi puhul on oluline kasutada sisendandmeid Finance and Operationsist. PowerAppis pääseb neile sisendandmetele ligi muutujat Param(„EntityId”) kasutades.  

Näiteks saate Finance and Operationsi sisendandmed PowerAppi funktsioonis OnStart seadistada järgmiseks muutujaks:

If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, "")); 

## <a name="viewing-an-embedded-powerapp"></a>Manustatud PowerAppi kuvamine
Manustatud PowerAppi kuvamiseks Finance and Operationsi lehel avage lihtsalt manustatud PowerAppiga leht. Meenutuseks, et PowerAppi saab avada standardse toimingupaani nupuga PowerApps või see võib olla kuvatud otse lehel vahekaardina, kiirkaardina, labana või tööruumi puhul uue jaotisena. Kui kasutaja püüab esimest korda PowerAppi lehele laadida, palutakse tal PowerAppsi sisse logida, tagamaks, et kasutajal on olemas vajalikud load PowerAppi kasutamiseks.   

## <a name="editing-an-embedded-powerapp"></a>Manustatud PowerAppi redigeerimine
Kui PowerApp on lehele manustatud, võib tekkida vajadus muuta PowerAppi konfiguratsiooni. Näiteks võite soovida muuta manustatud PowerAppiga seotud silti või on loodud PowerAppi uus versioon ja teil on vaja värskendada rakenduse ID-d, et viidata uusimale PowerAppile. 

Manustatud PowerAppi konfiguratsiooni redigeerimiseks tehke järgmist.
1. Avage paan **Redigeeri PowerAppi**. 
   - Kui kasutate manustatud PowerAppi avamiseks menüünuppu PowerApps, paremklõpsake menüünuppu PowerApps ja valige **Isikupärasta**. Valige rippmenüüst **Valige PowerApp** PowerApp, mida soovite konfigureerida.  
   - Kui manustatud PowerApp kuvatakse otse lehel, valige **Suvandid** ja seejärel **Vormi isikupärastamine**. Klõpsake **valimistööriista** kasutades manustatud PowerAppi.  
2. Tehke vajalikud muudatused PowerAppsi konfiguratsioonis ja klõpsake **Salvesta**.  

## <a name="removing-an-embedded-powerapp"></a>Manustatud PowerAppi eemaldamine
Kui lehele on manustatud PowerApp, on vajaduse korral võimalik seda eemaldada kahel viisil. 

- Avage paan **Redigeeri PowerAppi**, selleks leiate juhtnöörid selle teema varasemast jaotisest [Manustatud PowerAppi redigeerimine](#editing-an-embedded-powerapp). Veenduge, et see paan kuvab teavet eemaldada soovitud PowerAppi kohta, ja seejärel klõpsake nuppu **Kustuta**. 

- Kuna manustatud PowerApp salvestatakse isikupärastamisandmetena, eemaldatakse lehe isikupärastamiste kustutamisel ka lehele manustatud PowerApps. Pange tähele, et lehe isikupärastamised kustutatakse jäädavalt ja seda ei saa tagasi võtta. Lehe isikupärastamiste eemaldamiseks valige **Suvandid** ja seejärel klõpsake **Vormi isikupärastamine**. Valige menüüst **Halda** nupp **Tühjenda**. Pärast brauseri värskendamist on kõik lehe varasemad isikupärastamised eemaldatud. Isikupärastamist kasutavate lehtede optimeerimise kohta vaadake lisateavet teemast [Kasutuskogemuse isikupärastamine](personalize-user-experience.md).  

## <a name="appendix"></a>Lisa 
### <a name="developer-control-over-where-a-powerapp-can-be-embedded"></a>Arendaja kontroll PowerAppi manustamise asukohtade üle
Vaikimisi saavad kasutajad PowerAppsi manustada mis tahes lehele kas menüünuppu PowerApps kasutades või otse lehele vahekaardina, kiirkaardina, labana või tööruumi puhul jaotisena lisades. Ent kui see on vajalik, saavad arendajad järgmiste meetodite abil seda funktsiooni konfigureerida selliselt, et PowerAppsi saab manustada ainult teatud lehtedele. 

- **isPowerAppPersonalizationEnabled** – kui see meetod annab teatud lehe puhul väärtuseks vale, ei kuvata menüünuppu PowerApps ja kasutajad ei saa PowerAppsi kusagile lehele manustada, sh vahekaardina. 

- **isPowerAppTabPersonalizationEnabled** – kui see meetod annab teatud lehe puhul väärtuseks vale, ei saa kasutajad PowerAppsi otse vahekaardina, kiirkaardina või panoraamjaotisena lehele lisada. Kasutajatel on siiski võimalus manustada PowerAppsi menüünupu PowerAppsi abil, kui lehel on manustamine lubatud.  

Järgmises näites on toodud uus klass kahe konfigureerimist vajava meetodiga, kuhu PowerAppsi saab manustada.  

```
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{

    public static boolean isPowerAppPresonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPresonalizationEnabled(pageName);
        return true;
    }

    public static boolean isPowerAppTabPresonalizationEnabled(str pageName)   
    {
        var result = next isPowerAppTabPresonalizationEnabled(pageName);
        return true;
    }
    ```

}


