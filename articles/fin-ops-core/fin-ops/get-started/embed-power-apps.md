---
title: Power Appsi manustamine
description: Selles teemas kirjeldatakse, kuidas manustada Power Appsi klienti, et tõsta toote funktsionaalsust.
author: jasongre
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: 8b5e64cb9ba916f9cbd628703394318b4044867b
ms.sourcegitcommit: dc953c316c396c45ddd596e25c2b358e39a95d84
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/02/2019
ms.locfileid: "2870237"
---
# <a name="embed-microsoft-power-apps"></a>Microsoft Power Appsi manustamine

[!include [banner](../includes/banner.md)]

Platvormivärskendus 14 toetab integratsiooni Microsoft Power Appsiga, mis on mõeldud arendajatele ja mittetehnilistele kasutajatele kohandatud ärirakenduste ehitamiseks mobiilsideseadmete, tahvelarvutite ning veebi jaoks ilma koodi kirjutamata. Power Apps Teie, teie organisatsiooni või laiema ettevõtete „ökosüsteemi” arendatud PowerAppsi saab lisada Finance and Operationsi rakendustesse, et võimendada toote funktsionaalsust. Näiteks võib luua Power Appi, mis täiendab Finance and Operationsi rakenduste teisest süsteemist toodud teabega.

