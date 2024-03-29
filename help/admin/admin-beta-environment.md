---
description: Betamiljön används för att testa implementeringar av Audience Manager. Ändringar som görs i betaversionen påverkar inte produktionsdata. Audience Manager betamiljön är en mindre, fristående version av produktionsmiljön. Alla data som du vill testa måste anges och samlas in i den här miljön.
seo-description: The beta environment is for testing Audience Manager implementations. Changes made in beta do not affect production data. The Audience Manager beta environment is a smaller-scale, standalone version of the production environment. All the data that you want to test must be entered and collected in this environment.
seo-title: Beta Environment
solution: Audience Manager
title: Beta-miljö
uuid: 6a253f4e-96e7-4395-a783-a8eb213b7daf
exl-id: 78d5a1ff-c016-4366-ba34-9814a0d92067
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 2%

---

# Beta-miljö {#beta-environment}

Betamiljön används för att testa implementeringar av Audience Manager. Ändringar som görs i betaversionen påverkar inte produktionsdata. Audience Manager betamiljön är en mindre, fristående version av produktionsmiljön. Alla data som du vill testa måste anges och samlas in i den här miljön.

## Översikt {#overview}

<!-- beta_environment_admin.xml -->

| Tjänst | URL/värdnamn | Steg för etablering |
|--- |--- |--- |
| S3 |  | Se [Tillhandahåll Amazon S3-buffertar](admin-beta-environment.md#provision-s3-buckets). |
| DCS | /dcs-beta.demdex.net/.. | Inga extra steg behövs från vår sida. Se [Åtkomst till DCS i betamiljön](admin-beta-environment.md#access-dcs-beta-environment). |
| UI | /bank-beta.demdex.com | Data kopieras månadsvis från produktionen till betamiljön. Produktionsautentiseringsuppgifterna är giltiga för betaversion. |
| API | /api-beta.demdex.com/.. | Data kopieras månadsvis från produktionen till betamiljön. Produktionsautentiseringsuppgifterna är giltiga för betaversion. |

## Tillhandahåll Amazon S3-buffertar {#provision-s3-buckets}

>[!NOTE]
>
>Vi går från att använda [!DNL FTP/SFTP]. Observera också att utgående dataöverföringar inte fungerar för betamiljön.

Tillhandahållande [!DNL S3] för inkommande data:

1. Använd [**SKMS Begär hjälp för TechOps**](https://skms.adobe.com/) -funktion.
1. Gå till **[!UICONTROL Request TechOps Help]** till vänster i navigeringsfältet.
1. I **[!UICONTROL Request Search]** skriver du Audience Manager i sökfältet.
1. Bläddra nedåt i sökresultaten och klicka på **Audience Manager - S3 inkommande/utgående kontoetablering**.
1. Fyll i fälten i provisioneringsfönstret och ange **Sandlådemiljö** i **[!UICONTROL Environment]** fält.

>[!NOTE]
>
>Vi uppmuntrar inte till användning av [!DNL FTP/SFTP] och uppmuntra användningen av [!UICONTROL Amazon S3]. Skälen till att vi uppmuntrar användningen av [!UICONTROL Amazon S3] anges i [Amazon CS3:om](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html).

## Åtkomst till DCS i betamiljön {#access-dcs-beta-environment}

Så här öppnar du [!UICONTROL DCS] i betamiljön:

1. Gör en [!UICONTROL DCS] anrop, med [!DNL curl] [kommando](https://curl.haxx.se/docs/manpage.html). [!DNL Curl] är ett verktyg som du kan använda för att överföra data från eller till en server med hjälp av ett av många protokoll som stöds.

   Exempel: `curl -v https://dcs-beta.demdex.net/event`

1. Verifiera att din begäran har hanterats av betaversionen [!UICONTROL DCS] efter &quot;[!DNL sandbox]&quot; i [!UICONTROL DCS] svarshuvud.

   Exempel:

   ```
   curl -v http://dcs-beta.demdex.net/?event
   [...]
   < DCS: va6-sandbox-dcs-3.sandbox.demdex.com <release_number>
   [...]
   ```

<!--
1. Determine the load balancer's endpoint IP addresses.

   Run the `dig` [command](https://en.wikipedia.org/wiki/Dig_(command)) to determine the IP address of the nearest load balancer. The `dig` command queries the Domain Name System and returns the name and IP addresses of the Audience Manager [!UICONTROL Data Collection Servers (DCS)].

   ```
   dig dcs-beta.demdex.net
   ...
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 52.87.15.51
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 50.16.150.8
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 52.2.228.100
   ```

1. Using one of the addresses in the above table, add a static DNS entry in the [!DNL `/etc/hosts`] file.

   On Windows, modify [!DNL `c:\WINDOWS\system32\drivers\etc\hosts`].

   For example:

[!DNL `52.87.15.51 samplepartner.demdex.net`]

   >[!NOTE]
   >
   >The addresses change occasionally, so you must keep your [!DNL /etc/hosts] file up to date.

   Additionally, if you need to set up ID synchronization, you must add a similar entry for [!DNL dpm.demdex.net.]

[!DNL `52.87.15.51 dpm.demdex.net`] [!DNL]. 

1. Make a [!UICONTROL DCS] call, using the `curl` [command](https://curl.haxx.se/docs/manpage.html). Curl is a tool to transfer data from or to a server, using one of many supported protocols.

   For example:

[!DNL `https://<domain>/event?product=camera`] 

1. Verify that your request was served by the beta [!UICONTROL DCS] by looking for "sandbox" in the [!UICONTROL DCS] response header.

   For example:

   ```
   curl -v https://dcs-beta.demdex.net/?event
   [...]
   < DCS: va6-sandbox-dcs-3.sandbox.demdex.com <release_number>
   [...]
   ```
-->
