---
title: Uue transpordihalduse mootori loomine
description: See teema kirjeldab, kuidas luua uus transpordihalduse mootor moodulis Dynamics 365 Supply Chain Management.
author: Weijiesa
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSGenericEngine, TMSRateEngine, TMSMileageEngine, TMSEngineParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: 51661
ms.assetid: 0473acef-755e-4b42-acf5-5e5aa902dc0e
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be52c6afb66e88b36f3b2cdf5af14e17b3d3005f
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678118"
---
# <a name="create-a-new-transportation-management-engine"></a>Uue transpordihalduse mootori loomine

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas luua uus transpordihalduse mootor moodulis Dynamics 365 Supply Chain Management. 

Transpordihalduse (TMS) mootorid määratlevad loogika, mida kasutatakse transpordihindade loomiseks ja töötlemiseks transpordihalduse moodulis. Supply Chain Management pakub mitut erinevat tüüpi mootoritüüpe, mis arvutavad erinevaid parameetreid, nagu määrad, transiitajad ja transiidi ajal risttamistsoonide arv. See artikkel selgitab, kuidas kasutada Microsoft Visual Studio arenduskeskkonda koos Supply Chain Management arendustööriistadega, et luua ja juurutada uus TMS-i mootor ning kuidas seejärel mootorit operatsioonides seadistada. Lisateavet mootorite kohta vt [transpordihalduse mootoritest](transportation-management-engines.md).

## <a name="create-a-new-tms-engine"></a>Loo uus TMS mootor

See jaotis selgitab, kuidas luua klassiteeki, kus on TMS-i mootori rakendamine ja kuidas sellele viidata Supply Chain Management mudelist.

1. Oma uute mootorite juurutamiseks peab teil olema mudel, mis sisaldab mootoreid. Klõpsake **Dynamics 365** &gt; **mudelihalduse** menüüs **Uue mudeli** käsuga uue mudeli loomiseks. Esimesel **Mudeli loomise** lehel viisardis nimetage mudel **TMSEngines**. 

   [![Mudeli loomine.](./media/012.png)](./media/012.png)

2. Järgmisel leheküljel valige **Loo uus pakett**. 

   [![Uue paketi loomine.](./media/021.png)](./media/021.png)

3. Järgmisel leheküljel valige viidatav **ApplicationSuite** mudel. (**ApplicationPlatform** mudel on eelnevalt valitud.) 

   [![Valige viidatav mudel.](./media/032.png)](./media/032.png)

4. Uue mudeli loomise kinnitamiseks klõpsake **Valmis** nuppu järgmisel leheküljel. 

   [![Mudeli loomise lõpuleviimine.](./media/042.png)](./media/042.png)

5. Uues lahenduses looge uus Supply Chain Management projekt ja nimetage see **TMSThirdParty**. Seadke projekti atribuutides projekti mudeli väärtuseks **TMSEngines**.
6. Lisage lahendusele uus C\# klassi teek ja nimetage see **ThirdPartyTMSEngines**.
7. Projektis ThirdPartyTMSEngines lisage viited Supply Chain Management-seotud assembleritele:
   -   Rakenduse assemblerid, mis võimaldavad viidata X++ tüüpidele. Need assemblerid leiate järgmistest asukohtadest. \[Pakendite juur\] on kõigi juurutatud assemblerite asukoha tee, nagu näiteks C:\\pakendid.

        ```xpp
        [Packages root]\ApplicationPlatform\bin\Dynamics.AX.ApplicationPlatform.dll
        [Packages root]\ApplicationFoundation\bin\Dynamics.AX.ApplicationFoundation.dll
        [Packages root]\ApplicationSuite\bin\Dynamics.AX.ApplicationSuite.dll
        ```
        
   -   Raamistiku koostud, mis võimaldavad juurdepääsu andmetele, KKK-le ja abifunktsioonidele. Kõik need koosted leiate \[pakendite juur\]\\kaustast.

        ```xpp 
        Microsoft.Dynamics.ApplicationPlatform.Environment.dll
        Microsoft.Dynamics.AX.Data.Core.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.AdoNet.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Interface.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Msil.dll
        Microsoft.Dynamics.AX.Server.Core.dll
        Microsoft.Dynamics.AX.Xpp.AxShared.dll
        Microsoft.Dynamics.AX.Xpp.Support.dll
        ```

   -   TMS-i tuumkoost (mis sisaldab mootoreid) ja TMS-i põhikoost (mis sisaldab abilisi, konstante, andmete ülekande klassi definitsioone jne). Need assemblerid leiate järgmistest asukohtadest.

        ```xpp
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.dll
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.Base.dll
        ```
8. Nimetage ümber C\# klass, mis luuakse automaatselt ThirdPartyTMSEngines projekti **SampleRatingEngine**.
9. Juurutage mootor. Kuna selles näites oleme loomas mootori määra, siis pärime määra mootorite alusklassist. Alusklass juurutab enamiku määra mootori liidesest (**TMSFwkIRateEngine**). Me peame vaid rakendama määra meetodit. Et hoida see näide lihtsana, muudame selle meetodi registreerimise püsikoodiga määraks 100. Saate luua mootorid, mis juurutavad mootori mis tahes liideseid, nagu **TMSFwkIAccessorialEngine**. Kõik mootori liidesed määratletakse X++ abil.

    ```xpp
    namespace ThirdPartyTMSEngines
    {
        using Dynamics.AX.Application;
        using Microsoft.Dynamics.Ax.Tms.Base.Data;
        using Microsoft.Dynamics.Ax.Tms.Base.Utility;
        using Microsoft.Dynamics.Ax.Tms.Bll;
        using System.Xml.Linq;
        public class SampleRatingEngine : BaseRateEngine
        {
            public override RatingDto rate(TmsTransactionFacade transactionFacade, XElement shipment, TMSRateMasterCode rateMasterCode)
            {
               XElement re = shipment.RetrieveOrCreateRatingEntity(this.RatingDto);
               re.AddRate(TmsRateType.Rate, 100);
               return this.RatingDto;
            }
        }
    }
    ```