Lisateavet Power Appsi manustamise kohta vaadake lühivideost [Kuidas manustada Power Appsi rakendusse](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-power-app-to-a-page"></a>Manustatud Power Appi lisamine lehele

### <a name="overview"></a>Ülevaade

Enne Power Appi klienti manustamist peate esmalt leidma või looma soovitud visuaalide ja/või funktsionaalsusega Power Appi. Siin ei kirjeldata Power Appi üksikasjalikku loomisprotsessi. Kui olete alles uus Power Appsi kasutaja, siis teema  [Power Appsi sissejuhatus](https://docs.microsoft.com/powerapps/getting-started) on heaks algukspunktiks.

Kui olete valmis konkreetset Power Appi manustama, on teil valida kahe võimaluse vahel, kuidas Power Appi lehel avada, olenevalt sellest, milline viis teile paremini sobib. Esimene võimalus on kasutada standardselt toimingupaanile lisatud nuppu Power Apps. Sedasi lisatud Power Apps kuvatakse menüünupu Power Apps menüü üksusena. Valimisel avab iga menüü-üksus külgpaani, mis sisaldab manustatud Power Appi. Teise võimalusena saate Power Appi kuvada otse lehel uue vahekaardina, kiirkaardina, labana või uue jaotisena tööruumis.

Manustatud Power Appi konfigureerimisel saate valida ühe välja, mida Power Appi sisendina saata. See võimaldab Power Appil reageerida praegu vaadatavate andmete põhjal.

### <a name="details"></a>Üksikasjad

Järgmised juhised näitavad, kuidas manustada Power Appi veebiklienti.

1. Minge lehele, kuhu soovite Power Appi manustada. See on sama leht, mis sisaldab mis tahes andmeid, mis tuleb Power Appi sisendina edastada.
2. Paani **Lisa Power App** avamiseks tehke järgmist.

    - Klõpsake valikut **Suvandid** ja seejärel valige **Vormi isikupärastamine**. Valige menüüst **Lisa** suvand **Power App**. Lõpuks valige piirkond, kuhu soovite Power Appi lisada. Kui soovite Power Appi menüünupu Power Apps alt manustada, valige toimingupaan. Kui soovite Power Appi otse lehele manustada, valige asjakohane vahekaart, kiirkaart, laba või jaotis (kui kasutate tööruumi).
    - Kui Power Appi avamiseks kasutatakse menüünuppu Power Apps, võite teise võimalusena klõpsata standardse toimingupaani menüünuppu **Power Apps** ja valida seejärel suvandi  **Lisa Power App**.

3. Manustatud Power Appi konfigureerimiseks tehke järgmist.

    - Väljal **Nimi** on näidatud tekst, mis kuvatakse manustatud Power Appi sisaldava nupu või vahekaardi jaoks. Sageli korratakse sellel väljal Power Appi nime.
    - **Rakenduse ID** on manustatava Power Appi GUID. Selle väärtuse toomiseks leidke Power App aadressilt [web.powerapps.com](https://web.powerapps.com) ja seejärel väli **Rakenduse ID** jaotisest **Üksikasjad**.
    - Välja **Power Appi sisendandmed** jaoks võite valida ka välja, mis sisaldab andmeid, mida soovite Power Appi sisendina edastada. Üksikasju, kuidas Power App Finance and Operationsi rakendustest saadetud andmetele juurde pääseb, saate vaadata selle jaotise allpool olevast teemast pealkirjaga [Finance and Operationsi rakendustest andmeid kasutava Power Appi loomine](#building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps).
    - Valige **Rakenduse suurus**, mis on kooskõlas manustatava Power Appi tüübiga. Valige **Peenike** mobiilsetele seadmetele loodud Power Appsi jaoks ja **Lai** tahvelarvutitele loodud Power Appsi jaoks. See tagab, et manustatud Power Appi jaoks eraldatakse piisavalt ruumi.
    - Kiirkaardil **Juriidilised isikud** saate määrata, milliste juriidiliste isikute jaoks see Power App saadaval on. Vaikimisi kuvatakse Power App kõigis juriidilistes isikutes.

4. Kui olete veendunud, et Power Appi konfiguratsioon on õige, klõpsake Power Appi lehele manustamiseks suvandit **Lisa**. Manustatud Power Appi nägemiseks palutakse teil brauserit värskendada.

## <a name="sharing-an-embedded-power-app"></a>Manustatud Power Appi ühiskasutusse andmine

Kui olete Power Appi lehele manustanud ja veendunud, et see töötab korrektselt mis tahes lehelt edastatud andmete konteksti puhul, võite seda manustatud Power Appi teistele süsteemis olevatele kasutajatele ühiskasutusse anda. Seda saab toote isikupärastamisvõimalusi kasutades teha kahel viisil.

- Soovitatav on seda teha süsteemi administraatori kaudu, kes saab isikupärastamise avaldada kõigile kasutajatele või kasutajate alamkogumile.
- Teise võimalusena saate lehe isikupärastamised eksportida, saata need ühele või mitmele kasutajale ja igaüks neist saab muudatused importida. Isikupärastamise tööriistariba suvand Halda võimaldab teil isikupärastamisi eksportida ja importida.

Toote isikupärastamise võimaluste ja nende kasutamise kohta vaadake lisateavet teemast [Kasutuskogemuse isikupärastamine](personalize-user-experience.md).

## <a name="building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps"></a>Finance and Operationsi rakenduste andmeid kasutava Power Appi loomine

Finance and Operationsi rakenduste manustamiseks loodava Power Appi puhul on oluline kasutada sisendandmeid Finance and Operationsi rakendustest. Power Appis pääseb neile sisendandmetele ligi muutujat Param("EntityId") kasutades.

Näiteks saate Finance and Operationsi rakenduste sisendandmed Power Appi funktsioonis OnStart seadistada järgmiseks muutujaks:

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-embedded-power-app"></a>Manustatud Power Appi kuvamine

Manustatud Power Appi kuvamiseks Finance and Operationsi rakenduste lehel avage lihtsalt manustatud Power Appiga leht. Meenutuseks, et Power Appsi saab avada standardse toimingupaani nupuga Power Apps või see võib olla kuvatud otse lehel vahekaardina, kiirkaardina, labana või tööruumi puhul uue jaotisena. Kui kasutaja püüab esimest korda Power Appi lehele laadida, palutakse tal Power Appsi sisse logida, tagamaks, et kasutajal on olemas vajalikud load Power Appi kasutamiseks.

## <a name="editing-an-embedded-power-app"></a>Manustatud Power Appi redigeerimine

Kui Power App on lehele manustatud, võib tekkida vajadus muuta Power Appi konfiguratsiooni. Näiteks võite soovida muuta manustatud Power Appiga seotud silti või on loodud Power Appi uus versioon ja teil on vaja värskendada rakenduse ID-d, et viidata uusimale Power Appile.

Manustatud Power Appi konfiguratsiooni redigeerimiseks tehke järgmist.

1. Avage paan **Redigeeri Power Appi**.

    - Kui kasutate manustatud Power Appi avamiseks menüünuppu Power Apps, paremklõpsake menüünuppu Power Apps ja valige suvand **Isikupärasta**. Valige rippmenüüst **Valige Power App** Power App, mida soovite konfigureerida.
    - Kui manustatud Power App kuvatakse otse lehel, valige **Suvandid** ja seejärel **Vormi isikupärastamine**. Klõpsake **valimistööriista** kasutades manustatud Power Appi.

2. Tehke vajalikud muudatused Power Appsi konfiguratsioonis ja klõpsake **Salvesta**.

## <a name="removing-an-embedded-power-app"></a>Manustatud Power Appi eemaldamine

Kui lehele on manustatud Power App, on vajaduse korral võimalik seda eemaldada kahel viisil.

- Avage paan **Redigeeri Power Appi**, selleks leiate juhtnöörid selle teema varasemast jaotisest [Manustatud Power Appi redigeerimine](#editing-an-embedded-power-app). Veenduge, et see paan kuvaks teavet eemaldada soovitud Power Appi kohta, ja seejärel klõpsake nuppu **Kustuta**.
- Kuna manustatud Power App salvestatakse isikupärastamisandmetena, eemaldatakse lehe isikupärastamiste kustutamisel ka lehele manustatud Power Apps. Pange tähele, et lehe isikupärastamised kustutatakse jäädavalt ja seda ei saa tagasi võtta. Lehe isikupärastamiste eemaldamiseks valige **Suvandid** ja seejärel klõpsake **Vormi isikupärastamine**. Valige menüüst **Halda** nupp **Tühjenda**. Pärast brauseri värskendamist on kõik lehe varasemad isikupärastamised eemaldatud. Isikupärastamist kasutavate lehtede optimeerimise kohta vaadake lisateavet teemast [Kasutuskogemuse isikupärastamine](personalize-user-experience.md).

## <a name="appendix"></a>Lisa

### <a name="developer-control-over-where-a-power-app-can-be-embedded"></a>Arendaja kontroll Power Appi manustamise asukohtade üle

Vaikimisi saavad kasutajad Power Appsi manustada mis tahes lehele kas menüünuppu Power Apps kasutades või otse lehele vahekaardina, kiirkaardina, labana või tööruumi puhul jaotisena lisades. Ent kui see on vajalik, saavad arendajad järgmiste meetodite abil seda funktsiooni konfigureerida selliselt, et Power Appsi saab manustada ainult teatud lehtedele.

- **isPowerAppPersonalizationEnabled** – kui see meetod annab teatud lehe puhul väärtuseks vale, ei kuvata menüünuppu Power Apps ja kasutajad ei saa Power Appsi kusagile lehele manustada, sh vahekaardina.
- **isPowerAppTabPersonalizationEnabled** – kui see meetod annab teatud lehe puhul väärtuseks vale, ei saa kasutajad Power Appsi otse vahekaardina, kiirkaardina või panoraamjaotisena lehele manustada. Kasutajatel on siiski võimalus manustada Power Appsi menüünupu Power Appsi abil, kui lehel on manustamine lubatud.

Järgmises näites on toodud uus klass kahe konfigureerimist vajava meetodiga, kuhu Power Appsi saab manustada.

```
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{
    public static boolean isPowerAppPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPersonalizationEnabled(pageName);
        return result;
    }
    
    public static boolean isPowerAppTabPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppTabPersonalizationEnabled(pageName);
        return result;
    }
}
```
