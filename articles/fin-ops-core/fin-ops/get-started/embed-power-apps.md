---
title: Power Appsi lõuendirakenduste manustamine
description: Selles teemas seletatakse, kuidas manustada kliendis Microsoft Power Appsi lõuendirakendusi, et suurendada toote funktsionaalsust.
author: jasongre
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: c2f7b660d364be6e62d484e67908201027190a8a
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065097"
---
# <a name="embed-canvas-apps-from-power-apps"></a>Power Appsi lõuendirakenduste manustamine

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Microsoft Power Apps on teenus, mis võimaldab arendajatel ja mittetehnilistel kasutajatel luua kohandatud ärirakendusi mobiilsete seadmete, tahvelarvutite ja veebi jaoks ilma koodi kirjutamata. Finance and Operationsi rakendused toetavad integreerimist rakendusega Power Apps. Lõuendirakendusi, mida teie, teie organisatsioon või laiem ökosüsteem arendate, saab toote funktsioonide funktsionaalsuse täiendamiseks manustada rakendusse Finance and Operations. Näiteks võite luua lõuendirakenduse Power Apps, et täiendada rakendust Finance and Operations teabega, mis on toodud teisest süsteemist.

Lisateavet CanvasAppsi manustamise kohta vaadake lühivideost [Kuidas manustada CanvasAppsi rakendusse](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-canvas-app-from-power-apps-to-a-page"></a>Manustatud lõuendirakenduse lisamine Power Appsist lehele

Enne Power Appsi rakenduse manustamist klienti peate leidma või looma soovitud visuaalide või funktsioonidega rakenduse. Selles teemas ei kirjeldata rakenduste loomise protsessi üksikasjalikult. Kui hakkasite Power Appsi alles kasutama, lugege [Power Appsi dokumentatsiooni](/powerapps/).

Lõuendirakenduse manustamiseks finance and Operationsi rakendusse on kolm võimalust. Saate kasutada lähenemist, mis sobib kõige paremini teie stsenaariumiga. 

- Manustage lõuendirakendus lehekülje **Power Apps** standardsel tegevuspaanil olevale nupule. Sel viisil lisatavate rakenduste puhul kuvatakse üksused **Power Apps** menüü nupuga ja rakendused on avatud külgpaanil. 
- Manustage lõuendirakendus otse olemasolevale lehele uue vahelehe lehena (liigendtabel, kiirkaart, rakendus või tööruumi jaotis).
- Looge juhtpaneelilt lõuendrakendusele uus täislehekülje kasutuskogemus.

Manustatud lõuendirakenduse konfigureerimisel saate valida ühe välja, mida kontekstina rakendusse saata. Selle sammu tõttu saab rakendus reageerida praegu vaadatavate andmete põhjal.

> [!NOTE]
> Praegu ei saa seda mehhanismi kasutada mudelipõhiste rakenduste manustamiseks.

### <a name="embedding-a-canvas-app-on-an-existing-page"></a>Lõuendirakenduse manustamine olemasolevale lehele

Järgmises protsessis näidatakse, kuidas lõuendirakendust manustada Power Apps olemasolevale lehele.

1. Avage leht, kus soovite lõuendirakenduse manustada. See on leht, mis sisaldab andmeid, mis tuleb rakendusse sisendina edastada.
2. Avage paan **Lisa rakendus Power Appsist**.

    - Kui rakendus on manustatud otse leheküljele, valige suvand **Valikud** \> **Isikupärasta see lehekülg** \> **Veel**  ja järgige seejärel üht järgmistest sammudest:

        - Kui **täislehe rakenduste** funktsioon on sisse lülitatud, valige **lisa lehekülg** ja seejärel valige piirkond, kuhu soovite rakenduse lisada. Rakenduse kaasamiseks **Power Apps** menüü nupule, valige tegevuspaan. Kui soovite rakendust otse lehele manustada, valige asjakohane vahekaart, kiirkaart, laba või jaotis (kui kasutate tööruumi). Seejärel **Lisa rakendus** paanil, valige **Power Apps**.
        - Kui **täislehe rakenduste** funktsioon on välja lülitatud, valige **Lisa rakendus Power Apps**`ist, ja seejärel valige piirkond, kuhu soovite rakenduse lisada. Rakenduse kaasamiseks **Power Apps** menüü nupule, valige tegevuspaan. Kui soovite rakendust otse lehele manustada, valige asjakohane vahekaart, kiirkaart, laba või jaotis (kui kasutate tööruumi).

    - Kui rakenduse avamiseks kasutatakse **Power Apps** menüünuppu , võite teise võimalusena klõpsata standardse toimingupaani **Power Apps** menüünuppu ja valida seejärel suvandi **Lisa rakendus**.

3. Manustatud rakenduse konfigureerimine. Lisateabe saamiseks vaadake [Lõuendirakenduse konfigureerimine](#configuring-a-canvas-app) selle teema järgnevates jaotistes.
4. Kui olete kinnitanud, et konfiguratsioon on õige, valige **Sisesta**.

    - Kui **salvestatud vaadete** funktsioon on välja lülitatud, palutakse teil värskendada brauserit, et näha manustatud rakendust.
    - Kui **salvestatud vaadete** funktsioon on sisse lülitatud, peate muudatuse püsimiseks vaate salvestama.

### <a name="embedding-a-canvas-app-as-a-full-page-experience-from-the-dashboard"></a>Lõuendirakenduse manustamine juhtpaneelilt täisleheküljelise kogemusena

Võib-olla soovite manustada armatuurlaualt lõuendirakenduse, kui rakendus pole seotud olemasoleva lehega või kui soovite rakenduse lihtsalt rakenduse lisalehe kasutuskogemusena rakenduses Finance and Operations esile tuua.

> [!NOTE]
> Et see võimalus oleks saadaval, peate funktsioonihalduses lülitama sisse funktsiooni **Täieliku lehe rakendused**. 

1. Avage armatuurlaud.
2. Valige ja hoidke lehte all (või paremklõpsake), valige **isikupärastamine** ja seejärel valige **lisa lehekülg**.
3. Klõpsake paanil **Lisa leht** valikut **Power Apps**.
4. Manustatud rakenduse konfigureerimine. Lisateabe saamiseks vaadake [Lõuendirakenduse konfigureerimine](#configuring-a-canvas-app) selle teema järgnevates jaotistes.
5. Valige **Salvestamine**, et lisada rakendus armatuurlauale uue paanina.
6. Valige armatuurlaual uus paan ja veenduge, et lõuendirakendust kuvatakse nii, nagu oodatud.

### <a name="configuring-a-canvas-app"></a>Lõuendirakenduse konfigureerimine

Kui manustate lõuendi rakenduse, peate seadistama järgmised parameetrid:

- **Nimi** – sisestage tekst, mida tuleks kuvada nupu või vahekaardi jaoks, mis sisaldab manustatud rakendust. Sageli võiksite sellel väljal korrata rakenduse nime.
- **Rakenduse ID** - määrake manustatava lõuendrakenduse globaalselt kordumatu identifikaator (GUID). Selle väärtuse toomiseks leidke rakendus aadressilt [make.powerapps.com](https://make.powerapps.com) ja seejärel heitke pilk väljale **Rakenduse ID** jaotises **Üksikasjad**.
- **Rakenduse sisendkontekst** - valikuliselt saate valida välja, mis sisaldab andmeid, mida soovite rakendusele sisendina edastada. Lisateavet selle kohta, kuidas rakendus pääseb juurde finance and Operationsi rakendustest saadetud andmetele, leiate jaotisest [Rakenduse loomine, mis võimendab finance and Operationsi rakendustest](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps) hiljem saadetud andmeid selles teemas.

    Alates versioonist 10.0.19 edastatakse praegune juriidiline isik samuti ka lõuendi rakenduse kontekstina **cmp** URL-i parameetri kaudu. See käitumine ei mõjuta sihtmärgi lõuendi rakendust enne, kui rakendus kasutab seda teavet.

- **Rakenduse suurus** - Valige tüüp, mis on kooskõlas manustatava rakendusega. Valige **Peenike** mobiilsetele seadmetele loodud rakenduste jaoks ja **Lai** tahvelarvutitele loodud rakenduste jaoks. See parameeter tagab, et manustatud rakenduse jaoks eraldatakse piisavalt ruumi.
- **Juriidilised isikud** – Saate valida juriidilised isikud, kelle jaoks rakendus peaks olema saadaval. Rakendus on vaikimisi saadaval kõigi juriidiliste isikute jaoks. See suvand on saadaval ainult siis, kui manustate olemasolevale lehele otse ja **[salvestatud vaadete](saved-views.md)** funktsioon on välja lülitatud.

## <a name="sharing-an-embedded-app"></a>Manustatud rakenduse ühiskasutusse andmine

Kui olete lõuendirakenduse lehel manustanud ja veendunud, et see töötab korrektselt mis tahes lehelt edastatud andmekonteksti puhul, võite rakendust teiste süsteemis olevate kasutajatega jagada. Manustatud lõuendirakenduse jagamiseks toimige järgmiselt.

1. [Jagage lõuendirakendust Power Apps](/powerapps/maker/canvas-apps/share-app) sobivate kasutajatega, et nad pääseksid rakendusele Power Apps otse juurde.
2. Jagage manustatud rakendusega seostatud isikupärastamised soovitud kasutajatega. Saate kasutada üht järgmistest meetoditest.

    - **Avaldage vaade (soovitatav):** Kui **[Salvestatud vaadete](saved-views.md)** funktsioon on sisse lülitatud, on soovitatav ja eelistatud lähenemine vaate loomiseks, mis sisaldab manustatud lõuendi rakendust, ja seejärel avaldada see vaade soovitud kasutajatele. Selle meetodi puhul on tagatud, et kõik kasutajad, kellel on avaldatud vaatega seotud turberollid, näevad lehel lõuendirakendust.

        Saate avaldada ka lõuendirakenduse, mis on armatuurlaualt täislehe kogemusena manustatud. Valige ja hoidke armatuurlaual (või paremklõpsake) rakendusega seotud paanil, valige **isikupärastamine** ja seejärel valige **Avalda leht**. Kuvatakse selline kogemus, mis sarnaneb *avaldamisvaadete* kogemusega ja te saate valida turvarollid, mida avaldada. Kui **täiustatud juriidilise isiku tugi salvestatud vaadete** funktsiooni jaoks on sisse lülitatud, saate värskenduses 10.0.21 või hiljem avaldada rakenduses soovitud juriidilistele isikutele.

    - Kui **salvestatud vaadete** funktsioon on välja lülitatud, saab süsteemiadministraator lõuendirakenduse **Isikupärastamise** lehe kaudu sobivale kasutajakomplektile anda. Teise võimalusena saate eksportida oma lehe isikupärastamised ja saata need ühele või mitmele kasutajale. Seejärel saavad kõik need kasutajad isikupärastamise importida. Isikupärastamise tööriistaribal on nupud, mis võimaldavad isikupärastamisi eksportida ja importida.

> [!NOTE]
> Kui lõuendirakendust on jagatud väliste kasutajatega, ei saa need kasutajad kasutada finance and Operationsi rakendustes manustatud rakendust. Siiski pääsevad nad rakendusele juurde otse Power Appsis. Väliskasutajate hulka kuuluvad külalised ja kasutajad, kes ei kuulu Azure'i kataloogi, Microsoft 365 kus rakendus Finance and Operations juurutatakse.

Toote isikupärastamise võimaluste ja nende kasutamise kohta vaadake lisateavet teemast [Kasutuskogemuse isikupärastamine](personalize-user-experience.md).

## <a name="building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps"></a>Rakenduse Finance and Operations saadetud andmeid kasutava lõuendirakenduse loomine

Kui loote lõuendirakenduse, mis manustatakse rakendusse Finance and Operations, on üks oluline osa protsessist kasutada selle rakenduse Finance and Operations sisendandmeid. Power Apps Arenduskogemuse põhjal pääseb finance and Operations rakendusest edastatud sisendandmetele juurde muutuja Param("EntityId")**abil**. Alates versioonist 10.0.19 edastatakse praegune juriidiline isik lisaks ka lõuendi rakenduse kontekstina **Param("cmp")** muutuja kaudu. 

Näiteks rakenduse funktsioonis OnStart saate määrata Finance and Operationsi rakenduste sisendandmed selliseks muutujaks:

``` Power Apps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));