10. Lahenduse koostamine.
11. Lisage uus viide TMSThirdParty projektile. Viide peaks osutama ThirdPartyTMSEngines projektile. Kui olete lõpetanud, peaks lahendus selline olema. 

    [![Lahendus, mis sisaldab viidet TMSThirdParty projektile.](./media/052.png)](./media/052.png)

12. Lahenduse koostamine. Kontrollige, et uus teek ilmuks Application Exploreri **Viited** sõlmes. 

    [![Application Explorer viidete sõlme uus teek.](./media/061.png)](./media/061.png)

## <a name="deploy-the-tms-engine-as-a-package"></a>Juuruta TMS-i mootor paketina

Üks viis kolmanda osapoole TMS-i mootorite juurutamiseks on läbi juurutuspaketi. Seda lähenemist soovitatakse tootmiskeskkonnas. Arenduskeskkonnas saate kooste käsitsi kopeerida, nagu kirjeldatud järgmises jaotises "TMS mootori seadistamine rakenduses Supply Chain Management." Mootori paketina juurutamiseks järgige järgmisi etappe.

1. Menüüs **Dynamics 365** &gt; **Juuruta** klõpsake käsku <strong>Loo juurutuspakett</strong>.
2. Valige **Loo juurutuspakett** dialoogiboksis TMSEngines mudel sisestage tee, kuhu soovite oma paketifaile salvestada. 

   [![TMSEngines mudeli valimine.](./media/071.png)](./media/071.png)

3. Nüüd saate juurutada paketi sihtkeskkonda. Õpetuse vaatamiseks [Installeeri juurutuspakett](../../fin-ops-core/dev-itpro/deployment/install-deployable-package.md).

## <a name="set-up-the-tms-engine-in-supply-chain-management"></a>Määra TMS mootori häälestamine rakenduses Supply Chain Management

See jaotis selgitab, kuidas Supply Chain Management TMS-i mootori kasutamiseks seadistada, ja näitab, kuidas uut loodud mootorit kasutatakse määra ostudes. Selles jaotises kasutab näide USMF demo andmeettevõtet.

1. Looge uus mootor, nagu on kirjeldatud jaotises "Loo uus TMS-i mootor".
2. Oma lahenduse koostamine.
3. Kopeerige tulemuseks saadav kooste Supply Chain Management serveri asukoht \[AOSWebRoot\]kaustast. **Märkus:** See samm on oluline ainult arenduskeskkonnas. Tootmiskeskkonnas peaksite juurutama juurutuspaketi kaudu. Juhiseid vaata eelmisest jaotisest "TMS-i mootori juurutamine paketina."
4. Rakenduses Supply Chain Management **Mootorite hinne** lehel uus hindamismootor. Mootor peaks osutama mootori koostele, mis toodetakse mootoriklassi teeki ja teie rakendatud mootoriklassi abil. 

   [![Uue hindamismootori loomine lehel Hinda mootoreid.](./media/081.png)](./media/081.png)

5. Looge saadetise vedaja, mis kasutab näidismäära mootorit. Kuna meie mootor ei kasuta andmeid, ei pea te määra koondandmeid määrama. 

   [![Uue kättetoimetamise loomine.](./media/092.png)](./media/092.png)

6. Klõpsake **Hinda marsruudi töölauda** lehel valikut **Määra ost**. Peaksite SampleCarrier'i määraks seadma 100,00 nagu on näha järgmisel kuvatõmmisel. Selles näites määrame protsessi ostu määra 24. laost kliendini US-004. Kuid kuna hinne on raskesti kodeeritud, näete alati hinnangut 100,00.

   [![Marsruudi töölaua hinne.](./media/101.png)](./media/101.png)

## <a name="tips-and-tricks"></a>Vihjed ja näpunäited

- Kui kasutate Supply Chain Management arendustööriistu, on kasulik lisada lahendusele uus projekt. Kui seadistate selle projekti käivitusprojektiks ja käivitate silumisseansi, saate siluda nii X++ kui C\# koodi samas silumisseansis.
- Iga kord kui muudate ja kompileerite uuesti ThirdPartyTMSEngines projekti, peate tulemuseks saadud komplekti käsitsi kahendasukohta kopeerima või juurutama juurutuspaketi kaudu. Vastasel juhul võite käivitada aegunud komplekti.
- Pärast TMS-le omaste toimingute teostamist rakenduses Supply Chain Management, võib teenuse Internet Information Services (IIS) töötaja protsess lukustada ThirdPartyTMSEngine komplekti, nii et komplekti ei saaks värskendada. Sel juhul taaskäivitage w3svc protsess.

### <a name="whitepaper"></a>Tehniline ülevaade

Lisateabe saamiseks laadige alla järgmine tehniline ülevaade (kirjutatud versiooni AX2012 toetamiseks, kuid kehtib ka rakendusele Dynamics 365 Supply Chain Management)

- [Transpordihalduse mootorite rakendamine ja juurutamine](https://download.microsoft.com/download/b/5/f/b5ff8fef-3918-4c1d-92d5-b67eb0971684/ImplementingAndDeployingTransportationManagementEnginesInAX.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]