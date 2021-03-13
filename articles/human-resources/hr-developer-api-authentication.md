---
title: Autentimine
description: See artikkel annab ülevaate teabest, kuidas autentida rakenduse Microsoft Dynamics 365 Human Resources andmete rakenduse programmeerimisliidese (API) abil.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
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
ms.openlocfilehash: 963bec2b817c59e3b5860c5ff5885e165ec8656a
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115556"
---
# <a name="authentication"></a>Autentimine

See artikkel annab ülevaate teabest, kuidas autentida rakenduse Microsoft Dynamics 365 Human Resources andmete rakenduse programmeerimisliidese (API) abil.

## <a name="overview"></a>Ülevaade

Rakenduse Human Resources andmete API on OData juurutus. Lisateavet vaadake teemast [Avatud andmeprotokoll (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).

Teie rakendus peab autentima autoriseeritud kutsujana, enne kui API teenindab teie rakendusest taotlusi.

## <a name="fundamentals"></a>Põhisätted

Andmete API kutsumiseks peab teie rakendus hankima Microsofti identiteedi platvormilt juurdepääsuloa. Juurdepääsuluba sisaldab teavet teie rakenduse kohta ja luba, et see peab rakenduses Human Resources ressursse kutsuma.

### <a name="access-token"></a>Juurdepääsuluba

Microsofti identiteedi platvormi väljastatud juurdepääsuluba on Base64-kodeeringuga JavaScript Object Notationi (JSON) veebiload (JWTs). Need sisaldavad teavet (nõudeid), et andmete API (ja muud veebi API-d, mis on turvatud Microsofti identiteedi platvormiga) kasutavad kutsuja kinnitamist ja tagavad, et kutsujal on taotletud toimingu teostamiseks vajalikud load. Kutsumiste ajal saate käsitleda juurdepääsulubasid läbipaistmatutena. Peaksite alati edastama juurdepääsulubasid üle turvalise kanali, nt Transport Layer Security (TLS) ja Hypertext Transfer Protocol Secure (HTTPS).

Siin on juurdepääsuloa näide, mille on väljastanud Microsofti identiteedi platvorm.

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

Andmete API kutsumiseks lisate juurdepääsuloa oma HTTP-taotluse autoriseerimise päisesse vastutaja loana. Siin on näide.

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a>Uue rakenduse registreerimine Azure’i portaali kasutades

1. Logige [Microsoft Azure’i portaali](https://portal.azure.com) töö- või koolikontoga või isikliku Microsofti kontoga sisse.

2. Kui teie konto annab teile juurdepääsu rohkem kui ühele rentnikule, valige ülemises parempoolses nurgas oma konto ja seadke oma portaali seanss Azure Active Directory (Azure AD) soovitud rentnikule.

3. Vasakpoolsel paanil valige teenus **Azure Active Directory** ja seejärel valige **Rakenduse registreerimised \> Uus registreerimine**.

4. Kui ilmub leht **Rakenduse registreerimine**, sisestage oma rakenduse registreerimisteave.

    - **Nimi**: sisestage tähendusega rakenduse nimi, mis kuvatakse rakenduse kasutajatele.
    - **Toetatud kontotüübid**: valige kontode tüübid, mida teie rakendus peaks toetama.

        | Toetatud kontotüübid | Kirjeldus |
        |-------------------------|-------------|
        | Ainult selle organisatsioonikataloogi kontod | Valige see suvand, kui ehitate tegevusalapõhist rakendust. See suvand ei ole saadaval, kui te ei registreeri rakendust kataloogis.<p>See suvand on vastendatud suvandiga **Azure AD ainult üks rentnik**.</p><p>See suvand on vaikimisi suvand, kui te ei registreeri rakendust väljaspool kataloogi. Sellisel juhul on vaikimisi suvand **Azure AD mitu rentnikku ja isiklikud Microsofti kontod**.</p> |
        | Mis tahes organisatsioonikataloogi kontod | Valige see suvand kõikidele äri- ja haridusklientidele suunamiseks.<p>See suvand on vastendatud suvandiga **Azure AD ainult mitu rentnikku**.</p><p>Kui olete rakenduse registreerinud kui **Azure AD ainult üks rentnik**, saate kasutada laba **Autentimine**, et uuendada see valikule **Azure AD ainult mitu rentnikku** ja seejärel tagasi valikule **Azure AD ainult üks rentnik**.</p> |
        | Kontod mis tahes organisatsioonikataloogides ja isiklikes Microsofti kontodes | Valige see suvand kõige laiemale klientide kogumile suunamiseks.<p>See valik on vastendatud suvandiga **Azure AD mitu rentnikku ja isiklikud Microsofti kontod**.</p><p>Kui olete rakenduse registreerinud kui **Azure AD mitu rentnikku ja isiklikud Microsofti kontod**, ei saa te seda sätet kasutajaliideses (UI) muuta. Selle asemel peate toetatud kontotüüpide muutmiseks kasutama rakenduse manifesti redaktorit.</p> |

    - **Ümbersuunamis-URI (valikuline)** – valige loodava rakenduse tüüp: **veebisait** või **avalik klient (mobiili- ja töölauaga seade)**. Seejärel sisestage rakenduse ümbersuunamis-URI (või vastuse URL).

        - Veebirakenduste jaoks sisestage rakenduse baas-URL. Näiteks võib `http://localhost:31544` olla veebirakenduse URL, mis töötab teie kohalikus masinas. Kasutajad kasutavad seejärel seda URL-i, et logida sisse veebikliendi rakendusse.
        - Avalike kliendirakenduste jaoks sisestage URI, mida Azure AD kasutab loa vastuste tagastamiseks. Sisestage teie rakendusele omane väärtus, nt `myapp://auth`.

        Veebirakenduste või kohalike rakenduste kohta konkreetsete näidete nägemiseks vaadake lühijuhendeid [Microsofti identiteedi platvormil (varem arendajatele suunatud Azure Active Directory)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).

5. Jaotises **API load** valige suvand **Lisa luba**. Seejärel otsige vahekaardil **Minu organisatsiooni kasutatavad API-d** rakendust **Dynamics 365 Human Resources** ja lisage rakendusele luba **kasutaja\_matkimine**. Rakenduse Human Resources ID on f9be0c49-aa22-4ec6-911a-c5da515226ff. Kasutage seda ID-d, et tagada õige rakenduse valimine.

6. Valige suvand **Registreeri**.

   [![Azure’i portaalis uue rakenduse registreerimine](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)

Azure AD määrab rakendusele kordumatu rakenduse ID (kliendi ID) ja viib teid rakenduse lehele **Ülevaade**. Rakendusele täiendavate võimaluste lisamiseks saate valida teisi konfiguratsiooni suvandeid, nagu tootjakohasuse ja sertifikaatide ning saladuste suvandid.

## <a name="retrieving-an-access-token"></a>Juurdepääsuloa toomine

Rakenduse Human Resources andmete API juurdepääsuloa hankimise üksikasjad sõltuvad tehnoloogiatest, mida kliendi rakenduse arendamiseks kasutate. Näiteks võite [testida kolmanda poole utiliidiga](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (nt Postman), arendades C# konsooli rakendust või veebiteenust või luues Javascripti/TypeScripti kliendi.

C# kliendi rakenduse näide.
```C#
using System;
using System.Net.Http;
using System.Threading.Tasks;

// requires appropriate NuGet package references in the project
using Microsoft.IdentityModel.Clients.ActiveDirectory;

namespace TalentODataPoC
{
    class Program
    {
        // prereq: This client app must be registered in Azure Active Directory. The app must be
        // registered as requiring permission to the Dynamics 365 for Talent API (with the Dynamics
        // HCM Workload delegated permission).
        static string clientId = "4fc703ef-672c-4e2c-813f-2f9d29d726db"; // This value should be obtained from AAD and must match your registered app
        static string talentNamespaceUri = "";

        public static async Task CallTalentODataService()
        {
            // authority URI
            UriBuilder uri = new UriBuilder("https://login.microsoftonline.com/common");
            AuthenticationContext authenticationContext = new AuthenticationContext(uri.ToString());

            // request token for the resource we want to access (Human Resources). This will authenticate
            // the user and return an access token containing claims for the authenticated user.
            var authResult = await authenticationContext.AcquireTokenAsync(
                "http://hr.talent.dynamics.com", /*Talent app id or resource URI*/
                clientId, /*registered client app id*/
                new Uri("https://localhost"), /*redirect URI, as registered in your AAD app*/
                new PlatformParameters(PromptBehavior.SelectAccount));

            // create the authorization header, which needs to be passed in the Header of the HTTP Requests to Talent
            string authHeader = authResult.CreateAuthorizationHeader();

            // HINT: paste the JWT into https://jwt.ms to decode and view it
            Console.Write("authHeader: ");
            Console.WriteLine(authHeader);
            Console.WriteLine();

            HttpClient client = new HttpClient();
            client.DefaultRequestHeaders.Add("Authorization", authHeader);

            string s;

            Console.Write("Talent Namespace URI: ");
            Console.WriteLine(talentNamespaceUri);
            Console.WriteLine();

            // call the OData service to get JobType data from Talent
            var resultOdata = await client.GetAsync(talentNamespaceUri + "data/JobTypes");
            s = await resultOdata.Content.ReadAsStringAsync();
            Console.WriteLine(s);
            Console.WriteLine();
        }

        static void Main(string[] args)
        {
            Console.WriteLine();

            // if the user passes in a single parameter, assume it is the namespaceUri for Talent
            if (args.Length == 1)
            {
                talentNamespaceUri = args[0];
            } else if (args.Length == 0)
            {
                Console.WriteLine("Enter Talent URL including namespace.");
                Console.WriteLine("Example: https://aos-rts-sf-21454f9d830-prod-westus2.hr.talent.dynamics.com/namespaces/2328af1a-2d45-4c6a-99e3-12a4c3867dcf/");
                Console.Write("> ");
                talentNamespaceUri = Console.ReadLine();
                if (!talentNamespaceUri.EndsWith("/"))
                {
                    talentNamespaceUri = talentNamespaceUri + "/";
                }
            } else
            {
                Console.WriteLine("Unexpected Arguments");
                System.Environment.Exit(1);
            }

            Task t = Program.CallTalentODataService();
            t.Wait();
        }
    }
}
```

Kui olete juurdepääsuloa juba hankinud, edastate loa autoriseerimise päises vastutaja loana koos iga taotlusega, mille saadate andmete API-le, nagu eespool kirjeldatud.