If(!IsBlank(Param("cmp")), Set(FinOpsLegalEntity, Param("cmp")), Set(FinOpsLegalEntity, ""));
```

## <a name="viewing-a-canvas-app"></a>Lõuendirakenduse kuvamine

Manustatud lõuendirakenduse vaatamiseks finance and Operationsi rakenduste lehel minge lihtsalt lehele, millel on manustatud rakendus. Pidage meeles, et rakendustele on võimalik juurde pääseda standardsel toimingupaanil asuva nupu **Power Apps** kaudu. Teise võimalusena võidakse need kuvada otse lehel uue vahekaardi, kiirkaardi või labana või tööruumis uue jaotisena. Kui kasutajad püüavad rakendust esimest korda lehel laadida, palutakse neil sisse logida. Selle abil tagatakse, et kasutajatel oleksid rakenduse kasutamiseks sobivad load.

## <a name="editing-an-embedded-app"></a>Manustatud rakenduse redigeerimine

Kui rakendus on lehele manustatud, võib tekkida vajadus muuta rakenduse konfiguratsiooni. Näiteks võite soovida muuta manustatud rakendusega seotud silti või on loodud rakenduse uus versioon ja teil on vaja värskendada rakenduse ID-d, et viidata uusimale PowerAppile.

Manustatud rakenduse konfiguratsiooni redigeerimiseks tehke järgmist.

1. Avage paan **Redigeeri rakendust**.

    - Kui kasutate manustatud rakenduse avamiseks Power Apps menüünuppu, valige ja hoidke all (või paremklõpsake) Power Apps menüünuppu ja valige suvand **Isikupärasta**. Valige rippmenüüst **Valige rakendus** see rakendus, mida soovite konfigureerida.
    - Kui manustatud rakendus kuvatakse otse lehel, valige **Suvandid** ja seejärel **Isikupärasta see leht**. Klõpsake **valimistööriista** kasutades manustatud rakendust.
    - Kui manustatud rakendus lisati armatuurlaudalt, avage armatuurlaud, valige ja hoidke all (või paremklõpsake) lõuendi rakendusega seotud paani, valige **isikupärastamine** ja seejärel valige lehekülg **Redigeeri**.

2. Tehke vajalikud muudatused rakenduse konfiguratsioonis ja klõpsake **Salvesta**.

## <a name="removing-an-app"></a>Rakenduse eemaldamine

Kui rakendus on lehele manustatud, saate selle vajadusel eemaldada mitmel viisil:

- Avage paan **Redigeeri rakendust**, selleks leiate juhtnöörid selle teema varasemast jaotisest [Manustatud rakenduse redigeerimine](#editing-an-embedded-app). Veenduge, et see paan kuvab teavet eemaldada soovitud rakenduse kohta, ja seejärel klõpsake nuppu **Kustuta**.
- Kui manustatud rakendus lisati armatuurlaudalt, avage armatuurlaud, valige ja hoidke all (või paremklõpsake) lõuendi rakendusega seotud paani, valige **isikupärastamine** ja seejärel valige **Eemaldage lehekülg**. 
- Kuna manustatud rakendus salvestatakse isikupärastamisandmetena, eemaldatakse lehe isikupärastamiste kustutamisel ka lehele manustatud rakendused. Pange tähele, et lehe isikupärastamised kustutatakse jäädavalt ja seda ei saa tagasi võtta. Lehe isikupärastamiste eemaldamiseks valige **Suvandid** ja seejärel klõpsake **Isikupärasta see leht** ja lõpuks nuppu **Tühjenda**. Pärast brauseri värskendamist on kõik lehe varasemad isikupärastamised eemaldatud. Isikupärastamist kasutavate lehtede optimeerimise kohta vaadake lisateavet teemast [Kasutuskogemuse isikupärastamine](personalize-user-experience.md).

## <a name="appendix"></a>Lisa

### <a name="developer-modeling-a-canvas-app-on-a-form"></a>[Arendaja] Lõuendi rakenduse modelleerimine vormil

Kui see teema keskendub lõuendi rakenduste kaasamisele isikupärastamise kaudu, on arendajatel ka võimalus lisada lõuendi rakendus vormile, kasutades Visual Studio arenduskogemust. Selle tarbeks lisage vormile lihtsalt PowerAppsHostControl. Juhtelemendil saadaolevad metaandmete atribuudid pakuvad samu võimalusi nagu isikupärastamise kogemuski.

### <a name="developer-specifying-where-an-app-can-be-embedded"></a>[Arendajale] Rakenduse manustamise asukoha täpsustamine

Vaikimisi saavad kasutajad rakendusi manustada mis tahes lehele kas Power Appsi menüünuppu kasutades või otse lehele vahekaardina, kiirkaardina, labana või tööruumi puhul jaotisena lisades. Ent kui see on vajalik, saavad arendajad järgmiste meetodite abil seda funktsiooni konfigureerida selliselt, et rakendusi saab manustada ainult teatud lehtedele.

- **isPowerAppPersonalizationEnabled** – kui see meetod annab teatud lehe puhul väärtuseks vale, ei kuvata Power Appsi menüünuppu ja kasutajad ei saa rakendusi kusagile lehele manustada, sh vahekaardina.
- **isPowerAppTabPersonalizationEnabled** – kui see meetod annab teatud lehe puhul väärtuseks vale, ei saa kasutajad rakendusi otse vahekaardina, kiirkaardina või panoraamjaotisena lehele manustada. Kasutajatel on siiski võimalus manustada rakendusi Power Appsi menüünupu abil, kui lehel on manustamine lubatud.

Järgmises näites on toodud uus klass kahe konfigureerimist vajava meetodiga, kuhu rakendusi saab manustada.

```powerapps
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

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
